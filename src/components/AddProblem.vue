<script>
    export default {
        data() {
            return {
                input: false
            }
        },
        methods: {
            showInput: function() {
                this.input = !this.input
            }
        }
    }
</script>

<template>
  <div class="addBlock">
    <div class="AddProblem">
        <a href="#" class="textAdd" @click="showInput()"><img src="../assets/img/icon_plus.png" alt="">Добавить задачу</a>
        <input v-if="input" type="text" class="inputAdd">
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
  margin: 5%;
}

.addProblem {
    display: flex;
    line-height: normal;
    margin: 0 auto;
    justify-content: center;
    flex-direction: column;
}

.textAdd {
    display: flex;
    margin: 0 auto;
    font-weight: 400;
    font-size: 24px;
    line-height: normal;
    text-decoration: none;
    color: white;
}

.inputAdd {
    text-align: center;
    margin-left: auto;
    width: 90%;
}

</style>
