<template>
    <section class="albums container pt-5">
        <div class="row row-cols-1 row-cols-sm-2 row-cols-md-3 row-cols-lg-4 row-cols-xl-5 gx-4">
            <Album v-for="(album, index) in filteredAlbums" :key="index" :info="album"/>
        </div>
    </section>
</template>

<script>
import axios from 'axios';
import Album from '../components/Album';

export default {
    name: 'Albums',
    components: {
        Album
    },
    props: ['gnr'],
    data() {
        return {
            albums: []
        }
    },
    computed: {
        filteredAlbums() {
            return this.albums.filter(
                alb => {
                    return alb.genre == this.gnr || this.gnr == '';
                }
            )
        },
    },
    created() {
        axios
            .get("https://flynn.boolean.careers/exercises/api/array/music")
            .then((res) => {
                this.albums = res.data.response;

                const genres = [];
                this.albums.forEach( alb => {
                    if (genres.includes(alb.genre) == false) {
                        genres.push(alb.genre);
                    }
                })
                this.$emit('generateGenres', genres)
            });
    }
}
</script>

<style scoped lang="scss">
@import "../assets/style/variables.scss";


</style>