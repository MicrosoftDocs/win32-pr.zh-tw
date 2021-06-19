---
description: 瞭解 DocumentBinding 元素，其描述系結的方法。 DocumentBinding 和 JobBindAllDocuments 互斥。
ms.assetid: 36a7c360-2d26-46b9-b829-0fb35b36c79c
title: DocumentBinding
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf2b8f44c90cdef37a6599bf25904949748c82ba
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/19/2021
ms.locfileid: "112409461"
---
# <a name="documentbinding"></a><span data-ttu-id="336c4-104">DocumentBinding</span><span class="sxs-lookup"><span data-stu-id="336c4-104">DocumentBinding</span></span>

<span data-ttu-id="336c4-105">本主題並非最新的。</span><span class="sxs-lookup"><span data-stu-id="336c4-105">This topic is not current.</span></span> <span data-ttu-id="336c4-106">如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。</span><span class="sxs-lookup"><span data-stu-id="336c4-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="336c4-107">描述系結的方法。</span><span class="sxs-lookup"><span data-stu-id="336c4-107">Describes the method of binding.</span></span> <span data-ttu-id="336c4-108">每份檔都是分開系結。</span><span class="sxs-lookup"><span data-stu-id="336c4-108">Each document is bound separately.</span></span> <span data-ttu-id="336c4-109">DocumentBinding 和 JobBindAllDocuments 互斥。</span><span class="sxs-lookup"><span data-stu-id="336c4-109">DocumentBinding and JobBindAllDocuments are mutually exclusive.</span></span> <span data-ttu-id="336c4-110">驅動程式會決定關鍵字之間的條件約束處理。</span><span class="sxs-lookup"><span data-stu-id="336c4-110">It is up to the driver to determine constraint handling between keywords.</span></span>

