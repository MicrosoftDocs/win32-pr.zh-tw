---
description: 指示程式碼產生器產生檔案並指定輸出檔名稱。
ms.assetid: d2ee6886-995f-453d-8121-f849b2d910ec
title: file 項目
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41970da9cc6e389f4e45c5e55901ce8eb2e7797f
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/26/2021
ms.locfileid: "107995865"
---
# <a name="file-element"></a><span data-ttu-id="89fbc-103">file 項目</span><span class="sxs-lookup"><span data-stu-id="89fbc-103">file element</span></span>

<span data-ttu-id="89fbc-104">指示程式碼產生器產生檔案並指定輸出檔名稱。</span><span class="sxs-lookup"><span data-stu-id="89fbc-104">Directs the code generator to generate a file and specifies the output file name.</span></span>

## <a name="usage"></a><span data-ttu-id="89fbc-105">使用方式</span><span class="sxs-lookup"><span data-stu-id="89fbc-105">Usage</span></span>

``` syntax
<file
  name = "pathname string">
  child elements
</file>
```

## <a name="attributes"></a><span data-ttu-id="89fbc-106">屬性</span><span class="sxs-lookup"><span data-stu-id="89fbc-106">Attributes</span></span>



| <span data-ttu-id="89fbc-107">屬性</span><span class="sxs-lookup"><span data-stu-id="89fbc-107">Attribute</span></span>           | <span data-ttu-id="89fbc-108">類型</span><span class="sxs-lookup"><span data-stu-id="89fbc-108">Type</span></span>                       | <span data-ttu-id="89fbc-109">必要</span><span class="sxs-lookup"><span data-stu-id="89fbc-109">Required</span></span>       | <span data-ttu-id="89fbc-110">描述</span><span class="sxs-lookup"><span data-stu-id="89fbc-110">Description</span></span>                                                                                                                         |
|---------------------|----------------------------|----------------|-------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="89fbc-111">**name**</span><span class="sxs-lookup"><span data-stu-id="89fbc-111">**name**</span></span><br/> | <span data-ttu-id="89fbc-112">pathname 字串</span><span class="sxs-lookup"><span data-stu-id="89fbc-112">pathname string</span></span><br/> | <span data-ttu-id="89fbc-113">Yes</span><span class="sxs-lookup"><span data-stu-id="89fbc-113">Yes</span></span><br/> | <span data-ttu-id="89fbc-114">產生之內容的輸出檔案名。</span><span class="sxs-lookup"><span data-stu-id="89fbc-114">The output filename for the generated content.</span></span> <span data-ttu-id="89fbc-115">檔案名字串應該包含完整的路徑資訊。</span><span class="sxs-lookup"><span data-stu-id="89fbc-115">The filename string should include complete path information.</span></span><br/> <br/> |



## <a name="child-elements"></a><span data-ttu-id="89fbc-116">子元素</span><span class="sxs-lookup"><span data-stu-id="89fbc-116">Child elements</span></span>



