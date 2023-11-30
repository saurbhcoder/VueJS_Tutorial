<template>
  {{ formValues }}
  <form @submit="submitForm">
    <div>
      <label for="name">Name</label>
      <input id="name" name="name" v-model="formValues.name">
    </div>

    <div>
      <label for="name">profileSummery</label>
      <textarea id="profileSummery" name="profileSummery" v-model="formValues.profileSummery"></textarea>
    </div>

    <div>
      <label for="country">Country</label>
      <select id="country" name="country" v-model="formValues.country">
        <option>Select Country</option>
        <option>india 1</option>
        <option>india 2</option>
        <option>india 3</option>
      </select>
    </div>
    <div>
      <label for="country">jobLocation</label>
      <select id="jobLocation" name="jobLocation" multiple v-model="formValues.jobLocation">
        <option>Select jobLocation</option>
        <option>jobLocation 1</option>
        <option>jobLocation 2</option>
        <option>jobLocation 3</option>
      </select>
    </div>


    <div>
      <input type="checkbox" v-model="formValues.remoteWork" true-value="yes" false-value="no" />
      <label for="country">Remote Work</label>
    </div>


    <div>
      <label for="country">Skill Set</label>
      <input type="checkbox" id="html" value="html" v-model="formValues.skillSet"/><label for="html">html</label>
      <input type="checkbox" id="css" value="css" v-model="formValues.skillSet"/><label for="css">css</label>
      <input type="checkbox" id="vue" value="vue" v-model="formValues.skillSet"/><label for="vue">vue</label>
    </div>


    <div>
      <label for="country">Year of experince</label>
      <input
      type="radio"
      id="0-2"
      value="0-2"
      v-model="formValues.exp"/><label for="">0-2</label>
      <input
      type="radio"
      id="3-4"
      value="3-4"
      v-model="formValues.exp"/><label for="">3-4</label>
      
    </div>

    <input type="submit" value="submit">
  </form>
</template>
<script>
export default {
  name: "App",
  data() {
    return {
      formValues : {
        name : '',
        profileSummery : '',
        country : '',
        jobLocation : [],
        remoteWork : 'no',
        skillSet : [],
        exp : [],
      },
    }
  },
  methods : {
    submitForm(event){
      event.preventDefault();
      console.log(this.formValues);
    }
  }
};
</script>
<style></style>
