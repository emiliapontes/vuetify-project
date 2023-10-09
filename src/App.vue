<template>
  <v-app>
    <v-navigation-drawer v-model="isDrawerOpen">
      <v-list>
        <v-list-subreader class="ml-4">
          Menu
        </v-list-subreader>
        <v-list-item prepend-icon="mdi-home">Home</v-list-item>
        <v-list-item prepend-icon="mdi-account">Usuários</v-list-item>
        <v-list-group value="Clientes">
          <template #activator="{ props }">
          <v-list-item
          v-bind="props"
          prepend-icon="mdi-account-circle"
          title="Clientes">
        </v-list-item>
          </template>
          <v-list-item prepend-icon="mdi-currency-usd">Faturamento</v-list-item>
          <v-list-item prepend-icon="mdi-chart-line">Relatório</v-list-item>

        </v-list-group>
      </v-list>
    </v-navigation-drawer>
      <v-app-bar flat class="border-b">
        <v-app-bar-nav-icon @click="isDrawerOpen = !isDrawerOpen"></v-app-bar-nav-icon>
        <v-app-bar-title>Meu app</v-app-bar-title>

        <v-menu>
        <template #activator="{ props }">
          <v-btn icon class="mr-2" v-bind="props">
            <v-badge dot color="info">
              <v-icon icon="mdi-bell-outline"></v-icon>
            </v-badge>
          </v-btn>
        </template>
      
  <v-card
    class="mx-auto"
    max-width="400"
  >
    <v-card-item class="bg-orange-lighten-5">
      <v-card-title>
        Notificações
      </v-card-title>


    </v-card-item>

    <v-divider></v-divider>

    <v-virtual-scroll
      :items="items"
      height="300"
      item-height="90"
    >

    <v-card
      flat
      class="border-b"
      width="400"
      title="This is a title"
      subtitle="This is a subtitle"
      text="This is content">
    <v-btn class="ma-4" size="small">Ver mais</v-btn>
  </v-card>

    </v-virtual-scroll>
  </v-card>
      
        </v-menu>

          <v-menu>
            <template #activator="{ props }">
              <v-avatar class="mr-4" v-bind="props">
                  <v-img 
                  cover
                  src="https://yt3.ggpht.com/yti/ADpuP3PH8Yv_ZnjvnLg_0_KJv-6lxsGJ8OGbOQN_B9ggCA=s88-c-k-c0x00ffffff-no-rj">
                </v-img>
              </v-avatar>
            </template>
              <v-card min-width="200px">
                <v-list>

                  <v-list-item prepend-icon="mdi-account-outline">
                    <v-list-item-title>Meu perfil</v-list-item-title>
                  </v-list-item>

                  <v-list-item prepend-icon="mdi-heart-outline">
                    <v-list-item-title>Favoritos</v-list-item-title>
                  </v-list-item>

                </v-list>
              </v-card>
        </v-menu>

        

      </v-app-bar>

    <v-main>
      <v-container>
        <h1 class="mb-6">Dashboard</h1>

        <v-card flat class="border mb-4">
          <v-card-title>Últimos usuários</v-card-title>   
        <v-table density="compact">
          <thead>
            <tr>
              <th>Nome</th>
              <th>E-mail</th>
              <th>Cargo</th>
              <th>Ações</th>
            </tr>
          </thead>
              <tbody>
                <tr>
                  <td>Fulano</td>
                  <td>Fulano@gmail.com</td>
                  <td>Admin</td>
                  <td>
                    <v-btn variant="tonal" color="primary">
                      Editar
                    </v-btn>
                  </td>
                </tr>
                <tr>
                  <td>Cicrano</td>
                  <td>cicrano@gmail.com</td>
                  <td>Gerente</td>
                </tr>
                <tr>
                  <td>Beltrano</td>
                  <td>beltrano@gmail.com</td>
                  <td>Convidado</td>
                </tr>
              </tbody>
            </v-table>
          </v-card> 

      <v-row> 

        <v-col cols="12" sm="6" md="4" lg="3">
          <v-card>
            <v-img
            class="align-end text-white" 
            src="https://media.istockphoto.com/id/656700836/pt/foto/view-of-manaus-with-teatro-amazonas.jpg?s=1024x1024&w=is&k=20&c=gOiqev7BKOGU9KYd0laQBzU7IJFSE-8o14SizowcF38="
            gradient="to top right, rgba(91, 91, 91, 0.8), rgba(255, 143, 0, 0.31)">
              <v-card-title>Lugares de Manaus já feitos</v-card-title>
            </v-img>
            <v-card-subtitle class="pt-2">Ponta Negra</v-card-subtitle>
            <v-card-text>
              <div>Melhor lugar</div>
              <div>Experiência de praia em pleno rio negro</div>
            </v-card-text>
            <v-card-actions>
              <v-btn variant="outlined" color="primary">Ver mais</v-btn>
              <v-btn prepend-icon="mdi-cart" variant="tonal" color="blue">COMPRAR</v-btn>
            </v-card-actions>
          </v-card>
        </v-col>

        <v-col cols="12" sm="6" md="4" lg="3">
          <v-card>
            <v-img
            class="align-end text-white" 
            src="https://media.istockphoto.com/id/656700836/pt/foto/view-of-manaus-with-teatro-amazonas.jpg?s=1024x1024&w=is&k=20&c=gOiqev7BKOGU9KYd0laQBzU7IJFSE-8o14SizowcF38="
            gradient="to top right, rgba(91, 91, 91, 0.8), rgba(255, 143, 0, 0.31)">
              <v-card-title>Lugares de Manaus já feitos</v-card-title>
            </v-img>
            <v-card-subtitle class="pt-2">Ponta Negra</v-card-subtitle>
            <v-card-text>
              <div>Melhor lugar</div>
              <div>Experiência de praia em pleno rio negro</div>
            </v-card-text>
            <v-card-actions>
              <v-btn>Ver mais</v-btn>
              <v-btn prepend-icon="mdi-cart" variant="tonal" color="blue">COMPRAR</v-btn>
            </v-card-actions>
          </v-card>
        </v-col>

        <v-col cols="12" sm="6" md="4" lg="3">
          <v-card>
            <v-img
            class="align-end text-white" 
            src="https://media.istockphoto.com/id/656700836/pt/foto/view-of-manaus-with-teatro-amazonas.jpg?s=1024x1024&w=is&k=20&c=gOiqev7BKOGU9KYd0laQBzU7IJFSE-8o14SizowcF38="
            gradient="to top right, rgba(91, 91, 91, 0.8), rgba(255, 143, 0, 0.31)">
              <v-card-title>Lugares de Manaus já feitos</v-card-title>
            </v-img>
            <v-card-subtitle class="pt-2">Ponta Negra</v-card-subtitle>
            <v-card-text>
              <div>Melhor lugar</div>
              <div>Experiência de praia em pleno rio negro</div>
            </v-card-text>
            <v-card-actions>
              <v-btn>Ver mais</v-btn>
              <v-btn prepend-icon="mdi-cart" variant="tonal" color="blue">COMPRAR</v-btn>
            </v-card-actions>
          </v-card>
        </v-col>

        <v-col cols="12" sm="6" md="4" lg="3">
          <v-card>
            <v-img
            class="align-end text-white" 
            src="https://media.istockphoto.com/id/656700836/pt/foto/view-of-manaus-with-teatro-amazonas.jpg?s=1024x1024&w=is&k=20&c=gOiqev7BKOGU9KYd0laQBzU7IJFSE-8o14SizowcF38="
            gradient="to top right, rgba(91, 91, 91, 0.8), rgba(255, 143, 0, 0.31)">
              <v-card-title>Lugares de Manaus já feitos</v-card-title>
            </v-img>
            <v-card-subtitle class="pt-2">Ponta Negra</v-card-subtitle>
            <v-card-text>
              <div>Melhor lugar</div>
              <div>Experiência de praia em pleno rio negro</div>
            </v-card-text>
            <v-card-actions>
              <v-btn>Ver mais</v-btn>
              <v-btn prepend-icon="mdi-cart" variant="tonal" color="blue">COMPRAR</v-btn>
            </v-card-actions>
          </v-card>
        </v-col>

      </v-row>
      </v-container>
    </v-main>
  </v-app>
