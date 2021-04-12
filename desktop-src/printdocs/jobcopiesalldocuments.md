---
description: 本主題並非最新的。 如需最新資訊，請參閱列印架構規格。
ms.assetid: 584a71cd-fc32-485e-a627-27be95c377a9
title: JobCopiesAllDocuments
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6f8be33f98b540cab56b88df49cfb1e3c067988
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/05/2021
ms.locfileid: "103696314"
---
# <a name="jobcopiesalldocuments"></a><span data-ttu-id="bd327-104">JobCopiesAllDocuments</span><span class="sxs-lookup"><span data-stu-id="bd327-104">JobCopiesAllDocuments</span></span>

<span data-ttu-id="bd327-105">本主題並非最新的。</span><span class="sxs-lookup"><span data-stu-id="bd327-105">This topic is not current.</span></span> <span data-ttu-id="bd327-106">如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。</span><span class="sxs-lookup"><span data-stu-id="bd327-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="bd327-107">指定作業的複本數目。</span><span class="sxs-lookup"><span data-stu-id="bd327-107">Specifies the number of copies of a job.</span></span>

-   [<span data-ttu-id="bd327-108">項目資訊</span><span class="sxs-lookup"><span data-stu-id="bd327-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="bd327-109">結構內容</span><span class="sxs-lookup"><span data-stu-id="bd327-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="bd327-110">項目資訊</span><span class="sxs-lookup"><span data-stu-id="bd327-110">Element Information</span></span>



| <span data-ttu-id="bd327-111">Name</span><span class="sxs-lookup"><span data-stu-id="bd327-111">Name</span></span>                       |                         |
|----------------------------|-------------------------|
| <span data-ttu-id="bd327-112">項目類型</span><span class="sxs-lookup"><span data-stu-id="bd327-112">Element Type</span></span> <br/>   | <span data-ttu-id="bd327-113">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="bd327-113">ParameterDef</span></span><br/> |
| <span data-ttu-id="bd327-114">範圍前置詞</span><span class="sxs-lookup"><span data-stu-id="bd327-114">Scoping Prefix</span></span> <br/> | <span data-ttu-id="bd327-115">工作 (Job)</span><span class="sxs-lookup"><span data-stu-id="bd327-115">Job</span></span><br/>          |
| <span data-ttu-id="bd327-116">注意</span><span class="sxs-lookup"><span data-stu-id="bd327-116">Notes</span></span> <br/>          | <span data-ttu-id="bd327-117">None</span><span class="sxs-lookup"><span data-stu-id="bd327-117">None</span></span><br/>         |



 

## <a name="structure-content"></a><span data-ttu-id="bd327-118">結構內容</span><span class="sxs-lookup"><span data-stu-id="bd327-118">Structure Content</span></span>

<span data-ttu-id="bd327-119">此元素的 XML 結構為：</span><span class="sxs-lookup"><span data-stu-id="bd327-119">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="bd327-120">結構屬性</span><span class="sxs-lookup"><span data-stu-id="bd327-120">Structure Properties</span></span>

<span data-ttu-id="bd327-121">下表概述 XML 結構中所定義之變數的特性。</span><span class="sxs-lookup"><span data-stu-id="bd327-121">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="bd327-122">屬性</span><span class="sxs-lookup"><span data-stu-id="bd327-122">Property</span></span>                | <span data-ttu-id="bd327-123">xsi:type</span><span class="sxs-lookup"><span data-stu-id="bd327-123">xsi:type</span></span>           | <span data-ttu-id="bd327-124">值</span><span class="sxs-lookup"><span data-stu-id="bd327-124">Value</span></span>                        |
|-------------------------|--------------------|------------------------------|
| <span data-ttu-id="bd327-125">DataType</span><span class="sxs-lookup"><span data-stu-id="bd327-125">DataType</span></span><br/>     | <span data-ttu-id="bd327-126">字串</span><span class="sxs-lookup"><span data-stu-id="bd327-126">string</span></span><br/>  | <span data-ttu-id="bd327-127">xs:integer</span><span class="sxs-lookup"><span data-stu-id="bd327-127">xs:integer</span></span><br/>        |
| <span data-ttu-id="bd327-128">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="bd327-128">DefaultValue</span></span><br/> | <span data-ttu-id="bd327-129">整數</span><span class="sxs-lookup"><span data-stu-id="bd327-129">integer</span></span><br/> | <span data-ttu-id="bd327-130">1</span><span class="sxs-lookup"><span data-stu-id="bd327-130">1</span></span><br/>                 |
| <span data-ttu-id="bd327-131">MaxValue</span><span class="sxs-lookup"><span data-stu-id="bd327-131">MaxValue</span></span><br/>     | <span data-ttu-id="bd327-132">整數</span><span class="sxs-lookup"><span data-stu-id="bd327-132">integer</span></span><br/> | <span data-ttu-id="bd327-133">未定義</span><span class="sxs-lookup"><span data-stu-id="bd327-133">undefined</span></span><br/>         |
| <span data-ttu-id="bd327-134">MinValue</span><span class="sxs-lookup"><span data-stu-id="bd327-134">MinValue</span></span><br/>     | <span data-ttu-id="bd327-135">整數</span><span class="sxs-lookup"><span data-stu-id="bd327-135">integer</span></span><br/> | <span data-ttu-id="bd327-136">1</span><span class="sxs-lookup"><span data-stu-id="bd327-136">1</span></span><br/>                 |
| <span data-ttu-id="bd327-137">強制性</span><span class="sxs-lookup"><span data-stu-id="bd327-137">Mandatory</span></span><br/>    | <span data-ttu-id="bd327-138">字串</span><span class="sxs-lookup"><span data-stu-id="bd327-138">string</span></span><br/>  | <span data-ttu-id="bd327-139">psk：無條件</span><span class="sxs-lookup"><span data-stu-id="bd327-139">psk:Unconditional</span></span><br/> |
| <span data-ttu-id="bd327-140">多個</span><span class="sxs-lookup"><span data-stu-id="bd327-140">Multiple</span></span><br/>     | <span data-ttu-id="bd327-141">整數</span><span class="sxs-lookup"><span data-stu-id="bd327-141">integer</span></span><br/> | <span data-ttu-id="bd327-142">1</span><span class="sxs-lookup"><span data-stu-id="bd327-142">1</span></span><br/>                 |
| <span data-ttu-id="bd327-143">Unittype.pixel 表示</span><span class="sxs-lookup"><span data-stu-id="bd327-143">UnitType</span></span><br/>     | <span data-ttu-id="bd327-144">字串</span><span class="sxs-lookup"><span data-stu-id="bd327-144">string</span></span><br/>  | <span data-ttu-id="bd327-145">副本</span><span class="sxs-lookup"><span data-stu-id="bd327-145">copies</span></span><br/>            |



 

## <a name="related-topics"></a><span data-ttu-id="bd327-146">相關主題</span><span class="sxs-lookup"><span data-stu-id="bd327-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bd327-147">列印架構規格</span><span class="sxs-lookup"><span data-stu-id="bd327-147">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




