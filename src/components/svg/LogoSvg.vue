<template>
  <svg
    xmlns="http://www.w3.org/2000/svg"
    viewBox="0 0 1000 1000"
    :fill="fill">
    <path
      d="M1000,600c0-55,0-200-200-200H400c-243,0-200,16-200-200H300c36,0,100,1,100,100H600C600,138,471,0,300,0H0V400c0,55,0,200,200,200H600c202,2,202,2,200,200H700c-36,0-100-1-100-100H400c0,162,129,300,300,300h300Z"
      transform="translate(0 0)"></path>
    <polyline points="0 1000 300 1000 300 800 200 800 200 700 0 700" opacity=".5"></polyline>
    <polyline points="1000 0 700 0 700 200 800 200 800 300 1000 300" opacity=".5"></polyline>
  </svg>
</template>

<script>
export default {
  name: 'LogoSvg',
  props: {
    fill: {
      type: String,
      default: '#fff',
    },
  },
};
</script>
