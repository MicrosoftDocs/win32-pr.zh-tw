---
title: CheckBox 元素
description: 表示核取方塊控制項。
ms.assetid: ebb44d6d-91fb-4a59-9b62-4a694fea8a4d
keywords:
- CheckBox 元素視窗功能區
topic_type:
- apiref
api_name:
- CheckBox
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0af090058e0475f1997c681750009a12f4e5e7cd
ms.sourcegitcommit: 927b9c371f75f52b8011483edf3a4ba37d11ebe4
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/11/2020
ms.locfileid: "104092524"
---
# <a name="checkbox-element"></a><span data-ttu-id="df858-104">CheckBox 元素</span><span class="sxs-lookup"><span data-stu-id="df858-104">CheckBox element</span></span>

<span data-ttu-id="df858-105">表示 [核取方塊](windowsribbon-controls-checkbox.md) 控制項。</span><span class="sxs-lookup"><span data-stu-id="df858-105">Represents a [Check Box](windowsribbon-controls-checkbox.md) control.</span></span>

## <a name="usage"></a><span data-ttu-id="df858-106">使用方式</span><span class="sxs-lookup"><span data-stu-id="df858-106">Usage</span></span>

``` syntax
<CheckBox
  CommandName = "xs:positiveInteger or xs:string"
  ApplicationDefaults.IsChecked = "Boolean"/>
```

## <a name="attributes"></a><span data-ttu-id="df858-107">屬性</span><span class="sxs-lookup"><span data-stu-id="df858-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="df858-108">屬性</span><span class="sxs-lookup"><span data-stu-id="df858-108">Attribute</span></span></th>
<th><span data-ttu-id="df858-109">類型</span><span class="sxs-lookup"><span data-stu-id="df858-109">Type</span></span></th>
<th><span data-ttu-id="df858-110">必要</span><span class="sxs-lookup"><span data-stu-id="df858-110">Required</span></span></th>
<th><span data-ttu-id="df858-111">描述</span><span class="sxs-lookup"><span data-stu-id="df858-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="df858-112"><strong>S. IsChecked</strong></span><span class="sxs-lookup"><span data-stu-id="df858-112"><strong>ApplicationDefaults.IsChecked</strong></span></span><br/></td>
<td><span data-ttu-id="df858-113">Boolean</span><span class="sxs-lookup"><span data-stu-id="df858-113">Boolean</span></span><br/></td>
<td><span data-ttu-id="df858-114">No</span><span class="sxs-lookup"><span data-stu-id="df858-114">No</span></span><br/></td>
<td><span data-ttu-id="df858-115">只有當 <strong>CheckBox</strong> 元素是 <a href="windowsribbon-element-quickaccesstoolbar-applicationdefaults.md"><strong>QuickAccessToolbar. s</strong></a>的子系時，這個屬性才有效。</span><span class="sxs-lookup"><span data-stu-id="df858-115">This attribute is valid only when the <strong>CheckBox</strong> element is a child of <a href="windowsribbon-element-quickaccesstoolbar-applicationdefaults.md"><strong>QuickAccessToolbar.ApplicationDefaults</strong></a>.</span></span> <br/> <span data-ttu-id="df858-116">限制為下列其中一個值：</span><span class="sxs-lookup"><span data-stu-id="df858-116">Restricted to one of the following values:</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="df858-117">此 <strong>核取方塊</strong> 不支援第三個或不定的狀態。</span><span class="sxs-lookup"><span data-stu-id="df858-117">The <strong>CheckBox</strong> does not support a tertiary, or indeterminate, state.</span></span>
</blockquote>
<br/> <br/><span data-ttu-id="df858-118">
<dt><span></span><span></span><strong></strong> (true) </span><span class="sxs-lookup"><span data-stu-id="df858-118">
<dt><span></span><span></span><strong></strong> (true)</span></span><br/> </dt> <dd> <span data-ttu-id="df858-119">預設值。</span><span class="sxs-lookup"><span data-stu-id="df858-119">Default.</span></span> <br/> </dd> <span data-ttu-id="df858-120"><dt><span></span><span></span><strong></strong> (false) </span><span class="sxs-lookup"><span data-stu-id="df858-120"><dt><span></span><span></span><strong></strong> (false)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="df858-121"><strong>CommandName</strong></span><span class="sxs-lookup"><span data-stu-id="df858-121"><strong>CommandName</strong></span></span><br/></td>
<td><span data-ttu-id="df858-122">xs： positiveInteger 或 xs： string</span><span class="sxs-lookup"><span data-stu-id="df858-122">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="df858-123">No</span><span class="sxs-lookup"><span data-stu-id="df858-123">No</span></span><br/></td>
<td><span data-ttu-id="df858-124">將元素與 <a href="windowsribbon-element-command.md"><strong>命令</strong></a>產生關聯。</span><span class="sxs-lookup"><span data-stu-id="df858-124">Associates the element with a <a href="windowsribbon-element-command.md"><strong>Command</strong></a>.</span></span><br/> <br/><span data-ttu-id="df858-125">
<dt><span></span><span></span><strong></strong> (xs： positiveInteger 或 xs： string) </span><span class="sxs-lookup"><span data-stu-id="df858-125">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="df858-126">字串、介於2與59999（含）之間的整數值，或介於0x2 與0xea5f （含）之間的十六進位值。</span><span class="sxs-lookup"><span data-stu-id="df858-126">A string, an integer value between 2 and 59999, inclusive, or a hexadecimal value between 0x2 and 0xea5f, inclusive.</span></span> <br/> <span data-ttu-id="df858-127">值在功能區 XML 檔中必須是唯一的。</span><span class="sxs-lookup"><span data-stu-id="df858-127">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="df858-128">最大長度：100個字元。</span><span class="sxs-lookup"><span data-stu-id="df858-128">Maximum length: 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="df858-129">子元素</span><span class="sxs-lookup"><span data-stu-id="df858-129">Child elements</span></span>

