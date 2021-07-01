---
description: 深入瞭解 DocumentImpositionColor 參數。 本主題並非最新的。 如需最新資訊，請參閱列印架構規格。
ms.assetid: e1cb7e46-3078-46bf-a8c8-e10f6b9dd222
title: DocumentImpositionColor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b747487c19160d29778f306a91b62cf43d245f65
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120003"
---
# <a name="documentimpositioncolor"></a><span data-ttu-id="1c886-105">DocumentImpositionColor</span><span class="sxs-lookup"><span data-stu-id="1c886-105">DocumentImpositionColor</span></span>

<span data-ttu-id="1c886-106">本主題並非最新的。</span><span class="sxs-lookup"><span data-stu-id="1c886-106">This topic is not current.</span></span> <span data-ttu-id="1c886-107">如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。</span><span class="sxs-lookup"><span data-stu-id="1c886-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="1c886-108">以指定的命名色彩標記的應用程式內容，必須出現在所有色彩分隔上。</span><span class="sxs-lookup"><span data-stu-id="1c886-108">Application content labeled with the specified named color MUST appear on all color separations.</span></span>

-   [<span data-ttu-id="1c886-109">項目資訊</span><span class="sxs-lookup"><span data-stu-id="1c886-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="1c886-110">結構內容</span><span class="sxs-lookup"><span data-stu-id="1c886-110">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="1c886-111">項目資訊</span><span class="sxs-lookup"><span data-stu-id="1c886-111">Element Information</span></span>



| <span data-ttu-id="1c886-112">Name</span><span class="sxs-lookup"><span data-stu-id="1c886-112">Name</span></span> | <span data-ttu-id="1c886-113">值</span><span class="sxs-lookup"><span data-stu-id="1c886-113">Value</span></span> |
|----------------------------|-------------------------|
| <span data-ttu-id="1c886-114">項目類型</span><span class="sxs-lookup"><span data-stu-id="1c886-114">Element Type</span></span> <br/>   | <span data-ttu-id="1c886-115">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="1c886-115">ParameterDef</span></span><br/> |
| <span data-ttu-id="1c886-116">範圍前置詞</span><span class="sxs-lookup"><span data-stu-id="1c886-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="1c886-117">文件</span><span class="sxs-lookup"><span data-stu-id="1c886-117">Document</span></span><br/>     |
| <span data-ttu-id="1c886-118">注意</span><span class="sxs-lookup"><span data-stu-id="1c886-118">Notes</span></span> <br/>          | <span data-ttu-id="1c886-119">None</span><span class="sxs-lookup"><span data-stu-id="1c886-119">None</span></span><br/>         |



 

## <a name="structure-content"></a><span data-ttu-id="1c886-120">結構內容</span><span class="sxs-lookup"><span data-stu-id="1c886-120">Structure Content</span></span>

<span data-ttu-id="1c886-121">此元素的 XML 結構為：</span><span class="sxs-lookup"><span data-stu-id="1c886-121">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:DocumentImpositionColor">
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

## <a name="structure-properties"></a><span data-ttu-id="1c886-122">結構屬性</span><span class="sxs-lookup"><span data-stu-id="1c886-122">Structure Properties</span></span>

<span data-ttu-id="1c886-123">下表概述 XML 結構中所定義之變數的特性。</span><span class="sxs-lookup"><span data-stu-id="1c886-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="1c886-124">屬性</span><span class="sxs-lookup"><span data-stu-id="1c886-124">Property</span></span>                | <span data-ttu-id="1c886-125">xsi:type</span><span class="sxs-lookup"><span data-stu-id="1c886-125">xsi:type</span></span>           | <span data-ttu-id="1c886-126">值</span><span class="sxs-lookup"><span data-stu-id="1c886-126">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="1c886-127">DataType</span><span class="sxs-lookup"><span data-stu-id="1c886-127">DataType</span></span><br/>     | <span data-ttu-id="1c886-128">字串</span><span class="sxs-lookup"><span data-stu-id="1c886-128">string</span></span><br/>  | <span data-ttu-id="1c886-129">xs:string</span><span class="sxs-lookup"><span data-stu-id="1c886-129">xs:string</span></span><br/>       |
| <span data-ttu-id="1c886-130">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="1c886-130">DefaultValue</span></span><br/> | <span data-ttu-id="1c886-131">字串</span><span class="sxs-lookup"><span data-stu-id="1c886-131">string</span></span><br/>  | <span data-ttu-id="1c886-132">未定義</span><span class="sxs-lookup"><span data-stu-id="1c886-132">undefined</span></span><br/>       |
| <span data-ttu-id="1c886-133">MaxLength</span><span class="sxs-lookup"><span data-stu-id="1c886-133">MaxLength</span></span><br/>    | <span data-ttu-id="1c886-134">整數</span><span class="sxs-lookup"><span data-stu-id="1c886-134">integer</span></span><br/> | <span data-ttu-id="1c886-135">未定義</span><span class="sxs-lookup"><span data-stu-id="1c886-135">undefined</span></span><br/>       |
| <span data-ttu-id="1c886-136">MinLength</span><span class="sxs-lookup"><span data-stu-id="1c886-136">MinLength</span></span><br/>    | <span data-ttu-id="1c886-137">整數</span><span class="sxs-lookup"><span data-stu-id="1c886-137">integer</span></span><br/> | <span data-ttu-id="1c886-138">1</span><span class="sxs-lookup"><span data-stu-id="1c886-138">1</span></span><br/>               |
| <span data-ttu-id="1c886-139">強制性</span><span class="sxs-lookup"><span data-stu-id="1c886-139">Mandatory</span></span><br/>    | <span data-ttu-id="1c886-140">string</span><span class="sxs-lookup"><span data-stu-id="1c886-140">string</span></span><br/>  | <span data-ttu-id="1c886-141">psk：條件式</span><span class="sxs-lookup"><span data-stu-id="1c886-141">psk:Conditional</span></span><br/> |
| <span data-ttu-id="1c886-142">Unittype.pixel 表示</span><span class="sxs-lookup"><span data-stu-id="1c886-142">UnitType</span></span><br/>     | <span data-ttu-id="1c886-143">string</span><span class="sxs-lookup"><span data-stu-id="1c886-143">string</span></span><br/>  | <span data-ttu-id="1c886-144">字元</span><span class="sxs-lookup"><span data-stu-id="1c886-144">characters</span></span><br/>      |



 

## <a name="related-topics"></a><span data-ttu-id="1c886-145">相關主題</span><span class="sxs-lookup"><span data-stu-id="1c886-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1c886-146">列印架構規格</span><span class="sxs-lookup"><span data-stu-id="1c886-146">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




