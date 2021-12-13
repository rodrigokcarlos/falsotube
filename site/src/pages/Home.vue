<template>
    <main>
        <div class="text-top">Vídeos novos Toda às <b>sextas</b></div>
        <a href="https://www.youtube.com/channel/UCYEyqiE0unD6BjYQZiCPMPw" target="_blank">
        <img src="https://raw.githubusercontent.com/william-costa/wdev-mock-site-resources/master/assets/images/subscribe.svg" alt="Inscreva-se" id="subscribe"></a>
        <div class="text-bottom">youtube.com/rodrigokazan</div>
    </main>
</template>
<script>
export default {
    name: 'Home'
}
</script>
<style scoped>
    main{
        background-color: var(--color-background-home);
        justify-content: center;
        align-items: center;
    }
    .text-top{
        color: var(--color-text-light);
        font-size: 22px;
        margin-bottom: 20px;
    }
    #subscribe{
        width: 340px;
    }
    .text-bottom{
        color: var(--color-text-light);
        font-size: 18px;
        margin-top: 20px;
    }
    @media(min-width:700px){
        #subscribe{
            width: 370px;
        }
    }
</style>