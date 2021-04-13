---
description: 本主題並非最新的。 如需最新資訊，請參閱列印架構規格。
ms.assetid: 903ad358-a060-4c8f-b72e-5ec2eb898248
title: DocumentBindingGutter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4cf00f146373502564d559d00f66dedd24abf5b9
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/05/2021
ms.locfileid: "104195827"
---
# <a name="documentbindinggutter"></a><span data-ttu-id="a300c-104">DocumentBindingGutter</span><span class="sxs-lookup"><span data-stu-id="a300c-104">DocumentBindingGutter</span></span>

<span data-ttu-id="a300c-105">本主題並非最新的。</span><span class="sxs-lookup"><span data-stu-id="a300c-105">This topic is not current.</span></span> <span data-ttu-id="a300c-106">如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。</span><span class="sxs-lookup"><span data-stu-id="a300c-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="a300c-107">指定裝訂裝訂邊的寬度。</span><span class="sxs-lookup"><span data-stu-id="a300c-107">Specifies the width of the binding gutter.</span></span>

-   [<span data-ttu-id="a300c-108">項目資訊</span><span class="sxs-lookup"><span data-stu-id="a300c-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="a300c-109">結構內容</span><span class="sxs-lookup"><span data-stu-id="a300c-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="a300c-110">項目資訊</span><span class="sxs-lookup"><span data-stu-id="a300c-110">Element Information</span></span>



| <span data-ttu-id="a300c-111">Name</span><span class="sxs-lookup"><span data-stu-id="a300c-111">Name</span></span>                       |                                              |
|----------------------------|----------------------------------------------|
| <span data-ttu-id="a300c-112">項目類型</span><span class="sxs-lookup"><span data-stu-id="a300c-112">Element Type</span></span> <br/>   | <span data-ttu-id="a300c-113">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="a300c-113">ParameterDef</span></span><br/>                      |
| <span data-ttu-id="a300c-114">範圍前置詞</span><span class="sxs-lookup"><span data-stu-id="a300c-114">Scoping Prefix</span></span> <br/> | <span data-ttu-id="a300c-115">文件</span><span class="sxs-lookup"><span data-stu-id="a300c-115">Document</span></span><br/>                          |
| <span data-ttu-id="a300c-116">備註</span><span class="sxs-lookup"><span data-stu-id="a300c-116">Notes</span></span> <br/>          | <span data-ttu-id="a300c-117">連結至 DocumentBinding 元素</span><span class="sxs-lookup"><span data-stu-id="a300c-117">Linked to DocumentBinding element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="a300c-118">結構內容</span><span class="sxs-lookup"><span data-stu-id="a300c-118">Structure Content</span></span>

<span data-ttu-id="a300c-119">此元素的 XML 結構為：</span><span class="sxs-lookup"><span data-stu-id="a300c-119">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:DocumentBindingGutter">
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

## <a name="structure-properties"></a><span data-ttu-id="a300c-120">結構屬性</span><span class="sxs-lookup"><span data-stu-id="a300c-120">Structure Properties</span></span>

<span data-ttu-id="a300c-121">下表概述 XML 結構中所定義之變數的特性。</span><span class="sxs-lookup"><span data-stu-id="a300c-121">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="a300c-122">屬性</span><span class="sxs-lookup"><span data-stu-id="a300c-122">Property</span></span>                | <span data-ttu-id="a300c-123">xsi:type</span><span class="sxs-lookup"><span data-stu-id="a300c-123">xsi:type</span></span>           | <span data-ttu-id="a300c-124">值</span><span class="sxs-lookup"><span data-stu-id="a300c-124">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="a300c-125">DataType</span><span class="sxs-lookup"><span data-stu-id="a300c-125">DataType</span></span><br/>     | <span data-ttu-id="a300c-126">字串</span><span class="sxs-lookup"><span data-stu-id="a300c-126">string</span></span><br/>  | <span data-ttu-id="a300c-127">xs:integer</span><span class="sxs-lookup"><span data-stu-id="a300c-127">xs:integer</span></span><br/>      |
| <span data-ttu-id="a300c-128">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="a300c-128">DefaultValue</span></span><br/> | <span data-ttu-id="a300c-129">整數</span><span class="sxs-lookup"><span data-stu-id="a300c-129">integer</span></span><br/> | <span data-ttu-id="a300c-130">未定義</span><span class="sxs-lookup"><span data-stu-id="a300c-130">undefined</span></span><br/>       |
| <span data-ttu-id="a300c-131">MaxValue</span><span class="sxs-lookup"><span data-stu-id="a300c-131">MaxValue</span></span><br/>     | <span data-ttu-id="a300c-132">整數</span><span class="sxs-lookup"><span data-stu-id="a300c-132">integer</span></span><br/> | <span data-ttu-id="a300c-133">未定義</span><span class="sxs-lookup"><span data-stu-id="a300c-133">undefined</span></span><br/>       |
| <span data-ttu-id="a300c-134">MinValue</span><span class="sxs-lookup"><span data-stu-id="a300c-134">MinValue</span></span><br/>     | <span data-ttu-id="a300c-135">整數</span><span class="sxs-lookup"><span data-stu-id="a300c-135">integer</span></span><br/> | <span data-ttu-id="a300c-136">未定義</span><span class="sxs-lookup"><span data-stu-id="a300c-136">undefined</span></span><br/>       |
| <span data-ttu-id="a300c-137">強制性</span><span class="sxs-lookup"><span data-stu-id="a300c-137">Mandatory</span></span><br/>    | <span data-ttu-id="a300c-138">String</span><span class="sxs-lookup"><span data-stu-id="a300c-138">String</span></span><br/>  | <span data-ttu-id="a300c-139">psk：條件式</span><span class="sxs-lookup"><span data-stu-id="a300c-139">psk:Conditional</span></span><br/> |
| <span data-ttu-id="a300c-140">多個</span><span class="sxs-lookup"><span data-stu-id="a300c-140">Multiple</span></span><br/>     | <span data-ttu-id="a300c-141">整數</span><span class="sxs-lookup"><span data-stu-id="a300c-141">integer</span></span><br/> | <span data-ttu-id="a300c-142">1</span><span class="sxs-lookup"><span data-stu-id="a300c-142">1</span></span><br/>               |
| <span data-ttu-id="a300c-143">Unittype.pixel 表示</span><span class="sxs-lookup"><span data-stu-id="a300c-143">UnitType</span></span><br/>     | <span data-ttu-id="a300c-144">字串</span><span class="sxs-lookup"><span data-stu-id="a300c-144">string</span></span><br/>  | <span data-ttu-id="a300c-145">微米</span><span class="sxs-lookup"><span data-stu-id="a300c-145">microns</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="a300c-146">相關主題</span><span class="sxs-lookup"><span data-stu-id="a300c-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a300c-147">列印架構規格</span><span class="sxs-lookup"><span data-stu-id="a300c-147">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




