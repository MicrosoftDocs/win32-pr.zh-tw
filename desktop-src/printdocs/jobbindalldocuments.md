---
description: 本主題並非最新的。 如需最新資訊，請參閱列印架構規格。
ms.assetid: f21199e2-2220-40c4-9429-72aa2a34a5f2
title: JobBindAllDocuments
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: deff299aa5c8d76c9fb8e904539c287ecc881ee6
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/26/2021
ms.locfileid: "107998445"
---
# <a name="jobbindalldocuments"></a><span data-ttu-id="361d1-104">JobBindAllDocuments</span><span class="sxs-lookup"><span data-stu-id="361d1-104">JobBindAllDocuments</span></span>

<span data-ttu-id="361d1-105">本主題並非最新的。</span><span class="sxs-lookup"><span data-stu-id="361d1-105">This topic is not current.</span></span> <span data-ttu-id="361d1-106">如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。</span><span class="sxs-lookup"><span data-stu-id="361d1-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="361d1-107">描述系結的方法。</span><span class="sxs-lookup"><span data-stu-id="361d1-107">Describes the method of binding.</span></span> <span data-ttu-id="361d1-108">作業中的所有檔都系結在一起。</span><span class="sxs-lookup"><span data-stu-id="361d1-108">All documents in the job are bound together.</span></span> <span data-ttu-id="361d1-109">JobBindAllDocuments 和 DocumentBinding 互斥。</span><span class="sxs-lookup"><span data-stu-id="361d1-109">JobBindAllDocuments and DocumentBinding are mutually exclusive.</span></span> <span data-ttu-id="361d1-110">驅動程式會決定這些關鍵字之間的條件約束處理。</span><span class="sxs-lookup"><span data-stu-id="361d1-110">It is up to the driver to determine constraint handling between these keywords.</span></span>

