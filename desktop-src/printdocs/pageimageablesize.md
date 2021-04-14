---
description: 本主題並非最新的。 如需最新資訊，請參閱列印架構規格。
ms.assetid: 6b81814f-2d9e-4862-8633-6ba016c11dac
title: PageImageableSize
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26dca243defc08b43a79e897bfa91913a954bf37
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/06/2021
ms.locfileid: "104552636"
---
# <a name="pageimageablesize"></a><span data-ttu-id="782a8-104">PageImageableSize</span><span class="sxs-lookup"><span data-stu-id="782a8-104">PageImageableSize</span></span>

<span data-ttu-id="782a8-105">本主題並非最新的。</span><span class="sxs-lookup"><span data-stu-id="782a8-105">This topic is not current.</span></span> <span data-ttu-id="782a8-106">如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。</span><span class="sxs-lookup"><span data-stu-id="782a8-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="782a8-107">描述版面配置和轉譯的映射畫布。</span><span class="sxs-lookup"><span data-stu-id="782a8-107">Describes the imaged canvas for layout and rendering.</span></span> <span data-ttu-id="782a8-108">這會根據 PageMediaSize 和 PageOrientation 報告。</span><span class="sxs-lookup"><span data-stu-id="782a8-108">This will be reported based on PageMediaSize and PageOrientation.</span></span>

<span data-ttu-id="782a8-109">下圖說明以 PageOrientation 為基礎的 PageImageableSize 變數用法。</span><span class="sxs-lookup"><span data-stu-id="782a8-109">The following diagrams illustrate the PageImageableSize variables usage based on PageOrientation.</span></span>

![顯示頁面度量的圖表](images/local-1641910626-image.png)

