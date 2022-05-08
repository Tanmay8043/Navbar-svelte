<script>
  import { selectedStore } from "./stores"
  import { onMount } from 'svelte';
 
  var list
  onMount(() => {
     list = document.querySelectorAll('.list');
  });
 
  function activeLink(){
    for(const e of list){
      e.classList.remove('active')
    };
    this.classList.add('active');
  }
</script>

<div class="bg-gray-800 relative text-gray-700 min-h-screen min-w-screen flex items-center justify-center">
  <div class="navigation flex justify-center items-center bg-gray-50 px-12 pt-5 sm:rounded-xl h-16 fixed bottom-6 w-full sm:w-auto">
    <ul class="flex flex-row items-center justify-center gap-6 sm:gap-12 relative">
      <li class="list relative z-10 active" on:click={activeLink} on:click={()=>{selectedStore.set("Home")}}>
        <a 
          class="flex flex-col items-center relative justify-center ease-in-out duration-600 group focus:outline-none "
          href="#!">
          <div class="icon relative w-10 h-10 leading-8 transition duration-[400ms] ease-in ring-gray-800 rounded-full">
            <svg xmlns="http://www.w3.org/2000/svg" style={$selectedStore=='Home'?'fill:#3868A8;':'fill:#a0aec0;'} width="40" height="40" fill="currentColor" class="bi bi-house ease-in" viewBox="0 0 16 16"> <path fill-rule="evenodd" d="M2 13.5V7h1v6.5a.5.5 0 0 0 .5.5h9a.5.5 0 0 0 .5-.5V7h1v6.5a1.5 1.5 0 0 1-1.5 1.5h-9A1.5 1.5 0 0 1 2 13.5zm11-11V6l-2-2V2.5a.5.5 0 0 1 .5-.5h1a.5.5 0 0 1 .5.5z"/> <path fill-rule="evenodd" d="M7.293 1.5a1 1 0 0 1 1.414 0l6.647 6.646a.5.5 0 0 1-.708.708L8 2.207 1.354 8.854a.5.5 0 1 1-.708-.708L7.293 1.5z"/> </svg>
          </div>
          <span class="text-center text absolute text-gray-800 font-semibold text-sm translate-y-6 transition duration-[400ms] ease-in opacity-0">
            Home
          </span>
        </a>
      </li>
      <li class="list relative z-10" on:click={activeLink} on:click={()=>{selectedStore.set("Explore")}}>
        <a 
          class="flex flex-col relative items-center justify-center ease-in-out duration-600 group focus:outline-none "
          href="#!">
          <div class="icon w-10 h-10 relative leading-8 transition duration-[400ms] ease-in ring-gray-800 rounded-full">
            <svg xmlns="http://www.w3.org/2000/svg" style={$selectedStore=='Explore'?'fill:#3868A8;':'fill:#a0aec0;'} width="40" height="40" fill="currentColor" class="bi bi-hash ease-in" viewBox="0 0 16 16"> <path d="M8.39 12.648a1.32 1.32 0 0 0-.015.18c0 .305.21.508.5.508.266 0 .492-.172.555-.477l.554-2.703h1.204c.421 0 .617-.234.617-.547 0-.312-.188-.53-.617-.53h-.985l.516-2.524h1.265c.43 0 .618-.227.618-.547 0-.313-.188-.524-.618-.524h-1.046l.476-2.304a1.06 1.06 0 0 0 .016-.164.51.51 0 0 0-.516-.516.54.54 0 0 0-.539.43l-.523 2.554H7.617l.477-2.304c.008-.04.015-.118.015-.164a.512.512 0 0 0-.523-.516.539.539 0 0 0-.531.43L6.53 5.484H5.414c-.43 0-.617.22-.617.532 0 .312.187.539.617.539h.906l-.515 2.523H4.609c-.421 0-.609.219-.609.531 0 .313.188.547.61.547h.976l-.516 2.492c-.008.04-.015.125-.015.18 0 .305.21.508.5.508.265 0 .492-.172.554-.477l.555-2.703h2.242l-.515 2.492zm-1-6.109h2.266l-.515 2.563H6.859l.532-2.563z"/> </svg>
          </div>
          <span class="text-center text absolute text-gray-800 font-semibold text-sm translate-y-6 transition duration-[400ms] ease-in opacity-0">
            Explore
          </span>
        </a>
      </li>
      <li class="list relative z-10" on:click={activeLink} on:click={()=>{selectedStore.set("Chat")}}>
        <a 
          class="flex flex-col items-center justify-center relative ease-in-out duration-600 group focus:outline-none "
          href="#!">
          <div class="icon w-10 h-10 leading-8 relative transition duration-[400ms] ease-in ring-gray-800 rounded-full">
            <svg xmlns="http://www.w3.org/2000/svg" style={$selectedStore=='Chat'?'fill:#3868A8;':'fill:#a0aec0;'} width="38" height="38" class="ease-in" viewBox="0 0 16 16"> <path d="M14 1a1 1 0 0 1 1 1v8a1 1 0 0 1-1 1H4.414A2 2 0 0 0 3 11.586l-2 2V2a1 1 0 0 1 1-1h12zM2 0a2 2 0 0 0-2 2v12.793a.5.5 0 0 0 .854.353l2.853-2.853A1 1 0 0 1 4.414 12H14a2 2 0 0 0 2-2V2a2 2 0 0 0-2-2H2z"/> <path d="M3 3.5a.5.5 0 0 1 .5-.5h9a.5.5 0 0 1 0 1h-9a.5.5 0 0 1-.5-.5zM3 6a.5.5 0 0 1 .5-.5h9a.5.5 0 0 1 0 1h-9A.5.5 0 0 1 3 6zm0 2.5a.5.5 0 0 1 .5-.5h5a.5.5 0 0 1 0 1h-5a.5.5 0 0 1-.5-.5z"/> </svg></div>
          <span class="text-center text absolute text-gray-800 font-semibold text-sm translate-y-6 transition duration-[400ms] ease-in opacity-0">
            Messaging
          </span>
        </a>
      </li>
      <li class="list relative z-10" on:click={activeLink} on:click={()=>{selectedStore.set("Profile")}}>
        <a 
          class="flex flex-col relative items-center justify-center ease-in-out duration-600 group focus:outline-none "
          href="#!">
          <div class="icon w-10 h-10 relative leading-8 transition duration-[400ms] ease-in ring-gray-800 rounded-full">
            <svg xmlns="http://www.w3.org/2000/svg" style={$selectedStore=='Profile'?'fill:#3868A8;':'fill:#a0aec0;'} width="40" height="40" class="ease-in" viewBox="0 0 448 512"><path d="M272 304h-96C78.8 304 0 382.8 0 480c0 17.67 14.33 32 32 32h384c17.67 0 32-14.33 32-32C448 382.8 369.2 304 272 304zM48.99 464C56.89 400.9 110.8 352 176 352h96c65.16 0 119.1 48.95 127 112H48.99zM224 256c70.69 0 128-57.31 128-128c0-70.69-57.31-128-128-128S96 57.31 96 128C96 198.7 153.3 256 224 256zM224 48c44.11 0 80 35.89 80 80c0 44.11-35.89 80-80 80S144 172.1 144 128C144 83.89 179.9 48 224 48z"/></svg></div>
            <span class="text-center text absolute text-gray-800 font-semibold text-sm translate-y-6 transition duration-[400ms] ease-in opacity-0">
              Profile
            </span>
        </a>
      </li>
      <div class="indicator"></div>
    </ul>
  </div>
