---
description: 指定產生的 proxy 函數中是否包含非同步作業。
ms.assetid: 7b57d5c6-589b-4e03-bfcf-1faa671ebd77
title: async 元素
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea04eaa66fbdadfc784650c1a451cebf171f6372
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104027347"
---
# <a name="async-element"></a><span data-ttu-id="4417d-103">async 元素</span><span class="sxs-lookup"><span data-stu-id="4417d-103">async element</span></span>

<span data-ttu-id="4417d-104">指定產生的 proxy 函數中是否包含非同步作業。</span><span class="sxs-lookup"><span data-stu-id="4417d-104">Specifies whether asynchronous operations are included in the generated proxy functions.</span></span>

## <a name="usage"></a><span data-ttu-id="4417d-105">使用方式</span><span class="sxs-lookup"><span data-stu-id="4417d-105">Usage</span></span>

``` syntax
<async/>
```

## <a name="attributes"></a><span data-ttu-id="4417d-106">屬性</span><span class="sxs-lookup"><span data-stu-id="4417d-106">Attributes</span></span>

<span data-ttu-id="4417d-107">沒有任何屬性。</span><span class="sxs-lookup"><span data-stu-id="4417d-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="4417d-108">子元素</span><span class="sxs-lookup"><span data-stu-id="4417d-108">Child elements</span></span>

<span data-ttu-id="4417d-109">沒有任何子項目。</span><span class="sxs-lookup"><span data-stu-id="4417d-109">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="4417d-110">父元素</span><span class="sxs-lookup"><span data-stu-id="4417d-110">Parent elements</span></span>



| <span data-ttu-id="4417d-111">元素</span><span class="sxs-lookup"><span data-stu-id="4417d-111">Element</span></span>                                                                         | <span data-ttu-id="4417d-112">描述</span><span class="sxs-lookup"><span data-stu-id="4417d-112">Description</span></span>                                                                                                |
|---------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4417d-113">**functionDeclarations**</span><span class="sxs-lookup"><span data-stu-id="4417d-113">**functionDeclarations**</span></span>](functiondeclarations.md)<br/>                 | <span data-ttu-id="4417d-114">針對埠類型作業產生 proxy 函式的實作為宣告。</span><span class="sxs-lookup"><span data-stu-id="4417d-114">Generates implementation declarations for proxy functions for port type operations.</span></span><br/> <br/> |
| [<span data-ttu-id="4417d-115">**idlFunctionDeclarations**</span><span class="sxs-lookup"><span data-stu-id="4417d-115">**idlFunctionDeclarations**</span></span>](idlfunctiondeclarations.md)<br/>           | <span data-ttu-id="4417d-116">針對埠類型作業產生 proxy 函式的 IDL 宣告。</span><span class="sxs-lookup"><span data-stu-id="4417d-116">Generates IDL declarations for proxy functions for port type operations.</span></span><br/> <br/>            |
| [<span data-ttu-id="4417d-117">**proxyFunctionImplementations**</span><span class="sxs-lookup"><span data-stu-id="4417d-117">**proxyFunctionImplementations**</span></span>](proxyfunctionimplementations.md)<br/> | <span data-ttu-id="4417d-118">針對埠類型作業產生 proxy 函式的執行。</span><span class="sxs-lookup"><span data-stu-id="4417d-118">Generates implementations for proxy functions for port type operations.</span></span><br/> <br/>             |



## <a name="remarks"></a><span data-ttu-id="4417d-119">備註</span><span class="sxs-lookup"><span data-stu-id="4417d-119">Remarks</span></span>

<span data-ttu-id="4417d-120">可能的值為 1 (包含) 的非同步作業，而 0 (預設值) 排除非同步作業。</span><span class="sxs-lookup"><span data-stu-id="4417d-120">Possible values are 1 (asynchronous operations included) and 0 (default, asynchronous operations excluded).</span></span>

<span data-ttu-id="4417d-121">Proxy 可以有相同作業的非同步和同步版本。</span><span class="sxs-lookup"><span data-stu-id="4417d-121">A proxy can have both asynchronous and synchronous versions of the same operations.</span></span>

## <a name="element-information"></a><span data-ttu-id="4417d-122">項目資訊</span><span class="sxs-lookup"><span data-stu-id="4417d-122">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="4417d-123">最低支援系統</span><span class="sxs-lookup"><span data-stu-id="4417d-123">Minimum supported system</span></span><br/> | <span data-ttu-id="4417d-124">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4417d-124">Windows Vista</span></span> |
| <span data-ttu-id="4417d-125">可以是空的</span><span class="sxs-lookup"><span data-stu-id="4417d-125">Can be empty</span></span>                        | <span data-ttu-id="4417d-126">是</span><span class="sxs-lookup"><span data-stu-id="4417d-126">Yes</span></span>           |



 

 




