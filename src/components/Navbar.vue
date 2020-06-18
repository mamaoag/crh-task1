<template>
    <nav>
        <div class="row">
            <div class="col _20"></div>
            <div class="col _60">
                <div class="container">
                    <span class="toggle" @click="showMenu">
                        <i class="fas fa-bars"></i>
                    </span>
                    <div class="brand">
                        <h1>CRHSAMPLE</h1>
                    </div>
                    <ul class="main" ref="menu">
                        <li v-for="link in links" :key="link">
                            <a href="#">{{ link }} </a>
                        </li>
                    </ul>
                </div>
            </div>
            <div class="col _20"></div>
        </div>
    </nav>
</template>

<script>
export default {
    data() {
        return {
            links: [
                'News',
                'Service',
                'Company',
                'Contact'
            ]
        }
    },
    
    methods: {
        showMenu() {
            this.$refs.menu.classList.toggle('active')
        }
    }
}
</script>

<style>
    nav {
        height: 100px;
        max-height: 100px;
        background: linear-gradient(var(--color-primary), var(--color-secondary) 10%);
        color: #fff;
    }

    .container {
        display: flex;
        height: 100%;
        margin: auto;
        justify-content: space-between;
    }

    .main {
        display: flex;
        flex-direction: row;
        justify-content: flex-end;
        margin: auto;
        float: right;
        width: 100%;
    }

    .main > li {
        list-style-type: none;
        margin-left: 10px;
        margin-right: 10px;
    }

    .main > li > a {
        color: #fff;
        text-transform: uppercase;
        text-decoration: none;
    }

    .brand > h1 {
        font-size: 36px;
    }

    .toggle {
        display: none;
    }

    @media (max-width: 767.98px) { 
        .toggle {
            display: block;
            top: 45px;
            right: 20px;
            position: absolute;
            cursor: pointer;
        }  
        
        .container { 
            padding: 5px;
            display: block;
        }

        .brand {
            display: inline-block;
        }

        .active {
            display: block !important;
        }

        .main {
            display: none;
            text-align: center;
        }

        .main > li {
            padding: 5px;
            margin-bottom: 10px;
        }

        nav {
            height: 100%;
            max-height: 100%;
        }

        #section-content p{
            padding: 10px;
            text-align: justify;
        }

        #news-events {
            padding: 10px;
        }
        
        .link {
            margin-right: 10px;
        }
     }
</style>