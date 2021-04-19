---
title: SplitButtonGallery. MenuLayout 屬性
description: 代表分割按鈕庫下拉式功能表版面配置的容器。
ms.assetid: 4bebdff6-16ea-4cf3-adc7-9b86ea200e81
keywords:
- SplitButtonGallery. MenuLayout 屬性 Windows 功能區
topic_type:
- apiref
api_name:
- SplitButtonGallery.MenuLayout
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 04428c14b5e47795da47e5c03970610cd08a6e8f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106967956"
---
# <a name="splitbuttongallerymenulayout-property"></a><span data-ttu-id="ff7d8-104">SplitButtonGallery. MenuLayout 屬性</span><span class="sxs-lookup"><span data-stu-id="ff7d8-104">SplitButtonGallery.MenuLayout property</span></span>

<span data-ttu-id="ff7d8-105">代表 [分割按鈕庫](windowsribbon-controls-splitbuttongallery.md) 下拉式功能表版面配置的容器。</span><span class="sxs-lookup"><span data-stu-id="ff7d8-105">Represents a container for [Split Button Gallery](windowsribbon-controls-splitbuttongallery.md) drop-down menu layouts.</span></span>

## <a name="usage"></a><span data-ttu-id="ff7d8-106">使用方式</span><span class="sxs-lookup"><span data-stu-id="ff7d8-106">Usage</span></span>

``` syntax
<SplitButtonGallery.MenuLayout>
  child elements
</SplitButtonGallery.MenuLayout>
```

## <a name="attributes"></a><span data-ttu-id="ff7d8-107">屬性</span><span class="sxs-lookup"><span data-stu-id="ff7d8-107">Attributes</span></span>

<span data-ttu-id="ff7d8-108">沒有任何屬性。</span><span class="sxs-lookup"><span data-stu-id="ff7d8-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="ff7d8-109">子元素</span><span class="sxs-lookup"><span data-stu-id="ff7d8-109">Child elements</span></span>



| <span data-ttu-id="ff7d8-110">元素</span><span class="sxs-lookup"><span data-stu-id="ff7d8-110">Element</span></span>                                                                           | <span data-ttu-id="ff7d8-111">描述</span><span class="sxs-lookup"><span data-stu-id="ff7d8-111">Description</span></span>                                    |
|-----------------------------------------------------------------------------------|------------------------------------------------|
| [<span data-ttu-id="ff7d8-112">**FlowMenuLayout**</span><span class="sxs-lookup"><span data-stu-id="ff7d8-112">**FlowMenuLayout**</span></span>](windowsribbon-element-flowmenulayout.md)<br/>         | <span data-ttu-id="ff7d8-113">必須剛好發生一次</span><span class="sxs-lookup"><span data-stu-id="ff7d8-113">Must occur exactly once</span></span><br/> <br/> |
| [<span data-ttu-id="ff7d8-114">**VerticalMenuLayout**</span><span class="sxs-lookup"><span data-stu-id="ff7d8-114">**VerticalMenuLayout**</span></span>](windowsribbon-element-verticalmenulayout.md)<br/> | <span data-ttu-id="ff7d8-115">必須剛好發生一次</span><span class="sxs-lookup"><span data-stu-id="ff7d8-115">Must occur exactly once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="ff7d8-116">父元素</span><span class="sxs-lookup"><span data-stu-id="ff7d8-116">Parent elements</span></span>



