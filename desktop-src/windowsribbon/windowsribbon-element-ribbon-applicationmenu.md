---
title: ApplicationMenu 屬性
description: 表示應用程式功能表。 |ApplicationMenu 屬性
ms.assetid: 6945e976-8ac8-40fa-8e71-31812871b496
keywords:
- ApplicationMenu 屬性視窗功能區
topic_type:
- apiref
api_name:
- Ribbon.ApplicationMenu
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 71263a19057d3f66747b1a40aaa2d0a46528e9b6
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "106986068"
---
# <a name="ribbonapplicationmenu-property"></a><span data-ttu-id="11f50-105">ApplicationMenu 屬性</span><span class="sxs-lookup"><span data-stu-id="11f50-105">Ribbon.ApplicationMenu property</span></span>

<span data-ttu-id="11f50-106">表示應用程式功能表。</span><span class="sxs-lookup"><span data-stu-id="11f50-106">Represents the Application Menu.</span></span>

## <a name="usage"></a><span data-ttu-id="11f50-107">使用方式</span><span class="sxs-lookup"><span data-stu-id="11f50-107">Usage</span></span>

``` syntax
<Ribbon.ApplicationMenu>
  child elements
</Ribbon.ApplicationMenu>
```

## <a name="attributes"></a><span data-ttu-id="11f50-108">屬性</span><span class="sxs-lookup"><span data-stu-id="11f50-108">Attributes</span></span>

<span data-ttu-id="11f50-109">沒有任何屬性。</span><span class="sxs-lookup"><span data-stu-id="11f50-109">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="11f50-110">子元素</span><span class="sxs-lookup"><span data-stu-id="11f50-110">Child elements</span></span>



| <span data-ttu-id="11f50-111">元素</span><span class="sxs-lookup"><span data-stu-id="11f50-111">Element</span></span>                                                                     | <span data-ttu-id="11f50-112">描述</span><span class="sxs-lookup"><span data-stu-id="11f50-112">Description</span></span>                                    |
|-----------------------------------------------------------------------------|------------------------------------------------|
| [<span data-ttu-id="11f50-113">**ApplicationMenu**</span><span class="sxs-lookup"><span data-stu-id="11f50-113">**ApplicationMenu**</span></span>](windowsribbon-element-applicationmenu.md)<br/> | <span data-ttu-id="11f50-114">必須剛好發生一次</span><span class="sxs-lookup"><span data-stu-id="11f50-114">Must occur exactly once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="11f50-115">父元素</span><span class="sxs-lookup"><span data-stu-id="11f50-115">Parent elements</span></span>



| <span data-ttu-id="11f50-116">元素</span><span class="sxs-lookup"><span data-stu-id="11f50-116">Element</span></span>                                                   |
|-----------------------------------------------------------|
| [<span data-ttu-id="11f50-117">**功能區**</span><span class="sxs-lookup"><span data-stu-id="11f50-117">**Ribbon**</span></span>](windowsribbon-element-ribbon.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="11f50-118">備註</span><span class="sxs-lookup"><span data-stu-id="11f50-118">Remarks</span></span>

<span data-ttu-id="11f50-119">必要。</span><span class="sxs-lookup"><span data-stu-id="11f50-119">Required.</span></span>

<span data-ttu-id="11f50-120">每個 [**功能區**](windowsribbon-element-ribbon.md)最多可能會發生一次。</span><span class="sxs-lookup"><span data-stu-id="11f50-120">May occur at most once for each [**Ribbon**](windowsribbon-element-ribbon.md).</span></span>

## <a name="examples"></a><span data-ttu-id="11f50-121">範例</span><span class="sxs-lookup"><span data-stu-id="11f50-121">Examples</span></span>

<span data-ttu-id="11f50-122">下列範例示範 **ApplicationMenu** 元素的基本標記。</span><span class="sxs-lookup"><span data-stu-id="11f50-122">The following example demonstrates the basic markup for the **Ribbon.ApplicationMenu** element.</span></span>

<span data-ttu-id="11f50-123">這段程式碼會顯示 **ApplicationMenu** 控制項宣告。</span><span class="sxs-lookup"><span data-stu-id="11f50-123">This section of code shows the **Ribbon.ApplicationMenu** control declaration.</span></span>


```XML
<!-- Control declarations for Application Menu items. -->
<Ribbon.ApplicationMenu>
  <ApplicationMenu CommandName="cmdFileMenu">
    <!-- Most recently used items collection. -->
    <ApplicationMenu.RecentItems>
      <RecentItems CommandName="cmdMRUItems"/>
    </ApplicationMenu.RecentItems>
    <!-- Menu items collection. -->
    <MenuGroup>
      <Button CommandName="cmdNew" />
      <Button CommandName="cmdOpen" />
      <Button CommandName="cmdSave" />
    </MenuGroup>
    <MenuGroup>
      <Button CommandName="cmdPrint" />
      <Button CommandName="cmdExit" />
    </MenuGroup>
  </ApplicationMenu>
</Ribbon.ApplicationMenu>
```



## <a name="requirements"></a><span data-ttu-id="11f50-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="11f50-124">Requirements</span></span>



| <span data-ttu-id="11f50-125">需求</span><span class="sxs-lookup"><span data-stu-id="11f50-125">Requirement</span></span> | <span data-ttu-id="11f50-126">值</span><span class="sxs-lookup"><span data-stu-id="11f50-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="11f50-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="11f50-127">Minimum supported client</span></span><br/> | <span data-ttu-id="11f50-128">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="11f50-128">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="11f50-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="11f50-129">Minimum supported server</span></span><br/> | <span data-ttu-id="11f50-130">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="11f50-130">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



 

 





