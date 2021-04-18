---
title: ComboBox 元素
description: 表示下拉式方塊控制項。
ms.assetid: d796e26b-44c2-4e11-b1a5-2ede5bcff676
keywords:
- ComboBox 元素視窗功能區
topic_type:
- apiref
api_name:
- ComboBox
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5bdcc95c64c2bd60df4f2f53d3bd3699c0a7ee65
ms.sourcegitcommit: 927b9c371f75f52b8011483edf3a4ba37d11ebe4
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/11/2020
ms.locfileid: "106967241"
---
# <a name="combobox-element"></a><span data-ttu-id="327c2-104">ComboBox 元素</span><span class="sxs-lookup"><span data-stu-id="327c2-104">ComboBox element</span></span>

<span data-ttu-id="327c2-105">表示 [下拉式列示方塊](windowsribbon-controls-combobox.md) 控制項。</span><span class="sxs-lookup"><span data-stu-id="327c2-105">Represents a [Combo Box](windowsribbon-controls-combobox.md) control.</span></span>

## <a name="usage"></a><span data-ttu-id="327c2-106">使用方式</span><span class="sxs-lookup"><span data-stu-id="327c2-106">Usage</span></span>

``` syntax
<ComboBox
  CommandName = "xs:positiveInteger or xs:string"
  IsEditable = "Boolean"
  ResizeType = "ComboBoxResizeType"
  IsAutoCompleteEnabled = "Boolean"/>
```