| <span data-ttu-id="ff7d8-117">元素</span><span class="sxs-lookup"><span data-stu-id="ff7d8-117">Element</span></span>                                                                           |
|-----------------------------------------------------------------------------------|
| [<span data-ttu-id="ff7d8-118">**SplitButtonGallery**</span><span class="sxs-lookup"><span data-stu-id="ff7d8-118">**SplitButtonGallery**</span></span>](windowsribbon-element-splitbuttongallery.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="ff7d8-119">備註</span><span class="sxs-lookup"><span data-stu-id="ff7d8-119">Remarks</span></span>

<span data-ttu-id="ff7d8-120">選擇性。</span><span class="sxs-lookup"><span data-stu-id="ff7d8-120">Optional.</span></span>

<span data-ttu-id="ff7d8-121">每個 [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) 元素最多可能會發生一次。</span><span class="sxs-lookup"><span data-stu-id="ff7d8-121">May occur at most once for each [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) element.</span></span>

> [!Note]  
> <span data-ttu-id="ff7d8-122">最多隻允許一個子項目 ([**VerticalMenuLayout**](windowsribbon-element-verticalmenulayout.md) 或 [**FlowMenuLayout**](windowsribbon-element-flowmenulayout.md)) 。</span><span class="sxs-lookup"><span data-stu-id="ff7d8-122">A maximum of one child element ([**VerticalMenuLayout**](windowsribbon-element-verticalmenulayout.md) or [**FlowMenuLayout**](windowsribbon-element-flowmenulayout.md)) is allowed.</span></span>

 

## <a name="examples"></a><span data-ttu-id="ff7d8-123">範例</span><span class="sxs-lookup"><span data-stu-id="ff7d8-123">Examples</span></span>

<span data-ttu-id="ff7d8-124">下列範例示範 [分割按鈕圖庫](windowsribbon-controls-splitbuttongallery.md)的基本標記。</span><span class="sxs-lookup"><span data-stu-id="ff7d8-124">The following example demonstrates the basic markup for the [Split Button Gallery](windowsribbon-controls-splitbuttongallery.md).</span></span>

<span data-ttu-id="ff7d8-125">這段程式碼會顯示 **SplitButtonGallery MenuLayout** 控制項宣告。</span><span class="sxs-lookup"><span data-stu-id="ff7d8-125">This section of code shows the **SplitButtonGallery.MenuLayout** control declaration.</span></span>


```XML
<!-- SplitButtonGallery -->
<Group CommandName="cmdSplitButtonGalleryGroup">
  <SplitButtonGallery CommandName="cmdSplitButtonGallery">
    <SplitButtonGallery.MenuLayout>
      <FlowMenuLayout Rows="2"
                      Columns="3"
                      Gripper="None"/>
    </SplitButtonGallery.MenuLayout>
    <SplitButtonGallery.MenuGroups>
      <MenuGroup>
        <Button CommandName="cmdButton1"></Button>
        <Button CommandName="cmdButton2"></Button>
      </MenuGroup>
      <MenuGroup>
        <Button CommandName="cmdButton3"></Button>
      </MenuGroup>
    </SplitButtonGallery.MenuGroups>
  </SplitButtonGallery>
</Group>
```



## <a name="requirements"></a><span data-ttu-id="ff7d8-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="ff7d8-126">Requirements</span></span>



| <span data-ttu-id="ff7d8-127">需求</span><span class="sxs-lookup"><span data-stu-id="ff7d8-127">Requirement</span></span> | <span data-ttu-id="ff7d8-128">值</span><span class="sxs-lookup"><span data-stu-id="ff7d8-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="ff7d8-129">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ff7d8-129">Minimum supported client</span></span><br/> | <span data-ttu-id="ff7d8-130">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ff7d8-130">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="ff7d8-131">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ff7d8-131">Minimum supported server</span></span><br/> | <span data-ttu-id="ff7d8-132">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ff7d8-132">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ff7d8-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ff7d8-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ff7d8-134">分割按鈕資源庫控制項</span><span class="sxs-lookup"><span data-stu-id="ff7d8-134">Split Button Gallery control</span></span>](windowsribbon-controls-splitbuttongallery.md)
</dt> <dt>

[<span data-ttu-id="ff7d8-135">使用資源庫</span><span class="sxs-lookup"><span data-stu-id="ff7d8-135">Working with Galleries</span></span>](ribbon-controls-galleries.md)
</dt> </dl>

 

 





