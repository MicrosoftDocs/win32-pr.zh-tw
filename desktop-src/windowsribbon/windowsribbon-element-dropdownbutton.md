---
title: DropDownButton 元素
description: 表示標準 Drop-Down 按鈕控制項。
ms.assetid: 41031be2-43bc-4f75-b37a-1dcecc1635e1
keywords:
- DropDownButton 元素視窗功能區
topic_type:
- apiref
api_name:
- DropDownButton
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 98af363aeb70a61def04eaee0ad13ff60e6e7640
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103682838"
---
# <a name="dropdownbutton-element"></a><span data-ttu-id="6c7f0-104">DropDownButton 元素</span><span class="sxs-lookup"><span data-stu-id="6c7f0-104">DropDownButton element</span></span>

<span data-ttu-id="6c7f0-105">表示標準 [下拉式按鈕](windowsribbon-controls-dropdownbutton.md) 控制項。</span><span class="sxs-lookup"><span data-stu-id="6c7f0-105">Represents a standard [Drop-Down Button](windowsribbon-controls-dropdownbutton.md) control.</span></span>

## <a name="usage"></a><span data-ttu-id="6c7f0-106">使用方式</span><span class="sxs-lookup"><span data-stu-id="6c7f0-106">Usage</span></span>

``` syntax
<DropDownButton
  ApplicationModes = "xs:string"
  CommandName = "xs:positiveInteger or xs:string">
  child elements
</DropDownButton>
```

## <a name="attributes"></a><span data-ttu-id="6c7f0-107">屬性</span><span class="sxs-lookup"><span data-stu-id="6c7f0-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="6c7f0-108">屬性</span><span class="sxs-lookup"><span data-stu-id="6c7f0-108">Attribute</span></span></th>
<th><span data-ttu-id="6c7f0-109">類型</span><span class="sxs-lookup"><span data-stu-id="6c7f0-109">Type</span></span></th>
<th><span data-ttu-id="6c7f0-110">必要</span><span class="sxs-lookup"><span data-stu-id="6c7f0-110">Required</span></span></th>
<th><span data-ttu-id="6c7f0-111">描述</span><span class="sxs-lookup"><span data-stu-id="6c7f0-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="6c7f0-112"><strong>ApplicationModes</strong></span><span class="sxs-lookup"><span data-stu-id="6c7f0-112"><strong>ApplicationModes</strong></span></span><br/></td>
<td><span data-ttu-id="6c7f0-113">xs:string</span><span class="sxs-lookup"><span data-stu-id="6c7f0-113">xs:string</span></span><br/></td>
<td><span data-ttu-id="6c7f0-114">No</span><span class="sxs-lookup"><span data-stu-id="6c7f0-114">No</span></span><br/></td>
<td><span data-ttu-id="6c7f0-115">只有在 <a href="windowsribbon-element-menugroup.md"><strong>MenuGroup</strong></a> 是父元素時才有效。</span><span class="sxs-lookup"><span data-stu-id="6c7f0-115">Valid only if <a href="windowsribbon-element-menugroup.md"><strong>MenuGroup</strong></a> is the parent element.</span></span><br/> <br/><span data-ttu-id="6c7f0-116">
<dt><span></span><span></span><strong></strong> (xs： string) </span><span class="sxs-lookup"><span data-stu-id="6c7f0-116">
<dt><span></span><span></span><strong></strong> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="6c7f0-117">字串，其中包含0到31之間的整數清單（以逗號分隔）。</span><span class="sxs-lookup"><span data-stu-id="6c7f0-117">A string that contains a comma-separated list of integers between 0 and 31.</span></span><br/> <span data-ttu-id="6c7f0-118">空白字元是有效的，而且會被忽略。</span><span class="sxs-lookup"><span data-stu-id="6c7f0-118">White space is valid and ignored.</span></span><br/> <span data-ttu-id="6c7f0-119">最大長度：250個字元。</span><span class="sxs-lookup"><span data-stu-id="6c7f0-119">Maximum length: 250 characters.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6c7f0-120"><strong>CommandName</strong></span><span class="sxs-lookup"><span data-stu-id="6c7f0-120"><strong>CommandName</strong></span></span><br/></td>
<td><span data-ttu-id="6c7f0-121">xs： positiveInteger 或 xs： string</span><span class="sxs-lookup"><span data-stu-id="6c7f0-121">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="6c7f0-122">No</span><span class="sxs-lookup"><span data-stu-id="6c7f0-122">No</span></span><br/></td>
<td><span data-ttu-id="6c7f0-123">將元素與 <a href="windowsribbon-element-command.md"><strong>命令</strong></a>產生關聯。</span><span class="sxs-lookup"><span data-stu-id="6c7f0-123">Associates the element with a <a href="windowsribbon-element-command.md"><strong>Command</strong></a>.</span></span><br/> <br/><span data-ttu-id="6c7f0-124">
<dt><span></span><span></span><strong></strong> (xs： positiveInteger 或 xs： string) </span><span class="sxs-lookup"><span data-stu-id="6c7f0-124">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="6c7f0-125">字串、介於2與59999（含）之間的整數值，或介於0x2 與0xea5f （含）之間的十六進位值。</span><span class="sxs-lookup"><span data-stu-id="6c7f0-125">A string, an integer value between 2 and 59999, inclusive, or a hexadecimal value between 0x2 and 0xea5f, inclusive.</span></span> <br/> <span data-ttu-id="6c7f0-126">值在功能區 XML 檔中必須是唯一的。</span><span class="sxs-lookup"><span data-stu-id="6c7f0-126">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="6c7f0-127">最大長度：100個字元。</span><span class="sxs-lookup"><span data-stu-id="6c7f0-127">Maximum length: 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="6c7f0-128">子元素</span><span class="sxs-lookup"><span data-stu-id="6c7f0-128">Child elements</span></span>



