<style scoped>
    .index {
        width: 100%;
        position: absolute;
        top: 0;
        bottom: 0;
        left: 0;
        text-align: center;
    }

    .index h1 {
        height: 150px;
    }

    .index h1 img {
        height: 100%;
    }

    .index h2 {
        color: #666;
        margin-bottom: 200px;
    }

    .index h2 p {
        margin: 0 0 50px;
    }

    .index .ivu-row-flex {
        height: 100%;
    }
</style>
<template>
    <div class="index">
        <v-menu></v-menu>
        
        <Row type="flex" justify="center" align="middle">
            <Col span="24">
                <h1>
                    <img src="https://raw.githubusercontent.com/iview/iview/master/assets/logo.png">
                </h1>
                <h2>
                    <p>Welcome to your iView app!</p>
                    <Modal v-model="visible" title="Welcome">欢迎使用 iView</Modal>
                    <Button type="ghost" @click="handleStart">Start iView</Button>
                    <Button type="ghost" @click="hello">hello</Button>
                </h2>
            </Col>
        </Row>
    </div>
</template>
<script>
    import menu from "./menu.vue";
    export default {
        components: {
            'v-menu': menu
        },
        data:  function(){
            return {
                visible: false
            }
        },
        methods: {
            handleStart() {
                this.$Modal.info({
                    title: 'Bravo',
                    content: 'Now, enjoy the convenience of iView.'
                });
            },
            hello(){
                this.visible = true
            }
        }
    };
</script>