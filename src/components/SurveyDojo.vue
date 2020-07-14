<template>
  <div class="container">
    <form action="" method="POST">
      <div class="survey-title">
        <h1>{{ msg }}</h1>
      </div>
      <div class="survey-name">
        <p>Enter your name: <input type="text" v-model="name"></p>
      </div>
      <div class="survey-location">
        <p>Select your Dojo Location:
          <select v-model="location">
            <option disabled value="">Select your Dojo Location:</option>
            <option value="arlington">Arlington</option>
            <option value="boise">Boise</option>
            <option value="chicago">Chicago</option>
            <option value="dallas">Dallas</option>
            <option value="losangeles">Los Angeles</option>
            <option value="online">Online</option>
            <option value="orangecounty">Orange County</option>
            <option value="sanfrancisco">San Francisco</option>
            <option value="seattle">Seattle</option>
            <option value="siliconvaley">Silicon Valley</option>
            <option value="tulsa">Tulsa</option>
          </select>
        </p>
      </div>
      <div class="survey-framework">
        <p>Select your framework/s:
          <input type="checkbox" value="Angular" v-model="framework">
          <label for="angular">Angular</label>
          <input type="checkbox" value="React" v-model="framework">
          <label for="react">React</label>
          <input type="checkbox" value="Vue" v-model="framework">
          <label for="vue">Vue</label>
        </p>
      </div>
      <div class="survey-comments">
        <p>Please write any comments: <br><textarea v-model="comments"></textarea></p>
      </div>
      <div class="survey-submit">
        <p><input type="submit" v-on:click="submit"></p>
      </div>
    </form>
  </div>
</template>

<script>
export default {
    name: "SurveyDojo",
    props: {
    msg: String
    },
    data: function() {
        return {
            name: '',
            location: 0,
            framework: [],
            comments: ''
        };
    },
    methods: {
      submit: function(ev) {
        ev.preventDefault();
        alert("Survey sent! Thanks for answering")
      }
    }
}
</script>

<style scoped>
h1 {
  margin: 20px 0 0;
  font-size: 24px;
}
.container {
  border: 1px solid black;
  width: 600px;
  margin: 10px;
}
.survey-name input {
  width: 240px;
}
textarea {
  width: 400px;
  height: 80px;
}
</style>