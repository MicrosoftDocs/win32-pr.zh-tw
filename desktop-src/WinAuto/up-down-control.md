---
title: 'Up-Down 控制項 (MSAA UI 元素參考) '
description: 由上而下的控制項（也稱為微調控制項）結合了一組顯示為箭號的按鈕與一個好友編輯控制項。 按一下箭號會遞增或遞減編輯控制項中的值。
ms.assetid: 45e56c0f-4ac6-4731-b9a6-be4613bf40ae
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6fd2d28acc4c14a89ec73f5994ed0af47202145a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106966798"
---
# <a name="up-down-control-msaa-ui-element-reference"></a><span data-ttu-id="214ed-104">Up-Down 控制項 (MSAA UI 元素參考) </span><span class="sxs-lookup"><span data-stu-id="214ed-104">Up-Down Control (MSAA UI Element Reference)</span></span>

> [!Note]  
> <span data-ttu-id="214ed-105">本主題將針對 MSAA UI 元素參考的目的，描述 **最新的控制項** 物件。</span><span class="sxs-lookup"><span data-stu-id="214ed-105">This topic describes **Up-Down Control** objects for purposes of MSAA UI Element Reference.</span></span> <span data-ttu-id="214ed-106">此處不會說明如何在各種 UI 架構中建立 **最下層的控制項** 物件。</span><span class="sxs-lookup"><span data-stu-id="214ed-106">How to create **Up-Down Control** objects in various UI frameworks is not described here.</span></span> <span data-ttu-id="214ed-107">請參閱您所使用之 UI 架構的 API 參考檔。</span><span class="sxs-lookup"><span data-stu-id="214ed-107">See the API reference documentation for the UI framework you're using.</span></span>

 

<span data-ttu-id="214ed-108">由上而下的控制項（也稱為微調控制項）結合了一組顯示為箭號的按鈕與一個好友編輯控制項。</span><span class="sxs-lookup"><span data-stu-id="214ed-108">An up-down control, also known as a spin control, combines a pair of buttons displayed as arrows with a buddy edit control.</span></span> <span data-ttu-id="214ed-109">按一下箭號會遞增或遞減編輯控制項中的值。</span><span class="sxs-lookup"><span data-stu-id="214ed-109">Clicking the arrows increments or decrements the value in the edit control.</span></span>

<span data-ttu-id="214ed-110">上下按鈕控制項的視窗類別名稱是上下按鈕 \_ 類別，其定義為 Commctrl 中的 "msctls \_ updown32"。</span><span class="sxs-lookup"><span data-stu-id="214ed-110">The window class name for a up-down control is UPDOWN\_CLASS, which is defined as "msctls\_updown32" in Commctrl.h.</span></span>

## <a name="iaccessible-methods"></a><span data-ttu-id="214ed-111">IAccessible 方法</span><span class="sxs-lookup"><span data-stu-id="214ed-111">IAccessible Methods</span></span>

<span data-ttu-id="214ed-112">上下控制項支援下列 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 方法：</span><span class="sxs-lookup"><span data-stu-id="214ed-112">An up-down control supports the following [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) methods:</span></span>

