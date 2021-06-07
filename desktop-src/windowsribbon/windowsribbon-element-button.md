---
title: " (Windows 功能區架構) 的按鈕元素"
description: 表示按鈕控制項。
ms.assetid: a17d4dd8-9b0d-4b4a-93f4-f2a8c008fc58
keywords:
- 按鈕元素視窗功能區
topic_type:
- apiref
api_name:
- Button
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 40236b60a9fe9c72dd35d67fcf7c98bc188938af
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443569"
---
# <a name="button-element"></a><span data-ttu-id="536ea-104">Button 元素</span><span class="sxs-lookup"><span data-stu-id="536ea-104">Button element</span></span>

<span data-ttu-id="536ea-105">表示 [按鈕](windowsribbon-controls-button.md) 控制項。</span><span class="sxs-lookup"><span data-stu-id="536ea-105">Represents a [Button](windowsribbon-controls-button.md) control.</span></span>

## <a name="usage"></a><span data-ttu-id="536ea-106">使用方式</span><span class="sxs-lookup"><span data-stu-id="536ea-106">Usage</span></span>

``` syntax
<Button
  ApplicationModes = "xs:string"
  CommandName = "xs:positiveInteger or xs:string"
  ApplicationDefaults.IsChecked = "Boolean"/>
```

