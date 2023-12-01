<script>
    import { ref } from 'vue'

    export default {
        data() {
            return {
                input: false,
                addProblem: false  
            }
        },
        methods: {
            showInput: function() {
                this.input = !this.input
            },
            showAdd: function() {
                this.addProblem = !this.addProblem
            }
        }
    }
</script>

<template>
  <div class="addBlock">
    <div class="AddProblem">
        <a href="#" class="textAdd" @click="showInput()"><img src="../assets/img/icon_plus.png" alt="" class="iconPlus">Добавить задачу</a>
        <input  v-model="AddName" v-if="input" type="text" class="inputAdd"  placeholder="Название задачи">
        <button v-if="input" class="btn-add" type="button" @click="showAdd">Добавить</button>
        <p class="AddName">1.{{ AddName }}</p>
    </div>
  </div>
</template>

<style scoped>
.addBlock {
  height: 80vh;  
  width: 40%;
  background-color: #855DD9;
  border-radius: 10px;
  display: flex;
  flex-direction: row;
  justify-content: center;
    margin: 3% 4%;
}

.addProblem {
    display: flex;
    line-height: normal;
    justify-content: center;
    flex-direction: column;
    width: 100%;
    text-align: center;
}

.textAdd {
    display: flex;
    margin: 3% auto;
    font-weight: 400;
    font-size: 24px;
    line-height: normal;
    text-decoration: none;
    color: white;
    align-items: center;
}

.iconPlus:hover {
    transform: rotate(180deg);
    transition: 0.5s;
}

.inputAdd {
    width: 100%;
    left: 5%;
    height: 7vh;
    border-radius: 10px;
    box-shadow: none;
    border: none;
    font-size: large;
}

.btn-add {
    margin: 2% auto;
    width: 100%;
    height: 5vh;
    border: none;
    border-radius: 10px;
    background-color: #4D12C9;
    color: #fff;
    cursor: pointer;
}

.AddName {
    color: #fff;
}
</style>
