---
title: '功能表列 (MSAA UI 元素參考) '
description: 功能表列是緊接在標題列下方的視窗區域，其中包含 [檔案]、[編輯]、[視窗] 和 [說明] 等功能表項目。
ms.assetid: 63b496c7-ae3b-49b5-8c22-41fc9a8f3981
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a239a0bb5f860132ba0f9b9393129c2c7a093dae
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104507232"
---
# <a name="menu-bar-msaa-ui-element-reference"></a><span data-ttu-id="7f86c-103">功能表列 (MSAA UI 元素參考) </span><span class="sxs-lookup"><span data-stu-id="7f86c-103">Menu Bar (MSAA UI Element Reference)</span></span>

> [!Note]  
> <span data-ttu-id="7f86c-104">本主題描述用於 MSAA UI 專案參考之 **功能表列** 物件的用途。</span><span class="sxs-lookup"><span data-stu-id="7f86c-104">This topic describes **Menu Bar** objects for purposes of MSAA UI Element Reference.</span></span> <span data-ttu-id="7f86c-105">此處未說明如何在各種 UI 架構中建立 **功能表列** 物件。</span><span class="sxs-lookup"><span data-stu-id="7f86c-105">How to create **Menu Bar** objects in various UI frameworks is not described here.</span></span> <span data-ttu-id="7f86c-106">請參閱您所使用之 UI 架構的 API 參考檔。</span><span class="sxs-lookup"><span data-stu-id="7f86c-106">See the API reference documentation for the UI framework you're using.</span></span>

 

<span data-ttu-id="7f86c-107">功能表列是緊接在標題列下方的視窗區域，其中包含 [檔案 **]、[\*\*\*\*編輯**]、[**視窗]\*\*\*\*和 [** 說明] 等功能表項目。</span><span class="sxs-lookup"><span data-stu-id="7f86c-107">A menu bar is the area of a window immediately beneath the title bar that contains menu items such as **File**, **Edit**, **Window**, and **Help**.</span></span> <span data-ttu-id="7f86c-108">Microsoft Active Accessibility 也會建立 [系統] 功能表的功能表列物件（標題列左上角的功能表），並包含功能表項目，例如 [ **還原**]、[ **移動**]、[ **大小**]、[ **最小化**] 和 [ **最大化**]。</span><span class="sxs-lookup"><span data-stu-id="7f86c-108">Microsoft Active Accessibility also creates a menu bar object for a system menu, which is the menu in the top left corner of the title bar and contains menu items such as **Restore**, **Move**, **Size**, **Minimize**, and **Maximize**.</span></span>

> [!Note]  
> <span data-ttu-id="7f86c-109">因為功能表列控制項不會收到焦點，所以這個控制項不支援 [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect) 和 [**get \_ accFocus**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus) 方法。</span><span class="sxs-lookup"><span data-stu-id="7f86c-109">Because menu bar controls do not receive focus, the [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect) and [**get\_accFocus**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus) methods are not supported for this control.</span></span>

 

## <a name="iaccessible-methods"></a><span data-ttu-id="7f86c-110">IAccessible 方法</span><span class="sxs-lookup"><span data-stu-id="7f86c-110">IAccessible Methods</span></span>

<span data-ttu-id="7f86c-111">功能表列控制項支援下列 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 方法：</span><span class="sxs-lookup"><span data-stu-id="7f86c-111">Menu bar controls support the following [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) methods:</span></span>

