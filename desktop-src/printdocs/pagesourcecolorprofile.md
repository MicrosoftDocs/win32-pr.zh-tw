---
description: 瞭解 PageSourceColorProfile 元素。 此元素定義來源色彩設定檔的特性。
ms.assetid: aa4f5425-6ca1-4820-b15d-bbead1f6d735
title: PageSourceColorProfile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f709d44f8af7ea6c2709201e57bc047fe9b2d21b
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/30/2021
ms.locfileid: "113118993"
---
# <a name="pagesourcecolorprofile"></a><span data-ttu-id="55a7e-104">PageSourceColorProfile</span><span class="sxs-lookup"><span data-stu-id="55a7e-104">PageSourceColorProfile</span></span>

<span data-ttu-id="55a7e-105">本主題並非最新的。</span><span class="sxs-lookup"><span data-stu-id="55a7e-105">This topic is not current.</span></span> <span data-ttu-id="55a7e-106">如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。</span><span class="sxs-lookup"><span data-stu-id="55a7e-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="55a7e-107">定義來源色彩設定檔的特性。</span><span class="sxs-lookup"><span data-stu-id="55a7e-107">Defines the characteristics of the source color profile.</span></span>

-   [<span data-ttu-id="55a7e-108">項目資訊</span><span class="sxs-lookup"><span data-stu-id="55a7e-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="55a7e-109">結構化內容</span><span class="sxs-lookup"><span data-stu-id="55a7e-109">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="55a7e-110">可延伸標記語言 (XML)  (XML) 內容</span><span class="sxs-lookup"><span data-stu-id="55a7e-110">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="55a7e-111">項目資訊</span><span class="sxs-lookup"><span data-stu-id="55a7e-111">Element Information</span></span>



| <span data-ttu-id="55a7e-112">Name</span><span class="sxs-lookup"><span data-stu-id="55a7e-112">Name</span></span>                       | <span data-ttu-id="55a7e-113">值</span><span class="sxs-lookup"><span data-stu-id="55a7e-113">Value</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="55a7e-114">項目類型</span><span class="sxs-lookup"><span data-stu-id="55a7e-114">Element Type</span></span> <br/>   | <span data-ttu-id="55a7e-115">功能</span><span class="sxs-lookup"><span data-stu-id="55a7e-115">Feature</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="55a7e-116">範圍前置詞</span><span class="sxs-lookup"><span data-stu-id="55a7e-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="55a7e-117">頁面</span><span class="sxs-lookup"><span data-stu-id="55a7e-117">Page</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="55a7e-118">備註</span><span class="sxs-lookup"><span data-stu-id="55a7e-118">Notes</span></span> <br/>          | <span data-ttu-id="55a7e-119">符合 XPS 規範的取用者必須在列印功能檔或 PrintTicket 中，強制資源的 URI 參考（例如影像或色彩設定檔）必須參考元件名稱， (在包含結果 PrintTicket 的相同 XPS 檔封裝內的封裝根目錄) 的相對 URI。</span><span class="sxs-lookup"><span data-stu-id="55a7e-119">XPS-compliant consumers MUST enforce that a URI reference to a resource such as an image or color profile in either a Print Capabilities document or PrintTicket MUST refer to a part name (a relative URI to the package root) within the same XPS Document package that contains the resultant PrintTicket.</span></span> <span data-ttu-id="55a7e-120">相容的 XPS 取用者不能使用不符合元件名稱語法規范的 URI。</span><span class="sxs-lookup"><span data-stu-id="55a7e-120">A compliant XPS consumer MUST NOT use a URI that is not compliant with the part name syntax.</span></span> <span data-ttu-id="55a7e-121">這些設定是 XPS 專用的。</span><span class="sxs-lookup"><span data-stu-id="55a7e-121">These settings are XPS specific.</span></span> <br/> <span data-ttu-id="55a7e-122">在列印功能檔或 PrintTicket 中參考的 Uri 不得解析為 Url。</span><span class="sxs-lookup"><span data-stu-id="55a7e-122">URIs which are referenced in either a Print Capabilities document or PrintTicket MUST NOT be resolved as URLs.</span></span> <span data-ttu-id="55a7e-123">這是不安全的，因為它們可能無法如預期地解決，而且可能會產生驅動程式和作業系統的有害安全性風險。</span><span class="sxs-lookup"><span data-stu-id="55a7e-123">This is unsafe as they may not resolve as intended and may create harmful security risks for the driver and operating system.</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="55a7e-124">結構化內容</span><span class="sxs-lookup"><span data-stu-id="55a7e-124">Structural Content</span></span>

<span data-ttu-id="55a7e-125">此元素的 XML 結構為：</span><span class="sxs-lookup"><span data-stu-id="55a7e-125">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:PageSourceColorProfile">
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

## <a name="structure-variables"></a><span data-ttu-id="55a7e-126">結構變數</span><span class="sxs-lookup"><span data-stu-id="55a7e-126">Structure Variables</span></span>

<span data-ttu-id="55a7e-127">下表概述 XML 結構中所定義之變數的特性。</span><span class="sxs-lookup"><span data-stu-id="55a7e-127">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="55a7e-128">Name</span><span class="sxs-lookup"><span data-stu-id="55a7e-128">Name</span></span>                               | <span data-ttu-id="55a7e-129">資料類型</span><span class="sxs-lookup"><span data-stu-id="55a7e-129">Data type</span></span>         | <span data-ttu-id="55a7e-130">單位</span><span class="sxs-lookup"><span data-stu-id="55a7e-130">Unit</span></span>                  | <span data-ttu-id="55a7e-131">支援的值</span><span class="sxs-lookup"><span data-stu-id="55a7e-131">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="55a7e-132">總結</span><span class="sxs-lookup"><span data-stu-id="55a7e-132">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="55a7e-133">\_選項名稱\_</span><span class="sxs-lookup"><span data-stu-id="55a7e-133">\_OptionName\_</span></span><br/>          | <span data-ttu-id="55a7e-134">string</span><span class="sxs-lookup"><span data-stu-id="55a7e-134">string</span></span><br/> | <span data-ttu-id="55a7e-135">字元</span><span class="sxs-lookup"><span data-stu-id="55a7e-135">characters</span></span><br/> | <span data-ttu-id="55a7e-136">以 [XML 命名空間](https://www.w3.org/TR/1999/REC-xml-names-19990114/)所定義的有效完整名稱。</span><span class="sxs-lookup"><span data-stu-id="55a7e-136">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="55a7e-137">如果未指定命名空間，則會假設為預設命名空間。</span><span class="sxs-lookup"><span data-stu-id="55a7e-137">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="55a7e-138">選項的名稱。</span><span class="sxs-lookup"><span data-stu-id="55a7e-138">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="55a7e-139">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="55a7e-139">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="55a7e-140">string</span><span class="sxs-lookup"><span data-stu-id="55a7e-140">string</span></span><br/> | <span data-ttu-id="55a7e-141">n/a</span><span class="sxs-lookup"><span data-stu-id="55a7e-141">n/a</span></span><br/>        | <span data-ttu-id="55a7e-142">True、False。</span><span class="sxs-lookup"><span data-stu-id="55a7e-142">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="55a7e-143">定義選項，當選取此選項時，會停用此功能。</span><span class="sxs-lookup"><span data-stu-id="55a7e-143">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="55a7e-144">可延伸標記語言 (XML)  (XML) 內容</span><span class="sxs-lookup"><span data-stu-id="55a7e-144">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="55a7e-145">公用列印架構關鍵字是在 https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords 命名空間中定義。</span><span class="sxs-lookup"><span data-stu-id="55a7e-145">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="55a7e-146">此關鍵字的 public 可延伸標記語言 (XML)  (XML) 內容定義如下：</span><span class="sxs-lookup"><span data-stu-id="55a7e-146">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:PageSourceColorProfile">
  <psf:Option name="psk:RGB">
    <!-- Source profile used to perform color management for untagged RGB data. -->
    <psf:ScoredProperty name="psk:SourceColorProfileURI">
      <psf:ParameterRef name="psk:PageSourceColorProfileURI" />
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:SourceColorProfileEmbedded">
      <psf:ParameterRef name="psk:PageSourceColorProfileEmbedded" />
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:CMYK">
    <!-- Source profile used to perform color management for untagged CMYK data. -->
    <psf:ScoredProperty name="psk:SourceColorProfileURI">
      <psf:ParameterRef name="psk:PageSourceColorProfileURI" />
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:SourceColorProfileEmbedded">
      <psf:ParameterRef name="psk:PageSourceColorProfileEmbedded" />
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:None" />
</psf:Feature>
```

## <a name="related-topics"></a><span data-ttu-id="55a7e-147">相關主題</span><span class="sxs-lookup"><span data-stu-id="55a7e-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="55a7e-148">列印架構規格</span><span class="sxs-lookup"><span data-stu-id="55a7e-148">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




