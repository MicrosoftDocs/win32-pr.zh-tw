---
description: 本主題並非最新的。 如需最新資訊，請參閱列印架構規格。
ms.assetid: b360f870-bfaa-4d4d-adce-17fcfc48b6a6
title: PageDestinationColorProfileEmbedded
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47eaa810cd23462433c52292506999f90797d659
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/05/2021
ms.locfileid: "106981763"
---
# <a name="pagedestinationcolorprofileembedded"></a><span data-ttu-id="3b6b4-104">PageDestinationColorProfileEmbedded</span><span class="sxs-lookup"><span data-stu-id="3b6b4-104">PageDestinationColorProfileEmbedded</span></span>

<span data-ttu-id="3b6b4-105">本主題並非最新的。</span><span class="sxs-lookup"><span data-stu-id="3b6b4-105">This topic is not current.</span></span> <span data-ttu-id="3b6b4-106">如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。</span><span class="sxs-lookup"><span data-stu-id="3b6b4-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="3b6b4-107">指定內嵌的目的地色彩設定檔。</span><span class="sxs-lookup"><span data-stu-id="3b6b4-107">Specifies the embedded destination color profile.</span></span>

-   [<span data-ttu-id="3b6b4-108">項目資訊</span><span class="sxs-lookup"><span data-stu-id="3b6b4-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="3b6b4-109">結構內容</span><span class="sxs-lookup"><span data-stu-id="3b6b4-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="3b6b4-110">項目資訊</span><span class="sxs-lookup"><span data-stu-id="3b6b4-110">Element Information</span></span>



| <span data-ttu-id="3b6b4-111">Name</span><span class="sxs-lookup"><span data-stu-id="3b6b4-111">Name</span></span>                       |                                                          |
|----------------------------|----------------------------------------------------------|
| <span data-ttu-id="3b6b4-112">項目類型</span><span class="sxs-lookup"><span data-stu-id="3b6b4-112">Element Type</span></span> <br/>   | <span data-ttu-id="3b6b4-113">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="3b6b4-113">ParameterDef</span></span><br/>                                  |
| <span data-ttu-id="3b6b4-114">範圍前置詞</span><span class="sxs-lookup"><span data-stu-id="3b6b4-114">Scoping Prefix</span></span> <br/> | <span data-ttu-id="3b6b4-115">頁面</span><span class="sxs-lookup"><span data-stu-id="3b6b4-115">Page</span></span><br/>                                          |
| <span data-ttu-id="3b6b4-116">備註</span><span class="sxs-lookup"><span data-stu-id="3b6b4-116">Notes</span></span> <br/>          | <span data-ttu-id="3b6b4-117">連結至 PageDestinationColorProfile 元素</span><span class="sxs-lookup"><span data-stu-id="3b6b4-117">Linked to PageDestinationColorProfile element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="3b6b4-118">結構內容</span><span class="sxs-lookup"><span data-stu-id="3b6b4-118">Structure Content</span></span>

<span data-ttu-id="3b6b4-119">此元素的 XML 結構為：</span><span class="sxs-lookup"><span data-stu-id="3b6b4-119">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="3b6b4-120">結構屬性</span><span class="sxs-lookup"><span data-stu-id="3b6b4-120">Structure Properties</span></span>

<span data-ttu-id="3b6b4-121">下表概述 XML 結構中所定義之變數的特性。</span><span class="sxs-lookup"><span data-stu-id="3b6b4-121">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="3b6b4-122">屬性</span><span class="sxs-lookup"><span data-stu-id="3b6b4-122">Property</span></span>                | <span data-ttu-id="3b6b4-123">xsi:type</span><span class="sxs-lookup"><span data-stu-id="3b6b4-123">xsi:type</span></span>           | <span data-ttu-id="3b6b4-124">值</span><span class="sxs-lookup"><span data-stu-id="3b6b4-124">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="3b6b4-125">DataType</span><span class="sxs-lookup"><span data-stu-id="3b6b4-125">DataType</span></span><br/>     | <span data-ttu-id="3b6b4-126">字串</span><span class="sxs-lookup"><span data-stu-id="3b6b4-126">string</span></span><br/>  | <span data-ttu-id="3b6b4-127">xs:string</span><span class="sxs-lookup"><span data-stu-id="3b6b4-127">xs:string</span></span><br/>       |
| <span data-ttu-id="3b6b4-128">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="3b6b4-128">DefaultValue</span></span><br/> | <span data-ttu-id="3b6b4-129">字串</span><span class="sxs-lookup"><span data-stu-id="3b6b4-129">string</span></span><br/>  | <span data-ttu-id="3b6b4-130">未定義</span><span class="sxs-lookup"><span data-stu-id="3b6b4-130">undefined</span></span><br/>       |
| <span data-ttu-id="3b6b4-131">MaxLength</span><span class="sxs-lookup"><span data-stu-id="3b6b4-131">MaxLength</span></span><br/>    | <span data-ttu-id="3b6b4-132">整數</span><span class="sxs-lookup"><span data-stu-id="3b6b4-132">integer</span></span><br/> | <span data-ttu-id="3b6b4-133">未定義</span><span class="sxs-lookup"><span data-stu-id="3b6b4-133">undefined</span></span><br/>       |
| <span data-ttu-id="3b6b4-134">MinLength</span><span class="sxs-lookup"><span data-stu-id="3b6b4-134">MinLength</span></span><br/>    | <span data-ttu-id="3b6b4-135">整數</span><span class="sxs-lookup"><span data-stu-id="3b6b4-135">integer</span></span><br/> | <span data-ttu-id="3b6b4-136">1</span><span class="sxs-lookup"><span data-stu-id="3b6b4-136">1</span></span><br/>               |
| <span data-ttu-id="3b6b4-137">強制性</span><span class="sxs-lookup"><span data-stu-id="3b6b4-137">Mandatory</span></span><br/>    | <span data-ttu-id="3b6b4-138">字串</span><span class="sxs-lookup"><span data-stu-id="3b6b4-138">string</span></span><br/>  | <span data-ttu-id="3b6b4-139">psk：條件式</span><span class="sxs-lookup"><span data-stu-id="3b6b4-139">psk:Conditional</span></span><br/> |
| <span data-ttu-id="3b6b4-140">Unittype.pixel 表示</span><span class="sxs-lookup"><span data-stu-id="3b6b4-140">UnitType</span></span><br/>     | <span data-ttu-id="3b6b4-141">字串</span><span class="sxs-lookup"><span data-stu-id="3b6b4-141">string</span></span><br/>  | <span data-ttu-id="3b6b4-142">字元</span><span class="sxs-lookup"><span data-stu-id="3b6b4-142">characters</span></span><br/>      |



 

## <a name="related-topics"></a><span data-ttu-id="3b6b4-143">相關主題</span><span class="sxs-lookup"><span data-stu-id="3b6b4-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3b6b4-144">列印架構規格</span><span class="sxs-lookup"><span data-stu-id="3b6b4-144">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




