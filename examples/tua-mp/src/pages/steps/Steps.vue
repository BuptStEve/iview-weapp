<config>
{
    "navigationBarTitleText": "Steps 步骤条",
    "usingComponents": {
        "i-step": "/iview/step/index",
        "i-steps": "/iview/steps/index",
        "i-button": "/iview/button/index"
    }
}
</config>

<template lang="wxml">
    <view class="i-steps-demo">
        <view class="one-tag">基本用法</view>
        <i-steps>
            <i-step status="finish">
                <view slot="title">
                      已完成
                </view>
                <view slot="content">
                    这里是该步骤的描述信息
                </view>
            </i-step>
            <i-step status="process">
                <view slot="title">
                    进行中
                </view>
                <view slot="content">
                    这里是该步骤的描述信息
                </view>
            </i-step>
            <i-step status="">
                <view slot="title">
                    错误
                </view>
                <view slot="content">
                    这里是该步骤的描述信息
                </view>
            </i-step>
        </i-steps>

         <view class="one-tag">使用 icon 图标</view>
        <i-steps>
            <i-step status="finish" icon="barrage">
                <view slot="title">
                      已完成
                </view>
                <view slot="content">
                    这里是该步骤的描述信息
                </view>
            </i-step>
            <i-step status="process" icon="brush">
                <view slot="title">
                    进行中
                </view>
                <view slot="content" icon="camera">
                    这里是该步骤的描述信息
                </view>
            </i-step>
            <i-step  icon="collection">
                <view slot="title">
                    错误
                </view>
                <view slot="content">
                    这里是该步骤的描述信息
                </view>
            </i-step>
        </i-steps>

        <view class="one-tag">步骤进度</view>
        <i-steps current="{{current}}">
            <i-step>
                <view slot="title">
                      已完成
                </view>
                <view slot="content">
                    这里是该步骤的描述信息
                </view>
            </i-step>
            <i-step>
                <view slot="title">
                    进行中
                </view>
                <view slot="content">
                    这里是该步骤的描述信息
                </view>
            </i-step>
            <i-step>
                <view slot="title">
                    错误
                </view>
                <view slot="content">
                    这里是该步骤的描述信息
                </view>
            </i-step>
        </i-steps>
        <i-button bindclick="handleClick">下一步</i-button>

        <view class="one-tag">垂直方向</view>
        <i-steps current="{{verticalCurrent}}" direction="vertical">
            <i-step>
                <view slot="title">
                      已完成
                </view>
                <view slot="content">
                    这里是该步骤的描述信息
                </view>
            </i-step>
            <i-step>
                <view slot="title">
                    进行中
                </view>
                <view slot="content">
                    这里是该步骤的描述信息
                </view>
            </i-step>
            <i-step>
                <view slot="title">
                    错误
                </view>
                <view slot="content">
                    这里是该步骤的描述信息
                </view>
            </i-step>
        </i-steps>
    </view>
</template>

<script>
export default {
    data () {
        return {
            current: 2,
            verticalCurrent: 2,
        }
    },
    methods: {
        handleClick () {
            const addCurrent = this.current + 1
            const current = addCurrent > 2 ? 0 : addCurrent

            this.current = current
        },
    },
}
</script>

<style lang="scss">

.i-steps-demo {
    margin: 20px;
}
.one-tag {
    font-size: 14px;
    margin: 30px 5px 20px 0;
}

</style>