-   [<span data-ttu-id="782a8-111">項目資訊</span><span class="sxs-lookup"><span data-stu-id="782a8-111">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="782a8-112">結構化內容</span><span class="sxs-lookup"><span data-stu-id="782a8-112">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="782a8-113">可延伸標記語言 (XML)  (XML) 內容</span><span class="sxs-lookup"><span data-stu-id="782a8-113">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="782a8-114">項目資訊</span><span class="sxs-lookup"><span data-stu-id="782a8-114">Element Information</span></span>



|                            |                     |
|----------------------------|---------------------|
| <span data-ttu-id="782a8-115">Name</span><span class="sxs-lookup"><span data-stu-id="782a8-115">Name</span></span>                       |                     |
| <span data-ttu-id="782a8-116">項目類型</span><span class="sxs-lookup"><span data-stu-id="782a8-116">Element Type</span></span><br/>    | <span data-ttu-id="782a8-117">屬性</span><span class="sxs-lookup"><span data-stu-id="782a8-117">Property</span></span><br/> |
| <span data-ttu-id="782a8-118">範圍前置詞</span><span class="sxs-lookup"><span data-stu-id="782a8-118">Scoping Prefix</span></span> <br/> | <span data-ttu-id="782a8-119">頁面</span><span class="sxs-lookup"><span data-stu-id="782a8-119">Page</span></span><br/>     |
| <span data-ttu-id="782a8-120">注意</span><span class="sxs-lookup"><span data-stu-id="782a8-120">Notes</span></span> <br/>          | <span data-ttu-id="782a8-121">None</span><span class="sxs-lookup"><span data-stu-id="782a8-121">None</span></span><br/>     |



 

## <a name="structural-content"></a><span data-ttu-id="782a8-122">結構化內容</span><span class="sxs-lookup"><span data-stu-id="782a8-122">Structural Content</span></span>

<span data-ttu-id="782a8-123">此元素的 XML 結構為：</span><span class="sxs-lookup"><span data-stu-id="782a8-123">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="782a8-124">結構變數</span><span class="sxs-lookup"><span data-stu-id="782a8-124">Structure Variables</span></span>

<span data-ttu-id="782a8-125">下表概述 XML 結構中所定義之變數的特性。</span><span class="sxs-lookup"><span data-stu-id="782a8-125">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="782a8-126">Name</span><span class="sxs-lookup"><span data-stu-id="782a8-126">Name</span></span>                                    | <span data-ttu-id="782a8-127">資料類型</span><span class="sxs-lookup"><span data-stu-id="782a8-127">Data type</span></span>          | <span data-ttu-id="782a8-128">單位</span><span class="sxs-lookup"><span data-stu-id="782a8-128">Unit</span></span>               | <span data-ttu-id="782a8-129">支援的值</span><span class="sxs-lookup"><span data-stu-id="782a8-129">Supported values</span></span>                       | <span data-ttu-id="782a8-130">總結</span><span class="sxs-lookup"><span data-stu-id="782a8-130">Summary</span></span>                                                                                                                    |
|-----------------------------------------|--------------------|--------------------|----------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="782a8-131">\_ImageableSizeWidthValue\_</span><span class="sxs-lookup"><span data-stu-id="782a8-131">\_ImageableSizeWidthValue\_</span></span><br/>  | <span data-ttu-id="782a8-132">整數</span><span class="sxs-lookup"><span data-stu-id="782a8-132">integer</span></span><br/> | <span data-ttu-id="782a8-133">微米</span><span class="sxs-lookup"><span data-stu-id="782a8-133">microns</span></span><br/> | <span data-ttu-id="782a8-134">大於 0。</span><span class="sxs-lookup"><span data-stu-id="782a8-134">Greater than 0.</span></span><br/>             | <span data-ttu-id="782a8-135">指定相對於 PageOrientation 之應用程式媒體大小的水準維度。</span><span class="sxs-lookup"><span data-stu-id="782a8-135">Specifies the horizontal dimension of the application media size relative to the PageOrientation.</span></span><br/>               |
| <span data-ttu-id="782a8-136">\_ImageableSizeHeightValue\_</span><span class="sxs-lookup"><span data-stu-id="782a8-136">\_ImageableSizeHeightValue\_</span></span><br/> | <span data-ttu-id="782a8-137">整數</span><span class="sxs-lookup"><span data-stu-id="782a8-137">integer</span></span><br/> | <span data-ttu-id="782a8-138">微米</span><span class="sxs-lookup"><span data-stu-id="782a8-138">microns</span></span><br/> | <span data-ttu-id="782a8-139">大於 0。</span><span class="sxs-lookup"><span data-stu-id="782a8-139">Greater than 0.</span></span><br/>             | <span data-ttu-id="782a8-140">指定相對於 PageOrientation 的應用程式媒體大小垂直維度。</span><span class="sxs-lookup"><span data-stu-id="782a8-140">Specifies the vertical dimension of the application media size relative to the PageOrientation.</span></span><br/>                 |
| <span data-ttu-id="782a8-141">\_OriginWidthValue\_</span><span class="sxs-lookup"><span data-stu-id="782a8-141">\_OriginWidthValue\_</span></span><br/>         | <span data-ttu-id="782a8-142">整數</span><span class="sxs-lookup"><span data-stu-id="782a8-142">integer</span></span><br/> | <span data-ttu-id="782a8-143">微米</span><span class="sxs-lookup"><span data-stu-id="782a8-143">microns</span></span><br/> | <span data-ttu-id="782a8-144">大於或等於0。</span><span class="sxs-lookup"><span data-stu-id="782a8-144">Greater than or equal to 0.</span></span><br/> | <span data-ttu-id="782a8-145">指定相對於應用程式媒體大小的成像區域水準原點。</span><span class="sxs-lookup"><span data-stu-id="782a8-145">Specifies the horizontal origin of the imageable area relative to the application media size.</span></span><br/>                   |
| <span data-ttu-id="782a8-146">\_OriginHeightValue\_</span><span class="sxs-lookup"><span data-stu-id="782a8-146">\_OriginHeightValue\_</span></span><br/>        | <span data-ttu-id="782a8-147">整數</span><span class="sxs-lookup"><span data-stu-id="782a8-147">integer</span></span><br/> | <span data-ttu-id="782a8-148">微米</span><span class="sxs-lookup"><span data-stu-id="782a8-148">microns</span></span><br/> | <span data-ttu-id="782a8-149">大於或等於0。</span><span class="sxs-lookup"><span data-stu-id="782a8-149">Greater than or equal to 0.</span></span><br/> | <span data-ttu-id="782a8-150">指定相對於應用程式媒體大小的成像區域垂直來源。</span><span class="sxs-lookup"><span data-stu-id="782a8-150">Specifies the vertical origin of the imageable area relative to the application media size.</span></span><br/>                     |
| <span data-ttu-id="782a8-151">\_ExtentWidthValue\_</span><span class="sxs-lookup"><span data-stu-id="782a8-151">\_ExtentWidthValue\_</span></span><br/>         | <span data-ttu-id="782a8-152">整數</span><span class="sxs-lookup"><span data-stu-id="782a8-152">integer</span></span><br/> | <span data-ttu-id="782a8-153">微米</span><span class="sxs-lookup"><span data-stu-id="782a8-153">microns</span></span><br/> | <span data-ttu-id="782a8-154">大於 0。</span><span class="sxs-lookup"><span data-stu-id="782a8-154">Greater than 0.</span></span><br/>             | <span data-ttu-id="782a8-155">指定應用程式媒體大小的原點和周框限制之間的水準距離。</span><span class="sxs-lookup"><span data-stu-id="782a8-155">Specifies the horizontal distance between the origin and the bounding limit of the application media size.</span></span><br/>      |
| <span data-ttu-id="782a8-156">\_ExtentHeightValue\_</span><span class="sxs-lookup"><span data-stu-id="782a8-156">\_ExtentHeightValue\_</span></span><br/>        | <span data-ttu-id="782a8-157">整數</span><span class="sxs-lookup"><span data-stu-id="782a8-157">integer</span></span><br/> | <span data-ttu-id="782a8-158">微米</span><span class="sxs-lookup"><span data-stu-id="782a8-158">microns</span></span><br/> | <span data-ttu-id="782a8-159">大於 0。</span><span class="sxs-lookup"><span data-stu-id="782a8-159">Greater than 0.</span></span><br/>             | <span data-ttu-id="782a8-160">指定畫布應用程式媒體大小的原點和周框限制之間的垂直距離。</span><span class="sxs-lookup"><span data-stu-id="782a8-160">Specifies the vertical distance between the origin and the bounding limit of the canvas application media size.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="782a8-161">可延伸標記語言 (XML)  (XML) 內容</span><span class="sxs-lookup"><span data-stu-id="782a8-161">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="782a8-162">公用列印架構關鍵字是在 https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords 命名空間中定義。</span><span class="sxs-lookup"><span data-stu-id="782a8-162">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="782a8-163">此關鍵字的 public 可延伸標記語言 (XML)  (XML) 內容定義如下：</span><span class="sxs-lookup"><span data-stu-id="782a8-163">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="782a8-164">相關主題</span><span class="sxs-lookup"><span data-stu-id="782a8-164">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="782a8-165">列印架構規格</span><span class="sxs-lookup"><span data-stu-id="782a8-165">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




