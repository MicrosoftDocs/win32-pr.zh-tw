---
description: 本主題並非最新的。 如需最新資訊，請參閱列印架構規格。
ms.assetid: f94c1450-9648-4aee-8f88-2a9213eba4a9
title: PageWatermarkTransparency
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f0e96382656b1092a0dbc71352e788208f70b34
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/05/2021
ms.locfileid: "106981942"
---
# <a name="pagewatermarktransparency"></a><span data-ttu-id="d6f6a-104">PageWatermarkTransparency</span><span class="sxs-lookup"><span data-stu-id="d6f6a-104">PageWatermarkTransparency</span></span>

<span data-ttu-id="d6f6a-105">本主題並非最新的。</span><span class="sxs-lookup"><span data-stu-id="d6f6a-105">This topic is not current.</span></span> <span data-ttu-id="d6f6a-106">如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。</span><span class="sxs-lookup"><span data-stu-id="d6f6a-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="d6f6a-107">指定浮水印的透明度。</span><span class="sxs-lookup"><span data-stu-id="d6f6a-107">Specifies the transparency for the watermark.</span></span> <span data-ttu-id="d6f6a-108">完全不透明的值會是0。</span><span class="sxs-lookup"><span data-stu-id="d6f6a-108">Fully opaque would have a value of 0.</span></span>

-   [<span data-ttu-id="d6f6a-109">項目資訊</span><span class="sxs-lookup"><span data-stu-id="d6f6a-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="d6f6a-110">結構內容</span><span class="sxs-lookup"><span data-stu-id="d6f6a-110">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="d6f6a-111">項目資訊</span><span class="sxs-lookup"><span data-stu-id="d6f6a-111">Element Information</span></span>



| <span data-ttu-id="d6f6a-112">Name</span><span class="sxs-lookup"><span data-stu-id="d6f6a-112">Name</span></span>                       |                                            |
|----------------------------|--------------------------------------------|
| <span data-ttu-id="d6f6a-113">項目類型</span><span class="sxs-lookup"><span data-stu-id="d6f6a-113">Element Type</span></span> <br/>   | <span data-ttu-id="d6f6a-114">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="d6f6a-114">ParameterDef</span></span><br/>                    |
| <span data-ttu-id="d6f6a-115">範圍前置詞</span><span class="sxs-lookup"><span data-stu-id="d6f6a-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="d6f6a-116">頁面</span><span class="sxs-lookup"><span data-stu-id="d6f6a-116">Page</span></span><br/>                            |
| <span data-ttu-id="d6f6a-117">備註</span><span class="sxs-lookup"><span data-stu-id="d6f6a-117">Notes</span></span> <br/>          | <span data-ttu-id="d6f6a-118">連結至 PageWatermark 元素</span><span class="sxs-lookup"><span data-stu-id="d6f6a-118">Linked to PageWatermark element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="d6f6a-119">結構內容</span><span class="sxs-lookup"><span data-stu-id="d6f6a-119">Structure Content</span></span>

<span data-ttu-id="d6f6a-120">此元素的 XML 結構如下所示：</span><span class="sxs-lookup"><span data-stu-id="d6f6a-120">The XML structure of this element is as follows:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="d6f6a-121">結構屬性</span><span class="sxs-lookup"><span data-stu-id="d6f6a-121">Structure Properties</span></span>

<span data-ttu-id="d6f6a-122">下表概述 XML 結構中所定義之變數的特性。</span><span class="sxs-lookup"><span data-stu-id="d6f6a-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="d6f6a-123">屬性</span><span class="sxs-lookup"><span data-stu-id="d6f6a-123">Property</span></span>                | <span data-ttu-id="d6f6a-124">xsi:type</span><span class="sxs-lookup"><span data-stu-id="d6f6a-124">xsi:type</span></span>           | <span data-ttu-id="d6f6a-125">值</span><span class="sxs-lookup"><span data-stu-id="d6f6a-125">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="d6f6a-126">DataType</span><span class="sxs-lookup"><span data-stu-id="d6f6a-126">DataType</span></span><br/>     | <span data-ttu-id="d6f6a-127">字串</span><span class="sxs-lookup"><span data-stu-id="d6f6a-127">string</span></span><br/>  | <span data-ttu-id="d6f6a-128">xs:integer</span><span class="sxs-lookup"><span data-stu-id="d6f6a-128">xs:integer</span></span><br/>      |
| <span data-ttu-id="d6f6a-129">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="d6f6a-129">DefaultValue</span></span><br/> | <span data-ttu-id="d6f6a-130">整數</span><span class="sxs-lookup"><span data-stu-id="d6f6a-130">integer</span></span><br/> | <span data-ttu-id="d6f6a-131">0</span><span class="sxs-lookup"><span data-stu-id="d6f6a-131">0</span></span><br/>               |
| <span data-ttu-id="d6f6a-132">MaxValue</span><span class="sxs-lookup"><span data-stu-id="d6f6a-132">MaxValue</span></span><br/>     | <span data-ttu-id="d6f6a-133">整數</span><span class="sxs-lookup"><span data-stu-id="d6f6a-133">integer</span></span><br/> | <span data-ttu-id="d6f6a-134">100</span><span class="sxs-lookup"><span data-stu-id="d6f6a-134">100</span></span><br/>             |
| <span data-ttu-id="d6f6a-135">MinValue</span><span class="sxs-lookup"><span data-stu-id="d6f6a-135">MinValue</span></span><br/>     | <span data-ttu-id="d6f6a-136">整數</span><span class="sxs-lookup"><span data-stu-id="d6f6a-136">integer</span></span><br/> | <span data-ttu-id="d6f6a-137">0</span><span class="sxs-lookup"><span data-stu-id="d6f6a-137">0</span></span><br/>               |
| <span data-ttu-id="d6f6a-138">多個</span><span class="sxs-lookup"><span data-stu-id="d6f6a-138">Multiple</span></span><br/>     | <span data-ttu-id="d6f6a-139">整數</span><span class="sxs-lookup"><span data-stu-id="d6f6a-139">integer</span></span><br/> | <span data-ttu-id="d6f6a-140">1</span><span class="sxs-lookup"><span data-stu-id="d6f6a-140">1</span></span><br/>               |
| <span data-ttu-id="d6f6a-141">強制性</span><span class="sxs-lookup"><span data-stu-id="d6f6a-141">Mandatory</span></span><br/>    | <span data-ttu-id="d6f6a-142">字串</span><span class="sxs-lookup"><span data-stu-id="d6f6a-142">string</span></span><br/>  | <span data-ttu-id="d6f6a-143">psk：條件式</span><span class="sxs-lookup"><span data-stu-id="d6f6a-143">psk:Conditional</span></span><br/> |
| <span data-ttu-id="d6f6a-144">Unittype.pixel 表示</span><span class="sxs-lookup"><span data-stu-id="d6f6a-144">UnitType</span></span><br/>     | <span data-ttu-id="d6f6a-145">字串</span><span class="sxs-lookup"><span data-stu-id="d6f6a-145">string</span></span><br/>  | <span data-ttu-id="d6f6a-146">percent</span><span class="sxs-lookup"><span data-stu-id="d6f6a-146">percent</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="d6f6a-147">相關主題</span><span class="sxs-lookup"><span data-stu-id="d6f6a-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d6f6a-148">列印架構規格</span><span class="sxs-lookup"><span data-stu-id="d6f6a-148">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




