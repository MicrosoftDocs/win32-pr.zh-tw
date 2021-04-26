---
description: 指定產生的函數中是否包含相關事件。
ms.assetid: 23ca463c-b305-496b-a1e3-58dbb793f17e
title: events 元素
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6883f1bcca9b62c3d8b60ca86f47b0e688d513c2
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/26/2021
ms.locfileid: "107995925"
---
# <a name="events-element"></a><span data-ttu-id="8d637-103">events 元素</span><span class="sxs-lookup"><span data-stu-id="8d637-103">events element</span></span>

<span data-ttu-id="8d637-104">指定產生的函數中是否包含相關事件。</span><span class="sxs-lookup"><span data-stu-id="8d637-104">Specifies whether related events are included in the generated functions.</span></span>

## <a name="usage"></a><span data-ttu-id="8d637-105">使用方式</span><span class="sxs-lookup"><span data-stu-id="8d637-105">Usage</span></span>

``` syntax
<events/>
```

## <a name="attributes"></a><span data-ttu-id="8d637-106">屬性</span><span class="sxs-lookup"><span data-stu-id="8d637-106">Attributes</span></span>

<span data-ttu-id="8d637-107">沒有任何屬性。</span><span class="sxs-lookup"><span data-stu-id="8d637-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="8d637-108">子元素</span><span class="sxs-lookup"><span data-stu-id="8d637-108">Child elements</span></span>

<span data-ttu-id="8d637-109">沒有任何子項目。</span><span class="sxs-lookup"><span data-stu-id="8d637-109">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="8d637-110">父元素</span><span class="sxs-lookup"><span data-stu-id="8d637-110">Parent elements</span></span>



| <span data-ttu-id="8d637-111">元素</span><span class="sxs-lookup"><span data-stu-id="8d637-111">Element</span></span>                                                                         | <span data-ttu-id="8d637-112">描述</span><span class="sxs-lookup"><span data-stu-id="8d637-112">Description</span></span>                                                                                                |
|---------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8d637-113">**functionDeclarations**</span><span class="sxs-lookup"><span data-stu-id="8d637-113">**functionDeclarations**</span></span>](functiondeclarations.md)<br/>                 | <span data-ttu-id="8d637-114">針對埠類型作業產生 proxy 函式的實作為宣告。</span><span class="sxs-lookup"><span data-stu-id="8d637-114">Generates implementation declarations for proxy functions for port type operations.</span></span><br/> <br/> |
| [<span data-ttu-id="8d637-115">**idlFunctionDeclarations**</span><span class="sxs-lookup"><span data-stu-id="8d637-115">**idlFunctionDeclarations**</span></span>](idlfunctiondeclarations.md)<br/>           | <span data-ttu-id="8d637-116">針對埠類型作業產生 proxy 函式的 IDL 宣告。</span><span class="sxs-lookup"><span data-stu-id="8d637-116">Generates IDL declarations for proxy functions for port type operations.</span></span><br/> <br/>            |
| [<span data-ttu-id="8d637-117">**proxyFunctionImplementations**</span><span class="sxs-lookup"><span data-stu-id="8d637-117">**proxyFunctionImplementations**</span></span>](proxyfunctionimplementations.md)<br/> | <span data-ttu-id="8d637-118">針對埠類型作業產生 proxy 函式的執行。</span><span class="sxs-lookup"><span data-stu-id="8d637-118">Generates implementations for proxy functions for port type operations.</span></span><br/> <br/>             |
| [<span data-ttu-id="8d637-119">**stubDeclarations**</span><span class="sxs-lookup"><span data-stu-id="8d637-119">**stubDeclarations**</span></span>](stubdeclarations.md)<br/>                         | <span data-ttu-id="8d637-120">針對埠類型作業產生存根函式的宣告。</span><span class="sxs-lookup"><span data-stu-id="8d637-120">Generates declarations for stub functions for port type operations.</span></span><br/> <br/>                 |
| [<span data-ttu-id="8d637-121">**stubDefinitions**</span><span class="sxs-lookup"><span data-stu-id="8d637-121">**stubDefinitions**</span></span>](stubdefinitions.md)<br/>                           | <span data-ttu-id="8d637-122">針對埠類型作業產生存根函式的實作為。</span><span class="sxs-lookup"><span data-stu-id="8d637-122">Generates implementations for stub functions for port type operations.</span></span><br/> <br/>              |



## <a name="remarks"></a><span data-ttu-id="8d637-123">備註</span><span class="sxs-lookup"><span data-stu-id="8d637-123">Remarks</span></span>

<span data-ttu-id="8d637-124">可能的值為 1 (包含的事件) 和 0 (預設值) 排除的事件。</span><span class="sxs-lookup"><span data-stu-id="8d637-124">Possible values are 1 (events included) and 0 (default, events excluded).</span></span>

## <a name="element-information"></a><span data-ttu-id="8d637-125">項目資訊</span><span class="sxs-lookup"><span data-stu-id="8d637-125">Element information</span></span>



| <span data-ttu-id="8d637-126">標籤</span><span class="sxs-lookup"><span data-stu-id="8d637-126">Label</span></span> | <span data-ttu-id="8d637-127">值</span><span class="sxs-lookup"><span data-stu-id="8d637-127">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="8d637-128">最低支援系統</span><span class="sxs-lookup"><span data-stu-id="8d637-128">Minimum supported system</span></span><br/> | <span data-ttu-id="8d637-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8d637-129">Windows Vista</span></span> |
| <span data-ttu-id="8d637-130">可以是空的</span><span class="sxs-lookup"><span data-stu-id="8d637-130">Can be empty</span></span>                        | <span data-ttu-id="8d637-131">是</span><span class="sxs-lookup"><span data-stu-id="8d637-131">Yes</span></span>           |



 

 




