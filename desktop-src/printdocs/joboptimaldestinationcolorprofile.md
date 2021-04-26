---
description: 本主題並非最新的。 如需最新資訊，請參閱列印架構規格。
ms.assetid: 70790dc2-180a-4e04-91a9-a10ee76c836b
title: JobOptimalDestinationColorProfile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45630b2ddbe94f19905f01c508fc4d852d29566b
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/26/2021
ms.locfileid: "107999247"
---
# <a name="joboptimaldestinationcolorprofile"></a><span data-ttu-id="2db93-104">JobOptimalDestinationColorProfile</span><span class="sxs-lookup"><span data-stu-id="2db93-104">JobOptimalDestinationColorProfile</span></span>

<span data-ttu-id="2db93-105">本主題並非最新的。</span><span class="sxs-lookup"><span data-stu-id="2db93-105">This topic is not current.</span></span> <span data-ttu-id="2db93-106">如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。</span><span class="sxs-lookup"><span data-stu-id="2db93-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="2db93-107">指定目前裝置設定的最佳色彩設定檔。</span><span class="sxs-lookup"><span data-stu-id="2db93-107">Specifies the optimal color profile given the current device configuration.</span></span>

-   [<span data-ttu-id="2db93-108">項目資訊</span><span class="sxs-lookup"><span data-stu-id="2db93-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="2db93-109">結構化內容</span><span class="sxs-lookup"><span data-stu-id="2db93-109">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="2db93-110">可延伸標記語言 (XML)  (XML) 內容</span><span class="sxs-lookup"><span data-stu-id="2db93-110">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="2db93-111">項目資訊</span><span class="sxs-lookup"><span data-stu-id="2db93-111">Element Information</span></span>



| <span data-ttu-id="2db93-112">Name</span><span class="sxs-lookup"><span data-stu-id="2db93-112">Name</span></span> | <span data-ttu-id="2db93-113">值</span><span class="sxs-lookup"><span data-stu-id="2db93-113">Value</span></span> |
|----------------------------|---------------------|
| <span data-ttu-id="2db93-114">項目類型</span><span class="sxs-lookup"><span data-stu-id="2db93-114">Element Type</span></span> <br/>   | <span data-ttu-id="2db93-115">屬性</span><span class="sxs-lookup"><span data-stu-id="2db93-115">Property</span></span><br/> |
| <span data-ttu-id="2db93-116">範圍前置詞</span><span class="sxs-lookup"><span data-stu-id="2db93-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="2db93-117">工作 (Job)</span><span class="sxs-lookup"><span data-stu-id="2db93-117">Job</span></span><br/>      |
| <span data-ttu-id="2db93-118">注意</span><span class="sxs-lookup"><span data-stu-id="2db93-118">Notes</span></span> <br/>          | <span data-ttu-id="2db93-119">None</span><span class="sxs-lookup"><span data-stu-id="2db93-119">None</span></span><br/>     |



 

## <a name="structural-content"></a><span data-ttu-id="2db93-120">結構化內容</span><span class="sxs-lookup"><span data-stu-id="2db93-120">Structural Content</span></span>

<span data-ttu-id="2db93-121">此元素的 XML 結構為：</span><span class="sxs-lookup"><span data-stu-id="2db93-121">The XML structure of this element is:</span></span>

``` syntax
<psf:Property name="psk:JobOptimalDestinationColorProfile">
  <psf:Property name="psk:Profile">
    <psf:Value xsi:type="xs:string">_ProfileValue_</psf:Value>
    <psf:Property name="psk:ProfileData">
      <psf:Value xsi:type="xs:string">_ProfileDataValue_</psf:Value>
    </psf:Property>
    <psf:Property name="psk:Path">
      <psf:Value xsi:type="xs:string">_PathValue_</psf:Value>
    </psf:Property>
  </psf:Property>
</psf:Property>
```

## <a name="structure-variables"></a><span data-ttu-id="2db93-122">結構變數</span><span class="sxs-lookup"><span data-stu-id="2db93-122">Structure Variables</span></span>

<span data-ttu-id="2db93-123">下表概述 XML 結構中所定義之變數的特性。</span><span class="sxs-lookup"><span data-stu-id="2db93-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="2db93-124">Name</span><span class="sxs-lookup"><span data-stu-id="2db93-124">Name</span></span>                            | <span data-ttu-id="2db93-125">資料類型</span><span class="sxs-lookup"><span data-stu-id="2db93-125">Data type</span></span>         | <span data-ttu-id="2db93-126">單位</span><span class="sxs-lookup"><span data-stu-id="2db93-126">Unit</span></span>           | <span data-ttu-id="2db93-127">支援的值</span><span class="sxs-lookup"><span data-stu-id="2db93-127">Supported values</span></span>          | <span data-ttu-id="2db93-128">總結</span><span class="sxs-lookup"><span data-stu-id="2db93-128">Summary</span></span>                                        |
|---------------------------------|-------------------|----------------|---------------------------|------------------------------------------------|
| <span data-ttu-id="2db93-129">\_ProfileValue\_</span><span class="sxs-lookup"><span data-stu-id="2db93-129">\_ProfileValue\_</span></span><br/>     | <span data-ttu-id="2db93-130">字串</span><span class="sxs-lookup"><span data-stu-id="2db93-130">string</span></span><br/> | <span data-ttu-id="2db93-131">n/a</span><span class="sxs-lookup"><span data-stu-id="2db93-131">n/a</span></span><br/> | <span data-ttu-id="2db93-132">RGB、ICC、CMYK</span><span class="sxs-lookup"><span data-stu-id="2db93-132">RGB, ICC, CMYK</span></span><br/> | <span data-ttu-id="2db93-133">指定色彩設定檔。</span><span class="sxs-lookup"><span data-stu-id="2db93-133">Specifies the color profile.</span></span><br/>        |
| <span data-ttu-id="2db93-134">\_PathValue\_</span><span class="sxs-lookup"><span data-stu-id="2db93-134">\_PathValue\_</span></span><br/>        | <span data-ttu-id="2db93-135">字串</span><span class="sxs-lookup"><span data-stu-id="2db93-135">string</span></span><br/> | <span data-ttu-id="2db93-136">n/a</span><span class="sxs-lookup"><span data-stu-id="2db93-136">n/a</span></span><br/> | <span data-ttu-id="2db93-137">n/a</span><span class="sxs-lookup"><span data-stu-id="2db93-137">n/a</span></span><br/>            | <span data-ttu-id="2db93-138">指定設定檔的檔案路徑。</span><span class="sxs-lookup"><span data-stu-id="2db93-138">Specifies file path to the profile.</span></span><br/> |
| <span data-ttu-id="2db93-139">\_ProfileDataValue\_</span><span class="sxs-lookup"><span data-stu-id="2db93-139">\_ProfileDataValue\_</span></span><br/> | <span data-ttu-id="2db93-140">字串</span><span class="sxs-lookup"><span data-stu-id="2db93-140">string</span></span><br/> | <span data-ttu-id="2db93-141">n/a</span><span class="sxs-lookup"><span data-stu-id="2db93-141">n/a</span></span><br/> | <span data-ttu-id="2db93-142">n/a</span><span class="sxs-lookup"><span data-stu-id="2db93-142">n/a</span></span><br/>            | <span data-ttu-id="2db93-143">包含設定檔資料內容。</span><span class="sxs-lookup"><span data-stu-id="2db93-143">Contains profile data content.</span></span><br/>      |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="2db93-144">可延伸標記語言 (XML)  (XML) 內容</span><span class="sxs-lookup"><span data-stu-id="2db93-144">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="2db93-145">公用列印架構關鍵字是在 https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords 命名空間中定義。</span><span class="sxs-lookup"><span data-stu-id="2db93-145">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="2db93-146">此關鍵字的 public 可延伸標記語言 (XML)  (XML) 內容定義如下：</span><span class="sxs-lookup"><span data-stu-id="2db93-146">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
 <psf:Property name="psk:JobOptimalDestinationColorProfile">
  <psf:Property name="psk:Profile">
    <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    <psf:Property name="psk:ProfileData">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:Property>
    <psf:Property name="psk:Path">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:Property>
  </psf:Property>
</psf:Property>
```

## <a name="related-topics"></a><span data-ttu-id="2db93-147">相關主題</span><span class="sxs-lookup"><span data-stu-id="2db93-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2db93-148">列印架構規格</span><span class="sxs-lookup"><span data-stu-id="2db93-148">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