## <a name="attributes"></a><span data-ttu-id="327c2-107">屬性</span><span class="sxs-lookup"><span data-stu-id="327c2-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="327c2-108">屬性</span><span class="sxs-lookup"><span data-stu-id="327c2-108">Attribute</span></span></th>
<th><span data-ttu-id="327c2-109">類型</span><span class="sxs-lookup"><span data-stu-id="327c2-109">Type</span></span></th>
<th><span data-ttu-id="327c2-110">必要</span><span class="sxs-lookup"><span data-stu-id="327c2-110">Required</span></span></th>
<th><span data-ttu-id="327c2-111">描述</span><span class="sxs-lookup"><span data-stu-id="327c2-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="327c2-112"><strong>CommandName</strong></span><span class="sxs-lookup"><span data-stu-id="327c2-112"><strong>CommandName</strong></span></span><br/></td>
<td><span data-ttu-id="327c2-113">xs： positiveInteger 或 xs： string</span><span class="sxs-lookup"><span data-stu-id="327c2-113">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="327c2-114">No</span><span class="sxs-lookup"><span data-stu-id="327c2-114">No</span></span><br/></td>
<td><span data-ttu-id="327c2-115">將元素與 <a href="windowsribbon-element-command.md"><strong>命令</strong></a>產生關聯。</span><span class="sxs-lookup"><span data-stu-id="327c2-115">Associates the element with a <a href="windowsribbon-element-command.md"><strong>Command</strong></a>.</span></span><br/> <br/><span data-ttu-id="327c2-116">
<dt><span></span><span></span><strong></strong> (xs： positiveInteger 或 xs： string) </span><span class="sxs-lookup"><span data-stu-id="327c2-116">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="327c2-117">字串、介於2與59999（含）之間的整數值，或介於0x2 與0xea5f （含）之間的十六進位值。</span><span class="sxs-lookup"><span data-stu-id="327c2-117">A string, an integer value between 2 and 59999, inclusive, or a hexadecimal value between 0x2 and 0xea5f, inclusive.</span></span> <br/> <span data-ttu-id="327c2-118">值在功能區 XML 檔中必須是唯一的。</span><span class="sxs-lookup"><span data-stu-id="327c2-118">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="327c2-119">最大長度：100個字元。</span><span class="sxs-lookup"><span data-stu-id="327c2-119">Maximum length: 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="327c2-120"><strong>IsAutoCompleteEnabled</strong></span><span class="sxs-lookup"><span data-stu-id="327c2-120"><strong>IsAutoCompleteEnabled</strong></span></span><br/></td>
<td><span data-ttu-id="327c2-121">Boolean</span><span class="sxs-lookup"><span data-stu-id="327c2-121">Boolean</span></span><br/></td>
<td><span data-ttu-id="327c2-122">No</span><span class="sxs-lookup"><span data-stu-id="327c2-122">No</span></span><br/></td>
<td><span data-ttu-id="327c2-123">限制為下列其中一個值 (0 和1不是有效的) ：</span><span class="sxs-lookup"><span data-stu-id="327c2-123">Restricted to one of the following values (0 and 1 are not valid):</span></span><br/> <br/><span data-ttu-id="327c2-124">
<dt><span></span><span></span><strong></strong> (true) </span><span class="sxs-lookup"><span data-stu-id="327c2-124">
<dt><span></span><span></span><strong></strong> (true)</span></span><br/> </dt> <dd> <span data-ttu-id="327c2-125">預設值。</span><span class="sxs-lookup"><span data-stu-id="327c2-125">Default.</span></span> <br/> </dd> <span data-ttu-id="327c2-126"><dt><span></span><span></span><strong></strong> (false) </span><span class="sxs-lookup"><span data-stu-id="327c2-126"><dt><span></span><span></span><strong></strong> (false)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="327c2-127"><strong>IsEditable</strong></span><span class="sxs-lookup"><span data-stu-id="327c2-127"><strong>IsEditable</strong></span></span><br/></td>
<td><span data-ttu-id="327c2-128">Boolean</span><span class="sxs-lookup"><span data-stu-id="327c2-128">Boolean</span></span><br/></td>
<td><span data-ttu-id="327c2-129">No</span><span class="sxs-lookup"><span data-stu-id="327c2-129">No</span></span><br/></td>
<td><span data-ttu-id="327c2-130">限制為下列其中一個值 (0 和1不是有效的) ：</span><span class="sxs-lookup"><span data-stu-id="327c2-130">Restricted to one of the following values (0 and 1 are not valid):</span></span><br/> <br/><span data-ttu-id="327c2-131">
<dt><span></span><span></span><strong></strong> (true) </span><span class="sxs-lookup"><span data-stu-id="327c2-131">
<dt><span></span><span></span><strong></strong> (true)</span></span><br/> </dt> <dd> <span data-ttu-id="327c2-132">預設值。</span><span class="sxs-lookup"><span data-stu-id="327c2-132">Default.</span></span> <br/> </dd> <span data-ttu-id="327c2-133"><dt><span></span><span></span><strong></strong> (false) </span><span class="sxs-lookup"><span data-stu-id="327c2-133"><dt><span></span><span></span><strong></strong> (false)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="327c2-134"><strong>ResizeType</strong></span><span class="sxs-lookup"><span data-stu-id="327c2-134"><strong>ResizeType</strong></span></span><br/></td>
<td><span data-ttu-id="327c2-135">ComboBoxResizeType</span><span class="sxs-lookup"><span data-stu-id="327c2-135">ComboBoxResizeType</span></span><br/></td>
<td><span data-ttu-id="327c2-136">No</span><span class="sxs-lookup"><span data-stu-id="327c2-136">No</span></span><br/></td>
<td><span data-ttu-id="327c2-137"><dt><span></span><span></span><strong></strong> (NoResize) </span><span class="sxs-lookup"><span data-stu-id="327c2-137"><dt><span></span><span></span><strong></strong> (NoResize)</span></span><br/> </dt> <dd> <span data-ttu-id="327c2-138">預設值。</span><span class="sxs-lookup"><span data-stu-id="327c2-138">Default.</span></span> <br/> </dd> <span data-ttu-id="327c2-139"><dt><span></span><span></span><strong></strong> (VerticalResize) </span><span class="sxs-lookup"><span data-stu-id="327c2-139"><dt><span></span><span></span><strong></strong> (VerticalResize)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="327c2-140">子元素</span><span class="sxs-lookup"><span data-stu-id="327c2-140">Child elements</span></span>

<span data-ttu-id="327c2-141">沒有任何子項目。</span><span class="sxs-lookup"><span data-stu-id="327c2-141">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="327c2-142">父元素</span><span class="sxs-lookup"><span data-stu-id="327c2-142">Parent elements</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="327c2-143">元素</span><span class="sxs-lookup"><span data-stu-id="327c2-143">Element</span></span></th>
<th><span data-ttu-id="327c2-144">描述</span><span class="sxs-lookup"><span data-stu-id="327c2-144">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="327c2-145"><a href="windowsribbon-element-controlgroup.md"><strong>ControlGroup</strong></a></span><span class="sxs-lookup"><span data-stu-id="327c2-145"><a href="windowsribbon-element-controlgroup.md"><strong>ControlGroup</strong></a></span></span><br/></td>

