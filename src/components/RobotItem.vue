<template>
      <div class="robot" :class="robot.gender">
        <h4 class="robot__title">
          {{robot.first_name}}
          <strong>{{robot.last_name}}</strong>
        </h4>
        <div class="robot__portrait" :class="robot.gender">
          <img :src="robot.portrait" :class="robot.gender" alt>
          <p class="robot__portrait__type">
            <strong>Type</strong>
            : {{robot.type}}
          </p>
          <p class="robot__portrait__language">
            <strong>Langue parlée</strong> :
            <br>
            {{robot.language}}
          </p>
        </div>
        <p class="robot__description">{{robot.description}}</p>
      </div>
</template>

<script>
export default {
// propriétés passables à mon composant
  props: [
    // "first_name",
    // "last_name",
    // "portrait",
    // "type",
    // "language",
    // "description",
    // "gender",
    "robot",
  ] 
};
</script>

<style>
</style>
