---
description: 指定要產生程式碼的埠類型。
ms.assetid: 8a7762ae-2e39-46e1-b49f-09cae1af9b0d
title: portType 元素
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a98f02fc5a18e330bb5617b52563adc79a039831
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/26/2021
ms.locfileid: "107996535"
---
# <a name="porttype-element"></a><span data-ttu-id="cec1f-103">portType 元素</span><span class="sxs-lookup"><span data-stu-id="cec1f-103">portType element</span></span>

<span data-ttu-id="cec1f-104">指定要產生程式碼的埠類型。</span><span class="sxs-lookup"><span data-stu-id="cec1f-104">Specifies the port type for which code is to be generated.</span></span>

## <a name="usage"></a><span data-ttu-id="cec1f-105">使用方式</span><span class="sxs-lookup"><span data-stu-id="cec1f-105">Usage</span></span>

``` syntax
<portType/>
```

## <a name="attributes"></a><span data-ttu-id="cec1f-106">屬性</span><span class="sxs-lookup"><span data-stu-id="cec1f-106">Attributes</span></span>

<span data-ttu-id="cec1f-107">沒有任何屬性。</span><span class="sxs-lookup"><span data-stu-id="cec1f-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="cec1f-108">子元素</span><span class="sxs-lookup"><span data-stu-id="cec1f-108">Child elements</span></span>

<span data-ttu-id="cec1f-109">沒有任何子項目。</span><span class="sxs-lookup"><span data-stu-id="cec1f-109">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="cec1f-110">父元素</span><span class="sxs-lookup"><span data-stu-id="cec1f-110">Parent elements</span></span>



