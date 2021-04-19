---
description: 本主題並非最新的。 如需最新資訊，請參閱列印架構規格。
ms.assetid: 3b01f05c-fe2e-4467-b2a7-5431a41200cd
title: PageWatermarkTextText
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aef2310efaa91532493f7add14de8c2510e24e9b
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/05/2021
ms.locfileid: "106998952"
---
# <a name="pagewatermarktexttext"></a><span data-ttu-id="a4016-104">PageWatermarkTextText</span><span class="sxs-lookup"><span data-stu-id="a4016-104">PageWatermarkTextText</span></span>

<span data-ttu-id="a4016-105">本主題並非最新的。</span><span class="sxs-lookup"><span data-stu-id="a4016-105">This topic is not current.</span></span> <span data-ttu-id="a4016-106">如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。</span><span class="sxs-lookup"><span data-stu-id="a4016-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="a4016-107">指定浮水印的文字。</span><span class="sxs-lookup"><span data-stu-id="a4016-107">Specifies the text of the watermark.</span></span>

-   [<span data-ttu-id="a4016-108">項目資訊</span><span class="sxs-lookup"><span data-stu-id="a4016-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="a4016-109">結構內容</span><span class="sxs-lookup"><span data-stu-id="a4016-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="a4016-110">項目資訊</span><span class="sxs-lookup"><span data-stu-id="a4016-110">Element Information</span></span>



| <span data-ttu-id="a4016-111">Name</span><span class="sxs-lookup"><span data-stu-id="a4016-111">Name</span></span>                       |                                            |
|----------------------------|--------------------------------------------|
| <span data-ttu-id="a4016-112">項目類型</span><span class="sxs-lookup"><span data-stu-id="a4016-112">Element Type</span></span> <br/>   | <span data-ttu-id="a4016-113">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="a4016-113">ParameterDef</span></span><br/>                    |
| <span data-ttu-id="a4016-114">範圍前置詞</span><span class="sxs-lookup"><span data-stu-id="a4016-114">Scoping Prefix</span></span> <br/> | <span data-ttu-id="a4016-115">頁面</span><span class="sxs-lookup"><span data-stu-id="a4016-115">Page</span></span><br/>                            |
| <span data-ttu-id="a4016-116">備註</span><span class="sxs-lookup"><span data-stu-id="a4016-116">Notes</span></span> <br/>          | <span data-ttu-id="a4016-117">連結至 PageWatermark 元素</span><span class="sxs-lookup"><span data-stu-id="a4016-117">Linked to PageWatermark element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="a4016-118">結構內容</span><span class="sxs-lookup"><span data-stu-id="a4016-118">Structure Content</span></span>

<span data-ttu-id="a4016-119">此元素的 XML 結構如下所示：</span><span class="sxs-lookup"><span data-stu-id="a4016-119">The XML structure of this element is as follows:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageWatermarkTextText">
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
    <psf:Value xsi:type="xs:integer">1</psf:Value>
  </psf:Property>
  <psf:Property name="psf:Mandatory">
    <psf:Value xsi:type="xs:string">psk:Conditional</psf:Value>
  </psf:Property>
  <psf:Property name="psf:UnitType">
    <psf:Value xsi:type="xs:string">characters</psf:Value>
  </psf:Property>
</psf:ParameterDef>
```

## <a name="structure-properties"></a><span data-ttu-id="a4016-120">結構屬性</span><span class="sxs-lookup"><span data-stu-id="a4016-120">Structure Properties</span></span>

<span data-ttu-id="a4016-121">下表概述 XML 結構中所定義之變數的特性。</span><span class="sxs-lookup"><span data-stu-id="a4016-121">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="a4016-122">屬性</span><span class="sxs-lookup"><span data-stu-id="a4016-122">Property</span></span>                | <span data-ttu-id="a4016-123">xsi:type</span><span class="sxs-lookup"><span data-stu-id="a4016-123">xsi:type</span></span>           | <span data-ttu-id="a4016-124">值</span><span class="sxs-lookup"><span data-stu-id="a4016-124">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="a4016-125">DataType</span><span class="sxs-lookup"><span data-stu-id="a4016-125">DataType</span></span><br/>     | <span data-ttu-id="a4016-126">String</span><span class="sxs-lookup"><span data-stu-id="a4016-126">String</span></span><br/>  | <span data-ttu-id="a4016-127">xs:string</span><span class="sxs-lookup"><span data-stu-id="a4016-127">xs:string</span></span><br/>       |
| <span data-ttu-id="a4016-128">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="a4016-128">DefaultValue</span></span><br/> | <span data-ttu-id="a4016-129">整數</span><span class="sxs-lookup"><span data-stu-id="a4016-129">Integer</span></span><br/> | <span data-ttu-id="a4016-130">未定義</span><span class="sxs-lookup"><span data-stu-id="a4016-130">undefined</span></span><br/>       |
| <span data-ttu-id="a4016-131">MaxLength</span><span class="sxs-lookup"><span data-stu-id="a4016-131">MaxLength</span></span><br/>    | <span data-ttu-id="a4016-132">整數</span><span class="sxs-lookup"><span data-stu-id="a4016-132">Integer</span></span><br/> | <span data-ttu-id="a4016-133">未定義</span><span class="sxs-lookup"><span data-stu-id="a4016-133">undefined</span></span><br/>       |
| <span data-ttu-id="a4016-134">MinLength</span><span class="sxs-lookup"><span data-stu-id="a4016-134">MinLength</span></span><br/>    | <span data-ttu-id="a4016-135">整數</span><span class="sxs-lookup"><span data-stu-id="a4016-135">Integer</span></span><br/> | <span data-ttu-id="a4016-136">1</span><span class="sxs-lookup"><span data-stu-id="a4016-136">1</span></span><br/>               |
| <span data-ttu-id="a4016-137">強制性</span><span class="sxs-lookup"><span data-stu-id="a4016-137">Mandatory</span></span><br/>    | <span data-ttu-id="a4016-138">String</span><span class="sxs-lookup"><span data-stu-id="a4016-138">String</span></span><br/>  | <span data-ttu-id="a4016-139">psk：條件式</span><span class="sxs-lookup"><span data-stu-id="a4016-139">psk:Conditional</span></span><br/> |
| <span data-ttu-id="a4016-140">Unittype.pixel 表示</span><span class="sxs-lookup"><span data-stu-id="a4016-140">UnitType</span></span><br/>     | <span data-ttu-id="a4016-141">String</span><span class="sxs-lookup"><span data-stu-id="a4016-141">String</span></span><br/>  | <span data-ttu-id="a4016-142">字元</span><span class="sxs-lookup"><span data-stu-id="a4016-142">characters</span></span><br/>      |



 

## <a name="related-topics"></a><span data-ttu-id="a4016-143">相關主題</span><span class="sxs-lookup"><span data-stu-id="a4016-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a4016-144">列印架構規格</span><span class="sxs-lookup"><span data-stu-id="a4016-144">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




