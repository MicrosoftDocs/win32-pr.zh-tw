---
description: 指定要產生程式碼的作業。
ms.assetid: d198197e-d146-4f1b-99df-944822e83357
title: operation 元素
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c0e4562241f5f437554d0af28dc8bca482512ea
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/26/2021
ms.locfileid: "107994314"
---
# <a name="operation-element"></a><span data-ttu-id="2534d-103">operation 元素</span><span class="sxs-lookup"><span data-stu-id="2534d-103">operation element</span></span>

<span data-ttu-id="2534d-104">指定要產生程式碼的作業。</span><span class="sxs-lookup"><span data-stu-id="2534d-104">Specifies an operation for which code is to be generated.</span></span>

## <a name="usage"></a><span data-ttu-id="2534d-105">使用方式</span><span class="sxs-lookup"><span data-stu-id="2534d-105">Usage</span></span>

``` syntax
<operation/>
```

## <a name="attributes"></a><span data-ttu-id="2534d-106">屬性</span><span class="sxs-lookup"><span data-stu-id="2534d-106">Attributes</span></span>

<span data-ttu-id="2534d-107">沒有任何屬性。</span><span class="sxs-lookup"><span data-stu-id="2534d-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="2534d-108">子元素</span><span class="sxs-lookup"><span data-stu-id="2534d-108">Child elements</span></span>

<span data-ttu-id="2534d-109">沒有任何子項目。</span><span class="sxs-lookup"><span data-stu-id="2534d-109">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="2534d-110">父元素</span><span class="sxs-lookup"><span data-stu-id="2534d-110">Parent elements</span></span>



