<template>
    <span>
        <v-app-bar app color="primary" dark>
            <v-toolbar-title class="title-menu">Simpliz</v-toolbar-title>
            <v-spacer></v-spacer>
            <span class="hidden-md-and-up">
                <v-app-bar-nav-icon @click="sidebar = !sidebar" />
            </span>
            <v-btn class="text-lowercase item-menu hidden-sm-and-down" text to="/">Home</v-btn>
            <v-btn class="text-lowercase item-menu hidden-sm-and-down" text to="/plans">Preços</v-btn>
            <v-btn class="text-lowercase item-menu hidden-sm-and-down" text to="/cart">Carrinho</v-btn>
        </v-app-bar>

        <v-navigation-drawer v-model="sidebar" class="hidden-md-and-up primary" app dark temporary>
            <v-list>
                <v-list-item link to="/">
                    <v-list-item-content>
                        <v-list-item-title class="item-menu">Home</v-list-item-title>
                    </v-list-item-content>
                </v-list-item>
                <v-list-item link to="/plans">
                    <v-list-item-content>
                        <v-list-item-title class="item-menu">Preços</v-list-item-title>
                    </v-list-item-content>
                </v-list-item>
                <v-list-item link to="/cart">
                    <v-list-item-content>
                        <v-list-item-title class="item-menu">Carrinho</v-list-item-title>
                    </v-list-item-content>
                </v-list-item>
            </v-list>
        </v-navigation-drawer>
    </span>
</template>

<script>
export default {
    name: "MenuBar",
    data() {
        return {
            sidebar: false,
        };
    },
};
</script>

<style scoped>
.v-toolbar__content {
    gap: 10px;
}

.title-menu {
    font-family: var(--simpliz-title-font);
    font-size: 1.5rem;
    letter-spacing: 2px;
}

.item-menu {
    font-weight: 700;
}
</style>