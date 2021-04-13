---
title: Group 元素
description: 代表做為元素群組之容器的群組控制項。
ms.assetid: b0d3fcda-7165-40f4-9e57-c7ab88b31711
keywords:
- 群組元素視窗功能區
topic_type:
- apiref
api_name:
- Group
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3a42e9efb30397862037426041420d96be8fd387
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104375965"
---
# <a name="group-element"></a><span data-ttu-id="87015-104">Group 元素</span><span class="sxs-lookup"><span data-stu-id="87015-104">Group element</span></span>

<span data-ttu-id="87015-105">代表做為元素群組之容器的 [群組](windowsribbon-controls-group.md) 控制項。</span><span class="sxs-lookup"><span data-stu-id="87015-105">Represents a [Group](windowsribbon-controls-group.md) control that functions as a container for a group of elements.</span></span>

## <a name="usage"></a><span data-ttu-id="87015-106">使用方式</span><span class="sxs-lookup"><span data-stu-id="87015-106">Usage</span></span>

``` syntax
<Group
  SizeDefinition = "xs:string"
  ApplicationModes = "xs:string"
  CommandName = "xs:positiveInteger or xs:string">
  child elements
</Group>
```

## <a name="attributes"></a><span data-ttu-id="87015-107">屬性</span><span class="sxs-lookup"><span data-stu-id="87015-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="87015-108">屬性</span><span class="sxs-lookup"><span data-stu-id="87015-108">Attribute</span></span></th>
<th><span data-ttu-id="87015-109">類型</span><span class="sxs-lookup"><span data-stu-id="87015-109">Type</span></span></th>
<th><span data-ttu-id="87015-110">必要</span><span class="sxs-lookup"><span data-stu-id="87015-110">Required</span></span></th>
<th><span data-ttu-id="87015-111">描述</span><span class="sxs-lookup"><span data-stu-id="87015-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="87015-112"><strong>ApplicationModes</strong></span><span class="sxs-lookup"><span data-stu-id="87015-112"><strong>ApplicationModes</strong></span></span><br/></td>
<td><span data-ttu-id="87015-113">xs:string</span><span class="sxs-lookup"><span data-stu-id="87015-113">xs:string</span></span><br/></td>
<td><span data-ttu-id="87015-114">No</span><span class="sxs-lookup"><span data-stu-id="87015-114">No</span></span><br/></td>
<td><span data-ttu-id="87015-115"><dt><span></span><span></span><strong></strong> (xs： string) </span><span class="sxs-lookup"><span data-stu-id="87015-115"><dt><span></span><span></span><strong></strong> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="87015-116">字串，其中包含0到31之間的整數清單（以逗號分隔）。</span><span class="sxs-lookup"><span data-stu-id="87015-116">A string that contains a comma-separated list of integers between 0 and 31.</span></span><br/> <span data-ttu-id="87015-117">空白字元是有效的，而且會被忽略。</span><span class="sxs-lookup"><span data-stu-id="87015-117">White space is valid and ignored.</span></span><br/> <span data-ttu-id="87015-118">最大長度：250個字元。</span><span class="sxs-lookup"><span data-stu-id="87015-118">Maximum length: 250 characters.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="87015-119"><strong>CommandName</strong></span><span class="sxs-lookup"><span data-stu-id="87015-119"><strong>CommandName</strong></span></span><br/></td>
<td><span data-ttu-id="87015-120">xs： positiveInteger 或 xs： string</span><span class="sxs-lookup"><span data-stu-id="87015-120">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="87015-121">No</span><span class="sxs-lookup"><span data-stu-id="87015-121">No</span></span><br/></td>
<td><span data-ttu-id="87015-122">將元素與 <a href="windowsribbon-element-command.md"><strong>命令</strong></a>產生關聯。</span><span class="sxs-lookup"><span data-stu-id="87015-122">Associates the element with a <a href="windowsribbon-element-command.md"><strong>Command</strong></a>.</span></span><br/> <br/><span data-ttu-id="87015-123">
<dt><span></span><span></span><strong></strong> (xs： positiveInteger 或 xs： string) </span><span class="sxs-lookup"><span data-stu-id="87015-123">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="87015-124">字串、介於2與59999（含）之間的整數值，或介於0x2 與0xea5f （含）之間的十六進位值。</span><span class="sxs-lookup"><span data-stu-id="87015-124">A string, an integer value between 2 and 59999, inclusive, or a hexadecimal value between 0x2 and 0xea5f, inclusive.</span></span> <br/> <span data-ttu-id="87015-125">值在功能區 XML 檔中必須是唯一的。</span><span class="sxs-lookup"><span data-stu-id="87015-125">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="87015-126">最大長度：100個字元。</span><span class="sxs-lookup"><span data-stu-id="87015-126">Maximum length: 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="87015-127"><strong>SizeDefinition</strong></span><span class="sxs-lookup"><span data-stu-id="87015-127"><strong>SizeDefinition</strong></span></span><br/></td>
<td><span data-ttu-id="87015-128">xs:string</span><span class="sxs-lookup"><span data-stu-id="87015-128">xs:string</span></span><br/></td>
<td><span data-ttu-id="87015-129">No</span><span class="sxs-lookup"><span data-stu-id="87015-129">No</span></span><br/></td>
<td><span data-ttu-id="87015-130">當指定時， <em>SizeDefinition</em> 的值會限制為功能區架構所定義的其中一個 <a href="windowsribbon-templates.md">版面配置範本</a> 。</span><span class="sxs-lookup"><span data-stu-id="87015-130">When specified, the value of <em>SizeDefinition</em> is constrained to one of the <a href="windowsribbon-templates.md">layout templates</a> defined by the Ribbon framework.</span></span> <br/> <br/><span data-ttu-id="87015-131">
<dt><span></span><span></span><strong></strong> (xs： string) </span><span class="sxs-lookup"><span data-stu-id="87015-131">
<dt><span></span><span></span><strong></strong> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="87015-132">任何零或多個字元的序列。</span><span class="sxs-lookup"><span data-stu-id="87015-132">Any sequence of zero or more characters.</span></span><br/> <span data-ttu-id="87015-133">長度上限為未系結。</span><span class="sxs-lookup"><span data-stu-id="87015-133">The maximum length is unbounded.</span></span><br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="87015-134">子元素</span><span class="sxs-lookup"><span data-stu-id="87015-134">Child elements</span></span>



