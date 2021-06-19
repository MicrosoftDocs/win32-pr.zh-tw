---
description: 取得 PageSourceColorProfileURI 參數的相關資訊。 本主題並非最新的。 如需最新資訊，請參閱列印架構規格。
ms.assetid: 25c3c70f-20e3-4e44-9c59-bb66b4bd14d9
title: PageSourceColorProfileURI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7b6acd064a6b0652720a6c0d783f10a7467fa16
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/19/2021
ms.locfileid: "112395623"
---
# <a name="pagesourcecolorprofileuri"></a><span data-ttu-id="3a955-105">PageSourceColorProfileURI</span><span class="sxs-lookup"><span data-stu-id="3a955-105">PageSourceColorProfileURI</span></span>

<span data-ttu-id="3a955-106">本主題並非最新的。</span><span class="sxs-lookup"><span data-stu-id="3a955-106">This topic is not current.</span></span> <span data-ttu-id="3a955-107">如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。</span><span class="sxs-lookup"><span data-stu-id="3a955-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="3a955-108">指定色彩設定檔的來源。</span><span class="sxs-lookup"><span data-stu-id="3a955-108">Specifies the source for color profile.</span></span>

-   [<span data-ttu-id="3a955-109">項目資訊</span><span class="sxs-lookup"><span data-stu-id="3a955-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="3a955-110">結構內容</span><span class="sxs-lookup"><span data-stu-id="3a955-110">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="3a955-111">項目資訊</span><span class="sxs-lookup"><span data-stu-id="3a955-111">Element Information</span></span>



| <span data-ttu-id="3a955-112">Name</span><span class="sxs-lookup"><span data-stu-id="3a955-112">Name</span></span> | <span data-ttu-id="3a955-113">值</span><span class="sxs-lookup"><span data-stu-id="3a955-113">Value</span></span> |
|----------------------------|-----------------------------------------------------|
| <span data-ttu-id="3a955-114">項目類型</span><span class="sxs-lookup"><span data-stu-id="3a955-114">Element Type</span></span> <br/>   | <span data-ttu-id="3a955-115">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="3a955-115">ParameterDef</span></span><br/>                             |
| <span data-ttu-id="3a955-116">範圍前置詞</span><span class="sxs-lookup"><span data-stu-id="3a955-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="3a955-117">頁面</span><span class="sxs-lookup"><span data-stu-id="3a955-117">Page</span></span><br/>                                     |
| <span data-ttu-id="3a955-118">備註</span><span class="sxs-lookup"><span data-stu-id="3a955-118">Notes</span></span> <br/>          | <span data-ttu-id="3a955-119">連結至 PageSourceColorProfile 元素</span><span class="sxs-lookup"><span data-stu-id="3a955-119">Linked to PageSourceColorProfile element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="3a955-120">結構內容</span><span class="sxs-lookup"><span data-stu-id="3a955-120">Structure Content</span></span>

<span data-ttu-id="3a955-121">此元素的 XML 結構為：</span><span class="sxs-lookup"><span data-stu-id="3a955-121">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageSourceColorProfileURI">
  <psf:Property name="psf:DataType">
    <psf:Value xsi:type="xs:string">xs:string</psf:Value>
  </psf:Property>
  <psf:Property name="psf:DefaultValue">
    <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
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

## <a name="structure-properties"></a><span data-ttu-id="3a955-122">結構屬性</span><span class="sxs-lookup"><span data-stu-id="3a955-122">Structure Properties</span></span>

<span data-ttu-id="3a955-123">下表概述 XML 結構中所定義之變數的特性。</span><span class="sxs-lookup"><span data-stu-id="3a955-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="3a955-124">屬性</span><span class="sxs-lookup"><span data-stu-id="3a955-124">Property</span></span>                | <span data-ttu-id="3a955-125">xsi:type</span><span class="sxs-lookup"><span data-stu-id="3a955-125">xsi:type</span></span>           | <span data-ttu-id="3a955-126">值</span><span class="sxs-lookup"><span data-stu-id="3a955-126">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="3a955-127">DataType</span><span class="sxs-lookup"><span data-stu-id="3a955-127">DataType</span></span><br/>     | <span data-ttu-id="3a955-128">字串</span><span class="sxs-lookup"><span data-stu-id="3a955-128">string</span></span><br/>  | <span data-ttu-id="3a955-129">xs:string</span><span class="sxs-lookup"><span data-stu-id="3a955-129">xs:string</span></span><br/>       |
| <span data-ttu-id="3a955-130">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="3a955-130">DefaultValue</span></span><br/> | <span data-ttu-id="3a955-131">字串</span><span class="sxs-lookup"><span data-stu-id="3a955-131">string</span></span><br/>  | <span data-ttu-id="3a955-132">未定義</span><span class="sxs-lookup"><span data-stu-id="3a955-132">undefined</span></span><br/>       |
| <span data-ttu-id="3a955-133">MaxLength</span><span class="sxs-lookup"><span data-stu-id="3a955-133">MaxLength</span></span><br/>    | <span data-ttu-id="3a955-134">整數</span><span class="sxs-lookup"><span data-stu-id="3a955-134">integer</span></span><br/> | <span data-ttu-id="3a955-135">未定義</span><span class="sxs-lookup"><span data-stu-id="3a955-135">undefined</span></span><br/>       |
| <span data-ttu-id="3a955-136">MinLength</span><span class="sxs-lookup"><span data-stu-id="3a955-136">MinLength</span></span><br/>    | <span data-ttu-id="3a955-137">整數</span><span class="sxs-lookup"><span data-stu-id="3a955-137">integer</span></span><br/> | <span data-ttu-id="3a955-138">1</span><span class="sxs-lookup"><span data-stu-id="3a955-138">1</span></span><br/>               |
| <span data-ttu-id="3a955-139">強制性</span><span class="sxs-lookup"><span data-stu-id="3a955-139">Mandatory</span></span><br/>    | <span data-ttu-id="3a955-140">string</span><span class="sxs-lookup"><span data-stu-id="3a955-140">string</span></span><br/>  | <span data-ttu-id="3a955-141">psk：條件式</span><span class="sxs-lookup"><span data-stu-id="3a955-141">psk:Conditional</span></span><br/> |
| <span data-ttu-id="3a955-142">Unittype.pixel 表示</span><span class="sxs-lookup"><span data-stu-id="3a955-142">UnitType</span></span><br/>     | <span data-ttu-id="3a955-143">string</span><span class="sxs-lookup"><span data-stu-id="3a955-143">string</span></span><br/>  | <span data-ttu-id="3a955-144">字元</span><span class="sxs-lookup"><span data-stu-id="3a955-144">characters</span></span><br/>      |



 

## <a name="related-topics"></a><span data-ttu-id="3a955-145">相關主題</span><span class="sxs-lookup"><span data-stu-id="3a955-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3a955-146">列印架構規格</span><span class="sxs-lookup"><span data-stu-id="3a955-146">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




