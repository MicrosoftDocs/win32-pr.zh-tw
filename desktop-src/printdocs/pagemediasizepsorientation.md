---
description: 本主題並非最新的。 如需最新資訊，請參閱列印架構規格。
ms.assetid: b091c250-66f2-47cc-a012-1526c0ed02c9
title: PageMediaSizePSOrientation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a188c61d3bb3c47286b887406174a3fc41f3c58a
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/05/2021
ms.locfileid: "106988113"
---
# <a name="pagemediasizepsorientation"></a><span data-ttu-id="c4e4d-104">PageMediaSizePSOrientation</span><span class="sxs-lookup"><span data-stu-id="c4e4d-104">PageMediaSizePSOrientation</span></span>

<span data-ttu-id="c4e4d-105">本主題並非最新的。</span><span class="sxs-lookup"><span data-stu-id="c4e4d-105">This topic is not current.</span></span> <span data-ttu-id="c4e4d-106">如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。</span><span class="sxs-lookup"><span data-stu-id="c4e4d-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="c4e4d-107">指定相對於饋送方向方向的方向 (參考 [PostScript 印表機描述檔案格式規格](https://www.adobe.com/products/postscript/pdfs/PLRM.pdf)) 。</span><span class="sxs-lookup"><span data-stu-id="c4e4d-107">Specifies the orientation relative to the feed-orientation direction (Reference [PostScript Printer Description File Format Specification](https://www.adobe.com/products/postscript/pdfs/PLRM.pdf)).</span></span>

