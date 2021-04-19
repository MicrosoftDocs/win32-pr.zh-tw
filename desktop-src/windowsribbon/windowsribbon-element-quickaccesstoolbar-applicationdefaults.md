---
title: QuickAccessToolbar. s 屬性
description: 代表快速存取工具列 (QAT) 中預設命令的容器。
ms.assetid: 8f44d7c0-1a39-4a88-ae01-7d7d1bb6bf7e
keywords:
- QuickAccessToolbar. s 屬性 Windows 功能區
topic_type:
- apiref
api_name:
- QuickAccessToolbar.ApplicationDefaults
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 084ea334441cb0cf545adaa3d1016f7d02da1b88
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106995161"
---
# <a name="quickaccesstoolbarapplicationdefaults-property"></a><span data-ttu-id="c1288-104">QuickAccessToolbar. s 屬性</span><span class="sxs-lookup"><span data-stu-id="c1288-104">QuickAccessToolbar.ApplicationDefaults property</span></span>

<span data-ttu-id="c1288-105">代表 [快速存取工具列 (QAT) ](windowsribbon-controls-quickaccesstoolbar.md)中預設命令的容器。</span><span class="sxs-lookup"><span data-stu-id="c1288-105">Represents a container for default Commands in the [Quick Access Toolbar (QAT)](windowsribbon-controls-quickaccesstoolbar.md).</span></span>

## <a name="usage"></a><span data-ttu-id="c1288-106">使用方式</span><span class="sxs-lookup"><span data-stu-id="c1288-106">Usage</span></span>

``` syntax
<QuickAccessToolbar.ApplicationDefaults>
  child elements
</QuickAccessToolbar.ApplicationDefaults>
```

## <a name="attributes"></a><span data-ttu-id="c1288-107">屬性</span><span class="sxs-lookup"><span data-stu-id="c1288-107">Attributes</span></span>

<span data-ttu-id="c1288-108">沒有任何屬性。</span><span class="sxs-lookup"><span data-stu-id="c1288-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="c1288-109">子元素</span><span class="sxs-lookup"><span data-stu-id="c1288-109">Child elements</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c1288-110">元素</span><span class="sxs-lookup"><span data-stu-id="c1288-110">Element</span></span></th>
<th><span data-ttu-id="c1288-111">描述</span><span class="sxs-lookup"><span data-stu-id="c1288-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c1288-112"><a href="windowsribbon-element-button.md"><strong>Button</strong></a></span><span class="sxs-lookup"><span data-stu-id="c1288-112"><a href="windowsribbon-element-button.md"><strong>Button</strong></a></span></span><br/></td>
<td><span data-ttu-id="c1288-113">必須至少發生一次。</span><span class="sxs-lookup"><span data-stu-id="c1288-113">Must occur at least once.</span></span><br/> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c1288-114"><a href="windowsribbon-element-checkbox.md"><strong>相應</strong></a></span><span class="sxs-lookup"><span data-stu-id="c1288-114"><a href="windowsribbon-element-checkbox.md"><strong>CheckBox</strong></a></span></span><br/></td>
<td><span data-ttu-id="c1288-115">必須至少發生一次。</span><span class="sxs-lookup"><span data-stu-id="c1288-115">Must occur at least once.</span></span><br/> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c1288-116"><a href="windowsribbon-element-combobox.md"><strong>ComboBox</strong></a></span><span class="sxs-lookup"><span data-stu-id="c1288-116"><a href="windowsribbon-element-combobox.md"><strong>ComboBox</strong></a></span></span><br/></td>
<td><span data-ttu-id="c1288-117">必須至少發生一次。</span><span class="sxs-lookup"><span data-stu-id="c1288-117">Must occur at least once.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="c1288-118">Windows 8 和更新版本。</span><span class="sxs-lookup"><span data-stu-id="c1288-118">Windows 8 and newer.</span></span>
</blockquote>
<br/> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c1288-119"><a href="windowsribbon-element-dropdowngallery.md"><strong>DropDownGallery</strong></a></span><span class="sxs-lookup"><span data-stu-id="c1288-119"><a href="windowsribbon-element-dropdowngallery.md"><strong>DropDownGallery</strong></a></span></span><br/></td>
<td><span data-ttu-id="c1288-120">必須至少發生一次。</span><span class="sxs-lookup"><span data-stu-id="c1288-120">Must occur at least once.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="c1288-121">Windows 8 和更新版本。</span><span class="sxs-lookup"><span data-stu-id="c1288-121">Windows 8 and newer.</span></span>
</blockquote>
<br/> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c1288-122"><a href="windowsribbon-element-inribbongallery.md"><strong>InRibbonGallery</strong></a></span><span class="sxs-lookup"><span data-stu-id="c1288-122"><a href="windowsribbon-element-inribbongallery.md"><strong>InRibbonGallery</strong></a></span></span><br/></td>
<td><span data-ttu-id="c1288-123">必須至少發生一次。</span><span class="sxs-lookup"><span data-stu-id="c1288-123">Must occur at least once.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="c1288-124">Windows 8 和更新版本。</span><span class="sxs-lookup"><span data-stu-id="c1288-124">Windows 8 and newer.</span></span>
</blockquote>
<br/> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c1288-125"><a href="windowsribbon-element-splitbuttongallery.md"><strong>SplitButtonGallery</strong></a></span><span class="sxs-lookup"><span data-stu-id="c1288-125"><a href="windowsribbon-element-splitbuttongallery.md"><strong>SplitButtonGallery</strong></a></span></span><br/></td>
<td><span data-ttu-id="c1288-126">必須至少發生一次。</span><span class="sxs-lookup"><span data-stu-id="c1288-126">Must occur at least once.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="c1288-127">Windows 8 和更新版本。</span><span class="sxs-lookup"><span data-stu-id="c1288-127">Windows 8 and newer.</span></span>
</blockquote>
<br/> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c1288-128"><a href="windowsribbon-element-togglebutton.md"><strong>ToggleButton</strong></a></span><span class="sxs-lookup"><span data-stu-id="c1288-128"><a href="windowsribbon-element-togglebutton.md"><strong>ToggleButton</strong></a></span></span><br/></td>
<td><span data-ttu-id="c1288-129">必須至少發生一次。</span><span class="sxs-lookup"><span data-stu-id="c1288-129">Must occur at least once.</span></span><br/> <br/></td>
</tr>
</tbody>
</table>



