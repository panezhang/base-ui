<!-- @author yutiangan -->
<!-- @email yutiangan@yangqianguan.com -->
<!-- @date 2018-09-25 14:53:55.596 -->
<!-- @desc generated by yqg-cli@0.2.2 -->

<template>

    <div class="b-card-media">
        <div v-if="isTitleShow" class="b-card-media-title">
            <div class="b-card-title">{{ title }}</div>

            <div class="b-card-subtitle">{{ subTitle }}</div>
        </div>

        <div class="b-card-media-content">
            <slot name="content"></slot>
        </div>

        <slot></slot>
    </div>

</template>

<script type="text/babel">

    export default {
        name: 'BCardMedia',

        props: {
            title: {
                type: String,
                default: ''
            },
            subTitle: {
                type: String,
                default: ''
            }
        },

        computed: {
            isTitleShow() {
                const vm = this;
                const {title, subTitle} = vm;

                return title || subTitle;
            }
        }
    };

</script>
