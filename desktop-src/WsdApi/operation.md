---
description: 指定要產生程式碼的作業。
ms.assetid: d198197e-d146-4f1b-99df-944822e83357
title: operation 元素
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0bdd8324553e046000f467c103afd6ac0464cbc0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026538"
---
# <a name="operation-element"></a><span data-ttu-id="5fd5a-103">operation 元素</span><span class="sxs-lookup"><span data-stu-id="5fd5a-103">operation element</span></span>

<span data-ttu-id="5fd5a-104">指定要產生程式碼的作業。</span><span class="sxs-lookup"><span data-stu-id="5fd5a-104">Specifies an operation for which code is to be generated.</span></span>

## <a name="usage"></a><span data-ttu-id="5fd5a-105">使用方式</span><span class="sxs-lookup"><span data-stu-id="5fd5a-105">Usage</span></span>

``` syntax
<operation/>
```

## <a name="attributes"></a><span data-ttu-id="5fd5a-106">屬性</span><span class="sxs-lookup"><span data-stu-id="5fd5a-106">Attributes</span></span>

<span data-ttu-id="5fd5a-107">沒有任何屬性。</span><span class="sxs-lookup"><span data-stu-id="5fd5a-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="5fd5a-108">子元素</span><span class="sxs-lookup"><span data-stu-id="5fd5a-108">Child elements</span></span>

<span data-ttu-id="5fd5a-109">沒有任何子項目。</span><span class="sxs-lookup"><span data-stu-id="5fd5a-109">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="5fd5a-110">父元素</span><span class="sxs-lookup"><span data-stu-id="5fd5a-110">Parent elements</span></span>



