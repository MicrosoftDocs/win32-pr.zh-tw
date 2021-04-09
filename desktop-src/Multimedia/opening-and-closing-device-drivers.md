---
title: 開啟和關閉設備磁碟機
description: 開啟和關閉設備磁碟機
ms.assetid: 441bc0ec-41c9-4595-92f9-4c2304b10f16
keywords:
- 音樂檢測數位介面 (MIDI) ，開啟裝置
- MIDI (的音樂檢測數位介面) ，開啟裝置
- MIDI 服務，開啟裝置
- 開啟 MIDI 裝置
- 音樂檢測數位介面 (MIDI) ，關閉裝置
- MIDI (的音樂檢測數位介面) ，關閉裝置
- MIDI 服務，關閉裝置
- 關閉 MIDI 裝置
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53d7035455baa067b81af7da980a4ae043500c7b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "103681802"
---
# <a name="opening-and-closing-device-drivers"></a>開啟和關閉設備磁碟機

您必須在使用前先開啟 MIDI 裝置，並在使用完畢後立即關閉裝置。 Windows 提供下列功能來開啟和關閉不同類型的 MIDI 裝置。



| 值                                | 意義                                            |
|--------------------------------------|----------------------------------------------------|
| [**midiInClose**](/windows/win32/api/mmeapi/nf-mmeapi-midiinclose)   | 關閉指定的 MIDI 輸入裝置。              |
| [**midiInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midiinopen)     | 開啟指定的 MIDI 輸入裝置以進行錄製。 |
| [**midiOutClose**](/windows/win32/api/mmeapi/nf-mmeapi-midioutclose) | 關閉指定的 MIDI 輸出裝置。             |
| [**midiOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midioutopen)   | 開啟 MIDI 輸出裝置以供播放。           |



 

開啟 MIDI 裝置的每個函式會以裝置識別碼、記憶體位置的位址，以及一些 MIDI 裝置特有的參數作為參數。 記憶體位置會以裝置控制碼填滿，用來識別呼叫其他音訊函式的開放式音訊裝置。

許多 MIDI 函數可以接受裝置控制碼或裝置識別碼。 雖然您可以在使用裝置識別碼的任何地方使用裝置控制碼，但在呼叫控制碼時，不能一律使用裝置識別碼。

> [!Note]  
> MIDI 裝置不一定可共用，因此當使用者要求時，可能無法使用特定的裝置。 如果發生這種情況，應用程式應該會通知使用者，並讓使用者嘗試再次開啟裝置。

 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[MIDI 服務](midi-services.md)
</dt> </dl>

 

 