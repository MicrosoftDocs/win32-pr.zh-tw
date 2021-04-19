---
description: 本主題並非最新的。 如需最新資訊，請參閱列印架構規格。
ms.assetid: d1c36c47-107c-4012-a839-1018c2652209
title: PageWatermark
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8d0e0e47aa89a3cb6380a78dd49312d17f88ab8
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/06/2021
ms.locfileid: "106986461"
---
# <a name="pagewatermark"></a><span data-ttu-id="25c31-104">PageWatermark</span><span class="sxs-lookup"><span data-stu-id="25c31-104">PageWatermark</span></span>

<span data-ttu-id="25c31-105">本主題並非最新的。</span><span class="sxs-lookup"><span data-stu-id="25c31-105">This topic is not current.</span></span> <span data-ttu-id="25c31-106">如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。</span><span class="sxs-lookup"><span data-stu-id="25c31-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="25c31-107">描述輸出的浮水印設定和水位線特性。</span><span class="sxs-lookup"><span data-stu-id="25c31-107">Describes the watermark setting of the output and the watermark characteristics.</span></span> <span data-ttu-id="25c31-108">浮水印適用于邏輯頁面，而不是實體頁面。</span><span class="sxs-lookup"><span data-stu-id="25c31-108">Watermarks apply to the logical page, not the physical page.</span></span> <span data-ttu-id="25c31-109">例如，如果啟用 DocumentDuplex，每個工作表上的每個 NUp 頁面上都會出現浮水印。</span><span class="sxs-lookup"><span data-stu-id="25c31-109">For example, if DocumentDuplex is enabled, a watermark will appear on each NUp page on each sheet.</span></span> <span data-ttu-id="25c31-110">如果 DocumentDuplex，PagesPerSheet = 2，則每個工作表都會有2個浮水印。</span><span class="sxs-lookup"><span data-stu-id="25c31-110">If DocumentDuplex, PagesPerSheet=2, then each sheet will have 2 watermarks.</span></span>

