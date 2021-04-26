---
description: 本主題並非最新的。 如需最新資訊，請參閱列印架構規格。
ms.assetid: 6b81814f-2d9e-4862-8633-6ba016c11dac
title: PageImageableSize
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1eef9012a7fda3eed6afd16add1d483c35c1111
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/26/2021
ms.locfileid: "107996105"
---
# <a name="pageimageablesize"></a><span data-ttu-id="23ada-104">PageImageableSize</span><span class="sxs-lookup"><span data-stu-id="23ada-104">PageImageableSize</span></span>

<span data-ttu-id="23ada-105">本主題並非最新的。</span><span class="sxs-lookup"><span data-stu-id="23ada-105">This topic is not current.</span></span> <span data-ttu-id="23ada-106">如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。</span><span class="sxs-lookup"><span data-stu-id="23ada-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="23ada-107">描述版面配置和轉譯的映射畫布。</span><span class="sxs-lookup"><span data-stu-id="23ada-107">Describes the imaged canvas for layout and rendering.</span></span> <span data-ttu-id="23ada-108">這會根據 PageMediaSize 和 PageOrientation 報告。</span><span class="sxs-lookup"><span data-stu-id="23ada-108">This will be reported based on PageMediaSize and PageOrientation.</span></span>

<span data-ttu-id="23ada-109">下圖說明以 PageOrientation 為基礎的 PageImageableSize 變數用法。</span><span class="sxs-lookup"><span data-stu-id="23ada-109">The following diagrams illustrate the PageImageableSize variables usage based on PageOrientation.</span></span>

![顯示頁面度量的圖表](images/local-1641910626-image.png)

