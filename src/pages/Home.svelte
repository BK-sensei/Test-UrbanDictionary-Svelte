<script>
  import * as Yup from 'yup';
  import {Form, Message} from 'svelte-yup';
  import { useNavigate } from "svelte-navigator";
  import { useFocus } from "svelte-navigator";

  let fields = {
      username: "",
      password: "",
  };

  const schema = Yup.object().shape({
    username: Yup.string()
        .required("Username is required")
        .max(15, "Username is too long"),
    password: Yup.string()
        .required("Password is required")
        .min(6, "Password must contain a minimum of 6 characters")
  });

  let submitted = false;
  let isValid;
	const navigate = useNavigate();
  const registerFocus = useFocus();

  function formSubmit(){
      submitted = true;
      isValid = schema.isValidSync(fields);
      if(isValid){
        navigate('/generator')
        //  
        //console.log(fields)
        alert('Everything is validated!');
      }
  }
  
</script>
<div class="home-container">
    <div class="login-container">
      <Form class="form" {schema} {fields} submitHandler={formSubmit} {submitted}>
        <div class="input-container">
          <label for="username" >Username</label>
          <input 
              name="username"
              type="text" 
              placeholder="Enter your username"
              use:registerFocus
              bind:value={fields.username}
          />
          <span class="errorMessage"><Message name="username" /></span>
        </div>
        <div class="input-container">
          <label for="password" >Password</label>
          <input 
              name="password"
              type="password" 
              placeholder="Enter your password"
              bind:value={fields.password}
          />
          <span class="errorMessage"><Message name="password" /></span>
        </div>
        <div class="btn-container">
          <button class="btn-submit">Login</button>
        </div>
      </Form>
  </div>
</div>

<style scoped>

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
  