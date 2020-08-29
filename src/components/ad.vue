<template>
  <div>
    <div class="justify-center items-center grid lg:grid-cols-5 grid-cols-2 md:grid-cols-3">


      <div
            v-for="ads in 12"
      :key="ads"
      
       class="adcomp  flex flex-col  justify-center">
      <div class="favit flex">  
          

      </div>
      <div class="adimage ">
        <img class="mx-auto"
          src="https://hecdnw.hemlak.com/8/1/9/5/8/7/5/3/23fabfe9-e5d0-427f-8dc3-a20b185b1338.jpg"
        />
        <div class="flex justify-between btns110">
<button class="leftbtn">left</button><button class="rightbtn ">right</button></div>
        </div>
        <div class="ayir flex mx-auto flex-col">
          <div class="flex addetails text-gray-700">
            <h2 class="addetailsit">3+1</h2>
            <h2  class="addetailsit">Ev</h2>
            <h2  class="addetailsit">11400 TL</h2>
          </div>

          <div class="flex adtitle mx-auto">
            <h1 class="mx-auto adtitle1 pl-2">Devremülk ev, öğrenciden öğrenciye</h1>
          </div>

          <div class="flex addetails2">
            <h2 class="addetailsit2">Afyonkarahisar / Dinar</h2>
          </div>

          <div class="flex adtime">
            <h2 class="ml-auto">2 gün önce</h2>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import { library } from '@fortawesome/fontawesome-svg-core'
import { faUserSecret } from '@fortawesome/free-solid-svg-icons'

library.add(faUserSecret)

export default {};
</script>

<style lang="scss">
$radius: 10px;
$mx: 0 10px 0 10px;
$my: 3px 0 3px 0;

.adcomp {
width:100%;
  cursor: pointer;
  min-height: 310px;
  max-height: 310px;

border-radius: $radius;

  justify-content: center;
}

.ayir {
  margin-top: -50px;
  z-index: 2;
  background-color: white;
  box-shadow: 1px 1px 3px 1px rgba(1, 1, 1, 0.2);

  width: 85% !important;
  height: 130px !important;
  border-radius: $radius;
}

.adcomp:hover  {
    .adimage{
        img{
  box-shadow: 1px 1px 5px 3px rgba(1, 1, 1, 0.2);
        }
}

.ayir {
  box-shadow: 1px 1px 5px 3px rgba(1, 1, 1, 0.2);
    
}
}

@keyframes slide-tr {
  0% {
    transform: translateY(0) translateX(0);
  }
  100% {
    transform: translateY(-14px);
  }
}

.adimage {
       max-height: 200px;
  min-height: 200px;
    img {
  object-fit: cover;

     border-radius: $radius;
       max-height: 200px;
  min-height: 200px;
 max-width: 94.6%;
  min-width: 94.6%;
  box-shadow: 1px 1px 3px 1px rgba(1, 1, 1, 0.2); }
}

.adimage:hover {
    z-index:3;
    .leftbtn , .rightbtn {
        display:flex;
    }
}

.adtitle {
  min-height: 45px;
  max-height: 45px;
  overflow: hidden;
}

.adtitle1:hover {

opacity:70%;
}

.addetails {
  * {
    text-transform: capitalize;
    font-size: 12px;
    margin: 5px;
    margin-left:10px;
    padding: 2px 8px 2px 8px;
    background-color:rgba(0, 128, 0, 0.363);
    border-radius: 5px;
    color: green;
    justify-content: center;
    text-align: center;
  }
}
.addetails2{
    align-items: center;
    
    
  * {
    text-transform: capitalize;
    font-size: 12px;
    margin-top:5px;
    margin-left:10px;
    border-radius: 5px;
    color: gray;

  }
}
.addetailsit2:hover {
opacity:75%;


}

.addetailsit:hover {
  background-color: rgba(0, 128, 0, 0.5);
}

h1 {
  font-weight: bold;
  font-size: 16px;
  color: #313131;

  text-transform: capitalize;
}

.adtime {
  margin: $mx;
  font-size: 10px;
  text-transform: capitalize;
  color: gray;
}

.favit {

margin-bottom:-36px;
z-index:2;
margin-left:4%;
color:black;
border-radius:50%;
background-color:white;
width:30px !important;
height:30px !important;
justify-content: center;
align-items:center;
}

.leftbtn {
    position:relative;
    bottom:120px;
    display:none;
    min-width: 40px;
    max-width: 40px;
    min-height: 40px;
    max-height: 40px;
    background-color:#A2CE99;
    
    color:green;
    border-radius:50%;
align-items: center;
justify-content: center;    
opacity:50%;
}

.rightbtn {
    position:relative;
    bottom:120px;
       display:none;
    min-width: 40px;
    max-width: 40px;
    min-height: 40px;
    max-height: 40px;
    background-color:#A2CE99;
    
    color:green;
    border-radius:50%;
align-items: center;
justify-content: center;    
opacity:50%;
}

.rightbtn:hover {
        opacity:100%;

}


.leftbtn:hover {
        opacity:100%;

}
</style>