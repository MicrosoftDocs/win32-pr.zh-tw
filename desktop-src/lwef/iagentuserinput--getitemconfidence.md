---
title: IAgentUserInput GetItemConfidence
description: IAgentUserInput GetItemConfidence
ms.assetid: 7d1ca2f0-416c-43c3-99a8-9f287cb88de1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 846e1fca9ea1245a62fc68330d68263b63fb7cfd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104299979"
---
# <a name="iagentuserinputgetitemconfidence"></a><span data-ttu-id="270d3-103">IAgentUserInput::GetItemConfidence</span><span class="sxs-lookup"><span data-stu-id="270d3-103">IAgentUserInput::GetItemConfidence</span></span>

<span data-ttu-id="270d3-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="270d3-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetItemConfidence(
   long dwItemIndex,    // index of Command alternative
   long * plConfidence  // address of confidence value for Command 
);
```

<span data-ttu-id="270d3-105">抓取傳遞給 [**IAgentNotifySink：： command**](iagentnotifysink--command.md)回呼之 [**命令**](command-event.md)的信賴值。</span><span class="sxs-lookup"><span data-stu-id="270d3-105">Retrieves the confidence value for a [**Command**](command-event.md) passed to an [**IAgentNotifySink::Command**](iagentnotifysink--command.md) callback.</span></span>

-   <span data-ttu-id="270d3-106">傳回 \_ [確定] 表示作業成功。</span><span class="sxs-lookup"><span data-stu-id="270d3-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="270d3-107"><span id="dwItemIndex"></span><span id="dwitemindex"></span><span id="DWITEMINDEX"></span>*dwItemIndex*</span><span class="sxs-lookup"><span data-stu-id="270d3-107"><span id="dwItemIndex"></span><span id="dwitemindex"></span><span id="DWITEMINDEX"></span>*dwItemIndex*</span></span>
</dt> <dd>

<span data-ttu-id="270d3-108">傳遞至 [**IAgentNotifySink：： command**](iagentnotifysink--command.md)回呼的 [**命令**](command-event.md)替代索引。</span><span class="sxs-lookup"><span data-stu-id="270d3-108">The index of a [**Command**](command-event.md) alternative passed to the [**IAgentNotifySink::Command**](iagentnotifysink--command.md) callback.</span></span>

</dd> <dt>

<span data-ttu-id="270d3-109"><span id="plConfidence"></span><span id="plconfidence"></span><span id="PLCONFIDENCE"></span>*plConfidence*</span><span class="sxs-lookup"><span data-stu-id="270d3-109"><span id="plConfidence"></span><span id="plconfidence"></span><span id="PLCONFIDENCE"></span>*plConfidence*</span></span>
</dt> <dd>

<span data-ttu-id="270d3-110">接收傳給 [**IAgentNotifySink：： command**](iagentnotifysink--command.md)回呼的 [**命令**](command-event.md)替代項信賴分數的變數位址。</span><span class="sxs-lookup"><span data-stu-id="270d3-110">Address of a variable that receives the confidence score for a [**Command**](command-event.md) alternative passed to the [**IAgentNotifySink::Command**](iagentnotifysink--command.md) callback.</span></span>

</dd> </dl>

<span data-ttu-id="270d3-111">如果語音輸入不是命令的來源，例如，如果使用者從字元的快顯功能表中選取了命令，Microsoft 代理程式伺服器會將最佳相符專案的信賴值傳回為100，並將所有其他替代專案的信賴值傳回為零 (0) 。</span><span class="sxs-lookup"><span data-stu-id="270d3-111">If voice input was not the source for the command, for example, if the user selected the command from the character's pop-up menu, the Microsoft Agent server returns the confidence value of the best match as 100 and the confidence values for all other alternatives as zero (0).</span></span>

## <a name="see-also"></a><span data-ttu-id="270d3-112">另請參閱</span><span class="sxs-lookup"><span data-stu-id="270d3-112">See Also</span></span>

<span data-ttu-id="270d3-113">[**IAgentUserInput：： GetItemID**](iagentuserinput--getitemid.md)、 [**IAgentUserInput：： GetAllItemData**](iagentuserinput--getallitemdata.md)、 [**IAgentUserInput：： GetItemText**](iagentuserinput--getitemtext.md)</span><span class="sxs-lookup"><span data-stu-id="270d3-113">[**IAgentUserInput::GetItemID**](iagentuserinput--getitemid.md), [**IAgentUserInput::GetAllItemData**](iagentuserinput--getallitemdata.md), [**IAgentUserInput::GetItemText**](iagentuserinput--getitemtext.md)</span></span>


 

 




