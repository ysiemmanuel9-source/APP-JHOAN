# YOJHAN CHEATS

Private client build with Supabase key activation and automatic bundled patches.

## What this build does

- Shows the app as `YOJHAN CHEATS`.
- Requires a Supabase license key before opening the app.
- Consumes each key one time on the server and binds it to one iOS device ID.
- Re-checks the license on launch, foreground, and every 10 seconds while active.
- Syncs published remote files from Supabase Storage into YOJHAN CHEATS' own app storage, using a versioned `target_path` so replacing the same route downloads only the changed file.
- Downloads only changed files, verifies SHA-256, and rolls back local content if an update fails.
- Adds a PC admin panel in `admin/` for uploading, replacing, disabling, deleting, and publishing content changes.
- Creates the internal `Asset Indexer`, `Shaders`, and `144 fps` patches automatically after activation.
- Shows the extra `YOJHAN Especial` patch only for the special key `YJC-ESPECIAL927394HD`.
- Lets the client use `Apply`, `Original`, and name editing only.
- Hides Files, Cleaner, Wallpapers, patch creation, import, export, and editing.

## Included private payloads

The bundled payload files live in:

```text
ThreeOneOSFive/BundledPatchPayloads/
```

Included names:

```text
assetindexer.H5ak1JM1Eck~2FxRcJrEp~2FMzeuqmY~3D
shaders.HPt9DZviTSXL9hpGW9QNOMigNLA~3D
com.dts.freefireth.plist
assetindexer.yojhan-especial927394hd
```

Patch targets:

```text
Asset Indexer:
Documents/contentcache/Compulsory/ios/gameassetbundles/avatar/assetindexer.H5ak1JM1Eck~2FxRcJrEp~2FMzeuqmY~3D

Shaders:
Documents/contentcache/Optional/ios/gameassetbundles/shaders.HPt9DZviTSXL9hpGW9QNOMigNLA~3D

144 fps:
Library/Preferences/com.dts.freefireth.plist

YOJHAN Especial, only for `YJC-ESPECIAL927394HD`:
Documents/contentcache/Compulsory/ios/gameassetbundles/avatar/assetindexer.H5ak1JM1Eck~2FxRcJrEp~2FMzeuqmY~3D
```

Run `supabase/YOJHAN_CHEATS_SETUP.sql` once in the Supabase SQL Editor. It creates the license system, admin RPCs, Storage bucket, remote-content tables, RLS policies, and the initial special key.

The iOS client and the PC panel both use the YOJHAN Supabase project URL and publishable key; admin writes require Supabase Auth plus a row in `public.license_admins`.

See `YOJHAN_BUILD_GUIDE.md` for Supabase setup and GitHub Actions build steps.

