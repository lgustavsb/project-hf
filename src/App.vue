<template>
  <v-app id="inspire">
    <v-navigation-drawer v-model="drawer" app>
      <template v-slot:prepend>
        <v-list-item>
          <v-row justify="center">
            <v-img
              class="logo"
              src="./assets/logo.svg"
              width="100%"
              max-width="120"
            >
            </v-img>
          </v-row>
        </v-list-item>
      </template>
    </v-navigation-drawer>
    <v-app-bar app color="white" elevate-on-scroll>
      <v-app-bar-nav-icon @click="drawer = !drawer"></v-app-bar-nav-icon>
      <v-spacer></v-spacer>
      <div
        class="
          d-flex
          flex-lg-row
          justify-lg-center
          align-lg-center
          flex-md-row
          justify-md-center
          align-md-center
        "
      >
        <div
          class="
            box-menu
            d-flex
            flex-lg-column
            justify-lg-center
            align-lg-end
            flex-md-column
            justify-md-center
            align-md-end
          "
        >
          <p>Juraci Simão</p>
          <span>Comprador</span>
        </div>
        <v-avatar color="primary" size="40">
          <img src="./assets/juraci-simao.svg" alt="José Simão" />
        </v-avatar>
      </div>
    </v-app-bar>
    <v-main>
      <v-container>
        <v-row>
          <v-col cols="12">
            <div class="titulo-produtor mt-10">
              <div class="perfil-produtor">
                <img src="./assets/jose-arantes.svg" />
              </div>
              <div
                class="
                  dados-pessoais-produtor
                  green
                  darken-1
                  d-flex
                  flex-lg-column
                  justify-lg-end
                  align-lg-start
                  flex-md-column
                  justify-md-end
                  align-md-start
                "
              >
                <p
                  class="
                    d-flex
                    flex-lg-row
                    justify-lg-center
                    align-lg-center
                    flex-md-row
                    justify-md-center
                    align-md-center
                  "
                >
                  <i class="mdi mdi-food-apple"></i
                  ><span class="darken-4">Produtor</span>
                </p>
                <h2 class="white--text">José Arantes</h2>
              </div>
              <div class="localizacao-produtor d-flex flex-lg-row flex-md-row">
                <!-- <p>
                  <strong>Cidade: </strong> <span>Votuporanga </span>
                  <strong>UF: </strong> <span> SP </span>
                </p> -->
              </div>
            </div>
          </v-col>
          <v-col cols="4" offset-lg="8">
            <v-text-field
              outlined
              color="green"
              label="Pesquisar produto"
              prepend-inner-icon="mdi-magnify"
            ></v-text-field>
          </v-col>
          <v-col cols="12">
            <v-divider></v-divider>
          </v-col>
          <v-col class="mt-2 title-categorias" cols="12">
            <h2>Frutas</h2>
          </v-col>
          <v-col cols="12">
            <v-sheet>
              <v-slide-group show-arrows>
                <v-slide-item v-slot="{ active, toggle }">
                  <v-card
                    class="
                      ma-4
                      card-produto
                      d-flex
                      flex-lg-column
                      justify-lg-start
                      align-lg-center
                    "
                    height="auto"
                    max-width="100%"
                    width="250"
                  >
                    <v-img
                      src="./assets/produtos/frutas/banana.webp"
                      width="100%"
                      max-width="200"
                    >
                      <v-btn class="add-favoritos" icon white @click="toggle">
                        <v-icon>
                          {{ active ? "mdi-heart" : "mdi-heart-outline" }}
                        </v-icon>
                      </v-btn>
                    </v-img>
                    <div
                      class="
                        info-produto
                        d-flex
                        flex-lg-column
                        justify-lg-start
                        align-lg-start
                      "
                    >
                      <div class="sub-titulo-produto">
                        <span>Frutas</span>
                      </div>
                      <div class="titulo-produto">
                        <h3>Banana Nanica</h3>
                      </div>
                      <div class="preco-produto orange--text darken-4">
                        <p>
                          R$ 200,00
                          <span>/ 100u</span>
                        </p>
                      </div>
                    </div>
                    <v-btn block class="white--text green darken-1">
                      <i class="mdi mdi-cart"></i>
                      <span>Adicionar</span>
                    </v-btn>
                  </v-card>
                </v-slide-item>
                <v-slide-item v-slot="{ active, toggle }">
                  <v-card
                    class="
                      ma-4
                      card-produto
                      d-flex
                      flex-lg-column
                      justify-lg-start
                      align-lg-center
                    "
                    height="auto"
                    max-width="100%"
                    width="250"
                  >
                    <v-img
                      src="./assets/produtos/frutas/kiwi.webp"
                      width="100%"
                      max-width="200"
                      text="left"
                    >
                      <v-btn class="add-favoritos" icon white @click="toggle">
                        <v-icon>
                          {{ active ? "mdi-heart" : "mdi-heart-outline" }}
                        </v-icon>
                      </v-btn>
                    </v-img>
                    <div
                      class="
                        info-produto
                        d-flex
                        flex-lg-column
                        justify-lg-start
                        align-lg-start
                      "
                    >
                      <div class="sub-titulo-produto">
                        <span>Frutas</span>
                      </div>
                      <div class="titulo-produto">
                        <h3>Kiwi</h3>
                      </div>
                      <div class="preco-produto">
                        <p>
                          R$ 200,00
                          <span>/ 100u</span>
                        </p>
                      </div>
                    </div>
                    <v-btn block class="white--text green darken-1">
                      <i class="mdi mdi-cart"></i>
                      <span>Adicionar</span>
                    </v-btn>
                  </v-card>
                </v-slide-item>
                <v-slide-item v-slot="{ active, toggle }">
                  <v-card
                    class="
                      ma-4
                      card-produto
                      d-flex
                      flex-lg-column
                      justify-lg-start
                      align-lg-center
                    "
                    height="auto"
                    max-width="100%"
                    width="250"
                  >
                    <v-img
                      src="./assets/produtos/frutas/laranja-pera.webp"
                      width="100%"
                      max-width="200"
                      text="left"
                    >
                      <v-btn class="add-favoritos" icon white @click="toggle">
                        <v-icon>
                          {{ active ? "mdi-heart" : "mdi-heart-outline" }}
                        </v-icon>
                      </v-btn>
                    </v-img>
                    <div
                      class="
                        info-produto
                        d-flex
                        flex-lg-column
                        justify-lg-start
                        align-lg-start
                      "
                    >
                      <div class="sub-titulo-produto">
                        <span>Frutas</span>
                      </div>
                      <div class="titulo-produto">
                        <h3>Laranja Pera</h3>
                      </div>
                      <div class="preco-produto">
                        <p>
                          R$ 200,00
                          <span>/ 100u</span>
                        </p>
                      </div>
                    </div>
                    <v-btn block class="white--text green darken-1">
                      <i class="mdi mdi-cart"></i>
                      <span>Adicionar</span>
                    </v-btn>
                  </v-card>
                </v-slide-item>
                <v-slide-item v-slot="{ active, toggle }">
                  <v-card
                    class="
                      ma-4
                      card-produto
                      d-flex
                      flex-lg-column
                      justify-lg-start
                      align-lg-center
                    "
                    height="auto"
                    max-width="100%"
                    width="250"
                  >
                    <v-img
                      src="./assets/produtos/frutas/limao-siciliano.webp"
                      width="100%"
                      max-width="200"
                      text="left"
                    >
                      <v-btn class="add-favoritos" icon white @click="toggle">
                        <v-icon>
                          {{ active ? "mdi-heart" : "mdi-heart-outline" }}
                        </v-icon>
                      </v-btn>
                    </v-img>
                    <div
                      class="
                        info-produto
                        d-flex
                        flex-lg-column
                        justify-lg-start
                        align-lg-start
                      "
                    >
                      <div class="sub-titulo-produto">
                        <span>Frutas</span>
                      </div>
                      <div class="titulo-produto">
                        <h3>Limão Siciliano</h3>
                      </div>
                      <div class="preco-produto">
                        <p>
                          R$ 200,00
                          <span>/ 100u</span>
                        </p>
                      </div>
                    </div>
                    <v-btn block class="white--text green darken-1">
                      <i class="mdi mdi-cart"></i>
                      <span>Adicionar</span>
                    </v-btn>
                  </v-card>
                </v-slide-item>
                <v-slide-item v-slot="{ active, toggle }">
                  <v-card
                    class="
                      ma-4
                      card-produto
                      d-flex
                      flex-lg-column
                      justify-lg-start
                      align-lg-center
                      flex-md-column
                      justify-md-start
                      align-md-center
                    "
                    height="auto"
                    max-width="100%"
                    width="250"
                  >
                    <v-img
                      src="./assets/produtos/frutas/limao-tahiti.webp"
                      width="100%"
                      max-width="200"
                      text="left"
                    >
                      <v-btn class="add-favoritos" icon white @click="toggle">
                        <v-icon>
                          {{ active ? "mdi-heart" : "mdi-heart-outline" }}
                        </v-icon>
                      </v-btn>
                    </v-img>
                    <div
                      class="
                        info-produto
                        d-flex
                        flex-lg-column
                        justify-lg-start
                        align-lg-start
                        flex-md-column
                        justify-md-start
                        align-md-start
                      "
                    >
                      <div class="sub-titulo-produto">
                        <span>Frutas</span>
                      </div>
                      <div class="titulo-produto">
                        <h3>Limão Tahiti</h3>
                      </div>
                      <div class="preco-produto">
                        <p>
                          R$ 200,00
                          <span>/ 100u</span>
                        </p>
                      </div>
                    </div>
                    <v-btn block class="white--text green darken-1">
                      <i class="mdi mdi-cart"></i>
                      <span>Adicionar</span>
                    </v-btn>
                  </v-card>
                </v-slide-item>
                <v-slide-item v-slot="{ active, toggle }">
                  <v-card
                    class="
                      ma-4
                      card-produto
                      d-flex
                      flex-lg-column
                      justify-lg-start
                      align-lg-center
                      flex-md-column
                      justify-md-start
                      align-md-center
                    "
                    height="auto"
                    max-width="100%"
                    width="250"
                  >
                    <v-img
                      src="./assets/produtos/frutas/mamao.webp"
                      width="100%"
                      max-width="200"
                      text="left"
                    >
                      <v-btn class="add-favoritos" icon white @click="toggle">
                        <v-icon>
                          {{ active ? "mdi-heart" : "mdi-heart-outline" }}
                        </v-icon>
                      </v-btn>
                    </v-img>
                    <div
                      class="
                        info-produto
                        d-flex
                        flex-lg-column
                        justify-lg-start
                        align-lg-start
                        flex-md-column
                        justify-md-start
                        align-md-start
                      "
                    >
                      <div class="sub-titulo-produto">
                        <span>Frutas</span>
                      </div>
                      <div class="titulo-produto">
                        <h3>Mamão Papaya</h3>
                      </div>
                      <div class="preco-produto">
                        <p>
                          R$ 200,00
                          <span>/ 100u</span>
                        </p>
                      </div>
                    </div>
                    <v-btn block class="white--text green darken-1">
                      <i class="mdi mdi-cart"></i>
                      <span>Adicionar</span>
                    </v-btn>
                  </v-card>
                </v-slide-item>
                <v-slide-item v-slot="{ active, toggle }">
                  <v-card
                    class="
                      ma-4
                      card-produto
                      d-flex
                      flex-lg-column
                      justify-lg-start
                      align-lg-center
                      flex-md-column
                      justify-md-start
                      align-md-center
                    "
                    height="auto"
                    max-width="100%"
                    width="250"
                  >
                    <v-img
                      src="./assets/produtos/frutas/manga-palmer.webp"
                      width="100%"
                      max-width="200"
                      text="left"
                    >
                      <v-btn class="add-favoritos" icon white @click="toggle">
                        <v-icon>
                          {{ active ? "mdi-heart" : "mdi-heart-outline" }}
                        </v-icon>
                      </v-btn>
                    </v-img>
                    <div
                      class="
                        info-produto
                        d-flex
                        flex-lg-column
                        justify-lg-start
                        align-lg-start
                        flex-md-column
                        justify-md-start
                        align-md-start
                      "
                    >
                      <div class="sub-titulo-produto">
                        <span>Frutas</span>
                      </div>
                      <div class="titulo-produto">
                        <h3>Manga Palmer</h3>
                      </div>
                      <div class="preco-produto">
                        <p>
                          R$ 200,00
                          <span>/ 100u</span>
                        </p>
                      </div>
                    </div>
                    <v-btn block class="white--text green darken-1">
                      <i class="mdi mdi-cart"></i>
                      <span>Adicionar</span>
                    </v-btn>
                  </v-card>
                </v-slide-item>
                <v-slide-item v-slot="{ active, toggle }">
                  <v-card
                    class="
                      ma-4
                      card-produto
                      d-flex
                      flex-lg-column
                      justify-lg-start
                      align-lg-center
                      flex-md-column
                      justify-md-start
                      align-md-center
                    "
                    height="auto"
                    max-width="100%"
                    width="250"
                  >
                    <v-img
                      src="./assets/produtos/frutas/morango.webp"
                      width="100%"
                      max-width="200"
                      text="left"
                    >
                      <v-btn class="add-favoritos" icon white @click="toggle">
                        <v-icon>
                          {{ active ? "mdi-heart" : "mdi-heart-outline" }}
                        </v-icon>
                      </v-btn>
                    </v-img>
                    <div
                      class="
                        info-produto
                        d-flex
                        flex-lg-column
                        justify-lg-start
                        align-lg-start
                        flex-md-column
                        justify-md-start
                        align-md-start
                      "
                    >
                      <div class="sub-titulo-produto">
                        <span>Frutas</span>
                      </div>
                      <div class="titulo-produto">
                        <h3>Morango</h3>
                      </div>
                      <div class="preco-produto">
                        <p>
                          R$ 200,00
                          <span>/ 100u</span>
                        </p>
                      </div>
                    </div>
                    <v-btn block class="white--text green darken-1">
                      <i class="mdi mdi-cart"></i>
                      <span>Adicionar</span>
                    </v-btn>
                  </v-card>
                </v-slide-item>
              </v-slide-group>
            </v-sheet>
          </v-col>
          <v-col class="mt-2 title-categorias" cols="12">
            <h2>Legumes & Verduras</h2>
          </v-col>
          <v-col cols="12">
            <v-sheet>
              <v-slide-group show-arrows>
                <v-slide-item v-slot="{ active, toggle }">
                  <v-card
                    class="
                      ma-4
                      card-produto
                      d-flex
                      flex-lg-column
                      justify-lg-start
                      align-lg-center
                    "
                    height="auto"
                    max-width="100%"
                    width="250"
                  >
                    <v-img
                      src="./assets/produtos/legumes-verduras/abobrinha-italiana.webp"
                      width="100%"
                      max-width="200"
                    >
                      <v-btn class="add-favoritos" icon white @click="toggle">
                        <v-icon>
                          {{ active ? "mdi-heart" : "mdi-heart-outline" }}
                        </v-icon>
                      </v-btn>
                    </v-img>
                    <div
                      class="
                        info-produto
                        d-flex
                        flex-lg-column
                        justify-lg-start
                        align-lg-start
                      "
                    >
                      <div class="sub-titulo-produto">
                        <span>Legumes</span>
                      </div>
                      <div class="titulo-produto">
                        <h3>Abobrinha Italiana</h3>
                      </div>
                      <div class="preco-produto orange--text darken-4">
                        <p>
                          R$ 200,00
                          <span>/ 100u</span>
                        </p>
                      </div>
                    </div>
                    <v-btn block class="white--text green darken-1">
                      <i class="mdi mdi-cart"></i>
                      <span>Adicionar</span>
                    </v-btn>
                  </v-card>
                </v-slide-item>
                <v-slide-item v-slot="{ active, toggle }">
                  <v-card
                    class="
                      ma-4
                      card-produto
                      d-flex
                      flex-lg-column
                      justify-lg-start
                      align-lg-center
                    "
                    height="auto"
                    max-width="100%"
                    width="250"
                  >
                    <v-img
                      src="./assets/produtos/legumes-verduras/alho-roxo.webp"
                      width="100%"
                      max-width="200"
                      text="left"
                    >
                      <v-btn class="add-favoritos" icon white @click="toggle">
                        <v-icon>
                          {{ active ? "mdi-heart" : "mdi-heart-outline" }}
                        </v-icon>
                      </v-btn>
                    </v-img>
                    <div
                      class="
                        info-produto
                        d-flex
                        flex-lg-column
                        justify-lg-start
                        align-lg-start
                      "
                    >
                      <div class="sub-titulo-produto">
                        <span>Legumes</span>
                      </div>
                      <div class="titulo-produto">
                        <h3>Alho Roxo</h3>
                      </div>
                      <div class="preco-produto">
                        <p>
                          R$ 200,00
                          <span>/ 100u</span>
                        </p>
                      </div>
                    </div>
                    <v-btn block class="white--text green darken-1">
                      <i class="mdi mdi-cart"></i>
                      <span>Adicionar</span>
                    </v-btn>
                  </v-card>
                </v-slide-item>
                <v-slide-item v-slot="{ active, toggle }">
                  <v-card
                    class="
                      ma-4
                      card-produto
                      d-flex
                      flex-lg-column
                      justify-lg-start
                      align-lg-center
                    "
                    height="auto"
                    max-width="100%"
                    width="250"
                  >
                    <v-img
                      src="./assets/produtos/legumes-verduras/batata-doce-rosada.webp"
                      width="100%"
                      max-width="200"
                      text="left"
                    >
                      <v-btn class="add-favoritos" icon white @click="toggle">
                        <v-icon>
                          {{ active ? "mdi-heart" : "mdi-heart-outline" }}
                        </v-icon>
                      </v-btn>
                    </v-img>
                    <div
                      class="
                        info-produto
                        d-flex
                        flex-lg-column
                        justify-lg-start
                        align-lg-start
                      "
                    >
                      <div class="sub-titulo-produto">
                        <span>Legumes</span>
                      </div>
                      <div class="titulo-produto">
                        <h3>Batata Doce Rosada</h3>
                      </div>
                      <div class="preco-produto">
                        <p>
                          R$ 200,00
                          <span>/ 100u</span>
                        </p>
                      </div>
                    </div>
                    <v-btn block class="white--text green darken-1">
                      <i class="mdi mdi-cart"></i>
                      <span>Adicionar</span>
                    </v-btn>
                  </v-card>
                </v-slide-item>
                <v-slide-item v-slot="{ active, toggle }">
                  <v-card
                    class="
                      ma-4
                      card-produto
                      d-flex
                      flex-lg-column
                      justify-lg-start
                      align-lg-center
                    "
                    height="auto"
                    max-width="100%"
                    width="250"
                  >
                    <v-img
                      src="./assets/produtos/legumes-verduras/batata.webp"
                      width="100%"
                      max-width="200"
                      text="left"
                    >
                      <v-btn class="add-favoritos" icon white @click="toggle">
                        <v-icon>
                          {{ active ? "mdi-heart" : "mdi-heart-outline" }}
                        </v-icon>
                      </v-btn>
                    </v-img>
                    <div
                      class="
                        info-produto
                        d-flex
                        flex-lg-column
                        justify-lg-start
                        align-lg-start
                      "
                    >
                      <div class="sub-titulo-produto">
                        <span>Legumes</span>
                      </div>
                      <div class="titulo-produto">
                        <h3>Batata</h3>
                      </div>
                      <div class="preco-produto">
                        <p>
                          R$ 200,00
                          <span>/ 100u</span>
                        </p>
                      </div>
                    </div>
                    <v-btn block class="white--text green darken-1">
                      <i class="mdi mdi-cart"></i>
                      <span>Adicionar</span>
                    </v-btn>
                  </v-card>
                </v-slide-item>
                <v-slide-item v-slot="{ active, toggle }">
                  <v-card
                    class="
                      ma-4
                      card-produto
                      d-flex
                      flex-lg-column
                      justify-lg-start
                      align-lg-center
                      flex-md-column
                      justify-md-start
                      align-md-center
                    "
                    height="auto"
                    max-width="100%"
                    width="250"
                  >
                    <v-img
                      src="./assets/produtos/legumes-verduras/cebola-granel.webp"
                      width="100%"
                      max-width="200"
                      text="left"
                    >
                      <v-btn class="add-favoritos" icon white @click="toggle">
                        <v-icon>
                          {{ active ? "mdi-heart" : "mdi-heart-outline" }}
                        </v-icon>
                      </v-btn>
                    </v-img>
                    <div
                      class="
                        info-produto
                        d-flex
                        flex-lg-column
                        justify-lg-start
                        align-lg-start
                        flex-md-column
                        justify-md-start
                        align-md-start
                      "
                    >
                      <div class="sub-titulo-produto">
                        <span>Legumes</span>
                      </div>
                      <div class="titulo-produto">
                        <h3>Cebola Granel</h3>
                      </div>
                      <div class="preco-produto">
                        <p>
                          R$ 200,00
                          <span>/ 100u</span>
                        </p>
                      </div>
                    </div>
                    <v-btn block class="white--text green darken-1">
                      <i class="mdi mdi-cart"></i>
                      <span>Adicionar</span>
                    </v-btn>
                  </v-card>
                </v-slide-item>
                <v-slide-item v-slot="{ active, toggle }">
                  <v-card
                    class="
                      ma-4
                      card-produto
                      d-flex
                      flex-lg-column
                      justify-lg-start
                      align-lg-center
                      flex-md-column
                      justify-md-start
                      align-md-center
                    "
                    height="auto"
                    max-width="100%"
                    width="250"
                  >
                    <v-img
                      src="./assets/produtos/legumes-verduras/cenoura.webp"
                      width="100%"
                      max-width="200"
                      text="left"
                    >
                      <v-btn class="add-favoritos" icon white @click="toggle">
                        <v-icon>
                          {{ active ? "mdi-heart" : "mdi-heart-outline" }}
                        </v-icon>
                      </v-btn>
                    </v-img>
                    <div
                      class="
                        info-produto
                        d-flex
                        flex-lg-column
                        justify-lg-start
                        align-lg-start
                        flex-md-column
                        justify-md-start
                        align-md-start
                      "
                    >
                      <div class="sub-titulo-produto">
                        <span>Legumes</span>
                      </div>
                      <div class="titulo-produto">
                        <h3>Cenoura</h3>
                      </div>
                      <div class="preco-produto">
                        <p>
                          R$ 200,00
                          <span>/ 100u</span>
                        </p>
                      </div>
                    </div>
                    <v-btn block class="white--text green darken-1">
                      <i class="mdi mdi-cart"></i>
                      <span>Adicionar</span>
                    </v-btn>
                  </v-card>
                </v-slide-item>
                <v-slide-item v-slot="{ active, toggle }">
                  <v-card
                    class="
                      ma-4
                      card-produto
                      d-flex
                      flex-lg-column
                      justify-lg-start
                      align-lg-center
                      flex-md-column
                      justify-md-start
                      align-md-center
                    "
                    height="auto"
                    max-width="100%"
                    width="250"
                  >
                    <v-img
                      src="./assets/produtos/legumes-verduras/gengibre.webp"
                      width="100%"
                      max-width="200"
                      text="left"
                    >
                      <v-btn class="add-favoritos" icon white @click="toggle">
                        <v-icon>
                          {{ active ? "mdi-heart" : "mdi-heart-outline" }}
                        </v-icon>
                      </v-btn>
                    </v-img>
                    <div
                      class="
                        info-produto
                        d-flex
                        flex-lg-column
                        justify-lg-start
                        align-lg-start
                        flex-md-column
                        justify-md-start
                        align-md-start
                      "
                    >
                      <div class="sub-titulo-produto">
                        <span>Legumes</span>
                      </div>
                      <div class="titulo-produto">
                        <h3>Gengibre</h3>
                      </div>
                      <div class="preco-produto">
                        <p>
                          R$ 200,00
                          <span>/ 100u</span>
                        </p>
                      </div>
                    </div>
                    <v-btn block class="white--text green darken-1">
                      <i class="mdi mdi-cart"></i>
                      <span>Adicionar</span>
                    </v-btn>
                  </v-card>
                </v-slide-item>
              </v-slide-group>
            </v-sheet>
          </v-col>
        </v-row>
      </v-container>
    </v-main>
  </v-app>
