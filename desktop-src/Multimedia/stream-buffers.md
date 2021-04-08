---
title: 資料流程緩衝區
description: 資料流程緩衝區
ms.assetid: d73209a3-4b9d-4405-9e62-8ecfb94c0bd5
keywords:
- Windows 多媒體，資料流程緩衝區
- 多媒體、串流緩衝區
- 多媒體音訊、串流緩衝區
- 音訊、串流緩衝區
- 音樂檢測數位介面 (MIDI) 、串流緩衝區
- MIDI (音樂檢測數位介面) 、串流緩衝區
- 串流緩衝區，關於
- MIDIHDR 結構
- MIDIEVENT 結構
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d4a01862a8a8e6b7846cbe445737bd13422cf0f
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "103681870"
---
# <a name="stream-buffers"></a>資料流程緩衝區

應用程式可以使用串流緩衝區將 MIDI 事件的串流傳送至裝置。 每個資料流程緩衝區都是 [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) 結構所指向的記憶體區塊。 這個記憶體區塊包含一或多個 MIDI 事件的資料，每個事件都是由 [**MIDIEVENT**](/windows/win32/api/mmeapi/ns-mmeapi-midievent) 結構所定義。 應用程式會藉由呼叫資料流程操作函式（例如 [**midiStreamOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamopen)、 [**midiStreamOut**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamout)和 [**midiStreamClose**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamclose)）來控制緩衝區。

-   [資料流程緩衝區格式](stream-buffer-format.md)
-   [計時資訊](timing-information.md)
-   [MIDI 事件種類](midi-event-types.md)
-   [MIDI 串流](midi-streams.md)

 

 