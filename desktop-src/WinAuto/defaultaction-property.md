---
title: DefaultAction 屬性
description: 物件的 DefaultAction 屬性會描述物件的主要操作方法，從使用者的觀點來看。 物件的 DefaultAction 屬性應該是動詞或簡短動詞片語。
ms.assetid: 8242c0af-b42e-44a4-8807-d6740fa1a24a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73dc032037c331a2022f227cb8e8547dd8bce9d2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104300303"
---
# <a name="defaultaction-property"></a><span data-ttu-id="84eb9-104">DefaultAction 屬性</span><span class="sxs-lookup"><span data-stu-id="84eb9-104">DefaultAction Property</span></span>

<span data-ttu-id="84eb9-105">物件的 **DefaultAction** 屬性會描述物件的主要操作方法，從使用者的觀點來看。</span><span class="sxs-lookup"><span data-stu-id="84eb9-105">An object's **DefaultAction** property describes the object's primary method of manipulation from the user's viewpoint.</span></span> <span data-ttu-id="84eb9-106">物件的 **DefaultAction** 屬性應該是動詞或簡短動詞片語。</span><span class="sxs-lookup"><span data-stu-id="84eb9-106">An object's **DefaultAction** property should be a verb or a short verb phrase.</span></span>

<span data-ttu-id="84eb9-107">藉由呼叫 [**IAccessible：： get \_ accDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdefaultaction)，即可取出 **DefaultAction** 屬性。</span><span class="sxs-lookup"><span data-stu-id="84eb9-107">The **DefaultAction** property is retrieved by calling [**IAccessible::get\_accDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdefaultaction).</span></span>

<span data-ttu-id="84eb9-108">用戶端會呼叫 [**IAccessible：： accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction)來執行物件的預設動作。</span><span class="sxs-lookup"><span data-stu-id="84eb9-108">To perform an object's default action, clients call [**IAccessible::accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction).</span></span>

<span data-ttu-id="84eb9-109">並非所有物件都有預設動作，而某些物件具有與其 [**Value**](value-property.md) 屬性相關的預設動作，如下列範例所示：</span><span class="sxs-lookup"><span data-stu-id="84eb9-109">Not all objects have default actions, and some objects have a default action that is related to its [**Value**](value-property.md) property, such as in the following examples:</span></span>

-   <span data-ttu-id="84eb9-110">選取的核取方塊具有預設動作「取消核取」和「已檢查」的值。</span><span class="sxs-lookup"><span data-stu-id="84eb9-110">A selected check box has a default action of "Uncheck" and a value of "Checked."</span></span>
-   <span data-ttu-id="84eb9-111">已清除的核取方塊具有預設動作 [檢查] 和 [未選取] 的值。</span><span class="sxs-lookup"><span data-stu-id="84eb9-111">A cleared check box has a default action of "Check" and a value of "Unchecked."</span></span>
-   <span data-ttu-id="84eb9-112">標示為「列印」的按鈕具有預設動作「按下」，沒有任何值。</span><span class="sxs-lookup"><span data-stu-id="84eb9-112">A button labeled "Print" has a default action of "Press," with no value.</span></span>
-   <span data-ttu-id="84eb9-113">顯示「印表機」的靜態文字控制項或編輯控制項沒有預設動作，但值為「印表機」。</span><span class="sxs-lookup"><span data-stu-id="84eb9-113">A static text control or an edit control that shows "Printer" has no default action, but has a value of "Printer."</span></span>

 

 




