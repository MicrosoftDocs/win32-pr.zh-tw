---
title: PageBlackGenerationProcessingUnderColorAdditionStart
description: 本主題並非最新的。 如需最新資訊，請參閱列印架構規格。
ms.assetid: 6c2a7bb5-436d-40ed-a855-242a6a04bc16
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 595bc3e4514b1a2e8a4d302005b97e2625a560e2
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/26/2021
ms.locfileid: "107999185"
---
# <a name="pageblackgenerationprocessingundercoloradditionstart"></a><span data-ttu-id="2cd8c-104">PageBlackGenerationProcessingUnderColorAdditionStart</span><span class="sxs-lookup"><span data-stu-id="2cd8c-104">PageBlackGenerationProcessingUnderColorAdditionStart</span></span>

<span data-ttu-id="2cd8c-105">本主題並非最新的。</span><span class="sxs-lookup"><span data-stu-id="2cd8c-105">This topic is not current.</span></span> <span data-ttu-id="2cd8c-106">如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。</span><span class="sxs-lookup"><span data-stu-id="2cd8c-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="2cd8c-107">描述將套用 UCA 的陰影層級。</span><span class="sxs-lookup"><span data-stu-id="2cd8c-107">Describes the shadow level below which UCA will be applied.</span></span>

-   [<span data-ttu-id="2cd8c-108">項目資訊</span><span class="sxs-lookup"><span data-stu-id="2cd8c-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="2cd8c-109">結構內容</span><span class="sxs-lookup"><span data-stu-id="2cd8c-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="2cd8c-110">項目資訊</span><span class="sxs-lookup"><span data-stu-id="2cd8c-110">Element Information</span></span>



| <span data-ttu-id="2cd8c-111">Name</span><span class="sxs-lookup"><span data-stu-id="2cd8c-111">Name</span></span> | <span data-ttu-id="2cd8c-112">值</span><span class="sxs-lookup"><span data-stu-id="2cd8c-112">Value</span></span> |
|----------------------------|------------------------------------------------------------|
| <span data-ttu-id="2cd8c-113">項目類型</span><span class="sxs-lookup"><span data-stu-id="2cd8c-113">Element Type</span></span> <br/>   | <span data-ttu-id="2cd8c-114">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="2cd8c-114">ParameterDef</span></span><br/>                                    |
| <span data-ttu-id="2cd8c-115">範圍前置詞</span><span class="sxs-lookup"><span data-stu-id="2cd8c-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="2cd8c-116">頁面</span><span class="sxs-lookup"><span data-stu-id="2cd8c-116">Page</span></span><br/>                                            |
| <span data-ttu-id="2cd8c-117">備註</span><span class="sxs-lookup"><span data-stu-id="2cd8c-117">Notes</span></span> <br/>          | <span data-ttu-id="2cd8c-118">連結至 PageBlackGenerationProcessing 元素</span><span class="sxs-lookup"><span data-stu-id="2cd8c-118">Linked to PageBlackGenerationProcessing element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="2cd8c-119">結構內容</span><span class="sxs-lookup"><span data-stu-id="2cd8c-119">Structure Content</span></span>

<span data-ttu-id="2cd8c-120">此元素的 XML 結構為：</span><span class="sxs-lookup"><span data-stu-id="2cd8c-120">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="2cd8c-121">結構屬性</span><span class="sxs-lookup"><span data-stu-id="2cd8c-121">Structure Properties</span></span>

<span data-ttu-id="2cd8c-122">下表概述 XML 結構中所定義之變數的特性。</span><span class="sxs-lookup"><span data-stu-id="2cd8c-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="2cd8c-123">屬性</span><span class="sxs-lookup"><span data-stu-id="2cd8c-123">Property</span></span>                | <span data-ttu-id="2cd8c-124">xsi:type</span><span class="sxs-lookup"><span data-stu-id="2cd8c-124">xsi:type</span></span>           | <span data-ttu-id="2cd8c-125">值</span><span class="sxs-lookup"><span data-stu-id="2cd8c-125">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="2cd8c-126">DataType</span><span class="sxs-lookup"><span data-stu-id="2cd8c-126">DataType</span></span><br/>     | <span data-ttu-id="2cd8c-127">字串</span><span class="sxs-lookup"><span data-stu-id="2cd8c-127">string</span></span><br/>  | <span data-ttu-id="2cd8c-128">xs:integer</span><span class="sxs-lookup"><span data-stu-id="2cd8c-128">xs:integer</span></span><br/>      |
| <span data-ttu-id="2cd8c-129">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="2cd8c-129">DefaultValue</span></span><br/> | <span data-ttu-id="2cd8c-130">字串</span><span class="sxs-lookup"><span data-stu-id="2cd8c-130">string</span></span><br/>  | <span data-ttu-id="2cd8c-131">未定義</span><span class="sxs-lookup"><span data-stu-id="2cd8c-131">undefined</span></span><br/>       |
| <span data-ttu-id="2cd8c-132">MaxValue</span><span class="sxs-lookup"><span data-stu-id="2cd8c-132">MaxValue</span></span><br/>     | <span data-ttu-id="2cd8c-133">整數</span><span class="sxs-lookup"><span data-stu-id="2cd8c-133">integer</span></span><br/> | <span data-ttu-id="2cd8c-134">100</span><span class="sxs-lookup"><span data-stu-id="2cd8c-134">100</span></span><br/>             |
| <span data-ttu-id="2cd8c-135">MinValue</span><span class="sxs-lookup"><span data-stu-id="2cd8c-135">MinValue</span></span><br/>     | <span data-ttu-id="2cd8c-136">整數</span><span class="sxs-lookup"><span data-stu-id="2cd8c-136">integer</span></span><br/> | <span data-ttu-id="2cd8c-137">0</span><span class="sxs-lookup"><span data-stu-id="2cd8c-137">0</span></span><br/>               |
| <span data-ttu-id="2cd8c-138">多個</span><span class="sxs-lookup"><span data-stu-id="2cd8c-138">Multiple</span></span><br/>     | <span data-ttu-id="2cd8c-139">整數</span><span class="sxs-lookup"><span data-stu-id="2cd8c-139">integer</span></span><br/> | <span data-ttu-id="2cd8c-140">1</span><span class="sxs-lookup"><span data-stu-id="2cd8c-140">1</span></span><br/>               |
| <span data-ttu-id="2cd8c-141">強制性</span><span class="sxs-lookup"><span data-stu-id="2cd8c-141">Mandatory</span></span><br/>    | <span data-ttu-id="2cd8c-142">字串</span><span class="sxs-lookup"><span data-stu-id="2cd8c-142">string</span></span><br/>  | <span data-ttu-id="2cd8c-143">psk：條件式</span><span class="sxs-lookup"><span data-stu-id="2cd8c-143">psk:Conditional</span></span><br/> |
| <span data-ttu-id="2cd8c-144">Unittype.pixel 表示</span><span class="sxs-lookup"><span data-stu-id="2cd8c-144">UnitType</span></span><br/>     | <span data-ttu-id="2cd8c-145">字串</span><span class="sxs-lookup"><span data-stu-id="2cd8c-145">string</span></span><br/>  | <span data-ttu-id="2cd8c-146">percent</span><span class="sxs-lookup"><span data-stu-id="2cd8c-146">percent</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="2cd8c-147">相關主題</span><span class="sxs-lookup"><span data-stu-id="2cd8c-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2cd8c-148">列印架構規格</span><span class="sxs-lookup"><span data-stu-id="2cd8c-148">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




