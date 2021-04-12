---
description: 本主題並非最新的。 如需最新資訊，請參閱列印架構規格。
ms.assetid: ec41d0c8-ea77-44ac-a02b-6a48237b324f
title: DocumentCoverFrontSource
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f67ab3f3dc3515a494dad2ab72f1413de88cd00
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/05/2021
ms.locfileid: "104195813"
---
# <a name="documentcoverfrontsource"></a><span data-ttu-id="5c930-104">DocumentCoverFrontSource</span><span class="sxs-lookup"><span data-stu-id="5c930-104">DocumentCoverFrontSource</span></span>

<span data-ttu-id="5c930-105">本主題並非最新的。</span><span class="sxs-lookup"><span data-stu-id="5c930-105">This topic is not current.</span></span> <span data-ttu-id="5c930-106">如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。</span><span class="sxs-lookup"><span data-stu-id="5c930-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="5c930-107">指定自訂封面工作表的來源。</span><span class="sxs-lookup"><span data-stu-id="5c930-107">Specifies the source for a custom front-cover sheet.</span></span>

-   [<span data-ttu-id="5c930-108">項目資訊</span><span class="sxs-lookup"><span data-stu-id="5c930-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="5c930-109">結構內容</span><span class="sxs-lookup"><span data-stu-id="5c930-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="5c930-110">項目資訊</span><span class="sxs-lookup"><span data-stu-id="5c930-110">Element Information</span></span>



| <span data-ttu-id="5c930-111">Name</span><span class="sxs-lookup"><span data-stu-id="5c930-111">Name</span></span>                       |                                                 |
|----------------------------|-------------------------------------------------|
| <span data-ttu-id="5c930-112">項目類型</span><span class="sxs-lookup"><span data-stu-id="5c930-112">Element Type</span></span> <br/>   | <span data-ttu-id="5c930-113">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="5c930-113">ParameterDef</span></span><br/>                         |
| <span data-ttu-id="5c930-114">範圍前置詞</span><span class="sxs-lookup"><span data-stu-id="5c930-114">Scoping Prefix</span></span> <br/> | <span data-ttu-id="5c930-115">文件</span><span class="sxs-lookup"><span data-stu-id="5c930-115">Document</span></span><br/>                             |
| <span data-ttu-id="5c930-116">備註</span><span class="sxs-lookup"><span data-stu-id="5c930-116">Notes</span></span> <br/>          | <span data-ttu-id="5c930-117">連結至 DocumentCoverFront 元素</span><span class="sxs-lookup"><span data-stu-id="5c930-117">Linked to DocumentCoverFront element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="5c930-118">結構內容</span><span class="sxs-lookup"><span data-stu-id="5c930-118">Structure Content</span></span>

<span data-ttu-id="5c930-119">此元素的 XML 結構為：</span><span class="sxs-lookup"><span data-stu-id="5c930-119">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:DocumentCoverFrontSource">
  <psf:Property name="psf:DataType">
    <psf:Value xsi:type="xs:string">xs:string</psf:Value>
  </psf:Property>
  <psf:Property name="psf:DefaultValue">
    <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MaxLength">
    <psf:Value xsi:type="xs:integer ">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MinLength">
    <psf:Value xsi:type="xs:integer ">1</psf:Value>
  </psf:Property>
  <psf:Property name="psf:Mandatory">
    <psf:Value xsi:type="xs:string">psk:Conditional</psf:Value>
  </psf:Property>
  <psf:Property name="psf:UnitType">
    <psf:Value xsi:type="xs:string">characters</psf:Value>
  </psf:Property>
</psf:ParameterDef>      
```

## <a name="structure-properties"></a><span data-ttu-id="5c930-120">結構屬性</span><span class="sxs-lookup"><span data-stu-id="5c930-120">Structure Properties</span></span>

<span data-ttu-id="5c930-121">下表概述 XML 結構中所定義之變數的特性。</span><span class="sxs-lookup"><span data-stu-id="5c930-121">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="5c930-122">屬性</span><span class="sxs-lookup"><span data-stu-id="5c930-122">Property</span></span>                | <span data-ttu-id="5c930-123">xsi:type</span><span class="sxs-lookup"><span data-stu-id="5c930-123">xsi:type</span></span>           | <span data-ttu-id="5c930-124">值</span><span class="sxs-lookup"><span data-stu-id="5c930-124">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="5c930-125">DataType</span><span class="sxs-lookup"><span data-stu-id="5c930-125">DataType</span></span><br/>     | <span data-ttu-id="5c930-126">字串</span><span class="sxs-lookup"><span data-stu-id="5c930-126">string</span></span><br/>  | <span data-ttu-id="5c930-127">xs:string</span><span class="sxs-lookup"><span data-stu-id="5c930-127">xs:string</span></span><br/>       |
| <span data-ttu-id="5c930-128">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="5c930-128">DefaultValue</span></span><br/> | <span data-ttu-id="5c930-129">字串</span><span class="sxs-lookup"><span data-stu-id="5c930-129">string</span></span><br/>  | <span data-ttu-id="5c930-130">未定義</span><span class="sxs-lookup"><span data-stu-id="5c930-130">undefined</span></span><br/>       |
| <span data-ttu-id="5c930-131">MaxLength</span><span class="sxs-lookup"><span data-stu-id="5c930-131">MaxLength</span></span><br/>    | <span data-ttu-id="5c930-132">整數</span><span class="sxs-lookup"><span data-stu-id="5c930-132">integer</span></span><br/> | <span data-ttu-id="5c930-133">未定義</span><span class="sxs-lookup"><span data-stu-id="5c930-133">undefined</span></span><br/>       |
| <span data-ttu-id="5c930-134">MinLength</span><span class="sxs-lookup"><span data-stu-id="5c930-134">MinLength</span></span><br/>    | <span data-ttu-id="5c930-135">整數</span><span class="sxs-lookup"><span data-stu-id="5c930-135">integer</span></span><br/> | <span data-ttu-id="5c930-136">1</span><span class="sxs-lookup"><span data-stu-id="5c930-136">1</span></span><br/>               |
| <span data-ttu-id="5c930-137">強制性</span><span class="sxs-lookup"><span data-stu-id="5c930-137">Mandatory</span></span><br/>    | <span data-ttu-id="5c930-138">字串</span><span class="sxs-lookup"><span data-stu-id="5c930-138">string</span></span><br/>  | <span data-ttu-id="5c930-139">psk：條件式</span><span class="sxs-lookup"><span data-stu-id="5c930-139">psk:Conditional</span></span><br/> |
| <span data-ttu-id="5c930-140">Unittype.pixel 表示</span><span class="sxs-lookup"><span data-stu-id="5c930-140">UnitType</span></span><br/>     | <span data-ttu-id="5c930-141">字串</span><span class="sxs-lookup"><span data-stu-id="5c930-141">string</span></span><br/>  | <span data-ttu-id="5c930-142">字元</span><span class="sxs-lookup"><span data-stu-id="5c930-142">characters</span></span><br/>      |



 

## <a name="related-topics"></a><span data-ttu-id="5c930-143">相關主題</span><span class="sxs-lookup"><span data-stu-id="5c930-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5c930-144">列印架構規格</span><span class="sxs-lookup"><span data-stu-id="5c930-144">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




