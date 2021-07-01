---
description: 尋找 DocumentBindingGutter 參數的相關資訊。 本主題並非最新的。 如需最新資訊，請參閱列印架構規格。
ms.assetid: 903ad358-a060-4c8f-b72e-5ec2eb898248
title: DocumentBindingGutter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45839aa07d740d8498e477809b45aa823460b23f
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/30/2021
ms.locfileid: "113118463"
---
# <a name="documentbindinggutter"></a><span data-ttu-id="1af78-105">DocumentBindingGutter</span><span class="sxs-lookup"><span data-stu-id="1af78-105">DocumentBindingGutter</span></span>

<span data-ttu-id="1af78-106">本主題並非最新的。</span><span class="sxs-lookup"><span data-stu-id="1af78-106">This topic is not current.</span></span> <span data-ttu-id="1af78-107">如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。</span><span class="sxs-lookup"><span data-stu-id="1af78-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="1af78-108">指定裝訂裝訂邊的寬度。</span><span class="sxs-lookup"><span data-stu-id="1af78-108">Specifies the width of the binding gutter.</span></span>

-   [<span data-ttu-id="1af78-109">項目資訊</span><span class="sxs-lookup"><span data-stu-id="1af78-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="1af78-110">結構內容</span><span class="sxs-lookup"><span data-stu-id="1af78-110">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="1af78-111">項目資訊</span><span class="sxs-lookup"><span data-stu-id="1af78-111">Element Information</span></span>



| <span data-ttu-id="1af78-112">Name</span><span class="sxs-lookup"><span data-stu-id="1af78-112">Name</span></span> | <span data-ttu-id="1af78-113">值</span><span class="sxs-lookup"><span data-stu-id="1af78-113">Value</span></span> |
|----------------------------|----------------------------------------------|
| <span data-ttu-id="1af78-114">項目類型</span><span class="sxs-lookup"><span data-stu-id="1af78-114">Element Type</span></span> <br/>   | <span data-ttu-id="1af78-115">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="1af78-115">ParameterDef</span></span><br/>                      |
| <span data-ttu-id="1af78-116">範圍前置詞</span><span class="sxs-lookup"><span data-stu-id="1af78-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="1af78-117">文件</span><span class="sxs-lookup"><span data-stu-id="1af78-117">Document</span></span><br/>                          |
| <span data-ttu-id="1af78-118">備註</span><span class="sxs-lookup"><span data-stu-id="1af78-118">Notes</span></span> <br/>          | <span data-ttu-id="1af78-119">連結至 DocumentBinding 元素</span><span class="sxs-lookup"><span data-stu-id="1af78-119">Linked to DocumentBinding element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="1af78-120">結構內容</span><span class="sxs-lookup"><span data-stu-id="1af78-120">Structure Content</span></span>

<span data-ttu-id="1af78-121">此元素的 XML 結構為：</span><span class="sxs-lookup"><span data-stu-id="1af78-121">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="1af78-122">結構屬性</span><span class="sxs-lookup"><span data-stu-id="1af78-122">Structure Properties</span></span>

<span data-ttu-id="1af78-123">下表概述 XML 結構中所定義之變數的特性。</span><span class="sxs-lookup"><span data-stu-id="1af78-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="1af78-124">屬性</span><span class="sxs-lookup"><span data-stu-id="1af78-124">Property</span></span>                | <span data-ttu-id="1af78-125">xsi:type</span><span class="sxs-lookup"><span data-stu-id="1af78-125">xsi:type</span></span>           | <span data-ttu-id="1af78-126">值</span><span class="sxs-lookup"><span data-stu-id="1af78-126">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="1af78-127">DataType</span><span class="sxs-lookup"><span data-stu-id="1af78-127">DataType</span></span><br/>     | <span data-ttu-id="1af78-128">字串</span><span class="sxs-lookup"><span data-stu-id="1af78-128">string</span></span><br/>  | <span data-ttu-id="1af78-129">xs:integer</span><span class="sxs-lookup"><span data-stu-id="1af78-129">xs:integer</span></span><br/>      |
| <span data-ttu-id="1af78-130">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="1af78-130">DefaultValue</span></span><br/> | <span data-ttu-id="1af78-131">整數</span><span class="sxs-lookup"><span data-stu-id="1af78-131">integer</span></span><br/> | <span data-ttu-id="1af78-132">未定義</span><span class="sxs-lookup"><span data-stu-id="1af78-132">undefined</span></span><br/>       |
| <span data-ttu-id="1af78-133">MaxValue</span><span class="sxs-lookup"><span data-stu-id="1af78-133">MaxValue</span></span><br/>     | <span data-ttu-id="1af78-134">整數</span><span class="sxs-lookup"><span data-stu-id="1af78-134">integer</span></span><br/> | <span data-ttu-id="1af78-135">未定義</span><span class="sxs-lookup"><span data-stu-id="1af78-135">undefined</span></span><br/>       |
| <span data-ttu-id="1af78-136">MinValue</span><span class="sxs-lookup"><span data-stu-id="1af78-136">MinValue</span></span><br/>     | <span data-ttu-id="1af78-137">整數</span><span class="sxs-lookup"><span data-stu-id="1af78-137">integer</span></span><br/> | <span data-ttu-id="1af78-138">未定義</span><span class="sxs-lookup"><span data-stu-id="1af78-138">undefined</span></span><br/>       |
| <span data-ttu-id="1af78-139">強制性</span><span class="sxs-lookup"><span data-stu-id="1af78-139">Mandatory</span></span><br/>    | <span data-ttu-id="1af78-140">String</span><span class="sxs-lookup"><span data-stu-id="1af78-140">String</span></span><br/>  | <span data-ttu-id="1af78-141">psk：條件式</span><span class="sxs-lookup"><span data-stu-id="1af78-141">psk:Conditional</span></span><br/> |
| <span data-ttu-id="1af78-142">多個</span><span class="sxs-lookup"><span data-stu-id="1af78-142">Multiple</span></span><br/>     | <span data-ttu-id="1af78-143">整數</span><span class="sxs-lookup"><span data-stu-id="1af78-143">integer</span></span><br/> | <span data-ttu-id="1af78-144">1</span><span class="sxs-lookup"><span data-stu-id="1af78-144">1</span></span><br/>               |
| <span data-ttu-id="1af78-145">Unittype.pixel 表示</span><span class="sxs-lookup"><span data-stu-id="1af78-145">UnitType</span></span><br/>     | <span data-ttu-id="1af78-146">string</span><span class="sxs-lookup"><span data-stu-id="1af78-146">string</span></span><br/>  | <span data-ttu-id="1af78-147">微米</span><span class="sxs-lookup"><span data-stu-id="1af78-147">microns</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="1af78-148">相關主題</span><span class="sxs-lookup"><span data-stu-id="1af78-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1af78-149">列印架構規格</span><span class="sxs-lookup"><span data-stu-id="1af78-149">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