| <span data-ttu-id="89fbc-117">元素</span><span class="sxs-lookup"><span data-stu-id="89fbc-117">Element</span></span>                                                                                                 | <span data-ttu-id="89fbc-118">描述</span><span class="sxs-lookup"><span data-stu-id="89fbc-118">Description</span></span>                                                                                                                                                                                                           |
|---------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="89fbc-119">**Cdata**</span><span class="sxs-lookup"><span data-stu-id="89fbc-119">**CDATA**</span></span><br/>                                                                                    | <span data-ttu-id="89fbc-120">在不修改的情況下，會將 Text 和 CDATA 區段複製到檔案。</span><span class="sxs-lookup"><span data-stu-id="89fbc-120">Text and CDATA sections are copied to the file without modification.</span></span> <span data-ttu-id="89fbc-121">您可以使用 text 和 CDATA 區段，將不是合約輸入資料功能的原始程式碼新增至輸出檔案。</span><span class="sxs-lookup"><span data-stu-id="89fbc-121">Source code that is not a function of the contract input data can be added to output files using text and CDATA sections.</span></span><br/> <br/> |
| [<span data-ttu-id="89fbc-122">**enumerationValueDeclarations**</span><span class="sxs-lookup"><span data-stu-id="89fbc-122">**enumerationValueDeclarations**</span></span>](enumerationvaluedeclarations.md)<br/>                         | <span data-ttu-id="89fbc-123">針對所有列舉類型的值產生 C 宣告。</span><span class="sxs-lookup"><span data-stu-id="89fbc-123">Generates C declarations for values of all enumerated types.</span></span><br/> <br/>                                                                                                                                   |
| [<span data-ttu-id="89fbc-124">**eventSourceBuilderDeclarations**</span><span class="sxs-lookup"><span data-stu-id="89fbc-124">**eventSourceBuilderDeclarations**</span></span>](eventsourcebuilderdeclarations.md)<br/>                     | <span data-ttu-id="89fbc-125">針對建立事件來源類別的函式產生宣告。</span><span class="sxs-lookup"><span data-stu-id="89fbc-125">Generates declarations for functions that create event source classes.</span></span><br/> <br/>                                                                                                                         |
| [<span data-ttu-id="89fbc-126">**eventSourceBuilderImplementations**</span><span class="sxs-lookup"><span data-stu-id="89fbc-126">**eventSourceBuilderImplementations**</span></span>](eventsourcebuilderimplementations.md)<br/>               | <span data-ttu-id="89fbc-127">產生建立事件來源類別的函式。</span><span class="sxs-lookup"><span data-stu-id="89fbc-127">Generates functions that create event source classes.</span></span><br/> <br/>                                                                                                                                          |
| [<span data-ttu-id="89fbc-128">**functionDeclarations**</span><span class="sxs-lookup"><span data-stu-id="89fbc-128">**functionDeclarations**</span></span>](functiondeclarations.md)<br/>                                         | <span data-ttu-id="89fbc-129">針對埠類型作業產生 proxy 函式的實作為宣告。</span><span class="sxs-lookup"><span data-stu-id="89fbc-129">Generates implementation declarations for proxy functions for port type operations.</span></span><br/> <br/>                                                                                                            |
| [<span data-ttu-id="89fbc-130">**hostBuilderDeclaration**</span><span class="sxs-lookup"><span data-stu-id="89fbc-130">**hostBuilderDeclaration**</span></span>](hostbuilderdeclaration.md)<br/>                                     | <span data-ttu-id="89fbc-131">產生函式的宣告，這個函式會建立具類型的主控制項。</span><span class="sxs-lookup"><span data-stu-id="89fbc-131">Generates a declaration for a function that creates a typed host.</span></span><br/> <br/>                                                                                                                              |
| [<span data-ttu-id="89fbc-132">**hostBuilderImplementation**</span><span class="sxs-lookup"><span data-stu-id="89fbc-132">**hostBuilderImplementation**</span></span>](hostbuilderimplementation.md)<br/>                               | <span data-ttu-id="89fbc-133">產生可建立具型別主機的函式。</span><span class="sxs-lookup"><span data-stu-id="89fbc-133">Generates a function that creates a typed host.</span></span><br/> <br/>                                                                                                                                                |
| [<span data-ttu-id="89fbc-134">**idlFunctionDeclarations**</span><span class="sxs-lookup"><span data-stu-id="89fbc-134">**idlFunctionDeclarations**</span></span>](idlfunctiondeclarations.md)<br/>                                   | <span data-ttu-id="89fbc-135">針對埠類型作業產生 proxy 函式的 IDL 宣告。</span><span class="sxs-lookup"><span data-stu-id="89fbc-135">Generates IDL declarations for proxy functions for port type operations.</span></span><br/> <br/>                                                                                                                       |
| [<span data-ttu-id="89fbc-136">**包括**</span><span class="sxs-lookup"><span data-stu-id="89fbc-136">**include**</span></span>](include.md)<br/>                                                                   | <span data-ttu-id="89fbc-137">在產生的輸出中包含宏或檔案的內容。</span><span class="sxs-lookup"><span data-stu-id="89fbc-137">Includes the contents of a macro or file in the generated output.</span></span><br/> <br/>                                                                                                                              |
| [<span data-ttu-id="89fbc-138">**IUnknownDeclarations**</span><span class="sxs-lookup"><span data-stu-id="89fbc-138">**IUnknownDeclarations**</span></span>](iunknowndeclarations.md)<br/>                                         | <span data-ttu-id="89fbc-139">產生 QueryInterface、AddRef 和 Release 的宣告。</span><span class="sxs-lookup"><span data-stu-id="89fbc-139">Generates declarations for QueryInterface, AddRef and Release.</span></span><br/> <br/>                                                                                                                                 |
| [<span data-ttu-id="89fbc-140">**IUnknownDefinitions**</span><span class="sxs-lookup"><span data-stu-id="89fbc-140">**IUnknownDefinitions**</span></span>](iunknowndefinitions.md)<br/>                                           | <span data-ttu-id="89fbc-141">產生 QueryInterface、AddRef 和 Release 的實作為。</span><span class="sxs-lookup"><span data-stu-id="89fbc-141">Generates implementations for QueryInterface, AddRef and Release.</span></span><br/> <br/>                                                                                                                              |
| [<span data-ttu-id="89fbc-142">**literalInclude**</span><span class="sxs-lookup"><span data-stu-id="89fbc-142">**literalInclude**</span></span>](literalinclude.md)<br/>                                                     | <span data-ttu-id="89fbc-143">將 C 或 IDL include 語句放在產生的程式碼中。</span><span class="sxs-lookup"><span data-stu-id="89fbc-143">Places a C or IDL include statement in the generated code.</span></span> <br/> <br/>                                                                                                                                    |
| [<span data-ttu-id="89fbc-144">**messageStructureDefinitions**</span><span class="sxs-lookup"><span data-stu-id="89fbc-144">**messageStructureDefinitions**</span></span>](messagestructuredefinitions.md)<br/>                           | <span data-ttu-id="89fbc-145">產生訊息類型的 C 結構定義。</span><span class="sxs-lookup"><span data-stu-id="89fbc-145">Generates C structure definitions for message types.</span></span><br/> <br/>                                                                                                                                           |
| [<span data-ttu-id="89fbc-146">**messageTypeDeclarations**</span><span class="sxs-lookup"><span data-stu-id="89fbc-146">**messageTypeDeclarations**</span></span>](messagetypedeclarations.md)<br/>                                   | <span data-ttu-id="89fbc-147">針對訊息類型產生 XML 架構資料表的 C 常數宣告。</span><span class="sxs-lookup"><span data-stu-id="89fbc-147">Generates C constant declarations for XML schema tables for message types.</span></span><br/> <br/>                                                                                                                     |
| [<span data-ttu-id="89fbc-148">**messageTypeDefinitions**</span><span class="sxs-lookup"><span data-stu-id="89fbc-148">**messageTypeDefinitions**</span></span>](messagetypedefinitions.md)<br/>                                     | <span data-ttu-id="89fbc-149">針對訊息類型產生 XML 架構資料表的 C 常數。</span><span class="sxs-lookup"><span data-stu-id="89fbc-149">Generates C constants for XML schema tables for message types.</span></span><br/> <br/>                                                                                                                                 |
| [<span data-ttu-id="89fbc-150">**namespaceDeclarations**</span><span class="sxs-lookup"><span data-stu-id="89fbc-150">**namespaceDeclarations**</span></span>](namespacedeclarations.md)<br/>                                       | <span data-ttu-id="89fbc-151">為命名空間資料表產生 C 宣告。</span><span class="sxs-lookup"><span data-stu-id="89fbc-151">Generates C declarations for namespace tables.</span></span><br/> <br/>                                                                                                                                                 |
| [<span data-ttu-id="89fbc-152">**namespaceDefinitions**</span><span class="sxs-lookup"><span data-stu-id="89fbc-152">**namespaceDefinitions**</span></span>](namespacedefinitions.md)<br/>                                         | <span data-ttu-id="89fbc-153">產生命名空間資料表的 C 定義。</span><span class="sxs-lookup"><span data-stu-id="89fbc-153">Generates C definitions for namespace tables.</span></span><br/> <br/>                                                                                                                                                  |
| [<span data-ttu-id="89fbc-154">**portTypeDeclarations**</span><span class="sxs-lookup"><span data-stu-id="89fbc-154">**portTypeDeclarations**</span></span>](porttypedeclarations.md)<br/>                                         | <span data-ttu-id="89fbc-155">產生埠類型的 C 常數宣告。</span><span class="sxs-lookup"><span data-stu-id="89fbc-155">Generates C constant declarations for port types.</span></span><br/> <br/>                                                                                                                                              |
| [<span data-ttu-id="89fbc-156">**portTypeDefinitions**</span><span class="sxs-lookup"><span data-stu-id="89fbc-156">**portTypeDefinitions**</span></span>](porttypedefinitions.md)<br/>                                           | <span data-ttu-id="89fbc-157">產生埠類型的 C 常數。</span><span class="sxs-lookup"><span data-stu-id="89fbc-157">Generates C constants for port types.</span></span><br/> <br/>                                                                                                                                                          |
| [<span data-ttu-id="89fbc-158">**proxyBuilderDeclarations**</span><span class="sxs-lookup"><span data-stu-id="89fbc-158">**proxyBuilderDeclarations**</span></span>](proxybuilderdeclarations.md)<br/>                                 | <span data-ttu-id="89fbc-159">產生函數的宣告，以建立具類型的 proxy。</span><span class="sxs-lookup"><span data-stu-id="89fbc-159">Generates declarations for functions to create typed proxies.</span></span><br/> <br/>                                                                                                                                  |
| [<span data-ttu-id="89fbc-160">**proxyBuilderImplementations**</span><span class="sxs-lookup"><span data-stu-id="89fbc-160">**proxyBuilderImplementations**</span></span>](proxybuilderimplementations.md)<br/>                           | <span data-ttu-id="89fbc-161">產生函數以建立具類型的 proxy。</span><span class="sxs-lookup"><span data-stu-id="89fbc-161">Generates functions to create typed proxies.</span></span><br/> <br/>                                                                                                                                                   |
| [<span data-ttu-id="89fbc-162">**proxyFunctionImplementations**</span><span class="sxs-lookup"><span data-stu-id="89fbc-162">**proxyFunctionImplementations**</span></span>](proxyfunctionimplementations.md)<br/>                         | <span data-ttu-id="89fbc-163">針對埠類型作業產生 proxy 函式的執行。</span><span class="sxs-lookup"><span data-stu-id="89fbc-163">Generates implementations for proxy functions for port type operations.</span></span><br/> <br/>                                                                                                                        |
| [<span data-ttu-id="89fbc-164">**relationshipMetadataDeclaration**</span><span class="sxs-lookup"><span data-stu-id="89fbc-164">**relationshipMetadataDeclaration**</span></span>](relationshipmetadatadeclaration.md)<br/>                   | <span data-ttu-id="89fbc-165">針對 [**hostMetadata**](hostmetadata.md) 元素中指定的裝載中繼資料產生向前宣告。</span><span class="sxs-lookup"><span data-stu-id="89fbc-165">Generates a forward declaration for the hosting metadata specified in the [**hostMetadata**](hostmetadata.md) element.</span></span> <br/> <br/>                                                                       |
| [<span data-ttu-id="89fbc-166">**relationshipMetadataDefinition**</span><span class="sxs-lookup"><span data-stu-id="89fbc-166">**relationshipMetadataDefinition**</span></span>](relationshipmetadatadefinition.md)<br/>                     | <span data-ttu-id="89fbc-167">針對 [**hostMetadata**](hostmetadata.md) 元素中指定的裝載中繼資料產生 C 常數定義。</span><span class="sxs-lookup"><span data-stu-id="89fbc-167">Generates a C constant definition for the hosting metadata specified in the [**hostMetadata**](hostmetadata.md) element.</span></span> <br/> <br/>                                                                     |
| [<span data-ttu-id="89fbc-168">**structDeclarations**</span><span class="sxs-lookup"><span data-stu-id="89fbc-168">**structDeclarations**</span></span>](structdeclarations.md)<br/>                                             | <span data-ttu-id="89fbc-169">產生已知類型的 C 結構宣告。</span><span class="sxs-lookup"><span data-stu-id="89fbc-169">Generates C structure declarations for known types.</span></span><br/> <br/>                                                                                                                                            |
| [<span data-ttu-id="89fbc-170">**structDefinitions**</span><span class="sxs-lookup"><span data-stu-id="89fbc-170">**structDefinitions**</span></span>](structdefinitions.md)<br/>                                               | <span data-ttu-id="89fbc-171">產生已知類型的 C 結構定義。</span><span class="sxs-lookup"><span data-stu-id="89fbc-171">Generates C structure definitions for known types.</span></span><br/> <br/>                                                                                                                                             |
| [<span data-ttu-id="89fbc-172">**stubDeclarations**</span><span class="sxs-lookup"><span data-stu-id="89fbc-172">**stubDeclarations**</span></span>](stubdeclarations.md)<br/>                                                 | <span data-ttu-id="89fbc-173">針對埠類型作業產生存根函式的宣告。</span><span class="sxs-lookup"><span data-stu-id="89fbc-173">Generates declarations for stub functions for port type operations.</span></span><br/> <br/>                                                                                                                            |
| [<span data-ttu-id="89fbc-174">**stubDefinitions**</span><span class="sxs-lookup"><span data-stu-id="89fbc-174">**stubDefinitions**</span></span>](stubdefinitions.md)<br/>                                                   | <span data-ttu-id="89fbc-175">針對埠類型作業產生存根函式的實作為。</span><span class="sxs-lookup"><span data-stu-id="89fbc-175">Generates implementations for stub functions for port type operations.</span></span><br/> <br/>                                                                                                                         |
| [<span data-ttu-id="89fbc-176">**subscriptionFunctionDeclarations**</span><span class="sxs-lookup"><span data-stu-id="89fbc-176">**subscriptionFunctionDeclarations**</span></span>](subscriptionfunctiondeclarations.md)<br/>                 | <span data-ttu-id="89fbc-177">針對埠類型通知作業產生訂閱/取消訂閱 proxy 函式的實作為宣告。</span><span class="sxs-lookup"><span data-stu-id="89fbc-177">Generates implementation declarations for subscribe/unsubscribe proxy functions for port type notification operations.</span></span><br/> <br/>                                                                         |
| [<span data-ttu-id="89fbc-178">**subscriptionIdlFunctionDeclarations**</span><span class="sxs-lookup"><span data-stu-id="89fbc-178">**subscriptionIdlFunctionDeclarations**</span></span>](subscriptionidlfunctiondeclarations.md)<br/>           | <span data-ttu-id="89fbc-179">針對埠類型通知作業產生訂閱/取消訂閱 proxy 函式的 IDL 宣告。</span><span class="sxs-lookup"><span data-stu-id="89fbc-179">Generates IDL declarations for subscribe/unsubscribe proxy functions for port type notification operations.</span></span><br/> <br/>                                                                                    |
| [<span data-ttu-id="89fbc-180">**subscriptionProxyFunctionImplementations**</span><span class="sxs-lookup"><span data-stu-id="89fbc-180">**subscriptionProxyFunctionImplementations**</span></span>](subscriptionproxyfunctionimplementations.md)<br/> | <span data-ttu-id="89fbc-181">針對埠類型通知作業產生訂閱/取消訂閱 proxy 函式的執行。</span><span class="sxs-lookup"><span data-stu-id="89fbc-181">Generates implementations for subscribe/unsubscribe proxy functions for port type notification operations.</span></span><br/> <br/>                                                                                     |
| <span data-ttu-id="89fbc-182">**text**</span><span class="sxs-lookup"><span data-stu-id="89fbc-182">**text**</span></span><br/>                                                                                     | <span data-ttu-id="89fbc-183">在不修改的情況下，會將 Text 和 CDATA 區段複製到檔案。</span><span class="sxs-lookup"><span data-stu-id="89fbc-183">Text and CDATA sections are copied to the file without modification.</span></span> <span data-ttu-id="89fbc-184">您可以使用 text 和 CDATA 區段，將不是合約輸入資料功能的原始程式碼新增至輸出檔案。</span><span class="sxs-lookup"><span data-stu-id="89fbc-184">Source code that is not a function of the contract input data can be added to output files using text and CDATA sections.</span></span><br/> <br/> |
| [<span data-ttu-id="89fbc-185">**thisModelMetadataDeclaration**</span><span class="sxs-lookup"><span data-stu-id="89fbc-185">**thisModelMetadataDeclaration**</span></span>](thismodelmetadatadeclaration.md)<br/>                         | <span data-ttu-id="89fbc-186">針對 [**thisModelMetadata**](thismodelmetadata.md) 元素中指定的製造商中繼資料，產生 C 常數的向前宣告。</span><span class="sxs-lookup"><span data-stu-id="89fbc-186">Generates a forward declaration for the C constant for the manufacturer metadata specified in the [**thisModelMetadata**](thismodelmetadata.md) element.</span></span><br/> <br/>                                      |
| [<span data-ttu-id="89fbc-187">**thisModelMetadataDefinition**</span><span class="sxs-lookup"><span data-stu-id="89fbc-187">**thisModelMetadataDefinition**</span></span>](thismodelmetadatadefinition.md)<br/>                           | <span data-ttu-id="89fbc-188">針對 [**thisModelMetadata**](thismodelmetadata.md) 元素中指定的製造商中繼資料產生 C 常數。</span><span class="sxs-lookup"><span data-stu-id="89fbc-188">Generates a C constant for the manufacturer metadata specified in the [**thisModelMetadata**](thismodelmetadata.md) element.</span></span><br/> <br/>                                                                  |
| [<span data-ttu-id="89fbc-189">**typeTableDeclarations**</span><span class="sxs-lookup"><span data-stu-id="89fbc-189">**typeTableDeclarations**</span></span>](typetabledeclarations.md)<br/>                                       | <span data-ttu-id="89fbc-190">針對已知類型產生 XML 架構資料表的 C 常數宣告。</span><span class="sxs-lookup"><span data-stu-id="89fbc-190">Generates C constant declarations for XML schema tables for known types.</span></span><br/> <br/>                                                                                                                       |
| [<span data-ttu-id="89fbc-191">**typeTableDefinitions**</span><span class="sxs-lookup"><span data-stu-id="89fbc-191">**typeTableDefinitions**</span></span>](typetabledefinitions.md)<br/>                                         | <span data-ttu-id="89fbc-192">針對已知類型產生 XML 架構資料表的 C 常數。</span><span class="sxs-lookup"><span data-stu-id="89fbc-192">Generates C constants for XML schema tables for known types.</span></span><br/> <br/>                                                                                                                                   |



