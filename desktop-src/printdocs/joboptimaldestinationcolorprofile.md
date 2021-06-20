---
description: 瞭解指定目前裝置設定的最佳色彩設定檔的 JobOptimalDestinationColorProfile 元素。
ms.assetid: 70790dc2-180a-4e04-91a9-a10ee76c836b
title: JobOptimalDestinationColorProfile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e7ad2ea269594809b047922ea4f6c99b924e5ae
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/19/2021
ms.locfileid: "112408841"
---
# <a name="joboptimaldestinationcolorprofile"></a><span data-ttu-id="76d74-103">JobOptimalDestinationColorProfile</span><span class="sxs-lookup"><span data-stu-id="76d74-103">JobOptimalDestinationColorProfile</span></span>

<span data-ttu-id="76d74-104">本主題並非最新的。</span><span class="sxs-lookup"><span data-stu-id="76d74-104">This topic is not current.</span></span> <span data-ttu-id="76d74-105">如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。</span><span class="sxs-lookup"><span data-stu-id="76d74-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="76d74-106">指定目前裝置設定的最佳色彩設定檔。</span><span class="sxs-lookup"><span data-stu-id="76d74-106">Specifies the optimal color profile given the current device configuration.</span></span>

-   [<span data-ttu-id="76d74-107">項目資訊</span><span class="sxs-lookup"><span data-stu-id="76d74-107">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="76d74-108">結構化內容</span><span class="sxs-lookup"><span data-stu-id="76d74-108">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="76d74-109">可延伸標記語言 (XML)  (XML) 內容</span><span class="sxs-lookup"><span data-stu-id="76d74-109">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="76d74-110">項目資訊</span><span class="sxs-lookup"><span data-stu-id="76d74-110">Element Information</span></span>



| <span data-ttu-id="76d74-111">Name</span><span class="sxs-lookup"><span data-stu-id="76d74-111">Name</span></span> | <span data-ttu-id="76d74-112">值</span><span class="sxs-lookup"><span data-stu-id="76d74-112">Value</span></span> |
|----------------------------|---------------------|
| <span data-ttu-id="76d74-113">項目類型</span><span class="sxs-lookup"><span data-stu-id="76d74-113">Element Type</span></span> <br/>   | <span data-ttu-id="76d74-114">屬性</span><span class="sxs-lookup"><span data-stu-id="76d74-114">Property</span></span><br/> |
| <span data-ttu-id="76d74-115">範圍前置詞</span><span class="sxs-lookup"><span data-stu-id="76d74-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="76d74-116">工作 (Job)</span><span class="sxs-lookup"><span data-stu-id="76d74-116">Job</span></span><br/>      |
| <span data-ttu-id="76d74-117">注意</span><span class="sxs-lookup"><span data-stu-id="76d74-117">Notes</span></span> <br/>          | <span data-ttu-id="76d74-118">None</span><span class="sxs-lookup"><span data-stu-id="76d74-118">None</span></span><br/>     |



 

## <a name="structural-content"></a><span data-ttu-id="76d74-119">結構化內容</span><span class="sxs-lookup"><span data-stu-id="76d74-119">Structural Content</span></span>

<span data-ttu-id="76d74-120">此元素的 XML 結構為：</span><span class="sxs-lookup"><span data-stu-id="76d74-120">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="76d74-121">結構變數</span><span class="sxs-lookup"><span data-stu-id="76d74-121">Structure Variables</span></span>

<span data-ttu-id="76d74-122">下表概述 XML 結構中所定義之變數的特性。</span><span class="sxs-lookup"><span data-stu-id="76d74-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="76d74-123">Name</span><span class="sxs-lookup"><span data-stu-id="76d74-123">Name</span></span>                            | <span data-ttu-id="76d74-124">資料類型</span><span class="sxs-lookup"><span data-stu-id="76d74-124">Data type</span></span>         | <span data-ttu-id="76d74-125">單位</span><span class="sxs-lookup"><span data-stu-id="76d74-125">Unit</span></span>           | <span data-ttu-id="76d74-126">支援的值</span><span class="sxs-lookup"><span data-stu-id="76d74-126">Supported values</span></span>          | <span data-ttu-id="76d74-127">總結</span><span class="sxs-lookup"><span data-stu-id="76d74-127">Summary</span></span>                                        |
|---------------------------------|-------------------|----------------|---------------------------|------------------------------------------------|
| <span data-ttu-id="76d74-128">\_ProfileValue\_</span><span class="sxs-lookup"><span data-stu-id="76d74-128">\_ProfileValue\_</span></span><br/>     | <span data-ttu-id="76d74-129">string</span><span class="sxs-lookup"><span data-stu-id="76d74-129">string</span></span><br/> | <span data-ttu-id="76d74-130">n/a</span><span class="sxs-lookup"><span data-stu-id="76d74-130">n/a</span></span><br/> | <span data-ttu-id="76d74-131">RGB、ICC、CMYK</span><span class="sxs-lookup"><span data-stu-id="76d74-131">RGB, ICC, CMYK</span></span><br/> | <span data-ttu-id="76d74-132">指定色彩設定檔。</span><span class="sxs-lookup"><span data-stu-id="76d74-132">Specifies the color profile.</span></span><br/>        |
| <span data-ttu-id="76d74-133">\_PathValue\_</span><span class="sxs-lookup"><span data-stu-id="76d74-133">\_PathValue\_</span></span><br/>        | <span data-ttu-id="76d74-134">string</span><span class="sxs-lookup"><span data-stu-id="76d74-134">string</span></span><br/> | <span data-ttu-id="76d74-135">n/a</span><span class="sxs-lookup"><span data-stu-id="76d74-135">n/a</span></span><br/> | <span data-ttu-id="76d74-136">n/a</span><span class="sxs-lookup"><span data-stu-id="76d74-136">n/a</span></span><br/>            | <span data-ttu-id="76d74-137">指定設定檔的檔案路徑。</span><span class="sxs-lookup"><span data-stu-id="76d74-137">Specifies file path to the profile.</span></span><br/> |
| <span data-ttu-id="76d74-138">\_ProfileDataValue\_</span><span class="sxs-lookup"><span data-stu-id="76d74-138">\_ProfileDataValue\_</span></span><br/> | <span data-ttu-id="76d74-139">string</span><span class="sxs-lookup"><span data-stu-id="76d74-139">string</span></span><br/> | <span data-ttu-id="76d74-140">n/a</span><span class="sxs-lookup"><span data-stu-id="76d74-140">n/a</span></span><br/> | <span data-ttu-id="76d74-141">n/a</span><span class="sxs-lookup"><span data-stu-id="76d74-141">n/a</span></span><br/>            | <span data-ttu-id="76d74-142">包含設定檔資料內容。</span><span class="sxs-lookup"><span data-stu-id="76d74-142">Contains profile data content.</span></span><br/>      |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="76d74-143">可延伸標記語言 (XML)  (XML) 內容</span><span class="sxs-lookup"><span data-stu-id="76d74-143">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="76d74-144">公用列印架構關鍵字是在 https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords 命名空間中定義。</span><span class="sxs-lookup"><span data-stu-id="76d74-144">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="76d74-145">此關鍵字的 public 可延伸標記語言 (XML)  (XML) 內容定義如下：</span><span class="sxs-lookup"><span data-stu-id="76d74-145">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="76d74-146">相關主題</span><span class="sxs-lookup"><span data-stu-id="76d74-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="76d74-147">列印架構規格</span><span class="sxs-lookup"><span data-stu-id="76d74-147">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




