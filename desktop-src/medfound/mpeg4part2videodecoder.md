---
description: MPEG4 Part 2 影片解碼會將根據 MPEG4 第2部分標準編碼的影片串流進行編碼。
ms.assetid: 56e32d3c-9bd0-41fe-bb22-e4ff37b7cc5c
title: 'MPEG-2 第2部影片解碼 (Wmcodecdsp .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 847e5be8c506e534c42962ecf6b0037a2ecb2f184c9c47fa92981fa32fd55422
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118973017"
---
# <a name="mpeg-4-part-2-video-decoder"></a>MPEG 4 第2部分影片解碼

MPEG4 Part 2 影片解碼會將根據 MPEG4 第2部分標準編碼的影片串流進行編碼。

您可以藉由呼叫 **CoCreateInstance** 來建立 MPEG4 Part 2 Video 解碼的實例。 若要建立 (DMO) 的 DirectX 媒體物件行為的解碼器實例，請使用類別識別碼 **CLSID \_ CMpeg4sDecMediaObject**。 若要建立媒體基礎轉換 (MFT) 的解碼器實例，請使用類別識別碼 **CLSID \_ CMpeg4sDecMFT**。

## <a name="input-types"></a>輸入類型

MPEG4 Part 2 影片解碼支援下列輸入媒體類型。

-   MEDIASUBTYPE \_ M4S2
-   MEDIASUBTYPE \_ m4s2
-   MEDIASUBTYPE \_ MP4V
-   MEDIASUBTYPE \_ mp4v
-   MEDIASUBTYPE \_ mp4 (已淘汰) 
-   MEDIASUBTYPE \_ mp4 (已淘汰) 

## <a name="output-types"></a>輸出型別

MPEG4 Part 2 影片解碼可在作為 DMO 時，支援下列輸出媒體子類型。

-   MEDIASUBTYPE \_ YV12
-   MEDIASUBTYPE \_ NV12
-   MEDIASUBTYPE \_ YUY2
-   MEDIASUBTYPE \_ UYVY
-   MEDIASUBTYPE \_ YVYU
-   MEDIASUBTYPE \_ NV11
-   MEDIASUBTYPE \_ RGB32
-   MEDIASUBTYPE \_ RGB24
-   MEDIASUBTYPE \_ RGB565
-   MEDIASUBTYPE \_ RGB555
-   MEDIASUBTYPE \_ RGB8

MPEG4 Part 2 影片解碼可支援下列輸出媒體子類型作為 MFT。

-   MEDIASUBTYPE \_ NV12
-   MEDIASUBTYPE \_ YV12

## <a name="formats"></a>格式

MPEG4 Part 2 影片解碼接受下列格式。

-   [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader)
-   [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) (VIH2) 
-   [**MFVideoInfo**](/windows/desktop/api/mfobjects/ns-mfobjects-mfvideoinfo)
-   [**MPEG2VIDEOINFO**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo) (只會使用標頭的 VIH2 部分。 ) 

## <a name="interfaces-for-the-dmo"></a>DMO 的介面

如果您將 MPEG4 Part 2 影片解碼的實例建立為 DMO，則此解碼器會公開下列介面。

-   [**IMediaObject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject)
-   [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi)

您可以藉由呼叫 **CoCreateInstance** 來取得 [**IMediaObject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject)介面，也可以藉由呼叫 **QueryInterface** 來取得 [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi)介面。

## <a name="interfaces-for-the-mft"></a>適用于 MFT 的介面

如果您建立了 MPEG2 第2部分影片解碼器的實例作為 MFT，則此解碼器會公開下列介面。

-   [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)
-   [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes)
-   [**IMFQualityAdvise**](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise)
-   [**IMFQualityAdvise2**](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise2)
-   [**IMFRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol)
-   [**IMFRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport)

您可以藉由呼叫 **CoCreateInstance** 來取得 [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)介面的指標，也可以藉由呼叫 [**IMFTransform：： GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes)取得 [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes)介面的指標。 您可以藉由呼叫 MFT 上的 **QueryInterface** 來取得 [**IMFQualityAdvise**](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise)或 [**IMFQualityAdvise2**](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise2)介面的指標。 您可以藉由呼叫 [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice)並傳遞服務識別碼 **MF \_ 速率 \_ 控制 \_ 服務**，來取得 [**IMFRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol)或 [**IMFRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport)介面的指標。

