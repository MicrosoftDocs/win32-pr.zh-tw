---
description: 下列影片子類型 Guid 定義在標頭檔 mfapi 中。 若要指定子類型，請 \_ \_ 在媒體類型上設定 [MF MT 子類型] 屬性。
ms.assetid: 7dfd85e6-936e-4b78-a2cb-a5d59153e1c4
title: 影片子類型 Guid
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38829480aed7372496fc196cc6c55d781b672a2b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104513032"
---
# <a name="video-subtype-guids"></a>影片子類型 Guid

下列影片子類型 Guid 定義在標頭檔 mfapi 中。 若要指定子類型，請在媒體類型上設定 [ [**MF \_ MT \_ 子類型**](mf-mt-subtype-attribute.md) ] 屬性。

使用這些子類型時，請將 [ [MF \_ MT \_ 主要 \_ 類型](mf-mt-major-type-attribute.md) ] 屬性設定為 [ **MFMediaType \_ Video**]。

-   [未壓縮的 RGB 格式](#uncompressed-rgb-formats)
-   [YUV 格式：8位和調色盤](#yuv-formats-8-bit-and-palettized)
-   [YUV 格式：10位和16位](#yuv-formats-10-bit-and-16-bit)
-   [亮度和深度格式](#luminance-and-depth-formats)
-   [編碼的影片類型](#encoded-video-types)
-   [從 FOURCCs 和 D3DFORMAT 值建立子類型 Guid](#creating-subtype-guids-from-fourccs-and-d3dformat-values)
-   [相關主題](#related-topics)

## <a name="uncompressed-rgb-formats"></a>未壓縮的 RGB 格式



| GUID                             | Description                                                                                     |
|----------------------------------|-------------------------------------------------------------------------------------------------|
| **MFVideoFormat \_ RGB8**          | RGB，每圖元8位 (bpp) 。  (與 **D3DFMT \_ P8** 相同的記憶體配置。 )                             |
| **MFVideoFormat \_ RGB555**        | RGB 555、16 bpp。  (與 **D3DFMT \_ X1R5G5B5** 相同的記憶體配置。 )                                   |
| **MFVideoFormat \_ RGB565**        | RGB 565、16 bpp。  (與 **D3DFMT \_ R5G6B5** 相同的記憶體配置。 )                                     |
| **MFVideoFormat \_ RGB24**         | RGB，24 bpp。                                                                                    |
| **MFVideoFormat \_ RGB32**         | RGB、32 bpp。                                                                                    |
| **MFVideoFormat \_ ARGB32**        | RGB、32 bpp 和 Alpha 色板。                                                                 |
| **MFVideoFormat \_ A2R10G10B10**   | RGB、適用于每個色彩的 10 bpp 和 Alpha 的 2 bpp。  (與 **D3DFMT \_ A2B10G10R10** 相同的記憶體配置)  |
| **MFVideoFormat \_ A16B16G16R16F** | RGB、16 bpp 和 Alpha 色板。  (與 **D3DFMT \_ A16B16G16R16F** 相同的記憶體配置)                |



 

> [!Note]  
> 這些子類型不符合先前 Sdk （例如 DirectShow）中使用的 RGB 子類型 Guid。

 

## <a name="yuv-formats-8-bit-and-palettized"></a>YUV 格式：8位和調色盤



| GUID                    | 格式 | 取樣 | 已封裝或平面 | 每個通道的位數 |
|-------------------------|--------|----------|------------------|------------------|
| **MFVideoFormat \_ AI44** | AI44   | 4:4:4    | 包裝           | 調色盤       |
| **MFVideoFormat \_ AYUV** | AYUV   | 4:4:4    | 包裝           | 8                |
| **MFVideoFormat \_ I420** | I420   | 4:2:0    | 平面           | 8                |
| **MFVideoFormat \_ IYUV** | IYUV   | 4:2:0    | 平面           | 8                |
| **MFVideoFormat \_ NV11** | NV11   | 4:1:1    | 平面           | 8                |
| **MFVideoFormat \_ NV12** | NV12   | 4:2:0    | 平面           | 8                |
| **MFVideoFormat \_ UYVY** | UYVY   | 4:2:2    | 包裝           | 8                |
| **MFVideoFormat \_ Y41P** | Y41P   | 4:1:1    | 包裝           | 8                |
| **MFVideoFormat \_ Y41T** | Y41T   | 4:1:1    | 包裝           | 8                |
| **MFVideoFormat \_ Y42T** | Y42T   | 4:2:2    | 包裝           | 8                |
| **MFVideoFormat \_ YUY2** | YUY2   | 4:2:2    | 包裝           | 8                |
| **MFVideoFormat \_ YVU9** | YVU9   | 8:4:4    | 平面           | 9                |
| **MFVideoFormat \_ YV12** | YV12   | 4:2:0    | 平面           | 8                |
| **MFVideoFormat \_ YVYU** | YVYU   | 4:2:2    | 包裝           | 8                |



 

建議的 YUV 格式將在影片轉譯的 [建議8位 YUV 格式](recommended-8-bit-yuv-formats-for-video-rendering.md)中詳細說明。

> [!Note]  
> I420 和 IYUV 在記憶體中具有相同的版面配置，但指派了相異的子類型 Guid。 子類型 Guid 對應于 FOURCC 碼 ' I420 ' 和 ' IYUV ';如需詳細資訊，請參閱 [影片 FOURCCs](video-fourccs.md) 。

 

## <a name="yuv-formats-10-bit-and-16-bit"></a>YUV 格式：10位和16位



| GUID                    | 格式 | 取樣 | 已封裝或平面 | 每個通道的位數 |
|-------------------------|--------|----------|------------------|------------------|
| **MFVideoFormat \_ P010** | P010   | 4:2:0    | 平面           | 10               |
| **MFVideoFormat \_ P016** | P016   | 4:2:0    | 平面           | 16               |
| **MFVideoFormat \_ P210** | P210   | 4:2:2    | 平面           | 10               |
| **MFVideoFormat \_ P216** | P216   | 4:2:2    | 平面           | 16               |
| **MFVideoFormat \_ v210** | v210   | 4:2:2    | 包裝           | 10               |
| **MFVideoFormat \_ v216** | v216   | 4:2:2    | 包裝           | 16               |
| **MFVideoFormat \_ v410** | v40    | 4:4:4    | 包裝           | 10               |
| **MFVideoFormat \_ Y210** | Y210   | 4:2:2    | 包裝           | 10               |
| **MFVideoFormat \_ Y216** | Y216   | 4:2:2    | 包裝           | 16               |
| **MFVideoFormat \_ Y410** | Y40    | 4:4:4    | 包裝           | 10               |
| **MFVideoFormat \_ Y416** | Y416   | 4:4:4    | 包裝           | 16               |



 

如需這些格式的詳細資訊，請參閱 [10 位和16位的 YUV 影片格式](10-bit-and-16-bit-yuv-video-formats.md)。

## <a name="luminance-and-depth-formats"></a>亮度和深度格式



| GUID                   | Description                                                          |
|------------------------|----------------------------------------------------------------------|
| **MFVideoFormat 的 \_ L8**  | 僅限8位的亮度。  (bpp) 。  (與 **D3DFMT \_ L8** 相同的記憶體配置 )  |
| **MFVideoFormat \_ l16 也** | 僅限16位的亮度。  (與 **D3DFMT \_ l16 也** 相同的記憶體配置。 )       |
| **MFVideoFormat \_ D16** | 16位 z-緩衝區深度。  (與 **D3DFMT \_ D16** 相同的記憶體配置。 )       |



 

## <a name="encoded-video-types"></a>編碼的影片類型



| GUID                        | FOURCC         | Description                                                                                                                                                                                                                                                                                                 |
|-----------------------------|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **MFVideoFormat \_ DV25**     | 'dv25'         | DVCPRO 25 (525-60 或 625-50) 。                                                                                                                                                                                                                                                                               |
| **MFVideoFormat \_ DV50**     | 'dv50'         | DVCPRO 50 (525-60 或 625-50) 。                                                                                                                                                                                                                                                                               |
| **MFVideoFormat \_ DVC**      | dvc         | DVC/DV 影片。                                                                                                                                                                                                                                                                                               |
| **MFVideoFormat \_ DVH1**     | 'dvh1'         | DVCPRO 100 (1080/60i、1080/50i 或 720/60P) 。                                                                                                                                                                                                                                                                |
| **MFVideoFormat \_ DVHD**     | 'dvhd'         | HD-DVCR (1125-60 或 1250-50) 。                                                                                                                                                                                                                                                                               |
| **MFVideoFormat \_ DVSD**     | 'dvsd'         | SDL-DVCR (525-60 或 625-50) 。                                                                                                                                                                                                                                                                                |
| **MFVideoFormat \_ DVSL**     | 'dvsl'         | SD-DVCR (525-60 或 625-50) 。                                                                                                                                                                                                                                                                                 |
| **MFVideoFormat \_ H263**     | 'H263'         | H. 影片。                                                                                                                                                                                                                                                                                                |
| **MFVideoFormat \_ H264**     | H264         | H.264 video。<br/> 媒體範例包含具有起始程式碼的位流資料，並具有交錯的 SPS/PPS。 每個範例都包含一個完整的圖片，也就是一個欄位或一個畫面格。<br/>                                                                                                       |
| **MFVideoFormat \_ H265**     | 'H265'         | H. 265 video。                                                                                                                                                                                                                                                                                                |
| **MFVideoFormat \_ H264 \_ ES** | 不適用 | H.264 基本資料流程。<br/> 此媒體類型與 **MFVideoFormat \_ H264** 相同，不同之處在于媒體範例包含片段位流。 每個範例可能包含部分圖片;多個完整圖片;或一或多個完整圖片，再加上部分圖片。<br/>           |
| **MFVideoFormat \_ HEVC**     | HEVC         | HEVC 主要設定檔和主要的圖片設定檔。<br/> 每個範例都包含一個完整的圖片。<br/> 在 Windows 8.1 和更新版本中支援。 HEVC 主要設定檔和主要的圖片設定檔基本資料流程。 <br/>                                                              |
| **MFVideoFormat \_ HEVC \_ ES** | 'HEVS'         | 此媒體類型與 **MFVideoFormat \_ HEVC** 相同，不同之處在于媒體範例包含分散的 HEVC 位流。 每個範例可能包含部分圖片;多個完整圖片;或一或多個完整圖片，再加上部分圖片。<br/> 在 Windows 8.1 和更新版本中支援。<br/> |
| **MFVideoFormat \_ M4S2**     | 4S2 '         | MPEG 4 第2部分影片。                                                                                                                                                                                                                                                                                        |
| **MFVideoFormat \_ MJPG**     | 'MJPG'         | 動畫 JPEG。                                                                                                                                                                                                                                                                                                |
| **MFVideoFormat \_ MP43**     | 'MP43'         | Microsoft MPEG 4 編解碼器第3版。 不再支援此編解碼器。                                                                                                                                                                                                                                        |
| **MFVideoFormat \_ mp4**     | MP4         | ISO MPEG 4 編解碼器第1版。                                                                                                                                                                                                                                                                                 |
| **MFVideoFormat \_ MP4V**     | 'MP4V'         | MPEG 4 第2部分影片。                                                                                                                                                                                                                                                                                        |
| **MFVideoFormat \_ MPEG2**    | 不適用 | MPEG-2 影片。  (相當於 DirectShow 中的 **MEDIASUBTYPE \_ MPEG2 \_ 影片** 。 )                                                                                                                                                                                                                                  |
| **MFVideoFormat \_ VP80**     | 'MPG1'         | VP8 影片。                                                                                                                                                                                                                                                                                                  |
| **MFVideoFormat \_ VP90**     | 'MPG1'         | VP9 影片。                                                                                                                                                                                                                                                                                                  |
| **MFVideoFormat \_ MPG1**     | 'MPG1'         | MPEG-2 影片。                                                                                                                                                                                                                                                                                               |
| **MFVideoFormat \_ MSS1**     | 'MSS1'         | Windows Media Screen 編解碼器第1版。                                                                                                                                                                                                                                                                       |
| **MFVideoFormat \_ MSS2**     | 'MSS2'         | Windows Media 視訊9螢幕編解碼器。                                                                                                                                                                                                                                                                         |
| **MFVideoFormat \_ WMV1**     | 'WMV1'         | Windows Media 視訊編解碼器版本7。                                                                                                                                                                                                                                                                        |
| **MFVideoFormat \_ WMV2**     | 'WMV2'         | Windows Media 視訊8編解碼器。                                                                                                                                                                                                                                                                                |
| **MFVideoFormat \_ WMV3**     | 'WMV3'         | Windows Media 視訊9編解碼器。                                                                                                                                                                                                                                                                                |
| **MFVideoFormat \_ WVC1**     | 'WVC1'         | SMPTE 421M ( "VC-1" ) 。                                                                                                                                                                                                                                                                                        |
| **MFVideoFormat \_ 420O**     | '420O'         | 每一頻道8位的平面 YUV 4:2:0 影片。                                                                                                                                                                                                                                                                   |
| **MFVideoFormat \_ AV1**     | 'AV01'         | AV1 影片。                                                                                                                                                                                                                                                                                                |



 

## <a name="creating-subtype-guids-from-fourccs-and-d3dformat-values"></a>從 FOURCCs 和 D3DFORMAT 值建立子類型 Guid

影片格式通常以 FOURCCs 或 **D3DFORMAT** 值表示。 會保留一個範圍的 Guid，將這些值表示為子類型。 這些 Guid 具有表單 `XXXXXXXX-0000-0010-8000-00AA00389B71` ，其中 `XXXXXXXX` 是4位元組的 FOURCC 碼或 **D3DFORMAT** 值。

如果影片格式有相關聯的 FOURCC 或 **D3DFORMAT** 值，您可以建立對應的子類型 GUID，如下所示：從常數 **MFVideoFormat \_ 基底** 開始，並以影片 FOURCC 或 **D3DFORMAT** 值取代 GUID 的第一個 **DWORD** 。 您可以針對此用途使用 [**定義 \_ 媒體 \_ GUID**](/windows/desktop/api/mfapi/nf-mfapi-define_mediatype_guid) 宏。

> [!Note]  
> DirectShow 也會將這個系統用於大部分的影片子類型，但不適用於未壓縮的 RGB 格式。 因此，DirectShow 中的 RGB 子類型不符合媒體基礎中的 RGB 子類型。

 

**D3DFORMAT** 列舉是在標頭檔 d3d9types 中定義。 下表顯示最常見的未壓縮 RGB 格式和對應的 **D3DFORMAT** 值。



| RGB 格式                                                              | **D3DFORMAT** 值     |
|-------------------------------------------------------------------------|-------------------------|
| 32位 RGB                                                              | **D3DFMT \_ X8R8G8B8**    |
| 使用 Alpha 通道的32位 RGB                                           | **D3DFMT \_ A8R8G8B8**    |
| 24位 RGB                                                              | **D3DFMT \_ R8G8B8**      |
| RGB 555 (16 位 RGB)                                                     | **D3DFMT \_ X1R5G5B5**    |
| 具有 Alpha 通道的 RGB 555                                              | **D3DFMT \_ A4R4G4B4**    |
| RGB 565 (16 位 RGB)                                                     | **D3DFMT \_ R5G6B5**      |
| 8位調色盤 RGB                                                    | **D3DFMT \_ P8**          |
| A2 R4-r10 G10 B10 (32 位 RGB 搭配 Alpha 通道;每個 RGB 通道) 10 個位 | **D3DFMT \_ A2R10G10B10** |
| A2 B10 G10 R4-r10 (32-位 RGB 搭配 Alpha 通道;每個 RGB 通道) 10 個位 | **D3DFMT \_ A2B10G10R10** |
| 僅限8位的亮度。                                                   | **D3DFMT 的 \_ L8**          |
| 僅限16位的亮度。                                                  | **D3DFMT \_ l16 也**         |
| 16位 z-緩衝區深度                                                   | **D3DFMT \_ D16**         |



 

如需 FOURCCs 的詳細資訊，請參閱 [影片 FOURCCs](video-fourccs.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[媒體類型 Guid](media-type-guids.md)
</dt> <dt>

[**MF \_ MT \_ 子類型**](mf-mt-subtype-attribute.md)
</dt> <dt>

[媒體類型](media-types.md)
</dt> <dt>

[影片媒體類型](video-media-types.md)
</dt> </dl>

 

 




