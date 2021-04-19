---
title: SplitButton 元素
description: 表示標準分割按鈕控制項。
ms.assetid: dece1100-ed04-49a3-a16d-3c5d5e7a2225
keywords:
- SplitButton 元素視窗功能區
topic_type:
- apiref
api_name:
- SplitButton
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3235d58d6499d7d57c54e33e1049f40c50dd189a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106967681"
---
# <a name="splitbutton-element"></a><span data-ttu-id="2986d-104">SplitButton 元素</span><span class="sxs-lookup"><span data-stu-id="2986d-104">SplitButton element</span></span>

<span data-ttu-id="2986d-105">表示標準 [分割按鈕](windowsribbon-controls-splitbutton.md) 控制項。</span><span class="sxs-lookup"><span data-stu-id="2986d-105">Represents a standard [Split Button](windowsribbon-controls-splitbutton.md) control.</span></span>

## <a name="usage"></a><span data-ttu-id="2986d-106">使用方式</span><span class="sxs-lookup"><span data-stu-id="2986d-106">Usage</span></span>

``` syntax
<SplitButton
  ApplicationModes = "xs:string"
  CommandName = "xs:positiveInteger or xs:string">
  child elements
</SplitButton>
```

## <a name="attributes"></a><span data-ttu-id="2986d-107">屬性</span><span class="sxs-lookup"><span data-stu-id="2986d-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="2986d-108">屬性</span><span class="sxs-lookup"><span data-stu-id="2986d-108">Attribute</span></span></th>
<th><span data-ttu-id="2986d-109">類型</span><span class="sxs-lookup"><span data-stu-id="2986d-109">Type</span></span></th>
<th><span data-ttu-id="2986d-110">必要</span><span class="sxs-lookup"><span data-stu-id="2986d-110">Required</span></span></th>
<th><span data-ttu-id="2986d-111">描述</span><span class="sxs-lookup"><span data-stu-id="2986d-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="2986d-112"><strong>ApplicationModes</strong></span><span class="sxs-lookup"><span data-stu-id="2986d-112"><strong>ApplicationModes</strong></span></span><br/></td>
<td><span data-ttu-id="2986d-113">xs:string</span><span class="sxs-lookup"><span data-stu-id="2986d-113">xs:string</span></span><br/></td>
<td><span data-ttu-id="2986d-114">No</span><span class="sxs-lookup"><span data-stu-id="2986d-114">No</span></span><br/></td>
<td><span data-ttu-id="2986d-115">只有在 <a href="windowsribbon-element-menugroup.md"><strong>MenuGroup</strong></a> 是父元素時才有效。</span><span class="sxs-lookup"><span data-stu-id="2986d-115">Valid only if <a href="windowsribbon-element-menugroup.md"><strong>MenuGroup</strong></a> is the parent element.</span></span><br/> <br/><span data-ttu-id="2986d-116">
<dt><span></span><span></span><strong></strong> (xs： string) </span><span class="sxs-lookup"><span data-stu-id="2986d-116">
<dt><span></span><span></span><strong></strong> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="2986d-117">字串，其中包含0到31之間的整數清單（以逗號分隔）。</span><span class="sxs-lookup"><span data-stu-id="2986d-117">A string that contains a comma-separated list of integers between 0 and 31.</span></span><br/> <span data-ttu-id="2986d-118">空白字元是有效的，而且會被忽略。</span><span class="sxs-lookup"><span data-stu-id="2986d-118">White space is valid and ignored.</span></span><br/> <span data-ttu-id="2986d-119">最大長度：250個字元。</span><span class="sxs-lookup"><span data-stu-id="2986d-119">Maximum length: 250 characters.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2986d-120"><strong>CommandName</strong></span><span class="sxs-lookup"><span data-stu-id="2986d-120"><strong>CommandName</strong></span></span><br/></td>
<td><span data-ttu-id="2986d-121">xs： positiveInteger 或 xs： string</span><span class="sxs-lookup"><span data-stu-id="2986d-121">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="2986d-122">No</span><span class="sxs-lookup"><span data-stu-id="2986d-122">No</span></span><br/></td>
<td><span data-ttu-id="2986d-123">將元素與 <a href="windowsribbon-element-command.md"><strong>命令</strong></a>產生關聯。</span><span class="sxs-lookup"><span data-stu-id="2986d-123">Associates the element with a <a href="windowsribbon-element-command.md"><strong>Command</strong></a>.</span></span><br/> <br/><span data-ttu-id="2986d-124">
<dt><span></span><span></span><strong></strong> (xs： positiveInteger 或 xs： string) </span><span class="sxs-lookup"><span data-stu-id="2986d-124">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="2986d-125">字串、介於2與59999（含）之間的整數值，或介於0x2 與0xea5f （含）之間的十六進位值。</span><span class="sxs-lookup"><span data-stu-id="2986d-125">A string, an integer value between 2 and 59999, inclusive, or a hexadecimal value between 0x2 and 0xea5f, inclusive.</span></span> <br/> <span data-ttu-id="2986d-126">值在功能區 XML 檔中必須是唯一的。</span><span class="sxs-lookup"><span data-stu-id="2986d-126">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="2986d-127">最大長度：100個字元。</span><span class="sxs-lookup"><span data-stu-id="2986d-127">Maximum length: 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="2986d-128">子元素</span><span class="sxs-lookup"><span data-stu-id="2986d-128">Child elements</span></span>



