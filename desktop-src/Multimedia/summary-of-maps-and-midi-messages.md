---
title: 地圖和 MIDI 訊息的摘要
description: 地圖和 MIDI 訊息的摘要
ms.assetid: cd0ec7b0-2ba1-4e75-b85c-f5b95ac9dfeb
keywords:
- 音樂檢測數位介面 (MIDI) 、MIDI 對應程式
- MIDI (的音樂檢測數位介面) 、MIDI 對應程式
- MIDI 對應工具，通道對應
- MIDI 對應程式，修補程式對應
- MIDI 對應程式，金鑰組應
- 通道對應
- 修補程式對應
- 金鑰組應
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ddd962f848343ea493204d494943a99eedcc56a5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103675068"
---
# <a name="summary-of-maps-and-midi-messages"></a>地圖和 MIDI 訊息的摘要

以下是 MIDI 訊息的狀態位元組和影響每個訊息的對應類型。



| MIDI 狀態 | Description               | 對應類型                |
|-------------|---------------------------|--------------------------|
| 0x80-0x8F   | 請注意                  | 通道對應，金鑰組應   |
| 0x90-0x9F   | 注意                    | 通道對應，金鑰組應   |
| 0xA0-0xAF   | Polyphonic-key aftertouch | 通道對應，金鑰組應   |
| 0xB0-0xBF   | 控制項變更            | Channel maps、patch map |
| 0xC0-0xCF   | 程式變更            | Channel maps、patch map |
| 0xD0-0xDF   | 通道 aftertouch        | 通道對應             |
| 0xE0-0xEF   | 音調-折彎變更         | 通道對應             |
| 0xF0-0xFF   | 系統                    | 未對應               |



 

-   高序位四個位代表狀態值。 低序位四個位代表通道資訊。
-   修補程式對應只會影響主要磁碟區) 的控制器 7 (。
-   系統訊息會傳送至通道對應中列出的所有裝置。

 

 




