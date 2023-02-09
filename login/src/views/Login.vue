<template>
    <div class="login-wrapper">
    <!-- <v-card  color="grey-lighten-3">
        <p>sda</p>
        <p>sda</p>
        <p>sda</p>
    </v-card>     -->
    
        <div class="login-card">
                <v-sheet style="margin-top: 20px; padding-top: 20px;" class="sm-10">
                    <v-form @submit.prevent="submit">
                        <v-text-field
                        class="mx-10"
                        density="comfortable"
                            v-model="userName"
                            :rules="rules"
                            label="Username"
                        ></v-text-field>
                        <v-text-field
                        class="mx-10"
                        density="comfortable"
                            v-model="Password"
                            :rules="rules"
                            label="Password"
                        ></v-text-field>
                    <v-btn  :disabled='disableSubmit'  type=submit class="mx-10">Submit</v-btn>
                    </v-form>
                </v-sheet>
            </div>
        </div>
</template>
<script lang="ts">
  export default {
    data: () => ({
        disableSubmit:false,
        userName: '',
        Password: '',
        rules: [
            (value: any) => {
            if (value) return true
            return ''
            },
        ],
    }),
    methods:{
        submit() {
            console.log("danie")
            this.disableSubmit=true
            if(true){
                this.$router.push("/")
            }
        }
    }
  }
</script>

  
<style>
.login-wrapper {
  width: 90%;
  height: 50%;
  /* whatever width you want */
  display: inline-block;
}
.login-wrapper:after {
  /* padding-top: 56.25%; */
  /* 16:9 ratio */
  display: block;
  content: '';
}
.login-wrapper{
    position: fixed;
    left: 50%;
    top: 50%;
    transform: translate(-50%, -50%);
    display:flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
}
.login-card{
background-color: rgb(253, 253, 253);
 position: absolute;
  top: 0;
  bottom: 0;
  right: 0;
  left: 0;
  /* fill parent */
  /* background-color: deepskyblue; */
  /* let's see it! */
  color: white;
}
</style>