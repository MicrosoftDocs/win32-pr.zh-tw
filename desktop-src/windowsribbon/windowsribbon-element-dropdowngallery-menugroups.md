---
title: DropDownGallery. MenuGroups 屬性
description: 代表 Drop-Down 資源庫控制項中的一組下拉式功能表專案的容器。
ms.assetid: 594f6ae5-760e-456d-98cd-04ecae0bae99
keywords:
- DropDownGallery. MenuGroups 屬性 Windows 功能區
topic_type:
- apiref
api_name:
- DropDownGallery.MenuGroups
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 67fcaeb81020cf4c317bf065c25a770d2a77e21f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106969814"
---
# <a name="dropdowngallerymenugroups-property"></a><span data-ttu-id="e54bb-104">DropDownGallery. MenuGroups 屬性</span><span class="sxs-lookup"><span data-stu-id="e54bb-104">DropDownGallery.MenuGroups property</span></span>

<span data-ttu-id="e54bb-105">代表下拉式清單資源 [庫](windowsribbon-controls-dropdowngallery.md) 控制項中一組下拉式功能表專案的容器。</span><span class="sxs-lookup"><span data-stu-id="e54bb-105">Represents a container for a set of drop-down menu items in a [Drop-Down Gallery](windowsribbon-controls-dropdowngallery.md) control.</span></span>

## <a name="usage"></a><span data-ttu-id="e54bb-106">使用方式</span><span class="sxs-lookup"><span data-stu-id="e54bb-106">Usage</span></span>

``` syntax
<DropDownGallery.MenuGroups>
  child elements
</DropDownGallery.MenuGroups>
```

## <a name="attributes"></a><span data-ttu-id="e54bb-107">屬性</span><span class="sxs-lookup"><span data-stu-id="e54bb-107">Attributes</span></span>

<span data-ttu-id="e54bb-108">沒有任何屬性。</span><span class="sxs-lookup"><span data-stu-id="e54bb-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="e54bb-109">子元素</span><span class="sxs-lookup"><span data-stu-id="e54bb-109">Child elements</span></span>



| <span data-ttu-id="e54bb-110">元素</span><span class="sxs-lookup"><span data-stu-id="e54bb-110">Element</span></span>                                                         | <span data-ttu-id="e54bb-111">描述</span><span class="sxs-lookup"><span data-stu-id="e54bb-111">Description</span></span>                                     |
|-----------------------------------------------------------------|-------------------------------------------------|
| [<span data-ttu-id="e54bb-112">**MenuGroup**</span><span class="sxs-lookup"><span data-stu-id="e54bb-112">**MenuGroup**</span></span>](windowsribbon-element-menugroup.md)<br/> | <span data-ttu-id="e54bb-113">至少必須發生一次</span><span class="sxs-lookup"><span data-stu-id="e54bb-113">Must occur at least once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="e54bb-114">父元素</span><span class="sxs-lookup"><span data-stu-id="e54bb-114">Parent elements</span></span>



| <span data-ttu-id="e54bb-115">元素</span><span class="sxs-lookup"><span data-stu-id="e54bb-115">Element</span></span>                                                                     |
|-----------------------------------------------------------------------------|
| [<span data-ttu-id="e54bb-116">**DropDownGallery**</span><span class="sxs-lookup"><span data-stu-id="e54bb-116">**DropDownGallery**</span></span>](windowsribbon-element-dropdowngallery.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="e54bb-117">備註</span><span class="sxs-lookup"><span data-stu-id="e54bb-117">Remarks</span></span>

<span data-ttu-id="e54bb-118">必要。</span><span class="sxs-lookup"><span data-stu-id="e54bb-118">Required.</span></span>

<span data-ttu-id="e54bb-119">針對每個 [**DropDownGallery**](windowsribbon-element-dropdowngallery.md) 元素，必須剛好一次出現。</span><span class="sxs-lookup"><span data-stu-id="e54bb-119">Must occur exactly once for each [**DropDownGallery**](windowsribbon-element-dropdowngallery.md) element.</span></span>

## <a name="examples"></a><span data-ttu-id="e54bb-120">範例</span><span class="sxs-lookup"><span data-stu-id="e54bb-120">Examples</span></span>

<span data-ttu-id="e54bb-121">下列範例示範 **DropDownGallery. MenuGroups** 元素的基本標記。</span><span class="sxs-lookup"><span data-stu-id="e54bb-121">The following example demonstrates the basic markup for the **DropDownGallery.MenuGroups** element.</span></span>

<span data-ttu-id="e54bb-122">這段程式碼會在 [下拉式清單庫](windowsribbon-controls-dropdowngallery.md)命令空間中顯示 **DropDownGallery. MenuGroups** 控制項宣告。</span><span class="sxs-lookup"><span data-stu-id="e54bb-122">This section of code shows the **DropDownGallery.MenuGroups** control declaration in a [Drop-Down Gallery](windowsribbon-controls-dropdowngallery.md) Command Space.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="e54bb-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="e54bb-123">Requirements</span></span>



| <span data-ttu-id="e54bb-124">需求</span><span class="sxs-lookup"><span data-stu-id="e54bb-124">Requirement</span></span> | <span data-ttu-id="e54bb-125">值</span><span class="sxs-lookup"><span data-stu-id="e54bb-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="e54bb-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e54bb-126">Minimum supported client</span></span><br/> | <span data-ttu-id="e54bb-127">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e54bb-127">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="e54bb-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e54bb-128">Minimum supported server</span></span><br/> | <span data-ttu-id="e54bb-129">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e54bb-129">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e54bb-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e54bb-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e54bb-131">**下拉式圖庫控制項**</span><span class="sxs-lookup"><span data-stu-id="e54bb-131">**Drop-Down Gallery control**</span></span>](windowsribbon-element-dropdowngallery.md)
</dt> <dt>

[<span data-ttu-id="e54bb-132">使用資源庫</span><span class="sxs-lookup"><span data-stu-id="e54bb-132">Working with Galleries</span></span>](ribbon-controls-galleries.md)
</dt> </dl>

 

 





