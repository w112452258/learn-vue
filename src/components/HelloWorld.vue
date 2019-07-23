<template>
    <div>
      <div>
        <div class="div1">
          <ul v-for="t in title" v-bind:key="t.id"><li>{{ t }}</li></ul>
        </div>
      </div>
      <!-- <my-child test="我是父组件传过来的文本"></my-child> -->
      <div>
        <div>
          <my-child v-bind:imgUrl="book1.imgUrl" v-bind:title="book1.title" v-bind:details="book1.details"></my-child>
        </div>
        <div>
          <my-child v-bind:imgUrl="book2.imgUrl" v-bind:title="book2.title" v-bind:details="book2.details"></my-child>
        </div>
        <div>
          <my-child v-bind:imgUrl="book3.imgUrl" v-bind:title="book3.title" v-bind:details="book3.details"></my-child>
        </div>
      </div>
    </div>
</template>

<script>
import Child from "./Child.vue";
export default {
  name: "HelloWorld",
  components: {
    "my-child": Child
  },

  data() {
    return {
      test: "dgjkj",
      title: ["全部", "前端", "后端", "移动开发", "区块链", "通用"],
      book1: {
        imgUrl:
          "https://user-gold-cdn.xitu.io/2019/5/31/16b0ca4a5078c1f2?imageView2/1/w/200/h/280/q/95/format/webp/interlace/1",
        title: "[视频] Flutter 实战详解：企业级移动电商开发",
        details: "手把手教你一起用 Flutter 开发一个移动电商 App",
        author: "技术胖",
        message: "70小节 "
      },
      book2: {
        imgUrl:
          "https://user-gold-cdn.xitu.io/2019/5/31/16b0ca4a5078c1f2?imageView2/1/w/200/h/280/q/95/format/webp/interlace/1",
        title: "[视频] Flutter 实战详解：企业级移动电商开发",
        details: "手把手教你一起用 Flutter 开发一个移动电商 App",
        author: "技术胖",
        message: "70小节 "
      },
      book3: {
        imgUrl:
          "https://user-gold-cdn.xitu.io/2019/5/31/16b0ca4a5078c1f2?imageView2/1/w/200/h/280/q/95/format/webp/interlace/1",
        title: "[视频] Flutter 实战详解：企业级移动电商开发",
        details: "手把手教你一起用 Flutter 开发一个移动电商 App",
        author: "技术胖",
        message: "70小节 "
      }
    };
  }
};
// var vm = new Vue({
//   el: '#top',
//   data: {
//     title: ['全部', '前端', '后端']
//   }
// })

// Vue.component('book-details', {
//   props:
//   template: '<button v-on:click="count++">You clicked me {{ count }} times.</button>'
// })
</script>

<style>
li {
  font-size: 15px;
  float: left;
  list-style: none;
  width: 16%;
}
</style>