-   [<span data-ttu-id="25c31-111">項目資訊</span><span class="sxs-lookup"><span data-stu-id="25c31-111">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="25c31-112">結構化內容</span><span class="sxs-lookup"><span data-stu-id="25c31-112">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="25c31-113">可延伸標記語言 (XML)  (XML) 內容</span><span class="sxs-lookup"><span data-stu-id="25c31-113">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="25c31-114">項目資訊</span><span class="sxs-lookup"><span data-stu-id="25c31-114">Element Information</span></span>



| <span data-ttu-id="25c31-115">Name</span><span class="sxs-lookup"><span data-stu-id="25c31-115">Name</span></span>                       |                                                                                                                                                 |
|----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="25c31-116">項目類型</span><span class="sxs-lookup"><span data-stu-id="25c31-116">Element Type</span></span> <br/>   | <span data-ttu-id="25c31-117">功能</span><span class="sxs-lookup"><span data-stu-id="25c31-117">Feature</span></span><br/>                                                                                                                              |
| <span data-ttu-id="25c31-118">範圍前置詞</span><span class="sxs-lookup"><span data-stu-id="25c31-118">Scoping Prefix</span></span> <br/> | <span data-ttu-id="25c31-119">頁面</span><span class="sxs-lookup"><span data-stu-id="25c31-119">Page</span></span><br/>                                                                                                                                 |
| <span data-ttu-id="25c31-120">備註</span><span class="sxs-lookup"><span data-stu-id="25c31-120">Notes</span></span> <br/>          | <span data-ttu-id="25c31-121">座標是相對於 PageImageableSize，其中浮水印的原點相對於 PageImageableSize 的原點。</span><span class="sxs-lookup"><span data-stu-id="25c31-121">Coordinates are relative to PageImageableSize, where the origin of the watermark is relative to the origin of the PageImageableSize.</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="25c31-122">結構化內容</span><span class="sxs-lookup"><span data-stu-id="25c31-122">Structural Content</span></span>

<span data-ttu-id="25c31-123">此元素的 XML 結構如下所示：</span><span class="sxs-lookup"><span data-stu-id="25c31-123">The XML structure of this element is as follows:</span></span>

``` syntax
<psf:Feature name="psk:PageWatermark">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option name="psk:_OptionName_">
    <psf:Property name="psf:IdentityOption">
      <psf:Value xsi:type="xs:string">_IdentityOptionValue_</psf:Value>
    </psf:Property>
    <!-- Defines the width origin of the watermark. See the PageWatermarkOriginWidth ParameterDefinition for more information. -->
    <psf:ScoredProperty name="psk:OriginWidth">
      <psf:ParameterRef name="psk:PageWatermarkOriginWidth" />
    </psf:ScoredProperty>
    <!-- Defines the height origin of the watermark. See the PageWatermarkOriginHeight ParameterDefinition for more information. -->
    <psf:ScoredProperty name="psk:OriginHeight">
      <psf:ParameterRef name="psk:PageWatermarkOriginHeight" />
    </psf:ScoredProperty>
    <!-- Defines the transparency value of the watermark.  Transparency should be applied to all content, including transparent content. See the PageWatermarkTransparency ParameterDefinition for more information. -->
    <psf:ScoredProperty name="psk:Transparency">
      <psf:ParameterRef name="psk:PageWatermarkTransparency" />
    </psf:ScoredProperty>
    <!-- Defines the angle value of the watermark.  See the PageWatermarkAngle ParameterDefinition for more information. -->
    <psf:ScoredProperty name="psk:Angle">
      <psf:ParameterRef name="psk:PageWatermarkAngle" />
    </psf:ScoredProperty>
    <!-- Applicable to options that include bitmaps.  -->
    <!-- Specifies the text font color -->
    <!-- Applicable to options that include text. Defines the sRGB color for the watermark text.  Format is ARGB: #AARRGGBB.   -->
    <psf:ScoredProperty name="psk:FontColor">
      <psf:ParameterRef name="psk:PageWatermarkTextColor" />
    </psf:ScoredProperty>
    <!-- Applicable to options that include text.  Defines the available font sizes for the watermark text. Measured in points.-->
    <psf:ScoredProperty name="psk:FontSize">
      <psf:ParameterRef name="psk:PageWatermarkTextFontSize" />
    </psf:ScoredProperty>
    <!-- Applicable to options that include text. Defines the text to be displayed in the watermark. -->
    <psf:ScoredProperty name="psk:Text">
      <psf:ParameterRef name="psk:PageWatermarkTextText" />
    </psf:ScoredProperty>
  </psf:Option>
  <!--Defines the layering behavior of the watermark. -->
  <psf:Feature name="psk:Layering">
    <!-- Watermark appears over page content. -->
    <psf:Option name="psk:Overlay" />
    <!-- Watermark appear under page content. -->
    <psf:Option name="psk:Underlay" />
  </psf:Feature>
</psf:Feature>
```

## <a name="structure-variables"></a><span data-ttu-id="25c31-124">結構變數</span><span class="sxs-lookup"><span data-stu-id="25c31-124">Structure Variables</span></span>

<span data-ttu-id="25c31-125">下表概述 XML 結構中所定義之變數的特性。</span><span class="sxs-lookup"><span data-stu-id="25c31-125">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="25c31-126">Name</span><span class="sxs-lookup"><span data-stu-id="25c31-126">Name</span></span>                               | <span data-ttu-id="25c31-127">資料類型</span><span class="sxs-lookup"><span data-stu-id="25c31-127">Data type</span></span>         | <span data-ttu-id="25c31-128">單位</span><span class="sxs-lookup"><span data-stu-id="25c31-128">Unit</span></span>                  | <span data-ttu-id="25c31-129">支援的值</span><span class="sxs-lookup"><span data-stu-id="25c31-129">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="25c31-130">總結</span><span class="sxs-lookup"><span data-stu-id="25c31-130">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="25c31-131">\_選項名稱\_</span><span class="sxs-lookup"><span data-stu-id="25c31-131">\_OptionName\_</span></span><br/>          | <span data-ttu-id="25c31-132">字串</span><span class="sxs-lookup"><span data-stu-id="25c31-132">string</span></span><br/> | <span data-ttu-id="25c31-133">字元</span><span class="sxs-lookup"><span data-stu-id="25c31-133">characters</span></span><br/> | <span data-ttu-id="25c31-134">以 [XML 命名空間](https://www.w3.org/TR/1999/REC-xml-names-19990114/)所定義的有效完整名稱。</span><span class="sxs-lookup"><span data-stu-id="25c31-134">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="25c31-135">如果未指定命名空間，則會假設為預設命名空間。</span><span class="sxs-lookup"><span data-stu-id="25c31-135">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="25c31-136">選項的名稱。</span><span class="sxs-lookup"><span data-stu-id="25c31-136">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="25c31-137">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="25c31-137">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="25c31-138">字串</span><span class="sxs-lookup"><span data-stu-id="25c31-138">string</span></span><br/> | <span data-ttu-id="25c31-139">n/a</span><span class="sxs-lookup"><span data-stu-id="25c31-139">n/a</span></span><br/>        | <span data-ttu-id="25c31-140">True、False。</span><span class="sxs-lookup"><span data-stu-id="25c31-140">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="25c31-141">定義選項，當選取此選項時，會停用此功能。</span><span class="sxs-lookup"><span data-stu-id="25c31-141">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="25c31-142">可延伸標記語言 (XML)  (XML) 內容</span><span class="sxs-lookup"><span data-stu-id="25c31-142">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="25c31-143">公用列印架構關鍵字是在 https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords 命名空間中定義。</span><span class="sxs-lookup"><span data-stu-id="25c31-143">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="25c31-144">此關鍵字的 public 可延伸標記語言 (XML)  (XML) 內容定義如下：</span><span class="sxs-lookup"><span data-stu-id="25c31-144">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:PageWatermark">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!-- Specifies a text only watermark -->
  <psf:Option name="psk:Text">
    <psf:Property name="psf:IdentityOption">
      <psf:Value xsi:type="xs:string">True</psf:Value>
    </psf:Property>
    <psf:ScoredProperty name="psk:OriginWidth">
      <psf:ParameterRef name="psk:PageWatermarkOriginWidth" />
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:OriginHeight">
      <psf:ParameterRef name="psk:PageWatermarkOriginHeight" />
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:FontColor">
      <psf:ParameterRef name="psk:PageWatermarkTextColor" />
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:FontSize">
      <psf:ParameterRef name="psk:PageWatermarkTextFontSize" />
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Text">
      <psf:ParameterRef name="psk:PageWatermarkTextText" />
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Transparency">
      <psf:ParameterRef name="psk:PageWatermarkTransparency" />
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Angle">
      <psf:ParameterRef name="psk:PageWatermarkTextAngle" />
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Feature name="psk:Layering">
    <!--Specifies Overlay Layering-->
    <psf:Option name="psk:Overlay" />
    <!--Specifies Underlay Layering-->
    <psf:Option name="psk:Underlay" />
  </psf:Feature>
</psf:Feature>
```

## <a name="related-topics"></a><span data-ttu-id="25c31-145">相關主題</span><span class="sxs-lookup"><span data-stu-id="25c31-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="25c31-146">列印架構規格</span><span class="sxs-lookup"><span data-stu-id="25c31-146">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




