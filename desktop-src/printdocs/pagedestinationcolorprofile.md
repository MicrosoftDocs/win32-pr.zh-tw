---
description: 本主題並非最新的。 如需最新資訊，請參閱列印架構規格。
ms.assetid: 1a6ff76a-0818-464a-bf75-534dc7ea383f
title: PageDestinationColorProfile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fde6077bc2bae611c2a791ecf041cb52588c2ebb
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/06/2021
ms.locfileid: "106992248"
---
# <a name="pagedestinationcolorprofile"></a><span data-ttu-id="5ef34-104">PageDestinationColorProfile</span><span class="sxs-lookup"><span data-stu-id="5ef34-104">PageDestinationColorProfile</span></span>

<span data-ttu-id="5ef34-105">本主題並非最新的。</span><span class="sxs-lookup"><span data-stu-id="5ef34-105">This topic is not current.</span></span> <span data-ttu-id="5ef34-106">如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。</span><span class="sxs-lookup"><span data-stu-id="5ef34-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="5ef34-107">定義目的地色彩設定檔的特性。</span><span class="sxs-lookup"><span data-stu-id="5ef34-107">Defines the characteristics of the destination color profile.</span></span> <span data-ttu-id="5ef34-108">描述應用程式或驅動程式是否選取要使用的目的地色彩設定檔。</span><span class="sxs-lookup"><span data-stu-id="5ef34-108">Describes whether the application or driver selects the destination color profile to be used.</span></span>

