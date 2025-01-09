import React from 'react';
import{useState} from 'react';

import './App.css';

function App(){
  const[name,setName]=useState('');
  const[m,setmale]=useState('');
  const[pass,setPassword]=useState('');
  const[email,setEmail]=useState('');
  const[number,setNumber]=useState('');


  
  const handleSubmit=(e)=>{
    e.preventDefault();//prevent page load
   if(name === "DARSHUU" && pass === "IMRD" && email === "IMRD@123" && number === 7359468251 && m === m)
     {
    alert("Login Successful...");
   }
   else
   {
    alert("Login unsuccessful...");
   }
      
  };
  return (
    <div className="App">
    <h1> Registration Form </h1>
      <form onSubmit={handleSubmit}> 

        <div>
          <label>Name- </label>
          <input type="text" value={name}
          onChange={(e)=> setName(e.target.value)}
          placeholder='Enter Your Name'></input>  
        </div>
        <br></br>

        <div>
          <label>Gender- </label>
          <input type="radio" name="m" 
          value="Male"
          onChange={(e)=> setmale(e.target.value)}/> Male
          &nbsp;
          <input type="radio" name="m" 
          value="Female"
          onChange={(e)=> setmale(e.target.value)}/> Female
        </div>
        <br></br>

        <div>
          <label>Number- </label>
          <input type="number" value={number}
          onChange={(e)=> setNumber(e.target.value)}
          placeholder='Enter Your MOB.No'></input>  
        </div>
        <br></br>


        <div>
      <lable>Email- </lable>
        <input type="email" value={email}
        onChange={(e)=>setEmail(e.target.value)}
        placeholder="Enter User Email"/>
        </div>
        <br></br>


        <div>
          <label>Password- </label>
          <input type="password" value={pass}
          onChange={(e)=> setPassword(e.target.value)}
          placeholder='Enter Your Password'></input>  
        </div>
        <br></br>


        
        <div>
          <button type="submit">submit</button>
        </div>
        </form>
    
  </div>
  );
}

export default App;

