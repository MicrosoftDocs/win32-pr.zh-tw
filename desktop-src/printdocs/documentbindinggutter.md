---
description: 本主題並非最新的。 如需最新資訊，請參閱列印架構規格。
ms.assetid: 903ad358-a060-4c8f-b72e-5ec2eb898248
title: DocumentBindingGutter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2372636ea22610e6a209cfad3f1fe6297be34833
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/26/2021
ms.locfileid: "107997185"
---
# <a name="documentbindinggutter"></a><span data-ttu-id="1226a-104">DocumentBindingGutter</span><span class="sxs-lookup"><span data-stu-id="1226a-104">DocumentBindingGutter</span></span>

<span data-ttu-id="1226a-105">本主題並非最新的。</span><span class="sxs-lookup"><span data-stu-id="1226a-105">This topic is not current.</span></span> <span data-ttu-id="1226a-106">如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。</span><span class="sxs-lookup"><span data-stu-id="1226a-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="1226a-107">指定裝訂裝訂邊的寬度。</span><span class="sxs-lookup"><span data-stu-id="1226a-107">Specifies the width of the binding gutter.</span></span>

-   [<span data-ttu-id="1226a-108">項目資訊</span><span class="sxs-lookup"><span data-stu-id="1226a-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="1226a-109">結構內容</span><span class="sxs-lookup"><span data-stu-id="1226a-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="1226a-110">項目資訊</span><span class="sxs-lookup"><span data-stu-id="1226a-110">Element Information</span></span>



| <span data-ttu-id="1226a-111">Name</span><span class="sxs-lookup"><span data-stu-id="1226a-111">Name</span></span> | <span data-ttu-id="1226a-112">值</span><span class="sxs-lookup"><span data-stu-id="1226a-112">Value</span></span> |
|----------------------------|----------------------------------------------|
| <span data-ttu-id="1226a-113">項目類型</span><span class="sxs-lookup"><span data-stu-id="1226a-113">Element Type</span></span> <br/>   | <span data-ttu-id="1226a-114">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="1226a-114">ParameterDef</span></span><br/>                      |
| <span data-ttu-id="1226a-115">範圍前置詞</span><span class="sxs-lookup"><span data-stu-id="1226a-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="1226a-116">文件</span><span class="sxs-lookup"><span data-stu-id="1226a-116">Document</span></span><br/>                          |
| <span data-ttu-id="1226a-117">備註</span><span class="sxs-lookup"><span data-stu-id="1226a-117">Notes</span></span> <br/>          | <span data-ttu-id="1226a-118">連結至 DocumentBinding 元素</span><span class="sxs-lookup"><span data-stu-id="1226a-118">Linked to DocumentBinding element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="1226a-119">結構內容</span><span class="sxs-lookup"><span data-stu-id="1226a-119">Structure Content</span></span>

<span data-ttu-id="1226a-120">此元素的 XML 結構為：</span><span class="sxs-lookup"><span data-stu-id="1226a-120">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="1226a-121">結構屬性</span><span class="sxs-lookup"><span data-stu-id="1226a-121">Structure Properties</span></span>

<span data-ttu-id="1226a-122">下表概述 XML 結構中所定義之變數的特性。</span><span class="sxs-lookup"><span data-stu-id="1226a-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="1226a-123">屬性</span><span class="sxs-lookup"><span data-stu-id="1226a-123">Property</span></span>                | <span data-ttu-id="1226a-124">xsi:type</span><span class="sxs-lookup"><span data-stu-id="1226a-124">xsi:type</span></span>           | <span data-ttu-id="1226a-125">值</span><span class="sxs-lookup"><span data-stu-id="1226a-125">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="1226a-126">DataType</span><span class="sxs-lookup"><span data-stu-id="1226a-126">DataType</span></span><br/>     | <span data-ttu-id="1226a-127">字串</span><span class="sxs-lookup"><span data-stu-id="1226a-127">string</span></span><br/>  | <span data-ttu-id="1226a-128">xs:integer</span><span class="sxs-lookup"><span data-stu-id="1226a-128">xs:integer</span></span><br/>      |
| <span data-ttu-id="1226a-129">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="1226a-129">DefaultValue</span></span><br/> | <span data-ttu-id="1226a-130">整數</span><span class="sxs-lookup"><span data-stu-id="1226a-130">integer</span></span><br/> | <span data-ttu-id="1226a-131">未定義</span><span class="sxs-lookup"><span data-stu-id="1226a-131">undefined</span></span><br/>       |
| <span data-ttu-id="1226a-132">MaxValue</span><span class="sxs-lookup"><span data-stu-id="1226a-132">MaxValue</span></span><br/>     | <span data-ttu-id="1226a-133">整數</span><span class="sxs-lookup"><span data-stu-id="1226a-133">integer</span></span><br/> | <span data-ttu-id="1226a-134">未定義</span><span class="sxs-lookup"><span data-stu-id="1226a-134">undefined</span></span><br/>       |
| <span data-ttu-id="1226a-135">MinValue</span><span class="sxs-lookup"><span data-stu-id="1226a-135">MinValue</span></span><br/>     | <span data-ttu-id="1226a-136">整數</span><span class="sxs-lookup"><span data-stu-id="1226a-136">integer</span></span><br/> | <span data-ttu-id="1226a-137">未定義</span><span class="sxs-lookup"><span data-stu-id="1226a-137">undefined</span></span><br/>       |
| <span data-ttu-id="1226a-138">強制性</span><span class="sxs-lookup"><span data-stu-id="1226a-138">Mandatory</span></span><br/>    | <span data-ttu-id="1226a-139">String</span><span class="sxs-lookup"><span data-stu-id="1226a-139">String</span></span><br/>  | <span data-ttu-id="1226a-140">psk：條件式</span><span class="sxs-lookup"><span data-stu-id="1226a-140">psk:Conditional</span></span><br/> |
| <span data-ttu-id="1226a-141">多個</span><span class="sxs-lookup"><span data-stu-id="1226a-141">Multiple</span></span><br/>     | <span data-ttu-id="1226a-142">整數</span><span class="sxs-lookup"><span data-stu-id="1226a-142">integer</span></span><br/> | <span data-ttu-id="1226a-143">1</span><span class="sxs-lookup"><span data-stu-id="1226a-143">1</span></span><br/>               |
| <span data-ttu-id="1226a-144">Unittype.pixel 表示</span><span class="sxs-lookup"><span data-stu-id="1226a-144">UnitType</span></span><br/>     | <span data-ttu-id="1226a-145">字串</span><span class="sxs-lookup"><span data-stu-id="1226a-145">string</span></span><br/>  | <span data-ttu-id="1226a-146">微米</span><span class="sxs-lookup"><span data-stu-id="1226a-146">microns</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="1226a-147">相關主題</span><span class="sxs-lookup"><span data-stu-id="1226a-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1226a-148">列印架構規格</span><span class="sxs-lookup"><span data-stu-id="1226a-148">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




