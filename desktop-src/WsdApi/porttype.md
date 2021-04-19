---
description: 指定要產生程式碼的埠類型。
ms.assetid: 8a7762ae-2e39-46e1-b49f-09cae1af9b0d
title: portType 元素
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a466ccdcfda133a2a314609e9698cd37c6bf31c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106983513"
---
# <a name="porttype-element"></a><span data-ttu-id="acf90-103">portType 元素</span><span class="sxs-lookup"><span data-stu-id="acf90-103">portType element</span></span>

<span data-ttu-id="acf90-104">指定要產生程式碼的埠類型。</span><span class="sxs-lookup"><span data-stu-id="acf90-104">Specifies the port type for which code is to be generated.</span></span>

## <a name="usage"></a><span data-ttu-id="acf90-105">使用方式</span><span class="sxs-lookup"><span data-stu-id="acf90-105">Usage</span></span>

``` syntax
<portType/>
```

## <a name="attributes"></a><span data-ttu-id="acf90-106">屬性</span><span class="sxs-lookup"><span data-stu-id="acf90-106">Attributes</span></span>

<span data-ttu-id="acf90-107">沒有任何屬性。</span><span class="sxs-lookup"><span data-stu-id="acf90-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="acf90-108">子元素</span><span class="sxs-lookup"><span data-stu-id="acf90-108">Child elements</span></span>

<span data-ttu-id="acf90-109">沒有任何子項目。</span><span class="sxs-lookup"><span data-stu-id="acf90-109">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="acf90-110">父元素</span><span class="sxs-lookup"><span data-stu-id="acf90-110">Parent elements</span></span>



