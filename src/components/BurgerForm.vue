<template>
    <div>
        <p>Componente de Mensagem</p>
        <div>
            <form id="burguer-form">
                <div class="input-container">
                    <label for="nome">Nome do Cliente</label>
                    <input type="text" id="nome" name="nome" 
                    v-model="nome" placeholder="Digite o seu nome:">
                </div>
                <div class="input-container">
                    <label for="pao">Escolha o pão:</label>
                    <select name="pao" id="pao" v-model="pao">
                        <option value="">Selecione o seu pão</option>
                        <option value="integral">integral</option>
                        <option value="3queijos">3 Queijos</option>
                        <option value="DaCasa">Da Casa</option>
                    </select>
                </div>
                <div class="input-container">
                    <label for="carne">Escolha a carne:</label>
                    <select name="carne" id="carne" v-model="carne">
                        <option value="">Selecione o tipe de carne</option>
                        <option value="picanha">Picanha</option>
                        <option value="maminha">Maminha</option>
                        <option value="DaCasa">Da Casa</option>
                    </select>
                </div>
                <div class="input-container">
                    <label id="opcionais-title" for="opcionais">Escolha os opcionais:</label>
                    <div class="checkbox-container">
                        <input type="checkbox" name="opcionais" v-model="opcionais" value="salame">
                        <span>Salame</span><br>
                        <input type="checkbox" name="opcionais" v-model="opcionais" value="tomate">
                        <span>Tomate</span><br>
                        <input type="checkbox" name="opcionais" v-model="opcionais" value="alface">
                        <span>Alface</span><br>
                    </div>
                    <div class="input-container">
                        <input type="submit" class="submit-btn" value="Criar">
                    </div>
                </div>
            </form>
        </div>
    </div>
</template>
<script>
export default {
    name: "BurgerForm"
}
</script>
<style scoped>
    #burger-form {
        max-width: 400px;
        margin: 0 auto;
    }

    .input-container {
        display: flex;
        flex-direction: column;
        margin-bottom: 20px;
    }

    label{
        font-weight: bold;
        margin-bottom: 15px;
        color: #222;
        padding: 5px 10px;
        border-left: 4px solid #FCBA03;
    }

    input, select {
        padding: 5px 10px;
        width: 300px;
    }

    #opcionais-container {
        flex-direction: row;
        flex-wrap: wrap;
    }

    #opcionais-title {
        display: flex;
        align-items: flex-start;
        width: 50%;
        margin-bottom: 20px;
    }
</style>