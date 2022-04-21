<template>
  <div>
    <div id='header' class="bg-[url('/hero-bg.jpg')] px-20">
    <div id='menu' class="grid grid-cols-2 py-5">
      <div id='menu-left'>
        <img src="logo.png" class="w-[100px]" alt="">
      </div>
      <div id='menu-right'>
        <ul class="grid grid-cols-4 test-lg font-oswald text-white pt-10">
          <li>About Us</li>
          <li>Our Menu</li>
          <li>Locations</li>
          <li>Contacts</li>
        </ul>
      </div>
    </div>

    <div class="grid grid-cols-2">
      <img src="brain.jpg" class="pr-8 mt-3 mb-8" alt="">
      <div>
        <h1 class="text-2xl text-white text-center font-lilita mt-12">STEM</h1>
        <P class="text-white font-roboto font-light text-center">Malaysia Education Blueprint was initiated in 2011 with STEM as one of the priorities. STEM, the acronym for Science, Technology, Engineering and Mathematics is believed to be the key towards achieving a scientific and innovative society. The subjects of STEM are where students learn the skills to gather and study information (investigative skills of science), evaluate and make sense of information and last but not least, the analytical skills of mathematics.</P>

        <h1 class="text-2xl text-white text-center font-lilita mt-5">SPEEDMATHS</h1>
        <P class="text-white font-roboto font-light text-center">We aim to prepare our young generation for the future. Our SpeedMaths Programme provides students with strong foundation in Mathematics which is crucial in STEM education</P>
      </div>
    </div>
    </div>
    <div class="grid grid-cols-2 bg-blue-400 py-5">
      <div id='left'>
        <div class="text-center">
        <h1 class="text-3xl uppercase font-oswald pt-20">Abacus & MindMaths</h1>
        <p class="font-roboto font-light text-grey-500 py-5 px-8">ABACUS is a tool used to solve simple mathematical problem such as addition, subtraction, multiplication, and division. Solving mathematical problem using abacus enables our children to use both their hands. Since our right brain controls the left hand and left brain controls the right hand, this promotes the use of both the left brain and the right brain simultaneously. The stimulation of both brains means learning is enhanced, better concentration on a task, builds confidence and brings out the creativity.</p>
        <button class="font-oswald uppercase bg-red-500 text-white py-3 px-3 rounded rounded-lg">Explore</button>
        </div>
        </div>
      <img src="abacus.png" alt="">
    </div>
    <div class="grid grid-cols-2 bg-green-400 text-center">
      <img src="vedic.png" class="px-20 py-5" alt="">
      <div id='right-item-column'>
        <h1 class="text-3xl uppercase font-oswald pt-20 text-center">Vedic Maths</h1>
        <p class="font-roboto pt-5 pr-10 text-center">
          VEDIC MATHS has been a proven course to perform better in competitive examinations. These formula describe the way mind naturally works and are therefore a great help in directing the student to the appropriate method of solution.
        </p>
        <button class="font-oswald uppercase bg-red-500 text-white py-3 px-3 rounded rounded-lg">Explore</button>
      </div>
    </div>
    <div id='section-4' class="text-center">
      <h1 class="text-6xl font-oswald text-red-500 uppercase font-medium pt-8 pb-3">Our Programmes</h1>
      <p class="font-roboto">Our programmes are taught by experienced teachers</p>

      <div class="grid grid-cols-2 px-40 gap-5">
        <div id="left-item-colomn">
          <Item image='crispy-chicken.jpg'
          title='Crispy Chicken'
          description='crispy and nice'
          price='11.99'/>
          <Item image='ultimate-bacon.jpg'
          title='Ultimate Becon'
          description='Juicy'
          price='19.90'/>
          <Item image='img-06.jpg'
          title='Burger Set'
          description='A complete set'
          price='29.80'/>
        </div>
        <div id="right-item-column">
          <Item image='baa-baa.jpg'
          title='Baa Baa Blacksheep'
          description='American style'
          price='24.90'/>
          <Item image='double-burger.jpg'
          title='Double Burger'
          description='Nice and Tasty'
          price='18.90'/>
        </div>
      </div>

      <div class="grid grid-cols-12 font-oswald uppercase text-3xl text-yellow-800 px-40 gap-5">
        <div class="col-span-5 bg-cover bg-center bg-[url('/fries-bg-1.jpg')] pl-20 pb-10 pt-10">
          <h4>Get your <br>
          free</h4>
          <h4>Cheese <br>
          Fries</h4>
          <button class="uppercase bg-red-500 text-white text-1g px-8 py-3 mt-5">Claim Now</button>
        </div>
        <div class="col-span-7 bg-cover bg-center bg-[url('/burger-bg-1.jpg')] text-right pr-20 pl-20 pt-10">
          <h4>Crispy <br>
          Chicken</h4>
          <h4>Burger <br>
          is back</h4>
          <button class="uppercase bg-red-500 text-white text-1g px-8 py-3 mt-5">Claim Now</button>
        </div>
      </div>
      <div class="grid grid-cols-3 px-40 mt-5 gap-5">
        <img src="offer-1.jpg" alt=""><img src="offer-2.jpg" alt=""><img src="offer-3.jpg" alt="">
      </div>
      <div id='section -2'>
        <div class="grid grid-cols-3 text center gap-10 py-10 px-40 bg-yellow-500">
          <div>
            <svg
              xmlns="http://www.w3.org/2000/svg"
              class="h-20 w-20 stroke-1 mx-auto"
              fill="none"
              viewBox="0 0 24 24"
              stroke="currentColor"
              stroke-width="2"
            >
              <path stroke-linecap="round"
                stroke-linejoin="round"
                d="M5 3v4M3 5h4M6 17v4m-2-2h4m5-16l2.286 6.857L21 12l-5.714 2.143L13 21l-2.286-6.857L5 12l5.714-2.143L13 3z"
              />
            </svg>
            <h1 class="font-medium text-oswald text-2xl uppercase py-5">Original Recipes</h1>
            <p class="font-light">We use own secret recipes and only the best ingredients to make our burgers. Staring from patties, sauces, and even buns.</p>
          </div>
          <div>
            <svg xmlns="http://www.w3.org/2000/svg"
              class="h-20 w-20 mx-auto"
              fill="none"
              viewBox="0 0 24 24"
              stroke="currentColor"
              stroke-width="">
              <path stroke-linecap="round"
                stroke-linejoin="round"
                d="M21 15.546c-.523 0-1.046.151-1.5.454a2.704 2.704 0 01-3 0 2.704 2.704 0 00-3 0 2.704 2.704 0 01-3 0 2.704 2.704 0 00-3 0 2.704 2.704 0 01-3 0 2.701 2.701 0 00-1.5-.454M9 6v2m3-2v2m3-2v2M9 3h.01M12 3h.01M15 3h.01M21 21v-7a2 2 0 00-2-2H5a2 2 0 00-2 2v7h18zm-3-9v-2a2 2 0 00-2-2H8a2 2 0 00-2 2v2h12z"
            />
            </svg>
            <h1 class="font-medium text-oswald text-2xl uppercase py-5">Quality Foods</h1>
            <p class="font-light">We purchase our ingredients from the best suppliers daily to ensure the freshest quality of our burgers</p>
          </div>
          <div>
            <svg xmlns="http://www.w3.org/2000/svg"
              class="h-20 w-20 mx-auto"
              fill="none"
              viewBox="0 0 24 24"
              stroke="currentColor"
              stroke-width="1">
            <path stroke-linecap="round"
              stroke-linejoin="round"
              d="M13 10V3L4 14h7v7l9-11h-7z" />
            </svg>
            <h1 class="font-medium text-oswald text-2xl uppercase py-5">Fastest Delivery</h1>
            <p class="font-light">Burgers are best served while it's hot. We deliver to your door with our speedy delivery partners from the nearest outlets</p>
          </div>
        </div>

      </div>
      <div id='section-4' class="px-20 bg-gray-100 py-20">
        <div class="grid grid-cols-2 pt-5">
          <img src="about.png" alt="" class="pl-20">
          <h3 class="uppercase font-oswald text-5xl leading-snug pl-20 pr-4 pt-10">Nothing Brings People Together like a good burger</h3>
        </div>
        <p class="text-lg text-grey-500 mt-10">That's the philisophy that we always believe in. We're a family-owned and operated business, and we're proud to be a part of the community. We do our best to make sure that everyone's happy and having a good time</p>
        <p class="text-lg text-grey-500 mt-10">Burgers are what brought us together and what keeps us together. It's something that you can't put a price tag on. More importantly, we are interested in people. It's not about the food</p>
      </div>
      <div id="section-5" class="grid grid-cols-5 bg-yellow-500 text-amber-900">
        <div class="col-span-3 pl-20 pt-16 pb-16">
          <h4 class="font-oswald uppercase text-5xl">Download mobile app</h4>
          <h4 class="font-oswald uppercase text-6xl">Save up to 20%</h4>
          <p class="text-lg my-7">Bye bye long queues.Order before and your food will be ready in a flash. Enjoy the convenient of ordering food online at any time and from any location</p>
          <button><img src="/appstore.png" class="h-[50px]" alt=""></button>
          <button><img src="/googleplay.png" class="h-[50px]" alt=""></button>
        </div>
        <dir class="col-span-2"><img src="/eshop.png" class="-mt-10 h-[500px] object-cover" alt=""></dir>
      </div>
    </div>
  </div>
</template>
