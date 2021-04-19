---
description: 本主題並非最新的。 如需最新資訊，請參閱列印架構規格。
ms.assetid: 0de776f3-ae09-49f4-a829-b3c0e2ab5bbc
title: PageScalingScaleWidth
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7918f1a466621377e57190e0b967980fec1a07e
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/05/2021
ms.locfileid: "106990003"
---
# <a name="pagescalingscalewidth"></a><span data-ttu-id="46a4e-104">PageScalingScaleWidth</span><span class="sxs-lookup"><span data-stu-id="46a4e-104">PageScalingScaleWidth</span></span>

<span data-ttu-id="46a4e-105">本主題並非最新的。</span><span class="sxs-lookup"><span data-stu-id="46a4e-105">This topic is not current.</span></span> <span data-ttu-id="46a4e-106">如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。</span><span class="sxs-lookup"><span data-stu-id="46a4e-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="46a4e-107">針對自訂縮放比例指定 ImageableSizeWidth 方向的縮放比例。</span><span class="sxs-lookup"><span data-stu-id="46a4e-107">Specifies the scaling factor in the ImageableSizeWidth direction for custom scaling.</span></span>

-   [<span data-ttu-id="46a4e-108">項目資訊</span><span class="sxs-lookup"><span data-stu-id="46a4e-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="46a4e-109">結構內容</span><span class="sxs-lookup"><span data-stu-id="46a4e-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="46a4e-110">項目資訊</span><span class="sxs-lookup"><span data-stu-id="46a4e-110">Element Information</span></span>



| <span data-ttu-id="46a4e-111">Name</span><span class="sxs-lookup"><span data-stu-id="46a4e-111">Name</span></span>                       |                                                         |
|----------------------------|---------------------------------------------------------|
| <span data-ttu-id="46a4e-112">項目類型</span><span class="sxs-lookup"><span data-stu-id="46a4e-112">Element Type</span></span> <br/>   | <span data-ttu-id="46a4e-113">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="46a4e-113">ParameterDef</span></span><br/>                                 |
| <span data-ttu-id="46a4e-114">範圍前置詞</span><span class="sxs-lookup"><span data-stu-id="46a4e-114">Scoping Prefix</span></span> <br/> | <span data-ttu-id="46a4e-115">頁面</span><span class="sxs-lookup"><span data-stu-id="46a4e-115">Page</span></span><br/>                                         |
| <span data-ttu-id="46a4e-116">備註</span><span class="sxs-lookup"><span data-stu-id="46a4e-116">Notes</span></span> <br/>          | <span data-ttu-id="46a4e-117">連結至 PageScaling 元素，自訂選項</span><span class="sxs-lookup"><span data-stu-id="46a4e-117">Linked to PageScaling element, Custom option</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="46a4e-118">結構內容</span><span class="sxs-lookup"><span data-stu-id="46a4e-118">Structure Content</span></span>

<span data-ttu-id="46a4e-119">此元素的 XML 結構為：</span><span class="sxs-lookup"><span data-stu-id="46a4e-119">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageScalingScaleWidth">
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
    <psf:Value xsi:type="xs:integer">1</psf:Value>
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

## <a name="structure-properties"></a><span data-ttu-id="46a4e-120">結構屬性</span><span class="sxs-lookup"><span data-stu-id="46a4e-120">Structure Properties</span></span>

<span data-ttu-id="46a4e-121">下表概述 XML 結構中所定義之變數的特性。</span><span class="sxs-lookup"><span data-stu-id="46a4e-121">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="46a4e-122">屬性</span><span class="sxs-lookup"><span data-stu-id="46a4e-122">Property</span></span>                | <span data-ttu-id="46a4e-123">xsi:type</span><span class="sxs-lookup"><span data-stu-id="46a4e-123">xsi:type</span></span>           | <span data-ttu-id="46a4e-124">值</span><span class="sxs-lookup"><span data-stu-id="46a4e-124">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="46a4e-125">DataType</span><span class="sxs-lookup"><span data-stu-id="46a4e-125">DataType</span></span><br/>     | <span data-ttu-id="46a4e-126">String</span><span class="sxs-lookup"><span data-stu-id="46a4e-126">String</span></span><br/>  | <span data-ttu-id="46a4e-127">xs:integer</span><span class="sxs-lookup"><span data-stu-id="46a4e-127">xs:integer</span></span><br/>      |
| <span data-ttu-id="46a4e-128">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="46a4e-128">DefaultValue</span></span><br/> | <span data-ttu-id="46a4e-129">整數</span><span class="sxs-lookup"><span data-stu-id="46a4e-129">Integer</span></span><br/> | <span data-ttu-id="46a4e-130">未定義</span><span class="sxs-lookup"><span data-stu-id="46a4e-130">undefined</span></span><br/>       |
| <span data-ttu-id="46a4e-131">MaxValue</span><span class="sxs-lookup"><span data-stu-id="46a4e-131">MaxValue</span></span><br/>     | <span data-ttu-id="46a4e-132">整數</span><span class="sxs-lookup"><span data-stu-id="46a4e-132">Integer</span></span><br/> | <span data-ttu-id="46a4e-133">未定義</span><span class="sxs-lookup"><span data-stu-id="46a4e-133">undefined</span></span><br/>       |
| <span data-ttu-id="46a4e-134">MinValue</span><span class="sxs-lookup"><span data-stu-id="46a4e-134">MinValue</span></span><br/>     | <span data-ttu-id="46a4e-135">整數</span><span class="sxs-lookup"><span data-stu-id="46a4e-135">Integer</span></span><br/> | <span data-ttu-id="46a4e-136">1</span><span class="sxs-lookup"><span data-stu-id="46a4e-136">1</span></span><br/>               |
| <span data-ttu-id="46a4e-137">強制性</span><span class="sxs-lookup"><span data-stu-id="46a4e-137">Mandatory</span></span><br/>    | <span data-ttu-id="46a4e-138">String</span><span class="sxs-lookup"><span data-stu-id="46a4e-138">String</span></span><br/>  | <span data-ttu-id="46a4e-139">psk：條件式</span><span class="sxs-lookup"><span data-stu-id="46a4e-139">psk:Conditional</span></span><br/> |
| <span data-ttu-id="46a4e-140">多個</span><span class="sxs-lookup"><span data-stu-id="46a4e-140">Multiple</span></span><br/>     | <span data-ttu-id="46a4e-141">整數</span><span class="sxs-lookup"><span data-stu-id="46a4e-141">Integer</span></span><br/> | <span data-ttu-id="46a4e-142">1</span><span class="sxs-lookup"><span data-stu-id="46a4e-142">1</span></span><br/>               |
| <span data-ttu-id="46a4e-143">Unittype.pixel 表示</span><span class="sxs-lookup"><span data-stu-id="46a4e-143">UnitType</span></span><br/>     | <span data-ttu-id="46a4e-144">String</span><span class="sxs-lookup"><span data-stu-id="46a4e-144">String</span></span><br/>  | <span data-ttu-id="46a4e-145">微米</span><span class="sxs-lookup"><span data-stu-id="46a4e-145">microns</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="46a4e-146">相關主題</span><span class="sxs-lookup"><span data-stu-id="46a4e-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="46a4e-147">列印架構規格</span><span class="sxs-lookup"><span data-stu-id="46a4e-147">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




