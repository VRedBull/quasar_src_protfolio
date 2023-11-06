<template>
  <q-page class="flex flex-center">
    <q-parallax
      src="https://i.pinimg.com/originals/72/a1/84/72a184aa7846cad0d5a82cf55dc3f406.jpg"
    >
      <!-- <h1 class="text-white">Portfolio</h1> -->
    
    <div>
      
    <img
      alt="Profile Pic"
      src="..\assets\linkedin_portfolio_image.jpg"
      style="width: 200px; height: 200px;position: relative;
    overflow: hidden;
    border-radius: 50%;"

    >
  </div>
  <br>
  <div class="profile_header">
    <h2 class="text-black">Software Developer</h2>
    
  </div>
  
  <div>
                <p class="text-black"><b>I am outgoing, dedicated, and open-minded. I get across to people and adjust to changes with ease.<br> I believe that a person should work on developing their professional skills and learning new things all the time.</b>
                </p>
                <q-separator color="grey" inset />
              </div>
                <div class="q-pa-md q-gutter-sm">
    <!-- -->
  </div>
</q-parallax>
  <!-- Cards from here -->
  <div class="q-pa-md row items-start q-gutter-md">
    
<!-- ABOUT ME CARD -->
    <q-card class="my-card" >
      <!-- <span class="q-focus-helper"></span> -->

      <q-parallax
        src="https://icon-library.com/images/about-me-icon/about-me-icon-27.jpg"
        :height="150"
      />

      <q-card-section>
        <div class="text-h6">About Me</div>
        <div class="text-subtitle2">Hobbies | Origin | Non-Tech Stuff</div>
      </q-card-section>
      <q-card-actions>
        <!-- <q-btn color="green" text-color="white" icon="person" rounded :ripple="{ color: 'black' }" glossy label="About" />  -->
        <!-- EXPANDING HERE -->
        <div class="q-pa-md q-gutter-sm">
    <q-btn label="About" text-color="white" icon="person" color="green" :ripple="{ color: 'black' }" rounded glossy @click="dialog = true" />

    <q-dialog
      v-model="dialog"
      persistent  
      :maximized="maximizedToggle"
      transition-show="slide-up"
      transition-hide="slide-down"
    >
      <q-card class="bg-primary text-white">
        <q-bar>
          <q-space />

          <q-btn dense flat icon="minimize" @click="maximizedToggle = false" :disable="!maximizedToggle">
            <q-tooltip v-if="maximizedToggle" class="bg-white text-primary">Minimize</q-tooltip>
          </q-btn>
          <q-btn dense flat icon="crop_square" @click="maximizedToggle = true" :disable="maximizedToggle">
            <q-tooltip v-if="!maximizedToggle" class="bg-white text-primary">Maximize</q-tooltip>
          </q-btn>
          <q-btn dense flat icon="close" v-close-popup>
            <q-tooltip class="bg-white text-primary">Close</q-tooltip>
          </q-btn>
        </q-bar>

        <q-card-section>
          <div class="text-h6">ABOUT ME</div>
        </q-card-section>

        <q-card-section class="q-pt-none">
          <!-- TABLE HERE -->
          <!-- <div class="q-pa-md">
    <q-table
      title="My Hobbies"
      :rows="rows"
      :columns="columns"
      row-key="name"
    />
  </div> -->
  <q-card class="my-card">
      <q-parallax
        src="https://www.burningcompass.com/countries/india/maps/odisha-district-map.jpg"
        :height="150"
      />

      <q-card-section>
        <div class="text-h6 text-black">Where I am from</div>
        <div class="text-subtitle2 text-black">Odisha</div>
      </q-card-section>
     
    </q-card>
    <br>
  <q-card class="my-card">
      <q-parallax
        src="https://m.media-amazon.com/images/I/71wh6WUTXxL.jpg"
        :height="150"
      />

      <q-card-section>
        <div class="text-h6 text-black">Sports I play </div>
        <div class="text-subtitle2 text-black">Football | Table Tennis | Taekwondo | Cricket</div>
      </q-card-section>
      
    </q-card>
