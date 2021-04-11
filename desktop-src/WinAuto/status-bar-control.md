---
title: '狀態列控制項 (MSAA UI 元素參考) '
description: 狀態列會在應用程式視窗底部的水準視窗中顯示狀態資訊。
ms.assetid: e910a5c6-84d5-4ade-abf5-792ff1915021
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81bddf2898b9b7eca5385d86d6dabc6a50d3d4df
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104311204"
---
# <a name="status-bar-control-msaa-ui-element-reference"></a><span data-ttu-id="acf2c-103">狀態列控制項 (MSAA UI 元素參考) </span><span class="sxs-lookup"><span data-stu-id="acf2c-103">Status Bar Control (MSAA UI Element Reference)</span></span>

> [!Note]  
> <span data-ttu-id="acf2c-104">本主題描述用於 MSAA UI 專案參考之 **狀態列控制項** 物件的用途。</span><span class="sxs-lookup"><span data-stu-id="acf2c-104">This topic describes **Status Bar Control** objects for purposes of MSAA UI Element Reference.</span></span> <span data-ttu-id="acf2c-105">此處未說明如何在各種 UI 架構中建立 **狀態列控制項** 物件。</span><span class="sxs-lookup"><span data-stu-id="acf2c-105">How to create **Status Bar Control** objects in various UI frameworks is not described here.</span></span> <span data-ttu-id="acf2c-106">請參閱您所使用之 UI 架構的 API 參考檔。</span><span class="sxs-lookup"><span data-stu-id="acf2c-106">See the API reference documentation for the UI framework you're using.</span></span>

 

<span data-ttu-id="acf2c-107">狀態列會在應用程式視窗底部的水準視窗中顯示狀態資訊。</span><span class="sxs-lookup"><span data-stu-id="acf2c-107">Status bars display status information in a horizontal window at the bottom of an application window.</span></span> <span data-ttu-id="acf2c-108">狀態列通常會分成幾個部分，稱為「窗格」，而每個窗格會顯示不同的狀態資訊。</span><span class="sxs-lookup"><span data-stu-id="acf2c-108">Status bars are often divided into parts, called panes, and each pane displays different status information.</span></span> <span data-ttu-id="acf2c-109">此外，狀態列也可以包含不同類型的物件，包括按鈕和進度列。</span><span class="sxs-lookup"><span data-stu-id="acf2c-109">Additionally, status bars can contain objects of different types, including buttons and progress bars.</span></span> <span data-ttu-id="acf2c-110">狀態列控制項的視窗類別名稱是 STATUSCLASSNAME，其定義為 Commctrl 中的 "msctls \_ statusbar32"。</span><span class="sxs-lookup"><span data-stu-id="acf2c-110">The window class name for a status bar control is STATUSCLASSNAME, which is defined as "msctls\_statusbar32" in Commctrl.h.</span></span>

## <a name="iaccessible-methods"></a><span data-ttu-id="acf2c-111">IAccessible 方法</span><span class="sxs-lookup"><span data-stu-id="acf2c-111">IAccessible Methods</span></span>

<span data-ttu-id="acf2c-112">狀態列支援下列 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 方法：</span><span class="sxs-lookup"><span data-stu-id="acf2c-112">Status bars support the following [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) methods:</span></span>

