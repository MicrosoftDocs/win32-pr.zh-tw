---
description: 本主題並非最新的。 如需最新資訊，請參閱列印架構規格。
ms.assetid: e1bea06b-11b9-4652-915a-deb563ad59f8
title: PageWatermarkOriginWidth
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6780dd5cc3b90a4f15cb6ada66ab82c4269acd82
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/05/2021
ms.locfileid: "103853532"
---
# <a name="pagewatermarkoriginwidth"></a><span data-ttu-id="370e2-104">PageWatermarkOriginWidth</span><span class="sxs-lookup"><span data-stu-id="370e2-104">PageWatermarkOriginWidth</span></span>

<span data-ttu-id="370e2-105">本主題並非最新的。</span><span class="sxs-lookup"><span data-stu-id="370e2-105">This topic is not current.</span></span> <span data-ttu-id="370e2-106">如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。</span><span class="sxs-lookup"><span data-stu-id="370e2-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="370e2-107">指定相對於 PageImageableSize 原點的浮水印原點。</span><span class="sxs-lookup"><span data-stu-id="370e2-107">Specifies the origin of a watermark relative to the origin of the PageImageableSize.</span></span>

-   [<span data-ttu-id="370e2-108">項目資訊</span><span class="sxs-lookup"><span data-stu-id="370e2-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="370e2-109">結構內容</span><span class="sxs-lookup"><span data-stu-id="370e2-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="370e2-110">項目資訊</span><span class="sxs-lookup"><span data-stu-id="370e2-110">Element Information</span></span>



| <span data-ttu-id="370e2-111">Name</span><span class="sxs-lookup"><span data-stu-id="370e2-111">Name</span></span>                       |                                            |
|----------------------------|--------------------------------------------|
| <span data-ttu-id="370e2-112">項目類型</span><span class="sxs-lookup"><span data-stu-id="370e2-112">Element Type</span></span> <br/>   | <span data-ttu-id="370e2-113">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="370e2-113">ParameterDef</span></span><br/>                    |
| <span data-ttu-id="370e2-114">範圍前置詞</span><span class="sxs-lookup"><span data-stu-id="370e2-114">Scoping Prefix</span></span> <br/> | <span data-ttu-id="370e2-115">頁面</span><span class="sxs-lookup"><span data-stu-id="370e2-115">Page</span></span><br/>                            |
| <span data-ttu-id="370e2-116">備註</span><span class="sxs-lookup"><span data-stu-id="370e2-116">Notes</span></span> <br/>          | <span data-ttu-id="370e2-117">連結至 PageWatermark 元素</span><span class="sxs-lookup"><span data-stu-id="370e2-117">Linked to PageWatermark element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="370e2-118">結構內容</span><span class="sxs-lookup"><span data-stu-id="370e2-118">Structure Content</span></span>

<span data-ttu-id="370e2-119">此元素的 XML 結構為：</span><span class="sxs-lookup"><span data-stu-id="370e2-119">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageWatermarkOriginWidth">
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
    <psf:Value xsi:type="xs:integer">0</psf:Value>
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

## <a name="structure-properties"></a><span data-ttu-id="370e2-120">結構屬性</span><span class="sxs-lookup"><span data-stu-id="370e2-120">Structure Properties</span></span>

<span data-ttu-id="370e2-121">下表概述 XML 結構中所定義之變數的特性。</span><span class="sxs-lookup"><span data-stu-id="370e2-121">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="370e2-122">屬性</span><span class="sxs-lookup"><span data-stu-id="370e2-122">Property</span></span>                | <span data-ttu-id="370e2-123">xsi:type</span><span class="sxs-lookup"><span data-stu-id="370e2-123">xsi:type</span></span>           | <span data-ttu-id="370e2-124">值</span><span class="sxs-lookup"><span data-stu-id="370e2-124">Value</span></span>                                                                  |
|-------------------------|--------------------|------------------------------------------------------------------------|
| <span data-ttu-id="370e2-125">DataType</span><span class="sxs-lookup"><span data-stu-id="370e2-125">DataType</span></span><br/>     | <span data-ttu-id="370e2-126">字串</span><span class="sxs-lookup"><span data-stu-id="370e2-126">string</span></span><br/>  | <span data-ttu-id="370e2-127">xs:integer</span><span class="sxs-lookup"><span data-stu-id="370e2-127">xs:integer</span></span><br/>                                                  |
| <span data-ttu-id="370e2-128">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="370e2-128">DefaultValue</span></span><br/> | <span data-ttu-id="370e2-129">整數</span><span class="sxs-lookup"><span data-stu-id="370e2-129">integer</span></span><br/> | <span data-ttu-id="370e2-130">未定義</span><span class="sxs-lookup"><span data-stu-id="370e2-130">undefined</span></span><br/>                                                   |
| <span data-ttu-id="370e2-131">MaxValue</span><span class="sxs-lookup"><span data-stu-id="370e2-131">MaxValue</span></span><br/>     | <span data-ttu-id="370e2-132">整數</span><span class="sxs-lookup"><span data-stu-id="370e2-132">integer</span></span><br/> | <span data-ttu-id="370e2-133">小於或等於 PageImageableSize-System.windows.controls.primitives.iscrollinfo.extentwidth 值</span><span class="sxs-lookup"><span data-stu-id="370e2-133">Less than or equal to PageImageableSize - ExtentWidth value</span></span><br/> |
| <span data-ttu-id="370e2-134">MinValue</span><span class="sxs-lookup"><span data-stu-id="370e2-134">MinValue</span></span><br/>     | <span data-ttu-id="370e2-135">整數</span><span class="sxs-lookup"><span data-stu-id="370e2-135">integer</span></span><br/> | <span data-ttu-id="370e2-136">0</span><span class="sxs-lookup"><span data-stu-id="370e2-136">0</span></span><br/>                                                           |
| <span data-ttu-id="370e2-137">多個</span><span class="sxs-lookup"><span data-stu-id="370e2-137">Multiple</span></span><br/>     | <span data-ttu-id="370e2-138">整數</span><span class="sxs-lookup"><span data-stu-id="370e2-138">integer</span></span><br/> | <span data-ttu-id="370e2-139">1</span><span class="sxs-lookup"><span data-stu-id="370e2-139">1</span></span><br/>                                                           |
| <span data-ttu-id="370e2-140">強制性</span><span class="sxs-lookup"><span data-stu-id="370e2-140">Mandatory</span></span><br/>    | <span data-ttu-id="370e2-141">字串</span><span class="sxs-lookup"><span data-stu-id="370e2-141">string</span></span><br/>  | <span data-ttu-id="370e2-142">psk：條件式</span><span class="sxs-lookup"><span data-stu-id="370e2-142">psk:Conditional</span></span><br/>                                             |
| <span data-ttu-id="370e2-143">Unittype.pixel 表示</span><span class="sxs-lookup"><span data-stu-id="370e2-143">UnitType</span></span><br/>     | <span data-ttu-id="370e2-144">字串</span><span class="sxs-lookup"><span data-stu-id="370e2-144">string</span></span><br/>  | <span data-ttu-id="370e2-145">微米</span><span class="sxs-lookup"><span data-stu-id="370e2-145">microns</span></span><br/>                                                     |



 

## <a name="related-topics"></a><span data-ttu-id="370e2-146">相關主題</span><span class="sxs-lookup"><span data-stu-id="370e2-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="370e2-147">列印架構規格</span><span class="sxs-lookup"><span data-stu-id="370e2-147">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




