<script setup>
 import { ref } from 'vue';
 import Rainforest from '@/assets/img/img/Rainforest.jpeg'
 import build from '@/assets/img/img/build.jpeg'
 import health from '@/assets/img/img/health.webp'
 import water from '@/assets/img/img/water.jpeg'
 import refugee from '@/assets/img/img/refugee.jpeg'
 import library from '@/assets/img/img/library.jpeg'

  const showCam = ref(false)
 const showCampaignDesc = ref(false)
 const selectedCampaign = ref({})
 
 const Campaigns = [
    {   
        title:"Save the Rainforest",
        img:Rainforest,
        description:`Save the Rainforest is a crucial campaign aimed at combating the rapid deforestation of the Amazon. Our goal is to raise $100,000 to fund reforestation, protect endangered species, and advocate for environmental conservation. Your contribution will directly support tree planting efforts, wildlife protection, and education programs for local communities. Together, we can preserve this vital ecosystem, known as the “lungs of the Earth,” and help combat climate change.`,
        goal:"Goal:$50,000",
        raised:"Raised:$30,000",
        donors:"Donors:120",
        progress:90
    },
    {
        title:"Help build a school in Africa",
        img:build,
        description:`Education is the key to breaking the cycle of poverty, but many children in rural African communities lack access to schools. We aim to raise $75,000 to build a fully equipped school that will serve hundreds of children who currently have no place to learn. The funds will cover the construction of classrooms, the purchase of school supplies, and the hiring of qualified local teachers. This school will provide not just education, but also a safe space where children can grow, dream, and build a better future. Your contribution will have a lasting impact on the lives of these children, offering them opportunities they otherwise wouldn’t have and empowering them to shape their own destiny.`,
        goal:"Goal:$70,000",
        raised:"Raised:$65,000",
        donors:"Donors:200",
        progress:170
    },
    {
        title:"Community Health Clinic",
        img:health,
        description:`In many underserved areas, access to healthcare is scarce, and preventable diseases run rampant. This campaign seeks to raise $50,000 to build a community health clinic that will offer essential medical services to thousands of people. With your help, we can provide vaccinations, maternal care, and emergency treatments to families who need them the most. The funds will be used to equip the clinic with necessary medical supplies, hire healthcare professionals, and maintain a clean, safe facility. By donating, you’ll help improve the overall health and well-being of an entire community, reducing mortality rates and giving people the medical attention they need to thrive.`,
        goal:"Goal:$100,000",
        raised:"Raised:$45,000",
        donors:"Donors:95",
        progress: 100 
    },
    {
        title:"Rebuild the Community Library",
        img:library,
        description:`Our town’s community library was more than just a building—it was a place where children learned to read, students came to study, and neighbors connected over shared knowledge. Unfortunately, it was destroyed by recent floods, leaving a gap in our community’s educational resources. We are raising $30,000 to rebuild this vital institution from the ground up. The funds will be used to reconstruct the facility, replace damaged books and computers, and create an inviting space for people of all ages to learn and grow. With your support, we can restore this crucial resource and continue to provide opportunities for education, personal development, and community engagement.`,
        goal:"Goal:$15,000",
        raised:"Raised:$9,000",
        donors:"Donors:85",
        progress: 100
    },
    {
        title:"Clean water for rural Vilages",
        img:water,
        description:`Access to clean water is a basic human right, yet millions of people in rural areas are forced to drink from contaminated sources, leading to waterborne illnesses and preventable deaths. This campaign aims to raise $40,000 to bring clean, safe water to rural villages by constructing wells and installing water filtration systems. With your support, we can drastically improve the health and quality of life for entire communities. These funds will not only provide clean water but also educate local villagers on maintaining these systems and practicing proper sanitation, ensuring a long-term, sustainable solution to the water crisis. Your donation will directly help reduce sickness and mortality, allowing these villages to thrive.`,
        goal:"Goal:$25,000",
        raised:"Raised:$18,000",
        donors:"Donors:150",
        progress: 120
    },
    {
        title:"Medical supplies for Refugee",
        img:refugee,
        description:`Refugee camps around the world are overcrowded and under-resourced, leaving thousands without access to basic medical care. Many are struggling to survive without the medicines and equipment they need. We are raising $60,000 to provide life-saving medical supplies to these vulnerable populations. Your donation will help deliver essential items like bandages, antibiotics, clean syringes, and hygiene kits to refugee camps in conflict zones. By contributing, you’ll be directly aiding those who have lost everything to war and persecution, giving them a chance to recover and rebuild their lives in safety. Every dollar raised will help save lives, offering hope and healing to those in desperate need.`,
        goal:"Goal:$50,000",
        raised:"Raised:$42,000",
        donors:"Donors:300",
        progress: 150
    },
 ]
 function showCampaignDescription(Campaign) {
  selectedCampaign.value = Campaign;
  showCampaignDesc.value = true;
}
</script>

<template>
    <div>
     <button @click="showCam = ! showCam" class="px-6 py-4 bg-blue-500
      transition duration-300 ease-out hover:scale-110
       text-white rounded-full text-xl mb-4 w-[800px] mt-6 ml-[400px]">Campaign Listings</button>
    
    <section v-if="showCam" class="flex flex-wrap justify-center gap-4 text-center ">

    <div v-for="(Campaign , index ) in Campaigns" :key="index"
     class="w-64 bg-yellow-300 border rounded-lg shadow-md p-4 flex
      flex-col justify-between mt-10 transition duration-300 ease-out hover:scale-110 cursor-pointer">

    
        <img :src="Campaign.img" alt="image" class="w-full h-48 object-cover mb-4 rounded-lg" />
      
        <h3 class="text-xl font-bold">{{ Campaign.title }}</h3>
        <p>{{ Campaign.goal }}</p>
        <p>{{ Campaign.raised }}</p>
        <p>{{ Campaign.donors }}</p>
    
        
       
        <div class="w-full bg-gray-200 rounded-full h-2 mb-4 ml-4" style="width: 190px;">
            <div class="bg-green-500 h-2 rounded-full" :style="{width: Campaign.progress + 'px'}"></div>
        </div>
        
        <button @click="showCampaignDescription(Campaign)" class="px-6 py-2 transition duration-300 ease-out hover:scale-110 bg-blue-500 text-white rounded">View Campaign</button>
    </div>
    
</section>

<div v-if="showCampaignDesc" class="fixed top-0 left-0 w-full h-full bg-gray-500 bg-opacity-50 flex justify-center items-center ">
      <div class="bg-green-500 rounded-lg shadow-md font-serif p-4 w-1/2">
        <h2 class="text-4xl font-bold mb-10 text-center">{{ selectedCampaign.title }}</h2>
        <p class=" text-xl mb-4 ">{{ selectedCampaign.description }}</p>
        <button @click="showCampaignDesc = false" class="px-6 py-2 bg-blue-700 ml-[350px] text-white transition duration-300 ease-out hover:scale-110 rounded">Close</button>
      </div>
    </div>

</div>

</template>