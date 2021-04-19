---
description: MPEG 範例屬性
ms.assetid: 339aab84-e5ad-4071-8b67-2b04cb17e450
title: MPEG 範例屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c20df4b9285a77d00bd98bc6f21558f0d6b3c60
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106966616"
---
# <a name="mpeg-sample-properties"></a>MPEG 範例屬性

MPEG 範例具有下列特性。

**時間戳記**

並非所有範例都有開始和停止時間。 封包和承載資料的範例停止時間並不實用;通常會設定為開始時間加1。 如果產生的系統層封包具有有效的時間點，則 MPEG 封包或承載資料範例將會設定開始和停止時間。

如需時間戳記的詳細資訊，請參閱2.4.1 的 >ISO1-11172：「封包標頭可能包含解碼和/或呈現時間戳記 (DTS 和 PT) 參考封包中的第一個存取單位」。

針對 MPEG \_ 資料流程主要類型，開始時間是第一個位元組的位元組位置，以每秒1個位元組分級。 停止時間是最後一個位元組的位元組位置。 因此，連續的範例應該要有第一個封包的停止時間等於下一個封包的開始時間。 針對視訊 CD 資料，媒體的原點必須符合 CDFS.SYS 所公開之影片 CD 檔案的格式，且開頭必須有標準 RIFF 組塊。

針對 MPEG video 封包和裝載類型，時間戳記是第一個影片框架的呈現時間，其圖片開始程式碼會在範例中開始。

針對 MPEG 音訊封包和裝載類型，時間戳記是在範例中開始其同步程式碼的第一個音訊框架的呈現時間。

假設處理篩選器可以成功 prerolled 沒有時間戳記的封包和內容資料。

**間斷**

如果資料流程中有中斷 (例如，即時資料中的間隙，或是資料中或搜尋) 之後的錯誤，則會在下一個媒體範例上設定 [中斷] 屬性。 這也允許時間戳記不連續。

**資料流程結束通知**

當解碼器收到此通知時，它必須處理任何緩衝的資料。 任何新的資料都必須以不連續的屬性開頭。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[DirectShow 中的 MPEG 2 支援](mpeg-2-support-in-directshow.md)
</dt> </dl>

 

 



