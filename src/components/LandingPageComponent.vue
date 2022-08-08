<template>
	<div class="page">
		<div class="nav-header text-center">
			<nav class="navbar navbar-expand-md navbar-light fixed-top py-4" :class="{'menu-active': menuOpened}">
				<div class="container">
					<a class="navbar-brand" href="#">
						<img src="../assets/logo-bookmark.svg" alt="" class="d-inline-block align-text-top">
					</a>
					<button class="navbar-toggler" type="button" data-bs-toggle="collapse"
						data-bs-target="#navbarHeader" aria-controls="navbarHeader" aria-expanded="false"
						aria-label="Toggle navigation" @click="menuOpened ? menuOpened = false : menuOpened = true">
						<img src="../assets/icon-hamburger.svg" alt="">
					</button>
					<div class="collapse navbar-collapse" id="navbarHeader">
						<ul class="navbar-nav ms-auto align-items-center">
							<li class="nav-item">
								<a class="nav-link" href="#">Features</a>
							</li>
							<li class="nav-item">
								<a class="nav-link" href="#">Pricing</a>
							</li>
							<li class="nav-item">
								<a class="nav-link" href="#">Contact</a>
							</li>
							&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
							<li class="nav-item">
								<a class="nav-link btn btn-danger" href="#">Login</a>
							</li>
							<li class="nav-item social-media d-md-none" style=" padding-top: 55vh;">
								<ul>
									<li>
										<a href="">
											<img src="../assets/icon-facebook.svg" alt="" />
										</a>
									</li>
									<li>
										<a href="">
											<img src="../assets/icon-twitter.svg" alt="" />
										</a>
									</li>
								</ul>
							</li>
						</ul>
					</div>
				</div>
			</nav>
		</div>
		<div class="main">
			<div class="simple-bookmark position-relative">
				<div class="back-simple-bookmark-right"></div>
				<div class="container">
					<div class="row align-items-center">
						<div class="col-md-6 mb-5 simple-bookmark-image order-md-2">
							<img class="img-fluid mt-5" src="../assets/illustration-hero.svg" alt="">
						</div>
						<div class="col-md-6 simple-bookmark-content order-md-1">
							<h1 class="fw-bold">A Simple Bookmark Manager</h1>
							<p class="text-muted">A clean and simple interface to organize your favorite websites. Open
								a new browser tab and see your sites load instantly. Try it for free</p>
							<div class="simple-bookmark-buttons">
								<button class="btn me-2">Get it on Chrome</button>
								<button class="btn">Get it on Firefox</button>
							</div>
						</div>
					</div>
				</div>
			</div>
			<div class="features my-5">
				<div class="back-simple-bookmark-left"></div>
				<div class="container">
					<div class="features-description text-center container">
						<h3 class="fw-bold">FEATURES</h3>
						<p class="text-muted">Our aim is to make it quick and easy for you to access your favourite
							websites. Your bookmarks sync between your devices so you can access them on the go.</p>
					</div>
					<div class="features-tabs text-center">
						<ul class="nav-tab container">
							<li class="tab-item pb-2" :class="{'active': featuresComponent=='TabSimpleBookMark'}"
								@click="featuresComponent='TabSimpleBookMark'">
								Simple Bookmark
							</li>
							<li class="tab-item pb-2" :class="{'active': featuresComponent=='TabSpeedySearching'}"
								@click="featuresComponent='TabSpeedySearching'">
								Speedy Searching
							</li>
							<li class="tab-item pb-2" :class="{'active': featuresComponent=='TabEasySharing'}"
								@click="featuresComponent='TabEasySharing'">
								Easy Sharing
							</li>
						</ul>
						<TabSimpleBookMark v-show="featuresComponent=='TabSimpleBookMark'"></TabSimpleBookMark>
						<TabSpeedySearching v-show="featuresComponent=='TabSpeedySearching'"></TabSpeedySearching>
						<TabEasySharing v-show="featuresComponent=='TabEasySharing'"></TabEasySharing>
					</div>
				</div>
			</div>
			<div class="download text-center">
				<div class="container">
					<h3 class="fw-bold">Download the extension</h3>
					<p class="text-muted">We’ve got more browsers in the pipeline. Please do let us know if you’ve got a
						favourite you’d like us to prioritize.</p>
					<div class="row">
						<div class="col-md-4">

							<div class="bookmark-card card-chrome">
								<div class="bookmark-card-image">
									<img src="../assets/logo-chrome.svg" alt="" />
								</div>
								<div class="bookmark-card-description">
									<h3 class="fw-bold">Add to Chrome</h3>
									<p class="text-muted">Minimum version 62</p>
								</div>
								<div class="bookmark-card-hr">
								</div>
								<div class="bookmark-card-footer">
									<button class="btn w-100">
										Add & Install Extension
									</button>
								</div>
							</div>
						</div>
						<div class="col-md-4">
							<div class="bookmark-card card-firefox">
								<div class="bookmark-card-image">
									<img src="../assets/logo-firefox.svg" alt="">
								</div>
								<div class="bookmark-card-description">
									<h3 class="fw-bold">Add to Firefox</h3>
									<p class="text-muted">Minimum version 55</p>
								</div>
								<div class="bookmark-card-hr">
								</div>
								<div class="bookmark-card-footer">
									<button class="btn w-100">
										Add & Install Extension
									</button>
								</div>
							</div>
						</div>
						<div class="col-md-4">
							<div class="bookmark-card card-opera">
								<div class="bookmark-card-image">
									<img src="../assets/logo-opera.svg" alt="">
								</div>
								<div class="bookmark-card-description">
									<h3 class="fw-bold">Add to Opera</h3>
									<p class="text-muted">Minimum version 46</p>
								</div>
								<div class="bookmark-card-hr">
								</div>
								<div class="bookmark-card-footer">
									<button class="btn w-100">
										Add & Install Extension
									</button>
								</div>
							</div>
						</div>
					</div>
				</div>
			</div>
			<div class="frequently-asked-questions">
				<div class="container">
					<div class="questions-description text-center">
						<h3 class="fw-bold">Frequently Asked Questions</h3>
						<p class="text-muted">Here are some of our FAQs.If you have any other questions you’d like
							answered please feel free to email us.</p>
					</div>
					<div class="frequently-questions">
						<ul>
							<li @click="showQuestion">
								<div>
									What is Bookmark?
									<img src="../assets/icon-arrow.svg" alt="">
								</div>
								<span>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Fusce tincidunt justo
									eget ultricies fringilla. Phasellus blandit ipsum quis quam ornare mattis.</span>
							</li>
							<li @click="showQuestion">
								<div>
									How can I request a new browser?
									<img src="../assets/icon-arrow.svg" alt="" />
								</div>
								<span>Vivamus luctus eros aliquet convallis ultricies. Mauris augue massa, ultricies non
									ligula. Suspendisse imperdiet. Vivamus luctus eros aliquet convallis ultricies.
									Mauris augue massa, ultricies non ligula. Suspendisse imperdie tVivamus luctus eros
									aliquet convallis ultricies. Mauris augue massa, ultricies non ligula. Suspendisse
									imperdiet.</span>
							</li>
							<li @click="showQuestion">
								<div>
									Is there a mobile app?
									<img src="../assets/icon-arrow.svg" alt="" />
								</div>
								<span>Sed consectetur quam id neque fermentum accumsan. Praesent luctus vestibulum
									dolor, ut condimentum urna vulputate eget. Cras in ligula quis est pharetra mattis
									sit amet pharetra purus. Sed sollicitudin ex et ultricies bibendum.</span>
							</li>
							<li @click="showQuestion">
								<div>
									What about other Chromium browsers?
									<img src="../assets/icon-arrow.svg" alt="" />
								</div>
								<span>Integer condimentum ipsum id imperdiet finibus. Vivamus in placerat mi, at euismod
									dui. Aliquam vitae neque eget nisl gravida pellentesque non ut velit.</span>
							</li>
						</ul>
						<div class="frequently-button">
							<button class="btn">
								More Info
							</button>
						</div>
					</div>
				</div>
			</div>
			<div class="bookmark-contact">
				<div class="contact-description">
					<p>35,000+ already joined</p>
					<span>Stay up-to-date with what we’re doing</span>
				</div>
				<div class="contact-form">
					<form id="form-contact" :class="{'error-validation': !FormValidation.isValid}">
						<div class="form-input">
							<input type="email" placeholder="Enter your email address" required="">
							<div class="error-input-message" v-if="!FormValidation.isValid">
								{{FormValidation.message}}
							</div>
							<span class="icon-input-error">
								<img src="../assets/icon-error.svg" alt="">
							</span>
						</div>
						<div class="form-button">
							<button type="button" class="btn" @click="formContact">Contact Us</button> 
						</div>
					</form>
				</div>
			</div>
		</div>
		<div class="footer-nav">
			<div class="container"> 
				<div class="row">
					<div class="col-md-3 text-center text-md-end">
						<img class="img-footer-logo" src="../assets/logo-bookmark-footer.svg" alt="">
					</div>
					<div class="col-md-6 text-center text-md-start">
						<ul class="footer-links">
							<li class="d-block d-md-inline">
								<a href="">FEATURES</a>
							</li>
							<li class="d-block d-md-inline">
								<a href="">PRICING</a>
							</li>
							<li class="d-block d-md-inline">
								<a href="">CONTACT</a>
							</li>
						</ul>
					</div>
					<div class="col-md-3 text-center text-md-end social-media-footer">
						<ul>
							<li>
								<a href="#">
									<img src="../assets/icon-facebook.svg" alt="" />
								</a>
							</li>
							<li>
								<a href="#">
									<img src="../assets/icon-twitter.svg" alt="" />
								</a>
							</li>
						</ul>
					</div>
				</div>
			</div>
		</div>
	</div>
