---
title: 浮動工具列元素
description: 表示內容相關的工具列。
ms.assetid: bb50890d-554a-4add-a583-d4fd48b823bf
keywords:
- 浮動工具列元素視窗功能區
topic_type:
- apiref
api_name:
- MiniToolbar
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: cb5e4a27d10fe5233f8e7059bc9da8ecfd2fa383
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "104092333"
---
# <a name="minitoolbar-element"></a><span data-ttu-id="4b959-104">浮動工具列元素</span><span class="sxs-lookup"><span data-stu-id="4b959-104">MiniToolbar element</span></span>

<span data-ttu-id="4b959-105">表示內容相關的工具列。</span><span class="sxs-lookup"><span data-stu-id="4b959-105">Represents a contextual toolbar.</span></span>

## <a name="usage"></a><span data-ttu-id="4b959-106">使用方式</span><span class="sxs-lookup"><span data-stu-id="4b959-106">Usage</span></span>

``` syntax
<MiniToolbar
  Name = "xs:string">
  child elements
</MiniToolbar>
```

## <a name="attributes"></a><span data-ttu-id="4b959-107">屬性</span><span class="sxs-lookup"><span data-stu-id="4b959-107">Attributes</span></span>



| <span data-ttu-id="4b959-108">屬性</span><span class="sxs-lookup"><span data-stu-id="4b959-108">Attribute</span></span>           | <span data-ttu-id="4b959-109">類型</span><span class="sxs-lookup"><span data-stu-id="4b959-109">Type</span></span>                 | <span data-ttu-id="4b959-110">必要</span><span class="sxs-lookup"><span data-stu-id="4b959-110">Required</span></span>       | <span data-ttu-id="4b959-111">描述</span><span class="sxs-lookup"><span data-stu-id="4b959-111">Description</span></span>                                                                                                                                                                                                                |
|---------------------|----------------------|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4b959-112">**名稱**</span><span class="sxs-lookup"><span data-stu-id="4b959-112">**Name**</span></span><br/> | <span data-ttu-id="4b959-113">xs:string</span><span class="sxs-lookup"><span data-stu-id="4b959-113">xs:string</span></span><br/> | <span data-ttu-id="4b959-114">Yes</span><span class="sxs-lookup"><span data-stu-id="4b959-114">Yes</span></span><br/> | <span data-ttu-id="4b959-115"><dt> (xs： string) </span><span class="sxs-lookup"><span data-stu-id="4b959-115"><dt> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="4b959-116">由任何字元序列組成的字串，包括空白字元和分行符號字元。</span><span class="sxs-lookup"><span data-stu-id="4b959-116">A string composed of any sequence of characters, including white space and line-break characters.</span></span><br/> </dd> </dl> |



## <a name="child-elements"></a><span data-ttu-id="4b959-117">子元素</span><span class="sxs-lookup"><span data-stu-id="4b959-117">Child elements</span></span>



| <span data-ttu-id="4b959-118">元素</span><span class="sxs-lookup"><span data-stu-id="4b959-118">Element</span></span>                                                         | <span data-ttu-id="4b959-119">描述</span><span class="sxs-lookup"><span data-stu-id="4b959-119">Description</span></span>                                     |
|-----------------------------------------------------------------|-------------------------------------------------|
| [<span data-ttu-id="4b959-120">**MenuGroup**</span><span class="sxs-lookup"><span data-stu-id="4b959-120">**MenuGroup**</span></span>](windowsribbon-element-menugroup.md)<br/> | <span data-ttu-id="4b959-121">至少必須發生一次</span><span class="sxs-lookup"><span data-stu-id="4b959-121">Must occur at least once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="4b959-122">父元素</span><span class="sxs-lookup"><span data-stu-id="4b959-122">Parent elements</span></span>



