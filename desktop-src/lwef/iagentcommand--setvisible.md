---
title: IAgentCommand SetVisible
description: IAgentCommand SetVisible
ms.assetid: 58a383f4-6c98-4037-b469-ae68f06c852d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b583f79a93a5b13914486fb3e1a9cb513a682e63
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "106965017"
---
# <a name="iagentcommandsetvisible"></a><span data-ttu-id="3549f-103">IAgentCommand::SetVisible</span><span class="sxs-lookup"><span data-stu-id="3549f-103">IAgentCommand::SetVisible</span></span>

<span data-ttu-id="3549f-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="3549f-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetVisible(
   long bVisible  // Visible setting for Command
);
```

<span data-ttu-id="3549f-105">設定 [**命令**](/windows/desktop/lwef/the-command-object)的 [**Visible**](visible-property.md)屬性值。</span><span class="sxs-lookup"><span data-stu-id="3549f-105">Sets the value of the [**Visible**](visible-property.md) property for a [**Command**](/windows/desktop/lwef/the-command-object).</span></span>

-   <span data-ttu-id="3549f-106">傳回 \_ [確定] 表示作業成功。</span><span class="sxs-lookup"><span data-stu-id="3549f-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="3549f-107"><span id="bVisible"></span><span id="bvisible"></span><span id="BVISIBLE"></span>*bVisible*</span><span class="sxs-lookup"><span data-stu-id="3549f-107"><span id="bVisible"></span><span id="bvisible"></span><span id="BVISIBLE"></span>*bVisible*</span></span>
</dt> <dd>

<span data-ttu-id="3549f-108">布林值，決定 [**命令**](/windows/desktop/lwef/the-command-object)的 [**Visible**](visible-property.md)屬性。</span><span class="sxs-lookup"><span data-stu-id="3549f-108">A Boolean value that determines the [**Visible**](visible-property.md) property of a [**Command**](/windows/desktop/lwef/the-command-object).</span></span> <span data-ttu-id="3549f-109">**True** 會顯示 **命令**; **False** 會隱藏它。</span><span class="sxs-lookup"><span data-stu-id="3549f-109">**True** shows the **Command**; **False** hides it.</span></span>

</dd> </dl>

<span data-ttu-id="3549f-110">[**命令**](/windows/desktop/lwef/the-command-object)的 [**Visible**](visible-property.md)屬性必須設定為 **True** ，而且其 [**標題**](caption-property.md)屬性設定為顯示在字元的快顯功能表中。</span><span class="sxs-lookup"><span data-stu-id="3549f-110">A [**Command**](/windows/desktop/lwef/the-command-object) must have its [**Visible**](visible-property.md) property set to **True** and its [**Caption**](caption-property.md) property set to appear in the character's pop-up menu.</span></span>

## <a name="see-also"></a><span data-ttu-id="3549f-111">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3549f-111">See Also</span></span>

<span data-ttu-id="3549f-112">[**IAgentCommand：： GetVisible**](iagentcommand--getvisible.md)、 [**IAgentCommand：： SetCaption**](iagentcommand--setcaption.md)、 [**IAgentCommands：： Add**](iagentcommands--add.md)、 [**IAgentCommands：： Insert**](iagentcommands--insert.md)</span><span class="sxs-lookup"><span data-stu-id="3549f-112">[**IAgentCommand::GetVisible**](iagentcommand--getvisible.md), [**IAgentCommand::SetCaption**](iagentcommand--setcaption.md), [**IAgentCommands::Add**](iagentcommands--add.md), [**IAgentCommands::Insert**](iagentcommands--insert.md)</span></span>


 

 