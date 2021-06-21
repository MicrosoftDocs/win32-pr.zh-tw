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
# <a name="jobbindalldocumentsgutter"></a><span data-ttu-id="90848-103">JobBindAllDocumentsGutter</span><span class="sxs-lookup"><span data-stu-id="90848-103">JobBindAllDocumentsGutter</span></span>

<span data-ttu-id="90848-104">本主題並非最新的。</span><span class="sxs-lookup"><span data-stu-id="90848-104">This topic is not current.</span></span> <span data-ttu-id="90848-105">如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。</span><span class="sxs-lookup"><span data-stu-id="90848-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="90848-106">指定裝訂裝訂邊的寬度。</span><span class="sxs-lookup"><span data-stu-id="90848-106">Specifies the width of the binding gutter.</span></span>

-   [<span data-ttu-id="90848-107">項目資訊</span><span class="sxs-lookup"><span data-stu-id="90848-107">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="90848-108">結構內容</span><span class="sxs-lookup"><span data-stu-id="90848-108">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="90848-109">項目資訊</span><span class="sxs-lookup"><span data-stu-id="90848-109">Element Information</span></span>



| <span data-ttu-id="90848-110">Name</span><span class="sxs-lookup"><span data-stu-id="90848-110">Name</span></span> | <span data-ttu-id="90848-111">值</span><span class="sxs-lookup"><span data-stu-id="90848-111">Value</span></span> |
|----------------------------|-----------------------------------------|
| <span data-ttu-id="90848-112">項目類型</span><span class="sxs-lookup"><span data-stu-id="90848-112">Element Type</span></span> <br/>   | <span data-ttu-id="90848-113">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="90848-113">ParameterDef</span></span><br/>                 |
| <span data-ttu-id="90848-114">範圍前置詞</span><span class="sxs-lookup"><span data-stu-id="90848-114">Scoping Prefix</span></span> <br/> | <span data-ttu-id="90848-115">工作 (Job)</span><span class="sxs-lookup"><span data-stu-id="90848-115">Job</span></span> <br/>                         |
| <span data-ttu-id="90848-116">備註</span><span class="sxs-lookup"><span data-stu-id="90848-116">Notes</span></span> <br/>          | <span data-ttu-id="90848-117">連結至 JobBinding 元素</span><span class="sxs-lookup"><span data-stu-id="90848-117">Linked to JobBinding element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="90848-118">結構內容</span><span class="sxs-lookup"><span data-stu-id="90848-118">Structure Content</span></span>

<span data-ttu-id="90848-119">此元素的 XML 結構為：</span><span class="sxs-lookup"><span data-stu-id="90848-119">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="90848-120">結構屬性</span><span class="sxs-lookup"><span data-stu-id="90848-120">Structure Properties</span></span>

<span data-ttu-id="90848-121">下表概述 XML 結構中所定義之變數的特性。</span><span class="sxs-lookup"><span data-stu-id="90848-121">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="90848-122">屬性</span><span class="sxs-lookup"><span data-stu-id="90848-122">Property</span></span>                | <span data-ttu-id="90848-123">xsi:type</span><span class="sxs-lookup"><span data-stu-id="90848-123">xsi:type</span></span>           | <span data-ttu-id="90848-124">值</span><span class="sxs-lookup"><span data-stu-id="90848-124">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="90848-125">DataType</span><span class="sxs-lookup"><span data-stu-id="90848-125">DataType</span></span><br/>     | <span data-ttu-id="90848-126">字串</span><span class="sxs-lookup"><span data-stu-id="90848-126">string</span></span><br/>  | <span data-ttu-id="90848-127">xs:integer</span><span class="sxs-lookup"><span data-stu-id="90848-127">xs:integer</span></span><br/>      |
| <span data-ttu-id="90848-128">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="90848-128">DefaultValue</span></span><br/> | <span data-ttu-id="90848-129">整數</span><span class="sxs-lookup"><span data-stu-id="90848-129">integer</span></span><br/> | <span data-ttu-id="90848-130">未定義</span><span class="sxs-lookup"><span data-stu-id="90848-130">undefined</span></span><br/>       |
| <span data-ttu-id="90848-131">MaxValue</span><span class="sxs-lookup"><span data-stu-id="90848-131">MaxValue</span></span><br/>     | <span data-ttu-id="90848-132">整數</span><span class="sxs-lookup"><span data-stu-id="90848-132">integer</span></span><br/> | <span data-ttu-id="90848-133">未定義</span><span class="sxs-lookup"><span data-stu-id="90848-133">undefined</span></span><br/>       |
| <span data-ttu-id="90848-134">MinValue</span><span class="sxs-lookup"><span data-stu-id="90848-134">MinValue</span></span><br/>     | <span data-ttu-id="90848-135">整數</span><span class="sxs-lookup"><span data-stu-id="90848-135">integer</span></span><br/> | <span data-ttu-id="90848-136">未定義</span><span class="sxs-lookup"><span data-stu-id="90848-136">undefined</span></span><br/>       |
| <span data-ttu-id="90848-137">強制性</span><span class="sxs-lookup"><span data-stu-id="90848-137">Mandatory</span></span><br/>    | <span data-ttu-id="90848-138">String</span><span class="sxs-lookup"><span data-stu-id="90848-138">String</span></span><br/>  | <span data-ttu-id="90848-139">psk：條件式</span><span class="sxs-lookup"><span data-stu-id="90848-139">psk:Conditional</span></span><br/> |
| <span data-ttu-id="90848-140">多個</span><span class="sxs-lookup"><span data-stu-id="90848-140">Multiple</span></span><br/>     | <span data-ttu-id="90848-141">整數</span><span class="sxs-lookup"><span data-stu-id="90848-141">integer</span></span><br/> | <span data-ttu-id="90848-142">1</span><span class="sxs-lookup"><span data-stu-id="90848-142">1</span></span><br/>               |
| <span data-ttu-id="90848-143">Unittype.pixel 表示</span><span class="sxs-lookup"><span data-stu-id="90848-143">UnitType</span></span><br/>     | <span data-ttu-id="90848-144">string</span><span class="sxs-lookup"><span data-stu-id="90848-144">string</span></span><br/>  | <span data-ttu-id="90848-145">微米</span><span class="sxs-lookup"><span data-stu-id="90848-145">microns</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="90848-146">相關主題</span><span class="sxs-lookup"><span data-stu-id="90848-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="90848-147">列印架構規格</span><span class="sxs-lookup"><span data-stu-id="90848-147">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




