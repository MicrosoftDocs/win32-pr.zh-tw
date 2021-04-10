---
title: IAgentCommand GetCaption
description: IAgentCommand GetCaption
ms.assetid: e333faca-e2c2-478a-a803-cbc401793e4d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b44540ba9105e79ba675f8bf78be20e8961f98d0
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "103842115"
---
# <a name="iagentcommandgetcaption"></a><span data-ttu-id="8a0a8-103">IAgentCommand::GetCaption</span><span class="sxs-lookup"><span data-stu-id="8a0a8-103">IAgentCommand::GetCaption</span></span>

<span data-ttu-id="8a0a8-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="8a0a8-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetCaption(
   BSTR * pbszCaption  // address of Caption for Command
);
```

<span data-ttu-id="8a0a8-105">抓取 [**命令**](/windows/desktop/lwef/the-command-object)的 [**標題**](caption-property.md)。</span><span class="sxs-lookup"><span data-stu-id="8a0a8-105">Retrieves the [**Caption**](caption-property.md) for a [**Command**](/windows/desktop/lwef/the-command-object).</span></span>

-   <span data-ttu-id="8a0a8-106">傳回 \_ [確定] 表示作業成功。</span><span class="sxs-lookup"><span data-stu-id="8a0a8-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="8a0a8-107"><span id="pbszCaption"></span><span id="pbszcaption"></span><span id="PBSZCAPTION"></span>*pbszCaption*</span><span class="sxs-lookup"><span data-stu-id="8a0a8-107"><span id="pbszCaption"></span><span id="pbszcaption"></span><span id="PBSZCAPTION"></span>*pbszCaption*</span></span>
</dt> <dd>

<span data-ttu-id="8a0a8-108">接收針對 [**命令**](/windows/desktop/lwef/the-command-object)顯示之 [**標題**](caption-property.md)文字值的 BSTR 位址。</span><span class="sxs-lookup"><span data-stu-id="8a0a8-108">The address of a BSTR that receives the value of the [**Caption**](caption-property.md) text displayed for a [**Command**](/windows/desktop/lwef/the-command-object).</span></span>

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="8a0a8-109">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8a0a8-109">See Also</span></span>

<span data-ttu-id="8a0a8-110">[**IAgentCommand：： SetCaption**](iagentcommand--setcaption.md)、 [**IAgentCommand：： SetEnabled**](iagentcommand--setenabled.md)、 [**IAgentCommand：： SetVisible**](iagentcommand--setvisible.md)、 [**IAgentCommand：： SetVoice**](iagentcommand--setvoice.md)、 [**IAgentCommands：： Add**](iagentcommands--add.md)、 [**IAgentCommands：： Insert**](iagentcommands--insert.md)</span><span class="sxs-lookup"><span data-stu-id="8a0a8-110">[**IAgentCommand::SetCaption**](iagentcommand--setcaption.md), [**IAgentCommand::SetEnabled**](iagentcommand--setenabled.md), [**IAgentCommand::SetVisible**](iagentcommand--setvisible.md), [**IAgentCommand::SetVoice**](iagentcommand--setvoice.md), [**IAgentCommands::Add**](iagentcommands--add.md), [**IAgentCommands::Insert**](iagentcommands--insert.md)</span></span>


 

 