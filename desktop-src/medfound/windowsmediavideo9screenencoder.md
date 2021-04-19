---
description: Windows Media 視訊9螢幕編碼器最適合用來從電腦監視器編碼連續螢幕擷取畫面。
ms.assetid: 22faebf8-40c0-47f9-b66b-c0a8b5ba7202
title: 'Windows Media 視訊9螢幕編碼器 (Wmcodecdsp .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5e0729a7b8ef09ad9b86b07e6668a933a307550
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106979534"
---
# <a name="windows-media-video-9-screen-encoder"></a>Windows Media 視訊9螢幕編碼器

Windows Media 視訊9螢幕編碼器最適合用來從電腦監視器編碼連續螢幕擷取畫面。

## <a name="class-identifier"></a>類別識別碼

Windows Media 視訊9螢幕編碼器 (CLSID) 的類別識別碼是以常數 **CLSID \_ CMSSCEncMediaObject2** 來表示。 您可以藉由呼叫 **CoCreateInstance** 來建立編碼器的實例。

## <a name="input-types"></a>輸入類型

第9版螢幕編碼程式支援下列輸入類型，當它用來作為 DirectX 媒體物件時 (的) 。

-   MEDIASUBTYPE \_ RGB24
-   MEDIASUBTYPE \_ RGB32
-   MEDIASUBTYPE \_ ARGB32
-   MEDIASUBTYPE \_ RGB565
-   MEDIASUBTYPE \_ RGB555
-   MEDIASUBTYPE \_ RGB8

當第9版的螢幕編碼器作為媒體基礎轉換 (MFT) 時，支援下列輸入類型。

-   MFVideoFormat \_ RGB24
-   MFVideoFormat \_ RGB32
-   MFVideoFormat \_ ARGB32
-   MFVideoFormat \_ RGB565
-   MFVideoFormat \_ RGB555
-   MFVideoFormat \_ RGB8

## <a name="output-types"></a>輸出型別

適用于 Windows Media 視訊螢幕第9版編碼內容的四個字元的程式碼 (FOURCC) 為 "MSS2"。

第9版螢幕編碼器支援下列輸出類型。

-   MEDIASUBTYPE \_ MSS2

## <a name="encoder-properties"></a>編碼器屬性

Windows Media 視訊9螢幕編碼器支援下列屬性。



