---
title: PageBlackGenerationProcessingUnderColorAdditionStart
description: 檢查 PageBlackGenerationProcessingUnderColorAdditionStart 參數。 本主題並非最新的。 如需最新資訊，請參閱列印架構規格。
ms.assetid: 6c2a7bb5-436d-40ed-a855-242a6a04bc16
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11bdbd970f30a7d573b7c803ea447e4ac3e94ca2
ms.sourcegitcommit: 998d50f6def8a25850fc113fc8a2df903c829c5e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/09/2021
ms.locfileid: "113549346"
---
# <a name="pageblackgenerationprocessingundercoloradditionstart"></a><span data-ttu-id="dca0a-105">PageBlackGenerationProcessingUnderColorAdditionStart</span><span class="sxs-lookup"><span data-stu-id="dca0a-105">PageBlackGenerationProcessingUnderColorAdditionStart</span></span>

<span data-ttu-id="dca0a-106">本主題並非最新的。</span><span class="sxs-lookup"><span data-stu-id="dca0a-106">This topic is not current.</span></span> <span data-ttu-id="dca0a-107">如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。</span><span class="sxs-lookup"><span data-stu-id="dca0a-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="dca0a-108">描述將套用 UCA 的陰影層級。</span><span class="sxs-lookup"><span data-stu-id="dca0a-108">Describes the shadow level below which UCA will be applied.</span></span>

-   [<span data-ttu-id="dca0a-109">項目資訊</span><span class="sxs-lookup"><span data-stu-id="dca0a-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="dca0a-110">結構內容</span><span class="sxs-lookup"><span data-stu-id="dca0a-110">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="dca0a-111">項目資訊</span><span class="sxs-lookup"><span data-stu-id="dca0a-111">Element Information</span></span>



| <span data-ttu-id="dca0a-112">Name</span><span class="sxs-lookup"><span data-stu-id="dca0a-112">Name</span></span> | <span data-ttu-id="dca0a-113">值</span><span class="sxs-lookup"><span data-stu-id="dca0a-113">Value</span></span> |
|----------------------------|------------------------------------------------------------|
| <span data-ttu-id="dca0a-114">項目類型</span><span class="sxs-lookup"><span data-stu-id="dca0a-114">Element Type</span></span> <br/>   | <span data-ttu-id="dca0a-115">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="dca0a-115">ParameterDef</span></span><br/>                                    |
| <span data-ttu-id="dca0a-116">範圍前置詞</span><span class="sxs-lookup"><span data-stu-id="dca0a-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="dca0a-117">頁面</span><span class="sxs-lookup"><span data-stu-id="dca0a-117">Page</span></span><br/>                                            |
| <span data-ttu-id="dca0a-118">備註</span><span class="sxs-lookup"><span data-stu-id="dca0a-118">Notes</span></span> <br/>          | <span data-ttu-id="dca0a-119">連結至 PageBlackGenerationProcessing 元素</span><span class="sxs-lookup"><span data-stu-id="dca0a-119">Linked to PageBlackGenerationProcessing element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="dca0a-120">結構內容</span><span class="sxs-lookup"><span data-stu-id="dca0a-120">Structure Content</span></span>

<span data-ttu-id="dca0a-121">此元素的 XML 結構為：</span><span class="sxs-lookup"><span data-stu-id="dca0a-121">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageBlackGenerationProcessingUnderColorAdditionStart">
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

## <a name="structure-properties"></a><span data-ttu-id="dca0a-122">結構屬性</span><span class="sxs-lookup"><span data-stu-id="dca0a-122">Structure Properties</span></span>

<span data-ttu-id="dca0a-123">下表概述 XML 結構中所定義之變數的特性。</span><span class="sxs-lookup"><span data-stu-id="dca0a-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="dca0a-124">屬性</span><span class="sxs-lookup"><span data-stu-id="dca0a-124">Property</span></span>                | <span data-ttu-id="dca0a-125">xsi:type</span><span class="sxs-lookup"><span data-stu-id="dca0a-125">xsi:type</span></span>           | <span data-ttu-id="dca0a-126">值</span><span class="sxs-lookup"><span data-stu-id="dca0a-126">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="dca0a-127">DataType</span><span class="sxs-lookup"><span data-stu-id="dca0a-127">DataType</span></span><br/>     | <span data-ttu-id="dca0a-128">字串</span><span class="sxs-lookup"><span data-stu-id="dca0a-128">string</span></span><br/>  | <span data-ttu-id="dca0a-129">xs:integer</span><span class="sxs-lookup"><span data-stu-id="dca0a-129">xs:integer</span></span><br/>      |
| <span data-ttu-id="dca0a-130">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="dca0a-130">DefaultValue</span></span><br/> | <span data-ttu-id="dca0a-131">字串</span><span class="sxs-lookup"><span data-stu-id="dca0a-131">string</span></span><br/>  | <span data-ttu-id="dca0a-132">未定義</span><span class="sxs-lookup"><span data-stu-id="dca0a-132">undefined</span></span><br/>       |
| <span data-ttu-id="dca0a-133">MaxValue</span><span class="sxs-lookup"><span data-stu-id="dca0a-133">MaxValue</span></span><br/>     | <span data-ttu-id="dca0a-134">整數</span><span class="sxs-lookup"><span data-stu-id="dca0a-134">integer</span></span><br/> | <span data-ttu-id="dca0a-135">100</span><span class="sxs-lookup"><span data-stu-id="dca0a-135">100</span></span><br/>             |
| <span data-ttu-id="dca0a-136">MinValue</span><span class="sxs-lookup"><span data-stu-id="dca0a-136">MinValue</span></span><br/>     | <span data-ttu-id="dca0a-137">整數</span><span class="sxs-lookup"><span data-stu-id="dca0a-137">integer</span></span><br/> | <span data-ttu-id="dca0a-138">0</span><span class="sxs-lookup"><span data-stu-id="dca0a-138">0</span></span><br/>               |
| <span data-ttu-id="dca0a-139">多個</span><span class="sxs-lookup"><span data-stu-id="dca0a-139">Multiple</span></span><br/>     | <span data-ttu-id="dca0a-140">整數</span><span class="sxs-lookup"><span data-stu-id="dca0a-140">integer</span></span><br/> | <span data-ttu-id="dca0a-141">1</span><span class="sxs-lookup"><span data-stu-id="dca0a-141">1</span></span><br/>               |
| <span data-ttu-id="dca0a-142">強制性</span><span class="sxs-lookup"><span data-stu-id="dca0a-142">Mandatory</span></span><br/>    | <span data-ttu-id="dca0a-143">string</span><span class="sxs-lookup"><span data-stu-id="dca0a-143">string</span></span><br/>  | <span data-ttu-id="dca0a-144">psk：條件式</span><span class="sxs-lookup"><span data-stu-id="dca0a-144">psk:Conditional</span></span><br/> |
| <span data-ttu-id="dca0a-145">Unittype.pixel 表示</span><span class="sxs-lookup"><span data-stu-id="dca0a-145">UnitType</span></span><br/>     | <span data-ttu-id="dca0a-146">string</span><span class="sxs-lookup"><span data-stu-id="dca0a-146">string</span></span><br/>  | <span data-ttu-id="dca0a-147">percent</span><span class="sxs-lookup"><span data-stu-id="dca0a-147">percent</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="dca0a-148">相關主題</span><span class="sxs-lookup"><span data-stu-id="dca0a-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dca0a-149">列印架構規格</span><span class="sxs-lookup"><span data-stu-id="dca0a-149">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




