---
title: IAgentCommands GetCount
description: IAgentCommands GetCount
ms.assetid: 17140eda-17b0-49c2-8d50-5a38a553191a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65ece3e007b644b370ee721cef2d273fa50d43ce
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104374961"
---
# <a name="iagentcommandsgetcount"></a><span data-ttu-id="37d9b-103">IAgentCommands：： GetCount</span><span class="sxs-lookup"><span data-stu-id="37d9b-103">IAgentCommands::GetCount</span></span>

<span data-ttu-id="37d9b-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="37d9b-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetCount(
   long * pdwCount  // address of count of commands
);                    
```

<span data-ttu-id="37d9b-105">抓取 [**命令**](/windows/desktop/lwef/the-commands-collection-object)集合中的 [**命令**](/windows/desktop/lwef/the-command-object)物件數目。</span><span class="sxs-lookup"><span data-stu-id="37d9b-105">Retrieves the number of [**Command**](/windows/desktop/lwef/the-command-object) objects in a [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection.</span></span>

-   <span data-ttu-id="37d9b-106">傳回 \_ [確定] 表示作業成功。</span><span class="sxs-lookup"><span data-stu-id="37d9b-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="37d9b-107"><span id="pdwCount"></span><span id="pdwcount"></span><span id="PDWCOUNT"></span>*pdwCount*</span><span class="sxs-lookup"><span data-stu-id="37d9b-107"><span id="pdwCount"></span><span id="pdwcount"></span><span id="PDWCOUNT"></span>*pdwCount*</span></span>
</dt> <dd>

<span data-ttu-id="37d9b-108">接收 [**命令**](/windows/desktop/lwef/the-commands-collection-object)集合中 [**命令**](/windows/desktop/lwef/the-command-object)數目之變數的位址。</span><span class="sxs-lookup"><span data-stu-id="37d9b-108">Address of a variable that receives the number of [**Commands**](/windows/desktop/lwef/the-command-object) in a [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection.</span></span>

</dd> </dl>

<span data-ttu-id="37d9b-109">*pdwCount* 僅包含您在 [**命令**](/windows/desktop/lwef/the-commands-collection-object)集合中定義的 [**命令**](/windows/desktop/lwef/the-command-object)數目。</span><span class="sxs-lookup"><span data-stu-id="37d9b-109">*pdwCount* includes only the number of [**Commands**](/windows/desktop/lwef/the-command-object) you define in your [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection.</span></span> <span data-ttu-id="37d9b-110">不包含伺服器或其他用戶端專案。</span><span class="sxs-lookup"><span data-stu-id="37d9b-110">Server or other client entries are not included.</span></span>

 

 