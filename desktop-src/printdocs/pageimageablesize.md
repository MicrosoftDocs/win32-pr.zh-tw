---
description: 深入瞭解 PageImageableSize 使用者可設定的元素。 本主題並非最新的。 如需最新資訊，請參閱列印架構規格。
ms.assetid: 6b81814f-2d9e-4862-8633-6ba016c11dac
title: PageImageableSize
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee4e44bc9afe33b87d32b43c93eafc3b6d4ba4b0
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/19/2021
ms.locfileid: "112395303"
---
# <a name="pageimageablesize"></a><span data-ttu-id="2d242-105">PageImageableSize</span><span class="sxs-lookup"><span data-stu-id="2d242-105">PageImageableSize</span></span>

<span data-ttu-id="2d242-106">本主題並非最新的。</span><span class="sxs-lookup"><span data-stu-id="2d242-106">This topic is not current.</span></span> <span data-ttu-id="2d242-107">如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。</span><span class="sxs-lookup"><span data-stu-id="2d242-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="2d242-108">描述版面配置和轉譯的映射畫布。</span><span class="sxs-lookup"><span data-stu-id="2d242-108">Describes the imaged canvas for layout and rendering.</span></span> <span data-ttu-id="2d242-109">這會根據 PageMediaSize 和 PageOrientation 報告。</span><span class="sxs-lookup"><span data-stu-id="2d242-109">This will be reported based on PageMediaSize and PageOrientation.</span></span>

<span data-ttu-id="2d242-110">下圖說明以 PageOrientation 為基礎的 PageImageableSize 變數用法。</span><span class="sxs-lookup"><span data-stu-id="2d242-110">The following diagrams illustrate the PageImageableSize variables usage based on PageOrientation.</span></span>

![顯示頁面度量的圖表](images/local-1641910626-image.png)

