<script>
export default {
  name: "CountryComponent",
  props: [
    "name",
    "capital",
    "currency_name",
    "currency",
    "region",
    "code",
    "iso 2",
    "iso 3",
    "numeric code"
    //TODO: crear una propiedad para determinar si al componente se le puede hacer click
  ],
};
</script>

<template>
  <!--TODO: Utilizar la propiedad creada para controlar el click. Cuando el componente es "clickeable", redirigir a la pagina del pais.
  Mira las rutas para ver como redirigir al usuario.-->
  <div class="country">
  <!--TODO: Poblar el HTML con las propiedades. Usar https://countryflagsapi.com/png/${code}-->
    <img width="200" height="200" :src="img" />
    <h1>{{ name }}</h1>
    <h2>{{ capital }}</h2>
    <h3>{{ currency_name }}</h3>
    <h4>{{ currency }}</h4>
    <h5>{{ region }}</h5>
    <h6>{{ code }}</h6>
  <img
      width="200"
      height="200"
    />
  </div>
</template>

<style scoped>
.country {
  padding: 2px;
  white-space: nowrap;
  width: 350px;
  height: 350px;
  border-style: solid;
  border-radius: 5px;
  border-color: grey;
}

.country-hover:hover {
  background-color: rgb(49, 49, 49);
  cursor: pointer;
}

h1 {
  overflow: hidden;
  text-overflow: ellipsis;
}
</style>
