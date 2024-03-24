# coltogdyuhg.github.io
<div>
  <label class="toggle-button">
  	<input type="checkbox" class="toggle-checkbox">
    <span class="slider"></span>
    <span class="label label-dark">Dark</span>
    <span class="label label-light">Light</span>
  </label>
</div>

<style>
/* The switch - the box around the circle */
.toggle-button {
    position: relative;
    display: flex;
    width: 200px;
    height: 40px;
    margin: 10px;
    align-items: center;
    justify-content: space-around;
    flex-wrap: nowrap;
    flex-direction: row;
}

.toggle-checkbox {
  display: none;
}

.slider {
  position: absolute;
  top: 0;
  left: 65px;
  width: 80px;
  height: 40px;
  background-color: #ec6838;
  border-radius: 40px;
  transition: background-color 0.2s, transform 0.2s;
}

.slider:before {
  content: "";
  position: absolute;
  top: 4px;
  left: 4px;
  width: 32px;
  height: 32px;
  background-color: white;
  border-radius: 50%;
  transition: transform 0.2s;
}

/* When the checkbox is checked, change the background color and move the circle to the right */
.toggle-checkbox:checked + .slider {
  background-color: #ccc;
  transform: translateX(0px);

}

.toggle-checkbox:checked + .slider:before {
  transform: translateX(40px);

}

/* Label styles */
.label {
  position: absolute;
  top: 50%;
  transform: translateY(-50%);
  font-size: 16px;
  font-weight: bold;
  color: #ccc;
  transition: color 0.2s;
  text-align: center;
}

.label-light {
  color: #ccc;
 	right: 0px;
}

.label-dark {
  left: 0px;
  color: #ec6838;
}

.toggle-checkbox:checked + .label-light {
  color: #ccc;
}

.toggle-checkbox:checked + .label-dark {
  color: #fff;
  background-color: #ccc;
}

</style>