-   [<span data-ttu-id="23ada-111">項目資訊</span><span class="sxs-lookup"><span data-stu-id="23ada-111">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="23ada-112">結構化內容</span><span class="sxs-lookup"><span data-stu-id="23ada-112">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="23ada-113">可延伸標記語言 (XML)  (XML) 內容</span><span class="sxs-lookup"><span data-stu-id="23ada-113">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="23ada-114">項目資訊</span><span class="sxs-lookup"><span data-stu-id="23ada-114">Element Information</span></span>



|                            |                     |
|----------------------------|---------------------|
| <span data-ttu-id="23ada-115">Name</span><span class="sxs-lookup"><span data-stu-id="23ada-115">Name</span></span> | <span data-ttu-id="23ada-116">值</span><span class="sxs-lookup"><span data-stu-id="23ada-116">Value</span></span> |
| <span data-ttu-id="23ada-117">項目類型</span><span class="sxs-lookup"><span data-stu-id="23ada-117">Element Type</span></span><br/>    | <span data-ttu-id="23ada-118">屬性</span><span class="sxs-lookup"><span data-stu-id="23ada-118">Property</span></span><br/> |
| <span data-ttu-id="23ada-119">範圍前置詞</span><span class="sxs-lookup"><span data-stu-id="23ada-119">Scoping Prefix</span></span> <br/> | <span data-ttu-id="23ada-120">頁面</span><span class="sxs-lookup"><span data-stu-id="23ada-120">Page</span></span><br/>     |
| <span data-ttu-id="23ada-121">注意</span><span class="sxs-lookup"><span data-stu-id="23ada-121">Notes</span></span> <br/>          | <span data-ttu-id="23ada-122">None</span><span class="sxs-lookup"><span data-stu-id="23ada-122">None</span></span><br/>     |



 

## <a name="structural-content"></a><span data-ttu-id="23ada-123">結構化內容</span><span class="sxs-lookup"><span data-stu-id="23ada-123">Structural Content</span></span>

<span data-ttu-id="23ada-124">此元素的 XML 結構為：</span><span class="sxs-lookup"><span data-stu-id="23ada-124">The XML structure of this element is:</span></span>

``` syntax
<psf:Property name="psk:PageImageableSize">
  <psf:Property name="psk:ImageableSizeWidth">
    <psf:Value xsi:type="xs:integer">_ImageableSizeWidthValue_</psf:Value>
  </psf:Property>
  <psf:Property name="psk:ImageableSizeHeight">
    <psf:Value xsi:type="xs:integer">_ImageableSizeHeightValue_</psf:Value>
  </psf:Property>
  <!--Specifies the imageable area within the logical page.  -->
  <psf:Property name="psk:ImageableArea">
    <psf:Property name="psk:OriginWidth">
      <psf:Value xsi:type="xs:integer">_OriginWidthValue_</psf:Value>
    </psf:Property>
    <psf:Property name="psk:OriginHeight">
      <psf:Value xsi:type="xs:integer">_OriginHeightValue_</psf:Value>
    </psf:Property>
    <psf:Property name="psk:ExtentWidth">
      <psf:Value xsi:type="xs:integer">_ExtentWidthValue_</psf:Value>
    </psf:Property>
    <psf:Property name="psk:ExtentHeight">
      <psf:Value xsi:type="xs:integer">_ExtentHeightValue_</psf:Value>
    </psf:Property>
  </psf:Property>
</psf:Property>
```

## <a name="structure-variables"></a><span data-ttu-id="23ada-125">結構變數</span><span class="sxs-lookup"><span data-stu-id="23ada-125">Structure Variables</span></span>

<span data-ttu-id="23ada-126">下表概述 XML 結構中所定義之變數的特性。</span><span class="sxs-lookup"><span data-stu-id="23ada-126">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="23ada-127">Name</span><span class="sxs-lookup"><span data-stu-id="23ada-127">Name</span></span>                                    | <span data-ttu-id="23ada-128">資料類型</span><span class="sxs-lookup"><span data-stu-id="23ada-128">Data type</span></span>          | <span data-ttu-id="23ada-129">單位</span><span class="sxs-lookup"><span data-stu-id="23ada-129">Unit</span></span>               | <span data-ttu-id="23ada-130">支援的值</span><span class="sxs-lookup"><span data-stu-id="23ada-130">Supported values</span></span>                       | <span data-ttu-id="23ada-131">總結</span><span class="sxs-lookup"><span data-stu-id="23ada-131">Summary</span></span>                                                                                                                    |
|-----------------------------------------|--------------------|--------------------|----------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="23ada-132">\_ImageableSizeWidthValue\_</span><span class="sxs-lookup"><span data-stu-id="23ada-132">\_ImageableSizeWidthValue\_</span></span><br/>  | <span data-ttu-id="23ada-133">整數</span><span class="sxs-lookup"><span data-stu-id="23ada-133">integer</span></span><br/> | <span data-ttu-id="23ada-134">微米</span><span class="sxs-lookup"><span data-stu-id="23ada-134">microns</span></span><br/> | <span data-ttu-id="23ada-135">大於 0。</span><span class="sxs-lookup"><span data-stu-id="23ada-135">Greater than 0.</span></span><br/>             | <span data-ttu-id="23ada-136">指定相對於 PageOrientation 之應用程式媒體大小的水準維度。</span><span class="sxs-lookup"><span data-stu-id="23ada-136">Specifies the horizontal dimension of the application media size relative to the PageOrientation.</span></span><br/>               |
| <span data-ttu-id="23ada-137">\_ImageableSizeHeightValue\_</span><span class="sxs-lookup"><span data-stu-id="23ada-137">\_ImageableSizeHeightValue\_</span></span><br/> | <span data-ttu-id="23ada-138">整數</span><span class="sxs-lookup"><span data-stu-id="23ada-138">integer</span></span><br/> | <span data-ttu-id="23ada-139">微米</span><span class="sxs-lookup"><span data-stu-id="23ada-139">microns</span></span><br/> | <span data-ttu-id="23ada-140">大於 0。</span><span class="sxs-lookup"><span data-stu-id="23ada-140">Greater than 0.</span></span><br/>             | <span data-ttu-id="23ada-141">指定相對於 PageOrientation 的應用程式媒體大小垂直維度。</span><span class="sxs-lookup"><span data-stu-id="23ada-141">Specifies the vertical dimension of the application media size relative to the PageOrientation.</span></span><br/>                 |
| <span data-ttu-id="23ada-142">\_OriginWidthValue\_</span><span class="sxs-lookup"><span data-stu-id="23ada-142">\_OriginWidthValue\_</span></span><br/>         | <span data-ttu-id="23ada-143">整數</span><span class="sxs-lookup"><span data-stu-id="23ada-143">integer</span></span><br/> | <span data-ttu-id="23ada-144">微米</span><span class="sxs-lookup"><span data-stu-id="23ada-144">microns</span></span><br/> | <span data-ttu-id="23ada-145">大於或等於0。</span><span class="sxs-lookup"><span data-stu-id="23ada-145">Greater than or equal to 0.</span></span><br/> | <span data-ttu-id="23ada-146">指定相對於應用程式媒體大小的成像區域水準原點。</span><span class="sxs-lookup"><span data-stu-id="23ada-146">Specifies the horizontal origin of the imageable area relative to the application media size.</span></span><br/>                   |
| <span data-ttu-id="23ada-147">\_OriginHeightValue\_</span><span class="sxs-lookup"><span data-stu-id="23ada-147">\_OriginHeightValue\_</span></span><br/>        | <span data-ttu-id="23ada-148">整數</span><span class="sxs-lookup"><span data-stu-id="23ada-148">integer</span></span><br/> | <span data-ttu-id="23ada-149">微米</span><span class="sxs-lookup"><span data-stu-id="23ada-149">microns</span></span><br/> | <span data-ttu-id="23ada-150">大於或等於0。</span><span class="sxs-lookup"><span data-stu-id="23ada-150">Greater than or equal to 0.</span></span><br/> | <span data-ttu-id="23ada-151">指定相對於應用程式媒體大小的成像區域垂直來源。</span><span class="sxs-lookup"><span data-stu-id="23ada-151">Specifies the vertical origin of the imageable area relative to the application media size.</span></span><br/>                     |
| <span data-ttu-id="23ada-152">\_ExtentWidthValue\_</span><span class="sxs-lookup"><span data-stu-id="23ada-152">\_ExtentWidthValue\_</span></span><br/>         | <span data-ttu-id="23ada-153">整數</span><span class="sxs-lookup"><span data-stu-id="23ada-153">integer</span></span><br/> | <span data-ttu-id="23ada-154">微米</span><span class="sxs-lookup"><span data-stu-id="23ada-154">microns</span></span><br/> | <span data-ttu-id="23ada-155">大於 0。</span><span class="sxs-lookup"><span data-stu-id="23ada-155">Greater than 0.</span></span><br/>             | <span data-ttu-id="23ada-156">指定應用程式媒體大小的原點和周框限制之間的水準距離。</span><span class="sxs-lookup"><span data-stu-id="23ada-156">Specifies the horizontal distance between the origin and the bounding limit of the application media size.</span></span><br/>      |
| <span data-ttu-id="23ada-157">\_ExtentHeightValue\_</span><span class="sxs-lookup"><span data-stu-id="23ada-157">\_ExtentHeightValue\_</span></span><br/>        | <span data-ttu-id="23ada-158">整數</span><span class="sxs-lookup"><span data-stu-id="23ada-158">integer</span></span><br/> | <span data-ttu-id="23ada-159">微米</span><span class="sxs-lookup"><span data-stu-id="23ada-159">microns</span></span><br/> | <span data-ttu-id="23ada-160">大於 0。</span><span class="sxs-lookup"><span data-stu-id="23ada-160">Greater than 0.</span></span><br/>             | <span data-ttu-id="23ada-161">指定畫布應用程式媒體大小的原點和周框限制之間的垂直距離。</span><span class="sxs-lookup"><span data-stu-id="23ada-161">Specifies the vertical distance between the origin and the bounding limit of the canvas application media size.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="23ada-162">可延伸標記語言 (XML)  (XML) 內容</span><span class="sxs-lookup"><span data-stu-id="23ada-162">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="23ada-163">公用列印架構關鍵字是在 https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords 命名空間中定義。</span><span class="sxs-lookup"><span data-stu-id="23ada-163">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="23ada-164">此關鍵字的 public 可延伸標記語言 (XML)  (XML) 內容定義如下：</span><span class="sxs-lookup"><span data-stu-id="23ada-164">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Property name="psk:PageImageableSize">
  <psf:Property name="psk:ImageableSizeWidth">
    <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psk:ImageableSizeHeight">
    <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
  </psf:Property>
    <psf:Property name="psk:ImageableArea">
      <psf:Property name="psk:OriginWidth">
        <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
      </psf:Property>
    <psf:Property name="psk:OriginHeight">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:Property>
    <psf:Property name="psk:ExtentWidth">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:Property>
    <psf:Property name="psk:ExtentHeight">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:Property>
  </psf:Property>
</psf:Property>
  
```

## <a name="related-topics"></a><span data-ttu-id="23ada-165">相關主題</span><span class="sxs-lookup"><span data-stu-id="23ada-165">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="23ada-166">列印架構規格</span><span class="sxs-lookup"><span data-stu-id="23ada-166">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




