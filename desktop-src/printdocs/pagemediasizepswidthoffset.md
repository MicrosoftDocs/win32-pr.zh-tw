---
description: 本主題並非最新的。 如需最新資訊，請參閱列印架構規格。
ms.assetid: b93ad6e6-ab27-4fab-b488-6f402b6ee857
title: PageMediaSizePSWidthOffset
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91cb8440af2b35bbe8f3f4a82a567beee43d1d44
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/05/2021
ms.locfileid: "106975608"
---
# <a name="pagemediasizepswidthoffset"></a><span data-ttu-id="249b8-104">PageMediaSizePSWidthOffset</span><span class="sxs-lookup"><span data-stu-id="249b8-104">PageMediaSizePSWidthOffset</span></span>

<span data-ttu-id="249b8-105">本主題並非最新的。</span><span class="sxs-lookup"><span data-stu-id="249b8-105">This topic is not current.</span></span> <span data-ttu-id="249b8-106">如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。</span><span class="sxs-lookup"><span data-stu-id="249b8-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="249b8-107">指定相對於饋送方向方向的位移 (參考 [PostScript 印表機描述檔案格式規格](https://www.adobe.com/products/postscript/pdfs/PLRM.pdf)) 。</span><span class="sxs-lookup"><span data-stu-id="249b8-107">Specifies the offset perpendicular to the feed-orientation direction (Reference [PostScript Printer Description File Format Specification](https://www.adobe.com/products/postscript/pdfs/PLRM.pdf)).</span></span>

