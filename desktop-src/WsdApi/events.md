---
description: 指定產生的函數中是否包含相關事件。
ms.assetid: 23ca463c-b305-496b-a1e3-58dbb793f17e
title: events 元素
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2571cc8e9820ca38beb649b3c227fb1c01f61c50
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192177"
---
# <a name="events-element"></a><span data-ttu-id="15748-103">events 元素</span><span class="sxs-lookup"><span data-stu-id="15748-103">events element</span></span>

<span data-ttu-id="15748-104">指定產生的函數中是否包含相關事件。</span><span class="sxs-lookup"><span data-stu-id="15748-104">Specifies whether related events are included in the generated functions.</span></span>

## <a name="usage"></a><span data-ttu-id="15748-105">使用方式</span><span class="sxs-lookup"><span data-stu-id="15748-105">Usage</span></span>

``` syntax
<events/>
```

## <a name="attributes"></a><span data-ttu-id="15748-106">屬性</span><span class="sxs-lookup"><span data-stu-id="15748-106">Attributes</span></span>

<span data-ttu-id="15748-107">沒有任何屬性。</span><span class="sxs-lookup"><span data-stu-id="15748-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="15748-108">子元素</span><span class="sxs-lookup"><span data-stu-id="15748-108">Child elements</span></span>

<span data-ttu-id="15748-109">沒有任何子項目。</span><span class="sxs-lookup"><span data-stu-id="15748-109">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="15748-110">父元素</span><span class="sxs-lookup"><span data-stu-id="15748-110">Parent elements</span></span>



| <span data-ttu-id="15748-111">元素</span><span class="sxs-lookup"><span data-stu-id="15748-111">Element</span></span>                                                                         | <span data-ttu-id="15748-112">描述</span><span class="sxs-lookup"><span data-stu-id="15748-112">Description</span></span>                                                                                                |
|---------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="15748-113">**functionDeclarations**</span><span class="sxs-lookup"><span data-stu-id="15748-113">**functionDeclarations**</span></span>](functiondeclarations.md)<br/>                 | <span data-ttu-id="15748-114">針對埠類型作業產生 proxy 函式的實作為宣告。</span><span class="sxs-lookup"><span data-stu-id="15748-114">Generates implementation declarations for proxy functions for port type operations.</span></span><br/> <br/> |
| [<span data-ttu-id="15748-115">**idlFunctionDeclarations**</span><span class="sxs-lookup"><span data-stu-id="15748-115">**idlFunctionDeclarations**</span></span>](idlfunctiondeclarations.md)<br/>           | <span data-ttu-id="15748-116">針對埠類型作業產生 proxy 函式的 IDL 宣告。</span><span class="sxs-lookup"><span data-stu-id="15748-116">Generates IDL declarations for proxy functions for port type operations.</span></span><br/> <br/>            |
| [<span data-ttu-id="15748-117">**proxyFunctionImplementations**</span><span class="sxs-lookup"><span data-stu-id="15748-117">**proxyFunctionImplementations**</span></span>](proxyfunctionimplementations.md)<br/> | <span data-ttu-id="15748-118">針對埠類型作業產生 proxy 函式的執行。</span><span class="sxs-lookup"><span data-stu-id="15748-118">Generates implementations for proxy functions for port type operations.</span></span><br/> <br/>             |
| [<span data-ttu-id="15748-119">**stubDeclarations**</span><span class="sxs-lookup"><span data-stu-id="15748-119">**stubDeclarations**</span></span>](stubdeclarations.md)<br/>                         | <span data-ttu-id="15748-120">針對埠類型作業產生存根函式的宣告。</span><span class="sxs-lookup"><span data-stu-id="15748-120">Generates declarations for stub functions for port type operations.</span></span><br/> <br/>                 |
| [<span data-ttu-id="15748-121">**stubDefinitions**</span><span class="sxs-lookup"><span data-stu-id="15748-121">**stubDefinitions**</span></span>](stubdefinitions.md)<br/>                           | <span data-ttu-id="15748-122">針對埠類型作業產生存根函式的實作為。</span><span class="sxs-lookup"><span data-stu-id="15748-122">Generates implementations for stub functions for port type operations.</span></span><br/> <br/>              |



## <a name="remarks"></a><span data-ttu-id="15748-123">備註</span><span class="sxs-lookup"><span data-stu-id="15748-123">Remarks</span></span>

<span data-ttu-id="15748-124">可能的值為 1 (包含的事件) 和 0 (預設值) 排除的事件。</span><span class="sxs-lookup"><span data-stu-id="15748-124">Possible values are 1 (events included) and 0 (default, events excluded).</span></span>

## <a name="element-information"></a><span data-ttu-id="15748-125">項目資訊</span><span class="sxs-lookup"><span data-stu-id="15748-125">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="15748-126">最低支援系統</span><span class="sxs-lookup"><span data-stu-id="15748-126">Minimum supported system</span></span><br/> | <span data-ttu-id="15748-127">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="15748-127">Windows Vista</span></span> |
| <span data-ttu-id="15748-128">可以是空的</span><span class="sxs-lookup"><span data-stu-id="15748-128">Can be empty</span></span>                        | <span data-ttu-id="15748-129">是</span><span class="sxs-lookup"><span data-stu-id="15748-129">Yes</span></span>           |



 

 




