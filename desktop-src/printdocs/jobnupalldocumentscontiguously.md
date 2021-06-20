---
description: 深入瞭解 JobNUpAllDocumentsContiguously 元素，其描述多個邏輯頁面至單一實體工作表的輸出。
ms.assetid: e73e1736-9be5-4831-8277-23a62658b7b5
title: JobNUpAllDocumentsContiguously
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9106259c80a7efb89cc4481780bfb55af4f07e23
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/19/2021
ms.locfileid: "112408861"
---
# <a name="jobnupalldocumentscontiguously"></a><span data-ttu-id="859db-103">JobNUpAllDocumentsContiguously</span><span class="sxs-lookup"><span data-stu-id="859db-103">JobNUpAllDocumentsContiguously</span></span>

<span data-ttu-id="859db-104">本主題並非最新的。</span><span class="sxs-lookup"><span data-stu-id="859db-104">This topic is not current.</span></span> <span data-ttu-id="859db-105">如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。</span><span class="sxs-lookup"><span data-stu-id="859db-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="859db-106">描述多個邏輯頁面至單一實體工作表的輸出。</span><span class="sxs-lookup"><span data-stu-id="859db-106">Describes the output of multiple logical pages to a single physical sheet.</span></span> <span data-ttu-id="859db-107">作業中的所有檔都會連續編譯。</span><span class="sxs-lookup"><span data-stu-id="859db-107">All documents in the job are compiled together contiguously.</span></span> <span data-ttu-id="859db-108">JobNUpAllDocumentsContiguously 和 DocumentNUp 互斥。</span><span class="sxs-lookup"><span data-stu-id="859db-108">JobNUpAllDocumentsContiguously and DocumentNUp are mutually exclusive.</span></span> <span data-ttu-id="859db-109">驅動程式會決定這些關鍵字之間的條件約束處理。</span><span class="sxs-lookup"><span data-stu-id="859db-109">It is up to the driver to determine constraint handling between these keywords.</span></span>

<span data-ttu-id="859db-110">下圖說明含有3個頁面的檔1的範例，以及包含2個頁面的檔2。</span><span class="sxs-lookup"><span data-stu-id="859db-110">The following diagram illustrates an example with Document 1 containing 3 pages, and Document 2 containing 2 pages.</span></span> <span data-ttu-id="859db-111">作業中的每份檔都會連續 duplexed。</span><span class="sxs-lookup"><span data-stu-id="859db-111">Each document in the job is duplexed contiguously.</span></span> <span data-ttu-id="859db-112">範例中顯示的呈現方向是 RightBottom 選項。</span><span class="sxs-lookup"><span data-stu-id="859db-112">The presentation directions shown in the example is the RightBottom option.</span></span>

![顯示如何根據 documentnup 設定在單一工作表上設定檔頁面面的圖表](images/local-1242234459-jobduplexpics.gif)

