---
description: Windows Media 視訊9編碼器會編碼影片串流。
ms.assetid: 1d0a41bc-7f7c-4e25-860c-1108ab292951
title: 'WindowsMedia Video 9 編碼器 (Wmcodecdsp .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 852d3d3e7feb06cfbe9e9149fd9fd55d76ecf5abe2fbe0d6eea6ac961a0561ec
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119398238"
---
# <a name="windows-media-video-9-encoder"></a>WindowsMedia Video 9 編碼器

Windows Media 視訊9編碼器會編碼影片串流。 編碼器支援下列四種編碼輸出的類別。

-   Windows媒體 Video 9 簡單設定檔
-   Windows媒體 Video 9 主要設定檔
-   Windows媒體 Video 9 Advanced Profile
-   WindowsMedia Video 9.1 影像

## <a name="class-identifier"></a>類別識別碼

Windows Media 視訊編碼器 (clsid) 的類別識別碼是以常數 **CLSID \_ CWMV9EncMediaObject** 來表示。 您可以藉由呼叫 **CoCreateInstance** 來建立影片編碼器的實例。

## <a name="interfaces"></a>介面

影片編碼器物件會公開 [**IMediaObject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject)介面，讓物件可以作為 DirectX 媒體物件 (DMO) ，並公開 [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)介面，以便將物件當做媒體基礎轉換 (MFT) 使用。

影片編碼器會根據您取得的介面以及正在執行的 Windows 版本，以 DMO 或 MFT 的形式運作。 下表顯示影片編碼器作為 DMO 或 MFT 的行為條件。



| 作業系統            | 編碼器行為                                                                                                                                                      |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Windows XP                  | Windows 媒體影片編碼器一律會以 DMO 的方式運作。                                                                                                                |
| WindowsVista 和 Windows 7 | Windows 媒體影片編碼器預設會以 DMO 的方式運作。 如果您在影片編碼器上取得 [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) 介面，它會以 MFT 的形式運作。 |



 

## <a name="input-formats"></a>輸入格式

當 Windows Media 視訊編碼器作為 DMO 時，支援下列輸入媒體子類型。

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

下表顯示對應至編碼輸出分類 (FOURCCs) 的四個字元的代碼。



| 類別                               | FOURCC                                   |
|----------------------------------------|------------------------------------------|
| Windows媒體 Video 9 簡單設定檔   | "WMV3"                                   |
| Windows媒體 Video 9 主要設定檔     | "WMV3"                                   |
| Windows媒體 Video 9 Advanced Profile | "WVC1"                                   |
| WindowsMedia Video 9.1 影像          | "WMVP" 代表9.1，"WVP2" 代表9.1 第2版 |



 

若要區分簡單的設定檔和主要設定檔，請設定 [**MFPKEY \_ DECODERCOMPLEXITYREQUESTED**](mfpkey-decodercomplexityrequestedproperty.md) 屬性。

## <a name="properties"></a>屬性

