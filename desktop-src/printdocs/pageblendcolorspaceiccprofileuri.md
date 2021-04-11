---
description: 本主題並非最新的。 如需最新資訊，請參閱列印架構規格。
ms.assetid: 05924c7d-e074-4835-b42c-53c77dc1bbb5
title: PageBlendColorSpaceICCProfileURI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1f3a6143bd934ebcb75c3e5455a30c7365f1a89
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/05/2021
ms.locfileid: "104035237"
---
# <a name="pageblendcolorspaceiccprofileuri"></a><span data-ttu-id="4b427-104">PageBlendColorSpaceICCProfileURI</span><span class="sxs-lookup"><span data-stu-id="4b427-104">PageBlendColorSpaceICCProfileURI</span></span>

<span data-ttu-id="4b427-105">本主題並非最新的。</span><span class="sxs-lookup"><span data-stu-id="4b427-105">This topic is not current.</span></span> <span data-ttu-id="4b427-106">如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。</span><span class="sxs-lookup"><span data-stu-id="4b427-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="4b427-107">指定定義應用於混合之色彩空間的 ICC 設定檔的相對 URI 參考。</span><span class="sxs-lookup"><span data-stu-id="4b427-107">Specifies a relative URI reference to an ICC profile defining the color space that SHOULD be used for blending.</span></span> <span data-ttu-id="4b427-108"><Uri>是 \_ 相對於封裝根目錄的絕對部分名稱。</span><span class="sxs-lookup"><span data-stu-id="4b427-108">The <Uri> is an absolute part\_name relative to the package root.</span></span>

-   [<span data-ttu-id="4b427-109">項目資訊</span><span class="sxs-lookup"><span data-stu-id="4b427-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="4b427-110">結構內容</span><span class="sxs-lookup"><span data-stu-id="4b427-110">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="4b427-111">項目資訊</span><span class="sxs-lookup"><span data-stu-id="4b427-111">Element Information</span></span>



| <span data-ttu-id="4b427-112">Name</span><span class="sxs-lookup"><span data-stu-id="4b427-112">Name</span></span>                       |                                                                                                                                        |
|----------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4b427-113">項目類型</span><span class="sxs-lookup"><span data-stu-id="4b427-113">Element Type</span></span> <br/>   | <span data-ttu-id="4b427-114">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="4b427-114">ParameterDef</span></span><br/>                                                                                                                |
| <span data-ttu-id="4b427-115">範圍前置詞</span><span class="sxs-lookup"><span data-stu-id="4b427-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="4b427-116">頁面</span><span class="sxs-lookup"><span data-stu-id="4b427-116">Page</span></span><br/>                                                                                                                        |
| <span data-ttu-id="4b427-117">備註</span><span class="sxs-lookup"><span data-stu-id="4b427-117">Notes</span></span> <br/>          | <span data-ttu-id="4b427-118">這僅適用于 XPS 檔，不應該用於任意 PrintTickets。</span><span class="sxs-lookup"><span data-stu-id="4b427-118">This applies to XPS Documents only and should not be used in arbitrary PrintTickets.</span></span> <span data-ttu-id="4b427-119">連結到 PageBlendColorSpace 元素。</span><span class="sxs-lookup"><span data-stu-id="4b427-119">Linked to PageBlendColorSpace element.</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="4b427-120">結構內容</span><span class="sxs-lookup"><span data-stu-id="4b427-120">Structure Content</span></span>

<span data-ttu-id="4b427-121">此元素的 XML 結構為：</span><span class="sxs-lookup"><span data-stu-id="4b427-121">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="4b427-122">結構屬性</span><span class="sxs-lookup"><span data-stu-id="4b427-122">Structure Properties</span></span>

<span data-ttu-id="4b427-123">下表概述 XML 結構中所定義之變數的特性。</span><span class="sxs-lookup"><span data-stu-id="4b427-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="4b427-124">屬性</span><span class="sxs-lookup"><span data-stu-id="4b427-124">Property</span></span>                | <span data-ttu-id="4b427-125">xsi:type</span><span class="sxs-lookup"><span data-stu-id="4b427-125">xsi:type</span></span>           | <span data-ttu-id="4b427-126">值</span><span class="sxs-lookup"><span data-stu-id="4b427-126">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="4b427-127">DataType</span><span class="sxs-lookup"><span data-stu-id="4b427-127">DataType</span></span><br/>     | <span data-ttu-id="4b427-128">字串</span><span class="sxs-lookup"><span data-stu-id="4b427-128">string</span></span><br/>  | <span data-ttu-id="4b427-129">xs:string</span><span class="sxs-lookup"><span data-stu-id="4b427-129">xs:string</span></span><br/>       |
| <span data-ttu-id="4b427-130">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="4b427-130">DefaultValue</span></span><br/> | <span data-ttu-id="4b427-131">字串</span><span class="sxs-lookup"><span data-stu-id="4b427-131">string</span></span><br/>  | <span data-ttu-id="4b427-132">未定義</span><span class="sxs-lookup"><span data-stu-id="4b427-132">undefined</span></span><br/>       |
| <span data-ttu-id="4b427-133">MaxLength</span><span class="sxs-lookup"><span data-stu-id="4b427-133">MaxLength</span></span><br/>    | <span data-ttu-id="4b427-134">整數</span><span class="sxs-lookup"><span data-stu-id="4b427-134">integer</span></span><br/> | <span data-ttu-id="4b427-135">未定義</span><span class="sxs-lookup"><span data-stu-id="4b427-135">undefined</span></span><br/>       |
| <span data-ttu-id="4b427-136">MinLength</span><span class="sxs-lookup"><span data-stu-id="4b427-136">MinLength</span></span><br/>    | <span data-ttu-id="4b427-137">整數</span><span class="sxs-lookup"><span data-stu-id="4b427-137">integer</span></span><br/> | <span data-ttu-id="4b427-138">1</span><span class="sxs-lookup"><span data-stu-id="4b427-138">1</span></span><br/>               |
| <span data-ttu-id="4b427-139">強制性</span><span class="sxs-lookup"><span data-stu-id="4b427-139">Mandatory</span></span><br/>    | <span data-ttu-id="4b427-140">字串</span><span class="sxs-lookup"><span data-stu-id="4b427-140">string</span></span><br/>  | <span data-ttu-id="4b427-141">psk：條件式</span><span class="sxs-lookup"><span data-stu-id="4b427-141">psk:Conditional</span></span><br/> |
| <span data-ttu-id="4b427-142">Unittype.pixel 表示</span><span class="sxs-lookup"><span data-stu-id="4b427-142">UnitType</span></span><br/>     | <span data-ttu-id="4b427-143">字串</span><span class="sxs-lookup"><span data-stu-id="4b427-143">string</span></span><br/>  | <span data-ttu-id="4b427-144">字元</span><span class="sxs-lookup"><span data-stu-id="4b427-144">characters</span></span><br/>      |



 

## <a name="related-topics"></a><span data-ttu-id="4b427-145">相關主題</span><span class="sxs-lookup"><span data-stu-id="4b427-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4b427-146">列印架構規格</span><span class="sxs-lookup"><span data-stu-id="4b427-146">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




