---
description: 取得 PageWatermarkTransparency 參數的相關資訊。 本主題並非最新的。 如需最新資訊，請參閱列印架構規格。
ms.assetid: f94c1450-9648-4aee-8f88-2a9213eba4a9
title: PageWatermarkTransparency
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46ba405c3cd4a269edc4585ad8cba4c81f2c05e9
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/19/2021
ms.locfileid: "112394783"
---
# <a name="pagewatermarktransparency"></a><span data-ttu-id="fcbee-105">PageWatermarkTransparency</span><span class="sxs-lookup"><span data-stu-id="fcbee-105">PageWatermarkTransparency</span></span>

<span data-ttu-id="fcbee-106">本主題並非最新的。</span><span class="sxs-lookup"><span data-stu-id="fcbee-106">This topic is not current.</span></span> <span data-ttu-id="fcbee-107">如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。</span><span class="sxs-lookup"><span data-stu-id="fcbee-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="fcbee-108">指定浮水印的透明度。</span><span class="sxs-lookup"><span data-stu-id="fcbee-108">Specifies the transparency for the watermark.</span></span> <span data-ttu-id="fcbee-109">完全不透明的值會是0。</span><span class="sxs-lookup"><span data-stu-id="fcbee-109">Fully opaque would have a value of 0.</span></span>

-   [<span data-ttu-id="fcbee-110">項目資訊</span><span class="sxs-lookup"><span data-stu-id="fcbee-110">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="fcbee-111">結構內容</span><span class="sxs-lookup"><span data-stu-id="fcbee-111">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="fcbee-112">項目資訊</span><span class="sxs-lookup"><span data-stu-id="fcbee-112">Element Information</span></span>



| <span data-ttu-id="fcbee-113">Name</span><span class="sxs-lookup"><span data-stu-id="fcbee-113">Name</span></span> | <span data-ttu-id="fcbee-114">值</span><span class="sxs-lookup"><span data-stu-id="fcbee-114">Value</span></span> |
|----------------------------|--------------------------------------------|
| <span data-ttu-id="fcbee-115">項目類型</span><span class="sxs-lookup"><span data-stu-id="fcbee-115">Element Type</span></span> <br/>   | <span data-ttu-id="fcbee-116">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="fcbee-116">ParameterDef</span></span><br/>                    |
| <span data-ttu-id="fcbee-117">範圍前置詞</span><span class="sxs-lookup"><span data-stu-id="fcbee-117">Scoping Prefix</span></span> <br/> | <span data-ttu-id="fcbee-118">頁面</span><span class="sxs-lookup"><span data-stu-id="fcbee-118">Page</span></span><br/>                            |
| <span data-ttu-id="fcbee-119">備註</span><span class="sxs-lookup"><span data-stu-id="fcbee-119">Notes</span></span> <br/>          | <span data-ttu-id="fcbee-120">連結至 PageWatermark 元素</span><span class="sxs-lookup"><span data-stu-id="fcbee-120">Linked to PageWatermark element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="fcbee-121">結構內容</span><span class="sxs-lookup"><span data-stu-id="fcbee-121">Structure Content</span></span>

<span data-ttu-id="fcbee-122">此元素的 XML 結構如下所示：</span><span class="sxs-lookup"><span data-stu-id="fcbee-122">The XML structure of this element is as follows:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="fcbee-123">結構屬性</span><span class="sxs-lookup"><span data-stu-id="fcbee-123">Structure Properties</span></span>

<span data-ttu-id="fcbee-124">下表概述 XML 結構中所定義之變數的特性。</span><span class="sxs-lookup"><span data-stu-id="fcbee-124">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="fcbee-125">屬性</span><span class="sxs-lookup"><span data-stu-id="fcbee-125">Property</span></span>                | <span data-ttu-id="fcbee-126">xsi:type</span><span class="sxs-lookup"><span data-stu-id="fcbee-126">xsi:type</span></span>           | <span data-ttu-id="fcbee-127">值</span><span class="sxs-lookup"><span data-stu-id="fcbee-127">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="fcbee-128">DataType</span><span class="sxs-lookup"><span data-stu-id="fcbee-128">DataType</span></span><br/>     | <span data-ttu-id="fcbee-129">字串</span><span class="sxs-lookup"><span data-stu-id="fcbee-129">string</span></span><br/>  | <span data-ttu-id="fcbee-130">xs:integer</span><span class="sxs-lookup"><span data-stu-id="fcbee-130">xs:integer</span></span><br/>      |
| <span data-ttu-id="fcbee-131">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="fcbee-131">DefaultValue</span></span><br/> | <span data-ttu-id="fcbee-132">整數</span><span class="sxs-lookup"><span data-stu-id="fcbee-132">integer</span></span><br/> | <span data-ttu-id="fcbee-133">0</span><span class="sxs-lookup"><span data-stu-id="fcbee-133">0</span></span><br/>               |
| <span data-ttu-id="fcbee-134">MaxValue</span><span class="sxs-lookup"><span data-stu-id="fcbee-134">MaxValue</span></span><br/>     | <span data-ttu-id="fcbee-135">整數</span><span class="sxs-lookup"><span data-stu-id="fcbee-135">integer</span></span><br/> | <span data-ttu-id="fcbee-136">100</span><span class="sxs-lookup"><span data-stu-id="fcbee-136">100</span></span><br/>             |
| <span data-ttu-id="fcbee-137">MinValue</span><span class="sxs-lookup"><span data-stu-id="fcbee-137">MinValue</span></span><br/>     | <span data-ttu-id="fcbee-138">整數</span><span class="sxs-lookup"><span data-stu-id="fcbee-138">integer</span></span><br/> | <span data-ttu-id="fcbee-139">0</span><span class="sxs-lookup"><span data-stu-id="fcbee-139">0</span></span><br/>               |
| <span data-ttu-id="fcbee-140">多個</span><span class="sxs-lookup"><span data-stu-id="fcbee-140">Multiple</span></span><br/>     | <span data-ttu-id="fcbee-141">整數</span><span class="sxs-lookup"><span data-stu-id="fcbee-141">integer</span></span><br/> | <span data-ttu-id="fcbee-142">1</span><span class="sxs-lookup"><span data-stu-id="fcbee-142">1</span></span><br/>               |
| <span data-ttu-id="fcbee-143">強制性</span><span class="sxs-lookup"><span data-stu-id="fcbee-143">Mandatory</span></span><br/>    | <span data-ttu-id="fcbee-144">string</span><span class="sxs-lookup"><span data-stu-id="fcbee-144">string</span></span><br/>  | <span data-ttu-id="fcbee-145">psk：條件式</span><span class="sxs-lookup"><span data-stu-id="fcbee-145">psk:Conditional</span></span><br/> |
| <span data-ttu-id="fcbee-146">Unittype.pixel 表示</span><span class="sxs-lookup"><span data-stu-id="fcbee-146">UnitType</span></span><br/>     | <span data-ttu-id="fcbee-147">string</span><span class="sxs-lookup"><span data-stu-id="fcbee-147">string</span></span><br/>  | <span data-ttu-id="fcbee-148">percent</span><span class="sxs-lookup"><span data-stu-id="fcbee-148">percent</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="fcbee-149">相關主題</span><span class="sxs-lookup"><span data-stu-id="fcbee-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fcbee-150">列印架構規格</span><span class="sxs-lookup"><span data-stu-id="fcbee-150">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




