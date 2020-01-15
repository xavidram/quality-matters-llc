<template>
  <div class="jumbotron-container">
      <div class="jumbotron-content-container">
        <div class="jumbotron-content">
          <span class="jumbo-title">Quality Matters</span>
          <span class="jumbo-sub-title">Integrated Quality Management and Liaison Services</span>
        </div>
      </div>
  </div>
</template>
<script>
export default {
  title: 'Jumbotron',
  data: () => ({})
}
</script>
<style scoped lang="scss">
.jumbotron-container {
  height: calc(100vh - 92px);
  max-height: 500px;
  background-image: url('./../assets/images/city.jpg');
  background-position: top center;
  background-repeat: no-repeat;
  background-size: cover;
  display: flex;
}
.jumbotron-content-container {
  flex: 1;
  display: grid;
  height: calc(100vh - 92px);
  max-height: 500px;
  grid-template-columns: 1fr;
  grid-template-rows: 1fr;
  background: -moz-linear-gradient(left,  rgba(40,57,93,1) 14%, rgba(125,185,232,0) 75%);
  background: -webkit-linear-gradient(left,  rgba(40,57,93,1) 14%,rgba(125,185,232,0) 75%);
  background: linear-gradient(to right,  rgba(40,57,93,1) 14%,rgba(125,185,232,0) 75%);
  filter: progid:DXImageTransform.Microsoft.gradient( startColorstr='#28395d', endColorstr='#007db9e8',GradientType=1 );
}
.jumbotron-content {
  max-width: 1175px;
  margin: 0 auto;
  width: calc(100%);
  display: flex;
  flex-direction: column;
  align-items: flex-start;
  justify-content: center;
  padding: 0 1rem;
}
.jumbo-title {
  font-size: 170%;
  font-weight: 500;
  color: white;
  padding: 0.5rem 0.75rem;
  background: #243352;
  opacity: 0.85;
}
.jumbo-sub-title {
  font-size: 1rem;
  font-weight: 500;
  color: white;
  margin-top: 0.5rem;
  max-width: 270px;
  text-align: left;
  letter-spacing: 1px;
}
</style>
