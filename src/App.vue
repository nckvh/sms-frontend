<template>
  <div id="app">
    <div v-for="i in 4" class="card">
        <h2 class="website">Site {{i}}</h2>
        <div class="stats">
            <div class="metric">
                <p class="badge">campaigns</p>
                <div class="icon">
                    <i class="material-icons">chat</i>
                    2
                </div>
            </div>
            <div class="metric">
                <p class="badge">leads</p>
                <div class="icon">
                    <i class="material-icons">face</i>
                    14
                </div>
            </div>
            <div class="metric">
                <p class="badge">conversions</p>
                <div class="icon">
                    <i class="material-icons">done</i>
                    4
                </div>
            </div>
        </div>
    </div>

    <div class="fab" darken>
        <i class="material-icons" >add</i>
    </div>
  </div>
</template>

<script>
import Vue from 'vue'
import $ from 'jquery'
export default {
    data () {
        return {
            msg: 'Hello Vue!'
        }
    },
    methods{
        darken(){
            
        }
    }

}
</script>

<style lang="stylus">
@import './stylus/resources.styl'

body
    font-family 'Helvetica'
    background rgb(40,70,100)
    color rgb(240,230,230)

h1,h2
    font-weight normal


#app
    grid('column', 'center', 'center')
    height 100vh
    .card
        padding rem-calc(1rem)
        background rgb(10,10,40)
        min-width 400px
        width 40%
        box-shadow 1px 1px 2px rgba(40,40,40,.3)
        transition .14s
        cell(1,4, g:rem-calc(5rem))
        &:hover
            box-shadow 2px 4px 2px rgba(40,40,40,.7)
        .website
            color white
            margin-bottom rem-calc(2rem)
        .stats
            grid(row)
            .metric
                grid('column', 'center', 'center')
                cell(1,3, g:rem-calc(1rem))
                .icon
                    grid('row','center','center')
                    .material-icons
                        font-size 2em
    .fab
        background rgb(240,230,230)
        border-radius 50px
        font-size 1em
        line-height 1em
        height 50px
        width 50px
        grid('row','center','center')
        color rgb(10,10,40)
        transition .2s
        box-shadow 1px 1px 2px rgba(0,0,0,.3)
        cursor pointer
        &:hover
            background rgb(250,240,240)
            box-shadow 1px 4px 2px rgba(0,0,0,.5)
        &.darken
            background rgb(200,190,190)






</style>
