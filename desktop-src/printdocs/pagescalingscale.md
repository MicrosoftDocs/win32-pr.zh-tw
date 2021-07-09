---
description: 取得 PageScalingScale 參數的相關資訊。 本主題並非最新的。 如需最新資訊，請參閱列印架構規格。
ms.assetid: 49a60a94-fb65-4439-bebf-3f77ea0861fe
title: PageScalingScale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8c6cee5fc46568e3cf7f15ecd43c07c6584c856
ms.sourcegitcommit: 998d50f6def8a25850fc113fc8a2df903c829c5e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/09/2021
ms.locfileid: "113548826"
---
# <a name="pagescalingscale"></a><span data-ttu-id="73801-105">PageScalingScale</span><span class="sxs-lookup"><span data-stu-id="73801-105">PageScalingScale</span></span>

<span data-ttu-id="73801-106">本主題並非最新的。</span><span class="sxs-lookup"><span data-stu-id="73801-106">This topic is not current.</span></span> <span data-ttu-id="73801-107">如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。</span><span class="sxs-lookup"><span data-stu-id="73801-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="73801-108">指定自訂方形縮放比例的縮放比例。</span><span class="sxs-lookup"><span data-stu-id="73801-108">Specifies the scaling factor for custom square scaling.</span></span>

-   [<span data-ttu-id="73801-109">項目資訊</span><span class="sxs-lookup"><span data-stu-id="73801-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="73801-110">結構內容</span><span class="sxs-lookup"><span data-stu-id="73801-110">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="73801-111">項目資訊</span><span class="sxs-lookup"><span data-stu-id="73801-111">Element Information</span></span>



| <span data-ttu-id="73801-112">Name</span><span class="sxs-lookup"><span data-stu-id="73801-112">Name</span></span> | <span data-ttu-id="73801-113">值</span><span class="sxs-lookup"><span data-stu-id="73801-113">Value</span></span> |
|----------------------------|---------------------------------------------------------|
| <span data-ttu-id="73801-114">項目類型</span><span class="sxs-lookup"><span data-stu-id="73801-114">Element Type</span></span> <br/>   | <span data-ttu-id="73801-115">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="73801-115">ParameterDef</span></span><br/>                                 |
| <span data-ttu-id="73801-116">範圍前置詞</span><span class="sxs-lookup"><span data-stu-id="73801-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="73801-117">頁面</span><span class="sxs-lookup"><span data-stu-id="73801-117">Page</span></span><br/>                                         |
| <span data-ttu-id="73801-118">備註</span><span class="sxs-lookup"><span data-stu-id="73801-118">Notes</span></span> <br/>          | <span data-ttu-id="73801-119">連結至 PageScaling 元素，自訂選項</span><span class="sxs-lookup"><span data-stu-id="73801-119">Linked to PageScaling element, Custom option</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="73801-120">結構內容</span><span class="sxs-lookup"><span data-stu-id="73801-120">Structure Content</span></span>

<span data-ttu-id="73801-121">此元素的 XML 結構為：</span><span class="sxs-lookup"><span data-stu-id="73801-121">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="73801-122">結構屬性</span><span class="sxs-lookup"><span data-stu-id="73801-122">Structure Properties</span></span>

<span data-ttu-id="73801-123">下表概述 XML 結構中所定義之變數的特性。</span><span class="sxs-lookup"><span data-stu-id="73801-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="73801-124">屬性</span><span class="sxs-lookup"><span data-stu-id="73801-124">Property</span></span>                | <span data-ttu-id="73801-125">xsi:type</span><span class="sxs-lookup"><span data-stu-id="73801-125">xsi:type</span></span>           | <span data-ttu-id="73801-126">值</span><span class="sxs-lookup"><span data-stu-id="73801-126">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="73801-127">DataType</span><span class="sxs-lookup"><span data-stu-id="73801-127">DataType</span></span><br/>     | <span data-ttu-id="73801-128">字串</span><span class="sxs-lookup"><span data-stu-id="73801-128">string</span></span><br/>  | <span data-ttu-id="73801-129">xs:integer</span><span class="sxs-lookup"><span data-stu-id="73801-129">xs:integer</span></span><br/>      |
| <span data-ttu-id="73801-130">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="73801-130">DefaultValue</span></span><br/> | <span data-ttu-id="73801-131">整數</span><span class="sxs-lookup"><span data-stu-id="73801-131">integer</span></span><br/> | <span data-ttu-id="73801-132">未定義</span><span class="sxs-lookup"><span data-stu-id="73801-132">undefined</span></span><br/>       |
| <span data-ttu-id="73801-133">MaxValue</span><span class="sxs-lookup"><span data-stu-id="73801-133">MaxValue</span></span><br/>     | <span data-ttu-id="73801-134">整數</span><span class="sxs-lookup"><span data-stu-id="73801-134">integer</span></span><br/> | <span data-ttu-id="73801-135">未定義</span><span class="sxs-lookup"><span data-stu-id="73801-135">undefined</span></span><br/>       |
| <span data-ttu-id="73801-136">MinValue</span><span class="sxs-lookup"><span data-stu-id="73801-136">MinValue</span></span><br/>     | <span data-ttu-id="73801-137">整數</span><span class="sxs-lookup"><span data-stu-id="73801-137">integer</span></span><br/> | <span data-ttu-id="73801-138">1</span><span class="sxs-lookup"><span data-stu-id="73801-138">1</span></span><br/>               |
| <span data-ttu-id="73801-139">強制性</span><span class="sxs-lookup"><span data-stu-id="73801-139">Mandatory</span></span><br/>    | <span data-ttu-id="73801-140">string</span><span class="sxs-lookup"><span data-stu-id="73801-140">string</span></span><br/>  | <span data-ttu-id="73801-141">psk：條件式</span><span class="sxs-lookup"><span data-stu-id="73801-141">psk:Conditional</span></span><br/> |
| <span data-ttu-id="73801-142">多個</span><span class="sxs-lookup"><span data-stu-id="73801-142">Multiple</span></span><br/>     | <span data-ttu-id="73801-143">整數</span><span class="sxs-lookup"><span data-stu-id="73801-143">integer</span></span><br/> | <span data-ttu-id="73801-144">1</span><span class="sxs-lookup"><span data-stu-id="73801-144">1</span></span><br/>               |
| <span data-ttu-id="73801-145">Unittype.pixel 表示</span><span class="sxs-lookup"><span data-stu-id="73801-145">UnitType</span></span><br/>     | <span data-ttu-id="73801-146">string</span><span class="sxs-lookup"><span data-stu-id="73801-146">string</span></span><br/>  | <span data-ttu-id="73801-147">percent</span><span class="sxs-lookup"><span data-stu-id="73801-147">percent</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="73801-148">相關主題</span><span class="sxs-lookup"><span data-stu-id="73801-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="73801-149">列印架構規格</span><span class="sxs-lookup"><span data-stu-id="73801-149">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




