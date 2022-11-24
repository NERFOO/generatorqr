<template>
    <div>
        <label>Introduzca la url</label><br/>
        <input type="text" v-model="urlPagina"><br/>

        <label>En caso de querer un logo en el centro del QR</label><br/>
        <input type="text" v-model="urlLogo"><br/>

        <hr/>
        <vue-qr
            :logoSrc="this.urlLogo"
            :text="this.urlPagina"
            :size="200"
            dotScale="0.1"
        ></vue-qr>
        <hr/>
    </div>
</template>

<script>
import vueQr from 'vue-qr/src/packages/vue-qr.vue'

export default {
    name : "GenerarQr" ,
    data() {
        return {
            urlLogo : "" ,
            urlPagina : ""
        }
    } ,
    components : {
        vueQr
    }
}
</script>

<style>

</style>