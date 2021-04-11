---
description: 本主題並非最新的。 如需最新資訊，請參閱列印架構規格。
ms.assetid: ad30df59-0051-4471-8c0e-3207bcc7bfbe
title: JobErrorSheet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ef9d613bf3b3af980b5cb8e916eac115cd1a0cb
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/06/2021
ms.locfileid: "103853552"
---
# <a name="joberrorsheet"></a><span data-ttu-id="75904-104">JobErrorSheet</span><span class="sxs-lookup"><span data-stu-id="75904-104">JobErrorSheet</span></span>

<span data-ttu-id="75904-105">本主題並非最新的。</span><span class="sxs-lookup"><span data-stu-id="75904-105">This topic is not current.</span></span> <span data-ttu-id="75904-106">如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。</span><span class="sxs-lookup"><span data-stu-id="75904-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="75904-107">描述錯誤表輸出。</span><span class="sxs-lookup"><span data-stu-id="75904-107">Describes the error sheet output.</span></span> <span data-ttu-id="75904-108">整個作業將會有一個錯誤工作表。</span><span class="sxs-lookup"><span data-stu-id="75904-108">The entire job will have a single error sheet.</span></span> <span data-ttu-id="75904-109">錯誤工作表應該會輸出在預設 PageMediaSize 上，並使用預設 PageMediaType。</span><span class="sxs-lookup"><span data-stu-id="75904-109">The error sheet should be output on the default PageMediaSize and using the default PageMediaType.</span></span> <span data-ttu-id="75904-110">錯誤工作表應該與作業的其餘部分隔離。</span><span class="sxs-lookup"><span data-stu-id="75904-110">The error sheet should to be isolated from the remainder of the job.</span></span> <span data-ttu-id="75904-111">這表示任何精加工或處理選項 (例如 JobDuplex、JobStaple 或 JobBinding) 都不應包含錯誤工作表。</span><span class="sxs-lookup"><span data-stu-id="75904-111">This means that any finishing or processing options (such as JobDuplex, JobStaple, or JobBinding) should not include the error sheet.</span></span> <span data-ttu-id="75904-112">錯誤工作表應該會以工作的最終工作表的形式出現。</span><span class="sxs-lookup"><span data-stu-id="75904-112">The error sheet should occur as the final sheet of the job.</span></span>

