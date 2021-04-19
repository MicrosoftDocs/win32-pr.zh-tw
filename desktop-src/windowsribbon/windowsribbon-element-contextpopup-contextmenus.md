---
title: CoNtextPopup. CoNtextmenu 屬性
description: 代表 CoNtextMenu 元素的容器。
ms.assetid: 92633689-a892-421e-a5fb-e494f4cd1ea8
keywords:
- CoNtextPopup. CoNtextmenu 屬性 Windows 功能區
topic_type:
- apiref
api_name:
- ContextPopup.ContextMenus
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 12ef8ab053b9912f545c2aad931eb8ad9583ff62
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106967754"
---
# <a name="contextpopupcontextmenus-property"></a><span data-ttu-id="36b53-104">CoNtextPopup. CoNtextmenu 屬性</span><span class="sxs-lookup"><span data-stu-id="36b53-104">ContextPopup.ContextMenus property</span></span>

<span data-ttu-id="36b53-105">代表 [**CoNtextMenu**](windowsribbon-element-contextmenu.md) 元素的容器。</span><span class="sxs-lookup"><span data-stu-id="36b53-105">Represents a container for [**ContextMenu**](windowsribbon-element-contextmenu.md) elements.</span></span>

## <a name="usage"></a><span data-ttu-id="36b53-106">使用方式</span><span class="sxs-lookup"><span data-stu-id="36b53-106">Usage</span></span>

``` syntax
<ContextPopup.ContextMenus>
  child elements
</ContextPopup.ContextMenus>
```

## <a name="attributes"></a><span data-ttu-id="36b53-107">屬性</span><span class="sxs-lookup"><span data-stu-id="36b53-107">Attributes</span></span>

<span data-ttu-id="36b53-108">沒有任何屬性。</span><span class="sxs-lookup"><span data-stu-id="36b53-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="36b53-109">子元素</span><span class="sxs-lookup"><span data-stu-id="36b53-109">Child elements</span></span>



| <span data-ttu-id="36b53-110">元素</span><span class="sxs-lookup"><span data-stu-id="36b53-110">Element</span></span>                                                             | <span data-ttu-id="36b53-111">描述</span><span class="sxs-lookup"><span data-stu-id="36b53-111">Description</span></span>                                        |
|---------------------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="36b53-112">**ContextMenu**</span><span class="sxs-lookup"><span data-stu-id="36b53-112">**ContextMenu**</span></span>](windowsribbon-element-contextmenu.md)<br/> | <span data-ttu-id="36b53-113">可能會發生一次或多次</span><span class="sxs-lookup"><span data-stu-id="36b53-113">May occur one or more times</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="36b53-114">父元素</span><span class="sxs-lookup"><span data-stu-id="36b53-114">Parent elements</span></span>



| <span data-ttu-id="36b53-115">元素</span><span class="sxs-lookup"><span data-stu-id="36b53-115">Element</span></span>                                                               |
|-----------------------------------------------------------------------|
| [<span data-ttu-id="36b53-116">**CoNtextPopup**</span><span class="sxs-lookup"><span data-stu-id="36b53-116">**ContextPopup**</span></span>](windowsribbon-element-contextpopup.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="36b53-117">備註</span><span class="sxs-lookup"><span data-stu-id="36b53-117">Remarks</span></span>

<span data-ttu-id="36b53-118">選擇性。</span><span class="sxs-lookup"><span data-stu-id="36b53-118">Optional.</span></span>

<span data-ttu-id="36b53-119">每個 [**CoNtextPopup**](windowsribbon-element-contextpopup.md)最多可能會發生一次。</span><span class="sxs-lookup"><span data-stu-id="36b53-119">May occur at most once for each [**ContextPopup**](windowsribbon-element-contextpopup.md).</span></span>

## <a name="examples"></a><span data-ttu-id="36b53-120">範例</span><span class="sxs-lookup"><span data-stu-id="36b53-120">Examples</span></span>

<span data-ttu-id="36b53-121">下列範例示範 [**CoNtextPopup**](windowsribbon-element-contextpopup.md) View 的基本標記。</span><span class="sxs-lookup"><span data-stu-id="36b53-121">The following example demonstrates the basic markup for a [**ContextPopup**](windowsribbon-element-contextpopup.md) View.</span></span>

<span data-ttu-id="36b53-122">這一節的程式碼顯示 **CoNtextPopup coNtextmenu** 控制項宣告。</span><span class="sxs-lookup"><span data-stu-id="36b53-122">This section of code shows a **ContextPopup.ContextMenus** control declaration.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="36b53-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="36b53-123">Requirements</span></span>



| <span data-ttu-id="36b53-124">需求</span><span class="sxs-lookup"><span data-stu-id="36b53-124">Requirement</span></span> | <span data-ttu-id="36b53-125">值</span><span class="sxs-lookup"><span data-stu-id="36b53-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="36b53-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="36b53-126">Minimum supported client</span></span><br/> | <span data-ttu-id="36b53-127">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="36b53-127">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="36b53-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="36b53-128">Minimum supported server</span></span><br/> | <span data-ttu-id="36b53-129">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="36b53-129">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="36b53-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="36b53-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="36b53-131">CoNtext Popup 控制項</span><span class="sxs-lookup"><span data-stu-id="36b53-131">Context Popup control</span></span>](windowsribbon-controls-contextpopup.md)
</dt> </dl>

 

 





