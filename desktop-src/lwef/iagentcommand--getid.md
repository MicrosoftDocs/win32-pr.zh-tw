---
title: IAgentCommand GetID
description: IAgentCommand GetID
ms.assetid: 4d8d8be7-7003-4ef3-abba-b5232267c993
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d1f5887123df19496c0610c53fe59a3f64961cd
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104374996"
---
# <a name="iagentcommandgetid"></a><span data-ttu-id="91de4-103">IAgentCommand：： GetID</span><span class="sxs-lookup"><span data-stu-id="91de4-103">IAgentCommand::GetID</span></span>

<span data-ttu-id="91de4-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="91de4-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetID(
   long * pdwID  // address of ID for Command
);
```

<span data-ttu-id="91de4-105">抓取 [**命令**](/windows/desktop/lwef/the-command-object)的識別碼。</span><span class="sxs-lookup"><span data-stu-id="91de4-105">Retrieves the ID for a [**Command**](/windows/desktop/lwef/the-command-object).</span></span>

-   <span data-ttu-id="91de4-106">傳回 \_ [確定] 表示作業成功。</span><span class="sxs-lookup"><span data-stu-id="91de4-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="91de4-107"><span id="pdwID"></span><span id="pdwid"></span><span id="PDWID"></span>*pdwID*</span><span class="sxs-lookup"><span data-stu-id="91de4-107"><span id="pdwID"></span><span id="pdwid"></span><span id="PDWID"></span>*pdwID*</span></span>
</dt> <dd>

<span data-ttu-id="91de4-108">接收 [**命令**](/windows/desktop/lwef/the-command-object)識別碼之變數的位址。</span><span class="sxs-lookup"><span data-stu-id="91de4-108">The address of a variable that receives the ID of a [**Command**](/windows/desktop/lwef/the-command-object).</span></span>

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="91de4-109">另請參閱</span><span class="sxs-lookup"><span data-stu-id="91de4-109">See Also</span></span>

<span data-ttu-id="91de4-110">[**IAgentCommands：： Add**](iagentcommands--add.md)、 [**IAgentCommands：： Insert**](iagentcommands--insert.md)、 [**IAgentCommands：： Remove**](iagentcommands--remove.md)</span><span class="sxs-lookup"><span data-stu-id="91de4-110">[**IAgentCommands::Add**](iagentcommands--add.md), [**IAgentCommands::Insert**](iagentcommands--insert.md), [**IAgentCommands::Remove**](iagentcommands--remove.md)</span></span>


 

 