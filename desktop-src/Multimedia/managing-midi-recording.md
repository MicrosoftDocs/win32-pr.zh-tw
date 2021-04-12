---
title: 管理 MIDI 錄製
description: 管理 MIDI 錄製
ms.assetid: 48b2d815-72cf-4c96-8d93-247d2426b8f2
keywords:
- 音樂檢測數位介面 (MIDI) ，錄製
- MIDI (的音樂檢測數位介面) ，錄製
- 錄製 MIDI 音訊，管理
- MIDI 記錄
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0edfb81976e1f5333798c9705640e7676281968a
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104462973"
---
# <a name="managing-midi-recording"></a>管理 MIDI 錄製

開啟 MIDI 裝置之後，您就可以開始錄製 MIDI 資料。 Windows 提供下列功能來管理 MIDI 錄音。



| 值                                      | 意義                                                                                           |
|--------------------------------------------|---------------------------------------------------------------------------------------------------|
| [**midiInAddBuffer**](/windows/win32/api/mmeapi/nf-mmeapi-midiinaddbuffer) | 將緩衝區傳送到設備磁碟機，讓它可以填滿已記錄的系統專屬 MIDI 資料。 |
| [**midiInReset**](/windows/win32/api/mmeapi/nf-mmeapi-midiinreset)         | 停止 MIDI 記錄，並將所有暫止的緩衝區標示為已完成。                                       |
| [**midiInStart**](/windows/win32/api/mmeapi/nf-mmeapi-midiinstart)         | 啟動 MIDI 記錄，並將時間戳記重設為零。                                          |
| [**midiInStop**](/windows/win32/api/mmeapi/nf-mmeapi-midiinstop)           | 停止 MIDI 錄音。                                                                             |



 

若要將緩衝區傳送到設備磁碟機以記錄系統專屬的訊息，請使用 [**midiInAddBuffer**](/windows/win32/api/mmeapi/nf-mmeapi-midiinaddbuffer)。 當緩衝區填入系統專屬記錄資料時，就會通知應用程式。 如需有關通知技術的詳細資訊，請參閱 [管理 MIDI 資料區塊](managing-midi-data-blocks.md)。

[**MidiInStart**](/windows/win32/api/mmeapi/nf-mmeapi-midiinstart)函式會開始錄製進程。 記錄系統專屬的訊息時，請在開始錄製之前將至少一個緩衝區傳送至驅動程式。 若要停止錄製，請使用 [**midiInStop**](/windows/win32/api/mmeapi/nf-mmeapi-midiinstop)。 使用 [**midiInClose**](/windows/win32/api/mmeapi/nf-mmeapi-midiinclose) 函式來關閉裝置之前，請先呼叫 [**midiInReset**](/windows/win32/api/mmeapi/nf-mmeapi-midiinreset)，將任何擱置中的資料區塊標示為已完成。

需要時間戳記資料的應用程式會使用回呼函數來接收 MIDI 資料。 如果您的時間需求不是嚴格的，您可以使用視窗或執行緒回呼。 不過，您無法使用事件回呼來接收 MIDI 資料。

若要使用不使用串流緩衝區的應用程式來記錄系統專屬的訊息，您必須以緩衝區提供設備磁碟機。 您可以使用 [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) 結構來指定這些緩衝區。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[錄製 MIDI 音訊](recording-midi-audio.md)
</dt> </dl>

 

 