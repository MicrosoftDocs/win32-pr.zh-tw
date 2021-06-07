---
title: ControlGroup 元素
description: 代表 SizeDefinition 版面配置範本中的一組控制項。
ms.assetid: 688f3fa5-f305-4554-b16a-590983cf23b9
keywords:
- ControlGroup 元素視窗功能區
topic_type:
- apiref
api_name:
- ControlGroup
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7d2b49612102d03003c2f61395a56647aaef4475
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/04/2021
ms.locfileid: "111442939"
---
# <a name="controlgroup-element"></a><span data-ttu-id="2fe8f-104">ControlGroup 元素</span><span class="sxs-lookup"><span data-stu-id="2fe8f-104">ControlGroup element</span></span>

<span data-ttu-id="2fe8f-105">代表 [**SizeDefinition**](windowsribbon-element-sizedefinition.md) 版面配置範本中的一組控制項。</span><span class="sxs-lookup"><span data-stu-id="2fe8f-105">Represents a group of controls in a [**SizeDefinition**](windowsribbon-element-sizedefinition.md) layout template.</span></span>

## <a name="usage"></a><span data-ttu-id="2fe8f-106">使用方式</span><span class="sxs-lookup"><span data-stu-id="2fe8f-106">Usage</span></span>

``` syntax
<ControlGroup
  SequenceNumber = "xs:positiveInteger">
  child elements
</ControlGroup>
```

## <a name="attributes"></a><span data-ttu-id="2fe8f-107">屬性</span><span class="sxs-lookup"><span data-stu-id="2fe8f-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="2fe8f-108">屬性</span><span class="sxs-lookup"><span data-stu-id="2fe8f-108">Attribute</span></span></th>
<th><span data-ttu-id="2fe8f-109">類型</span><span class="sxs-lookup"><span data-stu-id="2fe8f-109">Type</span></span></th>
<th><span data-ttu-id="2fe8f-110">必要</span><span class="sxs-lookup"><span data-stu-id="2fe8f-110">Required</span></span></th>
<th><span data-ttu-id="2fe8f-111">描述</span><span class="sxs-lookup"><span data-stu-id="2fe8f-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="2fe8f-112"><strong>SequenceNumber</strong></span><span class="sxs-lookup"><span data-stu-id="2fe8f-112"><strong>SequenceNumber</strong></span></span><br/></td>
<td><span data-ttu-id="2fe8f-113">xs:positiveInteger</span><span class="sxs-lookup"><span data-stu-id="2fe8f-113">xs:positiveInteger</span></span><br/></td>
<td><span data-ttu-id="2fe8f-114">否</span><span class="sxs-lookup"><span data-stu-id="2fe8f-114">No</span></span><br/></td>
<td><span data-ttu-id="2fe8f-115">只有當 <a href="windowsribbon-element-group.md"><strong>群組</strong></a> 是父元素時才有效。</span><span class="sxs-lookup"><span data-stu-id="2fe8f-115">Valid only when <a href="windowsribbon-element-group.md"><strong>Group</strong></a> is the parent element.</span></span><br/> <span data-ttu-id="2fe8f-116">每個 <em>SequenceNumber</em> 在 <a href="windowsribbon-element-group.md"><strong>Group</strong></a> 元素內都必須是唯一的。</span><span class="sxs-lookup"><span data-stu-id="2fe8f-116">Each <em>SequenceNumber</em> must be unique within a <a href="windowsribbon-element-group.md"><strong>Group</strong></a> element.</span></span> <span data-ttu-id="2fe8f-117"><em>SequenceNumber</em>的值應該會增加每個<strong>群組</strong>元素，但不需要是連續的。</span><span class="sxs-lookup"><span data-stu-id="2fe8f-117">The values for <em>SequenceNumber</em> should increase for each <strong>Group</strong> element, but do not need to be sequential.</span></span> <br/> <br/><span data-ttu-id="2fe8f-118">
<dt><span></span><span></span><strong></strong> (xs： positiveInteger) </span><span class="sxs-lookup"><span data-stu-id="2fe8f-118">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger)</span></span><br/> </dt> <dd> <span data-ttu-id="2fe8f-119">介於1000和59999之間的任何正整數值（含）。</span><span class="sxs-lookup"><span data-stu-id="2fe8f-119">Any positive integer value between 1000 and 59999, inclusive.</span></span><br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="2fe8f-120">子元素</span><span class="sxs-lookup"><span data-stu-id="2fe8f-120">Child elements</span></span>



