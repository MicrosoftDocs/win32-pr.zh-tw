---
title: 內容快顯視窗
description: 內容快顯視窗是 Windows 功能區架構的 [CoNtextPopup] 視圖中的主要控制項。
ms.assetid: c41b888a-15aa-4c47-ad73-5dc30b5fa6f9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c77441cc3cdcc9212d27d2230d76d2618f1831ab
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106988027"
---
# <a name="context-popup"></a><span data-ttu-id="6b7a6-103">內容快顯視窗</span><span class="sxs-lookup"><span data-stu-id="6b7a6-103">Context Popup</span></span>

<span data-ttu-id="6b7a6-104">內容快顯視窗是 Windows 功能區架構的 [ [**CoNtextPopup] 視圖**](windowsribbon-element-contextpopup.md) 中的主要控制項。</span><span class="sxs-lookup"><span data-stu-id="6b7a6-104">A Context Popup is the principal control in the [**ContextPopup View**](windowsribbon-element-contextpopup.md) of the Windows Ribbon framework.</span></span> <span data-ttu-id="6b7a6-105">它是一個豐富的內容功能表系統，僅由架構公開為功能區實作為擴充功能，架構不會以獨立控制項的形式公開內容快顯視窗。</span><span class="sxs-lookup"><span data-stu-id="6b7a6-105">It is a rich context menu system that is only exposed by the framework as an extension to a Ribbon implementation—the framework does not expose the Context Popup as an independent control.</span></span>

