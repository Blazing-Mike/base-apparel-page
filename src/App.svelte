<script>
function submit(){
	let emailInput = document.getElementById("email");
	function displayError(error){
		let errorDiv = document.getElementById("errormessage");
		errorDiv.innerHTML = '	please enter a valid email address';
		errorDiv.style.display = "block";
		errorDiv.style.color = "red";
	}

	function displaySuccess(){
		let errorDiv = document.getElementById("errormessage");
		errorDiv.innerHTML = '	Thank you for subscribing';
		errorDiv.style.display = "block";
		errorDiv.style.color = "green";
	}

	if (emailInput.value == "" || emailInput.value.includes("@") == false || emailInput.value.includes(".") == false){
	   displayError();
	}    else {
		displaySuccess();
	
	   } 

}
</script>

<body>
	
<header>
	<img src="images/logo.svg" alt="logo" class="logo">
</header>

<main>

	<section class="hero-section">

		<div class="hero_text">
			<h1 class="heading">WE'RE <span class="black">COMING SOON</span> </h1>

			<p class="para">
				Hello fellow shoppers! We're currently building our new fashion store. 
				Add your email below to stay up-to-date with announcements and our launch deals.
			  
			</p>

			<div class="subscribe-cont">
				<div class="error" id="errormessage"></div>
				<input type="text" class="email" id="email">
				<button on:click="{submit}" class="submit"><img src="images/icon-arrow.svg" alt="arrow-button" class="arrow"></button>
				
			</div>
		</div>

		<div class="hero-image">
			<img src="images/hero-mobile.jpg" alt="model" class="mobile">
			<img src="images/hero-desktop.jpg" alt="model" class="desktop">
		</div>
		
	
	</section>

</main>
</body>







<style>
	@import url('https://fonts.googleapis.com/css2?family=Josefin+Sans:wght@400&display=swap');
*{
	margin: 0;
	padding: 0;
	box-sizing: border-box;
}
	body{
		background-image: linear-gradient(135deg, hsl(0, 0%, 100%), hsl(0, 100%, 98%));
		padding: 0;
	}
	main{
		background-image: linear-gradient(135deg, hsl(0, 0%, 100%), hsl(0, 100%, 98%));
		padding: 10px 0;
	}
	img{
		width: 100%
	}

	.logo{
		width: 8rem;
	}

	.arrow{
		width: 1rem;
	}
	main {
		font-family: 'Josefin Sans', sans-serif;
	}

	.heading{
		font-size: 3rem;
	}
.desktop{
	display: none;
}
.mobile{
	min-width: 26rem;
}

.subscribe-cont{
	display: flex;
	align-self: center;
	flex-wrap: wrap;
	align-items: center;
	justify-content: center;

}

.email{
	width: 19rem;
	font-size: 1.4rem;
	padding: 10px;
}

.email:focus{
	outline: none;
}


button{
	width: 6rem;
	margin-left: -4rem;
	height: 3rem;
	background-image:linear-gradient(135deg, hsl(0, 80%, 86%), hsl(0, 74%, 74%));
	border: transparent;
}

.email, button{
	border-radius: 35px;
	height: 4rem;

}

#errormessage{
	display: none;
	font-size: 1rem;
	margin-left: 1rem;
	width: 100%;
	transition: 2s ease;
}
.hero_text{
	text-align: center;
}

.hero-section{
	display: flex;
	flex-wrap: wrap-reverse;
	justify-content: center;
	gap: 2rem;
}
	@media (min-width: 640px) {
		.mobile{
			display: none;
		}

		.logo{
			width: 15rem;
		}
		.desktop{
			display: flex;
			position: absolute;
			right: 0;
			top: 0;
			width: auto;
			height: 100%;
		}
		.hero_text{
		text-align: left;
	    margin-top: 5rem ;
		position: absolute;
		left: 30px;
		top: 5rem;

			
		}

		.heading,.para,.subscribe-cont{
			width: 50rem;
			justify-content: start;
			align-items: center;
		
		}
		.subscribe-cont{
			margin-top: 2rem;
		}

		.heading span{
			font-weight: 900;
			color: black;
		}

		.heading{
			font-size: 6rem;
			letter-spacing: 12px;
			color: hsl(0, 36%, 70%);
		}
		.para{
			font-size: 1.5rem;
		}
		.email{
			width: 30rem;
			height: 4rem;
		}
	}
</style>