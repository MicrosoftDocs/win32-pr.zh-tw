---
title: 使用資料流程緩衝區傳送 MIDI 訊息
description: 使用資料流程緩衝區傳送 MIDI 訊息
ms.assetid: f9e77637-098c-4ee8-bca9-a05ecce0c569
keywords:
- 音樂檢測數位介面 (MIDI) 、串流緩衝區
- MIDI (音樂檢測數位介面) 、串流緩衝區
- 播放 MIDI 檔案，資料流程緩衝區
- 串流緩衝區，傳送 MIDI 訊息
- 音樂檢測數位介面 (MIDI) ，傳送訊息
- MIDI (的音樂檢測數位介面) ，傳送訊息
- 播放 MIDI 檔案，傳送訊息
- 傳送 MIDI 訊息
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35ab8fd8d09295cc40a3ea9b5d8070603a4e7813030b4f04f92a51f7f8709f5b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119892728"
---
# <a name="sending-midi-messages-with-stream-buffers"></a>使用資料流程緩衝區傳送 MIDI 訊息

當您的應用程式搭配串流緩衝區使用時，它會使用 [**midiStreamOut**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamout) 函式將所有 (短和長) 的 MIDI 訊息傳送至裝置。 若要指定資料流程資料區塊，請使用 [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) 和 [**MIDIEVENT**](/windows/win32/api/mmeapi/ns-mmeapi-midievent) 結構。 **MIDIHDR** 結構包含鎖定資料區塊的位址、資料區塊長度，以及一些各式各樣的旗標。 資料會以 **MIDIEVENT** 結構的形式儲存。 系統會在資料流程緩衝區上強加64的大小限制。

使用 **midiStreamOut** 傳送資料的資料流程緩衝區之後，您必須等到設備磁碟機完成後再釋放資料區塊。 如果您要傳送多個資料區塊，您必須監視每個資料區塊的完成，讓您知道何時傳送其他區塊。 如需有關監視資料區塊完成的不同技術的詳細資訊，請參閱 [管理 MIDI 資料區塊](managing-midi-data-blocks.md)。

 

 