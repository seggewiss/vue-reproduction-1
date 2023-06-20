<script setup lang="ts">
import { defineComponent } from 'vue';
import Criteria from 'node_modules/@shopware-ag/admin-extension-sdk/es/data/Criteria';

defineComponent({
  name: 'TheWelcome',

  template: '<h1>Welcome to Vue 3</h1>',

  data(): { var: Criteria|null } {
    return {
      var: null,
    };
  },

  created() {
    this.var = new Criteria();

    this.sayHello(this.var); // The type does not match the expected type 'Criteria'.

    // These however work:
    const criteria = new Criteria();
    this.sayHello(criteria);
    this.sayHello(new Criteria());
  },

  methods: {
    sayHello(v: Criteria) {
      console.log('Hello', v);
    },
  },
});
</script>
