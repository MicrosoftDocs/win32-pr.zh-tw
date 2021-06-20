---
description: 瞭解 JobCopiesAllDocuments 元素，它會指定作業的複本數目。
ms.assetid: 584a71cd-fc32-485e-a627-27be95c377a9
title: JobCopiesAllDocuments
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05166715a5985c5ddee33fa6808d0fb6b150774b
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/19/2021
ms.locfileid: "112409031"
---
# <a name="jobcopiesalldocuments"></a><span data-ttu-id="17e2b-103">JobCopiesAllDocuments</span><span class="sxs-lookup"><span data-stu-id="17e2b-103">JobCopiesAllDocuments</span></span>

<span data-ttu-id="17e2b-104">本主題並非最新的。</span><span class="sxs-lookup"><span data-stu-id="17e2b-104">This topic is not current.</span></span> <span data-ttu-id="17e2b-105">如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。</span><span class="sxs-lookup"><span data-stu-id="17e2b-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="17e2b-106">指定作業的複本數目。</span><span class="sxs-lookup"><span data-stu-id="17e2b-106">Specifies the number of copies of a job.</span></span>

-   [<span data-ttu-id="17e2b-107">項目資訊</span><span class="sxs-lookup"><span data-stu-id="17e2b-107">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="17e2b-108">結構內容</span><span class="sxs-lookup"><span data-stu-id="17e2b-108">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="17e2b-109">項目資訊</span><span class="sxs-lookup"><span data-stu-id="17e2b-109">Element Information</span></span>



| <span data-ttu-id="17e2b-110">Name</span><span class="sxs-lookup"><span data-stu-id="17e2b-110">Name</span></span> | <span data-ttu-id="17e2b-111">值</span><span class="sxs-lookup"><span data-stu-id="17e2b-111">Value</span></span> |
|----------------------------|-------------------------|
| <span data-ttu-id="17e2b-112">項目類型</span><span class="sxs-lookup"><span data-stu-id="17e2b-112">Element Type</span></span> <br/>   | <span data-ttu-id="17e2b-113">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="17e2b-113">ParameterDef</span></span><br/> |
| <span data-ttu-id="17e2b-114">範圍前置詞</span><span class="sxs-lookup"><span data-stu-id="17e2b-114">Scoping Prefix</span></span> <br/> | <span data-ttu-id="17e2b-115">工作 (Job)</span><span class="sxs-lookup"><span data-stu-id="17e2b-115">Job</span></span><br/>          |
| <span data-ttu-id="17e2b-116">注意</span><span class="sxs-lookup"><span data-stu-id="17e2b-116">Notes</span></span> <br/>          | <span data-ttu-id="17e2b-117">None</span><span class="sxs-lookup"><span data-stu-id="17e2b-117">None</span></span><br/>         |



 

## <a name="structure-content"></a><span data-ttu-id="17e2b-118">結構內容</span><span class="sxs-lookup"><span data-stu-id="17e2b-118">Structure Content</span></span>

<span data-ttu-id="17e2b-119">此元素的 XML 結構為：</span><span class="sxs-lookup"><span data-stu-id="17e2b-119">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:JobCopiesAllDocuments">
  <psf:Property name="psf:DataType">
    <psf:Value xsi:type="xs:string">xs:integer</psf:Value>
  </psf:Property>
  <psf:Property name="psf:DefaultValue">
    <psf:Value xsi:type="xs:integer">1</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MaxValue">
    <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MinValue">
    <psf:Value xsi:type="xs:integer">1</psf:Value>
  </psf:Property>
  <psf:Property name="psf:Multiple">
    <psf:Value xsi:type="xs:integer">1</psf:Value>
  </psf:Property>
  <psf:Property name="psf:Mandatory">
    <psf:Value xsi:type="xs:string">psk:Unconditional</psf:Value>
  </psf:Property>
  <psf:Property name="psf:UnitType">
    <psf:Value xsi:type="xs:string">copies</psf:Value>
  </psf:Property>
</psf:ParameterDef>
      
```

## <a name="structure-properties"></a><span data-ttu-id="17e2b-120">結構屬性</span><span class="sxs-lookup"><span data-stu-id="17e2b-120">Structure Properties</span></span>

<span data-ttu-id="17e2b-121">下表概述 XML 結構中所定義之變數的特性。</span><span class="sxs-lookup"><span data-stu-id="17e2b-121">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="17e2b-122">屬性</span><span class="sxs-lookup"><span data-stu-id="17e2b-122">Property</span></span>                | <span data-ttu-id="17e2b-123">xsi:type</span><span class="sxs-lookup"><span data-stu-id="17e2b-123">xsi:type</span></span>           | <span data-ttu-id="17e2b-124">值</span><span class="sxs-lookup"><span data-stu-id="17e2b-124">Value</span></span>                        |
|-------------------------|--------------------|------------------------------|
| <span data-ttu-id="17e2b-125">DataType</span><span class="sxs-lookup"><span data-stu-id="17e2b-125">DataType</span></span><br/>     | <span data-ttu-id="17e2b-126">字串</span><span class="sxs-lookup"><span data-stu-id="17e2b-126">string</span></span><br/>  | <span data-ttu-id="17e2b-127">xs:integer</span><span class="sxs-lookup"><span data-stu-id="17e2b-127">xs:integer</span></span><br/>        |
| <span data-ttu-id="17e2b-128">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="17e2b-128">DefaultValue</span></span><br/> | <span data-ttu-id="17e2b-129">整數</span><span class="sxs-lookup"><span data-stu-id="17e2b-129">integer</span></span><br/> | <span data-ttu-id="17e2b-130">1</span><span class="sxs-lookup"><span data-stu-id="17e2b-130">1</span></span><br/>                 |
| <span data-ttu-id="17e2b-131">MaxValue</span><span class="sxs-lookup"><span data-stu-id="17e2b-131">MaxValue</span></span><br/>     | <span data-ttu-id="17e2b-132">整數</span><span class="sxs-lookup"><span data-stu-id="17e2b-132">integer</span></span><br/> | <span data-ttu-id="17e2b-133">未定義</span><span class="sxs-lookup"><span data-stu-id="17e2b-133">undefined</span></span><br/>         |
| <span data-ttu-id="17e2b-134">MinValue</span><span class="sxs-lookup"><span data-stu-id="17e2b-134">MinValue</span></span><br/>     | <span data-ttu-id="17e2b-135">整數</span><span class="sxs-lookup"><span data-stu-id="17e2b-135">integer</span></span><br/> | <span data-ttu-id="17e2b-136">1</span><span class="sxs-lookup"><span data-stu-id="17e2b-136">1</span></span><br/>                 |
| <span data-ttu-id="17e2b-137">強制性</span><span class="sxs-lookup"><span data-stu-id="17e2b-137">Mandatory</span></span><br/>    | <span data-ttu-id="17e2b-138">string</span><span class="sxs-lookup"><span data-stu-id="17e2b-138">string</span></span><br/>  | <span data-ttu-id="17e2b-139">psk：無條件</span><span class="sxs-lookup"><span data-stu-id="17e2b-139">psk:Unconditional</span></span><br/> |
| <span data-ttu-id="17e2b-140">多個</span><span class="sxs-lookup"><span data-stu-id="17e2b-140">Multiple</span></span><br/>     | <span data-ttu-id="17e2b-141">整數</span><span class="sxs-lookup"><span data-stu-id="17e2b-141">integer</span></span><br/> | <span data-ttu-id="17e2b-142">1</span><span class="sxs-lookup"><span data-stu-id="17e2b-142">1</span></span><br/>                 |
| <span data-ttu-id="17e2b-143">Unittype.pixel 表示</span><span class="sxs-lookup"><span data-stu-id="17e2b-143">UnitType</span></span><br/>     | <span data-ttu-id="17e2b-144">string</span><span class="sxs-lookup"><span data-stu-id="17e2b-144">string</span></span><br/>  | <span data-ttu-id="17e2b-145">副本</span><span class="sxs-lookup"><span data-stu-id="17e2b-145">copies</span></span><br/>            |



 

## <a name="related-topics"></a><span data-ttu-id="17e2b-146">相關主題</span><span class="sxs-lookup"><span data-stu-id="17e2b-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="17e2b-147">列印架構規格</span><span class="sxs-lookup"><span data-stu-id="17e2b-147">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




