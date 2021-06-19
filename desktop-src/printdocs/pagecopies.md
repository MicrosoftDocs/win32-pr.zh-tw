---
description: 讀取 PageCopies 參數的參考資訊。 本主題並非最新的。 如需最新資訊，請參閱列印架構規格。
ms.assetid: a15fe075-6696-4c70-b658-ae62d542bb4e
title: PageCopies
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5002850fa1df5a86b0022a941e3b2a1f7e414a44
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/19/2021
ms.locfileid: "112396683"
---
# <a name="pagecopies"></a><span data-ttu-id="a9005-105">PageCopies</span><span class="sxs-lookup"><span data-stu-id="a9005-105">PageCopies</span></span>

<span data-ttu-id="a9005-106">本主題並非最新的。</span><span class="sxs-lookup"><span data-stu-id="a9005-106">This topic is not current.</span></span> <span data-ttu-id="a9005-107">如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。</span><span class="sxs-lookup"><span data-stu-id="a9005-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="a9005-108">指定頁面的複本數目。</span><span class="sxs-lookup"><span data-stu-id="a9005-108">Specifies the number of copies of a page.</span></span>

-   [<span data-ttu-id="a9005-109">項目資訊</span><span class="sxs-lookup"><span data-stu-id="a9005-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="a9005-110">結構內容</span><span class="sxs-lookup"><span data-stu-id="a9005-110">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="a9005-111">項目資訊</span><span class="sxs-lookup"><span data-stu-id="a9005-111">Element Information</span></span>



| <span data-ttu-id="a9005-112">Name</span><span class="sxs-lookup"><span data-stu-id="a9005-112">Name</span></span> | <span data-ttu-id="a9005-113">值</span><span class="sxs-lookup"><span data-stu-id="a9005-113">Value</span></span> |
|----------------------------|-------------------------|
| <span data-ttu-id="a9005-114">項目類型</span><span class="sxs-lookup"><span data-stu-id="a9005-114">Element Type</span></span> <br/>   | <span data-ttu-id="a9005-115">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="a9005-115">ParameterDef</span></span><br/> |
| <span data-ttu-id="a9005-116">範圍前置詞</span><span class="sxs-lookup"><span data-stu-id="a9005-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="a9005-117">頁面</span><span class="sxs-lookup"><span data-stu-id="a9005-117">Page</span></span><br/>         |
| <span data-ttu-id="a9005-118">注意</span><span class="sxs-lookup"><span data-stu-id="a9005-118">Notes</span></span> <br/>          | <span data-ttu-id="a9005-119">None</span><span class="sxs-lookup"><span data-stu-id="a9005-119">None</span></span><br/>         |



 

## <a name="structure-content"></a><span data-ttu-id="a9005-120">結構內容</span><span class="sxs-lookup"><span data-stu-id="a9005-120">Structure Content</span></span>

<span data-ttu-id="a9005-121">此元素的 XML 結構為：</span><span class="sxs-lookup"><span data-stu-id="a9005-121">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="a9005-122">結構屬性</span><span class="sxs-lookup"><span data-stu-id="a9005-122">Structure Properties</span></span>

<span data-ttu-id="a9005-123">下表概述 XML 結構中所定義之變數的特性。</span><span class="sxs-lookup"><span data-stu-id="a9005-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="a9005-124">屬性</span><span class="sxs-lookup"><span data-stu-id="a9005-124">Property</span></span>                | <span data-ttu-id="a9005-125">xsi:type</span><span class="sxs-lookup"><span data-stu-id="a9005-125">xsi:type</span></span>           | <span data-ttu-id="a9005-126">值</span><span class="sxs-lookup"><span data-stu-id="a9005-126">Value</span></span>                        |
|-------------------------|--------------------|------------------------------|
| <span data-ttu-id="a9005-127">DataType</span><span class="sxs-lookup"><span data-stu-id="a9005-127">DataType</span></span><br/>     | <span data-ttu-id="a9005-128">字串</span><span class="sxs-lookup"><span data-stu-id="a9005-128">string</span></span><br/>  | <span data-ttu-id="a9005-129">xs:integer</span><span class="sxs-lookup"><span data-stu-id="a9005-129">xs:integer</span></span><br/>        |
| <span data-ttu-id="a9005-130">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="a9005-130">DefaultValue</span></span><br/> | <span data-ttu-id="a9005-131">整數</span><span class="sxs-lookup"><span data-stu-id="a9005-131">integer</span></span><br/> | <span data-ttu-id="a9005-132">1</span><span class="sxs-lookup"><span data-stu-id="a9005-132">1</span></span><br/>                 |
| <span data-ttu-id="a9005-133">MaxValue</span><span class="sxs-lookup"><span data-stu-id="a9005-133">MaxValue</span></span><br/>     | <span data-ttu-id="a9005-134">整數</span><span class="sxs-lookup"><span data-stu-id="a9005-134">integer</span></span><br/> | <span data-ttu-id="a9005-135">未定義</span><span class="sxs-lookup"><span data-stu-id="a9005-135">undefined</span></span><br/>         |
| <span data-ttu-id="a9005-136">MinValue</span><span class="sxs-lookup"><span data-stu-id="a9005-136">MinValue</span></span><br/>     | <span data-ttu-id="a9005-137">整數</span><span class="sxs-lookup"><span data-stu-id="a9005-137">integer</span></span><br/> | <span data-ttu-id="a9005-138">1</span><span class="sxs-lookup"><span data-stu-id="a9005-138">1</span></span><br/>                 |
| <span data-ttu-id="a9005-139">強制性</span><span class="sxs-lookup"><span data-stu-id="a9005-139">Mandatory</span></span><br/>    | <span data-ttu-id="a9005-140">string</span><span class="sxs-lookup"><span data-stu-id="a9005-140">string</span></span><br/>  | <span data-ttu-id="a9005-141">psk：無條件</span><span class="sxs-lookup"><span data-stu-id="a9005-141">psk:Unconditional</span></span><br/> |
| <span data-ttu-id="a9005-142">多個</span><span class="sxs-lookup"><span data-stu-id="a9005-142">Multiple</span></span><br/>     | <span data-ttu-id="a9005-143">整數</span><span class="sxs-lookup"><span data-stu-id="a9005-143">integer</span></span><br/> | <span data-ttu-id="a9005-144">1</span><span class="sxs-lookup"><span data-stu-id="a9005-144">1</span></span><br/>                 |
| <span data-ttu-id="a9005-145">Unittype.pixel 表示</span><span class="sxs-lookup"><span data-stu-id="a9005-145">UnitType</span></span><br/>     | <span data-ttu-id="a9005-146">string</span><span class="sxs-lookup"><span data-stu-id="a9005-146">string</span></span><br/>  | <span data-ttu-id="a9005-147">副本</span><span class="sxs-lookup"><span data-stu-id="a9005-147">copies</span></span><br/>            |



 

## <a name="related-topics"></a><span data-ttu-id="a9005-148">相關主題</span><span class="sxs-lookup"><span data-stu-id="a9005-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a9005-149">列印架構規格</span><span class="sxs-lookup"><span data-stu-id="a9005-149">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




