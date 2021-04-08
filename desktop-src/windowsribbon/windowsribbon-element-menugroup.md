---
title: MenuGroup 元素
description: 表示要在圖庫、功能表或工具列中顯示的控制項容器。
ms.assetid: 75da63fe-dd9e-46af-8f13-a8d8e7575641
keywords:
- MenuGroup 元素視窗功能區
topic_type:
- apiref
api_name:
- MenuGroup
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: fa3c126a99cddd4918ea9033acffd185ad5cf3da
ms.sourcegitcommit: 927b9c371f75f52b8011483edf3a4ba37d11ebe4
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/11/2020
ms.locfileid: "103680831"
---
# <a name="menugroup-element"></a><span data-ttu-id="3091e-104">MenuGroup 元素</span><span class="sxs-lookup"><span data-stu-id="3091e-104">MenuGroup element</span></span>

<span data-ttu-id="3091e-105">表示要在圖庫、功能表或工具列中顯示的控制項容器。</span><span class="sxs-lookup"><span data-stu-id="3091e-105">Represents a container of controls to display in a gallery, menu, or toolbar.</span></span>

## <a name="usage"></a><span data-ttu-id="3091e-106">使用方式</span><span class="sxs-lookup"><span data-stu-id="3091e-106">Usage</span></span>

``` syntax
<MenuGroup
  Class = "xs:string"
  CommandName = "xs:positiveInteger or xs:string">
  child elements
</MenuGroup>
```

