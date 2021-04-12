---
title: IAgentCommands 移除
description: IAgentCommands 移除
ms.assetid: 1f41aa2d-e50b-48a8-87fc-fda4730b035a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d0c3321de3d06b5e2ebea873a4bace91482d8c5
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104185693"
---
# <a name="iagentcommandsremove"></a><span data-ttu-id="b8800-103">IAgentCommands：： Remove</span><span class="sxs-lookup"><span data-stu-id="b8800-103">IAgentCommands::Remove</span></span>

<span data-ttu-id="b8800-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="b8800-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT Remove(
   long dwID  // Command ID
);
```

<span data-ttu-id="b8800-105">從 [**命令**](/windows/desktop/lwef/the-commands-collection-object)集合中移除指定的 [**命令**](/windows/desktop/lwef/the-command-object)。</span><span class="sxs-lookup"><span data-stu-id="b8800-105">Removes the specified [**Command**](/windows/desktop/lwef/the-command-object) from a [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection.</span></span>

-   <span data-ttu-id="b8800-106">傳回 \_ [確定] 表示作業成功。</span><span class="sxs-lookup"><span data-stu-id="b8800-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="b8800-107"><span id="dwID"></span><span id="dwid"></span><span id="DWID"></span>*dwID*</span><span class="sxs-lookup"><span data-stu-id="b8800-107"><span id="dwID"></span><span id="dwid"></span><span id="DWID"></span>*dwID*</span></span>
</dt> <dd>

<span data-ttu-id="b8800-108">要從 [**命令**](/windows/desktop/lwef/the-commands-collection-object)集合中移除之 [**命令**](/windows/desktop/lwef/the-command-object)的識別碼。</span><span class="sxs-lookup"><span data-stu-id="b8800-108">The ID of a [**Command**](/windows/desktop/lwef/the-command-object) to remove from the [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection.</span></span>

</dd> </dl>

<span data-ttu-id="b8800-109">從 [**命令**](/windows/desktop/lwef/the-commands-collection-object)集合移除 [**命令**](/windows/desktop/lwef/the-command-object)，也會在您的應用程式為輸入-主動時，從快顯功能表和 [**語音命令] 視窗** 中移除它。</span><span class="sxs-lookup"><span data-stu-id="b8800-109">Removing a [**Command**](/windows/desktop/lwef/the-command-object) from a [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection also removes it from the pop-up menu and the **Voice Commands Window** when your application is input-active.</span></span>

## <a name="see-also"></a><span data-ttu-id="b8800-110">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b8800-110">See Also</span></span>

<span data-ttu-id="b8800-111">[**IAgentCommands：： Add**](iagentcommands--add.md)、 [**IAgentCommands：： Insert**](iagentcommands--insert.md)、 [**IAgentCommands：： RemoveAll**](iagentcommands--removeall.md)</span><span class="sxs-lookup"><span data-stu-id="b8800-111">[**IAgentCommands::Add**](iagentcommands--add.md), [**IAgentCommands::Insert**](iagentcommands--insert.md), [**IAgentCommands::RemoveAll**](iagentcommands--removeall.md)</span></span>


 

 