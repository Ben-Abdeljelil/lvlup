<template lang="html">
    <header class="header header--mobile">
        <div class="navigation--mobile">
            <div class="navigation__left">
                <nuxt-link to="/" class="ps-logo">
                    <img src="~/static/img/logo_light.png" alt="martfury" />
                </nuxt-link>
            </div>
            <mobile-header-actions />
        </div>
    </header>
</template>

<script>
import MobileHeaderActions from '~/components/shared/mobile/modules/MobileHeaderActions';
export default {
    name: 'HeaderMobile',
    components: { MobileHeaderActions }
};
</script>

<style lang="scss" scoped></style>