## <a name="attributes"></a><span data-ttu-id="3091e-107">屬性</span><span class="sxs-lookup"><span data-stu-id="3091e-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="3091e-108">屬性</span><span class="sxs-lookup"><span data-stu-id="3091e-108">Attribute</span></span></th>
<th><span data-ttu-id="3091e-109">類型</span><span class="sxs-lookup"><span data-stu-id="3091e-109">Type</span></span></th>
<th><span data-ttu-id="3091e-110">必要</span><span class="sxs-lookup"><span data-stu-id="3091e-110">Required</span></span></th>
<th><span data-ttu-id="3091e-111">描述</span><span class="sxs-lookup"><span data-stu-id="3091e-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="3091e-112"><strong>類別</strong></span><span class="sxs-lookup"><span data-stu-id="3091e-112"><strong>Class</strong></span></span><br/></td>
<td><span data-ttu-id="3091e-113">xs:string</span><span class="sxs-lookup"><span data-stu-id="3091e-113">xs:string</span></span><br/></td>
<td><span data-ttu-id="3091e-114">No</span><span class="sxs-lookup"><span data-stu-id="3091e-114">No</span></span><br/></td>
<td><span data-ttu-id="3091e-115">指定功能表 UI 中元素的大小和配置樣式。</span><span class="sxs-lookup"><span data-stu-id="3091e-115">Specifies the size and layout style for elements in the menu UI.</span></span><br/> <span data-ttu-id="3091e-116">您可以使用 <a href="windowsribbon-element-command-largeimages.md"><strong>LargeImages</strong></a> 和 <a href="windowsribbon-element-command-smallimages.md"><strong>SmallImages</strong></a> 屬性專案，以兩種大小提供影像資源 (大型和小型) ，並與標記中的元素相關聯。</span><span class="sxs-lookup"><span data-stu-id="3091e-116">An image resource can be supplied in two sizes (large and small) and associated with the element in markup using the <a href="windowsribbon-element-command-largeimages.md"><strong>Command.LargeImages</strong></a> and <a href="windowsribbon-element-command-smallimages.md"><strong>Command.SmallImages</strong></a> property elements.</span></span> <span data-ttu-id="3091e-117">如果只提供一個影像，則架構會視需要調整其大小。</span><span class="sxs-lookup"><span data-stu-id="3091e-117">If only one image is supplied, the framework resizes it as necessary.</span></span><br/> <span data-ttu-id="3091e-118">限制為下列其中一個值：</span><span class="sxs-lookup"><span data-stu-id="3091e-118">Restricted to one of the following values:</span></span><br/> <br/><span data-ttu-id="3091e-119">
<dt><span></span><span></span><strong></strong> (StandardItems) </span><span class="sxs-lookup"><span data-stu-id="3091e-119">
<dt><span></span><span></span><strong></strong> (StandardItems)</span></span><br/> </dt> <dd> <span data-ttu-id="3091e-120">預設值。</span><span class="sxs-lookup"><span data-stu-id="3091e-120">Default.</span></span> <br/> <span data-ttu-id="3091e-121">樣式：小型影像和反白的文字。</span><span class="sxs-lookup"><span data-stu-id="3091e-121">Style: small image and de-emphasized text.</span></span><br/><img src="images/markup/menugroup-standarditems.png" alt="Screen shot of a StandardItems button." /></dd> <span data-ttu-id="3091e-122"><dt><span></span><span></span><strong></strong> (MajorItems) </span><span class="sxs-lookup"><span data-stu-id="3091e-122"><dt><span></span><span></span><strong></strong> (MajorItems)</span></span><br/> </dt> <dd> <span data-ttu-id="3091e-123">樣式：大型影像和粗體文字。</span><span class="sxs-lookup"><span data-stu-id="3091e-123">Style: large image and bold text.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="3091e-124">如果 <strong>MenuGroup</strong> 是 <a href="windowsribbon-element-applicationmenu.md"><strong>ApplicationMenu</strong></a>的子系，則會忽略 <em>類別</em> 屬性，而 <code>MajorItems</code> 架構會強制執行的樣式。</span><span class="sxs-lookup"><span data-stu-id="3091e-124">If <strong>MenuGroup</strong> is a child of <a href="windowsribbon-element-applicationmenu.md"><strong>ApplicationMenu</strong></a>, the <em>Class</em> attribute is ignored and a style of <code>MajorItems</code> is enforced by the framework.</span></span>
</blockquote>
<br/> <img src="images/markup/menugroup-majoritems.png" alt="Screen shot of a MajorItems button." /></dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3091e-125"><strong>CommandName</strong></span><span class="sxs-lookup"><span data-stu-id="3091e-125"><strong>CommandName</strong></span></span><br/></td>
<td><span data-ttu-id="3091e-126">xs： positiveInteger 或 xs： string</span><span class="sxs-lookup"><span data-stu-id="3091e-126">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="3091e-127">No</span><span class="sxs-lookup"><span data-stu-id="3091e-127">No</span></span><br/></td>
<td><span data-ttu-id="3091e-128">將元素與 <a href="windowsribbon-element-command.md"><strong>命令</strong></a>產生關聯。</span><span class="sxs-lookup"><span data-stu-id="3091e-128">Associates the element with a <a href="windowsribbon-element-command.md"><strong>Command</strong></a>.</span></span><br/> <br/><span data-ttu-id="3091e-129">
<dt><span></span><span></span><strong></strong> (xs： positiveInteger 或 xs： string) </span><span class="sxs-lookup"><span data-stu-id="3091e-129">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="3091e-130">字串、介於2與59999（含）之間的整數值，或介於0x2 與0xea5f （含）之間的十六進位值。</span><span class="sxs-lookup"><span data-stu-id="3091e-130">A string, an integer value between 2 and 59999, inclusive, or a hexadecimal value between 0x2 and 0xea5f, inclusive.</span></span> <br/> <span data-ttu-id="3091e-131">值在功能區 XML 檔中必須是唯一的。</span><span class="sxs-lookup"><span data-stu-id="3091e-131">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="3091e-132">最大長度：100個字元。</span><span class="sxs-lookup"><span data-stu-id="3091e-132">Maximum length: 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="3091e-133">子元素</span><span class="sxs-lookup"><span data-stu-id="3091e-133">Child elements</span></span>



