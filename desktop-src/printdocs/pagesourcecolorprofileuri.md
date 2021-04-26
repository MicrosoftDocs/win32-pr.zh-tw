---
description: 本主題並非最新的。 如需最新資訊，請參閱列印架構規格。
ms.assetid: 25c3c70f-20e3-4e44-9c59-bb66b4bd14d9
title: PageSourceColorProfileURI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f515fca037e58c0794f20bc1dd1afee8a779fb49
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/26/2021
ms.locfileid: "107996895"
---
# <a name="pagesourcecolorprofileuri"></a><span data-ttu-id="5cd12-104">PageSourceColorProfileURI</span><span class="sxs-lookup"><span data-stu-id="5cd12-104">PageSourceColorProfileURI</span></span>

<span data-ttu-id="5cd12-105">本主題並非最新的。</span><span class="sxs-lookup"><span data-stu-id="5cd12-105">This topic is not current.</span></span> <span data-ttu-id="5cd12-106">如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。</span><span class="sxs-lookup"><span data-stu-id="5cd12-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="5cd12-107">指定色彩設定檔的來源。</span><span class="sxs-lookup"><span data-stu-id="5cd12-107">Specifies the source for color profile.</span></span>

-   [<span data-ttu-id="5cd12-108">項目資訊</span><span class="sxs-lookup"><span data-stu-id="5cd12-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="5cd12-109">結構內容</span><span class="sxs-lookup"><span data-stu-id="5cd12-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="5cd12-110">項目資訊</span><span class="sxs-lookup"><span data-stu-id="5cd12-110">Element Information</span></span>



| <span data-ttu-id="5cd12-111">Name</span><span class="sxs-lookup"><span data-stu-id="5cd12-111">Name</span></span> | <span data-ttu-id="5cd12-112">值</span><span class="sxs-lookup"><span data-stu-id="5cd12-112">Value</span></span> |
|----------------------------|-----------------------------------------------------|
| <span data-ttu-id="5cd12-113">項目類型</span><span class="sxs-lookup"><span data-stu-id="5cd12-113">Element Type</span></span> <br/>   | <span data-ttu-id="5cd12-114">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="5cd12-114">ParameterDef</span></span><br/>                             |
| <span data-ttu-id="5cd12-115">範圍前置詞</span><span class="sxs-lookup"><span data-stu-id="5cd12-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="5cd12-116">頁面</span><span class="sxs-lookup"><span data-stu-id="5cd12-116">Page</span></span><br/>                                     |
| <span data-ttu-id="5cd12-117">備註</span><span class="sxs-lookup"><span data-stu-id="5cd12-117">Notes</span></span> <br/>          | <span data-ttu-id="5cd12-118">連結至 PageSourceColorProfile 元素</span><span class="sxs-lookup"><span data-stu-id="5cd12-118">Linked to PageSourceColorProfile element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="5cd12-119">結構內容</span><span class="sxs-lookup"><span data-stu-id="5cd12-119">Structure Content</span></span>

<span data-ttu-id="5cd12-120">此元素的 XML 結構為：</span><span class="sxs-lookup"><span data-stu-id="5cd12-120">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="5cd12-121">結構屬性</span><span class="sxs-lookup"><span data-stu-id="5cd12-121">Structure Properties</span></span>

<span data-ttu-id="5cd12-122">下表概述 XML 結構中所定義之變數的特性。</span><span class="sxs-lookup"><span data-stu-id="5cd12-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="5cd12-123">屬性</span><span class="sxs-lookup"><span data-stu-id="5cd12-123">Property</span></span>                | <span data-ttu-id="5cd12-124">xsi:type</span><span class="sxs-lookup"><span data-stu-id="5cd12-124">xsi:type</span></span>           | <span data-ttu-id="5cd12-125">值</span><span class="sxs-lookup"><span data-stu-id="5cd12-125">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="5cd12-126">DataType</span><span class="sxs-lookup"><span data-stu-id="5cd12-126">DataType</span></span><br/>     | <span data-ttu-id="5cd12-127">字串</span><span class="sxs-lookup"><span data-stu-id="5cd12-127">string</span></span><br/>  | <span data-ttu-id="5cd12-128">xs:string</span><span class="sxs-lookup"><span data-stu-id="5cd12-128">xs:string</span></span><br/>       |
| <span data-ttu-id="5cd12-129">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="5cd12-129">DefaultValue</span></span><br/> | <span data-ttu-id="5cd12-130">字串</span><span class="sxs-lookup"><span data-stu-id="5cd12-130">string</span></span><br/>  | <span data-ttu-id="5cd12-131">未定義</span><span class="sxs-lookup"><span data-stu-id="5cd12-131">undefined</span></span><br/>       |
| <span data-ttu-id="5cd12-132">MaxLength</span><span class="sxs-lookup"><span data-stu-id="5cd12-132">MaxLength</span></span><br/>    | <span data-ttu-id="5cd12-133">整數</span><span class="sxs-lookup"><span data-stu-id="5cd12-133">integer</span></span><br/> | <span data-ttu-id="5cd12-134">未定義</span><span class="sxs-lookup"><span data-stu-id="5cd12-134">undefined</span></span><br/>       |
| <span data-ttu-id="5cd12-135">MinLength</span><span class="sxs-lookup"><span data-stu-id="5cd12-135">MinLength</span></span><br/>    | <span data-ttu-id="5cd12-136">整數</span><span class="sxs-lookup"><span data-stu-id="5cd12-136">integer</span></span><br/> | <span data-ttu-id="5cd12-137">1</span><span class="sxs-lookup"><span data-stu-id="5cd12-137">1</span></span><br/>               |
| <span data-ttu-id="5cd12-138">強制性</span><span class="sxs-lookup"><span data-stu-id="5cd12-138">Mandatory</span></span><br/>    | <span data-ttu-id="5cd12-139">字串</span><span class="sxs-lookup"><span data-stu-id="5cd12-139">string</span></span><br/>  | <span data-ttu-id="5cd12-140">psk：條件式</span><span class="sxs-lookup"><span data-stu-id="5cd12-140">psk:Conditional</span></span><br/> |
| <span data-ttu-id="5cd12-141">Unittype.pixel 表示</span><span class="sxs-lookup"><span data-stu-id="5cd12-141">UnitType</span></span><br/>     | <span data-ttu-id="5cd12-142">字串</span><span class="sxs-lookup"><span data-stu-id="5cd12-142">string</span></span><br/>  | <span data-ttu-id="5cd12-143">字元</span><span class="sxs-lookup"><span data-stu-id="5cd12-143">characters</span></span><br/>      |



 

## <a name="related-topics"></a><span data-ttu-id="5cd12-144">相關主題</span><span class="sxs-lookup"><span data-stu-id="5cd12-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5cd12-145">列印架構規格</span><span class="sxs-lookup"><span data-stu-id="5cd12-145">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




