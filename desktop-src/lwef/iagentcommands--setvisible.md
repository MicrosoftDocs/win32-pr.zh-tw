---
title: IAgentCommands SetVisible
description: IAgentCommands SetVisible
ms.assetid: 4b99989a-29bb-4e0e-8155-cf734cc667fd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04a4bdb3c1a7f1e11c9548eb1e1af415d0f5d18f
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "106979664"
---
# <a name="iagentcommandssetvisible"></a><span data-ttu-id="521a5-103">IAgentCommands::SetVisible</span><span class="sxs-lookup"><span data-stu-id="521a5-103">IAgentCommands::SetVisible</span></span>

<span data-ttu-id="521a5-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="521a5-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetVisible(
   long bVisible  // the Visible setting for Commands collection
);
```

<span data-ttu-id="521a5-105">設定 [**命令**](/windows/desktop/lwef/the-commands-collection-object)集合的 [**Visible**](visible-property.md)屬性值。</span><span class="sxs-lookup"><span data-stu-id="521a5-105">Sets the value of the [**Visible**](visible-property.md) property for a [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection.</span></span>

-   <span data-ttu-id="521a5-106">傳回 \_ [確定] 表示作業成功。</span><span class="sxs-lookup"><span data-stu-id="521a5-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="521a5-107"><span id="bVisible"></span><span id="bvisible"></span><span id="BVISIBLE"></span>*bVisible*</span><span class="sxs-lookup"><span data-stu-id="521a5-107"><span id="bVisible"></span><span id="bvisible"></span><span id="BVISIBLE"></span>*bVisible*</span></span>
</dt> <dd>

<span data-ttu-id="521a5-108">布林值，決定 [**命令**](/windows/desktop/lwef/the-commands-collection-object)集合的 [**Visible**](visible-property.md)屬性。</span><span class="sxs-lookup"><span data-stu-id="521a5-108">A Boolean value that determines the [**Visible**](visible-property.md) property of a [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection.</span></span> <span data-ttu-id="521a5-109">**True** 會在顯示字元的快顯功能表時，將 **命令** 集合的 [**標題**](caption-property.md) 設為可見。 *False* 不會顯示它。</span><span class="sxs-lookup"><span data-stu-id="521a5-109">**True** sets the **Commands** collection's [**Caption**](caption-property.md) to be visible when the character's pop-up menu is displayed; *False* does not display it.</span></span>

</dd> </dl>

<span data-ttu-id="521a5-110">[**命令**](/windows/desktop/lwef/the-commands-collection-object)集合必須設定 [**標題**](caption-property.md)屬性，並將其 [**Visible**](visible-property.md)屬性設定為 **True** ，才會出現在字元的快顯功能表上。</span><span class="sxs-lookup"><span data-stu-id="521a5-110">A [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection must have its [**Caption**](caption-property.md) property set and its [**Visible**](visible-property.md) property set to **True** to appear on the character's pop-up menu.</span></span> <span data-ttu-id="521a5-111">當您的用戶端應用程式為輸入-主動時，[ **可見** ] 屬性也必須設定為 [ **True** ]，才能讓集合中的命令出現。</span><span class="sxs-lookup"><span data-stu-id="521a5-111">The **Visible** property must also be set to **True** for commands in the collection to appear when your client application is input-active.</span></span>

## <a name="see-also"></a><span data-ttu-id="521a5-112">另請參閱</span><span class="sxs-lookup"><span data-stu-id="521a5-112">See Also</span></span>

<span data-ttu-id="521a5-113">[**IAgentCommands：： GetVisible**](iagentcommands--getvisible.md)、 [ **IAgentCommand：： SetCaption**](iagentcommand--setcaption.md)</span><span class="sxs-lookup"><span data-stu-id="521a5-113">[**IAgentCommands::GetVisible**](iagentcommands--getvisible.md), [**IAgentCommand::SetCaption**](iagentcommand--setcaption.md)</span></span>


 

 