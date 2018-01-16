# Vue-source-analysis

## 逐行分析Vue源代码

### 其实用Vue-cli所构建的工具，它会把Vue源码的功能分类成一个src文件夹中，方便读者阅读

### 文件目录
``` bash
├─compiler  
│   └─codegen
│      ├─events.js
│      └─index.js
│   └─directives
│      ├─bind.js
│      ├─index.js
│      └─model.js
│   └─parser
│      ├─entity-decoder.js
│      ├─filter-parser.js
│      ├─html-parser.js
│      ├─index.js
│      └─text-parser.js
│   ├─error-detector.js
│   ├─helpers.js
│   ├─index.js
│   └─optimizer.js
├─core
│   └─components
│      ├─index.js
│      └─keep-alive.js
│   └─global-api
│      ├─assets.js
│      ├─extend.js
│      ├─index.js
│      ├─mixin.js
│      └─use.js
│   └─instance
│      └─render-helpers
│         ├─bind-object-props.js
│         ├─check-keycodes.js
│         ├─render-list.js
│         ├─render-slot.js
│         ├─render-static.js
│         ├─resolve-filter.js
│         └─resolve-slots.js
│      ├─events.js
│      ├─index.js
│      ├─init.js
│      ├─inject.js
│      ├─lifecycle.js
│      ├─proxy.js
│      ├─render.js
│      └─state.js
│   └─observer
│      ├─array.js
│      ├─dep.js
│      ├─index.js
│      ├─scheduler.js
│      └─watcher.js
│   └─util
│      ├─debug.js
│      ├─env.js
│      ├─error.js
│      ├─index.js
│      ├─lang.js
│      ├─options.js
│      ├─perf.js
│      └─props.js
│   └─vdom
│      └─helpers
│         ├─extract-props.js
│         ├─get-first-component-child.js
│         ├─index.js
│         ├─merge-hook.js
│         ├─normalize-children.js
│         ├─resolve-async-component.js
│         └─update-listeners.js
│      └─modules
│         ├─directives.js
│         ├─index.js
│         └─ref.js
│      ├─create-component.js
│      ├─create-element.js
│      ├─create-functional-component.js
│      ├─patch.js
│      └─vnode.js
│   ├─config.js
│   └─index.js
├─platforms
│   └─web
│      └─compiler
│         └─directives
│            ├─html.js
│            ├─index.js
│            ├─model.js
│            └─text.js
│         └─modules
│            ├─class.js
│            ├─index.js
│            └─style.js
│         ├─index.js
│         └─util.js
│      └─runtime
│         └─components
│            ├─index.js
│            ├─transition.js
│            └─transition-group.js
│         └─directives
│            ├─index.js
│            ├─model.js
│            └─show.js
│         └─modules
│            ├─attrs.js
│            ├─class.js
│            ├─dom-props.js
│            ├─events.js
│            ├─index.js
│            ├─style.js
│            └─transition.js
│         ├─class-util.js
│         ├─index.js
│         ├─node-ops.js
│         ├─patch.js
│         └─transition-util.js
│      └─server
│         └─directives
│            ├─index.js
│            └─show.js
│         └─modules
│            ├─attrs.js
│            ├─class.js
│            ├─dom-props.js
│            ├─index.js
│            └─style.js
│         └─util.js
│      └─util
│         ├─attrs.js
│         ├─class.js
│         ├─compat.js
│         ├─element.js
│         ├─index.js
│         └─style.js
│      ├─compiler.js
│      ├─runtime.js
│      ├─runtime-with-compiler.js
│      └─server-renderer.js
│   └─weex
│      └─compiler
│         └─directives
│            ├─index.js
│            └─model.js
│         └─modules
│            ├─append.js
│            ├─class.js
│            ├─index.js
│            ├─props.js
│            └─style.js
│         └─index.js
│      └─runtime
│         └─components
│            ├─index.js
│            ├─transition.js
│            └─transition-group.js
│         └─directives
│            ├─index.js
│         └─modules
│            ├─attrs.js
│            ├─class.js
│            ├─events.js
│            ├─index.js
│            ├─style.js
│            └─transition.js
│         ├─index.js
│         ├─node-ops.js
│         ├─patch.js
│         └─text-node.js
│      └─util
│         ├─index.js
│      ├─compiler.js
│      ├─framework.js
│      └─runtime-factory.js
├─server
│   └─bundle-renderer
│      ├─create-bundle-renderer.js
│      ├─create-bundle-runner.js
│      └─source-map-support.js
│   └─template-renderer
│      ├─create-async-file-mapper.js
│      ├─index.js
│      ├─parse-template.js
│      └─template-stream.js
│   └─webpack-plugin
│      ├─client.js
│      ├─server.js
│      └─util.js
│   ├─create-renderer.js
│   ├─render.js
│   ├─render-context.js
│   ├─render-stream.js
│   ├─util.js
│   └─write.js
├─sfc
│   └─parser.js
└─shared
    ├─constants.js
    └─util.js
```