---
description: 取得 PageWatermarkTextFontSize 參數的相關資訊。 本主題並非最新的。 如需最新資訊，請參閱列印架構規格。
ms.assetid: 4c379898-d21f-4c6c-93c8-e5f386e032ba
title: PageWatermarkTextFontSize
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9eb28044ca676dedfb136cb58190db90a06fd624
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/19/2021
ms.locfileid: "112395993"
---
# <a name="pagewatermarktextfontsize"></a><span data-ttu-id="5ef5b-105">PageWatermarkTextFontSize</span><span class="sxs-lookup"><span data-stu-id="5ef5b-105">PageWatermarkTextFontSize</span></span>

<span data-ttu-id="5ef5b-106">本主題並非最新的。</span><span class="sxs-lookup"><span data-stu-id="5ef5b-106">This topic is not current.</span></span> <span data-ttu-id="5ef5b-107">如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。</span><span class="sxs-lookup"><span data-stu-id="5ef5b-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="5ef5b-108">定義浮水印文字的可用字型大小。</span><span class="sxs-lookup"><span data-stu-id="5ef5b-108">Defines the available font sizes for the watermark text.</span></span>

-   [<span data-ttu-id="5ef5b-109">項目資訊</span><span class="sxs-lookup"><span data-stu-id="5ef5b-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="5ef5b-110">結構內容</span><span class="sxs-lookup"><span data-stu-id="5ef5b-110">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="5ef5b-111">項目資訊</span><span class="sxs-lookup"><span data-stu-id="5ef5b-111">Element Information</span></span>



| <span data-ttu-id="5ef5b-112">Name</span><span class="sxs-lookup"><span data-stu-id="5ef5b-112">Name</span></span> | <span data-ttu-id="5ef5b-113">值</span><span class="sxs-lookup"><span data-stu-id="5ef5b-113">Value</span></span> |
|----------------------------|--------------------------------------------|
| <span data-ttu-id="5ef5b-114">項目類型</span><span class="sxs-lookup"><span data-stu-id="5ef5b-114">Element Type</span></span> <br/>   | <span data-ttu-id="5ef5b-115">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="5ef5b-115">ParameterDef</span></span><br/>                    |
| <span data-ttu-id="5ef5b-116">範圍前置詞</span><span class="sxs-lookup"><span data-stu-id="5ef5b-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="5ef5b-117">頁面</span><span class="sxs-lookup"><span data-stu-id="5ef5b-117">Page</span></span><br/>                            |
| <span data-ttu-id="5ef5b-118">備註</span><span class="sxs-lookup"><span data-stu-id="5ef5b-118">Notes</span></span> <br/>          | <span data-ttu-id="5ef5b-119">連結至 PageWatermark 元素</span><span class="sxs-lookup"><span data-stu-id="5ef5b-119">Linked to PageWatermark element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="5ef5b-120">結構內容</span><span class="sxs-lookup"><span data-stu-id="5ef5b-120">Structure Content</span></span>

<span data-ttu-id="5ef5b-121">此元素的 XML 結構如下所示：</span><span class="sxs-lookup"><span data-stu-id="5ef5b-121">The XML structure of this element is as follows:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="5ef5b-122">結構屬性</span><span class="sxs-lookup"><span data-stu-id="5ef5b-122">Structure Properties</span></span>

<span data-ttu-id="5ef5b-123">下表概述 XML 結構中所定義之變數的特性。</span><span class="sxs-lookup"><span data-stu-id="5ef5b-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="5ef5b-124">屬性</span><span class="sxs-lookup"><span data-stu-id="5ef5b-124">Property</span></span>                | <span data-ttu-id="5ef5b-125">xsi:type</span><span class="sxs-lookup"><span data-stu-id="5ef5b-125">xsi:type</span></span>           | <span data-ttu-id="5ef5b-126">值</span><span class="sxs-lookup"><span data-stu-id="5ef5b-126">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="5ef5b-127">DataType</span><span class="sxs-lookup"><span data-stu-id="5ef5b-127">DataType</span></span><br/>     | <span data-ttu-id="5ef5b-128">字串</span><span class="sxs-lookup"><span data-stu-id="5ef5b-128">string</span></span><br/>  | <span data-ttu-id="5ef5b-129">xs:integer</span><span class="sxs-lookup"><span data-stu-id="5ef5b-129">xs:integer</span></span><br/>      |
| <span data-ttu-id="5ef5b-130">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="5ef5b-130">DefaultValue</span></span><br/> | <span data-ttu-id="5ef5b-131">整數</span><span class="sxs-lookup"><span data-stu-id="5ef5b-131">integer</span></span><br/> | <span data-ttu-id="5ef5b-132">未定義</span><span class="sxs-lookup"><span data-stu-id="5ef5b-132">undefined</span></span><br/>       |
| <span data-ttu-id="5ef5b-133">MaxValue</span><span class="sxs-lookup"><span data-stu-id="5ef5b-133">MaxValue</span></span><br/>     | <span data-ttu-id="5ef5b-134">整數</span><span class="sxs-lookup"><span data-stu-id="5ef5b-134">integer</span></span><br/> | <span data-ttu-id="5ef5b-135">未定義</span><span class="sxs-lookup"><span data-stu-id="5ef5b-135">undefined</span></span><br/>       |
| <span data-ttu-id="5ef5b-136">MinValue</span><span class="sxs-lookup"><span data-stu-id="5ef5b-136">MinValue</span></span><br/>     | <span data-ttu-id="5ef5b-137">整數</span><span class="sxs-lookup"><span data-stu-id="5ef5b-137">integer</span></span><br/> | <span data-ttu-id="5ef5b-138">未定義</span><span class="sxs-lookup"><span data-stu-id="5ef5b-138">undefined</span></span><br/>       |
| <span data-ttu-id="5ef5b-139">多個</span><span class="sxs-lookup"><span data-stu-id="5ef5b-139">Multiple</span></span><br/>     | <span data-ttu-id="5ef5b-140">整數</span><span class="sxs-lookup"><span data-stu-id="5ef5b-140">integer</span></span><br/> | <span data-ttu-id="5ef5b-141">未定義</span><span class="sxs-lookup"><span data-stu-id="5ef5b-141">undefined</span></span><br/>       |
| <span data-ttu-id="5ef5b-142">強制性</span><span class="sxs-lookup"><span data-stu-id="5ef5b-142">Mandatory</span></span><br/>    | <span data-ttu-id="5ef5b-143">string</span><span class="sxs-lookup"><span data-stu-id="5ef5b-143">string</span></span><br/>  | <span data-ttu-id="5ef5b-144">psk：條件式</span><span class="sxs-lookup"><span data-stu-id="5ef5b-144">psk:Conditional</span></span><br/> |
| <span data-ttu-id="5ef5b-145">Unittype.pixel 表示</span><span class="sxs-lookup"><span data-stu-id="5ef5b-145">UnitType</span></span><br/>     | <span data-ttu-id="5ef5b-146">string</span><span class="sxs-lookup"><span data-stu-id="5ef5b-146">string</span></span><br/>  | <span data-ttu-id="5ef5b-147">點</span><span class="sxs-lookup"><span data-stu-id="5ef5b-147">points</span></span><br/>          |



 

## <a name="related-topics"></a><span data-ttu-id="5ef5b-148">相關主題</span><span class="sxs-lookup"><span data-stu-id="5ef5b-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5ef5b-149">列印架構規格</span><span class="sxs-lookup"><span data-stu-id="5ef5b-149">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




