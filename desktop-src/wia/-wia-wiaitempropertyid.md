---
description: 大部分的 Windows 影像取得 (WIA) 屬性常數會分組為一個列舉資料類型，WiaItemPropertyId 為腳本作者。
ms.assetid: d0fd6bd1-c646-4ed8-a6b2-43b424af8288
title: WiaItemPropertyId
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: dedd11a35d52d19a4fcff4299dce688e8163ecd19d2bf9e4b49e19cb1997b293
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118207505"
---
# <a name="wiaitempropertyid"></a>WiaItemPropertyId

大部分的 Windows 影像取得 (WIA) 屬性常數會分組為一個列舉資料類型，WiaItemPropertyId 為腳本作者。

下表提供在腳本和 c + + 中使用的命名慣例之間的對應。 例如，在腳本中，"CameraDevice" 前置詞會 \_ 對應到對應 c + + 常數的 "WIA DPC" 前置詞。 在更明確的範例中，"CameraDeviceFlashMode" 屬性相當於 c + + "WIA \_ DPC \_ FLASH \_ MODE" 常數。 如需每個屬性的描述，請參閱對應的屬性常數主題。 

| 腳本前置詞  | C + + 主題 (前置詞)                                                                     |
|----------------|---------------------------------------------------------------------------------------|
| 裝置         | [**(WIA DPA) 的一般裝置屬性常數 \_**](-wia-wiaitempropcommondevice.md)   |
| CameraDevice   | [**相機裝置屬性常數 (WIA \_ DPC)**](-wia-wiaitempropcameradevice.md)   |
| ScannerDevice  | [**掃描器裝置屬性常數 (WIA \_ DPS)**](-wia-wiaitempropscannerdevice.md) |
| VideoDevice    | [**(WIA DPV) 的視頻 WIA 裝置屬性常數 \_**](-wia-wiaitempropvideodevice.md) |
| Picture        | [**(WIA IPA) 的通用 WIA 專案屬性常數 \_**](-wia-wiaitempropcommonitem.md)   |
| CameraPicture  | [**(WIA IPC) 的相機 WIA 專案屬性常數 \_**](-wia-wiaitempropcameraitem.md)   |
| ScannerPicture | [**掃描器 WIA 專案屬性常數 (WIA \_ ip)**](-wia-wiaitempropscanneritem.md) |



 

下列範例會提供具有對應名稱的完整列舉型別。