| <span data-ttu-id="2fe8f-121">元素</span><span class="sxs-lookup"><span data-stu-id="2fe8f-121">Element</span></span>                                                                                 | <span data-ttu-id="2fe8f-122">描述</span><span class="sxs-lookup"><span data-stu-id="2fe8f-122">Description</span></span>                                        |
|-----------------------------------------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="2fe8f-123">**Button**</span><span class="sxs-lookup"><span data-stu-id="2fe8f-123">**Button**</span></span>](windowsribbon-element-button.md)<br/>                               | <span data-ttu-id="2fe8f-124">可能會發生一次或多次</span><span class="sxs-lookup"><span data-stu-id="2fe8f-124">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="2fe8f-125">**相應**</span><span class="sxs-lookup"><span data-stu-id="2fe8f-125">**CheckBox**</span></span>](windowsribbon-element-checkbox.md)<br/>                           | <span data-ttu-id="2fe8f-126">可能會發生一次或多次</span><span class="sxs-lookup"><span data-stu-id="2fe8f-126">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="2fe8f-127">**ComboBox**</span><span class="sxs-lookup"><span data-stu-id="2fe8f-127">**ComboBox**</span></span>](windowsribbon-element-combobox.md)<br/>                           | <span data-ttu-id="2fe8f-128">可能會發生一次或多次</span><span class="sxs-lookup"><span data-stu-id="2fe8f-128">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="2fe8f-129">**ControlSizeDefinition**</span><span class="sxs-lookup"><span data-stu-id="2fe8f-129">**ControlSizeDefinition**</span></span>](windowsribbon-element-controlsizedefinition.md)<br/> | <span data-ttu-id="2fe8f-130">可能會發生一次或多次</span><span class="sxs-lookup"><span data-stu-id="2fe8f-130">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="2fe8f-131">**DropDownButton**</span><span class="sxs-lookup"><span data-stu-id="2fe8f-131">**DropDownButton**</span></span>](windowsribbon-element-dropdownbutton.md)<br/>               | <span data-ttu-id="2fe8f-132">可能會發生一次或多次</span><span class="sxs-lookup"><span data-stu-id="2fe8f-132">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="2fe8f-133">**DropDownColorPicker**</span><span class="sxs-lookup"><span data-stu-id="2fe8f-133">**DropDownColorPicker**</span></span>](windowsribbon-element-dropdowncolorpicker.md)<br/>     | <span data-ttu-id="2fe8f-134">可能會發生一次或多次</span><span class="sxs-lookup"><span data-stu-id="2fe8f-134">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="2fe8f-135">**DropDownGallery**</span><span class="sxs-lookup"><span data-stu-id="2fe8f-135">**DropDownGallery**</span></span>](windowsribbon-element-dropdowngallery.md)<br/>             | <span data-ttu-id="2fe8f-136">可能會發生一次或多次</span><span class="sxs-lookup"><span data-stu-id="2fe8f-136">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="2fe8f-137">**FontControl**</span><span class="sxs-lookup"><span data-stu-id="2fe8f-137">**FontControl**</span></span>](windowsribbon-element-fontcontrol.md)<br/>                     | <span data-ttu-id="2fe8f-138">最多可能發生一次</span><span class="sxs-lookup"><span data-stu-id="2fe8f-138">May occur at most once</span></span><br/> <br/>      |
| [<span data-ttu-id="2fe8f-139">**InRibbonGallery**</span><span class="sxs-lookup"><span data-stu-id="2fe8f-139">**InRibbonGallery**</span></span>](windowsribbon-element-inribbongallery.md)<br/>             | <span data-ttu-id="2fe8f-140">可能會發生一次或多次</span><span class="sxs-lookup"><span data-stu-id="2fe8f-140">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="2fe8f-141">**Spinner**</span><span class="sxs-lookup"><span data-stu-id="2fe8f-141">**Spinner**</span></span>](windowsribbon-element-spinner.md)<br/>                             | <span data-ttu-id="2fe8f-142">可能會發生一次或多次</span><span class="sxs-lookup"><span data-stu-id="2fe8f-142">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="2fe8f-143">**SplitButton**</span><span class="sxs-lookup"><span data-stu-id="2fe8f-143">**SplitButton**</span></span>](windowsribbon-element-splitbutton.md)<br/>                     | <span data-ttu-id="2fe8f-144">可能會發生一次或多次</span><span class="sxs-lookup"><span data-stu-id="2fe8f-144">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="2fe8f-145">**SplitButtonGallery**</span><span class="sxs-lookup"><span data-stu-id="2fe8f-145">**SplitButtonGallery**</span></span>](windowsribbon-element-splitbuttongallery.md)<br/>       | <span data-ttu-id="2fe8f-146">可能會發生一次或多次</span><span class="sxs-lookup"><span data-stu-id="2fe8f-146">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="2fe8f-147">**ToggleButton**</span><span class="sxs-lookup"><span data-stu-id="2fe8f-147">**ToggleButton**</span></span>](windowsribbon-element-togglebutton.md)<br/>                   | <span data-ttu-id="2fe8f-148">可能會發生一次或多次</span><span class="sxs-lookup"><span data-stu-id="2fe8f-148">May occur one or more times</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="2fe8f-149">父元素</span><span class="sxs-lookup"><span data-stu-id="2fe8f-149">Parent elements</span></span>