| <span data-ttu-id="5fd5a-111">元素</span><span class="sxs-lookup"><span data-stu-id="5fd5a-111">Element</span></span>                                                                                                 | <span data-ttu-id="5fd5a-112">描述</span><span class="sxs-lookup"><span data-stu-id="5fd5a-112">Description</span></span>                                                                                                                                   |
|---------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5fd5a-113">**functionDeclarations**</span><span class="sxs-lookup"><span data-stu-id="5fd5a-113">**functionDeclarations**</span></span>](functiondeclarations.md)<br/>                                         | <span data-ttu-id="5fd5a-114">針對埠類型作業產生 proxy 函式的實作為宣告。</span><span class="sxs-lookup"><span data-stu-id="5fd5a-114">Generates implementation declarations for proxy functions for port type operations.</span></span><br/> <br/>                                    |
| [<span data-ttu-id="5fd5a-115">**idlFunctionDeclarations**</span><span class="sxs-lookup"><span data-stu-id="5fd5a-115">**idlFunctionDeclarations**</span></span>](idlfunctiondeclarations.md)<br/>                                   | <span data-ttu-id="5fd5a-116">針對埠類型作業產生 proxy 函式的 IDL 宣告。</span><span class="sxs-lookup"><span data-stu-id="5fd5a-116">Generates IDL declarations for proxy functions for port type operations.</span></span><br/> <br/>                                               |
| [<span data-ttu-id="5fd5a-117">**messageStructureDefinitions**</span><span class="sxs-lookup"><span data-stu-id="5fd5a-117">**messageStructureDefinitions**</span></span>](messagestructuredefinitions.md)<br/>                           | <span data-ttu-id="5fd5a-118">產生訊息類型的 C 結構定義。</span><span class="sxs-lookup"><span data-stu-id="5fd5a-118">Generates C structure definitions for message types.</span></span><br/> <br/>                                                                   |
| [<span data-ttu-id="5fd5a-119">**messageTypeDeclarations**</span><span class="sxs-lookup"><span data-stu-id="5fd5a-119">**messageTypeDeclarations**</span></span>](messagetypedeclarations.md)<br/>                                   | <span data-ttu-id="5fd5a-120">針對訊息類型產生 XML 架構資料表的 C 常數宣告。</span><span class="sxs-lookup"><span data-stu-id="5fd5a-120">Generates C constant declarations for XML schema tables for message types.</span></span><br/> <br/>                                             |
| [<span data-ttu-id="5fd5a-121">**messageTypeDefinitions**</span><span class="sxs-lookup"><span data-stu-id="5fd5a-121">**messageTypeDefinitions**</span></span>](messagetypedefinitions.md)<br/>                                     | <span data-ttu-id="5fd5a-122">針對訊息類型產生 XML 架構資料表的 C 常數。</span><span class="sxs-lookup"><span data-stu-id="5fd5a-122">Generates C constants for XML schema tables for message types.</span></span><br/> <br/>                                                         |
| [<span data-ttu-id="5fd5a-123">**portTypeDeclarations**</span><span class="sxs-lookup"><span data-stu-id="5fd5a-123">**portTypeDeclarations**</span></span>](porttypedeclarations.md)<br/>                                         | <span data-ttu-id="5fd5a-124">產生埠類型的 C 常數宣告。</span><span class="sxs-lookup"><span data-stu-id="5fd5a-124">Generates C constant declarations for port types.</span></span><br/> <br/>                                                                      |
| [<span data-ttu-id="5fd5a-125">**portTypeDefinitions**</span><span class="sxs-lookup"><span data-stu-id="5fd5a-125">**portTypeDefinitions**</span></span>](porttypedefinitions.md)<br/>                                           | <span data-ttu-id="5fd5a-126">產生埠類型的 C 常數。</span><span class="sxs-lookup"><span data-stu-id="5fd5a-126">Generates C constants for port types.</span></span><br/> <br/>                                                                                  |
| [<span data-ttu-id="5fd5a-127">**proxyFunctionImplementations**</span><span class="sxs-lookup"><span data-stu-id="5fd5a-127">**proxyFunctionImplementations**</span></span>](proxyfunctionimplementations.md)<br/>                         | <span data-ttu-id="5fd5a-128">針對埠類型作業產生 proxy 函式的執行。</span><span class="sxs-lookup"><span data-stu-id="5fd5a-128">Generates implementations for proxy functions for port type operations.</span></span><br/> <br/>                                                |
| [<span data-ttu-id="5fd5a-129">**stubDeclarations**</span><span class="sxs-lookup"><span data-stu-id="5fd5a-129">**stubDeclarations**</span></span>](stubdeclarations.md)<br/>                                                 | <span data-ttu-id="5fd5a-130">針對埠類型作業產生存根函式的宣告。</span><span class="sxs-lookup"><span data-stu-id="5fd5a-130">Generates declarations for stub functions for port type operations.</span></span><br/> <br/>                                                    |
| [<span data-ttu-id="5fd5a-131">**stubDefinitions**</span><span class="sxs-lookup"><span data-stu-id="5fd5a-131">**stubDefinitions**</span></span>](stubdefinitions.md)<br/>                                                   | <span data-ttu-id="5fd5a-132">針對埠類型作業產生存根函式的實作為。</span><span class="sxs-lookup"><span data-stu-id="5fd5a-132">Generates implementations for stub functions for port type operations.</span></span><br/> <br/>                                                 |
| [<span data-ttu-id="5fd5a-133">**subscriptionFunctionDeclarations**</span><span class="sxs-lookup"><span data-stu-id="5fd5a-133">**subscriptionFunctionDeclarations**</span></span>](subscriptionfunctiondeclarations.md)<br/>                 | <span data-ttu-id="5fd5a-134">針對埠類型通知作業產生訂閱/取消訂閱 proxy 函式的實作為宣告。</span><span class="sxs-lookup"><span data-stu-id="5fd5a-134">Generates implementation declarations for subscribe/unsubscribe proxy functions for port type notification operations.</span></span><br/> <br/> |
| [<span data-ttu-id="5fd5a-135">**subscriptionIdlFunctionDeclarations**</span><span class="sxs-lookup"><span data-stu-id="5fd5a-135">**subscriptionIdlFunctionDeclarations**</span></span>](subscriptionidlfunctiondeclarations.md)<br/>           | <span data-ttu-id="5fd5a-136">針對埠類型通知作業產生訂閱/取消訂閱 proxy 函式的 IDL 宣告。</span><span class="sxs-lookup"><span data-stu-id="5fd5a-136">Generates IDL declarations for subscribe/unsubscribe proxy functions for port type notification operations.</span></span><br/> <br/>            |
| [<span data-ttu-id="5fd5a-137">**subscriptionProxyFunctionImplementations**</span><span class="sxs-lookup"><span data-stu-id="5fd5a-137">**subscriptionProxyFunctionImplementations**</span></span>](subscriptionproxyfunctionimplementations.md)<br/> | <span data-ttu-id="5fd5a-138">針對埠類型通知作業產生訂閱/取消訂閱 proxy 函式的執行。</span><span class="sxs-lookup"><span data-stu-id="5fd5a-138">Generates implementations for subscribe/unsubscribe proxy functions for port type notification operations.</span></span><br/> <br/>             |



## <a name="remarks"></a><span data-ttu-id="5fd5a-139">備註</span><span class="sxs-lookup"><span data-stu-id="5fd5a-139">Remarks</span></span>

