---
description: 取得 PageMediaSizeMediaSizeHeight 參數的相關資訊。 本主題並非最新的。 如需最新資訊，請參閱列印架構規格。
ms.assetid: 209b3024-60cf-47e0-8738-cd7795e38c2a
title: PageMediaSizeMediaSizeHeight
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 547077e7a63d91d6db43e8ebf6225a771bf237d8
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/19/2021
ms.locfileid: "112395793"
---
# <a name="pagemediasizemediasizeheight"></a><span data-ttu-id="33937-105">PageMediaSizeMediaSizeHeight</span><span class="sxs-lookup"><span data-stu-id="33937-105">PageMediaSizeMediaSizeHeight</span></span>

<span data-ttu-id="33937-106">本主題並非最新的。</span><span class="sxs-lookup"><span data-stu-id="33937-106">This topic is not current.</span></span> <span data-ttu-id="33937-107">如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。</span><span class="sxs-lookup"><span data-stu-id="33937-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="33937-108">指定自訂 MediaSize 選項的維度 MediaSizeHeight 方向。</span><span class="sxs-lookup"><span data-stu-id="33937-108">Specifies the dimension MediaSizeHeight direction for the Custom MediaSize option.</span></span>

-   [<span data-ttu-id="33937-109">項目資訊</span><span class="sxs-lookup"><span data-stu-id="33937-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="33937-110">結構內容</span><span class="sxs-lookup"><span data-stu-id="33937-110">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="33937-111">項目資訊</span><span class="sxs-lookup"><span data-stu-id="33937-111">Element Information</span></span>



| <span data-ttu-id="33937-112">Name</span><span class="sxs-lookup"><span data-stu-id="33937-112">Name</span></span> | <span data-ttu-id="33937-113">值</span><span class="sxs-lookup"><span data-stu-id="33937-113">Value</span></span> |
|----------------------------|-----------------------------------------------------------|
| <span data-ttu-id="33937-114">項目類型</span><span class="sxs-lookup"><span data-stu-id="33937-114">Element Type</span></span> <br/>   | <span data-ttu-id="33937-115">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="33937-115">ParameterDef</span></span><br/>                                   |
| <span data-ttu-id="33937-116">範圍前置詞</span><span class="sxs-lookup"><span data-stu-id="33937-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="33937-117">頁面</span><span class="sxs-lookup"><span data-stu-id="33937-117">Page</span></span><br/>                                           |
| <span data-ttu-id="33937-118">備註</span><span class="sxs-lookup"><span data-stu-id="33937-118">Notes</span></span> <br/>          | <span data-ttu-id="33937-119">連結至 PageMediaSize 元素，自訂選項</span><span class="sxs-lookup"><span data-stu-id="33937-119">Linked to PageMediaSize element, Custom option</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="33937-120">結構內容</span><span class="sxs-lookup"><span data-stu-id="33937-120">Structure Content</span></span>

<span data-ttu-id="33937-121">此元素的 XML 結構為：</span><span class="sxs-lookup"><span data-stu-id="33937-121">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="33937-122">結構屬性</span><span class="sxs-lookup"><span data-stu-id="33937-122">Structure Properties</span></span>

<span data-ttu-id="33937-123">下表概述 XML 結構中所定義之變數的特性。</span><span class="sxs-lookup"><span data-stu-id="33937-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="33937-124">屬性</span><span class="sxs-lookup"><span data-stu-id="33937-124">Property</span></span>                | <span data-ttu-id="33937-125">xsi:type</span><span class="sxs-lookup"><span data-stu-id="33937-125">xsi:type</span></span>           | <span data-ttu-id="33937-126">值</span><span class="sxs-lookup"><span data-stu-id="33937-126">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="33937-127">DataType</span><span class="sxs-lookup"><span data-stu-id="33937-127">DataType</span></span><br/>     | <span data-ttu-id="33937-128">字串</span><span class="sxs-lookup"><span data-stu-id="33937-128">string</span></span><br/>  | <span data-ttu-id="33937-129">xs:integer</span><span class="sxs-lookup"><span data-stu-id="33937-129">xs:integer</span></span><br/>      |
| <span data-ttu-id="33937-130">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="33937-130">DefaultValue</span></span><br/> | <span data-ttu-id="33937-131">整數</span><span class="sxs-lookup"><span data-stu-id="33937-131">integer</span></span><br/> | <span data-ttu-id="33937-132">未定義</span><span class="sxs-lookup"><span data-stu-id="33937-132">undefined</span></span><br/>       |
| <span data-ttu-id="33937-133">MaxValue</span><span class="sxs-lookup"><span data-stu-id="33937-133">MaxValue</span></span><br/>     | <span data-ttu-id="33937-134">整數</span><span class="sxs-lookup"><span data-stu-id="33937-134">integer</span></span><br/> | <span data-ttu-id="33937-135">未定義</span><span class="sxs-lookup"><span data-stu-id="33937-135">undefined</span></span><br/>       |
| <span data-ttu-id="33937-136">MinValue</span><span class="sxs-lookup"><span data-stu-id="33937-136">MinValue</span></span><br/>     | <span data-ttu-id="33937-137">整數</span><span class="sxs-lookup"><span data-stu-id="33937-137">integer</span></span><br/> | <span data-ttu-id="33937-138">未定義</span><span class="sxs-lookup"><span data-stu-id="33937-138">undefined</span></span><br/>       |
| <span data-ttu-id="33937-139">強制性</span><span class="sxs-lookup"><span data-stu-id="33937-139">Mandatory</span></span><br/>    | <span data-ttu-id="33937-140">string</span><span class="sxs-lookup"><span data-stu-id="33937-140">string</span></span><br/>  | <span data-ttu-id="33937-141">psk：條件式</span><span class="sxs-lookup"><span data-stu-id="33937-141">psk:Conditional</span></span><br/> |
| <span data-ttu-id="33937-142">多個</span><span class="sxs-lookup"><span data-stu-id="33937-142">Multiple</span></span><br/>     | <span data-ttu-id="33937-143">整數</span><span class="sxs-lookup"><span data-stu-id="33937-143">integer</span></span><br/> | <span data-ttu-id="33937-144">1</span><span class="sxs-lookup"><span data-stu-id="33937-144">1</span></span><br/>               |
| <span data-ttu-id="33937-145">Unittype.pixel 表示</span><span class="sxs-lookup"><span data-stu-id="33937-145">UnitType</span></span><br/>     | <span data-ttu-id="33937-146">string</span><span class="sxs-lookup"><span data-stu-id="33937-146">string</span></span><br/>  | <span data-ttu-id="33937-147">微米</span><span class="sxs-lookup"><span data-stu-id="33937-147">microns</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="33937-148">相關主題</span><span class="sxs-lookup"><span data-stu-id="33937-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="33937-149">列印架構規格</span><span class="sxs-lookup"><span data-stu-id="33937-149">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




