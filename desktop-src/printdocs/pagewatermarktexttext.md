---
description: 本主題並非最新的。 如需最新資訊，請參閱列印架構規格。
ms.assetid: 3b01f05c-fe2e-4467-b2a7-5431a41200cd
title: PageWatermarkTextText
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb19f5965347e79732aa116e5be51f90e4ef6943
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/26/2021
ms.locfileid: "107996075"
---
# <a name="pagewatermarktexttext"></a><span data-ttu-id="be0e4-104">PageWatermarkTextText</span><span class="sxs-lookup"><span data-stu-id="be0e4-104">PageWatermarkTextText</span></span>

<span data-ttu-id="be0e4-105">本主題並非最新的。</span><span class="sxs-lookup"><span data-stu-id="be0e4-105">This topic is not current.</span></span> <span data-ttu-id="be0e4-106">如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。</span><span class="sxs-lookup"><span data-stu-id="be0e4-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="be0e4-107">指定浮水印的文字。</span><span class="sxs-lookup"><span data-stu-id="be0e4-107">Specifies the text of the watermark.</span></span>

-   [<span data-ttu-id="be0e4-108">項目資訊</span><span class="sxs-lookup"><span data-stu-id="be0e4-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="be0e4-109">結構內容</span><span class="sxs-lookup"><span data-stu-id="be0e4-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="be0e4-110">項目資訊</span><span class="sxs-lookup"><span data-stu-id="be0e4-110">Element Information</span></span>



| <span data-ttu-id="be0e4-111">Name</span><span class="sxs-lookup"><span data-stu-id="be0e4-111">Name</span></span> | <span data-ttu-id="be0e4-112">值</span><span class="sxs-lookup"><span data-stu-id="be0e4-112">Value</span></span> |
|----------------------------|--------------------------------------------|
| <span data-ttu-id="be0e4-113">項目類型</span><span class="sxs-lookup"><span data-stu-id="be0e4-113">Element Type</span></span> <br/>   | <span data-ttu-id="be0e4-114">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="be0e4-114">ParameterDef</span></span><br/>                    |
| <span data-ttu-id="be0e4-115">範圍前置詞</span><span class="sxs-lookup"><span data-stu-id="be0e4-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="be0e4-116">頁面</span><span class="sxs-lookup"><span data-stu-id="be0e4-116">Page</span></span><br/>                            |
| <span data-ttu-id="be0e4-117">備註</span><span class="sxs-lookup"><span data-stu-id="be0e4-117">Notes</span></span> <br/>          | <span data-ttu-id="be0e4-118">連結至 PageWatermark 元素</span><span class="sxs-lookup"><span data-stu-id="be0e4-118">Linked to PageWatermark element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="be0e4-119">結構內容</span><span class="sxs-lookup"><span data-stu-id="be0e4-119">Structure Content</span></span>

<span data-ttu-id="be0e4-120">此元素的 XML 結構如下所示：</span><span class="sxs-lookup"><span data-stu-id="be0e4-120">The XML structure of this element is as follows:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="be0e4-121">結構屬性</span><span class="sxs-lookup"><span data-stu-id="be0e4-121">Structure Properties</span></span>

<span data-ttu-id="be0e4-122">下表概述 XML 結構中所定義之變數的特性。</span><span class="sxs-lookup"><span data-stu-id="be0e4-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="be0e4-123">屬性</span><span class="sxs-lookup"><span data-stu-id="be0e4-123">Property</span></span>                | <span data-ttu-id="be0e4-124">xsi:type</span><span class="sxs-lookup"><span data-stu-id="be0e4-124">xsi:type</span></span>           | <span data-ttu-id="be0e4-125">值</span><span class="sxs-lookup"><span data-stu-id="be0e4-125">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="be0e4-126">DataType</span><span class="sxs-lookup"><span data-stu-id="be0e4-126">DataType</span></span><br/>     | <span data-ttu-id="be0e4-127">String</span><span class="sxs-lookup"><span data-stu-id="be0e4-127">String</span></span><br/>  | <span data-ttu-id="be0e4-128">xs:string</span><span class="sxs-lookup"><span data-stu-id="be0e4-128">xs:string</span></span><br/>       |
| <span data-ttu-id="be0e4-129">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="be0e4-129">DefaultValue</span></span><br/> | <span data-ttu-id="be0e4-130">整數</span><span class="sxs-lookup"><span data-stu-id="be0e4-130">Integer</span></span><br/> | <span data-ttu-id="be0e4-131">未定義</span><span class="sxs-lookup"><span data-stu-id="be0e4-131">undefined</span></span><br/>       |
| <span data-ttu-id="be0e4-132">MaxLength</span><span class="sxs-lookup"><span data-stu-id="be0e4-132">MaxLength</span></span><br/>    | <span data-ttu-id="be0e4-133">整數</span><span class="sxs-lookup"><span data-stu-id="be0e4-133">Integer</span></span><br/> | <span data-ttu-id="be0e4-134">未定義</span><span class="sxs-lookup"><span data-stu-id="be0e4-134">undefined</span></span><br/>       |
| <span data-ttu-id="be0e4-135">MinLength</span><span class="sxs-lookup"><span data-stu-id="be0e4-135">MinLength</span></span><br/>    | <span data-ttu-id="be0e4-136">整數</span><span class="sxs-lookup"><span data-stu-id="be0e4-136">Integer</span></span><br/> | <span data-ttu-id="be0e4-137">1</span><span class="sxs-lookup"><span data-stu-id="be0e4-137">1</span></span><br/>               |
| <span data-ttu-id="be0e4-138">強制性</span><span class="sxs-lookup"><span data-stu-id="be0e4-138">Mandatory</span></span><br/>    | <span data-ttu-id="be0e4-139">String</span><span class="sxs-lookup"><span data-stu-id="be0e4-139">String</span></span><br/>  | <span data-ttu-id="be0e4-140">psk：條件式</span><span class="sxs-lookup"><span data-stu-id="be0e4-140">psk:Conditional</span></span><br/> |
| <span data-ttu-id="be0e4-141">Unittype.pixel 表示</span><span class="sxs-lookup"><span data-stu-id="be0e4-141">UnitType</span></span><br/>     | <span data-ttu-id="be0e4-142">String</span><span class="sxs-lookup"><span data-stu-id="be0e4-142">String</span></span><br/>  | <span data-ttu-id="be0e4-143">字元</span><span class="sxs-lookup"><span data-stu-id="be0e4-143">characters</span></span><br/>      |



 

## <a name="related-topics"></a><span data-ttu-id="be0e4-144">相關主題</span><span class="sxs-lookup"><span data-stu-id="be0e4-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="be0e4-145">列印架構規格</span><span class="sxs-lookup"><span data-stu-id="be0e4-145">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