| <span data-ttu-id="2986d-129">元素</span><span class="sxs-lookup"><span data-stu-id="2986d-129">Element</span></span>                                                                                   | <span data-ttu-id="2986d-130">描述</span><span class="sxs-lookup"><span data-stu-id="2986d-130">Description</span></span>                                        |
|-------------------------------------------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="2986d-131">**Button**</span><span class="sxs-lookup"><span data-stu-id="2986d-131">**Button**</span></span>](windowsribbon-element-button.md)<br/>                                 | <span data-ttu-id="2986d-132">可能會發生一次或多次</span><span class="sxs-lookup"><span data-stu-id="2986d-132">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="2986d-133">**相應**</span><span class="sxs-lookup"><span data-stu-id="2986d-133">**CheckBox**</span></span>](windowsribbon-element-checkbox.md)<br/>                             | <span data-ttu-id="2986d-134">可能會發生一次或多次</span><span class="sxs-lookup"><span data-stu-id="2986d-134">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="2986d-135">**DropDownButton**</span><span class="sxs-lookup"><span data-stu-id="2986d-135">**DropDownButton**</span></span>](windowsribbon-element-dropdownbutton.md)<br/>                 | <span data-ttu-id="2986d-136">可能會發生一次或多次</span><span class="sxs-lookup"><span data-stu-id="2986d-136">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="2986d-137">**DropDownColorPicker**</span><span class="sxs-lookup"><span data-stu-id="2986d-137">**DropDownColorPicker**</span></span>](windowsribbon-element-dropdowncolorpicker.md)<br/>       | <span data-ttu-id="2986d-138">可能會發生一次或多次</span><span class="sxs-lookup"><span data-stu-id="2986d-138">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="2986d-139">**DropDownGallery**</span><span class="sxs-lookup"><span data-stu-id="2986d-139">**DropDownGallery**</span></span>](windowsribbon-element-dropdowngallery.md)<br/>               | <span data-ttu-id="2986d-140">可能會發生一次或多次</span><span class="sxs-lookup"><span data-stu-id="2986d-140">May occur one or more times</span></span><br/> <br/> |
| <span data-ttu-id="2986d-141">**SplitButton**</span><span class="sxs-lookup"><span data-stu-id="2986d-141">**SplitButton**</span></span><br/>                                                                | <span data-ttu-id="2986d-142">可能會發生一次或多次</span><span class="sxs-lookup"><span data-stu-id="2986d-142">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="2986d-143">**SplitButton. ButtonItem**</span><span class="sxs-lookup"><span data-stu-id="2986d-143">**SplitButton.ButtonItem**</span></span>](windowsribbon-element-splitbutton-buttonitem.md)<br/> | <span data-ttu-id="2986d-144">最多可能發生一次</span><span class="sxs-lookup"><span data-stu-id="2986d-144">May occur at most once</span></span><br/> <br/>      |
| [<span data-ttu-id="2986d-145">**SplitButton. MenuGroups**</span><span class="sxs-lookup"><span data-stu-id="2986d-145">**SplitButton.MenuGroups**</span></span>](windowsribbon-element-splitbutton-menugroups.md)<br/> | <span data-ttu-id="2986d-146">最多可能發生一次</span><span class="sxs-lookup"><span data-stu-id="2986d-146">May occur at most once</span></span><br/> <br/>      |
| [<span data-ttu-id="2986d-147">**SplitButtonGallery**</span><span class="sxs-lookup"><span data-stu-id="2986d-147">**SplitButtonGallery**</span></span>](windowsribbon-element-splitbuttongallery.md)<br/>         | <span data-ttu-id="2986d-148">可能會發生一次或多次</span><span class="sxs-lookup"><span data-stu-id="2986d-148">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="2986d-149">**ToggleButton**</span><span class="sxs-lookup"><span data-stu-id="2986d-149">**ToggleButton**</span></span>](windowsribbon-element-togglebutton.md)<br/>                     | <span data-ttu-id="2986d-150">可能會發生一次或多次</span><span class="sxs-lookup"><span data-stu-id="2986d-150">May occur one or more times</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="2986d-151">父元素</span><span class="sxs-lookup"><span data-stu-id="2986d-151">Parent elements</span></span>



