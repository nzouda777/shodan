<script setup>
import MixesInspiredBy from '../components/MixesInspiredBy.vue'
import MultiArtistSelect from '../components/MultiArtistSelect.vue'
import CustomCarousel from '../components/CustomCarousel.vue'
import HighLights from '../components/HighLights.vue'
</script>

<template>
  <div class="max-w-[1500px] mx-auto">
    <div class="px-8 mt-8 min-w-[800px] w-full">
      <div class="text-white text-xl font-semibold inline-block">
        Mixes inspired by...
        <div class="text-sm font-light text-[#A2A2AD]">Discover new tracks similar to your favourites</div>
      </div>
      <div class="py-3"></div>
      <div class="flex justify-between w-full gap-8">
        <div class="xl:w1/3 w-1/2 text-white">
          <MixesInspiredBy
            class="pb-1.5"
            text="Vampire (feat. Oli Sykes of Bring Me The Horizon)"
            by="Ic3peak"
            to="/artist"
            image="https://picsum.photos/id/147/300/300"
          />
          <MixesInspiredBy
            class="pb-1.5"
            text="Deutchland"
            by="Ramstein"
            to="/artist"
            image="https://picsum.photos/id/166/300/300"
          />
          <MixesInspiredBy
            class="pb-1.5"
            text="Fallout"
            by="Masked Wolf"
            to="/artist"
            image="https://picsum.photos/id/127/300/300"
          />
        </div>
        <div class="xl:w1/3 w-1/2 text-white">
          <MixesInspiredBy
            class="pb-1.5"
            text="Bad Life"
            by="Sigrid"
            to="/artist"
            image="https://picsum.photos/id/211/300/300"
          />
          <MixesInspiredBy
            class="pb-1.5"
            text="Dystopia"
            by="Megadeth"
            to="/artist"
            image="https://picsum.photos/id/123/300/300"
          />
          <MixesInspiredBy
            class="pb-1.5"
            text="Can You fell My Heart"
            by="Bring Me the Horizon"
            to="/artist"
            image="https://picsum.photos/id/94/300/300"
          />
        </div>
        
        <div class="xl:w1/3 xl:block hidden text-white">
          <MixesInspiredBy
            class="pb-1.5 "
            text="pray for plagues"
            by="bring me the horizon"
            to="/artist"
            image="https://picsum.photos/id/201/300/300"
          />
          <MixesInspiredBy
            class="pb-1.5"
            text="candy truck / you expected"
            by="bring me the horizon"
            to="/artist"
            image="https://picsum.photos/id/222/300/300"
          />
          <MixesInspiredBy
            class="pb-1.5"
            text="l'enfant sauvage"
            by="gojira"
            to="/artist"
            image="https://picsum.photos/id/212/300/300"
          />
        </div>
      </div>
    </div>
    <div class="px-8 mt-8 min-w-[800px]">
      <div class="text-white text-xl font-semibold inline-block">
        Made for you
      </div>
      <div class="py-3"></div>
      <div class="flex justify-start gap-7">
        <MultiArtistSelect
          class="w-1/4"
          category="daily"
          text="Featuring bring me the horizon, our last night, bad omens, the retaliators"
          to="/artist"
          :images="{
            one: 'https://picsum.photos/id/45/300/300',
            two: 'https://picsum.photos/id/55/300/300',
            three: 'https://picsum.photos/id/54/300/300',
            four: 'https://picsum.photos/id/76/300/300'
          }"
        />
        <MultiArtistSelect
          class="w-1/4"
          category="daily"
          text="Featuring Metallica, jessye Norman, Dresdener Philharmonie, San francisco symphony"
          to="/artist"
          :images="{
            one: 'https://picsum.photos/id/100/300/300',
            two: 'https://picsum.photos/id/154/300/300',
            three: 'https://picsum.photos/id/354/300/300',
            four: 'https://picsum.photos/id/176/300/300'
          }"
        />
        <MultiArtistSelect
          class="w-1/4"
          category="daily"
          text="Featuring rick ross, justin bieber, dj khaled, drake"
          to="/artist"
          :images="{
            one: 'https://picsum.photos/id/13/300/300',
            two: 'https://picsum.photos/id/12/300/300',
            three: 'https://picsum.photos/id/11/300/300',
            four: 'https://picsum.photos/id/16/300/300'
          }"
        />
         <MultiArtistSelect
          class="w-1/4"
          category="daily"
          text="Featuring machine gun kelly, girlfriends, mad sun, christian gates"
          to="/artist"
          :images="{
            one: 'https://picsum.photos/id/130/300/300',
            two: 'https://picsum.photos/id/124/300/300',
            three: 'https://picsum.photos/id/114/300/300',
            four: 'https://picsum.photos/id/116/300/300'
          }"
        />
      </div>
    </div>
    <div class="px-8 mt-8 min-w-[800px]">
      <div class="py-3"></div>

      <p class="text-center pb-6 text-[#D1D1D6] text-sm">
        Debloque le niveau en choisissant tes artiste favories pour ameliorer les recommendations
      </p>
      <div class="flex justify-center gap-7 w-full">
        <div class="flex items-center justify-center relative">
          <img 
            class="absolute -left-36 rounded-full z-0 cursor-pointer"
            src="https://i.discogs.com/Yld7gFqYu63hTW3zbjMjHhvaJmtWe1w_n6c62rZJjRQ/rs:fit/g:sm/q:40/h:300/w:300/czM6Ly9kaXNjb2dz/LWRhdGFiYXNlLWlt/YWdlcy9BLTExNzgz/MzktMTY0MzQwMzky/NS01OTg4LmpwZWc.jpeg" 
            width="100"
          >
          <img 
            class="absolute -left-[80px] rounded-full z-10 cursor-pointer"
            src="https://sortir-prod.s3-eu-west-1.amazonaws.com/uploads/events/covers/medium/6d2ec908230a6a99a1e2a5871704ad02a561805b.jpg?1639564506" 
            width="115"
          >
          <img 
            class=" rounded-full z-20 cursor-pointer"
            src="https://i.pinimg.com/564x/d5/ef/9a/d5ef9af761e067af037562228e4871c8.jpg" 
            width="160"
            height="160"
          >
          <img 
            class="absolute -right-[80px] rounded-full z-10 cursor-pointer"
            src="https://www.melty.fr/wp-content/uploads/meltyfr/2022/11/316557213_620970943113491_1516803408329280955_n-300x300.jpg" 
            width="115"
          >
          <img 
            class="absolute -right-36 rounded-full z-0 cursor-pointer"
            src="https://live.staticflickr.com/7247/7541649624_e9d2038079_n.jpg" 
            width="100"
          >
        </div>
      </div>
      <div class="w-full flex justify-center p-3">
        <button
          type="button"
          class="text-white text-[15px] font-semibold rounded-full bg-[#EF5465] hover:bg-[#d8384a] px-8 py-2 text-center"
        >
          Add Artists
        </button>
      </div>
    </div>
    <div class="mt-8 min-w-[800px]">
      <CustomCarousel 
        category="New releases for you"
        :data="[
          {url: 'https://cdn.justjared.com/wp-content/uploads/headlines/2023/02/rihanna-streaming.jpg', song: 'Foregone', by: 'Rihanna', releasedOn: '14/07/2023'},
          {url: 'https://media.resources.festicket.com/image/300x300/center/top/filters:quality(70)/www/artists/GIMS.jpg', song: 'Dark Waters', by: 'Gims', releasedOn: '14/07/2023'},
          {url: 'https://sansrefrain.fr/wp-content/uploads/import-images/images_artistes/artiste-15586.jpg', song: 'Foregone', by: 'Tiakola', releasedOn: '14/07/2023'},
          {url: 'https://cdn.justjared.com/wp-content/uploads/headlines/2023/02/rihanna-streaming.jpg', song: 'Foregone', by: 'Rihanna', releasedOn: '14/07/2023'},
          {url: 'https://media.resources.festicket.com/image/300x300/center/top/filters:quality(70)/www/artists/GIMS.jpg', song: 'Dark Waters', by: 'Gims', releasedOn: '14/07/2023'},
          {url: 'https://sansrefrain.fr/wp-content/uploads/import-images/images_artistes/artiste-15586.jpg', song: 'Foregone', by: 'Tiakola', releasedOn: '14/07/2023'},
          {url: 'https://cdn.justjared.com/wp-content/uploads/headlines/2023/02/rihanna-streaming.jpg', song: 'Foregone', by: 'Rihanna', releasedOn: '14/07/2023'},
          {url: 'https://media.resources.festicket.com/image/300x300/center/top/filters:quality(70)/www/artists/GIMS.jpg', song: 'Dark Waters', by: 'Gims', releasedOn: '14/07/2023'},
          {url: 'https://sansrefrain.fr/wp-content/uploads/import-images/images_artistes/artiste-15586.jpg', song: 'Foregone', by: 'Tiakola', releasedOn: '14/07/2023'},
          {url: 'https://cdn.justjared.com/wp-content/uploads/headlines/2023/02/rihanna-streaming.jpg', song: 'Foregone', by: 'Rihanna', releasedOn: '14/07/2023'},
          {url: 'https://media.resources.festicket.com/image/300x300/center/top/filters:quality(70)/www/artists/GIMS.jpg', song: 'Dark Waters', by: 'Gims', releasedOn: '14/07/2023'},
          {url: 'https://sansrefrain.fr/wp-content/uploads/import-images/images_artistes/artiste-15586.jpg', song: 'Foregone', by: 'Tiakola', releasedOn: '14/07/2023'}
        ]"
      />
    </div>
    <div class="px-8 mt-8 min-w-[800px]">
      <div class="text-white text-xl font-semi-bold inline-block">
        Highlights
      </div>
      <div class="py-3"></div>
      <div class="flex items-center gap-8">
        <div class="rounded-lg w-1/2">
          <HighLights 
            by="Damso"
            song="Peur d'etre sobre"
            image="https://picsum.photos/id/128/800/300"
          />
        </div>
        <div class="rounded-lg w-1/2">
          <HighLights 
            by="Mozart"
            song="Symphonie 5"
            image="https://picsum.photos/id/177/800/300"
          />
        </div>
      </div>
    </div>
    <div class="mt-8 min-w-[800px]">
      <CustomCarousel 
        category="New releases for you"
        :data="[
          {url: 'https://picsum.photos/id/14/300/300', song: 'Foregone', by: 'Rihanna', releasedOn: '14/07/2023'},
          {url: 'https://picsum.photos/id/30/300/300', song: 'Dark Waters', by: 'Gims', releasedOn: '14/07/2023'},
          {url: 'https://sansrefrain.fr/wp-content/uploads/import-images/images_artistes/artiste-15586.jpg', song: 'Foregone', by: 'Tiakola', releasedOn: '14/07/2023'},
          {url: 'https://picsum.photos/id/12/300/300', song: 'Foregone', by: 'Rihanna', releasedOn: '14/07/2023'},
          {url: 'https://picsum.photos/id/38/300/300', song: 'Dark Waters', by: 'Gims', releasedOn: '14/07/2023'},
          {url: 'https://sansrefrain.fr/wp-content/uploads/import-images/images_artistes/artiste-15586.jpg', song: 'Foregone', by: 'Tiakola', releasedOn: '14/07/2023'},
          {url: 'https://picsum.photos/id/13/300/300', song: 'Foregone', by: 'Rihanna', releasedOn: '14/07/2023'},
          {url: 'https://picsum.photos/id/35/300/300', song: 'Dark Waters', by: 'Gims', releasedOn: '14/07/2023'},
          {url: 'https://sansrefrain.fr/wp-content/uploads/import-images/images_artistes/artiste-15586.jpg', song: 'Foregone', by: 'Tiakola', releasedOn: '14/07/2023'},
          {url: 'https://picsum.photos/id/19/300/300', song: 'Foregone', by: 'Rihanna', releasedOn: '14/07/2023'},
          {url: 'https://media.resources.festicket.com/image/300x300/center/top/filters:quality(70)/www/artists/GIMS.jpg', song: 'Dark Waters', by: 'Gims', releasedOn: '14/07/2023'},
          {url: 'https://sansrefrain.fr/wp-content/uploads/import-images/images_artistes/artiste-15586.jpg', song: 'Foregone', by: 'Tiakola', releasedOn: '14/07/2023'}
        ]"
      />
    </div>
  </div>
</template>
