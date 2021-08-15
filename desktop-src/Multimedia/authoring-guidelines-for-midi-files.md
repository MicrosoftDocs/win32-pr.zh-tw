---
title: 適用于 MIDI 檔案的撰寫指導方針
description: 適用于 MIDI 檔案的撰寫指導方針
ms.assetid: 57e3d260-d275-4b0c-9db0-d036dd12fdb8
keywords:
- " (MIDI) 的音樂檢測數位介面，檔案撰寫指導方針"
- MIDI (的音樂檢測數位介面) ，檔案撰寫指導方針
- 建立 MIDI 檔案，檔案撰寫指導方針
- 標準 MIDI 修補程式指派
- 標準 MIDI 金鑰指派
- 音樂檢測數位介面 (MIDI) 、標準修補程式指派
- MIDI (的音樂檢測數位介面) ，標準修補程式指派
- " (MIDI) 的音樂檢測數位介面，標準金鑰指派"
- MIDI (的音樂檢測數位介面) ，標準金鑰指派
- 建立 MIDI 檔案，標準修補程式指派
- 建立 MIDI 檔案，標準金鑰指派
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe148c2fe1bb562aad994608a8c87c35e84bccb7d63ba1bc3ee3e5dd3bbc56a9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119065638"
---
# <a name="authoring-guidelines-for-midi-files"></a>適用于 MIDI 檔案的撰寫指導方針

遵循這些指導方針，為 Windows 撰寫與裝置無關的 MIDI 檔案：

-   使用 [標準的 Midi 修補程式指派](standard-midi-patch-assignments.md) 和 [標準的 midi 金鑰指派](standard-midi-key-assignments.md)。
-   一律將程式變更訊息傳送至通道以選取修補程式，然後再將其他訊息傳送至該通道。 針對兩個 percussion 通道 (10 和 16) ，請選取 [程式編號 0]。
-   一律遵循 MIDI 程式-變更訊息與 MIDI 主要磁片區控制器訊息 (控制器編號 7) 來設定修補程式的相對磁片區。
-   針對一般接聽層級，使用主要磁片區控制器的 80 (0x50) 。 如需更安靜或更高的層級，您可以使用較低或更高的值。
-   僅使用下列 MIDI 訊息：注意：具有速度、附注關閉、程式變更、音調彎曲、主要磁片區 (控制器 7) 和氣流踏板 (控制器 64) 。 需要內部合成者才能回應這些訊息，而大部分的 MIDI 樂器也會回應這些訊息。

 

 




