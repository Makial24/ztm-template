<template>
<div>
  <div id="header" class="md:pl-40 pl-10 pr-20 py-5">
    <div id="menu" class="grid grid-cols-2">
      <div id="left">
        <img src="logo1.png" class="w-[90px]" alt="">
      </div>
      <div id="right">
        <ul class="grid md:grid-cols-3 uppercase font-oswald text-lg py-5">
          <li>Home</li>
          <nuxt-link to="/locations">Locations</nuxt-link>
          <li>Course</li>
        </ul>
      </div>
    </div>
  </div>
  <div class="grid md:grid-cols-2 bg-blue-300 pb-10">
    <div id="left">
      <img src="brain.jpg" class="md:pl-20 py-10" alt="">
    </div>
    <div id="right" class="text-center font-oswald text-blue-900 md:px-20 px-10 md:py-10">
      <h1 class="text-5xl">STEM</h1>
      <p class="text-lg text-justify"> Malaysia Education Blueprint was initiated in 2022 with STEM as one of the priorities. STEM, the acronym for Science, Technology, Engineering and Mathematics is believed to be the key towards achieving a scientific and innovative society.<br>
      The subjects of science, technology, engineering and mathematics are where students learn the skills to gather and study information (investigative skills of science), evaluate and make sense of information and last but not least, the analytical skills of mathematics. </p>
      <p class="text-lg text-justify">The human brain consists of the right brain and the left brain. The shapes of these two parts are similar, but differences have been gradually found in their functions. The left brain is also referred to as the digital brain. It controls reading and writing, calculation, and logical thinking. The right brain is referred to as the analog brain. It controls three-dimensional sense, creativity, and artistic senses.</p>
    </div>
  </div>
  <div id="section1" class="grid md:grid-cols-12 bg-green-200 py-10">
    <div class="col-span-7 md:pl-20">
      <img src="aboutus1.jpg" alt="">
    </div>
    <div class="col-span-5 md:px-20 px-10 pt-10">
      <h1 class="text-5xl font-oswald uppercase text-center">About us</h1>
      <p class="font-oswald text-lg text-justify">People commonly say that if you want to learn Mathematics, there is only one way to learn it i.e. by Practice because “Practice Makes Man Perfect”. Yes but practicing similar mathematical problem over and over again will cause boredom and loss of interest especially among children. Our programs are designed to solve this common problem, and on top of that, we are helping to stimulate the child’s mind with Brain Gym, and Memory Games.</p>
      <p class="font-oswald text-lg">We are the Malaysia's leading academy in Abacus and MindMaths. We trained thousands of students since 2010.</p>
    </div>
  </div>
  <div class="grid md:grid-cols-2 py-10">
    <div class="pb-10">
      <h1 class="text-4xl font-oswald uppercase text-center">Junior Level</h1>
      <img src="abacus.png" class="md:px-20" alt="">
      <p class="text-lg font-oswald md:px-10 px-5 text-center">Junior Level is specially designed for kids betweenn 6 years to 8 years old.</p>
      <p class="text-lg font-oswald md:px-10 px-5 text-center">Kids are taught to solve mathematical problems in addition and subtraction.</p>
    </div>
    <div>
      <h1 class="text-4xl font-oswald uppercase text-center">Senior Level</h1>
      <img src="vedic.png" class="md:px-20" alt="">
      <p class="test-lg font-oswald md:px-10 px-5 text-center">Senior Level is for pupil above the age of 11. Kids are taught to solve mathematical problems in multiplication, division, addition and subtraction</p>
    </div>
  </div>
  <div id="Footer">
    <div class="grid md:grid-cols-12 bg-yellow-200 py-10">
      <div class="col-span-2 md:pl-40 pl-20">
        <svg
        xmlns="http://www.w3.org/2000/svg"
        class="h-10 w-10 stroke-1"
        fill="none"
        viewBox="0 0 24 24"
        stroke="currentColor"
        stroke-width="2">
        <path stroke-linecap="round" stroke-linejoin="round" d="M3 5a2 2 0 012-2h3.28a1 1 0 01.948.684l1.498 4.493a1 1 0 01-.502 1.21l-2.257 1.13a11.042 11.042 0 005.516 5.516l1.13-2.257a1 1 0 011.21-.502l4.493 1.498a1 1 0 01.684.949V19a2 2 0 01-2 2h-1C9.716 21 3 14.284 3 6V5z" />
        </svg>
        <div>
          <a href="https://api.whatsapp.com/send/?phone=60162687192"><img src="icons.png" alt=""></a>
        </div>
      </div>
      <div class="col-span-4">
        <h2 class="text-2xl font-oswald pt-5">016-268 7192</h2>
      </div>
      <div class="col-span-6 pl-20">
        <a href="https://www.facebook.com/petterrayen.gnanapragasam"><img src="facebook2.png" alt=""></a>
      </div>
    </div>
  </div>
</div>
</template>
