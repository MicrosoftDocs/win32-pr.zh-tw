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
ms.openlocfilehash: a42b8ffb6d39c1da8993972c0b25995f778bdaca
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/04/2021
ms.locfileid: "111442959"
---
# <a name="dropdownbutton-element"></a><span data-ttu-id="c2e50-104">DropDownButton 元素</span><span class="sxs-lookup"><span data-stu-id="c2e50-104">DropDownButton element</span></span>

<span data-ttu-id="c2e50-105">表示標準 [下拉式按鈕](windowsribbon-controls-dropdownbutton.md) 控制項。</span><span class="sxs-lookup"><span data-stu-id="c2e50-105">Represents a standard [Drop-Down Button](windowsribbon-controls-dropdownbutton.md) control.</span></span>

## <a name="usage"></a><span data-ttu-id="c2e50-106">使用方式</span><span class="sxs-lookup"><span data-stu-id="c2e50-106">Usage</span></span>

``` syntax
<DropDownButton
  ApplicationModes = "xs:string"
  CommandName = "xs:positiveInteger or xs:string">
  child elements
</DropDownButton>
```

## <a name="attributes"></a><span data-ttu-id="c2e50-107">屬性</span><span class="sxs-lookup"><span data-stu-id="c2e50-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c2e50-108">屬性</span><span class="sxs-lookup"><span data-stu-id="c2e50-108">Attribute</span></span></th>
<th><span data-ttu-id="c2e50-109">類型</span><span class="sxs-lookup"><span data-stu-id="c2e50-109">Type</span></span></th>
<th><span data-ttu-id="c2e50-110">必要</span><span class="sxs-lookup"><span data-stu-id="c2e50-110">Required</span></span></th>
<th><span data-ttu-id="c2e50-111">描述</span><span class="sxs-lookup"><span data-stu-id="c2e50-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c2e50-112"><strong>ApplicationModes</strong></span><span class="sxs-lookup"><span data-stu-id="c2e50-112"><strong>ApplicationModes</strong></span></span><br/></td>
<td><span data-ttu-id="c2e50-113">xs:string</span><span class="sxs-lookup"><span data-stu-id="c2e50-113">xs:string</span></span><br/></td>
<td><span data-ttu-id="c2e50-114">否</span><span class="sxs-lookup"><span data-stu-id="c2e50-114">No</span></span><br/></td>
<td><span data-ttu-id="c2e50-115">只有在 <a href="windowsribbon-element-menugroup.md"><strong>MenuGroup</strong></a> 是父元素時才有效。</span><span class="sxs-lookup"><span data-stu-id="c2e50-115">Valid only if <a href="windowsribbon-element-menugroup.md"><strong>MenuGroup</strong></a> is the parent element.</span></span><br/> <br/><span data-ttu-id="c2e50-116">
<dt><span></span><span></span><strong></strong> (xs： string) </span><span class="sxs-lookup"><span data-stu-id="c2e50-116">
<dt><span></span><span></span><strong></strong> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="c2e50-117">字串，其中包含0到31之間的整數清單（以逗號分隔）。</span><span class="sxs-lookup"><span data-stu-id="c2e50-117">A string that contains a comma-separated list of integers between 0 and 31.</span></span><br/> <span data-ttu-id="c2e50-118">空白字元是有效的，而且會被忽略。</span><span class="sxs-lookup"><span data-stu-id="c2e50-118">White space is valid and ignored.</span></span><br/> <span data-ttu-id="c2e50-119">最大長度：250個字元。</span><span class="sxs-lookup"><span data-stu-id="c2e50-119">Maximum length: 250 characters.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c2e50-120"><strong>CommandName</strong></span><span class="sxs-lookup"><span data-stu-id="c2e50-120"><strong>CommandName</strong></span></span><br/></td>
<td><span data-ttu-id="c2e50-121">xs： positiveInteger 或 xs： string</span><span class="sxs-lookup"><span data-stu-id="c2e50-121">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="c2e50-122">否</span><span class="sxs-lookup"><span data-stu-id="c2e50-122">No</span></span><br/></td>
<td><span data-ttu-id="c2e50-123">將元素與 <a href="windowsribbon-element-command.md"><strong>命令</strong></a>產生關聯。</span><span class="sxs-lookup"><span data-stu-id="c2e50-123">Associates the element with a <a href="windowsribbon-element-command.md"><strong>Command</strong></a>.</span></span><br/> <br/><span data-ttu-id="c2e50-124">
<dt><span></span><span></span><strong></strong> (xs： positiveInteger 或 xs： string) </span><span class="sxs-lookup"><span data-stu-id="c2e50-124">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="c2e50-125">字串、介於2與59999（含）之間的整數值，或介於0x2 與0xea5f （含）之間的十六進位值。</span><span class="sxs-lookup"><span data-stu-id="c2e50-125">A string, an integer value between 2 and 59999, inclusive, or a hexadecimal value between 0x2 and 0xea5f, inclusive.</span></span> <br/> <span data-ttu-id="c2e50-126">值在功能區 XML 檔中必須是唯一的。</span><span class="sxs-lookup"><span data-stu-id="c2e50-126">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="c2e50-127">最大長度：100個字元。</span><span class="sxs-lookup"><span data-stu-id="c2e50-127">Maximum length: 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="c2e50-128">子元素</span><span class="sxs-lookup"><span data-stu-id="c2e50-128">Child elements</span></span>