</template>

<script>
export default {
  data: () => ({
    drawer: null,
    items: [
      {
        text: "CEASA",
        disabled: false,
        href: "breadcrumbs_dashboard",
      },
      {
        text: "Produtor",
        disabled: false,
        href: "breadcrumbs_link_1",
      },
    ],
  }),
  components: {},
};
</script>

<style lang="scss">
$color-pack: false;

@import url("https://fonts.googleapis.com/css2?family=Inter:wght@400;600;700&display=swap");

.v-application {
  font-family: "Inter", sans-serif;
}

.title-categorias{
  color: #141414;
  padding-left: 5rem;
  position: relative;
  z-index: 2;
  &:after{
    content: "";
    position: absolute;
    width: 40px;
    height: 5px;
    background-color: #43A047;
    border-radius: 0.25rem;
    bottom: 10px;
    z-index: -1;
  }
}

.titulo-produtor {
  position: relative;
  height: 170px;
  .perfil-produtor {
    position: absolute;
    top: 50%;
    left: 6rem;
    transform: translate(-50%, -50%);
    img {
      max-width: 100%;
      width: 120px;
      height: auto;
    }
  }
  .dados-pessoais-produtor {
    border-radius: 0.25rem;
    padding-bottom: 5px;
    h2 {
      margin: 0;
      font-weight: 600;
    }
    p {
      gap: 3px;
      margin-bottom: -3px;
      i {
        color: #1b5e20;
      }
      span {
        font-weight: 600;
        color: #1b5e20;
      }
    }
  }
  .localizacao-produtor {
    padding-top: 5px;
    p {
      span {
        &:first-child() {
          font-weight: 600;
        }
      }
    }
  }
  .dados-pessoais-produtor,
  .localizacao-produtor {
    height: 5rem;
    padding-left: 11rem;
  }
}
.card-produto {
  padding: 1rem;
  position: relative;
  .add-favoritos {
    position: absolute;
    right: 0;
  }
}
.info-produto {
  width: 100%;
  .sub-titulo-produto {
    span {
      font-size: 11px;
      font-weight: 400;
      text-transform: uppercase;
      color: #757575;
      letter-spacing: 0.1px;
    }
  }
  .titulo-produto {
    color: #141414;
  }
  .preco-produto {
    p {
      font-size: 16px;
      font-weight: 600;
      margin-top: 10px;
      color: #f57c00;
      span {
        font-weight: 600;
        font-size: 12px;
        color: #757575;
      }
    }
  }
}
.box-menu {
  margin-right: 0.5rem;
  p {
    margin: 0;
    font-weight: 600;
  }
  span {
    font-size: 14px;
    margin-top: -3px;
    color: #757575;
  }
}
.logo {
  margin-top: 20px;
}
.v-text-field__details {
  display: none;
}
</style>