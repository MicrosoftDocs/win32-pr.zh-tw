---
description: 指定存根函式所要使用的釋放器類型。
ms.assetid: 58228dfd-1d4b-41e5-b423-a54525021c22
title: 釋放器元素
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3604f0efb366c3f88e2e0828c02344ee75606079
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192178"
---
# <a name="deallocator-element"></a><span data-ttu-id="2226d-103">釋放器元素</span><span class="sxs-lookup"><span data-stu-id="2226d-103">deallocator element</span></span>

<span data-ttu-id="2226d-104">指定存根函式所要使用的釋放器類型。</span><span class="sxs-lookup"><span data-stu-id="2226d-104">Specifies the type of deallocator to be used by a stub function.</span></span>

## <a name="usage"></a><span data-ttu-id="2226d-105">使用方式</span><span class="sxs-lookup"><span data-stu-id="2226d-105">Usage</span></span>

``` syntax
<deallocator/>
```

## <a name="attributes"></a><span data-ttu-id="2226d-106">屬性</span><span class="sxs-lookup"><span data-stu-id="2226d-106">Attributes</span></span>

<span data-ttu-id="2226d-107">沒有任何屬性。</span><span class="sxs-lookup"><span data-stu-id="2226d-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="2226d-108">子元素</span><span class="sxs-lookup"><span data-stu-id="2226d-108">Child elements</span></span>

<span data-ttu-id="2226d-109">沒有任何子項目。</span><span class="sxs-lookup"><span data-stu-id="2226d-109">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="2226d-110">父元素</span><span class="sxs-lookup"><span data-stu-id="2226d-110">Parent elements</span></span>



| <span data-ttu-id="2226d-111">元素</span><span class="sxs-lookup"><span data-stu-id="2226d-111">Element</span></span>                                               | <span data-ttu-id="2226d-112">描述</span><span class="sxs-lookup"><span data-stu-id="2226d-112">Description</span></span>                                                                                   |
|-------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2226d-113">**stubDefinitions**</span><span class="sxs-lookup"><span data-stu-id="2226d-113">**stubDefinitions**</span></span>](stubdefinitions.md)<br/> | <span data-ttu-id="2226d-114">針對埠類型作業產生存根函式的實作為。</span><span class="sxs-lookup"><span data-stu-id="2226d-114">Generates implementations for stub functions for port-type operations.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="2226d-115">備註</span><span class="sxs-lookup"><span data-stu-id="2226d-115">Remarks</span></span>

<span data-ttu-id="2226d-116">釋放器類型應該包含在一對 <deallocator></deallocator> 標記中。</span><span class="sxs-lookup"><span data-stu-id="2226d-116">The deallocator type should be enclosed in a pair of <deallocator></deallocator> tags.</span></span> <span data-ttu-id="2226d-117">下列字串是有效的釋放器值：</span><span class="sxs-lookup"><span data-stu-id="2226d-117">The following strings are valid deallocator values:</span></span>

-   <span data-ttu-id="2226d-118">無</span><span class="sxs-lookup"><span data-stu-id="2226d-118">none</span></span>
-   <span data-ttu-id="2226d-119">WSDFreeLinkedMemory</span><span class="sxs-lookup"><span data-stu-id="2226d-119">WSDFreeLinkedMemory</span></span>
-   <span data-ttu-id="2226d-120">CoTaskMemFree</span><span class="sxs-lookup"><span data-stu-id="2226d-120">CoTaskMemFree</span></span>
-   <span data-ttu-id="2226d-121">free</span><span class="sxs-lookup"><span data-stu-id="2226d-121">free</span></span>
-   <span data-ttu-id="2226d-122">delete</span><span class="sxs-lookup"><span data-stu-id="2226d-122">delete</span></span>
-   <span data-ttu-id="2226d-123">deleteArray</span><span class="sxs-lookup"><span data-stu-id="2226d-123">deleteArray</span></span>
-   <span data-ttu-id="2226d-124">版本</span><span class="sxs-lookup"><span data-stu-id="2226d-124">Release</span></span>

## <a name="element-information"></a><span data-ttu-id="2226d-125">項目資訊</span><span class="sxs-lookup"><span data-stu-id="2226d-125">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="2226d-126">最低支援系統</span><span class="sxs-lookup"><span data-stu-id="2226d-126">Minimum supported system</span></span><br/> | <span data-ttu-id="2226d-127">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2226d-127">Windows Vista</span></span> |
| <span data-ttu-id="2226d-128">可以是空的</span><span class="sxs-lookup"><span data-stu-id="2226d-128">Can be empty</span></span>                        | <span data-ttu-id="2226d-129">是</span><span class="sxs-lookup"><span data-stu-id="2226d-129">Yes</span></span>           |



 

 