| <span data-ttu-id="87015-135">元素</span><span class="sxs-lookup"><span data-stu-id="87015-135">Element</span></span>                                                                             | <span data-ttu-id="87015-136">描述</span><span class="sxs-lookup"><span data-stu-id="87015-136">Description</span></span>                                        |
|-------------------------------------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="87015-137">**Button**</span><span class="sxs-lookup"><span data-stu-id="87015-137">**Button**</span></span>](windowsribbon-element-button.md)<br/>                           | <span data-ttu-id="87015-138">可能會發生一次或多次</span><span class="sxs-lookup"><span data-stu-id="87015-138">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="87015-139">**相應**</span><span class="sxs-lookup"><span data-stu-id="87015-139">**CheckBox**</span></span>](windowsribbon-element-checkbox.md)<br/>                       | <span data-ttu-id="87015-140">可能會發生一次或多次</span><span class="sxs-lookup"><span data-stu-id="87015-140">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="87015-141">**ComboBox**</span><span class="sxs-lookup"><span data-stu-id="87015-141">**ComboBox**</span></span>](windowsribbon-element-combobox.md)<br/>                       | <span data-ttu-id="87015-142">可能會發生一次或多次</span><span class="sxs-lookup"><span data-stu-id="87015-142">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="87015-143">**ControlGroup**</span><span class="sxs-lookup"><span data-stu-id="87015-143">**ControlGroup**</span></span>](windowsribbon-element-controlgroup.md)<br/>               | <span data-ttu-id="87015-144">可能會發生一次或多次</span><span class="sxs-lookup"><span data-stu-id="87015-144">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="87015-145">**DropDownButton**</span><span class="sxs-lookup"><span data-stu-id="87015-145">**DropDownButton**</span></span>](windowsribbon-element-dropdownbutton.md)<br/>           | <span data-ttu-id="87015-146">可能會發生一次或多次</span><span class="sxs-lookup"><span data-stu-id="87015-146">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="87015-147">**DropDownColorPicker**</span><span class="sxs-lookup"><span data-stu-id="87015-147">**DropDownColorPicker**</span></span>](windowsribbon-element-dropdowncolorpicker.md)<br/> | <span data-ttu-id="87015-148">可能會發生一次或多次</span><span class="sxs-lookup"><span data-stu-id="87015-148">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="87015-149">**DropDownGallery**</span><span class="sxs-lookup"><span data-stu-id="87015-149">**DropDownGallery**</span></span>](windowsribbon-element-dropdowngallery.md)<br/>         | <span data-ttu-id="87015-150">可能會發生一次或多次</span><span class="sxs-lookup"><span data-stu-id="87015-150">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="87015-151">**FontControl**</span><span class="sxs-lookup"><span data-stu-id="87015-151">**FontControl**</span></span>](windowsribbon-element-fontcontrol.md)<br/>                 | <span data-ttu-id="87015-152">最多可能發生一次</span><span class="sxs-lookup"><span data-stu-id="87015-152">May occur at most once</span></span><br/> <br/>      |
| [<span data-ttu-id="87015-153">**InRibbonGallery**</span><span class="sxs-lookup"><span data-stu-id="87015-153">**InRibbonGallery**</span></span>](windowsribbon-element-inribbongallery.md)<br/>         | <span data-ttu-id="87015-154">可能會發生一次或多次</span><span class="sxs-lookup"><span data-stu-id="87015-154">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="87015-155">**SizeDefinition**</span><span class="sxs-lookup"><span data-stu-id="87015-155">**SizeDefinition**</span></span>](windowsribbon-element-sizedefinition.md)<br/>           | <span data-ttu-id="87015-156">最多可能發生一次</span><span class="sxs-lookup"><span data-stu-id="87015-156">May occur at most once</span></span><br/> <br/>      |
| [<span data-ttu-id="87015-157">**Spinner**</span><span class="sxs-lookup"><span data-stu-id="87015-157">**Spinner**</span></span>](windowsribbon-element-spinner.md)<br/>                         | <span data-ttu-id="87015-158">可能會發生一次或多次</span><span class="sxs-lookup"><span data-stu-id="87015-158">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="87015-159">**SplitButton**</span><span class="sxs-lookup"><span data-stu-id="87015-159">**SplitButton**</span></span>](windowsribbon-element-splitbutton.md)<br/>                 | <span data-ttu-id="87015-160">可能會發生一次或多次</span><span class="sxs-lookup"><span data-stu-id="87015-160">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="87015-161">**SplitButtonGallery**</span><span class="sxs-lookup"><span data-stu-id="87015-161">**SplitButtonGallery**</span></span>](windowsribbon-element-splitbuttongallery.md)<br/>   | <span data-ttu-id="87015-162">可能會發生一次或多次</span><span class="sxs-lookup"><span data-stu-id="87015-162">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="87015-163">**ToggleButton**</span><span class="sxs-lookup"><span data-stu-id="87015-163">**ToggleButton**</span></span>](windowsribbon-element-togglebutton.md)<br/>               | <span data-ttu-id="87015-164">可能會發生一次或多次</span><span class="sxs-lookup"><span data-stu-id="87015-164">May occur one or more times</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="87015-165">父元素</span><span class="sxs-lookup"><span data-stu-id="87015-165">Parent elements</span></span>



