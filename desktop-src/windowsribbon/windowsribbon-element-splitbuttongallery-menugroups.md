---
title: SplitButtonGallery. MenuGroups 屬性
description: 代表 SplitButtonGallery 控制項中一組下拉式功能表專案的容器。
ms.assetid: e30fcf9a-488b-423a-8bc4-fccbc78f74de
keywords:
- SplitButtonGallery. MenuGroups 屬性 Windows 功能區
topic_type:
- apiref
api_name:
- SplitButtonGallery.MenuGroups
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72176e7d7e79b076c3a7cf4d1fd847aa4f4e0561
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103643"
---
# <a name="splitbuttongallerymenugroups-property"></a><span data-ttu-id="c517b-104">SplitButtonGallery. MenuGroups 屬性</span><span class="sxs-lookup"><span data-stu-id="c517b-104">SplitButtonGallery.MenuGroups property</span></span>

<span data-ttu-id="c517b-105">代表 [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) 控制項中一組下拉式功能表專案的容器。</span><span class="sxs-lookup"><span data-stu-id="c517b-105">Represents a container for a set of drop-down menu items in a [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) control.</span></span>

## <a name="usage"></a><span data-ttu-id="c517b-106">使用方式</span><span class="sxs-lookup"><span data-stu-id="c517b-106">Usage</span></span>

``` syntax
<SplitButtonGallery.MenuGroups>
  child elements
</SplitButtonGallery.MenuGroups>
```

## <a name="attributes"></a><span data-ttu-id="c517b-107">屬性</span><span class="sxs-lookup"><span data-stu-id="c517b-107">Attributes</span></span>

<span data-ttu-id="c517b-108">沒有任何屬性。</span><span class="sxs-lookup"><span data-stu-id="c517b-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="c517b-109">子元素</span><span class="sxs-lookup"><span data-stu-id="c517b-109">Child elements</span></span>



| <span data-ttu-id="c517b-110">元素</span><span class="sxs-lookup"><span data-stu-id="c517b-110">Element</span></span>                                                         | <span data-ttu-id="c517b-111">描述</span><span class="sxs-lookup"><span data-stu-id="c517b-111">Description</span></span>                                     |
|-----------------------------------------------------------------|-------------------------------------------------|
| [<span data-ttu-id="c517b-112">**MenuGroup**</span><span class="sxs-lookup"><span data-stu-id="c517b-112">**MenuGroup**</span></span>](windowsribbon-element-menugroup.md)<br/> | <span data-ttu-id="c517b-113">至少必須發生一次</span><span class="sxs-lookup"><span data-stu-id="c517b-113">Must occur at least once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="c517b-114">父元素</span><span class="sxs-lookup"><span data-stu-id="c517b-114">Parent elements</span></span>



| <span data-ttu-id="c517b-115">元素</span><span class="sxs-lookup"><span data-stu-id="c517b-115">Element</span></span>                                                                           |
|-----------------------------------------------------------------------------------|
| [<span data-ttu-id="c517b-116">**SplitButtonGallery**</span><span class="sxs-lookup"><span data-stu-id="c517b-116">**SplitButtonGallery**</span></span>](windowsribbon-element-splitbuttongallery.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="c517b-117">備註</span><span class="sxs-lookup"><span data-stu-id="c517b-117">Remarks</span></span>

<span data-ttu-id="c517b-118">必要。</span><span class="sxs-lookup"><span data-stu-id="c517b-118">Required.</span></span>

<span data-ttu-id="c517b-119">針對每個 [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) 元素，必須剛好一次出現。</span><span class="sxs-lookup"><span data-stu-id="c517b-119">Must occur exactly once for each [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) element.</span></span>

## <a name="examples"></a><span data-ttu-id="c517b-120">範例</span><span class="sxs-lookup"><span data-stu-id="c517b-120">Examples</span></span>

<span data-ttu-id="c517b-121">下列範例示範 **SplitButtonGallery. MenuGroups** 元素的基本標記。</span><span class="sxs-lookup"><span data-stu-id="c517b-121">The following example demonstrates the basic markup for the **SplitButtonGallery.MenuGroups** element.</span></span>

<span data-ttu-id="c517b-122">這段程式碼會顯示 **SplitButtonGallery MenuGroups** 控制項宣告。</span><span class="sxs-lookup"><span data-stu-id="c517b-122">This section of code shows the **SplitButtonGallery.MenuGroups** control declaration.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="c517b-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="c517b-123">Requirements</span></span>



| <span data-ttu-id="c517b-124">需求</span><span class="sxs-lookup"><span data-stu-id="c517b-124">Requirement</span></span> | <span data-ttu-id="c517b-125">值</span><span class="sxs-lookup"><span data-stu-id="c517b-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="c517b-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c517b-126">Minimum supported client</span></span><br/> | <span data-ttu-id="c517b-127">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c517b-127">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="c517b-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c517b-128">Minimum supported server</span></span><br/> | <span data-ttu-id="c517b-129">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c517b-129">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c517b-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c517b-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c517b-131">分割按鈕資源庫控制項</span><span class="sxs-lookup"><span data-stu-id="c517b-131">Split Button Gallery control</span></span>](windowsribbon-controls-splitbuttongallery.md)
</dt> <dt>

[<span data-ttu-id="c517b-132">使用資源庫</span><span class="sxs-lookup"><span data-stu-id="c517b-132">Working with Galleries</span></span>](ribbon-controls-galleries.md)
</dt> </dl>

 

 





