---
description: 深入瞭解 PageOutputColor 使用者可設定的元素。 本主題並非最新的。 如需最新資訊，請參閱列印架構規格。
ms.assetid: 1afcf2e6-5d6d-4b87-a005-15d42a610f69
title: PageOutputColor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79fc71f58bde44224642d3a5f6979e3aef929976
ms.sourcegitcommit: 998d50f6def8a25850fc113fc8a2df903c829c5e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/09/2021
ms.locfileid: "113548986"
---
# <a name="pageoutputcolor"></a><span data-ttu-id="7c252-105">PageOutputColor</span><span class="sxs-lookup"><span data-stu-id="7c252-105">PageOutputColor</span></span>

<span data-ttu-id="7c252-106">本主題並非最新的。</span><span class="sxs-lookup"><span data-stu-id="7c252-106">This topic is not current.</span></span> <span data-ttu-id="7c252-107">如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。</span><span class="sxs-lookup"><span data-stu-id="7c252-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="7c252-108">描述輸出的色彩設定特性。</span><span class="sxs-lookup"><span data-stu-id="7c252-108">Describes the characteristics of the color settings for the output.</span></span>

-   [<span data-ttu-id="7c252-109">項目資訊</span><span class="sxs-lookup"><span data-stu-id="7c252-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="7c252-110">結構化內容</span><span class="sxs-lookup"><span data-stu-id="7c252-110">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="7c252-111">可延伸標記語言 (XML)  (XML) 內容</span><span class="sxs-lookup"><span data-stu-id="7c252-111">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="7c252-112">項目資訊</span><span class="sxs-lookup"><span data-stu-id="7c252-112">Element Information</span></span>



| <span data-ttu-id="7c252-113">Name</span><span class="sxs-lookup"><span data-stu-id="7c252-113">Name</span></span> | <span data-ttu-id="7c252-114">值</span><span class="sxs-lookup"><span data-stu-id="7c252-114">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="7c252-115">項目類型</span><span class="sxs-lookup"><span data-stu-id="7c252-115">Element Type</span></span> <br/>   | <span data-ttu-id="7c252-116">功能</span><span class="sxs-lookup"><span data-stu-id="7c252-116">Feature</span></span><br/> |
| <span data-ttu-id="7c252-117">範圍前置詞</span><span class="sxs-lookup"><span data-stu-id="7c252-117">Scoping Prefix</span></span> <br/> | <span data-ttu-id="7c252-118">頁面</span><span class="sxs-lookup"><span data-stu-id="7c252-118">Page</span></span><br/>    |
| <span data-ttu-id="7c252-119">注意</span><span class="sxs-lookup"><span data-stu-id="7c252-119">Notes</span></span> <br/>          | <span data-ttu-id="7c252-120">None</span><span class="sxs-lookup"><span data-stu-id="7c252-120">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="7c252-121">結構化內容</span><span class="sxs-lookup"><span data-stu-id="7c252-121">Structural Content</span></span>

<span data-ttu-id="7c252-122">此元素的 XML 結構為：</span><span class="sxs-lookup"><span data-stu-id="7c252-122">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:PageOutputColor">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option name="psk:_OptionName_">
    <psf:Property name="psf:IdentityOption">
      <psf:Value xsi:type="xs:string">_IdentityOptionValue_</psf:Value>
    </psf:Property>
    <psf:ScoredProperty name=psk:DeviceBitsPerPixel>
      <psf:Value xsi:type="xs:integer">_DeviceBitsPerPixelValue_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name=psk:DriverBitsPerPixel>
      <psf:Value xsi:type="xs:integer">_DriverBitsPerPixelValue_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature>
      
```

## <a name="structure-variables"></a><span data-ttu-id="7c252-123">結構變數</span><span class="sxs-lookup"><span data-stu-id="7c252-123">Structure Variables</span></span>

<span data-ttu-id="7c252-124">下表概述 XML 結構中所定義之變數的特性。</span><span class="sxs-lookup"><span data-stu-id="7c252-124">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="7c252-125">Name</span><span class="sxs-lookup"><span data-stu-id="7c252-125">Name</span></span>                                   | <span data-ttu-id="7c252-126">資料類型</span><span class="sxs-lookup"><span data-stu-id="7c252-126">Data type</span></span>          | <span data-ttu-id="7c252-127">單位</span><span class="sxs-lookup"><span data-stu-id="7c252-127">Unit</span></span>                      | <span data-ttu-id="7c252-128">支援的值</span><span class="sxs-lookup"><span data-stu-id="7c252-128">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="7c252-129">摘要</span><span class="sxs-lookup"><span data-stu-id="7c252-129">Summary</span></span>                                                                                                                           |
|----------------------------------------|--------------------|---------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7c252-130">\_選項名稱\_</span><span class="sxs-lookup"><span data-stu-id="7c252-130">\_OptionName\_</span></span><br/>              | <span data-ttu-id="7c252-131">string</span><span class="sxs-lookup"><span data-stu-id="7c252-131">string</span></span><br/>  | <span data-ttu-id="7c252-132">字元</span><span class="sxs-lookup"><span data-stu-id="7c252-132">characters</span></span><br/>     | <span data-ttu-id="7c252-133">以 [XML 命名空間](https://www.w3.org/TR/1999/REC-xml-names-19990114/)所定義的有效完整名稱。</span><span class="sxs-lookup"><span data-stu-id="7c252-133">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="7c252-134">如果未指定命名空間，則會假設為預設命名空間。</span><span class="sxs-lookup"><span data-stu-id="7c252-134">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="7c252-135">選項的名稱。</span><span class="sxs-lookup"><span data-stu-id="7c252-135">The name of the option.</span></span><br/>                                                                                                |
| <span data-ttu-id="7c252-136">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="7c252-136">\_IdentityOptionValue\_</span></span><br/>     | <span data-ttu-id="7c252-137">string</span><span class="sxs-lookup"><span data-stu-id="7c252-137">string</span></span><br/>  | <span data-ttu-id="7c252-138">n/a</span><span class="sxs-lookup"><span data-stu-id="7c252-138">n/a</span></span><br/>            | <span data-ttu-id="7c252-139">True、False。</span><span class="sxs-lookup"><span data-stu-id="7c252-139">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="7c252-140">定義選項，當選取此選項時，會停用此功能。</span><span class="sxs-lookup"><span data-stu-id="7c252-140">Defines an Option which when selected would disable this feature.</span></span><br/>                                                      |
| <span data-ttu-id="7c252-141">\_DeviceBitsPerPixelValue\_</span><span class="sxs-lookup"><span data-stu-id="7c252-141">\_DeviceBitsPerPixelValue\_</span></span><br/> | <span data-ttu-id="7c252-142">整數</span><span class="sxs-lookup"><span data-stu-id="7c252-142">integer</span></span><br/> | <span data-ttu-id="7c252-143">每圖元的位數</span><span class="sxs-lookup"><span data-stu-id="7c252-143">bits per pixel</span></span><br/> | <span data-ttu-id="7c252-144">大於0，小於裝置支援值上限。</span><span class="sxs-lookup"><span data-stu-id="7c252-144">Greater than 0, less than maximum device support value.</span></span><br/>                                                                                                                    | <span data-ttu-id="7c252-145">數值，指出印表機所支援之色彩資料的每一像素位元數。</span><span class="sxs-lookup"><span data-stu-id="7c252-145">Numeric value indicating the number of bits per pixel of color data supported by the printer.</span></span><br/>                          |
| <span data-ttu-id="7c252-146">\_DriverBitsPerPixelValue\_</span><span class="sxs-lookup"><span data-stu-id="7c252-146">\_DriverBitsPerPixelValue\_</span></span><br/> | <span data-ttu-id="7c252-147">整數</span><span class="sxs-lookup"><span data-stu-id="7c252-147">integer</span></span><br/> | <span data-ttu-id="7c252-148">每圖元的位數</span><span class="sxs-lookup"><span data-stu-id="7c252-148">bits per pixel</span></span><br/> | <span data-ttu-id="7c252-149">大於0，小於裝置支援值上限。</span><span class="sxs-lookup"><span data-stu-id="7c252-149">Greater than 0, less than maximum device support value.</span></span><br/>                                                                                                                    | <span data-ttu-id="7c252-150">數值，表示核心驅動程式應針對其點陣圖轉譯緩衝區使用的每一像素位元數。</span><span class="sxs-lookup"><span data-stu-id="7c252-150">Numeric value indicating the number of bits per pixel that the core driver should use for its bitmap rendering buffer.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="7c252-151">可延伸標記語言 (XML)  (XML) 內容</span><span class="sxs-lookup"><span data-stu-id="7c252-151">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="7c252-152">公用列印架構關鍵字是在 https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords 命名空間中定義。</span><span class="sxs-lookup"><span data-stu-id="7c252-152">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="7c252-153">此關鍵字的 public 可延伸標記語言 (XML)  (XML) 內容定義如下：</span><span class="sxs-lookup"><span data-stu-id="7c252-153">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:PageOutputColor">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!-- Specifies the output should be in color. -->
  <psf:Option name="psk:Color">
    <psf:ScoredProperty name="psk:DeviceBitsPerPixel">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:DriverBitsPerPixel">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies the output should be in grayscale. -->
  <psf:Option name="psk:Grayscale">
    <psf:ScoredProperty name="psk:DeviceBitsPerPixel">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:DriverBitsPerPixel">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies the output should be in monochrome (Black). -->
  <psf:Option name="psk:Monochrome">
    <psf:ScoredProperty name="psk:DeviceBitsPerPixel">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:DriverBitsPerPixel">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature>
```

## <a name="related-topics"></a><span data-ttu-id="7c252-154">相關主題</span><span class="sxs-lookup"><span data-stu-id="7c252-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7c252-155">列印架構規格</span><span class="sxs-lookup"><span data-stu-id="7c252-155">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




