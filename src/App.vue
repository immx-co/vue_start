<template>
    <navbar
        :pages="pages"
        :active-page="activePage"
        :nav-link-click="(index) => activePage = index"
    ></navbar>

    <page-viewer 
        :page="pages[activePage]"
        >

    </page-viewer>
</template>

<script>
import PageViewer from './components/PageViewer.vue';
import Navbar from './components/Navbar.vue';

export default {
    components: {
        Navbar,
        PageViewer
    },
    data() {
            return {
                activePage: 0,
                themeContent: 'dark',
                pages: [
                    {
                        link: {
                            text: 'Home', url: 'index.html'
                        },
                        pageTitle: 'Home Page',
                        content: 'This is the home content'
                    },
                    {
                        link: {
                            text: 'About', url: 'about.html'
                        },
                        pageTitle: 'About Page',
                        content: 'This is the about content'
                    },
                    {
                        link: {
                            text: 'Contacticus', url: 'contacticus.html'
                        },
                        pageTitle: 'Contacticus Page',
                        content: 'This is the content about contacticus, my contacticus'
                    }
                ]
            };
        }
}
</script>