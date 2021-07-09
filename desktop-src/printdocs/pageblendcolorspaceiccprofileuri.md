---
description: 閱讀 PageBlendColorSpaceICCProfileURI 參數。 本主題並非最新的。 如需最新資訊，請參閱列印架構規格。
ms.assetid: 05924c7d-e074-4835-b42c-53c77dc1bbb5
title: PageBlendColorSpaceICCProfileURI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50db89757737ff5aa6a1358af418ee33809b960e
ms.sourcegitcommit: 998d50f6def8a25850fc113fc8a2df903c829c5e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/09/2021
ms.locfileid: "113549316"
---
# <a name="pageblendcolorspaceiccprofileuri"></a><span data-ttu-id="0c803-105">PageBlendColorSpaceICCProfileURI</span><span class="sxs-lookup"><span data-stu-id="0c803-105">PageBlendColorSpaceICCProfileURI</span></span>

<span data-ttu-id="0c803-106">本主題並非最新的。</span><span class="sxs-lookup"><span data-stu-id="0c803-106">This topic is not current.</span></span> <span data-ttu-id="0c803-107">如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。</span><span class="sxs-lookup"><span data-stu-id="0c803-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="0c803-108">指定定義應用於混合之色彩空間的 ICC 設定檔的相對 URI 參考。</span><span class="sxs-lookup"><span data-stu-id="0c803-108">Specifies a relative URI reference to an ICC profile defining the color space that SHOULD be used for blending.</span></span> <span data-ttu-id="0c803-109"><Uri>是 \_ 相對於封裝根目錄的絕對部分名稱。</span><span class="sxs-lookup"><span data-stu-id="0c803-109">The <Uri> is an absolute part\_name relative to the package root.</span></span>

