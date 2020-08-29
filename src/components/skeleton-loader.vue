<template>
  <div>
    <div class="justify-center items-center grid lg:grid-cols-5 grid-cols-2 md:grid-cols-3">
      <div 
           v-for="skeletoncount in 5"
      :key="skeletoncount"
      
      class="skeletoncomp mx-auto self-center items-center  flex flex-col justify-center">
        <div class="skeletonimage mx-auto"></div>
        <div class="skeletonayir flex mx-auto flex-col">
          <div class="flex skeletondetails text-gray-700">
            <div class="skeletonblocktag"></div>
            <div class="skeletonblocktag"></div>
            <div class="skeletonblocktag"></div>
          </div>

          <div class="flex skeletontitle">
            <div class="skeletonblock1"></div>
          </div>
          <div class="flex skeletontitle">
            <div class="skeletonblock1"></div>
          </div>

          <div class="flex skeletondetails2">
            <div class="skeletonblock2"></div>
          </div>

          <div class="flex skeletontime">
            <div class="skeletonblocktime"></div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import { library } from "@fortawesome/fontawesome-svg-core";
import { faUserSecret } from "@fortawesome/free-solid-svg-icons";

library.add(faUserSecret);

export default {};
</script>

<style lang="scss">
$radius: 10px;
$mx: 0 10px 0 10px;
$my: 3px 0 3px 0;

.skeletoncomp {
  width: 100%;
  cursor: pointer;
  min-height: 310px;
  max-height: 310px;

  border-radius: $radius;

  overflow: hidden;
  justify-content: center;
}

.skeletonayir {
  margin-top: -50px;
  z-index: 2;
  background-color: white;
  width: 85% !important;
  height: 130px !important;
  border-radius: $radius;
  background-color: rgb(238, 236, 236);
  border: 1px solid rgb(212, 212, 212);
  * {
    margin: 5px 0 5px 0;
  }
}

.skeletonimage {
  max-height: 200px;
  min-height: 200px;
  max-width: 95%;
  min-width: 95%;
  border-radius: $radius;
  font-size: 12px;
 margin:4px;

  padding: 3px 10px 3px 10px;
  width: 125px;
  height: 70%;
  background-color: rgb(238, 236, 236);
  background: linear-gradient(
    90deg,
    rgba(160, 160, 160, 0.5) 0%,
    rgba(160, 160, 160, 0.3) 25%,
    rgba(160, 160, 160, 0.5) 50%,
       rgba(160, 160, 160, 0.3) 75%,
          rgba(160, 160, 160, 0.5) 100%,
  );
  background-size: 1500px  ;
  animation: shine infinite 50s linear forwards;
  border-radius: 5px;
  background-repeat: repeat;
}

.skeletonblocktag {
 margin:4px;

  padding: 3px 5px 3px 5px;
  width: 40px !important;
  height: 70%;
  background: rgb(160, 160, 160);
  background: linear-gradient(
    135deg,
    rgba(160, 160, 160, 0.5) 0%,
    rgba(160, 160, 160, 0.3) 50%,
    rgba(160, 160, 160, 0.5) 100%
  );

  border-radius: 5px;
  animation: shine infinite 600s linear;
  background-repeat: repeat;
}

.skeletonblock1 {
  font-size: 12px;
 margin:4px;

  padding: 3px 10px 3px 10px;
  width: 90%;
  height: 70%;
  background: rgb(160, 160, 160);
  background: linear-gradient(
    135deg,
    rgba(160, 160, 160, 0.5) 0%,
    rgba(160, 160, 160, 0.3) 50%,
    rgba(160, 160, 160, 0.5) 100%
  );

  animation: shine infinite 90s linear forwards;
  border-radius: 5px;
  background-repeat: repeat;
}

.skeletonblock2 {
  font-size: 12px;
 margin:4px;

  padding: 3px 10px 3px 10px;
  width: 125px;
  height: 70%;
  background: rgb(160, 160, 160);
  background: linear-gradient(
    135deg,
    rgba(160, 160, 160, 0.5) 0%,
    rgba(160, 160, 160, 0.3) 50%,
    rgba(160, 160, 160, 0.5) 100%
  );

  animation: shine infinite 200s linear forwards;
  border-radius: 5px;
  background-repeat: repeat;
}

.skeletonblocktime {
  text-transform: capitalize;
  font-size: 12px;
  margin-left: auto;
  margin-right: 24px;

  padding: 3px 10px 3px 10px;
  width: 20%;
  height: 70%;
  background: rgb(160, 160, 160);
  background: linear-gradient(
    135deg,
    rgba(160, 160, 160, 0.5) 0%,
    rgba(160, 160, 160, 0.3) 50%,
    rgba(160, 160, 160, 0.5) 100%
  );

  border-radius: 5px;
  animation: shine infinite 500s linear;

  background-repeat: repeat;
}

@keyframes shine {
  0% {
    background-position: -8000px;
  }
  100% {
    background-position: 8000px;
  }
}
</style>