| <span data-ttu-id="87015-166">元素</span><span class="sxs-lookup"><span data-stu-id="87015-166">Element</span></span>                                             |
|-----------------------------------------------------|
| [<span data-ttu-id="87015-167">**索引標籤**</span><span class="sxs-lookup"><span data-stu-id="87015-167">**Tab**</span></span>](windowsribbon-element-tab.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="87015-168">備註</span><span class="sxs-lookup"><span data-stu-id="87015-168">Remarks</span></span>

<span data-ttu-id="87015-169">選擇性。</span><span class="sxs-lookup"><span data-stu-id="87015-169">Optional.</span></span>

<span data-ttu-id="87015-170">每個索引標籤元素可能會 [**發生一次**](windowsribbon-element-tab.md) 或多次。</span><span class="sxs-lookup"><span data-stu-id="87015-170">May occur one or more times for each [**Tab**](windowsribbon-element-tab.md) element.</span></span>

<span data-ttu-id="87015-171">[**Tab**](windowsribbon-element-tab.md) 支援 [應用程式模式](ribbon-applicationmodes.md)。</span><span class="sxs-lookup"><span data-stu-id="87015-171">[**Tab**](windowsribbon-element-tab.md) supports [application modes](ribbon-applicationmodes.md).</span></span>

<span data-ttu-id="87015-172">只有當 **群組** 的子項目對應到針對 *SizeDefinition* 指定的範本時，功能區標記才有效。</span><span class="sxs-lookup"><span data-stu-id="87015-172">The Ribbon markup is valid only when the child elements of **Group** correspond to the template specified for *SizeDefinition*.</span></span>

## <a name="examples"></a><span data-ttu-id="87015-173">範例</span><span class="sxs-lookup"><span data-stu-id="87015-173">Examples</span></span>

<span data-ttu-id="87015-174">下列程式碼範例說明如何在 **群組** 中使用自訂範本。</span><span class="sxs-lookup"><span data-stu-id="87015-174">The following code example illustrates the use of a custom template in a **Group**.</span></span>


```
<Group CommandName="cmdCustomGroup1" SizeDefinition="CustomTemplate">
  <Button CommandName="cmdCommand1" />
</Group>
```



## <a name="element-information"></a><span data-ttu-id="87015-175">項目資訊</span><span class="sxs-lookup"><span data-stu-id="87015-175">Element information</span></span>



|                                     |           |
|-------------------------------------|-----------|
| <span data-ttu-id="87015-176">最低支援系統</span><span class="sxs-lookup"><span data-stu-id="87015-176">Minimum supported system</span></span><br/> | <span data-ttu-id="87015-177">Windows 7</span><span class="sxs-lookup"><span data-stu-id="87015-177">Windows 7</span></span> |
| <span data-ttu-id="87015-178">可以是空的</span><span class="sxs-lookup"><span data-stu-id="87015-178">Can be empty</span></span>                        | <span data-ttu-id="87015-179">否</span><span class="sxs-lookup"><span data-stu-id="87015-179">No</span></span>        |



## <a name="see-also"></a><span data-ttu-id="87015-180">另請參閱</span><span class="sxs-lookup"><span data-stu-id="87015-180">See also</span></span>

<dl> <dt>

[<span data-ttu-id="87015-181">透過大小定義和調整原則自訂功能區</span><span class="sxs-lookup"><span data-stu-id="87015-181">Customizing a Ribbon Through Size Definitions and Scaling Policies</span></span>](windowsribbon-templates.md)
</dt> <dt>

[<span data-ttu-id="87015-182">群組控制項</span><span class="sxs-lookup"><span data-stu-id="87015-182">Group control</span></span>](windowsribbon-controls-group.md)
</dt> <dt>

[<span data-ttu-id="87015-183">**SetModes**</span><span class="sxs-lookup"><span data-stu-id="87015-183">**SetModes**</span></span>](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setmodes)
</dt> </dl>

 

