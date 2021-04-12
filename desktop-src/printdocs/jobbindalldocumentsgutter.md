---
description: 本主題並非最新的。 如需最新資訊，請參閱列印架構規格。
ms.assetid: 97a00cd6-508c-47e9-a1c1-75646ca0c721
title: JobBindAllDocumentsGutter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 219a86f016edf820532c20fa473876265776a4ee
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/05/2021
ms.locfileid: "104195826"
---
# <a name="jobbindalldocumentsgutter"></a><span data-ttu-id="f2bfc-104">JobBindAllDocumentsGutter</span><span class="sxs-lookup"><span data-stu-id="f2bfc-104">JobBindAllDocumentsGutter</span></span>

<span data-ttu-id="f2bfc-105">本主題並非最新的。</span><span class="sxs-lookup"><span data-stu-id="f2bfc-105">This topic is not current.</span></span> <span data-ttu-id="f2bfc-106">如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。</span><span class="sxs-lookup"><span data-stu-id="f2bfc-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="f2bfc-107">指定裝訂裝訂邊的寬度。</span><span class="sxs-lookup"><span data-stu-id="f2bfc-107">Specifies the width of the binding gutter.</span></span>

-   [<span data-ttu-id="f2bfc-108">項目資訊</span><span class="sxs-lookup"><span data-stu-id="f2bfc-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="f2bfc-109">結構內容</span><span class="sxs-lookup"><span data-stu-id="f2bfc-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="f2bfc-110">項目資訊</span><span class="sxs-lookup"><span data-stu-id="f2bfc-110">Element Information</span></span>



| <span data-ttu-id="f2bfc-111">Name</span><span class="sxs-lookup"><span data-stu-id="f2bfc-111">Name</span></span>                       |                                         |
|----------------------------|-----------------------------------------|
| <span data-ttu-id="f2bfc-112">項目類型</span><span class="sxs-lookup"><span data-stu-id="f2bfc-112">Element Type</span></span> <br/>   | <span data-ttu-id="f2bfc-113">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="f2bfc-113">ParameterDef</span></span><br/>                 |
| <span data-ttu-id="f2bfc-114">範圍前置詞</span><span class="sxs-lookup"><span data-stu-id="f2bfc-114">Scoping Prefix</span></span> <br/> | <span data-ttu-id="f2bfc-115">工作 (Job)</span><span class="sxs-lookup"><span data-stu-id="f2bfc-115">Job</span></span> <br/>                         |
| <span data-ttu-id="f2bfc-116">備註</span><span class="sxs-lookup"><span data-stu-id="f2bfc-116">Notes</span></span> <br/>          | <span data-ttu-id="f2bfc-117">連結至 JobBinding 元素</span><span class="sxs-lookup"><span data-stu-id="f2bfc-117">Linked to JobBinding element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="f2bfc-118">結構內容</span><span class="sxs-lookup"><span data-stu-id="f2bfc-118">Structure Content</span></span>

<span data-ttu-id="f2bfc-119">此元素的 XML 結構為：</span><span class="sxs-lookup"><span data-stu-id="f2bfc-119">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="f2bfc-120">結構屬性</span><span class="sxs-lookup"><span data-stu-id="f2bfc-120">Structure Properties</span></span>

<span data-ttu-id="f2bfc-121">下表概述 XML 結構中所定義之變數的特性。</span><span class="sxs-lookup"><span data-stu-id="f2bfc-121">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="f2bfc-122">屬性</span><span class="sxs-lookup"><span data-stu-id="f2bfc-122">Property</span></span>                | <span data-ttu-id="f2bfc-123">xsi:type</span><span class="sxs-lookup"><span data-stu-id="f2bfc-123">xsi:type</span></span>           | <span data-ttu-id="f2bfc-124">值</span><span class="sxs-lookup"><span data-stu-id="f2bfc-124">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="f2bfc-125">DataType</span><span class="sxs-lookup"><span data-stu-id="f2bfc-125">DataType</span></span><br/>     | <span data-ttu-id="f2bfc-126">字串</span><span class="sxs-lookup"><span data-stu-id="f2bfc-126">string</span></span><br/>  | <span data-ttu-id="f2bfc-127">xs:integer</span><span class="sxs-lookup"><span data-stu-id="f2bfc-127">xs:integer</span></span><br/>      |
| <span data-ttu-id="f2bfc-128">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="f2bfc-128">DefaultValue</span></span><br/> | <span data-ttu-id="f2bfc-129">整數</span><span class="sxs-lookup"><span data-stu-id="f2bfc-129">integer</span></span><br/> | <span data-ttu-id="f2bfc-130">未定義</span><span class="sxs-lookup"><span data-stu-id="f2bfc-130">undefined</span></span><br/>       |
| <span data-ttu-id="f2bfc-131">MaxValue</span><span class="sxs-lookup"><span data-stu-id="f2bfc-131">MaxValue</span></span><br/>     | <span data-ttu-id="f2bfc-132">整數</span><span class="sxs-lookup"><span data-stu-id="f2bfc-132">integer</span></span><br/> | <span data-ttu-id="f2bfc-133">未定義</span><span class="sxs-lookup"><span data-stu-id="f2bfc-133">undefined</span></span><br/>       |
| <span data-ttu-id="f2bfc-134">MinValue</span><span class="sxs-lookup"><span data-stu-id="f2bfc-134">MinValue</span></span><br/>     | <span data-ttu-id="f2bfc-135">整數</span><span class="sxs-lookup"><span data-stu-id="f2bfc-135">integer</span></span><br/> | <span data-ttu-id="f2bfc-136">未定義</span><span class="sxs-lookup"><span data-stu-id="f2bfc-136">undefined</span></span><br/>       |
| <span data-ttu-id="f2bfc-137">強制性</span><span class="sxs-lookup"><span data-stu-id="f2bfc-137">Mandatory</span></span><br/>    | <span data-ttu-id="f2bfc-138">String</span><span class="sxs-lookup"><span data-stu-id="f2bfc-138">String</span></span><br/>  | <span data-ttu-id="f2bfc-139">psk：條件式</span><span class="sxs-lookup"><span data-stu-id="f2bfc-139">psk:Conditional</span></span><br/> |
| <span data-ttu-id="f2bfc-140">多個</span><span class="sxs-lookup"><span data-stu-id="f2bfc-140">Multiple</span></span><br/>     | <span data-ttu-id="f2bfc-141">整數</span><span class="sxs-lookup"><span data-stu-id="f2bfc-141">integer</span></span><br/> | <span data-ttu-id="f2bfc-142">1</span><span class="sxs-lookup"><span data-stu-id="f2bfc-142">1</span></span><br/>               |
| <span data-ttu-id="f2bfc-143">Unittype.pixel 表示</span><span class="sxs-lookup"><span data-stu-id="f2bfc-143">UnitType</span></span><br/>     | <span data-ttu-id="f2bfc-144">字串</span><span class="sxs-lookup"><span data-stu-id="f2bfc-144">string</span></span><br/>  | <span data-ttu-id="f2bfc-145">微米</span><span class="sxs-lookup"><span data-stu-id="f2bfc-145">microns</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="f2bfc-146">相關主題</span><span class="sxs-lookup"><span data-stu-id="f2bfc-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f2bfc-147">列印架構規格</span><span class="sxs-lookup"><span data-stu-id="f2bfc-147">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




