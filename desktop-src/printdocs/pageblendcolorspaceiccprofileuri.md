---
description: 本主題並非最新的。 如需最新資訊，請參閱列印架構規格。
ms.assetid: 05924c7d-e074-4835-b42c-53c77dc1bbb5
title: PageBlendColorSpaceICCProfileURI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2cbf1233e172a81053baee0abe1e21d79064045a
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/26/2021
ms.locfileid: "107997695"
---
# <a name="pageblendcolorspaceiccprofileuri"></a><span data-ttu-id="29bcd-104">PageBlendColorSpaceICCProfileURI</span><span class="sxs-lookup"><span data-stu-id="29bcd-104">PageBlendColorSpaceICCProfileURI</span></span>

<span data-ttu-id="29bcd-105">本主題並非最新的。</span><span class="sxs-lookup"><span data-stu-id="29bcd-105">This topic is not current.</span></span> <span data-ttu-id="29bcd-106">如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。</span><span class="sxs-lookup"><span data-stu-id="29bcd-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="29bcd-107">指定定義應用於混合之色彩空間的 ICC 設定檔的相對 URI 參考。</span><span class="sxs-lookup"><span data-stu-id="29bcd-107">Specifies a relative URI reference to an ICC profile defining the color space that SHOULD be used for blending.</span></span> <span data-ttu-id="29bcd-108"><Uri>是 \_ 相對於封裝根目錄的絕對部分名稱。</span><span class="sxs-lookup"><span data-stu-id="29bcd-108">The <Uri> is an absolute part\_name relative to the package root.</span></span>

-   [<span data-ttu-id="29bcd-109">項目資訊</span><span class="sxs-lookup"><span data-stu-id="29bcd-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="29bcd-110">結構內容</span><span class="sxs-lookup"><span data-stu-id="29bcd-110">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="29bcd-111">項目資訊</span><span class="sxs-lookup"><span data-stu-id="29bcd-111">Element Information</span></span>



| <span data-ttu-id="29bcd-112">Name</span><span class="sxs-lookup"><span data-stu-id="29bcd-112">Name</span></span> | <span data-ttu-id="29bcd-113">值</span><span class="sxs-lookup"><span data-stu-id="29bcd-113">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="29bcd-114">項目類型</span><span class="sxs-lookup"><span data-stu-id="29bcd-114">Element Type</span></span> <br/>   | <span data-ttu-id="29bcd-115">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="29bcd-115">ParameterDef</span></span><br/>                                                                                                                |
| <span data-ttu-id="29bcd-116">範圍前置詞</span><span class="sxs-lookup"><span data-stu-id="29bcd-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="29bcd-117">頁面</span><span class="sxs-lookup"><span data-stu-id="29bcd-117">Page</span></span><br/>                                                                                                                        |
| <span data-ttu-id="29bcd-118">備註</span><span class="sxs-lookup"><span data-stu-id="29bcd-118">Notes</span></span> <br/>          | <span data-ttu-id="29bcd-119">這僅適用于 XPS 檔，不應該用於任意 PrintTickets。</span><span class="sxs-lookup"><span data-stu-id="29bcd-119">This applies to XPS Documents only and should not be used in arbitrary PrintTickets.</span></span> <span data-ttu-id="29bcd-120">連結到 PageBlendColorSpace 元素。</span><span class="sxs-lookup"><span data-stu-id="29bcd-120">Linked to PageBlendColorSpace element.</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="29bcd-121">結構內容</span><span class="sxs-lookup"><span data-stu-id="29bcd-121">Structure Content</span></span>

<span data-ttu-id="29bcd-122">此元素的 XML 結構為：</span><span class="sxs-lookup"><span data-stu-id="29bcd-122">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="29bcd-123">結構屬性</span><span class="sxs-lookup"><span data-stu-id="29bcd-123">Structure Properties</span></span>

<span data-ttu-id="29bcd-124">下表概述 XML 結構中所定義之變數的特性。</span><span class="sxs-lookup"><span data-stu-id="29bcd-124">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="29bcd-125">屬性</span><span class="sxs-lookup"><span data-stu-id="29bcd-125">Property</span></span>                | <span data-ttu-id="29bcd-126">xsi:type</span><span class="sxs-lookup"><span data-stu-id="29bcd-126">xsi:type</span></span>           | <span data-ttu-id="29bcd-127">值</span><span class="sxs-lookup"><span data-stu-id="29bcd-127">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="29bcd-128">DataType</span><span class="sxs-lookup"><span data-stu-id="29bcd-128">DataType</span></span><br/>     | <span data-ttu-id="29bcd-129">字串</span><span class="sxs-lookup"><span data-stu-id="29bcd-129">string</span></span><br/>  | <span data-ttu-id="29bcd-130">xs:string</span><span class="sxs-lookup"><span data-stu-id="29bcd-130">xs:string</span></span><br/>       |
| <span data-ttu-id="29bcd-131">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="29bcd-131">DefaultValue</span></span><br/> | <span data-ttu-id="29bcd-132">字串</span><span class="sxs-lookup"><span data-stu-id="29bcd-132">string</span></span><br/>  | <span data-ttu-id="29bcd-133">未定義</span><span class="sxs-lookup"><span data-stu-id="29bcd-133">undefined</span></span><br/>       |
| <span data-ttu-id="29bcd-134">MaxLength</span><span class="sxs-lookup"><span data-stu-id="29bcd-134">MaxLength</span></span><br/>    | <span data-ttu-id="29bcd-135">整數</span><span class="sxs-lookup"><span data-stu-id="29bcd-135">integer</span></span><br/> | <span data-ttu-id="29bcd-136">未定義</span><span class="sxs-lookup"><span data-stu-id="29bcd-136">undefined</span></span><br/>       |
| <span data-ttu-id="29bcd-137">MinLength</span><span class="sxs-lookup"><span data-stu-id="29bcd-137">MinLength</span></span><br/>    | <span data-ttu-id="29bcd-138">整數</span><span class="sxs-lookup"><span data-stu-id="29bcd-138">integer</span></span><br/> | <span data-ttu-id="29bcd-139">1</span><span class="sxs-lookup"><span data-stu-id="29bcd-139">1</span></span><br/>               |
| <span data-ttu-id="29bcd-140">強制性</span><span class="sxs-lookup"><span data-stu-id="29bcd-140">Mandatory</span></span><br/>    | <span data-ttu-id="29bcd-141">字串</span><span class="sxs-lookup"><span data-stu-id="29bcd-141">string</span></span><br/>  | <span data-ttu-id="29bcd-142">psk：條件式</span><span class="sxs-lookup"><span data-stu-id="29bcd-142">psk:Conditional</span></span><br/> |
| <span data-ttu-id="29bcd-143">Unittype.pixel 表示</span><span class="sxs-lookup"><span data-stu-id="29bcd-143">UnitType</span></span><br/>     | <span data-ttu-id="29bcd-144">字串</span><span class="sxs-lookup"><span data-stu-id="29bcd-144">string</span></span><br/>  | <span data-ttu-id="29bcd-145">字元</span><span class="sxs-lookup"><span data-stu-id="29bcd-145">characters</span></span><br/>      |



 

## <a name="related-topics"></a><span data-ttu-id="29bcd-146">相關主題</span><span class="sxs-lookup"><span data-stu-id="29bcd-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="29bcd-147">列印架構規格</span><span class="sxs-lookup"><span data-stu-id="29bcd-147">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




