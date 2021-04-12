---
description: 音訊捕獲
ms.assetid: 2b7fbdcb-7b59-407e-8e82-e66bd5606507
title: 音訊捕獲
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e91c9063d96a5e56d078651c338b0ffd80f5aa79
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104317783"
---
# <a name="audio-capture"></a>音訊捕獲

應用程式可以透過音效卡上的輸入，使用 DirectShow 從麥克風、磁帶播放機和其他裝置捕獲音訊資料。 一般案例包括：

-   錄製 voiceover 旁白，以稍後透過影片串流進行配音。
-   將舊版類比音訊內容轉換為數字格式。
-   透過網路捕捉語音或音樂以進行傳輸。

終端使用者有數個選項可從音效卡將音訊捕獲到硬碟。 大部分的卡片都提供應用程式從其音訊輸入混合及錄製。 Windows 提供了答錄機，這是一個簡單的公用程式，可從麥克風錄製。 Windows Media 編碼器可以納入至 DirectShow 應用程式中，做為 [DirectX 媒體物件](directx-media-objects.md) (的) 。 本節說明如何使用 DirectShow 將音訊捕獲功能整合到您自己的應用程式中。

本節包含下列主題：

-   [關於音訊捕獲篩選器](about-the-audio-capture-filter.md)
-   [選取捕獲裝置](selecting-a-capture-device.md)
-   [建立音訊捕獲圖形](creating-an-audio-capture-graph.md)
-   [使用預覽建立音訊捕獲圖形](creating-an-audio-capture-graph-with-preview.md)
-   [設定音訊捕獲屬性](setting-audio-capture-properties.md)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用 DirectShow](using-directshow.md)
</dt> </dl>

 

 



