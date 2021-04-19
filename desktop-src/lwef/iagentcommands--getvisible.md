---
title: IAgentCommands GetVisible
description: IAgentCommands GetVisible
ms.assetid: 229a02c8-f0a1-4ee5-9bae-961b63792038
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 853a47f6136779415a08adc3c891d9b5cc95dcca
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "106999795"
---
# <a name="iagentcommandsgetvisible"></a><span data-ttu-id="25a78-103">IAgentCommands：： GetVisible</span><span class="sxs-lookup"><span data-stu-id="25a78-103">IAgentCommands::GetVisible</span></span>

<span data-ttu-id="25a78-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="25a78-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetVisible(
   long * pbVisible  // address of Visible setting for Commands collection
);
```

<span data-ttu-id="25a78-105">抓取 [**命令**](/windows/desktop/lwef/the-commands-collection-object)集合的 [**Visible**](visible-property.md)屬性值。</span><span class="sxs-lookup"><span data-stu-id="25a78-105">Retrieves the value of the [**Visible**](visible-property.md) property for a [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection.</span></span>

-   <span data-ttu-id="25a78-106">傳回 \_ [確定] 表示作業成功。</span><span class="sxs-lookup"><span data-stu-id="25a78-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="25a78-107"><span id="pbVisible"></span><span id="pbvisible"></span><span id="PBVISIBLE"></span>*pbVisible*</span><span class="sxs-lookup"><span data-stu-id="25a78-107"><span id="pbVisible"></span><span id="pbvisible"></span><span id="PBVISIBLE"></span>*pbVisible*</span></span>
</dt> <dd>

<span data-ttu-id="25a78-108">接收 [**命令**](/windows/desktop/lwef/the-commands-collection-object)集合之 [**Visible**](visible-property.md)屬性值的變數位址。</span><span class="sxs-lookup"><span data-stu-id="25a78-108">The address of a variable that receives the value of the [**Visible**](visible-property.md) property for a [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection.</span></span>

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="25a78-109">另請參閱</span><span class="sxs-lookup"><span data-stu-id="25a78-109">See Also</span></span>

<span data-ttu-id="25a78-110">[**IAgentCommands：： SetVisible**](iagentcommands--setvisible.md)、 [ **IAgentCommands：： SetCaption**](iagentcommands--setcaption.md)</span><span class="sxs-lookup"><span data-stu-id="25a78-110">[**IAgentCommands::SetVisible**](iagentcommands--setvisible.md), [**IAgentCommands::SetCaption**](iagentcommands--setcaption.md)</span></span>


 

 