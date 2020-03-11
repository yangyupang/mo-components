<template>
  <div>
    <button
      class="mo-btn"
      :class="[classType,{'circle':circle},{'round':round},{'plain':plain},{'disabled':disabled}]"
    >
      <i v-if="icon" class="iconfont" :class="[iconType]"></i>
      <i v-if="loading" class="iconfont icon-loading loading-status"></i>
      <slot v-if="$slots.title" name="title"></slot>
    </button>
  </div>
</template>

<script>
export default {
  props: {
    type: {
      type: String,
      default: ""
    },
    plain: {
      type: Boolean,
      default: false
    },
    round: {
      type: Boolean,
      default: false
    },
    icon: {
      type: String,
      default: ""
    },
    circle: {
      type: Boolean,
      default: false
    },
    disabled: {
      type: Boolean,
      default: false
    },
    loading: {
      type: Boolean,
      default: false
    }
  },
  data() {
    return {};
  },
  components: {},
  methods: {},
  mounted() {
    // console.log(this.$slots.title);
  },
  watch: {},
  computed: {
    classType() {
      return "mo-btn-" + this.type;
    },
    iconType() {
      return "icon-" + this.icon;
    }
  },
  filters: {}
};
</script>

<style scoped lang='scss'>
.mo-btn {
  padding: 12px 20px;
  font-size: 14px;
  border-radius: 4px;
  background: #fff;
  cursor: pointer;
  border: 1px solid #dcdfe6;
  color: #606266;
  line-height: 1;
  transition: 0.1s;
  background-color: transparent;
  outline: none;

  &:hover {
    color: #409eff;
    border-color: #c6e2ff;
    background-color: #ecf5ff;
  }
  &:focus {
    color: #409eff;
    border-color: #c6e2ff;
    background-color: #ecf5ff;
  }
  &.plain {
    &:hover {
      background: #fff;
      border-color: #409eff;
      color: #409eff;
    }
    &:focus {
      background: #fff;
      border-color: #409eff;
      color: #409eff;
    }
    &.disabled {
      background-color: #fff;
      border-color: #ebeef5;
      color: #c0c4cc;
      &:hover {
        background-color: #fff;
        border-color: #ebeef5;
        color: #c0c4cc;
      }
      &:focus {
        background-color: #fff;
        border-color: #ebeef5;
        color: #c0c4cc;
      }
    }
  }
  &.disabled {
    color: #c0c4cc;
    cursor: not-allowed;
    background-image: none;
    background-color: #fff;
    border-color: #ebeef5;
  }
  &-primary {
    color: #fff;
    background-color: #409eff;
    border-color: #409eff;
    &.plain {
      color: #409eff;
      background: #ecf5ff;
      border-color: #b3d8ff;
      &:hover {
        background: #66b1ff;
        border-color: #66b1ff;
        color: #fff;
      }
      &:focus {
        background: #66b1ff;
        border-color: #66b1ff;
        color: #fff;
      }
      &.disabled {
        color: #8cc5ff;
        background-color: #ecf5ff;
        border-color: #d9ecff;
        &:hover {
          color: #8cc5ff;
          background-color: #ecf5ff;
          border-color: #d9ecff;
        }
        &:focus {
          color: #8cc5ff;
          background-color: #ecf5ff;
          border-color: #d9ecff;
        }
      }
    }
    &.disabled {
      color: #fff;
      background-color: #a0cfff;
      border-color: #a0cfff;
      &:hover {
        color: #fff;
        background-color: #a0cfff;
        border-color: #a0cfff;
      }
      &:focus {
        color: #fff;
        background-color: #a0cfff;
        border-color: #a0cfff;
      }
    }
    &:hover {
      background: #66b1ff;
      border-color: #66b1ff;
      color: #fff;
    }
    &:focus {
      background: #66b1ff;
      border-color: #66b1ff;
      color: #fff;
    }
  }
  &-success {
    color: #fff;
    background-color: #67c23a;
    border-color: #67c23a;
    &.plain {
      color: #67c23a;
      background: #f0f9eb;
      border-color: #c2e7b0;
      &:hover {
        background: #67c23a;
        border-color: #67c23a;
        color: #fff;
      }
      &:focus {
        background: #67c23a;
        border-color: #67c23a;
        color: #fff;
      }
      &.disabled {
        color: #a4da89;
        background-color: #f0f9eb;
        border-color: #e1f3d8;
        &:hover {
          color: #a4da89;
          background-color: #f0f9eb;
          border-color: #e1f3d8;
        }
        &:focus {
          color: #a4da89;
          background-color: #f0f9eb;
          border-color: #e1f3d8;
        }
      }
    }
    &.disabled {
      color: #fff;
      background-color: #b3e19d;
      border-color: #b3e19d;
      &:hover {
        color: #fff;
        background-color: #b3e19d;
        border-color: #b3e19d;
      }
      &:focus {
        color: #fff;
        background-color: #b3e19d;
        border-color: #b3e19d;
      }
    }
    &:hover {
      background: #85ce61;
      border-color: #85ce61;
      color: #fff;
    }
    &:focus {
      background: #85ce61;
      border-color: #85ce61;
      color: #fff;
    }
  }
  &-info {
    color: #fff;
    background-color: #909399;
    border-color: #909399;
    &.plain {
      color: #909399;
      background: #f4f4f5;
      border-color: #d3d4d6;
      &:hover {
        background: #909399;
        border-color: #909399;
        color: #fff;
      }
      &:focus {
        background: #909399;
        border-color: #909399;
        color: #fff;
      }
      &.disabled {
        color: #bcbec2;
        background-color: #f4f4f5;
        border-color: #e9e9eb;
        &:hover {
          color: #bcbec2;
          background-color: #f4f4f5;
          border-color: #e9e9eb;
        }
        &:focus {
          color: #bcbec2;
          background-color: #f4f4f5;
          border-color: #e9e9eb;
        }
      }
    }
    &.disabled {
      color: #fff;
      background-color: #c8c9cc;
      border-color: #c8c9cc;
      &:hover {
        color: #fff;
        background-color: #c8c9cc;
        border-color: #c8c9cc;
      }
      &:focus {
        color: #fff;
        background-color: #c8c9cc;
        border-color: #c8c9cc;
      }
    }
    &:hover {
      background: #a6a9ad;
      border-color: #a6a9ad;
      color: #fff;
    }
    &:focus {
      background: #a6a9ad;
      border-color: #a6a9ad;
      color: #fff;
    }
  }
  &-warning {
    color: #fff;
    background-color: #e6a23c;
    border-color: #e6a23c;
    &.plain {
      color: #e6a23c;
      background: #fdf6ec;
      border-color: #f5dab1;
      &:hover {
        background: #e6a23c;
        border-color: #e6a23c;
        color: #fff;
      }
      &:focus {
        background: #e6a23c;
        border-color: #e6a23c;
        color: #fff;
      }
      &.disabled {
        color: #f0c78a;
        background-color: #fdf6ec;
        border-color: #faecd8;
        &:hover {
          color: #f0c78a;
          background-color: #fdf6ec;
          border-color: #faecd8;
        }
        &:focus {
          color: #f0c78a;
          background-color: #fdf6ec;
          border-color: #faecd8;
        }
      }
    }
    &.disabled {
      color: #fff;
      background-color: #f3d19e;
      border-color: #f3d19e;
      &:hover {
        color: #fff;
        background-color: #f3d19e;
        border-color: #f3d19e;
      }
      &:focus {
        color: #fff;
        background-color: #f3d19e;
        border-color: #f3d19e;
      }
    }
    &:hover {
      background: #ebb563;
      border-color: #ebb563;
      color: #fff;
    }
    &:focus {
      background: #ebb563;
      border-color: #ebb563;
      color: #fff;
    }
  }
  &-danger {
    color: #fff;
    background-color: #f56c6c;
    border-color: #f56c6c;
    &.plain {
      color: #f56c6c;
      background: #fef0f0;
      border-color: #fbc4c4;
      &:hover {
        background: #f56c6c;
        border-color: #f56c6c;
        color: #fff;
      }
      &:focus {
        background: #f56c6c;
        border-color: #f56c6c;
        color: #fff;
      }
      &.disabled {
        color: #f9a7a7;
        background-color: #fef0f0;
        border-color: #fde2e2;
        &:hover {
          color: #f9a7a7;
          background-color: #fef0f0;
          border-color: #fde2e2;
        }
        &:focus {
          color: #f9a7a7;
          background-color: #fef0f0;
          border-color: #fde2e2;
        }
      }
    }
    &.disabled {
      color: #fff;
      background-color: #fab6b6;
      border-color: #fab6b6;
      &:hover {
        color: #fff;
        background-color: #fab6b6;
        border-color: #fab6b6;
      }
      &:focus {
        color: #fff;
        background-color: #fab6b6;
        border-color: #fab6b6;
      }
    }
    &:hover {
      background: #f78989;
      border-color: #f78989;
      color: #fff;
    }
    &:focus {
      background: #f78989;
      border-color: #f78989;
      color: #fff;
    }
  }
}
.circle {
  height: 48px;
  width: 48px;
  border-radius: 50%;
  display: flex;
  align-items: center;
  justify-content: center;
}
.round {
  border-radius: 20px;
}
/*无限旋转动画*/
@keyframes rotating {
  0% {
    transform: rotate(0deg);
  }
  100% {
    transform: rotate(360deg);
  }
}
.loading-status {
  margin-right: 6px;
  display: inline-block;
  animation: rotating 2s linear 0.2s infinite;
}
</style>