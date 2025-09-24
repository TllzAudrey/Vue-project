<script setup>
const template = `
  <div class="report">
    <h1>{{project}}</h1>
    <h2>fait par : {{name}}</h2>
    <p>{{text}}</p>
  </div>
`;
// mettre en lien la reponse dans app.vue et object
const object = {
  project: "",
  name: "",
  text: "",
};
const compiledTemplate = Handlebars.compile(template);
const html = compiledTemplate(data);

</script>