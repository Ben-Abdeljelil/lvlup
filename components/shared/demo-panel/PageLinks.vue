<template lang="html">
    <v-tabs
        background-color="gray"
        color="warning"
        class="ps-tab-list"
        grow
        centered
    >
        <v-tab>
            <a href="#" @click.prevent class="tab-item">Hompages</a>
        </v-tab>
        <v-tab-item>
            <div class="tab-content pt-3">
                <div class="row">
                    <div
                        v-for="demo in homepages"
                        class="col-md-4 col-6"
                        :key="demo.id"
                    >
                        <demo-item :demo="demo" />
                    </div>
                </div>
            </div>
        </v-tab-item>
    </v-tabs>
</template>

<script>
import DemoItem from '~/components/elements/commons/DemoItem';
export default {
    name: 'PageLinks',
    components: { DemoItem },
    data() {
        return {
            homepages: [
                {
                    id: 1,
                    url: '/'
                }
            ]
        };
    }
};
</script>

<style lang="scss" scoped>
.tab-item {
    font-size: 16px;
    color: $color-heading;
    font-weight: 600;
}
</style>
