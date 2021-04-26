---
description: 本主題並非最新的。 如需最新資訊，請參閱列印架構規格。
ms.assetid: e82394d1-f765-4679-b1de-ea17825d6478
title: PageScalingOffsetWidth
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b82c2b0c0f2c86a792706ec7e00819ccda1038c
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/26/2021
ms.locfileid: "107997955"
---
# <a name="pagescalingoffsetwidth"></a><span data-ttu-id="88de7-104">PageScalingOffsetWidth</span><span class="sxs-lookup"><span data-stu-id="88de7-104">PageScalingOffsetWidth</span></span>

<span data-ttu-id="88de7-105">本主題並非最新的。</span><span class="sxs-lookup"><span data-stu-id="88de7-105">This topic is not current.</span></span> <span data-ttu-id="88de7-106">如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。</span><span class="sxs-lookup"><span data-stu-id="88de7-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="88de7-107">針對自訂縮放比例指定 ImageableSizeWidth 方向的縮放位移。</span><span class="sxs-lookup"><span data-stu-id="88de7-107">Specifies the scaling offset in the ImageableSizeWidth direction for custom scaling.</span></span>

-   [<span data-ttu-id="88de7-108">項目資訊</span><span class="sxs-lookup"><span data-stu-id="88de7-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="88de7-109">結構內容</span><span class="sxs-lookup"><span data-stu-id="88de7-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="88de7-110">項目資訊</span><span class="sxs-lookup"><span data-stu-id="88de7-110">Element Information</span></span>



| <span data-ttu-id="88de7-111">Name</span><span class="sxs-lookup"><span data-stu-id="88de7-111">Name</span></span> | <span data-ttu-id="88de7-112">值</span><span class="sxs-lookup"><span data-stu-id="88de7-112">Value</span></span> |
|----------------------------|---------------------------------------------------------|
| <span data-ttu-id="88de7-113">項目類型</span><span class="sxs-lookup"><span data-stu-id="88de7-113">Element Type</span></span> <br/>   | <span data-ttu-id="88de7-114">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="88de7-114">ParameterDef</span></span><br/>                                 |
| <span data-ttu-id="88de7-115">範圍前置詞</span><span class="sxs-lookup"><span data-stu-id="88de7-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="88de7-116">頁面</span><span class="sxs-lookup"><span data-stu-id="88de7-116">Page</span></span><br/>                                         |
| <span data-ttu-id="88de7-117">備註</span><span class="sxs-lookup"><span data-stu-id="88de7-117">Notes</span></span> <br/>          | <span data-ttu-id="88de7-118">連結至 PageScaling 元素，自訂選項</span><span class="sxs-lookup"><span data-stu-id="88de7-118">Linked to PageScaling element, Custom option</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="88de7-119">結構內容</span><span class="sxs-lookup"><span data-stu-id="88de7-119">Structure Content</span></span>

<span data-ttu-id="88de7-120">此元素的 XML 結構為：</span><span class="sxs-lookup"><span data-stu-id="88de7-120">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageScalingOffsetWidth">
  <psf:Property name="psf:DataType">
    <psf:Value xsi:type="xs:string">xs:integer</psf:Value>
  </psf:Property>
  <psf:Property name="psf:DefaultValue">
    <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MaxValue">
    <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MinValue">
    <psf:Value xsi:type="xs:decimal">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:Multiple">
    <psf:Value xsi:type="xs:integer">1</psf:Value>
  </psf:Property>
  <psf:Property name="psf:Mandatory">
    <psf:Value xsi:type="xs:string">psk:Conditional</psf:Value>
  </psf:Property>
  <psf:Property name="psf:UnitType">
    <psf:Value xsi:type="xs:string">microns</psf:Value>
  </psf:Property>
</psf:ParameterDef>
      
```

## <a name="structure-properties"></a><span data-ttu-id="88de7-121">結構屬性</span><span class="sxs-lookup"><span data-stu-id="88de7-121">Structure Properties</span></span>

<span data-ttu-id="88de7-122">下表概述 XML 結構中所定義之變數的特性。</span><span class="sxs-lookup"><span data-stu-id="88de7-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="88de7-123">屬性</span><span class="sxs-lookup"><span data-stu-id="88de7-123">Property</span></span>                | <span data-ttu-id="88de7-124">xsi:type</span><span class="sxs-lookup"><span data-stu-id="88de7-124">xsi:type</span></span>           | <span data-ttu-id="88de7-125">值</span><span class="sxs-lookup"><span data-stu-id="88de7-125">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="88de7-126">DataType</span><span class="sxs-lookup"><span data-stu-id="88de7-126">DataType</span></span><br/>     | <span data-ttu-id="88de7-127">字串</span><span class="sxs-lookup"><span data-stu-id="88de7-127">string</span></span><br/>  | <span data-ttu-id="88de7-128">xs:integer</span><span class="sxs-lookup"><span data-stu-id="88de7-128">xs:integer</span></span><br/>      |
| <span data-ttu-id="88de7-129">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="88de7-129">DefaultValue</span></span><br/> | <span data-ttu-id="88de7-130">整數</span><span class="sxs-lookup"><span data-stu-id="88de7-130">integer</span></span><br/> | <span data-ttu-id="88de7-131">未定義</span><span class="sxs-lookup"><span data-stu-id="88de7-131">undefined</span></span><br/>       |
| <span data-ttu-id="88de7-132">MaxValue</span><span class="sxs-lookup"><span data-stu-id="88de7-132">MaxValue</span></span><br/>     | <span data-ttu-id="88de7-133">整數</span><span class="sxs-lookup"><span data-stu-id="88de7-133">integer</span></span><br/> | <span data-ttu-id="88de7-134">未定義</span><span class="sxs-lookup"><span data-stu-id="88de7-134">undefined</span></span><br/>       |
| <span data-ttu-id="88de7-135">MinValue</span><span class="sxs-lookup"><span data-stu-id="88de7-135">MinValue</span></span><br/>     | <span data-ttu-id="88de7-136">整數</span><span class="sxs-lookup"><span data-stu-id="88de7-136">integer</span></span><br/> | <span data-ttu-id="88de7-137">未定義</span><span class="sxs-lookup"><span data-stu-id="88de7-137">undefined</span></span><br/>       |
| <span data-ttu-id="88de7-138">強制性</span><span class="sxs-lookup"><span data-stu-id="88de7-138">Mandatory</span></span><br/>    | <span data-ttu-id="88de7-139">字串</span><span class="sxs-lookup"><span data-stu-id="88de7-139">string</span></span><br/>  | <span data-ttu-id="88de7-140">psk：條件式</span><span class="sxs-lookup"><span data-stu-id="88de7-140">psk:Conditional</span></span><br/> |
| <span data-ttu-id="88de7-141">多個</span><span class="sxs-lookup"><span data-stu-id="88de7-141">Multiple</span></span><br/>     | <span data-ttu-id="88de7-142">整數</span><span class="sxs-lookup"><span data-stu-id="88de7-142">integer</span></span><br/> | <span data-ttu-id="88de7-143">1</span><span class="sxs-lookup"><span data-stu-id="88de7-143">1</span></span><br/>               |
| <span data-ttu-id="88de7-144">Unittype.pixel 表示</span><span class="sxs-lookup"><span data-stu-id="88de7-144">UnitType</span></span><br/>     | <span data-ttu-id="88de7-145">字串</span><span class="sxs-lookup"><span data-stu-id="88de7-145">string</span></span><br/>  | <span data-ttu-id="88de7-146">微米</span><span class="sxs-lookup"><span data-stu-id="88de7-146">microns</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="88de7-147">相關主題</span><span class="sxs-lookup"><span data-stu-id="88de7-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="88de7-148">列印架構規格</span><span class="sxs-lookup"><span data-stu-id="88de7-148">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




