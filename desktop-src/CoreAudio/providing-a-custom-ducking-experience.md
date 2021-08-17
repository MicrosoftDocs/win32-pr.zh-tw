---
description: 應用程式可以選擇不使用系統所處理的預設回避體驗，並將其取代為自訂的執行。
ms.assetid: 18290d05-b114-476b-8365-6bbb5fe6cffc
title: 提供自訂回避行為
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72cf4bb254b97a6a9d6b5c9d415d48a2c95f528f20efbf2ffbe4782ae5980400
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118406366"
---
# <a name="providing-a-custom-ducking-behavior"></a>提供自訂回避行為

應用程式可以選擇不使用系統所處理的 [預設回避體驗](stream-attenuation.md) ，並將其取代為自訂的執行。

應用程式可以提供自訂的回避體驗。 例如，Windows Media Player 藉由在通訊會話期間暫停目前的媒體串流，並在會話關閉時繼續播放，來提供自己的回避體驗。 Windows SDK 範例中包含了可實回避的範例媒體應用程式;如需詳細資訊，請參閱[DuckingMediaPlayer](duckingmediaplayer.md)。 若要模擬開啟和關閉通訊資料流程的體驗，以及產生回避事件，請參閱[DuckingCaptureSample](duckingcapturesample.md)，其中也包含 Windows SDK 範例中。

播放衰減音效的媒體應用程式，必須留意到在系統中開啟和關閉的通訊資料流程。 您可以使用 MediaFoundation、DirectShow 或 DirectSound （使用核心音訊 api）來提供自訂執行。 直接 WASAPI 用戶端也可以覆寫通訊會話開始和結束時的預設處理。

**若要提供自訂的回避體驗，WASAPI 用戶端必須執行下列工作：**

1.  註冊以接收來自 *回避 manager* 的回避事件，此為音訊系統的元件，可處理與通訊流變更相關的通知。 如需詳細資訊，請 [取得回避事件](handling-audio-ducking-events-from-communication-devices.md)。
    > [!Note]  
    > 如果用戶端已註冊接收回避通知，則回避管理員會停用系統所提供的預設行為。 如果停用預設行為明確 (請參閱 [停用預設回避體驗](disabling-the-ducking-experience.md)) 而用戶端未提供替代行為，則應用程式不會遇到任何回避行為。

     

2.  接聽回避管理員所傳送的「操作事件」通知，並執行所需的回避行為。 如需有關如何執行回避行為的詳細資訊，請參閱 [回避通知的執行考慮](handling-audio-ducking-events-from-communication-devices.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用通訊裝置](using-the-communication-device.md)
</dt> <dt>

[預設回避體驗](stream-attenuation.md)
</dt> <dt>

[停用預設的回避體驗](disabling-the-ducking-experience.md)
</dt> <dt>

[回避通知的執行考慮](handling-audio-ducking-events-from-communication-devices.md)
</dt> <dt>

[取得回避事件](getting-ducking-events-from-a-communication-device.md)
</dt> </dl>

 

 