<span data-ttu-id="5fd5a-140">您可以指定任意數目的作業。</span><span class="sxs-lookup"><span data-stu-id="5fd5a-140">Any number of operations may be specified.</span></span> <span data-ttu-id="5fd5a-141">如果未指定任何作業，則會針對所有相關埠類型中的所有作業產生程式碼。</span><span class="sxs-lookup"><span data-stu-id="5fd5a-141">If no operations are specified, code is generated for all operations in all the relevant port types.</span></span> <span data-ttu-id="5fd5a-142">使用 **operation** 元素會將產生的方法限制為包含在作業中的方法。</span><span class="sxs-lookup"><span data-stu-id="5fd5a-142">Using the **operation** element will limit the methods generated to those contained in the operation.</span></span>

<span data-ttu-id="5fd5a-143">例如，印表機支援這些作業的其他作業：</span><span class="sxs-lookup"><span data-stu-id="5fd5a-143">For example, a printer supports these operations among others:</span></span>

-   <span data-ttu-id="5fd5a-144">**PrintJobByPost**</span><span class="sxs-lookup"><span data-stu-id="5fd5a-144">**PrintJobByPost**</span></span>
-   <span data-ttu-id="5fd5a-145">**PrintJobByReference**</span><span class="sxs-lookup"><span data-stu-id="5fd5a-145">**PrintJobByReference**</span></span>
-   <span data-ttu-id="5fd5a-146">**CancelJob**</span><span class="sxs-lookup"><span data-stu-id="5fd5a-146">**CancelJob**</span></span>
-   <span data-ttu-id="5fd5a-147">**GetJobElements**</span><span class="sxs-lookup"><span data-stu-id="5fd5a-147">**GetJobElements**</span></span>
-   <span data-ttu-id="5fd5a-148">**GetActiveJobs**</span><span class="sxs-lookup"><span data-stu-id="5fd5a-148">**GetActiveJobs**</span></span>
-   <span data-ttu-id="5fd5a-149">**GetJobHistory**</span><span class="sxs-lookup"><span data-stu-id="5fd5a-149">**GetJobHistory**</span></span>
-   <span data-ttu-id="5fd5a-150">**SubscribeToPrinterConfigChange**</span><span class="sxs-lookup"><span data-stu-id="5fd5a-150">**SubscribeToPrinterConfigChange**</span></span>
-   <span data-ttu-id="5fd5a-151">**UnsubscribeToPrinterConfigChange**</span><span class="sxs-lookup"><span data-stu-id="5fd5a-151">**UnsubscribeToPrinterConfigChange**</span></span>

<span data-ttu-id="5fd5a-152">不過，若要只包含與 **PrintJobByPost** 和 **GetJobElements** 作業相關的方法，程式碼產生腳本會使用 [**idlFunctionDeclarations**](idlfunctiondeclarations.md) 元素，如下所示：</span><span class="sxs-lookup"><span data-stu-id="5fd5a-152">However, to include only the methods related to the **PrintJobByPost** and **GetJobElements** operations, the code generation script would use the [**idlFunctionDeclarations**](idlfunctiondeclarations.md) elements as follows:</span></span>

``` syntax
<idlFunctionDeclarations>
    <operation>PrintJobByPost</operation>
    <operation>GetJobElements></operation>
</idlFunctionDeclarations>
```

<span data-ttu-id="5fd5a-153">這會針對與這兩個作業相關聯的所有方法產生 idl 函式宣告 (例如， **BeginPrintJobByPost**、 **EndPrintJobByPost**、 **BeginGetJobElements** 和 **EndGetJobElements**) 。</span><span class="sxs-lookup"><span data-stu-id="5fd5a-153">This generates idl function declarations for all methods associated with the two operations (for example, **BeginPrintJobByPost**, **EndPrintJobByPost**, **BeginGetJobElements** and **EndGetJobElements**).</span></span>

## <a name="element-information"></a><span data-ttu-id="5fd5a-154">項目資訊</span><span class="sxs-lookup"><span data-stu-id="5fd5a-154">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="5fd5a-155">最低支援系統</span><span class="sxs-lookup"><span data-stu-id="5fd5a-155">Minimum supported system</span></span><br/> | <span data-ttu-id="5fd5a-156">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5fd5a-156">Windows Vista</span></span> |
| <span data-ttu-id="5fd5a-157">可以是空的</span><span class="sxs-lookup"><span data-stu-id="5fd5a-157">Can be empty</span></span>                        | <span data-ttu-id="5fd5a-158">是</span><span class="sxs-lookup"><span data-stu-id="5fd5a-158">Yes</span></span>           |



 

 




