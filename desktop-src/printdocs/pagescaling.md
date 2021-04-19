---
description: 本主題並非最新的。 如需最新資訊，請參閱列印架構規格。
ms.assetid: cf35bb37-bf67-4e86-bfef-9838606982a5
title: PageScaling
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41af04cc5657360fcc8d4b15812e9c2dd6b9fb06
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/06/2021
ms.locfileid: "106981767"
---
# <a name="pagescaling"></a><span data-ttu-id="c2f80-104">PageScaling</span><span class="sxs-lookup"><span data-stu-id="c2f80-104">PageScaling</span></span>

<span data-ttu-id="c2f80-105">本主題並非最新的。</span><span class="sxs-lookup"><span data-stu-id="c2f80-105">This topic is not current.</span></span> <span data-ttu-id="c2f80-106">如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。</span><span class="sxs-lookup"><span data-stu-id="c2f80-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="c2f80-107">描述輸出的縮放特性。</span><span class="sxs-lookup"><span data-stu-id="c2f80-107">Describes the scaling characteristics of the output.</span></span> <span data-ttu-id="c2f80-108">這項功能的特定選項會要求取用者能夠判斷「應用程式內容維度」的特性。</span><span class="sxs-lookup"><span data-stu-id="c2f80-108">Certain Options of this Feature requires the consumer to be able to determine characteristics of the "application content dimensions."</span></span> <span data-ttu-id="c2f80-109">如果沒有判斷這些特性的能力，取用者應該預設為識別選項。</span><span class="sxs-lookup"><span data-stu-id="c2f80-109">In the absence of the ability to determine these characteristics, the consumer should default to the identity option.</span></span> <span data-ttu-id="c2f80-110">這些特性包括：</span><span class="sxs-lookup"><span data-stu-id="c2f80-110">These characteristics are:</span></span>



|                          |                                                                                                                                                                                                                                                       |
|--------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c2f80-111">應用程式媒體大小</span><span class="sxs-lookup"><span data-stu-id="c2f80-111">Application Media Size</span></span>   | <span data-ttu-id="c2f80-112">應用程式版面配置所定義之媒體的維度。</span><span class="sxs-lookup"><span data-stu-id="c2f80-112">The dimensions of the media defined by the application layout.</span></span> <span data-ttu-id="c2f80-113">應用程式媒體大小可能會或可能不會對應至取用者所支援的 PageMediaSize。</span><span class="sxs-lookup"><span data-stu-id="c2f80-113">The application media size may or may not correspond to a PageMediaSize supported by the consumer.</span></span><br/>                                                                          |
| <span data-ttu-id="c2f80-114">應用程式內容大小</span><span class="sxs-lookup"><span data-stu-id="c2f80-114">Application Content Size</span></span> | <span data-ttu-id="c2f80-115">應用程式版面配置所定義之媒體的維度。</span><span class="sxs-lookup"><span data-stu-id="c2f80-115">The dimensions of the media defined by the application layout.</span></span> <span data-ttu-id="c2f80-116">應用程式媒體大小可能會或可能不會對應至取用者所支援的 PageMediaSize。</span><span class="sxs-lookup"><span data-stu-id="c2f80-116">The application media size may or may not correspond to a PageMediaSize supported by the consumer.</span></span><br/>                                                                          |
| <span data-ttu-id="c2f80-117">應用程式出血大小</span><span class="sxs-lookup"><span data-stu-id="c2f80-117">Application Bleed Size</span></span>   | <span data-ttu-id="c2f80-118">應用程式出血區域的位移和範圍、應用程式用來註冊和配置的溢位方塊（相對於應用程式媒體大小）。</span><span class="sxs-lookup"><span data-stu-id="c2f80-118">The offset and extent of the application bleed area, an overflow box used by application for registration and layout, in relation to the application media size.</span></span> <span data-ttu-id="c2f80-119">出血區域將會相當於或等於應用程式媒體大小。</span><span class="sxs-lookup"><span data-stu-id="c2f80-119">The bleed area will be great than or equal to the application media size.</span></span><br/> |



 