-   [<span data-ttu-id="7f86c-112">**accHitTest**</span><span class="sxs-lookup"><span data-stu-id="7f86c-112">**accHitTest**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [<span data-ttu-id="7f86c-113">**accLocation**</span><span class="sxs-lookup"><span data-stu-id="7f86c-113">**accLocation**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [<span data-ttu-id="7f86c-114">**accNavigate**</span><span class="sxs-lookup"><span data-stu-id="7f86c-114">**accNavigate**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [<span data-ttu-id="7f86c-115">**accSelect**</span><span class="sxs-lookup"><span data-stu-id="7f86c-115">**accSelect**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

## <a name="iaccessible-properties"></a><span data-ttu-id="7f86c-116">IAccessible 屬性</span><span class="sxs-lookup"><span data-stu-id="7f86c-116">IAccessible Properties</span></span>

<span data-ttu-id="7f86c-117">功能表列控制項支援下列 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 屬性：</span><span class="sxs-lookup"><span data-stu-id="7f86c-117">Menu bar controls support the following [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) properties:</span></span>



| <span data-ttu-id="7f86c-118">屬性</span><span class="sxs-lookup"><span data-stu-id="7f86c-118">Property</span></span>                                                                             | <span data-ttu-id="7f86c-119">註解</span><span class="sxs-lookup"><span data-stu-id="7f86c-119">Comments</span></span>                                                                                                                                                                                                                                                                                                                                                                         |
|--------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7f86c-120">**取得 \_ accChild**</span><span class="sxs-lookup"><span data-stu-id="7f86c-120">**get\_accChild**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild)                       | <span data-ttu-id="7f86c-121">針對指定的功能表項目抓取 [**IDispatch**](idispatch-interface.md) 。</span><span class="sxs-lookup"><span data-stu-id="7f86c-121">Retrieves the [**IDispatch**](idispatch-interface.md) for the specified menu item.</span></span> <span data-ttu-id="7f86c-122">功能表項目的子識別碼會依序從1開始以左至右編號。</span><span class="sxs-lookup"><span data-stu-id="7f86c-122">The child IDs for the menu items are numbered sequentially from left to right starting with one.</span></span>                                                                                                                                                                                             |
| [<span data-ttu-id="7f86c-123">**取得 \_ accChildCount**</span><span class="sxs-lookup"><span data-stu-id="7f86c-123">**get\_accChildCount**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)             | <span data-ttu-id="7f86c-124">**ChildCount** 屬性是功能表列上的功能表項目數目。</span><span class="sxs-lookup"><span data-stu-id="7f86c-124">The **ChildCount** property is the number of menu items on the menu bar.</span></span> <span data-ttu-id="7f86c-125">系統功能表的 **ChildCount** 屬性是一個。</span><span class="sxs-lookup"><span data-stu-id="7f86c-125">The **ChildCount** property for a system menu is one.</span></span>                                                                                                                                                                                                                                                   |
| [<span data-ttu-id="7f86c-126">**取得 \_ accDescription**</span><span class="sxs-lookup"><span data-stu-id="7f86c-126">**get\_accDescription**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdescription)           | <span data-ttu-id="7f86c-127">功能表列的 [ **描述** ] 屬性是「包含用來操作目前的視圖或檔的命令」。</span><span class="sxs-lookup"><span data-stu-id="7f86c-127">The **Description** property for a menu bar is "Contains commands to manipulate the current view or document".</span></span> <span data-ttu-id="7f86c-128">系統功能表的 [ **描述** ] 屬性是「包含用來操作視窗的命令」。</span><span class="sxs-lookup"><span data-stu-id="7f86c-128">The **Description** property for a system menu is "Contains commands to manipulate the window".</span></span>                                                                                                                                                                   |
| [<span data-ttu-id="7f86c-129">**取得 \_ accDefaultAction**</span><span class="sxs-lookup"><span data-stu-id="7f86c-129">**get\_accDefaultAction**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdefaultaction)       |                                                                                                                                                                                                                                                                                                                                                                                  |
| [<span data-ttu-id="7f86c-130">**取得 \_ accFocus**</span><span class="sxs-lookup"><span data-stu-id="7f86c-130">**get\_accFocus**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)                       |                                                                                                                                                                                                                                                                                                                                                                                  |
| [<span data-ttu-id="7f86c-131">**取得 \_ accHelp**</span><span class="sxs-lookup"><span data-stu-id="7f86c-131">**get\_accHelp**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelp)                         |                                                                                                                                                                                                                                                                                                                                                                                  |
| [<span data-ttu-id="7f86c-132">**取得 \_ accHelpTopic**</span><span class="sxs-lookup"><span data-stu-id="7f86c-132">**get\_accHelpTopic**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelptopic)               |                                                                                                                                                                                                                                                                                                                                                                                  |
| [<span data-ttu-id="7f86c-133">**取得 \_ accKeyboardShortcut**</span><span class="sxs-lookup"><span data-stu-id="7f86c-133">**get\_accKeyboardShortcut**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut) | <span data-ttu-id="7f86c-134">標題列下方的功能表列的 [ **KeyboardShortcut** ] 屬性是 [Alt]。</span><span class="sxs-lookup"><span data-stu-id="7f86c-134">The **KeyboardShortcut** property for a menu bar beneath the title bar is "Alt".</span></span> <span data-ttu-id="7f86c-135">系統功能表的 **KeyboardShortcut** 屬性是「Alt + 空格鍵」。</span><span class="sxs-lookup"><span data-stu-id="7f86c-135">The **KeyboardShortcut** property for a system menu is "Alt+Space".</span></span>                                                                                                                                                                                                                             |
| [<span data-ttu-id="7f86c-136">**取得 \_ accName**</span><span class="sxs-lookup"><span data-stu-id="7f86c-136">**get\_accName**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)                         | <span data-ttu-id="7f86c-137">標題列下方功能表列的 [ **名稱** ] 屬性是 [應用程式]。</span><span class="sxs-lookup"><span data-stu-id="7f86c-137">The **Name** property for a menu bar beneath the title bar is "Application".</span></span> <span data-ttu-id="7f86c-138">系統功能表的 [ **名稱** ] 屬性是 [system]。</span><span class="sxs-lookup"><span data-stu-id="7f86c-138">The **Name** property for a system menu is "System".</span></span>                                                                                                                                                                                                                                                |
| [<span data-ttu-id="7f86c-139">**取得 \_ accParent**</span><span class="sxs-lookup"><span data-stu-id="7f86c-139">**get\_accParent**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)                     |                                                                                                                                                                                                                                                                                                                                                                                  |
| [<span data-ttu-id="7f86c-140">**取得 \_ accRole**</span><span class="sxs-lookup"><span data-stu-id="7f86c-140">**get\_accRole**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)                         | <span data-ttu-id="7f86c-141">**Role** 屬性是 [**role \_ SYSTEM \_ 功能表列**](object-roles.md)。</span><span class="sxs-lookup"><span data-stu-id="7f86c-141">The **Role** property is [**ROLE\_SYSTEM\_MENUBAR**](object-roles.md).</span></span>                                                                                                                                                                                                                                                                                      |
| [<span data-ttu-id="7f86c-142">**取得 \_ accState**</span><span class="sxs-lookup"><span data-stu-id="7f86c-142">**get\_accState**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)                       | <span data-ttu-id="7f86c-143">**State** 屬性是下列一或多個 [值](object-state-constants.md)的組合：[**狀態 \_ 系統 \_ 隱藏**](object-state-constants.md) \| [**狀態 \_ 系統 \_ 聚焦**](object-state-constants.md)的 \| [**狀態系統可 \_ \_ 設定**](object-state-constants.md)目標</span><span class="sxs-lookup"><span data-stu-id="7f86c-143">The **State** property is a combination of one or more of the following [values](object-state-constants.md): [**STATE\_SYSTEM\_INVISIBLE**](object-state-constants.md) \| [**STATE\_SYSTEM\_FOCUSED**](object-state-constants.md) \| [**STATE\_SYSTEM\_FOCUSABLE**](object-state-constants.md)</span></span><br/> |



 

## <a name="notes"></a><span data-ttu-id="7f86c-144">備註</span><span class="sxs-lookup"><span data-stu-id="7f86c-144">Notes</span></span>

<span data-ttu-id="7f86c-145">系統會觸發一個以上的 [**事件 \_ 系統 \_ MENUSTART**](event-constants.md) 事件，而不一定會有對應的 [**事件 \_ 系統 \_ MENUEND**](event-constants.md) 事件。</span><span class="sxs-lookup"><span data-stu-id="7f86c-145">The system triggers more than one [**EVENT\_SYSTEM\_MENUSTART**](event-constants.md) event that does not always have a corresponding [**EVENT\_SYSTEM\_MENUEND**](event-constants.md) event.</span></span> <span data-ttu-id="7f86c-146">此外，系統不會一致地觸發 [**event \_ system \_ MENUPOPUPSTART**](event-constants.md) 和 [**event \_ system \_ MENUPOPUPEND**](event-constants.md) 事件。</span><span class="sxs-lookup"><span data-stu-id="7f86c-146">Additionally, the system does not trigger the [**EVENT\_SYSTEM\_MENUPOPUPSTART**](event-constants.md) and [**EVENT\_SYSTEM\_MENUPOPUPEND**](event-constants.md) events consistently.</span></span> <span data-ttu-id="7f86c-147">這是已知的問題，並已解決。</span><span class="sxs-lookup"><span data-stu-id="7f86c-147">This is a known issue and is being addressed.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7f86c-148">相關主題</span><span class="sxs-lookup"><span data-stu-id="7f86c-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7f86c-149">IAccessible 介面</span><span class="sxs-lookup"><span data-stu-id="7f86c-149">IAccessible Interface</span></span>](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> <dt>

[<span data-ttu-id="7f86c-150">**功能表項目**</span><span class="sxs-lookup"><span data-stu-id="7f86c-150">**Menu Item**</span></span>](menu-item.md)
</dt> <dt>

[<span data-ttu-id="7f86c-151">**快顯功能表**</span><span class="sxs-lookup"><span data-stu-id="7f86c-151">**Pop-up Menu**</span></span>](pop-up-menu.md)
</dt> </dl>

 

 