| <span data-ttu-id="acf90-111">元素</span><span class="sxs-lookup"><span data-stu-id="acf90-111">Element</span></span>                                                                                                 | <span data-ttu-id="acf90-112">描述</span><span class="sxs-lookup"><span data-stu-id="acf90-112">Description</span></span>                                                                                                                                   |
|---------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="acf90-113">**functionDeclarations**</span><span class="sxs-lookup"><span data-stu-id="acf90-113">**functionDeclarations**</span></span>](functiondeclarations.md)<br/>                                         | <span data-ttu-id="acf90-114">針對埠類型作業產生 proxy 函式的實作為宣告。</span><span class="sxs-lookup"><span data-stu-id="acf90-114">Generates implementation declarations for proxy functions for port type operations.</span></span><br/> <br/>                                    |
| [<span data-ttu-id="acf90-115">**idlFunctionDeclarations**</span><span class="sxs-lookup"><span data-stu-id="acf90-115">**idlFunctionDeclarations**</span></span>](idlfunctiondeclarations.md)<br/>                                   | <span data-ttu-id="acf90-116">針對埠類型作業產生 proxy 函式的 IDL 宣告。</span><span class="sxs-lookup"><span data-stu-id="acf90-116">Generates IDL declarations for proxy functions for port type operations.</span></span><br/> <br/>                                               |
| [<span data-ttu-id="acf90-117">**messageStructureDefinitions**</span><span class="sxs-lookup"><span data-stu-id="acf90-117">**messageStructureDefinitions**</span></span>](messagestructuredefinitions.md)<br/>                           | <span data-ttu-id="acf90-118">產生訊息類型的 C 結構定義。</span><span class="sxs-lookup"><span data-stu-id="acf90-118">Generates C structure definitions for message types.</span></span><br/> <br/>                                                                   |
| [<span data-ttu-id="acf90-119">**messageTypeDeclarations**</span><span class="sxs-lookup"><span data-stu-id="acf90-119">**messageTypeDeclarations**</span></span>](messagetypedeclarations.md)<br/>                                   | <span data-ttu-id="acf90-120">針對訊息類型產生 XML 架構資料表的 C 常數宣告。</span><span class="sxs-lookup"><span data-stu-id="acf90-120">Generates C constant declarations for XML schema tables for message types.</span></span><br/> <br/>                                             |
| [<span data-ttu-id="acf90-121">**messageTypeDefinitions**</span><span class="sxs-lookup"><span data-stu-id="acf90-121">**messageTypeDefinitions**</span></span>](messagetypedefinitions.md)<br/>                                     | <span data-ttu-id="acf90-122">針對訊息類型產生 XML 架構資料表的 C 常數。</span><span class="sxs-lookup"><span data-stu-id="acf90-122">Generates C constants for XML schema tables for message types.</span></span><br/> <br/>                                                         |
| [<span data-ttu-id="acf90-123">**portTypeDeclarations**</span><span class="sxs-lookup"><span data-stu-id="acf90-123">**portTypeDeclarations**</span></span>](porttypedeclarations.md)<br/>                                         | <span data-ttu-id="acf90-124">產生埠類型的 C 常數宣告。</span><span class="sxs-lookup"><span data-stu-id="acf90-124">Generates C constant declarations for port types.</span></span><br/> <br/>                                                                      |
| [<span data-ttu-id="acf90-125">**portTypeDefinitions**</span><span class="sxs-lookup"><span data-stu-id="acf90-125">**portTypeDefinitions**</span></span>](porttypedefinitions.md)<br/>                                           | <span data-ttu-id="acf90-126">產生埠類型的 C 常數。</span><span class="sxs-lookup"><span data-stu-id="acf90-126">Generates C constants for port types.</span></span><br/> <br/>                                                                                  |
| [<span data-ttu-id="acf90-127">**proxyFunctionImplementations**</span><span class="sxs-lookup"><span data-stu-id="acf90-127">**proxyFunctionImplementations**</span></span>](proxyfunctionimplementations.md)<br/>                         | <span data-ttu-id="acf90-128">針對埠類型作業產生 proxy 函式的執行。</span><span class="sxs-lookup"><span data-stu-id="acf90-128">Generates implementations for proxy functions for port type operations.</span></span><br/> <br/>                                                |
| [<span data-ttu-id="acf90-129">**stubDeclarations**</span><span class="sxs-lookup"><span data-stu-id="acf90-129">**stubDeclarations**</span></span>](stubdeclarations.md)<br/>                                                 | <span data-ttu-id="acf90-130">針對埠類型作業產生存根函式的宣告。</span><span class="sxs-lookup"><span data-stu-id="acf90-130">Generates declarations for stub functions for port type operations.</span></span><br/> <br/>                                                    |
| [<span data-ttu-id="acf90-131">**stubDefinitions**</span><span class="sxs-lookup"><span data-stu-id="acf90-131">**stubDefinitions**</span></span>](stubdefinitions.md)<br/>                                                   | <span data-ttu-id="acf90-132">針對埠類型作業產生存根函式的實作為。</span><span class="sxs-lookup"><span data-stu-id="acf90-132">Generates implementations for stub functions for port type operations.</span></span><br/> <br/>                                                 |
| [<span data-ttu-id="acf90-133">**subscriptionFunctionDeclarations**</span><span class="sxs-lookup"><span data-stu-id="acf90-133">**subscriptionFunctionDeclarations**</span></span>](subscriptionfunctiondeclarations.md)<br/>                 | <span data-ttu-id="acf90-134">針對埠類型通知作業產生訂閱/取消訂閱 proxy 函式的實作為宣告。</span><span class="sxs-lookup"><span data-stu-id="acf90-134">Generates implementation declarations for subscribe/unsubscribe proxy functions for port type notification operations.</span></span><br/> <br/> |
| [<span data-ttu-id="acf90-135">**subscriptionIdlFunctionDeclarations**</span><span class="sxs-lookup"><span data-stu-id="acf90-135">**subscriptionIdlFunctionDeclarations**</span></span>](subscriptionidlfunctiondeclarations.md)<br/>           | <span data-ttu-id="acf90-136">針對埠類型通知作業產生訂閱/取消訂閱 proxy 函式的 IDL 宣告。</span><span class="sxs-lookup"><span data-stu-id="acf90-136">Generates IDL declarations for subscribe/unsubscribe proxy functions for port type notification operations.</span></span><br/> <br/>            |
| [<span data-ttu-id="acf90-137">**subscriptionProxyFunctionImplementations**</span><span class="sxs-lookup"><span data-stu-id="acf90-137">**subscriptionProxyFunctionImplementations**</span></span>](subscriptionproxyfunctionimplementations.md)<br/> | <span data-ttu-id="acf90-138">針對埠類型通知作業產生訂閱/取消訂閱 proxy 函式的執行。</span><span class="sxs-lookup"><span data-stu-id="acf90-138">Generates implementations for subscribe/unsubscribe proxy functions for port type notification operations.</span></span><br/> <br/>             |



## <a name="remarks"></a><span data-ttu-id="acf90-139">備註</span><span class="sxs-lookup"><span data-stu-id="acf90-139">Remarks</span></span>

<span data-ttu-id="acf90-140">依預設，會針對 WSDL 輸入檔中的所有埠類型產生程式碼。</span><span class="sxs-lookup"><span data-stu-id="acf90-140">By default, code is generated for all port types in WSDL input files.</span></span>

## <a name="element-information"></a><span data-ttu-id="acf90-141">項目資訊</span><span class="sxs-lookup"><span data-stu-id="acf90-141">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="acf90-142">最低支援系統</span><span class="sxs-lookup"><span data-stu-id="acf90-142">Minimum supported system</span></span><br/> | <span data-ttu-id="acf90-143">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="acf90-143">Windows Vista</span></span> |
| <span data-ttu-id="acf90-144">可以是空的</span><span class="sxs-lookup"><span data-stu-id="acf90-144">Can be empty</span></span>                        | <span data-ttu-id="acf90-145">是</span><span class="sxs-lookup"><span data-stu-id="acf90-145">Yes</span></span>           |



 

 




