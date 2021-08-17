---
title: 查詢 MIDI 輸入裝置
description: 查詢 MIDI 輸入裝置
ms.assetid: 2da88418-f9cf-49da-b17f-8a26d357b5ab
keywords:
- 音樂檢測數位介面 (MIDI) 、輸入裝置
- MIDI (的音樂檢測數位介面) ，輸入裝置
- 錄製 MIDI 音訊、輸入裝置
- MIDI 輸入裝置
- " (MIDI) 的音樂檢測數位介面，查詢輸入裝置"
- MIDI (的音樂檢測數位介面) ，查詢輸入裝置
- 錄製 MIDI 音訊，查詢輸入裝置
- 查詢 MIDI 輸入裝置
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81340f767c1ef3acf3105f78d2cef000f7548361b387e6887ecc4136437dbe6e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118371930"
---
# <a name="querying-midi-input-devices"></a>查詢 MIDI 輸入裝置

錄製 MIDI 音訊之前，您應該使用 [**midiInGetDevCaps**](/windows/win32/api/mmeapi/nf-mmeapi-midiingetdevcaps) 函式來判斷系統中的 midi 輸入裝置的功能。 此函式會採用 [**MIDIINCAPS**](/windows/win32/api/mmeapi/ns-mmeapi-midiincaps) 結構的位址，其會填入指定裝置功能的相關資訊。 這項資訊包括製造商和產品識別碼、裝置的產品名稱，以及設備磁碟機的版本號碼。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[錄製 MIDI 音訊](recording-midi-audio.md)
</dt> </dl>

 

 