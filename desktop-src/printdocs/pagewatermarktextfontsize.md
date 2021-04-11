---
description: 本主題並非最新的。 如需最新資訊，請參閱列印架構規格。
ms.assetid: 4c379898-d21f-4c6c-93c8-e5f386e032ba
title: PageWatermarkTextFontSize
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 678630b7b7f6650a1317efef95c30effc71c6082
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/05/2021
ms.locfileid: "104035232"
---
# <a name="pagewatermarktextfontsize"></a><span data-ttu-id="d9abb-104">PageWatermarkTextFontSize</span><span class="sxs-lookup"><span data-stu-id="d9abb-104">PageWatermarkTextFontSize</span></span>

<span data-ttu-id="d9abb-105">本主題並非最新的。</span><span class="sxs-lookup"><span data-stu-id="d9abb-105">This topic is not current.</span></span> <span data-ttu-id="d9abb-106">如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。</span><span class="sxs-lookup"><span data-stu-id="d9abb-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="d9abb-107">定義浮水印文字的可用字型大小。</span><span class="sxs-lookup"><span data-stu-id="d9abb-107">Defines the available font sizes for the watermark text.</span></span>

-   [<span data-ttu-id="d9abb-108">項目資訊</span><span class="sxs-lookup"><span data-stu-id="d9abb-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="d9abb-109">結構內容</span><span class="sxs-lookup"><span data-stu-id="d9abb-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="d9abb-110">項目資訊</span><span class="sxs-lookup"><span data-stu-id="d9abb-110">Element Information</span></span>



| <span data-ttu-id="d9abb-111">Name</span><span class="sxs-lookup"><span data-stu-id="d9abb-111">Name</span></span>                       |                                            |
|----------------------------|--------------------------------------------|
| <span data-ttu-id="d9abb-112">項目類型</span><span class="sxs-lookup"><span data-stu-id="d9abb-112">Element Type</span></span> <br/>   | <span data-ttu-id="d9abb-113">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="d9abb-113">ParameterDef</span></span><br/>                    |
| <span data-ttu-id="d9abb-114">範圍前置詞</span><span class="sxs-lookup"><span data-stu-id="d9abb-114">Scoping Prefix</span></span> <br/> | <span data-ttu-id="d9abb-115">頁面</span><span class="sxs-lookup"><span data-stu-id="d9abb-115">Page</span></span><br/>                            |
| <span data-ttu-id="d9abb-116">備註</span><span class="sxs-lookup"><span data-stu-id="d9abb-116">Notes</span></span> <br/>          | <span data-ttu-id="d9abb-117">連結至 PageWatermark 元素</span><span class="sxs-lookup"><span data-stu-id="d9abb-117">Linked to PageWatermark element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="d9abb-118">結構內容</span><span class="sxs-lookup"><span data-stu-id="d9abb-118">Structure Content</span></span>

<span data-ttu-id="d9abb-119">此元素的 XML 結構如下所示：</span><span class="sxs-lookup"><span data-stu-id="d9abb-119">The XML structure of this element is as follows:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageWatermarkTextFontSize">
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
    <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:Multiple">
    <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:Mandatory">
    <psf:Value xsi:type="xs:string">psk:Conditional</psf:Value>
  </psf:Property>
  <psf:Property name="psf:UnitType">
    <psf:Value xsi:type="xs:string">points</psf:Value>
  </psf:Property>
</psf:ParameterDef>
      
```

## <a name="structure-properties"></a><span data-ttu-id="d9abb-120">結構屬性</span><span class="sxs-lookup"><span data-stu-id="d9abb-120">Structure Properties</span></span>

<span data-ttu-id="d9abb-121">下表概述 XML 結構中所定義之變數的特性。</span><span class="sxs-lookup"><span data-stu-id="d9abb-121">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="d9abb-122">屬性</span><span class="sxs-lookup"><span data-stu-id="d9abb-122">Property</span></span>                | <span data-ttu-id="d9abb-123">xsi:type</span><span class="sxs-lookup"><span data-stu-id="d9abb-123">xsi:type</span></span>           | <span data-ttu-id="d9abb-124">值</span><span class="sxs-lookup"><span data-stu-id="d9abb-124">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="d9abb-125">DataType</span><span class="sxs-lookup"><span data-stu-id="d9abb-125">DataType</span></span><br/>     | <span data-ttu-id="d9abb-126">字串</span><span class="sxs-lookup"><span data-stu-id="d9abb-126">string</span></span><br/>  | <span data-ttu-id="d9abb-127">xs:integer</span><span class="sxs-lookup"><span data-stu-id="d9abb-127">xs:integer</span></span><br/>      |
| <span data-ttu-id="d9abb-128">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="d9abb-128">DefaultValue</span></span><br/> | <span data-ttu-id="d9abb-129">整數</span><span class="sxs-lookup"><span data-stu-id="d9abb-129">integer</span></span><br/> | <span data-ttu-id="d9abb-130">未定義</span><span class="sxs-lookup"><span data-stu-id="d9abb-130">undefined</span></span><br/>       |
| <span data-ttu-id="d9abb-131">MaxValue</span><span class="sxs-lookup"><span data-stu-id="d9abb-131">MaxValue</span></span><br/>     | <span data-ttu-id="d9abb-132">整數</span><span class="sxs-lookup"><span data-stu-id="d9abb-132">integer</span></span><br/> | <span data-ttu-id="d9abb-133">未定義</span><span class="sxs-lookup"><span data-stu-id="d9abb-133">undefined</span></span><br/>       |
| <span data-ttu-id="d9abb-134">MinValue</span><span class="sxs-lookup"><span data-stu-id="d9abb-134">MinValue</span></span><br/>     | <span data-ttu-id="d9abb-135">整數</span><span class="sxs-lookup"><span data-stu-id="d9abb-135">integer</span></span><br/> | <span data-ttu-id="d9abb-136">未定義</span><span class="sxs-lookup"><span data-stu-id="d9abb-136">undefined</span></span><br/>       |
| <span data-ttu-id="d9abb-137">多個</span><span class="sxs-lookup"><span data-stu-id="d9abb-137">Multiple</span></span><br/>     | <span data-ttu-id="d9abb-138">整數</span><span class="sxs-lookup"><span data-stu-id="d9abb-138">integer</span></span><br/> | <span data-ttu-id="d9abb-139">未定義</span><span class="sxs-lookup"><span data-stu-id="d9abb-139">undefined</span></span><br/>       |
| <span data-ttu-id="d9abb-140">強制性</span><span class="sxs-lookup"><span data-stu-id="d9abb-140">Mandatory</span></span><br/>    | <span data-ttu-id="d9abb-141">字串</span><span class="sxs-lookup"><span data-stu-id="d9abb-141">string</span></span><br/>  | <span data-ttu-id="d9abb-142">psk：條件式</span><span class="sxs-lookup"><span data-stu-id="d9abb-142">psk:Conditional</span></span><br/> |
| <span data-ttu-id="d9abb-143">Unittype.pixel 表示</span><span class="sxs-lookup"><span data-stu-id="d9abb-143">UnitType</span></span><br/>     | <span data-ttu-id="d9abb-144">字串</span><span class="sxs-lookup"><span data-stu-id="d9abb-144">string</span></span><br/>  | <span data-ttu-id="d9abb-145">點</span><span class="sxs-lookup"><span data-stu-id="d9abb-145">points</span></span><br/>          |



 

## <a name="related-topics"></a><span data-ttu-id="d9abb-146">相關主題</span><span class="sxs-lookup"><span data-stu-id="d9abb-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d9abb-147">列印架構規格</span><span class="sxs-lookup"><span data-stu-id="d9abb-147">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




