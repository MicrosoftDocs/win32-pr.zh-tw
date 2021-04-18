---
title: 配置和準備 MIDI 資料區塊
description: 配置和準備 MIDI 資料區塊
ms.assetid: b3a70441-e8f9-4886-bf22-426ebd74d045
keywords:
- " (MIDI) 的音樂檢測數位介面，配置資料區塊"
- MIDI (的音樂檢測數位介面) ，配置資料區塊
- MIDI 服務，配置資料區塊
- 配置 MIDI 資料區塊
- 音樂檢測數位介面 (MIDI) ，準備資料區塊
- MIDI (的音樂檢測數位介面) ，準備資料區塊
- MIDI 服務，準備資料區塊
- 準備 MIDI 資料區塊
- 音樂檢測數位介面 (MIDI) 、資料區塊
- MIDI (音樂檢測數位介面) 、資料區塊
- MIDI 服務，資料區塊
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48b23a72dfd46035a3d23743faa7228e5fe85aaf
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "106965843"
---
# <a name="allocating-and-preparing-midi-data-blocks"></a>配置和準備 MIDI 資料區塊

[**MidiOutLongMsg**](/windows/win32/api/mmeapi/nf-mmeapi-midioutlongmsg)、 [**midiInAddBuffer**](/windows/win32/api/mmeapi/nf-mmeapi-midiinaddbuffer)和 [**midiStreamOut**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamout)函式需要應用程式佈建資料區塊，以傳遞至設備磁碟機以供播放或錄製之用。 這些函式中的每一個都會使用 [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) 結構來描述其資料區塊。

使用這些函式的其中一個來將資料區塊傳遞給設備磁碟機之前，您必須為緩衝區和描述資料區塊的標頭結構配置記憶體。

Windows 提供下列功能來準備和清除 MIDI 資料區塊。



| 值                                                    | 意義                                                |
|----------------------------------------------------------|--------------------------------------------------------|
| [**midiInPrepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-midiinprepareheader)       | 準備 MIDI 輸入資料區塊。                      |
| [**midiInUnprepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-midiinunprepareheader)   | 清除 MIDI 輸入資料區塊的準備工作。  |
| [**midiOutPrepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-midioutprepareheader)     | 準備 MIDI 輸出資料區塊。                     |
| [**midiOutUnprepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-midioutunprepareheader) | 清除 MIDI 輸出資料區塊的準備工作。 |



 

將 MIDI 資料區塊傳遞到設備磁碟機之前，您必須先將緩衝區傳遞給 [**midiInPrepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-midiinprepareheader) 或 [**midiOutPrepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-midioutprepareheader) 函式，以準備緩衝區。 當設備磁碟機完成緩衝區並傳回時，您必須先將緩衝區傳遞給 [**midiInUnprepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-midiinunprepareheader) 或 [**midiOutUnprepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-midioutunprepareheader) 函式，然後再釋放任何配置的記憶體，藉此清除這項準備工作。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[MIDI 服務](midi-services.md)
</dt> </dl>

 

 