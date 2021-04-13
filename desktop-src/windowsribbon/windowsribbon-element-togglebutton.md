---
title: 切換按鈕元素
description: 代表切換按鈕控制項。
ms.assetid: f26a90e6-9e9a-4fde-8753-50b8b1d09f80
keywords:
- 切換按鈕元素視窗功能區
topic_type:
- apiref
api_name:
- ToggleButton
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 652ea7b535f41cc3dbb40f25bbe49ab4fe52f5ff
ms.sourcegitcommit: 927b9c371f75f52b8011483edf3a4ba37d11ebe4
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/11/2020
ms.locfileid: "104314136"
---
# <a name="togglebutton-element"></a><span data-ttu-id="dc128-104">切換按鈕元素</span><span class="sxs-lookup"><span data-stu-id="dc128-104">ToggleButton element</span></span>

<span data-ttu-id="dc128-105">代表 [切換按鈕](windowsribbon-controls-togglebutton.md) 控制項。</span><span class="sxs-lookup"><span data-stu-id="dc128-105">Represents a [Toggle Button](windowsribbon-controls-togglebutton.md) control.</span></span>

## <a name="usage"></a><span data-ttu-id="dc128-106">使用方式</span><span class="sxs-lookup"><span data-stu-id="dc128-106">Usage</span></span>

``` syntax
<ToggleButton
  CommandName = "xs:positiveInteger or xs:string"
  ApplicationDefaults.IsChecked = "Boolean"/>
```

## <a name="attributes"></a><span data-ttu-id="dc128-107">屬性</span><span class="sxs-lookup"><span data-stu-id="dc128-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="dc128-108">屬性</span><span class="sxs-lookup"><span data-stu-id="dc128-108">Attribute</span></span></th>
<th><span data-ttu-id="dc128-109">類型</span><span class="sxs-lookup"><span data-stu-id="dc128-109">Type</span></span></th>
<th><span data-ttu-id="dc128-110">必要</span><span class="sxs-lookup"><span data-stu-id="dc128-110">Required</span></span></th>
<th><span data-ttu-id="dc128-111">描述</span><span class="sxs-lookup"><span data-stu-id="dc128-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="dc128-112"><strong>S. IsChecked</strong></span><span class="sxs-lookup"><span data-stu-id="dc128-112"><strong>ApplicationDefaults.IsChecked</strong></span></span><br/></td>
<td><span data-ttu-id="dc128-113">Boolean</span><span class="sxs-lookup"><span data-stu-id="dc128-113">Boolean</span></span><br/></td>
<td><span data-ttu-id="dc128-114">No</span><span class="sxs-lookup"><span data-stu-id="dc128-114">No</span></span><br/></td>
<td><span data-ttu-id="dc128-115">只有當 <strong>切換按鈕</strong> 專案是 <a href="windowsribbon-element-quickaccesstoolbar-applicationdefaults.md"><strong>QuickAccessToolbar. s</strong></a>的子系時，這個屬性才有效。</span><span class="sxs-lookup"><span data-stu-id="dc128-115">This attribute is valid only when the <strong>ToggleButton</strong> element is a child of <a href="windowsribbon-element-quickaccesstoolbar-applicationdefaults.md"><strong>QuickAccessToolbar.ApplicationDefaults</strong></a>.</span></span> <br/> <span data-ttu-id="dc128-116">限制為下列其中一個值：</span><span class="sxs-lookup"><span data-stu-id="dc128-116">Restricted to one of the following values:</span></span><br/> <br/><span data-ttu-id="dc128-117">
<dt><span></span><span></span><strong></strong> (true) </span><span class="sxs-lookup"><span data-stu-id="dc128-117">
<dt><span></span><span></span><strong></strong> (true)</span></span><br/> </dt> <dd> <span data-ttu-id="dc128-118">預設值。</span><span class="sxs-lookup"><span data-stu-id="dc128-118">Default.</span></span> <br/> </dd> <span data-ttu-id="dc128-119"><dt><span></span><span></span><strong></strong> (false) </span><span class="sxs-lookup"><span data-stu-id="dc128-119"><dt><span></span><span></span><strong></strong> (false)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dc128-120"><strong>CommandName</strong></span><span class="sxs-lookup"><span data-stu-id="dc128-120"><strong>CommandName</strong></span></span><br/></td>
<td><span data-ttu-id="dc128-121">xs： positiveInteger 或 xs： string</span><span class="sxs-lookup"><span data-stu-id="dc128-121">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="dc128-122">No</span><span class="sxs-lookup"><span data-stu-id="dc128-122">No</span></span><br/></td>
<td><span data-ttu-id="dc128-123">將元素與 <a href="windowsribbon-element-command.md"><strong>命令</strong></a>產生關聯。</span><span class="sxs-lookup"><span data-stu-id="dc128-123">Associates the element with a <a href="windowsribbon-element-command.md"><strong>Command</strong></a>.</span></span><br/> <br/><span data-ttu-id="dc128-124">
<dt><span></span><span></span><strong></strong> (xs： positiveInteger 或 xs： string) </span><span class="sxs-lookup"><span data-stu-id="dc128-124">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="dc128-125">字串、介於2與59999（含）之間的整數值，或介於0x2 與0xea5f （含）之間的十六進位值。</span><span class="sxs-lookup"><span data-stu-id="dc128-125">A string, an integer value between 2 and 59999, inclusive, or a hexadecimal value between 0x2 and 0xea5f, inclusive.</span></span> <br/> <span data-ttu-id="dc128-126">值在功能區 XML 檔中必須是唯一的。</span><span class="sxs-lookup"><span data-stu-id="dc128-126">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="dc128-127">最大長度：100個字元。</span><span class="sxs-lookup"><span data-stu-id="dc128-127">Maximum length: 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="dc128-128">子元素</span><span class="sxs-lookup"><span data-stu-id="dc128-128">Child elements</span></span>

