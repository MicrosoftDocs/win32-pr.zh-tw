---
title: Views 屬性
description: 表示每個功能區架構視圖的容器，特別是功能區和 CoNtextPopup。
ms.assetid: e7549b8b-0f95-477a-9024-1a99ee1412c2
keywords:
- 應用程式。 Views 屬性視窗功能區
topic_type:
- apiref
api_name:
- Application.Views
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 57e7d106d346a790ee3bd8879b2367f38341f0a9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106968560"
---
# <a name="applicationviews-property"></a><span data-ttu-id="a7add-104">Views 屬性</span><span class="sxs-lookup"><span data-stu-id="a7add-104">Application.Views property</span></span>

<span data-ttu-id="a7add-105">表示每個功能區架構視圖的容器，特別是 [**功能區**](windowsribbon-element-ribbon.md) 和 [**CoNtextPopup**](windowsribbon-element-contextpopup.md)。</span><span class="sxs-lookup"><span data-stu-id="a7add-105">Represents a container for each Ribbon framework View, specifically the [**Ribbon**](windowsribbon-element-ribbon.md) and the [**ContextPopup**](windowsribbon-element-contextpopup.md).</span></span>

## <a name="usage"></a><span data-ttu-id="a7add-106">使用方式</span><span class="sxs-lookup"><span data-stu-id="a7add-106">Usage</span></span>

``` syntax
<Application.Views>
  child elements
</Application.Views>
```

## <a name="attributes"></a><span data-ttu-id="a7add-107">屬性</span><span class="sxs-lookup"><span data-stu-id="a7add-107">Attributes</span></span>

<span data-ttu-id="a7add-108">沒有任何屬性。</span><span class="sxs-lookup"><span data-stu-id="a7add-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="a7add-109">子元素</span><span class="sxs-lookup"><span data-stu-id="a7add-109">Child elements</span></span>



| <span data-ttu-id="a7add-110">元素</span><span class="sxs-lookup"><span data-stu-id="a7add-110">Element</span></span>                                                               | <span data-ttu-id="a7add-111">描述</span><span class="sxs-lookup"><span data-stu-id="a7add-111">Description</span></span>                                        |
|-----------------------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="a7add-112">**CoNtextPopup**</span><span class="sxs-lookup"><span data-stu-id="a7add-112">**ContextPopup**</span></span>](windowsribbon-element-contextpopup.md)<br/> | <span data-ttu-id="a7add-113">可能會發生一次或多次</span><span class="sxs-lookup"><span data-stu-id="a7add-113">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="a7add-114">**功能區**</span><span class="sxs-lookup"><span data-stu-id="a7add-114">**Ribbon**</span></span>](windowsribbon-element-ribbon.md)<br/>             | <span data-ttu-id="a7add-115">必須剛好發生一次</span><span class="sxs-lookup"><span data-stu-id="a7add-115">Must occur exactly once</span></span><br/> <br/>     |



## <a name="parent-elements"></a><span data-ttu-id="a7add-116">父元素</span><span class="sxs-lookup"><span data-stu-id="a7add-116">Parent elements</span></span>



| <span data-ttu-id="a7add-117">元素</span><span class="sxs-lookup"><span data-stu-id="a7add-117">Element</span></span>                                                             |
|---------------------------------------------------------------------|
| [<span data-ttu-id="a7add-118">**應用程式**</span><span class="sxs-lookup"><span data-stu-id="a7add-118">**Application**</span></span>](windowsribbon-element-application.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="a7add-119">備註</span><span class="sxs-lookup"><span data-stu-id="a7add-119">Remarks</span></span>

<span data-ttu-id="a7add-120">必要。</span><span class="sxs-lookup"><span data-stu-id="a7add-120">Required.</span></span>

<span data-ttu-id="a7add-121">必須針對每個 [**應用程式**](windowsribbon-element-application.md) 元素剛好出現一次。</span><span class="sxs-lookup"><span data-stu-id="a7add-121">Must occur exactly once for each [**Application**](windowsribbon-element-application.md) element.</span></span>

## <a name="examples"></a><span data-ttu-id="a7add-122">範例</span><span class="sxs-lookup"><span data-stu-id="a7add-122">Examples</span></span>

<span data-ttu-id="a7add-123">下列範例顯示的是一個 **應用程式。 Views** 元素包含功能區控制項的資訊清單，而且每個專案都有一個在 [**Application 命令**](windowsribbon-element-application-commands.md) 專案中宣告之命令的參考。</span><span class="sxs-lookup"><span data-stu-id="a7add-123">The following example shows an **Application.Views** element that contains a manifest of Ribbon controls, each with a reference to a Command declared in the [**Application.Commands**](windowsribbon-element-application-commands.md) element.</span></span>


```C++
<Application.Views>
  <Ribbon Name="ScenicRibbonSampleApp">
    <Ribbon.Tabs>
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
    </Ribbon.Tabs>
  </Ribbon>
</Application.Views>
```



## <a name="requirements"></a><span data-ttu-id="a7add-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="a7add-124">Requirements</span></span>



| <span data-ttu-id="a7add-125">需求</span><span class="sxs-lookup"><span data-stu-id="a7add-125">Requirement</span></span> | <span data-ttu-id="a7add-126">值</span><span class="sxs-lookup"><span data-stu-id="a7add-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="a7add-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a7add-127">Minimum supported client</span></span><br/> | <span data-ttu-id="a7add-128">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a7add-128">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="a7add-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a7add-129">Minimum supported server</span></span><br/> | <span data-ttu-id="a7add-130">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a7add-130">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a7add-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a7add-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a7add-132">**應用程式。命令**</span><span class="sxs-lookup"><span data-stu-id="a7add-132">**Application.Commands**</span></span>](windowsribbon-element-application-commands.md)
</dt> </dl>

 

 