| <span data-ttu-id="2fe8f-150">元素</span><span class="sxs-lookup"><span data-stu-id="2fe8f-150">Element</span></span>                                                                             |
|-------------------------------------------------------------------------------------|
| <span data-ttu-id="2fe8f-151">**ControlGroup**</span><span class="sxs-lookup"><span data-stu-id="2fe8f-151">**ControlGroup**</span></span><br/>                                                         |
| [<span data-ttu-id="2fe8f-152">**群組**</span><span class="sxs-lookup"><span data-stu-id="2fe8f-152">**Group**</span></span>](windowsribbon-element-group.md)<br/>                             |
| [<span data-ttu-id="2fe8f-153">**GroupSizeDefinition**</span><span class="sxs-lookup"><span data-stu-id="2fe8f-153">**GroupSizeDefinition**</span></span>](windowsribbon-element-groupsizedefinition.md)<br/> |
| [<span data-ttu-id="2fe8f-154">**資料列**</span><span class="sxs-lookup"><span data-stu-id="2fe8f-154">**Row**</span></span>](windowsribbon-element-row.md)<br/>                                 |



## <a name="remarks"></a><span data-ttu-id="2fe8f-155">備註</span><span class="sxs-lookup"><span data-stu-id="2fe8f-155">Remarks</span></span>

<span data-ttu-id="2fe8f-156">選擇性。</span><span class="sxs-lookup"><span data-stu-id="2fe8f-156">Optional.</span></span>

<span data-ttu-id="2fe8f-157">每個 [**群組**](windowsribbon-element-group.md) 或 **ControlGroup** 專案可能會發生一次或多次。</span><span class="sxs-lookup"><span data-stu-id="2fe8f-157">May occur one or more times for each [**Group**](windowsribbon-element-group.md) or **ControlGroup** element.</span></span>

