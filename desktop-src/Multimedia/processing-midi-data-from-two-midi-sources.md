---
title: 處理來自兩個 MIDI 來源的 MIDI 資料
description: 處理來自兩個 MIDI 來源的 MIDI 資料
ms.assetid: d8b605d9-a12a-4830-8f29-ea700aefb41d
keywords:
- Windows 多媒體，處理來自兩個來源的 MIDI 資料
- 多媒體，處理來自兩個來源的 MIDI 資料
- 多媒體音訊，處理來自兩個來源的 MIDI 資料
- 音訊，處理來自兩個來源的 MIDI 資料
- 音樂檢測數位介面 (MIDI) ，處理來自兩個來源的資料
- MIDI (的音樂檢測數位介面) ，處理來自兩個來源的資料
- 處理來自兩個來源的 MIDI 資料
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 513dcd16036f6f833aec6813f75c6c082925f666
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104023410"
---
# <a name="processing-midi-data-from-two-midi-sources"></a>處理來自兩個 MIDI 來源的 MIDI 資料

MIDI 子系統可以將來自兩個數據源的 MIDI 訊息路由傳送到單一的 MIDI 輸出裝置，以供並行播放。 例如，一個來源可以是背景音樂，或是已預先錄製並儲存在檔案中的低音線。 第二個來源可以是來自 MIDI 檢測的即時資料，例如鍵盤或吉他。

這兩個數據源都會將 MIDI 資料傳送給以一個控制碼識別的單一 MIDI 裝置。 使用 [**midiStreamOut**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamout) 函數和一或多個資料流程緩衝區來傳送一個資料流程。 此資料流程通常包含封裝至緩衝區的預錄資料。

使用 [**midiOutShortMsg**](/windows/win32/api/mmeapi/nf-mmeapi-midioutshortmsg) 函式，以非同步方式將第二個數據流 (從 MIDI 檢測) 。 資料流程緩衝區的執行中狀態不會受到第二個數據流所進行之非同步呼叫的不良影響。

使用 **midiOutShortMsg** 傳送的每個簡短訊息都必須是完整的 MIDI 訊息，其中包含狀態位元組和適當的資料位元組數目。 如果省略狀態位元組， **midiOutShortMsg** 會傳回錯誤。  (不過，沒有資料流程輸出的執行中狀態。 ) 

 

 