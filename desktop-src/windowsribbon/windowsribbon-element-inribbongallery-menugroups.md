---
title: InRibbonGallery. MenuGroups 屬性
description: 代表 In-Ribbon 資源庫控制項之下拉式功能表專案集合的容器。
ms.assetid: 6b9ded25-4e8e-4e30-a349-f7c091dbfe7a
keywords:
- InRibbonGallery. MenuGroups 屬性 Windows 功能區
topic_type:
- apiref
api_name:
- InRibbonGallery.MenuGroups
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd447b66dada74b1a9b909b3030e080198143b12
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025156"
---
# <a name="inribbongallerymenugroups-property"></a><span data-ttu-id="2ed55-104">InRibbonGallery. MenuGroups 屬性</span><span class="sxs-lookup"><span data-stu-id="2ed55-104">InRibbonGallery.MenuGroups property</span></span>

<span data-ttu-id="2ed55-105">代表 [功能區資源庫控制項中](windowsribbon-controls-inribbongallery.md) ，一組下拉式功能表專案的容器。</span><span class="sxs-lookup"><span data-stu-id="2ed55-105">Represents a container for the set of drop-down menu items of an [In-Ribbon Gallery](windowsribbon-controls-inribbongallery.md) control.</span></span>

## <a name="usage"></a><span data-ttu-id="2ed55-106">使用方式</span><span class="sxs-lookup"><span data-stu-id="2ed55-106">Usage</span></span>

``` syntax
<InRibbonGallery.MenuGroups>
  child elements
</InRibbonGallery.MenuGroups>
```

## <a name="attributes"></a><span data-ttu-id="2ed55-107">屬性</span><span class="sxs-lookup"><span data-stu-id="2ed55-107">Attributes</span></span>

<span data-ttu-id="2ed55-108">沒有任何屬性。</span><span class="sxs-lookup"><span data-stu-id="2ed55-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="2ed55-109">子元素</span><span class="sxs-lookup"><span data-stu-id="2ed55-109">Child elements</span></span>



| <span data-ttu-id="2ed55-110">元素</span><span class="sxs-lookup"><span data-stu-id="2ed55-110">Element</span></span>                                                         | <span data-ttu-id="2ed55-111">描述</span><span class="sxs-lookup"><span data-stu-id="2ed55-111">Description</span></span>                                     |
|-----------------------------------------------------------------|-------------------------------------------------|
| [<span data-ttu-id="2ed55-112">**MenuGroup**</span><span class="sxs-lookup"><span data-stu-id="2ed55-112">**MenuGroup**</span></span>](windowsribbon-element-menugroup.md)<br/> | <span data-ttu-id="2ed55-113">至少必須發生一次</span><span class="sxs-lookup"><span data-stu-id="2ed55-113">Must occur at least once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="2ed55-114">父元素</span><span class="sxs-lookup"><span data-stu-id="2ed55-114">Parent elements</span></span>



| <span data-ttu-id="2ed55-115">元素</span><span class="sxs-lookup"><span data-stu-id="2ed55-115">Element</span></span>                                                                     |
|-----------------------------------------------------------------------------|
| [<span data-ttu-id="2ed55-116">**InRibbonGallery**</span><span class="sxs-lookup"><span data-stu-id="2ed55-116">**InRibbonGallery**</span></span>](windowsribbon-element-inribbongallery.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="2ed55-117">備註</span><span class="sxs-lookup"><span data-stu-id="2ed55-117">Remarks</span></span>

<span data-ttu-id="2ed55-118">選擇性。</span><span class="sxs-lookup"><span data-stu-id="2ed55-118">Optional.</span></span>

<span data-ttu-id="2ed55-119">每個 [**InRibbonGallery**](windowsribbon-element-inribbongallery.md) 元素最多可能會發生一次。</span><span class="sxs-lookup"><span data-stu-id="2ed55-119">May occur at most once for each [**InRibbonGallery**](windowsribbon-element-inribbongallery.md) element.</span></span>

## <a name="examples"></a><span data-ttu-id="2ed55-120">範例</span><span class="sxs-lookup"><span data-stu-id="2ed55-120">Examples</span></span>

<span data-ttu-id="2ed55-121">下列範例會示範 [功能區資源庫](windowsribbon-controls-inribbongallery.md) 控制項的基本標記。</span><span class="sxs-lookup"><span data-stu-id="2ed55-121">The following example demonstrates the basic markup for an [In-Ribbon Gallery](windowsribbon-controls-inribbongallery.md) control.</span></span>

<span data-ttu-id="2ed55-122">這段程式碼會顯示 **InRibbonGallery MenuGroups** 控制項宣告。</span><span class="sxs-lookup"><span data-stu-id="2ed55-122">This section of code shows the **InRibbonGallery.MenuGroups** control declaration.</span></span>


```XML
<!-- InRibbonGallery -->
<Group CommandName="cmdInRibbonGalleryGroup" SizeDefinition="OneInRibbonGallery">
  <InRibbonGallery CommandName="cmdInRibbonGallery"
                   MaxColumns="10"
                   MaxColumnsMedium="5"
                   MinColumnsLarge="5"
                   MinColumnsMedium="3"
                   Type="Items">
    <InRibbonGallery.MenuLayout>
      <VerticalMenuLayout Rows="2"
                          Gripper="Vertical"/>
    </InRibbonGallery.MenuLayout>
    <InRibbonGallery.MenuGroups>
      <MenuGroup>
        <Button CommandName="cmdButton1"></Button>
        <Button CommandName="cmdButton2"></Button>
      </MenuGroup>
      <MenuGroup>
        <Button CommandName="cmdButton3"></Button>
      </MenuGroup>
    </InRibbonGallery.MenuGroups>            
  </InRibbonGallery>
</Group>
```



## <a name="requirements"></a><span data-ttu-id="2ed55-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="2ed55-123">Requirements</span></span>



| <span data-ttu-id="2ed55-124">需求</span><span class="sxs-lookup"><span data-stu-id="2ed55-124">Requirement</span></span> | <span data-ttu-id="2ed55-125">值</span><span class="sxs-lookup"><span data-stu-id="2ed55-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="2ed55-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2ed55-126">Minimum supported client</span></span><br/> | <span data-ttu-id="2ed55-127">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2ed55-127">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="2ed55-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2ed55-128">Minimum supported server</span></span><br/> | <span data-ttu-id="2ed55-129">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2ed55-129">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="2ed55-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2ed55-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2ed55-131">功能區資源庫控制項</span><span class="sxs-lookup"><span data-stu-id="2ed55-131">In-Ribbon Gallery control</span></span>](windowsribbon-controls-inribbongallery.md)
</dt> <dt>

[<span data-ttu-id="2ed55-132">使用資源庫</span><span class="sxs-lookup"><span data-stu-id="2ed55-132">Working with Galleries</span></span>](ribbon-controls-galleries.md)
</dt> <dt>

[<span data-ttu-id="2ed55-133">透過大小定義和調整原則自訂功能區</span><span class="sxs-lookup"><span data-stu-id="2ed55-133">Customizing a Ribbon Through Size Definitions and Scaling Policies</span></span>](windowsribbon-templates.md)
</dt> </dl>

 

 





