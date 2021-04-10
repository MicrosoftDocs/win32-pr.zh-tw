---
title: IAgentUserInput GetCount
description: IAgentUserInput GetCount
ms.assetid: 9c127387-b680-405a-9a62-ee08cc70813a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ac4b597f7367eff10154bde256698ef371c3619
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104182932"
---
# <a name="iagentuserinputgetcount"></a><span data-ttu-id="55a12-103">IAgentUserInput：： GetCount</span><span class="sxs-lookup"><span data-stu-id="55a12-103">IAgentUserInput::GetCount</span></span>

<span data-ttu-id="55a12-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="55a12-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetCount(
   long * pdwCount  // address of a variable for number of alternatives 
);
```

<span data-ttu-id="55a12-105">抓取傳遞給 [**IAgentNotifySink：： command**](iagentnotifysink--command.md)回呼的 [**命令**](command-event.md)替代專案數目。</span><span class="sxs-lookup"><span data-stu-id="55a12-105">Retrieves the number of [**Command**](command-event.md) alternatives passed to an [**IAgentNotifySink::Command**](iagentnotifysink--command.md) callback.</span></span>

-   <span data-ttu-id="55a12-106">傳回 \_ [確定] 表示作業成功。</span><span class="sxs-lookup"><span data-stu-id="55a12-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="55a12-107"><span id="pdwCount"></span><span id="pdwcount"></span><span id="PDWCOUNT"></span>*pdwCount*</span><span class="sxs-lookup"><span data-stu-id="55a12-107"><span id="pdwCount"></span><span id="pdwcount"></span><span id="PDWCOUNT"></span>*pdwCount*</span></span>
</dt> <dd>

<span data-ttu-id="55a12-108">接收伺服器所識別的 [**命令**](command-event.md) 替代專案計數之變數的位址。</span><span class="sxs-lookup"><span data-stu-id="55a12-108">Address of a variable that receives the count of [**Commands**](command-event.md) alternatives identified by the server.</span></span>

</dd> </dl>

<span data-ttu-id="55a12-109">如果語音輸入不是命令的來源，例如，如果使用者從字元的快顯功能表中選取了命令， **GetCount** 會傳回1。</span><span class="sxs-lookup"><span data-stu-id="55a12-109">If voice input was not the source for the command, for example, if the user selected the command from the character's pop-up menu, **GetCount** returns 1.</span></span> <span data-ttu-id="55a12-110">如果 **GetCount** 傳回零 (0) ，語音辨識引擎會偵測到說話輸入，但卻判斷沒有相符的命令。</span><span class="sxs-lookup"><span data-stu-id="55a12-110">If **GetCount** returns zero (0), the speech recognition engine detected spoken input but determined that there was no matching command.</span></span>

 

 




