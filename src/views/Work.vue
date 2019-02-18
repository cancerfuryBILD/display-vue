<template>
  <div>
    <page-title :headline="headline"/>
    <div class="container category">
      <div class="filter">
        <label><input type="radio" v-model="selectedCategory" value="All" />All </label> / 
        <label><input type="radio" v-model="selectedCategory" value="Print" /> Print</label> / 
        <label><input type="radio" v-model="selectedCategory" value="Photography" /> Photography </label> / 
        <label><input type="radio" v-model="selectedCategory" value="Web" /> Web </label> / 
        <label><input type="radio" v-model="selectedCategory" value="Applications" /> Applications </label>
        <div class="layout" v-html="layoutSvg"></div>
      </div>
	
      <div class="list-images">
        <div v-for="(img, index) in filteredImgList" :key="index">
          <router-link to="#"><img :src="img.imgLocation" :alt="img.altTag"></router-link>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import PageTitle from '@/components/PageTitle.vue';
import img1 from '@/assets/img-1.png';
import img2 from '@/assets/img-2.png';
import img3 from '@/assets/img-3.png';
import img4 from '@/assets/img-4.png';
import img5 from '@/assets/img-5.png';
import img6 from '@/assets/img-6.png';
import img7 from '@/assets/img-7.png';
import img8 from '@/assets/img-8.png';
import img9 from '@/assets/img-9.png';

export default {
  name: "work",
  components: {
    PageTitle
  },
  data() {
    return {
       headline: 'Check out what I can do',
       categories: ['All ', ' Print ', ' Photography ', ' Web ', ' Applications'],
       layoutSvg: `<svg class="grid-view active-view" 
       xmlns="http://www.w3.org/2000/svg" 
       xmlns:xlink="http://www.w3.org/1999/xlink" 
       width="15" 
       height="15" 
       viewBox="0 0 15 15">
       <defs><path id="utska" d="M1129 329h6.033v5.929H1129zm8.946 0H1144v6.012h-6.054zm-8.946 8.905h6.012V344H1129zm8.967 0H1144V344h-6.033z"/>
       </defs><g><g transform="translate(-1129 -329)"><use fill="#737373" xlink:href="#utska"/></g></g></svg>
       <svg class="list-view"
       xmlns="http://www.w3.org/2000/svg" 
       xmlns:xlink="http://www.w3.org/1999/xlink" 
       width="15" 
       height="15" 
       viewBox="0 0 15 15">
       <defs><path id="xt56a" d="M1154 341h15v3h-15z"/><path id="xt56b" d="M1154 334.969h15V338h-15z"/><path id="xt56c" d="M1154 328.969h15V332h-15z"/>
       </defs><g><g transform="translate(-1154 -329)"><use fill="#737373" xlink:href="#xt56a"/></g><g transform="translate(-1154 -329)">
       <use fill="#737373" xlink:href="#xt56b"/></g><g transform="translate(-1154 -329)"><use fill="#737373" xlink:href="#xt56c"/></g></g></svg>`,
       
       imgList: [
         {
           imgLocation: img1,
           altTag: '3D Art',
           imgCategory: 'Print'
         },
         {
           imgLocation: img2,
           altTag: 'UI Components',
           imgCategory: 'Web'
         },
         {
           imgLocation: img3,
           altTag: 'Couple in love',
           imgCategory: 'Photography'
         },
         {
           imgLocation: img4,
           altTag: 'Smily face',
           imgCategory: 'Print'
         },
         {
           imgLocation: img5,
           altTag: 'Social Networks',
           imgCategory: 'Applications'
         },
         {
           imgLocation: img6,
           altTag: 'Jesus in love',
           imgCategory: 'Print'
         },
         {
           imgLocation: img7,
           altTag: 'Colored collage',
           imgCategory: 'Print'
         },
         {
           imgLocation: img8,
           altTag: 'Smoking gun',
           imgCategory: 'Photography'
         },
         {
           imgLocation: img9,
           altTag: 'Various graffiti',
           imgCategory: 'Print'
         }
       ],
       selectedCategory: "All"
    }
  },
  computed: {
		filteredImgList: function() {
			var vm = this;
			var category = vm.selectedCategory;
			
			if(category === "All") {
				return vm.imgList;
			} else {
				return vm.imgList.filter(function(img) {
					return img.imgCategory === category;
				});
			}
		}
	}
};
</script>

<style>
  .layout {
    float: right;
  }
  .layout svg {
    margin-left: 9px;
  }
  .category {
    padding-top: 40px;
    clear: right;
}
  .list-images {
      display: grid;
      grid-template-columns: 1fr 1fr 1fr;
      gap: 1.4em;
      margin-bottom: 249px;
      margin-top: 36px;
  }
  .list-images img {
      width: 100%;
  }
  .list-images img:hover {
      opacity: .3;
  }
  label [type='radio'] {
    display: none;
  }
  .filter {
    color:#8a8888;
    font-size: 1.1875rem;
    letter-spacing: .02rem;
  }
  .filter label {
        cursor: pointer;
  }
</style>
