---
description: 本主題並非最新的。 如需最新資訊，請參閱列印架構規格。
ms.assetid: 941515a8-ba3f-47b9-9f3f-08a48122661a
title: DocumentNUp
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08fdf22fa557ce1da4fde20ad1d8ea14625a1b77
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/06/2021
ms.locfileid: "104195851"
---
# <a name="documentnup"></a><span data-ttu-id="58da4-104">DocumentNUp</span><span class="sxs-lookup"><span data-stu-id="58da4-104">DocumentNUp</span></span>

<span data-ttu-id="58da4-105">本主題並非最新的。</span><span class="sxs-lookup"><span data-stu-id="58da4-105">This topic is not current.</span></span> <span data-ttu-id="58da4-106">如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。</span><span class="sxs-lookup"><span data-stu-id="58da4-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="58da4-107">描述單一實體工作表的多個邏輯頁面的輸出和格式。</span><span class="sxs-lookup"><span data-stu-id="58da4-107">Describes the output and format of multiple logical pages to a single physical sheet.</span></span> <span data-ttu-id="58da4-108">每份檔都是分開編譯的。</span><span class="sxs-lookup"><span data-stu-id="58da4-108">Each document is compiled separately.</span></span> <span data-ttu-id="58da4-109">DocumentNUp 和 JobNUpAllDocumentsContiguously 互斥。</span><span class="sxs-lookup"><span data-stu-id="58da4-109">DocumentNUp and JobNUpAllDocumentsContiguously are mutually exclusive.</span></span> <span data-ttu-id="58da4-110">驅動程式會決定這些關鍵字之間的條件約束處理。</span><span class="sxs-lookup"><span data-stu-id="58da4-110">It is up to the driver to determine constraint handling between these keywords.</span></span>

<span data-ttu-id="58da4-111">下圖說明含有3個頁面的檔1的範例，以及包含2個頁面的檔2。</span><span class="sxs-lookup"><span data-stu-id="58da4-111">The following diagram illustrates an example with Document 1 containing 3 pages, and Document 2 containing 2 pages.</span></span> <span data-ttu-id="58da4-112">每份檔都是分開 duplexed。</span><span class="sxs-lookup"><span data-stu-id="58da4-112">Each document is duplexed separately.</span></span> <span data-ttu-id="58da4-113">以下顯示的呈現方向是 RightBottom 選項。</span><span class="sxs-lookup"><span data-stu-id="58da4-113">The presentation direction shown below is the RightBottom option.</span></span>

![顯示如何根據 documentnup 設定在單一工作表上設定檔頁面面的圖表](images/local-1663869164-docduplex1.gif)

