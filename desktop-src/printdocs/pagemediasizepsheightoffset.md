---
description: 取得 PageMediaSizePSHeightOffset 參數的相關資訊。 本主題並非最新的。 如需最新資訊，請參閱列印架構規格。
ms.assetid: e86d6a5d-484d-4c80-8c86-7d12d287ee21
title: PageMediaSizePSHeightOffset
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5e2c0e3802a6c461fe2f9eec68b28677c254be9
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/19/2021
ms.locfileid: "112395733"
---
# <a name="pagemediasizepsheightoffset"></a><span data-ttu-id="cbcfd-105">PageMediaSizePSHeightOffset</span><span class="sxs-lookup"><span data-stu-id="cbcfd-105">PageMediaSizePSHeightOffset</span></span>

<span data-ttu-id="cbcfd-106">本主題並非最新的。</span><span class="sxs-lookup"><span data-stu-id="cbcfd-106">This topic is not current.</span></span> <span data-ttu-id="cbcfd-107">如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。</span><span class="sxs-lookup"><span data-stu-id="cbcfd-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="cbcfd-108">指定位移，與饋送方向方向 (參考 [PostScript 印表機描述檔案格式規格](https://www.adobe.com/products/postscript/pdfs/PLRM.pdf)) 。</span><span class="sxs-lookup"><span data-stu-id="cbcfd-108">Specifies the offset, parallel to the feed-orientation direction (Reference [PostScript Printer Description File Format Specification](https://www.adobe.com/products/postscript/pdfs/PLRM.pdf)).</span></span>

