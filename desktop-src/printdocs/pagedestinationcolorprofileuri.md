---
description: 本主題並非最新的。 如需最新資訊，請參閱列印架構規格。
ms.assetid: b2a4a4d2-a8bc-48dc-ad56-20380f5f91c9
title: PageDestinationColorProfileURI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8fff2ca269eaed9331f6c2077e6b396cca5a01c4
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/05/2021
ms.locfileid: "106997323"
---
# <a name="pagedestinationcolorprofileuri"></a><span data-ttu-id="d0d2b-104">PageDestinationColorProfileURI</span><span class="sxs-lookup"><span data-stu-id="d0d2b-104">PageDestinationColorProfileURI</span></span>

<span data-ttu-id="d0d2b-105">本主題並非最新的。</span><span class="sxs-lookup"><span data-stu-id="d0d2b-105">This topic is not current.</span></span> <span data-ttu-id="d0d2b-106">如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。</span><span class="sxs-lookup"><span data-stu-id="d0d2b-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="d0d2b-107">指定包含在 XPS 檔中之 ICC 設定檔的相對 URI 參考。</span><span class="sxs-lookup"><span data-stu-id="d0d2b-107">Specifies a relative URI reference to an ICC profile contained in an XPS Document.</span></span> <span data-ttu-id="d0d2b-108">此選項的處理取決於 PageDeviceColorSpaceUsage 功能的設定。</span><span class="sxs-lookup"><span data-stu-id="d0d2b-108">The processing of this option depends of the setting of the PageDeviceColorSpaceUsage feature.</span></span> <span data-ttu-id="d0d2b-109">使用該設定檔的所有元素都會假設已經在適當的裝置色彩空間中，而且不會在驅動程式或裝置中進行色彩管理。</span><span class="sxs-lookup"><span data-stu-id="d0d2b-109">All elements using that profile are assumed to be already in the appropriate device color space, and will not be color managed in the driver or device.</span></span>

