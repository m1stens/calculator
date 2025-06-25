
<template>

<img src="../src/assets/tr.jpeg" alt="Описание"><br><br>

<div class="container">
	<div class="input">
		<input type="text" v-model="a" placeholder="a">
		<input type="text" v-model="b" placeholder="b">
		<input type="text" v-model="c" placeholder="c">
		<input type="text" v-model="d" placeholder="d">
		<input type="text" v-model="e" placeholder="e">
		<input type="text" v-model="f" placeholder="f">
		<input type="text" v-model="g" placeholder="g">
	</div>

	<div class="result">
		<p>a = {{ resultA }}</p>
		<p>b = {{ resultB }}</p>
		<p>c = {{ resultC }}</p>
		<p>d = {{ resultD }}</p>
		<p>e = {{ resultE }}</p>
		<p>f = {{ resultF }}</p>
		<p>g = {{ resultG }}</p>
	</div>

</div>
	
	<button @click="sendData()">Посчитать</button>

</template>
<script>
export default {
	
	data() {
		return {
			info: 'Title!',
			someInfo: 'Anons of message',
			text: '',
			resultA: '',
			resultB: '',
			resultC: '',
			resultD: '',
			resultE: '',
			resultF: '',
			resultG: '',

			a: '',
			b: '',
			c: '',
			d: '',
			e: '',
			f: '',
			g: '',

		}
	},
	
	methods: {
		sendData() {
			if(this.e != 0){
				this.b = this.e
				this.c = this.e

				this.resultE = this.e
				this.resultC = this.e
				this.resultB = this.e

				this.a = (this.e * this.e) * 2
				
				this.resultA = Math.sqrt(this.a)

				if(this.g !=0){
					this.resultG = this.g
					this.resultD = this.g
					this.resultF = this.g - this.b
				}
			}else if(this.a !=0){
				this.b = (this.a * this.a) / 2

				this.resultA = this.a
				this.resultB = Math.sqrt(this.b) 
				this.resultE = this.resultB 
				this.resultC = this.resultB 
				this.resultG = this.g
				this.resultF = this.resultG - this.resultB
				this.resultD = this.resultF
				
			}else {
				this.resultA = this.a
				this.resultB = this.e
				this.resultC = this.e
				this.resultE = this.e
				this.resultG = this.g
				this.resultF = this.resultG - this.resultB
				this.resultD = this.resultF
			}
		},
		
	},
	

	
}
</script>

<style scoped>
	.container{
		display: flex;
	}
	.input{
		display: flex;
		flex-direction: column;
	}
	.input input[type="text"]{
		margin: 8px 0px;
	}

	.result{
		margin-left: 20px;
	}

	.result p{
		margin-top: 8px;
		margin-bottom: 19px;
	}
</style>
