---
title: 使用 PlaySound 來播放系統音效
description: 使用 PlaySound 來播放系統音效
ms.assetid: b645c488-8b76-4886-8909-75f0342263db
keywords:
- 波形音訊，PlaySound 函式
- 波形音訊，播放系統音效
- 波形音訊、音效事件
- PlaySound 函式，播放系統音效
- PlaySound 函式，音效事件
- 播放波形-音訊系統音效
- 音效活動
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf9978e9e33c049db82a033b2379ac9f52b5e2959fd9d8425deac180ba7a81e4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119804568"
---
# <a name="using-playsound-to-play-system-sounds"></a>使用 PlaySound 來播放系統音效

[**PlaySound**](/previous-versions//dd743680(v=vs.85))函式也會播放登錄中的 keyname 所參考的聲音。 使用者可以將自己的音效指派給系統警示和警告，或指派給使用者動作，例如按一下滑鼠按鍵。 與系統警示和警告相關的音效稱為「 *音效事件*」。

若要播放音效事件，請呼叫 **PlaySound** ，並將 *pszSound* 參數指向包含可識別音效之登錄專案名稱的字串。 例如，若要播放與 "MouseClick" 專案相關的音效，並等候音效完成後再返回，請使用下列語句：


```C++
PlaySound("MouseClick", NULL, SND_SYNC); 
```



如果指定的登錄專案或其識別的波形音訊檔案不存在，或檔案無法放入可用的記憶體中， **PlaySound** 會播放預設的系統音效。

系統預先定義的音效事件可能會因平臺而異。 下列清單提供針對 WIN32 API 的所有執行所定義的音效事件：

-   SystemAsterisk
-   SystemExclamation
-   發生 systemexit 時
-   SystemHand
-   SystemQuestion
-   SystemStart

如果應用程式註冊自己的音效事件，則使用者可以使用標準主控台介面設定音效事件。 應用程式應該使用標準登錄函式來註冊音效事件;如需詳細資訊，請參閱 [Registry](../sysinfo/registry.md)。 專案與其余的音效事件位於登錄階層中的相同位置。 這個位置會隨著 Win32 的執行而不同。 適當的資料值也會隨著執行而有所不同。

在嘗試載入具有這個名稱的檔案之前， [**sndPlaySound**](/previous-versions//dd798676(v=vs.85)) 函式一律會在登錄中搜尋符合 *lpszSound* 的 keyname。 [**PlaySound**](/previous-versions//dd743680(v=vs.85))函式會接受指定音效位置的旗標。

 

 