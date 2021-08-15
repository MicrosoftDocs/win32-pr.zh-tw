---
title: 金鑰地圖
description: 金鑰地圖
ms.assetid: 5d0367b0-bbf1-4a4b-98b2-dbca6f2f8b0c
keywords:
- 音樂檢測數位介面 (MIDI) 、MIDI 對應程式
- MIDI (的音樂檢測數位介面) 、MIDI 對應程式
- MIDI 對應程式，金鑰組應
- 金鑰組應
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72197de28a6596efa951b302f0ca351ac187532cd28d431cf1d954b53d841064
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118140219"
---
# <a name="key-maps"></a>金鑰地圖

Patch map 轉譯表中的每個專案都可以有相關聯的索引鍵對應。 金鑰組應會影響注意事項、注意和 polyphonic 的 aftertouch 訊息。 索引鍵對應具有轉譯資料表，其中每個128的 MIDI 金鑰值都有一個專案。 例如，如果索引鍵值60的專案是72，則 MIDI 對應工具會修改 MIDI 附注訊息，如下圖所示。

![midi 對應程式映射](images/mmap-a06.gif)

Key map 適用于具有金鑰型 percussion 檢測，並將特定 percussion 音效指派給每個金鑰的合成程式。 金鑰組應通常會指派給 percussion 通道 (10 和 16) 修補程式中的第一個修補程式。

 

 