<span data-ttu-id="df858-130">沒有任何子項目。</span><span class="sxs-lookup"><span data-stu-id="df858-130">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="df858-131">父元素</span><span class="sxs-lookup"><span data-stu-id="df858-131">Parent elements</span></span>



| <span data-ttu-id="df858-132">元素</span><span class="sxs-lookup"><span data-stu-id="df858-132">Element</span></span>                                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="df858-133">**ControlGroup**</span><span class="sxs-lookup"><span data-stu-id="df858-133">**ControlGroup**</span></span>](windowsribbon-element-controlgroup.md)<br/>                                                     |
| [<span data-ttu-id="df858-134">**DropDownButton**</span><span class="sxs-lookup"><span data-stu-id="df858-134">**DropDownButton**</span></span>](windowsribbon-element-dropdownbutton.md)<br/>                                                 |
| [<span data-ttu-id="df858-135">**DropDownGallery**</span><span class="sxs-lookup"><span data-stu-id="df858-135">**DropDownGallery**</span></span>](windowsribbon-element-dropdowngallery.md)<br/>                                               |
| [<span data-ttu-id="df858-136">**Group**</span><span class="sxs-lookup"><span data-stu-id="df858-136">**Group**</span></span>](windowsribbon-element-group.md)<br/>                                                                   |
| [<span data-ttu-id="df858-137">**MenuGroup**</span><span class="sxs-lookup"><span data-stu-id="df858-137">**MenuGroup**</span></span>](windowsribbon-element-menugroup.md)<br/>                                                           |
| [<span data-ttu-id="df858-138">**QuickAccessToolbar. s**</span><span class="sxs-lookup"><span data-stu-id="df858-138">**QuickAccessToolbar.ApplicationDefaults**</span></span>](windowsribbon-element-quickaccesstoolbar-applicationdefaults.md)<br/> |
| [<span data-ttu-id="df858-139">**SplitButton**</span><span class="sxs-lookup"><span data-stu-id="df858-139">**SplitButton**</span></span>](windowsribbon-element-splitbutton.md)<br/>                                                       |
| [<span data-ttu-id="df858-140">**SplitButtonGallery**</span><span class="sxs-lookup"><span data-stu-id="df858-140">**SplitButtonGallery**</span></span>](windowsribbon-element-splitbuttongallery.md)<br/>                                         |



