---
description: 本主題並非最新的。 如需最新資訊，請參閱列印架構規格。
ms.assetid: ef429727-d881-408b-95ce-2acce667654a
title: PageWatermarkOriginHeight
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90736f8cac9c919f9d640ffc01311024ef79bc3a
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/26/2021
ms.locfileid: "107994486"
---
# <a name="pagewatermarkoriginheight"></a><span data-ttu-id="28c38-104">PageWatermarkOriginHeight</span><span class="sxs-lookup"><span data-stu-id="28c38-104">PageWatermarkOriginHeight</span></span>

<span data-ttu-id="28c38-105">本主題並非最新的。</span><span class="sxs-lookup"><span data-stu-id="28c38-105">This topic is not current.</span></span> <span data-ttu-id="28c38-106">如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。</span><span class="sxs-lookup"><span data-stu-id="28c38-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="28c38-107">指定相對於 PageImageableSize 原點的浮水印原點。</span><span class="sxs-lookup"><span data-stu-id="28c38-107">Specifies the origin of a watermark relative to the origin of the PageImageableSize.</span></span>

-   [<span data-ttu-id="28c38-108">項目資訊</span><span class="sxs-lookup"><span data-stu-id="28c38-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="28c38-109">結構內容</span><span class="sxs-lookup"><span data-stu-id="28c38-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="28c38-110">項目資訊</span><span class="sxs-lookup"><span data-stu-id="28c38-110">Element Information</span></span>



| <span data-ttu-id="28c38-111">Name</span><span class="sxs-lookup"><span data-stu-id="28c38-111">Name</span></span> | <span data-ttu-id="28c38-112">值</span><span class="sxs-lookup"><span data-stu-id="28c38-112">Value</span></span> |
|----------------------------|--------------------------------------------|
| <span data-ttu-id="28c38-113">項目類型</span><span class="sxs-lookup"><span data-stu-id="28c38-113">Element Type</span></span> <br/>   | <span data-ttu-id="28c38-114">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="28c38-114">ParameterDef</span></span><br/>                    |
| <span data-ttu-id="28c38-115">範圍前置詞</span><span class="sxs-lookup"><span data-stu-id="28c38-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="28c38-116">頁面</span><span class="sxs-lookup"><span data-stu-id="28c38-116">Page</span></span><br/>                            |
| <span data-ttu-id="28c38-117">備註</span><span class="sxs-lookup"><span data-stu-id="28c38-117">Notes</span></span> <br/>          | <span data-ttu-id="28c38-118">連結至 PageWatermark 元素</span><span class="sxs-lookup"><span data-stu-id="28c38-118">Linked to PageWatermark element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="28c38-119">結構內容</span><span class="sxs-lookup"><span data-stu-id="28c38-119">Structure Content</span></span>

<span data-ttu-id="28c38-120">此元素的 XML 結構如下所示：</span><span class="sxs-lookup"><span data-stu-id="28c38-120">The XML structure of this element is as follows:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageWatermarkOriginHeight">
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

## <a name="structure-properties"></a><span data-ttu-id="28c38-121">結構屬性</span><span class="sxs-lookup"><span data-stu-id="28c38-121">Structure Properties</span></span>

<span data-ttu-id="28c38-122">下表概述 XML 結構中所定義之變數的特性。</span><span class="sxs-lookup"><span data-stu-id="28c38-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="28c38-123">屬性</span><span class="sxs-lookup"><span data-stu-id="28c38-123">Property</span></span>                | <span data-ttu-id="28c38-124">xsi:type</span><span class="sxs-lookup"><span data-stu-id="28c38-124">xsi:type</span></span>           | <span data-ttu-id="28c38-125">值</span><span class="sxs-lookup"><span data-stu-id="28c38-125">Value</span></span>                                                                   |
|-------------------------|--------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="28c38-126">DataType</span><span class="sxs-lookup"><span data-stu-id="28c38-126">DataType</span></span><br/>     | <span data-ttu-id="28c38-127">字串</span><span class="sxs-lookup"><span data-stu-id="28c38-127">string</span></span><br/>  | <span data-ttu-id="28c38-128">xs:integer</span><span class="sxs-lookup"><span data-stu-id="28c38-128">xs:integer</span></span><br/>                                                   |
| <span data-ttu-id="28c38-129">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="28c38-129">DefaultValue</span></span><br/> | <span data-ttu-id="28c38-130">整數</span><span class="sxs-lookup"><span data-stu-id="28c38-130">integer</span></span><br/> | <span data-ttu-id="28c38-131">未定義</span><span class="sxs-lookup"><span data-stu-id="28c38-131">undefined</span></span><br/>                                                    |
| <span data-ttu-id="28c38-132">MaxValue</span><span class="sxs-lookup"><span data-stu-id="28c38-132">MaxValue</span></span><br/>     | <span data-ttu-id="28c38-133">整數</span><span class="sxs-lookup"><span data-stu-id="28c38-133">integer</span></span><br/> | <span data-ttu-id="28c38-134">小於或等於 PageImageableSize-ExtentHeight 值</span><span class="sxs-lookup"><span data-stu-id="28c38-134">Less than or equal to PageImageableSize - ExtentHeight value</span></span><br/> |
| <span data-ttu-id="28c38-135">MinValue</span><span class="sxs-lookup"><span data-stu-id="28c38-135">MinValue</span></span><br/>     | <span data-ttu-id="28c38-136">整數</span><span class="sxs-lookup"><span data-stu-id="28c38-136">integer</span></span><br/> | <span data-ttu-id="28c38-137">0</span><span class="sxs-lookup"><span data-stu-id="28c38-137">0</span></span><br/>                                                            |
| <span data-ttu-id="28c38-138">多個</span><span class="sxs-lookup"><span data-stu-id="28c38-138">Multiple</span></span><br/>     | <span data-ttu-id="28c38-139">整數</span><span class="sxs-lookup"><span data-stu-id="28c38-139">integer</span></span><br/> | <span data-ttu-id="28c38-140">1</span><span class="sxs-lookup"><span data-stu-id="28c38-140">1</span></span><br/>                                                            |
| <span data-ttu-id="28c38-141">強制性</span><span class="sxs-lookup"><span data-stu-id="28c38-141">Mandatory</span></span><br/>    | <span data-ttu-id="28c38-142">字串</span><span class="sxs-lookup"><span data-stu-id="28c38-142">string</span></span><br/>  | <span data-ttu-id="28c38-143">psk：條件式</span><span class="sxs-lookup"><span data-stu-id="28c38-143">psk:Conditional</span></span><br/>                                              |
| <span data-ttu-id="28c38-144">Unittype.pixel 表示</span><span class="sxs-lookup"><span data-stu-id="28c38-144">UnitType</span></span><br/>     | <span data-ttu-id="28c38-145">字串</span><span class="sxs-lookup"><span data-stu-id="28c38-145">string</span></span><br/>  | <span data-ttu-id="28c38-146">微米</span><span class="sxs-lookup"><span data-stu-id="28c38-146">microns</span></span><br/>                                                      |



 

## <a name="related-topics"></a><span data-ttu-id="28c38-147">相關主題</span><span class="sxs-lookup"><span data-stu-id="28c38-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="28c38-148">列印架構規格</span><span class="sxs-lookup"><span data-stu-id="28c38-148">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




