---
title: 變更內部 MIDI 合成器磁片區
description: 變更內部 MIDI 合成器磁片區
ms.assetid: 75ab7ff5-f394-4a79-8dcc-f4eef434a36e
keywords:
- 音樂檢測數位介面 (MIDI) 、內部合成工具
- MIDI (的音樂檢測數位介面) ，內部合成
- 播放 MIDI 檔案，內部合成
- 內部 MIDI 合成
- 音樂檢測數位介面 (MIDI) ，變更音量
- MIDI (的音樂檢測數位介面) ，變更音量
- 播放 MIDI 檔案，變更磁片區
- 變更 MIDI 磁片區
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 646c7e17a7e8c0a6902e26dd8bbfdf8eb89c39297fdacdf062749d8c47a3d487
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119808208"
---
# <a name="changing-internal-midi-synthesizer-volume"></a>變更內部 MIDI 合成器磁片區

Windows 提供下列函式來取得和設定內部 MIDI 合成裝置的音量層級：



| 值                                        | 意義                                                                       |
|----------------------------------------------|-------------------------------------------------------------------------------|
| [**midiOutGetVolume**](/windows/win32/api/mmeapi/nf-mmeapi-midioutgetvolume) | 抓取指定內部 MIDI 合成裝置的磁片區層級。 |
| [**midiOutSetVolume**](/windows/win32/api/mmeapi/nf-mmeapi-midioutsetvolume) | 設定指定之內部 MIDI 合成裝置的音量層級。      |



 

並非所有的 MIDI 輸出裝置都支援磁片區變更。 某些裝置可支援左右通道上的個別磁片區變更。 如需如何判斷特定裝置是否支援磁片區變更的相關資訊，請參閱 [查詢 MIDI 輸出裝置](querying-midi-output-devices.md)。

除非您的應用程式是設計成主要磁片區控制應用程式 (為使用者提供系統) 中所有音訊裝置的音量控制，否則您應該先開啟音訊裝置，再變更其磁片區。 您也應該先檢查磁片區層級，再進行變更，並儘快將磁片區層級還原至先前的層級。

磁片區會指定為雙量值。 上層16位會指定右通道的相對磁片區，而較低的16個位則指定左邊通道的相對磁片區。

對於不支援左右通道上個別磁片區變更的裝置，較低的16位會指定磁片區層級，而會忽略前16位。 磁片區層級的值範圍從 0x0 (無回應) 至 0xFFFF (最大磁片區) ，而且會 logarithmically。 將磁片區層級從0x5000 增加至0x6000 時，觀察到的磁片區增加是相同的，因為它是從0x4000 到0x5000。

 

 