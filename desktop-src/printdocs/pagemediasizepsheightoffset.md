---
description: 本主題並非最新的。 如需最新資訊，請參閱列印架構規格。
ms.assetid: e86d6a5d-484d-4c80-8c86-7d12d287ee21
title: PageMediaSizePSHeightOffset
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e02129d5c8c20fceef01a9cd5cf40e5827374a7
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/05/2021
ms.locfileid: "106992238"
---
# <a name="pagemediasizepsheightoffset"></a><span data-ttu-id="fe783-104">PageMediaSizePSHeightOffset</span><span class="sxs-lookup"><span data-stu-id="fe783-104">PageMediaSizePSHeightOffset</span></span>

<span data-ttu-id="fe783-105">本主題並非最新的。</span><span class="sxs-lookup"><span data-stu-id="fe783-105">This topic is not current.</span></span> <span data-ttu-id="fe783-106">如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。</span><span class="sxs-lookup"><span data-stu-id="fe783-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="fe783-107">指定位移，與饋送方向方向 (參考 [PostScript 印表機描述檔案格式規格](https://www.adobe.com/products/postscript/pdfs/PLRM.pdf)) 。</span><span class="sxs-lookup"><span data-stu-id="fe783-107">Specifies the offset, parallel to the feed-orientation direction (Reference [PostScript Printer Description File Format Specification](https://www.adobe.com/products/postscript/pdfs/PLRM.pdf)).</span></span>

