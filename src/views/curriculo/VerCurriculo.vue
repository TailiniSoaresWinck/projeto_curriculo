<template>
    <div>
    <h2>Currículo</h2>
        <div id="Curriculo">
                    <h4>Dados Pessoais</h4>
                <div class="dados-container">
                    <label for="nome">Nome:</label>
                    <label for="email">Emai:</label>
                    <label for="telefone">Telefone:</label>
                </div>
                    <h4>Objetivo Profissional</h4>
                <div class="dados-container">
                    <label for="objetivo">Objetivo:</label>
                    <div>
                       <p>{{objetivo}}</p>
                    </div>
                </div>
                    <h4>Formação</h4>
                <div class="dados-container">
                    <label for="instituicao">Instituição:</label>
                    <div>
                        <p>{{instituição}}</p>
                    </div>
                    <label for="curso">Curso:</label>
                    <div>
                       <p>{{cursoFormaçao}}</p>
                    </div>
                    <label for="ano">Mês e Ano de Formação:</label>
                    <div>
                        <p>{{mesAnoFormação}}</p>
                    </div>
                    <label for="nivelEscolar">Nível Escolar:</label>
                    <div>
                         <p>{{nivelEscolar}}</p>
                    </div>
                </div>
                    <h4>Experiência</h4>
                <div class="dados-container">
                    <label for="empresa">Empresa:</label>
                    <div>
                         <p>{{empresa}}</p>
                    </div>
                    <label for="cargo">Cargo:</label>
                    <div>
                        <p>{{cargo}}</p>
                    </div>
                    <label for="admissao">Data de Admissão:</label>
                    <div>
                        <p>{{dataAdmissao}}</p>
                    </div>
                    <label for="saida">Data de Saída:</label>
                    <div>
                        <p>{{dataSaida}}</p>
                    </div>
                </div>
                    <h4>Idiomas</h4>
                <div class="dados-container">
                    <label for="idioma">Idioma:</label>
                    <div>
                        <p>{{idioma}}</p>
                    </div>
                    <label for="nivelIdioma">Nível Idioma:</label>
                    <div>
                        <p>{{nivelIdioma}}</p>
                    </div>
                </div>
                    <h4>Cursos de Qualificação</h4>
                <div class="dados-container">
                    <label for="curso">Curso:</label>
                    <div>
                        <p>{{curso}}</p>
                    </div>
                    <label for="duracao">Duração:</label>
                    <div>
                        {{duração}}
                    </div>
                </div>
                <div class="input-btn">
                    <button type="submit" id="btn-editar" >Editar</button>
                    <button type="submit" id="btn-excluir" >Excluir</button>
                </div>
        </div>
    </div>
</template>

<script>
export default {
    name:"VerCurriculo"
}
</script>

<style scoped>
    #Curriculo{
        margin:0 auto;
        max-width:600px;
    }
    .dados-container{
        background-color: #e7e7e7;
        border-radius:0 0 20px 20px;
        display:flex;
        flex-direction: column;
        margin-bottom:20px;
    }
    h4{
        border-radius:20px 20px 0 0;
        background-color: #c7c7c7;
        padding:10px 20px;
    }
    label{
        margin-left:10px;
        padding:5px 10px;
        background-color:transparent;
        border-left:4px solid #FCBA03;
        margin-top:15px;
        margin-bottom:15px;
        color:#222;
    }
    .dados-container div{
        background-color:transparent;
        align-items:center;
        display:flex;
        flex-direction: column;
    }
    .input-btn{
        justify-content:center;
        display:flex;
        margin-bottom:20px;
    }
    #btn-editar,#btn-excluir{
        padding: 10px 15px;
        border-radius:10px;
        margin:15px;
        cursor:pointer;
        transition:.5s;
    }
    #btn-editar{
        background-color:#2062AD;
        color:#FFF;
        border: 2px solid #2062AD;
    }
    #btn-excluir{
        background-color:#F29138;
        color:#FFF;
        border: 2px solid #F29138;
    }
    #btn-editar:hover, #btn-excluir:hover{
        background-color:transparent;
        color:#222;

    }
</style>