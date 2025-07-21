<script>
    let { title, subtitle } = $props();
</script>

<div class="title-card">
    <div class="content">
        <h1>{title}</h1>
        <p>{subtitle}</p>
    </div>
</div>

<style>
    .title-card {
        background-color: #fefcfb;
        height: 100vh;
        display: flex;
        justify-content: center;
        align-items: center;
        text-align: center;
        padding: 2rem;
        box-sizing: border-box;
        font-family: "Kanit", sans-serif;
    }

    .content {
        max-width: 800px;
        background-color: #1282a2;
        padding: 2rem;
        /* border: 6px solid #F2DC5D; */
        /* border-radius: 2rem; */
        box-shadow: 10px 10px #001f54;
    }

    h1 {
        font-size: 3rem;
        margin: 0;
        color: #000000;
        /* text-shadow: 1px 1px 0 #007052; */
    }

    p {
        font-size: 1.3rem;
        color: #f7f5eb;
        margin-top: 1rem;
    }

    @media (max-width: 600px) {
        h1 {
            font-size: 2.2rem;
        }

        p {
            font-size: 1.1rem;
        }
    }
</style>