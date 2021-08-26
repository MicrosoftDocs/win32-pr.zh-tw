---
title: 傳送 System-Exclusive 訊息
description: 傳送 System-Exclusive 訊息
ms.assetid: 2bb95e4e-004e-46c8-9c56-25436fcc7f6c
keywords:
- 音樂檢測數位介面 (MIDI) ，傳送訊息
- MIDI (的音樂檢測數位介面) ，傳送訊息
- 播放 MIDI 檔案，傳送訊息
- 傳送 MIDI 訊息
- 音樂檢測數位介面 (MIDI) 、系統專屬的訊息
- MIDI (的音樂檢測數位介面) 、系統專屬的訊息
- 播放 MIDI 檔案，系統專屬訊息
- 系統專屬的 MIDI 訊息
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aad97371f56c042e5acd230aba6144f5f9734a594b370a791422b2e8f8148861
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120037258"
---
# <a name="sending-system-exclusive-messages"></a>傳送 System-Exclusive 訊息

MIDI 系統專屬訊息是唯一不符合單一雙全半值的 MIDI 訊息。 系統專屬訊息可以是任何長度。 Windows 提供將系統專屬訊息傳送至 MIDI 輸出裝置的 [**midiOutLongMsg**](/windows/win32/api/mmeapi/nf-mmeapi-midioutlongmsg)函式。 若要指定 MIDI 系統專屬資料區塊，請使用 [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) 結構。

使用 **midiOutLongMsg** 傳送系統專屬的資料區塊之後，您必須等到設備磁碟機使用資料區塊完成後再釋放它。 如果您要傳送多個資料區塊，您必須監視每個資料區塊的完成，讓您知道何時傳送其他區塊。 如需有關監視資料區塊完成的不同技術的詳細資訊，請參閱 [管理 MIDI 資料區塊](managing-midi-data-blocks.md)。

> [!Note]  
> 系統即時訊息以外的任何 MIDI 狀態位元組都將終止系統專屬的訊息。 如果您使用多個資料區塊來傳送單一系統專屬的訊息，請勿在資料區塊之間傳送系統即時訊息以外的任何 MIDI 訊息。

 

 

 