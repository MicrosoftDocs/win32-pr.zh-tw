---
title: 管理 MIDI 資料區塊
description: 管理 MIDI 資料區塊
ms.assetid: f29fbc08-ef67-489c-aedf-5a2bc65233f7
keywords:
- " (MIDI) 的音樂檢測數位介面，管理資料區塊"
- MIDI (的音樂檢測數位介面) ，管理資料區塊
- MIDI 服務，管理資料區塊
- 管理 MIDI 資料區塊
- 音樂檢測數位介面 (MIDI) ，處理驅動程式訊息
- MIDI (的音樂檢測數位介面) ，處理驅動程式訊息
- MIDI 服務，處理驅動程式訊息
- 處理驅動程式訊息
- 音樂檢測數位介面 (MIDI) 、資料區塊
- MIDI (音樂檢測數位介面) 、資料區塊
- MIDI 服務，資料區塊
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 846c7391fedbcdc4f14934ed73ae9a47de675f435b9b2bd1fb63e97c340d5182
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118139147"
---
# <a name="managing-midi-data-blocks"></a>管理 MIDI 資料區塊

使用資料區塊傳遞系統專屬訊息的應用程式 (使用 [**midiOutLongMsg**](/windows/win32/api/mmeapi/nf-mmeapi-midioutlongmsg) 和 [**midiInAddBuffer**](/windows/win32/api/mmeapi/nf-mmeapi-midiinaddbuffer) 函式) 和串流緩衝區 (使用 [**midiStreamOut**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamout) 函式) 必須持續提供設備磁碟機與資料區塊，直到播放或錄製完成為止。

即使使用了單一資料區塊，應用程式也必須能夠判斷設備磁碟機何時完成資料區塊，讓它可以釋放與資料區塊和標頭結構相關聯的記憶體。 有三種方法可用來判斷設備磁碟機何時完成資料區塊：

-   指定回呼函式，以在使用資料區塊完成時，接收驅動程式所傳送的訊息。 若要取得時間戳記的 MIDI 輸入資料，您必須使用回呼函數。
-   使用事件回呼 (僅適用于輸出) 。
-   使用視窗或執行緒回呼來接收驅動程式完成資料區塊時所傳送的訊息。

如果應用程式在需要時無法取得設備磁碟機的資料區塊，則可能會發生播放或遺失傳入記錄資訊。 應用程式至少應該使用雙重緩衝配置，以在設備磁碟機之前至少保留一個資料區塊。

## <a name="using-a-callback-function-to-process-driver-messages"></a>使用回呼函式來處理驅動程式訊息

您可以撰寫自己的回呼函式來處理設備磁碟機所傳送的訊息。 若要使用回呼函式，請在 \_ *dwFlags* 參數中指定回呼函式旗標，並在 [**midiInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midiinopen)或 [**midiOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midioutopen)函數的 *dwCallback* 參數中指定回呼函數的位址。

傳送至回呼函式的訊息類似于傳送至視窗的訊息，但它們有兩個雙字參數，而不是不帶正負號的整數參數和雙量參數。 如需這些訊息的詳細資訊，請參閱傳送 [System-Exclusive 訊息](sending-system-exclusive-messages.md) 和 [管理 MIDI 記錄](managing-midi-recording.md)。

您可以使用下列其中一種技術，將實例資料從應用程式傳遞至回呼函數：

-   使用函式的 *dwCallbackInstance* 參數來開啟設備磁碟機。
-   使用 [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr)結構的 **dwUser** 成員，識別要傳送至 MIDI 設備磁碟機的資料區塊。

如果您需要超過32位的實例資料，請傳遞包含額外資訊的結構位址。

## <a name="using-an-event-callback-to-process-driver-messages"></a>使用事件回呼處理驅動程式訊息

若要使用事件回呼，請使用 [CreateEvent](/windows/win32/api/synchapi/nf-synchapi-createeventa) 函數來取出事件的控制碼，並 \_ 在 [**midiOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midioutopen) 函式的呼叫中指定回呼事件。

事件回呼是由任何可能導致函式回呼的專案所設定。 與回呼函數和視窗或執行緒回呼不同的是，事件回呼不會收到特定的關閉、完成或開啟通知。 因此，在事件發生之後，應用程式可能必須檢查正在等候的進程狀態。

如需事件回呼的詳細資訊，請參閱 [使用事件回呼來管理緩衝的播放](using-an-callback-to-manage-buffered-playback.md)。

## <a name="using-a-window-or-thread-callback-to-process-driver-messages"></a>使用視窗或執行緒回呼處理驅動程式訊息

若要使用視窗回呼，請在 \_ *dwFlags* 參數中指定回呼視窗旗標，並在 [**midiInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midiinopen)或 [**midiOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midioutopen)函式之 *dwCallback* 參數的低序位單字中指定視窗控制碼。 驅動程式訊息將會傳送至 *dwCallback* 中的控制碼所識別之視窗的視窗程式函式。

同樣地，若要使用執行緒回呼，請 \_ 在 **MidiInOpen** 或 **midiOutOpen** 的呼叫中指定回呼執行緒旗標和執行緒識別碼。 在此情況下，訊息將會張貼到指定的執行緒，而不是傳送至視窗。

傳送至視窗或執行緒回呼的訊息是使用的 MIDI 裝置專用的。 如需這些訊息的詳細資訊，請參閱傳送 [System-Exclusive 訊息](sending-system-exclusive-messages.md) 和 [管理 MIDI 記錄](managing-midi-recording.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[MIDI 服務](midi-services.md)
</dt> </dl>

 

 