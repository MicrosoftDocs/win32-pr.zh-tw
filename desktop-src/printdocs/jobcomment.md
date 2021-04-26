---
description: 本主題並非最新的。 如需最新資訊，請參閱列印架構規格。
ms.assetid: 100fe310-8e64-453f-8eaf-10abaf8b10b7
title: JobComment
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5210b80d4f81771dfa98d79d4ecf187b3ef145f5
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/26/2021
ms.locfileid: "107998345"
---
# <a name="jobcomment"></a><span data-ttu-id="ed39e-104">JobComment</span><span class="sxs-lookup"><span data-stu-id="ed39e-104">JobComment</span></span>

<span data-ttu-id="ed39e-105">本主題並非最新的。</span><span class="sxs-lookup"><span data-stu-id="ed39e-105">This topic is not current.</span></span> <span data-ttu-id="ed39e-106">如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。</span><span class="sxs-lookup"><span data-stu-id="ed39e-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="ed39e-107">指定與作業相關聯的批註。</span><span class="sxs-lookup"><span data-stu-id="ed39e-107">Specifies a comment associated with the job.</span></span> <span data-ttu-id="ed39e-108">範例：「請于完成時傳遞至房間1234」。</span><span class="sxs-lookup"><span data-stu-id="ed39e-108">Example: "Please deliver to room 1234 when completed".</span></span>

-   [<span data-ttu-id="ed39e-109">項目資訊</span><span class="sxs-lookup"><span data-stu-id="ed39e-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="ed39e-110">結構內容</span><span class="sxs-lookup"><span data-stu-id="ed39e-110">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="ed39e-111">項目資訊</span><span class="sxs-lookup"><span data-stu-id="ed39e-111">Element Information</span></span>



| <span data-ttu-id="ed39e-112">Name</span><span class="sxs-lookup"><span data-stu-id="ed39e-112">Name</span></span> | <span data-ttu-id="ed39e-113">值</span><span class="sxs-lookup"><span data-stu-id="ed39e-113">Value</span></span> |
|----------------------------|-------------------------|
| <span data-ttu-id="ed39e-114">項目類型</span><span class="sxs-lookup"><span data-stu-id="ed39e-114">Element Type</span></span> <br/>   | <span data-ttu-id="ed39e-115">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="ed39e-115">ParameterDef</span></span><br/> |
| <span data-ttu-id="ed39e-116">範圍前置詞</span><span class="sxs-lookup"><span data-stu-id="ed39e-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="ed39e-117">工作 (Job)</span><span class="sxs-lookup"><span data-stu-id="ed39e-117">Job</span></span><br/>          |
| <span data-ttu-id="ed39e-118">注意</span><span class="sxs-lookup"><span data-stu-id="ed39e-118">Notes</span></span> <br/>          | <span data-ttu-id="ed39e-119">None</span><span class="sxs-lookup"><span data-stu-id="ed39e-119">None</span></span><br/>         |



 

## <a name="structure-content"></a><span data-ttu-id="ed39e-120">結構內容</span><span class="sxs-lookup"><span data-stu-id="ed39e-120">Structure Content</span></span>

<span data-ttu-id="ed39e-121">此元素的 XML 結構如下所示：</span><span class="sxs-lookup"><span data-stu-id="ed39e-121">The XML structure of this element is as follows:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="ed39e-122">結構屬性</span><span class="sxs-lookup"><span data-stu-id="ed39e-122">Structure Properties</span></span>

<span data-ttu-id="ed39e-123">下表概述 XML 結構中所定義之變數的特性。</span><span class="sxs-lookup"><span data-stu-id="ed39e-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="ed39e-124">屬性</span><span class="sxs-lookup"><span data-stu-id="ed39e-124">Property</span></span>                | <span data-ttu-id="ed39e-125">xsi:type</span><span class="sxs-lookup"><span data-stu-id="ed39e-125">xsi:type</span></span>           | <span data-ttu-id="ed39e-126">值</span><span class="sxs-lookup"><span data-stu-id="ed39e-126">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="ed39e-127">DataType</span><span class="sxs-lookup"><span data-stu-id="ed39e-127">DataType</span></span><br/>     | <span data-ttu-id="ed39e-128">字串</span><span class="sxs-lookup"><span data-stu-id="ed39e-128">string</span></span><br/>  | <span data-ttu-id="ed39e-129">xs:string</span><span class="sxs-lookup"><span data-stu-id="ed39e-129">xs:string</span></span><br/>       |
| <span data-ttu-id="ed39e-130">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="ed39e-130">DefaultValue</span></span><br/> | <span data-ttu-id="ed39e-131">字串</span><span class="sxs-lookup"><span data-stu-id="ed39e-131">string</span></span><br/>  | <span data-ttu-id="ed39e-132">未定義</span><span class="sxs-lookup"><span data-stu-id="ed39e-132">undefined</span></span><br/>       |
| <span data-ttu-id="ed39e-133">MaxLength</span><span class="sxs-lookup"><span data-stu-id="ed39e-133">MaxLength</span></span><br/>    | <span data-ttu-id="ed39e-134">整數</span><span class="sxs-lookup"><span data-stu-id="ed39e-134">integer</span></span><br/> | <span data-ttu-id="ed39e-135">未定義</span><span class="sxs-lookup"><span data-stu-id="ed39e-135">undefined</span></span><br/>       |
| <span data-ttu-id="ed39e-136">MinLength</span><span class="sxs-lookup"><span data-stu-id="ed39e-136">MinLength</span></span><br/>    | <span data-ttu-id="ed39e-137">整數</span><span class="sxs-lookup"><span data-stu-id="ed39e-137">integer</span></span><br/> | <span data-ttu-id="ed39e-138">1</span><span class="sxs-lookup"><span data-stu-id="ed39e-138">1</span></span><br/>               |
| <span data-ttu-id="ed39e-139">強制性</span><span class="sxs-lookup"><span data-stu-id="ed39e-139">Mandatory</span></span><br/>    | <span data-ttu-id="ed39e-140">字串</span><span class="sxs-lookup"><span data-stu-id="ed39e-140">string</span></span><br/>  | <span data-ttu-id="ed39e-141">psk：條件式</span><span class="sxs-lookup"><span data-stu-id="ed39e-141">psk:Conditional</span></span><br/> |
| <span data-ttu-id="ed39e-142">Unittype.pixel 表示</span><span class="sxs-lookup"><span data-stu-id="ed39e-142">UnitType</span></span><br/>     | <span data-ttu-id="ed39e-143">字串</span><span class="sxs-lookup"><span data-stu-id="ed39e-143">string</span></span><br/>  | <span data-ttu-id="ed39e-144">字元</span><span class="sxs-lookup"><span data-stu-id="ed39e-144">characters</span></span><br/>      |



 

## <a name="related-topics"></a><span data-ttu-id="ed39e-145">相關主題</span><span class="sxs-lookup"><span data-stu-id="ed39e-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ed39e-146">列印架構規格</span><span class="sxs-lookup"><span data-stu-id="ed39e-146">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