| <span data-ttu-id="2986d-152">元素</span><span class="sxs-lookup"><span data-stu-id="2986d-152">Element</span></span>                                                                           |
|-----------------------------------------------------------------------------------|
| [<span data-ttu-id="2986d-153">**ControlGroup**</span><span class="sxs-lookup"><span data-stu-id="2986d-153">**ControlGroup**</span></span>](windowsribbon-element-controlgroup.md)<br/>             |
| [<span data-ttu-id="2986d-154">**DropDownGallery**</span><span class="sxs-lookup"><span data-stu-id="2986d-154">**DropDownGallery**</span></span>](windowsribbon-element-dropdowngallery.md)<br/>       |
| [<span data-ttu-id="2986d-155">**Group**</span><span class="sxs-lookup"><span data-stu-id="2986d-155">**Group**</span></span>](windowsribbon-element-group.md)<br/>                           |
| [<span data-ttu-id="2986d-156">**MenuGroup**</span><span class="sxs-lookup"><span data-stu-id="2986d-156">**MenuGroup**</span></span>](windowsribbon-element-menugroup.md)<br/>                   |
| <span data-ttu-id="2986d-157">**SplitButton**</span><span class="sxs-lookup"><span data-stu-id="2986d-157">**SplitButton**</span></span><br/>                                                        |
| [<span data-ttu-id="2986d-158">**SplitButtonGallery**</span><span class="sxs-lookup"><span data-stu-id="2986d-158">**SplitButtonGallery**</span></span>](windowsribbon-element-splitbuttongallery.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="2986d-159">備註</span><span class="sxs-lookup"><span data-stu-id="2986d-159">Remarks</span></span>

<span data-ttu-id="2986d-160">選擇性。</span><span class="sxs-lookup"><span data-stu-id="2986d-160">Optional.</span></span>

<span data-ttu-id="2986d-161">可能會針對每個 [**ControlGroup**](windowsribbon-element-controlgroup.md)、 [**DropDownGallery**](windowsribbon-element-dropdowngallery.md)、 [**Group**](windowsribbon-element-group.md)、 [**MenuGroup**](windowsribbon-element-menugroup.md)、 **SplitButton** 或 [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) 元素執行一次或多次。</span><span class="sxs-lookup"><span data-stu-id="2986d-161">May occur one or more times for each [**ControlGroup**](windowsribbon-element-controlgroup.md), [**DropDownGallery**](windowsribbon-element-dropdowngallery.md), [**Group**](windowsribbon-element-group.md), [**MenuGroup**](windowsribbon-element-menugroup.md), **SplitButton**, or [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) element.</span></span>

<span data-ttu-id="2986d-162">**SplitButton** 在應用程式功能表的左邊資料行中裝載時，支援 [應用程式模式](ribbon-applicationmodes.md) 。</span><span class="sxs-lookup"><span data-stu-id="2986d-162">**SplitButton** supports [application modes](ribbon-applicationmodes.md) when it is hosted in the left column of the Application Menu.</span></span>

<span data-ttu-id="2986d-163">當 **DropDownButton** 是 [**ApplicationMenu**](windowsribbon-element-applicationmenu.md)的子系時， [**DropDownGallery**](windowsribbon-element-dropdowngallery.md)和 [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md)不是 [**DropDownButton**](windowsribbon-element-dropdownbutton.md)的有效子項目。</span><span class="sxs-lookup"><span data-stu-id="2986d-163">[**DropDownGallery**](windowsribbon-element-dropdowngallery.md) and [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) are not valid child elements of [**DropDownButton**](windowsribbon-element-dropdownbutton.md) when **DropDownButton** is a descendant of [**ApplicationMenu**](windowsribbon-element-applicationmenu.md).</span></span>

<span data-ttu-id="2986d-164">如果下列專案不是 **SplitButton** 的子項目，則 [**SplitButton MenuGroups**](windowsribbon-element-splitbutton-menugroups.md)必須發生一次：</span><span class="sxs-lookup"><span data-stu-id="2986d-164">[**SplitButton.MenuGroups**](windowsribbon-element-splitbutton-menugroups.md) must occur once if the following are not present as child elements of **SplitButton**:</span></span>

-   [<span data-ttu-id="2986d-165">**按鈕**</span><span class="sxs-lookup"><span data-stu-id="2986d-165">**Button**</span></span>](windowsribbon-element-button.md)
-   [<span data-ttu-id="2986d-166">**相應**</span><span class="sxs-lookup"><span data-stu-id="2986d-166">**CheckBox**</span></span>](windowsribbon-element-checkbox.md)
-   [<span data-ttu-id="2986d-167">**DropDownButton**</span><span class="sxs-lookup"><span data-stu-id="2986d-167">**DropDownButton**</span></span>](windowsribbon-element-dropdownbutton.md)
-   [<span data-ttu-id="2986d-168">**DropDownColorPicker**</span><span class="sxs-lookup"><span data-stu-id="2986d-168">**DropDownColorPicker**</span></span>](windowsribbon-element-dropdowncolorpicker.md)
-   [<span data-ttu-id="2986d-169">**DropDownGallery**</span><span class="sxs-lookup"><span data-stu-id="2986d-169">**DropDownGallery**</span></span>](windowsribbon-element-dropdowngallery.md)
-   <span data-ttu-id="2986d-170">**SplitButton**</span><span class="sxs-lookup"><span data-stu-id="2986d-170">**SplitButton**</span></span>
-   [<span data-ttu-id="2986d-171">**SplitButtonGallery**</span><span class="sxs-lookup"><span data-stu-id="2986d-171">**SplitButtonGallery**</span></span>](windowsribbon-element-splitbuttongallery.md)
-   [<span data-ttu-id="2986d-172">**ToggleButton**</span><span class="sxs-lookup"><span data-stu-id="2986d-172">**ToggleButton**</span></span>](windowsribbon-element-togglebutton.md)

<span data-ttu-id="2986d-173">這些控制項會被視為單一預設 [**SplitButton. MenuGroups**](windowsribbon-element-splitbutton-menugroups.md) 元素的子項目。</span><span class="sxs-lookup"><span data-stu-id="2986d-173">These controls are treated as child elements of a single default [**SplitButton.MenuGroups**](windowsribbon-element-splitbutton-menugroups.md) element.</span></span>

## <a name="examples"></a><span data-ttu-id="2986d-174">範例</span><span class="sxs-lookup"><span data-stu-id="2986d-174">Examples</span></span>

<span data-ttu-id="2986d-175">下列範例示範 [分割按鈕](windowsribbon-controls-splitbutton.md)的基本標記。</span><span class="sxs-lookup"><span data-stu-id="2986d-175">The following example demonstrates the basic markup for the [Split Button](windowsribbon-controls-splitbutton.md).</span></span>

<span data-ttu-id="2986d-176">這段程式碼會顯示 **SplitButton** 命令宣告，以及可作為 **SplitButton** 元素之父容器的相關聯 [**群組**](windowsribbon-element-group.md)。</span><span class="sxs-lookup"><span data-stu-id="2986d-176">This section of code shows the **SplitButton** Command declarations, with an associated [**Group**](windowsribbon-element-group.md) that functions as the parent container for the **SplitButton** element.</span></span>


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



<span data-ttu-id="2986d-177">這段程式碼會顯示 **SplitButton** 控制項宣告。</span><span class="sxs-lookup"><span data-stu-id="2986d-177">This section of code shows the **SplitButton** control declarations.</span></span>


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



## <a name="element-information"></a><span data-ttu-id="2986d-178">項目資訊</span><span class="sxs-lookup"><span data-stu-id="2986d-178">Element information</span></span>



|                                     |           |
|-------------------------------------|-----------|
| <span data-ttu-id="2986d-179">最低支援系統</span><span class="sxs-lookup"><span data-stu-id="2986d-179">Minimum supported system</span></span><br/> | <span data-ttu-id="2986d-180">Windows 7</span><span class="sxs-lookup"><span data-stu-id="2986d-180">Windows 7</span></span> |
| <span data-ttu-id="2986d-181">可以是空的</span><span class="sxs-lookup"><span data-stu-id="2986d-181">Can be empty</span></span>                        | <span data-ttu-id="2986d-182">否</span><span class="sxs-lookup"><span data-stu-id="2986d-182">No</span></span>        |



## <a name="see-also"></a><span data-ttu-id="2986d-183">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2986d-183">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2986d-184">分割按鈕控制項</span><span class="sxs-lookup"><span data-stu-id="2986d-184">Split Button control</span></span>](windowsribbon-controls-splitbutton.md)
</dt> <dt>

[<span data-ttu-id="2986d-185">**SetModes**</span><span class="sxs-lookup"><span data-stu-id="2986d-185">**SetModes**</span></span>](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setmodes)
</dt> </dl>

 