-   [<span data-ttu-id="d0d2b-110">項目資訊</span><span class="sxs-lookup"><span data-stu-id="d0d2b-110">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="d0d2b-111">結構內容</span><span class="sxs-lookup"><span data-stu-id="d0d2b-111">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="d0d2b-112">項目資訊</span><span class="sxs-lookup"><span data-stu-id="d0d2b-112">Element Information</span></span>



| <span data-ttu-id="d0d2b-113">Name</span><span class="sxs-lookup"><span data-stu-id="d0d2b-113">Name</span></span>                       |                                                          |
|----------------------------|----------------------------------------------------------|
| <span data-ttu-id="d0d2b-114">項目類型</span><span class="sxs-lookup"><span data-stu-id="d0d2b-114">Element Type</span></span> <br/>   | <span data-ttu-id="d0d2b-115">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="d0d2b-115">ParameterDef</span></span><br/>                                  |
| <span data-ttu-id="d0d2b-116">範圍前置詞</span><span class="sxs-lookup"><span data-stu-id="d0d2b-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="d0d2b-117">頁面</span><span class="sxs-lookup"><span data-stu-id="d0d2b-117">Page</span></span><br/>                                          |
| <span data-ttu-id="d0d2b-118">備註</span><span class="sxs-lookup"><span data-stu-id="d0d2b-118">Notes</span></span> <br/>          | <span data-ttu-id="d0d2b-119">連結至 PageDestinationColorProfile 元素</span><span class="sxs-lookup"><span data-stu-id="d0d2b-119">Linked to PageDestinationColorProfile element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="d0d2b-120">結構內容</span><span class="sxs-lookup"><span data-stu-id="d0d2b-120">Structure Content</span></span>

<span data-ttu-id="d0d2b-121">此元素的 XML 結構為：</span><span class="sxs-lookup"><span data-stu-id="d0d2b-121">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageDestinationColorProfileURI">
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

## <a name="structure-properties"></a><span data-ttu-id="d0d2b-122">結構屬性</span><span class="sxs-lookup"><span data-stu-id="d0d2b-122">Structure Properties</span></span>

<span data-ttu-id="d0d2b-123">下表概述 XML 結構中所定義之變數的特性。</span><span class="sxs-lookup"><span data-stu-id="d0d2b-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="d0d2b-124">屬性</span><span class="sxs-lookup"><span data-stu-id="d0d2b-124">Property</span></span>                | <span data-ttu-id="d0d2b-125">xsi:type</span><span class="sxs-lookup"><span data-stu-id="d0d2b-125">xsi:type</span></span>           | <span data-ttu-id="d0d2b-126">值</span><span class="sxs-lookup"><span data-stu-id="d0d2b-126">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="d0d2b-127">DataType</span><span class="sxs-lookup"><span data-stu-id="d0d2b-127">DataType</span></span><br/>     | <span data-ttu-id="d0d2b-128">字串</span><span class="sxs-lookup"><span data-stu-id="d0d2b-128">string</span></span><br/>  | <span data-ttu-id="d0d2b-129">xs:string</span><span class="sxs-lookup"><span data-stu-id="d0d2b-129">xs:string</span></span><br/>       |
| <span data-ttu-id="d0d2b-130">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="d0d2b-130">DefaultValue</span></span><br/> | <span data-ttu-id="d0d2b-131">字串</span><span class="sxs-lookup"><span data-stu-id="d0d2b-131">string</span></span><br/>  | <span data-ttu-id="d0d2b-132">未定義</span><span class="sxs-lookup"><span data-stu-id="d0d2b-132">undefined</span></span><br/>       |
| <span data-ttu-id="d0d2b-133">MaxLength</span><span class="sxs-lookup"><span data-stu-id="d0d2b-133">MaxLength</span></span><br/>    | <span data-ttu-id="d0d2b-134">整數</span><span class="sxs-lookup"><span data-stu-id="d0d2b-134">integer</span></span><br/> | <span data-ttu-id="d0d2b-135">未定義</span><span class="sxs-lookup"><span data-stu-id="d0d2b-135">undefined</span></span><br/>       |
| <span data-ttu-id="d0d2b-136">MinLength</span><span class="sxs-lookup"><span data-stu-id="d0d2b-136">MinLength</span></span><br/>    | <span data-ttu-id="d0d2b-137">整數</span><span class="sxs-lookup"><span data-stu-id="d0d2b-137">integer</span></span><br/> | <span data-ttu-id="d0d2b-138">1</span><span class="sxs-lookup"><span data-stu-id="d0d2b-138">1</span></span><br/>               |
| <span data-ttu-id="d0d2b-139">強制性</span><span class="sxs-lookup"><span data-stu-id="d0d2b-139">Mandatory</span></span><br/>    | <span data-ttu-id="d0d2b-140">字串</span><span class="sxs-lookup"><span data-stu-id="d0d2b-140">string</span></span><br/>  | <span data-ttu-id="d0d2b-141">psk：條件式</span><span class="sxs-lookup"><span data-stu-id="d0d2b-141">psk:Conditional</span></span><br/> |
| <span data-ttu-id="d0d2b-142">Unittype.pixel 表示</span><span class="sxs-lookup"><span data-stu-id="d0d2b-142">UnitType</span></span><br/>     | <span data-ttu-id="d0d2b-143">字串</span><span class="sxs-lookup"><span data-stu-id="d0d2b-143">string</span></span><br/>  | <span data-ttu-id="d0d2b-144">字元</span><span class="sxs-lookup"><span data-stu-id="d0d2b-144">characters</span></span><br/>      |



 

## <a name="related-topics"></a><span data-ttu-id="d0d2b-145">相關主題</span><span class="sxs-lookup"><span data-stu-id="d0d2b-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d0d2b-146">列印架構規格</span><span class="sxs-lookup"><span data-stu-id="d0d2b-146">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




