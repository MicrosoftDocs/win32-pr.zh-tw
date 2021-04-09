---
title: 音訊資料區塊
description: 音訊資料區塊
ms.assetid: 9646e18c-294b-4532-bd5e-709d66ad31f4
keywords:
- 多媒體音訊，資料區塊
- 音訊、資料區塊
- 波形音訊、資料區塊
- 音訊資料區塊，關於
- WAVEHDR 結構
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8a81a5a29ec9718e7c11306b6bafc1aa20369e5
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "103933125"
---
# <a name="audio-data-blocks"></a>音訊資料區塊

[**WaveInAddBuffer**](/windows/win32/api/mmeapi/nf-mmeapi-waveinaddbuffer)和 [**waveOutWrite**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutwrite)函式需要應用程式佈建資料區塊，以傳遞至設備磁碟機以供錄製或播放之用。 這兩個函數都會使用 [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) 結構來描述其資料區塊。

使用這些函式的其中一個來將資料區塊傳遞給設備磁碟機之前，您必須為數據區塊和描述資料區塊的標頭結構配置記憶體。 您可以使用下列功能來備妥和取消準備標頭。



| 函式                                                 | 描述                                                      |
|----------------------------------------------------------|------------------------------------------------------------------|
| [**waveInPrepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-waveinprepareheader)       | 準備波形-音訊輸入資料區塊。                      |
| [**waveInUnprepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-waveinunprepareheader)   | 清除波形音訊輸入資料區塊的準備工作。  |
| [**waveOutPrepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutprepareheader)     | 準備波形音訊輸出資料區塊。                     |
| [**waveOutUnprepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutunprepareheader) | 清除波形音訊輸出資料區塊的準備工作。 |



 

將音訊資料區塊傳遞到設備磁碟機之前，您必須先將資料區塊傳遞給 [**waveInPrepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-waveinprepareheader) 或 [**waveOutPrepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutprepareheader)，以準備資料區塊。 當設備磁碟機完成資料區塊並傳回它時，您必須先將資料區塊傳遞至 [**waveInUnprepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-waveinunprepareheader) 或 [**waveOutUnprepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutunprepareheader) ，然後再釋放任何配置的記憶體，以清除此準備工作。

除非波形-音訊輸入和輸出資料小到足以包含在單一資料區塊中，否則應用程式必須持續提供設備磁碟機與資料區塊，直到播放或錄製完成為止。

即使使用單一資料區塊，應用程式也必須能夠判斷設備磁碟機何時完成資料區塊，讓應用程式可以釋放與資料區塊和標頭結構相關聯的記憶體。 有幾種方式可判斷設備磁碟機何時完成資料區塊：

-   藉由指定回呼函式，以在使用資料區塊完成時接收驅動程式所傳送的訊息
-   使用事件回呼
-   藉由指定視窗或執行緒，以接收驅動程式完成使用資料區塊時所傳送的訊息
-   藉由 \_ 在每個資料區塊所傳送之 [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr)結構的 **DWFLAGS** 成員中輪詢 WHDR 完成位

如果應用程式在需要時無法取得設備磁碟機的資料區塊，則播放可能會有可能出現的間隙或遺失傳入記錄的資訊。 這至少需要雙重緩衝配置，至少要在設備磁碟機之前保持至少一個資料區塊。

下列主題描述使用資料區塊完成設備磁碟機的判斷方式：

使用回呼函式來處理驅動程式訊息

-   [使用回呼函式來處理驅動程式訊息](using-a-callback-function-to-process-driver-messages.md)
-   [使用事件回呼處理驅動程式訊息](using-an-callback-to-process-driver-messages.md)
-   [使用視窗或執行緒驅動程式訊息](using-a-window-or-thread-to-process-driver-messages.md)
-   [藉由輪詢管理資料區塊](managing-data-blocks-by-polling.md)

 

 