---
title: IAgentCharacter GetVisible
description: IAgentCharacter GetVisible
ms.assetid: 6e8e3a68-a7bb-4afb-a753-836fe82a0b24
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0593b9b3a193b9d5910888b81b4ecba90469b1e
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104092654"
---
# <a name="iagentcharactergetvisible"></a><span data-ttu-id="dc762-103">IAgentCharacter：： GetVisible</span><span class="sxs-lookup"><span data-stu-id="dc762-103">IAgentCharacter::GetVisible</span></span>

<span data-ttu-id="dc762-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="dc762-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetVisible(
   long * pbVisible  // address of variable for character Visible setting
);
```

<span data-ttu-id="dc762-105">判斷字元的動畫框架目前是否可見。</span><span class="sxs-lookup"><span data-stu-id="dc762-105">Determines whether the character's animation frame is currently visible.</span></span>

-   <span data-ttu-id="dc762-106">傳回 \_ [確定] 表示作業成功。</span><span class="sxs-lookup"><span data-stu-id="dc762-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="dc762-107"><span id="pbVisible"></span><span id="pbvisible"></span><span id="PBVISIBLE"></span>*pbVisible*</span><span class="sxs-lookup"><span data-stu-id="dc762-107"><span id="pbVisible"></span><span id="pbvisible"></span><span id="PBVISIBLE"></span>*pbVisible*</span></span>
</dt> <dd>

<span data-ttu-id="dc762-108">如果可以看到字元的框架，則為收到 **True** 之變數的位址，如果隱藏，則為 **False** 。</span><span class="sxs-lookup"><span data-stu-id="dc762-108">Address of a variable that receives **True** if the character's frame is visible and **False** if hidden.</span></span>

</dd> </dl>

<span data-ttu-id="dc762-109">您可以使用這個方法來判斷字元的框架目前是否可見。</span><span class="sxs-lookup"><span data-stu-id="dc762-109">You can use this method to determine whether the character's frame is currently visible.</span></span> <span data-ttu-id="dc762-110">若要讓字元可見，請使用 [**Show**](/windows/desktop/lwef/iagentcharacter--show) 方法。</span><span class="sxs-lookup"><span data-stu-id="dc762-110">To make a character visible, use the [**Show**](/windows/desktop/lwef/iagentcharacter--show) method.</span></span> <span data-ttu-id="dc762-111">若要隱藏字元，請使用 [**hide**](/windows/desktop/lwef/iagentcharacter--hide) 方法。</span><span class="sxs-lookup"><span data-stu-id="dc762-111">To hide a character, use the [**Hide**](/windows/desktop/lwef/iagentcharacter--hide) method.</span></span>

 

 