</tr>
<tr class="even">
<td><span data-ttu-id="327c2-146"><a href="windowsribbon-element-dropdownbutton.md"><strong>DropDownButton</strong></a></span><span class="sxs-lookup"><span data-stu-id="327c2-146"><a href="windowsribbon-element-dropdownbutton.md"><strong>DropDownButton</strong></a></span></span><br/></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="327c2-147"><a href="windowsribbon-element-dropdowngallery.md"><strong>DropDownGallery</strong></a></span><span class="sxs-lookup"><span data-stu-id="327c2-147"><a href="windowsribbon-element-dropdowngallery.md"><strong>DropDownGallery</strong></a></span></span><br/></td>

</tr>
<tr class="even">
<td><span data-ttu-id="327c2-148"><a href="windowsribbon-element-group.md"><strong>Group</strong></a></span><span class="sxs-lookup"><span data-stu-id="327c2-148"><a href="windowsribbon-element-group.md"><strong>Group</strong></a></span></span><br/></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="327c2-149"><a href="windowsribbon-element-menugroup.md"><strong>MenuGroup</strong></a></span><span class="sxs-lookup"><span data-stu-id="327c2-149"><a href="windowsribbon-element-menugroup.md"><strong>MenuGroup</strong></a></span></span><br/></td>

</tr>
<tr class="even">
<td><span data-ttu-id="327c2-150"><a href="windowsribbon-element-quickaccesstoolbar-applicationdefaults.md"><strong>QuickAccessToolbar. s</strong></a></span><span class="sxs-lookup"><span data-stu-id="327c2-150"><a href="windowsribbon-element-quickaccesstoolbar-applicationdefaults.md"><strong>QuickAccessToolbar.ApplicationDefaults</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="327c2-151">Windows 8 和更新版本。</span><span class="sxs-lookup"><span data-stu-id="327c2-151">Windows 8 and newer.</span></span>
</blockquote>
<br/> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="327c2-152"><a href="windowsribbon-element-splitbuttongallery.md"><strong>SplitButtonGallery</strong></a></span><span class="sxs-lookup"><span data-stu-id="327c2-152"><a href="windowsribbon-element-splitbuttongallery.md"><strong>SplitButtonGallery</strong></a></span></span><br/></td>

</tr>
</tbody>
</table>



## <a name="remarks"></a><span data-ttu-id="327c2-153">備註</span><span class="sxs-lookup"><span data-stu-id="327c2-153">Remarks</span></span>

<span data-ttu-id="327c2-154">選擇性。</span><span class="sxs-lookup"><span data-stu-id="327c2-154">Optional.</span></span>

<span data-ttu-id="327c2-155">每個 [**ControlGroup**](windowsribbon-element-controlgroup.md)、 [**DropDownButton**](windowsribbon-element-dropdownbutton.md)、 [**DropDownGallery**](windowsribbon-element-dropdowngallery.md)、 [**Group**](windowsribbon-element-group.md)、 [**MenuGroup**](windowsribbon-element-menugroup.md)或 [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) 元素可能會發生一次或多次。</span><span class="sxs-lookup"><span data-stu-id="327c2-155">May occur one or more times for each [**ControlGroup**](windowsribbon-element-controlgroup.md), [**DropDownButton**](windowsribbon-element-dropdownbutton.md), [**DropDownGallery**](windowsribbon-element-dropdowngallery.md), [**Group**](windowsribbon-element-group.md), [**MenuGroup**](windowsribbon-element-menugroup.md), or [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) element.</span></span>

