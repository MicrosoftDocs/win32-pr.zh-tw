---
title: CoNtextPopup. MiniToolbars 屬性
description: 代表浮動工具列元素的容器。
ms.assetid: 5c17e070-0520-44e6-a066-476107691205
keywords:
- CoNtextPopup. MiniToolbars 屬性 Windows 功能區
topic_type:
- apiref
api_name:
- ContextPopup.MiniToolbars
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ee1e85e6b170b4b7408a17687bd26725e9183161
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466569"
---
# <a name="contextpopupminitoolbars-property"></a><span data-ttu-id="559e5-104">CoNtextPopup. MiniToolbars 屬性</span><span class="sxs-lookup"><span data-stu-id="559e5-104">ContextPopup.MiniToolbars property</span></span>

<span data-ttu-id="559e5-105">代表 [**浮動工具列**](windowsribbon-element-minitoolbar.md) 元素的容器。</span><span class="sxs-lookup"><span data-stu-id="559e5-105">Represents a container for [**MiniToolbar**](windowsribbon-element-minitoolbar.md) elements.</span></span>

## <a name="usage"></a><span data-ttu-id="559e5-106">使用方式</span><span class="sxs-lookup"><span data-stu-id="559e5-106">Usage</span></span>

``` syntax
<ContextPopup.MiniToolbars>
  child elements
</ContextPopup.MiniToolbars>
```

## <a name="attributes"></a><span data-ttu-id="559e5-107">屬性</span><span class="sxs-lookup"><span data-stu-id="559e5-107">Attributes</span></span>

<span data-ttu-id="559e5-108">沒有任何屬性。</span><span class="sxs-lookup"><span data-stu-id="559e5-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="559e5-109">子元素</span><span class="sxs-lookup"><span data-stu-id="559e5-109">Child elements</span></span>



| <span data-ttu-id="559e5-110">元素</span><span class="sxs-lookup"><span data-stu-id="559e5-110">Element</span></span>                                                             | <span data-ttu-id="559e5-111">描述</span><span class="sxs-lookup"><span data-stu-id="559e5-111">Description</span></span>                                        |
|---------------------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="559e5-112">**浮動工具列**</span><span class="sxs-lookup"><span data-stu-id="559e5-112">**MiniToolbar**</span></span>](windowsribbon-element-minitoolbar.md)<br/> | <span data-ttu-id="559e5-113">可能會發生一次或多次</span><span class="sxs-lookup"><span data-stu-id="559e5-113">May occur one or more times</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="559e5-114">父元素</span><span class="sxs-lookup"><span data-stu-id="559e5-114">Parent elements</span></span>



| <span data-ttu-id="559e5-115">元素</span><span class="sxs-lookup"><span data-stu-id="559e5-115">Element</span></span>                                                               |
|-----------------------------------------------------------------------|
| [<span data-ttu-id="559e5-116">**CoNtextPopup**</span><span class="sxs-lookup"><span data-stu-id="559e5-116">**ContextPopup**</span></span>](windowsribbon-element-contextpopup.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="559e5-117">備註</span><span class="sxs-lookup"><span data-stu-id="559e5-117">Remarks</span></span>

<span data-ttu-id="559e5-118">選擇性。</span><span class="sxs-lookup"><span data-stu-id="559e5-118">Optional.</span></span>

<span data-ttu-id="559e5-119">每個 [**CoNtextPopup**](windowsribbon-element-contextpopup.md)最多可能會發生一次。</span><span class="sxs-lookup"><span data-stu-id="559e5-119">May occur at most once for each [**ContextPopup**](windowsribbon-element-contextpopup.md).</span></span>

<span data-ttu-id="559e5-120">因為 [**浮動工具列**](windowsribbon-element-minitoolbar.md) 中的控制項無法存取鍵盤，所以它們所公開的命令應該可在功能區 UI 中的其他位置使用。</span><span class="sxs-lookup"><span data-stu-id="559e5-120">Because controls in the [**MiniToolbar**](windowsribbon-element-minitoolbar.md) are not keyboard accessible, the Commands they expose should be available elsewhere in the Ribbon UI.</span></span>

## <a name="examples"></a><span data-ttu-id="559e5-121">範例</span><span class="sxs-lookup"><span data-stu-id="559e5-121">Examples</span></span>

<span data-ttu-id="559e5-122">下列範例示範 [**CoNtextPopup**](windowsribbon-element-contextpopup.md) View 的基本標記。</span><span class="sxs-lookup"><span data-stu-id="559e5-122">The following example demonstrates the basic markup for a [**ContextPopup**](windowsribbon-element-contextpopup.md) View.</span></span>

<span data-ttu-id="559e5-123">這段程式碼會顯示 **CoNtextPopup MiniToolbars** 控制項宣告。</span><span class="sxs-lookup"><span data-stu-id="559e5-123">This section of code shows the **ContextPopup.MiniToolbars** control declaration.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="559e5-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="559e5-124">Requirements</span></span>



| <span data-ttu-id="559e5-125">需求</span><span class="sxs-lookup"><span data-stu-id="559e5-125">Requirement</span></span> | <span data-ttu-id="559e5-126">值</span><span class="sxs-lookup"><span data-stu-id="559e5-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="559e5-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="559e5-127">Minimum supported client</span></span><br/> | <span data-ttu-id="559e5-128">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="559e5-128">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="559e5-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="559e5-129">Minimum supported server</span></span><br/> | <span data-ttu-id="559e5-130">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="559e5-130">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="559e5-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="559e5-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="559e5-132">CoNtext Popup 控制項</span><span class="sxs-lookup"><span data-stu-id="559e5-132">Context Popup control</span></span>](windowsribbon-controls-contextpopup.md)
</dt> </dl>

 

 





