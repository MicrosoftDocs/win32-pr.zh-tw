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
ms.openlocfilehash: d9561897fb68f53aaa4ba33e433cf6d6120ec315
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122474914"
---
# <a name="trackcsv"></a>track.csv

此檔案包含目錄中每個追蹤的專案。 每個專案都是由下表所述定位字元分隔欄位所組成的資料列。 欄位必須依列出的順序出現。

下表中的 Format 資料行描述每個 Unicode 文字欄位的格式化方式。 它不會參考內容的資料類型。 例如，如果 [格式] 資料行中指出了整數，則表示該欄位包含表示整數值的 Unicode 字串，而不是實際的整數。




| 欄位 | 必要 | 格式 | 描述 | 
|-------|----------|--------|-------------|
| 用於 trackid | 是 | 非負整數。範例：32789<br /> | 內容提供者所提供的唯一識別碼。 必須小於 2 ^ 32。效能提示：如果指派給相同專輯追蹤的識別碼連續編號，目錄壓縮將會更有效率。 但是，不需要連續的專輯曲目編號。<br /> | 
| TrackTitle | 是 | Unicode 字串。 範例： Raygun Robbers 的藍色 | 資料軌的名稱。 | 
| 持續時間 | 是 | 非負整數。範例：543<br /> | 追蹤的持續時間（以秒為單位）。 | 
| TrackNumber | 是 | 非負整數。範例：7<br /> | 曲目專輯上的曲目編號。 曲目編號從1開始，並在各磁片組之間增加。 曲目編號必須小於256。 大於或等於256的曲目編號會在 Windows Media Player 中造成未預期的行為。 | 
| TrackPrice | 是 | Unicode 字串。 範例： $0.99。 | 追蹤價格。 應包含貨幣符號。 空字串0和-具有特殊意義。 空字串表示價格未知。 此欄位中的零表示曲目是免費的，而連字號 (-) 表示無法購買該曲目。 | 
| CanStream | 是 | 布林值。 可以是0或1。範例：0<br /> | 指出是否可以串流處理此追蹤。 | 
| CanDownload | 是 | 布林值。 可以是0或1。範例：0<br /> | 指出是否可以下載此追蹤。 | 
| HasPreviewClip | 是 | 布林值。 可以是0或1。範例：0<br /> | 指出曲目是否有預覽剪輯。 | 
| HasVideoClip | 是 | 布林值。 可以是0或1。範例：0<br /> | 指出曲目是否有影片剪輯。 | 
| ParentalRating | 是 | 列舉。 可以是 N、E 或 C。範例： N<br /> | 指出家長諮詢評等。 N、E 和 C 的值為正常、明確和清除。 | 
| LinkedAlbumID | 是 | 非負整數。 必須是專輯的識別碼。 範例：32423 | 包含此播放軌之專輯的識別碼。<blockquote>[!Note]<br />每個播放軌都必須屬於一個專輯。 也就是說，針對每個追蹤，LinkedAlbumID 欄位必須等於 album.csv 檔案中的其中一個專輯識別碼。</blockquote><br /> | 
| LinkedTrackArtist_ArtistIDs | 是 | 整數的清單。 此清單包含演出者識別碼，並以分號分隔。 範例： 41322; 12321;82123; | 對應于參與演出者的識別碼清單。 | 
| 編輯器 | 否 | Unicode 字串。 範例： Beethoven | 播放軌的編輯器。如果追蹤的類型沒有設定 HasComposer 欄位，則會忽略 Composer 欄位的值。 通常只用于爵士樂或傳統的曲目。 | 
| 熱門程度 | 是 | 非負整數或浮點數。範例：1252。6<br /> | 決定依熱門程度排序時，清單在清單中的位置。 較低的數位表示較熱門。 | 
| >system.starrating.average | 否 | Float。範例：4.21<br /> | 星級評等會先 Windows Media Player 舍入至最接近的1/4 星形，然後才會顯示在 Windows Media Player 使用者介面中。 | 




 

 

 