-   [<span data-ttu-id="361d1-111">項目資訊</span><span class="sxs-lookup"><span data-stu-id="361d1-111">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="361d1-112">結構化內容</span><span class="sxs-lookup"><span data-stu-id="361d1-112">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="361d1-113">可延伸標記語言 (XML)  (XML) 內容</span><span class="sxs-lookup"><span data-stu-id="361d1-113">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="361d1-114">項目資訊</span><span class="sxs-lookup"><span data-stu-id="361d1-114">Element Information</span></span>



| <span data-ttu-id="361d1-115">Name</span><span class="sxs-lookup"><span data-stu-id="361d1-115">Name</span></span> | <span data-ttu-id="361d1-116">值</span><span class="sxs-lookup"><span data-stu-id="361d1-116">Value</span></span> |
|----------------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="361d1-117">項目類型</span><span class="sxs-lookup"><span data-stu-id="361d1-117">Element Type</span></span> <br/>   | <span data-ttu-id="361d1-118">功能</span><span class="sxs-lookup"><span data-stu-id="361d1-118">Feature</span></span><br/>                                                             |
| <span data-ttu-id="361d1-119">範圍前置詞</span><span class="sxs-lookup"><span data-stu-id="361d1-119">Scoping Prefix</span></span> <br/> | <span data-ttu-id="361d1-120">工作 (Job)</span><span class="sxs-lookup"><span data-stu-id="361d1-120">Job</span></span><br/>                                                                 |
| <span data-ttu-id="361d1-121">備註</span><span class="sxs-lookup"><span data-stu-id="361d1-121">Notes</span></span> <br/>          | <span data-ttu-id="361d1-122">頂端、底部、左方和右邊都是相對於 PageImageableSize。</span><span class="sxs-lookup"><span data-stu-id="361d1-122">Top, Bottom, Left, and Right are relative to the PageImageableSize.</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="361d1-123">結構化內容</span><span class="sxs-lookup"><span data-stu-id="361d1-123">Structural Content</span></span>

<span data-ttu-id="361d1-124">此元素的 XML 結構為：</span><span class="sxs-lookup"><span data-stu-id="361d1-124">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:JobBindAllDocuments">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option name="psk:_OptionName_">
    <psf:Property name="psf:IdentityOption">
      <psf:Value xsi:type="xs:string">_IdentityOptionValue_</psf:Value>
    </psf:Property>
    <psf:ScoredProperty name="psk:BindingGutter">
      <psf:Value xsi:type="xs:integer">_BindingGutterValue_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature>
```

## <a name="structure-variables"></a><span data-ttu-id="361d1-125">結構變數</span><span class="sxs-lookup"><span data-stu-id="361d1-125">Structure Variables</span></span>

<span data-ttu-id="361d1-126">下表概述 XML 結構中所定義之變數的特性。</span><span class="sxs-lookup"><span data-stu-id="361d1-126">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="361d1-127">Name</span><span class="sxs-lookup"><span data-stu-id="361d1-127">Name</span></span>                               | <span data-ttu-id="361d1-128">資料類型</span><span class="sxs-lookup"><span data-stu-id="361d1-128">Data type</span></span>          | <span data-ttu-id="361d1-129">單位</span><span class="sxs-lookup"><span data-stu-id="361d1-129">Unit</span></span>                  | <span data-ttu-id="361d1-130">支援的值</span><span class="sxs-lookup"><span data-stu-id="361d1-130">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="361d1-131">總結</span><span class="sxs-lookup"><span data-stu-id="361d1-131">Summary</span></span>                                                                                                                                                                |
|------------------------------------|--------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="361d1-132">\_選項名稱\_</span><span class="sxs-lookup"><span data-stu-id="361d1-132">\_OptionName\_</span></span><br/>          | <span data-ttu-id="361d1-133">字串</span><span class="sxs-lookup"><span data-stu-id="361d1-133">string</span></span><br/>  | <span data-ttu-id="361d1-134">字元</span><span class="sxs-lookup"><span data-stu-id="361d1-134">characters</span></span><br/> | <span data-ttu-id="361d1-135">以 [XML 命名空間](https://www.w3.org/TR/1999/REC-xml-names-19990114/)所定義的有效完整名稱。</span><span class="sxs-lookup"><span data-stu-id="361d1-135">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="361d1-136">如果未指定命名空間，則會假設為預設命名空間。</span><span class="sxs-lookup"><span data-stu-id="361d1-136">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="361d1-137">選項的名稱。</span><span class="sxs-lookup"><span data-stu-id="361d1-137">The name of the option.</span></span><br/>                                                                                                                                     |
| <span data-ttu-id="361d1-138">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="361d1-138">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="361d1-139">字串</span><span class="sxs-lookup"><span data-stu-id="361d1-139">string</span></span><br/>  | <span data-ttu-id="361d1-140">n/a</span><span class="sxs-lookup"><span data-stu-id="361d1-140">n/a</span></span><br/>        | <span data-ttu-id="361d1-141">True、False。</span><span class="sxs-lookup"><span data-stu-id="361d1-141">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="361d1-142">定義選項，當選取此選項時，會停用此功能。</span><span class="sxs-lookup"><span data-stu-id="361d1-142">Defines an Option which when selected would disable this feature.</span></span><br/>                                                                                           |
| <span data-ttu-id="361d1-143">\_BindingGutterValue\_</span><span class="sxs-lookup"><span data-stu-id="361d1-143">\_BindingGutterValue\_</span></span><br/>  | <span data-ttu-id="361d1-144">整數</span><span class="sxs-lookup"><span data-stu-id="361d1-144">integer</span></span><br/> | <span data-ttu-id="361d1-145">微米</span><span class="sxs-lookup"><span data-stu-id="361d1-145">microns</span></span><br/>    | <span data-ttu-id="361d1-146">大於 0。</span><span class="sxs-lookup"><span data-stu-id="361d1-146">Greater than 0.</span></span><br/>                                                                                                                                                            | <span data-ttu-id="361d1-147">定義指定之完成裝訂系結的最小裝訂裝訂邊。</span><span class="sxs-lookup"><span data-stu-id="361d1-147">Defines minimum binding gutter for the specified finishing binding.</span></span> <span data-ttu-id="361d1-148">裝訂邊會以 microns 相對於實體媒體維度的邊緣來測量。</span><span class="sxs-lookup"><span data-stu-id="361d1-148">The gutter is measured in microns relative to the edge of the physical media dimension.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="361d1-149">可延伸標記語言 (XML)  (XML) 內容</span><span class="sxs-lookup"><span data-stu-id="361d1-149">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="361d1-150">公用列印架構關鍵字是在 https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords 命名空間中定義。</span><span class="sxs-lookup"><span data-stu-id="361d1-150">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="361d1-151">此關鍵字的 public 可延伸標記語言 (XML)  (XML) 內容定義如下：</span><span class="sxs-lookup"><span data-stu-id="361d1-151">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:JobBindAllDocuments">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!-- Specifies bale binding. -->
  <psf:Option name="psk:Bale">
    <psf:ScoredProperty name="psk:BindingGutter">
      <psf:ParameterRef name="psk:JobBindAllDocumentsGutter" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies binding along the bottom edge. -->
  <psf:Option name="psk:BindBottom">
    <psf:ScoredProperty name="psk:BindingGutter">
      <psf:ParameterRef name="psk:JobBindAllDocumentsGutter" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies binding along the left edge. -->
  <psf:Option name="psk:BindLeft">
    <psf:ScoredProperty name="psk:BindingGutter">
      <psf:ParameterRef name="psk:JobBindAllDocumentsGutter" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies binding along the right edge. -->
  <psf:Option name="psk:BindRight">
    <psf:ScoredProperty name="psk:BindingGutter">
      <psf:ParameterRef name="psk:JobBindAllDocumentsGutter" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies binding along the top edge. -->
  <psf:Option name="psk:BindTop">
    <psf:ScoredProperty name="psk:BindingGutter">
      <psf:ParameterRef name="psk:JobBindAllDocumentsGutter" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies booklet binding. -->
  <psf:Option name="psk:Booklet" />
    <psf:ScoredProperty name="psk:BindingGutter">
      <psf:ParameterRef name="psk:JobBindAllDocumentsGutter" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies edge stitching along the bottom edge. -->
  <psf:Option name="psk:EdgeStitchBottom">
    <psf:ScoredProperty name="psk:BindingGutter">
      <psf:ParameterRef name="psk:JobBindAllDocumentsGutter" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies edge stitching along the left edge. -->
  <psf:Option name="psk:EdgeStitchLeft">
    <psf:ScoredProperty name="psk:BindingGutter">
      <psf:ParameterRef name="psk:JobBindAllDocumentsGutter" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies edge stitching along the right edge. -->
  <psf:Option name="psk:EdgeStitchRight">
    <psf:ScoredProperty name="psk:BindingGutter">
      <psf:ParameterRef name="psk:JobBindAllDocumentsGutter" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies edge stitching along the top edge. -->
  <psf:Option name="psk:EdgeStitchTop">
    <psf:ScoredProperty name="psk:BindingGutter">
      <psf:ParameterRef name="psk:JobBindAllDocumentsGutter" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies a folded binding. -->
  <psf:Option name="psk:Fold" />
    <psf:ScoredProperty name="psk:BindingGutter">
      <psf:ParameterRef name="psk:JobBindAllDocumentsGutter" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies jog offset binding. -->
  <psf:Option name="psk:JogOffset" />
    <psf:ScoredProperty name="psk:BindingGutter">
      <psf:ParameterRef name="psk:JobBindAllDocumentsGutter" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies trimming binding. -->
  <psf:Option name="psk:Trim" />
    <psf:ScoredProperty name="psk:BindingGutter">
      <psf:ParameterRef name="psk:JobBindAllDocumentsGutter" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies no binding. -->
  <psf:Option name="psk:None" />
</psf:Feature>
```

## <a name="related-topics"></a><span data-ttu-id="361d1-152">相關主題</span><span class="sxs-lookup"><span data-stu-id="361d1-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="361d1-153">列印架構規格</span><span class="sxs-lookup"><span data-stu-id="361d1-153">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




