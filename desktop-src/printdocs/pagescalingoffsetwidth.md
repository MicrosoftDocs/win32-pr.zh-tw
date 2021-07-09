---
description: 取得 PageScalingOffsetWidth 參數的相關資訊。 本主題並非最新的。 如需最新資訊，請參閱列印架構規格。
ms.assetid: e82394d1-f765-4679-b1de-ea17825d6478
title: PageScalingOffsetWidth
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63152e6a3d9f8ea47bac3b5a0efe559e71e0cb35
ms.sourcegitcommit: 998d50f6def8a25850fc113fc8a2df903c829c5e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/09/2021
ms.locfileid: "113548846"
---
# <a name="pagescalingoffsetwidth"></a><span data-ttu-id="ad8ea-105">PageScalingOffsetWidth</span><span class="sxs-lookup"><span data-stu-id="ad8ea-105">PageScalingOffsetWidth</span></span>

<span data-ttu-id="ad8ea-106">本主題並非最新的。</span><span class="sxs-lookup"><span data-stu-id="ad8ea-106">This topic is not current.</span></span> <span data-ttu-id="ad8ea-107">如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。</span><span class="sxs-lookup"><span data-stu-id="ad8ea-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="ad8ea-108">針對自訂縮放比例指定 ImageableSizeWidth 方向的縮放位移。</span><span class="sxs-lookup"><span data-stu-id="ad8ea-108">Specifies the scaling offset in the ImageableSizeWidth direction for custom scaling.</span></span>