-   [<span data-ttu-id="5ef34-109">項目資訊</span><span class="sxs-lookup"><span data-stu-id="5ef34-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="5ef34-110">結構化內容</span><span class="sxs-lookup"><span data-stu-id="5ef34-110">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="5ef34-111">可延伸標記語言 (XML)  (XML) 內容</span><span class="sxs-lookup"><span data-stu-id="5ef34-111">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="5ef34-112">項目資訊</span><span class="sxs-lookup"><span data-stu-id="5ef34-112">Element Information</span></span>



| <span data-ttu-id="5ef34-113">Name</span><span class="sxs-lookup"><span data-stu-id="5ef34-113">Name</span></span>                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5ef34-114">項目類型</span><span class="sxs-lookup"><span data-stu-id="5ef34-114">Element Type</span></span> <br/>   | <span data-ttu-id="5ef34-115">功能</span><span class="sxs-lookup"><span data-stu-id="5ef34-115">Feature</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="5ef34-116">範圍前置詞</span><span class="sxs-lookup"><span data-stu-id="5ef34-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="5ef34-117">頁面</span><span class="sxs-lookup"><span data-stu-id="5ef34-117">Page</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="5ef34-118">備註</span><span class="sxs-lookup"><span data-stu-id="5ef34-118">Notes</span></span> <br/>          | <span data-ttu-id="5ef34-119">符合 XPS 規範的取用者必須在列印功能檔或 PrintTicket 中，強制資源的 URI 參考（例如影像或色彩設定檔）必須參考元件名稱， (在包含結果 PrintTicket 的相同 XPS 檔封裝內的封裝根目錄) 的相對 URI。</span><span class="sxs-lookup"><span data-stu-id="5ef34-119">XPS-compliant consumers MUST enforce that a URI reference to a resource such as an image or color profile in either a Print Capabilities document or PrintTicket MUST refer to a part name (a relative URI to the package root) within the same XPS Document package that contains the resultant PrintTicket.</span></span> <span data-ttu-id="5ef34-120">相容的 XPS 取用者不能使用不符合元件名稱語法規范的 URI。</span><span class="sxs-lookup"><span data-stu-id="5ef34-120">A compliant XPS consumer MUST NOT use a URI that is not compliant with the part name syntax.</span></span> <span data-ttu-id="5ef34-121">這些設定是 XPS 專用的。</span><span class="sxs-lookup"><span data-stu-id="5ef34-121">These settings are XPS specific.</span></span> <br/> <span data-ttu-id="5ef34-122">在列印功能檔或 PrintTicket 中參考的 Uri 不得解析為 Url。</span><span class="sxs-lookup"><span data-stu-id="5ef34-122">URIs which are referenced in either a Print Capabilities document or PrintTicket MUST NOT be resolved as URLs.</span></span> <span data-ttu-id="5ef34-123">這是不安全的，因為它們可能無法如預期地解決，而且可能會產生驅動程式和作業系統的有害安全性風險。</span><span class="sxs-lookup"><span data-stu-id="5ef34-123">This is unsafe as they may not resolve as intended and may create harmful security risks for the driver and operating system.</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="5ef34-124">結構化內容</span><span class="sxs-lookup"><span data-stu-id="5ef34-124">Structural Content</span></span>

<span data-ttu-id="5ef34-125">此元素的 XML 結構為：</span><span class="sxs-lookup"><span data-stu-id="5ef34-125">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:PageDestinationColorProfile">
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

## <a name="structure-variables"></a><span data-ttu-id="5ef34-126">結構變數</span><span class="sxs-lookup"><span data-stu-id="5ef34-126">Structure Variables</span></span>

<span data-ttu-id="5ef34-127">下表概述 XML 結構中所定義之變數的特性。</span><span class="sxs-lookup"><span data-stu-id="5ef34-127">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="5ef34-128">Name</span><span class="sxs-lookup"><span data-stu-id="5ef34-128">Name</span></span>                               | <span data-ttu-id="5ef34-129">資料類型</span><span class="sxs-lookup"><span data-stu-id="5ef34-129">Data type</span></span>         | <span data-ttu-id="5ef34-130">單位</span><span class="sxs-lookup"><span data-stu-id="5ef34-130">Unit</span></span>                  | <span data-ttu-id="5ef34-131">支援的值</span><span class="sxs-lookup"><span data-stu-id="5ef34-131">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="5ef34-132">總結</span><span class="sxs-lookup"><span data-stu-id="5ef34-132">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="5ef34-133">\_選項名稱\_</span><span class="sxs-lookup"><span data-stu-id="5ef34-133">\_OptionName\_</span></span><br/>          | <span data-ttu-id="5ef34-134">字串</span><span class="sxs-lookup"><span data-stu-id="5ef34-134">string</span></span><br/> | <span data-ttu-id="5ef34-135">字元</span><span class="sxs-lookup"><span data-stu-id="5ef34-135">characters</span></span><br/> | <span data-ttu-id="5ef34-136">以 [XML 命名空間](https://www.w3.org/TR/1999/REC-xml-names-19990114/)所定義的有效完整名稱。</span><span class="sxs-lookup"><span data-stu-id="5ef34-136">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="5ef34-137">如果未指定命名空間，則會假設為預設命名空間。</span><span class="sxs-lookup"><span data-stu-id="5ef34-137">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="5ef34-138">選項的名稱。</span><span class="sxs-lookup"><span data-stu-id="5ef34-138">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="5ef34-139">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="5ef34-139">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="5ef34-140">字串</span><span class="sxs-lookup"><span data-stu-id="5ef34-140">string</span></span><br/> | <span data-ttu-id="5ef34-141">n/a</span><span class="sxs-lookup"><span data-stu-id="5ef34-141">n/a</span></span><br/>        | <span data-ttu-id="5ef34-142">True、False。</span><span class="sxs-lookup"><span data-stu-id="5ef34-142">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="5ef34-143">定義選項，當選取此選項時，會停用此功能。</span><span class="sxs-lookup"><span data-stu-id="5ef34-143">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="5ef34-144">可延伸標記語言 (XML)  (XML) 內容</span><span class="sxs-lookup"><span data-stu-id="5ef34-144">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="5ef34-145">公用列印架構關鍵字是在 https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords 命名空間中定義。</span><span class="sxs-lookup"><span data-stu-id="5ef34-145">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="5ef34-146">此關鍵字的 public 可延伸標記語言 (XML)  (XML) 內容定義如下：</span><span class="sxs-lookup"><span data-stu-id="5ef34-146">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:PageDestinationColorProfile">
  <!-- Application specifies the destination profile to be used. -->
  <psf:Option name="psk:Application">
    <!-- Destination profile used to perform color management. -->
    <psf:ScoredProperty name="psk:DestinationColorProfileURI">
      <psf:ParameterRef name="psk:PageDestinationColorProfileURI" />
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:DestinationColorProfileEmbedded">
      <psf:ParameterRef name="psk:PageDestinationColorProfileEmbedded" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Driver selects the destination profile that best matches its current configuration. -->
  <psf:Option name="psk:DriverConfiguration" />
</psf:Feature>
```

## <a name="related-topics"></a><span data-ttu-id="5ef34-147">相關主題</span><span class="sxs-lookup"><span data-stu-id="5ef34-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5ef34-148">列印架構規格</span><span class="sxs-lookup"><span data-stu-id="5ef34-148">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




