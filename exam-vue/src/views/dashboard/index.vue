<template>
  <div class="app-container">
    <el-row :gutter="20">
      <el-col :span="16">
        <el-card class="box">
          <div slot="header" class="clearfix">
            <span>最新通知</span>
            <!-- <el-button style="float: right; padding: 3px 0; font-size: 12px" type="text">系统版本：{{ version }}</el-button> -->
          </div>

          <div style="line-height: 32px;">

            <div class="title" style="padding-top: 0px">2024年6月青少年等级考试安排</div>
            <!-- 考试系统是一款基于SpringBoot+Vue开发的考试系统。包含在线考试、用户体系、错题训练、考试规则、智能算分等考试功能，流程通畅。 -->

            <!-- <div class="title">技术栈</div>
            <div class="tags">
              <el-tag>SpringBoot</el-tag>
              <el-tag>Shiro</el-tag>
              <el-tag>MyBatis Plus</el-tag>
              <el-tag>Redis</el-tag>
              <el-tag>JWT</el-tag>
              <el-tag>Vue</el-tag>
              <el-tag>Vue2</el-tag>
              <el-tag>ElementUI</el-tag>
            </div> -->

            <div class="title">考试方式</div>
            <div>
              <div>1. 在线居家考试（全国）；</div>
              <div>2. 对于符合线下考试要求的考试服务网点，经地方实地调研报学会总部批准后，可组织线下考试。</div>
            </div>

            <div class="title">报名时间</div>
            <div>
              <p>报名网址：www.qceit.org.cn<br/>
                报名时间：2024年4月11日-6月12日16:00；<br/>
                考生注册、登录后填报信息并完成缴费视为报名成功；<br/>
                注意事项： <br/>
                1.报名结束前，考生因个人原因可申请退考，全额退费。<br/>
                2.报名结束后，因已启动考务组织程序、安排考试资源，不予退费。<br/>
                3.未参加考试的，视为缺考，不予退费。
              </p>
            </div>

            <div class="title">准考证下载</div>
            <div>
              <p>6月18日-考前1天<br/>
              </p>
            </div>

            <div class="title">考前集中测试</div>
            <div>
              <p>6月20日19:00-21:00 软件编程（C语言）软件编程（Python）软件编程（图形化）<br/>
                 6月27日19:00-21:00 无人机技术 三维创意设计 机器人技术<br/>
              </p>
            </div>

          </div>

        </el-card>
      </el-col>
      <el-col :span="8">

        <el-card class="box">
          <div slot="header" class="clearfix">
            <span>支持信息</span>
          </div>

          <div>

            <div class="title" style="padding-top: 0px">商业咨询</div>
            <div style="display: flex;">
              <div style="flex-grow: 1;">
                <div>微信号搜索手机13039111952</div>
                <!-- <div>手机：<a href="tel:18603038204">18603038204（郭女士）</a></div> -->
                <div>邮箱：<a href="mailto:13039111952@163.com">13039111952@163.com</a> </div>
              </div>
              <div style="width: 120px; display: flex; align-items: center; flex-direction: column; align-content: flex-end">
                <img style="width: 100px; height: 100px" src="@/assets/contact.png" >
                <div style="font-size: 12px; text-align: center; width: 100%">微信扫码加我好友</div>
              </div>

            </div>

            <!-- <div class="title">支持网站</div>
            <div>
              <div>企业官网：<a href="https://www.yfhl.net" target="_blank">https://www.yfhl.net</a></div>
              <div>在线试用：<a href="https://exam.yfhl.net" target="_blank">https://exam.yfhl.net</a></div>
            </div>

            <div class="title">在线试用</div>
            <div style="display: flex; align-items: center">
              <img src="@/assets/h5.png" style="width: 150px; height: 150px; border: #efefef 1px solid">
              <img src="@/assets/mp.jpg" style="width: 150px; height: 150px; border: #efefef 1px solid; margin-left: 20px">
            </div> -->

          </div>

        </el-card>

      </el-col>
    </el-row>
  </div>
</template>

<script>
import { mapGetters } from 'vuex'
import config from '../../../package.json'

export default {
  name: 'Dashboard',
  data() {
    return {
      currentRole: 'adminDashboard',
      version: config.version
    }
  },
  computed: {
    ...mapGetters([
      'roles',
      'siteData'
    ])
  },
  created() {

  }
}
</script>

<style scoped>
.box{
  height: calc(100vh - 120px);
  font-size: 14px;
  line-height: 28px;
  overflow-y: auto;
}
.title{
  font-size: 18px;
  font-weight: 700;
  padding-bottom: 10px;
  padding-top: 20px;
  margin-bottom: 10px;
  border-bottom: #eee 1px dotted;
}

.tags span{
  margin-right: 10px;
}

.box a{
  color: #20a0ff;
}

.box a:hover{
  color: #ff0000;
}
</style>
