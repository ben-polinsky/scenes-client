---
"@itwin/scenes-client": patch
---

Accept every schema version in the default `SceneObject`, `SceneObjectCreate`, `SceneObjectUpdate`, `CreateSceneObjectOperation` and `UpdateSceneObjectOperation` types.

Before, these types without type arguments accepted only version `1.0.0`, so a Cutout `2.0.0` object did not match `SceneObject`.

- Added `AnySchemaVersion` and `AnySchemaData` helper types.
- `SceneObject<"Cutout">` is now `CutoutV1 | CutoutV2`, so it narrows by `version`.
