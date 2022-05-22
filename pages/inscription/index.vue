<template>
  <main class="w-100">
    <Header />
    <div v-if="result" class="back">
      <div class="position-relative center-flex pop rounded shadow bg-white">
        <div class="">
          <h1 :class="scoreStyle" class="my-1 badge fs-3">Your score is : {{score}}</h1>
          <h1 :class="scoreStyle" class="my-1 badge fs-4">{{scoreMessage}}</h1>

        </div>
        <button
          @click="exit"
          class="
            btn btn-warning btn-active-light-info
            py-1
            fs-3
            px-4
            border border-blue-100
            rounded
            position-absolute
            bottom-10
            left-10
          "
        >
          Back
        </button>
      </div>
    </div>
    <!-- Q1 -->
    <div class="mb-3 px-4">
      <h1  v-if="!submited" class="py-3 my-3 fs-4 text-gray-700">
        Répondre au quiz en sélectionnant la bonne réponse
      </h1>
    </div>
    <div class="px-4">
      <div class="w-100">
        <h2 class="py-1 fs-5 text-gray-600">Q2 - Les bus ont pour but</h2>
        <div
          class="
            w-100
            form-check
            d-flex
            align-items-center
            gap-2
            form-check-custom form-check-solid
            my-2
          "
        >
          <input
            class="form-check-input"
            v-model="form.q1"
            type="checkbox"
            value="1"
          />
          <label class="form-label m-0 fs-5 text-gray"
            >Récupérer les données et présenter les résultats</label
          >
        </div>
        <div
          class="
            w-100
            form-check
            d-flex
            align-items-center
            gap-2
            form-check-custom form-check-solid
            my-2
          "
        >
          <input
            class="form-check-input"
            v-model="form.q1"
            type="checkbox"
            value="2"
          />
          <label class="form-label m-0 fs-5 text-gray"
            >La circulation de données</label
          >
        </div>
        <div
          class="
            w-100
            form-check
            d-flex
            align-items-center
            gap-2
            form-check-custom form-check-solid
            my-2
          "
        >
          <input
            class="form-check-input"
            v-model="form.q1"
            type="checkbox"
            value="3"
          />
          <label class="form-label m-0 fs-5 text-gray"
            >Le traitement de données</label
          >
        </div>
        <span v-if="submited" class="badge fs-5 badge-light-success">Response : 2</span>
      </div>
    </div>
    <!-- Q2 -->
    <div class="px-4">
      <div class="w-100">
        <h2 class="py-1 fs-5 text-gray-600">
          Q2 - Le cerveau de tout système informatique est ?</h2>
        <div
          class="
            w-100
            form-check
            d-flex
            align-items-center
            gap-2
            form-check-custom form-check-solid
            my-2
          "
        >
          <input
            class="form-check-input"
            v-model="form.q2"
            type="checkbox"
            value="1"
          />
          <label class="form-label m-0 fs-5 text-gray">Mémoire</label>
        </div>
        <div
          class="
            w-100
            form-check
            d-flex
            align-items-center
            gap-2
            form-check-custom form-check-solid
            my-2
          "
        >
          <input
            class="form-check-input"
            v-model="form.q2"
            type="checkbox"
            value="2"
          />
          <label class="form-label m-0 fs-5 text-gray">RAM</label>
        </div>
        <div
          class="
            w-100
            form-check
            d-flex
            align-items-center
            gap-2
            form-check-custom form-check-solid
            my-2
          "
        >
          <input
            class="form-check-input"
            v-model="form.q2"
            type="checkbox"
            value="3"
          />
          <label class="form-label m-0 fs-5 text-gray">CPU</label>
        </div>
        <div
          class="
            w-100
            form-check
            d-flex
            align-items-center
            gap-2
            form-check-custom form-check-solid
            my-2
          "
        >
          <input
            class="form-check-input"
            v-model="form.q2"
            type="checkbox"
            value="4"
          />
          <label class="form-label m-0 fs-5 text-gray">La souris</label>
        </div>
         <span v-if="submited" class="badge fs-5 badge-light-success">Response : 3</span>
      </div>
    </div>
    <!-- Q3 -->
    <div class="px-4">
      <div class="w-100">
        <h2 class="py-1 fs-5 text-gray-600">
          Q3 - Les périphérique sont utilisées pour
        </h2>
        <div
          class="
            w-100
            form-check
            d-flex
            align-items-center
            gap-2
            form-check-custom form-check-solid
            my-2
          "
        >
          <input
            class="form-check-input"
            v-model="form.q3"
            type="checkbox"
            value="1"
          />
          <label class="form-label m-0 fs-5 text-gray"
            >Stocker des données</label
          >
        </div>
        <div
          class="
            w-100
            form-check
            d-flex
            align-items-center
            gap-2
            form-check-custom form-check-solid
            my-2
          "
        >
          <input
            class="form-check-input"
            v-model="form.q3"
            type="checkbox"
            value="2"
          />
          <label class="form-label m-0 fs-5 text-gray"
            >Faire Démarer/Arrêt de l'ordinateur</label
          >
        </div>
        <div
          class="
            w-100
            form-check
            d-flex
            align-items-center
            gap-2
            form-check-custom form-check-solid
            my-2
          "
        >
          <input
            class="form-check-input"
            v-model="form.q3"
            type="checkbox"
            value="3"
          />
          <label class="form-label m-0 fs-5 text-gray"
            >Récupérer les données et présenter les résultats</label
          >
        </div>
        <span v-if="submited" class="badge fs-5 badge-light-success">Response : 3</span>
      </div>
    </div>
    <!-- Q4 -->
    <div class="px-4">
      <div class="w-100">
        <h2 class="py-1 fs-5 text-gray-600">
          Q4 - A quoi sert un boite d'alimentation ?
        </h2>
        <div
          class="
            w-100
            form-check
            d-flex
            align-items-center
            gap-2
            form-check-custom form-check-solid
            my-2
          "
        >
          <input
            class="form-check-input"
            v-model="form.q4"
            type="checkbox"
            value="1"
          />
          <label class="form-label m-0 fs-5 text-gray"
            >Traiter les données</label
          >
        </div>
        <div
          class="
            w-100
            form-check
            d-flex
            align-items-center
            gap-2
            form-check-custom form-check-solid
            my-2
          "
        >
          <input
            class="form-check-input"
            v-model="form.q4"
            type="checkbox"
            value="2"
          />
          <label class="form-label m-0 fs-5 text-gray"
            >Fournir le courant</label
          >
        </div>
        <div
          class="
            w-100
            form-check
            d-flex
            align-items-center
            gap-2
            form-check-custom form-check-solid
            my-2
          "
        >
          <input
            class="form-check-input"
            v-model="form.q4"
            type="checkbox"
            value="3"
          />
          <label class="form-label m-0 fs-5 text-gray"
            >Stocker les données</label
          >
        </div>
        <span v-if="submited" class="badge fs-5 badge-light-success">Response : 2</span>
      </div>
      <div class="my-2 px-4 d-flex bottom-bar justify-content-between">
        <nuxt-link to="/">
          <button
            class="
              btn btn-warning btn-active-light-info
              py-1
              fs-3
              px-4
              border border-blue-100
              rounded
            "
          >
            Back
          </button>
        </nuxt-link>

        <button
        v-if="!submited"
          @click="submit"
          class="
            btn btn-info btn-active-light-info
            py-1
            fs-3
            px-4
            border border-blue-100
            rounded
          "
        >
          Submit
        </button>
            <button
        v-if="submited"

          @click="reset"
          class="
            btn btn-info btn-active-light-info
            py-1
            fs-3
            px-4
            border border-blue-100
            rounded
          "
        >
          Reset
        </button>
      </div>
    </div>
  </main>
