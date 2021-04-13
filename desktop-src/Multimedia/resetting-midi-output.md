---
title: 重設 MIDI 輸出
description: 重設 MIDI 輸出
ms.assetid: 281a7cfa-f274-4c7a-b63a-c0573b9f1169
keywords:
- " (MIDI) 的音樂檢測數位介面，重設輸出裝置"
- MIDI (的音樂檢測數位介面) ，重設輸出裝置
- 播放 MIDI 檔案，重設輸出裝置
- 重設輸出裝置
- 音樂檢測數位介面 (MIDI) 、輸出裝置
- MIDI (的音樂檢測數位介面) ，輸出裝置
- 播放 MIDI 檔案，輸出裝置
- MIDI 輸出裝置
- 'EOX (結束專屬) '
- 'EOX 結尾 (的) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15778fc8a1a48c34b69915aafb7e3139153b5882
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104314686"
---
# <a name="resetting-midi-output"></a>重設 MIDI 輸出

[**MidiOutReset**](/windows/win32/api/mmeapi/nf-mmeapi-midioutreset)函式會關閉指定之 midi 裝置的所有 MIDI 通道上的所有便箋。 然後，此函式會將任何擱置中的系統專屬緩衝區標示為已完成，並將它們傳回給應用程式。 此函式可用於使用 MIDI 輸出的應用程式，讓使用者能夠重設 MIDI 輸出。

> [!Note]  
> 在不傳送 EOX 的情況下終止系統專屬的訊息， (端) 位元組會導致接收裝置發生問題。 **MidiOutReset** 函式會在終止系統專屬的訊息時，不會傳送 EOX 位元組，因為應用程式會負責執行此工作。

 

 

 