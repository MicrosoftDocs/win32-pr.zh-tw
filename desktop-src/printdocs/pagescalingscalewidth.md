---
description: 取得 PageScalingScaleWidth 參數的相關資訊。 本主題並非最新的。 如需最新資訊，請參閱列印架構規格。
ms.assetid: 0de776f3-ae09-49f4-a829-b3c0e2ab5bbc
title: PageScalingScaleWidth
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75b6180395eb656ee40d8558f7208fec2ad2fce8
ms.sourcegitcommit: 998d50f6def8a25850fc113fc8a2df903c829c5e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/09/2021
ms.locfileid: "113548796"
---
# <a name="pagescalingscalewidth"></a><span data-ttu-id="d85a3-105">PageScalingScaleWidth</span><span class="sxs-lookup"><span data-stu-id="d85a3-105">PageScalingScaleWidth</span></span>

<span data-ttu-id="d85a3-106">本主題並非最新的。</span><span class="sxs-lookup"><span data-stu-id="d85a3-106">This topic is not current.</span></span> <span data-ttu-id="d85a3-107">如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。</span><span class="sxs-lookup"><span data-stu-id="d85a3-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="d85a3-108">針對自訂縮放比例指定 ImageableSizeWidth 方向的縮放比例。</span><span class="sxs-lookup"><span data-stu-id="d85a3-108">Specifies the scaling factor in the ImageableSizeWidth direction for custom scaling.</span></span>

-   [<span data-ttu-id="d85a3-109">項目資訊</span><span class="sxs-lookup"><span data-stu-id="d85a3-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="d85a3-110">結構內容</span><span class="sxs-lookup"><span data-stu-id="d85a3-110">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="d85a3-111">項目資訊</span><span class="sxs-lookup"><span data-stu-id="d85a3-111">Element Information</span></span>



| <span data-ttu-id="d85a3-112">Name</span><span class="sxs-lookup"><span data-stu-id="d85a3-112">Name</span></span> | <span data-ttu-id="d85a3-113">值</span><span class="sxs-lookup"><span data-stu-id="d85a3-113">Value</span></span> |
|----------------------------|---------------------------------------------------------|
| <span data-ttu-id="d85a3-114">項目類型</span><span class="sxs-lookup"><span data-stu-id="d85a3-114">Element Type</span></span> <br/>   | <span data-ttu-id="d85a3-115">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="d85a3-115">ParameterDef</span></span><br/>                                 |
| <span data-ttu-id="d85a3-116">範圍前置詞</span><span class="sxs-lookup"><span data-stu-id="d85a3-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="d85a3-117">頁面</span><span class="sxs-lookup"><span data-stu-id="d85a3-117">Page</span></span><br/>                                         |
| <span data-ttu-id="d85a3-118">備註</span><span class="sxs-lookup"><span data-stu-id="d85a3-118">Notes</span></span> <br/>          | <span data-ttu-id="d85a3-119">連結至 PageScaling 元素，自訂選項</span><span class="sxs-lookup"><span data-stu-id="d85a3-119">Linked to PageScaling element, Custom option</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="d85a3-120">結構內容</span><span class="sxs-lookup"><span data-stu-id="d85a3-120">Structure Content</span></span>

<span data-ttu-id="d85a3-121">此元素的 XML 結構為：</span><span class="sxs-lookup"><span data-stu-id="d85a3-121">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageScalingScaleWidth">
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

## <a name="structure-properties"></a><span data-ttu-id="d85a3-122">結構屬性</span><span class="sxs-lookup"><span data-stu-id="d85a3-122">Structure Properties</span></span>

<span data-ttu-id="d85a3-123">下表概述 XML 結構中所定義之變數的特性。</span><span class="sxs-lookup"><span data-stu-id="d85a3-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="d85a3-124">屬性</span><span class="sxs-lookup"><span data-stu-id="d85a3-124">Property</span></span>                | <span data-ttu-id="d85a3-125">xsi:type</span><span class="sxs-lookup"><span data-stu-id="d85a3-125">xsi:type</span></span>           | <span data-ttu-id="d85a3-126">值</span><span class="sxs-lookup"><span data-stu-id="d85a3-126">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="d85a3-127">DataType</span><span class="sxs-lookup"><span data-stu-id="d85a3-127">DataType</span></span><br/>     | <span data-ttu-id="d85a3-128">String</span><span class="sxs-lookup"><span data-stu-id="d85a3-128">String</span></span><br/>  | <span data-ttu-id="d85a3-129">xs:integer</span><span class="sxs-lookup"><span data-stu-id="d85a3-129">xs:integer</span></span><br/>      |
| <span data-ttu-id="d85a3-130">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="d85a3-130">DefaultValue</span></span><br/> | <span data-ttu-id="d85a3-131">整數</span><span class="sxs-lookup"><span data-stu-id="d85a3-131">Integer</span></span><br/> | <span data-ttu-id="d85a3-132">未定義</span><span class="sxs-lookup"><span data-stu-id="d85a3-132">undefined</span></span><br/>       |
| <span data-ttu-id="d85a3-133">MaxValue</span><span class="sxs-lookup"><span data-stu-id="d85a3-133">MaxValue</span></span><br/>     | <span data-ttu-id="d85a3-134">整數</span><span class="sxs-lookup"><span data-stu-id="d85a3-134">Integer</span></span><br/> | <span data-ttu-id="d85a3-135">未定義</span><span class="sxs-lookup"><span data-stu-id="d85a3-135">undefined</span></span><br/>       |
| <span data-ttu-id="d85a3-136">MinValue</span><span class="sxs-lookup"><span data-stu-id="d85a3-136">MinValue</span></span><br/>     | <span data-ttu-id="d85a3-137">整數</span><span class="sxs-lookup"><span data-stu-id="d85a3-137">Integer</span></span><br/> | <span data-ttu-id="d85a3-138">1</span><span class="sxs-lookup"><span data-stu-id="d85a3-138">1</span></span><br/>               |
| <span data-ttu-id="d85a3-139">強制性</span><span class="sxs-lookup"><span data-stu-id="d85a3-139">Mandatory</span></span><br/>    | <span data-ttu-id="d85a3-140">String</span><span class="sxs-lookup"><span data-stu-id="d85a3-140">String</span></span><br/>  | <span data-ttu-id="d85a3-141">psk：條件式</span><span class="sxs-lookup"><span data-stu-id="d85a3-141">psk:Conditional</span></span><br/> |
| <span data-ttu-id="d85a3-142">多個</span><span class="sxs-lookup"><span data-stu-id="d85a3-142">Multiple</span></span><br/>     | <span data-ttu-id="d85a3-143">整數</span><span class="sxs-lookup"><span data-stu-id="d85a3-143">Integer</span></span><br/> | <span data-ttu-id="d85a3-144">1</span><span class="sxs-lookup"><span data-stu-id="d85a3-144">1</span></span><br/>               |
| <span data-ttu-id="d85a3-145">Unittype.pixel 表示</span><span class="sxs-lookup"><span data-stu-id="d85a3-145">UnitType</span></span><br/>     | <span data-ttu-id="d85a3-146">String</span><span class="sxs-lookup"><span data-stu-id="d85a3-146">String</span></span><br/>  | <span data-ttu-id="d85a3-147">微米</span><span class="sxs-lookup"><span data-stu-id="d85a3-147">microns</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="d85a3-148">相關主題</span><span class="sxs-lookup"><span data-stu-id="d85a3-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d85a3-149">列印架構規格</span><span class="sxs-lookup"><span data-stu-id="d85a3-149">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




