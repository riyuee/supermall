<template>
        <swiper>
            <swiper-item v-for="item in banners" :key="item.index"> 
                <!-- 不写:key=""会报错 item.acm也可以-->
                <!-- 因为值是动态变化的，所以加冒号：将这个属性当作变量解析，不加则当做字符串 -->
                <a :href="item.link">
                    <img :src="item.image" alt="">
                </a>
            </swiper-item>
        </swiper>
</template>

<script>
import {Swiper, SwiperItem} from 'components/common/swiper'

    export default {
        name: "HomeSwiper",
        props: {
            banners: {
                type: Array,
                default() {
                    return []
                }
            }
        },
        components: {
            Swiper,
            SwiperItem
        },
    }
</script>

<style scoped>

</style>