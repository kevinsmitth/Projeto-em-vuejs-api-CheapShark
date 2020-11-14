<template>
    <div style="background:#171a21;">
        <b-navbar toggleable="lg" type="dark"  class="container p-3 px-5" >
            <b-navbar-brand href="#"><img src="https://store.cloudflare.steamstatic.com/public/shared/images/header/globalheader_logo.png?t=962016"
             alt="" width="180"></b-navbar-brand>

            <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>

            <b-collapse id="nav-collapse" is-nav>
            <b-navbar-nav>
                <b-nav-item href="#">LOJA</b-nav-item>
            </b-navbar-nav>
            <b-navbar-nav>
                <b-nav-item href="#">COMUNIDADE</b-nav-item>
            </b-navbar-nav>
            <b-navbar-nav>
                <b-nav-item href="#">SOBRE</b-nav-item>
            </b-navbar-nav>
            <b-navbar-nav>
                <b-nav-item href="#">SUPORTE</b-nav-item>
            </b-navbar-nav>
            <div class="ml-auto d-none d-lg-block d-xl-block " style="top:0;position:absolute;right:0;">
                <b-navbar-nav >
                    <button class="btn btn-sm btn-success ">Instalar o Steam</button>
                    <b-nav-item-dropdown text="Idioma" right>
                    <b-dropdown-item href="#">EN</b-dropdown-item>
                    <b-dropdown-item href="#">ES</b-dropdown-item>
                    <b-dropdown-item href="#">RU</b-dropdown-item>
                    <b-dropdown-item href="#">FA</b-dropdown-item>
                    </b-nav-item-dropdown>

                    <b-nav-item-dropdown right>
                    <!-- Using 'button-content' slot -->
                    <template #button-content>
                        <em>User</em>
                    </template>
                    <b-dropdown-item href="#">Profile</b-dropdown-item>
                    <b-dropdown-item href="#">Sign Out</b-dropdown-item>
                    </b-nav-item-dropdown>
                </b-navbar-nav>
            </div>
            </b-collapse>
        </b-navbar>
    </div>
</template>

<style>
    .navbar{
        list-style: none;
        display: inline-flex;
    }
    .navbar li{
        margin: 15px;
    }
    .navbar li:hover{
        background: #171a21;
    }
    .navbar li a:hover{
        color:#ffffff !important;
    }
</style>