-   [<span data-ttu-id="859db-114">項目資訊</span><span class="sxs-lookup"><span data-stu-id="859db-114">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="859db-115">結構化內容</span><span class="sxs-lookup"><span data-stu-id="859db-115">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="859db-116">可延伸標記語言 (XML)  (XML) 內容</span><span class="sxs-lookup"><span data-stu-id="859db-116">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="859db-117">項目資訊</span><span class="sxs-lookup"><span data-stu-id="859db-117">Element Information</span></span>



| <span data-ttu-id="859db-118">Name</span><span class="sxs-lookup"><span data-stu-id="859db-118">Name</span></span> | <span data-ttu-id="859db-119">值</span><span class="sxs-lookup"><span data-stu-id="859db-119">Value</span></span> |
|----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="859db-120">項目類型</span><span class="sxs-lookup"><span data-stu-id="859db-120">Element Type</span></span> <br/>   | <span data-ttu-id="859db-121">功能</span><span class="sxs-lookup"><span data-stu-id="859db-121">Feature</span></span><br/>                                                                                                                             |
| <span data-ttu-id="859db-122">範圍前置詞</span><span class="sxs-lookup"><span data-stu-id="859db-122">Scoping Prefix</span></span> <br/> | <span data-ttu-id="859db-123">工作 (Job)</span><span class="sxs-lookup"><span data-stu-id="859db-123">Job</span></span><br/>                                                                                                                                 |
| <span data-ttu-id="859db-124">備註</span><span class="sxs-lookup"><span data-stu-id="859db-124">Notes</span></span> <br/>          | <span data-ttu-id="859db-125">頂端、底部、左方和右邊都是相對於 PageImageableSize，其中下拉式功能表由高度和寬度的原點表示。</span><span class="sxs-lookup"><span data-stu-id="859db-125">Top, Bottom, Left, and Right are relative to the PageImageableSize, where TopLeft is denoted by the origin of the height and width.</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="859db-126">結構化內容</span><span class="sxs-lookup"><span data-stu-id="859db-126">Structural Content</span></span>

<span data-ttu-id="859db-127">此元素的 XML 結構為：</span><span class="sxs-lookup"><span data-stu-id="859db-127">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="859db-128">結構變數</span><span class="sxs-lookup"><span data-stu-id="859db-128">Structure Variables</span></span>

<span data-ttu-id="859db-129">下表概述 XML 結構中所定義之變數的特性。</span><span class="sxs-lookup"><span data-stu-id="859db-129">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="859db-130">Name</span><span class="sxs-lookup"><span data-stu-id="859db-130">Name</span></span>                                           | <span data-ttu-id="859db-131">資料類型</span><span class="sxs-lookup"><span data-stu-id="859db-131">Data type</span></span>          | <span data-ttu-id="859db-132">單位</span><span class="sxs-lookup"><span data-stu-id="859db-132">Unit</span></span>                     | <span data-ttu-id="859db-133">支援的值</span><span class="sxs-lookup"><span data-stu-id="859db-133">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="859db-134">總結</span><span class="sxs-lookup"><span data-stu-id="859db-134">Summary</span></span>                                                                                                                              |
|------------------------------------------------|--------------------|--------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="859db-135">\_選項名稱\_</span><span class="sxs-lookup"><span data-stu-id="859db-135">\_OptionName\_</span></span><br/>                      | <span data-ttu-id="859db-136">string</span><span class="sxs-lookup"><span data-stu-id="859db-136">string</span></span><br/>  | <span data-ttu-id="859db-137">字元</span><span class="sxs-lookup"><span data-stu-id="859db-137">characters</span></span><br/>    | <span data-ttu-id="859db-138">以 [XML 命名空間](https://www.w3.org/TR/1999/REC-xml-names-19990114/)所定義的有效完整名稱。</span><span class="sxs-lookup"><span data-stu-id="859db-138">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="859db-139">如果未指定命名空間，則會假設為預設命名空間。</span><span class="sxs-lookup"><span data-stu-id="859db-139">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="859db-140">選項的名稱。</span><span class="sxs-lookup"><span data-stu-id="859db-140">The name of the option.</span></span><br/>                                                                                                   |
| <span data-ttu-id="859db-141">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="859db-141">\_IdentityOptionValue\_</span></span><br/>             | <span data-ttu-id="859db-142">string</span><span class="sxs-lookup"><span data-stu-id="859db-142">string</span></span><br/>  | <span data-ttu-id="859db-143">n/a</span><span class="sxs-lookup"><span data-stu-id="859db-143">n/a</span></span><br/>           | <span data-ttu-id="859db-144">True、False。</span><span class="sxs-lookup"><span data-stu-id="859db-144">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="859db-145">定義選項，當選取此選項時，會停用此功能。</span><span class="sxs-lookup"><span data-stu-id="859db-145">Defines an Option which when selected would disable this feature.</span></span><br/>                                                         |
| <span data-ttu-id="859db-146">\_PagesPerSheetValue\_</span><span class="sxs-lookup"><span data-stu-id="859db-146">\_PagesPerSheetValue\_</span></span><br/>              | <span data-ttu-id="859db-147">整數</span><span class="sxs-lookup"><span data-stu-id="859db-147">integer</span></span><br/> | <span data-ttu-id="859db-148">邏輯頁面</span><span class="sxs-lookup"><span data-stu-id="859db-148">Logical pages</span></span><br/> | <span data-ttu-id="859db-149">所有整數 (大於零) 。</span><span class="sxs-lookup"><span data-stu-id="859db-149">All integers (Greater than zero).</span></span><br/>                                                                                                                                          | <span data-ttu-id="859db-150">指定每個實體工作表的邏輯頁面數目。</span><span class="sxs-lookup"><span data-stu-id="859db-150">Specifies the number of logical pages per physical sheet.</span></span> <span data-ttu-id="859db-151">支援的集合可以是任何一組整數，例如</span><span class="sxs-lookup"><span data-stu-id="859db-151">Supported set can be any set of integers E.g.</span></span> <span data-ttu-id="859db-152">{1,2,4,6,8,9,16}.</span><span class="sxs-lookup"><span data-stu-id="859db-152">{1,2,4,6,8,9,16}.</span></span><br/> |
| <span data-ttu-id="859db-153">\_PresentationDirectionOptionName\_</span><span class="sxs-lookup"><span data-stu-id="859db-153">\_PresentationDirectionOptionName\_</span></span><br/> | <span data-ttu-id="859db-154">string</span><span class="sxs-lookup"><span data-stu-id="859db-154">string</span></span><br/>  | <span data-ttu-id="859db-155">字元</span><span class="sxs-lookup"><span data-stu-id="859db-155">characters</span></span><br/>    | <span data-ttu-id="859db-156">以 [XML 命名空間](https://www.w3.org/TR/1999/REC-xml-names-19990114/)所定義的有效完整名稱。</span><span class="sxs-lookup"><span data-stu-id="859db-156">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="859db-157">如果未指定命名空間，則會假設為預設命名空間。</span><span class="sxs-lookup"><span data-stu-id="859db-157">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="859db-158">選項的名稱。</span><span class="sxs-lookup"><span data-stu-id="859db-158">The name of the option.</span></span><br/>                                                                                                   |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="859db-159">可延伸標記語言 (XML)  (XML) 內容</span><span class="sxs-lookup"><span data-stu-id="859db-159">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="859db-160">公用列印架構關鍵字是在 https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords 命名空間中定義。</span><span class="sxs-lookup"><span data-stu-id="859db-160">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="859db-161">此關鍵字的 public 可延伸標記語言 (XML)  (XML) 內容定義如下：</span><span class="sxs-lookup"><span data-stu-id="859db-161">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="859db-162">相關主題</span><span class="sxs-lookup"><span data-stu-id="859db-162">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="859db-163">列印架構規格</span><span class="sxs-lookup"><span data-stu-id="859db-163">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