| <span data-ttu-id="3091e-134">元素</span><span class="sxs-lookup"><span data-stu-id="3091e-134">Element</span></span>                                                                             | <span data-ttu-id="3091e-135">描述</span><span class="sxs-lookup"><span data-stu-id="3091e-135">Description</span></span>                                        |
|-------------------------------------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="3091e-136">**Button**</span><span class="sxs-lookup"><span data-stu-id="3091e-136">**Button**</span></span>](windowsribbon-element-button.md)<br/>                           | <span data-ttu-id="3091e-137">可能會發生一次或多次</span><span class="sxs-lookup"><span data-stu-id="3091e-137">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="3091e-138">**相應**</span><span class="sxs-lookup"><span data-stu-id="3091e-138">**CheckBox**</span></span>](windowsribbon-element-checkbox.md)<br/>                       | <span data-ttu-id="3091e-139">可能會發生一次或多次</span><span class="sxs-lookup"><span data-stu-id="3091e-139">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="3091e-140">**ComboBox**</span><span class="sxs-lookup"><span data-stu-id="3091e-140">**ComboBox**</span></span>](windowsribbon-element-combobox.md)<br/>                       | <span data-ttu-id="3091e-141">可能會發生一次或多次</span><span class="sxs-lookup"><span data-stu-id="3091e-141">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="3091e-142">**DropDownButton**</span><span class="sxs-lookup"><span data-stu-id="3091e-142">**DropDownButton**</span></span>](windowsribbon-element-dropdownbutton.md)<br/>           | <span data-ttu-id="3091e-143">可能會發生一次或多次</span><span class="sxs-lookup"><span data-stu-id="3091e-143">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="3091e-144">**DropDownColorPicker**</span><span class="sxs-lookup"><span data-stu-id="3091e-144">**DropDownColorPicker**</span></span>](windowsribbon-element-dropdowncolorpicker.md)<br/> | <span data-ttu-id="3091e-145">可能會發生一次或多次</span><span class="sxs-lookup"><span data-stu-id="3091e-145">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="3091e-146">**DropDownGallery**</span><span class="sxs-lookup"><span data-stu-id="3091e-146">**DropDownGallery**</span></span>](windowsribbon-element-dropdowngallery.md)<br/>         | <span data-ttu-id="3091e-147">可能會發生一次或多次</span><span class="sxs-lookup"><span data-stu-id="3091e-147">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="3091e-148">**FontControl**</span><span class="sxs-lookup"><span data-stu-id="3091e-148">**FontControl**</span></span>](windowsribbon-element-fontcontrol.md)<br/>                 | <span data-ttu-id="3091e-149">最多可能發生一次</span><span class="sxs-lookup"><span data-stu-id="3091e-149">May occur at most once</span></span><br/> <br/>      |
| [<span data-ttu-id="3091e-150">**SplitButton**</span><span class="sxs-lookup"><span data-stu-id="3091e-150">**SplitButton**</span></span>](windowsribbon-element-splitbutton.md)<br/>                 | <span data-ttu-id="3091e-151">可能會發生一次或多次</span><span class="sxs-lookup"><span data-stu-id="3091e-151">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="3091e-152">**SplitButtonGallery**</span><span class="sxs-lookup"><span data-stu-id="3091e-152">**SplitButtonGallery**</span></span>](windowsribbon-element-splitbuttongallery.md)<br/>   | <span data-ttu-id="3091e-153">可能會發生一次或多次</span><span class="sxs-lookup"><span data-stu-id="3091e-153">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="3091e-154">**ToggleButton**</span><span class="sxs-lookup"><span data-stu-id="3091e-154">**ToggleButton**</span></span>](windowsribbon-element-togglebutton.md)<br/>               | <span data-ttu-id="3091e-155">可能會發生一次或多次</span><span class="sxs-lookup"><span data-stu-id="3091e-155">May occur one or more times</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="3091e-156">父元素</span><span class="sxs-lookup"><span data-stu-id="3091e-156">Parent elements</span></span>



