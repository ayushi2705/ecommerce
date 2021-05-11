<template>
    <div class="vue-tempalte">
        <form>
            <h3>Sign In</h3>

            <div class="form-group">
                <label>Email address</label>
                <input type="email" class="form-control form-control-lg" />
            </div>

            <div class="form-group">
                <label>Password</label>
                <input type="password" class="form-control form-control-lg" />
            </div>

            <div class = "button-block">
                <button type="submit" class="button is-dark">Sign In</button>
            </div>

        </form>
    </div>
</template>

<script>
    export default {
        data() {
            return {}
        }
    }
</script>

<style scoped>
    .vue-tempalte {
        width: 500px;
        border: 1px solid #CCCCCC;
        margin: auto;
        margin-top: 50px;
        padding: 20px;
    }

    h3 {
    text-align: center;
    margin: 0;
    line-height: 1;
    padding-bottom: 20px;
    font-weight: bold;
    }

    label{
        margin-top: 40px;
        font-weight: 500;
        font-weight: bold;
    }
    .button-block {
    text-align: center;
    margin-left: auto;
    margin-right: auto;
    margin-top: 40px;
    }

    button{
         font-weight: bold;
         color: #2c3e50;
    }

</style>