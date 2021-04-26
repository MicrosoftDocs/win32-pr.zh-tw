---
description: 本主題並非最新的。 如需最新資訊，請參閱列印架構規格。
ms.assetid: edbdd2c7-da04-49fb-a0f8-31a7df88f8ef
title: PageWatermarkTextColor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a2cc4d4f88724080b09ef52d7ded781039ff852
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/26/2021
ms.locfileid: "107996885"
---
# <a name="pagewatermarktextcolor"></a><span data-ttu-id="03153-104">PageWatermarkTextColor</span><span class="sxs-lookup"><span data-stu-id="03153-104">PageWatermarkTextColor</span></span>

<span data-ttu-id="03153-105">本主題並非最新的。</span><span class="sxs-lookup"><span data-stu-id="03153-105">This topic is not current.</span></span> <span data-ttu-id="03153-106">如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。</span><span class="sxs-lookup"><span data-stu-id="03153-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="03153-107">定義浮水印文字的 sRGB 色彩。</span><span class="sxs-lookup"><span data-stu-id="03153-107">Defines the sRGB color for the watermark text.</span></span> <span data-ttu-id="03153-108">格式為 ARGB： \# AARRGGBB。</span><span class="sxs-lookup"><span data-stu-id="03153-108">Format is ARGB: \#AARRGGBB.</span></span>

-   [<span data-ttu-id="03153-109">項目資訊</span><span class="sxs-lookup"><span data-stu-id="03153-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="03153-110">結構內容</span><span class="sxs-lookup"><span data-stu-id="03153-110">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="03153-111">項目資訊</span><span class="sxs-lookup"><span data-stu-id="03153-111">Element Information</span></span>



| <span data-ttu-id="03153-112">Name</span><span class="sxs-lookup"><span data-stu-id="03153-112">Name</span></span> | <span data-ttu-id="03153-113">值</span><span class="sxs-lookup"><span data-stu-id="03153-113">Value</span></span> |
|----------------------------|--------------------------------------------|
| <span data-ttu-id="03153-114">項目類型</span><span class="sxs-lookup"><span data-stu-id="03153-114">Element Type</span></span> <br/>   | <span data-ttu-id="03153-115">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="03153-115">ParameterDef</span></span><br/>                    |
| <span data-ttu-id="03153-116">範圍前置詞</span><span class="sxs-lookup"><span data-stu-id="03153-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="03153-117">頁面</span><span class="sxs-lookup"><span data-stu-id="03153-117">Page</span></span><br/>                            |
| <span data-ttu-id="03153-118">備註</span><span class="sxs-lookup"><span data-stu-id="03153-118">Notes</span></span> <br/>          | <span data-ttu-id="03153-119">連結至 PageWatermark 元素</span><span class="sxs-lookup"><span data-stu-id="03153-119">Linked to PageWatermark element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="03153-120">結構內容</span><span class="sxs-lookup"><span data-stu-id="03153-120">Structure Content</span></span>

<span data-ttu-id="03153-121">此元素的 XML 結構如下所示：</span><span class="sxs-lookup"><span data-stu-id="03153-121">The XML structure of this element is as follows:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="03153-122">結構屬性</span><span class="sxs-lookup"><span data-stu-id="03153-122">Structure Properties</span></span>

<span data-ttu-id="03153-123">下表概述 XML 結構中所定義之變數的特性。</span><span class="sxs-lookup"><span data-stu-id="03153-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="03153-124">屬性</span><span class="sxs-lookup"><span data-stu-id="03153-124">Property</span></span>                | <span data-ttu-id="03153-125">xsi:type</span><span class="sxs-lookup"><span data-stu-id="03153-125">xsi:type</span></span>           | <span data-ttu-id="03153-126">值</span><span class="sxs-lookup"><span data-stu-id="03153-126">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="03153-127">DataType</span><span class="sxs-lookup"><span data-stu-id="03153-127">DataType</span></span><br/>     | <span data-ttu-id="03153-128">字串</span><span class="sxs-lookup"><span data-stu-id="03153-128">string</span></span><br/>  | <span data-ttu-id="03153-129">xs:string</span><span class="sxs-lookup"><span data-stu-id="03153-129">xs:string</span></span><br/>       |
| <span data-ttu-id="03153-130">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="03153-130">DefaultValue</span></span><br/> | <span data-ttu-id="03153-131">整數</span><span class="sxs-lookup"><span data-stu-id="03153-131">integer</span></span><br/> | <span data-ttu-id="03153-132">未定義</span><span class="sxs-lookup"><span data-stu-id="03153-132">undefined</span></span><br/>       |
| <span data-ttu-id="03153-133">MaxValue</span><span class="sxs-lookup"><span data-stu-id="03153-133">MaxValue</span></span><br/>     | <span data-ttu-id="03153-134">整數</span><span class="sxs-lookup"><span data-stu-id="03153-134">integer</span></span><br/> | <span data-ttu-id="03153-135">未定義</span><span class="sxs-lookup"><span data-stu-id="03153-135">undefined</span></span><br/>       |
| <span data-ttu-id="03153-136">MinValue</span><span class="sxs-lookup"><span data-stu-id="03153-136">MinValue</span></span><br/>     | <span data-ttu-id="03153-137">整數</span><span class="sxs-lookup"><span data-stu-id="03153-137">integer</span></span><br/> | <span data-ttu-id="03153-138">未定義</span><span class="sxs-lookup"><span data-stu-id="03153-138">undefined</span></span><br/>       |
| <span data-ttu-id="03153-139">強制性</span><span class="sxs-lookup"><span data-stu-id="03153-139">Mandatory</span></span><br/>    | <span data-ttu-id="03153-140">字串</span><span class="sxs-lookup"><span data-stu-id="03153-140">string</span></span><br/>  | <span data-ttu-id="03153-141">psk：條件式</span><span class="sxs-lookup"><span data-stu-id="03153-141">psk:Conditional</span></span><br/> |
| <span data-ttu-id="03153-142">Unittype.pixel 表示</span><span class="sxs-lookup"><span data-stu-id="03153-142">UnitType</span></span><br/>     | <span data-ttu-id="03153-143">字串</span><span class="sxs-lookup"><span data-stu-id="03153-143">string</span></span><br/>  | <span data-ttu-id="03153-144">sRGB</span><span class="sxs-lookup"><span data-stu-id="03153-144">sRGB</span></span><br/>            |



 

## <a name="related-topics"></a><span data-ttu-id="03153-145">相關主題</span><span class="sxs-lookup"><span data-stu-id="03153-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="03153-146">列印架構規格</span><span class="sxs-lookup"><span data-stu-id="03153-146">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




