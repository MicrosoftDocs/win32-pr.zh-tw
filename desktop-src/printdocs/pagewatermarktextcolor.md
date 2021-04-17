---
description: 本主題並非最新的。 如需最新資訊，請參閱列印架構規格。
ms.assetid: edbdd2c7-da04-49fb-a0f8-31a7df88f8ef
title: PageWatermarkTextColor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be77e76dd1b304a46b2760565a09fe0134d3f0b5
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/05/2021
ms.locfileid: "104514377"
---
# <a name="pagewatermarktextcolor"></a><span data-ttu-id="da963-104">PageWatermarkTextColor</span><span class="sxs-lookup"><span data-stu-id="da963-104">PageWatermarkTextColor</span></span>

<span data-ttu-id="da963-105">本主題並非最新的。</span><span class="sxs-lookup"><span data-stu-id="da963-105">This topic is not current.</span></span> <span data-ttu-id="da963-106">如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。</span><span class="sxs-lookup"><span data-stu-id="da963-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="da963-107">定義浮水印文字的 sRGB 色彩。</span><span class="sxs-lookup"><span data-stu-id="da963-107">Defines the sRGB color for the watermark text.</span></span> <span data-ttu-id="da963-108">格式為 ARGB： \# AARRGGBB。</span><span class="sxs-lookup"><span data-stu-id="da963-108">Format is ARGB: \#AARRGGBB.</span></span>

-   [<span data-ttu-id="da963-109">項目資訊</span><span class="sxs-lookup"><span data-stu-id="da963-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="da963-110">結構內容</span><span class="sxs-lookup"><span data-stu-id="da963-110">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="da963-111">項目資訊</span><span class="sxs-lookup"><span data-stu-id="da963-111">Element Information</span></span>



| <span data-ttu-id="da963-112">Name</span><span class="sxs-lookup"><span data-stu-id="da963-112">Name</span></span>                       |                                            |
|----------------------------|--------------------------------------------|
| <span data-ttu-id="da963-113">項目類型</span><span class="sxs-lookup"><span data-stu-id="da963-113">Element Type</span></span> <br/>   | <span data-ttu-id="da963-114">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="da963-114">ParameterDef</span></span><br/>                    |
| <span data-ttu-id="da963-115">範圍前置詞</span><span class="sxs-lookup"><span data-stu-id="da963-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="da963-116">頁面</span><span class="sxs-lookup"><span data-stu-id="da963-116">Page</span></span><br/>                            |
| <span data-ttu-id="da963-117">備註</span><span class="sxs-lookup"><span data-stu-id="da963-117">Notes</span></span> <br/>          | <span data-ttu-id="da963-118">連結至 PageWatermark 元素</span><span class="sxs-lookup"><span data-stu-id="da963-118">Linked to PageWatermark element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="da963-119">結構內容</span><span class="sxs-lookup"><span data-stu-id="da963-119">Structure Content</span></span>

<span data-ttu-id="da963-120">此元素的 XML 結構如下所示：</span><span class="sxs-lookup"><span data-stu-id="da963-120">The XML structure of this element is as follows:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageWatermarkTextColor">
  <psf:Property name="psf:DataType">
    <psf:Value xsi:type="xs:string">xs:string</psf:Value>
  </psf:Property>
  <psf:Property name="psf:DefaultValue">
    <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MaxLength">
    <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MinLength">
    <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:Mandatory">
    <psf:Value xsi:type="xs:string">psk:Conditional</psf:Value>
  </psf:Property>
  <psf:Property name="psf:UnitType">
    <psf:Value xsi:type="xs:string">sRGB</psf:Value>
  </psf:Property>
</psf:ParameterDef>
      
```

## <a name="structure-properties"></a><span data-ttu-id="da963-121">結構屬性</span><span class="sxs-lookup"><span data-stu-id="da963-121">Structure Properties</span></span>

<span data-ttu-id="da963-122">下表概述 XML 結構中所定義之變數的特性。</span><span class="sxs-lookup"><span data-stu-id="da963-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="da963-123">屬性</span><span class="sxs-lookup"><span data-stu-id="da963-123">Property</span></span>                | <span data-ttu-id="da963-124">xsi:type</span><span class="sxs-lookup"><span data-stu-id="da963-124">xsi:type</span></span>           | <span data-ttu-id="da963-125">值</span><span class="sxs-lookup"><span data-stu-id="da963-125">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="da963-126">DataType</span><span class="sxs-lookup"><span data-stu-id="da963-126">DataType</span></span><br/>     | <span data-ttu-id="da963-127">字串</span><span class="sxs-lookup"><span data-stu-id="da963-127">string</span></span><br/>  | <span data-ttu-id="da963-128">xs:string</span><span class="sxs-lookup"><span data-stu-id="da963-128">xs:string</span></span><br/>       |
| <span data-ttu-id="da963-129">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="da963-129">DefaultValue</span></span><br/> | <span data-ttu-id="da963-130">整數</span><span class="sxs-lookup"><span data-stu-id="da963-130">integer</span></span><br/> | <span data-ttu-id="da963-131">未定義</span><span class="sxs-lookup"><span data-stu-id="da963-131">undefined</span></span><br/>       |
| <span data-ttu-id="da963-132">MaxValue</span><span class="sxs-lookup"><span data-stu-id="da963-132">MaxValue</span></span><br/>     | <span data-ttu-id="da963-133">整數</span><span class="sxs-lookup"><span data-stu-id="da963-133">integer</span></span><br/> | <span data-ttu-id="da963-134">未定義</span><span class="sxs-lookup"><span data-stu-id="da963-134">undefined</span></span><br/>       |
| <span data-ttu-id="da963-135">MinValue</span><span class="sxs-lookup"><span data-stu-id="da963-135">MinValue</span></span><br/>     | <span data-ttu-id="da963-136">整數</span><span class="sxs-lookup"><span data-stu-id="da963-136">integer</span></span><br/> | <span data-ttu-id="da963-137">未定義</span><span class="sxs-lookup"><span data-stu-id="da963-137">undefined</span></span><br/>       |
| <span data-ttu-id="da963-138">強制性</span><span class="sxs-lookup"><span data-stu-id="da963-138">Mandatory</span></span><br/>    | <span data-ttu-id="da963-139">字串</span><span class="sxs-lookup"><span data-stu-id="da963-139">string</span></span><br/>  | <span data-ttu-id="da963-140">psk：條件式</span><span class="sxs-lookup"><span data-stu-id="da963-140">psk:Conditional</span></span><br/> |
| <span data-ttu-id="da963-141">Unittype.pixel 表示</span><span class="sxs-lookup"><span data-stu-id="da963-141">UnitType</span></span><br/>     | <span data-ttu-id="da963-142">字串</span><span class="sxs-lookup"><span data-stu-id="da963-142">string</span></span><br/>  | <span data-ttu-id="da963-143">sRGB</span><span class="sxs-lookup"><span data-stu-id="da963-143">sRGB</span></span><br/>            |



 

## <a name="related-topics"></a><span data-ttu-id="da963-144">相關主題</span><span class="sxs-lookup"><span data-stu-id="da963-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="da963-145">列印架構規格</span><span class="sxs-lookup"><span data-stu-id="da963-145">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