-   [<span data-ttu-id="75904-113">項目資訊</span><span class="sxs-lookup"><span data-stu-id="75904-113">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="75904-114">結構化內容</span><span class="sxs-lookup"><span data-stu-id="75904-114">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="75904-115">可延伸標記語言 (XML)  (XML) 內容</span><span class="sxs-lookup"><span data-stu-id="75904-115">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="75904-116">項目資訊</span><span class="sxs-lookup"><span data-stu-id="75904-116">Element Information</span></span>



| <span data-ttu-id="75904-117">Name</span><span class="sxs-lookup"><span data-stu-id="75904-117">Name</span></span>                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="75904-118">項目類型</span><span class="sxs-lookup"><span data-stu-id="75904-118">Element Type</span></span> <br/>   | <span data-ttu-id="75904-119">功能</span><span class="sxs-lookup"><span data-stu-id="75904-119">Feature</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="75904-120">範圍前置詞</span><span class="sxs-lookup"><span data-stu-id="75904-120">Scoping Prefix</span></span> <br/> | <span data-ttu-id="75904-121">工作 (Job)</span><span class="sxs-lookup"><span data-stu-id="75904-121">Job</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="75904-122">備註</span><span class="sxs-lookup"><span data-stu-id="75904-122">Notes</span></span> <br/>          | <span data-ttu-id="75904-123">符合 XPS 規範的取用者必須在列印功能檔或 PrintTicket 中，強制資源的 URI 參考（例如影像或色彩設定檔）必須參考元件名稱， (在包含結果 PrintTicket 的相同 XPS 檔封裝內的封裝根目錄) 的相對 URI。</span><span class="sxs-lookup"><span data-stu-id="75904-123">XPS-compliant consumers MUST enforce that a URI reference to a resource such as an image or color profile in either a Print Capabilities document or PrintTicket MUST refer to a part name (a relative URI to the package root) within the same XPS Document package that contains the resultant PrintTicket.</span></span> <span data-ttu-id="75904-124">相容的 XPS 取用者不能使用不符合元件名稱語法規范的 URI。</span><span class="sxs-lookup"><span data-stu-id="75904-124">A compliant XPS consumer MUST NOT use a URI that is not compliant with the part name syntax.</span></span> <span data-ttu-id="75904-125">這些設定是 XPS 專用的。</span><span class="sxs-lookup"><span data-stu-id="75904-125">These settings are XPS specific.</span></span> <br/> <span data-ttu-id="75904-126">在列印功能檔或 PrintTicket 中參考的 Uri 不得解析為 Url。</span><span class="sxs-lookup"><span data-stu-id="75904-126">URIs which are referenced in either a Print Capabilities document or PrintTicket MUST NOT be resolved as URLs.</span></span> <span data-ttu-id="75904-127">這是不安全的，因為它們可能無法如預期地解決，而且可能會產生驅動程式和作業系統的有害安全性風險。</span><span class="sxs-lookup"><span data-stu-id="75904-127">This is unsafe as they may not resolve as intended and may create harmful security risks for the driver and operating system.</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="75904-128">結構化內容</span><span class="sxs-lookup"><span data-stu-id="75904-128">Structural Content</span></span>

<span data-ttu-id="75904-129">此元素的 XML 結構為：</span><span class="sxs-lookup"><span data-stu-id="75904-129">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:JobErrorSheet">
  <!--Describes when an error sheet should be output. -->
  <psf:Feature name="psk:ErrorSheetWhen">
    <psf:Property name="psf:SelectionType">
      <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
    </psf:Property>
    <psf:Option name="psk:_ErrorSheetWhenOptionName_">
      <psf:Property name="psf:IdentityOption">
        <psf:Value xsi:type="xs:string">_ErrorSheetWhenIdentityOptionValue_</psf:Value>
      </psf:Property>
    </psf:Option>
  </psf:Feature>
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option name="psk:_OptionName_">
    <psf:Property name="psf:IdentityOption">
      <psf:Value xsi:type="xs:string">_IdentityOptionValue_</psf:Value>
    </psf:Property>
    <!-- Specifies the XPS part name for the error sheet. -->
    <psf:ScoredProperty name="psk:ErrorSheetSource">
      <psf:ParameterRef name="psk:JobErrorSheetSource" />
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature>      
```

## <a name="structure-variables"></a><span data-ttu-id="75904-130">結構變數</span><span class="sxs-lookup"><span data-stu-id="75904-130">Structure Variables</span></span>

<span data-ttu-id="75904-131">下表概述 XML 結構中所定義之變數的特性。</span><span class="sxs-lookup"><span data-stu-id="75904-131">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="75904-132">Name</span><span class="sxs-lookup"><span data-stu-id="75904-132">Name</span></span>                                             | <span data-ttu-id="75904-133">資料類型</span><span class="sxs-lookup"><span data-stu-id="75904-133">Data type</span></span>         | <span data-ttu-id="75904-134">單位</span><span class="sxs-lookup"><span data-stu-id="75904-134">Unit</span></span>                  | <span data-ttu-id="75904-135">支援的值</span><span class="sxs-lookup"><span data-stu-id="75904-135">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="75904-136">總結</span><span class="sxs-lookup"><span data-stu-id="75904-136">Summary</span></span>                                                                      |
|--------------------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="75904-137">\_ErrorSheetWhenOptionName\_</span><span class="sxs-lookup"><span data-stu-id="75904-137">\_ErrorSheetWhenOptionName\_</span></span><br/>          | <span data-ttu-id="75904-138">字串</span><span class="sxs-lookup"><span data-stu-id="75904-138">string</span></span><br/> | <span data-ttu-id="75904-139">字元</span><span class="sxs-lookup"><span data-stu-id="75904-139">characters</span></span><br/> | <span data-ttu-id="75904-140">以 [XML 命名空間](https://www.w3.org/TR/1999/REC-xml-names-19990114/)所定義的有效完整名稱。</span><span class="sxs-lookup"><span data-stu-id="75904-140">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="75904-141">如果未指定命名空間，則會假設為預設命名空間。</span><span class="sxs-lookup"><span data-stu-id="75904-141">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="75904-142">選項的名稱。</span><span class="sxs-lookup"><span data-stu-id="75904-142">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="75904-143">\_ErrorSheetWhenIdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="75904-143">\_ErrorSheetWhenIdentityOptionValue\_</span></span><br/> | <span data-ttu-id="75904-144">字串</span><span class="sxs-lookup"><span data-stu-id="75904-144">string</span></span><br/> | <span data-ttu-id="75904-145">n/a</span><span class="sxs-lookup"><span data-stu-id="75904-145">n/a</span></span><br/>        | <span data-ttu-id="75904-146">True、False。</span><span class="sxs-lookup"><span data-stu-id="75904-146">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="75904-147">定義使用者介面 (UI) 選取準則。</span><span class="sxs-lookup"><span data-stu-id="75904-147">Defines the user interface (UI) selection criteria.</span></span><br/>               |
| <span data-ttu-id="75904-148">\_選項名稱\_</span><span class="sxs-lookup"><span data-stu-id="75904-148">\_OptionName\_</span></span><br/>                        | <span data-ttu-id="75904-149">字串</span><span class="sxs-lookup"><span data-stu-id="75904-149">string</span></span><br/> | <span data-ttu-id="75904-150">n/a</span><span class="sxs-lookup"><span data-stu-id="75904-150">n/a</span></span><br/>        | <span data-ttu-id="75904-151">由定義的有效完整名稱 https://www.w3.org/TR/1999/REC-xml-names-19990114/\#dt-qname 。</span><span class="sxs-lookup"><span data-stu-id="75904-151">Valid fully qualified name as defined by https://www.w3.org/TR/1999/REC-xml-names-19990114/\#dt-qname.</span></span> <span data-ttu-id="75904-152">如果未指定命名空間，則會假設為預設命名空間。</span><span class="sxs-lookup"><span data-stu-id="75904-152">If no namespace is specified, default namespace is assumed.</span></span><br/>          | <span data-ttu-id="75904-153">選項的名稱。</span><span class="sxs-lookup"><span data-stu-id="75904-153">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="75904-154">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="75904-154">\_IdentityOptionValue\_</span></span><br/>               | <span data-ttu-id="75904-155">字串</span><span class="sxs-lookup"><span data-stu-id="75904-155">string</span></span><br/> | <span data-ttu-id="75904-156">n/a</span><span class="sxs-lookup"><span data-stu-id="75904-156">n/a</span></span><br/>        | <span data-ttu-id="75904-157">True、False。</span><span class="sxs-lookup"><span data-stu-id="75904-157">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="75904-158">定義選項，當選取此選項時，會停用此功能。</span><span class="sxs-lookup"><span data-stu-id="75904-158">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="75904-159">可延伸標記語言 (XML)  (XML) 內容</span><span class="sxs-lookup"><span data-stu-id="75904-159">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="75904-160">公用列印架構關鍵字是在 https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords 命名空間中定義。</span><span class="sxs-lookup"><span data-stu-id="75904-160">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="75904-161">此關鍵字的 public 可延伸標記語言 (XML)  (XML) 內容定義如下：</span><span class="sxs-lookup"><span data-stu-id="75904-161">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:JobErrorSheet">
  <psf:Feature name="psk:ErrorSheetWhen">
    <psf:Property name="psf:SelectionType">
      <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
    </psf:Property>
    <!-- Specifies an error sheet will be output for every job. -->
    <psf:Option name="psk:Always" />
    <!-- Specifies an error sheet will be output only on error. -->
    <psf:Option name="psk:OnError" />
  </psf:Feature>
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!-- Specifies a custom error sheet should be output. If a JobErrorSheetSource 
     ParameterInit element is not specified, this Option should be ignored. -->
  <psf:Option name="psk:Custom">
    <psf:ScoredProperty name="psk:ErrorSheetSource">
      <psf:ParameterRef name="psk:JobErrorSheetSource" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies no error sheet should be output. -->
  <psf:Option name="psk:None" />
  <!-- Specifies the standard (device defined) error sheet should be output. -->
  <psf:Option name="psk:Standard" />
</psf:Feature>    
```

## <a name="related-topics"></a><span data-ttu-id="75904-162">相關主題</span><span class="sxs-lookup"><span data-stu-id="75904-162">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="75904-163">列印架構規格</span><span class="sxs-lookup"><span data-stu-id="75904-163">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




