<template>
	<div class="card content-box">
		<span class="text"> èåæé ðððð</span>
		<el-alert
			:title="'æ¨¡æåå°æ ¹æ®ä¸åç¨æ·è§è²è¿åå¯¹åºè·¯ç±ï¼è§å¯å·¦ä¾§èåååï¼admin è´¦å·å¯æ¥çææèåãuser è´¦å·åªå¯æ¥çé¨åèåï¼'"
			type="success"
			:closable="false"
		/>
		<el-button class="mt20" type="primary" :icon="Promotion" @click="handleToLogin">ç»å½å¶ä»è´¦å·</el-button>
	</div>
</template>

<script setup lang="ts" name="authMenu">
import { useRouter } from "vue-router";
import { LOGIN_URL } from "@/config/config";
import { GlobalStore } from "@/stores";
import { Promotion } from "@element-plus/icons-vue";

const router = useRouter();
const globalStore = GlobalStore();

const handleToLogin = () => {
	globalStore.setToken("");
	router.push(LOGIN_URL);
};
</script>
