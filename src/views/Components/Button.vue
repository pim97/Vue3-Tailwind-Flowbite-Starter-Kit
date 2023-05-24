<template>
    <button :type="props.type" :class="computedClasses">
      <slot></slot>
    </button>
  </template>
  
  <script setup>
  import { ref, computed, defineProps } from 'vue';
  
  const props = defineProps({
    type: {
      type: String,
      default: 'button',
    },
    color: {
      type: String,
      default: 'blue',
    },
    gradientColors: {
      type: Array,
      default: () => [],
    },
    variant: {
      type: String,
      default: 'default',
    },
    rounded: {
      type: Boolean,
      default: false,
    },
    gradient: {
      type: Boolean,
      default: false,
    },
    shadow: {
      type: Boolean,
      default: false,
    },
    size: {
      type: String,
      default: 'base',
      validator: (value) => ['xs', 'sm', 'base', 'lg', 'xl'].includes(value),
    },
  });
  
  const computedClasses = computed(() => {
    const classes = [
      'text-white',
      getBackgroundColor(),
      getHoverBackgroundColor(),
      'focus:outline-none',
      'focus:ring-4',
      getFocusRingColor(),
      getFontStyle(),
      getRoundedStyle(),
      getTextSize(),
      'text-center',
      ...getExtraClasses(),
    ];
  
    return classes.join(' ');
  });
  
  const getBackgroundColor = () => {
    if (props.gradient && props.gradientColors.length >= 2) {
      const [startColor, endColor] = props.gradientColors;
      return `bg-gradient-to-br from-${startColor} to-${endColor}`;
    } else {
      return `bg-${props.color}-700`;
    }
  };
  
  const getHoverBackgroundColor = () => {
    if (props.gradient && props.gradientColors.length >= 2) {
      const [startColor, endColor] = props.gradientColors;
      return `hover:bg-gradient-to-br group-hover:from-${startColor} group-hover:to-${endColor}`;
    } else {
      return `hover:bg-${props.color}-800`;
    }
  };
  
  const getFocusRingColor = () => {
    if (props.gradient && props.gradientColors.length >= 2) {
      const [startColor, endColor] = props.gradientColors;
      return `focus:ring-${startColor}-300 dark:focus:ring-${endColor}-800`;
    } else {
      return `focus:ring-${props.color}-300`;
    }
  };
  
  const getFontStyle = () => {
    return props.variant === 'default' ? 'font-medium' : '';
  };
  
  const getRoundedStyle = () => {
    return props.rounded ? 'rounded-full' : 'rounded-lg';
  };
  
  const getTextSize = () => {
    const sizeMap = {
      xs: 'px-3 py-2 text-xs',
      sm: 'px-3 py-2 text-sm',
      base: 'px-5 py-2.5 text-sm',
      lg: 'px-5 py-3 text-base',
      xl: 'px-6 py-3.5 text-base',
    };
  
    return sizeMap[props.size];
  };
  
  const getExtraClasses = () => {
    const classes = [];
    if (props.shadow) {
      classes.push('shadow-lg');
      classes.push(`shadow-${props.color}-500/50`);
      classes.push('dark:shadow-lg');
      classes.push(`dark:shadow-${props.color}-800/80`);
    }
    return classes;
  };
  </script>
  