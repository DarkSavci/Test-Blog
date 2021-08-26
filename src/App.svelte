<script>
	import Post from "./Post.svelte";
	import SearchBar from "./SearchBar.svelte";
	import TopBar from "./TopBar.svelte";
</script>

<main>
	<TopBar />

	<div class="slider">
		<div class="middle">
			<div class="article">
				En Başarılı İnsan, En İyi Bilgiye Sahip Olandır
				<span>Blogumuzda arayın</span>
			</div>

			<div class="searcharea">
				<SearchBar />
			</div>
		</div>
		<div
			class="coveredImg"
			style="background-image: url('https://external-content.duckduckgo.com/iu/?u=https%3A%2F%2Fwww.nottingham.ac.uk%2FCurrentStudents%2FImages%2FNews%2F2019%2Fbooks-current-students.x61f638e8.jpg&f=1&nofb=1');"
		/>
	</div>

	<div class="posts">
		<h2 class="title">Blog Yazıları | IIENSTITU</h2>

		<ul class="postsList">
			<li class="post">
				<Post
					title="Oryantasyon Süreci Nedir?"
					description="Oryantasyon, yönlendirme, kılavuzluk anlamlarını taşır. Oryantasyon sü..."
					image="https://www.iienstitu.com/uploads/blog-yazilari-agustos2021/risk-analiz-yontemleri_w378_h195_op.jpg"
					
					authorName="Bedirhan Dinç"
					date="18 Ağustos 2021"
					/>
			</li>

			<li class="post">
				<Post title="Başlık" />
			</li>
			<li class="post">
				<Post title="Başlık" />
			</li>
			<li class="post">
				<Post title="Başlık" />
			</li>
			<li class="post">
				<Post title="Başlık" />
			</li>
			<li class="post">
				<Post title="Başlık" />
			</li>
			<li class="post">
				<Post title="Başlık" />
			</li>
			<li class="post">
				<Post title="Başlık" />
			</li>
			<li class="post">
				<Post title="Başlık" />
			</li>
			<li class="post">
				<Post title="Başlık" />
			</li>
			<li class="post">
				<Post title="Başlık" />
			</li>
		</ul>
	</div>
</main>

<style>
	.slider {
		position: relative;
		width: 100%;
		height: 370px;
	}

	.slider .middle {
		width: 100%;
		position: absolute;
		top: 50%;
		left: 50%;
		transform: translateX(-50%) translateY(-50%);
		color: #fff;
		z-index: 1;
	}

	.slider .middle .article {
		text-align: center;
		display: block;
		font-size: 28px;
		font-weight: bold;
		line-height: 49px;
		margin-bottom: 10px;
	}

	.slider .middle .article span {
		text-align: center;
		display: block;
		font-weight: lighter;
		font-size: 20px;
		line-height: 27px;
	}

	.slider .coveredImg {
		background-size: cover;
		width: 100%;
		height: 100%;
		object-fit: cover;
		object-position: center bottom;
		background-position: center bottom;
	}

	.slider .coveredImg::after {
		content: "";
		position: absolute;
		inset: 0px;
		background-color: rgba(0, 0, 0, 0.3);
	}

	.posts .title {
		font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
		color: #fff;
		margin-left: 50px;
		top: 50px;
	}

	.posts .postsList {
		position: relative;
	}

	.posts li {
		display: block;
		color: #fff;
		-webkit-box-sizing: border-box;
		-moz-box-sizing: border-box;
		box-sizing: border-box;
		float: left;
		width: 25%;
		padding: 15px;
	}
</style>
