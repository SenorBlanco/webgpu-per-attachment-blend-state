# Per-attachment blend state

## To "unship" per-attachment blend state:

1. To the [GPUFeatureName](https://www.w3.org/TR/webgpu/#gpufeaturename) enum, add:

>`"per-attachment-blend-state",`

2. Under the section [validating GPUFragmentState](https://www.w3.org/TR/webgpu/#abstract-opdef-validating-gpufragmentstate), add:

If ``"per-attachment-blend-state"`` is not enabled:

- colorState.[blend](https://www.w3.org/TR/webgpu/#dom-gpucolortargetstate-blend) must contain the same value for all indices in _descriptor_.[targets](https://www.w3.org/TR/webgpu/#dom-gpufragmentstate-targets)
- colorState.[writemask](https://www.w3.org/TR/webgpu/#dom-gpucolortargetstate-writemask) must contain the same value for all indices in _descriptor_.[targets](https://www.w3.org/TR/webgpu/#dom-gpufragmentstate-targets)

3. Under the section [Feature Index](https://www.w3.org/TR/webgpu/#feature-index), add a new section:

25.12. "per-attachment-blend-state"

In GPUFragmentState indices in _descriptor_.[targets](https://www.w3.org/TR/webgpu/#dom-gpufragmentstate-targets), may differ in colorState.[blend](https://www.w3.org/TR/webgpu/#dom-gpucolor and/or colorState.[writemask](https://www.w3.org/TR/webgpu/#dom-gpucolortargetstate-writemask)

## with the Compatibility Mode flag:

1. Under the section [validating GPUFragmentState](https://www.w3.org/TR/webgpu/#abstract-opdef-validating-gpufragmentstate), add:

If `compatibilityMode` is enabled for this Adapter:

- colorState.[blend](https://www.w3.org/TR/webgpu/#dom-gpucolortargetstate-blend) must contain the same value for all indices in _descriptor_.[targets](https://www.w3.org/TR/webgpu/#dom-gpufragmentstate-targets)
- colorState.[writemask](https://www.w3.org/TR/webgpu/#dom-gpucolortargetstate-writemask) must contain the same value for all indices in _descriptor_.[targets](https://www.w3.org/TR/webgpu/#dom-gpufragmentstate-targets)


