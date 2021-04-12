---
description: 本主題並非最新的。 如需最新資訊，請參閱列印架構規格。
ms.assetid: 157bb79c-68d2-4121-8a85-cd2f48095541
title: PageWatermarkTextAngle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 916e409040f0c7163f1168d48581270f077aaa3a
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/05/2021
ms.locfileid: "104195820"
---
# <a name="pagewatermarktextangle"></a><span data-ttu-id="01712-104">PageWatermarkTextAngle</span><span class="sxs-lookup"><span data-stu-id="01712-104">PageWatermarkTextAngle</span></span>

<span data-ttu-id="01712-105">本主題並非最新的。</span><span class="sxs-lookup"><span data-stu-id="01712-105">This topic is not current.</span></span> <span data-ttu-id="01712-106">如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。</span><span class="sxs-lookup"><span data-stu-id="01712-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="01712-107">指定浮水印文字相對於 PageImageableSizeWidth 方向的角度。</span><span class="sxs-lookup"><span data-stu-id="01712-107">Specifies the angle of the watermark text relative to the PageImageableSizeWidth direction.</span></span> <span data-ttu-id="01712-108">角度是以逆時針方向來測量。</span><span class="sxs-lookup"><span data-stu-id="01712-108">The angle is measured in the counter-clockwise direction.</span></span>

-   [<span data-ttu-id="01712-109">項目資訊</span><span class="sxs-lookup"><span data-stu-id="01712-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="01712-110">結構內容</span><span class="sxs-lookup"><span data-stu-id="01712-110">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="01712-111">項目資訊</span><span class="sxs-lookup"><span data-stu-id="01712-111">Element Information</span></span>



| <span data-ttu-id="01712-112">Name</span><span class="sxs-lookup"><span data-stu-id="01712-112">Name</span></span>                       |                                            |
|----------------------------|--------------------------------------------|
| <span data-ttu-id="01712-113">項目類型</span><span class="sxs-lookup"><span data-stu-id="01712-113">Element Type</span></span> <br/>   | <span data-ttu-id="01712-114">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="01712-114">ParameterDef</span></span><br/>                    |
| <span data-ttu-id="01712-115">範圍前置詞</span><span class="sxs-lookup"><span data-stu-id="01712-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="01712-116">頁面</span><span class="sxs-lookup"><span data-stu-id="01712-116">Page</span></span><br/>                            |
| <span data-ttu-id="01712-117">備註</span><span class="sxs-lookup"><span data-stu-id="01712-117">Notes</span></span> <br/>          | <span data-ttu-id="01712-118">連結至 PageWatermark 元素</span><span class="sxs-lookup"><span data-stu-id="01712-118">Linked to PageWatermark element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="01712-119">結構內容</span><span class="sxs-lookup"><span data-stu-id="01712-119">Structure Content</span></span>

<span data-ttu-id="01712-120">此元素的 XML 結構如下所示：</span><span class="sxs-lookup"><span data-stu-id="01712-120">The XML structure of this element is as follows:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageWatermarkTextAngle">
  <psf:Property name="psf:DataType">
    <psf:Value xsi:type="xs:string">xs:integer</psf:Value>
  </psf:Property>
  <psf:Property name="psf:DefaultValue">
    <psf:Value xsi:type="xs:integer">0</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MaxValue">
    <psf:Value xsi:type="xs:integer">359</psf:Value>
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
    <psf:Value xsi:type="xs:string">degrees</psf:Value>
  </psf:Property>
</psf:ParameterDef>
      
```

## <a name="structure-properties"></a><span data-ttu-id="01712-121">結構屬性</span><span class="sxs-lookup"><span data-stu-id="01712-121">Structure Properties</span></span>

<span data-ttu-id="01712-122">下表概述 XML 結構中所定義之變數的特性。</span><span class="sxs-lookup"><span data-stu-id="01712-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="01712-123">屬性</span><span class="sxs-lookup"><span data-stu-id="01712-123">Property</span></span>                | <span data-ttu-id="01712-124">xsi:type</span><span class="sxs-lookup"><span data-stu-id="01712-124">xsi:type</span></span>           | <span data-ttu-id="01712-125">值</span><span class="sxs-lookup"><span data-stu-id="01712-125">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="01712-126">DataType</span><span class="sxs-lookup"><span data-stu-id="01712-126">DataType</span></span><br/>     | <span data-ttu-id="01712-127">字串</span><span class="sxs-lookup"><span data-stu-id="01712-127">string</span></span><br/>  | <span data-ttu-id="01712-128">xs:integer</span><span class="sxs-lookup"><span data-stu-id="01712-128">xs:integer</span></span><br/>      |
| <span data-ttu-id="01712-129">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="01712-129">DefaultValue</span></span><br/> | <span data-ttu-id="01712-130">整數</span><span class="sxs-lookup"><span data-stu-id="01712-130">integer</span></span><br/> | <span data-ttu-id="01712-131">0</span><span class="sxs-lookup"><span data-stu-id="01712-131">0</span></span><br/>               |
| <span data-ttu-id="01712-132">MaxValue</span><span class="sxs-lookup"><span data-stu-id="01712-132">MaxValue</span></span><br/>     | <span data-ttu-id="01712-133">整數</span><span class="sxs-lookup"><span data-stu-id="01712-133">integer</span></span><br/> | <span data-ttu-id="01712-134">359</span><span class="sxs-lookup"><span data-stu-id="01712-134">359</span></span><br/>             |
| <span data-ttu-id="01712-135">MinValue</span><span class="sxs-lookup"><span data-stu-id="01712-135">MinValue</span></span><br/>     | <span data-ttu-id="01712-136">整數</span><span class="sxs-lookup"><span data-stu-id="01712-136">integer</span></span><br/> | <span data-ttu-id="01712-137">0</span><span class="sxs-lookup"><span data-stu-id="01712-137">0</span></span><br/>               |
| <span data-ttu-id="01712-138">多個</span><span class="sxs-lookup"><span data-stu-id="01712-138">Multiple</span></span><br/>     | <span data-ttu-id="01712-139">整數</span><span class="sxs-lookup"><span data-stu-id="01712-139">integer</span></span><br/> | <span data-ttu-id="01712-140">1</span><span class="sxs-lookup"><span data-stu-id="01712-140">1</span></span><br/>               |
| <span data-ttu-id="01712-141">強制性</span><span class="sxs-lookup"><span data-stu-id="01712-141">Mandatory</span></span><br/>    | <span data-ttu-id="01712-142">字串</span><span class="sxs-lookup"><span data-stu-id="01712-142">string</span></span><br/>  | <span data-ttu-id="01712-143">psk：條件式</span><span class="sxs-lookup"><span data-stu-id="01712-143">psk:Conditional</span></span><br/> |
| <span data-ttu-id="01712-144">Unittype.pixel 表示</span><span class="sxs-lookup"><span data-stu-id="01712-144">UnitType</span></span><br/>     | <span data-ttu-id="01712-145">字串</span><span class="sxs-lookup"><span data-stu-id="01712-145">string</span></span><br/>  | <span data-ttu-id="01712-146">度</span><span class="sxs-lookup"><span data-stu-id="01712-146">degrees</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="01712-147">相關主題</span><span class="sxs-lookup"><span data-stu-id="01712-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="01712-148">列印架構規格</span><span class="sxs-lookup"><span data-stu-id="01712-148">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