### <a name="child-element-sequence"></a><span data-ttu-id="89fbc-193">子項目順序</span><span class="sxs-lookup"><span data-stu-id="89fbc-193">Child element sequence</span></span>

``` syntax
(
  text, 
  CDATA, 
  namespaceDeclarations*, 
  namespaceDefinitions*, 
  structDeclarations*, 
  structDefinitions*, 
  typeTableDeclarations*, 
  typeTableDefinitions*, 
  thisModelMetadataDeclaration*, 
  thisModelMetadataDefinition*, 
  portTypeDeclarations*, 
  portTypeDefinitions*, 
  messageStructureDefinitions*, 
  messageTypeDeclarations*, 
  messageTypeDefinitions*, 
  idlFunctionDeclarations*, 
  subscriptionIdlFunctionDeclarations*, 
  functionDeclarations*, 
  subscriptionFunctionDeclarations*, 
  proxyFunctionImplementations*, 
  subscriptionProxyFunctionImplementations*, 
  stubDeclarations*, 
  stubDefinitions*, 
  enumerationValueDeclarations*, 
  include*, 
  IUnknownDeclarations*, 
  IUnknownDefinitions*, 
  relationshipMetadataDeclaration*, 
  relationshipMetadataDefinition*, 
  proxyBuilderDeclarations*, 
  proxyBuilderImplementations*, 
  hostBuilderDeclaration*, 
  hostBuilderImplementation*, 
  eventSourceBuilderDeclarations*, 
  eventSourceBuilderImplementations*, 
  literalInclude*
)
```

