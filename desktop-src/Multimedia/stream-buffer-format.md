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
# <a name="stream-buffer-format"></a><span data-ttu-id="454aa-108">資料流程緩衝區格式</span><span class="sxs-lookup"><span data-stu-id="454aa-108">Stream Buffer Format</span></span>

<span data-ttu-id="454aa-109">[**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr)結構的 **lpData** 成員指向資料流程緩衝區，而 **dwbufferlength 相關聯** 成員則指定此緩衝區的實際大小。</span><span class="sxs-lookup"><span data-stu-id="454aa-109">The **lpData** member of the [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) structure points to a stream buffer, and the **dwBufferLength** member specifies the actual size of this buffer.</span></span> <span data-ttu-id="454aa-110">**MIDIHDR** 的 **dwBytesRecorded** 成員會指定由 MIDI 事件實際使用之緩衝區中的位元組數目;這個值必須小於或等於 **dwbufferlength 相關聯** 所指定的值。</span><span class="sxs-lookup"><span data-stu-id="454aa-110">The **dwBytesRecorded** member of **MIDIHDR** specifies the number of bytes in the buffer that are actually used by the MIDI events; this value must be less than or equal to the value specified by **dwBufferLength**.</span></span>

<span data-ttu-id="454aa-111">資料流程緩衝區中的每個 MIDI 事件都是由 [**MIDIEVENT**](/windows/win32/api/mmeapi/ns-mmeapi-midievent) 結構所指定，其中包含事件的時間、資料流程識別碼、事件代碼，以及事件的參數（如果有的話）。</span><span class="sxs-lookup"><span data-stu-id="454aa-111">Each of the MIDI events in the stream buffer is specified by a [**MIDIEVENT**](/windows/win32/api/mmeapi/ns-mmeapi-midievent) structure, which contains the time for the event, a stream identifier, an event code, and, when appropriate, parameters for the event.</span></span> <span data-ttu-id="454aa-112">這些 **MIDIEVENT** 結構的每一個都必須以雙量的邊界開始。</span><span class="sxs-lookup"><span data-stu-id="454aa-112">Each of these **MIDIEVENT** structures must begin on a doubleword boundary.</span></span> <span data-ttu-id="454aa-113">如有必要，必須將填充位元組新增至結構的結尾，以確保下一個位元組會在雙位元組界限上開始。</span><span class="sxs-lookup"><span data-stu-id="454aa-113">If necessary, pad bytes must be added to the end of the structure to ensure that the next one starts on a doubleword boundary.</span></span>

 

 