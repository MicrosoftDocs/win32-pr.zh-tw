---
description: 此篩選器會將 MPEG-2、MPEG-2、h.264 video 解碼。
ms.assetid: d8195c3a-97ac-4ad1-a097-18878c8fda6f
title: 'Microsoft MPEG-2 影片解碼 (Wmcodecdsp .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8460b5b554fffc8f0dd8679810e5ef3f42bcb004
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104385609"
---
# <a name="microsoft-mpeg-2-video-decoder"></a>Microsoft MPEG-2 影片解碼

此篩選器會將 MPEG-2、MPEG-2、h.264 video 解碼。

> [!Note]  
> 對 h.264 video 進行解碼需要 Windows 7。

 

> [!Note]  
> 以 IA-64 為基礎的平臺不支援此篩選器。

 

在登錄中，此篩選器的易記名稱是「Microsoft DTV DVD Video 解碼」。



篩選資訊

篩選介面

[**IAMDecoderCaps**](/windows/desktop/api/Strmif/nn-strmif-iamdecodercaps)<br/> [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)<br/> [**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)<br/>

輸入 Pin 媒體類型

影片輸入釘選：

-   媒體 \_ 媒體 \_ 加密 \_ 套件，MEDIASUBTYPE \_ MPEG2 \_ 影片
-   媒體 \_ \_ 上的 MPEG2，MEDIASUBTYPE \_ MPEG2 \_ 影片
-   媒體媒體 \_ 、MEDIASUBTYPE \_ MPEG1Packet
-   媒體媒體 \_ 、MEDIASUBTYPE \_ MPEG1Payload
-   媒體媒體 \_ MEDIASUBTYPE \_ MPEG2 \_ 影片

子圖片輸入 pin：<br/>

-   媒體 \_ \_ \_ MEDIASUBTYPE \_ DVD 子圖片、媒體加密 \_ 套件

從 Windows 7 開始，影片輸入 pin 也支援下列輸入類型：<br/>

-   **媒體媒體 \_影片**、 **MEDIASUBTYPE \_ AVC1**
-   **媒體媒體 \_影片**， **MEDIASUBTYPE \_ H264**
-   **媒體媒體 \_影片**， **MEDIASUBTYPE \_ h264**
-   **媒體媒體 \_影片**、 **MEDIASUBTYPE \_ X264**
-   **媒體媒體 \_影片**、 **MEDIASUBTYPE \_ x264**

如需詳細資訊，請參閱 h.264 [影片類型](h-264-video-types.md) 。 輸入媒體類型可以在 MPEG2 和 h.264 類型之間動態變更。<br/>

輸入 Pin 介面

[**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)<br/> [**IKsPropertySet**](ikspropertyset.md)<br/> [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin)<br/> [**IMFSampleProtection**](/windows/win32/api/mfidl/nn-mfidl-imfsampleprotection)<br/> [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)<br/> [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)<br/>

輸出 Pin 媒體類型

影片輸出圖釘：

-   媒體媒體 \_ 、DXVA \_ MODEMPEG2 \_ (DXVA 1.0) 
-   媒體媒體 \_ 、DXVA \_ ModeMPEG2 \_ C (DXVA 1.0) 
-   媒體媒體 \_ 、MEDIASUBTYPE \_ I420 (軟體解碼或 dxva 2.0) 
-   媒體媒體 \_ 、MEDIASUBTYPE \_ NV12 (軟體解碼或 dxva 2.0) 
-   媒體媒體 \_ 、MEDIASUBTYPE \_ YUY2 (軟體解碼或 dxva 2.0) 
-   媒體媒體 \_ 、MEDIASUBTYPE \_ IMC3 (僅限 dxva 2.0) 
-   媒體媒體 \_ 、MEDIASUBTYPE \_ IMC4 (僅限 dxva 2.0) 
-   媒體媒體 \_ 、MEDIASUBTYPE \_ S340 (僅限 dxva 2.0) 
-   媒體媒體 \_ 、MEDIASUBTYPE \_ YV12 (僅限 dxva 2.0) 

行21輸出圖釘：<br/>

-   媒體 \_ AUXLine21Data、MEDIASUBTYPE \_ Line21 \_ GOPPacket

子圖片輸出 pin：<br/>

-   媒體媒體 \_ 、MEDIASUBTYPE \_ AI44
-   媒體媒體 \_ 、MEDIASUBTYPE \_ ARGB32
-   媒體媒體 \_ 、MEDIASUBTYPE \_ ARGB4444
-   媒體媒體 \_ 、MEDIASUBTYPE \_ AYUV

輸出 Pin 介面

[**IAMVideoAcceleratorNotify**](/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoacceleratornotify) (video 輸出釘選) <br/> [**IKsPropertySet**](ikspropertyset.md)<br/> [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)<br/> [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)<br/> [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)<br/> [**IVPConfig**](/previous-versions/windows/desktop/api/Vpconfig/nn-vpconfig-ivpconfig)<br/>

篩選 CLSID

**CLSID \_** 在 wmcodecdsp 中定義的 CMPEG2VidDecoderDS () 

可執行檔

msmpeg2vdec.dll

[優點](merit.md)

**業績 \_正常** -1

