---
title: CoNtextMenu 元素
description: 表示內容功能表控制項。
ms.assetid: 08cc0514-0795-4e6b-b80c-33d920783032
keywords:
- CoNtextMenu 元素視窗功能區
topic_type:
- apiref
api_name:
- ContextMenu
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c824e87c063fb863e79f10cb9755b74df36023f7
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "103678452"
---
# <a name="contextmenu-element"></a><span data-ttu-id="ec6b8-104">CoNtextMenu 元素</span><span class="sxs-lookup"><span data-stu-id="ec6b8-104">ContextMenu element</span></span>

<span data-ttu-id="ec6b8-105">表示內容功能表控制項。</span><span class="sxs-lookup"><span data-stu-id="ec6b8-105">Represents a context menu control.</span></span>

## <a name="usage"></a><span data-ttu-id="ec6b8-106">使用方式</span><span class="sxs-lookup"><span data-stu-id="ec6b8-106">Usage</span></span>

``` syntax
<ContextMenu
  Name = "xs:string">
  child elements
</ContextMenu>
```

## <a name="attributes"></a><span data-ttu-id="ec6b8-107">屬性</span><span class="sxs-lookup"><span data-stu-id="ec6b8-107">Attributes</span></span>



| <span data-ttu-id="ec6b8-108">屬性</span><span class="sxs-lookup"><span data-stu-id="ec6b8-108">Attribute</span></span>           | <span data-ttu-id="ec6b8-109">類型</span><span class="sxs-lookup"><span data-stu-id="ec6b8-109">Type</span></span>                 | <span data-ttu-id="ec6b8-110">必要</span><span class="sxs-lookup"><span data-stu-id="ec6b8-110">Required</span></span>       | <span data-ttu-id="ec6b8-111">描述</span><span class="sxs-lookup"><span data-stu-id="ec6b8-111">Description</span></span>                                                                                                                                                                                                                |
|---------------------|----------------------|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ec6b8-112">**名稱**</span><span class="sxs-lookup"><span data-stu-id="ec6b8-112">**Name**</span></span><br/> | <span data-ttu-id="ec6b8-113">xs:string</span><span class="sxs-lookup"><span data-stu-id="ec6b8-113">xs:string</span></span><br/> | <span data-ttu-id="ec6b8-114">Yes</span><span class="sxs-lookup"><span data-stu-id="ec6b8-114">Yes</span></span><br/> | <span data-ttu-id="ec6b8-115"><dt> (xs： string) </span><span class="sxs-lookup"><span data-stu-id="ec6b8-115"><dt> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="ec6b8-116">由任何字元序列組成的字串，包括空白字元和分行符號字元。</span><span class="sxs-lookup"><span data-stu-id="ec6b8-116">A string composed of any sequence of characters, including white space and line-break characters.</span></span><br/> </dd> </dl> |



## <a name="child-elements"></a><span data-ttu-id="ec6b8-117">子元素</span><span class="sxs-lookup"><span data-stu-id="ec6b8-117">Child elements</span></span>



| <span data-ttu-id="ec6b8-118">元素</span><span class="sxs-lookup"><span data-stu-id="ec6b8-118">Element</span></span>                                                         | <span data-ttu-id="ec6b8-119">描述</span><span class="sxs-lookup"><span data-stu-id="ec6b8-119">Description</span></span>                                     |
|-----------------------------------------------------------------|-------------------------------------------------|
| [<span data-ttu-id="ec6b8-120">**MenuGroup**</span><span class="sxs-lookup"><span data-stu-id="ec6b8-120">**MenuGroup**</span></span>](windowsribbon-element-menugroup.md)<br/> | <span data-ttu-id="ec6b8-121">至少必須發生一次</span><span class="sxs-lookup"><span data-stu-id="ec6b8-121">Must occur at least once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="ec6b8-122">父元素</span><span class="sxs-lookup"><span data-stu-id="ec6b8-122">Parent elements</span></span>



| <span data-ttu-id="ec6b8-123">元素</span><span class="sxs-lookup"><span data-stu-id="ec6b8-123">Element</span></span>                                                                                         |
|-------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ec6b8-124">**CoNtextPopup. CoNtextmenu**</span><span class="sxs-lookup"><span data-stu-id="ec6b8-124">**ContextPopup.ContextMenus**</span></span>](windowsribbon-element-contextpopup-contextmenus.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="ec6b8-125">備註</span><span class="sxs-lookup"><span data-stu-id="ec6b8-125">Remarks</span></span>

<span data-ttu-id="ec6b8-126">選擇性。</span><span class="sxs-lookup"><span data-stu-id="ec6b8-126">Optional.</span></span>

<span data-ttu-id="ec6b8-127">每個 [**CoNtextPopup coNtextmenu**](windowsribbon-element-contextpopup-contextmenus.md)可能會發生一次或多次。</span><span class="sxs-lookup"><span data-stu-id="ec6b8-127">May occur one or more times for each [**ContextPopup.ContextMenus**](windowsribbon-element-contextpopup-contextmenus.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ec6b8-128">**CoNtextMenu** 無法裝載 [下拉式](windowsribbon-controls-combobox.md)方塊或 [微調](windowsribbon-controls-spinner.md)控制項。</span><span class="sxs-lookup"><span data-stu-id="ec6b8-128">A **ContextMenu** cannot host [Combo Box](windowsribbon-controls-combobox.md) or [Spinner](windowsribbon-controls-spinner.md) controls.</span></span>

 

## <a name="examples"></a><span data-ttu-id="ec6b8-129">範例</span><span class="sxs-lookup"><span data-stu-id="ec6b8-129">Examples</span></span>

<span data-ttu-id="ec6b8-130">下列範例示範 [**CoNtextPopup**](windowsribbon-element-contextpopup.md) View 的基本標記。</span><span class="sxs-lookup"><span data-stu-id="ec6b8-130">The following example demonstrates the basic markup for a [**ContextPopup**](windowsribbon-element-contextpopup.md) View.</span></span>

<span data-ttu-id="ec6b8-131">這段程式碼會顯示一組 **CoNtextMenu** 控制項宣告。</span><span class="sxs-lookup"><span data-stu-id="ec6b8-131">This section of code shows a set of **ContextMenu** control declarations.</span></span>


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



## <a name="element-information"></a><span data-ttu-id="ec6b8-132">項目資訊</span><span class="sxs-lookup"><span data-stu-id="ec6b8-132">Element information</span></span>



|                                     |           |
|-------------------------------------|-----------|
| <span data-ttu-id="ec6b8-133">最低支援系統</span><span class="sxs-lookup"><span data-stu-id="ec6b8-133">Minimum supported system</span></span><br/> | <span data-ttu-id="ec6b8-134">Windows 7</span><span class="sxs-lookup"><span data-stu-id="ec6b8-134">Windows 7</span></span> |
| <span data-ttu-id="ec6b8-135">可以是空的</span><span class="sxs-lookup"><span data-stu-id="ec6b8-135">Can be empty</span></span>                        | <span data-ttu-id="ec6b8-136">否</span><span class="sxs-lookup"><span data-stu-id="ec6b8-136">No</span></span>        |



## <a name="see-also"></a><span data-ttu-id="ec6b8-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ec6b8-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ec6b8-138">CoNtext Popup 控制項</span><span class="sxs-lookup"><span data-stu-id="ec6b8-138">Context Popup control</span></span>](windowsribbon-controls-contextpopup.md)
</dt> </dl>

 

 





