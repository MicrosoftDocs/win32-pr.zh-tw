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
ms.openlocfilehash: 7ec36628a417c19824e25c7ad013da9c539fe88cb6e58fd829a32205bce35679
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118371288"
---
# <a name="receiving-time-stamped-midi-messages"></a>接收 Time-Stamped 的 MIDI 訊息

由於設備磁碟機接收 MIDI 訊息的時間與應用程式接收訊息的時間之間的延遲，因此，MIDI 輸入裝置磁碟機時間會將 MIDI 訊息加上訊息收到的時間戳記。 指定接收訊息第一個位元組時間的 MIDI 時間戳記（以毫秒為單位）。 [**MidiInStart**](/windows/win32/api/mmeapi/nf-mmeapi-midiinstart)函式會將裝置的時間戳記重設為零。

如先前所述，若要接收具有 MIDI 輸入的時間戳記，您必須使用回呼函式。 回呼函數的 *dwParam2* 參數會指定與 [**MIM \_ 資料**](mim-data.md)相關聯之資料的時間戳記，以及 [**MIM \_ LONGDATA**](mim-longdata.md)訊息。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[錄製 MIDI 音訊](recording-midi-audio.md)
</dt> </dl>

 

 