</template>

<script>
export default {
  data() {
    return {
      validForm: {
        q1: 2,
        q2: 3,
        q3: 3,
        q4: 2,
      },
      form: {
        q1: [],
        q2: [],
        q3: [],
        q4: [],
      },
      score: 0,
      submited:false,
      result: false,
    };
  },
  methods: {
    submit() {
      let score = 0;
      if (this.form.q1.length == 1 && this.form.q1[0] == 2) {
        this.score += 5;
      }
      if (this.form.q2.length == 1 && this.form.q2[0] == 3) {
        this.score += 5;
      }
      if (this.form.q3.length == 1 && this.form.q3[0] == 3) {
        this.score += 5;
      }
      if (this.form.q4.length == 1 && this.form.q4[0] == 2) {
        this.score += 5;
      }
      this.result=true
    },
    
    exit() {
      this.submited=true
      this.result = false;
    },
    reset() {
      this. form= {
        q1: [],
        q2: [],
        q3: [],
        q4: [],
      },
      this.score=0
      this.submited=false

    },

  },
  computed:{
    scoreStyle:function(){
          switch (this.score) {
            case 0:
              return 'badge-light-danger'
              case 5:
              return 'badge-light-warning'    
              case 10:
              return 'badge-light-info'    
              case 15:
              return 'badge-light-primary'
               case 20:
              return 'badge-light-success'
            default:
              break;
          }
    },
        scoreMessage:function(){
          switch (this.score) {
            case 0:
              return 'Bad level you need york hard'
              case 5:
              return 'You need more work'    
              case 10:
              return 'Not bad! but work more'    
              case 15:
              return 'Good ! keep Going'
               case 20:
              return 'Excelent!!'
            default:
              break;
          }
    }
  }
};
</script>
<style scoped>
.back {
  position: fixed;
  inset: 0;
  display: flex;
  align-items: center;
  justify-content: center;
  background: rgba(17, 20, 22, 0.382);
  backdrop-filter: blur(8px);
  z-index: 10;
}
.pop {
  width: 80vw;
  height: 25vh;
  z-index: 11;
}
.bottom-10{
  bottom: 10px;
}
.left-10{
  left: 10px;
}
main {
  background: rgba(250, 255, 253, 0.863);
  min-height: 100vh;
}
.bottom-bar{
  position: absolute;
  right: 0;
  left: 0;
  bottom: 10px;
}
.center-flex{
    display: flex;
  align-items: center;
  justify-content: center;
}
</style>
