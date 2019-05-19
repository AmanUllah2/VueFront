<template>
  <div id="logincss">
      <img src="@/assets/hec.jpg">
      <div id="forms">
      <form class="form-group" action="http://localhost:3800/users/authenticate" method="POST">
        <label for="fname">User ID</label>
        <input type="text" id="fname" name="email" placeholder="Enter ID..">
        <label for="lname">Password</label>
        <input type="password" id="lname" name="password" placeholder="Enter Password..">
        <input type="submit" value="Submit">
      </form>
</div>
</div>
</template>

<script>
export default {
  name: 'app',
  data () {
    return {
      userData:{
                email: '',
                password: ''
              }
    }
  }
}
</script>

<style>
@import url('https://fonts.googleapis.com/css?family=Proza+Libre|Fira+Mono');

html, body {
  height: 100%;
  margin: 0;
  padding: 0;
}

#image {
  height: 100%;
}
#logincss {
  display: flex;
  height: 50%;
  align-items: center;
  flex-direction: column;
}

input[type=text], select {
  width: 100%;
  padding: 12px 20px;
  margin: 8px 0;
  display: inline-block;
  border: 1px solid #ccc;
  border-radius: 4px;
  box-sizing: border-box;
}

input[type=password], select {
  width: 100%;
  padding: 12px 20px;
  margin: 8px 0;
  display: inline-block;
  border: 1px solid #ccc;
  border-radius: 4px;
  box-sizing: border-box;
}

input[type=submit] {
  width: 100%;
  background-color: #95BCEa;
  color: white;
  padding: 14px 20px;
  margin: 8px 0;
  border: none;
  border-radius: 4px;
  cursor: pointer;
}

input[type=submit]:hover {
  background-color: #11397a;
}
#image{
  padding:10px;
}
#forms {
  border-radius: 5px;
  background-color: #f2f2f2;
  padding: 20px;
}
</style>

