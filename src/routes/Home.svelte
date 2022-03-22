<script>
	
</script>

<main>
	<div class="home-container">
		<div class="login-container">
			<form onSubmit="onSubmit" >
				<div class="input-container">
					<label type="username" >Username</label>
					<input 
						name="username"
						type="text" 
						placeholder="Enter your username"
						:rules = "validUsr"
					/>
					<span class="errorMessage"></span>
				</div>
				<div class="input-container">
					<label type="password" >Password</label>
					<input 
						name="password"
						type="password" 
						placeholder="Enter your password"
						:rules = "validPwd"
					/>
					<span class="errorMessage"></span>
				</div>

				<div class="btn-container">
					<button class="btn-submit">Login</button>
				</div>
				
			</form>
		</div>
  	</div>
</main>

<style>
	.home-container{
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		font-family: 'Lora', serif;
	}
	.login-container{
		width: 35%;
		padding: 20px;
		margin: 30px;
	}
	.input-container{
		display: flex;
		flex-direction: column;
		margin-bottom: 30px;
	}
	label{
		font-family: 'Lora', serif;
		font-size: 24px;
		line-height: 41px;
		font-weight: 700;
	}
	input{
		border-radius: 10px;
		padding: 10px;
		margin-bottom: 5px;
	}
	.errorMessage{
		font-size: 14px;
		color: red;
		padding-left: 10px;
	}
	.btn-container{
		display: flex;
		justify-content: center;
	}
	.btn-submit{
		background: #EFFF00;
		border: none;
		border-radius: 30px;
		color: black;
		font-family: 'Lora', serif;
		font-size: 20px;
		font-weight: 700;
		filter: drop-shadow(0px 4px 4px rgba(0, 0, 0, 0.25));
		padding: 10px 40px;
		margin-bottom: 30px;
		cursor: pointer;
	}
</style>