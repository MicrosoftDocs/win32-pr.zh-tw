---
description: 深入瞭解 JobComment 元素，它會指定與作業相關聯的批註，例如，當完成時，請傳遞到房間1234。
ms.assetid: 100fe310-8e64-453f-8eaf-10abaf8b10b7
title: JobComment
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1decf4cf3af7b3a992b07d8008579ac005d3d14e
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/19/2021
ms.locfileid: "112409041"
---
# <a name="jobcomment"></a><span data-ttu-id="e185f-103">JobComment</span><span class="sxs-lookup"><span data-stu-id="e185f-103">JobComment</span></span>

<span data-ttu-id="e185f-104">本主題並非最新的。</span><span class="sxs-lookup"><span data-stu-id="e185f-104">This topic is not current.</span></span> <span data-ttu-id="e185f-105">如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。</span><span class="sxs-lookup"><span data-stu-id="e185f-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="e185f-106">指定與作業相關聯的批註。</span><span class="sxs-lookup"><span data-stu-id="e185f-106">Specifies a comment associated with the job.</span></span> <span data-ttu-id="e185f-107">範例：「請于完成時傳遞至房間1234」。</span><span class="sxs-lookup"><span data-stu-id="e185f-107">Example: "Please deliver to room 1234 when completed".</span></span>

-   [<span data-ttu-id="e185f-108">項目資訊</span><span class="sxs-lookup"><span data-stu-id="e185f-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="e185f-109">結構內容</span><span class="sxs-lookup"><span data-stu-id="e185f-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="e185f-110">項目資訊</span><span class="sxs-lookup"><span data-stu-id="e185f-110">Element Information</span></span>



| <span data-ttu-id="e185f-111">Name</span><span class="sxs-lookup"><span data-stu-id="e185f-111">Name</span></span> | <span data-ttu-id="e185f-112">值</span><span class="sxs-lookup"><span data-stu-id="e185f-112">Value</span></span> |
|----------------------------|-------------------------|
| <span data-ttu-id="e185f-113">項目類型</span><span class="sxs-lookup"><span data-stu-id="e185f-113">Element Type</span></span> <br/>   | <span data-ttu-id="e185f-114">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="e185f-114">ParameterDef</span></span><br/> |
| <span data-ttu-id="e185f-115">範圍前置詞</span><span class="sxs-lookup"><span data-stu-id="e185f-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="e185f-116">工作 (Job)</span><span class="sxs-lookup"><span data-stu-id="e185f-116">Job</span></span><br/>          |
| <span data-ttu-id="e185f-117">注意</span><span class="sxs-lookup"><span data-stu-id="e185f-117">Notes</span></span> <br/>          | <span data-ttu-id="e185f-118">None</span><span class="sxs-lookup"><span data-stu-id="e185f-118">None</span></span><br/>         |



 

## <a name="structure-content"></a><span data-ttu-id="e185f-119">結構內容</span><span class="sxs-lookup"><span data-stu-id="e185f-119">Structure Content</span></span>

<span data-ttu-id="e185f-120">此元素的 XML 結構如下所示：</span><span class="sxs-lookup"><span data-stu-id="e185f-120">The XML structure of this element is as follows:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="e185f-121">結構屬性</span><span class="sxs-lookup"><span data-stu-id="e185f-121">Structure Properties</span></span>

<span data-ttu-id="e185f-122">下表概述 XML 結構中所定義之變數的特性。</span><span class="sxs-lookup"><span data-stu-id="e185f-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="e185f-123">屬性</span><span class="sxs-lookup"><span data-stu-id="e185f-123">Property</span></span>                | <span data-ttu-id="e185f-124">xsi:type</span><span class="sxs-lookup"><span data-stu-id="e185f-124">xsi:type</span></span>           | <span data-ttu-id="e185f-125">值</span><span class="sxs-lookup"><span data-stu-id="e185f-125">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="e185f-126">DataType</span><span class="sxs-lookup"><span data-stu-id="e185f-126">DataType</span></span><br/>     | <span data-ttu-id="e185f-127">字串</span><span class="sxs-lookup"><span data-stu-id="e185f-127">string</span></span><br/>  | <span data-ttu-id="e185f-128">xs:string</span><span class="sxs-lookup"><span data-stu-id="e185f-128">xs:string</span></span><br/>       |
| <span data-ttu-id="e185f-129">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="e185f-129">DefaultValue</span></span><br/> | <span data-ttu-id="e185f-130">字串</span><span class="sxs-lookup"><span data-stu-id="e185f-130">string</span></span><br/>  | <span data-ttu-id="e185f-131">未定義</span><span class="sxs-lookup"><span data-stu-id="e185f-131">undefined</span></span><br/>       |
| <span data-ttu-id="e185f-132">MaxLength</span><span class="sxs-lookup"><span data-stu-id="e185f-132">MaxLength</span></span><br/>    | <span data-ttu-id="e185f-133">整數</span><span class="sxs-lookup"><span data-stu-id="e185f-133">integer</span></span><br/> | <span data-ttu-id="e185f-134">未定義</span><span class="sxs-lookup"><span data-stu-id="e185f-134">undefined</span></span><br/>       |
| <span data-ttu-id="e185f-135">MinLength</span><span class="sxs-lookup"><span data-stu-id="e185f-135">MinLength</span></span><br/>    | <span data-ttu-id="e185f-136">整數</span><span class="sxs-lookup"><span data-stu-id="e185f-136">integer</span></span><br/> | <span data-ttu-id="e185f-137">1</span><span class="sxs-lookup"><span data-stu-id="e185f-137">1</span></span><br/>               |
| <span data-ttu-id="e185f-138">強制性</span><span class="sxs-lookup"><span data-stu-id="e185f-138">Mandatory</span></span><br/>    | <span data-ttu-id="e185f-139">string</span><span class="sxs-lookup"><span data-stu-id="e185f-139">string</span></span><br/>  | <span data-ttu-id="e185f-140">psk：條件式</span><span class="sxs-lookup"><span data-stu-id="e185f-140">psk:Conditional</span></span><br/> |
| <span data-ttu-id="e185f-141">Unittype.pixel 表示</span><span class="sxs-lookup"><span data-stu-id="e185f-141">UnitType</span></span><br/>     | <span data-ttu-id="e185f-142">string</span><span class="sxs-lookup"><span data-stu-id="e185f-142">string</span></span><br/>  | <span data-ttu-id="e185f-143">字元</span><span class="sxs-lookup"><span data-stu-id="e185f-143">characters</span></span><br/>      |



 

## <a name="related-topics"></a><span data-ttu-id="e185f-144">相關主題</span><span class="sxs-lookup"><span data-stu-id="e185f-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e185f-145">列印架構規格</span><span class="sxs-lookup"><span data-stu-id="e185f-145">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




