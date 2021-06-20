---
description: 深入瞭解 JobPrimaryCoverBackSource 元素，其指定工作的自訂後端主要工作表來源。
ms.assetid: b5c8e79c-cdae-4c53-b594-915726423b4f
title: JobPrimaryCoverBackSource
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74ed9bbc1b49e230eabc3fd7f45773a73401e058
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/19/2021
ms.locfileid: "112408691"
---
# <a name="jobprimarycoverbacksource"></a><span data-ttu-id="5c5df-103">JobPrimaryCoverBackSource</span><span class="sxs-lookup"><span data-stu-id="5c5df-103">JobPrimaryCoverBackSource</span></span>

<span data-ttu-id="5c5df-104">本主題並非最新的。</span><span class="sxs-lookup"><span data-stu-id="5c5df-104">This topic is not current.</span></span> <span data-ttu-id="5c5df-105">如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。</span><span class="sxs-lookup"><span data-stu-id="5c5df-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="5c5df-106">指定工作的自訂後置封面主工作表來源。</span><span class="sxs-lookup"><span data-stu-id="5c5df-106">Specifies the source for a custom back-cover primary sheet for the job.</span></span>

-   [<span data-ttu-id="5c5df-107">項目資訊</span><span class="sxs-lookup"><span data-stu-id="5c5df-107">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="5c5df-108">結構內容</span><span class="sxs-lookup"><span data-stu-id="5c5df-108">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="5c5df-109">項目資訊</span><span class="sxs-lookup"><span data-stu-id="5c5df-109">Element Information</span></span>



| <span data-ttu-id="5c5df-110">Name</span><span class="sxs-lookup"><span data-stu-id="5c5df-110">Name</span></span> | <span data-ttu-id="5c5df-111">值</span><span class="sxs-lookup"><span data-stu-id="5c5df-111">Value</span></span> |
|----------------------------|-------------------------------------------|
| <span data-ttu-id="5c5df-112">項目類型</span><span class="sxs-lookup"><span data-stu-id="5c5df-112">Element Type</span></span> <br/>   | <span data-ttu-id="5c5df-113">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="5c5df-113">ParameterDef</span></span><br/>                   |
| <span data-ttu-id="5c5df-114">範圍前置詞</span><span class="sxs-lookup"><span data-stu-id="5c5df-114">Scoping Prefix</span></span> <br/> | <span data-ttu-id="5c5df-115">工作 (Job)</span><span class="sxs-lookup"><span data-stu-id="5c5df-115">Job</span></span><br/>                            |
| <span data-ttu-id="5c5df-116">備註</span><span class="sxs-lookup"><span data-stu-id="5c5df-116">Notes</span></span> <br/>          | <span data-ttu-id="5c5df-117">連結至 JobCoverBack 元素</span><span class="sxs-lookup"><span data-stu-id="5c5df-117">Linked to JobCoverBack element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="5c5df-118">結構內容</span><span class="sxs-lookup"><span data-stu-id="5c5df-118">Structure Content</span></span>

<span data-ttu-id="5c5df-119">此元素的 XML 結構為：</span><span class="sxs-lookup"><span data-stu-id="5c5df-119">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:JobPrimaryCoverBackSource">
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

## <a name="structure-properties"></a><span data-ttu-id="5c5df-120">結構屬性</span><span class="sxs-lookup"><span data-stu-id="5c5df-120">Structure Properties</span></span>

<span data-ttu-id="5c5df-121">下表概述 XML 結構中所定義之變數的特性。</span><span class="sxs-lookup"><span data-stu-id="5c5df-121">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="5c5df-122">屬性</span><span class="sxs-lookup"><span data-stu-id="5c5df-122">Property</span></span>                | <span data-ttu-id="5c5df-123">xsi:type</span><span class="sxs-lookup"><span data-stu-id="5c5df-123">xsi:type</span></span>           | <span data-ttu-id="5c5df-124">值</span><span class="sxs-lookup"><span data-stu-id="5c5df-124">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="5c5df-125">DataType</span><span class="sxs-lookup"><span data-stu-id="5c5df-125">DataType</span></span><br/>     | <span data-ttu-id="5c5df-126">字串</span><span class="sxs-lookup"><span data-stu-id="5c5df-126">string</span></span><br/>  | <span data-ttu-id="5c5df-127">xs:string</span><span class="sxs-lookup"><span data-stu-id="5c5df-127">xs:string</span></span><br/>       |
| <span data-ttu-id="5c5df-128">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="5c5df-128">DefaultValue</span></span><br/> | <span data-ttu-id="5c5df-129">字串</span><span class="sxs-lookup"><span data-stu-id="5c5df-129">string</span></span><br/>  | <span data-ttu-id="5c5df-130">未定義</span><span class="sxs-lookup"><span data-stu-id="5c5df-130">undefined</span></span><br/>       |
| <span data-ttu-id="5c5df-131">MaxLength</span><span class="sxs-lookup"><span data-stu-id="5c5df-131">MaxLength</span></span><br/>    | <span data-ttu-id="5c5df-132">整數</span><span class="sxs-lookup"><span data-stu-id="5c5df-132">integer</span></span><br/> | <span data-ttu-id="5c5df-133">未定義</span><span class="sxs-lookup"><span data-stu-id="5c5df-133">undefined</span></span><br/>       |
| <span data-ttu-id="5c5df-134">MinLength</span><span class="sxs-lookup"><span data-stu-id="5c5df-134">MinLength</span></span><br/>    | <span data-ttu-id="5c5df-135">整數</span><span class="sxs-lookup"><span data-stu-id="5c5df-135">integer</span></span><br/> | <span data-ttu-id="5c5df-136">1</span><span class="sxs-lookup"><span data-stu-id="5c5df-136">1</span></span><br/>               |
| <span data-ttu-id="5c5df-137">強制性</span><span class="sxs-lookup"><span data-stu-id="5c5df-137">Mandatory</span></span><br/>    | <span data-ttu-id="5c5df-138">string</span><span class="sxs-lookup"><span data-stu-id="5c5df-138">string</span></span><br/>  | <span data-ttu-id="5c5df-139">psk：條件式</span><span class="sxs-lookup"><span data-stu-id="5c5df-139">psk:Conditional</span></span><br/> |
| <span data-ttu-id="5c5df-140">Unittype.pixel 表示</span><span class="sxs-lookup"><span data-stu-id="5c5df-140">UnitType</span></span><br/>     | <span data-ttu-id="5c5df-141">string</span><span class="sxs-lookup"><span data-stu-id="5c5df-141">string</span></span><br/>  | <span data-ttu-id="5c5df-142">字元</span><span class="sxs-lookup"><span data-stu-id="5c5df-142">characters</span></span><br/>      |



 

## <a name="related-topics"></a><span data-ttu-id="5c5df-143">相關主題</span><span class="sxs-lookup"><span data-stu-id="5c5df-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5c5df-144">列印架構規格</span><span class="sxs-lookup"><span data-stu-id="5c5df-144">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




