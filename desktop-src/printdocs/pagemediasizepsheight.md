---
description: 本主題並非最新的。 如需最新資訊，請參閱列印架構規格。
ms.assetid: 857caf51-ccf6-415c-aab3-1fed50fa7b34
title: PageMediaSizePSHeight
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96c6ddd593d95ae740a5e03d37e3d79c73e1638b
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/26/2021
ms.locfileid: "107993695"
---
# <a name="pagemediasizepsheight"></a><span data-ttu-id="e5451-104">PageMediaSizePSHeight</span><span class="sxs-lookup"><span data-stu-id="e5451-104">PageMediaSizePSHeight</span></span>

<span data-ttu-id="e5451-105">本主題並非最新的。</span><span class="sxs-lookup"><span data-stu-id="e5451-105">This topic is not current.</span></span> <span data-ttu-id="e5451-106">如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。</span><span class="sxs-lookup"><span data-stu-id="e5451-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="e5451-107">指定頁面的高度，與饋送方向方向 (參考 [PostScript 印表機描述檔案格式規格](https://www.adobe.com/products/postscript/pdfs/PLRM.pdf)) 。</span><span class="sxs-lookup"><span data-stu-id="e5451-107">Specifies the height of the page, parallel to the feed-orientation direction (Reference [PostScript Printer Description File Format Specification](https://www.adobe.com/products/postscript/pdfs/PLRM.pdf)).</span></span>