## <a name="remarks"></a><span data-ttu-id="df858-141">備註</span><span class="sxs-lookup"><span data-stu-id="df858-141">Remarks</span></span>

<span data-ttu-id="df858-142">選擇性或必要，視父元素而定。</span><span class="sxs-lookup"><span data-stu-id="df858-142">Optional or required, depending on the parent element.</span></span>

<span data-ttu-id="df858-143">可能會針對每個 [**ControlGroup**](windowsribbon-element-controlgroup.md)、 [**DropDownButton**](windowsribbon-element-dropdownbutton.md)、 [**DropDownGallery**](windowsribbon-element-dropdowngallery.md)、 [**Group**](windowsribbon-element-group.md)、 [**MenuGroup**](windowsribbon-element-menugroup.md)、 [**QuickAccessToolbar**](windowsribbon-element-quickaccesstoolbar-applicationdefaults.md)、s、 [**SplitButton**](windowsribbon-element-splitbutton.md)或 [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) 元素執行一次或多次。</span><span class="sxs-lookup"><span data-stu-id="df858-143">May occur one or more times for each [**ControlGroup**](windowsribbon-element-controlgroup.md), [**DropDownButton**](windowsribbon-element-dropdownbutton.md), [**DropDownGallery**](windowsribbon-element-dropdowngallery.md), [**Group**](windowsribbon-element-group.md), [**MenuGroup**](windowsribbon-element-menugroup.md), [**QuickAccessToolbar.ApplicationDefaults**](windowsribbon-element-quickaccesstoolbar-applicationdefaults.md), [**SplitButton**](windowsribbon-element-splitbutton.md), or [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) element.</span></span>

## <a name="examples"></a><span data-ttu-id="df858-144">範例</span><span class="sxs-lookup"><span data-stu-id="df858-144">Examples</span></span>

<span data-ttu-id="df858-145">下列範例示範 **CheckBox** 元素的基本標記。</span><span class="sxs-lookup"><span data-stu-id="df858-145">The following example demonstrates the basic markup for the **CheckBox** element.</span></span>

<span data-ttu-id="df858-146">這一節的程式碼會顯示 **核取方塊** 命令聲明。</span><span class="sxs-lookup"><span data-stu-id="df858-146">This section of code shows the **CheckBox** Command declarations.</span></span>


```XML
<Command Name="cmdCheckBoxGroup"
         Symbol="cmdCheckBoxGroup"
         Comment="CheckBox Group"
         LabelTitle="CheckBoxGroup"/>
<Command Name="cmdCheckBox"
         Symbol="cmdCheckBox"
         Comment="CheckBox"
         LabelTitle="CheckBox"/>
```



<span data-ttu-id="df858-147">這段程式碼會顯示 **CheckBox** 控制項宣告。</span><span class="sxs-lookup"><span data-stu-id="df858-147">This section of code shows the **CheckBox** control declarations.</span></span>


```XML
<Group CommandName="cmdCheckBoxGroup">
  <CheckBox CommandName="cmdCheckBox"></CheckBox>
</Group>
```



## <a name="element-information"></a><span data-ttu-id="df858-148">項目資訊</span><span class="sxs-lookup"><span data-stu-id="df858-148">Element information</span></span>



|                                     |           |
|-------------------------------------|-----------|
| <span data-ttu-id="df858-149">最低支援系統</span><span class="sxs-lookup"><span data-stu-id="df858-149">Minimum supported system</span></span><br/> | <span data-ttu-id="df858-150">Windows 7</span><span class="sxs-lookup"><span data-stu-id="df858-150">Windows 7</span></span> |
| <span data-ttu-id="df858-151">可以是空的</span><span class="sxs-lookup"><span data-stu-id="df858-151">Can be empty</span></span>                        | <span data-ttu-id="df858-152">Yes</span><span class="sxs-lookup"><span data-stu-id="df858-152">Yes</span></span>       |



## <a name="see-also"></a><span data-ttu-id="df858-153">另請參閱</span><span class="sxs-lookup"><span data-stu-id="df858-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="df858-154">核取方塊控制項</span><span class="sxs-lookup"><span data-stu-id="df858-154">Check Box control</span></span>](windowsribbon-controls-checkbox.md)
</dt> </dl>

 

 





