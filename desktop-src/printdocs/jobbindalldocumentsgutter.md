---
description: 本主題並非最新的。 如需最新資訊，請參閱列印架構規格。
ms.assetid: 97a00cd6-508c-47e9-a1c1-75646ca0c721
title: JobBindAllDocumentsGutter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04615b85939d483f6bd2e720afa65a88d44c1caf
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/26/2021
ms.locfileid: "107998375"
---
# <a name="jobbindalldocumentsgutter"></a><span data-ttu-id="7ffb5-104">JobBindAllDocumentsGutter</span><span class="sxs-lookup"><span data-stu-id="7ffb5-104">JobBindAllDocumentsGutter</span></span>

<span data-ttu-id="7ffb5-105">本主題並非最新的。</span><span class="sxs-lookup"><span data-stu-id="7ffb5-105">This topic is not current.</span></span> <span data-ttu-id="7ffb5-106">如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。</span><span class="sxs-lookup"><span data-stu-id="7ffb5-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="7ffb5-107">指定裝訂裝訂邊的寬度。</span><span class="sxs-lookup"><span data-stu-id="7ffb5-107">Specifies the width of the binding gutter.</span></span>

-   [<span data-ttu-id="7ffb5-108">項目資訊</span><span class="sxs-lookup"><span data-stu-id="7ffb5-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="7ffb5-109">結構內容</span><span class="sxs-lookup"><span data-stu-id="7ffb5-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="7ffb5-110">項目資訊</span><span class="sxs-lookup"><span data-stu-id="7ffb5-110">Element Information</span></span>



| <span data-ttu-id="7ffb5-111">Name</span><span class="sxs-lookup"><span data-stu-id="7ffb5-111">Name</span></span> | <span data-ttu-id="7ffb5-112">值</span><span class="sxs-lookup"><span data-stu-id="7ffb5-112">Value</span></span> |
|----------------------------|-----------------------------------------|
| <span data-ttu-id="7ffb5-113">項目類型</span><span class="sxs-lookup"><span data-stu-id="7ffb5-113">Element Type</span></span> <br/>   | <span data-ttu-id="7ffb5-114">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="7ffb5-114">ParameterDef</span></span><br/>                 |
| <span data-ttu-id="7ffb5-115">範圍前置詞</span><span class="sxs-lookup"><span data-stu-id="7ffb5-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="7ffb5-116">工作 (Job)</span><span class="sxs-lookup"><span data-stu-id="7ffb5-116">Job</span></span> <br/>                         |
| <span data-ttu-id="7ffb5-117">備註</span><span class="sxs-lookup"><span data-stu-id="7ffb5-117">Notes</span></span> <br/>          | <span data-ttu-id="7ffb5-118">連結至 JobBinding 元素</span><span class="sxs-lookup"><span data-stu-id="7ffb5-118">Linked to JobBinding element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="7ffb5-119">結構內容</span><span class="sxs-lookup"><span data-stu-id="7ffb5-119">Structure Content</span></span>

<span data-ttu-id="7ffb5-120">此元素的 XML 結構為：</span><span class="sxs-lookup"><span data-stu-id="7ffb5-120">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:JobBindAllDocumentsGutter">
  <psf:Property name="psf:DataType">
    <psf:Value xsi:type="xs:string">xs:integer</psf:Value>
  </psf:Property>
  <psf:Property name="psf:DefaultValue">
    <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MaxValue">
    <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MinValue">
    <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:Multiple">
    <psf:Value xsi:type="xs:integer">1</psf:Value>
  </psf:Property>
  <psf:Property name="psf:Mandatory">
    <psf:Value xsi:type="xs:string">psk:Conditional</psf:Value>
  </psf:Property>
  <psf:Property name="psf:UnitType">
    <psf:Value xsi:type="xs:string">microns</psf:Value>
  </psf:Property>
</psf:ParameterDef>
      
```

## <a name="structure-properties"></a><span data-ttu-id="7ffb5-121">結構屬性</span><span class="sxs-lookup"><span data-stu-id="7ffb5-121">Structure Properties</span></span>

<span data-ttu-id="7ffb5-122">下表概述 XML 結構中所定義之變數的特性。</span><span class="sxs-lookup"><span data-stu-id="7ffb5-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="7ffb5-123">屬性</span><span class="sxs-lookup"><span data-stu-id="7ffb5-123">Property</span></span>                | <span data-ttu-id="7ffb5-124">xsi:type</span><span class="sxs-lookup"><span data-stu-id="7ffb5-124">xsi:type</span></span>           | <span data-ttu-id="7ffb5-125">值</span><span class="sxs-lookup"><span data-stu-id="7ffb5-125">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="7ffb5-126">DataType</span><span class="sxs-lookup"><span data-stu-id="7ffb5-126">DataType</span></span><br/>     | <span data-ttu-id="7ffb5-127">字串</span><span class="sxs-lookup"><span data-stu-id="7ffb5-127">string</span></span><br/>  | <span data-ttu-id="7ffb5-128">xs:integer</span><span class="sxs-lookup"><span data-stu-id="7ffb5-128">xs:integer</span></span><br/>      |
| <span data-ttu-id="7ffb5-129">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="7ffb5-129">DefaultValue</span></span><br/> | <span data-ttu-id="7ffb5-130">整數</span><span class="sxs-lookup"><span data-stu-id="7ffb5-130">integer</span></span><br/> | <span data-ttu-id="7ffb5-131">未定義</span><span class="sxs-lookup"><span data-stu-id="7ffb5-131">undefined</span></span><br/>       |
| <span data-ttu-id="7ffb5-132">MaxValue</span><span class="sxs-lookup"><span data-stu-id="7ffb5-132">MaxValue</span></span><br/>     | <span data-ttu-id="7ffb5-133">整數</span><span class="sxs-lookup"><span data-stu-id="7ffb5-133">integer</span></span><br/> | <span data-ttu-id="7ffb5-134">未定義</span><span class="sxs-lookup"><span data-stu-id="7ffb5-134">undefined</span></span><br/>       |
| <span data-ttu-id="7ffb5-135">MinValue</span><span class="sxs-lookup"><span data-stu-id="7ffb5-135">MinValue</span></span><br/>     | <span data-ttu-id="7ffb5-136">整數</span><span class="sxs-lookup"><span data-stu-id="7ffb5-136">integer</span></span><br/> | <span data-ttu-id="7ffb5-137">未定義</span><span class="sxs-lookup"><span data-stu-id="7ffb5-137">undefined</span></span><br/>       |
| <span data-ttu-id="7ffb5-138">強制性</span><span class="sxs-lookup"><span data-stu-id="7ffb5-138">Mandatory</span></span><br/>    | <span data-ttu-id="7ffb5-139">String</span><span class="sxs-lookup"><span data-stu-id="7ffb5-139">String</span></span><br/>  | <span data-ttu-id="7ffb5-140">psk：條件式</span><span class="sxs-lookup"><span data-stu-id="7ffb5-140">psk:Conditional</span></span><br/> |
| <span data-ttu-id="7ffb5-141">多個</span><span class="sxs-lookup"><span data-stu-id="7ffb5-141">Multiple</span></span><br/>     | <span data-ttu-id="7ffb5-142">整數</span><span class="sxs-lookup"><span data-stu-id="7ffb5-142">integer</span></span><br/> | <span data-ttu-id="7ffb5-143">1</span><span class="sxs-lookup"><span data-stu-id="7ffb5-143">1</span></span><br/>               |
| <span data-ttu-id="7ffb5-144">Unittype.pixel 表示</span><span class="sxs-lookup"><span data-stu-id="7ffb5-144">UnitType</span></span><br/>     | <span data-ttu-id="7ffb5-145">字串</span><span class="sxs-lookup"><span data-stu-id="7ffb5-145">string</span></span><br/>  | <span data-ttu-id="7ffb5-146">微米</span><span class="sxs-lookup"><span data-stu-id="7ffb5-146">microns</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="7ffb5-147">相關主題</span><span class="sxs-lookup"><span data-stu-id="7ffb5-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7ffb5-148">列印架構規格</span><span class="sxs-lookup"><span data-stu-id="7ffb5-148">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




