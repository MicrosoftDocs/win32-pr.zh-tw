---
description: 深入瞭解 PageBlackGenerationProcessingGrayComponentReplacementLevel 元素，其指定灰色元件取代的百分比。
ms.assetid: e33634bb-5db5-4197-889d-82caf2e74191
title: PageBlackGenerationProcessingGrayComponentReplacementLevel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8499c8521b974d01657c171a99e86e738c82b4e5
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/19/2021
ms.locfileid: "112408481"
---
# <a name="pageblackgenerationprocessinggraycomponentreplacementlevel"></a><span data-ttu-id="cb76a-103">PageBlackGenerationProcessingGrayComponentReplacementLevel</span><span class="sxs-lookup"><span data-stu-id="cb76a-103">PageBlackGenerationProcessingGrayComponentReplacementLevel</span></span>

<span data-ttu-id="cb76a-104">本主題並非最新的。</span><span class="sxs-lookup"><span data-stu-id="cb76a-104">This topic is not current.</span></span> <span data-ttu-id="cb76a-105">如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。</span><span class="sxs-lookup"><span data-stu-id="cb76a-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="cb76a-106">指定要執行的灰色元件取代百分比。</span><span class="sxs-lookup"><span data-stu-id="cb76a-106">Specifies the percentage of gray component replacement to perform.</span></span>

