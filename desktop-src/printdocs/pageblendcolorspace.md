---
description: 本主題並非最新的。 如需最新資訊，請參閱列印架構規格。
ms.assetid: 86e3f44d-192e-412a-abb1-118e8592d90b
title: PageBlendColorSpace
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e12002b25265a66a0aa3a5168f29e1e8e542ce31
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/26/2021
ms.locfileid: "107998075"
---
# <a name="pageblendcolorspace"></a><span data-ttu-id="b66d4-104">PageBlendColorSpace</span><span class="sxs-lookup"><span data-stu-id="b66d4-104">PageBlendColorSpace</span></span>

<span data-ttu-id="b66d4-105">本主題並非最新的。</span><span class="sxs-lookup"><span data-stu-id="b66d4-105">This topic is not current.</span></span> <span data-ttu-id="b66d4-106">如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。</span><span class="sxs-lookup"><span data-stu-id="b66d4-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="b66d4-107">描述應該用於混合作業的色彩空間。</span><span class="sxs-lookup"><span data-stu-id="b66d4-107">Describes the color space that should be used for blending operations.</span></span>

-   [<span data-ttu-id="b66d4-108">項目資訊</span><span class="sxs-lookup"><span data-stu-id="b66d4-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="b66d4-109">結構化內容</span><span class="sxs-lookup"><span data-stu-id="b66d4-109">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="b66d4-110">可延伸標記語言 (XML)  (XML) 內容</span><span class="sxs-lookup"><span data-stu-id="b66d4-110">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="b66d4-111">項目資訊</span><span class="sxs-lookup"><span data-stu-id="b66d4-111">Element Information</span></span>



| <span data-ttu-id="b66d4-112">Name</span><span class="sxs-lookup"><span data-stu-id="b66d4-112">Name</span></span> | <span data-ttu-id="b66d4-113">值</span><span class="sxs-lookup"><span data-stu-id="b66d4-113">Value</span></span> |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b66d4-114">項目類型</span><span class="sxs-lookup"><span data-stu-id="b66d4-114">Element Type</span></span> <br/>   | <span data-ttu-id="b66d4-115">功能</span><span class="sxs-lookup"><span data-stu-id="b66d4-115">Feature</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="b66d4-116">範圍前置詞</span><span class="sxs-lookup"><span data-stu-id="b66d4-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="b66d4-117">工作 (Job)</span><span class="sxs-lookup"><span data-stu-id="b66d4-117">Job</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="b66d4-118">備註</span><span class="sxs-lookup"><span data-stu-id="b66d4-118">Notes</span></span> <br/>          | <span data-ttu-id="b66d4-119">符合 XPS 規範的取用者必須在列印功能檔或 PrintTicket 中，強制資源的 URI 參考（例如影像或色彩設定檔）必須參考元件名稱， (在包含結果 PrintTicket 的相同 XPS 檔封裝內的封裝根目錄) 的相對 URI。</span><span class="sxs-lookup"><span data-stu-id="b66d4-119">XPS-compliant consumers MUST enforce that a URI reference to a resource such as an image or color profile in either a Print Capabilities document or PrintTicket MUST refer to a part name (a relative URI to the package root) within the same XPS Document package that contains the resultant PrintTicket.</span></span> <span data-ttu-id="b66d4-120">相容的 XPS 取用者不能使用不符合元件名稱語法規范的 URI。</span><span class="sxs-lookup"><span data-stu-id="b66d4-120">A compliant XPS consumer MUST NOT use a URI that is not compliant with the part name syntax.</span></span> <span data-ttu-id="b66d4-121">這些設定是 XPS 專用的。</span><span class="sxs-lookup"><span data-stu-id="b66d4-121">These settings are XPS specific.</span></span> <br/> <span data-ttu-id="b66d4-122">在列印功能檔或 PrintTicket 中參考的 Uri 不得解析為 Url。</span><span class="sxs-lookup"><span data-stu-id="b66d4-122">URIs which are referenced in either a Print Capabilities document or PrintTicket MUST NOT be resolved as URLs.</span></span> <span data-ttu-id="b66d4-123">這是不安全的，因為它們可能無法如預期地解決，而且可能會產生驅動程式和作業系統的有害安全性風險。</span><span class="sxs-lookup"><span data-stu-id="b66d4-123">This is unsafe as they may not resolve as intended and may create harmful security risks for the driver and operating system.</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="b66d4-124">結構化內容</span><span class="sxs-lookup"><span data-stu-id="b66d4-124">Structural Content</span></span>

<span data-ttu-id="b66d4-125">此元素的 XML 結構為：</span><span class="sxs-lookup"><span data-stu-id="b66d4-125">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:PageBlendColorSpace">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option name="psk:_OptionName_">
    <psf:Property name="psf:IdentityOption">
      <psf:Value xsi:type="xs:string">_IdentityOptionValue_</psf:Value>
    </psf:Property>
  </psf:Option>
</psf:Feature>
```

## <a name="structure-variables"></a><span data-ttu-id="b66d4-126">結構變數</span><span class="sxs-lookup"><span data-stu-id="b66d4-126">Structure Variables</span></span>

<span data-ttu-id="b66d4-127">下表概述 XML 結構中所定義之變數的特性。</span><span class="sxs-lookup"><span data-stu-id="b66d4-127">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="b66d4-128">Name</span><span class="sxs-lookup"><span data-stu-id="b66d4-128">Name</span></span>                               | <span data-ttu-id="b66d4-129">資料類型</span><span class="sxs-lookup"><span data-stu-id="b66d4-129">Data type</span></span>         | <span data-ttu-id="b66d4-130">單位</span><span class="sxs-lookup"><span data-stu-id="b66d4-130">Unit</span></span>                  | <span data-ttu-id="b66d4-131">支援的值</span><span class="sxs-lookup"><span data-stu-id="b66d4-131">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="b66d4-132">總結</span><span class="sxs-lookup"><span data-stu-id="b66d4-132">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="b66d4-133">\_選項名稱\_</span><span class="sxs-lookup"><span data-stu-id="b66d4-133">\_OptionName\_</span></span><br/>          | <span data-ttu-id="b66d4-134">字串</span><span class="sxs-lookup"><span data-stu-id="b66d4-134">string</span></span><br/> | <span data-ttu-id="b66d4-135">字元</span><span class="sxs-lookup"><span data-stu-id="b66d4-135">characters</span></span><br/> | <span data-ttu-id="b66d4-136">以 [XML 命名空間](https://www.w3.org/TR/1999/REC-xml-names-19990114/)所定義的有效完整名稱。</span><span class="sxs-lookup"><span data-stu-id="b66d4-136">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="b66d4-137">如果未指定命名空間，則會假設為預設命名空間。</span><span class="sxs-lookup"><span data-stu-id="b66d4-137">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="b66d4-138">選項的名稱。</span><span class="sxs-lookup"><span data-stu-id="b66d4-138">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="b66d4-139">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="b66d4-139">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="b66d4-140">字串</span><span class="sxs-lookup"><span data-stu-id="b66d4-140">string</span></span><br/> | <span data-ttu-id="b66d4-141">n/a</span><span class="sxs-lookup"><span data-stu-id="b66d4-141">n/a</span></span><br/>        | <span data-ttu-id="b66d4-142">True、False。</span><span class="sxs-lookup"><span data-stu-id="b66d4-142">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="b66d4-143">定義選項，當選取此選項時，會停用此功能。</span><span class="sxs-lookup"><span data-stu-id="b66d4-143">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="b66d4-144">可延伸標記語言 (XML)  (XML) 內容</span><span class="sxs-lookup"><span data-stu-id="b66d4-144">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="b66d4-145">公用列印架構關鍵字是在 https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords 命名空間中定義。</span><span class="sxs-lookup"><span data-stu-id="b66d4-145">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="b66d4-146">此關鍵字的 public 可延伸標記語言 (XML)  (XML) 內容定義如下：</span><span class="sxs-lookup"><span data-stu-id="b66d4-146">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:PageBlendColorSpace">
  <psf:Property name="SelectionType">
    <psf:Value xsi:type="xs:string">PickOne</psf:Value>
  </psf:Property>
  <!-- sRGB color space SHOULD be used for blending. -->
  <psf:Option name="psk:sRGB" />
  <!-- scRGB color space SHOULD be used for blending. -->
  <psf:Option name="psk:scRGB" />
  <!-- Specifies an ICC profile defining the color space that SHOULD be used for blending.  Note: This applies to XPS Documents only and should not be used in arbitrary PrintTickets. -->
  <psf:Option name="psk:ICCProfile">
    <!-- XPS specific part name for the blend mode ICC Profile -->
    <psf:ScoredProperty name="psk:URI">
      <psf:ParameterRef name="psk:PageBlendColorSpaceICCProfileURI" />
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature>
```

## <a name="related-topics"></a><span data-ttu-id="b66d4-147">相關主題</span><span class="sxs-lookup"><span data-stu-id="b66d4-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b66d4-148">列印架構規格</span><span class="sxs-lookup"><span data-stu-id="b66d4-148">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