<span data-ttu-id="dc128-129">沒有任何子項目。</span><span class="sxs-lookup"><span data-stu-id="dc128-129">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="dc128-130">父元素</span><span class="sxs-lookup"><span data-stu-id="dc128-130">Parent elements</span></span>



| <span data-ttu-id="dc128-131">元素</span><span class="sxs-lookup"><span data-stu-id="dc128-131">Element</span></span>                                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="dc128-132">**ControlGroup**</span><span class="sxs-lookup"><span data-stu-id="dc128-132">**ControlGroup**</span></span>](windowsribbon-element-controlgroup.md)<br/>                                                     |
| [<span data-ttu-id="dc128-133">**DropDownButton**</span><span class="sxs-lookup"><span data-stu-id="dc128-133">**DropDownButton**</span></span>](windowsribbon-element-dropdownbutton.md)<br/>                                                 |
| [<span data-ttu-id="dc128-134">**DropDownGallery**</span><span class="sxs-lookup"><span data-stu-id="dc128-134">**DropDownGallery**</span></span>](windowsribbon-element-dropdowngallery.md)<br/>                                               |
| [<span data-ttu-id="dc128-135">**Group**</span><span class="sxs-lookup"><span data-stu-id="dc128-135">**Group**</span></span>](windowsribbon-element-group.md)<br/>                                                                   |
| [<span data-ttu-id="dc128-136">**MenuGroup**</span><span class="sxs-lookup"><span data-stu-id="dc128-136">**MenuGroup**</span></span>](windowsribbon-element-menugroup.md)<br/>                                                           |
| [<span data-ttu-id="dc128-137">**QuickAccessToolbar. s**</span><span class="sxs-lookup"><span data-stu-id="dc128-137">**QuickAccessToolbar.ApplicationDefaults**</span></span>](windowsribbon-element-quickaccesstoolbar-applicationdefaults.md)<br/> |
| [<span data-ttu-id="dc128-138">**SplitButton**</span><span class="sxs-lookup"><span data-stu-id="dc128-138">**SplitButton**</span></span>](windowsribbon-element-splitbutton.md)<br/>                                                       |
| [<span data-ttu-id="dc128-139">**SplitButton. ButtonItem**</span><span class="sxs-lookup"><span data-stu-id="dc128-139">**SplitButton.ButtonItem**</span></span>](windowsribbon-element-splitbutton-buttonitem.md)<br/>                                 |
| [<span data-ttu-id="dc128-140">**SplitButtonGallery**</span><span class="sxs-lookup"><span data-stu-id="dc128-140">**SplitButtonGallery**</span></span>](windowsribbon-element-splitbuttongallery.md)<br/>                                         |



## <a name="remarks"></a><span data-ttu-id="dc128-141">備註</span><span class="sxs-lookup"><span data-stu-id="dc128-141">Remarks</span></span>

<span data-ttu-id="dc128-142">選擇性或必要，視父元素而定。</span><span class="sxs-lookup"><span data-stu-id="dc128-142">Optional or required, depending on the parent element.</span></span>

