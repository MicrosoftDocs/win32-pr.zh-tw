---
title: Application 項目
description: 表示 Windows 功能區架構標記規格中的最上層元素。
ms.assetid: 05396d8b-fbd1-40bb-8d0f-8ac11506e7db
keywords:
- 應用程式元素視窗功能區
topic_type:
- apiref
api_name:
- Application
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9b116879a918ca0437c7f2bdd201ef4ffd6d3c61
ms.sourcegitcommit: 3d718d8f69d3f86eaecf94c5705d761c5a9ef4a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/20/2020
ms.locfileid: "103684211"
---
# <a name="application-element"></a><span data-ttu-id="b3d28-104">Application 項目</span><span class="sxs-lookup"><span data-stu-id="b3d28-104">Application element</span></span>

<span data-ttu-id="b3d28-105">表示 Windows 功能區架構標記規格中的最上層元素。</span><span class="sxs-lookup"><span data-stu-id="b3d28-105">Represents the top-level element in the Windows Ribbon framework markup specification.</span></span>

## <a name="usage"></a><span data-ttu-id="b3d28-106">使用方式</span><span class="sxs-lookup"><span data-stu-id="b3d28-106">Usage</span></span>

``` syntax
<Application
  xmlns = "xs:string">
  child elements
</Application>
```

## <a name="attributes"></a><span data-ttu-id="b3d28-107">屬性</span><span class="sxs-lookup"><span data-stu-id="b3d28-107">Attributes</span></span>



| <span data-ttu-id="b3d28-108">屬性</span><span class="sxs-lookup"><span data-stu-id="b3d28-108">Attribute</span></span>            | <span data-ttu-id="b3d28-109">類型</span><span class="sxs-lookup"><span data-stu-id="b3d28-109">Type</span></span>                 | <span data-ttu-id="b3d28-110">必要</span><span class="sxs-lookup"><span data-stu-id="b3d28-110">Required</span></span>       | <span data-ttu-id="b3d28-111">描述</span><span class="sxs-lookup"><span data-stu-id="b3d28-111">Description</span></span>                                                                                                                                                                                                       |
|----------------------|----------------------|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b3d28-112">**xmlns**</span><span class="sxs-lookup"><span data-stu-id="b3d28-112">**xmlns**</span></span><br/> | <span data-ttu-id="b3d28-113">xs:string</span><span class="sxs-lookup"><span data-stu-id="b3d28-113">xs:string</span></span><br/> | <span data-ttu-id="b3d28-114">Yes</span><span class="sxs-lookup"><span data-stu-id="b3d28-114">Yes</span></span><br/> | <dt>`http://schemas.microsoft.com/windows/2009/Ribbon`<br/> </dt> <dd> <span data-ttu-id="b3d28-115">功能區標記命名空間系結的 URI。</span><span class="sxs-lookup"><span data-stu-id="b3d28-115">The URI for the Ribbon markup namespace binding.</span></span> <br/> </dd> </dl> |



## <a name="child-elements"></a><span data-ttu-id="b3d28-116">子元素</span><span class="sxs-lookup"><span data-stu-id="b3d28-116">Child elements</span></span>



| <span data-ttu-id="b3d28-117">元素</span><span class="sxs-lookup"><span data-stu-id="b3d28-117">Element</span></span>                                                                               | <span data-ttu-id="b3d28-118">描述</span><span class="sxs-lookup"><span data-stu-id="b3d28-118">Description</span></span>                                    |
|---------------------------------------------------------------------------------------|------------------------------------------------|
| [<span data-ttu-id="b3d28-119">**應用程式。命令**</span><span class="sxs-lookup"><span data-stu-id="b3d28-119">**Application.Commands**</span></span>](windowsribbon-element-application-commands.md)<br/> | <span data-ttu-id="b3d28-120">最多可能發生一次</span><span class="sxs-lookup"><span data-stu-id="b3d28-120">May occur at most once</span></span><br/> <br/>  |
| [<span data-ttu-id="b3d28-121">**應用程式。 Views**</span><span class="sxs-lookup"><span data-stu-id="b3d28-121">**Application.Views**</span></span>](windowsribbon-element-application-views.md)<br/>       | <span data-ttu-id="b3d28-122">必須剛好發生一次</span><span class="sxs-lookup"><span data-stu-id="b3d28-122">Must occur exactly once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="b3d28-123">父元素</span><span class="sxs-lookup"><span data-stu-id="b3d28-123">Parent elements</span></span>

<span data-ttu-id="b3d28-124">沒有父元素。</span><span class="sxs-lookup"><span data-stu-id="b3d28-124">There are no parent elements.</span></span>

## <a name="remarks"></a><span data-ttu-id="b3d28-125">備註</span><span class="sxs-lookup"><span data-stu-id="b3d28-125">Remarks</span></span>

<span data-ttu-id="b3d28-126">必要。</span><span class="sxs-lookup"><span data-stu-id="b3d28-126">Required.</span></span>

<span data-ttu-id="b3d28-127">必須剛好一次就能作為所有功能區標記的容器。</span><span class="sxs-lookup"><span data-stu-id="b3d28-127">Must occur exactly once as the container for all of the Ribbon markup.</span></span>

<span data-ttu-id="b3d28-128">**應用程式** 元素的子項目必須以指定的順序發生：</span><span class="sxs-lookup"><span data-stu-id="b3d28-128">The child elements of the **Application** element must occur in the specified order:</span></span>

1.  [<span data-ttu-id="b3d28-129">**應用程式。命令**</span><span class="sxs-lookup"><span data-stu-id="b3d28-129">**Application.Commands**</span></span>](windowsribbon-element-application-commands.md)
2.  [<span data-ttu-id="b3d28-130">**應用程式。 Views**</span><span class="sxs-lookup"><span data-stu-id="b3d28-130">**Application.Views**</span></span>](windowsribbon-element-application-views.md)

## <a name="examples"></a><span data-ttu-id="b3d28-131">範例</span><span class="sxs-lookup"><span data-stu-id="b3d28-131">Examples</span></span>

<span data-ttu-id="b3d28-132">下列範例顯示 **應用程式** 元素宣告。</span><span class="sxs-lookup"><span data-stu-id="b3d28-132">The following example shows an **Application** element declaration.</span></span>


```XML
<Application xmlns="http://schemas.microsoft.com/windows/2009/Ribbon">
...
</Application>
```



## <a name="element-information"></a><span data-ttu-id="b3d28-133">項目資訊</span><span class="sxs-lookup"><span data-stu-id="b3d28-133">Element information</span></span>



|                                     |           |
|-------------------------------------|-----------|
| <span data-ttu-id="b3d28-134">最低支援系統</span><span class="sxs-lookup"><span data-stu-id="b3d28-134">Minimum supported system</span></span><br/> | <span data-ttu-id="b3d28-135">Windows 7</span><span class="sxs-lookup"><span data-stu-id="b3d28-135">Windows 7</span></span> |
| <span data-ttu-id="b3d28-136">可以是空的</span><span class="sxs-lookup"><span data-stu-id="b3d28-136">Can be empty</span></span>                        | <span data-ttu-id="b3d28-137">否</span><span class="sxs-lookup"><span data-stu-id="b3d28-137">No</span></span>        |



## <a name="see-also"></a><span data-ttu-id="b3d28-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b3d28-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b3d28-139">使用功能區標記宣告命令和控制項</span><span class="sxs-lookup"><span data-stu-id="b3d28-139">Declaring Commands and Controls with Ribbon Markup</span></span>](windowsribbon-schema.md)
</dt> </dl>

 

 





