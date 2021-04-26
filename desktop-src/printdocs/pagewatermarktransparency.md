---
description: 本主題並非最新的。 如需最新資訊，請參閱列印架構規格。
ms.assetid: f94c1450-9648-4aee-8f88-2a9213eba4a9
title: PageWatermarkTransparency
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8d46a03cfb1b2129f4c89a6ea7c751e23cd565e
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/26/2021
ms.locfileid: "107996875"
---
# <a name="pagewatermarktransparency"></a><span data-ttu-id="1cbb3-104">PageWatermarkTransparency</span><span class="sxs-lookup"><span data-stu-id="1cbb3-104">PageWatermarkTransparency</span></span>

<span data-ttu-id="1cbb3-105">本主題並非最新的。</span><span class="sxs-lookup"><span data-stu-id="1cbb3-105">This topic is not current.</span></span> <span data-ttu-id="1cbb3-106">如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。</span><span class="sxs-lookup"><span data-stu-id="1cbb3-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="1cbb3-107">指定浮水印的透明度。</span><span class="sxs-lookup"><span data-stu-id="1cbb3-107">Specifies the transparency for the watermark.</span></span> <span data-ttu-id="1cbb3-108">完全不透明的值會是0。</span><span class="sxs-lookup"><span data-stu-id="1cbb3-108">Fully opaque would have a value of 0.</span></span>

