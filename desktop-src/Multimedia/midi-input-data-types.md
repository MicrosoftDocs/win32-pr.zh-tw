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
ms.openlocfilehash: 4f3cb45c321cdac95c09274f25293f4635d5a715638367c8f9e06cf5c45777af
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119525218"
---
# <a name="midi-input-data-types"></a>MIDI 輸入資料類型

Windows 定義下列 MIDI 輸入函式的資料類型。



| 值                            | 意義                                                                                                                                                                                     |
|----------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **HMIDIIN**                      | MIDI 輸入裝置的控制碼。                                                                                                                                                              |
| [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr)       | 資料流程緩衝區或 MIDI 系統專屬資料區塊的標頭。 針對輸入應用程式，此結構只會記錄系統專屬的資料 (串流不支援 MIDI 輸入) 。 |
| [**MIDIINCAPS**](/windows/win32/api/mmeapi/ns-mmeapi-midiincaps) | 用來查詢 MIDI 輸入裝置功能的結構。                                                                                                                    |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[錄製 MIDI 音訊](recording-midi-audio.md)
</dt> </dl>

 

 