<template>
  <div id="app">
    <div class="container">
      <h2>Agregar nuevo libro</h2>
      <form class="f">
        <!--ISBN-->
        <div class="container">
          <div class="row">
            <div class="col-xs-2 ml-auto mt-auto mb-auto">
              <img src="../components/assets/barras.png" class="search" />
            </div>
            <div class="col-xs-6 mr-auto mt-auto mb-auto">
              <input
                class="form-control"
                placeholder="ISBN"
                v-model="isbn"
                type="number"
              /><br />
            </div>
          </div>
        </div>

        <!--Titulo-->
        <div class="container">
          <div class="row">
            <div class="col-xs-2 ml-auto mt-auto mb-auto">
              <img src="../components/assets/portada.png" class="search" />
            </div>
            <div class="col-xs-6 mr-auto mt-auto mb-auto">
              <input
                class="form-control"
                placeholder="Título"
                v-model="title"
              /><br />
            </div>
          </div>
        </div>

        <!--Año-->
        <div class="container">
          <div class="row">
            <div class="col-xs-2 ml-auto mt-auto mb-auto">
              <img src="../components/assets/calendario.png" class="search" />
            </div>
            <div class="col-xs-6 mr-auto mt-auto mb-auto">
              <input
                class="form-control"
                placeholder="Año de publicación"
                v-model="year"
                type="number"
              /><br />
            </div>
          </div>
        </div>

        <!--Genero-->
        <div class="container">
          <div class="row">
            <div class="col-xs-2 ml-auto mt-auto mb-auto">
              <img src="../components/assets/genero.jpg" class="search" />
            </div>
            <div class="col-xs-6 mr-auto mt-auto mb-auto">
              <input
                class="form-control"
                placeholder="Género"
                v-model="gender"
              /><br />
            </div>
          </div>
        </div>

        <!--Autor-->
        <div class="container">
          <div class="row">
            <div class="col-xs-2 ml-auto mt-auto mb-auto">
              <img src="../components/assets/monito.png" class="search" />
            </div>
            <div class="col-xs-6 mr-auto mt-auto mb-auto">
              <input
                class="form-control"
                placeholder="Autor"
                v-model="author"
              /><br />
            </div>
          </div>
        </div>

        <!--Descripcion-->
        <div class="container">
          <div class="row">
            <div class="col-xs-2 ml-auto mt-auto mb-auto">
              <img src="../components/assets/txt.png" class="search" />
            </div>
            <div class="col-xs-6 mr-auto mt-auto mb-auto">
              <input
                class="form-control"
                placeholder="Descripción breve"
                v-model="desc"
              /><br />
            </div>
          </div>
        </div>

        <span class="input-group-btn">
          <button
            class="btn btn-primary"
            type="submit"
            @click="search()"
            :disabled="
              !isbnIsValid ||
              !titleIsValid ||
              !genderIsValid ||
              !authorIsValid ||
              !descIsValid
            "
          >
            <i class="fa fa-save"></i>
            Añadir
          </button>
        </span>

        <div class="container book" v-if="isEdited">
          <h2>Título</h2>
          <img src="https://via.placeholder.com/150x200" alt="portada" />
          <h6>ISBN:</h6>
          <p>Autor:</p>
          <p>Año de publicación:</p>
          <p>Género:</p>
          <p>Descripción:</p>
        </div>
      </form>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      isbn: null,
      title: null,
      year: null,
      gender: null,
      author: null,
      desc: null,
      isEdited: false,
    };
  },

  name: "New",

  methods: {
    search() {
      this.isEdited = true;
    },
  },

  computed: {
    isbnIsValid() {
      return !!this.isbn;
    },
    titleIsValid() {
      return !!this.title;
    },
    yearIsValid() {
      return !!this.year;
    },
    genderIsValid() {
      return !!this.gender;
    },
    authorIsValid() {
      return !!this.author;
    },
    descIsValid() {
      return !!this.desc;
    },
  },
};
</script>

<style>
@import url(https://stackpath.bootstrapcdn.com/bootstrap/4.1.0/css/bootstrap.min.css);
@import url(https://use.fontawesome.com/releases/v5.0.13/css/all.css);

.container {
  margin-bottom: 10px;
}

.f {
  width: fit-content;
}

.book {
  background-color: lightgray;
  margin-top: 50px;
}

.book h6{
  margin-top: 10px;
}

.search {
  width: 50px;
  height: 50px;
  margin-right: 10px;
  object-fit: contain;
}
</style>
