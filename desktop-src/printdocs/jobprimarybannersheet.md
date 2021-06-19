---
description: 深入瞭解 JobPrimaryBannerSheet 元素，其描述要輸出作業的橫幅工作表。
ms.assetid: c8f9001e-9f92-405a-8f3a-bc59b47c9e35
title: JobPrimaryBannerSheet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39922f65d71ea0cc6d6de6103bc159f79467038f
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/19/2021
ms.locfileid: "112408751"
---
# <a name="jobprimarybannersheet"></a><span data-ttu-id="1acda-103">JobPrimaryBannerSheet</span><span class="sxs-lookup"><span data-stu-id="1acda-103">JobPrimaryBannerSheet</span></span>

<span data-ttu-id="1acda-104">本主題並非最新的。</span><span class="sxs-lookup"><span data-stu-id="1acda-104">This topic is not current.</span></span> <span data-ttu-id="1acda-105">如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。</span><span class="sxs-lookup"><span data-stu-id="1acda-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="1acda-106">描述要為作業輸出的橫幅工作表。</span><span class="sxs-lookup"><span data-stu-id="1acda-106">Describes the banner sheet to be output for the job.</span></span> <span data-ttu-id="1acda-107">橫幅工作表應該會輸出在預設 PageMediaSize 上，並使用預設 PageMediaType。</span><span class="sxs-lookup"><span data-stu-id="1acda-107">The banner sheet should be output on the default PageMediaSize and using the default PageMediaType.</span></span> <span data-ttu-id="1acda-108">橫幅工作表應該與作業的其餘部分隔離。</span><span class="sxs-lookup"><span data-stu-id="1acda-108">The banner sheet should be isolated from the remainder of the job.</span></span> <span data-ttu-id="1acda-109">這表示任何 (（例如 JobDuplexAllDocumentsContiguously、JobStapleAllDocuments 或) JobBindAllDocuments）的精加工或處理選項都不應包含橫幅工作表。</span><span class="sxs-lookup"><span data-stu-id="1acda-109">This means that any finishing or processing options (such as JobDuplexAllDocumentsContiguously, JobStapleAllDocuments, or JobBindAllDocuments) should not include the banner sheet.</span></span> <span data-ttu-id="1acda-110">橫幅工作表應該會以工作的第一個工作表的形式出現。</span><span class="sxs-lookup"><span data-stu-id="1acda-110">The banner sheet should occur as the first sheet of the job.</span></span>

