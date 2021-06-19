---
description: 取得 PageWatermarkTextColor 參數的相關資訊。 本主題並非最新的。 如需最新資訊，請參閱列印架構規格。
ms.assetid: edbdd2c7-da04-49fb-a0f8-31a7df88f8ef
title: PageWatermarkTextColor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db7cb7b893ec9a2ecf774173cf2a9f2410549087
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/19/2021
ms.locfileid: "112396013"
---
# <a name="pagewatermarktextcolor"></a><span data-ttu-id="ccf82-105">PageWatermarkTextColor</span><span class="sxs-lookup"><span data-stu-id="ccf82-105">PageWatermarkTextColor</span></span>

<span data-ttu-id="ccf82-106">本主題並非最新的。</span><span class="sxs-lookup"><span data-stu-id="ccf82-106">This topic is not current.</span></span> <span data-ttu-id="ccf82-107">如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。</span><span class="sxs-lookup"><span data-stu-id="ccf82-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="ccf82-108">定義浮水印文字的 sRGB 色彩。</span><span class="sxs-lookup"><span data-stu-id="ccf82-108">Defines the sRGB color for the watermark text.</span></span> <span data-ttu-id="ccf82-109">格式為 ARGB： \# AARRGGBB。</span><span class="sxs-lookup"><span data-stu-id="ccf82-109">Format is ARGB: \#AARRGGBB.</span></span>

