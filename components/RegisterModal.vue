<template>
  <div style="position: absolute">
	  <modal ref="modal" @modal-close="$emit('modal-close')">
		  <template v-slot:modal-header-text>Register</template>
		  <div class="form-container">
			  <form action="" class="form">
				  <div class="form-group">
					  <div class="input-group span-2">
						  <label for="" class="label">Email *</label>
						  <input type="email" class="form-control" placeholder="janedoe@example-mail.com">
					  </div>
					  <div class="input-group span-2">
						  <label for="" class="label">Password *</label>
						  <input type="password" class="form-control" placeholder="Password">
					  </div>
					  <div class="input-group span-2">
						  <label for="" class="label">Confim Password *</label>
						  <input type="password" class="form-control" placeholder="Password">
					  </div>
				  </div>
				  <div class="actions-container display-flex justify-content-center">
					  <button  type="submit" class="submit-button">Register</button>
				  </div>
			  </form>
			  <div class="display-flex justify-content-sb other-actions">
				  <span class="font-size--4 text-color-success cursor-pointer" >Forgot Password</span>
				  <span class="font-size--4 cursor-pointer" @click="goToLogin()">Have an account? <span class="text-color-callout">Login</span></span>
			  </div>
		  </div>
	  </modal>
  </div>
</template>

<script lang="ts">
import { Vue, Component, Prop } from "vue-property-decorator";
import Modal from "~/components/Modal.vue";

@Component({
	components: {
		Modal
	}
})
export default class RegisterModal extends Vue {
	goToLogin(){
		this.$emit('go-to-login')
	}
	close(){
		(this.$refs.modal as Modal).close()
	}
}
</script>

<style lang="scss" scoped>
@import '~assets/styles/components/modal_forms';
</style>