---
title: IAgentCommand GetEnabled
description: IAgentCommand GetEnabled
ms.assetid: b4ec25d2-b2e0-4b1b-8dc5-10fbb44149b5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 238844a70ea7fde3ef0c07cad1a6f3abab5613d1
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104463052"
---
# <a name="iagentcommandgetenabled"></a><span data-ttu-id="c8a6d-103">IAgentCommand：： GetEnabled</span><span class="sxs-lookup"><span data-stu-id="c8a6d-103">IAgentCommand::GetEnabled</span></span>

<span data-ttu-id="c8a6d-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="c8a6d-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetEnabled(
   long * pbEnabled  // address of Enabled setting for Command
);
```

<span data-ttu-id="c8a6d-105">抓取 [**命令**](/windows/desktop/lwef/the-command-object)的 [**Enabled**](enabled-property.md)屬性值。</span><span class="sxs-lookup"><span data-stu-id="c8a6d-105">Retrieves the value of the [**Enabled**](enabled-property.md) property for a [**Command**](/windows/desktop/lwef/the-command-object).</span></span>

-   <span data-ttu-id="c8a6d-106">傳回 \_ [確定] 表示作業成功。</span><span class="sxs-lookup"><span data-stu-id="c8a6d-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="c8a6d-107"><span id="pbEnabled"></span><span id="pbenabled"></span><span id="PBENABLED"></span>*pbEnabled*</span><span class="sxs-lookup"><span data-stu-id="c8a6d-107"><span id="pbEnabled"></span><span id="pbenabled"></span><span id="PBENABLED"></span>*pbEnabled*</span></span>
</dt> <dd>

<span data-ttu-id="c8a6d-108">如果已啟用 [**命令**](/windows/desktop/lwef/the-command-object)，則為收到 **True** 之變數的位址，如果已停用，則為 **False** 。</span><span class="sxs-lookup"><span data-stu-id="c8a6d-108">The address of a variable that receives **True** if the [**Command**](/windows/desktop/lwef/the-command-object) is enabled, or **False** if it is disabled.</span></span> <span data-ttu-id="c8a6d-109">無法選取已停用的 **命令** 。</span><span class="sxs-lookup"><span data-stu-id="c8a6d-109">A disabled **Command** cannot be selected.</span></span>

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="c8a6d-110">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c8a6d-110">See Also</span></span>

<span data-ttu-id="c8a6d-111">[**IAgentCommand：： SetCaption**](iagentcommand--setcaption.md)、 [**IAgentCommand：： SetVisible**](iagentcommand--setvisible.md)、 [**IAgentCommand：： SetVoice**](iagentcommand--setvoice.md)、 [**IAgentCommands：： Add**](iagentcommands--add.md)、 [**IAgentCommands：： Insert**](iagentcommands--insert.md)</span><span class="sxs-lookup"><span data-stu-id="c8a6d-111">[**IAgentCommand::SetCaption**](iagentcommand--setcaption.md), [**IAgentCommand::SetVisible**](iagentcommand--setvisible.md), [**IAgentCommand::SetVoice**](iagentcommand--setvoice.md), [**IAgentCommands::Add**](iagentcommands--add.md), [**IAgentCommands::Insert**](iagentcommands--insert.md)</span></span>


 

 