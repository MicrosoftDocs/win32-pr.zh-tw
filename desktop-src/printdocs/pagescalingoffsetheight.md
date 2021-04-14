---
description: 本主題並非最新的。 如需最新資訊，請參閱列印架構規格。
ms.assetid: f6fa0421-a125-4ead-a540-d2f7327a26b6
title: PageScalingOffsetHeight
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a475f7fa68cd961d9d7a7f42e40fc9ea80a72a4e
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/05/2021
ms.locfileid: "104386330"
---
# <a name="pagescalingoffsetheight"></a><span data-ttu-id="6d70b-104">PageScalingOffsetHeight</span><span class="sxs-lookup"><span data-stu-id="6d70b-104">PageScalingOffsetHeight</span></span>

<span data-ttu-id="6d70b-105">本主題並非最新的。</span><span class="sxs-lookup"><span data-stu-id="6d70b-105">This topic is not current.</span></span> <span data-ttu-id="6d70b-106">如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。</span><span class="sxs-lookup"><span data-stu-id="6d70b-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="6d70b-107">針對自訂縮放比例指定 ImageableSizeHeight 方向的縮放位移。</span><span class="sxs-lookup"><span data-stu-id="6d70b-107">Specifies the scaling offset in the ImageableSizeHeight direction for custom scaling.</span></span>

-   [<span data-ttu-id="6d70b-108">項目資訊</span><span class="sxs-lookup"><span data-stu-id="6d70b-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="6d70b-109">結構內容</span><span class="sxs-lookup"><span data-stu-id="6d70b-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="6d70b-110">項目資訊</span><span class="sxs-lookup"><span data-stu-id="6d70b-110">Element Information</span></span>



| <span data-ttu-id="6d70b-111">Name</span><span class="sxs-lookup"><span data-stu-id="6d70b-111">Name</span></span>                       |                                                         |
|----------------------------|---------------------------------------------------------|
| <span data-ttu-id="6d70b-112">項目類型</span><span class="sxs-lookup"><span data-stu-id="6d70b-112">Element Type</span></span> <br/>   | <span data-ttu-id="6d70b-113">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="6d70b-113">ParameterDef</span></span><br/>                                 |
| <span data-ttu-id="6d70b-114">範圍前置詞</span><span class="sxs-lookup"><span data-stu-id="6d70b-114">Scoping Prefix</span></span> <br/> | <span data-ttu-id="6d70b-115">頁面</span><span class="sxs-lookup"><span data-stu-id="6d70b-115">Page</span></span><br/>                                         |
| <span data-ttu-id="6d70b-116">備註</span><span class="sxs-lookup"><span data-stu-id="6d70b-116">Notes</span></span> <br/>          | <span data-ttu-id="6d70b-117">連結至 PageScaling 元素，自訂選項</span><span class="sxs-lookup"><span data-stu-id="6d70b-117">Linked to PageScaling element, Custom option</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="6d70b-118">結構內容</span><span class="sxs-lookup"><span data-stu-id="6d70b-118">Structure Content</span></span>

<span data-ttu-id="6d70b-119">此元素的 XML 結構為：</span><span class="sxs-lookup"><span data-stu-id="6d70b-119">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageScalingOffsetHeight">
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

## <a name="structure-properties"></a><span data-ttu-id="6d70b-120">結構屬性</span><span class="sxs-lookup"><span data-stu-id="6d70b-120">Structure Properties</span></span>

<span data-ttu-id="6d70b-121">下表概述 XML 結構中所定義之變數的特性。</span><span class="sxs-lookup"><span data-stu-id="6d70b-121">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="6d70b-122">屬性</span><span class="sxs-lookup"><span data-stu-id="6d70b-122">Property</span></span>                | <span data-ttu-id="6d70b-123">xsi:type</span><span class="sxs-lookup"><span data-stu-id="6d70b-123">xsi:type</span></span>           | <span data-ttu-id="6d70b-124">值</span><span class="sxs-lookup"><span data-stu-id="6d70b-124">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="6d70b-125">DataType</span><span class="sxs-lookup"><span data-stu-id="6d70b-125">DataType</span></span><br/>     | <span data-ttu-id="6d70b-126">字串</span><span class="sxs-lookup"><span data-stu-id="6d70b-126">string</span></span><br/>  | <span data-ttu-id="6d70b-127">xs:integer</span><span class="sxs-lookup"><span data-stu-id="6d70b-127">xs:integer</span></span><br/>      |
| <span data-ttu-id="6d70b-128">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="6d70b-128">DefaultValue</span></span><br/> | <span data-ttu-id="6d70b-129">整數</span><span class="sxs-lookup"><span data-stu-id="6d70b-129">integer</span></span><br/> | <span data-ttu-id="6d70b-130">未定義</span><span class="sxs-lookup"><span data-stu-id="6d70b-130">undefined</span></span><br/>       |
| <span data-ttu-id="6d70b-131">MaxValue</span><span class="sxs-lookup"><span data-stu-id="6d70b-131">MaxValue</span></span><br/>     | <span data-ttu-id="6d70b-132">整數</span><span class="sxs-lookup"><span data-stu-id="6d70b-132">integer</span></span><br/> | <span data-ttu-id="6d70b-133">未定義</span><span class="sxs-lookup"><span data-stu-id="6d70b-133">undefined</span></span><br/>       |
| <span data-ttu-id="6d70b-134">MinValue</span><span class="sxs-lookup"><span data-stu-id="6d70b-134">MinValue</span></span><br/>     | <span data-ttu-id="6d70b-135">整數</span><span class="sxs-lookup"><span data-stu-id="6d70b-135">integer</span></span><br/> | <span data-ttu-id="6d70b-136">未定義</span><span class="sxs-lookup"><span data-stu-id="6d70b-136">undefined</span></span><br/>       |
| <span data-ttu-id="6d70b-137">強制性</span><span class="sxs-lookup"><span data-stu-id="6d70b-137">Mandatory</span></span><br/>    | <span data-ttu-id="6d70b-138">字串</span><span class="sxs-lookup"><span data-stu-id="6d70b-138">string</span></span><br/>  | <span data-ttu-id="6d70b-139">psk：條件式</span><span class="sxs-lookup"><span data-stu-id="6d70b-139">psk:Conditional</span></span><br/> |
| <span data-ttu-id="6d70b-140">多個</span><span class="sxs-lookup"><span data-stu-id="6d70b-140">Multiple</span></span><br/>     | <span data-ttu-id="6d70b-141">整數</span><span class="sxs-lookup"><span data-stu-id="6d70b-141">integer</span></span><br/> | <span data-ttu-id="6d70b-142">1</span><span class="sxs-lookup"><span data-stu-id="6d70b-142">1</span></span><br/>               |
| <span data-ttu-id="6d70b-143">Unittype.pixel 表示</span><span class="sxs-lookup"><span data-stu-id="6d70b-143">UnitType</span></span><br/>     | <span data-ttu-id="6d70b-144">字串</span><span class="sxs-lookup"><span data-stu-id="6d70b-144">string</span></span><br/>  | <span data-ttu-id="6d70b-145">微米</span><span class="sxs-lookup"><span data-stu-id="6d70b-145">microns</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="6d70b-146">相關主題</span><span class="sxs-lookup"><span data-stu-id="6d70b-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6d70b-147">列印架構規格</span><span class="sxs-lookup"><span data-stu-id="6d70b-147">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




