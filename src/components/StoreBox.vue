<template>
    <div style="padding:8px;">
        <div class='row'>
            <div
                clickable
                v-for="store in stores"
                :key="store.id"
                @click="showDetails(store)"
                class='grid-item'><div class="grid-item-container"><h3>{{store.name}}</h3></div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    data() {
        return {
            stores: [
            {id: "1233", name: "Store1", details:"lorem ipsume dolores est un"},
            {id: "1234", name: "General Production Station", details:"lorem ipsume dolores est un"},
            {id: "1235", name: "Store2", details:"lorem ipsume dolores est un"},
            {id: "1236", name: "General Production Station", details:"lorem ipsume dolores est un"},
            {id: "1237", name: "Store3", details:"lorem ipsume dolores est un"}
            ]
        }
    },
    methods:{
    showDetails(store) {
      this.$q.dialog({
        title: store.name,
        message: `<pre>${JSON.stringify(store,null,2)}</pre>`,
        html: true,
        cancel: true,
        persistent: true
      }).onOk(() => {
        // console.log('>>>> OK')
      }).onOk(() => {
        // console.log('>>>> second OK catcher')
      }).onCancel(() => {
        // console.log('>>>> Cancel')
      }).onDismiss(() => {
        // console.log('I am triggered on both OK and Cancel')
      })
    },
    }
}
</script>


<style lang="scss">
body {
    background-color: black;
}

h3 {
    color: white;
}

.row {
  display: flex;
  flex-flow: row wrap;
  justify-content: flex-start;
}

.grid-item-container {
  height: 100%;
  width: 100%;
  padding: 8px;
  background-color: #c52035;
  display: flex;
  text-align: center;
  align-items : center;
  justify-content: center;

}
.grid-item {
    height: 250px;
    width: 250px;
    flex-basis: 20%;
    -ms-flex: auto;
    position: relative;
    box-sizing: border-box;
    padding: 8px 8px 40px 8px;
    :hover {
      cursor: pointer;
  }
}
// 
@media(max-width: 1333px) {
    .grid-item {
      flex-basis: 33.33%;
    }
  }
  
  @media(max-width: 1073px) {
     .grid-item {
      flex-basis: 33.33%;
    }
  }
  
  @media(max-width: 815px) {
    .grid-item {
      flex-basis: 50%;
    }
  }
  
  @media(max-width: 620px) {
    .col {
      clear: both;
      float: none;
      margin-left: auto;
      margin-right: auto;
      width: auto !important;
    }
  }
  
  @media(max-width: 555px) {
    .grid-item {
      flex-basis: 100%;
    }
  }

</style>
