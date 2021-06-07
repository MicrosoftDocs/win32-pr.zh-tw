---
title: '切換視窗 (MSAA UI 元素參考) '
description: 每當使用者按下 ALT + TAB 切換至不同的應用程式時，就會顯示 [切換] 視窗。 切換視窗包含每個目前正在執行之應用程式的圖示。
ms.assetid: 77b32eb1-7722-410b-b141-ac09fc7fdffb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5aa12b5fa3bfb9e6207ddaff4133b030e6c233c3
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443979"
---
# <a name="switch-window-msaa-ui-element-reference"></a><span data-ttu-id="b313d-104">切換視窗 (MSAA UI 元素參考) </span><span class="sxs-lookup"><span data-stu-id="b313d-104">Switch Window (MSAA UI Element Reference)</span></span>

<span data-ttu-id="b313d-105">每當使用者按下 ALT + TAB 切換至不同的應用程式時，就會顯示 [切換] 視窗。</span><span class="sxs-lookup"><span data-stu-id="b313d-105">The switch window displays whenever a user presses ALT+TAB to switch to a different application.</span></span> <span data-ttu-id="b313d-106">切換視窗包含每個目前正在執行之應用程式的圖示。</span><span class="sxs-lookup"><span data-stu-id="b313d-106">The switch window contains an icon for each application currently running.</span></span>

<span data-ttu-id="b313d-107">切換視窗的視窗類別名稱是 " \# 32771"。</span><span class="sxs-lookup"><span data-stu-id="b313d-107">The window class name for the switch window is "\#32771".</span></span>

## <a name="iaccessible-methods"></a><span data-ttu-id="b313d-108">IAccessible 方法</span><span class="sxs-lookup"><span data-stu-id="b313d-108">IAccessible Methods</span></span>

<span data-ttu-id="b313d-109">切換視窗支援下列 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 方法：</span><span class="sxs-lookup"><span data-stu-id="b313d-109">The switch window supports the following [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) methods:</span></span>



| <span data-ttu-id="b313d-110">方法</span><span class="sxs-lookup"><span data-stu-id="b313d-110">Method</span></span>                                                                    | <span data-ttu-id="b313d-111">註解</span><span class="sxs-lookup"><span data-stu-id="b313d-111">Comments</span></span>                                                                                                                                                                                                                          |
|---------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b313d-112">**accDoDefaultAction**</span><span class="sxs-lookup"><span data-stu-id="b313d-112">**accDoDefaultAction**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) | <span data-ttu-id="b313d-113">切換視窗物件本身沒有 **DefaultAction** 屬性。</span><span class="sxs-lookup"><span data-stu-id="b313d-113">The switch window object itself does not have a **DefaultAction** property.</span></span> <span data-ttu-id="b313d-114">在 [切換] 視窗中，每個專案的 [**accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) 方法會啟用指定的專案。</span><span class="sxs-lookup"><span data-stu-id="b313d-114">The [**accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) method for each item in the switch window activates the specified item.</span></span> |
| [<span data-ttu-id="b313d-115">**accHitTest**</span><span class="sxs-lookup"><span data-stu-id="b313d-115">**accHitTest**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)                 |                                                                                                                                                                                                                                   |
| [<span data-ttu-id="b313d-116">**accLocation**</span><span class="sxs-lookup"><span data-stu-id="b313d-116">**accLocation**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)               |                                                                                                                                                                                                                                   |
| [<span data-ttu-id="b313d-117">**accNavigate**</span><span class="sxs-lookup"><span data-stu-id="b313d-117">**accNavigate**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)               |                                                                                                                                                                                                                                   |
| [<span data-ttu-id="b313d-118">**accSelect**</span><span class="sxs-lookup"><span data-stu-id="b313d-118">**accSelect**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)                   |                                                                                                                                                                                                                                   |



 

## <a name="iaccessible-properties"></a><span data-ttu-id="b313d-119">IAccessible 屬性</span><span class="sxs-lookup"><span data-stu-id="b313d-119">IAccessible Properties</span></span>

<span data-ttu-id="b313d-120">切換視窗支援下列 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 屬性：</span><span class="sxs-lookup"><span data-stu-id="b313d-120">The switch window supports the following [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) properties:</span></span>



