---
title: CoNtextMap 元素
description: 表示 CoNtextMenu 和浮動工具列配對對應。
ms.assetid: 84379578-24c6-4bf7-8dcf-8e21e5665d29
keywords:
- CoNtextMap 元素視窗功能區
topic_type:
- apiref
api_name:
- ContextMap
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e2ddcc8bdea16f5e00974b2b2e58934941e44c68
ms.sourcegitcommit: 927b9c371f75f52b8011483edf3a4ba37d11ebe4
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/11/2020
ms.locfileid: "106967656"
---
# <a name="contextmap-element"></a><span data-ttu-id="32147-104">CoNtextMap 元素</span><span class="sxs-lookup"><span data-stu-id="32147-104">ContextMap element</span></span>

<span data-ttu-id="32147-105">表示 [**CoNtextMenu**](windowsribbon-element-contextmenu.md) 和 [**浮動工具列**](windowsribbon-element-minitoolbar.md) 配對對應。</span><span class="sxs-lookup"><span data-stu-id="32147-105">Represents a [**ContextMenu**](windowsribbon-element-contextmenu.md) and [**MiniToolbar**](windowsribbon-element-minitoolbar.md) pair mapping.</span></span>

## <a name="usage"></a><span data-ttu-id="32147-106">使用方式</span><span class="sxs-lookup"><span data-stu-id="32147-106">Usage</span></span>

``` syntax
<ContextMap
  CommandName = "xs:positiveInteger or xs:string"
  MiniToolbar = "xs:string"
  ContextMenu = "xs:string"/>
```

## <a name="attributes"></a><span data-ttu-id="32147-107">屬性</span><span class="sxs-lookup"><span data-stu-id="32147-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="32147-108">屬性</span><span class="sxs-lookup"><span data-stu-id="32147-108">Attribute</span></span></th>
<th><span data-ttu-id="32147-109">類型</span><span class="sxs-lookup"><span data-stu-id="32147-109">Type</span></span></th>
<th><span data-ttu-id="32147-110">必要</span><span class="sxs-lookup"><span data-stu-id="32147-110">Required</span></span></th>
<th><span data-ttu-id="32147-111">描述</span><span class="sxs-lookup"><span data-stu-id="32147-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="32147-112"><strong>CommandName</strong></span><span class="sxs-lookup"><span data-stu-id="32147-112"><strong>CommandName</strong></span></span><br/></td>
<td><span data-ttu-id="32147-113">xs： positiveInteger 或 xs： string</span><span class="sxs-lookup"><span data-stu-id="32147-113">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="32147-114">No</span><span class="sxs-lookup"><span data-stu-id="32147-114">No</span></span><br/></td>
<td><span data-ttu-id="32147-115">將元素與 <a href="windowsribbon-element-command.md"><strong>命令</strong></a>產生關聯。</span><span class="sxs-lookup"><span data-stu-id="32147-115">Associates the element with a <a href="windowsribbon-element-command.md"><strong>Command</strong></a>.</span></span><br/> <br/><span data-ttu-id="32147-116">
<dt><span></span><span></span><strong></strong> (xs： positiveInteger 或 xs： string) </span><span class="sxs-lookup"><span data-stu-id="32147-116">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="32147-117">字串、介於2與59999（含）之間的整數值，或介於0x2 與0xea5f （含）之間的十六進位值。</span><span class="sxs-lookup"><span data-stu-id="32147-117">A string, an integer value between 2 and 59999, inclusive, or a hexadecimal value between 0x2 and 0xea5f, inclusive.</span></span> <br/> <span data-ttu-id="32147-118">值在功能區 XML 檔中必須是唯一的。</span><span class="sxs-lookup"><span data-stu-id="32147-118">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="32147-119">最大長度：100個字元。</span><span class="sxs-lookup"><span data-stu-id="32147-119">Maximum length: 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="32147-120"><strong>ContextMenu</strong></span><span class="sxs-lookup"><span data-stu-id="32147-120"><strong>ContextMenu</strong></span></span><br/></td>
<td><span data-ttu-id="32147-121">xs:string</span><span class="sxs-lookup"><span data-stu-id="32147-121">xs:string</span></span><br/></td>
<td><span data-ttu-id="32147-122">No</span><span class="sxs-lookup"><span data-stu-id="32147-122">No</span></span><br/></td>
<td><span data-ttu-id="32147-123">必須對應至現有的 <a href="windowsribbon-element-contextmenu.md"><strong>CoNtextMenu</strong></a> <em>名稱</em>。</span><span class="sxs-lookup"><span data-stu-id="32147-123">Must correspond to an existing <a href="windowsribbon-element-contextmenu.md"><strong>ContextMenu</strong></a> <em>Name</em>.</span></span><br/> <br/><span data-ttu-id="32147-124">
<dt><span></span><span></span><strong></strong> (xs： string) </span><span class="sxs-lookup"><span data-stu-id="32147-124">
<dt><span></span><span></span><strong></strong> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="32147-125">由任何字元序列組成的字串，包括空白字元和分行符號字元。</span><span class="sxs-lookup"><span data-stu-id="32147-125">A string composed of any sequence of characters, including white space and line-break characters.</span></span><br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="32147-126"><strong>浮動工具列</strong></span><span class="sxs-lookup"><span data-stu-id="32147-126"><strong>MiniToolbar</strong></span></span><br/></td>
<td><span data-ttu-id="32147-127">xs:string</span><span class="sxs-lookup"><span data-stu-id="32147-127">xs:string</span></span><br/></td>
<td><span data-ttu-id="32147-128">No</span><span class="sxs-lookup"><span data-stu-id="32147-128">No</span></span><br/></td>
<td><span data-ttu-id="32147-129">必須對應至現有的<a href="windowsribbon-element-minitoolbar.md"><strong>浮動工具列</strong></a><em>名稱</em>。</span><span class="sxs-lookup"><span data-stu-id="32147-129">Must correspond to an existing <a href="windowsribbon-element-minitoolbar.md"><strong>MiniToolbar</strong></a> <em>Name</em>.</span></span><br/> <br/><span data-ttu-id="32147-130">
<dt><span></span><span></span><strong></strong> (xs： string) </span><span class="sxs-lookup"><span data-stu-id="32147-130">
<dt><span></span><span></span><strong></strong> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="32147-131">由任何字元序列組成的字串，包括空白字元和分行符號字元。</span><span class="sxs-lookup"><span data-stu-id="32147-131">A string composed of any sequence of characters, including white space and line-break characters.</span></span><br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="32147-132">子元素</span><span class="sxs-lookup"><span data-stu-id="32147-132">Child elements</span></span>

