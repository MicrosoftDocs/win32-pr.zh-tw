---
description: 本主題並非最新的。 如需最新資訊，請參閱列印架構規格。
ms.assetid: 584a71cd-fc32-485e-a627-27be95c377a9
title: JobCopiesAllDocuments
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e8e606095462dc3a2eee1391121bf663de3655c
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/26/2021
ms.locfileid: "107998365"
---
# <a name="jobcopiesalldocuments"></a><span data-ttu-id="62b03-104">JobCopiesAllDocuments</span><span class="sxs-lookup"><span data-stu-id="62b03-104">JobCopiesAllDocuments</span></span>

<span data-ttu-id="62b03-105">本主題並非最新的。</span><span class="sxs-lookup"><span data-stu-id="62b03-105">This topic is not current.</span></span> <span data-ttu-id="62b03-106">如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。</span><span class="sxs-lookup"><span data-stu-id="62b03-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="62b03-107">指定作業的複本數目。</span><span class="sxs-lookup"><span data-stu-id="62b03-107">Specifies the number of copies of a job.</span></span>

-   [<span data-ttu-id="62b03-108">項目資訊</span><span class="sxs-lookup"><span data-stu-id="62b03-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="62b03-109">結構內容</span><span class="sxs-lookup"><span data-stu-id="62b03-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="62b03-110">項目資訊</span><span class="sxs-lookup"><span data-stu-id="62b03-110">Element Information</span></span>



| <span data-ttu-id="62b03-111">Name</span><span class="sxs-lookup"><span data-stu-id="62b03-111">Name</span></span> | <span data-ttu-id="62b03-112">值</span><span class="sxs-lookup"><span data-stu-id="62b03-112">Value</span></span> |
|----------------------------|-------------------------|
| <span data-ttu-id="62b03-113">項目類型</span><span class="sxs-lookup"><span data-stu-id="62b03-113">Element Type</span></span> <br/>   | <span data-ttu-id="62b03-114">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="62b03-114">ParameterDef</span></span><br/> |
| <span data-ttu-id="62b03-115">範圍前置詞</span><span class="sxs-lookup"><span data-stu-id="62b03-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="62b03-116">工作 (Job)</span><span class="sxs-lookup"><span data-stu-id="62b03-116">Job</span></span><br/>          |
| <span data-ttu-id="62b03-117">注意</span><span class="sxs-lookup"><span data-stu-id="62b03-117">Notes</span></span> <br/>          | <span data-ttu-id="62b03-118">None</span><span class="sxs-lookup"><span data-stu-id="62b03-118">None</span></span><br/>         |



 

## <a name="structure-content"></a><span data-ttu-id="62b03-119">結構內容</span><span class="sxs-lookup"><span data-stu-id="62b03-119">Structure Content</span></span>

<span data-ttu-id="62b03-120">此元素的 XML 結構為：</span><span class="sxs-lookup"><span data-stu-id="62b03-120">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="62b03-121">結構屬性</span><span class="sxs-lookup"><span data-stu-id="62b03-121">Structure Properties</span></span>

<span data-ttu-id="62b03-122">下表概述 XML 結構中所定義之變數的特性。</span><span class="sxs-lookup"><span data-stu-id="62b03-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="62b03-123">屬性</span><span class="sxs-lookup"><span data-stu-id="62b03-123">Property</span></span>                | <span data-ttu-id="62b03-124">xsi:type</span><span class="sxs-lookup"><span data-stu-id="62b03-124">xsi:type</span></span>           | <span data-ttu-id="62b03-125">值</span><span class="sxs-lookup"><span data-stu-id="62b03-125">Value</span></span>                        |
|-------------------------|--------------------|------------------------------|
| <span data-ttu-id="62b03-126">DataType</span><span class="sxs-lookup"><span data-stu-id="62b03-126">DataType</span></span><br/>     | <span data-ttu-id="62b03-127">字串</span><span class="sxs-lookup"><span data-stu-id="62b03-127">string</span></span><br/>  | <span data-ttu-id="62b03-128">xs:integer</span><span class="sxs-lookup"><span data-stu-id="62b03-128">xs:integer</span></span><br/>        |
| <span data-ttu-id="62b03-129">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="62b03-129">DefaultValue</span></span><br/> | <span data-ttu-id="62b03-130">整數</span><span class="sxs-lookup"><span data-stu-id="62b03-130">integer</span></span><br/> | <span data-ttu-id="62b03-131">1</span><span class="sxs-lookup"><span data-stu-id="62b03-131">1</span></span><br/>                 |
| <span data-ttu-id="62b03-132">MaxValue</span><span class="sxs-lookup"><span data-stu-id="62b03-132">MaxValue</span></span><br/>     | <span data-ttu-id="62b03-133">整數</span><span class="sxs-lookup"><span data-stu-id="62b03-133">integer</span></span><br/> | <span data-ttu-id="62b03-134">未定義</span><span class="sxs-lookup"><span data-stu-id="62b03-134">undefined</span></span><br/>         |
| <span data-ttu-id="62b03-135">MinValue</span><span class="sxs-lookup"><span data-stu-id="62b03-135">MinValue</span></span><br/>     | <span data-ttu-id="62b03-136">整數</span><span class="sxs-lookup"><span data-stu-id="62b03-136">integer</span></span><br/> | <span data-ttu-id="62b03-137">1</span><span class="sxs-lookup"><span data-stu-id="62b03-137">1</span></span><br/>                 |
| <span data-ttu-id="62b03-138">強制性</span><span class="sxs-lookup"><span data-stu-id="62b03-138">Mandatory</span></span><br/>    | <span data-ttu-id="62b03-139">字串</span><span class="sxs-lookup"><span data-stu-id="62b03-139">string</span></span><br/>  | <span data-ttu-id="62b03-140">psk：無條件</span><span class="sxs-lookup"><span data-stu-id="62b03-140">psk:Unconditional</span></span><br/> |
| <span data-ttu-id="62b03-141">多個</span><span class="sxs-lookup"><span data-stu-id="62b03-141">Multiple</span></span><br/>     | <span data-ttu-id="62b03-142">整數</span><span class="sxs-lookup"><span data-stu-id="62b03-142">integer</span></span><br/> | <span data-ttu-id="62b03-143">1</span><span class="sxs-lookup"><span data-stu-id="62b03-143">1</span></span><br/>                 |
| <span data-ttu-id="62b03-144">Unittype.pixel 表示</span><span class="sxs-lookup"><span data-stu-id="62b03-144">UnitType</span></span><br/>     | <span data-ttu-id="62b03-145">字串</span><span class="sxs-lookup"><span data-stu-id="62b03-145">string</span></span><br/>  | <span data-ttu-id="62b03-146">副本</span><span class="sxs-lookup"><span data-stu-id="62b03-146">copies</span></span><br/>            |



 

## <a name="related-topics"></a><span data-ttu-id="62b03-147">相關主題</span><span class="sxs-lookup"><span data-stu-id="62b03-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="62b03-148">列印架構規格</span><span class="sxs-lookup"><span data-stu-id="62b03-148">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




