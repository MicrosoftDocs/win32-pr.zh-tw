---
description: 本主題並非最新的。 如需最新資訊，請參閱列印架構規格。
ms.assetid: e73e1736-9be5-4831-8277-23a62658b7b5
title: JobNUpAllDocumentsContiguously
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35f90620ac99bf97e85acb22c723a938c31605bd
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/26/2021
ms.locfileid: "107998085"
---
# <a name="jobnupalldocumentscontiguously"></a><span data-ttu-id="605a8-104">JobNUpAllDocumentsContiguously</span><span class="sxs-lookup"><span data-stu-id="605a8-104">JobNUpAllDocumentsContiguously</span></span>

<span data-ttu-id="605a8-105">本主題並非最新的。</span><span class="sxs-lookup"><span data-stu-id="605a8-105">This topic is not current.</span></span> <span data-ttu-id="605a8-106">如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。</span><span class="sxs-lookup"><span data-stu-id="605a8-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="605a8-107">描述多個邏輯頁面至單一實體工作表的輸出。</span><span class="sxs-lookup"><span data-stu-id="605a8-107">Describes the output of multiple logical pages to a single physical sheet.</span></span> <span data-ttu-id="605a8-108">作業中的所有檔都會連續編譯。</span><span class="sxs-lookup"><span data-stu-id="605a8-108">All documents in the job are compiled together contiguously.</span></span> <span data-ttu-id="605a8-109">JobNUpAllDocumentsContiguously 和 DocumentNUp 互斥。</span><span class="sxs-lookup"><span data-stu-id="605a8-109">JobNUpAllDocumentsContiguously and DocumentNUp are mutually exclusive.</span></span> <span data-ttu-id="605a8-110">驅動程式會決定這些關鍵字之間的條件約束處理。</span><span class="sxs-lookup"><span data-stu-id="605a8-110">It is up to the driver to determine constraint handling between these keywords.</span></span>

<span data-ttu-id="605a8-111">下圖說明含有3個頁面的檔1的範例，以及包含2個頁面的檔2。</span><span class="sxs-lookup"><span data-stu-id="605a8-111">The following diagram illustrates an example with Document 1 containing 3 pages, and Document 2 containing 2 pages.</span></span> <span data-ttu-id="605a8-112">作業中的每份檔都會連續 duplexed。</span><span class="sxs-lookup"><span data-stu-id="605a8-112">Each document in the job is duplexed contiguously.</span></span> <span data-ttu-id="605a8-113">範例中顯示的呈現方向是 RightBottom 選項。</span><span class="sxs-lookup"><span data-stu-id="605a8-113">The presentation directions shown in the example is the RightBottom option.</span></span>

![顯示如何根據 documentnup 設定在單一工作表上設定檔頁面面的圖表](images/local-1242234459-jobduplexpics.gif)

