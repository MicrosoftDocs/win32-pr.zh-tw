---
description: 深入瞭解 DocumentPageRanges 元素，其描述頁面中檔的輸出範圍。
ms.assetid: 4cd1b0f8-7f7e-40cc-8d19-d44187822cd1
title: DocumentPageRanges
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e854736c72b3bff5ba2e4750e0b09e0b87c2c9f
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/19/2021
ms.locfileid: "112409251"
---
# <a name="documentpageranges"></a><span data-ttu-id="47be4-103">DocumentPageRanges</span><span class="sxs-lookup"><span data-stu-id="47be4-103">DocumentPageRanges</span></span>

<span data-ttu-id="47be4-104">本主題並非最新的。</span><span class="sxs-lookup"><span data-stu-id="47be4-104">This topic is not current.</span></span> <span data-ttu-id="47be4-105">如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。</span><span class="sxs-lookup"><span data-stu-id="47be4-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="47be4-106">描述頁面中檔的輸出範圍。</span><span class="sxs-lookup"><span data-stu-id="47be4-106">Describes the output range of the document in pages.</span></span> <span data-ttu-id="47be4-107">參數值必須符合下列結構：</span><span class="sxs-lookup"><span data-stu-id="47be4-107">The parameter value must conform to the following structure:</span></span>

-   <span data-ttu-id="47be4-108">PageRangeText： "*PageRange*" 或 "*PageRange*，*PageRange*"</span><span class="sxs-lookup"><span data-stu-id="47be4-108">PageRangeText: "*PageRange*" or "*PageRange*,*PageRange*"</span></span>

-   <span data-ttu-id="47be4-109">PageRange： "*PageNumber*" 或 "*PageNumber* - *PageNumber*"</span><span class="sxs-lookup"><span data-stu-id="47be4-109">PageRange: "*PageNumber*" or "*PageNumber*-*PageNumber*"</span></span>

-   <span data-ttu-id="47be4-110">PageNumber：1到 N，其中 N 是檔中的頁面數目。</span><span class="sxs-lookup"><span data-stu-id="47be4-110">PageNumber: 1 to N, where N is the number of pages in the document.</span></span> <span data-ttu-id="47be4-111">如果 *PageNumber* > N，則 *PageNumber* = n。</span><span class="sxs-lookup"><span data-stu-id="47be4-111">If *PageNumber* > N, then *PageNumber* = N.</span></span>

<span data-ttu-id="47be4-112">應忽略字串中的空白字元。</span><span class="sxs-lookup"><span data-stu-id="47be4-112">Whitespace in the string should be ignored.</span></span>