<span data-ttu-id="32147-133">沒有任何子項目。</span><span class="sxs-lookup"><span data-stu-id="32147-133">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="32147-134">父元素</span><span class="sxs-lookup"><span data-stu-id="32147-134">Parent elements</span></span>



| <span data-ttu-id="32147-135">元素</span><span class="sxs-lookup"><span data-stu-id="32147-135">Element</span></span>                                                                                       |
|-----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="32147-136">**CoNtextPopup.CoNtextMaps**</span><span class="sxs-lookup"><span data-stu-id="32147-136">**ContextPopup.ContextMaps**</span></span>](windowsribbon-element-contextpopup-contextmaps.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="32147-137">備註</span><span class="sxs-lookup"><span data-stu-id="32147-137">Remarks</span></span>

<span data-ttu-id="32147-138">選擇性。</span><span class="sxs-lookup"><span data-stu-id="32147-138">Optional.</span></span>

<span data-ttu-id="32147-139">每個 [**CoNtextPopup CoNtextMaps**](windowsribbon-element-contextpopup-contextmaps.md)可能會發生一次或多次。</span><span class="sxs-lookup"><span data-stu-id="32147-139">May occur one or more times for each [**ContextPopup.ContextMaps**](windowsribbon-element-contextpopup-contextmaps.md).</span></span>

## <a name="examples"></a><span data-ttu-id="32147-140">範例</span><span class="sxs-lookup"><span data-stu-id="32147-140">Examples</span></span>

<span data-ttu-id="32147-141">下列範例示範 [**CoNtextPopup**](windowsribbon-element-contextpopup.md) View 的基本標記。</span><span class="sxs-lookup"><span data-stu-id="32147-141">The following example demonstrates the basic markup for a [**ContextPopup**](windowsribbon-element-contextpopup.md) View.</span></span>

<span data-ttu-id="32147-142">這段程式碼會顯示一組 **CoNtextMap** 控制項宣告。</span><span class="sxs-lookup"><span data-stu-id="32147-142">This section of code shows a set of **ContextMap** control declarations.</span></span>


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



## <a name="element-information"></a><span data-ttu-id="32147-143">項目資訊</span><span class="sxs-lookup"><span data-stu-id="32147-143">Element information</span></span>



|                                     |           |
|-------------------------------------|-----------|
| <span data-ttu-id="32147-144">最低支援系統</span><span class="sxs-lookup"><span data-stu-id="32147-144">Minimum supported system</span></span><br/> | <span data-ttu-id="32147-145">Windows 7</span><span class="sxs-lookup"><span data-stu-id="32147-145">Windows 7</span></span> |
| <span data-ttu-id="32147-146">可以是空的</span><span class="sxs-lookup"><span data-stu-id="32147-146">Can be empty</span></span>                        | <span data-ttu-id="32147-147">Yes</span><span class="sxs-lookup"><span data-stu-id="32147-147">Yes</span></span>       |



## <a name="see-also"></a><span data-ttu-id="32147-148">另請參閱</span><span class="sxs-lookup"><span data-stu-id="32147-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="32147-149">CoNtext Popup 控制項</span><span class="sxs-lookup"><span data-stu-id="32147-149">Context Popup control</span></span>](windowsribbon-controls-contextpopup.md)
</dt> </dl>

 

 





