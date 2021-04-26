---
description: 本主題並非最新的。 如需最新資訊，請參閱列印架構規格。
ms.assetid: 4edd1fdf-9601-440d-b967-82ffa6dceeb1
title: PageBlackGenerationProcessing
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4aba727cfa1c11850b62a883b95ab78a6dfae50
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/26/2021
ms.locfileid: "107996255"
---
# <a name="pageblackgenerationprocessing"></a><span data-ttu-id="3e388-104">PageBlackGenerationProcessing</span><span class="sxs-lookup"><span data-stu-id="3e388-104">PageBlackGenerationProcessing</span></span>

<span data-ttu-id="3e388-105">本主題並非最新的。</span><span class="sxs-lookup"><span data-stu-id="3e388-105">This topic is not current.</span></span> <span data-ttu-id="3e388-106">如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。</span><span class="sxs-lookup"><span data-stu-id="3e388-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="3e388-107">指定 CMYK 分離的黑色產生行為。</span><span class="sxs-lookup"><span data-stu-id="3e388-107">Specifies black generation behavior for CMYK separations.</span></span>

-   [<span data-ttu-id="3e388-108">項目資訊</span><span class="sxs-lookup"><span data-stu-id="3e388-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="3e388-109">結構化內容</span><span class="sxs-lookup"><span data-stu-id="3e388-109">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="3e388-110">可延伸標記語言 (XML)  (XML) 內容</span><span class="sxs-lookup"><span data-stu-id="3e388-110">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="3e388-111">項目資訊</span><span class="sxs-lookup"><span data-stu-id="3e388-111">Element Information</span></span>



| <span data-ttu-id="3e388-112">Name</span><span class="sxs-lookup"><span data-stu-id="3e388-112">Name</span></span> | <span data-ttu-id="3e388-113">值</span><span class="sxs-lookup"><span data-stu-id="3e388-113">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="3e388-114">項目類型</span><span class="sxs-lookup"><span data-stu-id="3e388-114">Element Type</span></span> <br/>   | <span data-ttu-id="3e388-115">功能</span><span class="sxs-lookup"><span data-stu-id="3e388-115">Feature</span></span><br/> |
| <span data-ttu-id="3e388-116">範圍前置詞</span><span class="sxs-lookup"><span data-stu-id="3e388-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="3e388-117">頁面</span><span class="sxs-lookup"><span data-stu-id="3e388-117">Page</span></span><br/>    |
| <span data-ttu-id="3e388-118">注意</span><span class="sxs-lookup"><span data-stu-id="3e388-118">Notes</span></span> <br/>          | <span data-ttu-id="3e388-119">None</span><span class="sxs-lookup"><span data-stu-id="3e388-119">None</span></span> <br/>   |



 

## <a name="structural-content"></a><span data-ttu-id="3e388-120">結構化內容</span><span class="sxs-lookup"><span data-stu-id="3e388-120">Structural Content</span></span>

<span data-ttu-id="3e388-121">此元素的 XML 結構為：</span><span class="sxs-lookup"><span data-stu-id="3e388-121">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:PageBlackGenerationProcessing">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option name="psk:_OptionName_">
    <psf:Property name="psf:IdentityOption">
      <psf:Value xsi:type="xs:string">_IdentityOptionValue_</psf:Value>
    </psf:Property>
  </psf:Option>
</psf:Feature>
```

## <a name="structure-variables"></a><span data-ttu-id="3e388-122">結構變數</span><span class="sxs-lookup"><span data-stu-id="3e388-122">Structure Variables</span></span>

<span data-ttu-id="3e388-123">下表概述 XML 結構中所定義之變數的特性。</span><span class="sxs-lookup"><span data-stu-id="3e388-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="3e388-124">Name</span><span class="sxs-lookup"><span data-stu-id="3e388-124">Name</span></span>                               | <span data-ttu-id="3e388-125">資料類型</span><span class="sxs-lookup"><span data-stu-id="3e388-125">Data type</span></span>         | <span data-ttu-id="3e388-126">單位</span><span class="sxs-lookup"><span data-stu-id="3e388-126">Unit</span></span>                  | <span data-ttu-id="3e388-127">支援的值</span><span class="sxs-lookup"><span data-stu-id="3e388-127">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="3e388-128">總結</span><span class="sxs-lookup"><span data-stu-id="3e388-128">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="3e388-129">\_選項名稱\_</span><span class="sxs-lookup"><span data-stu-id="3e388-129">\_OptionName\_</span></span><br/>          | <span data-ttu-id="3e388-130">字串</span><span class="sxs-lookup"><span data-stu-id="3e388-130">string</span></span><br/> | <span data-ttu-id="3e388-131">字元</span><span class="sxs-lookup"><span data-stu-id="3e388-131">characters</span></span><br/> | <span data-ttu-id="3e388-132">以 [XML 命名空間](https://www.w3.org/TR/1999/REC-xml-names-19990114/)所定義的有效完整名稱。</span><span class="sxs-lookup"><span data-stu-id="3e388-132">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="3e388-133">如果未指定命名空間，則會假設為預設命名空間。</span><span class="sxs-lookup"><span data-stu-id="3e388-133">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="3e388-134">選項的名稱。</span><span class="sxs-lookup"><span data-stu-id="3e388-134">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="3e388-135">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="3e388-135">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="3e388-136">字串</span><span class="sxs-lookup"><span data-stu-id="3e388-136">string</span></span><br/> | <span data-ttu-id="3e388-137">n/a</span><span class="sxs-lookup"><span data-stu-id="3e388-137">n/a</span></span><br/>        | <span data-ttu-id="3e388-138">True、False。</span><span class="sxs-lookup"><span data-stu-id="3e388-138">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="3e388-139">定義選項，當選取此選項時，會停用此功能。</span><span class="sxs-lookup"><span data-stu-id="3e388-139">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="3e388-140">可延伸標記語言 (XML)  (XML) 內容</span><span class="sxs-lookup"><span data-stu-id="3e388-140">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="3e388-141">公用列印架構關鍵字是在 https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords 命名空間中定義。</span><span class="sxs-lookup"><span data-stu-id="3e388-141">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="3e388-142">此關鍵字的 public 可延伸標記語言 (XML)  (XML) 內容定義如下：</span><span class="sxs-lookup"><span data-stu-id="3e388-142">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:PageBlackGenerationProcessing">
  <psf:Option name="psk:Automatic" />
  <psf:Option name="psk:Custom">
    <!-- The max allowable sum of the four ink coverages anywhere in an image. -->
    <psf:ScoredProperty name="psk:TotalInkCoverageLimit">
      <psf:ParameterRef name="psk:PageBlackGenerationProcessingTotalInkCoverageLimit" />
    </psf:ScoredProperty>
    <!-- The maximum allowed K channel value. -->
    <psf:ScoredProperty name="psk:BlackInkLimit">
      <psf:ParameterRef name="psk:PageBlackGenerationProcessingBlackInkLimit" />
    </psf:ScoredProperty>
    <!-- The percentage of gray component replacement to perform. -->
    <psf:ScoredProperty name="psk:GrayComponentReplacementLevel">
      <psf:ParameterRef name="psk:PageBlackGenerationProcessingGrayComponentReplacementLevel" />
    </psf:ScoredProperty>
    <!-- The point in the highlight to shadow range where GCR should start (100% = darkest shadow). -->
    <psf:ScoredProperty name="psk:GrayComponentReplacementStart">
      <psf:ParameterRef name="psk:PageBlackGenerationProcessingGrayComponentReplacementStart" />
    </psf:ScoredProperty>
    <!-- The extented beyond neutrals (into chromatic colors) that GCR applies.  0% = Undercolor component replacement, 100% = Gray component replacement.  -->
    <psf:ScoredProperty name="psk:GrayComponentReplacementExtent">
      <psf:ParameterRef name="psk:PageBlackGenerationProcessingGrayComponentReplacementExtent" />
    </psf:ScoredProperty>
    <!-- The shadow level below which UCA will be applied.  -->
    <psf:ScoredProperty name="psk:UnderColorAdditionStart">
      <psf:ParameterRef name="psk:PageBlackGenerationProcessingUnderColorAdditionStart" />
    </psf:ScoredProperty>
    <!-- The amount chromatic ink (in gray component ratios) to add to areas where GCR/UCR has generated "BlackInkLimit" (or UCAStart, if specified) in the dark neutrals and near-neutral areas.  -->
    <psf:ScoredProperty name="psk:UnderColorAdditionLevel">
      <psf:ParameterRef name="psk:PageBlackGenerationProcessingUnderColorAdditionLevel" />
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature> 
```

## <a name="related-topics"></a><span data-ttu-id="3e388-143">相關主題</span><span class="sxs-lookup"><span data-stu-id="3e388-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3e388-144">列印架構規格</span><span class="sxs-lookup"><span data-stu-id="3e388-144">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




