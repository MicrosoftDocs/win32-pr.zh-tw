---
title: 開啟 MIDI 輸入裝置
description: 開啟 MIDI 輸入裝置
ms.assetid: fd6ebd0c-6985-49d3-8015-a636d4c70ff3
keywords:
- 音樂檢測數位介面 (MIDI) 、輸入裝置
- MIDI (的音樂檢測數位介面) ，輸入裝置
- 錄製 MIDI 音訊、輸入裝置
- MIDI 輸入裝置
- " (MIDI) 的音樂檢測數位介面，開啟輸入裝置"
- MIDI (的音樂檢測數位介面) ，開啟輸入裝置
- 錄製 MIDI 音訊，開啟輸入裝置
- 開啟 MIDI 輸入裝置
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d4c1271cee1e6a47c35f8c555932d87d1055065
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "103682112"
---
# <a name="opening-midi-input-devices"></a>開啟 MIDI 輸入裝置

若要開啟 MIDI 輸入裝置以進行錄製，請使用 [**midiInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midiinopen) 函式。 此函式會開啟與指定裝置識別碼相關聯的裝置，並將控制碼寫入指定的記憶體位置，以傳回開啟裝置的控制碼。

如果您使用 [MIDI \_ IO \_ 狀態] 旗標搭配 **midiInOpen**，系統會使用 [**MIM \_ MOREDATA**](mim-moredata.md) 訊息來警示您的應用程式回呼函式，使其無法以足夠的速度處理 MIDI 資料來跟上輸入裝置磁碟機。  ([**MM \_ MIM \_ MOREDATA**](mm-mim-moredata.md) 訊息會使用視窗回呼執行相同的作業。 不過，基於效能考慮，大部分的應用程式都會使用回呼函式，而不是使用視窗回呼。 ) 如果您的應用程式在個別的執行緒中處理 MIDI 資料，提高執行緒的優先順序可能會對應用程式與資料流程的能力有顯著的影響。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[錄製 MIDI 音訊](recording-midi-audio.md)
</dt> </dl>

 

 