## <a name="attributes"></a><span data-ttu-id="536ea-107">屬性</span><span class="sxs-lookup"><span data-stu-id="536ea-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="536ea-108">屬性</span><span class="sxs-lookup"><span data-stu-id="536ea-108">Attribute</span></span></th>
<th><span data-ttu-id="536ea-109">類型</span><span class="sxs-lookup"><span data-stu-id="536ea-109">Type</span></span></th>
<th><span data-ttu-id="536ea-110">必要</span><span class="sxs-lookup"><span data-stu-id="536ea-110">Required</span></span></th>
<th><span data-ttu-id="536ea-111">描述</span><span class="sxs-lookup"><span data-stu-id="536ea-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="536ea-112"><strong>S. IsChecked</strong></span><span class="sxs-lookup"><span data-stu-id="536ea-112"><strong>ApplicationDefaults.IsChecked</strong></span></span><br/></td>
<td><span data-ttu-id="536ea-113">Boolean</span><span class="sxs-lookup"><span data-stu-id="536ea-113">Boolean</span></span><br/></td>
<td><span data-ttu-id="536ea-114">否</span><span class="sxs-lookup"><span data-stu-id="536ea-114">No</span></span><br/></td>
<td><span data-ttu-id="536ea-115">只有當 <strong>Button</strong> 元素是 <a href="windowsribbon-element-quickaccesstoolbar-applicationdefaults.md"><strong>QuickAccessToolbar. s</strong></a>的子系時，這個屬性才有效。</span><span class="sxs-lookup"><span data-stu-id="536ea-115">This attribute is valid only when the <strong>Button</strong> element is a child of <a href="windowsribbon-element-quickaccesstoolbar-applicationdefaults.md"><strong>QuickAccessToolbar.ApplicationDefaults</strong></a>.</span></span> <br/> <span data-ttu-id="536ea-116">限制為下列其中一個值：</span><span class="sxs-lookup"><span data-stu-id="536ea-116">Restricted to one of the following values:</span></span><br/> <br/><span data-ttu-id="536ea-117">
<dt><span></span><span></span><strong></strong> (true) </span><span class="sxs-lookup"><span data-stu-id="536ea-117">
<dt><span></span><span></span><strong></strong> (true)</span></span><br/> </dt> <dd> <span data-ttu-id="536ea-118">預設值。</span><span class="sxs-lookup"><span data-stu-id="536ea-118">Default.</span></span> <br/> </dd> <span data-ttu-id="536ea-119"><dt><span></span><span></span><strong></strong> (false) </span><span class="sxs-lookup"><span data-stu-id="536ea-119"><dt><span></span><span></span><strong></strong> (false)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="536ea-120"><strong>ApplicationModes</strong></span><span class="sxs-lookup"><span data-stu-id="536ea-120"><strong>ApplicationModes</strong></span></span><br/></td>
<td><span data-ttu-id="536ea-121">xs:string</span><span class="sxs-lookup"><span data-stu-id="536ea-121">xs:string</span></span><br/></td>
<td><span data-ttu-id="536ea-122">否</span><span class="sxs-lookup"><span data-stu-id="536ea-122">No</span></span><br/></td>
<td><span data-ttu-id="536ea-123">只有在 <a href="windowsribbon-element-menugroup.md"><strong>MenuGroup</strong></a> 是父元素時才有效。</span><span class="sxs-lookup"><span data-stu-id="536ea-123">Valid only if <a href="windowsribbon-element-menugroup.md"><strong>MenuGroup</strong></a> is the parent element.</span></span><br/> <br/><span data-ttu-id="536ea-124">
<dt><span></span><span></span><strong></strong> (xs： string) </span><span class="sxs-lookup"><span data-stu-id="536ea-124">
<dt><span></span><span></span><strong></strong> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="536ea-125">字串，其中包含0到31之間的整數清單（以逗號分隔）。</span><span class="sxs-lookup"><span data-stu-id="536ea-125">A string that contains a comma-separated list of integers between 0 and 31.</span></span><br/> <span data-ttu-id="536ea-126">空白字元是有效的，而且會被忽略。</span><span class="sxs-lookup"><span data-stu-id="536ea-126">White space is valid and ignored.</span></span><br/> <span data-ttu-id="536ea-127">最大長度：250個字元。</span><span class="sxs-lookup"><span data-stu-id="536ea-127">Maximum length: 250 characters.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="536ea-128"><strong>CommandName</strong></span><span class="sxs-lookup"><span data-stu-id="536ea-128"><strong>CommandName</strong></span></span><br/></td>
<td><span data-ttu-id="536ea-129">xs： positiveInteger 或 xs： string</span><span class="sxs-lookup"><span data-stu-id="536ea-129">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="536ea-130">否</span><span class="sxs-lookup"><span data-stu-id="536ea-130">No</span></span><br/></td>
<td><span data-ttu-id="536ea-131">將元素與 <a href="windowsribbon-element-command.md"><strong>命令</strong></a>產生關聯。</span><span class="sxs-lookup"><span data-stu-id="536ea-131">Associates the element with a <a href="windowsribbon-element-command.md"><strong>Command</strong></a>.</span></span><br/> <br/><span data-ttu-id="536ea-132">
<dt><span></span><span></span><strong></strong> (xs： positiveInteger 或 xs： string) </span><span class="sxs-lookup"><span data-stu-id="536ea-132">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="536ea-133">字串、介於2與59999（含）之間的整數值，或介於0x2 與0xea5f （含）之間的十六進位值。</span><span class="sxs-lookup"><span data-stu-id="536ea-133">A string, an integer value between 2 and 59999, inclusive, or a hexadecimal value between 0x2 and 0xea5f, inclusive.</span></span> <br/> <span data-ttu-id="536ea-134">值在功能區 XML 檔中必須是唯一的。</span><span class="sxs-lookup"><span data-stu-id="536ea-134">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="536ea-135">最大長度：100個字元。</span><span class="sxs-lookup"><span data-stu-id="536ea-135">Maximum length: 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="536ea-136">子元素</span><span class="sxs-lookup"><span data-stu-id="536ea-136">Child elements</span></span>

<span data-ttu-id="536ea-137">沒有任何子項目。</span><span class="sxs-lookup"><span data-stu-id="536ea-137">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="536ea-138">父元素</span><span class="sxs-lookup"><span data-stu-id="536ea-138">Parent elements</span></span>



