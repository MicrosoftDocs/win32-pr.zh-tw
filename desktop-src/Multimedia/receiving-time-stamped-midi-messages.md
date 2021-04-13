---
title: 接收 Time-Stamped 的 MIDI 訊息
description: 接收 Time-Stamped 的 MIDI 訊息
ms.assetid: a91c85fe-f9c4-4cf6-b0bb-49aa8ed45644
keywords:
- 音樂檢測數位介面 (MIDI) 、時間戳記訊息
- MIDI (音樂檢測數位介面) 、時間戳記訊息
- 錄製 MIDI 音訊、時間戳記訊息
- 時間戳記的 MIDI 訊息
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7ead268c6d022f67a3607bb8a43a3d773bd7325
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104314863"
---
# <a name="receiving-time-stamped-midi-messages"></a>接收 Time-Stamped 的 MIDI 訊息

由於設備磁碟機接收 MIDI 訊息的時間與應用程式接收訊息的時間之間的延遲，因此，MIDI 輸入裝置磁碟機時間會將 MIDI 訊息加上訊息收到的時間戳記。 指定接收訊息第一個位元組時間的 MIDI 時間戳記（以毫秒為單位）。 [**MidiInStart**](/windows/win32/api/mmeapi/nf-mmeapi-midiinstart)函式會將裝置的時間戳記重設為零。

如先前所述，若要接收具有 MIDI 輸入的時間戳記，您必須使用回呼函式。 回呼函數的 *dwParam2* 參數會指定與 [**Mim \_ 資料**](mim-data.md) 和 [**mim \_ LONGDATA**](mim-longdata.md) 訊息相關聯之資料的時間戳記。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[錄製 MIDI 音訊](recording-midi-audio.md)
</dt> </dl>

 

 