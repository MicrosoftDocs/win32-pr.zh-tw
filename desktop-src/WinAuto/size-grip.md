---
title: '大小手柄 (MSAA UI 元素參考) '
description: 大小底圖是視窗右下角的特殊滑鼠指標，可讓使用者按一下並拖曳大小底框來調整視窗大小。
ms.assetid: 886b27b3-e88d-47a1-85f3-a55bd14c7a7c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9fb7180a8936aff46903257e6be8ca4ab7f0e5b8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103675623"
---
# <a name="size-grip-msaa-ui-element-reference"></a><span data-ttu-id="7890c-103">大小手柄 (MSAA UI 元素參考) </span><span class="sxs-lookup"><span data-stu-id="7890c-103">Size Grip (MSAA UI Element Reference)</span></span>

<span data-ttu-id="7890c-104">大小底圖是視窗右下角的特殊滑鼠指標，可讓使用者按一下並拖曳大小底框來調整視窗大小。</span><span class="sxs-lookup"><span data-stu-id="7890c-104">The size grip is a special mouse pointer in the lower-right corner of a window that allows a user to click and drag the size grip to resize the window.</span></span>

## <a name="iaccessible-methods"></a><span data-ttu-id="7890c-105">IAccessible 方法</span><span class="sxs-lookup"><span data-stu-id="7890c-105">IAccessible Methods</span></span>

<span data-ttu-id="7890c-106">大小的底框支援下列 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 方法：</span><span class="sxs-lookup"><span data-stu-id="7890c-106">The size grip supports the following [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) methods:</span></span>

-   [<span data-ttu-id="7890c-107">**accHitTest**</span><span class="sxs-lookup"><span data-stu-id="7890c-107">**accHitTest**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [<span data-ttu-id="7890c-108">**accLocation**</span><span class="sxs-lookup"><span data-stu-id="7890c-108">**accLocation**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [<span data-ttu-id="7890c-109">**accNavigate**</span><span class="sxs-lookup"><span data-stu-id="7890c-109">**accNavigate**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)

## <a name="iaccessible-properties"></a><span data-ttu-id="7890c-110">IAccessible 屬性</span><span class="sxs-lookup"><span data-stu-id="7890c-110">IAccessible Properties</span></span>

<span data-ttu-id="7890c-111">大小的底框支援下列 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 屬性：</span><span class="sxs-lookup"><span data-stu-id="7890c-111">The size grip supports the following [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) properties:</span></span>



| <span data-ttu-id="7890c-112">屬性</span><span class="sxs-lookup"><span data-stu-id="7890c-112">Property</span></span>                                                                   | <span data-ttu-id="7890c-113">註解</span><span class="sxs-lookup"><span data-stu-id="7890c-113">Comments</span></span>                                                                                                                                                               |
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7890c-114">**取得 \_ accDescription**</span><span class="sxs-lookup"><span data-stu-id="7890c-114">**get\_accDescription**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdescription) | <span data-ttu-id="7890c-115">**Description** 屬性是「可以用來調整視窗的寬度和高度」。</span><span class="sxs-lookup"><span data-stu-id="7890c-115">The **Description** property is "Can be used to resize a window's width and height".</span></span>                                                                                   |
| [<span data-ttu-id="7890c-116">**取得 \_ accName**</span><span class="sxs-lookup"><span data-stu-id="7890c-116">**get\_accName**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)               | <span data-ttu-id="7890c-117">**Name** 屬性為「Size box」。</span><span class="sxs-lookup"><span data-stu-id="7890c-117">The **Name** property is "Size box".</span></span>                                                                                                                                   |
| [<span data-ttu-id="7890c-118">**取得 \_ accParent**</span><span class="sxs-lookup"><span data-stu-id="7890c-118">**get\_accParent**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)           | <span data-ttu-id="7890c-119">包含大小底框的視窗。</span><span class="sxs-lookup"><span data-stu-id="7890c-119">The window that contains the size grip.</span></span>                                                                                                                                |
| [<span data-ttu-id="7890c-120">**取得 \_ accRole**</span><span class="sxs-lookup"><span data-stu-id="7890c-120">**get\_accRole**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)               | <span data-ttu-id="7890c-121">**Role** 屬性是 [**role \_ SYSTEM \_**](object-roles.md)的底框。</span><span class="sxs-lookup"><span data-stu-id="7890c-121">The **Role** property is [**ROLE\_SYSTEM\_GRIP**](object-roles.md).</span></span>                                                                                  |
| [<span data-ttu-id="7890c-122">**取得 \_ accState**</span><span class="sxs-lookup"><span data-stu-id="7890c-122">**get\_accState**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)             | <span data-ttu-id="7890c-123">**State** 屬性的值為零，表示物件為可見或 [**狀態 \_ 系統 \_ 不可見**](object-state-constants.md)。</span><span class="sxs-lookup"><span data-stu-id="7890c-123">The value for the **State** property is zero, which means the object is visible, or [**STATE\_SYSTEM\_INVISIBLE**](object-state-constants.md).</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="7890c-124">相關主題</span><span class="sxs-lookup"><span data-stu-id="7890c-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7890c-125">IAccessible</span><span class="sxs-lookup"><span data-stu-id="7890c-125">IAccessible</span></span>](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 




