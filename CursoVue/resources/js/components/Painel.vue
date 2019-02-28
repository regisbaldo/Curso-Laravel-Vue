<template>
  <div class="card card-default" v-bind:style="defineCor">
      <div class="card-header">{{titulo}}</div>

      <div class="card-body">
        <!-- slot é o container onde ficara as informações -->
          <slot></slot>
      </div>
  </div>
</template>

<script>
    export default {
            props:["titulo",'cor-css'],
            computed:{
              defineCor: function(){
                return  (this.corCss || "background-color: #9ee29e");
              }
            }
    }
</script>