## <a name="parent-elements"></a><span data-ttu-id="89fbc-194">父元素</span><span class="sxs-lookup"><span data-stu-id="89fbc-194">Parent elements</span></span>



| <span data-ttu-id="89fbc-195">元素</span><span class="sxs-lookup"><span data-stu-id="89fbc-195">Element</span></span>                                     | <span data-ttu-id="89fbc-196">描述</span><span class="sxs-lookup"><span data-stu-id="89fbc-196">Description</span></span>                                                                          |
|---------------------------------------------|--------------------------------------------------------------------------------------|
| [<span data-ttu-id="89fbc-197">**wsdCodeGen**</span><span class="sxs-lookup"><span data-stu-id="89fbc-197">**wsdCodeGen**</span></span>](wsdcodegen.md)<br/> | <span data-ttu-id="89fbc-198">WSDAPI 程式碼產生器 XML 腳本檔的根項目。</span><span class="sxs-lookup"><span data-stu-id="89fbc-198">The root element of an WSDAPI code generator XML script file.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="89fbc-199">備註</span><span class="sxs-lookup"><span data-stu-id="89fbc-199">Remarks</span></span>

<span data-ttu-id="89fbc-200">檔案的名稱是由 name 屬性的值或子項目所決定。</span><span class="sxs-lookup"><span data-stu-id="89fbc-200">The name of the file is determined by the value of the name attribute or child element.</span></span> <span data-ttu-id="89fbc-201">檔案的內容是由 **file** 元素中的其他子項目、TEXT 和 CDATA 所決定。</span><span class="sxs-lookup"><span data-stu-id="89fbc-201">The content of the file is determined by the other child elements, text and CDATA in the **file** element.</span></span> <span data-ttu-id="89fbc-202">Text 和 CDATA 會複製到未修改的檔案。</span><span class="sxs-lookup"><span data-stu-id="89fbc-202">Text and CDATA are copied to the file unmodified.</span></span> <span data-ttu-id="89fbc-203">已產生的程式碼會取代子項目。</span><span class="sxs-lookup"><span data-stu-id="89fbc-203">Child elements are replaced with generated code.</span></span> <span data-ttu-id="89fbc-204">Text、CDATA 和子項目可能會以任何順序發生，而且可能會無限期地重複。</span><span class="sxs-lookup"><span data-stu-id="89fbc-204">Text, CDATA and child elements may occur in any order and may be repeated indefinitely.</span></span>

## <a name="element-information"></a><span data-ttu-id="89fbc-205">項目資訊</span><span class="sxs-lookup"><span data-stu-id="89fbc-205">Element information</span></span>



| <span data-ttu-id="89fbc-206">標籤</span><span class="sxs-lookup"><span data-stu-id="89fbc-206">Label</span></span> | <span data-ttu-id="89fbc-207">值</span><span class="sxs-lookup"><span data-stu-id="89fbc-207">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="89fbc-208">最低支援系統</span><span class="sxs-lookup"><span data-stu-id="89fbc-208">Minimum supported system</span></span><br/> | <span data-ttu-id="89fbc-209">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="89fbc-209">Windows Vista</span></span> |
| <span data-ttu-id="89fbc-210">可以是空的</span><span class="sxs-lookup"><span data-stu-id="89fbc-210">Can be empty</span></span>                        | <span data-ttu-id="89fbc-211">否</span><span class="sxs-lookup"><span data-stu-id="89fbc-211">No</span></span>            |



 

 




