---
description: 閱讀 PageDestinationColorProfileURI 參數。 本主題並非最新的。 如需最新資訊，請參閱列印架構規格。
ms.assetid: b2a4a4d2-a8bc-48dc-ad56-20380f5f91c9
title: PageDestinationColorProfileURI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c3cf719a97f8f8086e88425c1667199815efbbb
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/19/2021
ms.locfileid: "112396673"
---
# <a name="pagedestinationcolorprofileuri"></a><span data-ttu-id="e3752-105">PageDestinationColorProfileURI</span><span class="sxs-lookup"><span data-stu-id="e3752-105">PageDestinationColorProfileURI</span></span>

<span data-ttu-id="e3752-106">本主題並非最新的。</span><span class="sxs-lookup"><span data-stu-id="e3752-106">This topic is not current.</span></span> <span data-ttu-id="e3752-107">如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。</span><span class="sxs-lookup"><span data-stu-id="e3752-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="e3752-108">指定包含在 XPS 檔中之 ICC 設定檔的相對 URI 參考。</span><span class="sxs-lookup"><span data-stu-id="e3752-108">Specifies a relative URI reference to an ICC profile contained in an XPS Document.</span></span> <span data-ttu-id="e3752-109">此選項的處理取決於 PageDeviceColorSpaceUsage 功能的設定。</span><span class="sxs-lookup"><span data-stu-id="e3752-109">The processing of this option depends of the setting of the PageDeviceColorSpaceUsage feature.</span></span> <span data-ttu-id="e3752-110">使用該設定檔的所有元素都會假設已經在適當的裝置色彩空間中，而且不會在驅動程式或裝置中進行色彩管理。</span><span class="sxs-lookup"><span data-stu-id="e3752-110">All elements using that profile are assumed to be already in the appropriate device color space, and will not be color managed in the driver or device.</span></span>

-   [<span data-ttu-id="e3752-111">項目資訊</span><span class="sxs-lookup"><span data-stu-id="e3752-111">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="e3752-112">結構內容</span><span class="sxs-lookup"><span data-stu-id="e3752-112">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="e3752-113">項目資訊</span><span class="sxs-lookup"><span data-stu-id="e3752-113">Element Information</span></span>



| <span data-ttu-id="e3752-114">Name</span><span class="sxs-lookup"><span data-stu-id="e3752-114">Name</span></span> | <span data-ttu-id="e3752-115">值</span><span class="sxs-lookup"><span data-stu-id="e3752-115">Value</span></span> |
|----------------------------|----------------------------------------------------------|
| <span data-ttu-id="e3752-116">項目類型</span><span class="sxs-lookup"><span data-stu-id="e3752-116">Element Type</span></span> <br/>   | <span data-ttu-id="e3752-117">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="e3752-117">ParameterDef</span></span><br/>                                  |
| <span data-ttu-id="e3752-118">範圍前置詞</span><span class="sxs-lookup"><span data-stu-id="e3752-118">Scoping Prefix</span></span> <br/> | <span data-ttu-id="e3752-119">頁面</span><span class="sxs-lookup"><span data-stu-id="e3752-119">Page</span></span><br/>                                          |
| <span data-ttu-id="e3752-120">備註</span><span class="sxs-lookup"><span data-stu-id="e3752-120">Notes</span></span> <br/>          | <span data-ttu-id="e3752-121">連結至 PageDestinationColorProfile 元素</span><span class="sxs-lookup"><span data-stu-id="e3752-121">Linked to PageDestinationColorProfile element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="e3752-122">結構內容</span><span class="sxs-lookup"><span data-stu-id="e3752-122">Structure Content</span></span>

<span data-ttu-id="e3752-123">此元素的 XML 結構為：</span><span class="sxs-lookup"><span data-stu-id="e3752-123">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="e3752-124">結構屬性</span><span class="sxs-lookup"><span data-stu-id="e3752-124">Structure Properties</span></span>

<span data-ttu-id="e3752-125">下表概述 XML 結構中所定義之變數的特性。</span><span class="sxs-lookup"><span data-stu-id="e3752-125">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="e3752-126">屬性</span><span class="sxs-lookup"><span data-stu-id="e3752-126">Property</span></span>                | <span data-ttu-id="e3752-127">xsi:type</span><span class="sxs-lookup"><span data-stu-id="e3752-127">xsi:type</span></span>           | <span data-ttu-id="e3752-128">值</span><span class="sxs-lookup"><span data-stu-id="e3752-128">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="e3752-129">DataType</span><span class="sxs-lookup"><span data-stu-id="e3752-129">DataType</span></span><br/>     | <span data-ttu-id="e3752-130">字串</span><span class="sxs-lookup"><span data-stu-id="e3752-130">string</span></span><br/>  | <span data-ttu-id="e3752-131">xs:string</span><span class="sxs-lookup"><span data-stu-id="e3752-131">xs:string</span></span><br/>       |
| <span data-ttu-id="e3752-132">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="e3752-132">DefaultValue</span></span><br/> | <span data-ttu-id="e3752-133">字串</span><span class="sxs-lookup"><span data-stu-id="e3752-133">string</span></span><br/>  | <span data-ttu-id="e3752-134">未定義</span><span class="sxs-lookup"><span data-stu-id="e3752-134">undefined</span></span><br/>       |
| <span data-ttu-id="e3752-135">MaxLength</span><span class="sxs-lookup"><span data-stu-id="e3752-135">MaxLength</span></span><br/>    | <span data-ttu-id="e3752-136">整數</span><span class="sxs-lookup"><span data-stu-id="e3752-136">integer</span></span><br/> | <span data-ttu-id="e3752-137">未定義</span><span class="sxs-lookup"><span data-stu-id="e3752-137">undefined</span></span><br/>       |
| <span data-ttu-id="e3752-138">MinLength</span><span class="sxs-lookup"><span data-stu-id="e3752-138">MinLength</span></span><br/>    | <span data-ttu-id="e3752-139">整數</span><span class="sxs-lookup"><span data-stu-id="e3752-139">integer</span></span><br/> | <span data-ttu-id="e3752-140">1</span><span class="sxs-lookup"><span data-stu-id="e3752-140">1</span></span><br/>               |
| <span data-ttu-id="e3752-141">強制性</span><span class="sxs-lookup"><span data-stu-id="e3752-141">Mandatory</span></span><br/>    | <span data-ttu-id="e3752-142">string</span><span class="sxs-lookup"><span data-stu-id="e3752-142">string</span></span><br/>  | <span data-ttu-id="e3752-143">psk：條件式</span><span class="sxs-lookup"><span data-stu-id="e3752-143">psk:Conditional</span></span><br/> |
| <span data-ttu-id="e3752-144">Unittype.pixel 表示</span><span class="sxs-lookup"><span data-stu-id="e3752-144">UnitType</span></span><br/>     | <span data-ttu-id="e3752-145">string</span><span class="sxs-lookup"><span data-stu-id="e3752-145">string</span></span><br/>  | <span data-ttu-id="e3752-146">字元</span><span class="sxs-lookup"><span data-stu-id="e3752-146">characters</span></span><br/>      |



 

## <a name="related-topics"></a><span data-ttu-id="e3752-147">相關主題</span><span class="sxs-lookup"><span data-stu-id="e3752-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e3752-148">列印架構規格</span><span class="sxs-lookup"><span data-stu-id="e3752-148">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




