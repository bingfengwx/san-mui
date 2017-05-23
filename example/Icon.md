## 图标

材料图标使用几何形状来直观地表达核心思想、特性或主题。

**产品图标** 是一个品牌的产品、服务和工具的视觉表现。

**系统图标** 代表一个命令、文件、设备、目录或一般性操作。

```san 所有的 Icon
<template>
<section class="icon-demo">
    <div class="icon" san-for="icon in icons">
        <san-icon size="32">{{icon}}</san-icon>
        <p>{{icon}}</p>
    </div>
</section>
</template>
<script>
import icons from 'html!../src/common/font/codepoints';
import Icon from '../src/Icon';

import '../src/Icon/Icon.styl'

export default {
    components: {
        'san-icon': Icon
    },
    initData() {
        return {
            icons: icons
                .split('\n')
                .map(line => line.split(' ')[0])
        };
    }
};
</script>
<style media="screen">
.icon-demo {
    display: flex;
    flex-flow: row wrap;
    justify-content: space-between;
    align-items: center;
}

.icon-demo .icon {
    flex: 0 0 25%;
    display: flex;
    flex-flow: column;
    height: 81px;
    align-items: center;
    justify-content: center;
}

.icon-demo .icon p {
    margin-top: 5px;
    font-size: 12px
}

</style>
```