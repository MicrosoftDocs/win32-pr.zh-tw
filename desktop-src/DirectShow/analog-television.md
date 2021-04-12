---
description: 類比電視
ms.assetid: 9f2c18ec-3684-42a8-a3df-5f8827b27642
title: 類比電視
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33af8ba94831afed59d783598dbf6bc0eaee0ec6
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104109001"
---
# <a name="analog-television"></a>類比電視

類比電視與其他影片捕獲案例有數種不同之處：

-   調諧器卡會調整為類比信號，然後進行數位化。
-   音訊會攜帶在類比信號中。 音訊觸達音效卡的方式，會隨著硬體而異。
-   信號可能會以垂直空白間隔包含額外的資料 (VBI) ，例如隱藏式輔助字幕 (副本) 、World Standard Teletext (WST) 和外延資料服務 (XDS) 。

下圖顯示電視 preview 的一般篩選圖形。

![類比電視圖](images/vidcap06.png)

-   [電視調諧器](tv-tuner-filter.md)篩選器會控制微調。
-   [電視音訊](tv-audio-filter.md)篩選器會控制音訊解碼。
-   如果調諧器卡有一個以上的實體輸入，則 [類比視頻縱橫](analog-video-crossbar-filter.md) 條篩選器可讓應用程式選取已解碼和轉譯的輸入。
-   [WDM 影片捕獲](wdm-video-capture-filter.md)篩選器會傳遞數位化的影片串流。

「捕獲圖形產生器」會自動從「捕捉」篩選器中插入任何需要上游的篩選。

本節包含下列主題：

-   [類比電視微調](analog-television-tuning.md)
-   [類比電視音訊](analog-television-audio.md)
-   [隱藏式輔助字幕和 Teletext](closed-captions-and-teletext.md)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[影片捕獲](video-capture.md)
</dt> </dl>

 

 