| <span data-ttu-id="c2e50-129">元素</span><span class="sxs-lookup"><span data-stu-id="c2e50-129">Element</span></span>                                                                             | <span data-ttu-id="c2e50-130">描述</span><span class="sxs-lookup"><span data-stu-id="c2e50-130">Description</span></span>                                        |
|-------------------------------------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="c2e50-131">**Button**</span><span class="sxs-lookup"><span data-stu-id="c2e50-131">**Button**</span></span>](windowsribbon-element-button.md)<br/>                           | <span data-ttu-id="c2e50-132">可能會發生一次或多次</span><span class="sxs-lookup"><span data-stu-id="c2e50-132">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="c2e50-133">**相應**</span><span class="sxs-lookup"><span data-stu-id="c2e50-133">**CheckBox**</span></span>](windowsribbon-element-checkbox.md)<br/>                       | <span data-ttu-id="c2e50-134">可能會發生一次或多次</span><span class="sxs-lookup"><span data-stu-id="c2e50-134">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="c2e50-135">**ComboBox**</span><span class="sxs-lookup"><span data-stu-id="c2e50-135">**ComboBox**</span></span>](windowsribbon-element-combobox.md)<br/>                       | <span data-ttu-id="c2e50-136">可能會發生一次或多次</span><span class="sxs-lookup"><span data-stu-id="c2e50-136">May occur one or more times</span></span><br/> <br/> |
| <span data-ttu-id="c2e50-137">**DropDownButton**</span><span class="sxs-lookup"><span data-stu-id="c2e50-137">**DropDownButton**</span></span><br/>                                                       | <span data-ttu-id="c2e50-138">可能會發生一次或多次</span><span class="sxs-lookup"><span data-stu-id="c2e50-138">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="c2e50-139">**DropDownColorPicker**</span><span class="sxs-lookup"><span data-stu-id="c2e50-139">**DropDownColorPicker**</span></span>](windowsribbon-element-dropdowncolorpicker.md)<br/> | <span data-ttu-id="c2e50-140">可能會發生一次或多次</span><span class="sxs-lookup"><span data-stu-id="c2e50-140">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="c2e50-141">**DropDownGallery**</span><span class="sxs-lookup"><span data-stu-id="c2e50-141">**DropDownGallery**</span></span>](windowsribbon-element-dropdowngallery.md)<br/>         | <span data-ttu-id="c2e50-142">可能會發生一次或多次</span><span class="sxs-lookup"><span data-stu-id="c2e50-142">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="c2e50-143">**MenuGroup**</span><span class="sxs-lookup"><span data-stu-id="c2e50-143">**MenuGroup**</span></span>](windowsribbon-element-menugroup.md)<br/>                     | <span data-ttu-id="c2e50-144">至少必須發生一次</span><span class="sxs-lookup"><span data-stu-id="c2e50-144">Must occur at least once</span></span><br/> <br/>    |
| [<span data-ttu-id="c2e50-145">**SplitButton**</span><span class="sxs-lookup"><span data-stu-id="c2e50-145">**SplitButton**</span></span>](windowsribbon-element-splitbutton.md)<br/>                 | <span data-ttu-id="c2e50-146">可能會發生一次或多次</span><span class="sxs-lookup"><span data-stu-id="c2e50-146">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="c2e50-147">**SplitButtonGallery**</span><span class="sxs-lookup"><span data-stu-id="c2e50-147">**SplitButtonGallery**</span></span>](windowsribbon-element-splitbuttongallery.md)<br/>   | <span data-ttu-id="c2e50-148">可能會發生一次或多次</span><span class="sxs-lookup"><span data-stu-id="c2e50-148">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="c2e50-149">**ToggleButton**</span><span class="sxs-lookup"><span data-stu-id="c2e50-149">**ToggleButton**</span></span>](windowsribbon-element-togglebutton.md)<br/>               | <span data-ttu-id="c2e50-150">可能會發生一次或多次</span><span class="sxs-lookup"><span data-stu-id="c2e50-150">May occur one or more times</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="c2e50-151">父元素</span><span class="sxs-lookup"><span data-stu-id="c2e50-151">Parent elements</span></span>