-   [<span data-ttu-id="ccf82-110">項目資訊</span><span class="sxs-lookup"><span data-stu-id="ccf82-110">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="ccf82-111">結構內容</span><span class="sxs-lookup"><span data-stu-id="ccf82-111">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="ccf82-112">項目資訊</span><span class="sxs-lookup"><span data-stu-id="ccf82-112">Element Information</span></span>



| <span data-ttu-id="ccf82-113">Name</span><span class="sxs-lookup"><span data-stu-id="ccf82-113">Name</span></span> | <span data-ttu-id="ccf82-114">值</span><span class="sxs-lookup"><span data-stu-id="ccf82-114">Value</span></span> |
|----------------------------|--------------------------------------------|
| <span data-ttu-id="ccf82-115">項目類型</span><span class="sxs-lookup"><span data-stu-id="ccf82-115">Element Type</span></span> <br/>   | <span data-ttu-id="ccf82-116">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="ccf82-116">ParameterDef</span></span><br/>                    |
| <span data-ttu-id="ccf82-117">範圍前置詞</span><span class="sxs-lookup"><span data-stu-id="ccf82-117">Scoping Prefix</span></span> <br/> | <span data-ttu-id="ccf82-118">頁面</span><span class="sxs-lookup"><span data-stu-id="ccf82-118">Page</span></span><br/>                            |
| <span data-ttu-id="ccf82-119">備註</span><span class="sxs-lookup"><span data-stu-id="ccf82-119">Notes</span></span> <br/>          | <span data-ttu-id="ccf82-120">連結至 PageWatermark 元素</span><span class="sxs-lookup"><span data-stu-id="ccf82-120">Linked to PageWatermark element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="ccf82-121">結構內容</span><span class="sxs-lookup"><span data-stu-id="ccf82-121">Structure Content</span></span>

<span data-ttu-id="ccf82-122">此元素的 XML 結構如下所示：</span><span class="sxs-lookup"><span data-stu-id="ccf82-122">The XML structure of this element is as follows:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageWatermarkTextColor">
  <psf:Property name="psf:DataType">
    <psf:Value xsi:type="xs:string">xs:string</psf:Value>
  </psf:Property>
  <psf:Property name="psf:DefaultValue">
    <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MaxLength">
    <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MinLength">
    <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:Mandatory">
    <psf:Value xsi:type="xs:string">psk:Conditional</psf:Value>
  </psf:Property>
  <psf:Property name="psf:UnitType">
    <psf:Value xsi:type="xs:string">sRGB</psf:Value>
  </psf:Property>
</psf:ParameterDef>
      
```

## <a name="structure-properties"></a><span data-ttu-id="ccf82-123">結構屬性</span><span class="sxs-lookup"><span data-stu-id="ccf82-123">Structure Properties</span></span>

<span data-ttu-id="ccf82-124">下表概述 XML 結構中所定義之變數的特性。</span><span class="sxs-lookup"><span data-stu-id="ccf82-124">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="ccf82-125">屬性</span><span class="sxs-lookup"><span data-stu-id="ccf82-125">Property</span></span>                | <span data-ttu-id="ccf82-126">xsi:type</span><span class="sxs-lookup"><span data-stu-id="ccf82-126">xsi:type</span></span>           | <span data-ttu-id="ccf82-127">值</span><span class="sxs-lookup"><span data-stu-id="ccf82-127">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="ccf82-128">DataType</span><span class="sxs-lookup"><span data-stu-id="ccf82-128">DataType</span></span><br/>     | <span data-ttu-id="ccf82-129">字串</span><span class="sxs-lookup"><span data-stu-id="ccf82-129">string</span></span><br/>  | <span data-ttu-id="ccf82-130">xs:string</span><span class="sxs-lookup"><span data-stu-id="ccf82-130">xs:string</span></span><br/>       |
| <span data-ttu-id="ccf82-131">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="ccf82-131">DefaultValue</span></span><br/> | <span data-ttu-id="ccf82-132">整數</span><span class="sxs-lookup"><span data-stu-id="ccf82-132">integer</span></span><br/> | <span data-ttu-id="ccf82-133">未定義</span><span class="sxs-lookup"><span data-stu-id="ccf82-133">undefined</span></span><br/>       |
| <span data-ttu-id="ccf82-134">MaxValue</span><span class="sxs-lookup"><span data-stu-id="ccf82-134">MaxValue</span></span><br/>     | <span data-ttu-id="ccf82-135">整數</span><span class="sxs-lookup"><span data-stu-id="ccf82-135">integer</span></span><br/> | <span data-ttu-id="ccf82-136">未定義</span><span class="sxs-lookup"><span data-stu-id="ccf82-136">undefined</span></span><br/>       |
| <span data-ttu-id="ccf82-137">MinValue</span><span class="sxs-lookup"><span data-stu-id="ccf82-137">MinValue</span></span><br/>     | <span data-ttu-id="ccf82-138">整數</span><span class="sxs-lookup"><span data-stu-id="ccf82-138">integer</span></span><br/> | <span data-ttu-id="ccf82-139">未定義</span><span class="sxs-lookup"><span data-stu-id="ccf82-139">undefined</span></span><br/>       |
| <span data-ttu-id="ccf82-140">強制性</span><span class="sxs-lookup"><span data-stu-id="ccf82-140">Mandatory</span></span><br/>    | <span data-ttu-id="ccf82-141">string</span><span class="sxs-lookup"><span data-stu-id="ccf82-141">string</span></span><br/>  | <span data-ttu-id="ccf82-142">psk：條件式</span><span class="sxs-lookup"><span data-stu-id="ccf82-142">psk:Conditional</span></span><br/> |
| <span data-ttu-id="ccf82-143">Unittype.pixel 表示</span><span class="sxs-lookup"><span data-stu-id="ccf82-143">UnitType</span></span><br/>     | <span data-ttu-id="ccf82-144">string</span><span class="sxs-lookup"><span data-stu-id="ccf82-144">string</span></span><br/>  | <span data-ttu-id="ccf82-145">sRGB</span><span class="sxs-lookup"><span data-stu-id="ccf82-145">sRGB</span></span><br/>            |



 

## <a name="related-topics"></a><span data-ttu-id="ccf82-146">相關主題</span><span class="sxs-lookup"><span data-stu-id="ccf82-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ccf82-147">列印架構規格</span><span class="sxs-lookup"><span data-stu-id="ccf82-147">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




