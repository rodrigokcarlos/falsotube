<template>
    <header>
        <nav class="container">
            <a href="/">
                <img src="https://www.tenhomaisdiscosqueamigos.com/wp-content/uploads/2017/09/YouTube-novo-logo.jpg" alt="YT" id="logo"></a>
            <img v-on:click="openMenu" src="https://raw.githubusercontent.com/william-costa/wdev-mock-site-resources/master/assets/images/menu.svg" alt="Abrir Menu" id="menu-button">
            <div v-on:click="closeMenu" id="menu-overlay" v-if="menuActive"></div>
            <div id="menu-items" :class="{active:menuActive}">
                <img src="https://www.tenhomaisdiscosqueamigos.com/wp-content/uploads/2017/09/YouTube-novo-logo.jpg" alt="YT" id="menu-logo">
                <ul>
                    <li><a href="/">Home</a></li>
                    <li><a href="/videos">Video</a></li>
                    <li><a href="/sobre">Sobre</a></li>
                    <li><a href="/contato">Contato</a></li>
                </ul>
            </div>
            
        </nav>
    </header>
</template>
<script>
export default {
    name:'Header',
    data(){
        return{
            menuActive: false
        }
    },
    methods:{
        openMenu: function(){
            this.menuActive = true;

        },
        closeMenu: function(){
            this.menuActive = false;
        }
    }
}
</script>
<style scoped>

    header{
        background-color: var(--color-background-nav);
        width: 100%;
        height: 60px;
        display: flex;
        justify-content: center;
        align-items: center;
    }
    nav{
        display: flex;
        justify-content: space-between;
        height: 60px;
        align-items: center;
    }
    #logo{
        /* width: 130px; */
        height: 60px;
    }
    #menu-button{
        width: 30px;
    }
    #menu-overlay{
        position: fixed;
        top: 0;
        left: 0;
        width: 40%;
        height: 100vh;
        background-color: #000000;
        opacity: 0.8;
    }
    #menu-logo{
        margin-top: 10px;
        width: 110px;
    }
    #menu-items{
        position: fixed;
        top: 0;
        right: 0;
        background-color: var(--color-background-nav);
        width: 60%;
        height: 100vh;
        display: none;
        flex-direction: column;
        justify-content: flex-start;
        align-items: center;
    }
    #menu-items.active{
        display: flex;
    }
    ul {
        list-style: none;
        text-align: center;
    }
    ul li{
        margin: 20px 0px;
    }
    ul li a{
        color: var(--color-text-light);
    }
    @media (min-width:720px){
        #menu-button,
        #menu-logo,
        #menu-verlay{
            display: none;
        }
        #menu-items{
            display: flex;
            position: static;
            height: 60px;
            width: auto;
        }
        ul{
            display: flex;
            height: 60px;
            align-items: center;
        }
        ul li{
            margin: 0;
            margin-left: 10px;
        }
    }
</style>