---
title: PageBlackGenerationProcessingUnderColorAdditionStart
description: 本主題並非最新的。 如需最新資訊，請參閱列印架構規格。
ms.assetid: 6c2a7bb5-436d-40ed-a855-242a6a04bc16
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41d44dbc63632479c66686cea50b781abf715c76
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/05/2021
ms.locfileid: "104386338"
---
# <a name="pageblackgenerationprocessingundercoloradditionstart"></a><span data-ttu-id="fbb0b-104">PageBlackGenerationProcessingUnderColorAdditionStart</span><span class="sxs-lookup"><span data-stu-id="fbb0b-104">PageBlackGenerationProcessingUnderColorAdditionStart</span></span>

<span data-ttu-id="fbb0b-105">本主題並非最新的。</span><span class="sxs-lookup"><span data-stu-id="fbb0b-105">This topic is not current.</span></span> <span data-ttu-id="fbb0b-106">如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。</span><span class="sxs-lookup"><span data-stu-id="fbb0b-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="fbb0b-107">描述將套用 UCA 的陰影層級。</span><span class="sxs-lookup"><span data-stu-id="fbb0b-107">Describes the shadow level below which UCA will be applied.</span></span>

-   [<span data-ttu-id="fbb0b-108">項目資訊</span><span class="sxs-lookup"><span data-stu-id="fbb0b-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="fbb0b-109">結構內容</span><span class="sxs-lookup"><span data-stu-id="fbb0b-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="fbb0b-110">項目資訊</span><span class="sxs-lookup"><span data-stu-id="fbb0b-110">Element Information</span></span>



| <span data-ttu-id="fbb0b-111">Name</span><span class="sxs-lookup"><span data-stu-id="fbb0b-111">Name</span></span>                       |                                                            |
|----------------------------|------------------------------------------------------------|
| <span data-ttu-id="fbb0b-112">項目類型</span><span class="sxs-lookup"><span data-stu-id="fbb0b-112">Element Type</span></span> <br/>   | <span data-ttu-id="fbb0b-113">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="fbb0b-113">ParameterDef</span></span><br/>                                    |
| <span data-ttu-id="fbb0b-114">範圍前置詞</span><span class="sxs-lookup"><span data-stu-id="fbb0b-114">Scoping Prefix</span></span> <br/> | <span data-ttu-id="fbb0b-115">頁面</span><span class="sxs-lookup"><span data-stu-id="fbb0b-115">Page</span></span><br/>                                            |
| <span data-ttu-id="fbb0b-116">備註</span><span class="sxs-lookup"><span data-stu-id="fbb0b-116">Notes</span></span> <br/>          | <span data-ttu-id="fbb0b-117">連結至 PageBlackGenerationProcessing 元素</span><span class="sxs-lookup"><span data-stu-id="fbb0b-117">Linked to PageBlackGenerationProcessing element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="fbb0b-118">結構內容</span><span class="sxs-lookup"><span data-stu-id="fbb0b-118">Structure Content</span></span>

<span data-ttu-id="fbb0b-119">此元素的 XML 結構為：</span><span class="sxs-lookup"><span data-stu-id="fbb0b-119">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="fbb0b-120">結構屬性</span><span class="sxs-lookup"><span data-stu-id="fbb0b-120">Structure Properties</span></span>

<span data-ttu-id="fbb0b-121">下表概述 XML 結構中所定義之變數的特性。</span><span class="sxs-lookup"><span data-stu-id="fbb0b-121">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="fbb0b-122">屬性</span><span class="sxs-lookup"><span data-stu-id="fbb0b-122">Property</span></span>                | <span data-ttu-id="fbb0b-123">xsi:type</span><span class="sxs-lookup"><span data-stu-id="fbb0b-123">xsi:type</span></span>           | <span data-ttu-id="fbb0b-124">值</span><span class="sxs-lookup"><span data-stu-id="fbb0b-124">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="fbb0b-125">DataType</span><span class="sxs-lookup"><span data-stu-id="fbb0b-125">DataType</span></span><br/>     | <span data-ttu-id="fbb0b-126">字串</span><span class="sxs-lookup"><span data-stu-id="fbb0b-126">string</span></span><br/>  | <span data-ttu-id="fbb0b-127">xs:integer</span><span class="sxs-lookup"><span data-stu-id="fbb0b-127">xs:integer</span></span><br/>      |
| <span data-ttu-id="fbb0b-128">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="fbb0b-128">DefaultValue</span></span><br/> | <span data-ttu-id="fbb0b-129">字串</span><span class="sxs-lookup"><span data-stu-id="fbb0b-129">string</span></span><br/>  | <span data-ttu-id="fbb0b-130">未定義</span><span class="sxs-lookup"><span data-stu-id="fbb0b-130">undefined</span></span><br/>       |
| <span data-ttu-id="fbb0b-131">MaxValue</span><span class="sxs-lookup"><span data-stu-id="fbb0b-131">MaxValue</span></span><br/>     | <span data-ttu-id="fbb0b-132">整數</span><span class="sxs-lookup"><span data-stu-id="fbb0b-132">integer</span></span><br/> | <span data-ttu-id="fbb0b-133">100</span><span class="sxs-lookup"><span data-stu-id="fbb0b-133">100</span></span><br/>             |
| <span data-ttu-id="fbb0b-134">MinValue</span><span class="sxs-lookup"><span data-stu-id="fbb0b-134">MinValue</span></span><br/>     | <span data-ttu-id="fbb0b-135">整數</span><span class="sxs-lookup"><span data-stu-id="fbb0b-135">integer</span></span><br/> | <span data-ttu-id="fbb0b-136">0</span><span class="sxs-lookup"><span data-stu-id="fbb0b-136">0</span></span><br/>               |
| <span data-ttu-id="fbb0b-137">多個</span><span class="sxs-lookup"><span data-stu-id="fbb0b-137">Multiple</span></span><br/>     | <span data-ttu-id="fbb0b-138">整數</span><span class="sxs-lookup"><span data-stu-id="fbb0b-138">integer</span></span><br/> | <span data-ttu-id="fbb0b-139">1</span><span class="sxs-lookup"><span data-stu-id="fbb0b-139">1</span></span><br/>               |
| <span data-ttu-id="fbb0b-140">強制性</span><span class="sxs-lookup"><span data-stu-id="fbb0b-140">Mandatory</span></span><br/>    | <span data-ttu-id="fbb0b-141">字串</span><span class="sxs-lookup"><span data-stu-id="fbb0b-141">string</span></span><br/>  | <span data-ttu-id="fbb0b-142">psk：條件式</span><span class="sxs-lookup"><span data-stu-id="fbb0b-142">psk:Conditional</span></span><br/> |
| <span data-ttu-id="fbb0b-143">Unittype.pixel 表示</span><span class="sxs-lookup"><span data-stu-id="fbb0b-143">UnitType</span></span><br/>     | <span data-ttu-id="fbb0b-144">字串</span><span class="sxs-lookup"><span data-stu-id="fbb0b-144">string</span></span><br/>  | <span data-ttu-id="fbb0b-145">percent</span><span class="sxs-lookup"><span data-stu-id="fbb0b-145">percent</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="fbb0b-146">相關主題</span><span class="sxs-lookup"><span data-stu-id="fbb0b-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fbb0b-147">列印架構規格</span><span class="sxs-lookup"><span data-stu-id="fbb0b-147">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




