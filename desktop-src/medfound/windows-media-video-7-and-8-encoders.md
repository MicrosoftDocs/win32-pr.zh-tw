---
description: Windows Media 視訊7/8 編碼器會實施舊版的 Windows Media 視訊編碼器。
ms.assetid: c4165614-b9ec-4216-b36c-f57bc05e3a8e
title: 'Windows Media 視訊7/8 編碼器 (Wmcodecdsp .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be5467d02681ef319a508f6f6581e1f3c0191950
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999708"
---
# <a name="windows-media-video-78-encoder"></a>Windows Media 視訊7/8 編碼器

Windows Media 視訊7/8 編碼器會實施舊版的 Windows Media 視訊編碼器。

## <a name="class-identifier"></a>類別識別碼

Windows Media 視訊7/8 編碼器 (CLSID) 的類別識別碼是 **clsid \_ CWMVXEncMediaObject**。 您可以藉由呼叫 **CoCreateInstance** 來建立編碼器的實例。

## <a name="interfaces"></a>介面

影片編碼器物件會公開 [**IMediaObject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject) 介面，讓物件可以作為 DirectX 媒體物件 (的) ，並公開 [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) 介面，讓物件可以作為媒體基礎的轉換 (MFT) 。

影片編碼器會根據您取得的介面和執行的 Windows 版本，以一或一種方式來運作。 下表顯示影片編碼器以 SQL-DMO 或 MFT 作為的條件。



| 作業系統            | 編碼器行為                                                                                                                                                      |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Windows XP                  | Windows Media video 編碼器一律會以一種方式運作。                                                                                                                |
| Windows Vista 和 Windows 7 | Windows Media 影片編碼器預設會以一種方式運作。 如果您在影片編碼器上取得 [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) 介面，它會以 MFT 的形式運作。 |



 

## <a name="input-formats"></a>輸入格式

當 Windows Media 視訊編碼器作為一種時，支援下列輸入媒體子類型。

-   MEDIASUBTYPE \_ IYUV
-   MEDIASUBTYPE \_ I420
-   MEDIASUBTYPE \_ YV12
-   MEDIASUBTYPE \_ NV11
-   MEDIASUBTYPE \_ NV12
-   MEDIASUBTYPE \_ YUY2
-   MEDIASUBTYPE \_ UYVY
-   MEDIASUBTYPE \_ YVYU
-   MEDIASUBTYPE \_ RGB32
-   MEDIASUBTYPE \_ RGB24
-   MEDIASUBTYPE \_ RGB565
-   MEDIASUBTYPE \_ RGB555
-   MEDIASUBTYPE \_ RGB8
-   MEDIASUBTYPE \_ PHOTOMOTION

當 Windows Media 視訊編碼器作為 MFT 時，支援下列輸入媒體子類型。

-   MFVideoFormat \_ IYUV
-   MFVideoFormat \_ I420
-   MFVideoFormat \_ YV12
-   MFVideoFormat \_ NV11
-   MFVideoFormat \_ NV12
-   MFVideoFormat \_ YUY2
-   MFVideoFormat \_ UYVY
-   MFVideoFormat \_ YVYU
-   MFVideoFormat \_ RGB32
-   MFVideoFormat \_ RGB24
-   MFVideoFormat \_ RGB565
-   MFVideoFormat \_ RGB555
-   MFVideoFormat \_ RGB8
-   MEDIASUBTYPE \_ PHOTOMOTION

## <a name="output-formats"></a>輸出格式

下錶針對 Windows Media 視訊7/8 編碼器所支援的輸出類型，顯示四個字元的代碼 (FOURCCs) 。



| 類別              | FOURCC |
|-----------------------|--------|
| Windows Media 視訊7 | "WMV1" |
| Windows Media 視訊8 | "WMV2" |



 

## <a name="properties"></a>屬性

Windows Media 視訊7/8 編碼器支援下列屬性。



