<template>
  <div class="app-container" style="text-align: center; margin: auto">
    <el-upload
      class="upload-demo"
      drag
      action="https://jsonplaceholder.typicode.com/posts/"
      :on-success="handleSuccess"
      :on-error="handleError"
    >
      <i class="el-icon-upload"></i>
      <div class="el-upload__text">将文件拖到此处，或<em>点击上传</em></div>
    </el-upload>
  </div>
</template>

<script>
export default {
  data() {
    return {
      form: {
        name: '',
        region: '',
        date1: '',
        date2: '',
        delivery: false,
        type: [],
        resource: '',
        desc: ''
      }
    }
  },
  methods: {
    onSubmit() {
      this.$message('submit!')
    },
    onCancel() {
      this.$message({
        message: 'cancel!',
        type: 'warning'
      })
    },
    handleSuccess(response, file, fileList) {
      // 这里可以进行一些上传成功后的操作，比如显示提示信息
      alert('视频上传成功')
    },
    handleError(response, file, fileList) {
      alert('视频上传失败')
    }
  }
}
</script>

<style scoped>
.line{
  text-align: center;
}
</style>

