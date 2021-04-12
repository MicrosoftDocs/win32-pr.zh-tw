---
description: 本主題並非最新的。 如需最新資訊，請參閱列印架構規格。
ms.assetid: 1afcf2e6-5d6d-4b87-a005-15d42a610f69
title: PageOutputColor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71796bae9528fe6b32397f3467113630159c9954
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/06/2021
ms.locfileid: "104195855"
---
# <a name="pageoutputcolor"></a><span data-ttu-id="e4028-104">PageOutputColor</span><span class="sxs-lookup"><span data-stu-id="e4028-104">PageOutputColor</span></span>

<span data-ttu-id="e4028-105">本主題並非最新的。</span><span class="sxs-lookup"><span data-stu-id="e4028-105">This topic is not current.</span></span> <span data-ttu-id="e4028-106">如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。</span><span class="sxs-lookup"><span data-stu-id="e4028-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="e4028-107">描述輸出的色彩設定特性。</span><span class="sxs-lookup"><span data-stu-id="e4028-107">Describes the characteristics of the color settings for the output.</span></span>

-   [<span data-ttu-id="e4028-108">項目資訊</span><span class="sxs-lookup"><span data-stu-id="e4028-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="e4028-109">結構化內容</span><span class="sxs-lookup"><span data-stu-id="e4028-109">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="e4028-110">可延伸標記語言 (XML)  (XML) 內容</span><span class="sxs-lookup"><span data-stu-id="e4028-110">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="e4028-111">項目資訊</span><span class="sxs-lookup"><span data-stu-id="e4028-111">Element Information</span></span>



| <span data-ttu-id="e4028-112">Name</span><span class="sxs-lookup"><span data-stu-id="e4028-112">Name</span></span>                       |                    |
|----------------------------|--------------------|
| <span data-ttu-id="e4028-113">項目類型</span><span class="sxs-lookup"><span data-stu-id="e4028-113">Element Type</span></span> <br/>   | <span data-ttu-id="e4028-114">功能</span><span class="sxs-lookup"><span data-stu-id="e4028-114">Feature</span></span><br/> |
| <span data-ttu-id="e4028-115">範圍前置詞</span><span class="sxs-lookup"><span data-stu-id="e4028-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="e4028-116">頁面</span><span class="sxs-lookup"><span data-stu-id="e4028-116">Page</span></span><br/>    |
| <span data-ttu-id="e4028-117">注意</span><span class="sxs-lookup"><span data-stu-id="e4028-117">Notes</span></span> <br/>          | <span data-ttu-id="e4028-118">None</span><span class="sxs-lookup"><span data-stu-id="e4028-118">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="e4028-119">結構化內容</span><span class="sxs-lookup"><span data-stu-id="e4028-119">Structural Content</span></span>

<span data-ttu-id="e4028-120">此元素的 XML 結構為：</span><span class="sxs-lookup"><span data-stu-id="e4028-120">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="e4028-121">結構變數</span><span class="sxs-lookup"><span data-stu-id="e4028-121">Structure Variables</span></span>

<span data-ttu-id="e4028-122">下表概述 XML 結構中所定義之變數的特性。</span><span class="sxs-lookup"><span data-stu-id="e4028-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="e4028-123">Name</span><span class="sxs-lookup"><span data-stu-id="e4028-123">Name</span></span>                                   | <span data-ttu-id="e4028-124">資料類型</span><span class="sxs-lookup"><span data-stu-id="e4028-124">Data type</span></span>          | <span data-ttu-id="e4028-125">單位</span><span class="sxs-lookup"><span data-stu-id="e4028-125">Unit</span></span>                      | <span data-ttu-id="e4028-126">支援的值</span><span class="sxs-lookup"><span data-stu-id="e4028-126">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="e4028-127">總結</span><span class="sxs-lookup"><span data-stu-id="e4028-127">Summary</span></span>                                                                                                                           |
|----------------------------------------|--------------------|---------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e4028-128">\_選項名稱\_</span><span class="sxs-lookup"><span data-stu-id="e4028-128">\_OptionName\_</span></span><br/>              | <span data-ttu-id="e4028-129">字串</span><span class="sxs-lookup"><span data-stu-id="e4028-129">string</span></span><br/>  | <span data-ttu-id="e4028-130">字元</span><span class="sxs-lookup"><span data-stu-id="e4028-130">characters</span></span><br/>     | <span data-ttu-id="e4028-131">以 [XML 命名空間](https://www.w3.org/TR/1999/REC-xml-names-19990114/)所定義的有效完整名稱。</span><span class="sxs-lookup"><span data-stu-id="e4028-131">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="e4028-132">如果未指定命名空間，則會假設為預設命名空間。</span><span class="sxs-lookup"><span data-stu-id="e4028-132">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="e4028-133">選項的名稱。</span><span class="sxs-lookup"><span data-stu-id="e4028-133">The name of the option.</span></span><br/>                                                                                                |
| <span data-ttu-id="e4028-134">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="e4028-134">\_IdentityOptionValue\_</span></span><br/>     | <span data-ttu-id="e4028-135">字串</span><span class="sxs-lookup"><span data-stu-id="e4028-135">string</span></span><br/>  | <span data-ttu-id="e4028-136">n/a</span><span class="sxs-lookup"><span data-stu-id="e4028-136">n/a</span></span><br/>            | <span data-ttu-id="e4028-137">True、False。</span><span class="sxs-lookup"><span data-stu-id="e4028-137">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="e4028-138">定義選項，當選取此選項時，會停用此功能。</span><span class="sxs-lookup"><span data-stu-id="e4028-138">Defines an Option which when selected would disable this feature.</span></span><br/>                                                      |
| <span data-ttu-id="e4028-139">\_DeviceBitsPerPixelValue\_</span><span class="sxs-lookup"><span data-stu-id="e4028-139">\_DeviceBitsPerPixelValue\_</span></span><br/> | <span data-ttu-id="e4028-140">整數</span><span class="sxs-lookup"><span data-stu-id="e4028-140">integer</span></span><br/> | <span data-ttu-id="e4028-141">每圖元的位數</span><span class="sxs-lookup"><span data-stu-id="e4028-141">bits per pixel</span></span><br/> | <span data-ttu-id="e4028-142">大於0，小於裝置支援值上限。</span><span class="sxs-lookup"><span data-stu-id="e4028-142">Greater than 0, less than maximum device support value.</span></span><br/>                                                                                                                    | <span data-ttu-id="e4028-143">數值，指出印表機所支援之色彩資料的每一像素位元數。</span><span class="sxs-lookup"><span data-stu-id="e4028-143">Numeric value indicating the number of bits per pixel of color data supported by the printer.</span></span><br/>                          |
| <span data-ttu-id="e4028-144">\_DriverBitsPerPixelValue\_</span><span class="sxs-lookup"><span data-stu-id="e4028-144">\_DriverBitsPerPixelValue\_</span></span><br/> | <span data-ttu-id="e4028-145">整數</span><span class="sxs-lookup"><span data-stu-id="e4028-145">integer</span></span><br/> | <span data-ttu-id="e4028-146">每圖元的位數</span><span class="sxs-lookup"><span data-stu-id="e4028-146">bits per pixel</span></span><br/> | <span data-ttu-id="e4028-147">大於0，小於裝置支援值上限。</span><span class="sxs-lookup"><span data-stu-id="e4028-147">Greater than 0, less than maximum device support value.</span></span><br/>                                                                                                                    | <span data-ttu-id="e4028-148">數值，表示核心驅動程式應針對其點陣圖轉譯緩衝區使用的每一像素位元數。</span><span class="sxs-lookup"><span data-stu-id="e4028-148">Numeric value indicating the number of bits per pixel that the core driver should use for its bitmap rendering buffer.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="e4028-149">可延伸標記語言 (XML)  (XML) 內容</span><span class="sxs-lookup"><span data-stu-id="e4028-149">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="e4028-150">公用列印架構關鍵字是在 https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords 命名空間中定義。</span><span class="sxs-lookup"><span data-stu-id="e4028-150">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="e4028-151">此關鍵字的 public 可延伸標記語言 (XML)  (XML) 內容定義如下：</span><span class="sxs-lookup"><span data-stu-id="e4028-151">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="e4028-152">相關主題</span><span class="sxs-lookup"><span data-stu-id="e4028-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e4028-153">列印架構規格</span><span class="sxs-lookup"><span data-stu-id="e4028-153">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