-   [<span data-ttu-id="58da4-115">項目資訊</span><span class="sxs-lookup"><span data-stu-id="58da4-115">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="58da4-116">結構化內容</span><span class="sxs-lookup"><span data-stu-id="58da4-116">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="58da4-117">可延伸標記語言 (XML)  (XML) 內容</span><span class="sxs-lookup"><span data-stu-id="58da4-117">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="58da4-118">項目資訊</span><span class="sxs-lookup"><span data-stu-id="58da4-118">Element Information</span></span>



| <span data-ttu-id="58da4-119">Name</span><span class="sxs-lookup"><span data-stu-id="58da4-119">Name</span></span>                       |                                                                                                                                                 |
|----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="58da4-120">項目類型</span><span class="sxs-lookup"><span data-stu-id="58da4-120">Element Type</span></span> <br/>   | <span data-ttu-id="58da4-121">功能</span><span class="sxs-lookup"><span data-stu-id="58da4-121">Feature</span></span><br/>                                                                                                                              |
| <span data-ttu-id="58da4-122">範圍前置詞</span><span class="sxs-lookup"><span data-stu-id="58da4-122">Scoping Prefix</span></span> <br/> | <span data-ttu-id="58da4-123">文件</span><span class="sxs-lookup"><span data-stu-id="58da4-123">Document</span></span><br/>                                                                                                                             |
| <span data-ttu-id="58da4-124">備註</span><span class="sxs-lookup"><span data-stu-id="58da4-124">Notes</span></span> <br/>          | <span data-ttu-id="58da4-125">頂端、底部、左方和右邊都是相對於 PageImageableSize，其中下拉式功能表是以 X 軸和 y 軸的原點表示。</span><span class="sxs-lookup"><span data-stu-id="58da4-125">Top, Bottom, Left, and Right are relative to the PageImageableSize, where TopLeft is denoted by the origin of the x-axis and y-axis.</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="58da4-126">結構化內容</span><span class="sxs-lookup"><span data-stu-id="58da4-126">Structural Content</span></span>

<span data-ttu-id="58da4-127">此元素的 XML 結構如下所示：</span><span class="sxs-lookup"><span data-stu-id="58da4-127">The XML structure of this element is as follows:</span></span>

``` syntax
<psf:Feature name="psk:DocumentNUp">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option>
    <psf:Property name="psf:IdentityOption">
      <psf:Value xsi:type="xs:string">_IdentityOptionValue_</psf:Value>
    </psf:Property>
    <psf:ScoredProperty name="psk:PagesPerSheet">
      <psf:Value xsi:type="xs:integer">_PagesPerSheetValue_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies the ordering direction of the pages.  First direction followed by second direction. -->
  <psf:Feature name="psk:PresentationDirection">
    <psf:Option name="psk:_PresentationDirectionOptionName_" />
  </psf:Feature>
</psf:Feature>
```

## <a name="structure-variables"></a><span data-ttu-id="58da4-128">結構變數</span><span class="sxs-lookup"><span data-stu-id="58da4-128">Structure Variables</span></span>

<span data-ttu-id="58da4-129">下表概述 XML 結構中所定義之變數的特性。</span><span class="sxs-lookup"><span data-stu-id="58da4-129">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="58da4-130">Name</span><span class="sxs-lookup"><span data-stu-id="58da4-130">Name</span></span>                                           | <span data-ttu-id="58da4-131">資料類型</span><span class="sxs-lookup"><span data-stu-id="58da4-131">Data type</span></span>          | <span data-ttu-id="58da4-132">單位</span><span class="sxs-lookup"><span data-stu-id="58da4-132">Unit</span></span>                     | <span data-ttu-id="58da4-133">支援的值</span><span class="sxs-lookup"><span data-stu-id="58da4-133">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="58da4-134">總結</span><span class="sxs-lookup"><span data-stu-id="58da4-134">Summary</span></span>                                                                                                                              |
|------------------------------------------------|--------------------|--------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="58da4-135">\_選項名稱\_</span><span class="sxs-lookup"><span data-stu-id="58da4-135">\_OptionName\_</span></span><br/>                      | <span data-ttu-id="58da4-136">字串</span><span class="sxs-lookup"><span data-stu-id="58da4-136">string</span></span><br/>  | <span data-ttu-id="58da4-137">字元</span><span class="sxs-lookup"><span data-stu-id="58da4-137">characters</span></span><br/>    | <span data-ttu-id="58da4-138">以 [XML 命名空間](https://www.w3.org/TR/1999/REC-xml-names-19990114/)所定義的有效完整名稱。</span><span class="sxs-lookup"><span data-stu-id="58da4-138">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="58da4-139">如果未指定命名空間，則會假設為預設命名空間。</span><span class="sxs-lookup"><span data-stu-id="58da4-139">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="58da4-140">選項的名稱。</span><span class="sxs-lookup"><span data-stu-id="58da4-140">The name of the option.</span></span><br/>                                                                                                   |
| <span data-ttu-id="58da4-141">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="58da4-141">\_IdentityOptionValue\_</span></span><br/>             | <span data-ttu-id="58da4-142">字串</span><span class="sxs-lookup"><span data-stu-id="58da4-142">string</span></span><br/>  | <span data-ttu-id="58da4-143">n/a</span><span class="sxs-lookup"><span data-stu-id="58da4-143">n/a</span></span><br/>           | <span data-ttu-id="58da4-144">True、False。</span><span class="sxs-lookup"><span data-stu-id="58da4-144">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="58da4-145">定義選項，當選取此選項時，會停用此功能。</span><span class="sxs-lookup"><span data-stu-id="58da4-145">Defines an Option which when selected would disable this feature.</span></span><br/>                                                         |
| <span data-ttu-id="58da4-146">\_PagesPerSheetValue\_</span><span class="sxs-lookup"><span data-stu-id="58da4-146">\_PagesPerSheetValue\_</span></span><br/>              | <span data-ttu-id="58da4-147">整數</span><span class="sxs-lookup"><span data-stu-id="58da4-147">integer</span></span><br/> | <span data-ttu-id="58da4-148">邏輯頁面</span><span class="sxs-lookup"><span data-stu-id="58da4-148">Logical pages</span></span><br/> | <span data-ttu-id="58da4-149">所有整數 (大於零) 。</span><span class="sxs-lookup"><span data-stu-id="58da4-149">All integers (Greater than Zero).</span></span><br/>                                                                                                                                          | <span data-ttu-id="58da4-150">指定每個實體工作表的邏輯頁面數目。</span><span class="sxs-lookup"><span data-stu-id="58da4-150">Specifies the number of logical pages per physical sheet.</span></span> <span data-ttu-id="58da4-151">支援的集合可以是任何一組整數，例如</span><span class="sxs-lookup"><span data-stu-id="58da4-151">Supported set can be any set of integers E.g.</span></span> <span data-ttu-id="58da4-152">{1,2,4,6,8,9,16}.</span><span class="sxs-lookup"><span data-stu-id="58da4-152">{1,2,4,6,8,9,16}.</span></span><br/> |
| <span data-ttu-id="58da4-153">\_PresentationDirectionOptionName\_</span><span class="sxs-lookup"><span data-stu-id="58da4-153">\_PresentationDirectionOptionName\_</span></span><br/> | <span data-ttu-id="58da4-154">字串</span><span class="sxs-lookup"><span data-stu-id="58da4-154">string</span></span><br/>  | <span data-ttu-id="58da4-155">字元</span><span class="sxs-lookup"><span data-stu-id="58da4-155">characters</span></span><br/>    | <span data-ttu-id="58da4-156">以 [XML 命名空間](https://www.w3.org/TR/1999/REC-xml-names-19990114/)所定義的有效完整名稱。</span><span class="sxs-lookup"><span data-stu-id="58da4-156">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="58da4-157">如果未指定命名空間，則會假設為預設命名空間。</span><span class="sxs-lookup"><span data-stu-id="58da4-157">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="58da4-158">選項的名稱。</span><span class="sxs-lookup"><span data-stu-id="58da4-158">The name of the option.</span></span><br/>                                                                                                   |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="58da4-159">可延伸標記語言 (XML)  (XML) 內容</span><span class="sxs-lookup"><span data-stu-id="58da4-159">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="58da4-160">公用列印架構關鍵字是在 https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords 命名空間中定義。</span><span class="sxs-lookup"><span data-stu-id="58da4-160">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="58da4-161">此關鍵字的 public 可延伸標記語言 (XML)  (XML) 內容定義如下：</span><span class="sxs-lookup"><span data-stu-id="58da4-161">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:DocumentNUp">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option>
    <psf:ScoredProperty name="psk:PagesPerSheet">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Feature name="psk:PresentationDirection">
    <!-- Specifies format left to right, top to bottom. -->
    <psf:Option name="psk:RightBottom" />
    <!-- Specifies format top to bottom, left to right. -->
    <psf:Option name="psk:BottomRight" />
    <!-- Specifies format right to left, top to bottom. -->
    <psf:Option name="psk:LeftBottom" />
    <!-- Specifies format top to bottom, right to left. -->
    <psf:Option name="psk:BottomLeft" />
    <!-- Specifies format left to right, bottom to top. -->
    <psf:Option name="psk:RightTop" />
    <!-- Specifies format bottom to top, left to right. -->
    <psf:Option name="psk:TopRight" />
    <!-- Specifies format right to left, bottom to top. -->
    <psf:Option name="psk:LeftTop" />
    <!-- Specifies format bottom to top, right to left. -->
    <psf:Option name="psk:TopLeft" />
  </psf:Feature>
</psf:Feature>
    
```

## <a name="related-topics"></a><span data-ttu-id="58da4-162">相關主題</span><span class="sxs-lookup"><span data-stu-id="58da4-162">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="58da4-163">列印架構規格</span><span class="sxs-lookup"><span data-stu-id="58da4-163">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




