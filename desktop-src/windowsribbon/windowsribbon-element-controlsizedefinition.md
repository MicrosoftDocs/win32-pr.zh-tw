---
title: ControlSizeDefinition 元素
description: 表示自訂範本中控制項群組的版面配置樣式。
ms.assetid: f9b875f4-e0cf-4823-81b5-ed19c201dcbb
keywords:
- ControlSizeDefinition 元素視窗功能區
topic_type:
- apiref
api_name:
- ControlSizeDefinition
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e35fe159bf5bafa1ebfa6119215a4265ee900ef0
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "104312662"
---
# <a name="controlsizedefinition-element"></a><span data-ttu-id="3259c-104">ControlSizeDefinition 元素</span><span class="sxs-lookup"><span data-stu-id="3259c-104">ControlSizeDefinition element</span></span>

<span data-ttu-id="3259c-105">表示自訂範本中控制項群組的版面配置樣式。</span><span class="sxs-lookup"><span data-stu-id="3259c-105">Represents the layout style of a group of controls in a custom template.</span></span>

## <a name="usage"></a><span data-ttu-id="3259c-106">使用方式</span><span class="sxs-lookup"><span data-stu-id="3259c-106">Usage</span></span>

``` syntax
<ControlSizeDefinition
  ImageSize = "xs:string"
  IsLabelVisible = "Boolean"
  IsImageVisible = "Boolean"
  IsPopup = "Boolean"
  ControlName = "xs:positiveInteger or xs:string"/>
```