Windows Media 視訊9編碼器支援下列屬性。



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
<td>以位元組為單位，指定用來儲存壓縮內容的容器所需的額外負荷（以位元組為單位）。<br/> <dl> WindowsXP 和更新版本。<br />
簡單設定檔、主要設定檔、Advanced Profile、Image。<br />
唯寫。<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-avgframerateproperty.md"><strong>MFPKEY_AVGFRAMERATE</strong></a></td>
<td>指定影片內容的平均畫面播放速率（以每秒畫面格數為單位）。<br/> <dl> WindowsXP 和更新版本。<br />
簡單設定檔、主要設定檔、Advanced Profile、Image。<br />
唯讀。<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-bavgproperty.md"><strong>MFPKEY_BAVG</strong></a></td>
<td>以毫秒為單位，以毫秒為單位，指定限制的變數位速率 (VBR) 資料流程的平均位元速率 (由 <a href="mfpkey-ravgproperty.md"><strong>MFPKEY_RAVG</strong></a>) 指定。<br/> <dl> WindowsXP 和更新版本。<br />
簡單設定檔、主要設定檔、Advanced Profile。<br />
讀取/寫入<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-bdeltaqpproperty.md"><strong>MFPKEY_BDELTAQP</strong></a></td>
<td>指定在錨點框架的圖片 quantizer 與 B 型框架的圖片 quantizer 之間的差異增加。<br/> <dl> WindowsXP 和更新版本。<br />
主要設定檔、Advanced Profile。<br />
唯寫。<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-bmaxproperty.md"><strong>MFPKEY_BMAX</strong></a></td>
<td>以毫秒為單位，以毫秒為單位指定受限制的變數位速率 (VBR) 資料流程的尖峰位速率 (由 <a href="mfpkey-rmaxproperty.md"><strong>MFPKEY_RMAX</strong></a>) 指定。<br/> <dl> WindowsXP 和更新版本。<br />
簡單設定檔、主要設定檔、Advanced Profile、Image。<br />
讀取/寫入<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-bufferfullnessinfirstbyteproperty.md"><strong>MFPKEY_BUFFERFULLNESSINFIRSTBYTE</strong></a></td>
<td>指定編碼的影片位資料流程是否包含每個主要畫面格的緩衝區填滿值。<br/> <dl> WindowsXP 和更新版本。<br />
簡單設定檔、主要設定檔、Advanced Profile。<br />
唯讀。<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-closedentrypointproperty.md"><strong>MFPKEY_CLOSEDENTRYPOINT</strong></a></td>
<td>指定要在一組圖片的開頭使用的編碼模式。<br/> <dl> WindowsVista 和更新版本。<br />
簡單設定檔、主要設定檔、Advanced Profile、Image。<br />
唯寫。<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-codedframesproperty.md"><strong>MFPKEY_CODEDFRAMES</strong></a></td>
<td>指定編解碼器編碼的影片框架數目。<br/> <dl> WindowsXP 和更新版本。<br />
簡單設定檔、主要設定檔、Advanced Profile。<br />
唯讀。<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-codednonzeroframesproperty.md"><strong>MFPKEY_CODEDNONZEROFRAMES</strong></a></td>
<td>指定實際包含資料之編解碼器所編碼的影片框架數目。<br/> <dl> WindowsXP 和更新版本。<br />
簡單設定檔、主要設定檔、Advanced Profile。<br />
唯讀。<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-complexityproperty.md"><strong>MFPKEY_COMPLEXITY</strong></a></td>
<td>這個屬性會由 <a href="mfpkey-complexityexproperty.md"><strong>MFPKEY_COMPLEXITYEX</strong></a>取代。<br/></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-complexityexproperty.md"><strong>MFPKEY_COMPLEXITYEX</strong></a></td>
<td>指定編碼器演算法的複雜度。<br/> <dl> WindowsVista 和更新版本。<br />
簡單設定檔，主要設定檔。 Advanced Profile。<br />
唯寫。<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-compressionoptimizationtypeproperty.md"><strong>MFPKEY_COMPRESSIONOPTIMIZATIONTYPE</strong></a></td>
<td>指定要用於 Windows Media 視訊 9 Advanced Profile 編解碼器的優化類型。<br/> <dl> WindowsXP 和更新版本。<br />
簡單設定檔、主要設定檔、Advanced Profile。<br />
寫入。<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-crispproperty.md"><strong>MFPKEY_CRISP</strong></a></td>
<td>指定在編解碼器輸出中，動作平滑與影像品質之間的取捨的數值標記法。<br/> <dl> WindowsXP 和更新版本。<br />
簡單設定檔、主要設定檔、Advanced Profile。<br />
唯寫。<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-datarateproperty.md"><strong>MFPKEY_DATARATE</strong></a></td>
<td>未使用。<br/></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-decodercomplexityprofileproperty.md"><strong>MFPKEY_DECODERCOMPLEXITYPROFILE</strong></a></td>
<td>指定編碼內容符合的裝置一致性範本。<br/> <dl> WindowsXP 和更新版本。<br />
簡單設定檔、主要設定檔、Advanced Profile、Image。<br />
唯讀。<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-decodercomplexityrequestedproperty.md"><strong>MFPKEY_DECODERCOMPLEXITYREQUESTED</strong></a></td>
<td>指定您想要用於影片編碼的裝置一致性範本。<br/> <dl> WindowsXP 和更新版本。<br />
簡單設定檔、主要設定檔、Advanced Profile。<br />
唯寫。<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-deltamvrangeindexproperty.md"><strong>MFPKEY_DELTAMVRANGEINDEX</strong></a></td>
<td>指定用來對動作向量資訊進行編碼的方法。<br/> <dl> WindowsXP 和更新版本。<br />
簡單設定檔、主要設定檔、Advanced Profile。<br />
唯寫。<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-denoiseoptionproperty.md"><strong>MFPKEY_DENOISEOPTION</strong></a></td>
<td>指定編解碼器是否會在編碼時使用雜訊篩選器。<br/> <dl> WindowsXP 和更新版本。<br />
簡單設定檔、主要設定檔、Advanced Profile。<br />
唯寫。<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-desired-vbrqualityproperty.md"><strong>MFPKEY_DESIRED_VBRQUALITY</strong></a></td>
<td>針對以品質為基礎 (1-通過) 可變位速率 (VBR) 編碼方式，指定所需的品質等級。<br/> <dl> WindowsVista 和更新版本。<br />
簡單設定檔、主要設定檔、Advanced Profile、Image。<br />
唯寫。<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-droppedframesproperty.md"><strong>MFPKEY_DROPPEDFRAMES</strong></a></td>
<td>指定編碼期間卸載的影片框架數目。<br/> <dl> WindowsXP 和更新版本。<br />
簡單設定檔、主要設定檔、Advanced Profile。<br />
唯讀。<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-endofpassproperty.md"><strong>MFPKEY_ENDOFPASS</strong></a></td>
<td>指定編碼傳遞的結尾。<br/> <dl> WindowsXP 和更新版本。<br />
簡單設定檔、主要設定檔、Advanced Profile。<br />
唯寫。<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-forceframeheightproperty.md"><strong>MFPKEY_FORCEFRAMEHEIGHT</strong></a></td>
<td>為編碼的影片指定中繼框架高度。<br/> <dl> WindowsXP 和更新版本。<br />
Advanced Profile。<br />
唯寫。<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-forceframewidthproperty.md"><strong>MFPKEY_FORCEFRAMEWIDTH</strong></a></td>
<td>指定編碼影片的中繼框架寬度。<br/> <dl> WindowsXP 和更新版本。<br />
Advanced Profile。<br />
唯寫。<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-forcemediansettingproperty.md"><strong>MFPKEY_FORCEMEDIANSETTING</strong></a></td>
<td>指定編解碼器是否應在編碼期間使用中位數篩選。<br/> <dl> WindowsXP 和更新版本。<br />
簡單設定檔、主要設定檔、Advanced Profile。<br />
唯寫。<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-fourccproperty.md"><strong>MFPKEY_FOURCC</strong></a></td>
<td>指定可識別您要使用之編碼器的 FOURCC。<br/> <dl> WindowsXP 和更新版本。<br />
簡單設定檔、主要設定檔、Advanced Profile、Image。<br />
唯寫。<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-framecountproperty.md"><strong>MFPKEY_FRAMECOUNT</strong></a></td>
<td>已過時。<br/></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-fullframerateproperty.md"><strong>MFPKEY_FULLFRAMERATE</strong></a></td>
<td>指定是否允許編碼器卸載框架。<br/> <dl> WindowsXP 和更新版本。<br />
簡單設定檔、主要設定檔、Advanced Profile、Image。<br />
唯寫。<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-interlacedcodingenabledproperty.md"><strong>MFPKEY_INTERLACEDCODINGENABLED</strong></a></td>
<td>指定是否要將編解碼器輸出交錯。<br/> <dl> WindowsXP 和更新版本。<br />
Advanced Profile。<br />
唯寫。<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-keydistproperty.md"><strong>MFPKEY_KEYDIST</strong></a></td>
<td>指定編解碼器輸出中主要畫面格之間的最長時間（以毫秒為單位）。<br/> <dl> WindowsXP 和更新版本。<br />
簡單設定檔、主要設定檔、Advanced Profile、Image。<br />
唯寫。<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-liveencodeproperty.md"><strong>MFPKEY_LIVEENCODE</strong></a></td>
<td>未使用。<br/></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-lookaheadproperty.md"><strong>MFPKEY_LOOKAHEAD</strong></a></td>
<td>指定在將目前的框架編碼之前，編解碼器將評估之目前畫面格的框架數目。<br/> <dl> WindowsXP 和更新版本。<br />
簡單設定檔、主要設定檔、Advanced Profile。<br />
唯寫。<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-loopfilterproperty.md"><strong>MFPKEY_LOOPFILTER</strong></a></td>
<td>指定編解碼器是否應在編碼期間使用 in 迴圈 deblocking 篩選。<br/> <dl> WindowsXP 和更新版本。<br />
主要設定檔、Advanced Profile。<br />
唯寫。<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-macroblockmodecostmethodproperty.md"><strong>MFPKEY_MACROBLOCKMODECOSTMETHOD</strong></a></td>
<td>指定編解碼器用來判斷要使用哪一個巨大區塊模式的成本方法。<br/> <dl> WindowsXP 和更新版本。<br />
簡單設定檔、主要設定檔、Advanced Profile。<br />
唯寫。<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-motionmatchmethodproperty.md"><strong>MFPKEY_MOTIONMATCHMETHOD</strong></a></td>
<td>指定要用於動作比對的方法。<br/> <dl> WindowsXP 和更新版本。<br />
簡單設定檔、主要設定檔、Advanced Profile。<br />
唯寫。<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-motionsearchlevelproperty.md"><strong>MFPKEY_MOTIONSEARCHLEVEL</strong></a></td>
<td>指定用於移動搜尋作業的影片資訊類型。<br/> <dl> WindowsXP 和更新版本。<br />
簡單設定檔、主要設定檔、Advanced Profile。<br />
唯寫。<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-motionsearchrangeproperty.md"><strong>MFPKEY_MOTIONSEARCHRANGE</strong></a></td>
<td>指定用於移動搜尋的範圍。<br/> <dl> WindowsXP 和更新版本。<br />
主要設定檔、Advanced Profile。<br />
唯寫。<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-noiseedgeremovalproperty.md"><strong>MFPKEY_NOISEEDGEREMOVAL</strong></a></td>
<td>指定編解碼器是否應嘗試偵測出雜訊的框架邊緣並將其移除。<br/> <dl> WindowsXP 和更新版本。<br />
簡單設定檔、主要設定檔、Advanced Profile。<br />
唯寫。<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-numbframesproperty.md"><strong>MFPKEY_NUMBFRAMES</strong></a></td>
<td>指定 (B 框架) 的雙向預測框架數目。<br/> <dl> WindowsXP 和更新版本。<br />
主要設定檔、Advanced Profile。<br />
唯寫。<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-numthreadsproperty.md"><strong>MFPKEY_NUMTHREADS</strong></a></td>
<td>指定編解碼器將用於編碼的執行緒數目。<br/> <dl> WindowsXP 和更新版本。<br />
簡單設定檔、主要設定檔、Advanced Profile。<br />
唯寫。<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-passesrecommendedproperty.md"><strong>MFPKEY_PASSESRECOMMENDED</strong></a></td>
<td>指定編解碼器所支援的最大傳遞數目。<br/> <dl> WindowsXP 和更新版本。<br />
簡單設定檔、主要設定檔、Advanced Profile、Image。<br />
唯讀。<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-passesusedproperty.md"><strong>MFPKEY_PASSESUSED</strong></a></td>
<td>指定編解碼器將用來編碼內容的傳遞數目。<br/> <dl> WindowsXP 和更新版本。<br />
簡單設定檔、主要設定檔、Advanced Profile、Image。<br />
讀取/寫入<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-perceptualoptlevelproperty.md"><strong>MFPKEY_PERCEPTUALOPTLEVEL</strong></a></td>
<td>指定編解碼器在編碼時是否應該使用保守感知優化。<br/> <dl> WindowsXP 和更新版本。<br />
主要設定檔、Advanced Profile。<br />
唯寫。<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-producedummyframesproperty.md"><strong>MFPKEY_PRODUCEDUMMYFRAMES</strong></a></td>
<td>指定編碼器是否會在位流中產生重複框架的虛擬框架專案。<br/> <dl> WindowsXP 和更新版本。<br />
簡單設定檔、主要設定檔、Advanced Profile。<br />
唯寫。<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-qpperframeproperty.md"><strong>MFPKEY_QPPERFRAME</strong></a></td>
<td>指定 QP。<br/> <dl> WindowsVista 和更新版本。<br />
簡單設定檔、主要設定檔、Advanced Profile、Image。<br />
唯寫。<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-rangereduxproperty.md"><strong>MFPKEY_RANGEREDUX</strong></a></td>
<td>指定編解碼器應減少影片有效色彩範圍的程度。<br/> <dl> WindowsXP 和更新版本。<br />
Advanced Profile。<br />
唯寫。<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-ravgproperty.md"><strong>MFPKEY_RAVG</strong></a></td>
<td>指定平均位元速率（以每秒位數為單位），用於2次傳遞變數位速率 (VBR) 編碼。<br/> <dl> WindowsXP 和更新版本。<br />
簡單設定檔、主要設定檔、Advanced Profile。<br />
讀取/寫入<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-rdsubpixelsearchproperty.md"><strong>MFPKEY_RDSUBPIXELSEARCH</strong></a></td>
<td>指定編碼器是否使用以 RD 為基礎的子圖元 MV 搜尋。 <br/> <dl> WindowsXP 和更新版本。<br />
簡單設定檔、主要設定檔、Advanced Profile、Image。<br />
唯寫。<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-reencendbuffersizeproperty.md"><strong>MFPKEY_REENCENDBUFFERSIZE</strong></a></td>
<td>若為區段重新編碼，則指定緩衝區大小。<br/> <dl> WindowsVista 和更新版本。<br />
簡單設定檔、主要設定檔、Advanced Profile、Image。<br />
唯寫。<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-reencdurationproperty.md"><strong>MFPKEY_REENCDURATION</strong></a></td>
<td>若為區段重新編碼，則指定要重新編碼之區段的持續時間。<br/> <dl> WindowsVista 和更新版本。<br />
簡單設定檔、主要設定檔、Advanced Profile、Image。<br />
唯寫。<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-reencqprefproperty.md"><strong>MFPKEY_REENCQPREF</strong></a></td>
<td>針對區段重新編碼，指定開始區段之前的框架 quantizer。<br/> <dl> WindowsVista 和更新版本。<br />
簡單設定檔、主要設定檔、Advanced Profile、Image。<br />
唯寫。<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-reencstartbuffersizeproperty.md"><strong>MFPKEY_REENCSTARTBUFFERSIZE</strong></a></td>
<td>若為區段重新編碼，則指定起始緩衝區飽和度。<br/> <dl> WindowsVista 和更新版本。<br />
簡單設定檔、主要設定檔、Advanced Profile、Image。<br />
唯寫。<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-rmaxproperty.md"><strong>MFPKEY_RMAX</strong></a></td>
<td>指定尖峰位速率（以每秒位數為單位），用於受條件約束的2傳遞變數位速率 (VBR) 。<br/> <dl> WindowsXP 和更新版本。<br />
簡單設定檔、主要設定檔、Advanced Profile。<br />
讀取/寫入<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-totalframesproperty.md"><strong>MFPKEY_TOTALFRAMES</strong></a></td>
<td>指定在編碼過程中傳遞給編碼器的影片畫面數。<br/> <dl> WindowsXP 和更新版本。<br />
簡單設定檔、主要設定檔、Advanced Profile、Image。<br />
唯讀。<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-vbrenabledproperty.md"><strong>MFPKEY_VBRENABLED</strong></a></td>
<td>指定編解碼器是否會使用變數位速率 (VBR) 編碼。<br/> <dl> WindowsXP 和更新版本。<br />
簡單設定檔、主要設定檔、Advanced Profile、Image。<br />
讀取/寫入<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-vbrqualityproperty.md"><strong>MFPKEY_VBRQUALITY</strong></a></td>
<td>指定以品質為基礎的實際品質層級 (1-傳遞) 可變位速率 (VBR) 編碼。<br/> <dl> WindowsXP 和更新版本。<br />
簡單設定檔、主要設定檔、Advanced Profile。<br />
唯寫。<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-videoscalingproperty.md"><strong>MFPKEY_VIDEOSCALING</strong></a></td>
<td>指定編解碼器是否會使用影片調整優化。<br/> <dl> WindowsXP 和更新版本。<br />
簡單設定檔、主要設定檔、Advanced Profile。<br />
唯寫。<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-videowindowproperty.md"><strong>MFPKEY_VIDEOWINDOW</strong></a></td>
<td>指定可符合模型緩衝區的內容數量（以毫秒為單位）。<br/> <dl> WindowsXP 和更新版本。<br />
Advanced Profile。<br />
唯寫。<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-volheaderforreencodeproperty.md"><strong>MFPKEY_VOLHEADERFORREENCODE</strong></a></td>
<td>若為區段重新編碼，則指定要重新編碼之檔案的編解碼器私用資料。<br/> <dl> WindowsVista 和更新版本。<br />
簡單設定檔、主要設定檔、Advanced Profile、Image。<br />
唯寫。<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-vtypeproperty.md"><strong>MFPKEY_VTYPE</strong></a></td>
<td>指定編解碼器將用來偵測交錯式來源影片的邏輯類型。<br/> <dl> WindowsXP 和更新版本。<br />
Advanced Profile。<br />
唯寫。<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-zerobyteframesproperty.md"><strong>MFPKEY_ZEROBYTEFRAMES</strong></a></td>
<td>指定已略過的影片畫面格數目，因為它們與先前的畫面格重複。<br/> <dl> WindowsXP 和更新版本。<br />
簡單設定檔、主要設定檔、Advanced Profile。<br />
唯讀<br />
</dl></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|-----------------------------------------------------------------------------------------|
| 用戶端<br/> | WindowsXP、Windows Vista 或 Windows 7<br/>                                       |
| 標頭<br/> | <dl> <dt>Wmcodecdsp。h</dt> </dl> |
| DLL<br/>    | <dl> <dt>Wmvencod.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[編解碼器物件](codecobjects.md)
</dt> <dt>

[編解碼器實行](codecimplementation.md)
</dt> </dl>

 

 
