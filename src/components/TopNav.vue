<template>
    <div>
        <nav class="navbar navbar-expand-lg navbar-light bg-light border-bottom">
            <button class="btn btn-primary" id="menu-toggle">Toggle Menu</button>

            <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
            <span class="navbar-toggler-icon"></span>
            </button>

            <div class="collapse navbar-collapse" id="navbarSupportedContent">
                <ul class="navbar-nav ml-auto mt-2 mt-lg-0">
                    
                    <li class="nav-item " v-bind:class="{dropdown: top_menu.child }" v-bind:key="top_menu.id" v-for="top_menu in top_menus">
                        <a class="nav-link" v-bind:class="{'dropdown-toggle': top_menu.child }" href="#" id="navbarDropdown" role="button" data-toggle="dropdown" aria-haspopup="true" aria-expanded="false">
                            {{top_menu.name }}
                        </a>
                        <div class="dropdown-menu dropdown-menu-right" aria-labelledby="navbarDropdown" v-if="top_menu.child">
                            <a class="dropdown-item" href="#" v-bind:key="child.id" v-for="child in top_menu.child">{{ child.name }}</a>                                    
                        </div>
                    </li>
                </ul>
            </div>
        </nav>
    </div>
</template>


<script>
export default {
    name: "TopNav",
    props: ['top_menus',]
}
</script>