-   [<span data-ttu-id="2d242-112">項目資訊</span><span class="sxs-lookup"><span data-stu-id="2d242-112">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="2d242-113">結構化內容</span><span class="sxs-lookup"><span data-stu-id="2d242-113">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="2d242-114">可延伸標記語言 (XML)  (XML) 內容</span><span class="sxs-lookup"><span data-stu-id="2d242-114">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="2d242-115">項目資訊</span><span class="sxs-lookup"><span data-stu-id="2d242-115">Element Information</span></span>

| <span data-ttu-id="2d242-116">Name</span><span class="sxs-lookup"><span data-stu-id="2d242-116">Name</span></span>                 | <span data-ttu-id="2d242-117">值</span><span class="sxs-lookup"><span data-stu-id="2d242-117">Value</span></span>         |
|----------------------|---------------|
| <span data-ttu-id="2d242-118">項目類型</span><span class="sxs-lookup"><span data-stu-id="2d242-118">Element Type</span></span><br/>    | <span data-ttu-id="2d242-119">屬性</span><span class="sxs-lookup"><span data-stu-id="2d242-119">Property</span></span><br/> |
| <span data-ttu-id="2d242-120">範圍前置詞</span><span class="sxs-lookup"><span data-stu-id="2d242-120">Scoping Prefix</span></span> <br/> | <span data-ttu-id="2d242-121">頁面</span><span class="sxs-lookup"><span data-stu-id="2d242-121">Page</span></span><br/>     |
| <span data-ttu-id="2d242-122">注意</span><span class="sxs-lookup"><span data-stu-id="2d242-122">Notes</span></span> <br/>          | <span data-ttu-id="2d242-123">None</span><span class="sxs-lookup"><span data-stu-id="2d242-123">None</span></span><br/>     |

## <a name="structural-content"></a><span data-ttu-id="2d242-124">結構化內容</span><span class="sxs-lookup"><span data-stu-id="2d242-124">Structural Content</span></span>

<span data-ttu-id="2d242-125">此元素的 XML 結構為：</span><span class="sxs-lookup"><span data-stu-id="2d242-125">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="2d242-126">結構變數</span><span class="sxs-lookup"><span data-stu-id="2d242-126">Structure Variables</span></span>

<span data-ttu-id="2d242-127">下表概述 XML 結構中所定義之變數的特性。</span><span class="sxs-lookup"><span data-stu-id="2d242-127">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="2d242-128">Name</span><span class="sxs-lookup"><span data-stu-id="2d242-128">Name</span></span>                                    | <span data-ttu-id="2d242-129">資料類型</span><span class="sxs-lookup"><span data-stu-id="2d242-129">Data type</span></span>          | <span data-ttu-id="2d242-130">單位</span><span class="sxs-lookup"><span data-stu-id="2d242-130">Unit</span></span>               | <span data-ttu-id="2d242-131">支援的值</span><span class="sxs-lookup"><span data-stu-id="2d242-131">Supported values</span></span>                       | <span data-ttu-id="2d242-132">總結</span><span class="sxs-lookup"><span data-stu-id="2d242-132">Summary</span></span>                                                                                                                    |
|-----------------------------------------|--------------------|--------------------|----------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2d242-133">\_ImageableSizeWidthValue\_</span><span class="sxs-lookup"><span data-stu-id="2d242-133">\_ImageableSizeWidthValue\_</span></span><br/>  | <span data-ttu-id="2d242-134">整數</span><span class="sxs-lookup"><span data-stu-id="2d242-134">integer</span></span><br/> | <span data-ttu-id="2d242-135">微米</span><span class="sxs-lookup"><span data-stu-id="2d242-135">microns</span></span><br/> | <span data-ttu-id="2d242-136">大於 0。</span><span class="sxs-lookup"><span data-stu-id="2d242-136">Greater than 0.</span></span><br/>             | <span data-ttu-id="2d242-137">指定相對於 PageOrientation 之應用程式媒體大小的水準維度。</span><span class="sxs-lookup"><span data-stu-id="2d242-137">Specifies the horizontal dimension of the application media size relative to the PageOrientation.</span></span><br/>               |
| <span data-ttu-id="2d242-138">\_ImageableSizeHeightValue\_</span><span class="sxs-lookup"><span data-stu-id="2d242-138">\_ImageableSizeHeightValue\_</span></span><br/> | <span data-ttu-id="2d242-139">整數</span><span class="sxs-lookup"><span data-stu-id="2d242-139">integer</span></span><br/> | <span data-ttu-id="2d242-140">微米</span><span class="sxs-lookup"><span data-stu-id="2d242-140">microns</span></span><br/> | <span data-ttu-id="2d242-141">大於 0。</span><span class="sxs-lookup"><span data-stu-id="2d242-141">Greater than 0.</span></span><br/>             | <span data-ttu-id="2d242-142">指定相對於 PageOrientation 的應用程式媒體大小垂直維度。</span><span class="sxs-lookup"><span data-stu-id="2d242-142">Specifies the vertical dimension of the application media size relative to the PageOrientation.</span></span><br/>                 |
| <span data-ttu-id="2d242-143">\_OriginWidthValue\_</span><span class="sxs-lookup"><span data-stu-id="2d242-143">\_OriginWidthValue\_</span></span><br/>         | <span data-ttu-id="2d242-144">整數</span><span class="sxs-lookup"><span data-stu-id="2d242-144">integer</span></span><br/> | <span data-ttu-id="2d242-145">微米</span><span class="sxs-lookup"><span data-stu-id="2d242-145">microns</span></span><br/> | <span data-ttu-id="2d242-146">大於或等於0。</span><span class="sxs-lookup"><span data-stu-id="2d242-146">Greater than or equal to 0.</span></span><br/> | <span data-ttu-id="2d242-147">指定相對於應用程式媒體大小的成像區域水準原點。</span><span class="sxs-lookup"><span data-stu-id="2d242-147">Specifies the horizontal origin of the imageable area relative to the application media size.</span></span><br/>                   |
| <span data-ttu-id="2d242-148">\_OriginHeightValue\_</span><span class="sxs-lookup"><span data-stu-id="2d242-148">\_OriginHeightValue\_</span></span><br/>        | <span data-ttu-id="2d242-149">整數</span><span class="sxs-lookup"><span data-stu-id="2d242-149">integer</span></span><br/> | <span data-ttu-id="2d242-150">微米</span><span class="sxs-lookup"><span data-stu-id="2d242-150">microns</span></span><br/> | <span data-ttu-id="2d242-151">大於或等於0。</span><span class="sxs-lookup"><span data-stu-id="2d242-151">Greater than or equal to 0.</span></span><br/> | <span data-ttu-id="2d242-152">指定相對於應用程式媒體大小的成像區域垂直來源。</span><span class="sxs-lookup"><span data-stu-id="2d242-152">Specifies the vertical origin of the imageable area relative to the application media size.</span></span><br/>                     |
| <span data-ttu-id="2d242-153">\_ExtentWidthValue\_</span><span class="sxs-lookup"><span data-stu-id="2d242-153">\_ExtentWidthValue\_</span></span><br/>         | <span data-ttu-id="2d242-154">整數</span><span class="sxs-lookup"><span data-stu-id="2d242-154">integer</span></span><br/> | <span data-ttu-id="2d242-155">微米</span><span class="sxs-lookup"><span data-stu-id="2d242-155">microns</span></span><br/> | <span data-ttu-id="2d242-156">大於 0。</span><span class="sxs-lookup"><span data-stu-id="2d242-156">Greater than 0.</span></span><br/>             | <span data-ttu-id="2d242-157">指定應用程式媒體大小的原點和周框限制之間的水準距離。</span><span class="sxs-lookup"><span data-stu-id="2d242-157">Specifies the horizontal distance between the origin and the bounding limit of the application media size.</span></span><br/>      |
| <span data-ttu-id="2d242-158">\_ExtentHeightValue\_</span><span class="sxs-lookup"><span data-stu-id="2d242-158">\_ExtentHeightValue\_</span></span><br/>        | <span data-ttu-id="2d242-159">整數</span><span class="sxs-lookup"><span data-stu-id="2d242-159">integer</span></span><br/> | <span data-ttu-id="2d242-160">微米</span><span class="sxs-lookup"><span data-stu-id="2d242-160">microns</span></span><br/> | <span data-ttu-id="2d242-161">大於 0。</span><span class="sxs-lookup"><span data-stu-id="2d242-161">Greater than 0.</span></span><br/>             | <span data-ttu-id="2d242-162">指定畫布應用程式媒體大小的原點和周框限制之間的垂直距離。</span><span class="sxs-lookup"><span data-stu-id="2d242-162">Specifies the vertical distance between the origin and the bounding limit of the canvas application media size.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="2d242-163">可延伸標記語言 (XML)  (XML) 內容</span><span class="sxs-lookup"><span data-stu-id="2d242-163">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="2d242-164">公用列印架構關鍵字是在 https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords 命名空間中定義。</span><span class="sxs-lookup"><span data-stu-id="2d242-164">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="2d242-165">此關鍵字的 public 可延伸標記語言 (XML)  (XML) 內容定義如下：</span><span class="sxs-lookup"><span data-stu-id="2d242-165">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="2d242-166">相關主題</span><span class="sxs-lookup"><span data-stu-id="2d242-166">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2d242-167">列印架構規格</span><span class="sxs-lookup"><span data-stu-id="2d242-167">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




