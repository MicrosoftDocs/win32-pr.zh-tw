---
description: 本主題並非最新的。 如需最新資訊，請參閱列印架構規格。
ms.assetid: 4cd1b0f8-7f7e-40cc-8d19-d44187822cd1
title: DocumentPageRanges
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84ded7c18fc781fd4374feb8958a98b845d95546
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/26/2021
ms.locfileid: "107997175"
---
# <a name="documentpageranges"></a><span data-ttu-id="69a81-104">DocumentPageRanges</span><span class="sxs-lookup"><span data-stu-id="69a81-104">DocumentPageRanges</span></span>

<span data-ttu-id="69a81-105">本主題並非最新的。</span><span class="sxs-lookup"><span data-stu-id="69a81-105">This topic is not current.</span></span> <span data-ttu-id="69a81-106">如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。</span><span class="sxs-lookup"><span data-stu-id="69a81-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="69a81-107">描述頁面中檔的輸出範圍。</span><span class="sxs-lookup"><span data-stu-id="69a81-107">Describes the output range of the document in pages.</span></span> <span data-ttu-id="69a81-108">參數值必須符合下列結構：</span><span class="sxs-lookup"><span data-stu-id="69a81-108">The parameter value must conform to the following structure:</span></span>

-   <span data-ttu-id="69a81-109">PageRangeText： "*PageRange*" 或 "*PageRange*，*PageRange*"</span><span class="sxs-lookup"><span data-stu-id="69a81-109">PageRangeText: "*PageRange*" or "*PageRange*,*PageRange*"</span></span>

-   <span data-ttu-id="69a81-110">PageRange： "*PageNumber*" 或 "*PageNumber* - *PageNumber*"</span><span class="sxs-lookup"><span data-stu-id="69a81-110">PageRange: "*PageNumber*" or "*PageNumber*-*PageNumber*"</span></span>

-   <span data-ttu-id="69a81-111">PageNumber：1到 N，其中 N 是檔中的頁面數目。</span><span class="sxs-lookup"><span data-stu-id="69a81-111">PageNumber: 1 to N, where N is the number of pages in the document.</span></span> <span data-ttu-id="69a81-112">如果 *PageNumber* > N，則 *PageNumber* = n。</span><span class="sxs-lookup"><span data-stu-id="69a81-112">If *PageNumber* > N, then *PageNumber* = N.</span></span>

<span data-ttu-id="69a81-113">應忽略字串中的空白字元。</span><span class="sxs-lookup"><span data-stu-id="69a81-113">Whitespace in the string should be ignored.</span></span>

