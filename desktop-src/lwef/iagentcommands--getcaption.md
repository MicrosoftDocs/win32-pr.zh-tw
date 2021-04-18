---
title: IAgentCommands GetCaption
description: IAgentCommands GetCaption
ms.assetid: bbaaaa20-c8c2-41af-a6fc-cf8849daa399
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f886413ae6bfbfe104306d7280d8c66b08bf311a
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "106968489"
---
# <a name="iagentcommandsgetcaption"></a><span data-ttu-id="8070a-103">IAgentCommands::GetCaption</span><span class="sxs-lookup"><span data-stu-id="8070a-103">IAgentCommands::GetCaption</span></span>

<span data-ttu-id="8070a-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="8070a-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetCaption(
   BSTR * pbszCaption  // address of Caption text for Commands collection
);
```

<span data-ttu-id="8070a-105">抓取 [**命令**](/windows/desktop/lwef/the-commands-collection-object)集合的 [**標題**](caption-property.md)。</span><span class="sxs-lookup"><span data-stu-id="8070a-105">Retrieves the [**Caption**](caption-property.md) for a [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection.</span></span>

-   <span data-ttu-id="8070a-106">傳回 \_ [確定] 表示作業成功。</span><span class="sxs-lookup"><span data-stu-id="8070a-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="8070a-107"><span id="pbszCaption"></span><span id="pbszcaption"></span><span id="PBSZCAPTION"></span>*pbszCaption*</span><span class="sxs-lookup"><span data-stu-id="8070a-107"><span id="pbszCaption"></span><span id="pbszcaption"></span><span id="PBSZCAPTION"></span>*pbszCaption*</span></span>
</dt> <dd>

<span data-ttu-id="8070a-108">BSTR 的位址，這個位址會接收針對 [**命令**](/windows/desktop/lwef/the-commands-collection-object)集合顯示之 [**標題**](caption-property.md)文字設定的值。</span><span class="sxs-lookup"><span data-stu-id="8070a-108">The address of a BSTR that receives the value of the [**Caption**](caption-property.md) text setting displayed for a [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection.</span></span>

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="8070a-109">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8070a-109">See Also</span></span>

<span data-ttu-id="8070a-110">[**IAgentCommands：： SetCaption**](iagentcommands--setcaption.md)、 [**IAgentCommands：： GetVisible**](iagentcommands--getvisible.md)、 [**IAgentCommands：： GetVoice**](iagentcommands--getvoice.md)</span><span class="sxs-lookup"><span data-stu-id="8070a-110">[**IAgentCommands::SetCaption**](iagentcommands--setcaption.md), [**IAgentCommands::GetVisible**](iagentcommands--getvisible.md), [**IAgentCommands::GetVoice**](iagentcommands--getvoice.md)</span></span>


 

 