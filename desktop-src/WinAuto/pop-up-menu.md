---
title: '快顯功能表 (MSAA UI 元素參考) '
description: 快顯功能表會顯示功能表命令的清單。
ms.assetid: 9dbfa2d7-a086-4348-8b84-7e36d33e2d27
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 785fe8ac7a70352116b3a77cf30034092de04a23
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840380"
---
# <a name="pop-up-menu-msaa-ui-element-reference"></a><span data-ttu-id="0efd4-103">快顯功能表 (MSAA UI 元素參考) </span><span class="sxs-lookup"><span data-stu-id="0efd4-103">Pop-up Menu (MSAA UI Element Reference)</span></span>

> [!Note]  
> <span data-ttu-id="0efd4-104">本主題說明用於 MSAA UI 專案參考之 **快顯功能表** 物件的用途。</span><span class="sxs-lookup"><span data-stu-id="0efd4-104">This topic describes **Pop-up Menu** objects for purposes of MSAA UI Element Reference.</span></span> <span data-ttu-id="0efd4-105">這裡未說明如何在各種 UI 架構中建立 **快顯功能表** 物件。</span><span class="sxs-lookup"><span data-stu-id="0efd4-105">How to create **Pop-up Menu** objects in various UI frameworks is not described here.</span></span> <span data-ttu-id="0efd4-106">請參閱您所使用之 UI 架構的 API 參考檔。</span><span class="sxs-lookup"><span data-stu-id="0efd4-106">See the API reference documentation for the UI framework you're using.</span></span>

 

<span data-ttu-id="0efd4-107">快顯功能表會顯示功能表命令的清單。</span><span class="sxs-lookup"><span data-stu-id="0efd4-107">A pop-up menu displays a list of menu commands.</span></span> <span data-ttu-id="0efd4-108">當功能表列中的功能表項目開啟時，Microsoft Active Accessibility 建立功能表快顯物件。</span><span class="sxs-lookup"><span data-stu-id="0efd4-108">Microsoft Active Accessibility creates a menu pop-up object when a menu item in a menu bar is opened.</span></span> <span data-ttu-id="0efd4-109">Microsoft Active Accessibility 也會建立快顯功能表的功能表快顯物件，當使用者以滑鼠右鍵按一下使用者介面專案時，就會顯示此物件。</span><span class="sxs-lookup"><span data-stu-id="0efd4-109">Microsoft Active Accessibility also creates menu pop-up objects for context menus, which are displayed when the user right-clicks a user interface element.</span></span>

<span data-ttu-id="0efd4-110">快顯功能表的視窗類別名稱是 " \# 32768"。</span><span class="sxs-lookup"><span data-stu-id="0efd4-110">The window class name for a pop-up menu is "\#32768".</span></span>

## <a name="iaccessible-methods"></a><span data-ttu-id="0efd4-111">IAccessible 方法</span><span class="sxs-lookup"><span data-stu-id="0efd4-111">IAccessible Methods</span></span>

<span data-ttu-id="0efd4-112">快顯功能表支援下列 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 方法：</span><span class="sxs-lookup"><span data-stu-id="0efd4-112">A pop-up menu supports the following [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) methods:</span></span>

