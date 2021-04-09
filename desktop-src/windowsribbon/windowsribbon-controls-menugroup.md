---
title: 功能表群組
description: 功能表群組會在功能表或工具列中組織相關的命令和控制項。
ms.assetid: 5454f2a3-275b-47f4-ae97-d10dd12da5ff
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9862e78cbedf84b92c7540bec4de58288af5c9ef
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103933506"
---
# <a name="menu-group"></a><span data-ttu-id="9fcd0-103">功能表群組</span><span class="sxs-lookup"><span data-stu-id="9fcd0-103">Menu Group</span></span>

<span data-ttu-id="9fcd0-104">功能表群組會在功能表或工具列中組織相關的命令和控制項。</span><span class="sxs-lookup"><span data-stu-id="9fcd0-104">The Menu Group organizes related Commands and controls within a menu or toolbar.</span></span>

-   [<span data-ttu-id="9fcd0-105">簡介</span><span class="sxs-lookup"><span data-stu-id="9fcd0-105">Introduction</span></span>](#introduction)
-   [<span data-ttu-id="9fcd0-106">功能表群組屬性</span><span class="sxs-lookup"><span data-stu-id="9fcd0-106">Menu Group Properties</span></span>](#menu-group-properties)
-   [<span data-ttu-id="9fcd0-107">相關主題</span><span class="sxs-lookup"><span data-stu-id="9fcd0-107">Related topics</span></span>](#related-topics)

## <a name="introduction"></a><span data-ttu-id="9fcd0-108">簡介</span><span class="sxs-lookup"><span data-stu-id="9fcd0-108">Introduction</span></span>

<span data-ttu-id="9fcd0-109">透過 [**MenuGroup**](windowsribbon-element-menugroup.md) 標記專案公開的功能表群組控制項，是以功能表為基礎之控制項中的專案或命令群組的邏輯容器，包括 [內容快捷](windowsribbon-controls-contextpopup.md) 功能表迷你工具列。</span><span class="sxs-lookup"><span data-stu-id="9fcd0-109">The Menu Group control, exposed through the [**MenuGroup**](windowsribbon-element-menugroup.md) markup element, is a logical container for groups of items or Commands in menu-based controls, including the [Context Popup](windowsribbon-controls-contextpopup.md) Mini-Toolbar.</span></span>

<span data-ttu-id="9fcd0-110">您可以透過相關聯命令宣告的 *LabelTitle* 屬性或 [**LabelTitle**](windowsribbon-element-command-labeltitle.md) 屬性，為功能表群組指定標籤。</span><span class="sxs-lookup"><span data-stu-id="9fcd0-110">A label can be specified for a Menu Group through the *LabelTitle* attribute or [**Command.LabelTitle**](windowsribbon-element-command-labeltitle.md) property of an associated Command declaration.</span></span> <span data-ttu-id="9fcd0-111">指派給 *LabelTitle* 的值會轉譯為分類標頭。</span><span class="sxs-lookup"><span data-stu-id="9fcd0-111">The value assigned to *LabelTitle* is rendered as a category header.</span></span>

<span data-ttu-id="9fcd0-112">下列範例會示範 [分割按鈕](windowsribbon-controls-splitbutton.md) 控制項的命令標記，其中包含兩個功能表群組命令聲明。</span><span class="sxs-lookup"><span data-stu-id="9fcd0-112">The following example demonstrates the Command markup for a [Split Button](windowsribbon-controls-splitbutton.md) control that includes two Menu Group Command declarations.</span></span>


```XML
<!-- SplitButton -->
<Command Name="cmdSplitButtonGroup"
         Symbol="cmdSplitButtonGroup"
         Comment="SplitButton Group"
         LabelTitle="SplitButton"/>
<Command Name="cmdSplitButton"
         Symbol="cmdSplitButton"
         Comment="SplitButton"
         LabelTitle="SplitButton"/>
<Command Name="cmdSBButtonItem"
         Symbol="cmdSBButtonItem"
         Comment="SBButtonItem"
         LabelTitle="SB ButtonItem"/>
<Command Name="cmdSBButton1"
         Symbol="cmdSBButton1"
         Comment="SBButton1"
         LabelTitle="SB Button">
  <Command.LargeImages>
    <Image Source="res/copyL_32.bmp"/>
  </Command.LargeImages>
  <Command.SmallImages>
    <Image Source="res/copyS_16.bmp"/>
  </Command.SmallImages>
  <Command.LargeHighContrastImages>
    <Image Source="res/copyLHC_32.bmp"/>
  </Command.LargeHighContrastImages>
  <Command.SmallHighContrastImages>
    <Image Source="res/copySHC_16.bmp"/>
  </Command.SmallHighContrastImages>
</Command>
<Command Name="cmdSBMajorItems"
         Comment="Major Items Category"
         LabelTitle="Major Items"/>
<Command Name="cmdSBStandardItems"
         Comment="Standard Items Category"
         LabelTitle="Standard Items"/>
```



<span data-ttu-id="9fcd0-113">下列範例示範具有三個 [**MenuGroup**](windowsribbon-element-menugroup.md)元素宣告的 [**SplitButton**](windowsribbon-element-splitbutton.md)元素所需的標記，其中兩個會與上一個範例中的功能表群組命令相關聯。</span><span class="sxs-lookup"><span data-stu-id="9fcd0-113">The following example demonstrates the markup required for a [**SplitButton**](windowsribbon-element-splitbutton.md) element with three [**MenuGroup**](windowsribbon-element-menugroup.md) element declarations, two of which are associated with the Menu Group Commands from the previous example.</span></span> <span data-ttu-id="9fcd0-114">**MenuGroup** 元素的 *Class* 屬性可用來指定功能表項目的大小。</span><span class="sxs-lookup"><span data-stu-id="9fcd0-114">The *Class* attribute of the **MenuGroup** element is used to specify the size of the menu items.</span></span>


```XML
<Group CommandName="cmdSplitButtonGroup">
  <SplitButton CommandName="cmdSplitButton">
    <SplitButton.ButtonItem>
      <Button CommandName="cmdSBButtonItem"/>
    </SplitButton.ButtonItem>
    <SplitButton.MenuGroups>
      <MenuGroup CommandName="cmdSBMajorItems" 
                 Class="MajorItems">
        <Button CommandName="cmdSBButton1"/>
        <Button CommandName="cmdSBButton1"/>
      </MenuGroup>
      <MenuGroup CommandName="cmdSBStandardItems"
                 Class="StandardItems">
        <Button CommandName="cmdSBButton1"/>
        <Button CommandName="cmdSBButton1"/>
      </MenuGroup>
      <MenuGroup Class="StandardItems">
        <Button CommandName="cmdSBButton1"/>
        <Button CommandName="cmdSBButton1"/>
      </MenuGroup>
    </SplitButton.MenuGroups>
  </SplitButton>
</Group>
```



<span data-ttu-id="9fcd0-115">下列螢幕擷取畫面說明功能表 (，其中包含三個功能表群組控制項，) 由上述範例中的標記所產生。</span><span class="sxs-lookup"><span data-stu-id="9fcd0-115">The following screen shot illustrates the menu (with three Menu Group controls) that is generated from the markup in the previous examples.</span></span>

![具有三個功能表群組控制項之功能表的螢幕擷取畫面。](images/controls/menugroup.png)

## <a name="menu-group-properties"></a><span data-ttu-id="9fcd0-117">功能表群組屬性</span><span class="sxs-lookup"><span data-stu-id="9fcd0-117">Menu Group Properties</span></span>

<span data-ttu-id="9fcd0-118">功能區架構會針對功能表群組控制項定義 [屬性索引鍵](windowsribbon-reference-properties.md) 的集合。</span><span class="sxs-lookup"><span data-stu-id="9fcd0-118">The Ribbon framework defines a collection of [property keys](windowsribbon-reference-properties.md) for the Menu Group control.</span></span>

<span data-ttu-id="9fcd0-119">一般而言，功能區 UI 中的功能表群組屬性會透過呼叫 [**IUIFramework：： InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) 方法來使與控制項相關聯的命令失效，藉此更新。</span><span class="sxs-lookup"><span data-stu-id="9fcd0-119">Typically, a Menu Group property is updated in the ribbon UI by invalidating the Command associated with the control through a call to the [**IUIFramework::InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) method.</span></span> <span data-ttu-id="9fcd0-120">[**IUICommandHandler：： UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty)回呼方法會處理失效事件，並定義屬性更新。</span><span class="sxs-lookup"><span data-stu-id="9fcd0-120">The invalidation event is handled, and the property updates defined, by the [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) callback method.</span></span>

<span data-ttu-id="9fcd0-121">[**IUICommandHandler：： UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty)回呼方法未執行，而且應用程式會查詢已更新的屬性值，直到架構需要該屬性為止。</span><span class="sxs-lookup"><span data-stu-id="9fcd0-121">The [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) callback method is not executed, and the application queried for an updated property value, until the property is required by the framework.</span></span> <span data-ttu-id="9fcd0-122">例如，啟用索引標籤時，以及在功能區 UI 中顯示控制項，或顯示工具提示時。</span><span class="sxs-lookup"><span data-stu-id="9fcd0-122">For example, when a tab is activated and a control revealed in the ribbon UI, or when a tooltip is displayed.</span></span>

> [!Note]  
> <span data-ttu-id="9fcd0-123">在某些情況下，可以透過 [**IUIFramework：： GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) 方法抓取屬性，並使用 [**IUIFramework：： SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) 方法進行設定。</span><span class="sxs-lookup"><span data-stu-id="9fcd0-123">In some cases, a property can be retrieved through the [**IUIFramework::GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) method and set with the [**IUIFramework::SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) method.</span></span>

 

<span data-ttu-id="9fcd0-124">下表列出與功能表群組控制項相關聯的屬性索引鍵。</span><span class="sxs-lookup"><span data-stu-id="9fcd0-124">The following table lists the property keys that are associated with the Menu Group control.</span></span>



| <span data-ttu-id="9fcd0-125">屬性索引鍵</span><span class="sxs-lookup"><span data-stu-id="9fcd0-125">Property Key</span></span>                                                                                     | <span data-ttu-id="9fcd0-126">備註</span><span class="sxs-lookup"><span data-stu-id="9fcd0-126">Notes</span></span>                                                                                                                                                                                                                         |
|--------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9fcd0-127">UI \_ PKEY \_ 已啟用</span><span class="sxs-lookup"><span data-stu-id="9fcd0-127">UI\_PKEY\_Enabled</span></span>](windowsribbon-reference-properties-uipkey-enabled.md)                       | <span data-ttu-id="9fcd0-128">支援 [**IUIFramework：： GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) 和 [**IUIFramework：： SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty)。</span><span class="sxs-lookup"><span data-stu-id="9fcd0-128">Supports [**IUIFramework::GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) and [**IUIFramework::SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty).</span></span> |
| [<span data-ttu-id="9fcd0-129">UI \_ PKEY \_ 按鍵提示</span><span class="sxs-lookup"><span data-stu-id="9fcd0-129">UI\_PKEY\_Keytip</span></span>](windowsribbon-reference-properties-uipkey-keytip.md)                         | <span data-ttu-id="9fcd0-130">只能透過失效進行更新。</span><span class="sxs-lookup"><span data-stu-id="9fcd0-130">Can only be updated through invalidation.</span></span>                                                                                                                                                                                     |
| [<span data-ttu-id="9fcd0-131">UI \_ PKEY \_ 標籤</span><span class="sxs-lookup"><span data-stu-id="9fcd0-131">UI\_PKEY\_Label</span></span>](windowsribbon-reference-properties-uipkey-label.md)                           | <span data-ttu-id="9fcd0-132">只能透過失效進行更新。</span><span class="sxs-lookup"><span data-stu-id="9fcd0-132">Can only be updated through invalidation.</span></span>                                                                                                                                                                                     |
| [<span data-ttu-id="9fcd0-133">UI \_ PKEY \_ TooltipDescription</span><span class="sxs-lookup"><span data-stu-id="9fcd0-133">UI\_PKEY\_TooltipDescription</span></span>](windowsribbon-reference-properties-uipkey-tooltipdescription.md) | <span data-ttu-id="9fcd0-134">只能透過失效進行更新。</span><span class="sxs-lookup"><span data-stu-id="9fcd0-134">Can only be updated through invalidation.</span></span>                                                                                                                                                                                     |
| [<span data-ttu-id="9fcd0-135">UI \_ PKEY \_ TooltipTitle</span><span class="sxs-lookup"><span data-stu-id="9fcd0-135">UI\_PKEY\_TooltipTitle</span></span>](windowsribbon-reference-properties-uipkey-tooltiptitle.md)             | <span data-ttu-id="9fcd0-136">只能透過失效進行更新。</span><span class="sxs-lookup"><span data-stu-id="9fcd0-136">Can only be updated through invalidation.</span></span>                                                                                                                                                                                     |



 

## <a name="related-topics"></a><span data-ttu-id="9fcd0-137">相關主題</span><span class="sxs-lookup"><span data-stu-id="9fcd0-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9fcd0-138">Windows 功能區架構控制項程式庫</span><span class="sxs-lookup"><span data-stu-id="9fcd0-138">Windows Ribbon Framework Control Library</span></span>](windowsribbon-controls-entry.md)
</dt> <dt>

[<span data-ttu-id="9fcd0-139">**MenuGroup 標記元素**</span><span class="sxs-lookup"><span data-stu-id="9fcd0-139">**MenuGroup markup element**</span></span>](windowsribbon-element-menugroup.md)
</dt> </dl>

 

 