---
description: 本主題並非最新的。 如需最新資訊，請參閱列印架構規格。
ms.assetid: ec41d0c8-ea77-44ac-a02b-6a48237b324f
title: DocumentCoverFrontSource
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15b558a044716c5c13ae012665193f958f8ce6aa
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/26/2021
ms.locfileid: "107997895"
---
# <a name="documentcoverfrontsource"></a><span data-ttu-id="7c6d2-104">DocumentCoverFrontSource</span><span class="sxs-lookup"><span data-stu-id="7c6d2-104">DocumentCoverFrontSource</span></span>

<span data-ttu-id="7c6d2-105">本主題並非最新的。</span><span class="sxs-lookup"><span data-stu-id="7c6d2-105">This topic is not current.</span></span> <span data-ttu-id="7c6d2-106">如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。</span><span class="sxs-lookup"><span data-stu-id="7c6d2-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="7c6d2-107">指定自訂封面工作表的來源。</span><span class="sxs-lookup"><span data-stu-id="7c6d2-107">Specifies the source for a custom front-cover sheet.</span></span>

-   [<span data-ttu-id="7c6d2-108">項目資訊</span><span class="sxs-lookup"><span data-stu-id="7c6d2-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="7c6d2-109">結構內容</span><span class="sxs-lookup"><span data-stu-id="7c6d2-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="7c6d2-110">項目資訊</span><span class="sxs-lookup"><span data-stu-id="7c6d2-110">Element Information</span></span>



| <span data-ttu-id="7c6d2-111">Name</span><span class="sxs-lookup"><span data-stu-id="7c6d2-111">Name</span></span> | <span data-ttu-id="7c6d2-112">值</span><span class="sxs-lookup"><span data-stu-id="7c6d2-112">Value</span></span> |
|----------------------------|-------------------------------------------------|
| <span data-ttu-id="7c6d2-113">項目類型</span><span class="sxs-lookup"><span data-stu-id="7c6d2-113">Element Type</span></span> <br/>   | <span data-ttu-id="7c6d2-114">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="7c6d2-114">ParameterDef</span></span><br/>                         |
| <span data-ttu-id="7c6d2-115">範圍前置詞</span><span class="sxs-lookup"><span data-stu-id="7c6d2-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="7c6d2-116">文件</span><span class="sxs-lookup"><span data-stu-id="7c6d2-116">Document</span></span><br/>                             |
| <span data-ttu-id="7c6d2-117">備註</span><span class="sxs-lookup"><span data-stu-id="7c6d2-117">Notes</span></span> <br/>          | <span data-ttu-id="7c6d2-118">連結至 DocumentCoverFront 元素</span><span class="sxs-lookup"><span data-stu-id="7c6d2-118">Linked to DocumentCoverFront element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="7c6d2-119">結構內容</span><span class="sxs-lookup"><span data-stu-id="7c6d2-119">Structure Content</span></span>

<span data-ttu-id="7c6d2-120">此元素的 XML 結構為：</span><span class="sxs-lookup"><span data-stu-id="7c6d2-120">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="7c6d2-121">結構屬性</span><span class="sxs-lookup"><span data-stu-id="7c6d2-121">Structure Properties</span></span>

<span data-ttu-id="7c6d2-122">下表概述 XML 結構中所定義之變數的特性。</span><span class="sxs-lookup"><span data-stu-id="7c6d2-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="7c6d2-123">屬性</span><span class="sxs-lookup"><span data-stu-id="7c6d2-123">Property</span></span>                | <span data-ttu-id="7c6d2-124">xsi:type</span><span class="sxs-lookup"><span data-stu-id="7c6d2-124">xsi:type</span></span>           | <span data-ttu-id="7c6d2-125">值</span><span class="sxs-lookup"><span data-stu-id="7c6d2-125">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="7c6d2-126">DataType</span><span class="sxs-lookup"><span data-stu-id="7c6d2-126">DataType</span></span><br/>     | <span data-ttu-id="7c6d2-127">字串</span><span class="sxs-lookup"><span data-stu-id="7c6d2-127">string</span></span><br/>  | <span data-ttu-id="7c6d2-128">xs:string</span><span class="sxs-lookup"><span data-stu-id="7c6d2-128">xs:string</span></span><br/>       |
| <span data-ttu-id="7c6d2-129">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="7c6d2-129">DefaultValue</span></span><br/> | <span data-ttu-id="7c6d2-130">字串</span><span class="sxs-lookup"><span data-stu-id="7c6d2-130">string</span></span><br/>  | <span data-ttu-id="7c6d2-131">未定義</span><span class="sxs-lookup"><span data-stu-id="7c6d2-131">undefined</span></span><br/>       |
| <span data-ttu-id="7c6d2-132">MaxLength</span><span class="sxs-lookup"><span data-stu-id="7c6d2-132">MaxLength</span></span><br/>    | <span data-ttu-id="7c6d2-133">整數</span><span class="sxs-lookup"><span data-stu-id="7c6d2-133">integer</span></span><br/> | <span data-ttu-id="7c6d2-134">未定義</span><span class="sxs-lookup"><span data-stu-id="7c6d2-134">undefined</span></span><br/>       |
| <span data-ttu-id="7c6d2-135">MinLength</span><span class="sxs-lookup"><span data-stu-id="7c6d2-135">MinLength</span></span><br/>    | <span data-ttu-id="7c6d2-136">整數</span><span class="sxs-lookup"><span data-stu-id="7c6d2-136">integer</span></span><br/> | <span data-ttu-id="7c6d2-137">1</span><span class="sxs-lookup"><span data-stu-id="7c6d2-137">1</span></span><br/>               |
| <span data-ttu-id="7c6d2-138">強制性</span><span class="sxs-lookup"><span data-stu-id="7c6d2-138">Mandatory</span></span><br/>    | <span data-ttu-id="7c6d2-139">字串</span><span class="sxs-lookup"><span data-stu-id="7c6d2-139">string</span></span><br/>  | <span data-ttu-id="7c6d2-140">psk：條件式</span><span class="sxs-lookup"><span data-stu-id="7c6d2-140">psk:Conditional</span></span><br/> |
| <span data-ttu-id="7c6d2-141">Unittype.pixel 表示</span><span class="sxs-lookup"><span data-stu-id="7c6d2-141">UnitType</span></span><br/>     | <span data-ttu-id="7c6d2-142">字串</span><span class="sxs-lookup"><span data-stu-id="7c6d2-142">string</span></span><br/>  | <span data-ttu-id="7c6d2-143">字元</span><span class="sxs-lookup"><span data-stu-id="7c6d2-143">characters</span></span><br/>      |



 

## <a name="related-topics"></a><span data-ttu-id="7c6d2-144">相關主題</span><span class="sxs-lookup"><span data-stu-id="7c6d2-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7c6d2-145">列印架構規格</span><span class="sxs-lookup"><span data-stu-id="7c6d2-145">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




