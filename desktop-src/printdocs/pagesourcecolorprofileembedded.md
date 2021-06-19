---
description: 深入瞭解 PageSourceColorProfileEmbedded 參數。 本主題並非最新的。 如需最新資訊，請參閱列印架構規格。
ms.assetid: 38411802-2b2e-441c-b3a6-334d87b11b5d
title: PageSourceColorProfileEmbedded
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0633fa061601c1d575f174ab5572582efdf9a89e
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/19/2021
ms.locfileid: "112395633"
---
# <a name="pagesourcecolorprofileembedded"></a><span data-ttu-id="0498f-105">PageSourceColorProfileEmbedded</span><span class="sxs-lookup"><span data-stu-id="0498f-105">PageSourceColorProfileEmbedded</span></span>

<span data-ttu-id="0498f-106">本主題並非最新的。</span><span class="sxs-lookup"><span data-stu-id="0498f-106">This topic is not current.</span></span> <span data-ttu-id="0498f-107">如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。</span><span class="sxs-lookup"><span data-stu-id="0498f-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="0498f-108">指定內嵌來源色彩設定檔。</span><span class="sxs-lookup"><span data-stu-id="0498f-108">Specifies the embedded source color profile.</span></span>

-   [<span data-ttu-id="0498f-109">項目資訊</span><span class="sxs-lookup"><span data-stu-id="0498f-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="0498f-110">結構內容</span><span class="sxs-lookup"><span data-stu-id="0498f-110">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="0498f-111">項目資訊</span><span class="sxs-lookup"><span data-stu-id="0498f-111">Element Information</span></span>



| <span data-ttu-id="0498f-112">Name</span><span class="sxs-lookup"><span data-stu-id="0498f-112">Name</span></span> | <span data-ttu-id="0498f-113">值</span><span class="sxs-lookup"><span data-stu-id="0498f-113">Value</span></span> |
|----------------------------|-----------------------------------------------------|
| <span data-ttu-id="0498f-114">項目類型</span><span class="sxs-lookup"><span data-stu-id="0498f-114">Element Type</span></span> <br/>   | <span data-ttu-id="0498f-115">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="0498f-115">ParameterDef</span></span><br/>                             |
| <span data-ttu-id="0498f-116">範圍前置詞</span><span class="sxs-lookup"><span data-stu-id="0498f-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="0498f-117">頁面</span><span class="sxs-lookup"><span data-stu-id="0498f-117">Page</span></span><br/>                                     |
| <span data-ttu-id="0498f-118">備註</span><span class="sxs-lookup"><span data-stu-id="0498f-118">Notes</span></span> <br/>          | <span data-ttu-id="0498f-119">連結至 PageSourceColorProfile 元素</span><span class="sxs-lookup"><span data-stu-id="0498f-119">Linked to PageSourceColorProfile element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="0498f-120">結構內容</span><span class="sxs-lookup"><span data-stu-id="0498f-120">Structure Content</span></span>

<span data-ttu-id="0498f-121">此元素的 XML 結構為：</span><span class="sxs-lookup"><span data-stu-id="0498f-121">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageSourceColorProfileEmbedded">
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

## <a name="structure-properties"></a><span data-ttu-id="0498f-122">結構屬性</span><span class="sxs-lookup"><span data-stu-id="0498f-122">Structure Properties</span></span>

<span data-ttu-id="0498f-123">下表概述 XML 結構中所定義之變數的特性。</span><span class="sxs-lookup"><span data-stu-id="0498f-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="0498f-124">屬性</span><span class="sxs-lookup"><span data-stu-id="0498f-124">Property</span></span>                | <span data-ttu-id="0498f-125">xsi:type</span><span class="sxs-lookup"><span data-stu-id="0498f-125">xsi:type</span></span>           | <span data-ttu-id="0498f-126">值</span><span class="sxs-lookup"><span data-stu-id="0498f-126">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="0498f-127">DataType</span><span class="sxs-lookup"><span data-stu-id="0498f-127">DataType</span></span><br/>     | <span data-ttu-id="0498f-128">字串</span><span class="sxs-lookup"><span data-stu-id="0498f-128">string</span></span><br/>  | <span data-ttu-id="0498f-129">xs:string</span><span class="sxs-lookup"><span data-stu-id="0498f-129">xs:string</span></span><br/>       |
| <span data-ttu-id="0498f-130">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="0498f-130">DefaultValue</span></span><br/> | <span data-ttu-id="0498f-131">字串</span><span class="sxs-lookup"><span data-stu-id="0498f-131">string</span></span><br/>  | <span data-ttu-id="0498f-132">未定義</span><span class="sxs-lookup"><span data-stu-id="0498f-132">undefined</span></span><br/>       |
| <span data-ttu-id="0498f-133">MaxLength</span><span class="sxs-lookup"><span data-stu-id="0498f-133">MaxLength</span></span><br/>    | <span data-ttu-id="0498f-134">整數</span><span class="sxs-lookup"><span data-stu-id="0498f-134">integer</span></span><br/> | <span data-ttu-id="0498f-135">未定義</span><span class="sxs-lookup"><span data-stu-id="0498f-135">undefined</span></span><br/>       |
| <span data-ttu-id="0498f-136">MinLength</span><span class="sxs-lookup"><span data-stu-id="0498f-136">MinLength</span></span><br/>    | <span data-ttu-id="0498f-137">整數</span><span class="sxs-lookup"><span data-stu-id="0498f-137">integer</span></span><br/> | <span data-ttu-id="0498f-138">1</span><span class="sxs-lookup"><span data-stu-id="0498f-138">1</span></span><br/>               |
| <span data-ttu-id="0498f-139">強制性</span><span class="sxs-lookup"><span data-stu-id="0498f-139">Mandatory</span></span><br/>    | <span data-ttu-id="0498f-140">string</span><span class="sxs-lookup"><span data-stu-id="0498f-140">string</span></span><br/>  | <span data-ttu-id="0498f-141">psk：條件式</span><span class="sxs-lookup"><span data-stu-id="0498f-141">psk:Conditional</span></span><br/> |
| <span data-ttu-id="0498f-142">Unittype.pixel 表示</span><span class="sxs-lookup"><span data-stu-id="0498f-142">UnitType</span></span><br/>     | <span data-ttu-id="0498f-143">string</span><span class="sxs-lookup"><span data-stu-id="0498f-143">string</span></span><br/>  | <span data-ttu-id="0498f-144">字元</span><span class="sxs-lookup"><span data-stu-id="0498f-144">characters</span></span><br/>      |



 

## <a name="related-topics"></a><span data-ttu-id="0498f-145">相關主題</span><span class="sxs-lookup"><span data-stu-id="0498f-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0498f-146">列印架構規格</span><span class="sxs-lookup"><span data-stu-id="0498f-146">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




