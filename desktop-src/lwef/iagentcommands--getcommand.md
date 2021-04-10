---
title: IAgentCommands GetCommand
description: IAgentCommands GetCommand
ms.assetid: 0f4a9152-d5dc-4045-b469-8a03f0369e34
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e81043bb8dbe8a6d050f226d09f03b396d0f8f9
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104023467"
---
# <a name="iagentcommandsgetcommand"></a><span data-ttu-id="df091-103">IAgentCommands：： GetCommand</span><span class="sxs-lookup"><span data-stu-id="df091-103">IAgentCommands::GetCommand</span></span>

<span data-ttu-id="df091-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="df091-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetCommand(
   long dwCommandID,         // Command ID
   IUnknown ** ppunkCommand  // address of IUnknown interface
);                    
```

<span data-ttu-id="df091-105">從 [**命令**](/windows/desktop/lwef/the-commands-collection-object)集合中抓取 [**命令**](/windows/desktop/lwef/the-command-object)物件。</span><span class="sxs-lookup"><span data-stu-id="df091-105">Retrieves a [**Command**](/windows/desktop/lwef/the-command-object) object from the [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection.</span></span>

-   <span data-ttu-id="df091-106">傳回 \_ [確定] 表示作業成功。</span><span class="sxs-lookup"><span data-stu-id="df091-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="df091-107"><span id="dwCommandID"></span><span id="dwcommandid"></span><span id="DWCOMMANDID"></span>*dwCommandID*</span><span class="sxs-lookup"><span data-stu-id="df091-107"><span id="dwCommandID"></span><span id="dwcommandid"></span><span id="DWCOMMANDID"></span>*dwCommandID*</span></span>
</dt> <dd>

<span data-ttu-id="df091-108">[**命令集合中**](/windows/desktop/lwef/the-commands-collection-object)[**命令**](/windows/desktop/lwef/the-command-object)物件的識別碼。</span><span class="sxs-lookup"><span data-stu-id="df091-108">The ID of a [**Command**](/windows/desktop/lwef/the-command-object) object in the [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection.</span></span>

</dd> <dt>

<span data-ttu-id="df091-109"><span id="IUnknown"></span><span id="iunknown"></span><span id="IUNKNOWN"></span>*IUnknown*</span><span class="sxs-lookup"><span data-stu-id="df091-109"><span id="IUnknown"></span><span id="iunknown"></span><span id="IUNKNOWN"></span>*IUnknown*</span></span>
</dt> <dd>

<span data-ttu-id="df091-110">[**命令**](/windows/desktop/lwef/the-command-object)物件的 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面位址。</span><span class="sxs-lookup"><span data-stu-id="df091-110">The address of the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface for the [**Command**](/windows/desktop/lwef/the-command-object) object.</span></span>

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="df091-111">另請參閱</span><span class="sxs-lookup"><span data-stu-id="df091-111">See Also</span></span>

[<span data-ttu-id="df091-112">**IAgentCommand**</span><span class="sxs-lookup"><span data-stu-id="df091-112">**IAgentCommand**</span></span>](iagentcommand.md)


 

 