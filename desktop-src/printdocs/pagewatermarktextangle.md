---
description: 本主題並非最新的。 如需最新資訊，請參閱列印架構規格。
ms.assetid: 157bb79c-68d2-4121-8a85-cd2f48095541
title: PageWatermarkTextAngle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86c13d759232670c6957a91de12f9c35cf48aeb4
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/26/2021
ms.locfileid: "107995545"
---
# <a name="pagewatermarktextangle"></a><span data-ttu-id="6ebd1-104">PageWatermarkTextAngle</span><span class="sxs-lookup"><span data-stu-id="6ebd1-104">PageWatermarkTextAngle</span></span>

<span data-ttu-id="6ebd1-105">本主題並非最新的。</span><span class="sxs-lookup"><span data-stu-id="6ebd1-105">This topic is not current.</span></span> <span data-ttu-id="6ebd1-106">如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。</span><span class="sxs-lookup"><span data-stu-id="6ebd1-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="6ebd1-107">指定浮水印文字相對於 PageImageableSizeWidth 方向的角度。</span><span class="sxs-lookup"><span data-stu-id="6ebd1-107">Specifies the angle of the watermark text relative to the PageImageableSizeWidth direction.</span></span> <span data-ttu-id="6ebd1-108">角度是以逆時針方向來測量。</span><span class="sxs-lookup"><span data-stu-id="6ebd1-108">The angle is measured in the counter-clockwise direction.</span></span>

