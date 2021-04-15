---
title: 資料流程緩衝區格式
description: 資料流程緩衝區格式
ms.assetid: 4b24c12e-b43f-492e-a000-af4f59d5e16f
keywords:
- 音樂檢測數位介面 (MIDI) 、串流緩衝區
- MIDI (音樂檢測數位介面) 、串流緩衝區
- 資料流程緩衝區，格式
- MIDIHDR 結構
- MIDIEVENT 結構
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 801a7f0dbeabd0d7aebeae0387af415a831e4658
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104374973"
---
# <a name="stream-buffer-format"></a>資料流程緩衝區格式

[**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr)結構的 **lpData** 成員指向資料流程緩衝區，而 **dwbufferlength 相關聯** 成員則指定此緩衝區的實際大小。 **MIDIHDR** 的 **dwBytesRecorded** 成員會指定由 MIDI 事件實際使用之緩衝區中的位元組數目;這個值必須小於或等於 **dwbufferlength 相關聯** 所指定的值。

資料流程緩衝區中的每個 MIDI 事件都是由 [**MIDIEVENT**](/windows/win32/api/mmeapi/ns-mmeapi-midievent) 結構所指定，其中包含事件的時間、資料流程識別碼、事件代碼，以及事件的參數（如果有的話）。 這些 **MIDIEVENT** 結構的每一個都必須以雙量的邊界開始。 如有必要，必須將填充位元組新增至結構的結尾，以確保下一個位元組會在雙位元組界限上開始。

 

 