<span data-ttu-id="2fe8f-158">如果未提供任何序號，則會依功能區標記中指定的順序轉譯專案。</span><span class="sxs-lookup"><span data-stu-id="2fe8f-158">If no sequence numbers are supplied, elements are rendered in the order specified in the Ribbon markup.</span></span>

<span data-ttu-id="2fe8f-159">如果 [**Group**](windowsribbon-element-group.md) 或 **ControlGroup** 是父元素，則 **ControlGroup** 會限制為下列可能的子項目： [**Button**](windowsribbon-element-button.md)、 [**CheckBox**](windowsribbon-element-checkbox.md)、 [**ComboBox**](windowsribbon-element-combobox.md)、 [**DropDownButton**](windowsribbon-element-dropdownbutton.md)、 [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md)、 [**DropDownGallery**](windowsribbon-element-dropdowngallery.md)、 [**FontControl**](windowsribbon-element-fontcontrol.md)、 [**InRibbonGallery**](windowsribbon-element-inribbongallery.md)、 [**微調**](windowsribbon-element-spinner.md)、 [**SplitButton**](windowsribbon-element-splitbutton.md)、 [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md)或 [**切換按鈕**](windowsribbon-element-togglebutton.md)</span><span class="sxs-lookup"><span data-stu-id="2fe8f-159">If [**Group**](windowsribbon-element-group.md) or **ControlGroup** is the parent element then **ControlGroup** is constrained to the following possible child elements: [**Button**](windowsribbon-element-button.md), [**CheckBox**](windowsribbon-element-checkbox.md), [**ComboBox**](windowsribbon-element-combobox.md), [**DropDownButton**](windowsribbon-element-dropdownbutton.md), [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md), [**DropDownGallery**](windowsribbon-element-dropdowngallery.md), [**FontControl**](windowsribbon-element-fontcontrol.md), [**InRibbonGallery**](windowsribbon-element-inribbongallery.md), [**Spinner**](windowsribbon-element-spinner.md), [**SplitButton**](windowsribbon-element-splitbutton.md), [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md), or [**ToggleButton**](windowsribbon-element-togglebutton.md)</span></span>

<span data-ttu-id="2fe8f-160">否則，當 [**Row**](windowsribbon-element-row.md) 或 [**GroupSizeDefinition**](windowsribbon-element-groupsizedefinition.md) 是父系時， [**群組**](windowsribbon-element-group.md) 會限制為下列可能的子項目： [**ControlSizeDefinition**](windowsribbon-element-controlsizedefinition.md)。</span><span class="sxs-lookup"><span data-stu-id="2fe8f-160">Otherwise, when [**Row**](windowsribbon-element-row.md) or [**GroupSizeDefinition**](windowsribbon-element-groupsizedefinition.md) is the parent, [**Group**](windowsribbon-element-group.md) is constrained to the following possible child element: [**ControlSizeDefinition**](windowsribbon-element-controlsizedefinition.md).</span></span>

## <a name="examples"></a><span data-ttu-id="2fe8f-161">範例</span><span class="sxs-lookup"><span data-stu-id="2fe8f-161">Examples</span></span>

<span data-ttu-id="2fe8f-162">下列程式碼範例將示範具有各種 [**群組**](windowsribbon-element-group.md)專案之自訂四按鈕 [**SizeDefinition**](windowsribbon-element-sizedefinition.md)版面配置範本的基本標記。</span><span class="sxs-lookup"><span data-stu-id="2fe8f-162">The following code example demonstrates the basic markup for a custom four-button [**SizeDefinition**](windowsribbon-element-sizedefinition.md) layout template with various [**Group**](windowsribbon-element-group.md) elements.</span></span>


