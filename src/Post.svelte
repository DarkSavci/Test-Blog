<script>
	import Icon from '@smui/textfield/icon';
    export let title = "Unkown Title";
    export let image =
        "https://www.iienstitu.com/uploads/blog-yazilari-agustos2021/oryantasyon-sureci-nedir_w378_h195_op.jpg";
    export let description = "Unkown Description";

    export let authorName = "Unkown Author";
    export let authorImage =
        "https://www.iienstitu.com/uploads/blog-yazarlari/emine-busra-kanat.jpg";
    export let date = "24 Ağustos 2021";
</script>

<main>
    <div class="post">
        <img class="image" src={image} alt="Post Thumbnail" />
        <h4 class="title">{title}</h4>
        <p class="description">{description}</p>

        <div class="author">
            <img src={authorImage} alt="Author Img" class="authorImage" />
            <h6 class="authorName">{authorName}</h6>
            <p class="date">{date}</p>
        </div>
    </div>
</main>

<style>
    .post {
        border: 3px groove white;
        border-radius: 10px;
        min-height: 300px;

        -webkit-transition: opacity 0.2s ease-in-out;
        -moz-transition: opacity 0.2s ease-in-out;
        -ms-transition: opacity 0.2s ease-in-out;
        -o-transition: opacity 0.2s ease-in-out;
        transition: opacity 0.2s ease-in-out;
        opacity: 1;

        cursor: pointer;
    }

    .post:hover {
        opacity: 0.5;
    }

    .post .title {
        text-align: center;
        margin-top: 1px;
        font-family: "Segoe UI", Tahoma, Geneva, Verdana, sans-serif;
    }

    .post .description {
        font-family: "Segoe UI", Tahoma, Geneva, Verdana, sans-serif;
        margin-top: -10px;
        margin-left: 10px;
    }

    .post .image {
        width: 100%;
        height: 100%;
    }

    .post .author {
        position: relative;
        margin-left: 10px;
        align-content: center;
        overflow: hidden;
    }

    .post .author .authorImage {
        height: 40px;
        -moz-border-radius: 25%;
        -webkit-border-radius: 25%;
        border-radius: 50%;
    }

    .post .author .authorName {
        margin: -10px 50px 10px;
        margin-top: -40px;
        font-size: 14px;
    }

    .post .author .date {
        margin-left: 50px;
        margin-top: -5px;
        font-size: 12px;
        color: #979696;
    }
</style>
