---
description: 本主題並非最新的。 如需最新資訊，請參閱列印架構規格。
ms.assetid: 49a60a94-fb65-4439-bebf-3f77ea0861fe
title: PageScalingScale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 246f77c5878b74e1b149c6d4020230030fb3c5b0
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/05/2021
ms.locfileid: "106992657"
---
# <a name="pagescalingscale"></a><span data-ttu-id="ae9e3-104">PageScalingScale</span><span class="sxs-lookup"><span data-stu-id="ae9e3-104">PageScalingScale</span></span>

<span data-ttu-id="ae9e3-105">本主題並非最新的。</span><span class="sxs-lookup"><span data-stu-id="ae9e3-105">This topic is not current.</span></span> <span data-ttu-id="ae9e3-106">如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。</span><span class="sxs-lookup"><span data-stu-id="ae9e3-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="ae9e3-107">指定自訂方形縮放比例的縮放比例。</span><span class="sxs-lookup"><span data-stu-id="ae9e3-107">Specifies the scaling factor for custom square scaling.</span></span>

-   [<span data-ttu-id="ae9e3-108">項目資訊</span><span class="sxs-lookup"><span data-stu-id="ae9e3-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="ae9e3-109">結構內容</span><span class="sxs-lookup"><span data-stu-id="ae9e3-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="ae9e3-110">項目資訊</span><span class="sxs-lookup"><span data-stu-id="ae9e3-110">Element Information</span></span>



| <span data-ttu-id="ae9e3-111">Name</span><span class="sxs-lookup"><span data-stu-id="ae9e3-111">Name</span></span>                       |                                                         |
|----------------------------|---------------------------------------------------------|
| <span data-ttu-id="ae9e3-112">項目類型</span><span class="sxs-lookup"><span data-stu-id="ae9e3-112">Element Type</span></span> <br/>   | <span data-ttu-id="ae9e3-113">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="ae9e3-113">ParameterDef</span></span><br/>                                 |
| <span data-ttu-id="ae9e3-114">範圍前置詞</span><span class="sxs-lookup"><span data-stu-id="ae9e3-114">Scoping Prefix</span></span> <br/> | <span data-ttu-id="ae9e3-115">頁面</span><span class="sxs-lookup"><span data-stu-id="ae9e3-115">Page</span></span><br/>                                         |
| <span data-ttu-id="ae9e3-116">備註</span><span class="sxs-lookup"><span data-stu-id="ae9e3-116">Notes</span></span> <br/>          | <span data-ttu-id="ae9e3-117">連結至 PageScaling 元素，自訂選項</span><span class="sxs-lookup"><span data-stu-id="ae9e3-117">Linked to PageScaling element, Custom option</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="ae9e3-118">結構內容</span><span class="sxs-lookup"><span data-stu-id="ae9e3-118">Structure Content</span></span>

<span data-ttu-id="ae9e3-119">此元素的 XML 結構為：</span><span class="sxs-lookup"><span data-stu-id="ae9e3-119">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageScalingScale">
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
    <psf:Value xsi:type="xs:integer">1</psf:Value>
  </psf:Property>
  <psf:Property name="psf:Multiple">
    <psf:Value xsi:type="xs:integer">1</psf:Value>
  </psf:Property>
  <psf:Property name="psf:Mandatory">
    <psf:Value xsi:type="xs:string">psk:Conditional</psf:Value>
  </psf:Property>
  <psf:Property name="psf:UnitType">
    <psf:Value xsi:type="xs:string">percent</psf:Value>
  </psf:Property>
</psf:ParameterDef>
      
```

## <a name="structure-properties"></a><span data-ttu-id="ae9e3-120">結構屬性</span><span class="sxs-lookup"><span data-stu-id="ae9e3-120">Structure Properties</span></span>

<span data-ttu-id="ae9e3-121">下表概述 XML 結構中所定義之變數的特性。</span><span class="sxs-lookup"><span data-stu-id="ae9e3-121">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="ae9e3-122">屬性</span><span class="sxs-lookup"><span data-stu-id="ae9e3-122">Property</span></span>                | <span data-ttu-id="ae9e3-123">xsi:type</span><span class="sxs-lookup"><span data-stu-id="ae9e3-123">xsi:type</span></span>           | <span data-ttu-id="ae9e3-124">值</span><span class="sxs-lookup"><span data-stu-id="ae9e3-124">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="ae9e3-125">DataType</span><span class="sxs-lookup"><span data-stu-id="ae9e3-125">DataType</span></span><br/>     | <span data-ttu-id="ae9e3-126">字串</span><span class="sxs-lookup"><span data-stu-id="ae9e3-126">string</span></span><br/>  | <span data-ttu-id="ae9e3-127">xs:integer</span><span class="sxs-lookup"><span data-stu-id="ae9e3-127">xs:integer</span></span><br/>      |
| <span data-ttu-id="ae9e3-128">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="ae9e3-128">DefaultValue</span></span><br/> | <span data-ttu-id="ae9e3-129">整數</span><span class="sxs-lookup"><span data-stu-id="ae9e3-129">integer</span></span><br/> | <span data-ttu-id="ae9e3-130">未定義</span><span class="sxs-lookup"><span data-stu-id="ae9e3-130">undefined</span></span><br/>       |
| <span data-ttu-id="ae9e3-131">MaxValue</span><span class="sxs-lookup"><span data-stu-id="ae9e3-131">MaxValue</span></span><br/>     | <span data-ttu-id="ae9e3-132">整數</span><span class="sxs-lookup"><span data-stu-id="ae9e3-132">integer</span></span><br/> | <span data-ttu-id="ae9e3-133">未定義</span><span class="sxs-lookup"><span data-stu-id="ae9e3-133">undefined</span></span><br/>       |
| <span data-ttu-id="ae9e3-134">MinValue</span><span class="sxs-lookup"><span data-stu-id="ae9e3-134">MinValue</span></span><br/>     | <span data-ttu-id="ae9e3-135">整數</span><span class="sxs-lookup"><span data-stu-id="ae9e3-135">integer</span></span><br/> | <span data-ttu-id="ae9e3-136">1</span><span class="sxs-lookup"><span data-stu-id="ae9e3-136">1</span></span><br/>               |
| <span data-ttu-id="ae9e3-137">強制性</span><span class="sxs-lookup"><span data-stu-id="ae9e3-137">Mandatory</span></span><br/>    | <span data-ttu-id="ae9e3-138">字串</span><span class="sxs-lookup"><span data-stu-id="ae9e3-138">string</span></span><br/>  | <span data-ttu-id="ae9e3-139">psk：條件式</span><span class="sxs-lookup"><span data-stu-id="ae9e3-139">psk:Conditional</span></span><br/> |
| <span data-ttu-id="ae9e3-140">多個</span><span class="sxs-lookup"><span data-stu-id="ae9e3-140">Multiple</span></span><br/>     | <span data-ttu-id="ae9e3-141">整數</span><span class="sxs-lookup"><span data-stu-id="ae9e3-141">integer</span></span><br/> | <span data-ttu-id="ae9e3-142">1</span><span class="sxs-lookup"><span data-stu-id="ae9e3-142">1</span></span><br/>               |
| <span data-ttu-id="ae9e3-143">Unittype.pixel 表示</span><span class="sxs-lookup"><span data-stu-id="ae9e3-143">UnitType</span></span><br/>     | <span data-ttu-id="ae9e3-144">字串</span><span class="sxs-lookup"><span data-stu-id="ae9e3-144">string</span></span><br/>  | <span data-ttu-id="ae9e3-145">percent</span><span class="sxs-lookup"><span data-stu-id="ae9e3-145">percent</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="ae9e3-146">相關主題</span><span class="sxs-lookup"><span data-stu-id="ae9e3-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ae9e3-147">列印架構規格</span><span class="sxs-lookup"><span data-stu-id="ae9e3-147">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




