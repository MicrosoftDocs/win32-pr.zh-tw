---
description: 指定產生的函式中是否包含用來傳遞錯誤資訊的參數。
ms.assetid: aba78d50-f884-416a-b022-bb03416aad11
title: faultInfo 元素
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e3788af9aeb31d1ed84522bc6b177143ec0607b2
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/26/2021
ms.locfileid: "107995855"
---
# <a name="faultinfo-element"></a><span data-ttu-id="ed5d5-103">faultInfo 元素</span><span class="sxs-lookup"><span data-stu-id="ed5d5-103">faultInfo element</span></span>

<span data-ttu-id="ed5d5-104">指定產生的函式中是否包含用來傳遞錯誤資訊的參數。</span><span class="sxs-lookup"><span data-stu-id="ed5d5-104">Specifies whether parameters used to pass fault information are included in generated functions.</span></span>

## <a name="usage"></a><span data-ttu-id="ed5d5-105">使用方式</span><span class="sxs-lookup"><span data-stu-id="ed5d5-105">Usage</span></span>

``` syntax
<faultInfo/>
```

## <a name="attributes"></a><span data-ttu-id="ed5d5-106">屬性</span><span class="sxs-lookup"><span data-stu-id="ed5d5-106">Attributes</span></span>

<span data-ttu-id="ed5d5-107">沒有任何屬性。</span><span class="sxs-lookup"><span data-stu-id="ed5d5-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="ed5d5-108">子元素</span><span class="sxs-lookup"><span data-stu-id="ed5d5-108">Child elements</span></span>

<span data-ttu-id="ed5d5-109">沒有任何子項目。</span><span class="sxs-lookup"><span data-stu-id="ed5d5-109">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="ed5d5-110">父元素</span><span class="sxs-lookup"><span data-stu-id="ed5d5-110">Parent elements</span></span>



| <span data-ttu-id="ed5d5-111">元素</span><span class="sxs-lookup"><span data-stu-id="ed5d5-111">Element</span></span>                                                                         | <span data-ttu-id="ed5d5-112">描述</span><span class="sxs-lookup"><span data-stu-id="ed5d5-112">Description</span></span>                                                                                                |
|---------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ed5d5-113">**functionDeclarations**</span><span class="sxs-lookup"><span data-stu-id="ed5d5-113">**functionDeclarations**</span></span>](functiondeclarations.md)<br/>                 | <span data-ttu-id="ed5d5-114">針對埠類型作業產生 proxy 函式的實作為宣告。</span><span class="sxs-lookup"><span data-stu-id="ed5d5-114">Generates implementation declarations for proxy functions for port type operations.</span></span><br/> <br/> |
| [<span data-ttu-id="ed5d5-115">**idlFunctionDeclarations**</span><span class="sxs-lookup"><span data-stu-id="ed5d5-115">**idlFunctionDeclarations**</span></span>](idlfunctiondeclarations.md)<br/>           | <span data-ttu-id="ed5d5-116">針對埠類型作業產生 proxy 函式的 IDL 宣告。</span><span class="sxs-lookup"><span data-stu-id="ed5d5-116">Generates IDL declarations for proxy functions for port type operations.</span></span><br/> <br/>            |
| [<span data-ttu-id="ed5d5-117">**proxyFunctionImplementations**</span><span class="sxs-lookup"><span data-stu-id="ed5d5-117">**proxyFunctionImplementations**</span></span>](proxyfunctionimplementations.md)<br/> | <span data-ttu-id="ed5d5-118">針對埠類型作業產生 proxy 函式的執行。</span><span class="sxs-lookup"><span data-stu-id="ed5d5-118">Generates implementations for proxy functions for port type operations.</span></span><br/> <br/>             |
| [<span data-ttu-id="ed5d5-119">**stubDefinitions**</span><span class="sxs-lookup"><span data-stu-id="ed5d5-119">**stubDefinitions**</span></span>](stubdefinitions.md)<br/>                           | <span data-ttu-id="ed5d5-120">針對埠類型作業產生存根函式的實作為。</span><span class="sxs-lookup"><span data-stu-id="ed5d5-120">Generates implementations for stub functions for port type operations.</span></span><br/> <br/>              |



## <a name="remarks"></a><span data-ttu-id="ed5d5-121">備註</span><span class="sxs-lookup"><span data-stu-id="ed5d5-121">Remarks</span></span>

<span data-ttu-id="ed5d5-122">可能的值為 1 (包含的錯誤參數) 和 0 (排除) 的錯誤參數。</span><span class="sxs-lookup"><span data-stu-id="ed5d5-122">Possible values are 1 (fault parameters included) and 0 (fault parameters excluded).</span></span> <span data-ttu-id="ed5d5-123">預設會排除錯誤參數。</span><span class="sxs-lookup"><span data-stu-id="ed5d5-123">By default, fault parameters are excluded.</span></span>

## <a name="element-information"></a><span data-ttu-id="ed5d5-124">項目資訊</span><span class="sxs-lookup"><span data-stu-id="ed5d5-124">Element information</span></span>



| <span data-ttu-id="ed5d5-125">標籤</span><span class="sxs-lookup"><span data-stu-id="ed5d5-125">Label</span></span> | <span data-ttu-id="ed5d5-126">值</span><span class="sxs-lookup"><span data-stu-id="ed5d5-126">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="ed5d5-127">最低支援系統</span><span class="sxs-lookup"><span data-stu-id="ed5d5-127">Minimum supported system</span></span><br/> | <span data-ttu-id="ed5d5-128">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ed5d5-128">Windows Vista</span></span> |
| <span data-ttu-id="ed5d5-129">可以是空的</span><span class="sxs-lookup"><span data-stu-id="ed5d5-129">Can be empty</span></span>                        | <span data-ttu-id="ed5d5-130">是</span><span class="sxs-lookup"><span data-stu-id="ed5d5-130">Yes</span></span>           |



 

 