<table>
<thead>
<tr class="header">
<th>屬性</th>
<th>描述</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="mfpkey-asfoverheadperframeproperty.md">MFPKEY_ASFOVERHEADPERFRAME</a></td>
<td>以位元組為單位，指定用來儲存壓縮內容之容器所需的額外負荷（以位元組為單位）。<br/> <dl> Windows XP （含）以後版本。<br />
唯寫。<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-bavgproperty.md">MFPKEY_BAVG</a></td>
<td>以毫秒為單位，以毫秒為單位，指定限制的變數位速率 (VBR) 資料流程的平均位元速率 (由 <a href="mfpkey-ravgproperty.md">MFPKEY_RAVG</a>) 指定。<br/> <dl> Windows XP （含）以後版本。<br />
讀取/寫入<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-bmaxproperty.md">MFPKEY_BMAX</a></td>
<td>以毫秒為單位，以毫秒為單位指定受限制的變數位速率 (VBR) 資料流程的尖峰位速率 (由 <a href="mfpkey-rmaxproperty.md">MFPKEY_RMAX</a>) 指定。<br/> <dl> Windows XP （含）以後版本。<br />
讀取/寫入<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-bufferfullnessinfirstbyteproperty.md">MFPKEY_BUFFERFULLNESSINFIRSTBYTE</a></td>
<td>指定編碼的影片位資料流程是否包含每個主要畫面格的緩衝區填滿值。<br/> <dl> Windows XP （含）以後版本。<br />
唯讀。<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-codedframesproperty.md">MFPKEY_CODEDFRAMES</a></td>
<td>指定編解碼器編碼的影片框架數目。<br/> <dl> Windows XP （含）以後版本。<br />
唯讀。<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-codednonzeroframesproperty.md">MFPKEY_CODEDNONZEROFRAMES</a></td>
<td>指定實際包含資料之編解碼器所編碼的影片框架數目。<br/> <dl> Windows XP （含）以後版本。<br />
唯讀。<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-complexityproperty.md">MFPKEY_COMPLEXITY</a></td>
<td>這個屬性會由 <a href="mfpkey-complexityexproperty.md">MFPKEY_COMPLEXITYEX</a>取代。<br/></td>
</tr>
<tr class="even">
<td><a href="mfpkey-complexityexproperty.md">MFPKEY_COMPLEXITYEX</a></td>
<td>指定編碼器演算法的複雜度。<br/> <dl> Windows Vista （含）以後版本。<br />
唯寫。<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-crispproperty.md">MFPKEY_CRISP</a></td>
<td>指定在編解碼器輸出中，動作平滑與影像品質之間的取捨的數值標記法。<br/> <dl> Windows XP （含）以後版本。<br />
唯寫。<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-droppedframesproperty.md">MFPKEY_DROPPEDFRAMES</a></td>
<td>指定編碼期間卸載的影片框架數目。<br/> <dl> Windows XP （含）以後版本。<br />
唯讀。<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-endofpassproperty.md">MFPKEY_ENDOFPASS</a></td>
<td>指定編碼傳遞的結尾。<br/> <dl> Windows XP （含）以後版本。<br />
唯寫。<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-fourccproperty.md">MFPKEY_FOURCC</a></td>
<td>指定可識別您要使用之編碼器的 FOURCC。<br/> <dl> Windows XP （含）以後版本。<br />
唯寫。<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-keydistproperty.md">MFPKEY_KEYDIST</a></td>
<td>指定編解碼器輸出中主要畫面格之間的最長時間（以毫秒為單位）。<br/> <dl> Windows XP （含）以後版本。<br />
唯寫。<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-liveencodeproperty.md">MFPKEY_LIVEENCODE</a></td>
<td>已過時。<br/></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-passesrecommendedproperty.md">MFPKEY_PASSESRECOMMENDED</a></td>
<td>指定編解碼器所支援的最大傳遞數目。<br/> <dl> Windows XP （含）以後版本。<br />
唯讀。<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-passesusedproperty.md">MFPKEY_PASSESUSED</a></td>
<td>Windows XP （含）以後版本。 讀取/寫入<br/> 指定編解碼器將用來編碼內容的傳遞數目。<br/> <dl> Windows XP （含）以後版本。<br />
讀取/寫入<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-qpperframeproperty.md">MFPKEY_QPPERFRAME</a></td>
<td>指定 QP。 可能的值為1.0 到31.0。<br/> <dl> Windows Vista （含）以後版本。<br />
唯寫。<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-ravgproperty.md">MFPKEY_RAVG</a></td>
<td>指定平均位元速率（以每秒位數為單位），用於2次傳遞變數位速率 (VBR) 編碼。<br/> <dl> Windows XP （含）以後版本。<br />
讀取/寫入<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-rmaxproperty.md">MFPKEY_RMAX</a></td>
<td>指定尖峰位速率（以每秒位數為單位），用於受條件約束的2傳遞變數位速率 (VBR) 編碼。<br/> <dl> Windows XP （含）以後版本。<br />
讀取/寫入<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-totalframesproperty.md">MFPKEY_TOTALFRAMES</a></td>
<td>指定在編碼過程中傳遞給編碼器的影片畫面數。<br/> <dl> Windows XP （含）以後版本。<br />
唯讀。<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-vbrenabledproperty.md">MFPKEY_VBRENABLED</a></td>
<td>指定編解碼器是否會使用變數位速率 (VBR) 編碼。<br/> <dl> Windows XP （含）以後版本。<br />
讀取/寫入<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-vbrqualityproperty.md">MFPKEY_VBRQUALITY</a></td>
<td>指定以品質為基礎的實際品質層級 (1-傳遞) 可變位速率 (VBR) 編碼。<br/> <dl> Windows XP （含）以後版本。<br />
唯寫。<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-videowindowproperty.md">MFPKEY_VIDEOWINDOW</a></td>
<td>可符合模型緩衝區的內容數量（以毫秒為單位）。<br/> <dl> Windows XP 及更新版本，<br />
唯寫。<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-zerobyteframesproperty.md">MFPKEY_ZEROBYTEFRAMES</a></td>
<td>指定已略過的影片畫面格數目，因為它們與先前的畫面格重複。<br/> <dl> Windows XP （含）以後版本。<br />
唯讀。<br />
</dl></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a>備註

螢幕編碼器物件會公開 **IMediaObject** 介面，讓物件可以作為 DirectX 媒體物件 (的) ，並公開 **IMFTransform** 介面，讓物件可以作為媒體基礎的轉換 (MFT) 。

螢幕編碼器會根據您取得的介面和執行的 Windows 版本，以一或一種方式來運作。 下表所顯示的條件如下：螢幕編碼器的行為。



| 作業系統            | 編碼器行為                                                                                                                                    |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| Windows XP                  | Windows Media Screen 編碼器一律會以一種方式運作。                                                                                             |
| Windows Vista 和 Windows 7 | Windows Media Screen 編碼器預設會以一種方式運作。 如果您在螢幕編碼器上取得 **IMFTransform** 介面，它會以 MFT 的形式運作。 |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|-----------------------------------------------------------------------------------------|
| 用戶端<br/> | Windows XP、Windows Vista 或 Windows 7<br/>                                       |
| 標頭<br/> | <dl> <dt>Wmcodecdsp。h</dt> </dl> |
| DLL<br/>    | <dl> <dt>Wmvsencd.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[編解碼器物件](codecobjects.md)
</dt> <dt>

[編解碼器實行](codecimplementation.md)
</dt> <dt>

[使用 Windows Media 視訊9螢幕編解碼器](usingthewindowsmediavideo9screencodec.md)
</dt> <dt>

[Windows Media 視訊9螢幕解碼](windowsmediavideo9screendecoder.md)
</dt> </dl>

 

 




