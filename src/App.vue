<script lang="ts">
    import Vue from 'vue';
    export default Vue.extend({
        mpType: 'app',
        onLaunch() {
            console.log('App Launch')
        },
        onShow() {
            console.log('App Show')
        },
        onHide(e) {
            console.log('App Hide')
          if (e.wheelDelta) {
            //判断浏览器IE，谷歌滑轮事件
            this.$store.commit('common/SET_WHEEL_DELTA', e.wheelDelta)
          } else if (e.detail) {
            //Firefox滑轮事件
            this.$store.commit('common/SET_WHEEL_DELTA', e.detail)
          }
          this.$store.commit('common/SET_SCROLL_DISTANCE', e.target.scrollTop)
        },

    });
</script>

<style>
    /*每个页面公共css */
</style>
