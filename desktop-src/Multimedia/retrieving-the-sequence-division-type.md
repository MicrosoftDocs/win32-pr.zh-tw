---
title: 正在抓取序列除法類型
description: 正在抓取序列除法類型
ms.assetid: 9c7e3482-93a3-4f9c-8b70-a9c733de14fe
keywords:
- 音樂檢測數位介面 (MIDI) ，序列除法類型
- MIDI (音樂檢測數位介面) ，序列除法類型
- MCI MIDI sequencer，除法類型
- MCI_STATUS 命令
- sequence 除法類型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81b28bb7e32097b888cdd3dec739eaccfc2a37dfe14060168fb11f0a7ca3d00e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117801802"
---
# <a name="retrieving-the-sequence-division-type"></a>正在抓取序列除法類型

MIDI 順序的 *部門型* 別決定了序列中的 MIDI 事件之間的時間長度。 若要判斷序列的除法類型，請使用 [**mci \_ status**](mci-status.md)命令，並將 [**mci \_ status \_ PARMS**](mci-status-parms.md)結構的 **dwItem** 成員設定為 mci \_ SEQ \_ status \_ DIVTYPE。

如果 **mci \_ status** 命令成功， **mci \_ status \_ PARMS** 結構的 **dwReturn** 成員會包含下列其中一個值，以指出除法類型。



| 值                        | 除法類型                     |
|------------------------------|-----------------------------------|
| MCI \_ SEQ \_ DIV \_ PPQN          | PPQN (部分-每季附注)      |
| MCI \_ SEQ \_ DIV （ \_ SMPTE \_ 24）     | SMPTE，每秒 24 fps (畫面)  |
| MCI \_ SEQ \_ DIV 的 \_ SMPTE \_ 25     | SMPTE，25 fps                     |
| MCI \_ SEQ \_ DIV \_ \_ 30     | SMPTE，30 fps                     |
| MCI \_ SEQ \_ DIV \_ SMPTE \_ 30DROP | SMPTE，30 fps 捨棄框架          |



 

您必須知道順序的除法類型才能變更或查詢其節奏。 您無法使用 MCI sequencer 來變更序列的除法類型。

 

 




