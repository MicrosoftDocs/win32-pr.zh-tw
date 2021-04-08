---
title: 管理 MIDI
description: 管理 MIDI
ms.assetid: ba03a2a1-d998-498d-ad53-027ba2b6e276
keywords:
- 透過驅動程式 (MIDI) 的音樂檢測數位介面
- '透過驅動程式的 MIDI (音樂檢測數位介面) '
- 透過驅動程式錄製 MIDI 音訊
- MIDI 至驅動程式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24214dd3f6cd13ca034b2555398f6055e4ce2da1
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "103933131"
---
# <a name="managing-midi-thru"></a>管理 MIDI

您可以直接將 MIDI 輸入裝置連線到 MIDI 輸出裝置，如此一來，當輸入裝置收到 [**MIM \_ 資料**](mim-data.md) 訊息時，系統就會將具有相同 MIDI 事件資料的訊息傳送至輸出裝置磁碟機。 若要將 MIDI 輸出裝置連線至 MIDI 輸入裝置，請使用 [**midiConnect**](/windows/win32/api/mmeapi/nf-mmeapi-midiconnect) 函式。

為了達到具有多個輸出的最佳效能，應用程式可以選擇提供特殊形式的 MIDI 輸出驅動程式，稱為「透過 *驅動程式*」。 雖然系統只允許一個 MIDI 輸出裝置連線至 MIDI 輸入裝置，但多個 MIDI 輸出裝置可連接到「透過」驅動程式。 這類系統上的應用程式可以透過裝置將 MIDI 輸入裝置連線到此裝置，並視需要將 MIDI 裝置連線到任意數量的 MIDI 輸出裝置。 如需有關驅動程式的詳細資訊，請參閱 Windows 裝置驅動程式檔集。

## <a name="using-messages-to-manage-midi-recording"></a>使用訊息來管理 MIDI 記錄

下列訊息可以傳送至視窗或執行緒回呼程式，以管理 MIDI 錄製。



| 值                                          | 意義                                                                                                                                |
|------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| [**MM \_ MIM \_ 關閉**](mm-mim-close.md)         | 在使用 [**midiInClose**](/windows/win32/api/mmeapi/nf-mmeapi-midiinclose) 函式關閉 MIDI 輸入裝置時傳送。                                      |
| [**MM \_ MIM \_ 資料**](mm-mim-data.md)           | 收到完整的 MIDI 訊息時傳送。  (此訊息適用于除系統專屬訊息以外的所有 MIDI 訊息。 )           |
| [**MM \_ MIM \_ 錯誤**](mm-mim-error.md)         | 收到不正確 MIDI 訊息時傳送。  (此訊息適用于除系統專屬訊息以外的所有 MIDI 訊息。 )           |
| [**MM \_ MIM \_ LONGDATA**](mm-mim-longdata.md)   | 當收到完整的 MIDI 系統專屬訊息或緩衝區已填滿系統專屬資料時傳送。     |
| [**MM \_ MIM \_ LONGERROR**](mm-mim-longerror.md) | 收到不正確 MIDI 系統專屬訊息時傳送。                                                                        |
| [**MM \_ MIM \_ MOREDATA**](mm-mim-moredata.md)   | 當應用程式處理 [**MIM \_ 資料**](mim-data.md) 訊息的速度不夠快，無法跟上輸入裝置磁碟機時傳送。 |
| [**MM \_ MIM \_ 開啟**](mm-mim-open.md)           | 在使用 [**midiInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midiinopen) 函式開啟 MIDI 輸入裝置時傳送。                                        |



 

*WParam* 參數和 *lParam* 參數會與這些訊息相關聯。 *WParam* 參數一律會指定開啟之 MIDI 裝置的控制碼。 *LParam* 參數未針對 [**MM \_ mim \_ CLOSE**](mm-mim-close.md)和 [**mm \_ mim \_ OPEN**](mm-mim-open.md)訊息使用。

針對 [**MM \_ MIM \_ LONGDATA**](mm-mim-longdata.md) 訊息， *lpMidiHdr* 會指定 [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) 結構的位址，以識別系統專屬訊息的緩衝區。 緩衝區可能不會完全填滿，因為系統專屬訊息的大小通常在記錄之前不是已知的，而且必須配置大小總計可以包含最大預期訊息的緩衝區。 若要判斷存在於緩衝區中的有效資料量，請使用 **MIDIHDR** 結構的 **dwBytesRecorded** 成員。

## <a name="using-a-callback-function-to-manage-midi-recording"></a>使用回呼函式來管理 MIDI 記錄

您可以定義自己的回呼函式來管理 MIDI 輸入裝置的錄製。 回呼函數記載為 [**MidiInProc**](/previous-versions//dd798460(v=vs.85))。

下列訊息可以傳送至 **MidiInProc** 回呼函數的 *wMsg* 參數。



| 值                                   | 意義                                                                                                                                |
|-----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| [**MIM \_ 關閉**](mim-close.md)         | 在使用 [**midiInClose**](/windows/win32/api/mmeapi/nf-mmeapi-midiinclose) 函式關閉裝置時傳送。                                               |
| [**MIM \_ 資料**](mim-data.md)           | 收到完整的 MIDI 訊息時傳送 (此訊息會用於所有的 MIDI 訊息，但系統專屬的訊息) 除外。           |
| [**MIM \_ 錯誤**](mim-error.md)         | 收到不正確 MIDI 訊息時傳送 (此訊息會用於所有的 MIDI 訊息，但系統專屬的訊息) 除外。           |
| [**MIM \_ LONGDATA**](mim-longdata.md)   | 當收到完整的 MIDI 系統專屬訊息或緩衝區已填滿系統專屬資料時傳送。     |
| [**MIM \_ LONGERROR**](mim-longerror.md) | 收到不正確 MIDI 系統專屬訊息時傳送。                                                                        |
| [**MIM \_ MOREDATA**](mim-moredata.md)   | 當應用程式處理 [**MIM \_ 資料**](mim-data.md) 訊息的速度不夠快，無法跟上輸入裝置磁碟機時傳送。 |
| [**MIM \_ 開啟**](mim-open.md)           | 在使用 [**midiInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midiinopen) 函式開啟 MIDI 輸入裝置時傳送。                                      |



 

這些訊息類似于傳送至視窗程式函式的訊息，但參數不同。 開啟之 MIDI 裝置的控制碼會以參數形式傳遞給回呼函式，以及使用 **midiInOpen** 傳遞的實例資料的雙字。

針對 [**MIM \_ LONGDATA**](mim-longdata.md) 訊息， *lpMidiHdr* 會指定 [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) 結構的位址，以識別系統專屬訊息的緩衝區。 緩衝區可能不會完全填滿。 若要判斷存在於緩衝區中的有效資料量，請使用 **MIDIHDR** 結構的 **dwBytesRecorded** 成員。

使用資料區塊完成設備磁碟機之後，您可以清除並釋放資料區塊。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[錄製 MIDI 音訊](recording-midi-audio.md)
</dt> </dl>

 

 