| <span data-ttu-id="4b959-123">元素</span><span class="sxs-lookup"><span data-stu-id="4b959-123">Element</span></span>                                                                                         |
|-------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4b959-124">**CoNtextPopup.MiniToolbars**</span><span class="sxs-lookup"><span data-stu-id="4b959-124">**ContextPopup.MiniToolbars**</span></span>](windowsribbon-element-contextpopup-minitoolbars.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="4b959-125">備註</span><span class="sxs-lookup"><span data-stu-id="4b959-125">Remarks</span></span>

<span data-ttu-id="4b959-126">選擇性。</span><span class="sxs-lookup"><span data-stu-id="4b959-126">Optional.</span></span>

<span data-ttu-id="4b959-127">每個 [**CoNtextPopup MiniToolbars**](windowsribbon-element-contextpopup-minitoolbars.md)可能會發生一次或多次。</span><span class="sxs-lookup"><span data-stu-id="4b959-127">May occur one or more times for each [**ContextPopup.MiniToolbars**](windowsribbon-element-contextpopup-minitoolbars.md).</span></span>

<span data-ttu-id="4b959-128">與 [**CoNtextMenu**](windowsribbon-element-contextmenu.md) 元素不同，按一下工具列上的專案時， **浮動工具列** 會保持可見。</span><span class="sxs-lookup"><span data-stu-id="4b959-128">Unlike the [**ContextMenu**](windowsribbon-element-contextmenu.md) element, the **MiniToolbar** remains visible when an item on the toolbar is clicked.</span></span>

<span data-ttu-id="4b959-129">如果在沒有 [**CoNtextMenu**](windowsribbon-element-contextmenu.md)的情況下顯示，當滑鼠指標移開時， **浮動工具列** 就會淡出。</span><span class="sxs-lookup"><span data-stu-id="4b959-129">If displayed without a [**ContextMenu**](windowsribbon-element-contextmenu.md), the **MiniToolbar** fades as the mouse pointer is moved away.</span></span>

> [!Note]  
> <span data-ttu-id="4b959-130">由於這種淡化行為的緣故， [**CoNtextMenu**](windowsribbon-element-contextmenu.md) 應該會顯示在靠近滑鼠指標的附近。</span><span class="sxs-lookup"><span data-stu-id="4b959-130">Due to this fading behavior, a [**ContextMenu**](windowsribbon-element-contextmenu.md) should be displayed in close proximity to the mouse pointer.</span></span>

 

<span data-ttu-id="4b959-131">因為 **浮動工具列** 中的控制項無法存取鍵盤，所以它們所公開的命令應該可在功能區 UI 中的其他位置使用。</span><span class="sxs-lookup"><span data-stu-id="4b959-131">Because controls in the **MiniToolbar** are not keyboard accessible, the Commands they expose should be available elsewhere in the Ribbon UI.</span></span>

## <a name="examples"></a><span data-ttu-id="4b959-132">範例</span><span class="sxs-lookup"><span data-stu-id="4b959-132">Examples</span></span>

<span data-ttu-id="4b959-133">下列範例示範 [**CoNtextPopup**](windowsribbon-element-contextpopup.md) View 的基本標記。</span><span class="sxs-lookup"><span data-stu-id="4b959-133">The following example demonstrates the basic markup for a [**ContextPopup**](windowsribbon-element-contextpopup.md) View.</span></span>

<span data-ttu-id="4b959-134">這段程式碼會顯示一組 **浮動工具列** 控制項宣告。</span><span class="sxs-lookup"><span data-stu-id="4b959-134">This section of code shows a set of **MiniToolbar** control declarations.</span></span>