-   [<span data-ttu-id="336c4-111">項目資訊</span><span class="sxs-lookup"><span data-stu-id="336c4-111">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="336c4-112">結構化內容</span><span class="sxs-lookup"><span data-stu-id="336c4-112">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="336c4-113">可延伸標記語言 (XML)  (XML) 內容</span><span class="sxs-lookup"><span data-stu-id="336c4-113">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="336c4-114">項目資訊</span><span class="sxs-lookup"><span data-stu-id="336c4-114">Element Information</span></span>



| <span data-ttu-id="336c4-115">Name</span><span class="sxs-lookup"><span data-stu-id="336c4-115">Name</span></span> | <span data-ttu-id="336c4-116">值</span><span class="sxs-lookup"><span data-stu-id="336c4-116">Value</span></span> |
|----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="336c4-117">項目類型</span><span class="sxs-lookup"><span data-stu-id="336c4-117">Element Type</span></span> <br/>   | <span data-ttu-id="336c4-118">功能</span><span class="sxs-lookup"><span data-stu-id="336c4-118">Feature</span></span><br/>                                                                                                                              |
| <span data-ttu-id="336c4-119">範圍前置詞</span><span class="sxs-lookup"><span data-stu-id="336c4-119">Scoping Prefix</span></span> <br/> | <span data-ttu-id="336c4-120">文件</span><span class="sxs-lookup"><span data-stu-id="336c4-120">Document</span></span><br/>                                                                                                                             |
| <span data-ttu-id="336c4-121">備註</span><span class="sxs-lookup"><span data-stu-id="336c4-121">Notes</span></span> <br/>          | <span data-ttu-id="336c4-122">頂端、底部、左方和右邊都是相對於 PageImageableSize，其中下拉式功能表是以 X 軸和 y 軸的原點表示。</span><span class="sxs-lookup"><span data-stu-id="336c4-122">Top, Bottom, Left, and Right are relative to the PageImageableSize, where TopLeft is denoted by the origin of the x-axis and y-axis.</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="336c4-123">結構化內容</span><span class="sxs-lookup"><span data-stu-id="336c4-123">Structural Content</span></span>

<span data-ttu-id="336c4-124">此元素的 XML 結構如下所示：</span><span class="sxs-lookup"><span data-stu-id="336c4-124">The XML structure of this element is as follows:</span></span>

``` syntax
<psf:Feature name="psk:DocumentBinding">
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

## <a name="structure-variables"></a><span data-ttu-id="336c4-125">結構變數</span><span class="sxs-lookup"><span data-stu-id="336c4-125">Structure Variables</span></span>

<span data-ttu-id="336c4-126">下表概述 XML 結構中所定義之變數的特性。</span><span class="sxs-lookup"><span data-stu-id="336c4-126">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="336c4-127">Name</span><span class="sxs-lookup"><span data-stu-id="336c4-127">Name</span></span>                               | <span data-ttu-id="336c4-128">資料類型</span><span class="sxs-lookup"><span data-stu-id="336c4-128">Data type</span></span>          | <span data-ttu-id="336c4-129">單位</span><span class="sxs-lookup"><span data-stu-id="336c4-129">Unit</span></span>                  | <span data-ttu-id="336c4-130">支援的值</span><span class="sxs-lookup"><span data-stu-id="336c4-130">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="336c4-131">總結</span><span class="sxs-lookup"><span data-stu-id="336c4-131">Summary</span></span>                                                                                                                                                                |
|------------------------------------|--------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="336c4-132">\_選項名稱\_</span><span class="sxs-lookup"><span data-stu-id="336c4-132">\_OptionName\_</span></span><br/>          | <span data-ttu-id="336c4-133">string</span><span class="sxs-lookup"><span data-stu-id="336c4-133">string</span></span><br/>  | <span data-ttu-id="336c4-134">字元</span><span class="sxs-lookup"><span data-stu-id="336c4-134">characters</span></span><br/> | <span data-ttu-id="336c4-135">以 [XML 命名空間](https://www.w3.org/TR/1999/REC-xml-names-19990114/)所定義的有效完整名稱。</span><span class="sxs-lookup"><span data-stu-id="336c4-135">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="336c4-136">如果未指定命名空間，則會假設為預設命名空間。</span><span class="sxs-lookup"><span data-stu-id="336c4-136">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="336c4-137">選項的名稱。</span><span class="sxs-lookup"><span data-stu-id="336c4-137">The name of the option.</span></span><br/>                                                                                                                                     |
| <span data-ttu-id="336c4-138">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="336c4-138">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="336c4-139">string</span><span class="sxs-lookup"><span data-stu-id="336c4-139">string</span></span><br/>  | <span data-ttu-id="336c4-140">n/a</span><span class="sxs-lookup"><span data-stu-id="336c4-140">n/a</span></span><br/>        | <span data-ttu-id="336c4-141">True、False。</span><span class="sxs-lookup"><span data-stu-id="336c4-141">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="336c4-142">定義選項，當選取此選項時，會停用此功能。</span><span class="sxs-lookup"><span data-stu-id="336c4-142">Defines an Option which when selected would disable this feature.</span></span><br/>                                                                                           |
| <span data-ttu-id="336c4-143">\_BindingGutterValue\_</span><span class="sxs-lookup"><span data-stu-id="336c4-143">\_BindingGutterValue\_</span></span><br/>  | <span data-ttu-id="336c4-144">整數</span><span class="sxs-lookup"><span data-stu-id="336c4-144">Integer</span></span><br/> | <span data-ttu-id="336c4-145">微米</span><span class="sxs-lookup"><span data-stu-id="336c4-145">microns</span></span><br/>    | <span data-ttu-id="336c4-146">大於或等於0。</span><span class="sxs-lookup"><span data-stu-id="336c4-146">Greater than or equal to 0.</span></span><br/>                                                                                                                                                | <span data-ttu-id="336c4-147">定義指定之完成裝訂系結的最小裝訂裝訂邊。</span><span class="sxs-lookup"><span data-stu-id="336c4-147">Defines minimum binding gutter for the specified finishing binding.</span></span> <span data-ttu-id="336c4-148">裝訂邊會以 microns 相對於實體媒體維度的邊緣來測量。</span><span class="sxs-lookup"><span data-stu-id="336c4-148">The gutter is measured in microns relative to the edge of the physical media dimension.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="336c4-149">可延伸標記語言 (XML)  (XML) 內容</span><span class="sxs-lookup"><span data-stu-id="336c4-149">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="336c4-150">公用列印架構關鍵字是在 https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords 命名空間中定義。</span><span class="sxs-lookup"><span data-stu-id="336c4-150">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="336c4-151">此關鍵字的 public 可延伸標記語言 (XML)  (XML) 內容定義如下：</span><span class="sxs-lookup"><span data-stu-id="336c4-151">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:DocumentBinding">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!-- Specifies bale binding. -->
  <psf:Option name="psk:Bale" >
    <psf:ScoredProperty name="psk:BindingGutter">
      <psf:ParameterRef name="psk:DocumentBindingGutter" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies binding along the bottom edge. -->
  <psf:Option name="psk:BindBottom">
    <psf:ScoredProperty name="psk:BindingGutter">
      <psf:ParameterRef name="psk:DocumentBindingGutter" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies binding along the left edge. -->
  <psf:Option name="psk:BindLeft">
    <psf:ScoredProperty name="psk:BindingGutter">
      <psf:ParameterRef name="psk:DocumentBindingGutter" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies binding along the right edge. -->
  <psf:Option name="psk:BindRight">
    <psf:ScoredProperty name="psk:BindingGutter">
      <psf:ParameterRef name="psk:DocumentBindingGutter" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies binding along the top edge. -->
  <psf:Option name="psk:BindTop">
    <psf:ScoredProperty name="psk:BindingGutter">
      <psf:ParameterRef name="psk:DocumentBindingGutter" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies booklet binding. -->
  <psf:Option name="psk:Booklet" />
    <psf:ScoredProperty name="psk:BindingGutter">
      <psf:ParameterRef name="psk:DocumentBindingGutter" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies edge stitching along the bottom edge. -->
  <psf:Option name="psk:EdgeStitchBottom">
    <psf:ScoredProperty name="psk:BindingGutter">
      <psf:ParameterRef name="psk:DocumentBindingGutter" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies edge stitching along the left edge. -->
  <psf:Option name="psk:EdgeStitchLeft">
    <psf:ScoredProperty name="psk:BindingGutter">
      <psf:ParameterRef name="psk:DocumentBindingGutter" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies edge stitching along the right edge. -->
  <psf:Option name="psk:EdgeStitchRight">
    <psf:ScoredProperty name="psk:BindingGutter">
      <psf:ParameterRef name="psk:DocumentBindingGutter" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies edge stitching along the top edge. -->
  <psf:Option name="psk:EdgeStitchTop">
    <psf:ScoredProperty name="psk:BindingGutter">
      <psf:ParameterRef name="psk:DocumentBindingGutter" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies a folded binding. -->
  <psf:Option name="psk:Fold" />
    <psf:ScoredProperty name="psk:BindingGutter">
      <psf:ParameterRef name="psk:DocumentBindingGutter" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies jog offset binding. -->
  <psf:Option name="psk:JogOffset" />
    <psf:ScoredProperty name="psk:BindingGutter">
      <psf:ParameterRef name="psk:DocumentBindingGutter" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies trimming binding. -->
  <psf:Option name="psk:Trim" />
    <psf:ScoredProperty name="psk:BindingGutter">
      <psf:ParameterRef name="psk:DocumentBindingGutter" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies no binding. -->
  <psf:Option name="psk:None" />
</psf:Feature>
```

## <a name="related-topics"></a><span data-ttu-id="336c4-152">相關主題</span><span class="sxs-lookup"><span data-stu-id="336c4-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="336c4-153">列印架構規格</span><span class="sxs-lookup"><span data-stu-id="336c4-153">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




