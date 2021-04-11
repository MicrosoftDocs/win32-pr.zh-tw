---
title: IAgentCharacter 中斷
description: IAgentCharacter 中斷
ms.assetid: ae05d317-e2d9-4d11-a6df-f9b25e43467a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17c9f19f716b15a48ec3cdb064aa4c0fdbbd1774
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "103933102"
---
# <a name="iagentcharacterinterrupt"></a><span data-ttu-id="93697-103">IAgentCharacter：：中斷</span><span class="sxs-lookup"><span data-stu-id="93697-103">IAgentCharacter::Interrupt</span></span>

<span data-ttu-id="93697-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="93697-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT Interrupt(
   long dwReqID,    // request ID to interrupt
   long * pdwReqID  // address of request ID
);
```

<span data-ttu-id="93697-105">中斷指定的動畫 (要求另一個字元) 。</span><span class="sxs-lookup"><span data-stu-id="93697-105">Interrupts the specified animation (request) of another character.</span></span>

-   <span data-ttu-id="93697-106">傳回 \_ [確定] 表示作業成功。</span><span class="sxs-lookup"><span data-stu-id="93697-106">Returns S\_OK to indicate the operation was successful.</span></span> <span data-ttu-id="93697-107">當函式傳回時， *pdwReqID* 會包含要求的識別碼。</span><span class="sxs-lookup"><span data-stu-id="93697-107">When the function returns, *pdwReqID* contains the ID of the request.</span></span>

<dl> <dt>

<span data-ttu-id="93697-108"><span id="dwReqID"></span><span id="dwreqid"></span><span id="DWREQID"></span>*dwReqID*</span><span class="sxs-lookup"><span data-stu-id="93697-108"><span id="dwReqID"></span><span id="dwreqid"></span><span id="DWREQID"></span>*dwReqID*</span></span>
</dt> <dd>

<span data-ttu-id="93697-109">要中斷之要求的識別碼。</span><span class="sxs-lookup"><span data-stu-id="93697-109">An ID of the request to interrupt.</span></span>

</dd> <dt>

<span data-ttu-id="93697-110"><span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwReqID*</span><span class="sxs-lookup"><span data-stu-id="93697-110"><span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwReqID*</span></span>
</dt> <dd>

<span data-ttu-id="93697-111">接收 **中斷** 要求識別碼之變數的位址。</span><span class="sxs-lookup"><span data-stu-id="93697-111">Address of a variable that receives the **Interrupt** request ID.</span></span>

</dd> </dl>

<span data-ttu-id="93697-112">如果您載入多個字元，您可以使用這個方法來同步處理字元之間的動畫。</span><span class="sxs-lookup"><span data-stu-id="93697-112">If you load multiple characters, you can use this method to sync up animation between characters.</span></span> <span data-ttu-id="93697-113">例如，如果有另一個字元在迴圈動畫中，此方法將會停止迴圈動畫，並啟動字元佇列中的下一個動畫。</span><span class="sxs-lookup"><span data-stu-id="93697-113">For example, if another character is in a looping animation, this method will stop the looping animation and start the next animation in the character's queue.</span></span>

<span data-ttu-id="93697-114">**中斷** 會中止現有的動畫，但不會排清字元的動畫佇列。</span><span class="sxs-lookup"><span data-stu-id="93697-114">**Interrupt** halts the existing animation, but does not flush the character's animation queue.</span></span> <span data-ttu-id="93697-115">它會啟動字元佇列中的下一個動畫。</span><span class="sxs-lookup"><span data-stu-id="93697-115">It starts the next animation in the character's queue.</span></span> <span data-ttu-id="93697-116">若要停止並清除字元的佇列，請使用 [**Stop**](/windows/desktop/lwef/iagentcharacter--stop) 方法。</span><span class="sxs-lookup"><span data-stu-id="93697-116">To halt and flush a character's queue, use the [**Stop**](/windows/desktop/lwef/iagentcharacter--stop) method.</span></span>

<span data-ttu-id="93697-117">您無法使用這個方法來讓字元中斷本身，因為 Microsoft 代理程式伺服器會將 **中斷** 方法排入字元的動畫佇列中。</span><span class="sxs-lookup"><span data-stu-id="93697-117">You cannot use this method to have a character interrupt itself because the Microsoft Agent server queues the **Interrupt** method in the character's animation queue.</span></span> <span data-ttu-id="93697-118">因此，您只能使用插 **斷來停止** 已載入之另一個字元的動畫。</span><span class="sxs-lookup"><span data-stu-id="93697-118">Therefore, you can only use **Interrupt** to halt the animation of another character you have loaded.</span></span>

 

 