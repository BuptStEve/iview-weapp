<config>
{
    "navigationBarTitleText": "Input 输入框",
    "usingComponents": {
        "i-input": "/iview/input/index",
        "i-panel": "/iview/panel/index",
        "i-button": "/iview/button/index"
    }
}
</config>

<template lang="wxml">
    <i-panel title="基础用法">
        <i-input value="{{ value1 }}" title="收货人" autofocus placeholder="名字" />
        <i-input value="{{ value2 }}" type="number" title="联系电话" placeholder="请输入手机号" />
        <i-input value="{{ value3 }}" type="textarea" title="详细地址" placeholder="请输入详细地址(最多50字)" maxlength="50" />
        <i-input value="{{ value4 }}" title="用户信息" disabled />
    </i-panel>

    <i-panel title="无标题输入框">
        <i-input value="{{ value5 }}" placeholder="请输入收货人姓名" />
    </i-panel>

    <i-panel title="圆角输入框">
        <i-input value="{{ value6 }}" type="number" right title="消费总额" mode="wrapped" placeholder="询问收银员后输入" />
        <i-input value="{{ value7 }}" type="number" right error title="不参与优惠金额" mode="wrapped" placeholder="询问收银员后输入" />
    </i-panel>
</template>

<script>
export default {
    data () {
        return {
            value1: '',
            value2: '',
            value3: '',
            value4: '输入框已禁用',
            value5: '',
            value6: '',
            value7: '',
        }
    },
    methods: {
    },
}
</script>

<style lang="css">


</style>
