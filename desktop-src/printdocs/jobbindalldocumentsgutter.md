---
description: 瞭解 JobBindAllDocumentsGutter 元素，它會指定系結裝訂邊的寬度。
ms.assetid: 97a00cd6-508c-47e9-a1c1-75646ca0c721
title: JobBindAllDocumentsGutter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a42180ff9a00d1502d844b270fe5da7324825ca3
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/19/2021
ms.locfileid: "112409071"
---
# <a name="jobbindalldocumentsgutter"></a><span data-ttu-id="a67d3-103">JobBindAllDocumentsGutter</span><span class="sxs-lookup"><span data-stu-id="a67d3-103">JobBindAllDocumentsGutter</span></span>

<span data-ttu-id="a67d3-104">本主題並非最新的。</span><span class="sxs-lookup"><span data-stu-id="a67d3-104">This topic is not current.</span></span> <span data-ttu-id="a67d3-105">如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。</span><span class="sxs-lookup"><span data-stu-id="a67d3-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="a67d3-106">指定裝訂裝訂邊的寬度。</span><span class="sxs-lookup"><span data-stu-id="a67d3-106">Specifies the width of the binding gutter.</span></span>

-   [<span data-ttu-id="a67d3-107">項目資訊</span><span class="sxs-lookup"><span data-stu-id="a67d3-107">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="a67d3-108">結構內容</span><span class="sxs-lookup"><span data-stu-id="a67d3-108">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="a67d3-109">項目資訊</span><span class="sxs-lookup"><span data-stu-id="a67d3-109">Element Information</span></span>



| <span data-ttu-id="a67d3-110">Name</span><span class="sxs-lookup"><span data-stu-id="a67d3-110">Name</span></span> | <span data-ttu-id="a67d3-111">值</span><span class="sxs-lookup"><span data-stu-id="a67d3-111">Value</span></span> |
|----------------------------|-----------------------------------------|
| <span data-ttu-id="a67d3-112">項目類型</span><span class="sxs-lookup"><span data-stu-id="a67d3-112">Element Type</span></span> <br/>   | <span data-ttu-id="a67d3-113">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="a67d3-113">ParameterDef</span></span><br/>                 |
| <span data-ttu-id="a67d3-114">範圍前置詞</span><span class="sxs-lookup"><span data-stu-id="a67d3-114">Scoping Prefix</span></span> <br/> | <span data-ttu-id="a67d3-115">工作 (Job)</span><span class="sxs-lookup"><span data-stu-id="a67d3-115">Job</span></span> <br/>                         |
| <span data-ttu-id="a67d3-116">備註</span><span class="sxs-lookup"><span data-stu-id="a67d3-116">Notes</span></span> <br/>          | <span data-ttu-id="a67d3-117">連結至 JobBinding 元素</span><span class="sxs-lookup"><span data-stu-id="a67d3-117">Linked to JobBinding element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="a67d3-118">結構內容</span><span class="sxs-lookup"><span data-stu-id="a67d3-118">Structure Content</span></span>

<span data-ttu-id="a67d3-119">此元素的 XML 結構為：</span><span class="sxs-lookup"><span data-stu-id="a67d3-119">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="a67d3-120">結構屬性</span><span class="sxs-lookup"><span data-stu-id="a67d3-120">Structure Properties</span></span>

<span data-ttu-id="a67d3-121">下表概述 XML 結構中所定義之變數的特性。</span><span class="sxs-lookup"><span data-stu-id="a67d3-121">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="a67d3-122">屬性</span><span class="sxs-lookup"><span data-stu-id="a67d3-122">Property</span></span>                | <span data-ttu-id="a67d3-123">xsi:type</span><span class="sxs-lookup"><span data-stu-id="a67d3-123">xsi:type</span></span>           | <span data-ttu-id="a67d3-124">值</span><span class="sxs-lookup"><span data-stu-id="a67d3-124">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="a67d3-125">DataType</span><span class="sxs-lookup"><span data-stu-id="a67d3-125">DataType</span></span><br/>     | <span data-ttu-id="a67d3-126">字串</span><span class="sxs-lookup"><span data-stu-id="a67d3-126">string</span></span><br/>  | <span data-ttu-id="a67d3-127">xs:integer</span><span class="sxs-lookup"><span data-stu-id="a67d3-127">xs:integer</span></span><br/>      |
| <span data-ttu-id="a67d3-128">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="a67d3-128">DefaultValue</span></span><br/> | <span data-ttu-id="a67d3-129">整數</span><span class="sxs-lookup"><span data-stu-id="a67d3-129">integer</span></span><br/> | <span data-ttu-id="a67d3-130">未定義</span><span class="sxs-lookup"><span data-stu-id="a67d3-130">undefined</span></span><br/>       |
| <span data-ttu-id="a67d3-131">MaxValue</span><span class="sxs-lookup"><span data-stu-id="a67d3-131">MaxValue</span></span><br/>     | <span data-ttu-id="a67d3-132">整數</span><span class="sxs-lookup"><span data-stu-id="a67d3-132">integer</span></span><br/> | <span data-ttu-id="a67d3-133">未定義</span><span class="sxs-lookup"><span data-stu-id="a67d3-133">undefined</span></span><br/>       |
| <span data-ttu-id="a67d3-134">MinValue</span><span class="sxs-lookup"><span data-stu-id="a67d3-134">MinValue</span></span><br/>     | <span data-ttu-id="a67d3-135">整數</span><span class="sxs-lookup"><span data-stu-id="a67d3-135">integer</span></span><br/> | <span data-ttu-id="a67d3-136">未定義</span><span class="sxs-lookup"><span data-stu-id="a67d3-136">undefined</span></span><br/>       |
| <span data-ttu-id="a67d3-137">強制性</span><span class="sxs-lookup"><span data-stu-id="a67d3-137">Mandatory</span></span><br/>    | <span data-ttu-id="a67d3-138">String</span><span class="sxs-lookup"><span data-stu-id="a67d3-138">String</span></span><br/>  | <span data-ttu-id="a67d3-139">psk：條件式</span><span class="sxs-lookup"><span data-stu-id="a67d3-139">psk:Conditional</span></span><br/> |
| <span data-ttu-id="a67d3-140">多個</span><span class="sxs-lookup"><span data-stu-id="a67d3-140">Multiple</span></span><br/>     | <span data-ttu-id="a67d3-141">整數</span><span class="sxs-lookup"><span data-stu-id="a67d3-141">integer</span></span><br/> | <span data-ttu-id="a67d3-142">1</span><span class="sxs-lookup"><span data-stu-id="a67d3-142">1</span></span><br/>               |
| <span data-ttu-id="a67d3-143">Unittype.pixel 表示</span><span class="sxs-lookup"><span data-stu-id="a67d3-143">UnitType</span></span><br/>     | <span data-ttu-id="a67d3-144">string</span><span class="sxs-lookup"><span data-stu-id="a67d3-144">string</span></span><br/>  | <span data-ttu-id="a67d3-145">微米</span><span class="sxs-lookup"><span data-stu-id="a67d3-145">microns</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="a67d3-146">相關主題</span><span class="sxs-lookup"><span data-stu-id="a67d3-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a67d3-147">列印架構規格</span><span class="sxs-lookup"><span data-stu-id="a67d3-147">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




