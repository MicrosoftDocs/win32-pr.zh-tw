---
description: 本主題並非最新的。 如需最新資訊，請參閱列印架構規格。
ms.assetid: 209b3024-60cf-47e0-8738-cd7795e38c2a
title: PageMediaSizeMediaSizeHeight
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db500f5a64254a0e0d152cb019d7f11f25471ce3
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/05/2021
ms.locfileid: "106986028"
---
# <a name="pagemediasizemediasizeheight"></a><span data-ttu-id="f047d-104">PageMediaSizeMediaSizeHeight</span><span class="sxs-lookup"><span data-stu-id="f047d-104">PageMediaSizeMediaSizeHeight</span></span>

<span data-ttu-id="f047d-105">本主題並非最新的。</span><span class="sxs-lookup"><span data-stu-id="f047d-105">This topic is not current.</span></span> <span data-ttu-id="f047d-106">如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。</span><span class="sxs-lookup"><span data-stu-id="f047d-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="f047d-107">指定自訂 MediaSize 選項的維度 MediaSizeHeight 方向。</span><span class="sxs-lookup"><span data-stu-id="f047d-107">Specifies the dimension MediaSizeHeight direction for the Custom MediaSize option.</span></span>

-   [<span data-ttu-id="f047d-108">項目資訊</span><span class="sxs-lookup"><span data-stu-id="f047d-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="f047d-109">結構內容</span><span class="sxs-lookup"><span data-stu-id="f047d-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="f047d-110">項目資訊</span><span class="sxs-lookup"><span data-stu-id="f047d-110">Element Information</span></span>



| <span data-ttu-id="f047d-111">Name</span><span class="sxs-lookup"><span data-stu-id="f047d-111">Name</span></span>                       |                                                           |
|----------------------------|-----------------------------------------------------------|
| <span data-ttu-id="f047d-112">項目類型</span><span class="sxs-lookup"><span data-stu-id="f047d-112">Element Type</span></span> <br/>   | <span data-ttu-id="f047d-113">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="f047d-113">ParameterDef</span></span><br/>                                   |
| <span data-ttu-id="f047d-114">範圍前置詞</span><span class="sxs-lookup"><span data-stu-id="f047d-114">Scoping Prefix</span></span> <br/> | <span data-ttu-id="f047d-115">頁面</span><span class="sxs-lookup"><span data-stu-id="f047d-115">Page</span></span><br/>                                           |
| <span data-ttu-id="f047d-116">備註</span><span class="sxs-lookup"><span data-stu-id="f047d-116">Notes</span></span> <br/>          | <span data-ttu-id="f047d-117">連結至 PageMediaSize 元素，自訂選項</span><span class="sxs-lookup"><span data-stu-id="f047d-117">Linked to PageMediaSize element, Custom option</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="f047d-118">結構內容</span><span class="sxs-lookup"><span data-stu-id="f047d-118">Structure Content</span></span>

<span data-ttu-id="f047d-119">此元素的 XML 結構為：</span><span class="sxs-lookup"><span data-stu-id="f047d-119">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageMediaSizeMediaSizeHeight">
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

## <a name="structure-properties"></a><span data-ttu-id="f047d-120">結構屬性</span><span class="sxs-lookup"><span data-stu-id="f047d-120">Structure Properties</span></span>

<span data-ttu-id="f047d-121">下表概述 XML 結構中所定義之變數的特性。</span><span class="sxs-lookup"><span data-stu-id="f047d-121">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="f047d-122">屬性</span><span class="sxs-lookup"><span data-stu-id="f047d-122">Property</span></span>                | <span data-ttu-id="f047d-123">xsi:type</span><span class="sxs-lookup"><span data-stu-id="f047d-123">xsi:type</span></span>           | <span data-ttu-id="f047d-124">值</span><span class="sxs-lookup"><span data-stu-id="f047d-124">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="f047d-125">DataType</span><span class="sxs-lookup"><span data-stu-id="f047d-125">DataType</span></span><br/>     | <span data-ttu-id="f047d-126">字串</span><span class="sxs-lookup"><span data-stu-id="f047d-126">string</span></span><br/>  | <span data-ttu-id="f047d-127">xs:integer</span><span class="sxs-lookup"><span data-stu-id="f047d-127">xs:integer</span></span><br/>      |
| <span data-ttu-id="f047d-128">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="f047d-128">DefaultValue</span></span><br/> | <span data-ttu-id="f047d-129">整數</span><span class="sxs-lookup"><span data-stu-id="f047d-129">integer</span></span><br/> | <span data-ttu-id="f047d-130">未定義</span><span class="sxs-lookup"><span data-stu-id="f047d-130">undefined</span></span><br/>       |
| <span data-ttu-id="f047d-131">MaxValue</span><span class="sxs-lookup"><span data-stu-id="f047d-131">MaxValue</span></span><br/>     | <span data-ttu-id="f047d-132">整數</span><span class="sxs-lookup"><span data-stu-id="f047d-132">integer</span></span><br/> | <span data-ttu-id="f047d-133">未定義</span><span class="sxs-lookup"><span data-stu-id="f047d-133">undefined</span></span><br/>       |
| <span data-ttu-id="f047d-134">MinValue</span><span class="sxs-lookup"><span data-stu-id="f047d-134">MinValue</span></span><br/>     | <span data-ttu-id="f047d-135">整數</span><span class="sxs-lookup"><span data-stu-id="f047d-135">integer</span></span><br/> | <span data-ttu-id="f047d-136">未定義</span><span class="sxs-lookup"><span data-stu-id="f047d-136">undefined</span></span><br/>       |
| <span data-ttu-id="f047d-137">強制性</span><span class="sxs-lookup"><span data-stu-id="f047d-137">Mandatory</span></span><br/>    | <span data-ttu-id="f047d-138">字串</span><span class="sxs-lookup"><span data-stu-id="f047d-138">string</span></span><br/>  | <span data-ttu-id="f047d-139">psk：條件式</span><span class="sxs-lookup"><span data-stu-id="f047d-139">psk:Conditional</span></span><br/> |
| <span data-ttu-id="f047d-140">多個</span><span class="sxs-lookup"><span data-stu-id="f047d-140">Multiple</span></span><br/>     | <span data-ttu-id="f047d-141">整數</span><span class="sxs-lookup"><span data-stu-id="f047d-141">integer</span></span><br/> | <span data-ttu-id="f047d-142">1</span><span class="sxs-lookup"><span data-stu-id="f047d-142">1</span></span><br/>               |
| <span data-ttu-id="f047d-143">Unittype.pixel 表示</span><span class="sxs-lookup"><span data-stu-id="f047d-143">UnitType</span></span><br/>     | <span data-ttu-id="f047d-144">字串</span><span class="sxs-lookup"><span data-stu-id="f047d-144">string</span></span><br/>  | <span data-ttu-id="f047d-145">微米</span><span class="sxs-lookup"><span data-stu-id="f047d-145">microns</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="f047d-146">相關主題</span><span class="sxs-lookup"><span data-stu-id="f047d-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f047d-147">列印架構規格</span><span class="sxs-lookup"><span data-stu-id="f047d-147">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