<br>
    
    <q-card class="my-card">
      <q-parallax
        src="https://www.holidify.com/images/cmsuploads/compressed/shutterstock_649541308_20191010160155.png"
        :height="150"
      />

      <q-card-section>
        <div class="text-h6 text-black">What I Like to eat...</div>
        <div class="text-subtitle2 text-black">Pizza | Vada | Chicken | Biryani</div>
      </q-card-section>
      
    </q-card>
<br>
    <q-card class="my-card">
      <q-parallax
        src="https://images.theconversation.com/files/45159/original/rptgtpxd-1396254731.jpg?ixlib=rb-1.1.0&q=45&auto=format&w=1356&h=668&fit=crop"
        :height="150"
      />

      <q-card-section>
        <div class="text-h6 text-black">What I Like to do...</div>
        <div class="text-subtitle2 text-black">Read books | Sleep | Gym | Travel</div>
      </q-card-section>
      
    </q-card>

        </q-card-section>
      </q-card>
    </q-dialog>
  </div>
      </q-card-actions>
    </q-card>

    <!-- TECHNIACAL CARD -->
    <q-card class="my-card">
      <q-parallax
        src="https://t3.ftcdn.net/jpg/02/88/80/38/360_F_288803822_0CJ8L3gr6w6nGnUeje6pCllCX7s986xz.jpg"
        :height="150"
      />

      <q-card-section>
        <div class="text-h6">Technical Stuff</div>
        <div class="text-subtitle2">Skills | Projects | Acheivement | Education</div>
      </q-card-section>
      <q-card-actions>
        <div class="q-pa-md q-gutter-sm">
          <q-btn label="CLICK" color="green" icon="email" glossy rounded @click="alert = true" />
          <q-dialog v-model="alert">
      <q-card>
        <q-card-section>
          <div class="text-h6">Technical Stuff</div>
        </q-card-section>

        <q-card-section class="q-pt-none">
          <h5>My Education</h5>
  <ul>
    <li>10th - Holy Writ High School And Junior College, Badlapur</li>
    <li>12th - New English High School, Ulhasnagar</li>
    <li>B.E. - ISquareIT, Pune</li>
  </ul>
  <h5>My Skills</h5>
  <ul>
    <li>Flutter</li>
    <li>Java</li>
  </ul>
        </q-card-section>

        <q-card-actions align="right">
          <q-btn flat label="OK" color="primary" v-close-popup />
        </q-card-actions>
      </q-card>
    </q-dialog>
        </div>
      </q-card-actions>
    </q-card>

    <q-card class="my-card">
      <q-parallax :height="150">
      <template v-slot:media>
        <video width="720" height="440" poster="https://cdn.quasar.dev/img/polina.jpg" autoplay loop muted>
          <source type="video/mp4" src="..\assets\video.mp4">
        </video>
      </template>

      <h3 class="text-white">SPACE</h3>
    </q-parallax>

      <q-card-section>
        <div class="text-h6">Miscellaneous Stuff</div>
        <div class="text-subtitle2">Random Testing Playground</div>
      </q-card-section>
      <q-card-actions>
        <q-btn color="green" text-color="white" icon="announcement" rounded :ripple="{ color: 'black' }" glossy label=";D" /> 
      </q-card-actions>
    </q-card>
  </div>

  <div >
    
  </div>


</q-page>
<!-- <q-btn color="deep-orange" text-color="white" rounded icon="email" :ripple="{ color: 'black' }" glossy label="Contact" />  -->

</template>

<script >
import { defineComponent } from 'vue'
import { ref } from 'vue'

// export default defineComponent({
//   name: 'IndexPage'
// })


export default {
  setup () {
    return {
      dialog: ref(false),
      maximizedToggle: ref(true),
      alert: ref(false),
    
    }
  }
}



</script>
