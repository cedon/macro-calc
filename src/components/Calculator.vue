<template>
  <div>
    <form @submit.prevent="onSubmit">
      <label for="sex">Sex:</label>
      <select id="sex" name="sex">
        <option value="male">Male</option>
        <option value="female">Female</option>
      </select>
      <label for="weight">Weight:</label>
      <input id="weight" type="number" name="weight" required="required"/>
      <label for="weightUnits">Units:</label>
      <select id="weightUnits" name="weightUnits">
        <option value="pounds">Pounds</option>
        <option valus="kilograms">Kilograms</option>
      </select>
      <label for="bodyFat">Body Fat %:</label>
      <input id="bodyFat" type="number" name="bodyFat" required="required"/>
      <button>Submit</button>
    </form>
    <section>
      <Results />
    </section>
  </div>
</template>

<script>
import Results from '@/components/Results'

export default {
  name: 'Calculator',
  components: {
    Results
  },
  data () {
    return {
      calc: {}
    }
  },
  methods: {
    onSubmit () {
      console.log('The Form was Submitted')
    }
  }
}
</script>

<style scoped>

</style>