<span data-ttu-id="327c2-156">因為 **ComboBox** 只是一個專案資源庫，所以不支援命令專案。</span><span class="sxs-lookup"><span data-stu-id="327c2-156">Because the **ComboBox** is exclusively an item gallery, it does not support Command items.</span></span> <span data-ttu-id="327c2-157">它也是唯一不支援命令空間的資源庫控制項 (標記中宣告的命令集合，並列在專案庫或命令資源庫) 的底部。</span><span class="sxs-lookup"><span data-stu-id="327c2-157">It is also the only gallery control that does not support a Command Space (a collection of Commands that are declared in markup and listed at the bottom of an item gallery or Command gallery).</span></span> <span data-ttu-id="327c2-158">如需詳細資訊，請參閱 [使用資源庫](ribbon-controls-galleries.md)。</span><span class="sxs-lookup"><span data-stu-id="327c2-158">For more information, see [Working with Galleries](ribbon-controls-galleries.md).</span></span>

<span data-ttu-id="327c2-159">下列螢幕擷取畫面說明 Windows Live Movie Maker 的功能區 [下拉式列示方塊](windowsribbon-controls-combobox.md) 控制項。</span><span class="sxs-lookup"><span data-stu-id="327c2-159">The following screen shot illustrates a Ribbon [Combo Box](windowsribbon-controls-combobox.md) control from Windows Live Movie Maker.</span></span>

![microsoft 油漆功能區中 combobox 控制項的螢幕擷取畫面。](images/controls/combobox.png)

## <a name="examples"></a><span data-ttu-id="327c2-161">範例</span><span class="sxs-lookup"><span data-stu-id="327c2-161">Examples</span></span>

<span data-ttu-id="327c2-162">下列範例示範 **ComboBox** 的基本標記。</span><span class="sxs-lookup"><span data-stu-id="327c2-162">The following examples demonstrate the basic markup for the **ComboBox**.</span></span>

<span data-ttu-id="327c2-163">這一段程式碼會顯示 **combobox** 命令宣告，以及可做為 **ComboBox** 元素父容器的相關聯 [**群組**](windowsribbon-element-group.md)。</span><span class="sxs-lookup"><span data-stu-id="327c2-163">This section of code shows the **ComboBox** Command declarations, with an associated [**Group**](windowsribbon-element-group.md) that acts as the parent container for the **ComboBox** element.</span></span>


```XML
<!-- ComboBox -->
<Command Name="cmdComboBoxGroup"
         Symbol="cmdComboBoxGroup"
         Comment="ComboBox Group"
         LabelTitle="ComboBox"/>
<Command Name="cmdComboBox"
         Symbol="cmdComboBox"
         Comment="ComboBox"
         LabelTitle="ComboBox"/>
```



<span data-ttu-id="327c2-164">這段程式碼會顯示 **ComboBox** 控制項宣告。</span><span class="sxs-lookup"><span data-stu-id="327c2-164">This section of code shows the **ComboBox** control declarations.</span></span>


```XML
<!-- ComboBox -->
<Group CommandName="cmdComboBoxGroup">
  <ComboBox CommandName="cmdComboBox">              
  </ComboBox>
</Group>
```



## <a name="element-information"></a><span data-ttu-id="327c2-165">項目資訊</span><span class="sxs-lookup"><span data-stu-id="327c2-165">Element information</span></span>



|                                     |           |
|-------------------------------------|-----------|
| <span data-ttu-id="327c2-166">最低支援系統</span><span class="sxs-lookup"><span data-stu-id="327c2-166">Minimum supported system</span></span><br/> | <span data-ttu-id="327c2-167">Windows 7</span><span class="sxs-lookup"><span data-stu-id="327c2-167">Windows 7</span></span> |
| <span data-ttu-id="327c2-168">可以是空的</span><span class="sxs-lookup"><span data-stu-id="327c2-168">Can be empty</span></span>                        | <span data-ttu-id="327c2-169">Yes</span><span class="sxs-lookup"><span data-stu-id="327c2-169">Yes</span></span>       |



## <a name="see-also"></a><span data-ttu-id="327c2-170">另請參閱</span><span class="sxs-lookup"><span data-stu-id="327c2-170">See also</span></span>

<dl> <dt>

[<span data-ttu-id="327c2-171">下拉式方塊控制項</span><span class="sxs-lookup"><span data-stu-id="327c2-171">Combo Box control</span></span>](windowsribbon-controls-combobox.md)
</dt> <dt>

[<span data-ttu-id="327c2-172">資源庫範例</span><span class="sxs-lookup"><span data-stu-id="327c2-172">Gallery Sample</span></span>](windowsribbon-gallerysample.md)
</dt> </dl>

 

 





