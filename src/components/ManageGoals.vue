<template>
  <div>
    <h2>Manage Goals</h2>
    <input type="text" v-model="enteredValue" />
    <button @click="setGoal">Set Goal</button>

    <error-alert v-if="inputIsInvalid">
      <h2>Input is invalid!</h2>
      <p>Please enter at least 2 characters...</p>
      <button @click="confirmError">Okay</button>
    </error-alert>
  </div>
</template>

<script>
import ErrorAlert from "./ErrorAlert.vue";

export default {
  components: { ErrorAlert },
  data() {
    return {
      enteredValue: "",
      inputIsInvalid: false
    };
  },
  methods: {
    setGoal() {
      if (!this.enteredValue || this.enteredValue.trim().length < 2) {
        this.inputIsInvalid = true;
        return;
      }
      this.inputIsInvalid = false;
      // handle your new goal here...
      this.enteredValue = "";
    },
    confirmError(){
      this.inputIsInvalid = false;
    }
  }
};
</script>
