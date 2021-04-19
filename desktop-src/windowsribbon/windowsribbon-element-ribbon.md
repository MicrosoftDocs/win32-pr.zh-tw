---
title: 功能區元素
description: 表示功能區視圖中的功能區控制項。
ms.assetid: 51083180-4e86-4c90-9fd1-a58c12bcc756
keywords:
- 功能區元素視窗功能區
topic_type:
- apiref
api_name:
- Ribbon
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 76ce73735d05b3d8c8cfa686f53570fd08ae6f1c
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "106996360"
---
# <a name="ribbon-element"></a><span data-ttu-id="48e2f-104">功能區元素</span><span class="sxs-lookup"><span data-stu-id="48e2f-104">Ribbon element</span></span>

<span data-ttu-id="48e2f-105">表示功能區視圖中的功能區控制項。</span><span class="sxs-lookup"><span data-stu-id="48e2f-105">Represents the ribbon control in the Ribbon View.</span></span>

## <a name="usage"></a><span data-ttu-id="48e2f-106">使用方式</span><span class="sxs-lookup"><span data-stu-id="48e2f-106">Usage</span></span>

``` syntax
<Ribbon
  Name = "xs:string"
  GroupSpacing = "xs:string">
  child elements
</Ribbon>
```

## <a name="attributes"></a><span data-ttu-id="48e2f-107">屬性</span><span class="sxs-lookup"><span data-stu-id="48e2f-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="48e2f-108">屬性</span><span class="sxs-lookup"><span data-stu-id="48e2f-108">Attribute</span></span></th>
<th><span data-ttu-id="48e2f-109">類型</span><span class="sxs-lookup"><span data-stu-id="48e2f-109">Type</span></span></th>
<th><span data-ttu-id="48e2f-110">必要</span><span class="sxs-lookup"><span data-stu-id="48e2f-110">Required</span></span></th>
<th><span data-ttu-id="48e2f-111">描述</span><span class="sxs-lookup"><span data-stu-id="48e2f-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="48e2f-112"><strong>GroupSpacing</strong></span><span class="sxs-lookup"><span data-stu-id="48e2f-112"><strong>GroupSpacing</strong></span></span><br/></td>
<td><span data-ttu-id="48e2f-113">xs:string</span><span class="sxs-lookup"><span data-stu-id="48e2f-113">xs:string</span></span><br/></td>
<td><span data-ttu-id="48e2f-114">No</span><span class="sxs-lookup"><span data-stu-id="48e2f-114">No</span></span><br/></td>
<td><span data-ttu-id="48e2f-115"><dt><span></span><span></span><strong></strong> (Small) </span><span class="sxs-lookup"><span data-stu-id="48e2f-115"><dt><span></span><span></span><strong></strong> (Small)</span></span><br/> </dt> <dd> <span data-ttu-id="48e2f-116">預設值。</span><span class="sxs-lookup"><span data-stu-id="48e2f-116">Default.</span></span> <br/> </dd> <span data-ttu-id="48e2f-117"><dt><span></span><span></span><strong></strong> (中) </span><span class="sxs-lookup"><span data-stu-id="48e2f-117"><dt><span></span><span></span><strong></strong> (Medium)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="48e2f-118"><dt><span></span><span></span><strong></strong> (大型) </span><span class="sxs-lookup"><span data-stu-id="48e2f-118"><dt><span></span><span></span><strong></strong> (Large)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="48e2f-119"><strong>名稱</strong></span><span class="sxs-lookup"><span data-stu-id="48e2f-119"><strong>Name</strong></span></span><br/></td>
<td><span data-ttu-id="48e2f-120">xs:string</span><span class="sxs-lookup"><span data-stu-id="48e2f-120">xs:string</span></span><br/></td>
<td><span data-ttu-id="48e2f-121">No</span><span class="sxs-lookup"><span data-stu-id="48e2f-121">No</span></span><br/></td>
<td><span data-ttu-id="48e2f-122">用來批註命令元素。</span><span class="sxs-lookup"><span data-stu-id="48e2f-122">Used to annotate the command element.</span></span><br/> <br/><span data-ttu-id="48e2f-123">
<dt><span></span><span></span><strong></strong> (xs： string) </span><span class="sxs-lookup"><span data-stu-id="48e2f-123">
<dt><span></span><span></span><strong></strong> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="48e2f-124">任何零或多個字元的序列。</span><span class="sxs-lookup"><span data-stu-id="48e2f-124">Any sequence of zero or more characters.</span></span><br/> <span data-ttu-id="48e2f-125">長度上限為未系結。</span><span class="sxs-lookup"><span data-stu-id="48e2f-125">The maximum length is unbounded.</span></span><br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="48e2f-126">子元素</span><span class="sxs-lookup"><span data-stu-id="48e2f-126">Child elements</span></span>



