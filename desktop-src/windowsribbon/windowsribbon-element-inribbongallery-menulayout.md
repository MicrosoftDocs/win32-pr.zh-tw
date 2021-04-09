---
title: InRibbonGallery. MenuLayout 屬性
description: 代表 In-Ribbon 資源庫下拉式功能表版面配置的容器。
ms.assetid: 89e0eb39-2790-4571-a661-ab3ebafbb13f
keywords:
- InRibbonGallery. MenuLayout 屬性 Windows 功能區
topic_type:
- apiref
api_name:
- InRibbonGallery.MenuLayout
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d2fc5e0eab5d8dbc35cd9cb3be96e5d5d351416
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024680"
---
# <a name="inribbongallerymenulayout-property"></a><span data-ttu-id="ba65e-104">InRibbonGallery. MenuLayout 屬性</span><span class="sxs-lookup"><span data-stu-id="ba65e-104">InRibbonGallery.MenuLayout property</span></span>

<span data-ttu-id="ba65e-105">代表 [功能區圖庫](windowsribbon-controls-inribbongallery.md) 下拉式功能表版面配置的容器。</span><span class="sxs-lookup"><span data-stu-id="ba65e-105">Represents a container for [In-Ribbon Gallery](windowsribbon-controls-inribbongallery.md) drop-down menu layouts.</span></span>

## <a name="usage"></a><span data-ttu-id="ba65e-106">使用方式</span><span class="sxs-lookup"><span data-stu-id="ba65e-106">Usage</span></span>

``` syntax
<InRibbonGallery.MenuLayout>
  child elements
</InRibbonGallery.MenuLayout>
```

## <a name="attributes"></a><span data-ttu-id="ba65e-107">屬性</span><span class="sxs-lookup"><span data-stu-id="ba65e-107">Attributes</span></span>

<span data-ttu-id="ba65e-108">沒有任何屬性。</span><span class="sxs-lookup"><span data-stu-id="ba65e-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="ba65e-109">子元素</span><span class="sxs-lookup"><span data-stu-id="ba65e-109">Child elements</span></span>



| <span data-ttu-id="ba65e-110">元素</span><span class="sxs-lookup"><span data-stu-id="ba65e-110">Element</span></span>                                                                           | <span data-ttu-id="ba65e-111">描述</span><span class="sxs-lookup"><span data-stu-id="ba65e-111">Description</span></span>                                    |
|-----------------------------------------------------------------------------------|------------------------------------------------|
| [<span data-ttu-id="ba65e-112">**FlowMenuLayout**</span><span class="sxs-lookup"><span data-stu-id="ba65e-112">**FlowMenuLayout**</span></span>](windowsribbon-element-flowmenulayout.md)<br/>         | <span data-ttu-id="ba65e-113">必須剛好發生一次</span><span class="sxs-lookup"><span data-stu-id="ba65e-113">Must occur exactly once</span></span><br/> <br/> |
| [<span data-ttu-id="ba65e-114">**VerticalMenuLayout**</span><span class="sxs-lookup"><span data-stu-id="ba65e-114">**VerticalMenuLayout**</span></span>](windowsribbon-element-verticalmenulayout.md)<br/> | <span data-ttu-id="ba65e-115">必須剛好發生一次</span><span class="sxs-lookup"><span data-stu-id="ba65e-115">Must occur exactly once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="ba65e-116">父元素</span><span class="sxs-lookup"><span data-stu-id="ba65e-116">Parent elements</span></span>



| <span data-ttu-id="ba65e-117">元素</span><span class="sxs-lookup"><span data-stu-id="ba65e-117">Element</span></span>                                                                     |
|-----------------------------------------------------------------------------|
| [<span data-ttu-id="ba65e-118">**InRibbonGallery**</span><span class="sxs-lookup"><span data-stu-id="ba65e-118">**InRibbonGallery**</span></span>](windowsribbon-element-inribbongallery.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="ba65e-119">備註</span><span class="sxs-lookup"><span data-stu-id="ba65e-119">Remarks</span></span>

<span data-ttu-id="ba65e-120">選擇性。</span><span class="sxs-lookup"><span data-stu-id="ba65e-120">Optional.</span></span>

<span data-ttu-id="ba65e-121">每個 [**InRibbonGallery**](windowsribbon-element-inribbongallery.md) 元素最多可能會發生一次。</span><span class="sxs-lookup"><span data-stu-id="ba65e-121">May occur at most once for each [**InRibbonGallery**](windowsribbon-element-inribbongallery.md) element.</span></span>

> [!Note]  
> <span data-ttu-id="ba65e-122">最多隻允許一個子項目 ([**VerticalMenuLayout**](windowsribbon-element-verticalmenulayout.md) 或 [**FlowMenuLayout**](windowsribbon-element-flowmenulayout.md)) 。</span><span class="sxs-lookup"><span data-stu-id="ba65e-122">A maximum of one child element ([**VerticalMenuLayout**](windowsribbon-element-verticalmenulayout.md) or [**FlowMenuLayout**](windowsribbon-element-flowmenulayout.md)) is allowed.</span></span>

 

## <a name="examples"></a><span data-ttu-id="ba65e-123">範例</span><span class="sxs-lookup"><span data-stu-id="ba65e-123">Examples</span></span>

<span data-ttu-id="ba65e-124">下列範例會示範 [功能區元件庫](windowsribbon-controls-inribbongallery.md)的基本標記。</span><span class="sxs-lookup"><span data-stu-id="ba65e-124">The following example demonstrates the basic markup for the [In-Ribbon Gallery](windowsribbon-controls-inribbongallery.md).</span></span>

<span data-ttu-id="ba65e-125">這段程式碼會顯示 **InRibbonGallery MenuLayout** 控制項宣告。</span><span class="sxs-lookup"><span data-stu-id="ba65e-125">This section of code shows the **InRibbonGallery.MenuLayout** control declaration.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="ba65e-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="ba65e-126">Requirements</span></span>



| <span data-ttu-id="ba65e-127">需求</span><span class="sxs-lookup"><span data-stu-id="ba65e-127">Requirement</span></span> | <span data-ttu-id="ba65e-128">值</span><span class="sxs-lookup"><span data-stu-id="ba65e-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="ba65e-129">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ba65e-129">Minimum supported client</span></span><br/> | <span data-ttu-id="ba65e-130">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ba65e-130">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="ba65e-131">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ba65e-131">Minimum supported server</span></span><br/> | <span data-ttu-id="ba65e-132">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ba65e-132">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ba65e-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ba65e-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ba65e-134">功能區資源庫控制項</span><span class="sxs-lookup"><span data-stu-id="ba65e-134">In-Ribbon Gallery control</span></span>](windowsribbon-controls-inribbongallery.md)
</dt> <dt>

[<span data-ttu-id="ba65e-135">使用資源庫</span><span class="sxs-lookup"><span data-stu-id="ba65e-135">Working with Galleries</span></span>](ribbon-controls-galleries.md)
</dt> </dl>

 

 





