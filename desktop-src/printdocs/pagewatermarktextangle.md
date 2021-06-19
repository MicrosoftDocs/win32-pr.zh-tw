---
description: 取得 PageWatermarkTextAngle 參數的詳細資訊。 本主題並非最新的。 如需最新資訊，請參閱列印架構規格。
ms.assetid: 157bb79c-68d2-4121-8a85-cd2f48095541
title: PageWatermarkTextAngle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1dce37512314e1eaac0cbbe3b5b4b817cb2ee455
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/19/2021
ms.locfileid: "112395973"
---
# <a name="pagewatermarktextangle"></a><span data-ttu-id="ecc5f-105">PageWatermarkTextAngle</span><span class="sxs-lookup"><span data-stu-id="ecc5f-105">PageWatermarkTextAngle</span></span>

<span data-ttu-id="ecc5f-106">本主題並非最新的。</span><span class="sxs-lookup"><span data-stu-id="ecc5f-106">This topic is not current.</span></span> <span data-ttu-id="ecc5f-107">如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。</span><span class="sxs-lookup"><span data-stu-id="ecc5f-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="ecc5f-108">指定浮水印文字相對於 PageImageableSizeWidth 方向的角度。</span><span class="sxs-lookup"><span data-stu-id="ecc5f-108">Specifies the angle of the watermark text relative to the PageImageableSizeWidth direction.</span></span> <span data-ttu-id="ecc5f-109">角度是以逆時針方向來測量。</span><span class="sxs-lookup"><span data-stu-id="ecc5f-109">The angle is measured in the counter-clockwise direction.</span></span>

