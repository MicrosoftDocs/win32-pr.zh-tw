---
title: IAgentCommands RemoveAll
description: IAgentCommands RemoveAll
ms.assetid: fab43363-6325-4566-b7bb-599591f67321
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8bd374b7c5767c416d2c3bb2281e651ba71acd8
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "103682292"
---
# <a name="iagentcommandsremoveall"></a><span data-ttu-id="926c0-103">IAgentCommands：： RemoveAll</span><span class="sxs-lookup"><span data-stu-id="926c0-103">IAgentCommands::RemoveAll</span></span>

<span data-ttu-id="926c0-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="926c0-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT Remove();
```

<span data-ttu-id="926c0-105">從 [**命令**](/windows/desktop/lwef/the-commands-collection-object)集合中移除所有 [**命令**](/windows/desktop/lwef/the-command-object)。</span><span class="sxs-lookup"><span data-stu-id="926c0-105">Removes all [**Commands**](/windows/desktop/lwef/the-command-object) from a [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection.</span></span>

-   <span data-ttu-id="926c0-106">傳回 \_ [確定] 表示作業成功。</span><span class="sxs-lookup"><span data-stu-id="926c0-106">Returns S\_OK to indicate the operation was successful.</span></span>

<span data-ttu-id="926c0-107">從 [**命令**](/windows/desktop/lwef/the-commands-collection-object)集合移除所有 [**命令**](/windows/desktop/lwef/the-command-object)，也會在您的應用程式為輸入-主動時，從快顯功能表和 [**語音命令] 視窗** 中移除它們。</span><span class="sxs-lookup"><span data-stu-id="926c0-107">Removing all [**Commands**](/windows/desktop/lwef/the-command-object) from a [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection also removes them from the pop-up menu and the **Voice Commands Window** when your application is input-active.</span></span> <span data-ttu-id="926c0-108">**RemoveAll** 不會移除伺服器或其他用戶端的專案。</span><span class="sxs-lookup"><span data-stu-id="926c0-108">**RemoveAll** does not remove server or other client's entries.</span></span>

## <a name="see-also"></a><span data-ttu-id="926c0-109">另請參閱</span><span class="sxs-lookup"><span data-stu-id="926c0-109">See Also</span></span>

<span data-ttu-id="926c0-110">[**IAgentCommands：： Add**](iagentcommands--add.md)、 [**IAgentCommands：： Insert**](iagentcommands--insert.md)、 [**IAgentCommands：： Remove**](iagentcommands--remove.md)</span><span class="sxs-lookup"><span data-stu-id="926c0-110">[**IAgentCommands::Add**](iagentcommands--add.md), [**IAgentCommands::Insert**](iagentcommands--insert.md), [**IAgentCommands::Remove**](iagentcommands--remove.md)</span></span>


 

 