| <span data-ttu-id="536ea-139">元素</span><span class="sxs-lookup"><span data-stu-id="536ea-139">Element</span></span>                                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="536ea-140">**ControlGroup**</span><span class="sxs-lookup"><span data-stu-id="536ea-140">**ControlGroup**</span></span>](windowsribbon-element-controlgroup.md)<br/>                                                     |
| [<span data-ttu-id="536ea-141">**DropDownButton**</span><span class="sxs-lookup"><span data-stu-id="536ea-141">**DropDownButton**</span></span>](windowsribbon-element-dropdownbutton.md)<br/>                                                 |
| [<span data-ttu-id="536ea-142">**DropDownGallery**</span><span class="sxs-lookup"><span data-stu-id="536ea-142">**DropDownGallery**</span></span>](windowsribbon-element-dropdowngallery.md)<br/>                                               |
| [<span data-ttu-id="536ea-143">**群組**</span><span class="sxs-lookup"><span data-stu-id="536ea-143">**Group**</span></span>](windowsribbon-element-group.md)<br/>                                                                   |
| [<span data-ttu-id="536ea-144">**MenuGroup**</span><span class="sxs-lookup"><span data-stu-id="536ea-144">**MenuGroup**</span></span>](windowsribbon-element-menugroup.md)<br/>                                                           |
| [<span data-ttu-id="536ea-145">**QuickAccessToolbar. s**</span><span class="sxs-lookup"><span data-stu-id="536ea-145">**QuickAccessToolbar.ApplicationDefaults**</span></span>](windowsribbon-element-quickaccesstoolbar-applicationdefaults.md)<br/> |
| [<span data-ttu-id="536ea-146">**SplitButton**</span><span class="sxs-lookup"><span data-stu-id="536ea-146">**SplitButton**</span></span>](windowsribbon-element-splitbutton.md)<br/>                                                       |
| [<span data-ttu-id="536ea-147">**SplitButton. ButtonItem**</span><span class="sxs-lookup"><span data-stu-id="536ea-147">**SplitButton.ButtonItem**</span></span>](windowsribbon-element-splitbutton-buttonitem.md)<br/>                                 |
| [<span data-ttu-id="536ea-148">**SplitButtonGallery**</span><span class="sxs-lookup"><span data-stu-id="536ea-148">**SplitButtonGallery**</span></span>](windowsribbon-element-splitbuttongallery.md)<br/>                                         |



## <a name="remarks"></a><span data-ttu-id="536ea-149">備註</span><span class="sxs-lookup"><span data-stu-id="536ea-149">Remarks</span></span>

<span data-ttu-id="536ea-150">選擇性。</span><span class="sxs-lookup"><span data-stu-id="536ea-150">Optional.</span></span>

<span data-ttu-id="536ea-151">每個 [**SplitButton. ButtonItem**](windowsribbon-element-splitbutton-buttonitem.md) 元素最多可能會發生一次。</span><span class="sxs-lookup"><span data-stu-id="536ea-151">May occur at most once for each [**SplitButton.ButtonItem**](windowsribbon-element-splitbutton-buttonitem.md) element.</span></span>

<span data-ttu-id="536ea-152">可能會針對每個 [**ControlGroup**](windowsribbon-element-controlgroup.md)、 [**DropDownButton**](windowsribbon-element-dropdownbutton.md)、 [**DropDownGallery**](windowsribbon-element-dropdowngallery.md)、 [**Group**](windowsribbon-element-group.md)、 [**MenuGroup**](windowsribbon-element-menugroup.md)、 [**QuickAccessToolbar**](windowsribbon-element-quickaccesstoolbar-applicationdefaults.md)、s、 [**SplitButton**](windowsribbon-element-splitbutton.md)或 [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) 元素執行一次或多次。</span><span class="sxs-lookup"><span data-stu-id="536ea-152">May occur one or more times for each [**ControlGroup**](windowsribbon-element-controlgroup.md), [**DropDownButton**](windowsribbon-element-dropdownbutton.md), [**DropDownGallery**](windowsribbon-element-dropdowngallery.md), [**Group**](windowsribbon-element-group.md), [**MenuGroup**](windowsribbon-element-menugroup.md), [**QuickAccessToolbar.ApplicationDefaults**](windowsribbon-element-quickaccesstoolbar-applicationdefaults.md), [**SplitButton**](windowsribbon-element-splitbutton.md), or [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) element.</span></span>

<span data-ttu-id="536ea-153">**按鈕** 會在應用程式功能表的左邊資料行中裝載時，支援 [應用程式模式](ribbon-applicationmodes.md) 。</span><span class="sxs-lookup"><span data-stu-id="536ea-153">**Button** supports [application modes](ribbon-applicationmodes.md) when it is hosted in the left column of the Application Menu.</span></span>

## <a name="examples"></a><span data-ttu-id="536ea-154">範例</span><span class="sxs-lookup"><span data-stu-id="536ea-154">Examples</span></span>

<span data-ttu-id="536ea-155">下列範例示範 **按鈕** 的基本標記。</span><span class="sxs-lookup"><span data-stu-id="536ea-155">The following example demonstrates the basic markup for the **Button**.</span></span>