## <a name="attributes"></a><span data-ttu-id="3259c-107">屬性</span><span class="sxs-lookup"><span data-stu-id="3259c-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="3259c-108">屬性</span><span class="sxs-lookup"><span data-stu-id="3259c-108">Attribute</span></span></th>
<th><span data-ttu-id="3259c-109">類型</span><span class="sxs-lookup"><span data-stu-id="3259c-109">Type</span></span></th>
<th><span data-ttu-id="3259c-110">必要</span><span class="sxs-lookup"><span data-stu-id="3259c-110">Required</span></span></th>
<th><span data-ttu-id="3259c-111">描述</span><span class="sxs-lookup"><span data-stu-id="3259c-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="3259c-112"><strong>Controlnameinrow</strong></span><span class="sxs-lookup"><span data-stu-id="3259c-112"><strong>ControlName</strong></span></span><br/></td>
<td><span data-ttu-id="3259c-113">xs： positiveInteger 或 xs： string</span><span class="sxs-lookup"><span data-stu-id="3259c-113">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="3259c-114">No</span><span class="sxs-lookup"><span data-stu-id="3259c-114">No</span></span><br/></td>
<td><span data-ttu-id="3259c-115"><dt><span></span><span></span><strong></strong> (xs： positiveInteger 或 xs： string) </span><span class="sxs-lookup"><span data-stu-id="3259c-115"><dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="3259c-116">字串、介於2與59999（含）之間的整數值，或介於0x2 與0xea5f （含）之間的十六進位值。</span><span class="sxs-lookup"><span data-stu-id="3259c-116">A string, an integer value between 2 and 59999, inclusive, or a hexadecimal value between 0x2 and 0xea5f, inclusive.</span></span> <br/> <span data-ttu-id="3259c-117">值在功能區 XML 檔中必須是唯一的。</span><span class="sxs-lookup"><span data-stu-id="3259c-117">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="3259c-118">最大長度：100個字元。</span><span class="sxs-lookup"><span data-stu-id="3259c-118">Maximum length: 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3259c-119"><strong>ImageSize</strong></span><span class="sxs-lookup"><span data-stu-id="3259c-119"><strong>ImageSize</strong></span></span><br/></td>
<td><span data-ttu-id="3259c-120">xs:string</span><span class="sxs-lookup"><span data-stu-id="3259c-120">xs:string</span></span><br/></td>
<td><span data-ttu-id="3259c-121">No</span><span class="sxs-lookup"><span data-stu-id="3259c-121">No</span></span><br/></td>
<td><span data-ttu-id="3259c-122">限制為下列其中一個值：</span><span class="sxs-lookup"><span data-stu-id="3259c-122">Restricted to one of the following values:</span></span><br/> <br/><span data-ttu-id="3259c-123">
<dt><span></span><span></span><strong></strong> (大型) </span><span class="sxs-lookup"><span data-stu-id="3259c-123">
<dt><span></span><span></span><strong></strong> (Large)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="3259c-124"><dt><span></span><span></span><strong></strong> (Small) </span><span class="sxs-lookup"><span data-stu-id="3259c-124"><dt><span></span><span></span><strong></strong> (Small)</span></span><br/> </dt> <dd> <span data-ttu-id="3259c-125">預設值。</span><span class="sxs-lookup"><span data-stu-id="3259c-125">Default.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3259c-126"><strong>IsImageVisible</strong></span><span class="sxs-lookup"><span data-stu-id="3259c-126"><strong>IsImageVisible</strong></span></span><br/></td>
<td><span data-ttu-id="3259c-127">Boolean</span><span class="sxs-lookup"><span data-stu-id="3259c-127">Boolean</span></span><br/></td>
<td><span data-ttu-id="3259c-128">No</span><span class="sxs-lookup"><span data-stu-id="3259c-128">No</span></span><br/></td>
<td><span data-ttu-id="3259c-129">限制為下列其中一個值 (0 和1不是有效的) ：</span><span class="sxs-lookup"><span data-stu-id="3259c-129">Restricted to one of the following values (0 and 1 are not valid):</span></span><br/> <br/><span data-ttu-id="3259c-130">
<dt><span></span><span></span><strong></strong> (true) </span><span class="sxs-lookup"><span data-stu-id="3259c-130">
<dt><span></span><span></span><strong></strong> (true)</span></span><br/> </dt> <dd> <span data-ttu-id="3259c-131">預設值。</span><span class="sxs-lookup"><span data-stu-id="3259c-131">Default.</span></span> <br/> </dd> <span data-ttu-id="3259c-132"><dt><span></span><span></span><strong></strong> (false) </span><span class="sxs-lookup"><span data-stu-id="3259c-132"><dt><span></span><span></span><strong></strong> (false)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3259c-133"><strong>IsLabelVisible</strong></span><span class="sxs-lookup"><span data-stu-id="3259c-133"><strong>IsLabelVisible</strong></span></span><br/></td>
<td><span data-ttu-id="3259c-134">Boolean</span><span class="sxs-lookup"><span data-stu-id="3259c-134">Boolean</span></span><br/></td>
<td><span data-ttu-id="3259c-135">No</span><span class="sxs-lookup"><span data-stu-id="3259c-135">No</span></span><br/></td>
<td><span data-ttu-id="3259c-136">限制為下列其中一個值 (0 和1不是有效的) ：</span><span class="sxs-lookup"><span data-stu-id="3259c-136">Restricted to one of the following values (0 and 1 are not valid):</span></span><br/> <br/><span data-ttu-id="3259c-137">
<dt><span></span><span></span><strong></strong> (true) </span><span class="sxs-lookup"><span data-stu-id="3259c-137">
<dt><span></span><span></span><strong></strong> (true)</span></span><br/> </dt> <dd> <span data-ttu-id="3259c-138">預設值。</span><span class="sxs-lookup"><span data-stu-id="3259c-138">Default.</span></span> <br/> </dd> <span data-ttu-id="3259c-139"><dt><span></span><span></span><strong></strong> (false) </span><span class="sxs-lookup"><span data-stu-id="3259c-139"><dt><span></span><span></span><strong></strong> (false)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3259c-140"><strong>IsPopup</strong></span><span class="sxs-lookup"><span data-stu-id="3259c-140"><strong>IsPopup</strong></span></span><br/></td>
<td><span data-ttu-id="3259c-141">Boolean</span><span class="sxs-lookup"><span data-stu-id="3259c-141">Boolean</span></span><br/></td>
<td><span data-ttu-id="3259c-142">No</span><span class="sxs-lookup"><span data-stu-id="3259c-142">No</span></span><br/></td>
<td><span data-ttu-id="3259c-143">限制為下列其中一個值 (0 和1不是有效的) ：</span><span class="sxs-lookup"><span data-stu-id="3259c-143">Restricted to one of the following values (0 and 1 are not valid):</span></span><br/> <br/><span data-ttu-id="3259c-144">
<dt><span></span><span></span><strong></strong> (true) </span><span class="sxs-lookup"><span data-stu-id="3259c-144">
<dt><span></span><span></span><strong></strong> (true)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="3259c-145"><dt><span></span><span></span><strong></strong> (false) </span><span class="sxs-lookup"><span data-stu-id="3259c-145"><dt><span></span><span></span><strong></strong> (false)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="3259c-146">子元素</span><span class="sxs-lookup"><span data-stu-id="3259c-146">Child elements</span></span>

