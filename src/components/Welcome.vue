<template>
    <div class="hello">
        <h1>{{ msg }}</h1>

        <h3>Javascript Events</h3>

        <ul>
            <li>Date() Event:  <button v-on:click="setTime">Click for Time</button> &nbsp;</li>
                <p v-model="time">{{ time }}</p>
        </ul>

        <h3>Props</h3>
        <ul>
            <li>The title is received from the App.vue via props.</li>
            <li>Props tell the child component to be ready to receive data.
            <li>The prop is written in the child component and describes the data to be received.</li>
        </ul>

        <h3>Custom Events</h3>
        <p>Passing Data from Child to Parent Component via Custom Events</p>

        <h4>Using <code>$emit()</code> Method</h4>

        <ul>
            <li><code>this.$emit('change', value);</code></li>
            <li>The dollar sign, $, signifies a built-in method</li>
        </ul>



        <br><br>
        <button @click="printAdjective">Click Here</button>

    </div>
</template>

<script>
  export default {
    name: 'Welcome',
    time: '',
    props: {
      msg: String,
      adjective: String
    },
    methods: {
      setTime() {
        this.time = "Time is 1300";
      },
      printAdjective() {
        this.adjective = "Supertacilus";
        this.$emit('adjectiveReset', this.adjective);

      }
    }
  }
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
    h3 {
        margin: 40px 0 0;
        text-align: left;
    }

    h4 {
        text-align: left;
    }
    .align-left {
        text-align:left;
    }
    p {
        text-align: left;
    }

    ul {
        list-style-type: none;
        padding: 0;
        text-align: left;
    }

    li {
        /*display: inline-block;*/
        margin: 0 10px;
    }

    a {
        color: #42b983;
    }

</style>