-   [<span data-ttu-id="c4e4d-108">項目資訊</span><span class="sxs-lookup"><span data-stu-id="c4e4d-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="c4e4d-109">結構內容</span><span class="sxs-lookup"><span data-stu-id="c4e4d-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="c4e4d-110">項目資訊</span><span class="sxs-lookup"><span data-stu-id="c4e4d-110">Element Information</span></span>



| <span data-ttu-id="c4e4d-111">Name</span><span class="sxs-lookup"><span data-stu-id="c4e4d-111">Name</span></span>                       |                                                             |
|----------------------------|-------------------------------------------------------------|
| <span data-ttu-id="c4e4d-112">項目類型</span><span class="sxs-lookup"><span data-stu-id="c4e4d-112">Element Type</span></span> <br/>   | <span data-ttu-id="c4e4d-113">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="c4e4d-113">ParameterDef</span></span><br/>                                     |
| <span data-ttu-id="c4e4d-114">範圍前置詞</span><span class="sxs-lookup"><span data-stu-id="c4e4d-114">Scoping Prefix</span></span> <br/> | <span data-ttu-id="c4e4d-115">頁面</span><span class="sxs-lookup"><span data-stu-id="c4e4d-115">Page</span></span><br/>                                             |
| <span data-ttu-id="c4e4d-116">備註</span><span class="sxs-lookup"><span data-stu-id="c4e4d-116">Notes</span></span> <br/>          | <span data-ttu-id="c4e4d-117">連結至 PageMediaSize 元素，CustomPS 選項</span><span class="sxs-lookup"><span data-stu-id="c4e4d-117">Linked to PageMediaSize element, CustomPS option</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="c4e4d-118">結構內容</span><span class="sxs-lookup"><span data-stu-id="c4e4d-118">Structure Content</span></span>

<span data-ttu-id="c4e4d-119">此元素的 XML 結構為：</span><span class="sxs-lookup"><span data-stu-id="c4e4d-119">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageMediaSizePSOrientation">
  <psf:Property name="psf:DataType">
    <psf:Value xsi:type="xs:string">xs:integer</psf:Value>
  </psf:Property>
  <psf:Property name="psf:DefaultValue">
    <psf:Value xsi:type="xs:integer">0</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MaxValue">
    <psf:Value xsi:type="xs:integer">3</psf:Value>
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
    <psf:Value xsi:type="xs:string">PageMediaSizeEnum</psf:Value>
  </psf:Property>
</psf:ParameterDef>
      
```

## <a name="structure-properties"></a><span data-ttu-id="c4e4d-120">結構屬性</span><span class="sxs-lookup"><span data-stu-id="c4e4d-120">Structure Properties</span></span>

<span data-ttu-id="c4e4d-121">下表概述 XML 結構中所定義之變數的特性。</span><span class="sxs-lookup"><span data-stu-id="c4e4d-121">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="c4e4d-122">屬性</span><span class="sxs-lookup"><span data-stu-id="c4e4d-122">Property</span></span>                | <span data-ttu-id="c4e4d-123">xsi:type</span><span class="sxs-lookup"><span data-stu-id="c4e4d-123">xsi:type</span></span>           | <span data-ttu-id="c4e4d-124">值</span><span class="sxs-lookup"><span data-stu-id="c4e4d-124">Value</span></span>                        |
|-------------------------|--------------------|------------------------------|
| <span data-ttu-id="c4e4d-125">DataType</span><span class="sxs-lookup"><span data-stu-id="c4e4d-125">DataType</span></span><br/>     | <span data-ttu-id="c4e4d-126">字串</span><span class="sxs-lookup"><span data-stu-id="c4e4d-126">string</span></span><br/>  | <span data-ttu-id="c4e4d-127">xs:integer</span><span class="sxs-lookup"><span data-stu-id="c4e4d-127">xs:integer</span></span><br/>        |
| <span data-ttu-id="c4e4d-128">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="c4e4d-128">DefaultValue</span></span><br/> | <span data-ttu-id="c4e4d-129">整數</span><span class="sxs-lookup"><span data-stu-id="c4e4d-129">integer</span></span><br/> | <span data-ttu-id="c4e4d-130">0</span><span class="sxs-lookup"><span data-stu-id="c4e4d-130">0</span></span><br/>                 |
| <span data-ttu-id="c4e4d-131">MaxValue</span><span class="sxs-lookup"><span data-stu-id="c4e4d-131">MaxValue</span></span><br/>     | <span data-ttu-id="c4e4d-132">整數</span><span class="sxs-lookup"><span data-stu-id="c4e4d-132">integer</span></span><br/> | <span data-ttu-id="c4e4d-133">3</span><span class="sxs-lookup"><span data-stu-id="c4e4d-133">3</span></span><br/>                 |
| <span data-ttu-id="c4e4d-134">MinValue</span><span class="sxs-lookup"><span data-stu-id="c4e4d-134">MinValue</span></span><br/>     | <span data-ttu-id="c4e4d-135">整數</span><span class="sxs-lookup"><span data-stu-id="c4e4d-135">integer</span></span><br/> | <span data-ttu-id="c4e4d-136">0</span><span class="sxs-lookup"><span data-stu-id="c4e4d-136">0</span></span><br/>                 |
| <span data-ttu-id="c4e4d-137">強制性</span><span class="sxs-lookup"><span data-stu-id="c4e4d-137">Mandatory</span></span><br/>    | <span data-ttu-id="c4e4d-138">字串</span><span class="sxs-lookup"><span data-stu-id="c4e4d-138">string</span></span><br/>  | <span data-ttu-id="c4e4d-139">psk：條件式</span><span class="sxs-lookup"><span data-stu-id="c4e4d-139">psk:Conditional</span></span><br/>   |
| <span data-ttu-id="c4e4d-140">多個</span><span class="sxs-lookup"><span data-stu-id="c4e4d-140">Multiple</span></span><br/>     | <span data-ttu-id="c4e4d-141">整數</span><span class="sxs-lookup"><span data-stu-id="c4e4d-141">integer</span></span><br/> | <span data-ttu-id="c4e4d-142">1</span><span class="sxs-lookup"><span data-stu-id="c4e4d-142">1</span></span><br/>                 |
| <span data-ttu-id="c4e4d-143">Unittype.pixel 表示</span><span class="sxs-lookup"><span data-stu-id="c4e4d-143">UnitType</span></span><br/>     | <span data-ttu-id="c4e4d-144">字串</span><span class="sxs-lookup"><span data-stu-id="c4e4d-144">string</span></span><br/>  | <span data-ttu-id="c4e4d-145">PageMediaSizeEnum</span><span class="sxs-lookup"><span data-stu-id="c4e4d-145">PageMediaSizeEnum</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="c4e4d-146">相關主題</span><span class="sxs-lookup"><span data-stu-id="c4e4d-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c4e4d-147">PostScript 印表機描述檔案格式規格</span><span class="sxs-lookup"><span data-stu-id="c4e4d-147">PostScript Printer Description File Format Specification</span></span>](https://www.adobe.com/products/postscript/pdfs/PLRM.pdf)
</dt> <dt>

[<span data-ttu-id="c4e4d-148">列印架構規格</span><span class="sxs-lookup"><span data-stu-id="c4e4d-148">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




