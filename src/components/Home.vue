<template>
  <Layout>
    <template #header>
      <Header></Header>
    </template>
    <template #resume>
      <Resume
        :total-label="'Ahorro total'"
        :label="label"
        :total-amount="10000"
        :amount="amount"
      >
        <template #graphic>
          <Graphic :amounts="amounts" />
        </template>
        <template #action>
          <Action />
        </template>
      </Resume>
    </template>
    <template #movements>
      <Movements :movements="movements" />
    </template>
  </Layout>
</template>

<script>
import Layout from "./Layout.vue";
import Header from "./Header.vue";
import Resume from "./Resume/Index.vue";
import Movements from "./Movements/Index.vue";
import Action from "./Action.vue";
import Graphic from "./Resume/Graphic.vue";

export default {
  components: {
    Layout,
    Header,
    Resume,
    Movements,
    Action,
    Graphic,
  },
  data() {
    return {
      label: null,
      amount: null,
      amounts: [100, 200, 500, -300, -500, -600, -300, 0, 300, 500],
      movements: [
        {
          id: 0,
          title: "Movimiento",
          description: "lorem ipsum dolor sit amet",
          amount: 1000,
        },
        {
          id: 1,
          title: "Movimiento",
          description: "lorem ipsum dolor sit amet",
          amount: -1000,
        },
        {
          id: 2,
          title: "Movimiento",
          description: "lorem ipsum dolor sit amet",
          amount: -1000,
        },
        {
          id: 3,
          title: "Movimiento",
          description: "lorem ipsum dolor sit amet",
          amount: 1000,
        },
        {
          id: 4,
          title: "Movimiento",
          description: "lorem ipsum dolor sit amet",
          amount: 1000,
        },
        {
          id: 5,
          title: "Movimiento",
          description: "lorem ipsum dolor sit amet",
          amount: 1000,
        },
        {
          id: 6,
          title: "Movimiento",
          description: "lorem ipsum dolor sit amet",
          amount: 1000,
        },
        {
          id: 7,
          title: "Movimiento",
          description: "lorem ipsum dolor sit amet",
          amount: 1000,
        },
      ],
    };
  },
};
</script>
