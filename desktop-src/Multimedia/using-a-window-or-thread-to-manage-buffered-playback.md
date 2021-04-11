---
title: 使用視窗或執行緒管理緩衝播放
description: 使用視窗或執行緒管理緩衝播放
ms.assetid: 3c8145a8-e56a-449d-ad45-2ae016f79697
keywords:
- 音樂檢測數位介面 (MIDI) 、緩衝播放
- MIDI (的音樂檢測數位介面) ，經過緩衝的播放
- 播放 MIDI 檔案，緩衝播放
- 緩衝播放
- MM_MOM_CLOSE 訊息
- MM_MOM_DONE 訊息
- MM_MOM_OPEN 訊息
- 音樂檢測數位介面 (MIDI) ，傳送訊息
- MIDI (的音樂檢測數位介面) ，傳送訊息
- 播放 MIDI 檔案，傳送訊息
- 傳送 MIDI 訊息
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c8c120504a4a25ddcf01474db341a367a2e9854
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104315013"
---
# <a name="using-a-window-or-thread-to-manage-buffered-playback"></a>使用視窗或執行緒管理緩衝播放

下列訊息可傳送至視窗或執行緒，以管理 MIDI 系統專屬訊息或串流緩衝區的播放。



| 值                                  | 意義                                                                                                                                                                  |
|----------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**MM \_ MOM \_ 關閉**](mm-mom-close.md) | 在使用 [**midiOutClose**](/windows/win32/api/mmeapi/nf-mmeapi-midioutclose) 函式關閉裝置時傳送。                                                                               |
| [**MM \_ MOM \_ 完成**](mm-mom-done.md)   | 當設備磁碟機使用 [**midiOutLongMsg**](/windows/win32/api/mmeapi/nf-mmeapi-midioutlongmsg) 或 [**midiStreamOut**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamout) 函數傳送的資料區塊完成時傳送。 |
| [**分鐘 \_ MOM \_ 開啟**](mm-mom-open.md)   | 在使用 [**midiOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midioutopen) 函式開啟裝置時傳送。                                                                                 |



 

*WParam* 參數和 *lParam* 參數會與這些訊息相關聯。 *WParam* 參數一律會指定開啟之 MIDI 裝置的控制碼。 若是 [**\_ MOM \_ 完成**](mm-mom-done.md)， *lParam* 會指定識別已完成資料區塊之 [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) 結構的位址。 *LParam* 參數未用於 [**mm \_ mom \_ CLOSE**](mm-mom-close.md)和 [**mm \_ \_ OPEN**](mm-mom-open.md)。

最有用的訊息可能是 \_ MOM \_ 完成。 除非您需要配置記憶體或初始化變數，否則您可能不需要處理 MM \_ mom \_ OPEN 和 mm \_ mom \_ CLOSE。 當資料區塊的播放完成時，您可以清除並釋放資料區塊。

 

 