-   [<span data-ttu-id="47be4-113">項目資訊</span><span class="sxs-lookup"><span data-stu-id="47be4-113">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="47be4-114">結構化內容</span><span class="sxs-lookup"><span data-stu-id="47be4-114">Structural Content</span></span>](#structural-content)

## <a name="element-information"></a><span data-ttu-id="47be4-115">項目資訊</span><span class="sxs-lookup"><span data-stu-id="47be4-115">Element Information</span></span>



| <span data-ttu-id="47be4-116">Name</span><span class="sxs-lookup"><span data-stu-id="47be4-116">Name</span></span> | <span data-ttu-id="47be4-117">值</span><span class="sxs-lookup"><span data-stu-id="47be4-117">Value</span></span> |
|----------------------------|-------------------------|
| <span data-ttu-id="47be4-118">項目類型</span><span class="sxs-lookup"><span data-stu-id="47be4-118">Element Type</span></span> <br/>   | <span data-ttu-id="47be4-119">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="47be4-119">ParameterDef</span></span><br/> |
| <span data-ttu-id="47be4-120">範圍前置詞</span><span class="sxs-lookup"><span data-stu-id="47be4-120">Scoping Prefix</span></span> <br/> | <span data-ttu-id="47be4-121">文件</span><span class="sxs-lookup"><span data-stu-id="47be4-121">Document</span></span><br/>     |
| <span data-ttu-id="47be4-122">注意</span><span class="sxs-lookup"><span data-stu-id="47be4-122">Notes</span></span> <br/>          | <span data-ttu-id="47be4-123">None</span><span class="sxs-lookup"><span data-stu-id="47be4-123">None</span></span><br/>         |



 

## <a name="structural-content"></a><span data-ttu-id="47be4-124">結構化內容</span><span class="sxs-lookup"><span data-stu-id="47be4-124">Structural Content</span></span>

<span data-ttu-id="47be4-125">此元素的 XML 結構為：</span><span class="sxs-lookup"><span data-stu-id="47be4-125">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:DocumentPageRanges">
  <psf:Property name="psf:DataType">
    <psf:Value xsi:type="xs:string">xs:string</psf:Value>
  </psf:Property>
  <psf:Property name="psf:DefaultValue">
    <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MaxLength">
    <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MinLength">
    <psf:Value xsi:type="xs:integer">1</psf:Value>
  </psf:Property>
  <psf:Property name="psf:Mandatory">
    <psf:Value xsi:type="xs:string">psk:Conditional</psf:Value>
  </psf:Property>
  <psf:Property name="psf:UnitType">
    <psf:Value xsi:type="xs:string">characters</psf:Value>
  </psf:Property>
</psf:ParameterDef>
      
```

## <a name="structure-properties"></a><span data-ttu-id="47be4-126">結構屬性</span><span class="sxs-lookup"><span data-stu-id="47be4-126">Structure Properties</span></span>

<span data-ttu-id="47be4-127">下表概述 XML 結構中所定義之變數的特性。</span><span class="sxs-lookup"><span data-stu-id="47be4-127">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="47be4-128">屬性</span><span class="sxs-lookup"><span data-stu-id="47be4-128">Property</span></span>                | <span data-ttu-id="47be4-129">xsi:type</span><span class="sxs-lookup"><span data-stu-id="47be4-129">xsi:type</span></span>           | <span data-ttu-id="47be4-130">值</span><span class="sxs-lookup"><span data-stu-id="47be4-130">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="47be4-131">DataType</span><span class="sxs-lookup"><span data-stu-id="47be4-131">DataType</span></span><br/>     | <span data-ttu-id="47be4-132">字串</span><span class="sxs-lookup"><span data-stu-id="47be4-132">string</span></span><br/>  | <span data-ttu-id="47be4-133">xs:string</span><span class="sxs-lookup"><span data-stu-id="47be4-133">xs:string</span></span><br/>       |
| <span data-ttu-id="47be4-134">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="47be4-134">DefaultValue</span></span><br/> | <span data-ttu-id="47be4-135">字串</span><span class="sxs-lookup"><span data-stu-id="47be4-135">string</span></span><br/>  | <span data-ttu-id="47be4-136">未定義</span><span class="sxs-lookup"><span data-stu-id="47be4-136">undefined</span></span><br/>       |
| <span data-ttu-id="47be4-137">MaxLength</span><span class="sxs-lookup"><span data-stu-id="47be4-137">MaxLength</span></span><br/>    | <span data-ttu-id="47be4-138">整數</span><span class="sxs-lookup"><span data-stu-id="47be4-138">integer</span></span><br/> | <span data-ttu-id="47be4-139">未定義</span><span class="sxs-lookup"><span data-stu-id="47be4-139">undefined</span></span><br/>       |
| <span data-ttu-id="47be4-140">MinLength</span><span class="sxs-lookup"><span data-stu-id="47be4-140">MinLength</span></span><br/>    | <span data-ttu-id="47be4-141">整數</span><span class="sxs-lookup"><span data-stu-id="47be4-141">integer</span></span><br/> | <span data-ttu-id="47be4-142">1</span><span class="sxs-lookup"><span data-stu-id="47be4-142">1</span></span><br/>               |
| <span data-ttu-id="47be4-143">強制性</span><span class="sxs-lookup"><span data-stu-id="47be4-143">Mandatory</span></span><br/>    | <span data-ttu-id="47be4-144">string</span><span class="sxs-lookup"><span data-stu-id="47be4-144">string</span></span><br/>  | <span data-ttu-id="47be4-145">psk：條件式</span><span class="sxs-lookup"><span data-stu-id="47be4-145">psk:Conditional</span></span><br/> |
| <span data-ttu-id="47be4-146">Unittype.pixel 表示</span><span class="sxs-lookup"><span data-stu-id="47be4-146">UnitType</span></span><br/>     | <span data-ttu-id="47be4-147">string</span><span class="sxs-lookup"><span data-stu-id="47be4-147">string</span></span><br/>  | <span data-ttu-id="47be4-148">字元</span><span class="sxs-lookup"><span data-stu-id="47be4-148">characters</span></span><br/>      |



 

## <a name="related-topics"></a><span data-ttu-id="47be4-149">相關主題</span><span class="sxs-lookup"><span data-stu-id="47be4-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="47be4-150">列印架構規格</span><span class="sxs-lookup"><span data-stu-id="47be4-150">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