</template>

<script>

  import { ref } from 'vue';
  const isDrawerOpen = ref(false)

  export default {
    data: () => ({
      colors: ['#2196F3', '#90CAF9', '#64B5F6', '#42A5F5', '#1E88E5', '#1976D2', '#1565C0', '#0D47A1', '#82B1FF', '#448AFF', '#2979FF', '#2962FF'],
      names: ['Oliver', 'Jake', 'Noah', 'James', 'Jack', 'Connor', 'Liam', 'John', 'Harry', 'Callum', 'Mason', 'Robert', 'Jacob', 'Jacob', 'Jacob', 'Michael', 'Charlie', 'Kyle', 'William', 'William', 'Thomas', 'Joe', 'Ethan', 'David', 'George', 'Reece', 'Michael', 'Richard', 'Oscar', 'Rhys', 'Alexander', 'Joseph', 'James', 'Charlie', 'James', 'Charles', 'William', 'Damian', 'Daniel', 'Thomas', 'Amelia', 'Margaret', 'Emma', 'Mary', 'Olivia', 'Samantha', 'Olivia', 'Patricia', 'Isla', 'Bethany'],
      surnames: ['Smith', 'Anderson', 'Clark', 'Wright', 'Mitchell', 'Johnson', 'Thomas', 'Rodriguez', 'Lopez', 'Perez', 'Williams', 'Jackson', 'Lewis', 'Hill', 'Roberts', 'Jones', 'White', 'Lee', 'Scott', 'Turner', 'Brown', 'Harris', 'Walker', 'Green', 'Phillips', 'Davis', 'Martin', 'Hall', 'Adams', 'Campbell', 'Miller', 'Thompson', 'Allen', 'Baker', 'Parker', 'Wilson', 'Garcia', 'Young', 'Gonzalez', 'Evans', 'Moore', 'Martinez', 'Hernandez', 'Nelson', 'Edwards', 'Taylor', 'Robinson', 'King', 'Carter', 'Collins'],
    }),

    computed: {
      items () {
        const namesLength = this.names.length
        const surnamesLength = this.surnames.length
        const colorsLength = this.colors.length

        return Array.from({ length: 10000 }, () => {
          const name = this.names[this.genRandomIndex(namesLength)]
          const surname = this.surnames[this.genRandomIndex(surnamesLength)]

          return {
            color: this.colors[this.genRandomIndex(colorsLength)],
            fullName: `${name} ${surname}`,
            initials: `${name[0]} ${surname[0]}`,
          }
        })
      },
    },

    methods: {
      genRandomIndex (length) {
        return Math.ceil(Math.random() * (length - 1))
      },
    },
  }
</script>