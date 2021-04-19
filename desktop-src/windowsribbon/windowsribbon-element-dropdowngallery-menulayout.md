---
title: DropDownGallery. MenuLayout 屬性
description: 代表 DropDownGallery 下拉式功能表版面配置的容器。
ms.assetid: 7251e889-377d-4d7f-b049-bd81a202774d
keywords:
- DropDownGallery. MenuLayout 屬性 Windows 功能區
topic_type:
- apiref
api_name:
- DropDownGallery.MenuLayout
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d1b6ad3f07f369dfef90b1e6c52c34793e60520
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106968376"
---
# <a name="dropdowngallerymenulayout-property"></a><span data-ttu-id="5918c-104">DropDownGallery. MenuLayout 屬性</span><span class="sxs-lookup"><span data-stu-id="5918c-104">DropDownGallery.MenuLayout property</span></span>

<span data-ttu-id="5918c-105">代表 [**DropDownGallery**](windowsribbon-element-dropdowngallery.md) 下拉式功能表版面配置的容器。</span><span class="sxs-lookup"><span data-stu-id="5918c-105">Represents a container for [**DropDownGallery**](windowsribbon-element-dropdowngallery.md) drop-down menu layouts.</span></span>

## <a name="usage"></a><span data-ttu-id="5918c-106">使用方式</span><span class="sxs-lookup"><span data-stu-id="5918c-106">Usage</span></span>

``` syntax
<DropDownGallery.MenuLayout>
  child elements
</DropDownGallery.MenuLayout>
```

## <a name="attributes"></a><span data-ttu-id="5918c-107">屬性</span><span class="sxs-lookup"><span data-stu-id="5918c-107">Attributes</span></span>

<span data-ttu-id="5918c-108">沒有任何屬性。</span><span class="sxs-lookup"><span data-stu-id="5918c-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="5918c-109">子元素</span><span class="sxs-lookup"><span data-stu-id="5918c-109">Child elements</span></span>



| <span data-ttu-id="5918c-110">元素</span><span class="sxs-lookup"><span data-stu-id="5918c-110">Element</span></span>                                                                           | <span data-ttu-id="5918c-111">描述</span><span class="sxs-lookup"><span data-stu-id="5918c-111">Description</span></span>                                    |
|-----------------------------------------------------------------------------------|------------------------------------------------|
| [<span data-ttu-id="5918c-112">**FlowMenuLayout**</span><span class="sxs-lookup"><span data-stu-id="5918c-112">**FlowMenuLayout**</span></span>](windowsribbon-element-flowmenulayout.md)<br/>         | <span data-ttu-id="5918c-113">必須剛好發生一次</span><span class="sxs-lookup"><span data-stu-id="5918c-113">Must occur exactly once</span></span><br/> <br/> |
| [<span data-ttu-id="5918c-114">**VerticalMenuLayout**</span><span class="sxs-lookup"><span data-stu-id="5918c-114">**VerticalMenuLayout**</span></span>](windowsribbon-element-verticalmenulayout.md)<br/> | <span data-ttu-id="5918c-115">必須剛好發生一次</span><span class="sxs-lookup"><span data-stu-id="5918c-115">Must occur exactly once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="5918c-116">父元素</span><span class="sxs-lookup"><span data-stu-id="5918c-116">Parent elements</span></span>



