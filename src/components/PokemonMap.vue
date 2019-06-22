<template>
  
    <div class="container">
      <h1>
        Pokemon Apocalypse Map
      </h1>
      <div class="row mt-5">
        <div class="col-md-9">
          <div class="imagewrap">
            <img src="../assets/pokemon-map-image.png" width="100%"/>
            <a class="pokeball sinnoh" 
            @mouseover="hovertext('sinnoh')"
            @mouseleave="goodbye()"
            >
            </a>

            <a class="pokeball hoenn" 
            @mouseover="hovertext('hoenn')"
            @mouseleave="goodbye()">
            </a>
          </div>
        </div>
        <div class="col-md-3 text-left">
          <b-card
            style="max-width: 20rem;"
            class="mb-2"
          >
          <b-card-text>
            Name: {{name }}
            <br>
            Description: {{ desc }}
            <br>
            Population: {{ pop }}
          </b-card-text>
        </b-card>
        </div>

      </div>
    </div>

</template>

<script>
export default {
  data(){
    return{
      show: false,
      regions:{
        sinnoh:{
          name: "Sinnoh",
          desc: "This is the city of Sinnoh! Pokemon live here.",
          pop: 1000
        },
        hoenn:{
          name: "Hoenn",
          desc: "This is the city of Hoenn! Pokemon live here.",
          pop: 3000
        },
      },
      name:"default name",
      desc:"default desc",
      pop:"default pop"
    }
        
  },
  methods:{
    hovertext(id){
      this.name = this.regions[id].name
      this.desc = this.regions[id].desc
      this.pop = this.regions[id].pop
    },
    goodbye(){
      this.name= "default name"
      this.desc= "default desc"
      this.pop="default pop"
    }
  }
}
</script>

<style>

.pokeball:hover{
  transform:scale(1.3,1.3)
  
}
.button:click{
  outline: none;
}
.pokeball {
  position:absolute;
  width:50px;
  height: 50px;
  background: transparent;
  border: none;
  cursor: pointer;
  background-image: url(../assets/Poke_Ball_Sprite.png);
  background-size: cover;
}

.sinnoh {
  top: 85%;
  left: 20%;
}

.hoenn {
  top: 55%;
  left: 30%;
}
.imagewrap {
  display:inline-block;
  position:relative;
  width:100%;
}

.map g:hover {
  fill: #fc0 !important;
  cursor: help;
}

.info_panel {
  background-color: rgba(255,255,255, .7);
  padding: .3em;
  font-size: .8em;
  font-family: Helvetica, Arial, sans-serif;
  position: absolute;
}

.info_panel::first-line {
   font-weight: bold;   
}
</style>

