---
title: 使用回呼函式來管理緩衝的播放
description: 使用回呼函式來管理緩衝的播放
ms.assetid: aaaf9c5f-c9b2-4e55-a4c1-28c99cc03945
keywords:
- 音樂檢測數位介面 (MIDI) 、緩衝播放
- MIDI (的音樂檢測數位介面) ，經過緩衝的播放
- 播放 MIDI 檔案，緩衝播放
- 緩衝播放
- MOM_CLOSE 訊息
- MOM_DONE 訊息
- MOM_OPEN 訊息
- 音樂檢測數位介面 (MIDI) ，傳送訊息
- MIDI (的音樂檢測數位介面) ，傳送訊息
- 播放 MIDI 檔案，傳送訊息
- 傳送 MIDI 訊息
- 音樂檢測數位介面 (MIDI) 、回呼函式
- MIDI (音樂檢測數位介面) 、回呼函式
- 播放 MIDI 檔案，回呼函數
- MidiOutProc 回呼函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bccccd8e5fb052b89e8ca1804b89de6da26cd5b7
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "103682106"
---
# <a name="using-a-callback-function-to-manage-buffered-playback"></a>使用回呼函式來管理緩衝的播放

您可以定義自己的回呼函式，以管理已緩衝播放的 MIDI 輸出裝置。 回呼函數記載為 [**MidiOutProc**](/previous-versions//dd798478(v=vs.85))。

下列訊息可以傳送至 **MidiOutProc** 回呼函數的 *wMsg* 參數。



| 值                           | 意義                                                                                                                                                                  |
|---------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**MOM \_ 關閉**](mom-close.md) | 在使用 [**midiOutClose**](/windows/win32/api/mmeapi/nf-mmeapi-midioutclose) 函式關閉裝置時傳送。                                                                               |
| [**MOM \_ 完成**](mom-done.md)   | 當設備磁碟機使用 [**midiOutLongMsg**](/windows/win32/api/mmeapi/nf-mmeapi-midioutlongmsg) 或 [**midiStreamOut**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamout) 函數傳送的資料區塊完成時傳送。 |
| [**MOM \_ OPEN**](mom-open.md)   | 在使用 [**midiOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midioutopen) 函式開啟裝置時傳送。                                                                                 |



 

這些訊息類似于傳送至視窗程式函式的訊息，但參數不同。 開啟之 MIDI 裝置的控制碼會以參數形式傳遞給回呼函式，以及使用 **midiOutOpen** 傳遞的實例資料的雙量。

使用資料區塊完成驅動程式之後，您可以清除並釋放資料區塊。 因為回呼函式有建議的限制，所以最好不要從回呼函式內進行。

 

 