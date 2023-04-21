<script>
export default {
    data() {
        return {
            data() {
                return {
                    loading:false,
                }
            },
            fApi: {},
            value: { field1: '111', field2: '21111111122', time: '11:11:11' },
            options: {
                onSubmit: (formData) => {
                    alert(JSON.stringify(formData))
                },
                info: {
                    //提示消息类型,popover,tooltip
                    type: "popover"
                },
                submitBtn: {
                    //类型 primary / success / warning / danger / info / text
                    type: "primary",
                    //尺寸 medium / small / mini
                    size: "medium",
                    //是否朴素按钮
                    plain: false,
                    //是否圆角按钮
                    round: false,
                    //是否圆形按钮
                    circle: false,
                    //是否加载中状态
                    loading: false,
                    //是否禁用状态
                    disabled: false,
                    //图标类名
                    icon: 'el-icon-upload',
                    //按钮宽度
                    width: '125px',
                    //是否默认聚焦
                    autofocus: false,
                    //原生 type 属性
                    nativeType: "button",
                    //按钮内容
                    innerText: "试试试试",
                    //按钮是否显示
                    show: true,
                    //按钮布局规则
                    col: undefined,
                    //按钮点击事件
                    click: undefined,
                }
            },
            rule: [
                { type: 'input', field: 'field1', title: 'field1', value: 'aaa' },
                { type: 'input', field: 'field2', title: 'field2', value: 'sss' },
                { type: 'timePicker', field: 'time', title: 'time', value: '12:12:12' },
                {
                    type: 'ElButton',
                    title: 'Modify field1',
                    native: false,
                    on: {
                        click: () => {
                           
                        }
                    },
                    children: ['Click'],
                },
            ]
        }
    }
}
</script>

<template>
    <div>
        <form-create :rule="rule" v-model="fApi" :option="options" :value.sync="value" />
    </div>
</template>
<style ></style>