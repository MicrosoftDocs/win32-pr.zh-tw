---
description: 本主題並非最新的。 如需最新資訊，請參閱列印架構規格。
ms.assetid: b091c250-66f2-47cc-a012-1526c0ed02c9
title: PageMediaSizePSOrientation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d16a9a2e59ebffb41ad7c9a9c16eaf41497ade62
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/26/2021
ms.locfileid: "107997555"
---
# <a name="pagemediasizepsorientation"></a><span data-ttu-id="79541-104">PageMediaSizePSOrientation</span><span class="sxs-lookup"><span data-stu-id="79541-104">PageMediaSizePSOrientation</span></span>

<span data-ttu-id="79541-105">本主題並非最新的。</span><span class="sxs-lookup"><span data-stu-id="79541-105">This topic is not current.</span></span> <span data-ttu-id="79541-106">如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。</span><span class="sxs-lookup"><span data-stu-id="79541-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="79541-107">指定相對於饋送方向方向的方向 (參考 [PostScript 印表機描述檔案格式規格](https://www.adobe.com/products/postscript/pdfs/PLRM.pdf)) 。</span><span class="sxs-lookup"><span data-stu-id="79541-107">Specifies the orientation relative to the feed-orientation direction (Reference [PostScript Printer Description File Format Specification](https://www.adobe.com/products/postscript/pdfs/PLRM.pdf)).</span></span>

-   [<span data-ttu-id="79541-108">項目資訊</span><span class="sxs-lookup"><span data-stu-id="79541-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="79541-109">結構內容</span><span class="sxs-lookup"><span data-stu-id="79541-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="79541-110">項目資訊</span><span class="sxs-lookup"><span data-stu-id="79541-110">Element Information</span></span>



| <span data-ttu-id="79541-111">Name</span><span class="sxs-lookup"><span data-stu-id="79541-111">Name</span></span> | <span data-ttu-id="79541-112">值</span><span class="sxs-lookup"><span data-stu-id="79541-112">Value</span></span> |
|----------------------------|-------------------------------------------------------------|
| <span data-ttu-id="79541-113">項目類型</span><span class="sxs-lookup"><span data-stu-id="79541-113">Element Type</span></span> <br/>   | <span data-ttu-id="79541-114">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="79541-114">ParameterDef</span></span><br/>                                     |
| <span data-ttu-id="79541-115">範圍前置詞</span><span class="sxs-lookup"><span data-stu-id="79541-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="79541-116">頁面</span><span class="sxs-lookup"><span data-stu-id="79541-116">Page</span></span><br/>                                             |
| <span data-ttu-id="79541-117">備註</span><span class="sxs-lookup"><span data-stu-id="79541-117">Notes</span></span> <br/>          | <span data-ttu-id="79541-118">連結至 PageMediaSize 元素，CustomPS 選項</span><span class="sxs-lookup"><span data-stu-id="79541-118">Linked to PageMediaSize element, CustomPS option</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="79541-119">結構內容</span><span class="sxs-lookup"><span data-stu-id="79541-119">Structure Content</span></span>

<span data-ttu-id="79541-120">此元素的 XML 結構為：</span><span class="sxs-lookup"><span data-stu-id="79541-120">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="79541-121">結構屬性</span><span class="sxs-lookup"><span data-stu-id="79541-121">Structure Properties</span></span>

<span data-ttu-id="79541-122">下表概述 XML 結構中所定義之變數的特性。</span><span class="sxs-lookup"><span data-stu-id="79541-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="79541-123">屬性</span><span class="sxs-lookup"><span data-stu-id="79541-123">Property</span></span>                | <span data-ttu-id="79541-124">xsi:type</span><span class="sxs-lookup"><span data-stu-id="79541-124">xsi:type</span></span>           | <span data-ttu-id="79541-125">值</span><span class="sxs-lookup"><span data-stu-id="79541-125">Value</span></span>                        |
|-------------------------|--------------------|------------------------------|
| <span data-ttu-id="79541-126">DataType</span><span class="sxs-lookup"><span data-stu-id="79541-126">DataType</span></span><br/>     | <span data-ttu-id="79541-127">字串</span><span class="sxs-lookup"><span data-stu-id="79541-127">string</span></span><br/>  | <span data-ttu-id="79541-128">xs:integer</span><span class="sxs-lookup"><span data-stu-id="79541-128">xs:integer</span></span><br/>        |
| <span data-ttu-id="79541-129">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="79541-129">DefaultValue</span></span><br/> | <span data-ttu-id="79541-130">整數</span><span class="sxs-lookup"><span data-stu-id="79541-130">integer</span></span><br/> | <span data-ttu-id="79541-131">0</span><span class="sxs-lookup"><span data-stu-id="79541-131">0</span></span><br/>                 |
| <span data-ttu-id="79541-132">MaxValue</span><span class="sxs-lookup"><span data-stu-id="79541-132">MaxValue</span></span><br/>     | <span data-ttu-id="79541-133">整數</span><span class="sxs-lookup"><span data-stu-id="79541-133">integer</span></span><br/> | <span data-ttu-id="79541-134">3</span><span class="sxs-lookup"><span data-stu-id="79541-134">3</span></span><br/>                 |
| <span data-ttu-id="79541-135">MinValue</span><span class="sxs-lookup"><span data-stu-id="79541-135">MinValue</span></span><br/>     | <span data-ttu-id="79541-136">整數</span><span class="sxs-lookup"><span data-stu-id="79541-136">integer</span></span><br/> | <span data-ttu-id="79541-137">0</span><span class="sxs-lookup"><span data-stu-id="79541-137">0</span></span><br/>                 |
| <span data-ttu-id="79541-138">強制性</span><span class="sxs-lookup"><span data-stu-id="79541-138">Mandatory</span></span><br/>    | <span data-ttu-id="79541-139">字串</span><span class="sxs-lookup"><span data-stu-id="79541-139">string</span></span><br/>  | <span data-ttu-id="79541-140">psk：條件式</span><span class="sxs-lookup"><span data-stu-id="79541-140">psk:Conditional</span></span><br/>   |
| <span data-ttu-id="79541-141">多個</span><span class="sxs-lookup"><span data-stu-id="79541-141">Multiple</span></span><br/>     | <span data-ttu-id="79541-142">整數</span><span class="sxs-lookup"><span data-stu-id="79541-142">integer</span></span><br/> | <span data-ttu-id="79541-143">1</span><span class="sxs-lookup"><span data-stu-id="79541-143">1</span></span><br/>                 |
| <span data-ttu-id="79541-144">Unittype.pixel 表示</span><span class="sxs-lookup"><span data-stu-id="79541-144">UnitType</span></span><br/>     | <span data-ttu-id="79541-145">字串</span><span class="sxs-lookup"><span data-stu-id="79541-145">string</span></span><br/>  | <span data-ttu-id="79541-146">PageMediaSizeEnum</span><span class="sxs-lookup"><span data-stu-id="79541-146">PageMediaSizeEnum</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="79541-147">相關主題</span><span class="sxs-lookup"><span data-stu-id="79541-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="79541-148">PostScript 印表機描述檔案格式規格</span><span class="sxs-lookup"><span data-stu-id="79541-148">PostScript Printer Description File Format Specification</span></span>](https://www.adobe.com/products/postscript/pdfs/PLRM.pdf)
</dt> <dt>

[<span data-ttu-id="79541-149">列印架構規格</span><span class="sxs-lookup"><span data-stu-id="79541-149">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




