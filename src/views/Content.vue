<template>
  <div class="body">
    <div class="content">
      <div class="content_c1">
        <div class="c1_img">
          <img
            src="https://schoolpal.oss-cn-hangzhou.aliyuncs.com/erpbanner/erplogin0827.jpg"
          />
        </div>
        <div class="c1_form">
          <div class="form" id="form">
            <div class="c1_from_m">
              <div class="c1_rigth_a">
                <div class="c1_rigth_hh">
                  <div @click="acomes()" class="hh">手机号码登录</div>
                  <div @click="agos()" class="hhh">账号登录</div>
                </div>
                <div class="c1_rigth_b">
                  <div class="c1_form_rud" ref="ph1" v-if="ph1"></div>
                  <div class="c1_form_rud1" ref="ph2" v-if="ph2"></div>
                </div>

                <!-- 手机号码登录 -->
                <div class="c1_form_kuang" ref="pp1" v-if="pp1">
                  <div class="c1_form_phone">
                    <!-- <img src="#" class=""> -->
                    <input
                      class="ha"
                      type="text"
                      name="name"
                      v-model="phoneNum"
                      @blur="blurp1"
                      ref="phoneNum"
                      placeholder="请输入手机号码"
                    />
                  </div>
                  <div :class="{ hh1: !tag, aa33: tag }"></div>
                  <div class="msg" ref="p1" v-if="p1">请输入手机号</div>
                  <div class="msgg" ref="p11" v-if="p11">
                    请输入正确的手机号
                  </div>
                  <div class="c1_form_psw">
                    <!-- <img src="#" class=""> -->
                    <input
                      id="input"
                      class="hb"
                      name="password"
                      type="password"
                      @blur="blurp2"
                      v-model="phonePsw"
                      ref="phonepsw"
                      placeholder="请输入密码"
                    />
                  </div>
                  <div :class="{ hh2: !tag1, aa33: tag1 }"></div>
                  <div class="msg1" ref="p2" v-if="p2">请输入密码</div>
                </div>
                <div
                  class="c1_right_b"
                  @click="submit"
                  ref="p3"
                  v-if="p3"
                ></div>

                <!-- 账号登录 -->
                <div class="c1_from_user" ref="pp2" v-if="pp2">
                  <div class="c1_from_user_kuang">
                    <!-- <img src="#" class=""> -->
                    <input
                      class="user_uaname"
                      type="text"
                      @blur="blurp3"
                      name=""
                      v-model="useraftername"
                      ref="userafterName"
                      placeholder="请输入机构后缀"
                    />
                  </div>
                  <div :class="{ aa1: !tag2, aa33: tag2 }"></div>
                  <div class="msg2" ref="ppp1" v-if="ppp1">请输入机构后缀</div>
                  <div class="c1_from_user_ukuang">
                    <!-- <img src="#" class=""> -->
                    <input
                      class="user_uname"
                      type="text"
                      name=""
                      @blur="blurp4"
                      v-model="username"
                      ref="userName"
                      placeholder="请输入登录名"
                    />
                  </div>
                  <div :class="{ aa2: !tag3, aa33: tag3 }"></div>
                  <div class="msg3" ref="ppp1" v-if="ppp2">请输入登录名</div>
                  <div class="c1_from_user_pkuang">
                    <!-- <img src="#" class=""> -->
                    <input
                      class="user_upsw"
                      type="password"
                      name=""
                      @blur="blurp5"
                      v-model="userpsw"
                      ref="userPsw"
                      placeholder="请输入密码"
                    />
                  </div>
                  <div :class="{ aa3: !tag4, aa33: tag4 }"></div>
                  <div class="msg4" ref="ppp1" v-if="ppp3">请输入密码</div>
                </div>
                <div class="c1_right_bn" @click="ago" ref="pp3" v-if="pp3">
                  <div class="c1_form_btn1"><span>登录</span></div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>

    <div class="footer">
      <div class="footer_text">相关产品</div>
      <div class="footer_bao">
        <div class="footer_bao_one">
          <img src="https://prox.schoolpal.cn/common/images/icon-scp.png" />
          <div class="footer_bao_one_t">
            <div class="footer_bao_one_t1">校宝收银宝</div>
            <div class="footer_bao_one_t2">学校收费标配</div>
          </div>
        </div>
        <div class="footer_bao_two">
          <img
            src="https://prox.schoolpal.cn/common/images/icon-zhaoshengbao.png"
          />
          <div class="footer_bao_two_t">
            <div class="footer_bao_two_t1">校宝招生宝</div>
            <div class="footer_bao_two_t2">一站招生服务</div>
          </div>
        </div>
        <div class="footer_bao_three">
          <img
            src="https://prox.schoolpal.cn/common/images/icon-anxinbao.png"
          />
          <div class="footer_bao_three_t">
            <div class="footer_bao_three_t1">校宝安心宝</div>
            <div class="footer_bao_three_t2">教育保险精选</div>
          </div>
        </div>
      </div>
      <div class="footer_zixun">
        <div class="footer_zixun_t1">咨询热线</div>
        <div class="footer_zixun_t2">400-6999-707</div>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  name: "Home",
  component: {},
  data() {
    return {
      phoneNum: "",
      phonePsw: "",
      useraftername: "",
      username: "",
      userpsw: "",
      p1: false,
      p11: false,
      p2: false,
      p3: false,
      pp1: true,
      pp2: false,
      pp3: true,
      ph1: true,
      ph2: false,
      tag: false,
      tag1: false,
      tag2: false,
      tag3: false,
      tag4: false,
      tag5: false,
      ppp1: false,
      ppp2: false,
      ppp3: false,
    };
  },
  methods: {
    submit() {
      console.log(111);
      this.blurp1();
      this.blurp2();
      if (this.phoneNum == "" && this.phonePsw == "") {
        this.p1 = true;
        this.p11 = false;
        this.tag = true;
      } else if (this.phoneNum == "" && this.phonePsw !== "") {
      } else if (this.phoneNum !== "" && this.phonePsw == "") {
      } else if (this.phoneNum !== "" && this.phonePsw !== "") {
      }
    },
    ago() {
      if (this.pp2) {
        console.log(11111);
        this.blurp3();
        this.blurp4();
        this.blurp5();
      } else {
        this.blurp1();
        this.blurp2();
      }
    },
    agos() {
      this.pp2 = true;
      this.pp1 = false;
      this.ph1 = false;
      this.ph2 = true;
    },
    acomes() {
      this.pp2 = false;
      this.pp1 = true;
      this.ph1 = true;
      this.ph2 = false;
    },
    blurp1() {
      if (this.phoneNum == "") {
        console.log(this.p1);
        this.p1 = true;
        this.p11 = false;
        this.tag = true;
      } else if (
        this.phoneNum.length > 0 &&
        this.phoneNum.length < 12 &&
        !/^1[3|4|5|7|8]\d{9}$/.test(this.phoneNum)
      ) {
        this.p1 = false;
        this.p11 = true;
        this.tag = true;
        // alert(111)
      } else if (this.phoneNum.length == 11) {
        this.p1 = false;
        this.p11 = false;
        this.tag = false;
      } else {
        this.p11 = true;
        this.tag = true;
      }
      console.log("blur:" + this.phoneNum);
    },
    blurp2() {
      if (this.phonePsw == "") {
        this.p2 = true;
        this.tag1 = true;
      } else {
        this.p2 = false;
        this.tag1 = false;
      }
    },
    blurp3() {
      if (this.useraftername == "") {
        this.tag2 = true;
        this.ppp1 = true;
      } else {
        this.tag2 = false;
        this.ppp1 = false;
      }
    },
    blurp4() {
      if (this.username == "") {
        this.tag3 = true;
        this.ppp2 = true;
      } else {
        this.tag3 = false;
        this.ppp2 = false;
      }
    },
    blurp5() {
      if (this.userpsw == "") {
        this.tag4 = true;
        this.ppp3 = true;
      } else {
        this.tag4 = false;
        this.ppp3 = false;
      }
    },
  },
};
</script>
<style>
.content {
  background-color: #ffffff;
  width: 1000px;
  position: relative;
  margin: 0 auto;
  border-radius: 8px;
}
.content_c1 {
  position: relative;
  display: flex;
  width: 1000px;
  /* background-color: #ffffff; */
  margin-top: 120px;
  /* border-radius: 8px; */
}
.content_c1 .c1_img img {
  width: 560px;
  height: 560px;
  border-radius: 8px;
}