| <span data-ttu-id="3091e-157">元素</span><span class="sxs-lookup"><span data-stu-id="3091e-157">Element</span></span>                                                                                                 |
|---------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3091e-158">**ApplicationMenu**</span><span class="sxs-lookup"><span data-stu-id="3091e-158">**ApplicationMenu**</span></span>](windowsribbon-element-applicationmenu.md)<br/>                             |
| [<span data-ttu-id="3091e-159">**ContextMenu**</span><span class="sxs-lookup"><span data-stu-id="3091e-159">**ContextMenu**</span></span>](windowsribbon-element-contextmenu.md)<br/>                                     |
| [<span data-ttu-id="3091e-160">**DropDownButton**</span><span class="sxs-lookup"><span data-stu-id="3091e-160">**DropDownButton**</span></span>](windowsribbon-element-dropdownbutton.md)<br/>                               |
| [<span data-ttu-id="3091e-161">**DropDownGallery.MenuGroups**</span><span class="sxs-lookup"><span data-stu-id="3091e-161">**DropDownGallery.MenuGroups**</span></span>](windowsribbon-element-dropdowngallery-menugroups.md)<br/>       |
| [<span data-ttu-id="3091e-162">**InRibbonGallery.MenuGroups**</span><span class="sxs-lookup"><span data-stu-id="3091e-162">**InRibbonGallery.MenuGroups**</span></span>](windowsribbon-element-inribbongallery-menugroups.md)<br/>       |
| [<span data-ttu-id="3091e-163">**浮動工具列**</span><span class="sxs-lookup"><span data-stu-id="3091e-163">**MiniToolbar**</span></span>](windowsribbon-element-minitoolbar.md)<br/>                                     |
| [<span data-ttu-id="3091e-164">**SplitButton. MenuGroups**</span><span class="sxs-lookup"><span data-stu-id="3091e-164">**SplitButton.MenuGroups**</span></span>](windowsribbon-element-splitbutton-menugroups.md)<br/>               |
| [<span data-ttu-id="3091e-165">**SplitButtonGallery.MenuGroups**</span><span class="sxs-lookup"><span data-stu-id="3091e-165">**SplitButtonGallery.MenuGroups**</span></span>](windowsribbon-element-splitbuttongallery-menugroups.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="3091e-166">備註</span><span class="sxs-lookup"><span data-stu-id="3091e-166">Remarks</span></span>

<span data-ttu-id="3091e-167">必要。</span><span class="sxs-lookup"><span data-stu-id="3091e-167">Required.</span></span>

<span data-ttu-id="3091e-168">每個 [**ApplicationMenu**](windowsribbon-element-applicationmenu.md)、 [**CoNtextMenu**](windowsribbon-element-contextmenu.md)、 [**DropDownButton**](windowsribbon-element-dropdownbutton.md)、 [**DropDownGallery**](windowsribbon-element-dropdowngallery-menugroups.md)、MenuGroups、 [**InRibbonGallery**](windowsribbon-element-inribbongallery-menugroups.md) [**、MenuGroups**](windowsribbon-element-splitbutton-menugroups.md)、SplitButton、 [**MenuGroups**](windowsribbon-element-minitoolbar.md)或 [**浮動工具列**](windowsribbon-element-splitbuttongallery-menugroups.md) 元素都必須至少發生一次。</span><span class="sxs-lookup"><span data-stu-id="3091e-168">Must occur at least once for each [**ApplicationMenu**](windowsribbon-element-applicationmenu.md), [**ContextMenu**](windowsribbon-element-contextmenu.md), [**DropDownButton**](windowsribbon-element-dropdownbutton.md), [**DropDownGallery.MenuGroups**](windowsribbon-element-dropdowngallery-menugroups.md), [**InRibbonGallery.MenuGroups**](windowsribbon-element-inribbongallery-menugroups.md), [**SplitButton.MenuGroups**](windowsribbon-element-splitbutton-menugroups.md), [**MiniToolbar**](windowsribbon-element-minitoolbar.md), or [**SplitButtonGallery.MenuGroups**](windowsribbon-element-splitbuttongallery-menugroups.md) element.</span></span>

<span data-ttu-id="3091e-169">如果 [**ApplicationMenu**](windowsribbon-element-applicationmenu.md) 是父元素，則 **MenuGroup** 會限制為下列子項目： [**Button**](windowsribbon-element-button.md)、 [**DropDownButton**](windowsribbon-element-dropdownbutton.md)、 [**DropDownGallery**](windowsribbon-element-dropdowngallery.md)、 [**SplitButton**](windowsribbon-element-splitbutton.md)或 [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md)。</span><span class="sxs-lookup"><span data-stu-id="3091e-169">If [**ApplicationMenu**](windowsribbon-element-applicationmenu.md) is the parent element then **MenuGroup** is constrained to the following child elements: [**Button**](windowsribbon-element-button.md), [**DropDownButton**](windowsribbon-element-dropdownbutton.md), [**DropDownGallery**](windowsribbon-element-dropdowngallery.md), [**SplitButton**](windowsribbon-element-splitbutton.md), or [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md).</span></span>

<span data-ttu-id="3091e-170">如果 [**CoNtextMenu**](windowsribbon-element-contextmenu.md)、 [**DropDownButton**](windowsribbon-element-dropdownbutton.md)、 [**DropDownGallery、MenuGroups**](windowsribbon-element-dropdowngallery-menugroups.md)、 [**InRibbonGallery**](windowsribbon-element-inribbongallery-menugroups.md)、 [**MenuGroups**](windowsribbon-element-splitbutton-menugroups.md)、SplitButton 或 [**MenuGroups**](windowsribbon-element-splitbuttongallery-menugroups.md) 是父元素，則 **SplitButtonGallery** 會限制為下列子項目： [**Button**](windowsribbon-element-button.md)、 [**CheckBox**](windowsribbon-element-checkbox.md)、 **MenuGroups**、 [**MenuGroup**](windowsribbon-element-dropdowncolorpicker.md)、 [**DropDownButton**](windowsribbon-element-dropdowngallery.md)、 [**DropDownColorPicker**](windowsribbon-element-splitbutton.md)、 [**DropDownGallery**](windowsribbon-element-splitbuttongallery.md)或 [**切換按鈕**](windowsribbon-element-togglebutton.md)。</span><span class="sxs-lookup"><span data-stu-id="3091e-170">If [**ContextMenu**](windowsribbon-element-contextmenu.md), [**DropDownButton**](windowsribbon-element-dropdownbutton.md), [**DropDownGallery.MenuGroups**](windowsribbon-element-dropdowngallery-menugroups.md), [**InRibbonGallery.MenuGroups**](windowsribbon-element-inribbongallery-menugroups.md), [**SplitButton.MenuGroups**](windowsribbon-element-splitbutton-menugroups.md), or [**SplitButtonGallery.MenuGroups**](windowsribbon-element-splitbuttongallery-menugroups.md) is the parent element then **MenuGroup** is constrained to the following child elements: [**Button**](windowsribbon-element-button.md), [**CheckBox**](windowsribbon-element-checkbox.md), **DropDownButton**, [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md), [**DropDownGallery**](windowsribbon-element-dropdowngallery.md), [**SplitButton**](windowsribbon-element-splitbutton.md), [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md), or [**ToggleButton**](windowsribbon-element-togglebutton.md).</span></span>

<span data-ttu-id="3091e-171">如果 [**浮動工具列**](windowsribbon-element-minitoolbar.md) 是父元素，則 **MenuGroup** 會限制為下列子項目： [**Button**](windowsribbon-element-button.md)、 [**CheckBox**](windowsribbon-element-checkbox.md)、 [**ComboBox**](windowsribbon-element-combobox.md)、 [**DropDownButton**](windowsribbon-element-dropdownbutton.md)、 [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md)、 [**DropDownGallery**](windowsribbon-element-dropdowngallery.md)、 [**FontControl**](windowsribbon-element-fontcontrol.md)、 [**微調**](windowsribbon-element-spinner.md)、 [**SplitButton**](windowsribbon-element-splitbutton.md)、 [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md)或 [**切換按鈕**](windowsribbon-element-togglebutton.md)。</span><span class="sxs-lookup"><span data-stu-id="3091e-171">If [**MiniToolbar**](windowsribbon-element-minitoolbar.md) is the parent element then **MenuGroup** is constrained to the following child elements: [**Button**](windowsribbon-element-button.md), [**CheckBox**](windowsribbon-element-checkbox.md), [**ComboBox**](windowsribbon-element-combobox.md), [**DropDownButton**](windowsribbon-element-dropdownbutton.md), [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md), [**DropDownGallery**](windowsribbon-element-dropdowngallery.md), [**FontControl**](windowsribbon-element-fontcontrol.md), [**Spinner**](windowsribbon-element-spinner.md), [**SplitButton**](windowsribbon-element-splitbutton.md), [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md), or [**ToggleButton**](windowsribbon-element-togglebutton.md).</span></span>

<span data-ttu-id="3091e-172">當 [**ApplicationMenu**](windowsribbon-element-applicationmenu.md) 是父元素時，不需要類別屬性。</span><span class="sxs-lookup"><span data-stu-id="3091e-172">The Class attribute is not required when [**ApplicationMenu**](windowsribbon-element-applicationmenu.md) is the parent element.</span></span> <span data-ttu-id="3091e-173">架構會強制執行類別屬性的 MajorItems 值。</span><span class="sxs-lookup"><span data-stu-id="3091e-173">The framework enforces a value of MajorItems for the Class attribute.</span></span>

<span data-ttu-id="3091e-174">當 [**ApplicationMenu**](windowsribbon-element-applicationmenu.md) 是父元素時，不需要類別屬性。</span><span class="sxs-lookup"><span data-stu-id="3091e-174">When [**ApplicationMenu**](windowsribbon-element-applicationmenu.md) is the parent element the Class attribute is not required.</span></span>

## <a name="examples"></a><span data-ttu-id="3091e-175">範例</span><span class="sxs-lookup"><span data-stu-id="3091e-175">Examples</span></span>

<span data-ttu-id="3091e-176">下列範例示範具有 **MenuGroup** 元素之 [**SplitButton**](windowsribbon-element-splitbutton.md)的基本標記。</span><span class="sxs-lookup"><span data-stu-id="3091e-176">The following example demonstrates the basic markup for the [**SplitButton**](windowsribbon-element-splitbutton.md) with a **MenuGroup** element.</span></span>

<span data-ttu-id="3091e-177">這段程式碼會顯示具有大型和小型影像資源的 [**SplitButton**](windowsribbon-element-splitbutton.md) 和 **MenuGroup** 命令宣告。</span><span class="sxs-lookup"><span data-stu-id="3091e-177">This section of code shows the [**SplitButton**](windowsribbon-element-splitbutton.md) and **MenuGroup** Command declarations with a large and a small image resource.</span></span> <span data-ttu-id="3091e-178">也會宣告作為 **SplitButton** 專案父容器的相關聯 [**群組**](windowsribbon-element-group.md)。</span><span class="sxs-lookup"><span data-stu-id="3091e-178">An associated [**Group**](windowsribbon-element-group.md) that acts as the parent container for the **SplitButton** element is also declared.</span></span>


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



<span data-ttu-id="3091e-179">這段程式碼會以和來顯示 [**SplitButton**](windowsribbon-element-splitbutton.md) 和 **MenuGroup** 控制項 `StandardItems` 宣告 `MajorItems` 。</span><span class="sxs-lookup"><span data-stu-id="3091e-179">This section of code shows the [**SplitButton**](windowsribbon-element-splitbutton.md) and **MenuGroup** control declarations with both `StandardItems` and `MajorItems`.</span></span>


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



## <a name="element-information"></a><span data-ttu-id="3091e-180">項目資訊</span><span class="sxs-lookup"><span data-stu-id="3091e-180">Element information</span></span>



|                                     |           |
|-------------------------------------|-----------|
| <span data-ttu-id="3091e-181">最低支援系統</span><span class="sxs-lookup"><span data-stu-id="3091e-181">Minimum supported system</span></span><br/> | <span data-ttu-id="3091e-182">Windows 7</span><span class="sxs-lookup"><span data-stu-id="3091e-182">Windows 7</span></span> |
| <span data-ttu-id="3091e-183">可以是空的</span><span class="sxs-lookup"><span data-stu-id="3091e-183">Can be empty</span></span>                        | <span data-ttu-id="3091e-184">否</span><span class="sxs-lookup"><span data-stu-id="3091e-184">No</span></span>        |



## <a name="see-also"></a><span data-ttu-id="3091e-185">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3091e-185">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3091e-186">指定功能區影像資源</span><span class="sxs-lookup"><span data-stu-id="3091e-186">Specifying Ribbon Image Resources</span></span>](windowsribbon-imageformats.md)
</dt> <dt>

[<span data-ttu-id="3091e-187">功能表群組</span><span class="sxs-lookup"><span data-stu-id="3091e-187">Menu Group</span></span>](windowsribbon-controls-menugroup.md)
</dt> </dl>

 

 