-   [<span data-ttu-id="cb76a-107">項目資訊</span><span class="sxs-lookup"><span data-stu-id="cb76a-107">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="cb76a-108">結構內容</span><span class="sxs-lookup"><span data-stu-id="cb76a-108">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="cb76a-109">項目資訊</span><span class="sxs-lookup"><span data-stu-id="cb76a-109">Element Information</span></span>



| <span data-ttu-id="cb76a-110">Name</span><span class="sxs-lookup"><span data-stu-id="cb76a-110">Name</span></span> | <span data-ttu-id="cb76a-111">值</span><span class="sxs-lookup"><span data-stu-id="cb76a-111">Value</span></span> |
|----------------------------|------------------------------------------------------------|
| <span data-ttu-id="cb76a-112">項目類型</span><span class="sxs-lookup"><span data-stu-id="cb76a-112">Element Type</span></span> <br/>   | <span data-ttu-id="cb76a-113">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="cb76a-113">ParameterDef</span></span><br/>                                    |
| <span data-ttu-id="cb76a-114">範圍前置詞</span><span class="sxs-lookup"><span data-stu-id="cb76a-114">Scoping Prefix</span></span> <br/> | <span data-ttu-id="cb76a-115">頁面</span><span class="sxs-lookup"><span data-stu-id="cb76a-115">Page</span></span><br/>                                            |
| <span data-ttu-id="cb76a-116">備註</span><span class="sxs-lookup"><span data-stu-id="cb76a-116">Notes</span></span> <br/>          | <span data-ttu-id="cb76a-117">連結至 PageBlackGenerationProcessing 元素</span><span class="sxs-lookup"><span data-stu-id="cb76a-117">Linked to PageBlackGenerationProcessing element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="cb76a-118">結構內容</span><span class="sxs-lookup"><span data-stu-id="cb76a-118">Structure Content</span></span>

<span data-ttu-id="cb76a-119">此元素的 XML 結構為：</span><span class="sxs-lookup"><span data-stu-id="cb76a-119">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageBlackGenerationProcessingGrayComponentReplacementLevel">
  <psf:Property name="psf:DataType">
    <psf:Value xsi:type="xs:string">xs:integer</psf:Value>
  </psf:Property>
  <psf:Property name="psf:DefaultValue">
    <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MaxValue">
    <psf:Value xsi:type="xs:integer">100</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MinValue">
    <psf:Value xsi:type="xs:integer">0</psf:Value>
  </psf:Property>
  <psf:Property name="psf:Multiple">
    <psf:Value xsi:type="xs:integer">1</psf:Value>
  </psf:Property>
  <psf:Property name="psf:Mandatory">
    <psf:Value xsi:type="xs:string">psk:Conditional</psf:Value>
  </psf:Property>
  <psf:Property name="psf:UnitType">
    <psf:Value xsi:type="xs:string">percent</psf:Value>
  </psf:Property>
</psf:ParameterDef>
```

## <a name="structure-properties"></a><span data-ttu-id="cb76a-120">結構屬性</span><span class="sxs-lookup"><span data-stu-id="cb76a-120">Structure Properties</span></span>

<span data-ttu-id="cb76a-121">下表概述 XML 結構中所定義之變數的特性。</span><span class="sxs-lookup"><span data-stu-id="cb76a-121">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="cb76a-122">屬性</span><span class="sxs-lookup"><span data-stu-id="cb76a-122">Property</span></span>                | <span data-ttu-id="cb76a-123">xsi:type</span><span class="sxs-lookup"><span data-stu-id="cb76a-123">xsi:type</span></span>           | <span data-ttu-id="cb76a-124">值</span><span class="sxs-lookup"><span data-stu-id="cb76a-124">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="cb76a-125">DataType</span><span class="sxs-lookup"><span data-stu-id="cb76a-125">DataType</span></span><br/>     | <span data-ttu-id="cb76a-126">字串</span><span class="sxs-lookup"><span data-stu-id="cb76a-126">string</span></span><br/>  | <span data-ttu-id="cb76a-127">xs:integer</span><span class="sxs-lookup"><span data-stu-id="cb76a-127">xs:integer</span></span><br/>      |
| <span data-ttu-id="cb76a-128">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="cb76a-128">DefaultValue</span></span><br/> | <span data-ttu-id="cb76a-129">字串</span><span class="sxs-lookup"><span data-stu-id="cb76a-129">string</span></span><br/>  | <span data-ttu-id="cb76a-130">未定義</span><span class="sxs-lookup"><span data-stu-id="cb76a-130">undefined</span></span><br/>       |
| <span data-ttu-id="cb76a-131">MaxValue</span><span class="sxs-lookup"><span data-stu-id="cb76a-131">MaxValue</span></span><br/>     | <span data-ttu-id="cb76a-132">整數</span><span class="sxs-lookup"><span data-stu-id="cb76a-132">integer</span></span><br/> | <span data-ttu-id="cb76a-133">100</span><span class="sxs-lookup"><span data-stu-id="cb76a-133">100</span></span><br/>             |
| <span data-ttu-id="cb76a-134">MinValue</span><span class="sxs-lookup"><span data-stu-id="cb76a-134">MinValue</span></span><br/>     | <span data-ttu-id="cb76a-135">整數</span><span class="sxs-lookup"><span data-stu-id="cb76a-135">integer</span></span><br/> | <span data-ttu-id="cb76a-136">0</span><span class="sxs-lookup"><span data-stu-id="cb76a-136">0</span></span><br/>               |
| <span data-ttu-id="cb76a-137">多個</span><span class="sxs-lookup"><span data-stu-id="cb76a-137">Multiple</span></span><br/>     | <span data-ttu-id="cb76a-138">整數</span><span class="sxs-lookup"><span data-stu-id="cb76a-138">integer</span></span><br/> | <span data-ttu-id="cb76a-139">1</span><span class="sxs-lookup"><span data-stu-id="cb76a-139">1</span></span><br/>               |
| <span data-ttu-id="cb76a-140">強制性</span><span class="sxs-lookup"><span data-stu-id="cb76a-140">Mandatory</span></span><br/>    | <span data-ttu-id="cb76a-141">string</span><span class="sxs-lookup"><span data-stu-id="cb76a-141">string</span></span><br/>  | <span data-ttu-id="cb76a-142">psk：條件式</span><span class="sxs-lookup"><span data-stu-id="cb76a-142">psk:Conditional</span></span><br/> |
| <span data-ttu-id="cb76a-143">Unittype.pixel 表示</span><span class="sxs-lookup"><span data-stu-id="cb76a-143">UnitType</span></span><br/>     | <span data-ttu-id="cb76a-144">string</span><span class="sxs-lookup"><span data-stu-id="cb76a-144">string</span></span><br/>  | <span data-ttu-id="cb76a-145">percent</span><span class="sxs-lookup"><span data-stu-id="cb76a-145">percent</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="cb76a-146">相關主題</span><span class="sxs-lookup"><span data-stu-id="cb76a-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cb76a-147">列印架構規格</span><span class="sxs-lookup"><span data-stu-id="cb76a-147">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