```JScript
typedef enum WiaItemPropertyId {
    CameraDevicePicturesTaken = WIA_DPC_PICTURES_TAKEN,
    CameraDevicePicturesRemaining = WIA_DPC_PICTURES_REMAINING,
    CameraDeviceExposureMode = WIA_DPC_EXPOSURE_MODE,
    CameraDeviceExposureComp = WIA_DPC_EXPOSURE_COMP,
    CameraDeviceExposureTime = WIA_DPC_EXPOSURE_TIME,
    CameraDeviceFNumber = WIA_DPC_FNUMBER,
    CameraDeviceFlashMode = WIA_DPC_FLASH_MODE,
    CameraDeviceFocusMode = WIA_DPC_FOCUS_MODE,
    CameraDevicePanPosition = WIA_DPC_PAN_POSITION,
    CameraDeviceTiltPosition = WIA_DPC_TILT_POSITION,
    CameraDeviceTimerMode = WIA_DPC_TIMER_MODE,
    CameraDeviceTimerValue = WIA_DPC_TIMER_VALUE,
    CameraDevicePowerMode = WIA_DPC_POWER_MODE,
    CameraDeviceBatteryStatus = WIA_DPC_BATTERY_STATUS,
    CameraDeviceThumbWidth = WIA_DPC_THUMB_WIDTH,
    CameraDeviceThumbHeight = WIA_DPC_THUMB_HEIGHT,
    CameraDevicePictWidth = WIA_DPC_PICT_WIDTH,
    CameraDevicePictHeight = WIA_DPC_PICT_HEIGHT,
    CameraDeviceCompressionSetting = WIA_DPC_COMPRESSION_SETTING,
    CameraDeviceTimelapseInterval = WIA_DPC_TIMELAPSE_INTERVAL,
    CameraDeviceTimelapseNumber = WIA_DPC_TIMELAPSE_NUMBER,
    CameraDeviceBurstInterval = WIA_DPC_BURST_INTERVAL,
    CameraDeviceBurstNumber = WIA_DPC_BURST_NUMBER,
    CameraDeviceEffectMode = WIA_DPC_EFFECT_MODE,
    CameraDeviceDigitalZoom = WIA_DPC_DIGITAL_ZOOM,
    CameraDeviceSharpness = WIA_DPC_SHARPNESS,
    CameraDeviceContrast = WIA_DPC_CONTRAST,
    CameraDeviceCaptureMode = WIA_DPC_CAPTURE_MODE,
    CameraDeviceCaptureDelay = WIA_DPC_CAPTURE_DELAY,
    CameraDeviceExposureIndex = WIA_DPC_EXPOSURE_INDEX,
    CameraDeviceExposureMeteringMode = WIA_DPC_EXPOSURE_METERING_MODE,
    CameraDeviceFocusMeteringMode = WIA_DPC_FOCUS_METERING_MODE,
    CameraDeviceFocusDistance = WIA_DPC_FOCUS_DISTANCE,
    CameraDeviceFocalLength = WIA_DPC_FOCAL_LENGTH,
    CameraDeviceRGBGain = WIA_DPC_RGB_GAIN,
    CameraDeviceWhiteBalance = WIA_DPC_WHITE_BALANCE,
    CameraDeviceUploadURL = WIA_DPC_UPLOAD_URL,
    CameraDeviceArtist = WIA_DPC_ARTIST,
    CameraDeviceCopyrightInfo = WIA_DPC_COPYRIGHT_INFO,
    ScannerDeviceHorizontalBedSize = WIA_DPS_HORIZONTAL_BED_SIZE,
    ScannerDeviceVerticalBedSize = WIA_DPS_VERTICAL_BED_SIZE,
    ScannerDeviceHorizontalSheetFeedSize = WIA_DPS_HORIZONTAL_SHEET_FEED_SIZE,
    ScannerDeviceVerticalSheetFeedSize = WIA_DPS_VERTICAL_SHEET_FEED_SIZE,
    ScannerDeviceSheetFeederRegistration = WIA_DPS_SHEET_FEEDER_REGISTRATION,
    ScannerDeviceHorizontalBedRegistration = WIA_DPS_HORIZONTAL_BED_REGISTRATION,
    ScannerDeviceVerticalBedRegistration = WIA_DPS_VERTICAL_BED_REGISTRATION,
    ScannerDevicePlatenColor = WIA_DPS_PLATEN_COLOR,
    ScannerDevicePadColor = WIA_DPS_PAD_COLOR,
    ScannerDeviceDocumentHandlingCapabilities = WIA_DPS_DOCUMENT_HANDLING_CAPABILITIES,
    ScannerDeviceDocumentHandlingStatus = WIA_DPS_DOCUMENT_HANDLING_STATUS,
    ScannerDeviceDocumentHandlingSelect = WIA_DPS_DOCUMENT_HANDLING_SELECT,
    ScannerDeviceDocumentHandlingCapacity = WIA_DPS_DOCUMENT_HANDLING_CAPACITY,
    ScannerDeviceOpticalXres = WIA_DPS_OPTICAL_XRES,
    ScannerDeviceOpticalYres = WIA_DPS_OPTICAL_YRES,
    ScannerDeviceEndorserCharacters = WIA_DPS_ENDORSER_CHARACTERS,
    ScannerDeviceEndorserString = WIA_DPS_ENDORSER_STRING,
    ScannerDeviceScanAheadPages = WIA_DPS_SCAN_AHEAD_PAGES,
    ScannerDeviceMaxScanTime = WIA_DPS_MAX_SCAN_TIME,
    ScannerDevicePages = WIA_DPS_PAGES,
    ScannerDevicePageSize = WIA_DPS_PAGE_SIZE,
    ScannerDevicePageWidth = WIA_DPS_PAGE_WIDTH,
    ScannerDevicePageHeight = WIA_DPS_PAGE_HEIGHT,
    ScannerDevicePreview = WIA_DPS_PREVIEW,
    ScannerDeviceTransparency = WIA_DPS_TRANSPARENCY,
    ScannerDeviceTransparencySelect = WIA_DPS_TRANSPARENCY_SELECT,
    ScannerDeviceShowPreviewControl = WIA_DPS_SHOW_PREVIEW_CONTROL,
    ScannerDeviceMinHorizontalSheetFeedSize = WIA_DPS_MIN_HORIZONTAL_SHEET_FEED_SIZE,
    ScannerDeviceMinVerticalSheetFeedSize = WIA_DPS_MIN_VERTICAL_SHEET_FEED_SIZE,
    FileDeviceMountPoint = WIA_DPF_MOUNT_POINT,
    VideoDeviceLastPictureTaken = WIA_DPV_LAST_PICTURE_TAKEN,
    VideoDeviceImagesDirectory = WIA_DPV_IMAGES_DIRECTORY,
    VideoDeviceDShowDevicePath = WIA_DPV_DSHOW_DEVICE_PATH,
    PictureItemName = WIA_IPA_ITEM_NAME,
    PictureFullItemName = WIA_IPA_FULL_ITEM_NAME,
    PictureItemTime = WIA_IPA_ITEM_TIME,
    PictureItemFlags = WIA_IPA_ITEM_FLAGS,
    PictureAccessRights = WIA_IPA_ACCESS_RIGHTS,
    PictureDatatype = WIA_IPA_DATATYPE,
    PictureDepth = WIA_IPA_DEPTH,
    PicturePreferredFormat = WIA_IPA_PREFERRED_FORMAT,
    PictureFormat = WIA_IPA_FORMAT,
    PictureCompression = WIA_IPA_COMPRESSION,
    PictureTymed = WIA_IPA_TYMED,
    PictureChannelsPerPixel = WIA_IPA_CHANNELS_PER_PIXEL,
    PictureBitsPerChannel = WIA_IPA_BITS_PER_CHANNEL,
    PicturePlanar = WIA_IPA_PLANAR,
    PicturePixelsPerLine = WIA_IPA_PIXELS_PER_LINE,
    PictureBytesPerLine = WIA_IPA_BYTES_PER_LINE,
    PictureNumberOfLines = WIA_IPA_NUMBER_OF_LINES,
    PictureGammaCurves = WIA_IPA_GAMMA_CURVES,
    PictureItemSize = WIA_IPA_ITEM_SIZE,
    PictureColorProfile = WIA_IPA_COLOR_PROFILE,
    PictureMinBufferSize = WIA_IPA_MIN_BUFFER_SIZE,
    PictureBufferSize = WIA_IPA_BUFFER_SIZE,
    PictureRegionType = WIA_IPA_REGION_TYPE,
    PictureIcmProfileName = WIA_IPA_ICM_PROFILE_NAME,
    PictureAppColorMapping = WIA_IPA_APP_COLOR_MAPPING,
    PicturePropStreamCompatId = WIA_IPA_PROP_STREAM_COMPAT_ID,
    PictureFilenameExtension = WIA_IPA_FILENAME_EXTENSION,
    PictureSuppressPropertyPage = WIA_IPA_SUPPRESS_PROPERTY_PAGE,
    CameraPictureThumbnail = WIA_IPC_THUMBNAIL,
    CameraPictureThumbWidth = WIA_IPC_THUMB_WIDTH,
    CameraPictureThumbHeight = WIA_IPC_THUMB_HEIGHT,
    CameraPictureAudioAvailable = WIA_IPC_AUDIO_AVAILABLE,
    CameraPictureAudioDataFormat = WIA_IPC_AUDIO_DATA_FORMAT,
    CameraPictureAudioData = WIA_IPC_AUDIO_DATA,
    CameraPictureNumPictPerRow = WIA_IPC_NUM_PICT_PER_ROW,
    CameraPictureSequence = WIA_IPC_SEQUENCE,
    CameraPictureTimedelay = WIA_IPC_TIMEDELAY,
    ScannerPictureCurIntent = WIA_IPS_CUR_INTENT,
    ScannerPictureXres = WIA_IPS_XRES,
    ScannerPictureYres = WIA_IPS_YRES,
    ScannerPictureXpos = WIA_IPS_XPOS,
    ScannerPictureYpos = WIA_IPS_YPOS,
    ScannerPictureXextent = WIA_IPS_XEXTENT,
    ScannerPictureYextent = WIA_IPS_YEXTENT,
    ScannerPicturePhotometricInterp = WIA_IPS_PHOTOMETRIC_INTERP,
    ScannerPictureBrightness = WIA_IPS_BRIGHTNESS,
    ScannerPictureContrast = WIA_IPS_CONTRAST,
    ScannerPictureOrientation = WIA_IPS_ORIENTATION,
    ScannerPictureRotation = WIA_IPS_ROTATION,
    ScannerPictureMirror = WIA_IPS_MIRROR,
    ScannerPictureThreshold = WIA_IPS_THRESHOLD,
    ScannerPictureInvert = WIA_IPS_INVERT,
    ScannerPictureWarmUpTime = WIA_IPS_WARM_UP_TIME
} WiaItemPropertyId;
```



 

 



