<template>
<div>
    <h2>Como Funciona?</h2>
    <div id="paragrafos">
        <p>
        Utilize este setor, para <strong>criar</strong> e <strong>atualizar</strong> seu currículo, 
        dessa forma você terá a oportunidade de ser selecionado 
        para entrevistas de empregos.
        </p>
        <p>
        Salientamos que após cadastro de seu currículo, 
        haja <strong>atualizações</strong> para que você não perca oportunidades!
        </p>
    </div>
</div>
</template>

<script>
export default {
    name:"ComoFunciona"
}
</script>

<style scoped>
    #paragrafos{
        max-width:600px;
        margin:0 auto;
    }
    #paragrafos p{
        text-align:justify;
        margin-bottom:40px;
        font-size:18px;
        line-height:2;
        color:#222;
    }
</style>