-   [<span data-ttu-id="1acda-111">項目資訊</span><span class="sxs-lookup"><span data-stu-id="1acda-111">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="1acda-112">結構化內容</span><span class="sxs-lookup"><span data-stu-id="1acda-112">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="1acda-113">可延伸標記語言 (XML)  (XML) 內容</span><span class="sxs-lookup"><span data-stu-id="1acda-113">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="1acda-114">項目資訊</span><span class="sxs-lookup"><span data-stu-id="1acda-114">Element Information</span></span>



| <span data-ttu-id="1acda-115">Name</span><span class="sxs-lookup"><span data-stu-id="1acda-115">Name</span></span> | <span data-ttu-id="1acda-116">值</span><span class="sxs-lookup"><span data-stu-id="1acda-116">Value</span></span> |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1acda-117">項目類型</span><span class="sxs-lookup"><span data-stu-id="1acda-117">Element Type</span></span> <br/>   | <span data-ttu-id="1acda-118">功能</span><span class="sxs-lookup"><span data-stu-id="1acda-118">Feature</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="1acda-119">範圍前置詞</span><span class="sxs-lookup"><span data-stu-id="1acda-119">Scoping Prefix</span></span> <br/> | <span data-ttu-id="1acda-120">工作 (Job)</span><span class="sxs-lookup"><span data-stu-id="1acda-120">Job</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="1acda-121">備註</span><span class="sxs-lookup"><span data-stu-id="1acda-121">Notes</span></span> <br/>          | <span data-ttu-id="1acda-122">符合 XPS 規範的取用者必須在列印功能檔或 PrintTicket 中，強制資源的 URI 參考（例如影像或色彩設定檔）必須參考元件名稱， (在包含結果 PrintTicket 的相同 XPS 檔封裝內的封裝根目錄) 的相對 URI。</span><span class="sxs-lookup"><span data-stu-id="1acda-122">XPS-compliant consumers MUST enforce that a URI reference to a resource such as an image or color profile in either a Print Capabilities document or PrintTicket MUST refer to a part name (a relative URI to the package root) within the same XPS Document package that contains the resultant PrintTicket.</span></span> <span data-ttu-id="1acda-123">相容的 XPS 取用者不能使用不符合元件名稱語法規范的 URI。</span><span class="sxs-lookup"><span data-stu-id="1acda-123">A compliant XPS consumer MUST NOT use a URI that is not compliant with the part name syntax.</span></span> <span data-ttu-id="1acda-124">這些設定是 XPS 專用的。</span><span class="sxs-lookup"><span data-stu-id="1acda-124">These settings are XPS specific.</span></span> <br/> <span data-ttu-id="1acda-125">在列印功能檔或 PrintTicket 中參考的 Uri 不得解析為 Url。</span><span class="sxs-lookup"><span data-stu-id="1acda-125">URIs which are referenced in either a Print Capabilities document or PrintTicket MUST NOT be resolved as URLs.</span></span> <span data-ttu-id="1acda-126">這是不安全的，因為它們可能無法如預期地解決，而且可能會產生驅動程式和作業系統的有害安全性風險。</span><span class="sxs-lookup"><span data-stu-id="1acda-126">This is unsafe as they may not resolve as intended and may create harmful security risks for the driver and operating system.</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="1acda-127">結構化內容</span><span class="sxs-lookup"><span data-stu-id="1acda-127">Structural Content</span></span>

<span data-ttu-id="1acda-128">此元素的 XML 結構為：</span><span class="sxs-lookup"><span data-stu-id="1acda-128">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:JobPrimaryBannerSheet">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option name="psk:_OptionName_">
    <psf:Property name="psf:IdentityOption">
      <psf:Value xsi:type="xs:string">_IdentityOptionValue_</psf:Value>
    </psf:Property>
    <!-- Specifies the XPS part name for the banner sheet. -->
    <psf:ScoredProperty name="psk:BannerSheetSource">
      <psf:ParameterRef name="psk:JobPrimaryBannerSheetSource" />
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature>
```

## <a name="structure-variables"></a><span data-ttu-id="1acda-129">結構變數</span><span class="sxs-lookup"><span data-stu-id="1acda-129">Structure Variables</span></span>

<span data-ttu-id="1acda-130">下表概述 XML 結構中所定義之變數的特性。</span><span class="sxs-lookup"><span data-stu-id="1acda-130">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="1acda-131">Name</span><span class="sxs-lookup"><span data-stu-id="1acda-131">Name</span></span>                               | <span data-ttu-id="1acda-132">資料類型</span><span class="sxs-lookup"><span data-stu-id="1acda-132">Data type</span></span>         | <span data-ttu-id="1acda-133">單位</span><span class="sxs-lookup"><span data-stu-id="1acda-133">Unit</span></span>                  | <span data-ttu-id="1acda-134">支援的值</span><span class="sxs-lookup"><span data-stu-id="1acda-134">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="1acda-135">總結</span><span class="sxs-lookup"><span data-stu-id="1acda-135">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="1acda-136">\_選項名稱\_</span><span class="sxs-lookup"><span data-stu-id="1acda-136">\_OptionName\_</span></span><br/>          | <span data-ttu-id="1acda-137">string</span><span class="sxs-lookup"><span data-stu-id="1acda-137">string</span></span><br/> | <span data-ttu-id="1acda-138">字元</span><span class="sxs-lookup"><span data-stu-id="1acda-138">characters</span></span><br/> | <span data-ttu-id="1acda-139">以 [XML 命名空間](https://www.w3.org/TR/1999/REC-xml-names-19990114/)所定義的有效完整名稱。</span><span class="sxs-lookup"><span data-stu-id="1acda-139">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="1acda-140">如果未指定命名空間，則會假設為預設命名空間。</span><span class="sxs-lookup"><span data-stu-id="1acda-140">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="1acda-141">選項的名稱。</span><span class="sxs-lookup"><span data-stu-id="1acda-141">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="1acda-142">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="1acda-142">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="1acda-143">string</span><span class="sxs-lookup"><span data-stu-id="1acda-143">string</span></span><br/> | <span data-ttu-id="1acda-144">n/a</span><span class="sxs-lookup"><span data-stu-id="1acda-144">n/a</span></span><br/>        | <span data-ttu-id="1acda-145">True、False。</span><span class="sxs-lookup"><span data-stu-id="1acda-145">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="1acda-146">定義選項，當選取此選項時，會停用此功能。</span><span class="sxs-lookup"><span data-stu-id="1acda-146">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="1acda-147">可延伸標記語言 (XML)  (XML) 內容</span><span class="sxs-lookup"><span data-stu-id="1acda-147">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="1acda-148">公用列印架構關鍵字是在 https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords 命名空間中定義。</span><span class="sxs-lookup"><span data-stu-id="1acda-148">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="1acda-149">此關鍵字的 public 可延伸標記語言 (XML)  (XML) 內容定義如下：</span><span class="sxs-lookup"><span data-stu-id="1acda-149">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:JobPrimaryBannerSheet">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!-- Specifies a custom banner sheet should be output. If a JobPrimaryBannerSheetSource 
     ParameterInit element is not specified, this Option should be ignored.  -->
  <psf:Option name="psk:Custom">
    <psf:ScoredProperty name="psk:BannerSheetSource">
      <psf:ParameterRef name="psk:JobPrimaryBannerSheetSource" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies no banner sheet should be output. -->
  <psf:Option name="psk:None" />
  <!-- Specifies the standard (device defined) banner sheet should be output. -->
  <psf:Option name="psk:Standard" />
</psf:Feature>
```

## <a name="related-topics"></a><span data-ttu-id="1acda-150">相關主題</span><span class="sxs-lookup"><span data-stu-id="1acda-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1acda-151">列印架構規格</span><span class="sxs-lookup"><span data-stu-id="1acda-151">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




