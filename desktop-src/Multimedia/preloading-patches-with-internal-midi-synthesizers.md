---
title: 使用內部 MIDI 合成程式預先載入修補程式
description: 使用內部 MIDI 合成程式預先載入修補程式
ms.assetid: c200aa91-ab91-48e8-b3b5-8e7f36e511be
keywords:
- 音樂檢測數位介面 (MIDI) 、內部合成工具
- MIDI (的音樂檢測數位介面) ，內部合成
- 播放 MIDI 檔案，內部合成
- 內部 MIDI 合成
- " (MIDI) 的音樂檢測數位介面，預先載入修補程式"
- MIDI (的音樂檢測數位介面) ，預先載入修補程式
- 播放 MIDI 檔案，預先載入修補程式
- 預先載入 MIDI 修補程式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de389e058c015c38d05fb8ff2a960ca3ef75a662faa6a1ce519c26afe14f09b3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118372495"
---
# <a name="preloading-patches-with-internal-midi-synthesizers"></a>使用內部 MIDI 合成程式預先載入修補程式

某些內部的 MIDI 合成器裝置無法同時載入其所有修補程式。 這些裝置必須預先載入其修補程式資料。

Windows 提供下列函式，以要求合成器預先載入並快取指定的修補程式。



| 值                                                      | 意義                                                                                                     |
|------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| [**midiOutCachePatches**](/windows/win32/api/mmeapi/nf-mmeapi-midioutcachepatches)         | 要求內部 MIDI 合成器裝置預先載入並快取指定的 melodic 修補程式。              |
| [**midiOutCacheDrumPatches**](/windows/win32/api/mmeapi/nf-mmeapi-midioutcachedrumpatches) | 要求內部 MIDI 合成器裝置預先載入並快取指定的金鑰型 percussion 修補程式。 |



 

如需如何判斷特定裝置是否支援預先載入修補程式的相關資訊，請參閱 [查詢 MIDI 輸出裝置](querying-midi-output-devices.md)。

 

 