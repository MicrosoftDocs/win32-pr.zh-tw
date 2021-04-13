---
title: '[功能區] 索引標籤屬性'
description: 代表功能區中所有核心索引標籤的容器。
ms.assetid: b43d0544-c110-4785-85d7-935842b8f03e
keywords:
- '[功能區] 屬性視窗功能區'
topic_type:
- apiref
api_name:
- Ribbon.Tabs
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4300a2385b6ada64e05e16671802460930cc2a7b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464441"
---
# <a name="ribbontabs-property"></a><span data-ttu-id="4a93f-104">[功能區] 索引標籤屬性</span><span class="sxs-lookup"><span data-stu-id="4a93f-104">Ribbon.Tabs property</span></span>

<span data-ttu-id="4a93f-105">代表功能區中所有核心索引標籤的容器。</span><span class="sxs-lookup"><span data-stu-id="4a93f-105">Represents a container for all core tabs in a Ribbon.</span></span>

## <a name="usage"></a><span data-ttu-id="4a93f-106">使用方式</span><span class="sxs-lookup"><span data-stu-id="4a93f-106">Usage</span></span>

``` syntax
<Ribbon.Tabs>
  child elements
</Ribbon.Tabs>
```

## <a name="attributes"></a><span data-ttu-id="4a93f-107">屬性</span><span class="sxs-lookup"><span data-stu-id="4a93f-107">Attributes</span></span>

<span data-ttu-id="4a93f-108">沒有任何屬性。</span><span class="sxs-lookup"><span data-stu-id="4a93f-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="4a93f-109">子元素</span><span class="sxs-lookup"><span data-stu-id="4a93f-109">Child elements</span></span>



| <span data-ttu-id="4a93f-110">元素</span><span class="sxs-lookup"><span data-stu-id="4a93f-110">Element</span></span>                                             | <span data-ttu-id="4a93f-111">描述</span><span class="sxs-lookup"><span data-stu-id="4a93f-111">Description</span></span>                                     |
|-----------------------------------------------------|-------------------------------------------------|
| [<span data-ttu-id="4a93f-112">**索引標籤**</span><span class="sxs-lookup"><span data-stu-id="4a93f-112">**Tab**</span></span>](windowsribbon-element-tab.md)<br/> | <span data-ttu-id="4a93f-113">至少必須發生一次</span><span class="sxs-lookup"><span data-stu-id="4a93f-113">Must occur at least once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="4a93f-114">父元素</span><span class="sxs-lookup"><span data-stu-id="4a93f-114">Parent elements</span></span>



| <span data-ttu-id="4a93f-115">元素</span><span class="sxs-lookup"><span data-stu-id="4a93f-115">Element</span></span>                                                   |
|-----------------------------------------------------------|
| [<span data-ttu-id="4a93f-116">**功能區**</span><span class="sxs-lookup"><span data-stu-id="4a93f-116">**Ribbon**</span></span>](windowsribbon-element-ribbon.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="4a93f-117">備註</span><span class="sxs-lookup"><span data-stu-id="4a93f-117">Remarks</span></span>

<span data-ttu-id="4a93f-118">必要。</span><span class="sxs-lookup"><span data-stu-id="4a93f-118">Required.</span></span>

<span data-ttu-id="4a93f-119">每個 [**功能區**](windowsribbon-element-ribbon.md)可能會出現一次或多次。</span><span class="sxs-lookup"><span data-stu-id="4a93f-119">May occur one or more times for each [**Ribbon**](windowsribbon-element-ribbon.md).</span></span>

## <a name="examples"></a><span data-ttu-id="4a93f-120">範例</span><span class="sxs-lookup"><span data-stu-id="4a93f-120">Examples</span></span>

<span data-ttu-id="4a93f-121">下列範例會示範 **功能區** 的基本標記，其中包含 **首頁** [](windowsribbon-element-tab.md)索引標籤宣告。</span><span class="sxs-lookup"><span data-stu-id="4a93f-121">The following example demonstrates the basic markup for a **Ribbon.Tabs** element with a **Home** [**Tab**](windowsribbon-element-tab.md) declaration.</span></span>


```C++
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
```




```C++
<Tab CommandName="cmdHomeTab">
  <Group CommandName="cmdClipboardGroup" 
         SizeDefinition="ThreeButtons">
    <Button CommandName="cmdCopy"/>
    <Button CommandName="cmdPaste"/>
    <ToggleButton CommandName="cmdMinimize"/>
  </Group>
</Tab>
```




```C++
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



## <a name="requirements"></a><span data-ttu-id="4a93f-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="4a93f-122">Requirements</span></span>



| <span data-ttu-id="4a93f-123">需求</span><span class="sxs-lookup"><span data-stu-id="4a93f-123">Requirement</span></span> | <span data-ttu-id="4a93f-124">值</span><span class="sxs-lookup"><span data-stu-id="4a93f-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="4a93f-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4a93f-125">Minimum supported client</span></span><br/> | <span data-ttu-id="4a93f-126">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4a93f-126">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="4a93f-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4a93f-127">Minimum supported server</span></span><br/> | <span data-ttu-id="4a93f-128">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4a93f-128">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="4a93f-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4a93f-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4a93f-130">**功能區. CoNtextualTabs**</span><span class="sxs-lookup"><span data-stu-id="4a93f-130">**Ribbon.ContextualTabs**</span></span>](windowsribbon-element-ribbon-contextualtabs.md)
</dt> </dl>

 

 