-   [<span data-ttu-id="214ed-113">**accHitTest**</span><span class="sxs-lookup"><span data-stu-id="214ed-113">**accHitTest**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [<span data-ttu-id="214ed-114">**accLocation**</span><span class="sxs-lookup"><span data-stu-id="214ed-114">**accLocation**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [<span data-ttu-id="214ed-115">**accNavigate**</span><span class="sxs-lookup"><span data-stu-id="214ed-115">**accNavigate**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [<span data-ttu-id="214ed-116">**accSelect**</span><span class="sxs-lookup"><span data-stu-id="214ed-116">**accSelect**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

## <a name="iaccessible-properties"></a><span data-ttu-id="214ed-117">IAccessible 屬性</span><span class="sxs-lookup"><span data-stu-id="214ed-117">IAccessible Properties</span></span>

<span data-ttu-id="214ed-118">上下控制項支援下列 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 屬性：</span><span class="sxs-lookup"><span data-stu-id="214ed-118">An up-down control supports the following [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) properties:</span></span>



| <span data-ttu-id="214ed-119">屬性</span><span class="sxs-lookup"><span data-stu-id="214ed-119">Property</span></span>                                                                 | <span data-ttu-id="214ed-120">註解</span><span class="sxs-lookup"><span data-stu-id="214ed-120">Comments</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|--------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="214ed-121">**取得 \_ accChild**</span><span class="sxs-lookup"><span data-stu-id="214ed-121">**get\_accChild**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild)           |                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| [<span data-ttu-id="214ed-122">**取得 \_ accChildCount**</span><span class="sxs-lookup"><span data-stu-id="214ed-122">**get\_accChildCount**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount) | <span data-ttu-id="214ed-123">**ChildCount** 屬性為 "2" (向上箭號和向下箭號按鈕) 。</span><span class="sxs-lookup"><span data-stu-id="214ed-123">The **ChildCount** property is "2" (the up and down arrow buttons).</span></span>                                                                                                                                                                                                                                                                                                                                                                                                           |
| [<span data-ttu-id="214ed-124">**取得 \_ accFocus**</span><span class="sxs-lookup"><span data-stu-id="214ed-124">**get\_accFocus**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)           |                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| [<span data-ttu-id="214ed-125">**取得 \_ accHelp**</span><span class="sxs-lookup"><span data-stu-id="214ed-125">**get\_accHelp**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelp)             |                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| [<span data-ttu-id="214ed-126">**取得 \_ accHelpTopic**</span><span class="sxs-lookup"><span data-stu-id="214ed-126">**get\_accHelpTopic**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelptopic)   |                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| [<span data-ttu-id="214ed-127">**取得 \_ accName**</span><span class="sxs-lookup"><span data-stu-id="214ed-127">**get\_accName**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)             | <span data-ttu-id="214ed-128">上下按鈕控制項物件的 [ **名稱** ] 屬性是從控制項的視窗文字 (或標題) 取得。</span><span class="sxs-lookup"><span data-stu-id="214ed-128">The **Name** property for the up-down control object is obtained from the control's window text (or caption).</span></span> <span data-ttu-id="214ed-129">此文字不會與上下按鈕控制項一起顯示，因此伺服器開發人員必須在控制項的資源定義語句中提供有意義的文字，以協助用戶端公用程式的使用者識別控制項。</span><span class="sxs-lookup"><span data-stu-id="214ed-129">This text is not displayed with the up-down control, so server developers must provide meaningful text in the control's resource definition statement to help users of client utilities identify the control.</span></span> <span data-ttu-id="214ed-130">上下箭號控制項中上方箭號按鈕的 [ **名稱** ] 屬性是 [更多]，而底部箭號按鈕的 [ **名稱** ] 屬性則是「Less」。</span><span class="sxs-lookup"><span data-stu-id="214ed-130">The **Name** property for the top arrow button in the up-down control is "More", and the **Name** property for the bottom arrow button is "Less".</span></span> |
| [<span data-ttu-id="214ed-131">**取得 \_ accParent**</span><span class="sxs-lookup"><span data-stu-id="214ed-131">**get\_accParent**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)         | <span data-ttu-id="214ed-132">上下按鈕控制項的 **Parent** 屬性是視窗 ( [**角色 \_ 系統 \_ 視窗**](object-roles.md) ) ，它會圍繞控制項，而且具有與控制項相同的 **名稱** 屬性和視窗類別名稱。</span><span class="sxs-lookup"><span data-stu-id="214ed-132">The **Parent** property of the up-down control is a window ( [**ROLE\_SYSTEM\_WINDOW**](object-roles.md) ) that surrounds the control and has the same **Name** property and window class name as the control.</span></span> <span data-ttu-id="214ed-133">向上和向下箭號按鈕的 **父** 屬性是上下按鈕控制項物件。</span><span class="sxs-lookup"><span data-stu-id="214ed-133">The **Parent** property of the up and down arrow buttons is the up-down control object.</span></span>                                                                                                                                                    |
| [<span data-ttu-id="214ed-134">**取得 \_ accRole**</span><span class="sxs-lookup"><span data-stu-id="214ed-134">**get\_accRole**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)             | <span data-ttu-id="214ed-135">由上而下控制物件的 **role** 屬性是 [**由 \_ 角色 \_ 系統**](object-roles.md)調整。</span><span class="sxs-lookup"><span data-stu-id="214ed-135">The **Role** property for up-down control object is [**ROLE\_SYSTEM\_SPINBUTTON**](object-roles.md).</span></span> <span data-ttu-id="214ed-136">箭號按鈕的 **role** 屬性是 [**角色 \_ 系統 \_ 按鍵**](object-roles.md)。</span><span class="sxs-lookup"><span data-stu-id="214ed-136">The **Role** property for the arrow buttons is [**ROLE\_SYSTEM\_PUSHBUTTON**](object-roles.md).</span></span>                                                                                                                                                                                                                          |
| [<span data-ttu-id="214ed-137">**取得 \_ accState**</span><span class="sxs-lookup"><span data-stu-id="214ed-137">**get\_accState**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)           | <span data-ttu-id="214ed-138">由上而下控制物件的 state 屬性是下列其中一個 [值](object-state-constants.md)：以 [**狀態 \_ 系統為 \_ 焦點**](object-state-constants.md)的 \| [**狀態 \_ 系統可 \_ 設定焦點**](object-state-constants.md)</span><span class="sxs-lookup"><span data-stu-id="214ed-138">The State property for up-down control object is one of the following [values](object-state-constants.md):[**STATE\_SYSTEM\_FOCUSED**](object-state-constants.md) \| [**STATE\_SYSTEM\_FOCUSABLE**](object-state-constants.md)</span></span><br/>                                                                                                                                                                                      |
| [<span data-ttu-id="214ed-139">**取得 \_ accValue**</span><span class="sxs-lookup"><span data-stu-id="214ed-139">**get\_accValue**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accvalue)           |                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |



 

## <a name="notes"></a><span data-ttu-id="214ed-140">備註</span><span class="sxs-lookup"><span data-stu-id="214ed-140">Notes</span></span>

<span data-ttu-id="214ed-141">Microsoft Active Accessibility 會將好友編輯控制項公開為個別的物件。</span><span class="sxs-lookup"><span data-stu-id="214ed-141">Microsoft Active Accessibility exposes the buddy edit control as a separate object.</span></span>

## <a name="related-topics"></a><span data-ttu-id="214ed-142">相關主題</span><span class="sxs-lookup"><span data-stu-id="214ed-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="214ed-143">IAccessible 介面</span><span class="sxs-lookup"><span data-stu-id="214ed-143">IAccessible Interface</span></span>](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 