.form {
  margin-left: 28px;
  width: 400px;
  height: 450px;
}
.c1_form {
  margin-top: 70px;
}
.c1_form_m {
  flex: 1;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
}
.c1_form .c1_rigth_b {
  display: flex;
  justify-content: center;
}
.c1_form .c1_rigth_b .c1_form_rud {
  display: flex;
  flex: 0.5;
  justify-content: center;
  border-bottom: #007aff 5px solid;
  width: 32px;
  margin-top: 10px;
  position: absolute;
  margin-right: 200px;
}
.c1_form .c1_rigth_b .c1_form_rud1 {
  /* border: red 4px solid; */
  display: flex;
  justify-content: center;
  flex: 0.5;
  border-bottom: #007aff 5px solid;
  width: 32px;
  margin-top: 10px;
  position: absolute;
  margin-left: 200px;
}
.c1_form .c1_rigth_hh {
  /* border: black 1px solid; */
  display: flex;
  justify-content: center;
}
.c1_form .c1_rigth_hh .hh {
  /* border: black 1px solid; */
  display: flex;
  justify-content: center;
  flex: 0.5;
  text-decoration: none;
  color: black;
  font-size: 18px;
  font-weight: bold;

  /* text-align: center; */
}
.c1_form .c1_rigth_hh .hh:hover {
  cursor: pointer;
}
.c1_form .c1_rigth_hh .hhh {
  /* border: black 1px solid; */
  display: flex;
  justify-content: center;
  flex: 0.5;
  text-decoration: none;
  color: black;
  font-size: 18px;
  font-weight: bold;

  /* text-align: center; */
}
.c1_form .c1_rigth_hh .hhh:hover {
  cursor: pointer;
}

