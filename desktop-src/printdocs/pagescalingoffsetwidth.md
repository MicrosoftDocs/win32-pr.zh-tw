---
description: 本主題並非最新的。 如需最新資訊，請參閱列印架構規格。
ms.assetid: e82394d1-f765-4679-b1de-ea17825d6478
title: PageScalingOffsetWidth
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25a9cd5532bf4d109b94c579ef2ad21d242aca9a
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/05/2021
ms.locfileid: "106986685"
---
# <a name="pagescalingoffsetwidth"></a><span data-ttu-id="384e5-104">PageScalingOffsetWidth</span><span class="sxs-lookup"><span data-stu-id="384e5-104">PageScalingOffsetWidth</span></span>

<span data-ttu-id="384e5-105">本主題並非最新的。</span><span class="sxs-lookup"><span data-stu-id="384e5-105">This topic is not current.</span></span> <span data-ttu-id="384e5-106">如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。</span><span class="sxs-lookup"><span data-stu-id="384e5-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="384e5-107">針對自訂縮放比例指定 ImageableSizeWidth 方向的縮放位移。</span><span class="sxs-lookup"><span data-stu-id="384e5-107">Specifies the scaling offset in the ImageableSizeWidth direction for custom scaling.</span></span>

-   [<span data-ttu-id="384e5-108">項目資訊</span><span class="sxs-lookup"><span data-stu-id="384e5-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="384e5-109">結構內容</span><span class="sxs-lookup"><span data-stu-id="384e5-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="384e5-110">項目資訊</span><span class="sxs-lookup"><span data-stu-id="384e5-110">Element Information</span></span>



| <span data-ttu-id="384e5-111">Name</span><span class="sxs-lookup"><span data-stu-id="384e5-111">Name</span></span>                       |                                                         |
|----------------------------|---------------------------------------------------------|
| <span data-ttu-id="384e5-112">項目類型</span><span class="sxs-lookup"><span data-stu-id="384e5-112">Element Type</span></span> <br/>   | <span data-ttu-id="384e5-113">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="384e5-113">ParameterDef</span></span><br/>                                 |
| <span data-ttu-id="384e5-114">範圍前置詞</span><span class="sxs-lookup"><span data-stu-id="384e5-114">Scoping Prefix</span></span> <br/> | <span data-ttu-id="384e5-115">頁面</span><span class="sxs-lookup"><span data-stu-id="384e5-115">Page</span></span><br/>                                         |
| <span data-ttu-id="384e5-116">備註</span><span class="sxs-lookup"><span data-stu-id="384e5-116">Notes</span></span> <br/>          | <span data-ttu-id="384e5-117">連結至 PageScaling 元素，自訂選項</span><span class="sxs-lookup"><span data-stu-id="384e5-117">Linked to PageScaling element, Custom option</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="384e5-118">結構內容</span><span class="sxs-lookup"><span data-stu-id="384e5-118">Structure Content</span></span>

<span data-ttu-id="384e5-119">此元素的 XML 結構為：</span><span class="sxs-lookup"><span data-stu-id="384e5-119">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="384e5-120">結構屬性</span><span class="sxs-lookup"><span data-stu-id="384e5-120">Structure Properties</span></span>

<span data-ttu-id="384e5-121">下表概述 XML 結構中所定義之變數的特性。</span><span class="sxs-lookup"><span data-stu-id="384e5-121">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="384e5-122">屬性</span><span class="sxs-lookup"><span data-stu-id="384e5-122">Property</span></span>                | <span data-ttu-id="384e5-123">xsi:type</span><span class="sxs-lookup"><span data-stu-id="384e5-123">xsi:type</span></span>           | <span data-ttu-id="384e5-124">值</span><span class="sxs-lookup"><span data-stu-id="384e5-124">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="384e5-125">DataType</span><span class="sxs-lookup"><span data-stu-id="384e5-125">DataType</span></span><br/>     | <span data-ttu-id="384e5-126">字串</span><span class="sxs-lookup"><span data-stu-id="384e5-126">string</span></span><br/>  | <span data-ttu-id="384e5-127">xs:integer</span><span class="sxs-lookup"><span data-stu-id="384e5-127">xs:integer</span></span><br/>      |
| <span data-ttu-id="384e5-128">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="384e5-128">DefaultValue</span></span><br/> | <span data-ttu-id="384e5-129">整數</span><span class="sxs-lookup"><span data-stu-id="384e5-129">integer</span></span><br/> | <span data-ttu-id="384e5-130">未定義</span><span class="sxs-lookup"><span data-stu-id="384e5-130">undefined</span></span><br/>       |
| <span data-ttu-id="384e5-131">MaxValue</span><span class="sxs-lookup"><span data-stu-id="384e5-131">MaxValue</span></span><br/>     | <span data-ttu-id="384e5-132">整數</span><span class="sxs-lookup"><span data-stu-id="384e5-132">integer</span></span><br/> | <span data-ttu-id="384e5-133">未定義</span><span class="sxs-lookup"><span data-stu-id="384e5-133">undefined</span></span><br/>       |
| <span data-ttu-id="384e5-134">MinValue</span><span class="sxs-lookup"><span data-stu-id="384e5-134">MinValue</span></span><br/>     | <span data-ttu-id="384e5-135">整數</span><span class="sxs-lookup"><span data-stu-id="384e5-135">integer</span></span><br/> | <span data-ttu-id="384e5-136">未定義</span><span class="sxs-lookup"><span data-stu-id="384e5-136">undefined</span></span><br/>       |
| <span data-ttu-id="384e5-137">強制性</span><span class="sxs-lookup"><span data-stu-id="384e5-137">Mandatory</span></span><br/>    | <span data-ttu-id="384e5-138">字串</span><span class="sxs-lookup"><span data-stu-id="384e5-138">string</span></span><br/>  | <span data-ttu-id="384e5-139">psk：條件式</span><span class="sxs-lookup"><span data-stu-id="384e5-139">psk:Conditional</span></span><br/> |
| <span data-ttu-id="384e5-140">多個</span><span class="sxs-lookup"><span data-stu-id="384e5-140">Multiple</span></span><br/>     | <span data-ttu-id="384e5-141">整數</span><span class="sxs-lookup"><span data-stu-id="384e5-141">integer</span></span><br/> | <span data-ttu-id="384e5-142">1</span><span class="sxs-lookup"><span data-stu-id="384e5-142">1</span></span><br/>               |
| <span data-ttu-id="384e5-143">Unittype.pixel 表示</span><span class="sxs-lookup"><span data-stu-id="384e5-143">UnitType</span></span><br/>     | <span data-ttu-id="384e5-144">字串</span><span class="sxs-lookup"><span data-stu-id="384e5-144">string</span></span><br/>  | <span data-ttu-id="384e5-145">微米</span><span class="sxs-lookup"><span data-stu-id="384e5-145">microns</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="384e5-146">相關主題</span><span class="sxs-lookup"><span data-stu-id="384e5-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="384e5-147">列印架構規格</span><span class="sxs-lookup"><span data-stu-id="384e5-147">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