<span data-ttu-id="dc128-143">每個 [**SplitButton. ButtonItem**](windowsribbon-element-splitbutton-buttonitem.md) 元素最多可能會發生一次。</span><span class="sxs-lookup"><span data-stu-id="dc128-143">May occur at most once for each [**SplitButton.ButtonItem**](windowsribbon-element-splitbutton-buttonitem.md) element.</span></span>

<span data-ttu-id="dc128-144">可能會針對每個 [**ControlGroup**](windowsribbon-element-controlgroup.md)、 [**DropDownButton**](windowsribbon-element-dropdownbutton.md)、 [**Group**](windowsribbon-element-group.md)、 [**DropDownGallery**](windowsribbon-element-dropdowngallery.md)、 [**MenuGroup**](windowsribbon-element-menugroup.md)、 [**QuickAccessToolbar**](windowsribbon-element-quickaccesstoolbar-applicationdefaults.md)、s、 [**SplitButton**](windowsribbon-element-splitbutton.md)或 [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) 元素執行一次或多次。</span><span class="sxs-lookup"><span data-stu-id="dc128-144">May occur one or more times for each [**ControlGroup**](windowsribbon-element-controlgroup.md), [**DropDownButton**](windowsribbon-element-dropdownbutton.md), [**Group**](windowsribbon-element-group.md), [**DropDownGallery**](windowsribbon-element-dropdowngallery.md), [**MenuGroup**](windowsribbon-element-menugroup.md), [**QuickAccessToolbar.ApplicationDefaults**](windowsribbon-element-quickaccesstoolbar-applicationdefaults.md), [**SplitButton**](windowsribbon-element-splitbutton.md), or [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) element.</span></span>

## <a name="examples"></a><span data-ttu-id="dc128-145">範例</span><span class="sxs-lookup"><span data-stu-id="dc128-145">Examples</span></span>

<span data-ttu-id="dc128-146">下列範例示範 **切換按鈕** 元素的基本標記。</span><span class="sxs-lookup"><span data-stu-id="dc128-146">The following example demonstrates the basic markup for the **ToggleButton** element.</span></span>

<span data-ttu-id="dc128-147">這段程式碼會顯示 [**QuickAccessToolbar. s**](windowsribbon-element-quickaccesstoolbar-applicationdefaults.md)元素內的 **切換按鈕** 元素宣告。</span><span class="sxs-lookup"><span data-stu-id="dc128-147">This section of code shows a **ToggleButton** element declaration within the [**QuickAccessToolbar.ApplicationDefaults**](windowsribbon-element-quickaccesstoolbar-applicationdefaults.md) element.</span></span>


```XML
      <Ribbon.QuickAccessToolbar>
        <QuickAccessToolbar CommandName="cmdQAT"
                            CustomizeCommandName="cmdCustomizeQAT">
          <QuickAccessToolbar.ApplicationDefaults>
            <Button CommandName="cmdButton1"/>
            <ToggleButton CommandName="cmdMinimize"
                          ApplicationDefaults.IsChecked="false"/>
          </QuickAccessToolbar.ApplicationDefaults>
        </QuickAccessToolbar>
      </Ribbon.QuickAccessToolbar>
```



## <a name="element-information"></a><span data-ttu-id="dc128-148">項目資訊</span><span class="sxs-lookup"><span data-stu-id="dc128-148">Element information</span></span>



|                                     |           |
|-------------------------------------|-----------|
| <span data-ttu-id="dc128-149">最低支援系統</span><span class="sxs-lookup"><span data-stu-id="dc128-149">Minimum supported system</span></span><br/> | <span data-ttu-id="dc128-150">Windows 7</span><span class="sxs-lookup"><span data-stu-id="dc128-150">Windows 7</span></span> |
| <span data-ttu-id="dc128-151">可以是空的</span><span class="sxs-lookup"><span data-stu-id="dc128-151">Can be empty</span></span>                        | <span data-ttu-id="dc128-152">Yes</span><span class="sxs-lookup"><span data-stu-id="dc128-152">Yes</span></span>       |



## <a name="see-also"></a><span data-ttu-id="dc128-153">另請參閱</span><span class="sxs-lookup"><span data-stu-id="dc128-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dc128-154">切換按鈕控制項</span><span class="sxs-lookup"><span data-stu-id="dc128-154">Toggle Button control</span></span>](windowsribbon-controls-togglebutton.md)
</dt> </dl>

 

 