<table>
<thead>
<tr class="header">
<th>屬性</th>
<th>描述</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="mfpkey-asfoverheadperframeproperty.md"><strong>MFPKEY_ASFOVERHEADPERFRAME</strong></a></td>
<td>以位元組為單位，指定用來儲存壓縮內容的容器所需的額外負荷（以位元組為單位）。<br/> <dl> Windows XP （含）以後版本。<br />
唯寫。<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-avgframerateproperty.md"><strong>MFPKEY_AVGFRAMERATE</strong></a></td>
<td>指定影片內容的平均畫面播放速率（以每秒畫面格數為單位）。<br/> <dl> Windows XP （含）以後版本。<br />
唯讀。<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-bavgproperty.md"><strong>MFPKEY_BAVG</strong></a></td>
<td>以毫秒為單位，以毫秒為單位，指定限制的變數位速率 (VBR) 資料流程的平均位元速率 (由 <a href="mfpkey-ravgproperty.md"><strong>MFPKEY_RAVG</strong></a>) 指定。<br/> <dl> Windows XP （含）以後版本。<br />
讀取/寫入<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-bmaxproperty.md"><strong>MFPKEY_BMAX</strong></a></td>
<td>以毫秒為單位，以毫秒為單位指定受限制的變數位速率 (VBR) 資料流程的尖峰位速率 (由 <a href="mfpkey-rmaxproperty.md"><strong>MFPKEY_RMAX</strong></a>) 指定。<br/> <dl> Windows XP （含）以後版本。<br />
讀取/寫入<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-bufferfullnessinfirstbyteproperty.md"><strong>MFPKEY_BUFFERFULLNESSINFIRSTBYTE</strong></a></td>
<td>指定編碼的影片位資料流程是否包含每個主要畫面格的緩衝區填滿值。<br/> <dl> Windows XP （含）以後版本。<br />
唯讀。<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-codedframesproperty.md"><strong>MFPKEY_CODEDFRAMES</strong></a></td>
<td>指定編解碼器編碼的影片框架數目。<br/> <dl> Windows XP （含）以後版本。<br />
唯讀。<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-codednonzeroframesproperty.md"><strong>MFPKEY_CODEDNONZEROFRAMES</strong></a></td>
<td>指定實際包含資料之編解碼器所編碼的影片框架數目。<br/> <dl> Windows XP （含）以後版本。<br />
唯讀。<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-complexityproperty.md"><strong>MFPKEY_COMPLEXITY</strong></a></td>
<td>這個屬性會由 <a href="mfpkey-complexityexproperty.md"><strong>MFPKEY_COMPLEXITYEX</strong></a>取代。<br/></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-complexityexproperty.md"><strong>MFPKEY_COMPLEXITYEX</strong></a></td>
<td>指定編碼器演算法的複雜度。<br/> <dl> Windows Vista （含）以後版本。<br />
唯寫。<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-crispproperty.md"><strong>MFPKEY_CRISP</strong></a></td>
<td>指定在編解碼器輸出中，動作平滑與影像品質之間的取捨的數值標記法。<br/> <dl> Windows XP （含）以後版本。<br />
唯寫。<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-decodercomplexityprofileproperty.md"><strong>MFPKEY_DECODERCOMPLEXITYPROFILE</strong></a></td>
<td>指定編碼內容符合的裝置一致性範本。<br/> <dl> Windows XP （含）以後版本。<br />
唯讀。<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-decodercomplexityrequestedproperty.md"><strong>MFPKEY_DECODERCOMPLEXITYREQUESTED</strong></a></td>
<td>指定您想要用於影片編碼的裝置一致性範本。<br/> <dl> Windows XP （含）以後版本。<br />
唯寫。<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-droppedframesproperty.md"><strong>MFPKEY_DROPPEDFRAMES</strong></a></td>
<td>指定編碼期間卸載的影片框架數目。<br/> <dl> Windows XP （含）以後版本。<br />
唯讀。<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-endofpassproperty.md"><strong>MFPKEY_ENDOFPASS</strong></a></td>
<td>指定編碼傳遞的結尾。<br/> <dl> Windows XP （含）以後版本。<br />
唯寫。<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-fourccproperty.md"><strong>MFPKEY_FOURCC</strong></a></td>
<td>指定可識別您要使用之編碼器的 FOURCC。<br/> <dl> Windows XP （含）以後版本。<br />
唯寫。<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-interlacedcodingenabledproperty.md"><strong>MFPKEY_INTERLACEDCODINGENABLED</strong></a></td>
<td>指定是否要將編解碼器輸出交錯。<br/> <dl> Windows XP （含）以後版本。<br />
唯寫。<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-keydistproperty.md"><strong>MFPKEY_KEYDIST</strong></a></td>
<td>指定編解碼器輸出中主要畫面格之間的最長時間（以毫秒為單位）。<br/> <dl> Windows XP （含）以後版本。<br />
唯寫。<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-passesrecommendedproperty.md"><strong>MFPKEY_PASSESRECOMMENDED</strong></a></td>
<td>指定編解碼器所支援的最大傳遞數目。<br/> <dl> Windows XP （含）以後版本。<br />
唯讀。<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-passesusedproperty.md"><strong>MFPKEY_PASSESUSED</strong></a></td>
<td>指定編解碼器將用來編碼內容的傳遞數目。<br/> <dl> Windows XP （含）以後版本。<br />
讀取/寫入<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-producedummyframesproperty.md"><strong>MFPKEY_PRODUCEDUMMYFRAMES</strong></a></td>
<td>指定編碼器是否會在位流中產生重複框架的虛擬框架專案。<br/> <dl> Windows XP （含）以後版本。<br />
唯寫。<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-qpperframeproperty.md"><strong>MFPKEY_QPPERFRAME</strong></a></td>
<td>指定 QP。<br/> <dl> Windows Vista （含）以後版本。<br />
唯寫。<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-ravgproperty.md"><strong>MFPKEY_RAVG</strong></a></td>
<td>指定平均位元速率（以每秒位數為單位），用於2次傳遞變數位速率 (VBR) 編碼。<br/> <dl> Windows XP （含）以後版本。<br />
讀取/寫入<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-rmaxproperty.md"><strong>MFPKEY_RMAX</strong></a></td>
<td>指定尖峰位速率（以每秒位數為單位），用於受條件約束的2傳遞變數位速率 (VBR) 。<br/> <dl> Windows XP （含）以後版本。<br />
讀取/寫入<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-totalframesproperty.md"><strong>MFPKEY_TOTALFRAMES</strong></a></td>
<td>指定在編碼過程中傳遞給編碼器的影片畫面數。<br/> <dl> Windows XP （含）以後版本。<br />
唯讀。<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-vbrenabledproperty.md"><strong>MFPKEY_VBRENABLED</strong></a></td>
<td>指定編解碼器是否會使用變數位速率 (VBR) 編碼。<br/> <dl> Windows XP （含）以後版本。<br />
讀取/寫入<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-vbrqualityproperty.md"><strong>MFPKEY_VBRQUALITY</strong></a></td>
<td>指定以品質為基礎的實際品質層級 (1-傳遞) 可變位速率 (VBR) 編碼。<br/> <dl> Windows XP （含）以後版本。<br />
唯寫。<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-videowindowproperty.md"><strong>MFPKEY_VIDEOWINDOW</strong></a></td>
<td>指定可符合模型緩衝區的內容數量（以毫秒為單位）。<br/> <dl> Windows XP （含）以後版本。<br />
唯寫。<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-zerobyteframesproperty.md"><strong>MFPKEY_ZEROBYTEFRAMES</strong></a></td>
<td>指定已略過的影片畫面格數目，因為它們與先前的畫面格重複。<br/> <dl> Windows XP （含）以後版本。<br />
唯讀<br />
</dl></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|-----------------------------------------------------------------------------------------|
| 用戶端<br/> | Windows XP、Windows Vista 或 Windows 7<br/>                                       |
| 標頭<br/> | <dl> <dt>Wmcodecdsp。h</dt> </dl> |
| DLL<br/>    | <dl> <dt>Wmvxencd.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[編解碼器物件](codecobjects.md)
</dt> <dt>

[編解碼器實行](codecimplementation.md)
</dt> <dt>

[影片子類型 Guid](video-subtype-guids.md)
</dt> </dl>

 

 
