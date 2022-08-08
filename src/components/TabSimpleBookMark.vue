<template>
	<div class="tab-simple-bookmark mt-5 position-relative">
		<div class="container">
			<div class="row align-items-center tab-simple-bookmark-image">
				<div class="col-md-6 mb-5">
					<img class="img-fluid" src="../assets/illustration-features-tab-1.svg" alt="" />
				</div>
				<div class="col-md-6 tab-simple-bookmark-content container">
					<h3 class="fw-bold">Bookmark is one click</h3>
					<p class="text-muted">Organize you bookmarks however you like. Our simple drag-and-drop interface gives you complete control over how you manage your favourite sites.</p>
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

.tab-simple-bookmark{
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
	.tab-simple-bookmark-content{
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
		.tab-simple-bookmark-content{
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
		.tab-simple-bookmark-content{
			padding: 0;
		}
	}
}
</style>