| <span data-ttu-id="6c7f0-129">元素</span><span class="sxs-lookup"><span data-stu-id="6c7f0-129">Element</span></span>                                                                             | <span data-ttu-id="6c7f0-130">描述</span><span class="sxs-lookup"><span data-stu-id="6c7f0-130">Description</span></span>                                        |
|-------------------------------------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="6c7f0-131">**Button**</span><span class="sxs-lookup"><span data-stu-id="6c7f0-131">**Button**</span></span>](windowsribbon-element-button.md)<br/>                           | <span data-ttu-id="6c7f0-132">可能會發生一次或多次</span><span class="sxs-lookup"><span data-stu-id="6c7f0-132">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="6c7f0-133">**相應**</span><span class="sxs-lookup"><span data-stu-id="6c7f0-133">**CheckBox**</span></span>](windowsribbon-element-checkbox.md)<br/>                       | <span data-ttu-id="6c7f0-134">可能會發生一次或多次</span><span class="sxs-lookup"><span data-stu-id="6c7f0-134">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="6c7f0-135">**ComboBox**</span><span class="sxs-lookup"><span data-stu-id="6c7f0-135">**ComboBox**</span></span>](windowsribbon-element-combobox.md)<br/>                       | <span data-ttu-id="6c7f0-136">可能會發生一次或多次</span><span class="sxs-lookup"><span data-stu-id="6c7f0-136">May occur one or more times</span></span><br/> <br/> |
| <span data-ttu-id="6c7f0-137">**DropDownButton**</span><span class="sxs-lookup"><span data-stu-id="6c7f0-137">**DropDownButton**</span></span><br/>                                                       | <span data-ttu-id="6c7f0-138">可能會發生一次或多次</span><span class="sxs-lookup"><span data-stu-id="6c7f0-138">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="6c7f0-139">**DropDownColorPicker**</span><span class="sxs-lookup"><span data-stu-id="6c7f0-139">**DropDownColorPicker**</span></span>](windowsribbon-element-dropdowncolorpicker.md)<br/> | <span data-ttu-id="6c7f0-140">可能會發生一次或多次</span><span class="sxs-lookup"><span data-stu-id="6c7f0-140">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="6c7f0-141">**DropDownGallery**</span><span class="sxs-lookup"><span data-stu-id="6c7f0-141">**DropDownGallery**</span></span>](windowsribbon-element-dropdowngallery.md)<br/>         | <span data-ttu-id="6c7f0-142">可能會發生一次或多次</span><span class="sxs-lookup"><span data-stu-id="6c7f0-142">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="6c7f0-143">**MenuGroup**</span><span class="sxs-lookup"><span data-stu-id="6c7f0-143">**MenuGroup**</span></span>](windowsribbon-element-menugroup.md)<br/>                     | <span data-ttu-id="6c7f0-144">至少必須發生一次</span><span class="sxs-lookup"><span data-stu-id="6c7f0-144">Must occur at least once</span></span><br/> <br/>    |
| [<span data-ttu-id="6c7f0-145">**SplitButton**</span><span class="sxs-lookup"><span data-stu-id="6c7f0-145">**SplitButton**</span></span>](windowsribbon-element-splitbutton.md)<br/>                 | <span data-ttu-id="6c7f0-146">可能會發生一次或多次</span><span class="sxs-lookup"><span data-stu-id="6c7f0-146">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="6c7f0-147">**SplitButtonGallery**</span><span class="sxs-lookup"><span data-stu-id="6c7f0-147">**SplitButtonGallery**</span></span>](windowsribbon-element-splitbuttongallery.md)<br/>   | <span data-ttu-id="6c7f0-148">可能會發生一次或多次</span><span class="sxs-lookup"><span data-stu-id="6c7f0-148">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="6c7f0-149">**ToggleButton**</span><span class="sxs-lookup"><span data-stu-id="6c7f0-149">**ToggleButton**</span></span>](windowsribbon-element-togglebutton.md)<br/>               | <span data-ttu-id="6c7f0-150">可能會發生一次或多次</span><span class="sxs-lookup"><span data-stu-id="6c7f0-150">May occur one or more times</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="6c7f0-151">父元素</span><span class="sxs-lookup"><span data-stu-id="6c7f0-151">Parent elements</span></span>



