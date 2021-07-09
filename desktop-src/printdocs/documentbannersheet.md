---
description: 閱讀 DocumentBannerSheet 使用者可設定的元素。 本主題並非最新的。 如需最新資訊，請參閱列印架構規格。
ms.assetid: c10da176-946a-4439-8ad7-037013b39e41
title: DocumentBannerSheet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80ce05ffae190835e4a8b4082c634b34e26103ab
ms.sourcegitcommit: 998d50f6def8a25850fc113fc8a2df903c829c5e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/09/2021
ms.locfileid: "113548766"
---
# <a name="documentbannersheet"></a><span data-ttu-id="cfa44-105">DocumentBannerSheet</span><span class="sxs-lookup"><span data-stu-id="cfa44-105">DocumentBannerSheet</span></span>

<span data-ttu-id="cfa44-106">本主題並非最新的。</span><span class="sxs-lookup"><span data-stu-id="cfa44-106">This topic is not current.</span></span> <span data-ttu-id="cfa44-107">如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。</span><span class="sxs-lookup"><span data-stu-id="cfa44-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="cfa44-108">描述要為特定檔輸出的橫幅工作表。</span><span class="sxs-lookup"><span data-stu-id="cfa44-108">Describes the banner sheet to be output for a particular document.</span></span> <span data-ttu-id="cfa44-109">橫幅工作表應該會使用預設 PageMediaType 輸出在預設 PageMediaSize 上。</span><span class="sxs-lookup"><span data-stu-id="cfa44-109">The banner sheet should be output on the default PageMediaSize ,using the default PageMediaType.</span></span> <span data-ttu-id="cfa44-110">橫幅工作表也應該與檔的其餘部分隔離。</span><span class="sxs-lookup"><span data-stu-id="cfa44-110">The banner sheet should also be isolated from the remainder of the document.</span></span> <span data-ttu-id="cfa44-111">這表示任何檔完成或處理選項 (例如 DocumentDuplex、DocumentStaple 或 DocumentBinding) 不應包含橫幅工作表。</span><span class="sxs-lookup"><span data-stu-id="cfa44-111">This means that any document finishing or processing options (such as DocumentDuplex, DocumentStaple, or DocumentBinding) should not include the banner sheet.</span></span> <span data-ttu-id="cfa44-112">橫幅工作表可能不會與作業的其餘部分隔離。</span><span class="sxs-lookup"><span data-stu-id="cfa44-112">The banner sheet may or may not be isolated from the remainder of the job.</span></span> <span data-ttu-id="cfa44-113">這表示任何工作完成或處理選項，都可能包含檔橫幅表。</span><span class="sxs-lookup"><span data-stu-id="cfa44-113">This means that any job finishing or processing options, may include the document banner sheet.</span></span> <span data-ttu-id="cfa44-114">橫幅工作表應該會以檔的第一頁的形式出現。</span><span class="sxs-lookup"><span data-stu-id="cfa44-114">The banner sheet should occur as the first sheet of the document.</span></span>

