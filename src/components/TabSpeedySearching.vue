<template>
	<div class="tab-speedy-search mt-5 position-relative">
		<div class="container">
			<div class="row align-items-center tab-speedy-search-image">
				<div class="col-md-6 mb-5">
					<img class="img-fluid" src="../assets/illustration-features-tab-2.svg" alt="" />
				</div>
				<div class="col-md-6 tab-speedy-search-content container">
					<h3 class="fw-bold">Intelligent search</h3>
					<p class="text-muted">Our powerful search feature will help you find saved sites in no time at all. No need to trawl through all of your bookmarks.</p>
					<div class="simple-bookmark-buttons">
						<button class="btn">More info</button>
					</div>
				</div>
			</div>
		</div>
	</div>
</template>

<script>
export default {

}
</script>

<style lang="scss">

.back-simple-bookmark-left{
	top: 50% !important;
}

.tab-speedy-search{
	.back-simple-bookmark-left{
		z-index: -1;
		position: absolute;
		left: 0;
		top: 35%;
		width: 40%;
		height: 80%;
		border-radius: 0 160px 160px 0;
		background-color: #4f62d8;
	}
	.tab-speedy-search-content{
		text-align: justify;
		padding: 0 80px 0 40px;
		.btn{
			background-color: #4f62d8;
			color: #fff;
			padding: 13px 30px;
		}
	}
}
@media (max-width: 991px){
	.main{
		.back-simple-bookmark-left{
			height: 35% !important;
			width: 40% !important;
			top: 60% !important;
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
		.back-simple-bookmark-left{
			height: 35% !important;
			width: 65% !important;
			top: 40% !important;
		}
		.tab-speedy-search-content{
			margin-top: 80px;
			text-align: center;
		}
	}
}

@media (max-width: 574px){
	.main{
		.back-simple-bookmark-left{
			height: 50vw !important;
			width: 65%;
			top: 15%;
			transform: translate(0,6%);
		}
		.tab-speedy-search-content{
			padding: 0;
		}
	}
}
</style>