-   [<span data-ttu-id="c2f80-120">項目資訊</span><span class="sxs-lookup"><span data-stu-id="c2f80-120">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="c2f80-121">結構化內容</span><span class="sxs-lookup"><span data-stu-id="c2f80-121">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="c2f80-122">可延伸標記語言 (XML)  (XML) 內容</span><span class="sxs-lookup"><span data-stu-id="c2f80-122">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="c2f80-123">項目資訊</span><span class="sxs-lookup"><span data-stu-id="c2f80-123">Element Information</span></span>



| <span data-ttu-id="c2f80-124">Name</span><span class="sxs-lookup"><span data-stu-id="c2f80-124">Name</span></span>                       |                                                                                                                                                                                                       |
|----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c2f80-125">項目類型</span><span class="sxs-lookup"><span data-stu-id="c2f80-125">Element Type</span></span> <br/>   | <span data-ttu-id="c2f80-126">功能</span><span class="sxs-lookup"><span data-stu-id="c2f80-126">Feature</span></span><br/>                                                                                                                                                                                    |
| <span data-ttu-id="c2f80-127">範圍前置詞</span><span class="sxs-lookup"><span data-stu-id="c2f80-127">Scoping Prefix</span></span> <br/> | <span data-ttu-id="c2f80-128">頁面</span><span class="sxs-lookup"><span data-stu-id="c2f80-128">Page</span></span><br/>                                                                                                                                                                                       |
| <span data-ttu-id="c2f80-129">備註</span><span class="sxs-lookup"><span data-stu-id="c2f80-129">Notes</span></span> <br/>          | <span data-ttu-id="c2f80-130">頂端、底部、左方和右邊都是相對於 PageImageableSize。</span><span class="sxs-lookup"><span data-stu-id="c2f80-130">Top, Bottom, Left, and Right are relative to the PageImageableSize.</span></span> <span data-ttu-id="c2f80-131">座標相對於 PageImageableSize，其中的來源相對於 PageImageableSize 的原點。</span><span class="sxs-lookup"><span data-stu-id="c2f80-131">Coordinates are relative to PageImageableSize, where the origin of is relative to the origin of the PageImageableSize.</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="c2f80-132">結構化內容</span><span class="sxs-lookup"><span data-stu-id="c2f80-132">Structural Content</span></span>

<span data-ttu-id="c2f80-133">此元素的 XML 結構為：</span><span class="sxs-lookup"><span data-stu-id="c2f80-133">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:PageScaling">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option name="psk:_OptionName_">
    <psf:Property name="psf:IdentityOption">
      <psf:Value xsi:type="xs:string">_IdentityOptionValue_</psf:Value>
    </psf:Property>
    <!-- Specifies offset of the width relative to the PageImageableSize.  
         Measured in microns. -->
    <psf:ScoredProperty name="psk:OffsetWidth">
      <psf:ParameterRef name="psk:PageScalingOffsetWidth" />
    </psf:ScoredProperty>
    <!-- Specifies offset of the height relative to the PageImageableSize.  
         Measured in microns. -->
    <psf:ScoredProperty name="psk:OffsetHeight">
      <psf:ParameterRef name="psk:PageScalingOffsetHeight" />
    </psf:ScoredProperty>
    <!-- Specifies the scaling percentage for the width dimension relative to the PageImageableSize. -->
    <psf:ScoredProperty name="psk:ScaleWidth">
      <psf:ParameterRef name="psk:PageScalingScaleWidth" />
    </psf:ScoredProperty>
    <!-- Specifies the scaling percentage for the height dimension relative to the PageImageableSize. -->
    <psf:ScoredProperty name="psk:ScaleHeight">
      <psf:ParameterRef name="psk:PageScalingScaleHeight" />
    </psf:ScoredProperty>
    <!-- Specifies the scaling percentage for square scaling (both dimensions are scaled equally). -->
    <psf:ScoredProperty name="psk:Scale">
      <psf:ParameterRef name="psk:PageScalingScale" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies the alignment of the scaled content. -->
  <psf:Feature name="psk:ScaleOffsetAlignment">
    <!-- Specifies the scaling should be aligned on the center of the bottom edge of the media. -->
    <psf:Option name="psk:BottomCenter"/>
    <!-- Specifies the scaling should be aligned on the bottom left corner of the media. -->
    <psf:Option name="psk:BottomLeft" />
    <!-- Specifies the scaling should be aligned on the bottom right corner of the media. -->
    <psf:Option name="psk:BottomRight "/>
    <!-- Specifies the scaling should be aligned on the bottom right corner of the media. -->
    <psf:Option name="psk:Center"/>
    <!-- Specifies the scaling should be aligned on the center of the left edge of the media. -->
    <psf:Option name="psk:LeftCenter"/>
    <!-- Specifies the scaling should be aligned on the center of the right edge of the media. -->
    <psf:Option name="psk:RightCenter"/>
    <!-- Specifies the scaling should be aligned on the center of the top edge of the media. -->
    <psf:Option name="psk:TopCenter"/>
    <!-- Specifies the scaling should be aligned on the top left corner of the media. -->
    <psf:Option name="psk:TopLeft"/>
    <!-- Specifies the scaling should be aligned on the top right corner of the media. -->
    <psf:Option name="psk:TopRight"/>
  </psf:Feature>
</psf:Feature>
```

## <a name="structure-variables"></a><span data-ttu-id="c2f80-134">結構變數</span><span class="sxs-lookup"><span data-stu-id="c2f80-134">Structure Variables</span></span>

<span data-ttu-id="c2f80-135">下表概述 XML 結構中所定義之變數的特性。</span><span class="sxs-lookup"><span data-stu-id="c2f80-135">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="c2f80-136">Name</span><span class="sxs-lookup"><span data-stu-id="c2f80-136">Name</span></span>                               | <span data-ttu-id="c2f80-137">資料類型</span><span class="sxs-lookup"><span data-stu-id="c2f80-137">Data type</span></span>         | <span data-ttu-id="c2f80-138">單位</span><span class="sxs-lookup"><span data-stu-id="c2f80-138">Unit</span></span>                  | <span data-ttu-id="c2f80-139">支援的值</span><span class="sxs-lookup"><span data-stu-id="c2f80-139">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="c2f80-140">總結</span><span class="sxs-lookup"><span data-stu-id="c2f80-140">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="c2f80-141">\_選項名稱\_</span><span class="sxs-lookup"><span data-stu-id="c2f80-141">\_OptionName\_</span></span><br/>          | <span data-ttu-id="c2f80-142">字串</span><span class="sxs-lookup"><span data-stu-id="c2f80-142">string</span></span><br/> | <span data-ttu-id="c2f80-143">字元</span><span class="sxs-lookup"><span data-stu-id="c2f80-143">characters</span></span><br/> | <span data-ttu-id="c2f80-144">以 [XML 命名空間](https://www.w3.org/TR/1999/REC-xml-names-19990114/)所定義的有效完整名稱。</span><span class="sxs-lookup"><span data-stu-id="c2f80-144">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="c2f80-145">如果未指定命名空間，則會假設為預設命名空間。</span><span class="sxs-lookup"><span data-stu-id="c2f80-145">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="c2f80-146">選項的名稱。</span><span class="sxs-lookup"><span data-stu-id="c2f80-146">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="c2f80-147">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="c2f80-147">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="c2f80-148">字串</span><span class="sxs-lookup"><span data-stu-id="c2f80-148">string</span></span><br/> | <span data-ttu-id="c2f80-149">n/a</span><span class="sxs-lookup"><span data-stu-id="c2f80-149">n/a</span></span><br/>        | <span data-ttu-id="c2f80-150">True、False。</span><span class="sxs-lookup"><span data-stu-id="c2f80-150">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="c2f80-151">定義選項，當選取此選項時，會停用此功能。</span><span class="sxs-lookup"><span data-stu-id="c2f80-151">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="c2f80-152">可延伸標記語言 (XML)  (XML) 內容</span><span class="sxs-lookup"><span data-stu-id="c2f80-152">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="c2f80-153">公用列印架構關鍵字是在 https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords 命名空間中定義。</span><span class="sxs-lookup"><span data-stu-id="c2f80-153">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="c2f80-154">此關鍵字的 public 可延伸標記語言 (XML)  (XML) 內容定義如下：</span><span class="sxs-lookup"><span data-stu-id="c2f80-154">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:PageScaling">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option name="psk:Custom">
    <psf:ScoredProperty name="psk:OffsetWidth">
      <psf:ParameterRef name="psk:PageScalingOffsetWidth" />
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:OffsetHeight">
      <psf:ParameterRef name="psk:PageScalingOffsetHeight" />
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:ScaleWidth">
      <psf:ParameterRef name="psk:PageScalingScaleWidth" />
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:ScaleHeight">
      <psf:ParameterRef name="psk:PageScalingScaleHeight" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies a custom square scaling should be applied to the Application Media Size. -->
  <psf:Option name="psk:CustomSquare">
    <psf:ScoredProperty name="psk:OffsetWidth">
      <psf:ParameterRef name="psk:PageScalingOffsetWidth" />
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:OffsetHeight">
      <psf:ParameterRef name="psk:PageScalingOffsetHeight" />
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Scale">
      <psf:ParameterRef name="psk:PageScalingScale" />
    </psf:ScoredProperty>
  </psf:Option>

  <!-- Specifies the application bleed size should be scaled to the PageImageableSize preserving the aspect ratio. -->
  <psf:Option name="psk:FitApplicationBleedSizeToPageImageableSize" />
  <!-- Specifies the application content size should be scaled to the PageImageableSize preserving the aspect ratio. -->
  <psf:Option name="psk:FitApplicationContentSizeToPageImageableSize" />
  <!-- Specifies the application media size should be scaled to the PageImageableSize preserving the aspect ratio. -->
  <psf:Option name="psk:FitApplicationMediaSizeToPageImageableSize" />
  <!-- Specifies the application media size should be scaled to the PageMediaSize preserving the aspect ratio. -->
  <psf:Option name="psk:FitApplicationMediaSizeToPageMediaSize" />

  <!-- Specifies that no scaling should be applied. -->
  <psf:Option name="psk:None" />

  <!-- Specifies the alignment of the scaled content. -->
  <psf:Feature name="psk:ScaleOffsetAlignment">
    <!-- Specifies the scaling should be aligned on the center of the bottom edge of the media. -->
    <psf:Option name="psk:BottomCenter" />
    <!-- Specifies the scaling should be aligned on the bottom left corner of the media.-->
    <psf:Option name="psk:BottomLeft" />
    <!--Specifies the scaling should be aligned on the bottom right corner of the media.-->
    <psf:Option name="psk:BottomRight" />
    <!-- Specifies the scaling should be centered on the media.-->
    <psf:Option name="psk:Center" />
    <!-- Specifies the scaling should be aligned on the center of the left edge of the media.-->
    <psf:Option name="psk:LeftCenter" />
    <!--Specifies the scaling should be aligned on the center of the right edge of the media.-->
    <psf:Option name="psk:RightCenter" />
    <!-- Specifies the scaling should be aligned on the center of the top edge of the media.-->
    <psf:Option name="psk:TopCenter" />
    <!--  Specifies the scaling should be aligned on the top left corner of the media.-->
    <psf:Option name="psk:TopLeft" />
    <!-- Specifies the scaling should be aligned on the top right corner of the media.-->
    <psf:Option name="psk:TopRight" />
  </psf:Feature>
</psf:Feature>
```

## <a name="related-topics"></a><span data-ttu-id="c2f80-155">相關主題</span><span class="sxs-lookup"><span data-stu-id="c2f80-155">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c2f80-156">列印架構規格</span><span class="sxs-lookup"><span data-stu-id="c2f80-156">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




