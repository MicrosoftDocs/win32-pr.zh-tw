---
title: 使用 midiOutShortMsg 傳送個別的 MIDI 訊息
description: 使用 midiOutShortMsg 傳送個別的 MIDI 訊息
ms.assetid: 7a8f7c6c-28ac-4aa6-9073-969fc8e59f4e
keywords:
- 音樂檢測數位介面 (MIDI) ，傳送訊息
- MIDI (的音樂檢測數位介面) ，傳送訊息
- 傳送 MIDI 訊息
- " (MIDI) ，midiOutShortMsg 函式的音樂檢測數位介面"
- MIDI (音樂檢測數位介面) ，midiOutShortMsg 函式
- midiOutShortMsg 函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: accd4f1f7482c81acdff1c950ada8947d3b1d456438dd96092ae094ae587de42
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117800820"
---
# <a name="using-midioutshortmsg-to-send-individual-midi-messages"></a>使用 midiOutShortMsg 傳送個別的 MIDI 訊息

下列範例會使用 [**midiOutShortMsg**](/windows/win32/api/mmeapi/nf-mmeapi-midioutshortmsg) 函式，將指定的 midi 事件傳送到指定的 midi 輸出裝置：


```C++
UINT sendMIDIEvent(HMIDIOUT hmo, BYTE bStatus, BYTE bData1, 
    BYTE bData2) 
{ 
    union { 
        DWORD dwData; 
        BYTE bData[4]; 
    } u; 
 
    // Construct the MIDI message. 
 
    u.bData[0] = bStatus;  // MIDI status byte 
    u.bData[1] = bData1;   // first MIDI data byte 
    u.bData[2] = bData2;   // second MIDI data byte 
    u.bData[3] = 0; 
 
    // Send the message. 
    return midiOutShortMsg(hmo, u.dwData); 
} 
```



> [!Note]  
> 在將資料傳送至輸出埠之前，不需要使用 MIDI 輸出驅動程式來驗證資料。 應用程式必須確定只傳送有效的資料。

 

 

 