| <span data-ttu-id="2534d-111">元素</span><span class="sxs-lookup"><span data-stu-id="2534d-111">Element</span></span>                                                                                                 | <span data-ttu-id="2534d-112">描述</span><span class="sxs-lookup"><span data-stu-id="2534d-112">Description</span></span>                                                                                                                                   |
|---------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2534d-113">**functionDeclarations**</span><span class="sxs-lookup"><span data-stu-id="2534d-113">**functionDeclarations**</span></span>](functiondeclarations.md)<br/>                                         | <span data-ttu-id="2534d-114">針對埠類型作業產生 proxy 函式的實作為宣告。</span><span class="sxs-lookup"><span data-stu-id="2534d-114">Generates implementation declarations for proxy functions for port type operations.</span></span><br/> <br/>                                    |
| [<span data-ttu-id="2534d-115">**idlFunctionDeclarations**</span><span class="sxs-lookup"><span data-stu-id="2534d-115">**idlFunctionDeclarations**</span></span>](idlfunctiondeclarations.md)<br/>                                   | <span data-ttu-id="2534d-116">針對埠類型作業產生 proxy 函式的 IDL 宣告。</span><span class="sxs-lookup"><span data-stu-id="2534d-116">Generates IDL declarations for proxy functions for port type operations.</span></span><br/> <br/>                                               |
| [<span data-ttu-id="2534d-117">**messageStructureDefinitions**</span><span class="sxs-lookup"><span data-stu-id="2534d-117">**messageStructureDefinitions**</span></span>](messagestructuredefinitions.md)<br/>                           | <span data-ttu-id="2534d-118">產生訊息類型的 C 結構定義。</span><span class="sxs-lookup"><span data-stu-id="2534d-118">Generates C structure definitions for message types.</span></span><br/> <br/>                                                                   |
| [<span data-ttu-id="2534d-119">**messageTypeDeclarations**</span><span class="sxs-lookup"><span data-stu-id="2534d-119">**messageTypeDeclarations**</span></span>](messagetypedeclarations.md)<br/>                                   | <span data-ttu-id="2534d-120">針對訊息類型產生 XML 架構資料表的 C 常數宣告。</span><span class="sxs-lookup"><span data-stu-id="2534d-120">Generates C constant declarations for XML schema tables for message types.</span></span><br/> <br/>                                             |
| [<span data-ttu-id="2534d-121">**messageTypeDefinitions**</span><span class="sxs-lookup"><span data-stu-id="2534d-121">**messageTypeDefinitions**</span></span>](messagetypedefinitions.md)<br/>                                     | <span data-ttu-id="2534d-122">針對訊息類型產生 XML 架構資料表的 C 常數。</span><span class="sxs-lookup"><span data-stu-id="2534d-122">Generates C constants for XML schema tables for message types.</span></span><br/> <br/>                                                         |
| [<span data-ttu-id="2534d-123">**portTypeDeclarations**</span><span class="sxs-lookup"><span data-stu-id="2534d-123">**portTypeDeclarations**</span></span>](porttypedeclarations.md)<br/>                                         | <span data-ttu-id="2534d-124">產生埠類型的 C 常數宣告。</span><span class="sxs-lookup"><span data-stu-id="2534d-124">Generates C constant declarations for port types.</span></span><br/> <br/>                                                                      |
| [<span data-ttu-id="2534d-125">**portTypeDefinitions**</span><span class="sxs-lookup"><span data-stu-id="2534d-125">**portTypeDefinitions**</span></span>](porttypedefinitions.md)<br/>                                           | <span data-ttu-id="2534d-126">產生埠類型的 C 常數。</span><span class="sxs-lookup"><span data-stu-id="2534d-126">Generates C constants for port types.</span></span><br/> <br/>                                                                                  |
| [<span data-ttu-id="2534d-127">**proxyFunctionImplementations**</span><span class="sxs-lookup"><span data-stu-id="2534d-127">**proxyFunctionImplementations**</span></span>](proxyfunctionimplementations.md)<br/>                         | <span data-ttu-id="2534d-128">針對埠類型作業產生 proxy 函式的執行。</span><span class="sxs-lookup"><span data-stu-id="2534d-128">Generates implementations for proxy functions for port type operations.</span></span><br/> <br/>                                                |
| [<span data-ttu-id="2534d-129">**stubDeclarations**</span><span class="sxs-lookup"><span data-stu-id="2534d-129">**stubDeclarations**</span></span>](stubdeclarations.md)<br/>                                                 | <span data-ttu-id="2534d-130">針對埠類型作業產生存根函式的宣告。</span><span class="sxs-lookup"><span data-stu-id="2534d-130">Generates declarations for stub functions for port type operations.</span></span><br/> <br/>                                                    |
| [<span data-ttu-id="2534d-131">**stubDefinitions**</span><span class="sxs-lookup"><span data-stu-id="2534d-131">**stubDefinitions**</span></span>](stubdefinitions.md)<br/>                                                   | <span data-ttu-id="2534d-132">針對埠類型作業產生存根函式的實作為。</span><span class="sxs-lookup"><span data-stu-id="2534d-132">Generates implementations for stub functions for port type operations.</span></span><br/> <br/>                                                 |
| [<span data-ttu-id="2534d-133">**subscriptionFunctionDeclarations**</span><span class="sxs-lookup"><span data-stu-id="2534d-133">**subscriptionFunctionDeclarations**</span></span>](subscriptionfunctiondeclarations.md)<br/>                 | <span data-ttu-id="2534d-134">針對埠類型通知作業產生訂閱/取消訂閱 proxy 函式的實作為宣告。</span><span class="sxs-lookup"><span data-stu-id="2534d-134">Generates implementation declarations for subscribe/unsubscribe proxy functions for port type notification operations.</span></span><br/> <br/> |
| [<span data-ttu-id="2534d-135">**subscriptionIdlFunctionDeclarations**</span><span class="sxs-lookup"><span data-stu-id="2534d-135">**subscriptionIdlFunctionDeclarations**</span></span>](subscriptionidlfunctiondeclarations.md)<br/>           | <span data-ttu-id="2534d-136">針對埠類型通知作業產生訂閱/取消訂閱 proxy 函式的 IDL 宣告。</span><span class="sxs-lookup"><span data-stu-id="2534d-136">Generates IDL declarations for subscribe/unsubscribe proxy functions for port type notification operations.</span></span><br/> <br/>            |
| [<span data-ttu-id="2534d-137">**subscriptionProxyFunctionImplementations**</span><span class="sxs-lookup"><span data-stu-id="2534d-137">**subscriptionProxyFunctionImplementations**</span></span>](subscriptionproxyfunctionimplementations.md)<br/> | <span data-ttu-id="2534d-138">針對埠類型通知作業產生訂閱/取消訂閱 proxy 函式的執行。</span><span class="sxs-lookup"><span data-stu-id="2534d-138">Generates implementations for subscribe/unsubscribe proxy functions for port type notification operations.</span></span><br/> <br/>             |



## <a name="remarks"></a><span data-ttu-id="2534d-139">備註</span><span class="sxs-lookup"><span data-stu-id="2534d-139">Remarks</span></span>