-   [<span data-ttu-id="69a81-114">項目資訊</span><span class="sxs-lookup"><span data-stu-id="69a81-114">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="69a81-115">結構化內容</span><span class="sxs-lookup"><span data-stu-id="69a81-115">Structural Content</span></span>](#structural-content)

## <a name="element-information"></a><span data-ttu-id="69a81-116">項目資訊</span><span class="sxs-lookup"><span data-stu-id="69a81-116">Element Information</span></span>



| <span data-ttu-id="69a81-117">Name</span><span class="sxs-lookup"><span data-stu-id="69a81-117">Name</span></span> | <span data-ttu-id="69a81-118">值</span><span class="sxs-lookup"><span data-stu-id="69a81-118">Value</span></span> |
|----------------------------|-------------------------|
| <span data-ttu-id="69a81-119">項目類型</span><span class="sxs-lookup"><span data-stu-id="69a81-119">Element Type</span></span> <br/>   | <span data-ttu-id="69a81-120">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="69a81-120">ParameterDef</span></span><br/> |
| <span data-ttu-id="69a81-121">範圍前置詞</span><span class="sxs-lookup"><span data-stu-id="69a81-121">Scoping Prefix</span></span> <br/> | <span data-ttu-id="69a81-122">文件</span><span class="sxs-lookup"><span data-stu-id="69a81-122">Document</span></span><br/>     |
| <span data-ttu-id="69a81-123">注意</span><span class="sxs-lookup"><span data-stu-id="69a81-123">Notes</span></span> <br/>          | <span data-ttu-id="69a81-124">None</span><span class="sxs-lookup"><span data-stu-id="69a81-124">None</span></span><br/>         |



 

## <a name="structural-content"></a><span data-ttu-id="69a81-125">結構化內容</span><span class="sxs-lookup"><span data-stu-id="69a81-125">Structural Content</span></span>

<span data-ttu-id="69a81-126">此元素的 XML 結構為：</span><span class="sxs-lookup"><span data-stu-id="69a81-126">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="69a81-127">結構屬性</span><span class="sxs-lookup"><span data-stu-id="69a81-127">Structure Properties</span></span>

<span data-ttu-id="69a81-128">下表概述 XML 結構中所定義之變數的特性。</span><span class="sxs-lookup"><span data-stu-id="69a81-128">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="69a81-129">屬性</span><span class="sxs-lookup"><span data-stu-id="69a81-129">Property</span></span>                | <span data-ttu-id="69a81-130">xsi:type</span><span class="sxs-lookup"><span data-stu-id="69a81-130">xsi:type</span></span>           | <span data-ttu-id="69a81-131">值</span><span class="sxs-lookup"><span data-stu-id="69a81-131">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="69a81-132">DataType</span><span class="sxs-lookup"><span data-stu-id="69a81-132">DataType</span></span><br/>     | <span data-ttu-id="69a81-133">字串</span><span class="sxs-lookup"><span data-stu-id="69a81-133">string</span></span><br/>  | <span data-ttu-id="69a81-134">xs:string</span><span class="sxs-lookup"><span data-stu-id="69a81-134">xs:string</span></span><br/>       |
| <span data-ttu-id="69a81-135">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="69a81-135">DefaultValue</span></span><br/> | <span data-ttu-id="69a81-136">字串</span><span class="sxs-lookup"><span data-stu-id="69a81-136">string</span></span><br/>  | <span data-ttu-id="69a81-137">未定義</span><span class="sxs-lookup"><span data-stu-id="69a81-137">undefined</span></span><br/>       |
| <span data-ttu-id="69a81-138">MaxLength</span><span class="sxs-lookup"><span data-stu-id="69a81-138">MaxLength</span></span><br/>    | <span data-ttu-id="69a81-139">整數</span><span class="sxs-lookup"><span data-stu-id="69a81-139">integer</span></span><br/> | <span data-ttu-id="69a81-140">未定義</span><span class="sxs-lookup"><span data-stu-id="69a81-140">undefined</span></span><br/>       |
| <span data-ttu-id="69a81-141">MinLength</span><span class="sxs-lookup"><span data-stu-id="69a81-141">MinLength</span></span><br/>    | <span data-ttu-id="69a81-142">整數</span><span class="sxs-lookup"><span data-stu-id="69a81-142">integer</span></span><br/> | <span data-ttu-id="69a81-143">1</span><span class="sxs-lookup"><span data-stu-id="69a81-143">1</span></span><br/>               |
| <span data-ttu-id="69a81-144">強制性</span><span class="sxs-lookup"><span data-stu-id="69a81-144">Mandatory</span></span><br/>    | <span data-ttu-id="69a81-145">字串</span><span class="sxs-lookup"><span data-stu-id="69a81-145">string</span></span><br/>  | <span data-ttu-id="69a81-146">psk：條件式</span><span class="sxs-lookup"><span data-stu-id="69a81-146">psk:Conditional</span></span><br/> |
| <span data-ttu-id="69a81-147">Unittype.pixel 表示</span><span class="sxs-lookup"><span data-stu-id="69a81-147">UnitType</span></span><br/>     | <span data-ttu-id="69a81-148">字串</span><span class="sxs-lookup"><span data-stu-id="69a81-148">string</span></span><br/>  | <span data-ttu-id="69a81-149">字元</span><span class="sxs-lookup"><span data-stu-id="69a81-149">characters</span></span><br/>      |



 

## <a name="related-topics"></a><span data-ttu-id="69a81-150">相關主題</span><span class="sxs-lookup"><span data-stu-id="69a81-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="69a81-151">列印架構規格</span><span class="sxs-lookup"><span data-stu-id="69a81-151">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




