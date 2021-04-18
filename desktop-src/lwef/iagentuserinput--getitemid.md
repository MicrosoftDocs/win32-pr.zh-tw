---
title: IAgentUserInput GetItemID
description: IAgentUserInput GetItemID
ms.assetid: 3afd4d9d-51bb-4086-bf7b-7c9a2ddcd807
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 716ae1386d87fa6051111801c5603837519eeb4c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106965350"
---
# <a name="iagentuserinputgetitemid"></a><span data-ttu-id="a501b-103">IAgentUserInput::GetItemID</span><span class="sxs-lookup"><span data-stu-id="a501b-103">IAgentUserInput::GetItemID</span></span>

<span data-ttu-id="a501b-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="a501b-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetItemID(
   long dwItemIndex,    // index of Command alternative
   long * pdwCommandID  // address of a variable for number of alternatives 
);
```

<span data-ttu-id="a501b-105">抓取傳遞給 [**IAgentNotifySink：： command**](iagentnotifysink--command.md)回呼的 [**命令**](command-event.md)替代識別碼。</span><span class="sxs-lookup"><span data-stu-id="a501b-105">Retrieves the identifier of a [**Command**](command-event.md) alternative passed to an [**IAgentNotifySink::Command**](iagentnotifysink--command.md) callback.</span></span>

-   <span data-ttu-id="a501b-106">傳回 \_ [確定] 表示作業成功。</span><span class="sxs-lookup"><span data-stu-id="a501b-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="a501b-107"><span id="dwItemIndex"></span><span id="dwitemindex"></span><span id="DWITEMINDEX"></span>*dwItemIndex*</span><span class="sxs-lookup"><span data-stu-id="a501b-107"><span id="dwItemIndex"></span><span id="dwitemindex"></span><span id="DWITEMINDEX"></span>*dwItemIndex*</span></span>
</dt> <dd>

<span data-ttu-id="a501b-108">傳遞至 [**IAgentNotifySink：： command**](iagentnotifysink--command.md)回呼的 [**命令**](command-event.md)替代索引。</span><span class="sxs-lookup"><span data-stu-id="a501b-108">The index of the [**Command**](command-event.md) alternative passed to the [**IAgentNotifySink::Command**](iagentnotifysink--command.md) callback.</span></span>

</dd> <dt>

<span data-ttu-id="a501b-109"><span id="pdwCommandID"></span><span id="pdwcommandid"></span><span id="PDWCOMMANDID"></span>*pdwCommandID*</span><span class="sxs-lookup"><span data-stu-id="a501b-109"><span id="pdwCommandID"></span><span id="pdwcommandid"></span><span id="PDWCOMMANDID"></span>*pdwCommandID*</span></span>
</dt> <dd>

<span data-ttu-id="a501b-110">接收 [**命令**](command-event.md)識別碼之變數的位址。</span><span class="sxs-lookup"><span data-stu-id="a501b-110">Address of a variable that receives the ID of a [**Command**](command-event.md).</span></span>

</dd> </dl>

<span data-ttu-id="a501b-111">如果語音輸入觸發 [**IAgentNotifySink：： Command**](iagentnotifysink--command.md) 回呼，伺服器會傳回您應用程式所定義之任何相符 [**命令**](command-event.md) 的識別碼。</span><span class="sxs-lookup"><span data-stu-id="a501b-111">If voice input triggers the [**IAgentNotifySink::Command**](iagentnotifysink--command.md) callback, the server returns the IDs for any matching [**Commands**](command-event.md) defined by your application.</span></span>

## <a name="see-also"></a><span data-ttu-id="a501b-112">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a501b-112">See Also</span></span>

<span data-ttu-id="a501b-113">[**IAgentUserInput：： GetItemConfidence**](iagentuserinput--getitemconfidence.md)、 [**IAgentUserInput：： GetItemText**](iagentuserinput--getitemtext.md)、 [**IAgentUserInput：： GetAllItemData**](iagentuserinput--getallitemdata.md)</span><span class="sxs-lookup"><span data-stu-id="a501b-113">[**IAgentUserInput::GetItemConfidence**](iagentuserinput--getitemconfidence.md), [**IAgentUserInput::GetItemText**](iagentuserinput--getitemtext.md), [**IAgentUserInput::GetAllItemData**](iagentuserinput--getallitemdata.md)</span></span>


 

 




