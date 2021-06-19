---
description: 閱讀 PageResolution 使用者可設定的元素。 本主題並非最新的。 如需最新資訊，請參閱列印架構規格。
ms.assetid: 88f9a9a3-520e-4044-9ab2-961de03878fa
title: PageResolution
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 760384ff900e7b35e37105fdb19e3635a434aa5a
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/19/2021
ms.locfileid: "112394815"
---
# <a name="pageresolution"></a><span data-ttu-id="75490-105">PageResolution</span><span class="sxs-lookup"><span data-stu-id="75490-105">PageResolution</span></span>

<span data-ttu-id="75490-106">本主題並非最新的。</span><span class="sxs-lookup"><span data-stu-id="75490-106">This topic is not current.</span></span> <span data-ttu-id="75490-107">如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。</span><span class="sxs-lookup"><span data-stu-id="75490-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="75490-108">定義列印輸出的頁面解析度，可為質化值、Dot Per Inch (DPI) 或兩者併用。</span><span class="sxs-lookup"><span data-stu-id="75490-108">Defines the page resolution of printed output as either a qualitative value or as dots per inch, or both.</span></span>

-   [<span data-ttu-id="75490-109">項目資訊</span><span class="sxs-lookup"><span data-stu-id="75490-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="75490-110">結構化內容</span><span class="sxs-lookup"><span data-stu-id="75490-110">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="75490-111">可延伸標記語言 (XML)  (XML) 內容</span><span class="sxs-lookup"><span data-stu-id="75490-111">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="75490-112">項目資訊</span><span class="sxs-lookup"><span data-stu-id="75490-112">Element Information</span></span>



| <span data-ttu-id="75490-113">Name</span><span class="sxs-lookup"><span data-stu-id="75490-113">Name</span></span> | <span data-ttu-id="75490-114">值</span><span class="sxs-lookup"><span data-stu-id="75490-114">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="75490-115">項目類型</span><span class="sxs-lookup"><span data-stu-id="75490-115">Element Type</span></span> <br/>   | <span data-ttu-id="75490-116">功能</span><span class="sxs-lookup"><span data-stu-id="75490-116">Feature</span></span><br/> |
| <span data-ttu-id="75490-117">範圍前置詞</span><span class="sxs-lookup"><span data-stu-id="75490-117">Scoping Prefix</span></span> <br/> | <span data-ttu-id="75490-118">頁面</span><span class="sxs-lookup"><span data-stu-id="75490-118">Page</span></span><br/>    |
| <span data-ttu-id="75490-119">注意</span><span class="sxs-lookup"><span data-stu-id="75490-119">Notes</span></span> <br/>          | <span data-ttu-id="75490-120">None</span><span class="sxs-lookup"><span data-stu-id="75490-120">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="75490-121">結構化內容</span><span class="sxs-lookup"><span data-stu-id="75490-121">Structural Content</span></span>

<span data-ttu-id="75490-122">此元素的 XML 結構為：</span><span class="sxs-lookup"><span data-stu-id="75490-122">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:PageResolution">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option>
    <psf:Property name="psf:IdentityOption">
      <psf:Value xsi:type="xs:string">_IdentityOptionValue_</psf:Value>
    </psf:Property>
    <psf:ScoredProperty name="psk:ResolutionX">
      <psf:Value xsi:type="xs:integer">_ResolutionXValue_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:ResolutionY">
      <psf:Value xsi:type="xs:integer">_ResolutionYValue_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:QualitativeResolution">
      <psf:Value xsi:type="xs:string">_QualitativeResolutionValue_</psf:Value>
    </psf:ScoredProperty> 
  </psf:Option>
</psf:Feature>      
```

## <a name="structure-variables"></a><span data-ttu-id="75490-123">結構變數</span><span class="sxs-lookup"><span data-stu-id="75490-123">Structure Variables</span></span>

<span data-ttu-id="75490-124">下表概述 XML 結構中所定義之變數的特性。</span><span class="sxs-lookup"><span data-stu-id="75490-124">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="75490-125">Name</span><span class="sxs-lookup"><span data-stu-id="75490-125">Name</span></span>                                      | <span data-ttu-id="75490-126">資料類型</span><span class="sxs-lookup"><span data-stu-id="75490-126">Data type</span></span>          | <span data-ttu-id="75490-127">單位</span><span class="sxs-lookup"><span data-stu-id="75490-127">Unit</span></span>                  | <span data-ttu-id="75490-128">支援的值</span><span class="sxs-lookup"><span data-stu-id="75490-128">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="75490-129">總結</span><span class="sxs-lookup"><span data-stu-id="75490-129">Summary</span></span>                                                                                                                                                          |
|-------------------------------------------|--------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="75490-130">\_選項名稱\_</span><span class="sxs-lookup"><span data-stu-id="75490-130">\_OptionName\_</span></span><br/>                 | <span data-ttu-id="75490-131">string</span><span class="sxs-lookup"><span data-stu-id="75490-131">string</span></span><br/>  | <span data-ttu-id="75490-132">字元</span><span class="sxs-lookup"><span data-stu-id="75490-132">characters</span></span><br/> | <span data-ttu-id="75490-133">以 [XML 命名空間](https://www.w3.org/TR/1999/REC-xml-names-19990114/)所定義的有效完整名稱。</span><span class="sxs-lookup"><span data-stu-id="75490-133">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="75490-134">如果未指定命名空間，則會假設為預設命名空間。</span><span class="sxs-lookup"><span data-stu-id="75490-134">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="75490-135">選項的名稱。</span><span class="sxs-lookup"><span data-stu-id="75490-135">The name of the option.</span></span><br/>                                                                                                                               |
| <span data-ttu-id="75490-136">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="75490-136">\_IdentityOptionValue\_</span></span><br/>        | <span data-ttu-id="75490-137">string</span><span class="sxs-lookup"><span data-stu-id="75490-137">string</span></span><br/>  | <span data-ttu-id="75490-138">n/a</span><span class="sxs-lookup"><span data-stu-id="75490-138">n/a</span></span><br/>        | <span data-ttu-id="75490-139">True、False。</span><span class="sxs-lookup"><span data-stu-id="75490-139">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="75490-140">定義選項，當選取此選項時，會停用此功能。</span><span class="sxs-lookup"><span data-stu-id="75490-140">Defines an Option which when selected would disable this feature.</span></span><br/>                                                                                     |
| <span data-ttu-id="75490-141">\_ResolutionXValue\_</span><span class="sxs-lookup"><span data-stu-id="75490-141">\_ResolutionXValue\_</span></span><br/>           | <span data-ttu-id="75490-142">整數</span><span class="sxs-lookup"><span data-stu-id="75490-142">integer</span></span><br/> | <span data-ttu-id="75490-143">DPI</span><span class="sxs-lookup"><span data-stu-id="75490-143">DPI</span></span><br/>        | <span data-ttu-id="75490-144">大於 0。</span><span class="sxs-lookup"><span data-stu-id="75490-144">Greater than 0.</span></span><br/>                                                                                                                                                            | <span data-ttu-id="75490-145">以 DPI (（相對於媒體) 的 PageMediaSize 和饋送方向），指定相對於 PageImageableSize 的解析度 x 元件。</span><span class="sxs-lookup"><span data-stu-id="75490-145">Specifies the x component of the resolution relative to the PageImageableSize in DPI (relative to the PageMediaSize and feed direction of the media).</span></span><br/> |
| <span data-ttu-id="75490-146">\_ResolutionYValue\_</span><span class="sxs-lookup"><span data-stu-id="75490-146">\_ResolutionYValue\_</span></span><br/>           | <span data-ttu-id="75490-147">整數</span><span class="sxs-lookup"><span data-stu-id="75490-147">integer</span></span><br/> | <span data-ttu-id="75490-148">DPI</span><span class="sxs-lookup"><span data-stu-id="75490-148">DPI</span></span><br/>        | <span data-ttu-id="75490-149">大於 0。</span><span class="sxs-lookup"><span data-stu-id="75490-149">Greater than 0.</span></span><br/>                                                                                                                                                            | <span data-ttu-id="75490-150">指定相對於媒體) 的 PageMediaSize 和饋送方向，相對於 DPI (的解析度的 y 元件。</span><span class="sxs-lookup"><span data-stu-id="75490-150">Specifies the y component of the resolution relative to the PageImageableSize in DPI (relative to the PageMediaSize and feed direction of the media).</span></span><br/> |
| <span data-ttu-id="75490-151">\_QualitativeResolutionValue\_</span><span class="sxs-lookup"><span data-stu-id="75490-151">\_QualitativeResolutionValue\_</span></span><br/> | <span data-ttu-id="75490-152">string</span><span class="sxs-lookup"><span data-stu-id="75490-152">string</span></span><br/>  | <span data-ttu-id="75490-153">n/a</span><span class="sxs-lookup"><span data-stu-id="75490-153">n/a</span></span><br/>        | <span data-ttu-id="75490-154">預設值、草稿、高、標準、其他。</span><span class="sxs-lookup"><span data-stu-id="75490-154">Default, Draft, High, Normal, Other.</span></span><br/>                                                                                                                                       | <span data-ttu-id="75490-155">指定解析度的品質標籤。</span><span class="sxs-lookup"><span data-stu-id="75490-155">Specifies a quality label for the resolution.</span></span><br/>                                                                                                         |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="75490-156">可延伸標記語言 (XML)  (XML) 內容</span><span class="sxs-lookup"><span data-stu-id="75490-156">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="75490-157">公用列印架構關鍵字是在 https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords 命名空間中定義。</span><span class="sxs-lookup"><span data-stu-id="75490-157">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="75490-158">此關鍵字的 public 可延伸標記語言 (XML)  (XML) 內容定義如下：</span><span class="sxs-lookup"><span data-stu-id="75490-158">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:PageResolution">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option>
    <!-- The horizontal resolution in dots per inch -->
    <psf:ScoredProperty name="psk:ResolutionX">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <!-- The vertical resolution in dots per inch -->
    <psf:ScoredProperty name="psk:ResolutionY">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <!-- Value representing the resolution -->
    <psf:ScoredProperty name="psk:QualitativeResolution">
      <psf:Value xsi:type="xs:string">Other</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature>    
```

## <a name="related-topics"></a><span data-ttu-id="75490-159">相關主題</span><span class="sxs-lookup"><span data-stu-id="75490-159">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="75490-160">列印架構規格</span><span class="sxs-lookup"><span data-stu-id="75490-160">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




