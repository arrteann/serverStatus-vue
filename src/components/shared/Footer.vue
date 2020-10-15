<template>
    <footer>
        <p>&copy; NOBODY</p>
    </footer>
</template>

<script>
export default {
    name:'app-footer'
}
</script>


<style lang="scss" scoped>
    footer{
        width: auto;
        background: #323232;
        padding: 5px 10px;
        text-align: center;
        border-radius: 5px;
        display: flex;
        align-items: center;
        justify-content: center;
        p{
            font-weight: 300;
            font-size: .8rem;
            text-transform: uppercase;
            color: white;

        }
        align-self: end;
    }
</style>