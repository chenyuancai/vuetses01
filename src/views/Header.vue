<template>
    <div class="home">
    <div class="head">
        <div class="head_h1">
            <div class="h1_img">
                <img src="https://cdn.schoolpal.cn/schoolpal/resource/ci/SchoolPal-NETCore-PC/130/common/images/icon-loginlogo-new.jpg?version=20201022223932" class="">
            </div>
            <div class="h1_menu">
                <div class="h1_menu_m2">
                    <div class="h1_menu_m2_t">
                        申请使用
                    </div>
                    <div class="h1_menu_m_d"></div>
                    
                </div>

                <div class="h1_menu_m2">
                    <div class="h1_menu_m2_t">
                        官网
                    </div>
                    <div class="h1_menu_m_d"></div>
                </div>
                <div class="h1_menu_m2">
                    <div class="h1_menu_m2_t">
                        周边
                    </div>
                    <div class="h1_menu_m_d"></div>
                </div>
                <div class="h1_menu_m2">
                    <div class="h1_menu_m2_t">
                        帮助
                    </div>
                    <div class="h1_menu_m_d"></div>
                </div>
                <div class="h1_menu_m2">
                    <div class="h1_menu_m2_t">
                        公众号
                    </div>
                    <div class="h1_menu_m_d"></div>
                </div>
            </div>
        </div>
    </div>
  </div>
</template>
<style>
.head{
    height: 60px;
    background-color: #ffffff;
    
}
.head_h1{
    width: 1000px;
    margin:  0 auto ;
    display: flex;
    justify-content: space-between;

}
.h1_menu{
    height: 60px;
    display: flex;
    justify-content: center;
    align-items: center;
}
.h1_img{
    position: relative;
    height: 60px;
    background-repeat: no-repeat;

}

.h1_menu .h1_menu_m2{
    position: relative;
    padding-right: 40px;
    font-size: 16px;
    padding: 19px 19px 19px 19px;    
}

.h1_menu .h1_menu_m_d{
    width: 40px;
    height: 4px;
    border-bottom: #007aff 4px solid;
    position: absolute;
    left: 50%;
    transform: translateX(-50%);
    top: 50px;
    /* top: 50px;
    left: 30px; */
    display: none;
}
.h1_menu div:hover{
    cursor: pointer;
    color: #007aff;
}
.h1_menu div:hover+.h1_menu_m_d{
    display: block;
}
</style>