| <span data-ttu-id="48e2f-127">元素</span><span class="sxs-lookup"><span data-stu-id="48e2f-127">Element</span></span>                                                                                         | <span data-ttu-id="48e2f-128">描述</span><span class="sxs-lookup"><span data-stu-id="48e2f-128">Description</span></span>                                   |
|-------------------------------------------------------------------------------------------------|-----------------------------------------------|
| [<span data-ttu-id="48e2f-129">**功能區. ApplicationMenu**</span><span class="sxs-lookup"><span data-stu-id="48e2f-129">**Ribbon.ApplicationMenu**</span></span>](windowsribbon-element-ribbon-applicationmenu.md)<br/>       | <span data-ttu-id="48e2f-130">最多可能發生一次</span><span class="sxs-lookup"><span data-stu-id="48e2f-130">May occur at most once</span></span><br/> <br/> |
| [<span data-ttu-id="48e2f-131">**功能區. CoNtextualTabs**</span><span class="sxs-lookup"><span data-stu-id="48e2f-131">**Ribbon.ContextualTabs**</span></span>](windowsribbon-element-ribbon-contextualtabs.md)<br/>         | <span data-ttu-id="48e2f-132">最多可能發生一次</span><span class="sxs-lookup"><span data-stu-id="48e2f-132">May occur at most once</span></span><br/> <br/> |
| [<span data-ttu-id="48e2f-133">**功能區. HelpButton**</span><span class="sxs-lookup"><span data-stu-id="48e2f-133">**Ribbon.HelpButton**</span></span>](windowsribbon-element-ribbon-helpbutton.md)<br/>                 | <span data-ttu-id="48e2f-134">最多可能發生一次</span><span class="sxs-lookup"><span data-stu-id="48e2f-134">May occur at most once</span></span><br/> <br/> |
| [<span data-ttu-id="48e2f-135">**功能區. QuickAccessToolbar**</span><span class="sxs-lookup"><span data-stu-id="48e2f-135">**Ribbon.QuickAccessToolbar**</span></span>](windowsribbon-element-ribbon-quickaccesstoolbar.md)<br/> | <span data-ttu-id="48e2f-136">最多可能發生一次</span><span class="sxs-lookup"><span data-stu-id="48e2f-136">May occur at most once</span></span><br/> <br/> |
| [<span data-ttu-id="48e2f-137">**功能區. SizeDefinitions**</span><span class="sxs-lookup"><span data-stu-id="48e2f-137">**Ribbon.SizeDefinitions**</span></span>](windowsribbon-element-ribbon-sizedefinitions.md)<br/>       | <span data-ttu-id="48e2f-138">最多可能發生一次</span><span class="sxs-lookup"><span data-stu-id="48e2f-138">May occur at most once</span></span><br/> <br/> |
| <span data-ttu-id="48e2f-139">[**功能區] 索引標籤**](windowsribbon-element-ribbon-tabs.md)</span><span class="sxs-lookup"><span data-stu-id="48e2f-139">[**Ribbon.Tabs**](windowsribbon-element-ribbon-tabs.md)</span></span><br/>                             | <span data-ttu-id="48e2f-140">最多可能發生一次</span><span class="sxs-lookup"><span data-stu-id="48e2f-140">May occur at most once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="48e2f-141">父元素</span><span class="sxs-lookup"><span data-stu-id="48e2f-141">Parent elements</span></span>



| <span data-ttu-id="48e2f-142">元素</span><span class="sxs-lookup"><span data-stu-id="48e2f-142">Element</span></span>                                                                         |
|---------------------------------------------------------------------------------|
| [<span data-ttu-id="48e2f-143">**應用程式。 Views**</span><span class="sxs-lookup"><span data-stu-id="48e2f-143">**Application.Views**</span></span>](windowsribbon-element-application-views.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="48e2f-144">備註</span><span class="sxs-lookup"><span data-stu-id="48e2f-144">Remarks</span></span>

<span data-ttu-id="48e2f-145">必要。</span><span class="sxs-lookup"><span data-stu-id="48e2f-145">Required.</span></span>

<span data-ttu-id="48e2f-146">每個應用程式都必須剛好發生一次 [**。 Views**](windowsribbon-element-application-views.md) 元素。</span><span class="sxs-lookup"><span data-stu-id="48e2f-146">Must occur exactly once for each [**Application.Views**](windowsribbon-element-application-views.md) element.</span></span>

## <a name="examples"></a><span data-ttu-id="48e2f-147">範例</span><span class="sxs-lookup"><span data-stu-id="48e2f-147">Examples</span></span>

<span data-ttu-id="48e2f-148">下列範例會示範 **功能區** 視圖的基本標記。</span><span class="sxs-lookup"><span data-stu-id="48e2f-148">The following example demonstrates the basic markup for a **Ribbon** View.</span></span>


```XML
<Ribbon Name="ScenicRibbonSampleApp">
  <Ribbon.QuickAccessToolbar>
  ...
  </Ribbon.QuickAccessToolbar>
  <Ribbon.ApplicationMenu>
  ...
  </Ribbon.ApplicationMenu>
  <Ribbon.SizeDefinitions>
  ...
  </Ribbon.SizeDefinitions>
  <Ribbon.Tabs>
  ...
  </Ribbon.Tabs>
  <Ribbon.ContextualTabs>
  ...
  </Ribbon.ContextualTabs>
  <Ribbon.HelpButton>
  ...
  </Ribbon.HelpButton>
</Ribbon>
```



## <a name="element-information"></a><span data-ttu-id="48e2f-149">項目資訊</span><span class="sxs-lookup"><span data-stu-id="48e2f-149">Element information</span></span>



|                                     |           |
|-------------------------------------|-----------|
| <span data-ttu-id="48e2f-150">最低支援系統</span><span class="sxs-lookup"><span data-stu-id="48e2f-150">Minimum supported system</span></span><br/> | <span data-ttu-id="48e2f-151">Windows 7</span><span class="sxs-lookup"><span data-stu-id="48e2f-151">Windows 7</span></span> |
| <span data-ttu-id="48e2f-152">可以是空的</span><span class="sxs-lookup"><span data-stu-id="48e2f-152">Can be empty</span></span>                        | <span data-ttu-id="48e2f-153">否</span><span class="sxs-lookup"><span data-stu-id="48e2f-153">No</span></span>        |



 

 