| <span data-ttu-id="6c7f0-152">元素</span><span class="sxs-lookup"><span data-stu-id="6c7f0-152">Element</span></span>                                                                           |
|-----------------------------------------------------------------------------------|
| [<span data-ttu-id="6c7f0-153">**ControlGroup**</span><span class="sxs-lookup"><span data-stu-id="6c7f0-153">**ControlGroup**</span></span>](windowsribbon-element-controlgroup.md)<br/>             |
| <span data-ttu-id="6c7f0-154">**DropDownButton**</span><span class="sxs-lookup"><span data-stu-id="6c7f0-154">**DropDownButton**</span></span><br/>                                                     |
| [<span data-ttu-id="6c7f0-155">**DropDownGallery**</span><span class="sxs-lookup"><span data-stu-id="6c7f0-155">**DropDownGallery**</span></span>](windowsribbon-element-dropdowngallery.md)<br/>       |
| [<span data-ttu-id="6c7f0-156">**Group**</span><span class="sxs-lookup"><span data-stu-id="6c7f0-156">**Group**</span></span>](windowsribbon-element-group.md)<br/>                           |
| [<span data-ttu-id="6c7f0-157">**MenuGroup**</span><span class="sxs-lookup"><span data-stu-id="6c7f0-157">**MenuGroup**</span></span>](windowsribbon-element-menugroup.md)<br/>                   |
| [<span data-ttu-id="6c7f0-158">**SplitButton**</span><span class="sxs-lookup"><span data-stu-id="6c7f0-158">**SplitButton**</span></span>](windowsribbon-element-splitbutton.md)<br/>               |
| [<span data-ttu-id="6c7f0-159">**SplitButtonGallery**</span><span class="sxs-lookup"><span data-stu-id="6c7f0-159">**SplitButtonGallery**</span></span>](windowsribbon-element-splitbuttongallery.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="6c7f0-160">備註</span><span class="sxs-lookup"><span data-stu-id="6c7f0-160">Remarks</span></span>

<span data-ttu-id="6c7f0-161">選擇性或必要，視父元素而定。</span><span class="sxs-lookup"><span data-stu-id="6c7f0-161">Optional or required, depending on the parent element.</span></span>

<span data-ttu-id="6c7f0-162">可能會針對每個 [**ControlGroup**](windowsribbon-element-controlgroup.md)、 **DropDownButton**、 [**DropDownGallery**](windowsribbon-element-dropdowngallery.md)、 [**Group**](windowsribbon-element-group.md)、 [**MenuGroup**](windowsribbon-element-menugroup.md)、 [**SplitButton**](windowsribbon-element-splitbutton.md)或 [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) 元素執行一次或多次。</span><span class="sxs-lookup"><span data-stu-id="6c7f0-162">May occur one or more times for each [**ControlGroup**](windowsribbon-element-controlgroup.md), **DropDownButton**, [**DropDownGallery**](windowsribbon-element-dropdowngallery.md), [**Group**](windowsribbon-element-group.md), [**MenuGroup**](windowsribbon-element-menugroup.md), [**SplitButton**](windowsribbon-element-splitbutton.md), or [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) element.</span></span>

<span data-ttu-id="6c7f0-163">**DropDownButton** 在應用程式功能表的左邊資料行中裝載時，支援 [應用程式模式](ribbon-applicationmodes.md) 。</span><span class="sxs-lookup"><span data-stu-id="6c7f0-163">**DropDownButton** supports [application modes](ribbon-applicationmodes.md) when it is hosted in the left column of the Application Menu.</span></span>

<span data-ttu-id="6c7f0-164">當 **DropDownButton** 是 [**ApplicationMenu**](windowsribbon-element-applicationmenu.md)的子系時， [**DropDownGallery**](windowsribbon-element-dropdowngallery.md)和 [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md)不是 **DropDownButton** 的有效子項目。</span><span class="sxs-lookup"><span data-stu-id="6c7f0-164">[**DropDownGallery**](windowsribbon-element-dropdowngallery.md) and [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) are not valid child elements of **DropDownButton** when **DropDownButton** is a descendant of [**ApplicationMenu**](windowsribbon-element-applicationmenu.md).</span></span>

## <a name="examples"></a><span data-ttu-id="6c7f0-165">範例</span><span class="sxs-lookup"><span data-stu-id="6c7f0-165">Examples</span></span>

<span data-ttu-id="6c7f0-166">下列範例示範 **DropDownButton** 的基本標記。</span><span class="sxs-lookup"><span data-stu-id="6c7f0-166">The following example demonstrates the basic markup for the **DropDownButton**.</span></span>

<span data-ttu-id="6c7f0-167">這段程式碼會顯示 **DropDownButton** 命令宣告，以及可作為 **DropDownButton** 元素之父容器的相關聯 [**群組**](windowsribbon-element-group.md)。</span><span class="sxs-lookup"><span data-stu-id="6c7f0-167">This section of code shows the **DropDownButton** Command declarations, with an associated [**Group**](windowsribbon-element-group.md) that functions as the parent container for the **DropDownButton** element.</span></span>


```XML
<!-- DropDownButton -->
<Command Name="cmdDropDownButtonGroup"
         Symbol="cmdDropDownButtonGroup"
         Comment="DropDownButton Group"
         LabelTitle="DropDownButton"/>
<Command Name="cmdDropDownButton"
         Symbol="cmdDropDownButton"
         Comment="DropDownButton"
         LabelTitle="DropDownButton"/>
<Command Name="cmdDDBButton1"
         Symbol="cmdDDBButton1"
         Comment="DDBButton1"
         LabelTitle="DDB Button"/>
<Command Name="cmdDDBColorPicker"
         Symbol="cmdDDBColorPicker"
         Comment="DDBColorPicker"
         LabelTitle="DDB ColorPicker"/>
```



<span data-ttu-id="6c7f0-168">這段程式碼會顯示 **DropDownButton** 控制項宣告。</span><span class="sxs-lookup"><span data-stu-id="6c7f0-168">This section of code shows the **DropDownButton** control declarations.</span></span>


```XML
<Group CommandName="cmdDropDownButtonGroup">
  <DropDownButton CommandName="cmdDropDownButton">
    <MenuGroup>
      <Button CommandName="cmdDDBButton1"/>
      <DropDownColorPicker CommandName="cmdDDBColorPicker"/>
    </MenuGroup>
  </DropDownButton>
</Group>
```



## <a name="element-information"></a><span data-ttu-id="6c7f0-169">項目資訊</span><span class="sxs-lookup"><span data-stu-id="6c7f0-169">Element information</span></span>



|                                     |           |
|-------------------------------------|-----------|
| <span data-ttu-id="6c7f0-170">最低支援系統</span><span class="sxs-lookup"><span data-stu-id="6c7f0-170">Minimum supported system</span></span><br/> | <span data-ttu-id="6c7f0-171">Windows 7</span><span class="sxs-lookup"><span data-stu-id="6c7f0-171">Windows 7</span></span> |
| <span data-ttu-id="6c7f0-172">可以是空的</span><span class="sxs-lookup"><span data-stu-id="6c7f0-172">Can be empty</span></span>                        | <span data-ttu-id="6c7f0-173">否</span><span class="sxs-lookup"><span data-stu-id="6c7f0-173">No</span></span>        |



## <a name="see-also"></a><span data-ttu-id="6c7f0-174">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6c7f0-174">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c7f0-175">下拉式按鈕控制項</span><span class="sxs-lookup"><span data-stu-id="6c7f0-175">Drop-Down Button control</span></span>](windowsribbon-controls-dropdownbutton.md)
</dt> <dt>

[<span data-ttu-id="6c7f0-176">**SetModes**</span><span class="sxs-lookup"><span data-stu-id="6c7f0-176">**SetModes**</span></span>](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setmodes)
</dt> </dl>

 