| <span data-ttu-id="cec1f-111">元素</span><span class="sxs-lookup"><span data-stu-id="cec1f-111">Element</span></span>                                                                                                 | <span data-ttu-id="cec1f-112">描述</span><span class="sxs-lookup"><span data-stu-id="cec1f-112">Description</span></span>                                                                                                                                   |
|---------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="cec1f-113">**functionDeclarations**</span><span class="sxs-lookup"><span data-stu-id="cec1f-113">**functionDeclarations**</span></span>](functiondeclarations.md)<br/>                                         | <span data-ttu-id="cec1f-114">針對埠類型作業產生 proxy 函式的實作為宣告。</span><span class="sxs-lookup"><span data-stu-id="cec1f-114">Generates implementation declarations for proxy functions for port type operations.</span></span><br/> <br/>                                    |
| [<span data-ttu-id="cec1f-115">**idlFunctionDeclarations**</span><span class="sxs-lookup"><span data-stu-id="cec1f-115">**idlFunctionDeclarations**</span></span>](idlfunctiondeclarations.md)<br/>                                   | <span data-ttu-id="cec1f-116">針對埠類型作業產生 proxy 函式的 IDL 宣告。</span><span class="sxs-lookup"><span data-stu-id="cec1f-116">Generates IDL declarations for proxy functions for port type operations.</span></span><br/> <br/>                                               |
| [<span data-ttu-id="cec1f-117">**messageStructureDefinitions**</span><span class="sxs-lookup"><span data-stu-id="cec1f-117">**messageStructureDefinitions**</span></span>](messagestructuredefinitions.md)<br/>                           | <span data-ttu-id="cec1f-118">產生訊息類型的 C 結構定義。</span><span class="sxs-lookup"><span data-stu-id="cec1f-118">Generates C structure definitions for message types.</span></span><br/> <br/>                                                                   |
| [<span data-ttu-id="cec1f-119">**messageTypeDeclarations**</span><span class="sxs-lookup"><span data-stu-id="cec1f-119">**messageTypeDeclarations**</span></span>](messagetypedeclarations.md)<br/>                                   | <span data-ttu-id="cec1f-120">針對訊息類型產生 XML 架構資料表的 C 常數宣告。</span><span class="sxs-lookup"><span data-stu-id="cec1f-120">Generates C constant declarations for XML schema tables for message types.</span></span><br/> <br/>                                             |
| [<span data-ttu-id="cec1f-121">**messageTypeDefinitions**</span><span class="sxs-lookup"><span data-stu-id="cec1f-121">**messageTypeDefinitions**</span></span>](messagetypedefinitions.md)<br/>                                     | <span data-ttu-id="cec1f-122">針對訊息類型產生 XML 架構資料表的 C 常數。</span><span class="sxs-lookup"><span data-stu-id="cec1f-122">Generates C constants for XML schema tables for message types.</span></span><br/> <br/>                                                         |
| [<span data-ttu-id="cec1f-123">**portTypeDeclarations**</span><span class="sxs-lookup"><span data-stu-id="cec1f-123">**portTypeDeclarations**</span></span>](porttypedeclarations.md)<br/>                                         | <span data-ttu-id="cec1f-124">產生埠類型的 C 常數宣告。</span><span class="sxs-lookup"><span data-stu-id="cec1f-124">Generates C constant declarations for port types.</span></span><br/> <br/>                                                                      |
| [<span data-ttu-id="cec1f-125">**portTypeDefinitions**</span><span class="sxs-lookup"><span data-stu-id="cec1f-125">**portTypeDefinitions**</span></span>](porttypedefinitions.md)<br/>                                           | <span data-ttu-id="cec1f-126">產生埠類型的 C 常數。</span><span class="sxs-lookup"><span data-stu-id="cec1f-126">Generates C constants for port types.</span></span><br/> <br/>                                                                                  |
| [<span data-ttu-id="cec1f-127">**proxyFunctionImplementations**</span><span class="sxs-lookup"><span data-stu-id="cec1f-127">**proxyFunctionImplementations**</span></span>](proxyfunctionimplementations.md)<br/>                         | <span data-ttu-id="cec1f-128">針對埠類型作業產生 proxy 函式的執行。</span><span class="sxs-lookup"><span data-stu-id="cec1f-128">Generates implementations for proxy functions for port type operations.</span></span><br/> <br/>                                                |
| [<span data-ttu-id="cec1f-129">**stubDeclarations**</span><span class="sxs-lookup"><span data-stu-id="cec1f-129">**stubDeclarations**</span></span>](stubdeclarations.md)<br/>                                                 | <span data-ttu-id="cec1f-130">針對埠類型作業產生存根函式的宣告。</span><span class="sxs-lookup"><span data-stu-id="cec1f-130">Generates declarations for stub functions for port type operations.</span></span><br/> <br/>                                                    |
| [<span data-ttu-id="cec1f-131">**stubDefinitions**</span><span class="sxs-lookup"><span data-stu-id="cec1f-131">**stubDefinitions**</span></span>](stubdefinitions.md)<br/>                                                   | <span data-ttu-id="cec1f-132">針對埠類型作業產生存根函式的實作為。</span><span class="sxs-lookup"><span data-stu-id="cec1f-132">Generates implementations for stub functions for port type operations.</span></span><br/> <br/>                                                 |
| [<span data-ttu-id="cec1f-133">**subscriptionFunctionDeclarations**</span><span class="sxs-lookup"><span data-stu-id="cec1f-133">**subscriptionFunctionDeclarations**</span></span>](subscriptionfunctiondeclarations.md)<br/>                 | <span data-ttu-id="cec1f-134">針對埠類型通知作業產生訂閱/取消訂閱 proxy 函式的實作為宣告。</span><span class="sxs-lookup"><span data-stu-id="cec1f-134">Generates implementation declarations for subscribe/unsubscribe proxy functions for port type notification operations.</span></span><br/> <br/> |
| [<span data-ttu-id="cec1f-135">**subscriptionIdlFunctionDeclarations**</span><span class="sxs-lookup"><span data-stu-id="cec1f-135">**subscriptionIdlFunctionDeclarations**</span></span>](subscriptionidlfunctiondeclarations.md)<br/>           | <span data-ttu-id="cec1f-136">針對埠類型通知作業產生訂閱/取消訂閱 proxy 函式的 IDL 宣告。</span><span class="sxs-lookup"><span data-stu-id="cec1f-136">Generates IDL declarations for subscribe/unsubscribe proxy functions for port type notification operations.</span></span><br/> <br/>            |
| [<span data-ttu-id="cec1f-137">**subscriptionProxyFunctionImplementations**</span><span class="sxs-lookup"><span data-stu-id="cec1f-137">**subscriptionProxyFunctionImplementations**</span></span>](subscriptionproxyfunctionimplementations.md)<br/> | <span data-ttu-id="cec1f-138">針對埠類型通知作業產生訂閱/取消訂閱 proxy 函式的執行。</span><span class="sxs-lookup"><span data-stu-id="cec1f-138">Generates implementations for subscribe/unsubscribe proxy functions for port type notification operations.</span></span><br/> <br/>             |



## <a name="remarks"></a><span data-ttu-id="cec1f-139">備註</span><span class="sxs-lookup"><span data-stu-id="cec1f-139">Remarks</span></span>

<span data-ttu-id="cec1f-140">依預設，會針對 WSDL 輸入檔中的所有埠類型產生程式碼。</span><span class="sxs-lookup"><span data-stu-id="cec1f-140">By default, code is generated for all port types in WSDL input files.</span></span>

## <a name="element-information"></a><span data-ttu-id="cec1f-141">項目資訊</span><span class="sxs-lookup"><span data-stu-id="cec1f-141">Element information</span></span>



| <span data-ttu-id="cec1f-142">標籤</span><span class="sxs-lookup"><span data-stu-id="cec1f-142">Label</span></span> | <span data-ttu-id="cec1f-143">值</span><span class="sxs-lookup"><span data-stu-id="cec1f-143">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="cec1f-144">最低支援系統</span><span class="sxs-lookup"><span data-stu-id="cec1f-144">Minimum supported system</span></span><br/> | <span data-ttu-id="cec1f-145">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="cec1f-145">Windows Vista</span></span> |
| <span data-ttu-id="cec1f-146">可以是空的</span><span class="sxs-lookup"><span data-stu-id="cec1f-146">Can be empty</span></span>                        | <span data-ttu-id="cec1f-147">是</span><span class="sxs-lookup"><span data-stu-id="cec1f-147">Yes</span></span>           |



 

 