```XML
<Group CommandName="cmdButtonGroup2">
  <SizeDefinition>
    <ControlNameMap>
      <ControlNameDefinition Name="button1"/>
      <ControlNameDefinition Name="button2"/>
      <ControlNameDefinition Name="button3"/>
      <ControlNameDefinition Name="button4"/>
    </ControlNameMap>
    <GroupSizeDefinition Size="Large">
      <ControlGroup>
        <ControlSizeDefinition ControlName="button1"
                               ImageSize="Large"
                               IsLabelVisible="true" />
        <ControlSizeDefinition ControlName="button2"
                               ImageSize="Large"
                               IsLabelVisible="true" />
      </ControlGroup>
      <ColumnBreak ShowSeparator="true"/>
      <ControlGroup>
        <ControlSizeDefinition ControlName="button3"
                               ImageSize="Large"
                              IsLabelVisible="true" />
        <ControlSizeDefinition ControlName="button4"
                              ImageSize="Large"
                              IsLabelVisible="true" />
      </ControlGroup>
    </GroupSizeDefinition>
    <GroupSizeDefinition Size="Medium">
      <Row>
        <ControlSizeDefinition ControlName="button1"
                               ImageSize="Small"
                               IsLabelVisible="true" />
        <ControlSizeDefinition ControlName="button3"
                               ImageSize="Small"
                               IsLabelVisible="true" />
      </Row>
      <Row>
        <ControlSizeDefinition ControlName="button2"
                               ImageSize="Small"
                               IsLabelVisible="true" />
        <ControlSizeDefinition ControlName="button4"
                               ImageSize="Small"
                               IsLabelVisible="true" />
      </Row>
    </GroupSizeDefinition>
    <GroupSizeDefinition Size="Small">
      <Row>
        <ControlSizeDefinition ControlName="button1"
                               ImageSize="Small"
                               IsLabelVisible="true" />
        <ControlSizeDefinition ControlName="button3"
                               ImageSize="Small"
                               IsLabelVisible="false" />
      </Row>
      <Row>
        <ControlSizeDefinition ControlName="button2"
                               ImageSize="Small"
                               IsLabelVisible="true" />
        <ControlSizeDefinition ControlName="button4"
                               ImageSize="Small"
                               IsLabelVisible="false" />
      </Row>
    </GroupSizeDefinition>
  </SizeDefinition>
  <Button CommandName="cmdButtonG21"></Button>
  <Button CommandName="cmdButtonG22"></Button>
  <Button CommandName="cmdButtonG23"></Button>
  <Button CommandName="cmdButtonG24"></Button>
</Group>
<Group CommandName="cmdCheckBoxGroup">
  <CheckBox CommandName="cmdCheckBox"></CheckBox>
</Group>
<Group CommandName="cmdToggleButtonGroup"
       SizeDefinition="OneButton">
  <ToggleButton CommandName="cmdToggleButton"></ToggleButton>
</Group>
<Group CommandName="cmdButtonGroup"
       SizeDefinition="ThreeButtons">
  <Button CommandName="cmdButton1"></Button>
  <Button CommandName="cmdButton2"></Button>
  <Button CommandName="cmdButton3"></Button>
</Group>
```



## <a name="element-information"></a><span data-ttu-id="2fe8f-163">項目資訊</span><span class="sxs-lookup"><span data-stu-id="2fe8f-163">Element information</span></span>

* <span data-ttu-id="2fe8f-164">**最低支援系統**： Windows 7</span><span class="sxs-lookup"><span data-stu-id="2fe8f-164">**Minimum supported system**: Windows 7</span></span>
* <span data-ttu-id="2fe8f-165">**可以是空** 的：否</span><span class="sxs-lookup"><span data-stu-id="2fe8f-165">**Can be empty**: No</span></span>



## <a name="see-also"></a><span data-ttu-id="2fe8f-166">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2fe8f-166">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2fe8f-167">透過大小定義和調整原則自訂功能區</span><span class="sxs-lookup"><span data-stu-id="2fe8f-167">Customizing a Ribbon Through Size Definitions and Scaling Policies</span></span>](windowsribbon-templates.md)
</dt> </dl>

 

 