-   [<span data-ttu-id="ecc5f-110">項目資訊</span><span class="sxs-lookup"><span data-stu-id="ecc5f-110">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="ecc5f-111">結構內容</span><span class="sxs-lookup"><span data-stu-id="ecc5f-111">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="ecc5f-112">項目資訊</span><span class="sxs-lookup"><span data-stu-id="ecc5f-112">Element Information</span></span>



| <span data-ttu-id="ecc5f-113">Name</span><span class="sxs-lookup"><span data-stu-id="ecc5f-113">Name</span></span> | <span data-ttu-id="ecc5f-114">值</span><span class="sxs-lookup"><span data-stu-id="ecc5f-114">Value</span></span> |
|----------------------------|--------------------------------------------|
| <span data-ttu-id="ecc5f-115">項目類型</span><span class="sxs-lookup"><span data-stu-id="ecc5f-115">Element Type</span></span> <br/>   | <span data-ttu-id="ecc5f-116">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="ecc5f-116">ParameterDef</span></span><br/>                    |
| <span data-ttu-id="ecc5f-117">範圍前置詞</span><span class="sxs-lookup"><span data-stu-id="ecc5f-117">Scoping Prefix</span></span> <br/> | <span data-ttu-id="ecc5f-118">頁面</span><span class="sxs-lookup"><span data-stu-id="ecc5f-118">Page</span></span><br/>                            |
| <span data-ttu-id="ecc5f-119">備註</span><span class="sxs-lookup"><span data-stu-id="ecc5f-119">Notes</span></span> <br/>          | <span data-ttu-id="ecc5f-120">連結至 PageWatermark 元素</span><span class="sxs-lookup"><span data-stu-id="ecc5f-120">Linked to PageWatermark element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="ecc5f-121">結構內容</span><span class="sxs-lookup"><span data-stu-id="ecc5f-121">Structure Content</span></span>

<span data-ttu-id="ecc5f-122">此元素的 XML 結構如下所示：</span><span class="sxs-lookup"><span data-stu-id="ecc5f-122">The XML structure of this element is as follows:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="ecc5f-123">結構屬性</span><span class="sxs-lookup"><span data-stu-id="ecc5f-123">Structure Properties</span></span>

<span data-ttu-id="ecc5f-124">下表概述 XML 結構中所定義之變數的特性。</span><span class="sxs-lookup"><span data-stu-id="ecc5f-124">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="ecc5f-125">屬性</span><span class="sxs-lookup"><span data-stu-id="ecc5f-125">Property</span></span>                | <span data-ttu-id="ecc5f-126">xsi:type</span><span class="sxs-lookup"><span data-stu-id="ecc5f-126">xsi:type</span></span>           | <span data-ttu-id="ecc5f-127">值</span><span class="sxs-lookup"><span data-stu-id="ecc5f-127">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="ecc5f-128">DataType</span><span class="sxs-lookup"><span data-stu-id="ecc5f-128">DataType</span></span><br/>     | <span data-ttu-id="ecc5f-129">字串</span><span class="sxs-lookup"><span data-stu-id="ecc5f-129">string</span></span><br/>  | <span data-ttu-id="ecc5f-130">xs:integer</span><span class="sxs-lookup"><span data-stu-id="ecc5f-130">xs:integer</span></span><br/>      |
| <span data-ttu-id="ecc5f-131">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="ecc5f-131">DefaultValue</span></span><br/> | <span data-ttu-id="ecc5f-132">整數</span><span class="sxs-lookup"><span data-stu-id="ecc5f-132">integer</span></span><br/> | <span data-ttu-id="ecc5f-133">0</span><span class="sxs-lookup"><span data-stu-id="ecc5f-133">0</span></span><br/>               |
| <span data-ttu-id="ecc5f-134">MaxValue</span><span class="sxs-lookup"><span data-stu-id="ecc5f-134">MaxValue</span></span><br/>     | <span data-ttu-id="ecc5f-135">整數</span><span class="sxs-lookup"><span data-stu-id="ecc5f-135">integer</span></span><br/> | <span data-ttu-id="ecc5f-136">359</span><span class="sxs-lookup"><span data-stu-id="ecc5f-136">359</span></span><br/>             |
| <span data-ttu-id="ecc5f-137">MinValue</span><span class="sxs-lookup"><span data-stu-id="ecc5f-137">MinValue</span></span><br/>     | <span data-ttu-id="ecc5f-138">整數</span><span class="sxs-lookup"><span data-stu-id="ecc5f-138">integer</span></span><br/> | <span data-ttu-id="ecc5f-139">0</span><span class="sxs-lookup"><span data-stu-id="ecc5f-139">0</span></span><br/>               |
| <span data-ttu-id="ecc5f-140">多個</span><span class="sxs-lookup"><span data-stu-id="ecc5f-140">Multiple</span></span><br/>     | <span data-ttu-id="ecc5f-141">整數</span><span class="sxs-lookup"><span data-stu-id="ecc5f-141">integer</span></span><br/> | <span data-ttu-id="ecc5f-142">1</span><span class="sxs-lookup"><span data-stu-id="ecc5f-142">1</span></span><br/>               |
| <span data-ttu-id="ecc5f-143">強制性</span><span class="sxs-lookup"><span data-stu-id="ecc5f-143">Mandatory</span></span><br/>    | <span data-ttu-id="ecc5f-144">string</span><span class="sxs-lookup"><span data-stu-id="ecc5f-144">string</span></span><br/>  | <span data-ttu-id="ecc5f-145">psk：條件式</span><span class="sxs-lookup"><span data-stu-id="ecc5f-145">psk:Conditional</span></span><br/> |
| <span data-ttu-id="ecc5f-146">Unittype.pixel 表示</span><span class="sxs-lookup"><span data-stu-id="ecc5f-146">UnitType</span></span><br/>     | <span data-ttu-id="ecc5f-147">string</span><span class="sxs-lookup"><span data-stu-id="ecc5f-147">string</span></span><br/>  | <span data-ttu-id="ecc5f-148">度</span><span class="sxs-lookup"><span data-stu-id="ecc5f-148">degrees</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="ecc5f-149">相關主題</span><span class="sxs-lookup"><span data-stu-id="ecc5f-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ecc5f-150">列印架構規格</span><span class="sxs-lookup"><span data-stu-id="ecc5f-150">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




