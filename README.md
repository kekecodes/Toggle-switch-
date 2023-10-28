# Toggle-switch-
<!DOCTYPE html>
<html>
<head>
  <title>My Website</title>
<style>
  root {
  --bg-color: white;
  --text-color: black;
}

@media (prefers-color-scheme: dark) {
  :root {
    --bg-color: black;
    --text-color: white;
  }
}

body {
  background-color: var(--bg-color);
  color: var(--text-color);
  display: grid;
  justify-content: center;
  align-items: center;
}

/* The switch - the box around the slider */

  
  

.switch {
 font-size: 17px;
 position: relative;
 display: flex;
 width: 62px;
 height: 35px;
 
 
}

/* Hide default HTML checkbox */
.switch input {
 opacity: 1;
 width: 0;
 height: 0;
}

/* The slider */
.slider {
 position: absolute;
 cursor: pointer;
 top: 0;
 left: 0;
 right: 0;
 bottom: 0px;
 background: #fff;
 transition: .4s;
 border-radius: 30px;
 border: 2px solid #ccc;
}

.slider:before {
 position: absolute;
 content: "";
 height: 1.9em;
 width: 1.9em;
 border-radius: 16px;
 left: 1.2px;
 top: 0;
 bottom: 0;
 background-color: white;
 box-shadow: 0 2px 5px #999999;
 transition: .4s;
}

input:checked + .slider {
 background-color: black;
 border: 1px solid transparent;
}

input:checked + .slider:before {
 transform: translateX(1.5em);
}

</style>
</head>
<body>
  <div id="switch">
 <label class="switch">
  <input type="checkbox" id="change-background-color-checkbox">
  <span class="slider"></span>
</label>
</div>
<script>
  const changeBackgroundColorCheckbox = document.querySelector('#change-background-color-checkbox');

  changeBackgroundColorCheckbox.addEventListener('change', () => {
    const backgroundColor = changeBackgroundColorCheckbox.checked ? 'white' : 'var(--bg-color)';
    document.body.style.backgroundColor = backgroundColor;
  });


  
  
   // This code is not necessary for the basic functionality of the website, but it can be used to add additional features, such as changing the background color when the user hovers over a button.


  </script>
</body>
</html>

