<template>
    <div>
        <footer>
            <p>CIMOL &copy;2022</p>
        </footer>
    </div>
</template>

<script>
export default{
    name:"Footer"
}
</script>

<style scoped>
    footer{
            height:150px;
            background-color:#c2c2c2;
            border-top:4px solid #c1c1c1;
            color:#111;
            display:flex;
            align-items: center;
            justify-content:center;
            width:100%;
        }
    footer p{
        background-color:transparent;
    }
</style>