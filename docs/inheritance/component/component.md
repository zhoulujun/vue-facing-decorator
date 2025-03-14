## Usage

Use decorator `ComponentBase` to define a super component. It's parameter is same to decorator `Component`'s.

Components which `vue-facing-decorator` generated can inherit another directly.

Consider code:

[](./code-example.ts ':include :type=code typescript')

There are two components: `MyComponent` and `SuperComponent`. The inheritance is implemented by vue `extends`.

## For vue native components

Use `mixins` to merge vue native components.

Consider code:

[](./code-native.ts ':include :type=code typescript')

`VueNativeComponent` is component defined by vue option api and mixin into `MyComponent`. The type information of VueNativeComponent is lost. So we need to build a context with types `VueNativeComponentContext`.

> The strategy of `mixins` and `extends` is according to [vue implementation](https://vuejs.org/api/options-composition.html#extends).