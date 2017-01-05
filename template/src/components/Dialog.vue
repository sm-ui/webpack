<template>
<div class="dialog-panel-demo">
    <inline-dialog ref="dialog">
        <div slot="title">表头</div>
        <div slot="content">
            <form-panel></form-panel>
        </div>
        <div slot="footer">
            <button>确定</button>
        </div>
    </inline-dialog>

    <button @click="showDialog">显示弹窗</button>
</div>
</template>
<script type="text/javascript">
import Dialog from 'smui/Dialog'
import InlineDialog from 'smui/Message/InlineDialog'
import FormPanel from './Form.vue'

export default {
    methods: {
        showDialog() {
            this.$refs.dialog.showModal({
                width: 600,
                height: 350
            })
        }
    },
    components: {InlineDialog, FormPanel}
}
</script>

<style type="text/css" lang="less">
.dialog-panel-demo {
    width: 500px;
    height: 500px;
}
</style>
