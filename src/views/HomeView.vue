<template>
  <div class="container">
    <div class="home">
      <header>
        <h1>Librería Vuevill</h1>
      </header>

      <section>
        <h2>Bienvenido a Vuevill</h2>
        <p>
          En nuestra librería, encontrarás una gran variedad de libros
          literarios de diferentes géneros, así como libros científicos que
          abarcan múltiples áreas del área tecnologica, tanto en formato físico
          como digital. Además, contamos con obras de autores reconocidos y
          emergentes, para que puedas descubrir nuevos talentos y explotar los
          que ya tienes, así como para que puedas pasar de una tarde agradable
          sumergido en un mundo de fantasía o lleno de acción.
        </p>
        <img
          src="https://via.placeholder.com/300x200"
          alt="Libros en una estantería"
        />
        <p>
          NOTA: De momento las imágenes y la información de los libros no 
          están disponibles puesto que esto se realizará en la segunda parte 
          del proyecto cuando se implemente el backend
        </p>
      </section>

      <section>
        <h2>Novedades</h2>
        <ul>
          <li>
            <a href="#">
              <img
                src="https://via.placeholder.com/150x200"
                alt="Portada de 'La Casa de Papel'"
              />
              <br />
              "La Casa de Papel"</a
            >
            de Javier Gómez Santander
          </li>
          <li>
            <a href="#">
              <img
                src="https://via.placeholder.com/150x200"
                alt="Portada de '1984'"
              />
              <br />
              "Fórmulas y funciones matemáticas con Excel"</a
            >
            de Axel Zaldivar
          </li>
          <li>
            <a href="#">
              <img
                src="https://via.placeholder.com/150x200"
                alt="Portada de 'Los Pilares de la Tierra'"
              />
              <br />
              "Los Pilares de la Tierra"</a
            >
            de Ken Follett
          </li>
          <li>
            <a href="#">
              <img
                src="https://via.placeholder.com/150x200"
                alt="Portada de 'El Laberinto de los Espíritus'"
              />
              <br />
              "El Laberinto de los Espíritus"</a
            >
            de Carlos Ruiz Zafón
          </li>
        </ul>
      </section>

      <section>
        <h2>Lo más vendido</h2>
        <ul>
          <li>
            <a href="#">
              <img
                src="https://via.placeholder.com/150x200"
                alt="Portada de 'El Código Da Vinci'"
              />
              <br />
              "El Código Da Vinci"</a
            >
            de Dan Brown
          </li>
          <li>
            <a href="#">
              <img
                src="https://via.placeholder.com/150x200"
                alt="Portada de 'Cien años de soledad'"
              />
              <br />
              "Cien años de soledad"</a
            >
            de Gabriel García Márquez
          </li>
        </ul>
      </section>
    </div>
  </div>
</template>

<script>
export default {
  name: "HomeView",
  components: {},
};
</script>

<style>
/* Fuentes */
@import url("https://fonts.googleapis.com/css2?family=Montserrat:wght@400;600&display=swap");
@import url("https://fonts.googleapis.com/css2?family=Open+Sans&display=swap");

.home {
  margin: 0;
  font-family: "Open Sans", sans-serif;
  font-size: 16px;
  line-height: 1.5;
  background-color: #f8f8f8;
}

.home h1,
.home h2 {
  margin: 0;
  font-family: "Montserrat", sans-serif;
  font-weight: 600;
  text-transform: uppercase;
}

.home header {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 80px;
  color: #fff;
  background-color: #41b883;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
  padding: 20px;
}

.home h1 {
  font-size: 36px;
  text-align: center;
  color: #fff;
}

.home section {
  margin: 10px;
  padding: 20px;
}

.home section h2 {
  font-size: 24px;
  margin-bottom: 20px;
  color: #333;
}

.home section p {
  margin-bottom: 20px;
  color: gray;
}

.home section ul {
  display: flex;
  flex-wrap: wrap;
  justify-content: space-between;
}

.home section li {
  width: calc(50% - 10px);
  margin-bottom: 20px;
  background-color: #fff;
  border-radius: 5px;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
  padding: 20px;
  transition: all 0.3s ease-in-out;
  text-align: center;
}

.home section li a {
  display: flex;
  flex-direction: column;
  align-items: center;
  text-align: center;
  color: #333;
  text-decoration: none;
}

.home section li:hover {
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
  transform: translateY(-5px);
}

.home section li a:hover {
  text-decoration: underline;
}

.home section li img {
  margin-bottom: 10px;
}

.home section li span {
  font-size: 1.2rem;
  margin-top: 10px;
  font-style: italic;
}
</style>
