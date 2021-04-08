---
title: CoNtextPopup 元素
description: 表示 CoNtextPopup View 中的內容快顯視窗控制項。
ms.assetid: b955be16-803e-47b5-a72d-f993180fbf14
keywords:
- CoNtextPopup 元素視窗功能區
topic_type:
- apiref
api_name:
- ContextPopup
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4feb7c4fbd2ca538fe4d0c2b2584163ee8c9fcea
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "104022520"
---
# <a name="contextpopup-element"></a><span data-ttu-id="08ad2-104">CoNtextPopup 元素</span><span class="sxs-lookup"><span data-stu-id="08ad2-104">ContextPopup element</span></span>

<span data-ttu-id="08ad2-105">表示 CoNtextPopup View 中的 [內容快顯視窗](windowsribbon-controls-contextpopup.md) 控制項。</span><span class="sxs-lookup"><span data-stu-id="08ad2-105">Represents the [Context Popup](windowsribbon-controls-contextpopup.md) control in the ContextPopup View.</span></span>

## <a name="usage"></a><span data-ttu-id="08ad2-106">使用方式</span><span class="sxs-lookup"><span data-stu-id="08ad2-106">Usage</span></span>

``` syntax
<ContextPopup>
  child elements
</ContextPopup>
```

## <a name="attributes"></a><span data-ttu-id="08ad2-107">屬性</span><span class="sxs-lookup"><span data-stu-id="08ad2-107">Attributes</span></span>

<span data-ttu-id="08ad2-108">沒有任何屬性。</span><span class="sxs-lookup"><span data-stu-id="08ad2-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="08ad2-109">子元素</span><span class="sxs-lookup"><span data-stu-id="08ad2-109">Child elements</span></span>



| <span data-ttu-id="08ad2-110">元素</span><span class="sxs-lookup"><span data-stu-id="08ad2-110">Element</span></span>                                                                                         | <span data-ttu-id="08ad2-111">描述</span><span class="sxs-lookup"><span data-stu-id="08ad2-111">Description</span></span>                                   |
|-------------------------------------------------------------------------------------------------|-----------------------------------------------|
| [<span data-ttu-id="08ad2-112">**CoNtextPopup.CoNtextMaps**</span><span class="sxs-lookup"><span data-stu-id="08ad2-112">**ContextPopup.ContextMaps**</span></span>](windowsribbon-element-contextpopup-contextmaps.md)<br/>   | <span data-ttu-id="08ad2-113">最多可能發生一次</span><span class="sxs-lookup"><span data-stu-id="08ad2-113">May occur at most once</span></span><br/> <br/> |
| [<span data-ttu-id="08ad2-114">**CoNtextPopup. CoNtextmenu**</span><span class="sxs-lookup"><span data-stu-id="08ad2-114">**ContextPopup.ContextMenus**</span></span>](windowsribbon-element-contextpopup-contextmenus.md)<br/> | <span data-ttu-id="08ad2-115">最多可能發生一次</span><span class="sxs-lookup"><span data-stu-id="08ad2-115">May occur at most once</span></span><br/> <br/> |
| [<span data-ttu-id="08ad2-116">**CoNtextPopup.MiniToolbars**</span><span class="sxs-lookup"><span data-stu-id="08ad2-116">**ContextPopup.MiniToolbars**</span></span>](windowsribbon-element-contextpopup-minitoolbars.md)<br/> | <span data-ttu-id="08ad2-117">最多可能發生一次</span><span class="sxs-lookup"><span data-stu-id="08ad2-117">May occur at most once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="08ad2-118">父元素</span><span class="sxs-lookup"><span data-stu-id="08ad2-118">Parent elements</span></span>



| <span data-ttu-id="08ad2-119">元素</span><span class="sxs-lookup"><span data-stu-id="08ad2-119">Element</span></span>                                                                         |
|---------------------------------------------------------------------------------|
| [<span data-ttu-id="08ad2-120">**應用程式。 Views**</span><span class="sxs-lookup"><span data-stu-id="08ad2-120">**Application.Views**</span></span>](windowsribbon-element-application-views.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="08ad2-121">備註</span><span class="sxs-lookup"><span data-stu-id="08ad2-121">Remarks</span></span>

<span data-ttu-id="08ad2-122">選擇性。</span><span class="sxs-lookup"><span data-stu-id="08ad2-122">Optional.</span></span>

<span data-ttu-id="08ad2-123">每個 [**應用程式**](windowsribbon-element-application-views.md)最多可能會發生一次。</span><span class="sxs-lookup"><span data-stu-id="08ad2-123">May occur at most once for each [**Application.Views**](windowsribbon-element-application-views.md).</span></span>

## <a name="examples"></a><span data-ttu-id="08ad2-124">範例</span><span class="sxs-lookup"><span data-stu-id="08ad2-124">Examples</span></span>

<span data-ttu-id="08ad2-125">下列範例示範 **CoNtextPopup** View 的基本標記。</span><span class="sxs-lookup"><span data-stu-id="08ad2-125">The following example demonstrates the basic markup for a **ContextPopup** View.</span></span>


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



## <a name="element-information"></a><span data-ttu-id="08ad2-126">項目資訊</span><span class="sxs-lookup"><span data-stu-id="08ad2-126">Element information</span></span>



|                                     |           |
|-------------------------------------|-----------|
| <span data-ttu-id="08ad2-127">最低支援系統</span><span class="sxs-lookup"><span data-stu-id="08ad2-127">Minimum supported system</span></span><br/> | <span data-ttu-id="08ad2-128">Windows 7</span><span class="sxs-lookup"><span data-stu-id="08ad2-128">Windows 7</span></span> |
| <span data-ttu-id="08ad2-129">可以是空的</span><span class="sxs-lookup"><span data-stu-id="08ad2-129">Can be empty</span></span>                        | <span data-ttu-id="08ad2-130">否</span><span class="sxs-lookup"><span data-stu-id="08ad2-130">No</span></span>        |



## <a name="see-also"></a><span data-ttu-id="08ad2-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="08ad2-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="08ad2-132">CoNtext Popup 控制項</span><span class="sxs-lookup"><span data-stu-id="08ad2-132">Context Popup control</span></span>](windowsribbon-controls-contextpopup.md)
</dt> </dl>

 

 





