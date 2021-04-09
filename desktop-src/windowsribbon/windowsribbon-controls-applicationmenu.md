---
title: 應用程式功能表
description: '[應用程式] 功能表是執行 Windows 功能區架構之應用程式的主功能表。'
ms.assetid: 5be93a5b-277b-44c1-be24-a0598a140bfc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e99f57045daa35149e5fa074cb59e2f538c589b2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103842308"
---
# <a name="application-menu"></a><span data-ttu-id="0e702-103">應用程式功能表</span><span class="sxs-lookup"><span data-stu-id="0e702-103">Application Menu</span></span>

<span data-ttu-id="0e702-104">[應用程式] 功能表是執行 Windows 功能區架構之應用程式的主功能表。</span><span class="sxs-lookup"><span data-stu-id="0e702-104">The Application Menu is the main menu for an application that implements the Windows Ribbon framework.</span></span>

-   [<span data-ttu-id="0e702-105">簡介</span><span class="sxs-lookup"><span data-stu-id="0e702-105">Introduction</span></span>](#introduction)
-   [<span data-ttu-id="0e702-106">應用程式功能表的元件</span><span class="sxs-lookup"><span data-stu-id="0e702-106">Components of the Application Menu</span></span>](#components-of-the-application-menu)
    -   [<span data-ttu-id="0e702-107">應用程式功能表 MenuGroup</span><span class="sxs-lookup"><span data-stu-id="0e702-107">Application Menu MenuGroup</span></span>](#application-menu-menugroup)
-   [<span data-ttu-id="0e702-108">調整應用程式功能表的大小</span><span class="sxs-lookup"><span data-stu-id="0e702-108">Sizing the Application Menu</span></span>](#sizing-the-application-menu)
-   [<span data-ttu-id="0e702-109">應用程式功能表屬性</span><span class="sxs-lookup"><span data-stu-id="0e702-109">Application Menu Properties</span></span>](#application-menu-properties)
-   [<span data-ttu-id="0e702-110">相關主題</span><span class="sxs-lookup"><span data-stu-id="0e702-110">Related topics</span></span>](#related-topics)

## <a name="introduction"></a><span data-ttu-id="0e702-111">簡介</span><span class="sxs-lookup"><span data-stu-id="0e702-111">Introduction</span></span>

<span data-ttu-id="0e702-112">[應用程式] 功能表是由下拉式按鈕控制項所組成，它會顯示一個功能表，其中包含的命令會公開與完整專案相關的功能，例如整個檔、圖片或影片。</span><span class="sxs-lookup"><span data-stu-id="0e702-112">The Application Menu is composed of a drop-down button control that displays a menu containing Commands that expose functionality related to a complete project, such as an entire document, picture, or movie.</span></span> <span data-ttu-id="0e702-113">範例包括 [**新增**]、[**開啟**]、[**儲存**] 和 [結束 **] 命令。**</span><span class="sxs-lookup"><span data-stu-id="0e702-113">Examples include the **New**, **Open**, **Save**, and **Exit** Commands.</span></span>

<span data-ttu-id="0e702-114">下列螢幕擷取畫面顯示應用程式功能表。</span><span class="sxs-lookup"><span data-stu-id="0e702-114">The following screen shot illustrates the Application Menu.</span></span>

![windows 7 功能區的 [應用程式] 功能表和 [最近使用的專案] 清單的螢幕擷取畫面。](images/controls/recentitems.png)

## <a name="components-of-the-application-menu"></a><span data-ttu-id="0e702-116">應用程式功能表的元件</span><span class="sxs-lookup"><span data-stu-id="0e702-116">Components of the Application Menu</span></span>

<span data-ttu-id="0e702-117">應用程式功能表是任何功能區應用程式中的必要元素。</span><span class="sxs-lookup"><span data-stu-id="0e702-117">The Application Menu is a mandatory element in any Ribbon application.</span></span> <span data-ttu-id="0e702-118">[應用程式 []](windowsribbon-controls-tab.md) 功能表中的進入點是一種特殊按鈕，會顯示為索引標籤資料列中的第一個專案，如下列螢幕擷取畫面所示。</span><span class="sxs-lookup"><span data-stu-id="0e702-118">The entry point into the Application Menu is a distinctive button that appears as the first item in the [Tab](windowsribbon-controls-tab.md) row, as shown in the following screen shot.</span></span>

> [!Note]  
> <span data-ttu-id="0e702-119">Windows 8 和更新版本：應用程式功能表按鈕影像已變更為 label： **File**。</span><span class="sxs-lookup"><span data-stu-id="0e702-119">Windows 8 and newer: Application Menu button image changed to label: **File**.</span></span> <span data-ttu-id="0e702-120">建議您不要使用 [檔案] 作為任何您自己的索引標籤的標籤。</span><span class="sxs-lookup"><span data-stu-id="0e702-120">We recommend that you do not use File as the label for any of your own tabs.</span></span>

 

![適用于 windows 7 之 wordpad 的 [應用程式] 功能表按鈕的螢幕擷取畫面。](images/overviews/applicationmenu-button.png)

<span data-ttu-id="0e702-122">按一下時，此按鈕會顯示在下列螢幕擷取畫面中顯示的豐富功能表 (從 WordPad for Windows 7) 的應用程式功能表。</span><span class="sxs-lookup"><span data-stu-id="0e702-122">When clicked, this button displays the rich menu that is shown in the following screen shot (the Application Menu from WordPad for Windows 7).</span></span>

![適用于 windows 7 之 wordpad 的 [應用程式] 功能表功能表的螢幕擷取畫面。](images/overviews/applicationmenu-menu.png)

> [!Note]  
> <span data-ttu-id="0e702-124">按一下 [應用程式] 功能表按鈕時，不會影響索引標籤設定;相反地，焦點會進入功能表。</span><span class="sxs-lookup"><span data-stu-id="0e702-124">There is no impact on the tab set when the Application Menu button is clicked; instead, the focus enters the menu.</span></span>

 

<span data-ttu-id="0e702-125">[應用程式] 功能表包含兩個窗格：一或多個 [**MenuGroup**](windowsribbon-element-menugroup.md)專案所代表的命令清單，以及由 [**ApplicationMenu. RecentItems**](windowsribbon-element-applicationmenu-recentitems.md)元素表示的 [最新專案](windowsribbon-controls-recentitems.md)清單。</span><span class="sxs-lookup"><span data-stu-id="0e702-125">The Application Menu contains two panes: a list of Commands represented by one or more [**MenuGroup**](windowsribbon-element-menugroup.md) elements, and a [Recent Items](windowsribbon-controls-recentitems.md) list represented by an [**ApplicationMenu.RecentItems**](windowsribbon-element-applicationmenu-recentitems.md) element.</span></span>

### <a name="application-menu-menugroup"></a><span data-ttu-id="0e702-126">應用程式功能表 MenuGroup</span><span class="sxs-lookup"><span data-stu-id="0e702-126">Application Menu MenuGroup</span></span>

<span data-ttu-id="0e702-127">[**ApplicationMenu**](windowsribbon-element-applicationmenu.md)元素必須包含至少一個 [**MenuGroup**](windowsribbon-element-menugroup.md)子項目，以公開應用層級命令的清單。</span><span class="sxs-lookup"><span data-stu-id="0e702-127">The [**ApplicationMenu**](windowsribbon-element-applicationmenu.md) element must contain at least one [**MenuGroup**](windowsribbon-element-menugroup.md) child element that exposes a list of application-level commands.</span></span> <span data-ttu-id="0e702-128">如果宣告多個 **MenuGroup** 元素，則會在群組之間繪製分隔線，如下列螢幕擷取畫面所示。</span><span class="sxs-lookup"><span data-stu-id="0e702-128">If multiple **MenuGroup** elements are declared, a divider line is drawn between the groups, as shown in the following screen shot.</span></span>

![應用程式功能表 menugroup 的螢幕擷取畫面。](images/overviews/applicationmenu-menugroup.png)

<span data-ttu-id="0e702-130">以下是應用程式功能表中 [**MenuGroup**](windowsribbon-element-menugroup.md) 元素的條件約束清單：</span><span class="sxs-lookup"><span data-stu-id="0e702-130">The following is a list of constraints for a [**MenuGroup**](windowsribbon-element-menugroup.md) element of an Application Menu:</span></span>

-   <span data-ttu-id="0e702-131">所有的 [**MenuGroup**](windowsribbon-element-menugroup.md) 專案都必須使用的 *類別* 屬性值進行宣告 `MajorItems` 。</span><span class="sxs-lookup"><span data-stu-id="0e702-131">All [**MenuGroup**](windowsribbon-element-menugroup.md) items must be declared with a *Class* attribute value of `MajorItems`.</span></span>
-   <span data-ttu-id="0e702-132">應用程式功能表  [**MenuGroup**](windowsribbon-element-menugroup.md) 僅支援 [按鈕](windowsribbon-controls-button.md)、 [切換按鈕](windowsribbon-controls-togglebutton.md)、 [下拉式按鈕](windowsribbon-controls-dropdownbutton.md)、 [分割按鈕](windowsribbon-controls-splitbutton.md)、 [下拉式清單庫](windowsribbon-controls-dropdowngallery.md)和 [分割按鈕資源庫](windowsribbon-controls-splitbuttongallery.md) 控制項。</span><span class="sxs-lookup"><span data-stu-id="0e702-132">An Application Menu  [**MenuGroup**](windowsribbon-element-menugroup.md) supports only the [Button](windowsribbon-controls-button.md), [Toggle Button](windowsribbon-controls-togglebutton.md), [Drop-Down Button](windowsribbon-controls-dropdownbutton.md), [Split Button](windowsribbon-controls-splitbutton.md), [Drop-Down Gallery](windowsribbon-controls-dropdowngallery.md), and [Split Button Gallery](windowsribbon-controls-splitbuttongallery.md) controls.</span></span>
    > <span data-ttu-id="0e702-133">\[!重要\]</span><span class="sxs-lookup"><span data-stu-id="0e702-133">\[!Important\]</span></span>  
    > <span data-ttu-id="0e702-134">命令資源庫是應用程式功能表中唯一支援的資源庫類型。</span><span class="sxs-lookup"><span data-stu-id="0e702-134">Command galleries are the only type of gallery that are supported in the Application Menu.</span></span> <span data-ttu-id="0e702-135">如需資源庫控制項的詳細資訊，請參閱使用資源 [庫](./ribbon-controls-galleries.md)。</span><span class="sxs-lookup"><span data-stu-id="0e702-135">See [Working with Galleries](./ribbon-controls-galleries.md), for more information on gallery controls.</span></span>

     

<span data-ttu-id="0e702-136">在 [**MenuGroup**](windowsribbon-element-menugroup.md)中使用 [按鈕](windowsribbon-controls-button.md)或 [切換按鈕](windowsribbon-controls-togglebutton.md)時， [**LabelTitle**](windowsribbon-element-command-labeltitle.md)的值會顯示在功能表中，而 [**TooltipTitle**](windowsribbon-element-command-tooltiptitle.md)和 [**TooltipDescription**](windowsribbon-element-command-tooltipdescription.md)命令的值會顯示為工具提示，如下列螢幕擷取畫面所示。</span><span class="sxs-lookup"><span data-stu-id="0e702-136">When a [Button](windowsribbon-controls-button.md) or [Toggle Button](windowsribbon-controls-togglebutton.md) is used in a [**MenuGroup**](windowsribbon-element-menugroup.md), the value of [**Command.LabelTitle**](windowsribbon-element-command-labeltitle.md) is displayed in the menu and the values of [**Command.TooltipTitle**](windowsribbon-element-command-tooltiptitle.md) and [**Command.TooltipDescription**](windowsribbon-element-command-tooltipdescription.md) are displayed as the tooltip, as shown in the following screen shot.</span></span>

![應用程式功能表中按鈕控制項的螢幕擷取畫面。](images/overviews/applicationmenu-menubutton.png)

<span data-ttu-id="0e702-138">在 [應用程式] 功能表中使用 [下拉式](windowsribbon-controls-dropdownbutton.md)按鈕、 [分割按鈕](windowsribbon-controls-splitbutton.md)、 [下拉式清單庫](windowsribbon-controls-dropdowngallery.md)或 [分割按鈕庫](windowsribbon-controls-splitbuttongallery.md) 時，功能表部分會顯示為包含和隱藏 [ **最近使用的專案** ] 窗格的飛出視窗。</span><span class="sxs-lookup"><span data-stu-id="0e702-138">When a [Drop-Down Button](windowsribbon-controls-dropdownbutton.md), [Split Button](windowsribbon-controls-splitbutton.md), [Drop-Down Gallery](windowsribbon-controls-dropdowngallery.md), or [Split Button Gallery](windowsribbon-controls-splitbuttongallery.md) is used in the Application Menu, the menu portion is displayed as a flyout that covers and conceals the **Recent items** pane.</span></span>

<span data-ttu-id="0e702-139">針對 [分割按鈕](windowsribbon-controls-splitbutton.md) 和 [下拉式按鈕](windowsribbon-controls-dropdownbutton.md) 控制項， [**LabelDescription**](windowsribbon-element-command-labeldescription.md) 的值會以內嵌方式顯示在飛出視窗功能表中，以視覺化方式協助使用者探索命令功能。</span><span class="sxs-lookup"><span data-stu-id="0e702-139">For [Split Button](windowsribbon-controls-splitbutton.md) and [Drop-Down Button](windowsribbon-controls-dropdownbutton.md) controls, the value of [**Command.LabelDescription**](windowsribbon-element-command-labeldescription.md) is shown inline in the flyout menu to visually assist users with discovering the Command functionality.</span></span> <span data-ttu-id="0e702-140">**LabelDescription** 的顯示值會以程式設計方式在兩行範圍內中斷，並嘗試將值完全放在下方的 [**最近的專案**] 窗格中。</span><span class="sxs-lookup"><span data-stu-id="0e702-140">The displayed value of **Command.LabelDescription** is programmatically broken over a two-line span, and an attempt is made to fit the value exactly over the **Recent items** pane beneath.</span></span> <span data-ttu-id="0e702-141">如果 **LabelDescription** 值不符合，就會展開飛出視窗以容納最長的 [**命令。**](windowsribbon-element-command-comment.md) [**MenuGroup**](windowsribbon-element-menugroup.md)中的批註值。</span><span class="sxs-lookup"><span data-stu-id="0e702-141">If the **Command.LabelDescription** value does not fit, the flyout will expand to accommodate the longest [**Command.Comment**](windowsribbon-element-command-comment.md) value in the [**MenuGroup**](windowsribbon-element-menugroup.md).</span></span>

<span data-ttu-id="0e702-142">下列螢幕擷取畫面說明 [分割按鈕](windowsribbon-controls-splitbutton.md) 飛出視窗中的這些行為。</span><span class="sxs-lookup"><span data-stu-id="0e702-142">The following screen shot illustrates these behaviors in a [Split Button](windowsribbon-controls-splitbutton.md) flyout.</span></span>

![應用程式功能表中清單控制項飛出視窗的螢幕擷取畫面。](images/overviews/applicationmenu-menuflyout.png)

<span data-ttu-id="0e702-144">使用 [下拉式程式庫](windowsribbon-controls-dropdowngallery.md) 和 [分割按鈕資源庫](windowsribbon-controls-splitbuttongallery.md)時，只會顯示標籤和影像。</span><span class="sxs-lookup"><span data-stu-id="0e702-144">With a [Drop-Down Gallery](windowsribbon-controls-dropdowngallery.md) and a [Split Button Gallery](windowsribbon-controls-splitbuttongallery.md), only a label and an image are shown.</span></span>

## <a name="sizing-the-application-menu"></a><span data-ttu-id="0e702-145">調整應用程式功能表的大小</span><span class="sxs-lookup"><span data-stu-id="0e702-145">Sizing the Application Menu</span></span>

<span data-ttu-id="0e702-146">功能區架構會處理應用程式功能表的大小。</span><span class="sxs-lookup"><span data-stu-id="0e702-146">Sizing of the Application Menu is handled by the Ribbon framework.</span></span> <span data-ttu-id="0e702-147">如果為 [**LabelTitle**](windowsribbon-element-command-labeltitle.md) 或 [**LabelDescription**](windowsribbon-element-command-labeldescription.md)的值提供非常長的字串，或使用一長串的命令，則功能表會調整其大小以容納內容。</span><span class="sxs-lookup"><span data-stu-id="0e702-147">If very long strings are supplied for the value of [**Command.LabelTitle**](windowsribbon-element-command-labeltitle.md) or [**Command.LabelDescription**](windowsribbon-element-command-labeldescription.md), or a long list of Commands is used, the menu will adjust its size to accommodate the contents.</span></span> <span data-ttu-id="0e702-148">某些形式的調整包括擴充 flyouts 或功能表窗格的大小，以及在需要滾動時加入平移檢視器。</span><span class="sxs-lookup"><span data-stu-id="0e702-148">Some forms of adjustment include expanding the size of flyouts or menu panes, and adding pan viewers when scrolling is required.</span></span>

## <a name="application-menu-properties"></a><span data-ttu-id="0e702-149">應用程式功能表屬性</span><span class="sxs-lookup"><span data-stu-id="0e702-149">Application Menu Properties</span></span>

<span data-ttu-id="0e702-150">功能區架構會針對應用程式功能表控制項定義 [屬性索引鍵](windowsribbon-reference-properties.md) 的集合。</span><span class="sxs-lookup"><span data-stu-id="0e702-150">The Ribbon framework defines a collection of [property keys](windowsribbon-reference-properties.md) for the Application Menu control.</span></span>

<span data-ttu-id="0e702-151">一般而言，應用程式功能表屬性會在功能區 UI 中更新，方法是透過呼叫 [**IUIFramework：： InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) 方法來使與控制項相關聯的命令失效。</span><span class="sxs-lookup"><span data-stu-id="0e702-151">Typically, an Application Menu property is updated in the ribbon UI by invalidating the Command associated with the control through a call to the [**IUIFramework::InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) method.</span></span> <span data-ttu-id="0e702-152">會處理「失效」事件，而屬性更新則由 [**IUICommandHandler：： UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) 回呼方法定義。</span><span class="sxs-lookup"><span data-stu-id="0e702-152">The invalidation event is handled and the property updates are defined by the [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) callback method.</span></span>

<span data-ttu-id="0e702-153">[**IUICommandHandler：： UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty)回呼方法未執行，而且應用程式不會針對更新的屬性值進行查詢，直到架構需要該屬性為止。</span><span class="sxs-lookup"><span data-stu-id="0e702-153">The [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) callback method is not executed and the application is not queried for an updated property value until the property is required by the framework.</span></span> <span data-ttu-id="0e702-154">例如，當啟用索引標籤，且在功能區 UI 中顯示控制項，或顯示工具提示時，架構會要求屬性。</span><span class="sxs-lookup"><span data-stu-id="0e702-154">For example, the framework requires the property when a tab is activated and a control is revealed in the ribbon UI, or when a tooltip is displayed.</span></span>



| <span data-ttu-id="0e702-155">屬性索引鍵</span><span class="sxs-lookup"><span data-stu-id="0e702-155">Property key</span></span>                                                                                     | <span data-ttu-id="0e702-156">備註</span><span class="sxs-lookup"><span data-stu-id="0e702-156">Notes</span></span>                                     |
|--------------------------------------------------------------------------------------------------|-------------------------------------------|
| [<span data-ttu-id="0e702-157">UI \_ PKEY \_ TooltipDescription</span><span class="sxs-lookup"><span data-stu-id="0e702-157">UI\_PKEY\_TooltipDescription</span></span>](windowsribbon-reference-properties-uipkey-tooltipdescription.md) | <span data-ttu-id="0e702-158">只能透過失效進行更新。</span><span class="sxs-lookup"><span data-stu-id="0e702-158">Can only be updated through invalidation.</span></span> |
| [<span data-ttu-id="0e702-159">UI \_ PKEY \_ TooltipTitle</span><span class="sxs-lookup"><span data-stu-id="0e702-159">UI\_PKEY\_TooltipTitle</span></span>](windowsribbon-reference-properties-uipkey-tooltiptitle.md)             | <span data-ttu-id="0e702-160">只能透過失效進行更新。</span><span class="sxs-lookup"><span data-stu-id="0e702-160">Can only be updated through invalidation.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="0e702-161">相關主題</span><span class="sxs-lookup"><span data-stu-id="0e702-161">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0e702-162">Windows 功能區架構控制項程式庫</span><span class="sxs-lookup"><span data-stu-id="0e702-162">Windows Ribbon Framework Control Library</span></span>](windowsribbon-controls-entry.md)
</dt> <dt>

[<span data-ttu-id="0e702-163">**ApplicationMenu 標記元素**</span><span class="sxs-lookup"><span data-stu-id="0e702-163">**ApplicationMenu markup element**</span></span>](windowsribbon-element-applicationmenu.md)
</dt> </dl>

 

 