</div>

<style>
  .navigation ul li.active a .text{
    opacity: 100;
    transform: translateY(20px);
  }

  .navigation ul li.active a .icon{
    transform: translateY(-20px);
  }

  .navigation ul li{
    position: relative;
    list-style: none;
    width: 70px;
    height: 70px;
  }

  .indicator{
    position: absolute;
    width: 70px;
    height: 70px;
    background: #29fd53;
    top: -50%;
    border-radius: 50%;
    left: 1px;
    border: 6px solid rgb(31 41 55 );
    transition: 0.5s;
  }

  .indicator::before{
    content: '';
    position: absolute;
    top: 38%;
    left: -33px;
    width: 31px;
    height: 30px;
    background: transparent;
    border-top-right-radius: 28px;
    box-shadow: 1px -15px 0px 0 rgb(31, 41, 55);
  }
  .indicator::after{
    content: '';
    position: absolute;
    top: 38%;
    right: -33px;
    width: 31px;
    height: 30px;
    background: transparent;
    border-top-left-radius: 28px;
    box-shadow: -1px -15px 0px 0 rgb(31, 41, 55);
  }
  .navigation ul li:nth-child(1).active ~ .indicator{
    transform: translateX(calc(120px * 0));
  }
  .navigation ul li:nth-child(2).active ~ .indicator{
    transform: translateX(calc(95px * 1));
  }
  .navigation ul li:nth-child(3).active ~ .indicator{
    transform: translateX(calc(93px * 2));
  } 
  .navigation ul li:nth-child(4).active ~ .indicator{
    transform: translateX(calc(94px * 3));
  } 
  @media (min-width: 640px) { 
    .navigation ul li:nth-child(1).active ~ .indicator{
    transform: translateX(calc(120px * 0));
  }
  .navigation ul li:nth-child(2).active ~ .indicator{
    transform: translateX(calc(117px * 1));
  }
  .navigation ul li:nth-child(3).active ~ .indicator{
    transform: translateX(calc(117px * 2));
  } 
  .navigation ul li:nth-child(4).active ~ .indicator{
    transform: translateX(calc(118px * 3));
  } 
   }
  
  
</style>