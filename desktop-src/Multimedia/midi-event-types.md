---
title: MIDI 事件種類
description: MIDI 事件種類
ms.assetid: 0b0984b7-3087-461e-90f2-a899dc1a88c6
keywords:
- 音樂檢測數位介面 (MIDI) 、事件種類
- MIDI (的音樂檢測數位介面) 、事件種類
- MIDIEVENT 結構
- 串流緩衝區，MIDI 事件種類
- MIDI 事件種類
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 823ce5ce7af898ca3178e0379fb814c54fbf06b7
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104023455"
---
# <a name="midi-event-types"></a>MIDI 事件種類

[**MIDIEVENT**](/windows/win32/api/mmeapi/ns-mmeapi-midievent)結構的 **dwEvent** 成員描述所要進行的 MIDI 事件。 簡短事件完全符合這個成員。 長事件除了 **dwEvent** 成員之外，還需要一個或多個雙列值來儲存事件描述。

**DwEvent** 成員的最大位元組包含事件是否很長或較短的資訊，以及是否隨著事件產生回呼。 此外，這個位元組也用來描述事件種類。 剩餘的24位 **dwEvent** 成員是用來包含短訊息 (的事件參數) 或包含事件參數的長度 (長訊息) 。 若要從 **dwEvent** 成員解壓縮資訊，請使用 [**MEVT \_**](/windows/win32/api/mmeapi/nf-mmeapi-mevt_eventtype) 的執行事件和 [**MEVT \_ EVENTPARM**](/windows/win32/api/mmeapi/nf-mmeapi-mevt_eventparm) 宏。

如需預先定義之事件種類的描述，請參閱 **MIDIEVENT** 結構的參考資料。

 

 