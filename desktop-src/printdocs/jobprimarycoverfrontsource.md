---
description: 取得 JobPrimaryCoverFrontSource 參數的相關資訊。 本主題並非最新的。 如需最新資訊，請參閱列印架構規格。
ms.assetid: f27c5e65-87b0-47a4-a5dc-27b52082f097
title: JobPrimaryCoverFrontSource
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e4698d826e59e513d5eb171381cd1b18ea4a751
ms.sourcegitcommit: 998d50f6def8a25850fc113fc8a2df903c829c5e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/09/2021
ms.locfileid: "113549396"
---
# <a name="jobprimarycoverfrontsource"></a><span data-ttu-id="87b52-105">JobPrimaryCoverFrontSource</span><span class="sxs-lookup"><span data-stu-id="87b52-105">JobPrimaryCoverFrontSource</span></span>

<span data-ttu-id="87b52-106">本主題並非最新的。</span><span class="sxs-lookup"><span data-stu-id="87b52-106">This topic is not current.</span></span> <span data-ttu-id="87b52-107">如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。</span><span class="sxs-lookup"><span data-stu-id="87b52-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="87b52-108">指定工作的自訂封面主工作表來源。</span><span class="sxs-lookup"><span data-stu-id="87b52-108">Specifies the source for a custom front-cover primary sheet for the job.</span></span>

-   [<span data-ttu-id="87b52-109">項目資訊</span><span class="sxs-lookup"><span data-stu-id="87b52-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="87b52-110">結構內容</span><span class="sxs-lookup"><span data-stu-id="87b52-110">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="87b52-111">項目資訊</span><span class="sxs-lookup"><span data-stu-id="87b52-111">Element Information</span></span>



| <span data-ttu-id="87b52-112">Name</span><span class="sxs-lookup"><span data-stu-id="87b52-112">Name</span></span> | <span data-ttu-id="87b52-113">值</span><span class="sxs-lookup"><span data-stu-id="87b52-113">Value</span></span> |
|----------------------------|--------------------------------------------|
| <span data-ttu-id="87b52-114">項目類型</span><span class="sxs-lookup"><span data-stu-id="87b52-114">Element Type</span></span> <br/>   | <span data-ttu-id="87b52-115">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="87b52-115">ParameterDef</span></span><br/>                    |
| <span data-ttu-id="87b52-116">範圍前置詞</span><span class="sxs-lookup"><span data-stu-id="87b52-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="87b52-117">工作 (Job)</span><span class="sxs-lookup"><span data-stu-id="87b52-117">Job</span></span><br/>                             |
| <span data-ttu-id="87b52-118">備註</span><span class="sxs-lookup"><span data-stu-id="87b52-118">Notes</span></span> <br/>          | <span data-ttu-id="87b52-119">連結至 JobCoverFront 元素</span><span class="sxs-lookup"><span data-stu-id="87b52-119">Linked to JobCoverFront element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="87b52-120">結構內容</span><span class="sxs-lookup"><span data-stu-id="87b52-120">Structure Content</span></span>

<span data-ttu-id="87b52-121">此元素的 XML 結構為：</span><span class="sxs-lookup"><span data-stu-id="87b52-121">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:JobPrimaryCoverFrontSource">
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

## <a name="structure-properties"></a><span data-ttu-id="87b52-122">結構屬性</span><span class="sxs-lookup"><span data-stu-id="87b52-122">Structure Properties</span></span>

<span data-ttu-id="87b52-123">下表概述 XML 結構中所定義之變數的特性。</span><span class="sxs-lookup"><span data-stu-id="87b52-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="87b52-124">屬性</span><span class="sxs-lookup"><span data-stu-id="87b52-124">Property</span></span>                | <span data-ttu-id="87b52-125">xsi:type</span><span class="sxs-lookup"><span data-stu-id="87b52-125">xsi:type</span></span>           | <span data-ttu-id="87b52-126">值</span><span class="sxs-lookup"><span data-stu-id="87b52-126">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="87b52-127">DataType</span><span class="sxs-lookup"><span data-stu-id="87b52-127">DataType</span></span><br/>     | <span data-ttu-id="87b52-128">字串</span><span class="sxs-lookup"><span data-stu-id="87b52-128">string</span></span><br/>  | <span data-ttu-id="87b52-129">xs:string</span><span class="sxs-lookup"><span data-stu-id="87b52-129">xs:string</span></span><br/>       |
| <span data-ttu-id="87b52-130">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="87b52-130">DefaultValue</span></span><br/> | <span data-ttu-id="87b52-131">字串</span><span class="sxs-lookup"><span data-stu-id="87b52-131">string</span></span><br/>  | <span data-ttu-id="87b52-132">未定義</span><span class="sxs-lookup"><span data-stu-id="87b52-132">undefined</span></span><br/>       |
| <span data-ttu-id="87b52-133">MaxLength</span><span class="sxs-lookup"><span data-stu-id="87b52-133">MaxLength</span></span><br/>    | <span data-ttu-id="87b52-134">整數</span><span class="sxs-lookup"><span data-stu-id="87b52-134">integer</span></span><br/> | <span data-ttu-id="87b52-135">未定義</span><span class="sxs-lookup"><span data-stu-id="87b52-135">undefined</span></span><br/>       |
| <span data-ttu-id="87b52-136">MinLength</span><span class="sxs-lookup"><span data-stu-id="87b52-136">MinLength</span></span><br/>    | <span data-ttu-id="87b52-137">整數</span><span class="sxs-lookup"><span data-stu-id="87b52-137">integer</span></span><br/> | <span data-ttu-id="87b52-138">1</span><span class="sxs-lookup"><span data-stu-id="87b52-138">1</span></span><br/>               |
| <span data-ttu-id="87b52-139">強制性</span><span class="sxs-lookup"><span data-stu-id="87b52-139">Mandatory</span></span><br/>    | <span data-ttu-id="87b52-140">string</span><span class="sxs-lookup"><span data-stu-id="87b52-140">string</span></span><br/>  | <span data-ttu-id="87b52-141">psk：條件式</span><span class="sxs-lookup"><span data-stu-id="87b52-141">psk:Conditional</span></span><br/> |
| <span data-ttu-id="87b52-142">Unittype.pixel 表示</span><span class="sxs-lookup"><span data-stu-id="87b52-142">UnitType</span></span><br/>     | <span data-ttu-id="87b52-143">string</span><span class="sxs-lookup"><span data-stu-id="87b52-143">string</span></span><br/>  | <span data-ttu-id="87b52-144">字元</span><span class="sxs-lookup"><span data-stu-id="87b52-144">characters</span></span><br/>      |



 

## <a name="related-topics"></a><span data-ttu-id="87b52-145">相關主題</span><span class="sxs-lookup"><span data-stu-id="87b52-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="87b52-146">列印架構規格</span><span class="sxs-lookup"><span data-stu-id="87b52-146">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