-   [<span data-ttu-id="6ebd1-109">項目資訊</span><span class="sxs-lookup"><span data-stu-id="6ebd1-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="6ebd1-110">結構內容</span><span class="sxs-lookup"><span data-stu-id="6ebd1-110">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="6ebd1-111">項目資訊</span><span class="sxs-lookup"><span data-stu-id="6ebd1-111">Element Information</span></span>



| <span data-ttu-id="6ebd1-112">Name</span><span class="sxs-lookup"><span data-stu-id="6ebd1-112">Name</span></span> | <span data-ttu-id="6ebd1-113">值</span><span class="sxs-lookup"><span data-stu-id="6ebd1-113">Value</span></span> |
|----------------------------|--------------------------------------------|
| <span data-ttu-id="6ebd1-114">項目類型</span><span class="sxs-lookup"><span data-stu-id="6ebd1-114">Element Type</span></span> <br/>   | <span data-ttu-id="6ebd1-115">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="6ebd1-115">ParameterDef</span></span><br/>                    |
| <span data-ttu-id="6ebd1-116">範圍前置詞</span><span class="sxs-lookup"><span data-stu-id="6ebd1-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="6ebd1-117">頁面</span><span class="sxs-lookup"><span data-stu-id="6ebd1-117">Page</span></span><br/>                            |
| <span data-ttu-id="6ebd1-118">備註</span><span class="sxs-lookup"><span data-stu-id="6ebd1-118">Notes</span></span> <br/>          | <span data-ttu-id="6ebd1-119">連結至 PageWatermark 元素</span><span class="sxs-lookup"><span data-stu-id="6ebd1-119">Linked to PageWatermark element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="6ebd1-120">結構內容</span><span class="sxs-lookup"><span data-stu-id="6ebd1-120">Structure Content</span></span>

<span data-ttu-id="6ebd1-121">此元素的 XML 結構如下所示：</span><span class="sxs-lookup"><span data-stu-id="6ebd1-121">The XML structure of this element is as follows:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="6ebd1-122">結構屬性</span><span class="sxs-lookup"><span data-stu-id="6ebd1-122">Structure Properties</span></span>

<span data-ttu-id="6ebd1-123">下表概述 XML 結構中所定義之變數的特性。</span><span class="sxs-lookup"><span data-stu-id="6ebd1-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="6ebd1-124">屬性</span><span class="sxs-lookup"><span data-stu-id="6ebd1-124">Property</span></span>                | <span data-ttu-id="6ebd1-125">xsi:type</span><span class="sxs-lookup"><span data-stu-id="6ebd1-125">xsi:type</span></span>           | <span data-ttu-id="6ebd1-126">值</span><span class="sxs-lookup"><span data-stu-id="6ebd1-126">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="6ebd1-127">DataType</span><span class="sxs-lookup"><span data-stu-id="6ebd1-127">DataType</span></span><br/>     | <span data-ttu-id="6ebd1-128">字串</span><span class="sxs-lookup"><span data-stu-id="6ebd1-128">string</span></span><br/>  | <span data-ttu-id="6ebd1-129">xs:integer</span><span class="sxs-lookup"><span data-stu-id="6ebd1-129">xs:integer</span></span><br/>      |
| <span data-ttu-id="6ebd1-130">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="6ebd1-130">DefaultValue</span></span><br/> | <span data-ttu-id="6ebd1-131">整數</span><span class="sxs-lookup"><span data-stu-id="6ebd1-131">integer</span></span><br/> | <span data-ttu-id="6ebd1-132">0</span><span class="sxs-lookup"><span data-stu-id="6ebd1-132">0</span></span><br/>               |
| <span data-ttu-id="6ebd1-133">MaxValue</span><span class="sxs-lookup"><span data-stu-id="6ebd1-133">MaxValue</span></span><br/>     | <span data-ttu-id="6ebd1-134">整數</span><span class="sxs-lookup"><span data-stu-id="6ebd1-134">integer</span></span><br/> | <span data-ttu-id="6ebd1-135">359</span><span class="sxs-lookup"><span data-stu-id="6ebd1-135">359</span></span><br/>             |
| <span data-ttu-id="6ebd1-136">MinValue</span><span class="sxs-lookup"><span data-stu-id="6ebd1-136">MinValue</span></span><br/>     | <span data-ttu-id="6ebd1-137">整數</span><span class="sxs-lookup"><span data-stu-id="6ebd1-137">integer</span></span><br/> | <span data-ttu-id="6ebd1-138">0</span><span class="sxs-lookup"><span data-stu-id="6ebd1-138">0</span></span><br/>               |
| <span data-ttu-id="6ebd1-139">多個</span><span class="sxs-lookup"><span data-stu-id="6ebd1-139">Multiple</span></span><br/>     | <span data-ttu-id="6ebd1-140">整數</span><span class="sxs-lookup"><span data-stu-id="6ebd1-140">integer</span></span><br/> | <span data-ttu-id="6ebd1-141">1</span><span class="sxs-lookup"><span data-stu-id="6ebd1-141">1</span></span><br/>               |
| <span data-ttu-id="6ebd1-142">強制性</span><span class="sxs-lookup"><span data-stu-id="6ebd1-142">Mandatory</span></span><br/>    | <span data-ttu-id="6ebd1-143">字串</span><span class="sxs-lookup"><span data-stu-id="6ebd1-143">string</span></span><br/>  | <span data-ttu-id="6ebd1-144">psk：條件式</span><span class="sxs-lookup"><span data-stu-id="6ebd1-144">psk:Conditional</span></span><br/> |
| <span data-ttu-id="6ebd1-145">Unittype.pixel 表示</span><span class="sxs-lookup"><span data-stu-id="6ebd1-145">UnitType</span></span><br/>     | <span data-ttu-id="6ebd1-146">字串</span><span class="sxs-lookup"><span data-stu-id="6ebd1-146">string</span></span><br/>  | <span data-ttu-id="6ebd1-147">度</span><span class="sxs-lookup"><span data-stu-id="6ebd1-147">degrees</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="6ebd1-148">相關主題</span><span class="sxs-lookup"><span data-stu-id="6ebd1-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6ebd1-149">列印架構規格</span><span class="sxs-lookup"><span data-stu-id="6ebd1-149">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




