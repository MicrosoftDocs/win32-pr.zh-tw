---
description: 本主題並非最新的。 如需最新資訊，請參閱列印架構規格。
ms.assetid: ad33b2cd-8409-4782-8eb9-5f12aca8405b
title: JobPrimaryBannerSheetSource
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c86e840c3507fce80bda0f4c31efe8b0d714242
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/05/2021
ms.locfileid: "104321727"
---
# <a name="jobprimarybannersheetsource"></a><span data-ttu-id="a4c9b-104">JobPrimaryBannerSheetSource</span><span class="sxs-lookup"><span data-stu-id="a4c9b-104">JobPrimaryBannerSheetSource</span></span>

<span data-ttu-id="a4c9b-105">本主題並非最新的。</span><span class="sxs-lookup"><span data-stu-id="a4c9b-105">This topic is not current.</span></span> <span data-ttu-id="a4c9b-106">如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。</span><span class="sxs-lookup"><span data-stu-id="a4c9b-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="a4c9b-107">指定作業的主要自訂橫幅工作表來源。</span><span class="sxs-lookup"><span data-stu-id="a4c9b-107">Specifies the source for a primary custom banner sheet for the job.</span></span>

-   [<span data-ttu-id="a4c9b-108">項目資訊</span><span class="sxs-lookup"><span data-stu-id="a4c9b-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="a4c9b-109">結構內容</span><span class="sxs-lookup"><span data-stu-id="a4c9b-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="a4c9b-110">項目資訊</span><span class="sxs-lookup"><span data-stu-id="a4c9b-110">Element Information</span></span>



| <span data-ttu-id="a4c9b-111">Name</span><span class="sxs-lookup"><span data-stu-id="a4c9b-111">Name</span></span>                       |                                             |
|----------------------------|---------------------------------------------|
| <span data-ttu-id="a4c9b-112">項目類型</span><span class="sxs-lookup"><span data-stu-id="a4c9b-112">Element Type</span></span> <br/>   | <span data-ttu-id="a4c9b-113">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="a4c9b-113">ParameterDef</span></span><br/>                     |
| <span data-ttu-id="a4c9b-114">範圍前置詞</span><span class="sxs-lookup"><span data-stu-id="a4c9b-114">Scoping Prefix</span></span> <br/> | <span data-ttu-id="a4c9b-115">工作 (Job)</span><span class="sxs-lookup"><span data-stu-id="a4c9b-115">Job</span></span><br/>                              |
| <span data-ttu-id="a4c9b-116">備註</span><span class="sxs-lookup"><span data-stu-id="a4c9b-116">Notes</span></span> <br/>          | <span data-ttu-id="a4c9b-117">連結至 JobBannerSheet 元素</span><span class="sxs-lookup"><span data-stu-id="a4c9b-117">Linked to JobBannerSheet element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="a4c9b-118">結構內容</span><span class="sxs-lookup"><span data-stu-id="a4c9b-118">Structure Content</span></span>

<span data-ttu-id="a4c9b-119">此元素的 XML 結構為：</span><span class="sxs-lookup"><span data-stu-id="a4c9b-119">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:JobPrimaryBannerSheetSource">
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

## <a name="structure-properties"></a><span data-ttu-id="a4c9b-120">結構屬性</span><span class="sxs-lookup"><span data-stu-id="a4c9b-120">Structure Properties</span></span>

<span data-ttu-id="a4c9b-121">下表概述 XML 結構中所定義之變數的特性。</span><span class="sxs-lookup"><span data-stu-id="a4c9b-121">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="a4c9b-122">屬性</span><span class="sxs-lookup"><span data-stu-id="a4c9b-122">Property</span></span>                | <span data-ttu-id="a4c9b-123">xsi:type</span><span class="sxs-lookup"><span data-stu-id="a4c9b-123">xsi:type</span></span>           | <span data-ttu-id="a4c9b-124">值</span><span class="sxs-lookup"><span data-stu-id="a4c9b-124">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="a4c9b-125">DataType</span><span class="sxs-lookup"><span data-stu-id="a4c9b-125">DataType</span></span><br/>     | <span data-ttu-id="a4c9b-126">字串</span><span class="sxs-lookup"><span data-stu-id="a4c9b-126">string</span></span><br/>  | <span data-ttu-id="a4c9b-127">xs:string</span><span class="sxs-lookup"><span data-stu-id="a4c9b-127">xs:string</span></span><br/>       |
| <span data-ttu-id="a4c9b-128">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="a4c9b-128">DefaultValue</span></span><br/> | <span data-ttu-id="a4c9b-129">字串</span><span class="sxs-lookup"><span data-stu-id="a4c9b-129">string</span></span><br/>  | <span data-ttu-id="a4c9b-130">未定義</span><span class="sxs-lookup"><span data-stu-id="a4c9b-130">undefined</span></span><br/>       |
| <span data-ttu-id="a4c9b-131">MaxLength</span><span class="sxs-lookup"><span data-stu-id="a4c9b-131">MaxLength</span></span><br/>    | <span data-ttu-id="a4c9b-132">整數</span><span class="sxs-lookup"><span data-stu-id="a4c9b-132">integer</span></span><br/> | <span data-ttu-id="a4c9b-133">未定義</span><span class="sxs-lookup"><span data-stu-id="a4c9b-133">undefined</span></span><br/>       |
| <span data-ttu-id="a4c9b-134">MinLength</span><span class="sxs-lookup"><span data-stu-id="a4c9b-134">MinLength</span></span><br/>    | <span data-ttu-id="a4c9b-135">整數</span><span class="sxs-lookup"><span data-stu-id="a4c9b-135">integer</span></span><br/> | <span data-ttu-id="a4c9b-136">1</span><span class="sxs-lookup"><span data-stu-id="a4c9b-136">1</span></span><br/>               |
| <span data-ttu-id="a4c9b-137">強制性</span><span class="sxs-lookup"><span data-stu-id="a4c9b-137">Mandatory</span></span><br/>    | <span data-ttu-id="a4c9b-138">字串</span><span class="sxs-lookup"><span data-stu-id="a4c9b-138">string</span></span><br/>  | <span data-ttu-id="a4c9b-139">psk：條件式</span><span class="sxs-lookup"><span data-stu-id="a4c9b-139">psk:Conditional</span></span><br/> |
| <span data-ttu-id="a4c9b-140">Unittype.pixel 表示</span><span class="sxs-lookup"><span data-stu-id="a4c9b-140">UnitType</span></span><br/>     | <span data-ttu-id="a4c9b-141">字串</span><span class="sxs-lookup"><span data-stu-id="a4c9b-141">string</span></span><br/>  | <span data-ttu-id="a4c9b-142">字元</span><span class="sxs-lookup"><span data-stu-id="a4c9b-142">characters</span></span><br/>      |



 

## <a name="related-topics"></a><span data-ttu-id="a4c9b-143">相關主題</span><span class="sxs-lookup"><span data-stu-id="a4c9b-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a4c9b-144">列印架構規格</span><span class="sxs-lookup"><span data-stu-id="a4c9b-144">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




