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
ms.openlocfilehash: 905b0ce924f9aebce67f515fc0714fdc855cbe33
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104463073"
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

 

 

 