-   [<span data-ttu-id="6b7a6-106">內容快顯視窗的元件</span><span class="sxs-lookup"><span data-stu-id="6b7a6-106">Components of the Context Popup</span></span>](#context-popup)
-   [<span data-ttu-id="6b7a6-107">執行內容快顯視窗</span><span class="sxs-lookup"><span data-stu-id="6b7a6-107">Implement the Context Popup</span></span>](#implement-the-context-popup)
    -   [<span data-ttu-id="6b7a6-108">標記</span><span class="sxs-lookup"><span data-stu-id="6b7a6-108">Markup</span></span>](#markup)
    -   [<span data-ttu-id="6b7a6-109">程式碼</span><span class="sxs-lookup"><span data-stu-id="6b7a6-109">Code</span></span>](#code)
-   [<span data-ttu-id="6b7a6-110">內容快顯功能表屬性</span><span class="sxs-lookup"><span data-stu-id="6b7a6-110">Context Popup Properties</span></span>](#context-popup-properties)
-   [<span data-ttu-id="6b7a6-111">相關主題</span><span class="sxs-lookup"><span data-stu-id="6b7a6-111">Related topics</span></span>](#related-topics)

## <a name="components-of-the-context-popup"></a><span data-ttu-id="6b7a6-112">內容快顯視窗的元件</span><span class="sxs-lookup"><span data-stu-id="6b7a6-112">Components of the Context Popup</span></span>

<span data-ttu-id="6b7a6-113">內容快顯視窗是內容功能表的邏輯容器，也是透過 [**CoNtextMenu**](windowsribbon-element-contextmenu.md) 和 [**浮動工具列**](windowsribbon-element-minitoolbar.md) 標記元素分別公開的 Mini-Toolbar 子控制項：</span><span class="sxs-lookup"><span data-stu-id="6b7a6-113">The Context Popup is a logical container for the Context Menu and Mini-Toolbar sub-controls that are exposed through the [**ContextMenu**](windowsribbon-element-contextmenu.md) and [**MiniToolbar**](windowsribbon-element-minitoolbar.md) markup elements, respectively:</span></span>

-   <span data-ttu-id="6b7a6-114">[**CoNtextMenu**](windowsribbon-element-contextmenu.md)會公開命令和資源庫的功能表。</span><span class="sxs-lookup"><span data-stu-id="6b7a6-114">The [**ContextMenu**](windowsribbon-element-contextmenu.md) exposes a menu of Commands and galleries.</span></span>
-   <span data-ttu-id="6b7a6-115">[**浮動工具列**](windowsribbon-element-minitoolbar.md)會公開各種命令、資源庫和複雜控制項（例如 [字型控制項](windowsribbon-controls-fontcontrol.md)和 [下拉式](windowsribbon-controls-combobox.md)方塊）的浮動工具列。</span><span class="sxs-lookup"><span data-stu-id="6b7a6-115">The [**MiniToolbar**](windowsribbon-element-minitoolbar.md) exposes a floating toolbar of various Commands, galleries, and complex controls such as the [Font Control](windowsribbon-controls-fontcontrol.md) and the [Combo Box](windowsribbon-controls-combobox.md).</span></span>

<span data-ttu-id="6b7a6-116">每個子控制項在內容快顯視窗中最多隻能出現一次。</span><span class="sxs-lookup"><span data-stu-id="6b7a6-116">Each sub-control can appear at most once in a Context Popup.</span></span>

<span data-ttu-id="6b7a6-117">下列螢幕擷取畫面說明內容快顯視窗及其組成子控制項。</span><span class="sxs-lookup"><span data-stu-id="6b7a6-117">The following screen shot illustrates the Context Popup and its constituent sub-controls.</span></span>

![顯示功能區內容 ui 元件之標注的螢幕擷取畫面。](images/controls/contextpopup.png)

<span data-ttu-id="6b7a6-119">內容快顯視窗純粹是概念，而且不會公開任何 UI 功能，例如定位或調整大小。</span><span class="sxs-lookup"><span data-stu-id="6b7a6-119">The Context Popup is purely conceptual and does not expose any UI functionality itself, such as positioning or sizing.</span></span>

> [!Note]  
> <span data-ttu-id="6b7a6-120">在感興趣的物件上，以滑鼠右鍵按一下 (或透過鍵盤快速鍵 SHIFT + F10) ，通常會顯示內容快顯視窗。</span><span class="sxs-lookup"><span data-stu-id="6b7a6-120">The Context Popup is typically displayed by right-clicking the mouse (or through the keyboard shortcut SHIFT+F10) on an object of interest.</span></span> <span data-ttu-id="6b7a6-121">不過，顯示內容快顯視窗所需的步驟是由應用程式所定義。</span><span class="sxs-lookup"><span data-stu-id="6b7a6-121">However, the steps required to display the Context Popup are defined by the application.</span></span>

 

## <a name="implement-the-context-popup"></a><span data-ttu-id="6b7a6-122">執行內容快顯視窗</span><span class="sxs-lookup"><span data-stu-id="6b7a6-122">Implement the Context Popup</span></span>

<span data-ttu-id="6b7a6-123">以類似于其他 Windows 功能區架構控制項的方式，會透過標記元件來執行內容快顯視窗，該元件會指定其簡報詳細資料，以及控制其功能的程式碼元件。</span><span class="sxs-lookup"><span data-stu-id="6b7a6-123">In similar fashion to other Windows Ribbon framework controls, the Context Popup is implemented through a markup component that specifies its presentation details and a code component that governs its functionality.</span></span>

<span data-ttu-id="6b7a6-124">下表列出每個內容快顯項目子控制項所支援的控制項。</span><span class="sxs-lookup"><span data-stu-id="6b7a6-124">The following table lists the controls that are supported by each Context Popup sub-control.</span></span>



| <span data-ttu-id="6b7a6-125">控制</span><span class="sxs-lookup"><span data-stu-id="6b7a6-125">Control</span></span>                                                                  | <span data-ttu-id="6b7a6-126">Mini-Toolbar</span><span class="sxs-lookup"><span data-stu-id="6b7a6-126">Mini-Toolbar</span></span> | <span data-ttu-id="6b7a6-127">操作功能表</span><span class="sxs-lookup"><span data-stu-id="6b7a6-127">Context Menu</span></span> |
|--------------------------------------------------------------------------|--------------|--------------|
| [<span data-ttu-id="6b7a6-128">按鈕</span><span class="sxs-lookup"><span data-stu-id="6b7a6-128">Button</span></span>](windowsribbon-controls-button.md)                              | <span data-ttu-id="6b7a6-129">x</span><span class="sxs-lookup"><span data-stu-id="6b7a6-129">x</span></span>            | <span data-ttu-id="6b7a6-130">x</span><span class="sxs-lookup"><span data-stu-id="6b7a6-130">x</span></span>            |
| [<span data-ttu-id="6b7a6-131">核取方塊</span><span class="sxs-lookup"><span data-stu-id="6b7a6-131">Check Box</span></span>](windowsribbon-controls-checkbox.md)                         | <span data-ttu-id="6b7a6-132">x</span><span class="sxs-lookup"><span data-stu-id="6b7a6-132">x</span></span>            | <span data-ttu-id="6b7a6-133">x</span><span class="sxs-lookup"><span data-stu-id="6b7a6-133">x</span></span>            |
| [<span data-ttu-id="6b7a6-134">下拉式方塊</span><span class="sxs-lookup"><span data-stu-id="6b7a6-134">Combo Box</span></span>](windowsribbon-controls-combobox.md)                         | <span data-ttu-id="6b7a6-135">x</span><span class="sxs-lookup"><span data-stu-id="6b7a6-135">x</span></span>            |              |
| [<span data-ttu-id="6b7a6-136">下拉式按鈕</span><span class="sxs-lookup"><span data-stu-id="6b7a6-136">Drop-Down Button</span></span>](windowsribbon-controls-dropdownbutton.md)            | <span data-ttu-id="6b7a6-137">x</span><span class="sxs-lookup"><span data-stu-id="6b7a6-137">x</span></span>            | <span data-ttu-id="6b7a6-138">x</span><span class="sxs-lookup"><span data-stu-id="6b7a6-138">x</span></span>            |
| [<span data-ttu-id="6b7a6-139">下拉式色彩選擇器</span><span class="sxs-lookup"><span data-stu-id="6b7a6-139">Drop-Down Color Picker</span></span>](windowsribbon-controls-dropdowncolorpicker.md) | <span data-ttu-id="6b7a6-140">x</span><span class="sxs-lookup"><span data-stu-id="6b7a6-140">x</span></span>            | <span data-ttu-id="6b7a6-141">x</span><span class="sxs-lookup"><span data-stu-id="6b7a6-141">x</span></span>            |
| [<span data-ttu-id="6b7a6-142">下拉式圖庫</span><span class="sxs-lookup"><span data-stu-id="6b7a6-142">Drop-Down Gallery</span></span>](windowsribbon-controls-dropdowngallery.md)          | <span data-ttu-id="6b7a6-143">x</span><span class="sxs-lookup"><span data-stu-id="6b7a6-143">x</span></span>            | <span data-ttu-id="6b7a6-144">x</span><span class="sxs-lookup"><span data-stu-id="6b7a6-144">x</span></span>            |
| [<span data-ttu-id="6b7a6-145">字型控制項</span><span class="sxs-lookup"><span data-stu-id="6b7a6-145">Font Control</span></span>](windowsribbon-controls-fontcontrol.md)                   | <span data-ttu-id="6b7a6-146">x</span><span class="sxs-lookup"><span data-stu-id="6b7a6-146">x</span></span>            |              |
| [<span data-ttu-id="6b7a6-147">說明按鈕</span><span class="sxs-lookup"><span data-stu-id="6b7a6-147">Help Button</span></span>](windowsribbon-controls-helpbutton.md)                     |              |              |
| [<span data-ttu-id="6b7a6-148">功能區中的資源庫</span><span class="sxs-lookup"><span data-stu-id="6b7a6-148">In-Ribbon Gallery</span></span>](windowsribbon-controls-inribbongallery.md)          |              |              |
| [<span data-ttu-id="6b7a6-149">Spinner</span><span class="sxs-lookup"><span data-stu-id="6b7a6-149">Spinner</span></span>](windowsribbon-controls-spinner.md)                            |              |              |
| [<span data-ttu-id="6b7a6-150">分割按鈕</span><span class="sxs-lookup"><span data-stu-id="6b7a6-150">Split Button</span></span>](windowsribbon-controls-splitbutton.md)                   | <span data-ttu-id="6b7a6-151">x</span><span class="sxs-lookup"><span data-stu-id="6b7a6-151">x</span></span>            | <span data-ttu-id="6b7a6-152">x</span><span class="sxs-lookup"><span data-stu-id="6b7a6-152">x</span></span>            |
| [<span data-ttu-id="6b7a6-153">分割按鈕資源庫</span><span class="sxs-lookup"><span data-stu-id="6b7a6-153">Split Button Gallery</span></span>](windowsribbon-controls-splitbuttongallery.md)    | <span data-ttu-id="6b7a6-154">x</span><span class="sxs-lookup"><span data-stu-id="6b7a6-154">x</span></span>            | <span data-ttu-id="6b7a6-155">x</span><span class="sxs-lookup"><span data-stu-id="6b7a6-155">x</span></span>            |
| [<span data-ttu-id="6b7a6-156">切換按鈕</span><span class="sxs-lookup"><span data-stu-id="6b7a6-156">Toggle Button</span></span>](windowsribbon-controls-togglebutton.md)                 | <span data-ttu-id="6b7a6-157">x</span><span class="sxs-lookup"><span data-stu-id="6b7a6-157">x</span></span>            | <span data-ttu-id="6b7a6-158">x</span><span class="sxs-lookup"><span data-stu-id="6b7a6-158">x</span></span>            |



 

### <a name="markup"></a><span data-ttu-id="6b7a6-159">標記</span><span class="sxs-lookup"><span data-stu-id="6b7a6-159">Markup</span></span>

<span data-ttu-id="6b7a6-160">每個內容快顯視窗子控制項都必須在標記中個別宣告。</span><span class="sxs-lookup"><span data-stu-id="6b7a6-160">Each Context Popup sub-control must be declared individually in markup.</span></span>

### <a name="mini-toolbar"></a><span data-ttu-id="6b7a6-161">Mini-Toolbar</span><span class="sxs-lookup"><span data-stu-id="6b7a6-161">Mini-Toolbar</span></span>

<span data-ttu-id="6b7a6-162">將控制項新增至內容快顯視窗迷你工具列時，應考慮下列兩個建議：</span><span class="sxs-lookup"><span data-stu-id="6b7a6-162">When adding controls to a Context Popup Mini-Toolbar, the following two recommendations should be considered:</span></span>

-   <span data-ttu-id="6b7a6-163">控制項應可高度辨識，並提供明顯的功能。</span><span class="sxs-lookup"><span data-stu-id="6b7a6-163">Controls should be highly recognizable and provide obvious functionality.</span></span> <span data-ttu-id="6b7a6-164">熟悉的是關鍵，因為標籤和工具提示不會公開給 Mini-Toolbar 控制項。</span><span class="sxs-lookup"><span data-stu-id="6b7a6-164">Familiarity is key, as labels and tooltips are not exposed for Mini-Toolbar controls.</span></span>
-   <span data-ttu-id="6b7a6-165">控制項所公開的每個命令都應該顯示在功能區 UI 的其他位置。</span><span class="sxs-lookup"><span data-stu-id="6b7a6-165">Each Command exposed by a control should be presented elsewhere in the ribbon UI.</span></span> <span data-ttu-id="6b7a6-166">Mini-Toolbar 不支援鍵盤流覽。</span><span class="sxs-lookup"><span data-stu-id="6b7a6-166">The Mini-Toolbar does not support keyboard navigation.</span></span>

<span data-ttu-id="6b7a6-167">下列範例示範 [**浮動工具列**](windowsribbon-element-minitoolbar.md) 專案的基本標記，其中包含三個 [按鈕](windowsribbon-controls-button.md) 控制項。</span><span class="sxs-lookup"><span data-stu-id="6b7a6-167">The following example demonstrates the basic markup for a [**MiniToolbar**](windowsribbon-element-minitoolbar.md) element that contains three [Button](windowsribbon-controls-button.md) controls.</span></span>

> [!Note]  
> <span data-ttu-id="6b7a6-168">針對迷你工具列中的每個控制項資料列指定一個 [**MenuGroup**](windowsribbon-element-menugroup.md) 元素。</span><span class="sxs-lookup"><span data-stu-id="6b7a6-168">One [**MenuGroup**](windowsribbon-element-menugroup.md) element is specified for each row of controls in the Mini-Toolbar.</span></span>

 


```C++
<MiniToolbar Name="MiniToolbar">
  <MenuGroup>
    <Button CommandName="cmdButton1" />
    <Button CommandName="cmdButton2" />
    <Button CommandName="cmdButton3" />
  </MenuGroup>
</MiniToolbar>
```



### <a name="context-menu"></a><span data-ttu-id="6b7a6-169">操作功能表</span><span class="sxs-lookup"><span data-stu-id="6b7a6-169">Context Menu</span></span>

<span data-ttu-id="6b7a6-170">下列範例示範 [**CoNtextMenu**](windowsribbon-element-contextmenu.md) 專案的基本標記，其中包含三個 [按鈕](windowsribbon-controls-button.md) 控制項。</span><span class="sxs-lookup"><span data-stu-id="6b7a6-170">The following example demonstrates the basic markup for a [**ContextMenu**](windowsribbon-element-contextmenu.md) element that contains three [Button](windowsribbon-controls-button.md) controls.</span></span>

> [!Note]  
> <span data-ttu-id="6b7a6-171">[**MenuGroup**](windowsribbon-element-menugroup.md)元素中的每一組控制項都會以內容功能表中的水準橫條分隔。</span><span class="sxs-lookup"><span data-stu-id="6b7a6-171">Each set of controls in the [**MenuGroup**](windowsribbon-element-menugroup.md) element is separated by a horizontal bar in the Context Menu.</span></span>

 


```C++
<ContextMenu Name="ContextMenu">
  <MenuGroup>
    <Button CommandName="cmdCut" />
    <Button CommandName="cmdCopy" />
    <Button CommandName="cmdPaste" />
  </MenuGroup>
</ContextMenu>
```



<span data-ttu-id="6b7a6-172">雖然內容快顯視窗最多可包含每個子控制項的其中一個，但功能區標記中的多個 [**CoNtextMenu**](windowsribbon-element-contextmenu.md) 和 [**浮動工具列**](windowsribbon-element-minitoolbar.md) 元素宣告是有效的。</span><span class="sxs-lookup"><span data-stu-id="6b7a6-172">Although a Context Popup can contain at most one of each sub-control, multiple [**ContextMenu**](windowsribbon-element-contextmenu.md) and [**MiniToolbar**](windowsribbon-element-minitoolbar.md) element declarations in the Ribbon markup are valid.</span></span> <span data-ttu-id="6b7a6-173">如此一來，應用程式就可以根據應用程式所定義的準則（例如工作區內容）支援各種內容功能表和 Mini-Toolbar 控制群組合。</span><span class="sxs-lookup"><span data-stu-id="6b7a6-173">This allows an application to support various combinations of Context Menu and Mini-Toolbar controls, based on criteria defined by the application, such as workspace context.</span></span>

<span data-ttu-id="6b7a6-174">如需詳細資訊，請參閱 [**CoNtextMap**](windowsribbon-element-contextmap.md) 元素。</span><span class="sxs-lookup"><span data-stu-id="6b7a6-174">For more information, see the [**ContextMap**](windowsribbon-element-contextmap.md) element.</span></span>

<span data-ttu-id="6b7a6-175">下列範例示範 [**CoNtextPopup**](windowsribbon-element-contextpopup.md) 元素的基本標記。</span><span class="sxs-lookup"><span data-stu-id="6b7a6-175">The following example demonstrates the basic markup for the [**ContextPopup**](windowsribbon-element-contextpopup.md) element.</span></span>


```C++
<ContextPopup>
  <ContextPopup.MiniToolbars>
    <MiniToolbar Name="MiniToolbar">
      <MenuGroup>
        <Button CommandName="cmdButton1" />
        <Button CommandName="cmdButton2" />
        <Button CommandName="cmdButton3" />
      </MenuGroup>
    </MiniToolbar>
  </ContextPopup.MiniToolbars>
  <ContextPopup.ContextMenus>
    <ContextMenu Name="ContextMenu">
      <MenuGroup>
        <Button CommandName="cmdCut" />
        <Button CommandName="cmdCopy" />
        <Button CommandName="cmdPaste" />
      </MenuGroup>
    </ContextMenu>
  </ContextPopup.ContextMenus>
  <ContextPopup.ContextMaps>
    <ContextMap CommandName="cmdContextMap" ContextMenu="ContextMenu" MiniToolbar="MiniToolbar"/>
  </ContextPopup.ContextMaps>
</ContextPopup>
```



### <a name="code"></a><span data-ttu-id="6b7a6-176">程式碼</span><span class="sxs-lookup"><span data-stu-id="6b7a6-176">Code</span></span>

<span data-ttu-id="6b7a6-177">若要叫用內容快顯視窗，在功能區應用程式的最上層視窗收到 WM CONTEXTMENU 通知時，會呼叫 [**IUICoNtextualUI：： ShowAtLocation**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicontextualui-showatlocation) 方法 \_ 。</span><span class="sxs-lookup"><span data-stu-id="6b7a6-177">To invoke a Context Popup, the [**IUIContextualUI::ShowAtLocation**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicontextualui-showatlocation) method is called when the top-level window of the Ribbon application receives a WM\_CONTEXTMENU notification.</span></span>

<span data-ttu-id="6b7a6-178">此範例示範如何 \_ 在功能區應用程式的 WndProc () 方法中處理 WM CONTEXTMENU 通知。</span><span class="sxs-lookup"><span data-stu-id="6b7a6-178">This example demonstrates how to handle the WM\_CONTEXTMENU notification in the WndProc() method of the Ribbon application.</span></span>


```C++
case WM_CONTEXTMENU:
  POINT pt;
  POINTSTOPOINT(pt, lParam);

  // ShowContextualUI method defined by the application.
  ShowContextualUI (pt, hWnd);
  break;
```



<span data-ttu-id="6b7a6-179">下列範例會示範功能區應用程式如何使用 [**IUICoNtextualUI：： ShowAtLocation**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicontextualui-showatlocation) 方法，在特定螢幕位置顯示內容快顯視窗。</span><span class="sxs-lookup"><span data-stu-id="6b7a6-179">The following example demonstrates how a Ribbon application can show the Context Popup at a specific screen location using the [**IUIContextualUI::ShowAtLocation**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicontextualui-showatlocation) method.</span></span>

<span data-ttu-id="6b7a6-180">GetCurrentCoNtext () 具有 `cmdContextMap` 上述標記範例中所定義的值。</span><span class="sxs-lookup"><span data-stu-id="6b7a6-180">GetCurrentContext() has a value of `cmdContextMap` as defined in the preceding markup example.</span></span>

<span data-ttu-id="6b7a6-181">g \_ pApplication 是 [**IUIFramework**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiframework) 介面的參考。</span><span class="sxs-lookup"><span data-stu-id="6b7a6-181">g\_pApplication is a reference to the [**IUIFramework**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiframework) interface.</span></span>


```C++
HRESULT ShowContextualUI(POINT& ptLocation, HWND hWnd)
{
  GetDisplayLocation(ptLocation, hWnd);

  HRESULT hr = E_FAIL;

  IUIContextualUI* pContextualUI = NULL;
 
  if (SUCCEEDED(g_pFramework->GetView(
                                g_pApplication->GetCurrentContext(), 
                                IID_PPV_ARGS(&pContextualUI))))
  {
    hr = pContextualUI->ShowAtLocation(ptLocation.x, ptLocation.y);
    pContextualUI->Release();
  }

  return hr;
}
```



<span data-ttu-id="6b7a6-182">您可以在關閉內容快顯視窗之前釋放 [**IUICoNtextualUI**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicontextualui) 的參考，如上述範例所示。</span><span class="sxs-lookup"><span data-stu-id="6b7a6-182">The reference to [**IUIContextualUI**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicontextualui) can be released before the Context Popup is dismissed, as shown in the preceding example.</span></span> <span data-ttu-id="6b7a6-183">不過，您必須在某個時間點釋放參考，以避免記憶體流失。</span><span class="sxs-lookup"><span data-stu-id="6b7a6-183">However, the reference must be released at some point to avoid memory leaks.</span></span>

> [!Caution]  
> <span data-ttu-id="6b7a6-184">Mini-Toolbar 的內建淡化效果是以滑鼠指標的相近為基礎。</span><span class="sxs-lookup"><span data-stu-id="6b7a6-184">The Mini-Toolbar has a built-in fade effect that is based on the proximity of the mouse pointer.</span></span> <span data-ttu-id="6b7a6-185">基於這個理由，建議您盡可能將 Mini-Toolbar 顯示為靠近滑鼠指標。</span><span class="sxs-lookup"><span data-stu-id="6b7a6-185">For this reason, it is recommended that the Mini-Toolbar be displayed as close to the mouse pointer as possible.</span></span> <span data-ttu-id="6b7a6-186">否則，由於衝突的顯示機制，Mini-Toolbar 可能不會如預期般呈現。</span><span class="sxs-lookup"><span data-stu-id="6b7a6-186">Otherwise, due to the conflicting display mechanisms, the Mini-Toolbar may not render as expected.</span></span>

 

## <a name="context-popup-properties"></a><span data-ttu-id="6b7a6-187">內容快顯功能表屬性</span><span class="sxs-lookup"><span data-stu-id="6b7a6-187">Context Popup Properties</span></span>

<span data-ttu-id="6b7a6-188">沒有與內容快顯功能表控制項相關聯的屬性索引鍵。</span><span class="sxs-lookup"><span data-stu-id="6b7a6-188">There are no property keys associated with the Context Popup control.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6b7a6-189">相關主題</span><span class="sxs-lookup"><span data-stu-id="6b7a6-189">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6b7a6-190">Windows 功能區架構控制項程式庫</span><span class="sxs-lookup"><span data-stu-id="6b7a6-190">Windows Ribbon Framework Control Library</span></span>](windowsribbon-controls-entry.md)
</dt> <dt>

[<span data-ttu-id="6b7a6-191">CoNtextPopup 範例</span><span class="sxs-lookup"><span data-stu-id="6b7a6-191">ContextPopup Sample</span></span>](windowsribbon-contextpopupsample.md)
</dt> </dl>

 

 