-   [<span data-ttu-id="cfa44-115">項目資訊</span><span class="sxs-lookup"><span data-stu-id="cfa44-115">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="cfa44-116">結構化內容</span><span class="sxs-lookup"><span data-stu-id="cfa44-116">Structural Content</span></span>](#structural-content)

## <a name="element-information"></a><span data-ttu-id="cfa44-117">項目資訊</span><span class="sxs-lookup"><span data-stu-id="cfa44-117">Element Information</span></span>



| <span data-ttu-id="cfa44-118">Name</span><span class="sxs-lookup"><span data-stu-id="cfa44-118">Name</span></span> | <span data-ttu-id="cfa44-119">值</span><span class="sxs-lookup"><span data-stu-id="cfa44-119">Value</span></span> |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cfa44-120">項目類型</span><span class="sxs-lookup"><span data-stu-id="cfa44-120">Element Type</span></span> <br/>   | <span data-ttu-id="cfa44-121">功能</span><span class="sxs-lookup"><span data-stu-id="cfa44-121">Feature</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="cfa44-122">範圍前置詞</span><span class="sxs-lookup"><span data-stu-id="cfa44-122">Scoping Prefix</span></span> <br/> | <span data-ttu-id="cfa44-123">文件</span><span class="sxs-lookup"><span data-stu-id="cfa44-123">Document</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="cfa44-124">備註</span><span class="sxs-lookup"><span data-stu-id="cfa44-124">Notes</span></span> <br/>          | <span data-ttu-id="cfa44-125">符合 XPS 規範的取用者必須在列印功能檔或 PrintTicket 中，強制資源的 URI 參考（例如影像或色彩設定檔）必須參考元件名稱， (在包含結果 PrintTicket 的相同 XPS 檔封裝內的封裝根目錄) 的相對 URI。</span><span class="sxs-lookup"><span data-stu-id="cfa44-125">XPS-compliant consumers MUST enforce that a URI reference to a resource such as an image or color profile in either a Print Capabilities document or PrintTicket MUST refer to a part name (a relative URI to the package root) within the same XPS Document package that contains the resultant PrintTicket.</span></span> <span data-ttu-id="cfa44-126">相容的 XPS 取用者不能使用不符合元件名稱語法規范的 URI。</span><span class="sxs-lookup"><span data-stu-id="cfa44-126">A compliant XPS consumer MUST NOT use a URI that is not compliant with the part name syntax.</span></span> <span data-ttu-id="cfa44-127">這些設定是 XPS 專用的。</span><span class="sxs-lookup"><span data-stu-id="cfa44-127">These settings are XPS specific.</span></span> <br/> <span data-ttu-id="cfa44-128">在列印功能檔或 PrintTicket 中參考的 Uri 不得解析為 Url。</span><span class="sxs-lookup"><span data-stu-id="cfa44-128">URIs which are referenced in either a Print Capabilities document or PrintTicket MUST NOT be resolved as URLs.</span></span> <span data-ttu-id="cfa44-129">這是不安全的，因為它們可能無法如預期地解決，而且可能會產生驅動程式和作業系統的有害安全性風險。</span><span class="sxs-lookup"><span data-stu-id="cfa44-129">This is unsafe as they may not resolve as intended and may create harmful security risks for the driver and operating system.</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="cfa44-130">結構化內容</span><span class="sxs-lookup"><span data-stu-id="cfa44-130">Structural Content</span></span>

<span data-ttu-id="cfa44-131">此元素的 XML 結構為：</span><span class="sxs-lookup"><span data-stu-id="cfa44-131">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:DocumentBannerSheet">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option name="psk:_OptionName_">
    <psf:Property name="psf:IdentityOption">
      <psf:Value xsi:type="xs:string">_IdentityOptionValue_</psf:Value>
    </psf:Property>
    <!-- Specifies the XPS specific part name -->
    <psf:ScoredProperty name="psk:BannerSheetSource">
      <psf:ParameterRef name="psk:DocumentBannerSheetSource" />
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature>
```

## <a name="structure-variables"></a><span data-ttu-id="cfa44-132">結構變數</span><span class="sxs-lookup"><span data-stu-id="cfa44-132">Structure Variables</span></span>

<span data-ttu-id="cfa44-133">下表概述 XML 結構中所定義之變數的特性。</span><span class="sxs-lookup"><span data-stu-id="cfa44-133">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="cfa44-134">Name</span><span class="sxs-lookup"><span data-stu-id="cfa44-134">Name</span></span>                               | <span data-ttu-id="cfa44-135">資料類型</span><span class="sxs-lookup"><span data-stu-id="cfa44-135">Data type</span></span>         | <span data-ttu-id="cfa44-136">單位</span><span class="sxs-lookup"><span data-stu-id="cfa44-136">Unit</span></span>                   | <span data-ttu-id="cfa44-137">支援的值</span><span class="sxs-lookup"><span data-stu-id="cfa44-137">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="cfa44-138">摘要</span><span class="sxs-lookup"><span data-stu-id="cfa44-138">Summary</span></span>                                                                      |
|------------------------------------|-------------------|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="cfa44-139">\_選項名稱\_</span><span class="sxs-lookup"><span data-stu-id="cfa44-139">\_OptionName\_</span></span><br/>          | <span data-ttu-id="cfa44-140">string</span><span class="sxs-lookup"><span data-stu-id="cfa44-140">string</span></span><br/> | <span data-ttu-id="cfa44-141">字元</span><span class="sxs-lookup"><span data-stu-id="cfa44-141">characters</span></span> <br/> | <span data-ttu-id="cfa44-142">以 [XML 命名空間](https://www.w3.org/TR/1999/REC-xml-names-19990114/)所定義的有效完整名稱。</span><span class="sxs-lookup"><span data-stu-id="cfa44-142">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="cfa44-143">如果未指定命名空間，則會假設為預設命名空間。</span><span class="sxs-lookup"><span data-stu-id="cfa44-143">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="cfa44-144">選項的名稱。</span><span class="sxs-lookup"><span data-stu-id="cfa44-144">The name of the option</span></span><br/>                                            |
| <span data-ttu-id="cfa44-145">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="cfa44-145">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="cfa44-146">string</span><span class="sxs-lookup"><span data-stu-id="cfa44-146">string</span></span><br/> | <span data-ttu-id="cfa44-147">n/a</span><span class="sxs-lookup"><span data-stu-id="cfa44-147">n/a</span></span><br/>         | <span data-ttu-id="cfa44-148">True、False</span><span class="sxs-lookup"><span data-stu-id="cfa44-148">True, False</span></span><br/>                                                                                                                                                                | <span data-ttu-id="cfa44-149">定義選項，當選取此選項時，會停用此功能。</span><span class="sxs-lookup"><span data-stu-id="cfa44-149">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="cfa44-150">可延伸標記語言 (XML)  (XML) 內容</span><span class="sxs-lookup"><span data-stu-id="cfa44-150">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="cfa44-151">公用列印架構關鍵字是在 https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords 命名空間中定義。</span><span class="sxs-lookup"><span data-stu-id="cfa44-151">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="cfa44-152">此關鍵字的 public 可延伸標記語言 (XML)  (XML) 內容定義如下：</span><span class="sxs-lookup"><span data-stu-id="cfa44-152">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:DocumentBannerSheet">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!-- Specifies a custom banner sheet should be output. If a DocumentBannerSheetSource 
     ParameterInit element is not specified, this Option should be ignored. -->
  <psf:Option name="psk:Custom">
    <psf:ScoredProperty name="psk:BannerSheetSource">
      <psf:ParameterRef name="psk:DocumentBannerSheetSource" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies no banner sheet should be output. -->
  <psf:Option name="psk:None" />
  <!-- Specifies the standard (device defined) banner sheet should be output. -->
  <psf:Option name="psk:Standard" />
</psf:Feature>
```

## <a name="related-topics"></a><span data-ttu-id="cfa44-153">相關主題</span><span class="sxs-lookup"><span data-stu-id="cfa44-153">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cfa44-154">列印架構規格</span><span class="sxs-lookup"><span data-stu-id="cfa44-154">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




