---
title: 通道對應
description: 通道對應
ms.assetid: f35d8b76-dfbf-4453-baec-9c0b22f5278a
keywords:
- 音樂檢測數位介面 (MIDI) 、MIDI 對應程式
- MIDI (的音樂檢測數位介面) 、MIDI 對應程式
- MIDI 對應工具，通道對應
- 通道對應
- MIDI 對應程式，通道訊息
- MIDI 通道訊息
- 通道訊息
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5d514b5af6df6426db7cc5a313d1c6a52070a49c22a8a04e8cd2a9c34f49d80
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119688281"
---
# <a name="the-channel-map"></a>通道對應

通道對應會影響所有的 MIDI 通道訊息。 MIDI 通道訊息包括注意事項、注意事項、polyphonic-按鍵 aftertouch、控制項變更、程式變更、通道 aftertouch 和音調彎曲變更訊息。 MIDI 對應工具使用單一通道對應，其中每個16個 MIDI 通道都有一個專案。 每個通道對應專案都會指定下列專案：

-   MIDI 訊息的目的地通道
-   適用于 MIDI 訊息的目的地輸出裝置
-   選用的 patch map，可指定其他可能的 MIDI 訊息修改

目的地通道會設定為16個 MIDI 通道的其中一個。 會修改 MIDI 訊息，以反映每個新的通道指派。 例如，如果 MIDI 通道4的目的地通道專案設定為6，傳送至通道4的所有 MIDI 訊息都會對應到 channel 6，如下圖所示。

![對應的 midi 映射](images/mmap-a05.gif)

在此範例中，MIDI 狀態位元組0x93 會對應至0x95。 MIDI 狀態位元組的低順序會指定頻道號碼。 來源通道設定為 [作用中] 或 [非使用中]。 傳送至非使用中來源通道的訊息會被忽略，因此非作用中的通道會變成靜音或關閉。

目的地輸出裝置會設定為其中一個可用的 MIDI 輸出裝置。 MIDI 輸出裝置可以是內部合成器或實體的 MIDI 輸出埠。

MIDI 系統訊息是 (狀態位元組) 從0xF0 到0xFF 的 MIDI 訊息。 沒有與 MIDI 系統訊息相關聯的通道，因此無法對應。 MIDI 系統訊息會傳送至通道對應中列出的所有 MIDI 輸出裝置。

 

 