-   [<span data-ttu-id="605a8-115">項目資訊</span><span class="sxs-lookup"><span data-stu-id="605a8-115">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="605a8-116">結構化內容</span><span class="sxs-lookup"><span data-stu-id="605a8-116">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="605a8-117">可延伸標記語言 (XML)  (XML) 內容</span><span class="sxs-lookup"><span data-stu-id="605a8-117">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="605a8-118">項目資訊</span><span class="sxs-lookup"><span data-stu-id="605a8-118">Element Information</span></span>



| <span data-ttu-id="605a8-119">Name</span><span class="sxs-lookup"><span data-stu-id="605a8-119">Name</span></span> | <span data-ttu-id="605a8-120">值</span><span class="sxs-lookup"><span data-stu-id="605a8-120">Value</span></span> |
|----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="605a8-121">項目類型</span><span class="sxs-lookup"><span data-stu-id="605a8-121">Element Type</span></span> <br/>   | <span data-ttu-id="605a8-122">功能</span><span class="sxs-lookup"><span data-stu-id="605a8-122">Feature</span></span><br/>                                                                                                                             |
| <span data-ttu-id="605a8-123">範圍前置詞</span><span class="sxs-lookup"><span data-stu-id="605a8-123">Scoping Prefix</span></span> <br/> | <span data-ttu-id="605a8-124">工作 (Job)</span><span class="sxs-lookup"><span data-stu-id="605a8-124">Job</span></span><br/>                                                                                                                                 |
| <span data-ttu-id="605a8-125">備註</span><span class="sxs-lookup"><span data-stu-id="605a8-125">Notes</span></span> <br/>          | <span data-ttu-id="605a8-126">頂端、底部、左方和右邊都是相對於 PageImageableSize，其中下拉式功能表由高度和寬度的原點表示。</span><span class="sxs-lookup"><span data-stu-id="605a8-126">Top, Bottom, Left, and Right are relative to the PageImageableSize, where TopLeft is denoted by the origin of the height and width.</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="605a8-127">結構化內容</span><span class="sxs-lookup"><span data-stu-id="605a8-127">Structural Content</span></span>

<span data-ttu-id="605a8-128">此元素的 XML 結構為：</span><span class="sxs-lookup"><span data-stu-id="605a8-128">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:JobNUpAllDocumentsContiguously">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option name="psk:_OptionName_">
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

## <a name="structure-variables"></a><span data-ttu-id="605a8-129">結構變數</span><span class="sxs-lookup"><span data-stu-id="605a8-129">Structure Variables</span></span>

<span data-ttu-id="605a8-130">下表概述 XML 結構中所定義之變數的特性。</span><span class="sxs-lookup"><span data-stu-id="605a8-130">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="605a8-131">Name</span><span class="sxs-lookup"><span data-stu-id="605a8-131">Name</span></span>                                           | <span data-ttu-id="605a8-132">資料類型</span><span class="sxs-lookup"><span data-stu-id="605a8-132">Data type</span></span>          | <span data-ttu-id="605a8-133">單位</span><span class="sxs-lookup"><span data-stu-id="605a8-133">Unit</span></span>                     | <span data-ttu-id="605a8-134">支援的值</span><span class="sxs-lookup"><span data-stu-id="605a8-134">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="605a8-135">總結</span><span class="sxs-lookup"><span data-stu-id="605a8-135">Summary</span></span>                                                                                                                              |
|------------------------------------------------|--------------------|--------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="605a8-136">\_選項名稱\_</span><span class="sxs-lookup"><span data-stu-id="605a8-136">\_OptionName\_</span></span><br/>                      | <span data-ttu-id="605a8-137">字串</span><span class="sxs-lookup"><span data-stu-id="605a8-137">string</span></span><br/>  | <span data-ttu-id="605a8-138">字元</span><span class="sxs-lookup"><span data-stu-id="605a8-138">characters</span></span><br/>    | <span data-ttu-id="605a8-139">以 [XML 命名空間](https://www.w3.org/TR/1999/REC-xml-names-19990114/)所定義的有效完整名稱。</span><span class="sxs-lookup"><span data-stu-id="605a8-139">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="605a8-140">如果未指定命名空間，則會假設為預設命名空間。</span><span class="sxs-lookup"><span data-stu-id="605a8-140">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="605a8-141">選項的名稱。</span><span class="sxs-lookup"><span data-stu-id="605a8-141">The name of the option.</span></span><br/>                                                                                                   |
| <span data-ttu-id="605a8-142">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="605a8-142">\_IdentityOptionValue\_</span></span><br/>             | <span data-ttu-id="605a8-143">字串</span><span class="sxs-lookup"><span data-stu-id="605a8-143">string</span></span><br/>  | <span data-ttu-id="605a8-144">n/a</span><span class="sxs-lookup"><span data-stu-id="605a8-144">n/a</span></span><br/>           | <span data-ttu-id="605a8-145">True、False。</span><span class="sxs-lookup"><span data-stu-id="605a8-145">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="605a8-146">定義選項，當選取此選項時，會停用此功能。</span><span class="sxs-lookup"><span data-stu-id="605a8-146">Defines an Option which when selected would disable this feature.</span></span><br/>                                                         |
| <span data-ttu-id="605a8-147">\_PagesPerSheetValue\_</span><span class="sxs-lookup"><span data-stu-id="605a8-147">\_PagesPerSheetValue\_</span></span><br/>              | <span data-ttu-id="605a8-148">整數</span><span class="sxs-lookup"><span data-stu-id="605a8-148">integer</span></span><br/> | <span data-ttu-id="605a8-149">邏輯頁面</span><span class="sxs-lookup"><span data-stu-id="605a8-149">Logical pages</span></span><br/> | <span data-ttu-id="605a8-150">所有整數 (大於零) 。</span><span class="sxs-lookup"><span data-stu-id="605a8-150">All integers (Greater than zero).</span></span><br/>                                                                                                                                          | <span data-ttu-id="605a8-151">指定每個實體工作表的邏輯頁面數目。</span><span class="sxs-lookup"><span data-stu-id="605a8-151">Specifies the number of logical pages per physical sheet.</span></span> <span data-ttu-id="605a8-152">支援的集合可以是任何一組整數，例如</span><span class="sxs-lookup"><span data-stu-id="605a8-152">Supported set can be any set of integers E.g.</span></span> <span data-ttu-id="605a8-153">{1,2,4,6,8,9,16}.</span><span class="sxs-lookup"><span data-stu-id="605a8-153">{1,2,4,6,8,9,16}.</span></span><br/> |
| <span data-ttu-id="605a8-154">\_PresentationDirectionOptionName\_</span><span class="sxs-lookup"><span data-stu-id="605a8-154">\_PresentationDirectionOptionName\_</span></span><br/> | <span data-ttu-id="605a8-155">字串</span><span class="sxs-lookup"><span data-stu-id="605a8-155">string</span></span><br/>  | <span data-ttu-id="605a8-156">字元</span><span class="sxs-lookup"><span data-stu-id="605a8-156">characters</span></span><br/>    | <span data-ttu-id="605a8-157">以 [XML 命名空間](https://www.w3.org/TR/1999/REC-xml-names-19990114/)所定義的有效完整名稱。</span><span class="sxs-lookup"><span data-stu-id="605a8-157">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="605a8-158">如果未指定命名空間，則會假設為預設命名空間。</span><span class="sxs-lookup"><span data-stu-id="605a8-158">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="605a8-159">選項的名稱。</span><span class="sxs-lookup"><span data-stu-id="605a8-159">The name of the option.</span></span><br/>                                                                                                   |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="605a8-160">可延伸標記語言 (XML)  (XML) 內容</span><span class="sxs-lookup"><span data-stu-id="605a8-160">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="605a8-161">公用列印架構關鍵字是在 https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords 命名空間中定義。</span><span class="sxs-lookup"><span data-stu-id="605a8-161">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="605a8-162">此關鍵字的 public 可延伸標記語言 (XML)  (XML) 內容定義如下：</span><span class="sxs-lookup"><span data-stu-id="605a8-162">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:JobNUpAllDocumentsContiguously">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option>
    <psf:ScoredProperty name="psk:PagesPerSheet">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Feature name="psk:PresentationDirection">
    <!-- Specifies left to right, top to bottom. -->
    <psf:Option name="psk:RightBottom" />
    <!-- Specifies top to bottom, left to right. -->
    <psf:Option name="psk:BottomRight" />
    <!-- Specifies right to left, top to bottom. -->
    <psf:Option name="psk:LeftBottom" />
    <!-- Specifies top to bottom, right to left. -->
    <psf:Option name="psk:BottomLeft" />
    <!-- Specifies left to right, bottom to top. -->
    <psf:Option name="psk:RightTop" />
    <!-- Specifies bottom to top, left to right. -->
    <psf:Option name="psk:TopRight" />
    <!-- Specifies right to left, bottom to top. -->
    <psf:Option name="psk:LeftTop" />
    <!-- Specifies bottom to top, right to left. -->
    <psf:Option name="psk:TopLeft" />
  </psf:Feature>
</psf:Feature>
    
```

## <a name="related-topics"></a><span data-ttu-id="605a8-163">相關主題</span><span class="sxs-lookup"><span data-stu-id="605a8-163">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="605a8-164">列印架構規格</span><span class="sxs-lookup"><span data-stu-id="605a8-164">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




