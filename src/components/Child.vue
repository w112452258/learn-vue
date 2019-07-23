<template>
    <div>
        <div class="left">
          <a href="http://www.baidu.com">
            <div id="div2">
              <img :src="imgUrl">
            </div>
            <div>
              
              <div>
                <h4>{{ title }}</h4>
                <span class="">{{ details }}</span>
                <span>{{ author }}</span>
                <span>{{ message }}</span>
              </div>
            </div>
          </a>
        </div>
    </div>
</template>

<script>
export default {
    name: 'Child',
    props: ['imgUrl', 'title', 'details', 'author', 'message']
}
</script>

<style>

.left{
  float: left;
  width: 100%;
  height: 170px;
}

#div2 {
  float: left;
}

img {
  margin:20px 5px 15px 10px;
  width: 80px;
  height: 120px;
}

</style>
