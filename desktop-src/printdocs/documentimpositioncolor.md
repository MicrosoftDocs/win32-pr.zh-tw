---
description: 本主題並非最新的。 如需最新資訊，請參閱列印架構規格。
ms.assetid: e1cb7e46-3078-46bf-a8c8-e10f6b9dd222
title: DocumentImpositionColor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea74db8ac616bc9ca6b7f6cde22f62bea742e7fb
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/05/2021
ms.locfileid: "106999959"
---
# <a name="documentimpositioncolor"></a><span data-ttu-id="f0942-104">DocumentImpositionColor</span><span class="sxs-lookup"><span data-stu-id="f0942-104">DocumentImpositionColor</span></span>

<span data-ttu-id="f0942-105">本主題並非最新的。</span><span class="sxs-lookup"><span data-stu-id="f0942-105">This topic is not current.</span></span> <span data-ttu-id="f0942-106">如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。</span><span class="sxs-lookup"><span data-stu-id="f0942-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="f0942-107">以指定的命名色彩標記的應用程式內容，必須出現在所有色彩分隔上。</span><span class="sxs-lookup"><span data-stu-id="f0942-107">Application content labeled with the specified named color MUST appear on all color separations.</span></span>

-   [<span data-ttu-id="f0942-108">項目資訊</span><span class="sxs-lookup"><span data-stu-id="f0942-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="f0942-109">結構內容</span><span class="sxs-lookup"><span data-stu-id="f0942-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="f0942-110">項目資訊</span><span class="sxs-lookup"><span data-stu-id="f0942-110">Element Information</span></span>



| <span data-ttu-id="f0942-111">Name</span><span class="sxs-lookup"><span data-stu-id="f0942-111">Name</span></span>                       |                         |
|----------------------------|-------------------------|
| <span data-ttu-id="f0942-112">項目類型</span><span class="sxs-lookup"><span data-stu-id="f0942-112">Element Type</span></span> <br/>   | <span data-ttu-id="f0942-113">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="f0942-113">ParameterDef</span></span><br/> |
| <span data-ttu-id="f0942-114">範圍前置詞</span><span class="sxs-lookup"><span data-stu-id="f0942-114">Scoping Prefix</span></span> <br/> | <span data-ttu-id="f0942-115">文件</span><span class="sxs-lookup"><span data-stu-id="f0942-115">Document</span></span><br/>     |
| <span data-ttu-id="f0942-116">注意</span><span class="sxs-lookup"><span data-stu-id="f0942-116">Notes</span></span> <br/>          | <span data-ttu-id="f0942-117">None</span><span class="sxs-lookup"><span data-stu-id="f0942-117">None</span></span><br/>         |



 

## <a name="structure-content"></a><span data-ttu-id="f0942-118">結構內容</span><span class="sxs-lookup"><span data-stu-id="f0942-118">Structure Content</span></span>

<span data-ttu-id="f0942-119">此元素的 XML 結構為：</span><span class="sxs-lookup"><span data-stu-id="f0942-119">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="f0942-120">結構屬性</span><span class="sxs-lookup"><span data-stu-id="f0942-120">Structure Properties</span></span>

<span data-ttu-id="f0942-121">下表概述 XML 結構中所定義之變數的特性。</span><span class="sxs-lookup"><span data-stu-id="f0942-121">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="f0942-122">屬性</span><span class="sxs-lookup"><span data-stu-id="f0942-122">Property</span></span>                | <span data-ttu-id="f0942-123">xsi:type</span><span class="sxs-lookup"><span data-stu-id="f0942-123">xsi:type</span></span>           | <span data-ttu-id="f0942-124">值</span><span class="sxs-lookup"><span data-stu-id="f0942-124">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="f0942-125">DataType</span><span class="sxs-lookup"><span data-stu-id="f0942-125">DataType</span></span><br/>     | <span data-ttu-id="f0942-126">字串</span><span class="sxs-lookup"><span data-stu-id="f0942-126">string</span></span><br/>  | <span data-ttu-id="f0942-127">xs:string</span><span class="sxs-lookup"><span data-stu-id="f0942-127">xs:string</span></span><br/>       |
| <span data-ttu-id="f0942-128">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="f0942-128">DefaultValue</span></span><br/> | <span data-ttu-id="f0942-129">字串</span><span class="sxs-lookup"><span data-stu-id="f0942-129">string</span></span><br/>  | <span data-ttu-id="f0942-130">未定義</span><span class="sxs-lookup"><span data-stu-id="f0942-130">undefined</span></span><br/>       |
| <span data-ttu-id="f0942-131">MaxLength</span><span class="sxs-lookup"><span data-stu-id="f0942-131">MaxLength</span></span><br/>    | <span data-ttu-id="f0942-132">整數</span><span class="sxs-lookup"><span data-stu-id="f0942-132">integer</span></span><br/> | <span data-ttu-id="f0942-133">未定義</span><span class="sxs-lookup"><span data-stu-id="f0942-133">undefined</span></span><br/>       |
| <span data-ttu-id="f0942-134">MinLength</span><span class="sxs-lookup"><span data-stu-id="f0942-134">MinLength</span></span><br/>    | <span data-ttu-id="f0942-135">整數</span><span class="sxs-lookup"><span data-stu-id="f0942-135">integer</span></span><br/> | <span data-ttu-id="f0942-136">1</span><span class="sxs-lookup"><span data-stu-id="f0942-136">1</span></span><br/>               |
| <span data-ttu-id="f0942-137">強制性</span><span class="sxs-lookup"><span data-stu-id="f0942-137">Mandatory</span></span><br/>    | <span data-ttu-id="f0942-138">字串</span><span class="sxs-lookup"><span data-stu-id="f0942-138">string</span></span><br/>  | <span data-ttu-id="f0942-139">psk：條件式</span><span class="sxs-lookup"><span data-stu-id="f0942-139">psk:Conditional</span></span><br/> |
| <span data-ttu-id="f0942-140">Unittype.pixel 表示</span><span class="sxs-lookup"><span data-stu-id="f0942-140">UnitType</span></span><br/>     | <span data-ttu-id="f0942-141">字串</span><span class="sxs-lookup"><span data-stu-id="f0942-141">string</span></span><br/>  | <span data-ttu-id="f0942-142">字元</span><span class="sxs-lookup"><span data-stu-id="f0942-142">characters</span></span><br/>      |



 

## <a name="related-topics"></a><span data-ttu-id="f0942-143">相關主題</span><span class="sxs-lookup"><span data-stu-id="f0942-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f0942-144">列印架構規格</span><span class="sxs-lookup"><span data-stu-id="f0942-144">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




