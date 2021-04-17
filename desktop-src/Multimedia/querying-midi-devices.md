---
title: 查詢 MIDI 裝置
description: 查詢 MIDI 裝置
ms.assetid: 0c9882a7-b5cb-41d1-a52e-003112225035
keywords:
- " (MIDI) 的音樂檢測數位介面，查詢裝置"
- MIDI (的音樂檢測數位介面) ，查詢裝置
- MIDI 服務，查詢裝置
- 查詢 MIDI 裝置
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 066648d6e9ce89e03b26940cb27f3b62b6a03c07
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104375048"
---
# <a name="querying-midi-devices"></a>查詢 MIDI 裝置

在播放或錄製 MIDI 資料之前，您必須先判斷出系統中的 MIDI 硬體有哪些功能。 MIDI 功能可能會因一部多媒體電腦而異;應用程式不應對指定系統中的硬體提出假設。

Windows 提供下列功能，以判斷指定系統中有多少部 MIDI 裝置可供輸入或輸出。



| 值                                          | 意義                                                            |
|------------------------------------------------|--------------------------------------------------------------------|
| [**midiInGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-midiingetnumdevs)   | 抓取系統中出現的 MIDI 輸入裝置數目。  |
| [**midiOutGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-midioutgetnumdevs) | 抓取系統中出現的 MIDI 輸出裝置數目。 |



 

就像其他音訊裝置一樣，MIDI 裝置是由裝置識別碼來識別，而這是由指定系統中的裝置數目隱含決定。 裝置識別碼的範圍從零到已存在的裝置數目，減去一。 例如，如果系統中有兩個 MIDI 輸出裝置，則有效的裝置識別碼為0和1。

判斷出系統中有多少個 MIDI 輸入或輸出裝置之後，您就可以查詢每個裝置的功能。 Windows 提供下列功能來判斷音訊裝置的功能。



| 值                                          | 意義                                                                                                                                   |
|------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| [**midiInGetDevCaps**](/windows/win32/api/mmeapi/nf-mmeapi-midiingetdevcaps)   | 抓取指定之 MIDI 輸入裝置的功能，並將這項資訊放在 [**MIDIINCAPS**](/windows/win32/api/mmeapi/ns-mmeapi-midiincaps) 結構中。    |
| [**midiOutGetDevCaps**](/windows/win32/api/mmeapi/nf-mmeapi-midioutgetdevcaps) | 抓取指定之 MIDI 輸出裝置的功能，並將這項資訊放在 [**MIDIOUTCAPS**](/windows/win32/api/mmeapi/ns-mmeapi-midioutcaps) 結構中。 |



 

這些函式中的每一個都有參數，可指定函式所填滿的結構位址，以及指定裝置功能的相關資訊。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[MIDI 服務](midi-services.md)
</dt> </dl>

 

 