<template>
<!-- 右侧菜单 -->
  <div class="marqueen">
          <span class="marqueen-title">商城头条</span>
          <div class="demo">
            <ul>
              <div class="mod-vip">
                <div class="m-baseinfo" v-if="!!token">
                  <a href="javascript:void(0)"><img src="/images/getAvatar.do.jpg" /></a><em>
                    Hi,<span class="s-name">{{token}}</span><a href="javascript:void(0)"><p>点击更多优惠活动</p></a></em>
                </div>
                <div class="member-logout" v-if="!token">
                  <router-link :to="{name:'Login'}" class="mr-btn-warning btn">登录</router-link>
                  <router-link :to="{name:'Register'}" class="mr-btn-warning btn">注册</router-link>
                </div>
                <div class="member-login" v-else style="display:block;">
                  <a href="javascript:void(0)"><strong>0</strong>待收货</a>
                  <a href="javascript:void(0)"><strong>0</strong>待发货</a>
                  <a href="javascript:void(0)"><strong>0</strong>待付款</a>
                  <a href="javascript:void(0)"><strong>0</strong>待评价</a>
                </div>
                <div class="clear"></div>
              </div>
              <li class="title-first">
                <a href="javascript:void(0)"
                  ><span>[特惠]</span>商城爆品1分秒杀
                </a>
              </li>
              <li class="title-first">
                <a target="_blank" href="javascript:void(0)"
                  ><span>[公告]</span>商城与长春市签署战略合作协议
                </a>
              </li>
              <li>
                <a target="_blank" href="javascript:void(0)"
                  ><span>[特惠]</span>洋河年末大促，低至两件五折</a
                >
              </li>
              <li>
                <a target="_blank" href="javascript:void(0)"
                  ><span>[公告]</span>华北、华中部分地区配送延迟</a
                >
              </li>
              <li>
                <a target="_blank" href="javascript:void(0)"
                  ><span>[特惠]</span>家电狂欢千亿礼券 买1送1！</a
                >
              </li>
            </ul>
            <div class="advTip">
              <img src="/images/advTip.jpg" />
            </div>
          </div>
        </div>
</template>

<script>
import { mapState } from "vuex";
export default {
  name: 'RMenu',
  computed:{
    ...mapState(["token"]),
  }
}
</script>

<style lang="less" scoped>

</style>