-   [<span data-ttu-id="249b8-108">項目資訊</span><span class="sxs-lookup"><span data-stu-id="249b8-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="249b8-109">結構內容</span><span class="sxs-lookup"><span data-stu-id="249b8-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="249b8-110">項目資訊</span><span class="sxs-lookup"><span data-stu-id="249b8-110">Element Information</span></span>



| <span data-ttu-id="249b8-111">Name</span><span class="sxs-lookup"><span data-stu-id="249b8-111">Name</span></span>                       |                                                             |
|----------------------------|-------------------------------------------------------------|
| <span data-ttu-id="249b8-112">項目類型</span><span class="sxs-lookup"><span data-stu-id="249b8-112">Element Type</span></span> <br/>   | <span data-ttu-id="249b8-113">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="249b8-113">ParameterDef</span></span><br/>                                     |
| <span data-ttu-id="249b8-114">範圍前置詞</span><span class="sxs-lookup"><span data-stu-id="249b8-114">Scoping Prefix</span></span> <br/> | <span data-ttu-id="249b8-115">頁面</span><span class="sxs-lookup"><span data-stu-id="249b8-115">Page</span></span><br/>                                             |
| <span data-ttu-id="249b8-116">備註</span><span class="sxs-lookup"><span data-stu-id="249b8-116">Notes</span></span> <br/>          | <span data-ttu-id="249b8-117">連結至 PageMediaSize 元素，CustomPS 選項</span><span class="sxs-lookup"><span data-stu-id="249b8-117">Linked to PageMediaSize element, CustomPS option</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="249b8-118">結構內容</span><span class="sxs-lookup"><span data-stu-id="249b8-118">Structure Content</span></span>

<span data-ttu-id="249b8-119">此元素的 XML 結構為：</span><span class="sxs-lookup"><span data-stu-id="249b8-119">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageMediaSizePSWidthOffset">
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

## <a name="structure-properties"></a><span data-ttu-id="249b8-120">結構屬性</span><span class="sxs-lookup"><span data-stu-id="249b8-120">Structure Properties</span></span>

<span data-ttu-id="249b8-121">下表概述 XML 結構中所定義之變數的特性。</span><span class="sxs-lookup"><span data-stu-id="249b8-121">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="249b8-122">屬性</span><span class="sxs-lookup"><span data-stu-id="249b8-122">Property</span></span>                | <span data-ttu-id="249b8-123">xsi:type</span><span class="sxs-lookup"><span data-stu-id="249b8-123">xsi:type</span></span>           | <span data-ttu-id="249b8-124">值</span><span class="sxs-lookup"><span data-stu-id="249b8-124">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="249b8-125">DataType</span><span class="sxs-lookup"><span data-stu-id="249b8-125">DataType</span></span><br/>     | <span data-ttu-id="249b8-126">字串</span><span class="sxs-lookup"><span data-stu-id="249b8-126">string</span></span><br/>  | <span data-ttu-id="249b8-127">xs:integer</span><span class="sxs-lookup"><span data-stu-id="249b8-127">xs:integer</span></span><br/>      |
| <span data-ttu-id="249b8-128">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="249b8-128">DefaultValue</span></span><br/> | <span data-ttu-id="249b8-129">整數</span><span class="sxs-lookup"><span data-stu-id="249b8-129">integer</span></span><br/> | <span data-ttu-id="249b8-130">未定義</span><span class="sxs-lookup"><span data-stu-id="249b8-130">undefined</span></span><br/>       |
| <span data-ttu-id="249b8-131">MaxValue</span><span class="sxs-lookup"><span data-stu-id="249b8-131">MaxValue</span></span><br/>     | <span data-ttu-id="249b8-132">整數</span><span class="sxs-lookup"><span data-stu-id="249b8-132">integer</span></span><br/> | <span data-ttu-id="249b8-133">未定義</span><span class="sxs-lookup"><span data-stu-id="249b8-133">undefined</span></span><br/>       |
| <span data-ttu-id="249b8-134">MinValue</span><span class="sxs-lookup"><span data-stu-id="249b8-134">MinValue</span></span><br/>     | <span data-ttu-id="249b8-135">整數</span><span class="sxs-lookup"><span data-stu-id="249b8-135">integer</span></span><br/> | <span data-ttu-id="249b8-136">未定義</span><span class="sxs-lookup"><span data-stu-id="249b8-136">undefined</span></span><br/>       |
| <span data-ttu-id="249b8-137">強制性</span><span class="sxs-lookup"><span data-stu-id="249b8-137">Mandatory</span></span><br/>    | <span data-ttu-id="249b8-138">字串</span><span class="sxs-lookup"><span data-stu-id="249b8-138">string</span></span><br/>  | <span data-ttu-id="249b8-139">psk：條件式</span><span class="sxs-lookup"><span data-stu-id="249b8-139">psk:Conditional</span></span><br/> |
| <span data-ttu-id="249b8-140">多個</span><span class="sxs-lookup"><span data-stu-id="249b8-140">Multiple</span></span><br/>     | <span data-ttu-id="249b8-141">整數</span><span class="sxs-lookup"><span data-stu-id="249b8-141">integer</span></span><br/> | <span data-ttu-id="249b8-142">1</span><span class="sxs-lookup"><span data-stu-id="249b8-142">1</span></span><br/>               |
| <span data-ttu-id="249b8-143">Unittype.pixel 表示</span><span class="sxs-lookup"><span data-stu-id="249b8-143">UnitType</span></span><br/>     | <span data-ttu-id="249b8-144">字串</span><span class="sxs-lookup"><span data-stu-id="249b8-144">string</span></span><br/>  | <span data-ttu-id="249b8-145">微米</span><span class="sxs-lookup"><span data-stu-id="249b8-145">microns</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="249b8-146">相關主題</span><span class="sxs-lookup"><span data-stu-id="249b8-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="249b8-147">PostScript 印表機描述檔案格式規格</span><span class="sxs-lookup"><span data-stu-id="249b8-147">PostScript Printer Description File Format Specification</span></span>](https://www.adobe.com/products/postscript/pdfs/PLRM.pdf)
</dt> <dt>

[<span data-ttu-id="249b8-148">列印架構規格</span><span class="sxs-lookup"><span data-stu-id="249b8-148">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




