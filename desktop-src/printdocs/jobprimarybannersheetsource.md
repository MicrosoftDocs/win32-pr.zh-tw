---
description: 本主題並非最新的。 如需最新資訊，請參閱列印架構規格。
ms.assetid: ad33b2cd-8409-4782-8eb9-5f12aca8405b
title: JobPrimaryBannerSheetSource
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 556390d58df3073263a6a6b666d98c48ceed6469
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/26/2021
ms.locfileid: "107997735"
---
# <a name="jobprimarybannersheetsource"></a><span data-ttu-id="a1e3c-104">JobPrimaryBannerSheetSource</span><span class="sxs-lookup"><span data-stu-id="a1e3c-104">JobPrimaryBannerSheetSource</span></span>

<span data-ttu-id="a1e3c-105">本主題並非最新的。</span><span class="sxs-lookup"><span data-stu-id="a1e3c-105">This topic is not current.</span></span> <span data-ttu-id="a1e3c-106">如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。</span><span class="sxs-lookup"><span data-stu-id="a1e3c-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="a1e3c-107">指定作業的主要自訂橫幅工作表來源。</span><span class="sxs-lookup"><span data-stu-id="a1e3c-107">Specifies the source for a primary custom banner sheet for the job.</span></span>

-   [<span data-ttu-id="a1e3c-108">項目資訊</span><span class="sxs-lookup"><span data-stu-id="a1e3c-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="a1e3c-109">結構內容</span><span class="sxs-lookup"><span data-stu-id="a1e3c-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="a1e3c-110">項目資訊</span><span class="sxs-lookup"><span data-stu-id="a1e3c-110">Element Information</span></span>



| <span data-ttu-id="a1e3c-111">Name</span><span class="sxs-lookup"><span data-stu-id="a1e3c-111">Name</span></span> | <span data-ttu-id="a1e3c-112">值</span><span class="sxs-lookup"><span data-stu-id="a1e3c-112">Value</span></span> |
|----------------------------|---------------------------------------------|
| <span data-ttu-id="a1e3c-113">項目類型</span><span class="sxs-lookup"><span data-stu-id="a1e3c-113">Element Type</span></span> <br/>   | <span data-ttu-id="a1e3c-114">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="a1e3c-114">ParameterDef</span></span><br/>                     |
| <span data-ttu-id="a1e3c-115">範圍前置詞</span><span class="sxs-lookup"><span data-stu-id="a1e3c-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="a1e3c-116">工作 (Job)</span><span class="sxs-lookup"><span data-stu-id="a1e3c-116">Job</span></span><br/>                              |
| <span data-ttu-id="a1e3c-117">備註</span><span class="sxs-lookup"><span data-stu-id="a1e3c-117">Notes</span></span> <br/>          | <span data-ttu-id="a1e3c-118">連結至 JobBannerSheet 元素</span><span class="sxs-lookup"><span data-stu-id="a1e3c-118">Linked to JobBannerSheet element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="a1e3c-119">結構內容</span><span class="sxs-lookup"><span data-stu-id="a1e3c-119">Structure Content</span></span>

<span data-ttu-id="a1e3c-120">此元素的 XML 結構為：</span><span class="sxs-lookup"><span data-stu-id="a1e3c-120">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="a1e3c-121">結構屬性</span><span class="sxs-lookup"><span data-stu-id="a1e3c-121">Structure Properties</span></span>

<span data-ttu-id="a1e3c-122">下表概述 XML 結構中所定義之變數的特性。</span><span class="sxs-lookup"><span data-stu-id="a1e3c-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="a1e3c-123">屬性</span><span class="sxs-lookup"><span data-stu-id="a1e3c-123">Property</span></span>                | <span data-ttu-id="a1e3c-124">xsi:type</span><span class="sxs-lookup"><span data-stu-id="a1e3c-124">xsi:type</span></span>           | <span data-ttu-id="a1e3c-125">值</span><span class="sxs-lookup"><span data-stu-id="a1e3c-125">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="a1e3c-126">DataType</span><span class="sxs-lookup"><span data-stu-id="a1e3c-126">DataType</span></span><br/>     | <span data-ttu-id="a1e3c-127">字串</span><span class="sxs-lookup"><span data-stu-id="a1e3c-127">string</span></span><br/>  | <span data-ttu-id="a1e3c-128">xs:string</span><span class="sxs-lookup"><span data-stu-id="a1e3c-128">xs:string</span></span><br/>       |
| <span data-ttu-id="a1e3c-129">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="a1e3c-129">DefaultValue</span></span><br/> | <span data-ttu-id="a1e3c-130">字串</span><span class="sxs-lookup"><span data-stu-id="a1e3c-130">string</span></span><br/>  | <span data-ttu-id="a1e3c-131">未定義</span><span class="sxs-lookup"><span data-stu-id="a1e3c-131">undefined</span></span><br/>       |
| <span data-ttu-id="a1e3c-132">MaxLength</span><span class="sxs-lookup"><span data-stu-id="a1e3c-132">MaxLength</span></span><br/>    | <span data-ttu-id="a1e3c-133">整數</span><span class="sxs-lookup"><span data-stu-id="a1e3c-133">integer</span></span><br/> | <span data-ttu-id="a1e3c-134">未定義</span><span class="sxs-lookup"><span data-stu-id="a1e3c-134">undefined</span></span><br/>       |
| <span data-ttu-id="a1e3c-135">MinLength</span><span class="sxs-lookup"><span data-stu-id="a1e3c-135">MinLength</span></span><br/>    | <span data-ttu-id="a1e3c-136">整數</span><span class="sxs-lookup"><span data-stu-id="a1e3c-136">integer</span></span><br/> | <span data-ttu-id="a1e3c-137">1</span><span class="sxs-lookup"><span data-stu-id="a1e3c-137">1</span></span><br/>               |
| <span data-ttu-id="a1e3c-138">強制性</span><span class="sxs-lookup"><span data-stu-id="a1e3c-138">Mandatory</span></span><br/>    | <span data-ttu-id="a1e3c-139">字串</span><span class="sxs-lookup"><span data-stu-id="a1e3c-139">string</span></span><br/>  | <span data-ttu-id="a1e3c-140">psk：條件式</span><span class="sxs-lookup"><span data-stu-id="a1e3c-140">psk:Conditional</span></span><br/> |
| <span data-ttu-id="a1e3c-141">Unittype.pixel 表示</span><span class="sxs-lookup"><span data-stu-id="a1e3c-141">UnitType</span></span><br/>     | <span data-ttu-id="a1e3c-142">字串</span><span class="sxs-lookup"><span data-stu-id="a1e3c-142">string</span></span><br/>  | <span data-ttu-id="a1e3c-143">字元</span><span class="sxs-lookup"><span data-stu-id="a1e3c-143">characters</span></span><br/>      |



 

## <a name="related-topics"></a><span data-ttu-id="a1e3c-144">相關主題</span><span class="sxs-lookup"><span data-stu-id="a1e3c-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a1e3c-145">列印架構規格</span><span class="sxs-lookup"><span data-stu-id="a1e3c-145">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




