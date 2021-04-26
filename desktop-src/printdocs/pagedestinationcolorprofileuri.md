---
description: 本主題並非最新的。 如需最新資訊，請參閱列印架構規格。
ms.assetid: b2a4a4d2-a8bc-48dc-ad56-20380f5f91c9
title: PageDestinationColorProfileURI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b321cba1608b1098dcc91f3800ef11f4968fb3f2
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/26/2021
ms.locfileid: "107996095"
---
# <a name="pagedestinationcolorprofileuri"></a><span data-ttu-id="aa93e-104">PageDestinationColorProfileURI</span><span class="sxs-lookup"><span data-stu-id="aa93e-104">PageDestinationColorProfileURI</span></span>

<span data-ttu-id="aa93e-105">本主題並非最新的。</span><span class="sxs-lookup"><span data-stu-id="aa93e-105">This topic is not current.</span></span> <span data-ttu-id="aa93e-106">如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。</span><span class="sxs-lookup"><span data-stu-id="aa93e-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="aa93e-107">指定包含在 XPS 檔中之 ICC 設定檔的相對 URI 參考。</span><span class="sxs-lookup"><span data-stu-id="aa93e-107">Specifies a relative URI reference to an ICC profile contained in an XPS Document.</span></span> <span data-ttu-id="aa93e-108">此選項的處理取決於 PageDeviceColorSpaceUsage 功能的設定。</span><span class="sxs-lookup"><span data-stu-id="aa93e-108">The processing of this option depends of the setting of the PageDeviceColorSpaceUsage feature.</span></span> <span data-ttu-id="aa93e-109">使用該設定檔的所有元素都會假設已經在適當的裝置色彩空間中，而且不會在驅動程式或裝置中進行色彩管理。</span><span class="sxs-lookup"><span data-stu-id="aa93e-109">All elements using that profile are assumed to be already in the appropriate device color space, and will not be color managed in the driver or device.</span></span>

-   [<span data-ttu-id="aa93e-110">項目資訊</span><span class="sxs-lookup"><span data-stu-id="aa93e-110">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="aa93e-111">結構內容</span><span class="sxs-lookup"><span data-stu-id="aa93e-111">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="aa93e-112">項目資訊</span><span class="sxs-lookup"><span data-stu-id="aa93e-112">Element Information</span></span>



| <span data-ttu-id="aa93e-113">Name</span><span class="sxs-lookup"><span data-stu-id="aa93e-113">Name</span></span> | <span data-ttu-id="aa93e-114">值</span><span class="sxs-lookup"><span data-stu-id="aa93e-114">Value</span></span> |
|----------------------------|----------------------------------------------------------|
| <span data-ttu-id="aa93e-115">項目類型</span><span class="sxs-lookup"><span data-stu-id="aa93e-115">Element Type</span></span> <br/>   | <span data-ttu-id="aa93e-116">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="aa93e-116">ParameterDef</span></span><br/>                                  |
| <span data-ttu-id="aa93e-117">範圍前置詞</span><span class="sxs-lookup"><span data-stu-id="aa93e-117">Scoping Prefix</span></span> <br/> | <span data-ttu-id="aa93e-118">頁面</span><span class="sxs-lookup"><span data-stu-id="aa93e-118">Page</span></span><br/>                                          |
| <span data-ttu-id="aa93e-119">備註</span><span class="sxs-lookup"><span data-stu-id="aa93e-119">Notes</span></span> <br/>          | <span data-ttu-id="aa93e-120">連結至 PageDestinationColorProfile 元素</span><span class="sxs-lookup"><span data-stu-id="aa93e-120">Linked to PageDestinationColorProfile element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="aa93e-121">結構內容</span><span class="sxs-lookup"><span data-stu-id="aa93e-121">Structure Content</span></span>

<span data-ttu-id="aa93e-122">此元素的 XML 結構為：</span><span class="sxs-lookup"><span data-stu-id="aa93e-122">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="aa93e-123">結構屬性</span><span class="sxs-lookup"><span data-stu-id="aa93e-123">Structure Properties</span></span>

<span data-ttu-id="aa93e-124">下表概述 XML 結構中所定義之變數的特性。</span><span class="sxs-lookup"><span data-stu-id="aa93e-124">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="aa93e-125">屬性</span><span class="sxs-lookup"><span data-stu-id="aa93e-125">Property</span></span>                | <span data-ttu-id="aa93e-126">xsi:type</span><span class="sxs-lookup"><span data-stu-id="aa93e-126">xsi:type</span></span>           | <span data-ttu-id="aa93e-127">值</span><span class="sxs-lookup"><span data-stu-id="aa93e-127">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="aa93e-128">DataType</span><span class="sxs-lookup"><span data-stu-id="aa93e-128">DataType</span></span><br/>     | <span data-ttu-id="aa93e-129">字串</span><span class="sxs-lookup"><span data-stu-id="aa93e-129">string</span></span><br/>  | <span data-ttu-id="aa93e-130">xs:string</span><span class="sxs-lookup"><span data-stu-id="aa93e-130">xs:string</span></span><br/>       |
| <span data-ttu-id="aa93e-131">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="aa93e-131">DefaultValue</span></span><br/> | <span data-ttu-id="aa93e-132">字串</span><span class="sxs-lookup"><span data-stu-id="aa93e-132">string</span></span><br/>  | <span data-ttu-id="aa93e-133">未定義</span><span class="sxs-lookup"><span data-stu-id="aa93e-133">undefined</span></span><br/>       |
| <span data-ttu-id="aa93e-134">MaxLength</span><span class="sxs-lookup"><span data-stu-id="aa93e-134">MaxLength</span></span><br/>    | <span data-ttu-id="aa93e-135">整數</span><span class="sxs-lookup"><span data-stu-id="aa93e-135">integer</span></span><br/> | <span data-ttu-id="aa93e-136">未定義</span><span class="sxs-lookup"><span data-stu-id="aa93e-136">undefined</span></span><br/>       |
| <span data-ttu-id="aa93e-137">MinLength</span><span class="sxs-lookup"><span data-stu-id="aa93e-137">MinLength</span></span><br/>    | <span data-ttu-id="aa93e-138">整數</span><span class="sxs-lookup"><span data-stu-id="aa93e-138">integer</span></span><br/> | <span data-ttu-id="aa93e-139">1</span><span class="sxs-lookup"><span data-stu-id="aa93e-139">1</span></span><br/>               |
| <span data-ttu-id="aa93e-140">強制性</span><span class="sxs-lookup"><span data-stu-id="aa93e-140">Mandatory</span></span><br/>    | <span data-ttu-id="aa93e-141">字串</span><span class="sxs-lookup"><span data-stu-id="aa93e-141">string</span></span><br/>  | <span data-ttu-id="aa93e-142">psk：條件式</span><span class="sxs-lookup"><span data-stu-id="aa93e-142">psk:Conditional</span></span><br/> |
| <span data-ttu-id="aa93e-143">Unittype.pixel 表示</span><span class="sxs-lookup"><span data-stu-id="aa93e-143">UnitType</span></span><br/>     | <span data-ttu-id="aa93e-144">字串</span><span class="sxs-lookup"><span data-stu-id="aa93e-144">string</span></span><br/>  | <span data-ttu-id="aa93e-145">字元</span><span class="sxs-lookup"><span data-stu-id="aa93e-145">characters</span></span><br/>      |



 

## <a name="related-topics"></a><span data-ttu-id="aa93e-146">相關主題</span><span class="sxs-lookup"><span data-stu-id="aa93e-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="aa93e-147">列印架構規格</span><span class="sxs-lookup"><span data-stu-id="aa93e-147">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




