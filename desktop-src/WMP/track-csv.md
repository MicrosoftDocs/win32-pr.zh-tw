---
title: track.csv
description: track.csv
ms.assetid: 5ce782b7-5fb8-4e6e-80cb-fa1dd7c47716
keywords:
- Windows Media Player 線上商店，track.csv
- 線上商店、track.csv
- 輸入1個線上商店，track.csv
- track.csv
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9826dbcc7b553caba89b2288057b643cdb0712bf
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104301208"
---
# <a name="trackcsv"></a>track.csv

此檔案包含目錄中每個追蹤的專案。 每個專案都是由下表所述定位字元分隔欄位所組成的資料列。 欄位必須依列出的順序出現。

下表中的 Format 資料行描述每個 Unicode 文字欄位的格式化方式。 它不會參考內容的資料類型。 例如，如果 [格式] 資料行中指出了整數，則表示該欄位包含表示整數值的 Unicode 字串，而不是實際的整數。



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th>欄位</th>
<th>必要</th>
<th>格式</th>
<th>描述</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>用於 trackid</td>
<td>Yes</td>
<td>非負整數。範例：32789<br/></td>
<td>內容提供者所提供的唯一識別碼。 必須小於 2 ^ 32。效能提示：如果指派給相同專輯追蹤的識別碼連續編號，目錄壓縮將會更有效率。 但是，不需要連續的專輯曲目編號。<br/></td>
</tr>
<tr class="even">
<td>TrackTitle</td>
<td>Yes</td>
<td>Unicode 字串。 範例： Raygun Robbers 的藍色</td>
<td>資料軌的名稱。</td>
</tr>
<tr class="odd">
<td>持續時間</td>
<td>Yes</td>
<td>非負整數。範例：543<br/></td>
<td>追蹤的持續時間（以秒為單位）。</td>
</tr>
<tr class="even">
<td>TrackNumber</td>
<td>Yes</td>
<td>非負整數。範例：7<br/></td>
<td>曲目專輯上的曲目編號。 曲目編號從1開始，並在各磁片組之間增加。 曲目編號必須小於256。 大於或等於256的曲目編號會在 Windows Media Player 中造成未預期的行為。</td>
</tr>
<tr class="odd">
<td>TrackPrice</td>
<td>Yes</td>
<td>Unicode 字串。 範例： $0.99。</td>
<td>追蹤價格。 應包含貨幣符號。 空字串0和-具有特殊意義。 空字串表示價格未知。 此欄位中的零表示曲目是免費的，而連字號 (-) 表示無法購買該曲目。</td>
</tr>
<tr class="even">
<td>CanStream</td>
<td>Yes</td>
<td>布林值。 可以是0或1。範例：0<br/></td>
<td>指出是否可以串流處理此追蹤。</td>
</tr>
<tr class="odd">
<td>CanDownload</td>
<td>Yes</td>
<td>布林值。 可以是0或1。範例：0<br/></td>
<td>指出是否可以下載此追蹤。</td>
</tr>
<tr class="even">
<td>HasPreviewClip</td>
<td>Yes</td>
<td>布林值。 可以是0或1。範例：0<br/></td>
<td>指出曲目是否有預覽剪輯。</td>
</tr>
<tr class="odd">
<td>HasVideoClip</td>
<td>Yes</td>
<td>布林值。 可以是0或1。範例：0<br/></td>
<td>指出曲目是否有影片剪輯。</td>
</tr>
<tr class="even">
<td>ParentalRating</td>
<td>Yes</td>
<td>列舉。 可以是 N、E 或 C。範例： N<br/></td>
<td>指出家長諮詢評等。 N、E 和 C 的值為正常、明確和清除。</td>
</tr>
<tr class="odd">
<td>LinkedAlbumID</td>
<td>Yes</td>
<td>非負整數。 必須是專輯的識別碼。 範例：32423</td>
<td>包含此播放軌之專輯的識別碼。
<blockquote>
[!Note]<br />
每個播放軌都必須屬於一個專輯。 也就是說，針對每個追蹤，LinkedAlbumID 欄位必須等於 album.csv 檔案中的其中一個專輯識別碼。
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td>LinkedTrackArtist_ArtistIDs</td>
<td>Yes</td>
<td>整數的清單。 此清單包含演出者識別碼，並以分號分隔。 範例： 41322; 12321;82123;</td>
<td>對應于參與演出者的識別碼清單。</td>
</tr>
<tr class="odd">
<td>編輯器</td>
<td>No</td>
<td>Unicode 字串。 範例： Beethoven</td>
<td>播放軌的編輯器。如果追蹤的類型沒有設定 HasComposer 欄位，則會忽略編輯器欄位的值。 通常只用于爵士樂或傳統的曲目。</td>
</tr>
<tr class="even">
<td>熱門程度</td>
<td>Yes</td>
<td>非負整數或浮點數。範例：1252。6<br/></td>
<td>決定依熱門程度排序時，清單在清單中的位置。 較低的數位表示較熱門。</td>
</tr>
<tr class="odd">
<td>>system.starrating.average</td>
<td>No</td>
<td>Float。範例：4.21<br/></td>
<td>星級評等會先 Windows Media Player 舍入至最接近的1/4 星形，然後才會顯示在 Windows Media Player 使用者介面中。</td>
</tr>
</tbody>
</table>



 

 

 