-   [<span data-ttu-id="0c803-110">項目資訊</span><span class="sxs-lookup"><span data-stu-id="0c803-110">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="0c803-111">結構內容</span><span class="sxs-lookup"><span data-stu-id="0c803-111">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="0c803-112">項目資訊</span><span class="sxs-lookup"><span data-stu-id="0c803-112">Element Information</span></span>



| <span data-ttu-id="0c803-113">Name</span><span class="sxs-lookup"><span data-stu-id="0c803-113">Name</span></span> | <span data-ttu-id="0c803-114">值</span><span class="sxs-lookup"><span data-stu-id="0c803-114">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0c803-115">項目類型</span><span class="sxs-lookup"><span data-stu-id="0c803-115">Element Type</span></span> <br/>   | <span data-ttu-id="0c803-116">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="0c803-116">ParameterDef</span></span><br/>                                                                                                                |
| <span data-ttu-id="0c803-117">範圍前置詞</span><span class="sxs-lookup"><span data-stu-id="0c803-117">Scoping Prefix</span></span> <br/> | <span data-ttu-id="0c803-118">頁面</span><span class="sxs-lookup"><span data-stu-id="0c803-118">Page</span></span><br/>                                                                                                                        |
| <span data-ttu-id="0c803-119">備註</span><span class="sxs-lookup"><span data-stu-id="0c803-119">Notes</span></span> <br/>          | <span data-ttu-id="0c803-120">這僅適用于 XPS 檔，不應該用於任意 PrintTickets。</span><span class="sxs-lookup"><span data-stu-id="0c803-120">This applies to XPS Documents only and should not be used in arbitrary PrintTickets.</span></span> <span data-ttu-id="0c803-121">連結到 PageBlendColorSpace 元素。</span><span class="sxs-lookup"><span data-stu-id="0c803-121">Linked to PageBlendColorSpace element.</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="0c803-122">結構內容</span><span class="sxs-lookup"><span data-stu-id="0c803-122">Structure Content</span></span>

<span data-ttu-id="0c803-123">此元素的 XML 結構為：</span><span class="sxs-lookup"><span data-stu-id="0c803-123">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageBlendColorSpaceICCProfileURI">
  <psf:Property name="psf:DataType">
    <psf:Value xsi:type="xs:string">xs:string</psf:Value>
  </psf:Property>
  <psf:Property name="psf:DefaultValue">
    <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MaxLength">
    <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MinLength">
    <psf:Value xsi:type="xs:integer">1</psf:Value>
  </psf:Property>
  <psf:Property name="psf:Mandatory">
    <psf:Value xsi:type="xs:string">psk:Conditional</psf:Value>
  </psf:Property>
  <psf:Property name="psf:UnitType">
    <psf:Value xsi:type="xs:string">characters</psf:Value>
  </psf:Property>
</psf:ParameterDef>
```

## <a name="structure-properties"></a><span data-ttu-id="0c803-124">結構屬性</span><span class="sxs-lookup"><span data-stu-id="0c803-124">Structure Properties</span></span>

<span data-ttu-id="0c803-125">下表概述 XML 結構中所定義之變數的特性。</span><span class="sxs-lookup"><span data-stu-id="0c803-125">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="0c803-126">屬性</span><span class="sxs-lookup"><span data-stu-id="0c803-126">Property</span></span>                | <span data-ttu-id="0c803-127">xsi:type</span><span class="sxs-lookup"><span data-stu-id="0c803-127">xsi:type</span></span>           | <span data-ttu-id="0c803-128">值</span><span class="sxs-lookup"><span data-stu-id="0c803-128">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="0c803-129">DataType</span><span class="sxs-lookup"><span data-stu-id="0c803-129">DataType</span></span><br/>     | <span data-ttu-id="0c803-130">字串</span><span class="sxs-lookup"><span data-stu-id="0c803-130">string</span></span><br/>  | <span data-ttu-id="0c803-131">xs:string</span><span class="sxs-lookup"><span data-stu-id="0c803-131">xs:string</span></span><br/>       |
| <span data-ttu-id="0c803-132">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="0c803-132">DefaultValue</span></span><br/> | <span data-ttu-id="0c803-133">字串</span><span class="sxs-lookup"><span data-stu-id="0c803-133">string</span></span><br/>  | <span data-ttu-id="0c803-134">未定義</span><span class="sxs-lookup"><span data-stu-id="0c803-134">undefined</span></span><br/>       |
| <span data-ttu-id="0c803-135">MaxLength</span><span class="sxs-lookup"><span data-stu-id="0c803-135">MaxLength</span></span><br/>    | <span data-ttu-id="0c803-136">整數</span><span class="sxs-lookup"><span data-stu-id="0c803-136">integer</span></span><br/> | <span data-ttu-id="0c803-137">未定義</span><span class="sxs-lookup"><span data-stu-id="0c803-137">undefined</span></span><br/>       |
| <span data-ttu-id="0c803-138">MinLength</span><span class="sxs-lookup"><span data-stu-id="0c803-138">MinLength</span></span><br/>    | <span data-ttu-id="0c803-139">整數</span><span class="sxs-lookup"><span data-stu-id="0c803-139">integer</span></span><br/> | <span data-ttu-id="0c803-140">1</span><span class="sxs-lookup"><span data-stu-id="0c803-140">1</span></span><br/>               |
| <span data-ttu-id="0c803-141">強制性</span><span class="sxs-lookup"><span data-stu-id="0c803-141">Mandatory</span></span><br/>    | <span data-ttu-id="0c803-142">string</span><span class="sxs-lookup"><span data-stu-id="0c803-142">string</span></span><br/>  | <span data-ttu-id="0c803-143">psk：條件式</span><span class="sxs-lookup"><span data-stu-id="0c803-143">psk:Conditional</span></span><br/> |
| <span data-ttu-id="0c803-144">Unittype.pixel 表示</span><span class="sxs-lookup"><span data-stu-id="0c803-144">UnitType</span></span><br/>     | <span data-ttu-id="0c803-145">string</span><span class="sxs-lookup"><span data-stu-id="0c803-145">string</span></span><br/>  | <span data-ttu-id="0c803-146">字元</span><span class="sxs-lookup"><span data-stu-id="0c803-146">characters</span></span><br/>      |



 

## <a name="related-topics"></a><span data-ttu-id="0c803-147">相關主題</span><span class="sxs-lookup"><span data-stu-id="0c803-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0c803-148">列印架構規格</span><span class="sxs-lookup"><span data-stu-id="0c803-148">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




