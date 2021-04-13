---
title: 值屬性
description: Value 屬性提供物件中所含視覺資訊的文字標記法。 並非所有物件都支援 Value 屬性。
ms.assetid: 89b99645-31f5-458a-ae61-a72bf1338195
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a6cd3ad86b9ce3a4fcc917fc4f49792adf432bd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104300991"
---
# <a name="value-property"></a><span data-ttu-id="e3608-104">值屬性</span><span class="sxs-lookup"><span data-stu-id="e3608-104">Value Property</span></span>

<span data-ttu-id="e3608-105">**Value** 屬性提供物件中所含視覺資訊的文字標記法。</span><span class="sxs-lookup"><span data-stu-id="e3608-105">The **Value** property provides a textual representation of the visual information contained in an object.</span></span> <span data-ttu-id="e3608-106">並非所有物件都支援 **Value** 屬性。</span><span class="sxs-lookup"><span data-stu-id="e3608-106">Not all objects support the **Value** property.</span></span>

<span data-ttu-id="e3608-107">藉由呼叫 [**IAccessible：： get \_ accValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accvalue)，即可取出 **Value** 屬性。</span><span class="sxs-lookup"><span data-stu-id="e3608-107">The **Value** property is retrieved by calling [**IAccessible::get\_accValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accvalue).</span></span>

<span data-ttu-id="e3608-108">**Value** 屬性會告知用戶端有關物件中所包含的視覺資訊。</span><span class="sxs-lookup"><span data-stu-id="e3608-108">The **Value** property tells the client about the visual information contained in an object.</span></span> <span data-ttu-id="e3608-109">例如，編輯控制項的值是它所包含的文字，而功能表項目則沒有任何值。</span><span class="sxs-lookup"><span data-stu-id="e3608-109">For example, an edit control's value is the text it contains, whereas a menu item has no value.</span></span>

## <a name="providing-hierarchical-information"></a><span data-ttu-id="e3608-110">提供階層式資訊</span><span class="sxs-lookup"><span data-stu-id="e3608-110">Providing Hierarchical Information</span></span>

<span data-ttu-id="e3608-111">[ **值** ] 屬性會在例如樹狀檢視控制項的情況下提供階層式資訊。</span><span class="sxs-lookup"><span data-stu-id="e3608-111">The **Value** property provides hierarchical information in cases such as a tree view control.</span></span> <span data-ttu-id="e3608-112">雖然樹狀檢視控制項中的父物件不提供 [ **值** ] 屬性中的資訊，但控制項內的每個專案都有以零為基底的值，表示其在階層內的層級。</span><span class="sxs-lookup"><span data-stu-id="e3608-112">Although the parent object in the tree view control does not provide information in the **Value** property, each item within the control has a zero-based value that represents its level within the hierarchy.</span></span> <span data-ttu-id="e3608-113">最上層專案的值為零，第二層專案的值為1，依此類推。</span><span class="sxs-lookup"><span data-stu-id="e3608-113">Top-level items have a value of zero, second-level items have a value of one, and so on.</span></span>

 

 