-   [<span data-ttu-id="cbcfd-109">項目資訊</span><span class="sxs-lookup"><span data-stu-id="cbcfd-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="cbcfd-110">結構內容</span><span class="sxs-lookup"><span data-stu-id="cbcfd-110">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="cbcfd-111">項目資訊</span><span class="sxs-lookup"><span data-stu-id="cbcfd-111">Element Information</span></span>



| <span data-ttu-id="cbcfd-112">Name</span><span class="sxs-lookup"><span data-stu-id="cbcfd-112">Name</span></span> | <span data-ttu-id="cbcfd-113">值</span><span class="sxs-lookup"><span data-stu-id="cbcfd-113">Value</span></span> |
|----------------------------|-------------------------------------------------------------|
| <span data-ttu-id="cbcfd-114">項目類型</span><span class="sxs-lookup"><span data-stu-id="cbcfd-114">Element Type</span></span> <br/>   | <span data-ttu-id="cbcfd-115">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="cbcfd-115">ParameterDef</span></span><br/>                                     |
| <span data-ttu-id="cbcfd-116">範圍前置詞</span><span class="sxs-lookup"><span data-stu-id="cbcfd-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="cbcfd-117">頁面</span><span class="sxs-lookup"><span data-stu-id="cbcfd-117">Page</span></span><br/>                                             |
| <span data-ttu-id="cbcfd-118">備註</span><span class="sxs-lookup"><span data-stu-id="cbcfd-118">Notes</span></span> <br/>          | <span data-ttu-id="cbcfd-119">連結至 PageMediaSize 元素，CustomPS 選項</span><span class="sxs-lookup"><span data-stu-id="cbcfd-119">Linked to PageMediaSize element, CustomPS option</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="cbcfd-120">結構內容</span><span class="sxs-lookup"><span data-stu-id="cbcfd-120">Structure Content</span></span>

<span data-ttu-id="cbcfd-121">此元素的 XML 結構為：</span><span class="sxs-lookup"><span data-stu-id="cbcfd-121">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="cbcfd-122">結構屬性</span><span class="sxs-lookup"><span data-stu-id="cbcfd-122">Structure Properties</span></span>

<span data-ttu-id="cbcfd-123">下表概述 XML 結構中所定義之變數的特性。</span><span class="sxs-lookup"><span data-stu-id="cbcfd-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="cbcfd-124">屬性</span><span class="sxs-lookup"><span data-stu-id="cbcfd-124">Property</span></span>                | <span data-ttu-id="cbcfd-125">xsi:type</span><span class="sxs-lookup"><span data-stu-id="cbcfd-125">xsi:type</span></span>           | <span data-ttu-id="cbcfd-126">值</span><span class="sxs-lookup"><span data-stu-id="cbcfd-126">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="cbcfd-127">DataType</span><span class="sxs-lookup"><span data-stu-id="cbcfd-127">DataType</span></span><br/>     | <span data-ttu-id="cbcfd-128">字串</span><span class="sxs-lookup"><span data-stu-id="cbcfd-128">string</span></span><br/>  | <span data-ttu-id="cbcfd-129">xs:integer</span><span class="sxs-lookup"><span data-stu-id="cbcfd-129">xs:integer</span></span><br/>      |
| <span data-ttu-id="cbcfd-130">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="cbcfd-130">DefaultValue</span></span><br/> | <span data-ttu-id="cbcfd-131">整數</span><span class="sxs-lookup"><span data-stu-id="cbcfd-131">integer</span></span><br/> | <span data-ttu-id="cbcfd-132">未定義</span><span class="sxs-lookup"><span data-stu-id="cbcfd-132">undefined</span></span><br/>       |
| <span data-ttu-id="cbcfd-133">MaxValue</span><span class="sxs-lookup"><span data-stu-id="cbcfd-133">MaxValue</span></span><br/>     | <span data-ttu-id="cbcfd-134">整數</span><span class="sxs-lookup"><span data-stu-id="cbcfd-134">integer</span></span><br/> | <span data-ttu-id="cbcfd-135">未定義</span><span class="sxs-lookup"><span data-stu-id="cbcfd-135">undefined</span></span><br/>       |
| <span data-ttu-id="cbcfd-136">MinValue</span><span class="sxs-lookup"><span data-stu-id="cbcfd-136">MinValue</span></span><br/>     | <span data-ttu-id="cbcfd-137">整數</span><span class="sxs-lookup"><span data-stu-id="cbcfd-137">integer</span></span><br/> | <span data-ttu-id="cbcfd-138">未定義</span><span class="sxs-lookup"><span data-stu-id="cbcfd-138">undefined</span></span><br/>       |
| <span data-ttu-id="cbcfd-139">強制性</span><span class="sxs-lookup"><span data-stu-id="cbcfd-139">Mandatory</span></span><br/>    | <span data-ttu-id="cbcfd-140">string</span><span class="sxs-lookup"><span data-stu-id="cbcfd-140">string</span></span><br/>  | <span data-ttu-id="cbcfd-141">psk：條件式</span><span class="sxs-lookup"><span data-stu-id="cbcfd-141">psk:Conditional</span></span><br/> |
| <span data-ttu-id="cbcfd-142">多個</span><span class="sxs-lookup"><span data-stu-id="cbcfd-142">Multiple</span></span><br/>     | <span data-ttu-id="cbcfd-143">整數</span><span class="sxs-lookup"><span data-stu-id="cbcfd-143">integer</span></span><br/> | <span data-ttu-id="cbcfd-144">1</span><span class="sxs-lookup"><span data-stu-id="cbcfd-144">1</span></span><br/>               |
| <span data-ttu-id="cbcfd-145">Unittype.pixel 表示</span><span class="sxs-lookup"><span data-stu-id="cbcfd-145">UnitType</span></span><br/>     | <span data-ttu-id="cbcfd-146">string</span><span class="sxs-lookup"><span data-stu-id="cbcfd-146">string</span></span><br/>  | <span data-ttu-id="cbcfd-147">微米</span><span class="sxs-lookup"><span data-stu-id="cbcfd-147">microns</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="cbcfd-148">相關主題</span><span class="sxs-lookup"><span data-stu-id="cbcfd-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cbcfd-149">PostScript 印表機描述檔案格式規格</span><span class="sxs-lookup"><span data-stu-id="cbcfd-149">PostScript Printer Description File Format Specification</span></span>](https://www.adobe.com/products/postscript/pdfs/PLRM.pdf)
</dt> <dt>

[<span data-ttu-id="cbcfd-150">列印架構規格</span><span class="sxs-lookup"><span data-stu-id="cbcfd-150">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




