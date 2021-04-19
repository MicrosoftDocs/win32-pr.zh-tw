---
description: 本主題並非最新的。 如需最新資訊，請參閱列印架構規格。
ms.assetid: ccc2ad1c-b0c2-4c45-bc95-7c15426c2534
title: PageScalingScaleHeight
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f3f91f6b188dadbd86a18152be5228b62d21ab4
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/05/2021
ms.locfileid: "106988118"
---
# <a name="pagescalingscaleheight"></a><span data-ttu-id="ecf22-104">PageScalingScaleHeight</span><span class="sxs-lookup"><span data-stu-id="ecf22-104">PageScalingScaleHeight</span></span>

<span data-ttu-id="ecf22-105">本主題並非最新的。</span><span class="sxs-lookup"><span data-stu-id="ecf22-105">This topic is not current.</span></span> <span data-ttu-id="ecf22-106">如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。</span><span class="sxs-lookup"><span data-stu-id="ecf22-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="ecf22-107">針對自訂縮放比例指定 ImageableSizeHeight 方向的縮放比例。</span><span class="sxs-lookup"><span data-stu-id="ecf22-107">Specifies the scaling factor in the ImageableSizeHeight direction for custom scaling.</span></span>

-   [<span data-ttu-id="ecf22-108">項目資訊</span><span class="sxs-lookup"><span data-stu-id="ecf22-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="ecf22-109">結構內容</span><span class="sxs-lookup"><span data-stu-id="ecf22-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="ecf22-110">項目資訊</span><span class="sxs-lookup"><span data-stu-id="ecf22-110">Element Information</span></span>



| <span data-ttu-id="ecf22-111">Name</span><span class="sxs-lookup"><span data-stu-id="ecf22-111">Name</span></span>                       |                                                         |
|----------------------------|---------------------------------------------------------|
| <span data-ttu-id="ecf22-112">項目類型</span><span class="sxs-lookup"><span data-stu-id="ecf22-112">Element Type</span></span> <br/>   | <span data-ttu-id="ecf22-113">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="ecf22-113">ParameterDef</span></span><br/>                                 |
| <span data-ttu-id="ecf22-114">範圍前置詞</span><span class="sxs-lookup"><span data-stu-id="ecf22-114">Scoping Prefix</span></span> <br/> | <span data-ttu-id="ecf22-115">頁面</span><span class="sxs-lookup"><span data-stu-id="ecf22-115">Page</span></span><br/>                                         |
| <span data-ttu-id="ecf22-116">備註</span><span class="sxs-lookup"><span data-stu-id="ecf22-116">Notes</span></span> <br/>          | <span data-ttu-id="ecf22-117">連結至 PageScaling 元素，自訂選項</span><span class="sxs-lookup"><span data-stu-id="ecf22-117">Linked to PageScaling element, Custom option</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="ecf22-118">結構內容</span><span class="sxs-lookup"><span data-stu-id="ecf22-118">Structure Content</span></span>

<span data-ttu-id="ecf22-119">此元素的 XML 結構為：</span><span class="sxs-lookup"><span data-stu-id="ecf22-119">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageScalingScaleHeight">
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

## <a name="structure-properties"></a><span data-ttu-id="ecf22-120">結構屬性</span><span class="sxs-lookup"><span data-stu-id="ecf22-120">Structure Properties</span></span>

<span data-ttu-id="ecf22-121">下表概述 XML 結構中所定義之變數的特性。</span><span class="sxs-lookup"><span data-stu-id="ecf22-121">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="ecf22-122">屬性</span><span class="sxs-lookup"><span data-stu-id="ecf22-122">Property</span></span>                | <span data-ttu-id="ecf22-123">xsi:type</span><span class="sxs-lookup"><span data-stu-id="ecf22-123">xsi:type</span></span>           | <span data-ttu-id="ecf22-124">值</span><span class="sxs-lookup"><span data-stu-id="ecf22-124">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="ecf22-125">DataType</span><span class="sxs-lookup"><span data-stu-id="ecf22-125">DataType</span></span><br/>     | <span data-ttu-id="ecf22-126">String</span><span class="sxs-lookup"><span data-stu-id="ecf22-126">String</span></span><br/>  | <span data-ttu-id="ecf22-127">xs:integer</span><span class="sxs-lookup"><span data-stu-id="ecf22-127">xs:integer</span></span><br/>      |
| <span data-ttu-id="ecf22-128">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="ecf22-128">DefaultValue</span></span><br/> | <span data-ttu-id="ecf22-129">整數</span><span class="sxs-lookup"><span data-stu-id="ecf22-129">Integer</span></span><br/> | <span data-ttu-id="ecf22-130">未定義</span><span class="sxs-lookup"><span data-stu-id="ecf22-130">undefined</span></span><br/>       |
| <span data-ttu-id="ecf22-131">MaxValue</span><span class="sxs-lookup"><span data-stu-id="ecf22-131">MaxValue</span></span><br/>     | <span data-ttu-id="ecf22-132">整數</span><span class="sxs-lookup"><span data-stu-id="ecf22-132">Integer</span></span><br/> | <span data-ttu-id="ecf22-133">未定義</span><span class="sxs-lookup"><span data-stu-id="ecf22-133">undefined</span></span><br/>       |
| <span data-ttu-id="ecf22-134">MinValue</span><span class="sxs-lookup"><span data-stu-id="ecf22-134">MinValue</span></span><br/>     | <span data-ttu-id="ecf22-135">整數</span><span class="sxs-lookup"><span data-stu-id="ecf22-135">Integer</span></span><br/> | <span data-ttu-id="ecf22-136">1</span><span class="sxs-lookup"><span data-stu-id="ecf22-136">1</span></span><br/>               |
| <span data-ttu-id="ecf22-137">強制性</span><span class="sxs-lookup"><span data-stu-id="ecf22-137">Mandatory</span></span><br/>    | <span data-ttu-id="ecf22-138">String</span><span class="sxs-lookup"><span data-stu-id="ecf22-138">String</span></span><br/>  | <span data-ttu-id="ecf22-139">psk：條件式</span><span class="sxs-lookup"><span data-stu-id="ecf22-139">psk:Conditional</span></span><br/> |
| <span data-ttu-id="ecf22-140">多個</span><span class="sxs-lookup"><span data-stu-id="ecf22-140">Multiple</span></span><br/>     | <span data-ttu-id="ecf22-141">整數</span><span class="sxs-lookup"><span data-stu-id="ecf22-141">Integer</span></span><br/> | <span data-ttu-id="ecf22-142">1</span><span class="sxs-lookup"><span data-stu-id="ecf22-142">1</span></span><br/>               |
| <span data-ttu-id="ecf22-143">Unittype.pixel 表示</span><span class="sxs-lookup"><span data-stu-id="ecf22-143">UnitType</span></span><br/>     | <span data-ttu-id="ecf22-144">String</span><span class="sxs-lookup"><span data-stu-id="ecf22-144">String</span></span><br/>  | <span data-ttu-id="ecf22-145">percent</span><span class="sxs-lookup"><span data-stu-id="ecf22-145">percent</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="ecf22-146">相關主題</span><span class="sxs-lookup"><span data-stu-id="ecf22-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ecf22-147">列印架構規格</span><span class="sxs-lookup"><span data-stu-id="ecf22-147">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




