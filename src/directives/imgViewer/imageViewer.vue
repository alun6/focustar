<template>
  <el-image-viewer
    style="z-index: 2800;"
    v-if="showPreview"
    :urlList="previewImages"
    :on-close="closeViewer"
  ></el-image-viewer>
</template>
<script>
import ElImageViewer from "element-ui/packages/image/src/image-viewer";
export default {
  data() {
    return {
      showPreview: false,
      previewImages: []
    };
  },
  components: {
    ElImageViewer
  },
  methods: {
    closeViewer() {
      this.showPreview = false;
    }
  }
};
</script>