-   [<span data-ttu-id="e5451-108">項目資訊</span><span class="sxs-lookup"><span data-stu-id="e5451-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="e5451-109">結構內容</span><span class="sxs-lookup"><span data-stu-id="e5451-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="e5451-110">項目資訊</span><span class="sxs-lookup"><span data-stu-id="e5451-110">Element Information</span></span>



| <span data-ttu-id="e5451-111">Name</span><span class="sxs-lookup"><span data-stu-id="e5451-111">Name</span></span> | <span data-ttu-id="e5451-112">值</span><span class="sxs-lookup"><span data-stu-id="e5451-112">Value</span></span> |
|----------------------------|-------------------------------------------------------------|
| <span data-ttu-id="e5451-113">項目類型</span><span class="sxs-lookup"><span data-stu-id="e5451-113">Element Type</span></span> <br/>   | <span data-ttu-id="e5451-114">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="e5451-114">ParameterDef</span></span><br/>                                     |
| <span data-ttu-id="e5451-115">範圍前置詞</span><span class="sxs-lookup"><span data-stu-id="e5451-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="e5451-116">頁面</span><span class="sxs-lookup"><span data-stu-id="e5451-116">Page</span></span><br/>                                             |
| <span data-ttu-id="e5451-117">備註</span><span class="sxs-lookup"><span data-stu-id="e5451-117">Notes</span></span> <br/>          | <span data-ttu-id="e5451-118">連結至 PageMediaSize 元素，CustomPS 選項</span><span class="sxs-lookup"><span data-stu-id="e5451-118">Linked to PageMediaSize element, CustomPS option</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="e5451-119">結構內容</span><span class="sxs-lookup"><span data-stu-id="e5451-119">Structure Content</span></span>

<span data-ttu-id="e5451-120">此元素的 XML 結構為：</span><span class="sxs-lookup"><span data-stu-id="e5451-120">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageMediaSizePSHeight">
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

## <a name="structure-properties"></a><span data-ttu-id="e5451-121">結構屬性</span><span class="sxs-lookup"><span data-stu-id="e5451-121">Structure Properties</span></span>

<span data-ttu-id="e5451-122">下表概述 XML 結構中所定義之變數的特性。</span><span class="sxs-lookup"><span data-stu-id="e5451-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="e5451-123">屬性</span><span class="sxs-lookup"><span data-stu-id="e5451-123">Property</span></span>                | <span data-ttu-id="e5451-124">xsi:type</span><span class="sxs-lookup"><span data-stu-id="e5451-124">xsi:type</span></span>           | <span data-ttu-id="e5451-125">值</span><span class="sxs-lookup"><span data-stu-id="e5451-125">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="e5451-126">DataType</span><span class="sxs-lookup"><span data-stu-id="e5451-126">DataType</span></span><br/>     | <span data-ttu-id="e5451-127">字串</span><span class="sxs-lookup"><span data-stu-id="e5451-127">string</span></span><br/>  | <span data-ttu-id="e5451-128">xs:integer</span><span class="sxs-lookup"><span data-stu-id="e5451-128">xs:integer</span></span><br/>      |
| <span data-ttu-id="e5451-129">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="e5451-129">DefaultValue</span></span><br/> | <span data-ttu-id="e5451-130">整數</span><span class="sxs-lookup"><span data-stu-id="e5451-130">integer</span></span><br/> | <span data-ttu-id="e5451-131">未定義</span><span class="sxs-lookup"><span data-stu-id="e5451-131">undefined</span></span><br/>       |
| <span data-ttu-id="e5451-132">MaxValue</span><span class="sxs-lookup"><span data-stu-id="e5451-132">MaxValue</span></span><br/>     | <span data-ttu-id="e5451-133">整數</span><span class="sxs-lookup"><span data-stu-id="e5451-133">integer</span></span><br/> | <span data-ttu-id="e5451-134">未定義</span><span class="sxs-lookup"><span data-stu-id="e5451-134">undefined</span></span><br/>       |
| <span data-ttu-id="e5451-135">MinValue</span><span class="sxs-lookup"><span data-stu-id="e5451-135">MinValue</span></span><br/>     | <span data-ttu-id="e5451-136">整數</span><span class="sxs-lookup"><span data-stu-id="e5451-136">integer</span></span><br/> | <span data-ttu-id="e5451-137">未定義</span><span class="sxs-lookup"><span data-stu-id="e5451-137">undefined</span></span><br/>       |
| <span data-ttu-id="e5451-138">強制性</span><span class="sxs-lookup"><span data-stu-id="e5451-138">Mandatory</span></span><br/>    | <span data-ttu-id="e5451-139">字串</span><span class="sxs-lookup"><span data-stu-id="e5451-139">string</span></span><br/>  | <span data-ttu-id="e5451-140">psk：條件式</span><span class="sxs-lookup"><span data-stu-id="e5451-140">psk:Conditional</span></span><br/> |
| <span data-ttu-id="e5451-141">多個</span><span class="sxs-lookup"><span data-stu-id="e5451-141">Multiple</span></span><br/>     | <span data-ttu-id="e5451-142">整數</span><span class="sxs-lookup"><span data-stu-id="e5451-142">integer</span></span><br/> | <span data-ttu-id="e5451-143">1</span><span class="sxs-lookup"><span data-stu-id="e5451-143">1</span></span><br/>               |
| <span data-ttu-id="e5451-144">Unittype.pixel 表示</span><span class="sxs-lookup"><span data-stu-id="e5451-144">UnitType</span></span><br/>     | <span data-ttu-id="e5451-145">字串</span><span class="sxs-lookup"><span data-stu-id="e5451-145">string</span></span><br/>  | <span data-ttu-id="e5451-146">微米</span><span class="sxs-lookup"><span data-stu-id="e5451-146">microns</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="e5451-147">相關主題</span><span class="sxs-lookup"><span data-stu-id="e5451-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e5451-148">PostScript 印表機描述檔案格式規格</span><span class="sxs-lookup"><span data-stu-id="e5451-148">PostScript Printer Description File Format Specification</span></span>](https://www.adobe.com/products/postscript/pdfs/PLRM.pdf)
</dt> <dt>

[<span data-ttu-id="e5451-149">列印架構規格</span><span class="sxs-lookup"><span data-stu-id="e5451-149">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