| <span data-ttu-id="5918c-117">元素</span><span class="sxs-lookup"><span data-stu-id="5918c-117">Element</span></span>                                                                     |
|-----------------------------------------------------------------------------|
| [<span data-ttu-id="5918c-118">**DropDownGallery**</span><span class="sxs-lookup"><span data-stu-id="5918c-118">**DropDownGallery**</span></span>](windowsribbon-element-dropdowngallery.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="5918c-119">備註</span><span class="sxs-lookup"><span data-stu-id="5918c-119">Remarks</span></span>

<span data-ttu-id="5918c-120">選擇性。</span><span class="sxs-lookup"><span data-stu-id="5918c-120">Optional.</span></span>

<span data-ttu-id="5918c-121">每個 [**DropDownGallery**](windowsribbon-element-dropdowngallery.md) 元素最多可能會發生一次。</span><span class="sxs-lookup"><span data-stu-id="5918c-121">May occur at most once for each [**DropDownGallery**](windowsribbon-element-dropdowngallery.md) element.</span></span>

> [!Note]  
> <span data-ttu-id="5918c-122">最多隻允許一個子項目 ([**VerticalMenuLayout**](windowsribbon-element-verticalmenulayout.md) 或 [**FlowMenuLayout**](windowsribbon-element-flowmenulayout.md)) 。</span><span class="sxs-lookup"><span data-stu-id="5918c-122">A maximum of one child element ([**VerticalMenuLayout**](windowsribbon-element-verticalmenulayout.md) or [**FlowMenuLayout**](windowsribbon-element-flowmenulayout.md)) is allowed.</span></span>

 

## <a name="examples"></a><span data-ttu-id="5918c-123">範例</span><span class="sxs-lookup"><span data-stu-id="5918c-123">Examples</span></span>

<span data-ttu-id="5918c-124">下列範例示範 [**DropDownGallery**](windowsribbon-element-dropdowngallery.md)的基本標記。</span><span class="sxs-lookup"><span data-stu-id="5918c-124">The following example demonstrates the basic markup for the [**DropDownGallery**](windowsribbon-element-dropdowngallery.md).</span></span>

<span data-ttu-id="5918c-125">這段程式碼會顯示 **DropDownGallery MenuLayout** 控制項宣告。</span><span class="sxs-lookup"><span data-stu-id="5918c-125">This section of code shows the **DropDownGallery.MenuLayout** control declaration.</span></span>


```XML
<!-- DropDownGallery -->
<Group CommandName="cmdDropDownGalleryGroup">
  <DropDownGallery CommandName="cmdDropDownGallery"
                   TextPosition="Hide"
                   Type="Commands"
                   ItemHeight="32"
                   ItemWidth="32">
    <DropDownGallery.MenuLayout>
      <FlowMenuLayout Rows="2"
                      Columns="3"
                      Gripper="None"/>
    </DropDownGallery.MenuLayout>
    <DropDownGallery.MenuGroups>
      <MenuGroup>
        <Button CommandName="cmdButton1"></Button>
        <Button CommandName="cmdButton2"></Button>
       </MenuGroup>
       <MenuGroup>
        <Button CommandName="cmdButton3"></Button>
      </MenuGroup>
    </DropDownGallery.MenuGroups>
  </DropDownGallery>
</Group>
```



## <a name="requirements"></a><span data-ttu-id="5918c-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="5918c-126">Requirements</span></span>



| <span data-ttu-id="5918c-127">需求</span><span class="sxs-lookup"><span data-stu-id="5918c-127">Requirement</span></span> | <span data-ttu-id="5918c-128">值</span><span class="sxs-lookup"><span data-stu-id="5918c-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="5918c-129">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5918c-129">Minimum supported client</span></span><br/> | <span data-ttu-id="5918c-130">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5918c-130">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="5918c-131">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5918c-131">Minimum supported server</span></span><br/> | <span data-ttu-id="5918c-132">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5918c-132">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="5918c-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5918c-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5918c-134">**下拉式圖庫控制項**</span><span class="sxs-lookup"><span data-stu-id="5918c-134">**Drop-Down Gallery control**</span></span>](windowsribbon-element-dropdowngallery.md)
</dt> <dt>

[<span data-ttu-id="5918c-135">使用資源庫</span><span class="sxs-lookup"><span data-stu-id="5918c-135">Working with Galleries</span></span>](ribbon-controls-galleries.md)
</dt> </dl>

 

 