<span data-ttu-id="3259c-147">沒有任何子項目。</span><span class="sxs-lookup"><span data-stu-id="3259c-147">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="3259c-148">父元素</span><span class="sxs-lookup"><span data-stu-id="3259c-148">Parent elements</span></span>



| <span data-ttu-id="3259c-149">元素</span><span class="sxs-lookup"><span data-stu-id="3259c-149">Element</span></span>                                                                             |
|-------------------------------------------------------------------------------------|
| [<span data-ttu-id="3259c-150">**ControlGroup**</span><span class="sxs-lookup"><span data-stu-id="3259c-150">**ControlGroup**</span></span>](windowsribbon-element-controlgroup.md)<br/>               |
| [<span data-ttu-id="3259c-151">**GroupSizeDefinition**</span><span class="sxs-lookup"><span data-stu-id="3259c-151">**GroupSizeDefinition**</span></span>](windowsribbon-element-groupsizedefinition.md)<br/> |
| [<span data-ttu-id="3259c-152">**資料列**</span><span class="sxs-lookup"><span data-stu-id="3259c-152">**Row**</span></span>](windowsribbon-element-row.md)<br/>                                 |



## <a name="remarks"></a><span data-ttu-id="3259c-153">備註</span><span class="sxs-lookup"><span data-stu-id="3259c-153">Remarks</span></span>

<span data-ttu-id="3259c-154">選擇性。</span><span class="sxs-lookup"><span data-stu-id="3259c-154">Optional.</span></span>

<span data-ttu-id="3259c-155">每個 [**ControlGroup**](windowsribbon-element-controlgroup.md)、 [**Row**](windowsribbon-element-row.md)或 [**SizeDefinition**](windowsribbon-element-sizedefinition.md) 元素可能會發生一次或多次。</span><span class="sxs-lookup"><span data-stu-id="3259c-155">May occur one or more times for each [**ControlGroup**](windowsribbon-element-controlgroup.md), [**Row**](windowsribbon-element-row.md), or [**SizeDefinition**](windowsribbon-element-sizedefinition.md) element.</span></span>

## <a name="examples"></a><span data-ttu-id="3259c-156">範例</span><span class="sxs-lookup"><span data-stu-id="3259c-156">Examples</span></span>

<span data-ttu-id="3259c-157">下列程式碼範例示範具有各種 **ControlSizeDefinition** 元素之自訂四個按鈕 [**SizeDefinition**](windowsribbon-element-sizedefinition.md)版面配置範本的基本標記。</span><span class="sxs-lookup"><span data-stu-id="3259c-157">The following code example demonstrates the basic markup for a custom four-button [**SizeDefinition**](windowsribbon-element-sizedefinition.md) layout template with various **ControlSizeDefinition** elements.</span></span>


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



## <a name="element-information"></a><span data-ttu-id="3259c-158">項目資訊</span><span class="sxs-lookup"><span data-stu-id="3259c-158">Element information</span></span>



|                                     |           |
|-------------------------------------|-----------|
| <span data-ttu-id="3259c-159">最低支援系統</span><span class="sxs-lookup"><span data-stu-id="3259c-159">Minimum supported system</span></span><br/> | <span data-ttu-id="3259c-160">Windows 7</span><span class="sxs-lookup"><span data-stu-id="3259c-160">Windows 7</span></span> |
| <span data-ttu-id="3259c-161">可以是空的</span><span class="sxs-lookup"><span data-stu-id="3259c-161">Can be empty</span></span>                        | <span data-ttu-id="3259c-162">Yes</span><span class="sxs-lookup"><span data-stu-id="3259c-162">Yes</span></span>       |



## <a name="see-also"></a><span data-ttu-id="3259c-163">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3259c-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3259c-164">透過大小定義和調整原則自訂功能區</span><span class="sxs-lookup"><span data-stu-id="3259c-164">Customizing a Ribbon Through Size Definitions and Scaling Policies</span></span>](windowsribbon-templates.md)
</dt> </dl>

 

 





