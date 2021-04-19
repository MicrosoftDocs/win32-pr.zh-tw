---
description: 本主題並非最新的。 如需最新資訊，請參閱列印架構規格。
ms.assetid: 100fe310-8e64-453f-8eaf-10abaf8b10b7
title: JobComment
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8ebfbd2e62c18153dd0930197b6f49cbb3480d6
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/05/2021
ms.locfileid: "106985707"
---
# <a name="jobcomment"></a><span data-ttu-id="9f2a6-104">JobComment</span><span class="sxs-lookup"><span data-stu-id="9f2a6-104">JobComment</span></span>

<span data-ttu-id="9f2a6-105">本主題並非最新的。</span><span class="sxs-lookup"><span data-stu-id="9f2a6-105">This topic is not current.</span></span> <span data-ttu-id="9f2a6-106">如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。</span><span class="sxs-lookup"><span data-stu-id="9f2a6-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="9f2a6-107">指定與作業相關聯的批註。</span><span class="sxs-lookup"><span data-stu-id="9f2a6-107">Specifies a comment associated with the job.</span></span> <span data-ttu-id="9f2a6-108">範例：「請于完成時傳遞至房間1234」。</span><span class="sxs-lookup"><span data-stu-id="9f2a6-108">Example: "Please deliver to room 1234 when completed".</span></span>

-   [<span data-ttu-id="9f2a6-109">項目資訊</span><span class="sxs-lookup"><span data-stu-id="9f2a6-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="9f2a6-110">結構內容</span><span class="sxs-lookup"><span data-stu-id="9f2a6-110">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="9f2a6-111">項目資訊</span><span class="sxs-lookup"><span data-stu-id="9f2a6-111">Element Information</span></span>



| <span data-ttu-id="9f2a6-112">Name</span><span class="sxs-lookup"><span data-stu-id="9f2a6-112">Name</span></span>                       |                         |
|----------------------------|-------------------------|
| <span data-ttu-id="9f2a6-113">項目類型</span><span class="sxs-lookup"><span data-stu-id="9f2a6-113">Element Type</span></span> <br/>   | <span data-ttu-id="9f2a6-114">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="9f2a6-114">ParameterDef</span></span><br/> |
| <span data-ttu-id="9f2a6-115">範圍前置詞</span><span class="sxs-lookup"><span data-stu-id="9f2a6-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="9f2a6-116">工作 (Job)</span><span class="sxs-lookup"><span data-stu-id="9f2a6-116">Job</span></span><br/>          |
| <span data-ttu-id="9f2a6-117">注意</span><span class="sxs-lookup"><span data-stu-id="9f2a6-117">Notes</span></span> <br/>          | <span data-ttu-id="9f2a6-118">None</span><span class="sxs-lookup"><span data-stu-id="9f2a6-118">None</span></span><br/>         |



 

## <a name="structure-content"></a><span data-ttu-id="9f2a6-119">結構內容</span><span class="sxs-lookup"><span data-stu-id="9f2a6-119">Structure Content</span></span>

<span data-ttu-id="9f2a6-120">此元素的 XML 結構如下所示：</span><span class="sxs-lookup"><span data-stu-id="9f2a6-120">The XML structure of this element is as follows:</span></span>

``` syntax
<psf:ParameterDef name="psk:JobComment">
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

## <a name="structure-properties"></a><span data-ttu-id="9f2a6-121">結構屬性</span><span class="sxs-lookup"><span data-stu-id="9f2a6-121">Structure Properties</span></span>

<span data-ttu-id="9f2a6-122">下表概述 XML 結構中所定義之變數的特性。</span><span class="sxs-lookup"><span data-stu-id="9f2a6-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="9f2a6-123">屬性</span><span class="sxs-lookup"><span data-stu-id="9f2a6-123">Property</span></span>                | <span data-ttu-id="9f2a6-124">xsi:type</span><span class="sxs-lookup"><span data-stu-id="9f2a6-124">xsi:type</span></span>           | <span data-ttu-id="9f2a6-125">值</span><span class="sxs-lookup"><span data-stu-id="9f2a6-125">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="9f2a6-126">DataType</span><span class="sxs-lookup"><span data-stu-id="9f2a6-126">DataType</span></span><br/>     | <span data-ttu-id="9f2a6-127">字串</span><span class="sxs-lookup"><span data-stu-id="9f2a6-127">string</span></span><br/>  | <span data-ttu-id="9f2a6-128">xs:string</span><span class="sxs-lookup"><span data-stu-id="9f2a6-128">xs:string</span></span><br/>       |
| <span data-ttu-id="9f2a6-129">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="9f2a6-129">DefaultValue</span></span><br/> | <span data-ttu-id="9f2a6-130">字串</span><span class="sxs-lookup"><span data-stu-id="9f2a6-130">string</span></span><br/>  | <span data-ttu-id="9f2a6-131">未定義</span><span class="sxs-lookup"><span data-stu-id="9f2a6-131">undefined</span></span><br/>       |
| <span data-ttu-id="9f2a6-132">MaxLength</span><span class="sxs-lookup"><span data-stu-id="9f2a6-132">MaxLength</span></span><br/>    | <span data-ttu-id="9f2a6-133">整數</span><span class="sxs-lookup"><span data-stu-id="9f2a6-133">integer</span></span><br/> | <span data-ttu-id="9f2a6-134">未定義</span><span class="sxs-lookup"><span data-stu-id="9f2a6-134">undefined</span></span><br/>       |
| <span data-ttu-id="9f2a6-135">MinLength</span><span class="sxs-lookup"><span data-stu-id="9f2a6-135">MinLength</span></span><br/>    | <span data-ttu-id="9f2a6-136">整數</span><span class="sxs-lookup"><span data-stu-id="9f2a6-136">integer</span></span><br/> | <span data-ttu-id="9f2a6-137">1</span><span class="sxs-lookup"><span data-stu-id="9f2a6-137">1</span></span><br/>               |
| <span data-ttu-id="9f2a6-138">強制性</span><span class="sxs-lookup"><span data-stu-id="9f2a6-138">Mandatory</span></span><br/>    | <span data-ttu-id="9f2a6-139">字串</span><span class="sxs-lookup"><span data-stu-id="9f2a6-139">string</span></span><br/>  | <span data-ttu-id="9f2a6-140">psk：條件式</span><span class="sxs-lookup"><span data-stu-id="9f2a6-140">psk:Conditional</span></span><br/> |
| <span data-ttu-id="9f2a6-141">Unittype.pixel 表示</span><span class="sxs-lookup"><span data-stu-id="9f2a6-141">UnitType</span></span><br/>     | <span data-ttu-id="9f2a6-142">字串</span><span class="sxs-lookup"><span data-stu-id="9f2a6-142">string</span></span><br/>  | <span data-ttu-id="9f2a6-143">字元</span><span class="sxs-lookup"><span data-stu-id="9f2a6-143">characters</span></span><br/>      |



 

## <a name="related-topics"></a><span data-ttu-id="9f2a6-144">相關主題</span><span class="sxs-lookup"><span data-stu-id="9f2a6-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9f2a6-145">列印架構規格</span><span class="sxs-lookup"><span data-stu-id="9f2a6-145">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




