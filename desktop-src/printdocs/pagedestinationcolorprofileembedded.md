---
description: 閱讀 PageDestinationColorProfileEmbedded 參數。 本主題並非最新的。 如需最新資訊，請參閱列印架構規格。
ms.assetid: b360f870-bfaa-4d4d-adce-17fcfc48b6a6
title: PageDestinationColorProfileEmbedded
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05865636b6554873844a99b523f8c21fe2bfc1c7
ms.sourcegitcommit: 998d50f6def8a25850fc113fc8a2df903c829c5e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/09/2021
ms.locfileid: "113549206"
---
# <a name="pagedestinationcolorprofileembedded"></a><span data-ttu-id="e59a9-105">PageDestinationColorProfileEmbedded</span><span class="sxs-lookup"><span data-stu-id="e59a9-105">PageDestinationColorProfileEmbedded</span></span>

<span data-ttu-id="e59a9-106">本主題並非最新的。</span><span class="sxs-lookup"><span data-stu-id="e59a9-106">This topic is not current.</span></span> <span data-ttu-id="e59a9-107">如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。</span><span class="sxs-lookup"><span data-stu-id="e59a9-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="e59a9-108">指定內嵌的目的地色彩設定檔。</span><span class="sxs-lookup"><span data-stu-id="e59a9-108">Specifies the embedded destination color profile.</span></span>

-   [<span data-ttu-id="e59a9-109">項目資訊</span><span class="sxs-lookup"><span data-stu-id="e59a9-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="e59a9-110">結構內容</span><span class="sxs-lookup"><span data-stu-id="e59a9-110">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="e59a9-111">項目資訊</span><span class="sxs-lookup"><span data-stu-id="e59a9-111">Element Information</span></span>



| <span data-ttu-id="e59a9-112">Name</span><span class="sxs-lookup"><span data-stu-id="e59a9-112">Name</span></span> | <span data-ttu-id="e59a9-113">值</span><span class="sxs-lookup"><span data-stu-id="e59a9-113">Value</span></span> |
|----------------------------|----------------------------------------------------------|
| <span data-ttu-id="e59a9-114">項目類型</span><span class="sxs-lookup"><span data-stu-id="e59a9-114">Element Type</span></span> <br/>   | <span data-ttu-id="e59a9-115">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="e59a9-115">ParameterDef</span></span><br/>                                  |
| <span data-ttu-id="e59a9-116">範圍前置詞</span><span class="sxs-lookup"><span data-stu-id="e59a9-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="e59a9-117">頁面</span><span class="sxs-lookup"><span data-stu-id="e59a9-117">Page</span></span><br/>                                          |
| <span data-ttu-id="e59a9-118">備註</span><span class="sxs-lookup"><span data-stu-id="e59a9-118">Notes</span></span> <br/>          | <span data-ttu-id="e59a9-119">連結至 PageDestinationColorProfile 元素</span><span class="sxs-lookup"><span data-stu-id="e59a9-119">Linked to PageDestinationColorProfile element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="e59a9-120">結構內容</span><span class="sxs-lookup"><span data-stu-id="e59a9-120">Structure Content</span></span>

<span data-ttu-id="e59a9-121">此元素的 XML 結構為：</span><span class="sxs-lookup"><span data-stu-id="e59a9-121">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageDestinationColorProfileEmbedded">
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

## <a name="structure-properties"></a><span data-ttu-id="e59a9-122">結構屬性</span><span class="sxs-lookup"><span data-stu-id="e59a9-122">Structure Properties</span></span>

<span data-ttu-id="e59a9-123">下表概述 XML 結構中所定義之變數的特性。</span><span class="sxs-lookup"><span data-stu-id="e59a9-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="e59a9-124">屬性</span><span class="sxs-lookup"><span data-stu-id="e59a9-124">Property</span></span>                | <span data-ttu-id="e59a9-125">xsi:type</span><span class="sxs-lookup"><span data-stu-id="e59a9-125">xsi:type</span></span>           | <span data-ttu-id="e59a9-126">值</span><span class="sxs-lookup"><span data-stu-id="e59a9-126">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="e59a9-127">DataType</span><span class="sxs-lookup"><span data-stu-id="e59a9-127">DataType</span></span><br/>     | <span data-ttu-id="e59a9-128">字串</span><span class="sxs-lookup"><span data-stu-id="e59a9-128">string</span></span><br/>  | <span data-ttu-id="e59a9-129">xs:string</span><span class="sxs-lookup"><span data-stu-id="e59a9-129">xs:string</span></span><br/>       |
| <span data-ttu-id="e59a9-130">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="e59a9-130">DefaultValue</span></span><br/> | <span data-ttu-id="e59a9-131">字串</span><span class="sxs-lookup"><span data-stu-id="e59a9-131">string</span></span><br/>  | <span data-ttu-id="e59a9-132">未定義</span><span class="sxs-lookup"><span data-stu-id="e59a9-132">undefined</span></span><br/>       |
| <span data-ttu-id="e59a9-133">MaxLength</span><span class="sxs-lookup"><span data-stu-id="e59a9-133">MaxLength</span></span><br/>    | <span data-ttu-id="e59a9-134">整數</span><span class="sxs-lookup"><span data-stu-id="e59a9-134">integer</span></span><br/> | <span data-ttu-id="e59a9-135">未定義</span><span class="sxs-lookup"><span data-stu-id="e59a9-135">undefined</span></span><br/>       |
| <span data-ttu-id="e59a9-136">MinLength</span><span class="sxs-lookup"><span data-stu-id="e59a9-136">MinLength</span></span><br/>    | <span data-ttu-id="e59a9-137">整數</span><span class="sxs-lookup"><span data-stu-id="e59a9-137">integer</span></span><br/> | <span data-ttu-id="e59a9-138">1</span><span class="sxs-lookup"><span data-stu-id="e59a9-138">1</span></span><br/>               |
| <span data-ttu-id="e59a9-139">強制性</span><span class="sxs-lookup"><span data-stu-id="e59a9-139">Mandatory</span></span><br/>    | <span data-ttu-id="e59a9-140">string</span><span class="sxs-lookup"><span data-stu-id="e59a9-140">string</span></span><br/>  | <span data-ttu-id="e59a9-141">psk：條件式</span><span class="sxs-lookup"><span data-stu-id="e59a9-141">psk:Conditional</span></span><br/> |
| <span data-ttu-id="e59a9-142">Unittype.pixel 表示</span><span class="sxs-lookup"><span data-stu-id="e59a9-142">UnitType</span></span><br/>     | <span data-ttu-id="e59a9-143">string</span><span class="sxs-lookup"><span data-stu-id="e59a9-143">string</span></span><br/>  | <span data-ttu-id="e59a9-144">字元</span><span class="sxs-lookup"><span data-stu-id="e59a9-144">characters</span></span><br/>      |



 

## <a name="related-topics"></a><span data-ttu-id="e59a9-145">相關主題</span><span class="sxs-lookup"><span data-stu-id="e59a9-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e59a9-146">列印架構規格</span><span class="sxs-lookup"><span data-stu-id="e59a9-146">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




