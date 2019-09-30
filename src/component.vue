<template>
        <button :class="classType"
                :disabled="isDisabled">
                <div class="btn-spn" v-if="needSpinner && isRequesting">
                    <div class="spinner"></div>
                </div>
                <div class="btn-text">
                    {{text}}
                </div>
        </button>
</template>
<script>
import '../fonts/fonts.css'

export default {

  props: {
    classType: {
      type: String,
      default: 'button success'
    },
    text: {
      type: String,
      default: 'Salvar'
    },
    needSpinner: {
      type: Boolean,
      default: false
    },
    isRequesting: {
      type: Boolean,
      default: false
    },
    isDisabled: {
      type: Boolean,
      default: false
    }
  },
  data () {
    return { }
  }
}
</script>
<style>

.btn-spn{
    /* border: 1px solid red; */
    width: 20%;
    height: 30px;
    flex: 0.4;
    overflow: hidden;
    display: flex;
    justify-content: center;
    align-items: center;
}
.btn-text{
    /* border: 1px solid red; */
    font-family:'Montserrat SemiBold';
    font-size: 13px;
    width: 100%;
    height: 30px;
    flex: 1;
    overflow: hidden;
    display: flex;
    justify-content: center;
    align-items: center;
}

/*Default Buttons*/

.button {
  -webkit-appearance: none;
  border: 0;
  width:121px;
  height: 37px;
  border-radius: 4px;
  font-size: 16px;
  margin-top: 0.6em;
  transition: background-color .3s;
  float: left;
  display: flex;
  overflow: hidden;
  justify-content: center;
  margin-left: 10px;
  cursor: pointer;
  box-shadow: 0 0 1px rgba(0, 0, 0, 0);
  background-color: none;
}

.button.primary {
  background-color: #9696FF;
  color: #000;
}
.button.primary[disabled]{
    background-color: #BABAFF;
}
.button.primary-outline {
  border: 1px solid #9696FF;
  color: #9696FF;
}

.button.success {
  background-color: Transparent;
  background-repeat:no-repeat;
  background-color: #30C9B1;
  color: #000;
}
.button.success[disabled]{
    background-color: #A3D5CD;
}
.button.success-outline {
  background-color: Transparent;
  background-repeat:no-repeat;
  border: 1px solid #30C9B1;
  color: #30C9B1;
}

.button.danger {
  background-color: #FF827F;
  color: #000;
}
.button.danger-outline {
  background-color: Transparent;
  background-repeat:no-repeat;
  border: 1px solid #FF827F;
  color: #FF827F;
}

.button.info {
  background-color: #73A0FE;
  color: #000;
}
.button.info-outline {
  background-color: Transparent;
  background-repeat:no-repeat;
  border: 1px solid #73A0FE;
  color: #73A0FE;
}

.button.secondary {
  background-color: #ABB3C9;
  color: #000;
}
.button.secondary[disabled]{
    background-color: Transparent;
    border: 1px solid #8C93A8;
    color: #8C93A8;
}
.button.secondary-outline {
  background-color: Transparent;
  background-repeat:no-repeat;
  border: 1px solid #DBDEE6;
  color: #DBDEE6;
}

.button.warning {
  background-color: #D1A032;
  color: #000;
}
.button.warning-outline {
  background-color: Transparent;
  background-repeat:no-repeat;
  border: 1px solid #D1A032;
  color: #D1A032;
}

/*Spinners*/

.spinner {
    border: 4px solid rgba(0, 0, 0, .1);
    width: 25px;
    height: 25px;
    border-left-color: #242939;
    border-bottom-color: #242939;
    border-top-color: #242939;
    border-radius: 50%;
    animation: spin 1s linear infinite;
}

@keyframes spin {
    to { transform: rotate(360deg); }
}
/*Big Buttons*/
.button-bg {
  -webkit-appearance: none;
  border: 0;
  width:136px;
  height: 51px;
  border-radius: 4px;
  font-size: 16px;
  margin-top: 0.6em;
  transition: background-color .3s;
  float: left;
  display: flex;
  overflow: hidden;
  justify-content: center;
  margin-left: 10px;
  cursor: pointer;
  box-shadow: 0 0 1px rgba(0, 0, 0, 0);
  background-color: none;
}

.button-bg:hover {
  transform: translate(0, -1px);
    box-shadow: 0 27px 10px -20px rgba(0, 0, 0, 0.5);
}

.button-bg.primary {
  background-color: #9696FF;
  color: #000;
}
.button-bg.primary[disabled]{
    background-color: #BABAFF;
}
.button-bg.primary-outline {
  border: 1px solid #9696FF;
  color: #9696FF;
}

.button-bg.success {
  background-color: Transparent;
  background-repeat:no-repeat;
  background-color: #30C9B1;
  color: #000;
}
.button-bg.success[disabled]{
    background-color: #A3D5CD;
}
.button-bg.success-outline {
  background-color: Transparent;
  background-repeat:no-repeat;
  border: 1px solid #30C9B1;
  color: #30C9B1;
}

.button-bg.danger {
  background-color: #FF827F;
  color: #000;
}
.button-bg.danger-outline {
  background-color: Transparent;
  background-repeat:no-repeat;
  border: 1px solid #FF827F;
  color: #FF827F;
}

.button-bg.info {
  background-color: #73A0FE;
  color: #000;
}
.button-bg.info-outline {
  background-color: Transparent;
  background-repeat:no-repeat;
  border: 1px solid #73A0FE;
  color: #73A0FE;
}

.button-bg.secondary {
  background-color: #ABB3C9;
  color: #000;
}
.button-bg.secondary[disabled]{
    background-color: Transparent;
    border: 1px solid #8C93A8;
    color: #8C93A8;
}
.button-bg.secondary-outline {
  background-color: Transparent;
  background-repeat:no-repeat;
  border: 1px solid #DBDEE6;
  color: #DBDEE6;
}

.button-bg.warning {
  background-color: #D1A032;
  color: #000;
}
.button-bg.warning-outline {
  background-color: Transparent;
  background-repeat:no-repeat;
  border: 1px solid #D1A032;
  color: #D1A032;
}

@media (min-width: 1024px) and (max-width: 1124px){
  .button {
    width: 76px;
    height: 35px;
  }

  .btn-text {
      /* border: 1px solid red; */
      font-family: 'Montserrat SemiBold';
      font-size: 10px;
  }

}

@media (min-width: 768px) and (max-width: 800px) {
  .button {
      width: 76px;
      height: 35px;
  }

  .btn-text {
      /* border: 1px solid red; */
      font-family: 'Montserrat SemiBold';
      font-size: 10px;
  }
}

</style>
