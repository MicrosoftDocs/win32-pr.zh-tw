---
description: 本主題並非最新的。 如需最新資訊，請參閱列印架構規格。
ms.assetid: a15fe075-6696-4c70-b658-ae62d542bb4e
title: PageCopies
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83b1fc822d27d104364c2414ca89cf1fdf30c7d3
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/26/2021
ms.locfileid: "107997665"
---
# <a name="pagecopies"></a><span data-ttu-id="469a1-104">PageCopies</span><span class="sxs-lookup"><span data-stu-id="469a1-104">PageCopies</span></span>

<span data-ttu-id="469a1-105">本主題並非最新的。</span><span class="sxs-lookup"><span data-stu-id="469a1-105">This topic is not current.</span></span> <span data-ttu-id="469a1-106">如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。</span><span class="sxs-lookup"><span data-stu-id="469a1-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="469a1-107">指定頁面的複本數目。</span><span class="sxs-lookup"><span data-stu-id="469a1-107">Specifies the number of copies of a page.</span></span>

-   [<span data-ttu-id="469a1-108">項目資訊</span><span class="sxs-lookup"><span data-stu-id="469a1-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="469a1-109">結構內容</span><span class="sxs-lookup"><span data-stu-id="469a1-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="469a1-110">項目資訊</span><span class="sxs-lookup"><span data-stu-id="469a1-110">Element Information</span></span>



| <span data-ttu-id="469a1-111">Name</span><span class="sxs-lookup"><span data-stu-id="469a1-111">Name</span></span> | <span data-ttu-id="469a1-112">值</span><span class="sxs-lookup"><span data-stu-id="469a1-112">Value</span></span> |
|----------------------------|-------------------------|
| <span data-ttu-id="469a1-113">項目類型</span><span class="sxs-lookup"><span data-stu-id="469a1-113">Element Type</span></span> <br/>   | <span data-ttu-id="469a1-114">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="469a1-114">ParameterDef</span></span><br/> |
| <span data-ttu-id="469a1-115">範圍前置詞</span><span class="sxs-lookup"><span data-stu-id="469a1-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="469a1-116">頁面</span><span class="sxs-lookup"><span data-stu-id="469a1-116">Page</span></span><br/>         |
| <span data-ttu-id="469a1-117">注意</span><span class="sxs-lookup"><span data-stu-id="469a1-117">Notes</span></span> <br/>          | <span data-ttu-id="469a1-118">None</span><span class="sxs-lookup"><span data-stu-id="469a1-118">None</span></span><br/>         |



 

## <a name="structure-content"></a><span data-ttu-id="469a1-119">結構內容</span><span class="sxs-lookup"><span data-stu-id="469a1-119">Structure Content</span></span>

<span data-ttu-id="469a1-120">此元素的 XML 結構為：</span><span class="sxs-lookup"><span data-stu-id="469a1-120">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageCopies">
  <psf:Property name="psf:DataType">
    <psf:Value xsi:type="xs:string">xs:integer</psf:Value>
  </psf:Property>
  <psf:Property name="psf:DefaultValue">
    <psf:Value xsi:type="xs:integer">1</psf:Value>
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
    <psf:Value xsi:type="xs:string">psk:Unconditional</psf:Value>
  </psf:Property>
  <psf:Property name="psf:UnitType">
    <psf:Value xsi:type="xs:string">copies</psf:Value>
  </psf:Property>
</psf:ParameterDef>
      
```

## <a name="structure-properties"></a><span data-ttu-id="469a1-121">結構屬性</span><span class="sxs-lookup"><span data-stu-id="469a1-121">Structure Properties</span></span>

<span data-ttu-id="469a1-122">下表概述 XML 結構中所定義之變數的特性。</span><span class="sxs-lookup"><span data-stu-id="469a1-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="469a1-123">屬性</span><span class="sxs-lookup"><span data-stu-id="469a1-123">Property</span></span>                | <span data-ttu-id="469a1-124">xsi:type</span><span class="sxs-lookup"><span data-stu-id="469a1-124">xsi:type</span></span>           | <span data-ttu-id="469a1-125">值</span><span class="sxs-lookup"><span data-stu-id="469a1-125">Value</span></span>                        |
|-------------------------|--------------------|------------------------------|
| <span data-ttu-id="469a1-126">DataType</span><span class="sxs-lookup"><span data-stu-id="469a1-126">DataType</span></span><br/>     | <span data-ttu-id="469a1-127">字串</span><span class="sxs-lookup"><span data-stu-id="469a1-127">string</span></span><br/>  | <span data-ttu-id="469a1-128">xs:integer</span><span class="sxs-lookup"><span data-stu-id="469a1-128">xs:integer</span></span><br/>        |
| <span data-ttu-id="469a1-129">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="469a1-129">DefaultValue</span></span><br/> | <span data-ttu-id="469a1-130">整數</span><span class="sxs-lookup"><span data-stu-id="469a1-130">integer</span></span><br/> | <span data-ttu-id="469a1-131">1</span><span class="sxs-lookup"><span data-stu-id="469a1-131">1</span></span><br/>                 |
| <span data-ttu-id="469a1-132">MaxValue</span><span class="sxs-lookup"><span data-stu-id="469a1-132">MaxValue</span></span><br/>     | <span data-ttu-id="469a1-133">整數</span><span class="sxs-lookup"><span data-stu-id="469a1-133">integer</span></span><br/> | <span data-ttu-id="469a1-134">未定義</span><span class="sxs-lookup"><span data-stu-id="469a1-134">undefined</span></span><br/>         |
| <span data-ttu-id="469a1-135">MinValue</span><span class="sxs-lookup"><span data-stu-id="469a1-135">MinValue</span></span><br/>     | <span data-ttu-id="469a1-136">整數</span><span class="sxs-lookup"><span data-stu-id="469a1-136">integer</span></span><br/> | <span data-ttu-id="469a1-137">1</span><span class="sxs-lookup"><span data-stu-id="469a1-137">1</span></span><br/>                 |
| <span data-ttu-id="469a1-138">強制性</span><span class="sxs-lookup"><span data-stu-id="469a1-138">Mandatory</span></span><br/>    | <span data-ttu-id="469a1-139">字串</span><span class="sxs-lookup"><span data-stu-id="469a1-139">string</span></span><br/>  | <span data-ttu-id="469a1-140">psk：無條件</span><span class="sxs-lookup"><span data-stu-id="469a1-140">psk:Unconditional</span></span><br/> |
| <span data-ttu-id="469a1-141">多個</span><span class="sxs-lookup"><span data-stu-id="469a1-141">Multiple</span></span><br/>     | <span data-ttu-id="469a1-142">整數</span><span class="sxs-lookup"><span data-stu-id="469a1-142">integer</span></span><br/> | <span data-ttu-id="469a1-143">1</span><span class="sxs-lookup"><span data-stu-id="469a1-143">1</span></span><br/>                 |
| <span data-ttu-id="469a1-144">Unittype.pixel 表示</span><span class="sxs-lookup"><span data-stu-id="469a1-144">UnitType</span></span><br/>     | <span data-ttu-id="469a1-145">字串</span><span class="sxs-lookup"><span data-stu-id="469a1-145">string</span></span><br/>  | <span data-ttu-id="469a1-146">副本</span><span class="sxs-lookup"><span data-stu-id="469a1-146">copies</span></span><br/>            |



 

## <a name="related-topics"></a><span data-ttu-id="469a1-147">相關主題</span><span class="sxs-lookup"><span data-stu-id="469a1-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="469a1-148">列印架構規格</span><span class="sxs-lookup"><span data-stu-id="469a1-148">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




