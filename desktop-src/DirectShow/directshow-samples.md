---
description: DirectShow樣品
ms.assetid: 4166d5ca-5e02-49f6-bcb1-d448f8175a0c
title: DirectShow樣品
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb99271821fcef80b66b379b29bd42de0505011fd47c8dfee208e6f00b007208
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117821163"
---
# <a name="directshow-samples"></a>DirectShow樣品

DirectShow 範例包含在[Windows SDK](https://msdn.microsoft.com/windows/aa904949.aspx)中。 它們位於 path \[ SDK 根 \] \\ 範例 \\ 多媒體 \\ DirectShow 下。

下表列出 Windows SDK 中提供的所有 DirectShow 範例。 如需有關如何建立範例的指示，請參閱 Windows SDK 中提供的檔。

如果有其他範例檔，此資料表的第一個資料行會與其連結。



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th>範例</th>
<th>區域</th>
<th>描述</th>
<th>其他相依性</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="directshow-base-classes.md">DirectShow基類</a></td>
<td>基礎類別庫</td>
<td>設計用來執行 DirectShow 篩選準則的 c + + 類別和公用程式函式。</td>

</tr>
<tr class="even">
<td><a href="amcap-sample.md">AmCap 範例</a></td>
<td>擷取</td>
<td>影片捕獲應用程式。</td>
<td>strmbase .lib</td>
</tr>
<tr class="odd">
<td><a href="dvapp-sample.md">DVApp 範例</a></td>
<td>擷取</td>
<td>數位視訊 (DV) capture 應用程式。</td>

</tr>
<tr class="even">
<td><a href="playcap-sample.md">PlayCap 範例</a></td>
<td>擷取</td>
<td>簡易 capture 應用程式。</td>

</tr>
<tr class="odd">
<td><a href="dmo-demo-sample.md">DMO示範範例</a></td>
<td>DMO</td>
<td>透過音訊效果 DMO 將音訊資料從 WAV 檔案串流處理。</td>
<td>DirectX SDK</td>
</tr>
<tr class="even">
<td>DVD 範例</td>
<td>DVD</td>
<td>示範基本的 DVD 播放和流覽，加上先進的功能，例如家長監護管理、書簽、卡拉卡拉和命令同步處理。</td>

</tr>
<tr class="odd">
<td><a href="inftee-filter-sample.md">InfTee 篩選範例</a></td>
<td>篩選準則，其他</td>
<td><a href="infinite-pin-tee-filter.md">無限圖釘指標</a>篩選的範例執行。</td>
<td>strmbase .lib</td>
</tr>
<tr class="even">
<td><a href="metronome-filter-sample.md">Metronome 篩選範例</a></td>
<td>篩選準則，其他</td>
<td>顯示如何執行參考時鐘。</td>
<td>strmbase .lib</td>
</tr>
<tr class="odd">
<td><a href="psi-parser-filter-sample.md">PSI 剖析器篩選範例</a></td>
<td>篩選準則，其他</td>
<td>從 MPEG-2 傳輸串流接收 (PSI) 資料表的程式特定資訊，並解壓縮程式資訊。</td>
<td>strmbase .lib</td>
</tr>
<tr class="even">
<td><a href="dump-filter-sample.md">傾印篩選範例</a></td>
<td>篩選器，轉譯器</td>
<td>寫入媒體範例接收到文字檔。</td>
<td>strmbase .lib</td>
</tr>
<tr class="odd">
<td>SampVid 篩選</td>
<td>篩選器，轉譯器</td>
<td>影片轉譯器篩選。</td>
<td>strmbase .lib</td>
</tr>
<tr class="even">
<td><a href="scope-filter-sample.md">範圍篩選範例</a></td>
<td>篩選器，轉譯器</td>
<td>以 wave 形式顯示音效資料。</td>
<td>strmbase .lib</td>
</tr>
<tr class="odd">
<td><a href="async-filter-sample.md">非同步篩選範例</a></td>
<td>篩選準則，來源</td>
<td>支援漸進式下載的檔案讀取器篩選。</td>
<td>strmbase .lib</td>
</tr>
<tr class="even">
<td><a href="ball-filter-sample.md">球形濾波器範例</a></td>
<td>篩選準則，來源</td>
<td>產生彈跳球影像的影片來源篩選器。</td>
<td>strmbase .lib</td>
</tr>
<tr class="odd">
<td><a href="push-source-filters-sample.md">推送來源篩選範例</a></td>
<td>篩選準則，來源</td>
<td>提供下列資料做為影片資料流程的來源篩選：單一點陣圖、一組點陣圖、目前桌面映射的複本。</td>
<td>strmbase .lib</td>
</tr>
<tr class="even">
<td><a href="synth-filter-sample.md">合成濾波器範例</a></td>
<td>篩選準則，來源</td>
<td>產生音訊波形的來源篩選。 此範例示範動態圖形建築物。</td>
<td>strmbase .lib</td>
</tr>
<tr class="odd">
<td><a href="ezrgb24-filter-sample.md">EZRGB24 篩選範例</a></td>
<td>篩選準則，轉換</td>
<td>影像處理篩選。</td>
<td>strmbase .lib</td>
</tr>
<tr class="even">
<td><a href="gargle-filter-sample.md">Gargle 篩選範例</a></td>
<td>篩選準則，轉換</td>
<td>音訊效果篩選。</td>
<td>strmbase .lib</td>
</tr>
<tr class="odd">
<td><a href="wavdest-filter-sample.md">WavDest 篩選範例</a></td>
<td>篩選準則，轉換</td>
<td>將音訊串流寫入至 WAV 檔案。</td>
<td>strmbase .lib</td>
</tr>
<tr class="even">
<td><a href="dmoenum-sample.md">DMOEnum 範例</a></td>
<td>其他</td>
<td>說明如何 (DMOs) 列舉 <a href="directx-media-objects.md">DirectX 媒體物件</a> 。</td>

</tr>
<tr class="odd">
<td><a href="mapper-sample.md">對應工具範例</a></td>
<td>其他</td>
<td>顯示如何使用 <a href="filter-mapper.md">篩選器</a> 對應程式在登錄中尋找篩選。</td>

</tr>
<tr class="even">
<td>SysEnum 範例</td>
<td>其他</td>
<td>示範如何使用 <a href="system-device-enumerator.md">系統裝置</a> 列舉值來列舉裝置和篩選器。</td>

</tr>
<tr class="odd">
<td><a href="cutscene-sample.md">CutScene 範例</a></td>
<td>播放</td>
<td>以全螢幕模式播放影片檔案。</td>

</tr>
<tr class="even">
<td>DDrawXCL 範例</td>
<td>播放</td>
<td>使用覆迭<a href="overlay-mixer-filter.md">Mixer</a>篩選上的<a href="/windows/desktop/api/Strmif/nn-strmif-iddrawexclmodevideo"><strong>IDDrawExclModeVideo</strong></a>介面，在 DirectDraw 專屬全螢幕模式下播放影片。</td>

</tr>
<tr class="odd">
<td>DShowPlayer 範例</td>
<td>播放</td>
<td>影片播放應用程式。</td>

</tr>
<tr class="even">
<td>EVRPlayer 範例</td>
<td>播放</td>
<td>示範如何使用 DirectShow EVR 篩選。
<blockquote>
[!Note]<br />
需要 Windows Vista 或更新版本。
</blockquote>
<br/> <br/> 此範例可在 Windows Server 2008 或更新版本的 Windows SDK 中取得。<br/></td>
<td>strmbase .lib</td>
</tr>
<tr class="odd">
<td>Texture3D9 範例</td>
<td>播放</td>
<td>在 Microsoft DirectX 9.0 材質表面上繪製影片。</td>
<td>strmbase .lib、DirectX SDK</td>
</tr>
<tr class="even">
<td><a href="ticker-sample.md">報價範例</a></td>
<td>VMR-9</td>
<td>使用 VMR-9 來 blend 影片和文字。</td>

</tr>
<tr class="odd">
<td>VMR9Allocator 範例</td>
<td>VMR-9</td>
<td>VMR-9 的自訂配置器提供者。</td>
<td>strmbase .lib</td>
</tr>
<tr class="even">
<td>VMR9Compositor 範例</td>
<td>VMR-9</td>
<td>實 VMR-9 的自訂混音器。</td>

</tr>
<tr class="odd">
<td><a href="vmrplayer-sample.md">VMRPlayer 範例</a></td>
<td>VMR-9</td>
<td>使用 VMR-9 來 blend 一或兩個執行中的影片和靜態影像。</td>

</tr>
<tr class="even">
<td>水位線範例</td>
<td>VMR-9</td>
<td>使用 VMR-9，在播放期間將靜態點陣圖混合到影片。</td>

</tr>
<tr class="odd">
<td><a href="windowless-sample.md">無視窗範例</a></td>
<td>VMR-9</td>
<td>示範 VMR-9 的無視窗模式。</td>

</tr>
</tbody>
</table>



 

## <a name="additional-dependencies"></a>其他相依性

部分範例會連結到 DirectShow 基類庫。 若要建立這些範例，您必須先建立基類庫。 如需詳細資訊，請參閱[DirectShow 基類](directshow-base-classes.md)。 所有範例篩選都需要基底類別庫。

除了 Windows SDK 之外，一些範例也需要 DirectX SDK。 若要建立這些範例，您必須安裝 DirectX SDK，並將% DXSDK \_ DIR% 環境變數設為等於 DIRECTX SDK 安裝路徑。

許多 DirectShow 範例都會使用一組常見的標頭和原始程式檔（位於 directrory \[ SDK 根 \] \\ 範例 \\ 多媒體 \\ DirectShow） \\ 。 如果您將範例資料夾複製到另一個目錄，請務必同時複製 [一般] 資料夾。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[設定組建環境](setting-up-the-build-environment.md)
</dt> </dl>

 

 




