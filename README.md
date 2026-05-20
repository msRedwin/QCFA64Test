# QCFA64Test

Small diagnostic Camera2 app for POCO F2 Pro / lmi.

It tries to create a `9248x6944` JPEG output surface and sends Xiaomi vendor request keys:

```text
xiaomi.remosaic.enabled = 1
xiaomi.quadcfa.enabled = 1
```

This app is only for testing whether the vendor HAL accepts QCFA/remosaic capture without MIUI/Leica/ANX Camera.

## Build with GitHub Actions

1. Upload this repository to GitHub.
2. Open `Actions`.
3. Run `Build APK`.
4. Download artifact `QCFA64Test-debug-apk`.
5. Install the APK on the phone.

## Expected result

Success:
- `DCIM/QCFA_Test/QCFA64_*.jpg`
- Image size should be `9248x6944`

Failure:
- `CONFIGURE FAILED for 9248x6944 JPEG session`
- `CAPTURE FAILED`
- `Camera error`
