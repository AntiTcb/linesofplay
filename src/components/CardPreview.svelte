<script>
    export let card;
</script>

<div class="ygocard">
    <p class="name">{card.name}</p>
    <img class="pic" src={card.image} />
</div>

<style lang="scss">
    .ygocard {
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: center;
        width: 15rem;
        height: auto;
        border-radius: 0.5rem;
        box-shadow: 0 0.5rem 1rem rgba(0, 0, 0, 0.8);
        padding: 1rem 1rem;
    }
    .name {
        text-align: center;
    }
    .pic {
        max-width: 100%;
        max-height: 100%;
        aspect-ratio: 0.68;
        margin-top: 1rem;
    }
</style>
