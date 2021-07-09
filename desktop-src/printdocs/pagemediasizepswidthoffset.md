---
description: 取得 PageMediaSizePSWidthOffset 參數的相關資訊。 本主題並非最新的。 如需最新資訊，請參閱列印架構規格。
ms.assetid: b93ad6e6-ab27-4fab-b488-6f402b6ee857
title: PageMediaSizePSWidthOffset
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 265acad803dbc334be115440e195967465b3ef50
ms.sourcegitcommit: 998d50f6def8a25850fc113fc8a2df903c829c5e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/09/2021
ms.locfileid: "113549096"
---
# <a name="pagemediasizepswidthoffset"></a><span data-ttu-id="56929-105">PageMediaSizePSWidthOffset</span><span class="sxs-lookup"><span data-stu-id="56929-105">PageMediaSizePSWidthOffset</span></span>

<span data-ttu-id="56929-106">本主題並非最新的。</span><span class="sxs-lookup"><span data-stu-id="56929-106">This topic is not current.</span></span> <span data-ttu-id="56929-107">如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。</span><span class="sxs-lookup"><span data-stu-id="56929-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="56929-108">指定相對於饋送方向方向的位移 (參考[PostScript 印表機描述檔案格式規格](https://www.adobe.com/products/postscript/pdfs/PLRM.pdf)) 。</span><span class="sxs-lookup"><span data-stu-id="56929-108">Specifies the offset perpendicular to the feed-orientation direction (Reference [PostScript Printer Description File Format Specification](https://www.adobe.com/products/postscript/pdfs/PLRM.pdf)).</span></span>

-   [<span data-ttu-id="56929-109">項目資訊</span><span class="sxs-lookup"><span data-stu-id="56929-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="56929-110">結構內容</span><span class="sxs-lookup"><span data-stu-id="56929-110">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="56929-111">項目資訊</span><span class="sxs-lookup"><span data-stu-id="56929-111">Element Information</span></span>



| <span data-ttu-id="56929-112">Name</span><span class="sxs-lookup"><span data-stu-id="56929-112">Name</span></span> | <span data-ttu-id="56929-113">值</span><span class="sxs-lookup"><span data-stu-id="56929-113">Value</span></span> |
|----------------------------|-------------------------------------------------------------|
| <span data-ttu-id="56929-114">項目類型</span><span class="sxs-lookup"><span data-stu-id="56929-114">Element Type</span></span> <br/>   | <span data-ttu-id="56929-115">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="56929-115">ParameterDef</span></span><br/>                                     |
| <span data-ttu-id="56929-116">範圍前置詞</span><span class="sxs-lookup"><span data-stu-id="56929-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="56929-117">頁面</span><span class="sxs-lookup"><span data-stu-id="56929-117">Page</span></span><br/>                                             |
| <span data-ttu-id="56929-118">備註</span><span class="sxs-lookup"><span data-stu-id="56929-118">Notes</span></span> <br/>          | <span data-ttu-id="56929-119">連結至 PageMediaSize 元素，CustomPS 選項</span><span class="sxs-lookup"><span data-stu-id="56929-119">Linked to PageMediaSize element, CustomPS option</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="56929-120">結構內容</span><span class="sxs-lookup"><span data-stu-id="56929-120">Structure Content</span></span>

<span data-ttu-id="56929-121">此元素的 XML 結構為：</span><span class="sxs-lookup"><span data-stu-id="56929-121">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="56929-122">結構屬性</span><span class="sxs-lookup"><span data-stu-id="56929-122">Structure Properties</span></span>

<span data-ttu-id="56929-123">下表概述 XML 結構中所定義之變數的特性。</span><span class="sxs-lookup"><span data-stu-id="56929-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="56929-124">屬性</span><span class="sxs-lookup"><span data-stu-id="56929-124">Property</span></span>                | <span data-ttu-id="56929-125">xsi:type</span><span class="sxs-lookup"><span data-stu-id="56929-125">xsi:type</span></span>           | <span data-ttu-id="56929-126">值</span><span class="sxs-lookup"><span data-stu-id="56929-126">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="56929-127">DataType</span><span class="sxs-lookup"><span data-stu-id="56929-127">DataType</span></span><br/>     | <span data-ttu-id="56929-128">字串</span><span class="sxs-lookup"><span data-stu-id="56929-128">string</span></span><br/>  | <span data-ttu-id="56929-129">xs:integer</span><span class="sxs-lookup"><span data-stu-id="56929-129">xs:integer</span></span><br/>      |
| <span data-ttu-id="56929-130">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="56929-130">DefaultValue</span></span><br/> | <span data-ttu-id="56929-131">整數</span><span class="sxs-lookup"><span data-stu-id="56929-131">integer</span></span><br/> | <span data-ttu-id="56929-132">未定義</span><span class="sxs-lookup"><span data-stu-id="56929-132">undefined</span></span><br/>       |
| <span data-ttu-id="56929-133">MaxValue</span><span class="sxs-lookup"><span data-stu-id="56929-133">MaxValue</span></span><br/>     | <span data-ttu-id="56929-134">整數</span><span class="sxs-lookup"><span data-stu-id="56929-134">integer</span></span><br/> | <span data-ttu-id="56929-135">未定義</span><span class="sxs-lookup"><span data-stu-id="56929-135">undefined</span></span><br/>       |
| <span data-ttu-id="56929-136">MinValue</span><span class="sxs-lookup"><span data-stu-id="56929-136">MinValue</span></span><br/>     | <span data-ttu-id="56929-137">整數</span><span class="sxs-lookup"><span data-stu-id="56929-137">integer</span></span><br/> | <span data-ttu-id="56929-138">未定義</span><span class="sxs-lookup"><span data-stu-id="56929-138">undefined</span></span><br/>       |
| <span data-ttu-id="56929-139">強制性</span><span class="sxs-lookup"><span data-stu-id="56929-139">Mandatory</span></span><br/>    | <span data-ttu-id="56929-140">string</span><span class="sxs-lookup"><span data-stu-id="56929-140">string</span></span><br/>  | <span data-ttu-id="56929-141">psk：條件式</span><span class="sxs-lookup"><span data-stu-id="56929-141">psk:Conditional</span></span><br/> |
| <span data-ttu-id="56929-142">多個</span><span class="sxs-lookup"><span data-stu-id="56929-142">Multiple</span></span><br/>     | <span data-ttu-id="56929-143">整數</span><span class="sxs-lookup"><span data-stu-id="56929-143">integer</span></span><br/> | <span data-ttu-id="56929-144">1</span><span class="sxs-lookup"><span data-stu-id="56929-144">1</span></span><br/>               |
| <span data-ttu-id="56929-145">Unittype.pixel 表示</span><span class="sxs-lookup"><span data-stu-id="56929-145">UnitType</span></span><br/>     | <span data-ttu-id="56929-146">string</span><span class="sxs-lookup"><span data-stu-id="56929-146">string</span></span><br/>  | <span data-ttu-id="56929-147">微米</span><span class="sxs-lookup"><span data-stu-id="56929-147">microns</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="56929-148">相關主題</span><span class="sxs-lookup"><span data-stu-id="56929-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="56929-149">PostScript印表機描述檔案格式規格</span><span class="sxs-lookup"><span data-stu-id="56929-149">PostScript Printer Description File Format Specification</span></span>](https://www.adobe.com/products/postscript/pdfs/PLRM.pdf)
</dt> <dt>

[<span data-ttu-id="56929-150">列印架構規格</span><span class="sxs-lookup"><span data-stu-id="56929-150">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




