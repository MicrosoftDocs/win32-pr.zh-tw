---
title: 查詢 MIDI 輸出裝置
description: 查詢 MIDI 輸出裝置
ms.assetid: c6a33a4e-c61a-4e06-805e-5128a97f5199
keywords:
- 音樂檢測數位介面 (MIDI) 、輸出裝置
- MIDI (的音樂檢測數位介面) ，輸出裝置
- 播放 MIDI 檔案，輸出裝置
- MIDI 輸出裝置
- 音樂檢測數位介面 (MIDI) ，查詢輸出裝置
- MIDI (的音樂檢測數位介面) ，查詢輸出裝置
- 播放 MIDI 檔案，查詢輸出裝置
- 查詢 MIDI 輸出裝置
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b493c0b3554a9a60cfc349d13a5404ec4d2b27915933c14b387df29a582406e5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118371910"
---
# <a name="querying-midi-output-devices"></a>查詢 MIDI 輸出裝置

播放 MIDI 檔案之前，您應該使用 [**midiOutGetDevCaps**](/windows/win32/api/mmeapi/nf-mmeapi-midioutgetdevcaps) 函式來判斷系統中的 midi 輸出裝置的功能。 此函式會採用 [**MIDIOUTCAPS**](/windows/win32/api/mmeapi/ns-mmeapi-midioutcaps) 結構的位址，其會填入指定裝置功能的相關資訊。 這項資訊包括製造商和產品識別碼、裝置的產品名稱，以及 (在 **wMid**、 **wPid**、 **szPname** 和 **vDriverVersion** 成員中分別指定的設備磁碟機版本號碼) 。

MIDI 輸出裝置可以是內部合成或外部 MIDI 輸出埠。 **MIDIOUTCAPS** 結構的 **wTechnology** 成員會指定裝置的技術。

如果裝置是內部合成器， **wVoices**、 **wNotes** 和 **wChannelMask** 成員中會提供其他的裝置資訊。 **WVoices** 成員會指定裝置支援的語音數目。 每個語音可以有不同的音效或 timbre。 語音會組織成 MIDI 頻道。 **WNotes** 成員會指定裝置的 *polyphony* ，也就是可以同時播放的最大附注數目。 **WChannelMask** 成員是裝置所回應之 MIDI 通道的位標記法。 例如，如果裝置回應前八個 MIDI 通道，則 **wChannelMask** 為0x00FF。 如果裝置是外部輸出埠，則不會使用 **wVoices** 和 **WNotes** ，而 **wChannelMask** 會設定為0xffff。

**MIDIOUTCAPS** 結構的 **dwSupport** 成員會指出設備磁碟機是否支援磁片區變更、修補程式快取，以及串流處理。 只有內部合成裝置才支援磁片區變更。 外部 MIDI 輸出埠不支援磁片區變更。 如需變更磁片區的相關資訊，請參閱 [變更內部 MIDI 合成器磁片](changing-internal-midi-synthesizer-volume.md)區。

 

 