</template>

<script>
import TabSimpleBookMark from "@/components/TabSimpleBookMark"
import TabSpeedySearching from "@/components/TabSpeedySearching"
import TabEasySharing from "@/components/TabEasySharing"
export default {
	components: {
		TabSimpleBookMark,
		TabSpeedySearching,
		TabEasySharing,
	},
	data() {
		return {
			menuOpened: false,
			featuresComponent: "TabSimpleBookMark",
			FormValidation: {isValid: true, message: ""}
		}
	},
	methods: {
		showQuestion(e){
			let element = e.currentTarget
			if(element.className.indexOf('active') == -1){
				element.classList.add('active')
			}else{
				element.classList.remove('active')
			}
		},
		formContact(e){
			let input = document.querySelector('#form-contact input')
			if(!input.validity.valid && input.validity.typeMismatch){
				this.FormValidation.isValid = false
				this.FormValidation.message = "Whoops, make sure it's an email"
			}else{
				this.FormValidation.isValid = true
				this.FormValidation.message = ""
			}
		}
	}
}
</script>

<style lang="scss">

.page{
	.nav-header{
		.navbar{
			background-color: #fff;
			transition: .5s;
		}
		.navbar-toggler{
			border: none;
			box-shadow: none;
			img{
				width: 25px;
			}

			&[aria-expanded="true"] img{
				content: url(../assets/icon-close.svg);
			}
		}
		.nav-item {
			width: 100%;
			a {
				text-transform: uppercase;
				color: #000;

				&:hover{
					color: #ff5c5c !important;
				}
				&.btn{
					padding: 10px 30px;
					font-weight: 600;
					color: #fff;
					background: #ff5c5c;
					box-shadow: 0px 7px 8px #ccc;

					&:hover{
						background: transparent;
						outline: 2px solid #ff5c5c;
						color: #ff5c5c
					}
				}
			}
		}
		.social-media{
			ul{
				list-style:none;
				padding: 0;
				li{

					&:first-child a:hover img{
						content: url(../assets/icon-facebok-active.svg);
					}
					&:last-child a:hover img{
						content: url(../assets/icon-twitter-active.svg);
					}
					padding:0;
					display: inline;
					padding: 0 10px;
				}
			}
		}
	}
	.main{
		margin-top: 110px;

		.back-simple-bookmark-right{
			z-index: -1;
			position: absolute;
			right: 0;
			top: 35%;
			width: 40%;
			height: 55%;
			border-radius: 160px 0 0 160px;
			background-color: #4f62d8;
		}
		
		.simple-bookmark{

			.btn{
				box-shadow: 0px 5px 10px #ccc;
				background: #4f62d8;
				color: #fff;
				
				&:hover{
					background: #fff;
					color: #4f62d8;
					outline: 2px solid #4f62d8;
				}
				&:last-child{
					background: #f7f7f7;
					color: #333;
					
					&:hover{
						background: #fff;
						color: #333;
						outline: 2px solid #333;
					}
				}
			}
		}
		.features{
			position: relative;
			.features-description{
				padding: 0 20%;
			}
			.back-simple-bookmark-left{
				z-index: -1;
				position: absolute;
				left: 0;
				top: 60%;
				width: 40%;
				height: 50%;
				border-radius: 0 160px 160px 0;
				background-color: #4f62d8;
			}
			.features-tabs{
				.nav-tab{
					display: flex;
					list-style: none;
					justify-content: space-around;
					width: 70%;
					.tab-item {
						border-bottom: 1px solid #ccc;
						width: 100%;

						&:hover{
							color: #ff5c5c !important;
							cursor: pointer;
						}

						&.active {
							font-weight: 600;
							border-bottom: 5px solid red !important;
						}
					}
				}
			}
		}
		.bookmark-card{
			width: 100%;
    		max-width: 275px;
			text-align: center;
			padding: 35px 15px;
			box-shadow: 0px 9px 7px 0px #d8e7f9;
			position: relative;
			margin: auto;
			border-radius: 10px;
			&.card-firefox{
				margin-top: 80px;
			}
			&.card-opera{
				margin-top: 160px;
			}
			.bookmark-card-description{
				padding: 30px 0;
			}
			.bookmark-card-hr{
				position: absolute;
				top: 70%;
				left: 0;
				width: 100%;
				height: 25px;
				background-position: center;
				background-size: contain;
				background: url(../assets/bg-dots.svg) no-repeat;
			}
			.bookmark-card-footer{
				.btn{
					background: #5266df;
					color: #fff;
				}
			}
		}
		.frequently-asked-questions{
			.questions-description{
				max-width: 450px;
				margin: 200px auto 50px auto;
			}
			.frequently-questions{
				max-width: 500px;
				margin: auto;
				ul{
					list-style: none;
					padding: 0;
					li{
						padding: 20px 10px 40px 0;
						border-top: 1px solid #ccc;
						transition-property: background-color, border-radius;
						max-height: 0;
						overflow: hidden;
						transition: 0.5s linear;

						&:last-child {
							border-bottom: 1px solid #ccc;
						}

						&:hover{
							cursor: pointer;
						}

						div{
							margin: 0;
							padding: 0;
							padding-bottom: 20px;
							img{
								text-align: right;
								float: right;
								margin-top: 5px;
								transition: 0.2s;
							}
						}
						&:hover{
							div{
								color: #ff5c5c;
							}
						}
						&.active{
							max-height: 15em;
							transition: 0.5s linear;
							div{
								img{
									content: url(../assets/icon-arrow-active.svg);
									transform: rotate(180deg);
								}
							}
						}
					}
				}
				.frequently-button{
					text-align: center;

					.btn{
						background: #5266df;
						color: #fff
					}
				}
			}
		}
		.bookmark-contact{
			margin-top: 50px;
			background: #4f62d8;
			padding: 40px 10px;
			text-align: center;
			p{
				color: #fff;
				text-transform: uppercase;
			}
			span{
				color: #fff;
    			font-size: 2em;
			}
			.contact-description{
				max-width: 370px;
    			margin: auto;
			}
			.contact-form{
				margin-top: 30px;
				form{
					display: grid;
					grid-template-columns: 55% 45%;
					.form-input{
						text-align: end;
						position: relative;
						input{
							padding: 12px;
							padding-right: 30px;
							border-radius: 3px;
							outline: none;
							border: none;
							max-width: 270px;
							font-size: 0.9em;
							width: 100%;
						}
						.error-input-message{
							background: #ff5c5c;
							color: #fff;
							border-radius: 0 0 10px 10px;
							text-align: center;
							max-width: 270px;
							margin-left: auto;
							display: none;
						}
						.icon-input-error{
							position: absolute;
							top: -5px;
							right: 5px;
							display: none;
						}
					}
					.form-button{
						text-align: start;
						padding-left: 20px;
						button{
							padding: 10px 15px;
							background: #ff5c5c;
							color: #fff;
							font-weight: 600;

							&:hover{
								background: #ccc;
								color: #333;
							}
						}
					}
					&.error-validation{
						input{
							outline: 2px solid #ff5c5c;
						}
						button{
							&:hover{
								background: #fff;
								color: #ff5c5c;
								outline: 2px solid;
							}
						}
						.error-input-message, .icon-input-error{
							display: block !important;
						}
					}
				}
			}
		}
	}
	.footer-nav{
		background: rgba(47, 53, 79, 1) !important;
		padding-top: 20px;
		
		.img-footer-logo{
			width: 160px;
		}

		ul{
			list-style:none;
			padding: 0;
			&.footer-links{
				margin-top: 3px;
			}

			li{
				display: inline-block;
				padding: 0 10px;

				a{
					text-decoration: none;
					color: #d8e7f9;

					&:hover{
						color: #ff5c5c;
					}
				}
			}
		}
		.social-media-footer{
			ul{
				list-style:none;
				padding: 0;
				li{

					&:first-child a:hover img{
						content: url(../assets/icon-facebok-active.svg);
					}
					&:last-child a:hover img{
						content: url(../assets/icon-twitter-active.svg);
					}
					padding:0;
					display: inline;
					padding: 0 10px;
				}
			}
		}
	}

	@media (max-width: 991px){
		.features-tabs{
			.nav-tab{
				width: 80% !important;
			}
		}
	}

	@media (max-width: 767px){
		.nav-header{
			.menu-active{
				background-color: rgba(#2f354f, .9) !important;
				.navbar-brand img{
					content: url(../assets/logo-bookmark_menu-active.svg);
				}
				.nav-item{
					width: 100%;
					.nav-link{
						color: #fff;
						&.btn{
							box-shadow: none;
							&:hover{
								background: transparent;
								outline: 2px solid #fff;
								color: #fff !important;
							}
						}
					}	
				}
			}
		}
		.main{
			.back-simple-bookmark-right{
				height: 45%;
				width: 65%;
				top: 25%;
			}
			.features-description{
				padding: 0 !important;
			}
			.simple-bookmark-buttons{
				text-align:center;
			}
			.features-tabs{
				.nav-tab{
					padding: 0;
					display: block !important;
					list-style: none !important;
					text-align: center !important;
				}
			}
			.bookmark-card{
				margin-top: 50px !important;
			}
			.contact-form{
				form{
					grid-template-columns: 100% !important;
					.form-input{
						position: relative;
						display: inline-block;
						width: 100%;
						max-width: 270px;
						margin: auto;
						text-align: center !important;
					}
					.form-button{
						text-align: center !important;
						margin-top: 20px
					}
				}
			}
		}
		.footer-nav{

			ul{

				li{
					padding-top: 20px;
				}
			}
		}
	}

	@media (max-width: 574px){
		.main{
			text-align: center;
			.back-simple-bookmark-right{
				height: 50vw;
				width: 65%;
				top: 15%;
				transform: translate(0,6%);
			} 
		}
	}

}
</style>