-   [<span data-ttu-id="acf2c-113">**accHitTest**</span><span class="sxs-lookup"><span data-stu-id="acf2c-113">**accHitTest**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [<span data-ttu-id="acf2c-114">**accLocation**</span><span class="sxs-lookup"><span data-stu-id="acf2c-114">**accLocation**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [<span data-ttu-id="acf2c-115">**accNavigate**</span><span class="sxs-lookup"><span data-stu-id="acf2c-115">**accNavigate**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [<span data-ttu-id="acf2c-116">**accSelect**</span><span class="sxs-lookup"><span data-stu-id="acf2c-116">**accSelect**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

## <a name="iaccessible-properties"></a><span data-ttu-id="acf2c-117">IAccessible 屬性</span><span class="sxs-lookup"><span data-stu-id="acf2c-117">IAccessible Properties</span></span>

<span data-ttu-id="acf2c-118">狀態列支援下列 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 屬性：</span><span class="sxs-lookup"><span data-stu-id="acf2c-118">Status bars support the following [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) properties:</span></span>



| <span data-ttu-id="acf2c-119">屬性</span><span class="sxs-lookup"><span data-stu-id="acf2c-119">Property</span></span>                                                                 | <span data-ttu-id="acf2c-120">註解</span><span class="sxs-lookup"><span data-stu-id="acf2c-120">Comments</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|--------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="acf2c-121">**取得 \_ accChildCount**</span><span class="sxs-lookup"><span data-stu-id="acf2c-121">**get\_accChildCount**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount) | <span data-ttu-id="acf2c-122">**ChildCount** 屬性是狀態列中的窗格數目。</span><span class="sxs-lookup"><span data-stu-id="acf2c-122">The **ChildCount** property is the number of panes in the status bar.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                     |
| [<span data-ttu-id="acf2c-123">**取得 \_ accFocus**</span><span class="sxs-lookup"><span data-stu-id="acf2c-123">**get\_accFocus**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)           |                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [<span data-ttu-id="acf2c-124">**取得 \_ accName**</span><span class="sxs-lookup"><span data-stu-id="acf2c-124">**get\_accName**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)             | <span data-ttu-id="acf2c-125">狀態列物件本身沒有 **名稱** 屬性。</span><span class="sxs-lookup"><span data-stu-id="acf2c-125">The status bar object itself does not have a **Name** property.</span></span> <span data-ttu-id="acf2c-126">狀態列中每個窗格的 [ **名稱** ] 屬性與顯示的文字相同。</span><span class="sxs-lookup"><span data-stu-id="acf2c-126">The **Name** property of each pane in the status bar is the same as the displayed text.</span></span>                                                                                                                                                                                                                                                                                                                   |
| [<span data-ttu-id="acf2c-127">**取得 \_ accParent**</span><span class="sxs-lookup"><span data-stu-id="acf2c-127">**get\_accParent**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)         | <span data-ttu-id="acf2c-128">狀態列物件的 **父** 屬性是視窗 ( [**角色 \_ 系統 \_ 視窗**](object-roles.md) ) ，它會圍繞控制項，而且具有與控制項相同的視窗類別名稱。</span><span class="sxs-lookup"><span data-stu-id="acf2c-128">The **Parent** property of the status bar object is a window ( [**ROLE\_SYSTEM\_WINDOW**](object-roles.md) ) that surrounds the control and has the same window class name as the control.</span></span> <span data-ttu-id="acf2c-129">狀態列中窗格的 **父** 屬性是狀態列物件。</span><span class="sxs-lookup"><span data-stu-id="acf2c-129">The **Parent** property of the panes in the status bar is the status bar object.</span></span>                                                                                                                                                                           |
| [<span data-ttu-id="acf2c-130">**取得 \_ accRole**</span><span class="sxs-lookup"><span data-stu-id="acf2c-130">**get\_accRole**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)             | <span data-ttu-id="acf2c-131">狀態列物件本身的 **角色** 屬性是 [**角色 \_ 系統的 \_ 狀態列**](object-roles.md)。</span><span class="sxs-lookup"><span data-stu-id="acf2c-131">The **Role** property for the status bar object itself is [**ROLE\_SYSTEM\_STATUSBAR**](object-roles.md).</span></span> <span data-ttu-id="acf2c-132">狀態列中顯示的文字具有 [**角色 \_ 系統 \_ STATICTEXT**](object-roles.md) 作為其 **角色** 屬性。</span><span class="sxs-lookup"><span data-stu-id="acf2c-132">The text displayed in a status bar has [**ROLE\_SYSTEM\_STATICTEXT**](object-roles.md) as its **Role** property.</span></span>                                                                                                                                                                                                 |
| [<span data-ttu-id="acf2c-133">**取得 \_ accState**</span><span class="sxs-lookup"><span data-stu-id="acf2c-133">**get\_accState**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)           | <span data-ttu-id="acf2c-134">**State** 屬性是下列一或多個 [值](object-state-constants.md)的組合：[**狀態 \_ 系統 \_ 隱藏**](object-state-constants.md) \| [**狀態 \_ 系統 \_ 無法使用**](object-state-constants.md)狀態 \| [**\_ 系統 \_ 焦點**](object-state-constants.md)狀態系統可 \| [**\_ \_ 設定焦點**](object-state-constants.md)</span><span class="sxs-lookup"><span data-stu-id="acf2c-134">The **State** property is a combination of one or more of the following [values](object-state-constants.md): [**STATE\_SYSTEM\_INVISIBLE**](object-state-constants.md) \| [**STATE\_SYSTEM\_UNAVAILABLE**](object-state-constants.md) \| [**STATE\_SYSTEM\_FOCUSED**](object-state-constants.md) \| [**STATE\_SYSTEM\_FOCUSABLE**](object-state-constants.md)</span></span><br/> |



 

## <a name="notes"></a><span data-ttu-id="acf2c-135">備註</span><span class="sxs-lookup"><span data-stu-id="acf2c-135">Notes</span></span>

<span data-ttu-id="acf2c-136">因為狀態列控制項或狀態列上的文字區域不支援鍵盤快速鍵，所以不支援 [**get \_ accKeyboardShortcut**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut) 。</span><span class="sxs-lookup"><span data-stu-id="acf2c-136">Because keyboard shortcuts are not supported for status bar controls or text areas on status bars, [**get\_accKeyboardShortcut**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut) is not supported.</span></span>

## <a name="related-topics"></a><span data-ttu-id="acf2c-137">相關主題</span><span class="sxs-lookup"><span data-stu-id="acf2c-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="acf2c-138">IAccessible 介面</span><span class="sxs-lookup"><span data-stu-id="acf2c-138">IAccessible Interface</span></span>](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 