|      <span data-ttu-id="b313d-121">屬性</span><span class="sxs-lookup"><span data-stu-id="b313d-121">Property</span></span>                                                                          |      <span data-ttu-id="b313d-122">描述</span><span class="sxs-lookup"><span data-stu-id="b313d-122">Description</span></span>                                                                                                                                                                                                                          |
|--------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b313d-123">**取得 \_ accChildCount**</span><span class="sxs-lookup"><span data-stu-id="b313d-123">**get\_accChildCount**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)       | <span data-ttu-id="b313d-124">**ChildCount** 屬性為零。</span><span class="sxs-lookup"><span data-stu-id="b313d-124">The **ChildCount** property is zero.</span></span>                                                                                                                                                                                           |
| [<span data-ttu-id="b313d-125">**取得 \_ accDefaultAction**</span><span class="sxs-lookup"><span data-stu-id="b313d-125">**get\_accDefaultAction**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdefaultaction) | <span data-ttu-id="b313d-126">切換視窗物件本身沒有 **DefaultAction** 屬性。</span><span class="sxs-lookup"><span data-stu-id="b313d-126">The switch window object itself does not have a **DefaultAction** property.</span></span> <span data-ttu-id="b313d-127">切換視窗中每個專案的 **DefaultAction** 屬性為 "switch"。</span><span class="sxs-lookup"><span data-stu-id="b313d-127">The **DefaultAction** property for each item in the switch window is "Switch".</span></span>                                                                     |
| [<span data-ttu-id="b313d-128">**取得 \_ accFocus**</span><span class="sxs-lookup"><span data-stu-id="b313d-128">**get\_accFocus**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)                 | <span data-ttu-id="b313d-129">切換視窗父物件無法接收焦點;只有個別子女才能獲得焦點。</span><span class="sxs-lookup"><span data-stu-id="b313d-129">The switch window parent object cannot receive focus; only the individual children can receive focus.</span></span>                                                                                                                          |
| [<span data-ttu-id="b313d-130">**取得 \_ accName**</span><span class="sxs-lookup"><span data-stu-id="b313d-130">**get\_accName**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)                   | <span data-ttu-id="b313d-131">切換視窗物件本身沒有 **名稱** 屬性。</span><span class="sxs-lookup"><span data-stu-id="b313d-131">The switch window object itself does not have a **Name** property.</span></span> <span data-ttu-id="b313d-132">切換視窗中每個應用程式圖示的 [ **名稱** ] 屬性與顯示的應用程式名稱相同。</span><span class="sxs-lookup"><span data-stu-id="b313d-132">The **Name** property for each application icon in the switch window is the same as the displayed application name.</span></span>                                         |
| [<span data-ttu-id="b313d-133">**取得 \_ accRole**</span><span class="sxs-lookup"><span data-stu-id="b313d-133">**get\_accRole**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)                   | <span data-ttu-id="b313d-134">切換視窗物件本身具有 "window 32771" 的 **Role** 屬性 \[ \] 。</span><span class="sxs-lookup"><span data-stu-id="b313d-134">The switch window object itself has a **Role** property of "window \[32771\]".</span></span> <span data-ttu-id="b313d-135">此外，切換視窗中的每個應用程式圖示都有 **角色** 屬性 [**角色系統的 [ \_ 系統 \_**](object-roles.md)]。</span><span class="sxs-lookup"><span data-stu-id="b313d-135">Also, each application icon in the switch window has the **Role** property [**ROLE\_SYSTEM\_LISTITEM**](object-roles.md).</span></span> |
| [<span data-ttu-id="b313d-136">**取得 \_ accState**</span><span class="sxs-lookup"><span data-stu-id="b313d-136">**get\_accState**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)                 | <span data-ttu-id="b313d-137">切換視窗物件本身不支援 **State** 屬性。</span><span class="sxs-lookup"><span data-stu-id="b313d-137">The switch window object itself does not support the **State** property.</span></span> <span data-ttu-id="b313d-138">清單視圖專案的 **狀態** 值是 [**狀態系統可 \_ \_ 設定**](object-state-constants.md)的。</span><span class="sxs-lookup"><span data-stu-id="b313d-138">The **State** value for the list view items is [**STATE\_SYSTEM\_FOCUSABLE**](object-state-constants.md).</span></span>                     |



 

## <a name="related-topics"></a><span data-ttu-id="b313d-139">相關主題</span><span class="sxs-lookup"><span data-stu-id="b313d-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b313d-140">IAccessible 介面</span><span class="sxs-lookup"><span data-stu-id="b313d-140">IAccessible Interface</span></span>](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 