<span data-ttu-id="536ea-156">這段程式碼會顯示 **按鈕** 命令宣告，以及可做為 **Button** 元素父容器的相關聯 [**群組**](windowsribbon-element-group.md)。</span><span class="sxs-lookup"><span data-stu-id="536ea-156">This section of code shows the **Button** Command declarations, with an associated [**Group**](windowsribbon-element-group.md) that acts as the parent container for the **Button** element.</span></span>


```XML
<!-- Button -->
<Command Name="cmdButtonGroup"
         Symbol="cmdButtonGroup"
         Comment="Button Group"
         LabelTitle="ButtonGroup"/>
<Command Name="cmdButton1"
         Symbol="cmdButton1"
         Comment="Button1"
         LabelTitle="Button1"/>
<Command Name="cmdButton2"
         Symbol="cmdButton2"
         Comment="Button2"
         LabelTitle="Button2"/>
<Command Name="cmdButton3"
         Symbol="cmdButton3"
         Comment="Button3"
         LabelTitle="Button3"/>
<Command Name="cmdButtonGroup2"
         Symbol="cmdButtonGroup2"
         Comment="Button Group2"
         LabelTitle="ButtonGroup2"/>
<Command Name="cmdButtonG21"
         Symbol="cmdButtonG21"
         Comment="ButtonG21"
         LabelTitle="ButtonG21">
  <Command.LargeImages>
    <Image Source="res/large.bmp"/>
  </Command.LargeImages>
  <Command.SmallImages>
    <Image Source="res/small.bmp"/>
  </Command.SmallImages>
</Command>
<Command Name="cmdButtonG22"
         Symbol="cmdButtonG22"
         Comment="ButtonG22"
         LabelTitle="ButtonG22">
  <Command.LargeImages>
    <Image Source="res/large.bmp"/>
  </Command.LargeImages>
  <Command.SmallImages>
    <Image Source="res/small.bmp"/>
  </Command.SmallImages>
</Command>
<Command Name="cmdButtonG23"
         Symbol="cmdButtonG23"
         Comment="ButtonG23"
         LabelTitle="ButtonG23">
  <Command.LargeImages>
    <Image Source="res/large.bmp"/>
  </Command.LargeImages>
  <Command.SmallImages>
    <Image Source="res/small.bmp"/>
  </Command.SmallImages>
</Command>
<Command Name="cmdButtonG24"
         Symbol="cmdButtonG24"
         Comment="ButtonG24"
         LabelTitle="ButtonG24">
  <Command.LargeImages>
    <Image Source="res/large.bmp"/>
  </Command.LargeImages>
  <Command.SmallImages>
    <Image Source="res/small.bmp"/>
  </Command.SmallImages>
</Command>
```



<span data-ttu-id="536ea-157">這段程式碼會顯示 **按鈕** 控制項宣告。</span><span class="sxs-lookup"><span data-stu-id="536ea-157">This section of code shows the **Button** control declarations.</span></span>


```XML
<Group CommandName="cmdButtonGroup"
       SizeDefinition="ThreeButtons">
  <Button CommandName="cmdButton1"></Button>
  <Button CommandName="cmdButton2"></Button>
  <Button CommandName="cmdButton3"></Button>
</Group>
```



## <a name="element-information"></a><span data-ttu-id="536ea-158">項目資訊</span><span class="sxs-lookup"><span data-stu-id="536ea-158">Element information</span></span>

* <span data-ttu-id="536ea-159">**最低支援系統**： Windows 7</span><span class="sxs-lookup"><span data-stu-id="536ea-159">**Minimum supported system**: Windows 7</span></span>
* <span data-ttu-id="536ea-160">**可以是空** 的：是</span><span class="sxs-lookup"><span data-stu-id="536ea-160">**Can be empty**: Yes</span></span>



## <a name="see-also"></a><span data-ttu-id="536ea-161">另請參閱</span><span class="sxs-lookup"><span data-stu-id="536ea-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="536ea-162">Button 控制項</span><span class="sxs-lookup"><span data-stu-id="536ea-162">Button control</span></span>](windowsribbon-controls-button.md)
</dt> <dt>

[<span data-ttu-id="536ea-163">**SetModes**</span><span class="sxs-lookup"><span data-stu-id="536ea-163">**SetModes**</span></span>](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setmodes)
</dt> </dl>

 

