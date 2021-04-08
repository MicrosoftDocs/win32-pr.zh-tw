---
title: Sequencer 錯誤
description: Sequencer 錯誤
ms.assetid: 07f2d6c5-8c23-4f3e-8b8a-4f659eda57f7
keywords:
- MCIERR 傳回值，sequencer 錯誤
- 多媒體參考，sequencer 錯誤
- 多媒體的參考、sequencer 錯誤
- 媒體控制介面 (MCI) 、sequencer 錯誤
- MCI (媒體控制介面) 、sequencer 錯誤
- MCI、sequencer 錯誤的參考
- MCI 參考，sequencer 錯誤
- 媒體控制介面 (MCI) ，錯誤
- MCI (媒體控制介面) ，錯誤
- MCI 的參考，錯誤
- MCI 參考，錯誤
- sequencer 錯誤
- MCI sequencer 錯誤
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7dd7d55d3b49be3d641f7396148d98766b224a58
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103673160"
---
# <a name="sequencer-errors"></a>Sequencer 錯誤

下列額外的傳回值是針對 MCI sequencers 所定義：



| 值                          | 意義                                                                                                                                                  |
|--------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| MCIERR \_ SEQ \_ DIV \_ 不相容 | "Song 指標" 和 SMPTE 的時間格式為單數。 您無法一起使用它們。                                                              |
| MCIERR \_ SEQ \_ NOMIDIPRESENT     | 此系統沒有任何已安裝的 MIDI 裝置。 使用主控台的 [驅動程式] 選項來安裝 MIDI 驅動程式。                                       |
| MCIERR \_ SEQ \_ PORT \_ INUSE       | 指定的 MIDI 埠已在使用中。 等到免費為止;然後再試一次。                                                                       |
| MCIERR \_ SEQ \_ PORT \_ MAPNODEVICE | 目前的 MIDI 對應程式安裝程式指的是未安裝在系統上的 MIDI 裝置。 使用主控台的 MIDI 對應程式來編輯安裝程式。 |
| MCIERR \_ SEQ \_ PORT \_ MISCERROR   | 指定的埠發生錯誤。                                                                                                                   |
| MCIERR \_ SEQ \_ 埠不 \_ 存在 | 系統上未安裝指定的 MIDI 裝置。 使用主控台的 [驅動程式] 選項來安裝 MIDI 裝置。                        |
| MCIERR \_ SEQ \_ PORTUNSPECIFIED   | 系統未指定目前的 MIDI 埠。                                                                                                  |
| MCIERR \_ SEQ \_ 計時器             | 所有的多媒體計時器都是由其他應用程式使用中。 結束其中一個應用程式;然後再試一次。                                             |



 

 

 