[篩選準則分類](filter-categories.md)

**CLSID \_ LegacyAmFilterCategory**



 

## <a name="remarks"></a>備註

此篩選器有兩個輸入圖釘和三個輸出圖釘。

輸入釘：

-   視訊輸入
-   子圖片輸入

輸出圖釘：

-   視訊輸出
-   行21輸出
-   子圖片輸出

篩選不會建立子圖片輸出 pin，除非影片輸入 pin 與媒體 **\_ \_ 加密 \_ 套件** 媒體類型連線。

### <a name="mpeg-12-support"></a>MPEG 1/2 支援

若為 MPEG 1 和 MPEG-2，此解碼器支援下列格式：



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>設定檔/層級</td>
<td>下列設定檔和層級的任意組合：<br/>
<ul>
<li>設定檔：簡單、主要</li>
<li>層級：低、主要、高、高1440</li>
</ul></td>
</tr>
<tr class="even">
<td>色度格式</td>
<td>4:2:0 色度</td>
</tr>
<tr class="odd">
<td>最大解析度</td>
<td>1920×1088圖元</td>
</tr>
<tr class="even">
<td>DXVA</td>
<td>此解碼器支援 DirectX Video 加速 (DXVA) 第1版和第2版。</td>
</tr>
</tbody>
</table>



 

此解碼器不支援可調整的 bitstreams。 輸入必須是基本影片串流。

此解碼器不支援4:2:2 色度格式。

### <a name="h264-support"></a>H.264 支援

針對 h.264，此解碼器支援下列格式：



| 需求 | 值 |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 設定檔/層級    | 基準、主要和高設定檔，最高到層級5.1。  (如需詳細資料，請參閱 ITU-T h.264 規格。 )                                                                                                                                                                           |
| 色度格式     | 4:2:0 色度或單色                                                                                                                                                                                                                                                |
| 最低解析度 | 48×48圖元                                                                                                                                                                                                                                                            |
| 最大解析度 | 1920×1088圖元                                                                                                                                                                                                                                                        |
| DXVA               | 此解碼器支援 DXVA 第2版，但不支援 DXVA 第1版。 只有主要相容的基準、主要和高設定檔 bitstreams 才支援 DXVA 解碼。  (主要相容的基準 bitstreams 定義為 **設定檔 \_ idc**= 66，且 **限制 \_ set1 \_ 旗** 標 = 1。 )  |



 

此解碼器不支援電影細微性技術。

如需有關 h.264 媒體類型的詳細資訊，請參閱 h.264 [影片類型](h-264-video-types.md)。

### <a name="codec-properties"></a>編解碼器屬性

輸入 pin 支援下列透過 [**IKsPropertySet**](ikspropertyset.md)的屬性集：

-   [**DVD 禁止複製屬性集**](dvd-copy-protection-property-set.md)
-   [**DVD 子圖片屬性集**](dvd-subpicture-property-set.md) (僅子圖片 pin) 

輸入 pin 透過 [**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)支援下列屬性：



| 屬性                                                                  | 需要      |
|---------------------------------------------------------------------------|---------------|
| [**AVDecCommonInputFormat**](avdeccommoninputformat-property.md)         | Windows Vista |
| [**AVDecVideoInputScanType**](avdecvideoinputscantype-property.md)       | Windows Vista |
| [**AVDecVideoPixelAspectRatio**](avdecvideopixelaspectratio-property.md) | Windows Vista |



 

篩選準則透過 [**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)支援下列屬性：



| 屬性                                                                                | 需要      |
|-----------------------------------------------------------------------------------------|---------------|
| [**AVDecMmcssClass**](avdecmmcss-property.md)                                          | Windows Vista |
| [**AVDecVideoAcceleration \_ H264**](avdecvideoacceleration-h264-property.md)            | Windows 7     |
| [**AVDecVideoAcceleration \_ MPEG2**](avdecvideoacceleration-mpeg2-property.md)          | Windows 7     |
| [**AVDecVideoDropPicWithMissingRef**](avdecvideodroppicwithmissingref-property.md)     | Windows 7     |
| [**AVDecVideoFastDecodeMode**](avdecvideofastdecodemode.md)                            | Windows 7     |
| [**AVDecVideoImageSize**](avdecvideoimagesize.md)                                      | Windows 7     |
| [**AVDecVideoSoftwareDeinterlaceMode**](avdecvideosoftwaredeinterlacemode-property.md) | Windows 7     |
| [**AVDecVideoThumbnailGenerationMode**](avdecvideothumbnailgenerationmode-property.md) | Windows 7     |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista Home Premium、Windows Vista 旗艦版、Windows 7 Home Premium、Windows 7 Professional、Windows 7 企業版、僅限 Windows 7 旗艦版傳統型 \[ 應用程式\]<br/> |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                                                                                                     |
| 標頭<br/>                   | <dl> <dt>Wmcodecdsp。h</dt> </dl>                                                                                       |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[DirectShow 篩選](directshow-filters.md)
</dt> <dt>

[**DVD 媒體類型**](dvd-media-types.md)
</dt> <dt>

[H.264 影片類型](h-264-video-types.md)
</dt> </dl>

 

 
