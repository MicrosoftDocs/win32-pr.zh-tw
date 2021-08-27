---
title: 傳送個別的 MIDI 訊息
description: 傳送個別的 MIDI 訊息
ms.assetid: 9e5b7194-d6d0-40a6-b8c1-ea9442f34bd8
keywords:
- 音樂檢測數位介面 (MIDI) ，傳送訊息
- MIDI (的音樂檢測數位介面) ，傳送訊息
- 播放 MIDI 檔案，傳送訊息
- 傳送 MIDI 訊息
- 音樂檢測數位介面 (MIDI) 、個別訊息
- MIDI (音樂檢測數位介面) 、個別訊息
- 播放 MIDI 檔案，個別訊息
- 個別的 MIDI 訊息
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d1f73d0956004f90644ce2e8b0e41b368137a7b61fd04e6d17302619980336d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120037448"
---
# <a name="sending-individual-midi-messages"></a>傳送個別的 MIDI 訊息

您可以使用下列功能來處理個別的 MIDI 訊息。



| 值                                      | 意義                                                                                                                                                                             |
|--------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**midiOutLongMsg**](/windows/win32/api/mmeapi/nf-mmeapi-midioutlongmsg)   | 將 MIDI 資料的緩衝區傳送至指定的 MIDI 輸出裝置。 使用此函式可將系統專屬訊息傳送至 MIDI 裝置。                                              |
| [**midiOutReset**](/windows/win32/api/mmeapi/nf-mmeapi-midioutreset)       | 針對指定的 MIDI 輸出裝置，關閉所有通道上的所有附注。 任何擱置中的系統專屬緩衝區和資料流程緩衝區都會標示為已完成，並傳回給應用程式。 |
| [**midiOutShortMsg**](/windows/win32/api/mmeapi/nf-mmeapi-midioutshortmsg) | 將 MIDI 訊息傳送至指定的 MIDI 輸出裝置。                                                                                                                             |



 

若要傳送任何 MIDI 訊息 (除了系統專屬的訊息) 之外，請使用 [**midiOutShortMsg**](/windows/win32/api/mmeapi/nf-mmeapi-midioutshortmsg)。

 

 