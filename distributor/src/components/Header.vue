<template>
    <div class="pt-7 pb-7 mb-7 bg-dark bg-ellipses">
      <div class="container-fluid">
        <div class="row justify-content-center">
          <div class="col-8 text-center">
            <img v-bind:src="'data:image/png;base64,'+logo" />
            <h1 class="display-3 text-center text-white mt-4" v-text="title"/>
            
            <p class="lead text-center text-muted"><slot></slot></p>
          </div>
        </div>
      </div>
    </div>
</template>
<script>
export default {
    name:"Header",
    props:{
        logo:String,
        title:String,
        text:String
    }
}
</script>