-   [<span data-ttu-id="fe783-108">項目資訊</span><span class="sxs-lookup"><span data-stu-id="fe783-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="fe783-109">結構內容</span><span class="sxs-lookup"><span data-stu-id="fe783-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="fe783-110">項目資訊</span><span class="sxs-lookup"><span data-stu-id="fe783-110">Element Information</span></span>



| <span data-ttu-id="fe783-111">Name</span><span class="sxs-lookup"><span data-stu-id="fe783-111">Name</span></span>                       |                                                             |
|----------------------------|-------------------------------------------------------------|
| <span data-ttu-id="fe783-112">項目類型</span><span class="sxs-lookup"><span data-stu-id="fe783-112">Element Type</span></span> <br/>   | <span data-ttu-id="fe783-113">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="fe783-113">ParameterDef</span></span><br/>                                     |
| <span data-ttu-id="fe783-114">範圍前置詞</span><span class="sxs-lookup"><span data-stu-id="fe783-114">Scoping Prefix</span></span> <br/> | <span data-ttu-id="fe783-115">頁面</span><span class="sxs-lookup"><span data-stu-id="fe783-115">Page</span></span><br/>                                             |
| <span data-ttu-id="fe783-116">備註</span><span class="sxs-lookup"><span data-stu-id="fe783-116">Notes</span></span> <br/>          | <span data-ttu-id="fe783-117">連結至 PageMediaSize 元素，CustomPS 選項</span><span class="sxs-lookup"><span data-stu-id="fe783-117">Linked to PageMediaSize element, CustomPS option</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="fe783-118">結構內容</span><span class="sxs-lookup"><span data-stu-id="fe783-118">Structure Content</span></span>

<span data-ttu-id="fe783-119">此元素的 XML 結構為：</span><span class="sxs-lookup"><span data-stu-id="fe783-119">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageMediaSizePSHeightOffset">
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

## <a name="structure-properties"></a><span data-ttu-id="fe783-120">結構屬性</span><span class="sxs-lookup"><span data-stu-id="fe783-120">Structure Properties</span></span>

<span data-ttu-id="fe783-121">下表概述 XML 結構中所定義之變數的特性。</span><span class="sxs-lookup"><span data-stu-id="fe783-121">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="fe783-122">屬性</span><span class="sxs-lookup"><span data-stu-id="fe783-122">Property</span></span>                | <span data-ttu-id="fe783-123">xsi:type</span><span class="sxs-lookup"><span data-stu-id="fe783-123">xsi:type</span></span>           | <span data-ttu-id="fe783-124">值</span><span class="sxs-lookup"><span data-stu-id="fe783-124">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="fe783-125">DataType</span><span class="sxs-lookup"><span data-stu-id="fe783-125">DataType</span></span><br/>     | <span data-ttu-id="fe783-126">字串</span><span class="sxs-lookup"><span data-stu-id="fe783-126">string</span></span><br/>  | <span data-ttu-id="fe783-127">xs:integer</span><span class="sxs-lookup"><span data-stu-id="fe783-127">xs:integer</span></span><br/>      |
| <span data-ttu-id="fe783-128">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="fe783-128">DefaultValue</span></span><br/> | <span data-ttu-id="fe783-129">整數</span><span class="sxs-lookup"><span data-stu-id="fe783-129">integer</span></span><br/> | <span data-ttu-id="fe783-130">未定義</span><span class="sxs-lookup"><span data-stu-id="fe783-130">undefined</span></span><br/>       |
| <span data-ttu-id="fe783-131">MaxValue</span><span class="sxs-lookup"><span data-stu-id="fe783-131">MaxValue</span></span><br/>     | <span data-ttu-id="fe783-132">整數</span><span class="sxs-lookup"><span data-stu-id="fe783-132">integer</span></span><br/> | <span data-ttu-id="fe783-133">未定義</span><span class="sxs-lookup"><span data-stu-id="fe783-133">undefined</span></span><br/>       |
| <span data-ttu-id="fe783-134">MinValue</span><span class="sxs-lookup"><span data-stu-id="fe783-134">MinValue</span></span><br/>     | <span data-ttu-id="fe783-135">整數</span><span class="sxs-lookup"><span data-stu-id="fe783-135">integer</span></span><br/> | <span data-ttu-id="fe783-136">未定義</span><span class="sxs-lookup"><span data-stu-id="fe783-136">undefined</span></span><br/>       |
| <span data-ttu-id="fe783-137">強制性</span><span class="sxs-lookup"><span data-stu-id="fe783-137">Mandatory</span></span><br/>    | <span data-ttu-id="fe783-138">字串</span><span class="sxs-lookup"><span data-stu-id="fe783-138">string</span></span><br/>  | <span data-ttu-id="fe783-139">psk：條件式</span><span class="sxs-lookup"><span data-stu-id="fe783-139">psk:Conditional</span></span><br/> |
| <span data-ttu-id="fe783-140">多個</span><span class="sxs-lookup"><span data-stu-id="fe783-140">Multiple</span></span><br/>     | <span data-ttu-id="fe783-141">整數</span><span class="sxs-lookup"><span data-stu-id="fe783-141">integer</span></span><br/> | <span data-ttu-id="fe783-142">1</span><span class="sxs-lookup"><span data-stu-id="fe783-142">1</span></span><br/>               |
| <span data-ttu-id="fe783-143">Unittype.pixel 表示</span><span class="sxs-lookup"><span data-stu-id="fe783-143">UnitType</span></span><br/>     | <span data-ttu-id="fe783-144">字串</span><span class="sxs-lookup"><span data-stu-id="fe783-144">string</span></span><br/>  | <span data-ttu-id="fe783-145">微米</span><span class="sxs-lookup"><span data-stu-id="fe783-145">microns</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="fe783-146">相關主題</span><span class="sxs-lookup"><span data-stu-id="fe783-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fe783-147">PostScript 印表機描述檔案格式規格</span><span class="sxs-lookup"><span data-stu-id="fe783-147">PostScript Printer Description File Format Specification</span></span>](https://www.adobe.com/products/postscript/pdfs/PLRM.pdf)
</dt> <dt>

[<span data-ttu-id="fe783-148">列印架構規格</span><span class="sxs-lookup"><span data-stu-id="fe783-148">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




