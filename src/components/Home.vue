<template>
	<div id="right-content">
		<header>
			<div class="block">
				<span class="demonstration">默认</span>
				<el-date-picker
					v-model="value1"
					type="date"
					placeholder="选择日期"
					:picker-options="pickerOptions0">
				</el-date-picker>
			</div>
		</header>
	</div>
</template>

<style>
	#right-content {
		width: 100%;
		height: 300px;
		background: cyan;
	}
</style>

<script>
export default {
  data () {
    return {
      pickerOptions0: {
        disabledDate (time) {
          return time.getTime() < Date.now() - 8.64e7
        }
      },
      value1: ''
    }
  }
}
</script>