## <a name="parent-elements"></a><span data-ttu-id="c1288-130">父元素</span><span class="sxs-lookup"><span data-stu-id="c1288-130">Parent elements</span></span>



| <span data-ttu-id="c1288-131">元素</span><span class="sxs-lookup"><span data-stu-id="c1288-131">Element</span></span>                                                                           |
|-----------------------------------------------------------------------------------|
| [<span data-ttu-id="c1288-132">**QuickAccessToolbar**</span><span class="sxs-lookup"><span data-stu-id="c1288-132">**QuickAccessToolbar**</span></span>](windowsribbon-element-quickaccesstoolbar.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="c1288-133">備註</span><span class="sxs-lookup"><span data-stu-id="c1288-133">Remarks</span></span>

<span data-ttu-id="c1288-134">選擇性。</span><span class="sxs-lookup"><span data-stu-id="c1288-134">Optional.</span></span>

<span data-ttu-id="c1288-135">每個 [**QuickAccessToolbar**](windowsribbon-element-quickaccesstoolbar.md)最多可能會發生一次。</span><span class="sxs-lookup"><span data-stu-id="c1288-135">May occur at most once for each [**QuickAccessToolbar**](windowsribbon-element-quickaccesstoolbar.md).</span></span>

<span data-ttu-id="c1288-136">至少必須指定一個子項目。</span><span class="sxs-lookup"><span data-stu-id="c1288-136">A minimum of one child element must be specified.</span></span>

<span data-ttu-id="c1288-137">最多可以指定20個子項目。</span><span class="sxs-lookup"><span data-stu-id="c1288-137">A maximum of 20 child elements can be specified.</span></span>

## <a name="examples"></a><span data-ttu-id="c1288-138">範例</span><span class="sxs-lookup"><span data-stu-id="c1288-138">Examples</span></span>

<span data-ttu-id="c1288-139">下列範例示範 [**QuickAccessToolbar**](windowsribbon-element-quickaccesstoolbar.md)的基本標記。</span><span class="sxs-lookup"><span data-stu-id="c1288-139">The following example demonstrates the basic markup for the [**QuickAccessToolbar**](windowsribbon-element-quickaccesstoolbar.md).</span></span>

<span data-ttu-id="c1288-140">這段程式碼會顯示 **QuickAccessToolbar s** 控制項宣告。</span><span class="sxs-lookup"><span data-stu-id="c1288-140">This section of code shows the **QuickAccessToolbar.ApplicationDefaults** control declaration.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="c1288-141">規格需求</span><span class="sxs-lookup"><span data-stu-id="c1288-141">Requirements</span></span>



| <span data-ttu-id="c1288-142">需求</span><span class="sxs-lookup"><span data-stu-id="c1288-142">Requirement</span></span> | <span data-ttu-id="c1288-143">值</span><span class="sxs-lookup"><span data-stu-id="c1288-143">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="c1288-144">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c1288-144">Minimum supported client</span></span><br/> | <span data-ttu-id="c1288-145">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c1288-145">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="c1288-146">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c1288-146">Minimum supported server</span></span><br/> | <span data-ttu-id="c1288-147">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c1288-147">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c1288-148">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c1288-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c1288-149">快速存取工具列控制項</span><span class="sxs-lookup"><span data-stu-id="c1288-149">Quick Access Toolbar control</span></span>](windowsribbon-controls-quickaccesstoolbar.md)
</dt> </dl>

 

 





