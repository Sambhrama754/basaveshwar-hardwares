<template>
  <div class="body">
    <div id="container">
      <div id="contacts">
        <div id="contacts--contact">
          <p></p>
          <p></p>
        </div>
      </div>
      <div id="mentions">
        <p></p>
      </div>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style>
@import url("https://fonts.googleapis.com/css?family=Open+Sans");

.body {
  display: flex;
  background-color: #f0f8ff;
  justify-content: center;
  align-items: flex-end;
  font-family: Open Sans;
}

#container {
  padding-top: 20px;
  width: 100vw;
  color: white;
  background-color: #03020c;
  display: flex;
  flex-direction: column;
  align-items: center;
}
#contacts {
  display: flex;
  justify-content: space-around;
  align-items: center;
  width: 100%;
}
#contacts--contact {
  text-align: right;
}
#contacts--social div {
  height: 30px;
  width: 30px;
  background-color: white;
  border-radius: 50%;
}
#mentions p {
  font-size: 0.5em;
}
</style>