-   [<span data-ttu-id="0efd4-113">**accHitTest**</span><span class="sxs-lookup"><span data-stu-id="0efd4-113">**accHitTest**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [<span data-ttu-id="0efd4-114">**accLocation**</span><span class="sxs-lookup"><span data-stu-id="0efd4-114">**accLocation**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [<span data-ttu-id="0efd4-115">**accNavigate**</span><span class="sxs-lookup"><span data-stu-id="0efd4-115">**accNavigate**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [<span data-ttu-id="0efd4-116">**accSelect**</span><span class="sxs-lookup"><span data-stu-id="0efd4-116">**accSelect**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

## <a name="iaccessible-properties"></a><span data-ttu-id="0efd4-117">IAccessible 屬性</span><span class="sxs-lookup"><span data-stu-id="0efd4-117">IAccessible Properties</span></span>

<span data-ttu-id="0efd4-118">快顯功能表支援下列 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 屬性：</span><span class="sxs-lookup"><span data-stu-id="0efd4-118">A pop-up menu supports the following [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) properties:</span></span>



| <span data-ttu-id="0efd4-119">屬性</span><span class="sxs-lookup"><span data-stu-id="0efd4-119">Property</span></span>                                                                 | <span data-ttu-id="0efd4-120">註解</span><span class="sxs-lookup"><span data-stu-id="0efd4-120">Comments</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|--------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0efd4-121">**取得 \_ accChild**</span><span class="sxs-lookup"><span data-stu-id="0efd4-121">**get\_accChild**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild)           | <span data-ttu-id="0efd4-122">針對指定的功能表項目抓取 [**IDispatch**](idispatch-interface.md) 。</span><span class="sxs-lookup"><span data-stu-id="0efd4-122">Retrieves the [**IDispatch**](idispatch-interface.md) for the specified menu item.</span></span> <span data-ttu-id="0efd4-123">功能表項目的子識別碼會依序從上到下編號，從1開始。</span><span class="sxs-lookup"><span data-stu-id="0efd4-123">The child IDs for the menu items are numbered sequentially from top to bottom starting with one.</span></span>                                                                                                                                                                                                                                                                                      |
| [<span data-ttu-id="0efd4-124">**取得 \_ accChildCount**</span><span class="sxs-lookup"><span data-stu-id="0efd4-124">**get\_accChildCount**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount) | <span data-ttu-id="0efd4-125">**ChildCount** 屬性是功能表中功能表項目的數目，包括功能表分隔符號。</span><span class="sxs-lookup"><span data-stu-id="0efd4-125">The **ChildCount** property is the number of menu items in the menu, including menu separators.</span></span>                                                                                                                                                                                                                                                                                                                                                                           |
| [<span data-ttu-id="0efd4-126">**取得 \_ accFocus**</span><span class="sxs-lookup"><span data-stu-id="0efd4-126">**get\_accFocus**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)           |                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [<span data-ttu-id="0efd4-127">**取得 \_ accName**</span><span class="sxs-lookup"><span data-stu-id="0efd4-127">**get\_accName**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)             | <span data-ttu-id="0efd4-128">快顯功能表的 [ **名稱** ] 屬性與功能表的名稱相同。</span><span class="sxs-lookup"><span data-stu-id="0efd4-128">The **Name** property for a pop-up menu is the same name as the menu.</span></span> <span data-ttu-id="0efd4-129">內容功能表的 [ **名稱** ] 屬性是「內容」。</span><span class="sxs-lookup"><span data-stu-id="0efd4-129">The **Name** property for a context menu is "Context".</span></span>                                                                                                                                                                                                                                                                                                                                              |
| [<span data-ttu-id="0efd4-130">**取得 \_ accParent**</span><span class="sxs-lookup"><span data-stu-id="0efd4-130">**get\_accParent**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)         | <span data-ttu-id="0efd4-131">**父** 屬性是視窗 ([**角色 \_ 系統 \_ 視窗**](object-roles.md)) ，它會圍繞快顯功能表，而且具有與快顯功能表相同的 **名稱** 屬性和視窗類別名稱。</span><span class="sxs-lookup"><span data-stu-id="0efd4-131">The **Parent** property is a window ( [**ROLE\_SYSTEM\_WINDOW**](object-roles.md) ) that surrounds the pop-up menu and has the same **Name** property and window class name as the pop-up menu .</span></span>                                                                                                                                                                                                                                                      |
| [<span data-ttu-id="0efd4-132">**取得 \_ accRole**</span><span class="sxs-lookup"><span data-stu-id="0efd4-132">**get\_accRole**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)             | <span data-ttu-id="0efd4-133">**Role** 屬性為 [**role \_ SYSTEM \_ MENUPOPUP**](object-roles.md)。</span><span class="sxs-lookup"><span data-stu-id="0efd4-133">The **Role** property is [**ROLE\_SYSTEM\_MENUPOPUP**](object-roles.md).</span></span>                                                                                                                                                                                                                                                                                                                                                                           |
| [<span data-ttu-id="0efd4-134">**取得 \_ accState**</span><span class="sxs-lookup"><span data-stu-id="0efd4-134">**get\_accState**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)           | <span data-ttu-id="0efd4-135">**State** 屬性是下列一或多個 [值](object-state-constants.md)的組合：[**狀態 \_ 系統 \_ 隱藏**](object-state-constants.md) \| [**狀態 \_ 系統 \_ 無法使用**](object-state-constants.md)狀態 \| [**\_ 系統 \_ 焦點**](object-state-constants.md)狀態系統可 \| [**\_ \_ 設定焦點**](object-state-constants.md)</span><span class="sxs-lookup"><span data-stu-id="0efd4-135">The **State** property is a combination of one or more of the following [values](object-state-constants.md): [**STATE\_SYSTEM\_INVISIBLE**](object-state-constants.md) \| [**STATE\_SYSTEM\_UNAVAILABLE**](object-state-constants.md) \| [**STATE\_SYSTEM\_FOCUSED**](object-state-constants.md) \| [**STATE\_SYSTEM\_FOCUSABLE**](object-state-constants.md)</span></span><br/> |



 

## <a name="notes"></a><span data-ttu-id="0efd4-136">備註</span><span class="sxs-lookup"><span data-stu-id="0efd4-136">Notes</span></span>

-   <span data-ttu-id="0efd4-137">快顯功能表物件不會觸發 [**事件 \_ 物件 \_ 建立**](event-constants.md) 和 [**事件 \_ 物件 \_**](event-constants.md) 終結事件。</span><span class="sxs-lookup"><span data-stu-id="0efd4-137">Pop-up menu objects do not trigger [**EVENT\_OBJECT\_CREATE**](event-constants.md) and [**EVENT\_OBJECT\_DESTROY**](event-constants.md) events.</span></span>
-   <span data-ttu-id="0efd4-138">多重資料行功能表不支援 [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)方法的 [**NAVDIR \_ LEFT**](navigation-constants.md)或 [**NAVDIR \_ RIGHT**](navigation-constants.md)旗標。</span><span class="sxs-lookup"><span data-stu-id="0efd4-138">Multi-column menus do not support the [**NAVDIR\_LEFT**](navigation-constants.md) or [**NAVDIR\_RIGHT**](navigation-constants.md) flags of the [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate) method.</span></span>
-   <span data-ttu-id="0efd4-139">Events [**事件 \_ 系統 \_ MENUPOPUPSTART**](event-constants.md) 和 [**event \_ system \_ MENUPOPUPEND**](event-constants.md) 不會以一致方式傳送。</span><span class="sxs-lookup"><span data-stu-id="0efd4-139">The events [**EVENT\_SYSTEM\_MENUPOPUPSTART**](event-constants.md) and [**EVENT\_SYSTEM\_MENUPOPUPEND**](event-constants.md) are not sent consistently.</span></span> <span data-ttu-id="0efd4-140">這是已知的問題，並已解決。</span><span class="sxs-lookup"><span data-stu-id="0efd4-140">This is a known issue and is being addressed.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0efd4-141">相關主題</span><span class="sxs-lookup"><span data-stu-id="0efd4-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0efd4-142">IAccessible 介面</span><span class="sxs-lookup"><span data-stu-id="0efd4-142">IAccessible Interface</span></span>](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> <dt>

[<span data-ttu-id="0efd4-143">**功能表列**</span><span class="sxs-lookup"><span data-stu-id="0efd4-143">**Menu Bar**</span></span>](menu-bar.md)
</dt> <dt>

[<span data-ttu-id="0efd4-144">**功能表項目**</span><span class="sxs-lookup"><span data-stu-id="0efd4-144">**Menu Item**</span></span>](menu-item.md)
</dt> </dl>

 

 





