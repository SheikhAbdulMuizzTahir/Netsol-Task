<template>
	<header>
		<div class="header-text">NETSOL</div>
		<div class="button">	
			<DropdownButton />
		</div>
		
	</header>
  <body class="background">
    <div class="rounded-pill">
      <div class="centertitle">News and Insights</div>
    </div>
    <div class="text1">Latest Insights from Leading Voices</div>
    <div class="text2">
      Solving the world’s problems through technology wouldn’t be possible
      without our most important invention: the NetSol. Have a look at our
      talented teams.
    </div>
    	<div class="cards">
     	 	<div class="card">
        		<img src="../assets/img1.png"  class="box-image" />
        		<div class="news-tag">News</div>
			<div class="title-card">Leasing Life Conference & Awards</div>
			<div class="text-card">Solving the world’s problems through technology wouldn’t be possible without our most important invention.</div>
		</div>
      	
      	<div class="card">
        	<div class="card">
        		<img src="../assets/img2.png"  class="box-image" />
        		<div class="news-tag">News</div>
			<div class="title-card">Auto Finance Summit 2023</div>
			<div class="text-card">Solving the world’s problems through technology wouldn’t be possible without our most important invention.</div>
		</div>
      	</div>
      	<div class="card">
        	<div class="card">
        		<img src="../assets/img3.png"  class="box-image" />
        		<div class="news-tag">News</div>
			<div class="title-card">Careers at Netsol</div>
			<div class="text-card">Solving the world’s problems through technology wouldn’t be possible without our most important invention.</div>
		</div>
      	</div>
      	<div class="card">
        	<div class="card">
        		<img src="../assets/img4.png"  class="box-image" />
        		<div class="news-tag">News</div>
			<div class="title-card">Leasing Life Conference & Awards</div>
			<div class="text-card">Solving the world’s problems through technology wouldn’t be possible without our most important invention.</div>
		</div>
      	</div>
    </div>
    <div class="news">View All News</div>
  </body>
</template>
<script>
import DropdownButton from '../components/dropdownButton'
</script>
<style>
.background {
  position: relative;
  width: 100%;
  height: 100vh; 
  overflow: hidden; 
}
.background::before {
  content: "";
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background-image: url("/assets/bg.jpeg");
  background-position: center;
  background-attachment: fixed;
  background-repeat: no-repeat;
  background-size: cover;
  filter: blur(50px); 
  z-index: -1; 
   transform: scale(1.1);

}

.centertitle {


  font-family: "Aeonik";
  font-style: normal;
  font-weight: 500;
  font-size: 24px;
  line-height: 29px;
  text-align: center;

  text-align: center;
  text-rendering: optimizeLegibility; 
  vertical-align: middle;

  background: linear-gradient(180deg, #ffffff 49.51%, #c0c0c0 89.32%);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  background-clip: text;
  -webkit-text-fill-color: transparent;
}
.rounded-pill {
  position: absolute;
  width: 201px;
  height: 29px;
  left: 0;
  right: 0;
  margin-left: auto;
  margin-right: auto;
  top: 157px;
  display: inline-block;
  padding: 5px 10px; 
  border-radius: 20px; 
  background-color: rgba(0, 0, 0, 0.548);
  color: white; 
}
.text1 {
  

  position: absolute;
  width: 904px;
  height: 67px;
  left: 0;
  right: 0;
  margin-left: auto;
  margin-right: auto;
  top: 205px;

  font-family: "Aeonik";
  font-style: normal;
  font-weight: 500;
  font-size: 56px;
  line-height: 67px;
  text-align: center;

  background: linear-gradient(180deg, #ffffff 49.51%, #c0c0c0 89.32%);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  background-clip: text;
}
.text2 {
  position: absolute;
  width: 1108px;
  height: 64px;
  left: 0;
  right: 0;
  margin-left: auto;
  margin-right: auto;
  top: 282px;

  font-family: "Aeonik";
  font-style: normal;
  font-weight: 400;
  font-size: 24px;
  line-height: 32px;
  text-align: center;

  color: rgba(255, 255, 255, 0.72);
}
.news {


  position: absolute;
  width: 102px;
  height: 24px;
  left: 0;
  right: 0;
  margin-left: auto;
  margin-right: auto;
  top: 366px;

  font-family: "Aeonik";
  font-style: normal;
  font-weight: 500;
  font-size: 16px;
  line-height: 24px;
  text-decoration-line: underline;

  color: #ffffff;
}
.cards {
  
  position: absolute;
  width: 90%;
  height:30%;
  left: 0;
  right: 0;
  margin-left: auto;
  margin-right: auto;
  top: 471px;
  background-color:transparent;
  display: flex;
}
.card {
  flex: 1;
  background-color:transparent;
  margin: 0.6%;
  display: flex;
  flex-direction: column;
  position: relative; 
}

.box-image {

  flex: 1;

  width: 100%;
  height: 60%;
  max-height: 60%;
  border-radius: 5px;
 
}

.news-tag {
  flex: 2;
  width: 20%;
  height: 5%;
  max-height:5%;
  background-color:rgba(255, 255, 255, 0.1);
  
  border-radius: 5px;
  font-size: 1.1vw;
  margin: 2px;
  text-align: center;
  color: #18EBFE;
  
}
.title-card{

width: 100%;
height: 20%;
font-family: 'Aeonik';
font-style: normal;
font-weight: 500;
font-size: 1.5vw;
line-height: 2.5vw;



color: rgb(241, 241, 235);

flex: 3;
order: 0;
flex-grow: 0;

}
.text-card{

width: 100%;
height: 30%;

font-family: 'Aeonik';
font-style: normal;
font-weight: 400;
font-size: 1vw;
line-height: 2vw;

color: #fdfcfc;

flex: 4;
order: 1;
flex-grow: 0;

}
.header-text{


position: absolute;
top: 2%;
left: 3%;
color: #ffffff;
font-size: 2.5vw;
font-family: Impact, Haettenschweiler, 'Arial Narrow Bold', sans-serif;
background: transparent;

}
.button{
position: absolute;

top: 2%;
left: 85%;
}


</style>