| <span data-ttu-id="c2e50-152">元素</span><span class="sxs-lookup"><span data-stu-id="c2e50-152">Element</span></span>                                                                           |
|-----------------------------------------------------------------------------------|
| [<span data-ttu-id="c2e50-153">**ControlGroup**</span><span class="sxs-lookup"><span data-stu-id="c2e50-153">**ControlGroup**</span></span>](windowsribbon-element-controlgroup.md)<br/>             |
| <span data-ttu-id="c2e50-154">**DropDownButton**</span><span class="sxs-lookup"><span data-stu-id="c2e50-154">**DropDownButton**</span></span><br/>                                                     |
| [<span data-ttu-id="c2e50-155">**DropDownGallery**</span><span class="sxs-lookup"><span data-stu-id="c2e50-155">**DropDownGallery**</span></span>](windowsribbon-element-dropdowngallery.md)<br/>       |
| [<span data-ttu-id="c2e50-156">**群組**</span><span class="sxs-lookup"><span data-stu-id="c2e50-156">**Group**</span></span>](windowsribbon-element-group.md)<br/>                           |
| [<span data-ttu-id="c2e50-157">**MenuGroup**</span><span class="sxs-lookup"><span data-stu-id="c2e50-157">**MenuGroup**</span></span>](windowsribbon-element-menugroup.md)<br/>                   |
| [<span data-ttu-id="c2e50-158">**SplitButton**</span><span class="sxs-lookup"><span data-stu-id="c2e50-158">**SplitButton**</span></span>](windowsribbon-element-splitbutton.md)<br/>               |
| [<span data-ttu-id="c2e50-159">**SplitButtonGallery**</span><span class="sxs-lookup"><span data-stu-id="c2e50-159">**SplitButtonGallery**</span></span>](windowsribbon-element-splitbuttongallery.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="c2e50-160">備註</span><span class="sxs-lookup"><span data-stu-id="c2e50-160">Remarks</span></span>

<span data-ttu-id="c2e50-161">選擇性或必要，視父元素而定。</span><span class="sxs-lookup"><span data-stu-id="c2e50-161">Optional or required, depending on the parent element.</span></span>

<span data-ttu-id="c2e50-162">可能會針對每個 [**ControlGroup**](windowsribbon-element-controlgroup.md)、 **DropDownButton**、 [**DropDownGallery**](windowsribbon-element-dropdowngallery.md)、 [**Group**](windowsribbon-element-group.md)、 [**MenuGroup**](windowsribbon-element-menugroup.md)、 [**SplitButton**](windowsribbon-element-splitbutton.md)或 [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) 元素執行一次或多次。</span><span class="sxs-lookup"><span data-stu-id="c2e50-162">May occur one or more times for each [**ControlGroup**](windowsribbon-element-controlgroup.md), **DropDownButton**, [**DropDownGallery**](windowsribbon-element-dropdowngallery.md), [**Group**](windowsribbon-element-group.md), [**MenuGroup**](windowsribbon-element-menugroup.md), [**SplitButton**](windowsribbon-element-splitbutton.md), or [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) element.</span></span>

<span data-ttu-id="c2e50-163">**DropDownButton** 在應用程式功能表的左邊資料行中裝載時，支援 [應用程式模式](ribbon-applicationmodes.md) 。</span><span class="sxs-lookup"><span data-stu-id="c2e50-163">**DropDownButton** supports [application modes](ribbon-applicationmodes.md) when it is hosted in the left column of the Application Menu.</span></span>

<span data-ttu-id="c2e50-164">當 **DropDownButton** 是 [**ApplicationMenu**](windowsribbon-element-applicationmenu.md)的子系時， [**DropDownGallery**](windowsribbon-element-dropdowngallery.md)和 [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md)不是 **DropDownButton** 的有效子項目。</span><span class="sxs-lookup"><span data-stu-id="c2e50-164">[**DropDownGallery**](windowsribbon-element-dropdowngallery.md) and [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) are not valid child elements of **DropDownButton** when **DropDownButton** is a descendant of [**ApplicationMenu**](windowsribbon-element-applicationmenu.md).</span></span>

## <a name="examples"></a><span data-ttu-id="c2e50-165">範例</span><span class="sxs-lookup"><span data-stu-id="c2e50-165">Examples</span></span>

<span data-ttu-id="c2e50-166">下列範例示範 **DropDownButton** 的基本標記。</span><span class="sxs-lookup"><span data-stu-id="c2e50-166">The following example demonstrates the basic markup for the **DropDownButton**.</span></span>

<span data-ttu-id="c2e50-167">這段程式碼會顯示 **DropDownButton** 命令宣告，以及可作為 **DropDownButton** 元素之父容器的相關聯 [**群組**](windowsribbon-element-group.md)。</span><span class="sxs-lookup"><span data-stu-id="c2e50-167">This section of code shows the **DropDownButton** Command declarations, with an associated [**Group**](windowsribbon-element-group.md) that functions as the parent container for the **DropDownButton** element.</span></span>


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



<span data-ttu-id="c2e50-168">這段程式碼會顯示 **DropDownButton** 控制項宣告。</span><span class="sxs-lookup"><span data-stu-id="c2e50-168">This section of code shows the **DropDownButton** control declarations.</span></span>


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



## <a name="element-information"></a><span data-ttu-id="c2e50-169">項目資訊</span><span class="sxs-lookup"><span data-stu-id="c2e50-169">Element information</span></span>

* <span data-ttu-id="c2e50-170">**最低支援系統**： Windows 7</span><span class="sxs-lookup"><span data-stu-id="c2e50-170">**Minimum supported system**: Windows 7</span></span>
* <span data-ttu-id="c2e50-171">**可以是空** 的：否</span><span class="sxs-lookup"><span data-stu-id="c2e50-171">**Can be empty**: No</span></span>



## <a name="see-also"></a><span data-ttu-id="c2e50-172">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c2e50-172">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c2e50-173">下拉式按鈕控制項</span><span class="sxs-lookup"><span data-stu-id="c2e50-173">Drop-Down Button control</span></span>](windowsribbon-controls-dropdownbutton.md)
</dt> <dt>

[<span data-ttu-id="c2e50-174">**SetModes**</span><span class="sxs-lookup"><span data-stu-id="c2e50-174">**SetModes**</span></span>](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setmodes)
</dt> </dl>

 

