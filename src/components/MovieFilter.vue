<template>
        <div id="movie-filter">
            <h2>filter results</h2>
            <h3>By Time Of Day</h3>
            <div class="filter-group">
                <check-filter category="time" v-for="time in times" v-bind:title="time" ><check-filter>
            </div>
            <h3>By Genre</h3>
            <div class="filter-group">
                <check-filter category="genre" v-for="genre in genres" v-bind:title="genre" ><check-filter>
            </div>
        </div>
</template>

<script>
import genres from '../util/genres.js'
import times from '../util/times.js'
import CheckFilter from './CheckFilter.vue'
export default{
    data() {
        return {
            genres,
            times
            }
        },
        components: {
            CheckFilter
        }
    }
</script>