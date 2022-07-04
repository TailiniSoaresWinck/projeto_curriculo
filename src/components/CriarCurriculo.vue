<template>
    <div>
    <h2>Crie seu Currículo</h2>
        <div>
            <form id="form-curriculo"  @submit="createCurriculo">
                    <h4>Dados Pessoais</h4>
                <div class="input-container">
                    <label for="nome">Nome:</label>
                     <div>
                        <input type="text" name="nome" id="nome" placeholder="Digite seu nome" v-model="nome"/>
                    </div>
                    <label for="email">Emai:</label>
                     <div>
                        <input type="email" name="email" id="email" placeholder="Digite seu email" v-model="email"/>
                    </div>
                    <label for="telefone">Telefone:</label>
                     <div>
                        <input type="text" name="telefone" id="telefone" placeholder="Digite seu número de telefone" v-model="telefone"/>
                    </div>
                </div>
                    <h4>Objetivo Profissional</h4>
                <div class="input-container">
                    <label for="objetivo">Objetivo:</label>
                    <div>
                        <textarea  name="objetivo" id="objetivo" placeholder="Digite seu objetivo profissional" rows="4" v-model="objetivo"></textarea>
                    </div>
                </div>
                    <h4>Formação</h4>
                <div class="input-container">
                    <label for="instituicao">Instituição:</label>
                    <div>
                        <input type="text" name="instituicao" id="instituicao" placeholder="Digite o nome da instituição" v-model="instituicao"/>
                    </div>
                    <label for="curso">Curso:</label>
                    <div>
                        <input type="text" name="curso" id="curso" placeholder="Digite o curso de formação" v-model="curso"/>
                    </div>
                    <label for="ano">Mês e Ano de Formação:</label>
                    <div>
                        <input type="month" name="MesAno" id="MesAno" v-model="mesAno"/>
                    </div>
                    <label for="nivelEscolar">Nível Escolar:</label>
                    <div>
                         <select name="nivelEscolar" id="nivelEscolar" v-model="nivelEscolar">
                            <option value="">Selecione o nível</option>
                            <option value="Medio/Técnico">Médio/Técnico</option>
                            <option value="Técnico">Técnico</option>
                            <option value="Superior">Superior</option>
                            <option value="Especialização">Especialização</option>
                            <option value="Mestrado">Mestrado</option>
                            <option value="Doutorado">Doutorado</option>
                            <option value="PHD">PHD</option>
                        </select>
                    </div>
                </div>
                    <h4>Última Experiência</h4>
                <div class="input-container">
                    <label for="empresa">Empresa:</label>
                    <div>
                         <input type="text" name="empresa" id="empresa" placeholder="Digite o nome da empresa" v-model="empresa"/>
                    </div>
                    <label for="cargo">Cargo:</label>
                    <div>
                        <input type="text" name="cargo" id="cargo" placeholder="Digite o cargo" v-model="cargo"/>
                    </div>
                    <label for="admissao">Data de Admissão:</label>
                    <div>
                        <input type="date" name="admissao" id="admissao" v-model="admissao"/>
                    </div>
                    <label for="saida">Data de Saída:</label>
                    <div>
                        <input type="date" name="saida" id="saida" v-model="saida"/>
                    </div>
                </div>
                    <h4>Idiomas</h4>
                <div class="input-container">
                    <label for="idioma">Idioma:</label>
                    <div>
                        <input type="text" name="idioma" id="idioma" placeholder="Digite o idioma" v-model="idioma"/>
                    </div>
                    <label for="nivelIdioma">Nível Idioma:</label>
                    <div>
                        <select name="nivelIdioma" id="nivelIdioma" v-model="nivelIdioma">
                            <option value="">Selecione o nível</option>
                            <option value="Basico">Básico</option>
                            <option value="Intermediario">Intermediário</option>
                            <option value="Bom">Bom</option>
                            <option value="Excelente">Excelente</option>
                        </select>
                    </div>
                </div>
                    <h4>Curso de Qualificação</h4>
                <div class="input-container">
                    <label for="curso">Curso:</label>
                    <div>
                        <input type="text" name="curso" id="curso" placeholder="Digite o curso" v-model="cursoQualificacao"/>
                    </div>
                    <label for="duracao">Duração:</label>
                    <div>
                        <input type="number" name="duracao" id="duracao" placeholder="Horas" v-model="duracao"/>
                    </div>
                </div>
                <div class="input-btn">
                    <button type="submit" id="btn-criar">Criar</button>
                </div>
            </form>
            <div class="input-btn">
                <button type="button" id="btn-voltar" @click="voltar">Voltar</button>
                <button type="button" id="btn-limpar"  @click="limpar">Limpar</button>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name:"CriarCurriculo",
    props:{
        curriculo_cadastrado:Boolean
    },

    data(){
        return{
            nome:null,
            email:null,
            telefone:null,
            objetivo:null,
            instituicao:null,
            curso:null,
            mesAno:null,
            nivelEscolar:null,
            empresa:null,
            cargo:null,
            admissao:null,
            saida:null,
            idioma:null,
            nivelIdioma:null,
            cursoQualificacao:null,
            duracao:null
        }
    },
    methods:{
        async createCurriculo(e){
            e.preventDefault();
            const data={
                dadosPessoais:Array.from(
                    [   Nome=this.nome,
                        Email= this.email,
                        Telefone=this.telefone
                    ]),
                objetivo:Array.from([Objetivo=this.objetivo]),
                formacao:Array.from([
                    Instituição=this.instituicao, 
                    Curso=this.curso,
                    MêsAno=this.mesAno, 
                    NívelEscolar=this.nivelEscolar
                    ]),
                experiencia:Array.from([
                    Empresa=this.empresa, 
                    Cargo=this.cargo,
                    DataAdmissao=this.admissao,
                    DataSaida=this.saida
                    ]),
                idioma:Array.from([
                    Idioma=this.idioma, 
                    NivelIdioma=this.nivelIdioma
                    ]),
                cursoQualificacao:Array.from([
                    Curso=this.cursoQualificacao,
                    Duracao=this.duracao
                    ])

                    
               
            }
         
                const dataJson = JSON.stringify(data)   
                const req = await fetch("http://localhost:3000/curriculo", {
                method: "POST", 
                headers: { "Content-Type" : "application/json" },
                body: dataJson
                })

                const res = await req.json()
                console.log(res)
        },
        limpar(){
            this.nome='',
            this.email='',
            this.telefone='',
            this.objetivo='',
            this.instituicao='',
            this.curso='',
            this.mesAno='',
            this.nivelEscolar='',
            this.empresa='',
            this.cargo='',
            this.admissao='',
            this.saida='',
            this.idioma='',
            this.nivelIdioma='',
            this.cursoQualificacao='',
            this.duracao=''
        },
        voltar(){
            this.$router.replace("/")
        }
    }
}
</script>
    
<style scoped>
    #form-curriculo{
        margin:0 auto;
        max-width:600px;
    }
    .input-container{
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
    .input-container div{
        background-color:transparent;
        align-items:center;
        display:flex;
        flex-direction: column;
    }
    textarea, input, select{
        cursor:pointer;
        width:500px;
        padding:8px 10px;
        margin-bottom:20px;
        border-radius:10px;
    }
    .input-btn{
        justify-content:center;
        display:flex;
        margin-bottom:20px;
    }
    #btn-voltar,#btn-criar,#btn-limpar{
        padding: 10px 15px;
        border-radius:10px;
        margin:15px;
        cursor:pointer;
        transition:.5s;
    }
    #btn-voltar,#btn-criar{
        background-color:#2062AD;
        color:#FFF;
        border: 2px solid #2062AD;
    }
    #btn-limpar{
        background-color:#F29138;
        color:#FFF;
        border: 2px solid #F29138;
    }
    #btn-voltar:hover,#btn-criar:hover, #btn-limpar:hover{
        background-color:transparent;
        color:#222;

    }
</style>