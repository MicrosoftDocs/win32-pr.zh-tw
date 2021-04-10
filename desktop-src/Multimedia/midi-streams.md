---
title: MIDI 串流
description: MIDI 串流
ms.assetid: 622472d9-2888-407f-bdaa-4943896c0bac
keywords:
- 音樂檢測數位介面 (MIDI) 、串流
- MIDI (音樂檢測數位介面) 、串流
- 串流緩衝區，MIDI 串流
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4237e1590f3af2e15a3b0b9fedea2fea4c9c40fc
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104092709"
---
# <a name="midi-streams"></a>MIDI 串流

Midi 事件會發生在 MIDI 資料串流的內容中。 雖然應用程式可以使用數個數據流來定義音樂資料，但 MIDI 對應工具無法辨識多個資料流程。 大部分使用串流的應用程式都使用單一的 MIDI 串流。

下列函式可用於資料流程。



| 值                                            | 意義                                                                 |
|--------------------------------------------------|-------------------------------------------------------------------------|
| [**midiStreamClose**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamclose)       | 關閉 MIDI 串流。                                                   |
| [**midiStreamOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamopen)         | 開啟 MIDI 資料流程並抓取控制碼。                             |
| [**midiStreamOut**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamout)           | 將 MIDI 資料的串流 (緩衝區) 播放或佇列至 MIDI 輸出裝置。 |
| [**midiStreamPause**](/windows/win32/api/mmeapi/nf-mmeapi-midistreampause)       | 暫停指定之 MIDI 串流的播放。                             |
| [**midiStreamPosition**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamposition) | 抓取 MIDI 串流中的目前位置。                        |
| [**midiStreamProperty**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamproperty) | 設定和捕獲資料流程屬性。                                   |
| [**midiStreamRestart**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamrestart)   | 重新開機已暫停之 MIDI 串流的播放。                              |
| [**midiStreamStop**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamstop)         | 針對指定的 MIDI 串流，關閉所有 MIDI 通道上的所有便箋。 |



 

 

 