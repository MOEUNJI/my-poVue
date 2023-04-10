<template>
    <div class="container">
        <div class="pro_title">
            <img src="" alt="">
            <h2>{{ title_name }}</h2>
        </div>
        <div class="pro_detail">
            <p>{{ detail_1 }}
                <span>{{ detail_01 }}</span>
            </p>
            <p>{{ detail_2 }}
                <span>{{ detail_02 }}</span>
            </p>
            <p>{{ detail_3 }}
                <span>{{ detail_03 }}</span>
            </p>
        </div>
    </div>
</template>

<script>
export default {
    name: 'profile',
    props: ['title_img','title_name','detail_1','detail_2','detail_3','deatil_01','detail_02','detail_03'],
        data() {
        return {
        }
    },
}
</script>

<style>

</style>