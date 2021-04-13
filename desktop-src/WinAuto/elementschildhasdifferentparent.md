---
title: ElementsChildHasDifferentParent
description: ElementsChildHasDifferentParent
ms.assetid: 2347A33C-8FBD-4C30-8B40-9CB35F121C8E
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 843ea0f0ec7708f91d407f1fa7a55fa59a813234
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104311522"
---
# <a name="elementschildhasdifferentparent"></a><span data-ttu-id="28c30-103">ElementsChildHasDifferentParent</span><span class="sxs-lookup"><span data-stu-id="28c30-103">ElementsChildHasDifferentParent</span></span>

## <a name="text"></a><span data-ttu-id="28c30-104">Text</span><span class="sxs-lookup"><span data-stu-id="28c30-104">Text</span></span>

<span data-ttu-id="28c30-105">專案的子 ({0}) 具有不同于元素的父 ({1}) </span><span class="sxs-lookup"><span data-stu-id="28c30-105">Element's child({0}) has different parent({1}) than element</span></span>

## <a name="type"></a><span data-ttu-id="28c30-106">類型</span><span class="sxs-lookup"><span data-stu-id="28c30-106">Type</span></span>

<span data-ttu-id="28c30-107">錯誤</span><span class="sxs-lookup"><span data-stu-id="28c30-107">Error</span></span>

## <a name="description"></a><span data-ttu-id="28c30-108">描述</span><span class="sxs-lookup"><span data-stu-id="28c30-108">Description</span></span>

<span data-ttu-id="28c30-109">此錯誤表示在目標專案的子系上呼叫 [**get \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent) 時，子系不會報告一致的父系。</span><span class="sxs-lookup"><span data-stu-id="28c30-109">This error indicates that, when [**get\_accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent) is called on the children of the target element, the children do not report a consistent parent.</span></span>

![一個專案的子系的範例，其會報告不一致的父系](images/accchecker-inconsistent-parent.png)

<span data-ttu-id="28c30-111">此問題可能會導致自動化工具的導覽問題，因為進行中的元素可能不穩定且無法預測。</span><span class="sxs-lookup"><span data-stu-id="28c30-111">This issue can cause navigation problems for automated tools because traversing elements might be erratic and unpredictable.</span></span>

## <a name="possible-causes"></a><span data-ttu-id="28c30-112">可能的原因</span><span class="sxs-lookup"><span data-stu-id="28c30-112">Possible causes</span></span>

<span data-ttu-id="28c30-113">不正確或不正確 MSAA 執行。</span><span class="sxs-lookup"><span data-stu-id="28c30-113">An incorrect or invalid MSAA implementation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="28c30-114">相關主題</span><span class="sxs-lookup"><span data-stu-id="28c30-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="28c30-115">**AccessibleChildren**</span><span class="sxs-lookup"><span data-stu-id="28c30-115">**AccessibleChildren**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-accessiblechildren)
</dt> </dl>

 

 




