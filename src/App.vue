<template>
  <MyComponent :items="myItems">
    <div slot="header">My test header</div>
    <div slot="item" slot-scope="it">
      <span>{{ it.data.id }}</span>
      <span>{{ it.data.name }}</span>
    </div>
  </MyComponent>
</template>

<script>
import MyComponent from "./MyComponent";
export default {
  name: "App",
  components: {
    MyComponent,
  },
  data() {
    return {
      myItems: [
        {
          id: 1,
          name: "Item_1",
        },
        {
          id: 2,
          name: "Item_2",
        },
        {
          id: 3,
          name: "Item_3",
        },
        {
          id: 4,
          name: "Item_4",
        },
      ],
    };
  },
};
</script>

