<template>
    <!-- <q-page class="flex flex-center"> -->
    <q-page>
       <div :style="[{'background-image': 'url(' + require('../img/AboutUs/conoce_chatbot.jpeg') + ')'}, {'background-size': 'cover'}]">
        <!-- <div :style="background-image: url('~@/assets/img.jpeg');"> -->
       <!-- <div style="background-image: url('../src/img/AboutUs/conoce_chatbot.jpeg'); background-size: cover; padding: 50px; "> -->
        <a href="http://fime.uanl.mx/"><img src="https://iconape.com/wp-content/files/hi/194343/svg/194343.svg" width="120px;"></a>
        <h2 style="color: white; font-weight: 300; font-size: 50px; text-align: center;">ChatBot FIME</h2>
        <h1 style="color: white; font-weight: 900; display: grid; font-size: 40px; line-height: 3rem; text-align: center;">Conoce el asistente virtual de la Facultad de Ingeniería Mecánica y Eléctrica</h1>
        <p><span style="font-size: 18px;">&nbsp;</span></font></p>
      </div>

      <div class="row" style="margin-top: 0px; margin-bottom: 0px; padding-top: 20px;">
        <!-- Logotipo -->
        <div class="col-4 text-center" style="text-align: -webkit-center; align-self: center;">
          <div style="width: 140px;height: 100px;overflow: hidden; vertical-align: middle; display: table-cell;">
            <!-- <img src="../img/AboutUs/loading.gif"  class="img img-responsive" style="max-width:140px; max-height:100px;"> -->
          </div>
        </div>
        <div class="col-8">
          <h5 style="color: black; font-weight: 500; display: grid; line-height: 2rem; margin: 0px;">Te ayudará a resolver dudas a través de mensajes de texto</h5><br/>
          <p style="font-size: 20px;">Por ejemplo, puedes preguntarle "¿Cuál es el proceso para tramitar el servicio social?" y tendrás la información que necesitas.</p>
          <!-- <address>
              <span>f</span><br/>
          </address> -->
        </div>
      </div>
      <!-- <table style="width:100% !important;">
        <tr >
          <th class="col-xs-6"><p style="margin-bottom: unset;">s</p></th>
          <th class="col-xs-6"><p style="margin-bottom: unset;">f</p></th>
        </tr>
        <tr>
          <td >
            <span>f</span><br/>
          </td>
          <td >
            <span>f</span><br/>
          </td>
        </tr>
      </table> -->
      <div class="q-pa-md">
        <div class="q-gutter-y-md" style="max-width: 100%">
          <q-card>
            <q-tabs
              v-model="tab"
              dense
              class="text-grey"
              active-color="primary"
              indicator-color="primary"
              align="justify"
              narrow-indicator
            >
              <q-tab name="bot_start" label="QUÉ NECESITAS" />
              <q-tab name="bot_use" label="HAZLE PREGUNTAS" />
              <!-- <q-tab name="movies" label="Movies" /> -->
            </q-tabs>

            <q-separator/>

            <q-tab-panels v-model="tab" animated>
              <q-tab-panel name="bot_start">
                <div class="row" style="margin-top: 0px; margin-bottom: 0px; padding-top: 20px;">
                  <div class="col-6">
                    <h5 style="color: black; font-weight: 500; display: grid; line-height: 2rem; margin: 0px;">Desde tu dispositivo móvil, entra a tu navegador favorito</h5><br/>
                    <p style="font-size: 20px;">En el menú de opciones, selecciona la opción del ChatBot o desde la página principal presionando su icono.</p>
                  </div>
                  <!-- Logotipo -->
                  <div class="col-6 text-center" style="text-align: -webkit-center; align-self: center;">
                    <div style="width: 500px;height: 500px;overflow: hidden; vertical-align: middle; display: table-cell;">
                      <img src="../img/AboutUs/bot_start.png"  class="img img-responsive" style="max-width:500px; max-height:500px;">
                    </div>
                  </div>

                </div>
              </q-tab-panel>

              <q-tab-panel name="bot_use">
                <div class="row" style="margin-top: 0px; margin-bottom: 0px; padding-top: 20px;">
                  <div class="col-6">
                    <h5 style="color: black; font-weight: 500; display: grid; line-height: 2rem; margin: 0px;">"¿Cuál es el plan de estudios para la carrera ITS?"</h5><br/>
                    <p style="font-size: 20px;">Pidele a ChatBot FIME por texto la información que necesites.</p>
                  </div>
                  <!-- Logotipo -->
                  <div class="col-6 text-center" style="text-align: -webkit-center; align-self: center;">
                    <div style="width: 500px;height: 500px;overflow: hidden; vertical-align: middle; display: table-cell;">
                      <img src="../img/AboutUs/bot_use.png"  class="img img-responsive" style="max-width:500px; max-height:500px;">
                    </div>
                  </div>

                </div>
              </q-tab-panel>
              <!-- <q-tab-panel name="movies">
                <div class="text-h6">Movies</div>
                Lorem ipsum dolor sit amet consectetur adipisicing elit.
              </q-tab-panel> -->
            </q-tab-panels>
          </q-card>

        </div>
        <!-- <p>Creditos</p> -->
      </div>

    </q-page>
</template>

<script>
export default {
  data () {
    return {
      tab: 'bot_start'
    }
  }
}
</script>

<style scoped>
.text-good{
  font-family: 'Lora', serif;
}

.img{
  background: white;
}
.img-size
{width: 35%;
}
</style>
