<template>
<div>
<div class='row'>
    <div class='grid-item'><div class="grid-item-container"><h3>General Production Station</h3></div></div>
    <div class='grid-item'><div class="grid-item-container"><h3>General Production Station</h3></div></div>
    <div class='grid-item'><div class="grid-item-container"><h3>General Production Station</h3></div></div>
    <div class='grid-item'><div class="grid-item-container"><h3>General Production Station</h3></div></div>
    <div class='grid-item'><div class="grid-item-container"><h3>General Production Station</h3></div></div>
</div>
</div>
</template>

<style lang="stylus">

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
  background-color: #c52035;

}
.grid-item {
    height: 250px;
    width: 250px;
    flex-basis: 20%;
    -ms-flex: auto;
    position: relative;
    box-sizing: border-box;
    // margin: 8px;
    padding: 8px;
    display: flex;
    text-align: center;
    align-items : center;
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