```XML
    <ContextPopup>
      <!--
        The MiniToolbars and Context Menus are the basic ingredients for 
        the contextual UI popup. 
        Mix-and-match and associate each combination with a ContextMap Command 
        invoked in code.
      -->
      <ContextPopup.MiniToolbars>
        <MiniToolbar Name="MiniToolbar1">
          <MenuGroup Class="MajorItems">
            <Button CommandName="cmdCut" />
            <Button CommandName="cmdCopy" />
            <Button CommandName="cmdPaste" />
          </MenuGroup>
          <MenuGroup>
            <ToggleButton CommandName="cmdToggleButton" />
            <DropDownButton CommandName="cmdButtons">
              <MenuGroup>
                <Button CommandName="cmdButton1" />
                <Button CommandName="cmdButton2" />
                <Button CommandName="cmdButton3" />
              </MenuGroup>
            </DropDownButton>
          </MenuGroup>
        </MiniToolbar>
        <MiniToolbar Name="MiniToolbar2">
          <MenuGroup>
            <Button CommandName="cmdButton1" />
            <Button CommandName="cmdButton2" />
            <Button CommandName="cmdButton3" />
          </MenuGroup>
        </MiniToolbar>
      </ContextPopup.MiniToolbars>
      <ContextPopup.ContextMenus>
        <ContextMenu Name="ContextMenu1">
          <MenuGroup>
            <Button CommandName="cmdCut" />
            <Button CommandName="cmdCopy" />
            <Button CommandName="cmdPaste" />
          </MenuGroup>
        </ContextMenu>
        <ContextMenu Name="ContextMenu2">
          <MenuGroup>
            <ToggleButton CommandName="cmdToggleButton" />
          </MenuGroup>
          <MenuGroup>
            <Button CommandName="cmdButton1" />
            <Button CommandName="cmdButton2" />
            <Button CommandName="cmdButton3" />
          </MenuGroup>
        </ContextMenu>
        <ContextMenu Name="ContextMenu4">
          <MenuGroup>
            <Button CommandName="cmdCut" />
            <Button CommandName="cmdCopy" />
            <Button CommandName="cmdPaste" />
          </MenuGroup>
          <MenuGroup>
            <ToggleButton CommandName="cmdToggleButton" />
          </MenuGroup>
          <MenuGroup>
            <Button CommandName="cmdButton1" />
            <Button CommandName="cmdButton2" />
            <Button CommandName="cmdButton3" />
          </MenuGroup>
        </ContextMenu>
      </ContextPopup.ContextMenus>
      <ContextPopup.ContextMaps>
        <ContextMap CommandName="cmdContextMap1"
                    ContextMenu="ContextMenu1"/>
        <ContextMap CommandName="cmdContextMap2"
                    ContextMenu="ContextMenu2"
                    MiniToolbar="MiniToolbar1"/>
        <ContextMap CommandName="cmdContextMap3"
                    MiniToolbar="MiniToolbar2"/>
        <ContextMap CommandName="cmdContextMap4"
                    ContextMenu="ContextMenu4"/>
      </ContextPopup.ContextMaps>
    </ContextPopup>
```



## <a name="element-information"></a><span data-ttu-id="4b959-135">項目資訊</span><span class="sxs-lookup"><span data-stu-id="4b959-135">Element information</span></span>



|                                     |           |
|-------------------------------------|-----------|
| <span data-ttu-id="4b959-136">最低支援系統</span><span class="sxs-lookup"><span data-stu-id="4b959-136">Minimum supported system</span></span><br/> | <span data-ttu-id="4b959-137">Windows 7</span><span class="sxs-lookup"><span data-stu-id="4b959-137">Windows 7</span></span> |
| <span data-ttu-id="4b959-138">可以是空的</span><span class="sxs-lookup"><span data-stu-id="4b959-138">Can be empty</span></span>                        | <span data-ttu-id="4b959-139">否</span><span class="sxs-lookup"><span data-stu-id="4b959-139">No</span></span>        |



## <a name="see-also"></a><span data-ttu-id="4b959-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4b959-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4b959-141">CoNtext Popup 控制項</span><span class="sxs-lookup"><span data-stu-id="4b959-141">Context Popup control</span></span>](windowsribbon-controls-contextpopup.md)
</dt> </dl>

 

 





