---
description: 本主題並非最新的。 如需最新資訊，請參閱列印架構規格。
ms.assetid: a15fe075-6696-4c70-b658-ae62d542bb4e
title: PageCopies
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6feef0745e3f9a86b3697b7e0ab65111fc3dfcb
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/05/2021
ms.locfileid: "104195809"
---
# <a name="pagecopies"></a><span data-ttu-id="6bd7c-104">PageCopies</span><span class="sxs-lookup"><span data-stu-id="6bd7c-104">PageCopies</span></span>

<span data-ttu-id="6bd7c-105">本主題並非最新的。</span><span class="sxs-lookup"><span data-stu-id="6bd7c-105">This topic is not current.</span></span> <span data-ttu-id="6bd7c-106">如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。</span><span class="sxs-lookup"><span data-stu-id="6bd7c-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="6bd7c-107">指定頁面的複本數目。</span><span class="sxs-lookup"><span data-stu-id="6bd7c-107">Specifies the number of copies of a page.</span></span>

-   [<span data-ttu-id="6bd7c-108">項目資訊</span><span class="sxs-lookup"><span data-stu-id="6bd7c-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="6bd7c-109">結構內容</span><span class="sxs-lookup"><span data-stu-id="6bd7c-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="6bd7c-110">項目資訊</span><span class="sxs-lookup"><span data-stu-id="6bd7c-110">Element Information</span></span>



| <span data-ttu-id="6bd7c-111">Name</span><span class="sxs-lookup"><span data-stu-id="6bd7c-111">Name</span></span>                       |                         |
|----------------------------|-------------------------|
| <span data-ttu-id="6bd7c-112">項目類型</span><span class="sxs-lookup"><span data-stu-id="6bd7c-112">Element Type</span></span> <br/>   | <span data-ttu-id="6bd7c-113">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="6bd7c-113">ParameterDef</span></span><br/> |
| <span data-ttu-id="6bd7c-114">範圍前置詞</span><span class="sxs-lookup"><span data-stu-id="6bd7c-114">Scoping Prefix</span></span> <br/> | <span data-ttu-id="6bd7c-115">頁面</span><span class="sxs-lookup"><span data-stu-id="6bd7c-115">Page</span></span><br/>         |
| <span data-ttu-id="6bd7c-116">注意</span><span class="sxs-lookup"><span data-stu-id="6bd7c-116">Notes</span></span> <br/>          | <span data-ttu-id="6bd7c-117">None</span><span class="sxs-lookup"><span data-stu-id="6bd7c-117">None</span></span><br/>         |



 

## <a name="structure-content"></a><span data-ttu-id="6bd7c-118">結構內容</span><span class="sxs-lookup"><span data-stu-id="6bd7c-118">Structure Content</span></span>

<span data-ttu-id="6bd7c-119">此元素的 XML 結構為：</span><span class="sxs-lookup"><span data-stu-id="6bd7c-119">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="6bd7c-120">結構屬性</span><span class="sxs-lookup"><span data-stu-id="6bd7c-120">Structure Properties</span></span>

<span data-ttu-id="6bd7c-121">下表概述 XML 結構中所定義之變數的特性。</span><span class="sxs-lookup"><span data-stu-id="6bd7c-121">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="6bd7c-122">屬性</span><span class="sxs-lookup"><span data-stu-id="6bd7c-122">Property</span></span>                | <span data-ttu-id="6bd7c-123">xsi:type</span><span class="sxs-lookup"><span data-stu-id="6bd7c-123">xsi:type</span></span>           | <span data-ttu-id="6bd7c-124">值</span><span class="sxs-lookup"><span data-stu-id="6bd7c-124">Value</span></span>                        |
|-------------------------|--------------------|------------------------------|
| <span data-ttu-id="6bd7c-125">DataType</span><span class="sxs-lookup"><span data-stu-id="6bd7c-125">DataType</span></span><br/>     | <span data-ttu-id="6bd7c-126">字串</span><span class="sxs-lookup"><span data-stu-id="6bd7c-126">string</span></span><br/>  | <span data-ttu-id="6bd7c-127">xs:integer</span><span class="sxs-lookup"><span data-stu-id="6bd7c-127">xs:integer</span></span><br/>        |
| <span data-ttu-id="6bd7c-128">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="6bd7c-128">DefaultValue</span></span><br/> | <span data-ttu-id="6bd7c-129">整數</span><span class="sxs-lookup"><span data-stu-id="6bd7c-129">integer</span></span><br/> | <span data-ttu-id="6bd7c-130">1</span><span class="sxs-lookup"><span data-stu-id="6bd7c-130">1</span></span><br/>                 |
| <span data-ttu-id="6bd7c-131">MaxValue</span><span class="sxs-lookup"><span data-stu-id="6bd7c-131">MaxValue</span></span><br/>     | <span data-ttu-id="6bd7c-132">整數</span><span class="sxs-lookup"><span data-stu-id="6bd7c-132">integer</span></span><br/> | <span data-ttu-id="6bd7c-133">未定義</span><span class="sxs-lookup"><span data-stu-id="6bd7c-133">undefined</span></span><br/>         |
| <span data-ttu-id="6bd7c-134">MinValue</span><span class="sxs-lookup"><span data-stu-id="6bd7c-134">MinValue</span></span><br/>     | <span data-ttu-id="6bd7c-135">整數</span><span class="sxs-lookup"><span data-stu-id="6bd7c-135">integer</span></span><br/> | <span data-ttu-id="6bd7c-136">1</span><span class="sxs-lookup"><span data-stu-id="6bd7c-136">1</span></span><br/>                 |
| <span data-ttu-id="6bd7c-137">強制性</span><span class="sxs-lookup"><span data-stu-id="6bd7c-137">Mandatory</span></span><br/>    | <span data-ttu-id="6bd7c-138">字串</span><span class="sxs-lookup"><span data-stu-id="6bd7c-138">string</span></span><br/>  | <span data-ttu-id="6bd7c-139">psk：無條件</span><span class="sxs-lookup"><span data-stu-id="6bd7c-139">psk:Unconditional</span></span><br/> |
| <span data-ttu-id="6bd7c-140">多個</span><span class="sxs-lookup"><span data-stu-id="6bd7c-140">Multiple</span></span><br/>     | <span data-ttu-id="6bd7c-141">整數</span><span class="sxs-lookup"><span data-stu-id="6bd7c-141">integer</span></span><br/> | <span data-ttu-id="6bd7c-142">1</span><span class="sxs-lookup"><span data-stu-id="6bd7c-142">1</span></span><br/>                 |
| <span data-ttu-id="6bd7c-143">Unittype.pixel 表示</span><span class="sxs-lookup"><span data-stu-id="6bd7c-143">UnitType</span></span><br/>     | <span data-ttu-id="6bd7c-144">字串</span><span class="sxs-lookup"><span data-stu-id="6bd7c-144">string</span></span><br/>  | <span data-ttu-id="6bd7c-145">副本</span><span class="sxs-lookup"><span data-stu-id="6bd7c-145">copies</span></span><br/>            |



 

## <a name="related-topics"></a><span data-ttu-id="6bd7c-146">相關主題</span><span class="sxs-lookup"><span data-stu-id="6bd7c-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6bd7c-147">列印架構規格</span><span class="sxs-lookup"><span data-stu-id="6bd7c-147">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