<span data-ttu-id="2534d-140">您可以指定任意數目的作業。</span><span class="sxs-lookup"><span data-stu-id="2534d-140">Any number of operations may be specified.</span></span> <span data-ttu-id="2534d-141">如果未指定任何作業，則會針對所有相關埠類型中的所有作業產生程式碼。</span><span class="sxs-lookup"><span data-stu-id="2534d-141">If no operations are specified, code is generated for all operations in all the relevant port types.</span></span> <span data-ttu-id="2534d-142">使用 **operation** 元素會將產生的方法限制為包含在作業中的方法。</span><span class="sxs-lookup"><span data-stu-id="2534d-142">Using the **operation** element will limit the methods generated to those contained in the operation.</span></span>

<span data-ttu-id="2534d-143">例如，印表機支援這些作業的其他作業：</span><span class="sxs-lookup"><span data-stu-id="2534d-143">For example, a printer supports these operations among others:</span></span>

-   <span data-ttu-id="2534d-144">**PrintJobByPost**</span><span class="sxs-lookup"><span data-stu-id="2534d-144">**PrintJobByPost**</span></span>
-   <span data-ttu-id="2534d-145">**PrintJobByReference**</span><span class="sxs-lookup"><span data-stu-id="2534d-145">**PrintJobByReference**</span></span>
-   <span data-ttu-id="2534d-146">**CancelJob**</span><span class="sxs-lookup"><span data-stu-id="2534d-146">**CancelJob**</span></span>
-   <span data-ttu-id="2534d-147">**GetJobElements**</span><span class="sxs-lookup"><span data-stu-id="2534d-147">**GetJobElements**</span></span>
-   <span data-ttu-id="2534d-148">**GetActiveJobs**</span><span class="sxs-lookup"><span data-stu-id="2534d-148">**GetActiveJobs**</span></span>
-   <span data-ttu-id="2534d-149">**GetJobHistory**</span><span class="sxs-lookup"><span data-stu-id="2534d-149">**GetJobHistory**</span></span>
-   <span data-ttu-id="2534d-150">**SubscribeToPrinterConfigChange**</span><span class="sxs-lookup"><span data-stu-id="2534d-150">**SubscribeToPrinterConfigChange**</span></span>
-   <span data-ttu-id="2534d-151">**UnsubscribeToPrinterConfigChange**</span><span class="sxs-lookup"><span data-stu-id="2534d-151">**UnsubscribeToPrinterConfigChange**</span></span>

<span data-ttu-id="2534d-152">不過，若要只包含與 **PrintJobByPost** 和 **GetJobElements** 作業相關的方法，程式碼產生腳本會使用 [**idlFunctionDeclarations**](idlfunctiondeclarations.md) 元素，如下所示：</span><span class="sxs-lookup"><span data-stu-id="2534d-152">However, to include only the methods related to the **PrintJobByPost** and **GetJobElements** operations, the code generation script would use the [**idlFunctionDeclarations**](idlfunctiondeclarations.md) elements as follows:</span></span>

``` syntax
<idlFunctionDeclarations>
    <operation>PrintJobByPost</operation>
    <operation>GetJobElements></operation>
</idlFunctionDeclarations>
```

<span data-ttu-id="2534d-153">這會針對與這兩個作業相關聯的所有方法產生 idl 函式宣告 (例如， **BeginPrintJobByPost**、 **EndPrintJobByPost**、 **BeginGetJobElements** 和 **EndGetJobElements**) 。</span><span class="sxs-lookup"><span data-stu-id="2534d-153">This generates idl function declarations for all methods associated with the two operations (for example, **BeginPrintJobByPost**, **EndPrintJobByPost**, **BeginGetJobElements** and **EndGetJobElements**).</span></span>

## <a name="element-information"></a><span data-ttu-id="2534d-154">項目資訊</span><span class="sxs-lookup"><span data-stu-id="2534d-154">Element information</span></span>



| <span data-ttu-id="2534d-155">標籤</span><span class="sxs-lookup"><span data-stu-id="2534d-155">Label</span></span> | <span data-ttu-id="2534d-156">值</span><span class="sxs-lookup"><span data-stu-id="2534d-156">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="2534d-157">最低支援系統</span><span class="sxs-lookup"><span data-stu-id="2534d-157">Minimum supported system</span></span><br/> | <span data-ttu-id="2534d-158">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2534d-158">Windows Vista</span></span> |
| <span data-ttu-id="2534d-159">可以是空的</span><span class="sxs-lookup"><span data-stu-id="2534d-159">Can be empty</span></span>                        | <span data-ttu-id="2534d-160">是</span><span class="sxs-lookup"><span data-stu-id="2534d-160">Yes</span></span>           |



 

 