/* 手机号码登录 */
.c1_form_phone input {
  margin-top: 40px;
  position: relative;
  margin-left: 32px;
  width: 330px;
  padding: 10px;
  border-style: none;
  outline: none;
}
.hh1 {
  margin-top: 10px;
  border-bottom: 1px solid;
  background-color: grey;
}
.c1_form_phone:hover + .hh1 {
  border-bottom: #007aff 1px solid;
}
.c1_form_psw {
  margin-top: 50px;
}
.c1_form_psw input {
  margin-top: 40px;
  position: relative;
  margin-left: 32px;
  width: 330px;
  padding: 10px;
  border-style: none;
  outline: none;
}
.hh2 {
  margin-top: 10px;
  border-bottom: 1px solid;
  background-color: grey;
}
.c1_form_psw:hover + .hh2 {
  border-bottom: #007aff 1px solid;
}
.c1_right_b {
  margin-bottom: 30px;
  /* border: blue 1px solid; */
  position: relative;
  top: 140px;
}
.msg {
  position: relative;
  margin-left: 280px;
  font-size: 12px;
  color: #ff3366;
  /* display: none; */
}
.msgg {
  position: relative;
  margin-left: 280px;
  font-size: 12px;
  color: #ff3366;
  /* display: none; */
}
.msg1 {
  position: relative;
  margin-left: 280px;
  font-size: 12px;
  color: #ff3366;
  /* display: none; */
}
.msg2 {
  position: relative;
  margin-left: 280px;
  font-size: 12px;
  color: #ff3366;
  /* display: none; */
}
.msg3 {
  position: relative;
  margin-left: 280px;
  font-size: 12px;
  color: #ff3366;
  /* display: none; */
}
.msg4 {
  position: relative;
  margin-left: 280px;
  font-size: 12px;
  color: #ff3366;
  /* display: none; */
}

.c1_right_b {
  /* position: relative;*/
  margin-bottom: 30px;
}
.c1_form_btn {
  position: relative;
  width: 320px;
  height: 54px;
  background-color: #007aff;
  text-align: center;
  font-size: 16px;
  margin: 0 auto;
  color: honeydew;
  border: none;
  border-radius: 20px;
}
.c1_form_btn span {
  position: absolute;
  left: 50%;
  top: 50%;
  transform: translate(-50%, -50%);
}
.c1_form_btn:hover {
  cursor: pointer;
  background-color: #0064dc;
}

/* 账号登录 */
.c1_from_user_kuang input {
  margin-top: 40px;
  position: relative;
  margin-left: 32px;
  width: 330px;
  padding: 10px;
  border-style: none;
  outline: none;
}
.aa1 {
  margin-top: 10px;
  border-bottom: 1px solid;
  background-color: grey;
}
.c1_from_user_kuang:hover + .aa1 {
  border-bottom: #007aff 1px solid;
}
.c1_from_user_ukuang {
  margin-top: 10px;
}
.c1_from_user_ukuang input {
  margin-top: 40px;
  position: relative;
  margin-left: 32px;
  width: 330px;
  padding: 10px;
  border-style: none;
  outline: none;
}
.aa2 {
  margin-top: 10px;
  border-bottom: 1px solid;
  background-color: grey;
}
.c1_from_user_ukuang:hover + .aa2 {
  border-bottom: #007aff 1px solid;
}
.c1_from_user_pkuang {
  margin-top: 10px;
}
.c1_from_user_pkuang input {
  margin-top: 40px;
  position: relative;
  margin-left: 32px;
  width: 330px;
  padding: 10px;
  border-style: none;
  outline: none;
}
.aa3 {
  margin-top: 10px;
  border-bottom: 1px solid;
  background-color: grey;
}
.aa33 {
  border-bottom: #ff3366 1px solid;
}
.c1_from_user_pkuang:hover + .aa3 {
  border-bottom: #007aff 1px solid;
}