-   [<span data-ttu-id="ad8ea-109">項目資訊</span><span class="sxs-lookup"><span data-stu-id="ad8ea-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="ad8ea-110">結構內容</span><span class="sxs-lookup"><span data-stu-id="ad8ea-110">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="ad8ea-111">項目資訊</span><span class="sxs-lookup"><span data-stu-id="ad8ea-111">Element Information</span></span>



| <span data-ttu-id="ad8ea-112">Name</span><span class="sxs-lookup"><span data-stu-id="ad8ea-112">Name</span></span> | <span data-ttu-id="ad8ea-113">值</span><span class="sxs-lookup"><span data-stu-id="ad8ea-113">Value</span></span> |
|----------------------------|---------------------------------------------------------|
| <span data-ttu-id="ad8ea-114">項目類型</span><span class="sxs-lookup"><span data-stu-id="ad8ea-114">Element Type</span></span> <br/>   | <span data-ttu-id="ad8ea-115">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="ad8ea-115">ParameterDef</span></span><br/>                                 |
| <span data-ttu-id="ad8ea-116">範圍前置詞</span><span class="sxs-lookup"><span data-stu-id="ad8ea-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="ad8ea-117">頁面</span><span class="sxs-lookup"><span data-stu-id="ad8ea-117">Page</span></span><br/>                                         |
| <span data-ttu-id="ad8ea-118">備註</span><span class="sxs-lookup"><span data-stu-id="ad8ea-118">Notes</span></span> <br/>          | <span data-ttu-id="ad8ea-119">連結至 PageScaling 元素，自訂選項</span><span class="sxs-lookup"><span data-stu-id="ad8ea-119">Linked to PageScaling element, Custom option</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="ad8ea-120">結構內容</span><span class="sxs-lookup"><span data-stu-id="ad8ea-120">Structure Content</span></span>

<span data-ttu-id="ad8ea-121">此元素的 XML 結構為：</span><span class="sxs-lookup"><span data-stu-id="ad8ea-121">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageScalingOffsetWidth">
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
    <psf:Value xsi:type="xs:decimal">_Undefined_</psf:Value>
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

## <a name="structure-properties"></a><span data-ttu-id="ad8ea-122">結構屬性</span><span class="sxs-lookup"><span data-stu-id="ad8ea-122">Structure Properties</span></span>

<span data-ttu-id="ad8ea-123">下表概述 XML 結構中所定義之變數的特性。</span><span class="sxs-lookup"><span data-stu-id="ad8ea-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="ad8ea-124">屬性</span><span class="sxs-lookup"><span data-stu-id="ad8ea-124">Property</span></span>                | <span data-ttu-id="ad8ea-125">xsi:type</span><span class="sxs-lookup"><span data-stu-id="ad8ea-125">xsi:type</span></span>           | <span data-ttu-id="ad8ea-126">值</span><span class="sxs-lookup"><span data-stu-id="ad8ea-126">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="ad8ea-127">DataType</span><span class="sxs-lookup"><span data-stu-id="ad8ea-127">DataType</span></span><br/>     | <span data-ttu-id="ad8ea-128">字串</span><span class="sxs-lookup"><span data-stu-id="ad8ea-128">string</span></span><br/>  | <span data-ttu-id="ad8ea-129">xs:integer</span><span class="sxs-lookup"><span data-stu-id="ad8ea-129">xs:integer</span></span><br/>      |
| <span data-ttu-id="ad8ea-130">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="ad8ea-130">DefaultValue</span></span><br/> | <span data-ttu-id="ad8ea-131">整數</span><span class="sxs-lookup"><span data-stu-id="ad8ea-131">integer</span></span><br/> | <span data-ttu-id="ad8ea-132">未定義</span><span class="sxs-lookup"><span data-stu-id="ad8ea-132">undefined</span></span><br/>       |
| <span data-ttu-id="ad8ea-133">MaxValue</span><span class="sxs-lookup"><span data-stu-id="ad8ea-133">MaxValue</span></span><br/>     | <span data-ttu-id="ad8ea-134">整數</span><span class="sxs-lookup"><span data-stu-id="ad8ea-134">integer</span></span><br/> | <span data-ttu-id="ad8ea-135">未定義</span><span class="sxs-lookup"><span data-stu-id="ad8ea-135">undefined</span></span><br/>       |
| <span data-ttu-id="ad8ea-136">MinValue</span><span class="sxs-lookup"><span data-stu-id="ad8ea-136">MinValue</span></span><br/>     | <span data-ttu-id="ad8ea-137">整數</span><span class="sxs-lookup"><span data-stu-id="ad8ea-137">integer</span></span><br/> | <span data-ttu-id="ad8ea-138">未定義</span><span class="sxs-lookup"><span data-stu-id="ad8ea-138">undefined</span></span><br/>       |
| <span data-ttu-id="ad8ea-139">強制性</span><span class="sxs-lookup"><span data-stu-id="ad8ea-139">Mandatory</span></span><br/>    | <span data-ttu-id="ad8ea-140">string</span><span class="sxs-lookup"><span data-stu-id="ad8ea-140">string</span></span><br/>  | <span data-ttu-id="ad8ea-141">psk：條件式</span><span class="sxs-lookup"><span data-stu-id="ad8ea-141">psk:Conditional</span></span><br/> |
| <span data-ttu-id="ad8ea-142">多個</span><span class="sxs-lookup"><span data-stu-id="ad8ea-142">Multiple</span></span><br/>     | <span data-ttu-id="ad8ea-143">整數</span><span class="sxs-lookup"><span data-stu-id="ad8ea-143">integer</span></span><br/> | <span data-ttu-id="ad8ea-144">1</span><span class="sxs-lookup"><span data-stu-id="ad8ea-144">1</span></span><br/>               |
| <span data-ttu-id="ad8ea-145">Unittype.pixel 表示</span><span class="sxs-lookup"><span data-stu-id="ad8ea-145">UnitType</span></span><br/>     | <span data-ttu-id="ad8ea-146">string</span><span class="sxs-lookup"><span data-stu-id="ad8ea-146">string</span></span><br/>  | <span data-ttu-id="ad8ea-147">微米</span><span class="sxs-lookup"><span data-stu-id="ad8ea-147">microns</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="ad8ea-148">相關主題</span><span class="sxs-lookup"><span data-stu-id="ad8ea-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ad8ea-149">列印架構規格</span><span class="sxs-lookup"><span data-stu-id="ad8ea-149">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