## <a name="profiles-and-levels"></a>設定檔和層級

MPEG4 規格會定義數個設定檔，其中每個設定檔都會指定編碼器可用來產生編碼資料流程的工具。 MPEG4 第2部分 Video 解碼支援下列兩個設定檔：簡單的視覺化設定檔和 Advanced Simple Profile。 換句話說，MPEG4 Part 2 影片解碼可將根據簡單視覺化設定檔或 Advanced Simple Profile 編碼的資料流程解碼。

簡單的視覺效果設定檔支援漸進式模式下低位速率影片的基本傳輸。 它僅支援內部和預測圖片。 它也支援簡短的標頭模式，它可回溯相容于 .H 基準設定檔。 從 Windows 10 開始，MPEG 4 第2部分影片解碼器也支援支援自訂圖片大小的 263v2 (.h +) 。

先進的簡單設定檔支援簡單的視覺效果設定檔的所有工具，此外也支援交錯式影片、B 框架、季-pel 運動補償、額外的量化資料表，以及全球動作補償。

MPEG4 規格也會定義數個層級，其中每個層級都會針對編碼器所產生的輸出資料流程指定條件約束。

下表顯示 MPEG4 第2部分影片解碼所支援的設定檔和層級，以及一般的解決方案。



| 設定檔         | 層級 | 一般解決方式 |
|-----------------|-------|--------------------|
| 簡單視覺效果   | 0     | 176 x 144          |
| 簡單視覺效果   | 1     | 176 x 144          |
| 簡單視覺效果   | 2     | 352 x 288          |
| 簡單視覺效果   | 3     | 352 x 288          |
| SimpleVisual    | 4a    | 640 x 480          |
| 簡單視覺效果   | 5     | 720 x 576          |
| Advanced Simple | 0     | 176 x 144          |
| Advanced Simple | 1     | 176 x 144          |
| Advanced Simple | 2     | 352 x 288          |
| Advanced Simple | 3     | 352 x 288          |
| Advanced Simple | 3b    | 352 x 288          |
| Advanced Simple | 4     | 352 x 756          |
| Advanced Simple | 5     | 720 x 576          |



 

如需設定檔和層級的詳細資訊，請參閱 MPEG4 第2部分規格 (ISO/IEC 14496-2) ：資訊技術--音訊-視覺化物件的編碼--第2部分：視覺效果。

## <a name="decoder-properties"></a>解碼器屬性

若要設定 MPEG4 第2部分影片解碼器上的屬性，請使用 [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) 介面或 [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) 介面。

MPEG4 Part 2 影片解碼支援下列屬性。



<table>
<thead>
<tr class="header">
<th>屬性</th>
<th>描述</th>
<th>預設值</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/DirectShow/avdecvideoswpowerlevel-property"><strong>CODECAPI_AVDecVideoSWPowerLevel</strong></a></td>
<td>指定電源等級。<br/> <dl> Windows 7。<br />
唯寫。<br />
</dl></td>
<td>100</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/DirectShow/avdecvideothumbnailgenerationmode-property"><strong>CODECAPI_AVDecVideoThumbnailGenerationMode</strong></a></td>
<td>指定縮圖產生模式。<br/> <dl> Windows 7。<br />
唯寫。<br />
</dl></td>
<td><strong>VARIANT_FALSE</strong></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a>備註

針對 RGB 媒體子類型 (guid) 的全域唯一識別碼，會隨著解碼器是否做為 DMO 或 MFT 而有所不同。 非 RGB 媒體子類型的 guid 是相同的，不論解碼器是否做為 DMO 或 MFT。 如需表示媒體子類型之 Guid 的詳細資訊，請參閱 [媒體類型](media-types.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅 Windows 7 \[ 桌面應用程式\]<br/>                                              |
| 最低支援的伺服器<br/> | Windows僅限 Server 2008 R2 \[ desktop 應用程式\]<br/>                                 |
| 標頭<br/>                   | <dl> <dt>Wmcodecdsp。h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MP4SDecd.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[編解碼器物件](codecobjects.md)
</dt> </dl>

 

 