.c1_right_bn {
  position: absolute;
  display: flex;
  justify-content: center;
  margin-top: 60px;
  margin-left: 40px;
  /* margin-bottom: 30px;  */
}
.c1_form_btn1 {
  position: relative;
  width: 320px;
  height: 54px;
  background-color: #007aff;
  text-align: center;
  font-size: 16px;
  margin: 0 auto;
  color: honeydew;
  border: none;
  border-radius: 20px;
}
.c1_form_btn1 span {
  position: absolute;
  left: 50%;
  top: 50%;
  transform: translate(-50%, -50%);
}
.c1_form_btn1:hover {
  cursor: pointer;
  background-color: #0064dc;
}
.footer {
  width: 1000px;
  position: relative;
  margin: 0 auto;
  border-radius: 8px;
  margin-top: 10px;
}
.footer_text {
  font-weight: bold;
  font-size: 16px;
}
.footer_bao {
  position: relative;
  top: 30px;
  left: -65px;
  flex: 1;
  display: flex;
  flex-direction: row;
  /* justify-content: ; */
}
.footer_bao div {
  /* padding-right: px; */
  margin-right: 10px;
}
.footer_bao_one {
  border-radius: 8px;
  background-color: #d49c68;
  width: 210px;
  height: 60px;
}
.footer_bao_one img {
  width: 40px;
  height: 40px;
  margin-left: 20px;
  margin-top: 10px;
}
.footer_bao_one .footer_bao_one_t .footer_bao_one_t1 {
  font-weight: bold;
  font-size: 14px;
}
.footer_bao_one .footer_bao_one_t .footer_bao_one_t2 {
  font-size: 12px;
}
.footer_bao_one .footer_bao_one_t {
  position: relative;
  left: 70px;
  top: -40px;
}
.footer_bao_one:hover {
  cursor: pointer;
  background-color: #eaedf2;
  position: relative;
  top: -3px;
}
.footer_bao_two {
  border-radius: 8px;
  background-color: #d49c68;
  width: 210px;
  height: 60px;
}
.footer_bao_two img {
  width: 40px;
  height: 40px;
  margin-left: 20px;
  margin-top: 10px;
}
.footer_bao_two .footer_bao_two_t {
  position: relative;
  left: 70px;
  top: -40px;
}
.footer_bao_two .footer_bao_two_t .footer_bao_two_t1 {
  font-weight: bold;
  font-size: 14px;
}
.footer_bao_two .footer_bao_two_t .footer_bao_two_t2 {
  font-size: 12px;
}
.footer_bao_two:hover {
  cursor: pointer;
  background-color: #eaedf2;
  position: relative;
  top: -3px;
}
.footer_bao_three {
  border-radius: 8px;
  background-color: #d49c68;
  width: 210px;
  height: 60px;
}
.footer_bao_three img {
  width: 40px;
  height: 40px;
  margin-left: 20px;
  margin-top: 10px;
}
.footer_bao_three .footer_bao_three_t .footer_bao_three_t1 {
  font-weight: bold;
  font-size: 14px;
}
.footer_bao_three .footer_bao_three_t .footer_bao_three_t2 {
  font-size: 12px;
}
.footer_bao_three .footer_bao_three_t {
  position: relative;
  left: 70px;
  top: -40px;
}
.footer_bao_three:hover {
  cursor: pointer;
  background-color: #eaedf2;
  position: relative;
  top: -3px;
}

.footer {
  flex: 1;
  display: flex;
  flex-direction: row;
  justify-content: space-between;
}
.footer_zixun {
  position: relative;
  margin-top: 10px;
  margin-right: 10px;
}
.footer_zixun .footer_zixun_t1 {
  font-size: 16px;
  font-weight: bold;
}
.footer_zixun .footer_zixun_t2 {
  font-size: 28px;
  font-weight: bold;
  margin-top: 10px;
}
</style>