-   [<span data-ttu-id="1cbb3-109">項目資訊</span><span class="sxs-lookup"><span data-stu-id="1cbb3-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="1cbb3-110">結構內容</span><span class="sxs-lookup"><span data-stu-id="1cbb3-110">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="1cbb3-111">項目資訊</span><span class="sxs-lookup"><span data-stu-id="1cbb3-111">Element Information</span></span>



| <span data-ttu-id="1cbb3-112">Name</span><span class="sxs-lookup"><span data-stu-id="1cbb3-112">Name</span></span> | <span data-ttu-id="1cbb3-113">值</span><span class="sxs-lookup"><span data-stu-id="1cbb3-113">Value</span></span> |
|----------------------------|--------------------------------------------|
| <span data-ttu-id="1cbb3-114">項目類型</span><span class="sxs-lookup"><span data-stu-id="1cbb3-114">Element Type</span></span> <br/>   | <span data-ttu-id="1cbb3-115">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="1cbb3-115">ParameterDef</span></span><br/>                    |
| <span data-ttu-id="1cbb3-116">範圍前置詞</span><span class="sxs-lookup"><span data-stu-id="1cbb3-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="1cbb3-117">頁面</span><span class="sxs-lookup"><span data-stu-id="1cbb3-117">Page</span></span><br/>                            |
| <span data-ttu-id="1cbb3-118">備註</span><span class="sxs-lookup"><span data-stu-id="1cbb3-118">Notes</span></span> <br/>          | <span data-ttu-id="1cbb3-119">連結至 PageWatermark 元素</span><span class="sxs-lookup"><span data-stu-id="1cbb3-119">Linked to PageWatermark element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="1cbb3-120">結構內容</span><span class="sxs-lookup"><span data-stu-id="1cbb3-120">Structure Content</span></span>

<span data-ttu-id="1cbb3-121">此元素的 XML 結構如下所示：</span><span class="sxs-lookup"><span data-stu-id="1cbb3-121">The XML structure of this element is as follows:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageWatermarkTransparency">
  <psf:Property name="psf:DataType">
    <psf:Value xsi:type="xs:string">xs:integer</psf:Value>
  </psf:Property>
  <psf:Property name="psf:DefaultValue">
    <psf:Value xsi:type="xs:integer">0</psf:Value>
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

## <a name="structure-properties"></a><span data-ttu-id="1cbb3-122">結構屬性</span><span class="sxs-lookup"><span data-stu-id="1cbb3-122">Structure Properties</span></span>

<span data-ttu-id="1cbb3-123">下表概述 XML 結構中所定義之變數的特性。</span><span class="sxs-lookup"><span data-stu-id="1cbb3-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="1cbb3-124">屬性</span><span class="sxs-lookup"><span data-stu-id="1cbb3-124">Property</span></span>                | <span data-ttu-id="1cbb3-125">xsi:type</span><span class="sxs-lookup"><span data-stu-id="1cbb3-125">xsi:type</span></span>           | <span data-ttu-id="1cbb3-126">值</span><span class="sxs-lookup"><span data-stu-id="1cbb3-126">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="1cbb3-127">DataType</span><span class="sxs-lookup"><span data-stu-id="1cbb3-127">DataType</span></span><br/>     | <span data-ttu-id="1cbb3-128">字串</span><span class="sxs-lookup"><span data-stu-id="1cbb3-128">string</span></span><br/>  | <span data-ttu-id="1cbb3-129">xs:integer</span><span class="sxs-lookup"><span data-stu-id="1cbb3-129">xs:integer</span></span><br/>      |
| <span data-ttu-id="1cbb3-130">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="1cbb3-130">DefaultValue</span></span><br/> | <span data-ttu-id="1cbb3-131">整數</span><span class="sxs-lookup"><span data-stu-id="1cbb3-131">integer</span></span><br/> | <span data-ttu-id="1cbb3-132">0</span><span class="sxs-lookup"><span data-stu-id="1cbb3-132">0</span></span><br/>               |
| <span data-ttu-id="1cbb3-133">MaxValue</span><span class="sxs-lookup"><span data-stu-id="1cbb3-133">MaxValue</span></span><br/>     | <span data-ttu-id="1cbb3-134">整數</span><span class="sxs-lookup"><span data-stu-id="1cbb3-134">integer</span></span><br/> | <span data-ttu-id="1cbb3-135">100</span><span class="sxs-lookup"><span data-stu-id="1cbb3-135">100</span></span><br/>             |
| <span data-ttu-id="1cbb3-136">MinValue</span><span class="sxs-lookup"><span data-stu-id="1cbb3-136">MinValue</span></span><br/>     | <span data-ttu-id="1cbb3-137">整數</span><span class="sxs-lookup"><span data-stu-id="1cbb3-137">integer</span></span><br/> | <span data-ttu-id="1cbb3-138">0</span><span class="sxs-lookup"><span data-stu-id="1cbb3-138">0</span></span><br/>               |
| <span data-ttu-id="1cbb3-139">多個</span><span class="sxs-lookup"><span data-stu-id="1cbb3-139">Multiple</span></span><br/>     | <span data-ttu-id="1cbb3-140">整數</span><span class="sxs-lookup"><span data-stu-id="1cbb3-140">integer</span></span><br/> | <span data-ttu-id="1cbb3-141">1</span><span class="sxs-lookup"><span data-stu-id="1cbb3-141">1</span></span><br/>               |
| <span data-ttu-id="1cbb3-142">強制性</span><span class="sxs-lookup"><span data-stu-id="1cbb3-142">Mandatory</span></span><br/>    | <span data-ttu-id="1cbb3-143">字串</span><span class="sxs-lookup"><span data-stu-id="1cbb3-143">string</span></span><br/>  | <span data-ttu-id="1cbb3-144">psk：條件式</span><span class="sxs-lookup"><span data-stu-id="1cbb3-144">psk:Conditional</span></span><br/> |
| <span data-ttu-id="1cbb3-145">Unittype.pixel 表示</span><span class="sxs-lookup"><span data-stu-id="1cbb3-145">UnitType</span></span><br/>     | <span data-ttu-id="1cbb3-146">字串</span><span class="sxs-lookup"><span data-stu-id="1cbb3-146">string</span></span><br/>  | <span data-ttu-id="1cbb3-147">percent</span><span class="sxs-lookup"><span data-stu-id="1cbb3-147">percent</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="1cbb3-148">相關主題</span><span class="sxs-lookup"><span data-stu-id="1cbb3-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1cbb3-149">列印架構規格</span><span class="sxs-lookup"><span data-stu-id="1cbb3-149">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




