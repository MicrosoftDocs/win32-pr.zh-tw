---
description: 本主題並非最新的。 如需最新資訊，請參閱列印架構規格。
ms.assetid: 49a60a94-fb65-4439-bebf-3f77ea0861fe
title: PageScalingScale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 974242cf43bae50a8e81b17bcdd13d653032c6a9
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/26/2021
ms.locfileid: "107999195"
---
# <a name="pagescalingscale"></a><span data-ttu-id="abe9c-104">PageScalingScale</span><span class="sxs-lookup"><span data-stu-id="abe9c-104">PageScalingScale</span></span>

<span data-ttu-id="abe9c-105">本主題並非最新的。</span><span class="sxs-lookup"><span data-stu-id="abe9c-105">This topic is not current.</span></span> <span data-ttu-id="abe9c-106">如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。</span><span class="sxs-lookup"><span data-stu-id="abe9c-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="abe9c-107">指定自訂方形縮放比例的縮放比例。</span><span class="sxs-lookup"><span data-stu-id="abe9c-107">Specifies the scaling factor for custom square scaling.</span></span>

-   [<span data-ttu-id="abe9c-108">項目資訊</span><span class="sxs-lookup"><span data-stu-id="abe9c-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="abe9c-109">結構內容</span><span class="sxs-lookup"><span data-stu-id="abe9c-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="abe9c-110">項目資訊</span><span class="sxs-lookup"><span data-stu-id="abe9c-110">Element Information</span></span>



| <span data-ttu-id="abe9c-111">Name</span><span class="sxs-lookup"><span data-stu-id="abe9c-111">Name</span></span> | <span data-ttu-id="abe9c-112">值</span><span class="sxs-lookup"><span data-stu-id="abe9c-112">Value</span></span> |
|----------------------------|---------------------------------------------------------|
| <span data-ttu-id="abe9c-113">項目類型</span><span class="sxs-lookup"><span data-stu-id="abe9c-113">Element Type</span></span> <br/>   | <span data-ttu-id="abe9c-114">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="abe9c-114">ParameterDef</span></span><br/>                                 |
| <span data-ttu-id="abe9c-115">範圍前置詞</span><span class="sxs-lookup"><span data-stu-id="abe9c-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="abe9c-116">頁面</span><span class="sxs-lookup"><span data-stu-id="abe9c-116">Page</span></span><br/>                                         |
| <span data-ttu-id="abe9c-117">備註</span><span class="sxs-lookup"><span data-stu-id="abe9c-117">Notes</span></span> <br/>          | <span data-ttu-id="abe9c-118">連結至 PageScaling 元素，自訂選項</span><span class="sxs-lookup"><span data-stu-id="abe9c-118">Linked to PageScaling element, Custom option</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="abe9c-119">結構內容</span><span class="sxs-lookup"><span data-stu-id="abe9c-119">Structure Content</span></span>

<span data-ttu-id="abe9c-120">此元素的 XML 結構為：</span><span class="sxs-lookup"><span data-stu-id="abe9c-120">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageScalingScale">
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
    <psf:Value xsi:type="xs:integer">1</psf:Value>
  </psf:Property>
  <psf:Property name="psf:Multiple">
    <psf:Value xsi:type="xs:integer">1</psf:Value>
  </psf:Property>
  <psf:Property name="psf:Mandatory">
    <psf:Value xsi:type="xs:string">psk:Conditional</psf:Value>
  </psf:Property>
  <psf:Property name="psf:UnitType">
    <psf:Value xsi:type="xs:string">percent</psf:Value>
  </psf:Property>
</psf:ParameterDef>
      
```

## <a name="structure-properties"></a><span data-ttu-id="abe9c-121">結構屬性</span><span class="sxs-lookup"><span data-stu-id="abe9c-121">Structure Properties</span></span>

<span data-ttu-id="abe9c-122">下表概述 XML 結構中所定義之變數的特性。</span><span class="sxs-lookup"><span data-stu-id="abe9c-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="abe9c-123">屬性</span><span class="sxs-lookup"><span data-stu-id="abe9c-123">Property</span></span>                | <span data-ttu-id="abe9c-124">xsi:type</span><span class="sxs-lookup"><span data-stu-id="abe9c-124">xsi:type</span></span>           | <span data-ttu-id="abe9c-125">值</span><span class="sxs-lookup"><span data-stu-id="abe9c-125">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="abe9c-126">DataType</span><span class="sxs-lookup"><span data-stu-id="abe9c-126">DataType</span></span><br/>     | <span data-ttu-id="abe9c-127">字串</span><span class="sxs-lookup"><span data-stu-id="abe9c-127">string</span></span><br/>  | <span data-ttu-id="abe9c-128">xs:integer</span><span class="sxs-lookup"><span data-stu-id="abe9c-128">xs:integer</span></span><br/>      |
| <span data-ttu-id="abe9c-129">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="abe9c-129">DefaultValue</span></span><br/> | <span data-ttu-id="abe9c-130">整數</span><span class="sxs-lookup"><span data-stu-id="abe9c-130">integer</span></span><br/> | <span data-ttu-id="abe9c-131">未定義</span><span class="sxs-lookup"><span data-stu-id="abe9c-131">undefined</span></span><br/>       |
| <span data-ttu-id="abe9c-132">MaxValue</span><span class="sxs-lookup"><span data-stu-id="abe9c-132">MaxValue</span></span><br/>     | <span data-ttu-id="abe9c-133">整數</span><span class="sxs-lookup"><span data-stu-id="abe9c-133">integer</span></span><br/> | <span data-ttu-id="abe9c-134">未定義</span><span class="sxs-lookup"><span data-stu-id="abe9c-134">undefined</span></span><br/>       |
| <span data-ttu-id="abe9c-135">MinValue</span><span class="sxs-lookup"><span data-stu-id="abe9c-135">MinValue</span></span><br/>     | <span data-ttu-id="abe9c-136">整數</span><span class="sxs-lookup"><span data-stu-id="abe9c-136">integer</span></span><br/> | <span data-ttu-id="abe9c-137">1</span><span class="sxs-lookup"><span data-stu-id="abe9c-137">1</span></span><br/>               |
| <span data-ttu-id="abe9c-138">強制性</span><span class="sxs-lookup"><span data-stu-id="abe9c-138">Mandatory</span></span><br/>    | <span data-ttu-id="abe9c-139">字串</span><span class="sxs-lookup"><span data-stu-id="abe9c-139">string</span></span><br/>  | <span data-ttu-id="abe9c-140">psk：條件式</span><span class="sxs-lookup"><span data-stu-id="abe9c-140">psk:Conditional</span></span><br/> |
| <span data-ttu-id="abe9c-141">多個</span><span class="sxs-lookup"><span data-stu-id="abe9c-141">Multiple</span></span><br/>     | <span data-ttu-id="abe9c-142">整數</span><span class="sxs-lookup"><span data-stu-id="abe9c-142">integer</span></span><br/> | <span data-ttu-id="abe9c-143">1</span><span class="sxs-lookup"><span data-stu-id="abe9c-143">1</span></span><br/>               |
| <span data-ttu-id="abe9c-144">Unittype.pixel 表示</span><span class="sxs-lookup"><span data-stu-id="abe9c-144">UnitType</span></span><br/>     | <span data-ttu-id="abe9c-145">字串</span><span class="sxs-lookup"><span data-stu-id="abe9c-145">string</span></span><br/>  | <span data-ttu-id="abe9c-146">percent</span><span class="sxs-lookup"><span data-stu-id="abe9c-146">percent</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="abe9c-147">相關主題</span><span class="sxs-lookup"><span data-stu-id="abe9c-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="abe9c-148">列印架構規格</span><span class="sxs-lookup"><span data-stu-id="abe9c-148">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




