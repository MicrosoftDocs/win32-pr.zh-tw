---
title: MIDI 輸入資料類型
description: MIDI 輸入資料類型
ms.assetid: c67f149e-60b8-4f9e-8e3c-a88cd579d29f
keywords:
- 音樂檢測數位介面 (MIDI) 、輸入資料類型
- MIDI (的音樂檢測數位介面) 、輸入資料類型
- 錄製 MIDI 音訊，輸入資料類型
- MIDI 輸入資料類型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8f0738827cce4cfd8cb4a237dcd2031c2fe71a7
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "106968696"
---
# <a name="midi-input-data-types"></a>MIDI 輸入資料類型

Windows 會為 MIDI 輸入函式定義下列資料類型。



| 值                            | 意義                                                                                                                                                                                     |
|----------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **HMIDIIN**                      | MIDI 輸入裝置的控制碼。                                                                                                                                                              |
| [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr)       | 資料流程緩衝區或 MIDI 系統專屬資料區塊的標頭。 針對輸入應用程式，此結構只會記錄系統專屬的資料 (串流不支援 MIDI 輸入) 。 |
| [**MIDIINCAPS**](/windows/win32/api/mmeapi/ns-mmeapi-midiincaps) | 用來查詢 MIDI 輸入裝置功能的結構。                                                                                                                    |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[錄製 MIDI 音訊](recording-midi-audio.md)
</dt> </dl>

 

 