---
description: 深入瞭解 DocumentCoverFront 使用者可設定的元素。 本主題並非最新的。 如需最新資訊，請參閱列印架構規格。
ms.assetid: 25dbd083-5815-4b25-bfdc-4d14f96d2b45
title: DocumentCoverFront
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 301b67c9a741caa48024646854b208ac5dffbb20
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119823"
---
# <a name="documentcoverfront"></a><span data-ttu-id="ce5c7-105">DocumentCoverFront</span><span class="sxs-lookup"><span data-stu-id="ce5c7-105">DocumentCoverFront</span></span>

<span data-ttu-id="ce5c7-106">本主題並非最新的。</span><span class="sxs-lookup"><span data-stu-id="ce5c7-106">This topic is not current.</span></span> <span data-ttu-id="ce5c7-107">如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。</span><span class="sxs-lookup"><span data-stu-id="ce5c7-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="ce5c7-108">描述) 封面頁開始 (。</span><span class="sxs-lookup"><span data-stu-id="ce5c7-108">Describes the front (beginning) cover sheet.</span></span> <span data-ttu-id="ce5c7-109">每份檔都有個別的工作表。</span><span class="sxs-lookup"><span data-stu-id="ce5c7-109">Each document will have a separate sheet.</span></span> <span data-ttu-id="ce5c7-110">在檔的第一頁所使用的 PageMediaSize 和 PageMediaType 上，應該列印封面表。</span><span class="sxs-lookup"><span data-stu-id="ce5c7-110">The cover sheet should be printed on the PageMediaSize and PageMediaType used for the first page of the document.</span></span> <span data-ttu-id="ce5c7-111">封面工作表應該整合至處理選項 (例如 DocumentDuplex、DocumentNUp) ，如指定的選項所指定。</span><span class="sxs-lookup"><span data-stu-id="ce5c7-111">The cover sheet should be integrated into processing options (such as DocumentDuplex, DocumentNUp) as indicated by the Option specified.</span></span>

-   [<span data-ttu-id="ce5c7-112">項目資訊</span><span class="sxs-lookup"><span data-stu-id="ce5c7-112">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="ce5c7-113">結構化內容</span><span class="sxs-lookup"><span data-stu-id="ce5c7-113">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="ce5c7-114">可延伸標記語言 (XML)  (XML) 內容</span><span class="sxs-lookup"><span data-stu-id="ce5c7-114">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="ce5c7-115">項目資訊</span><span class="sxs-lookup"><span data-stu-id="ce5c7-115">Element Information</span></span>



| <span data-ttu-id="ce5c7-116">Name</span><span class="sxs-lookup"><span data-stu-id="ce5c7-116">Name</span></span> | <span data-ttu-id="ce5c7-117">值</span><span class="sxs-lookup"><span data-stu-id="ce5c7-117">Value</span></span> |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ce5c7-118">項目類型</span><span class="sxs-lookup"><span data-stu-id="ce5c7-118">Element Type</span></span> <br/>   | <span data-ttu-id="ce5c7-119">功能</span><span class="sxs-lookup"><span data-stu-id="ce5c7-119">Feature</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="ce5c7-120">範圍前置詞</span><span class="sxs-lookup"><span data-stu-id="ce5c7-120">Scoping Prefix</span></span> <br/> | <span data-ttu-id="ce5c7-121">文件</span><span class="sxs-lookup"><span data-stu-id="ce5c7-121">Document</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="ce5c7-122">備註</span><span class="sxs-lookup"><span data-stu-id="ce5c7-122">Notes</span></span> <br/>          | <span data-ttu-id="ce5c7-123">符合 XPS 規範的取用者必須在列印功能檔或 PrintTicket 中，強制資源的 URI 參考（例如影像或色彩設定檔）必須參考元件名稱， (在包含結果 PrintTicket 的相同 XPS 檔封裝內的封裝根目錄) 的相對 URI。</span><span class="sxs-lookup"><span data-stu-id="ce5c7-123">XPS-compliant consumers MUST enforce that a URI reference to a resource such as an image or color profile in either a Print Capabilities document or PrintTicket MUST refer to a part name (a relative URI to the package root) within the same XPS Document package that contains the resultant PrintTicket.</span></span> <span data-ttu-id="ce5c7-124">相容的 XPS 取用者不能使用不符合元件名稱語法規范的 URI。</span><span class="sxs-lookup"><span data-stu-id="ce5c7-124">A compliant XPS consumer MUST NOT use a URI that is not compliant with the part name syntax.</span></span> <span data-ttu-id="ce5c7-125">這些設定是 XPS 專用的。</span><span class="sxs-lookup"><span data-stu-id="ce5c7-125">These settings are XPS specific.</span></span> <br/> <span data-ttu-id="ce5c7-126">在列印功能檔或 PrintTicket 中參考的 Uri 不得解析為 Url。</span><span class="sxs-lookup"><span data-stu-id="ce5c7-126">URIs which are referenced in either a Print Capabilities document or PrintTicket MUST NOT be resolved as URLs.</span></span> <span data-ttu-id="ce5c7-127">這是不安全的，因為它們可能無法如預期地解決，而且可能會產生驅動程式和作業系統的有害安全性風險。</span><span class="sxs-lookup"><span data-stu-id="ce5c7-127">This is unsafe as they may not resolve as intended and may create harmful security risks for the driver and operating system.</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="ce5c7-128">結構化內容</span><span class="sxs-lookup"><span data-stu-id="ce5c7-128">Structural Content</span></span>

<span data-ttu-id="ce5c7-129">此元素的 XML 結構為：</span><span class="sxs-lookup"><span data-stu-id="ce5c7-129">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:DocumentCoverFront">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option name="psk:_OptionName_">
    <psf:Property name="psf:IdentityOption">
      <psf:Value xsi:type="xs:string">_IdentityOptionValue_</psf:Value>
    </psf:Property>
    <!-- Specifies the XPS specific part name for the front cover sheet. -->
    <psf:ScoredProperty name="psk:CoverFrontSource">
      <psf:ParameterRef name="psk:DocumentCoverFrontSource" />
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature>
      
```

## <a name="structure-variables"></a><span data-ttu-id="ce5c7-130">結構變數</span><span class="sxs-lookup"><span data-stu-id="ce5c7-130">Structure Variables</span></span>

<span data-ttu-id="ce5c7-131">下表概述 XML 結構中所定義之變數的特性。</span><span class="sxs-lookup"><span data-stu-id="ce5c7-131">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="ce5c7-132">Name</span><span class="sxs-lookup"><span data-stu-id="ce5c7-132">Name</span></span>                               | <span data-ttu-id="ce5c7-133">資料類型</span><span class="sxs-lookup"><span data-stu-id="ce5c7-133">Data type</span></span>         | <span data-ttu-id="ce5c7-134">單位</span><span class="sxs-lookup"><span data-stu-id="ce5c7-134">Unit</span></span>                  | <span data-ttu-id="ce5c7-135">支援的值</span><span class="sxs-lookup"><span data-stu-id="ce5c7-135">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="ce5c7-136">總結</span><span class="sxs-lookup"><span data-stu-id="ce5c7-136">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="ce5c7-137">\_選項名稱\_</span><span class="sxs-lookup"><span data-stu-id="ce5c7-137">\_OptionName\_</span></span><br/>          | <span data-ttu-id="ce5c7-138">string</span><span class="sxs-lookup"><span data-stu-id="ce5c7-138">string</span></span><br/> | <span data-ttu-id="ce5c7-139">字元</span><span class="sxs-lookup"><span data-stu-id="ce5c7-139">characters</span></span><br/> | <span data-ttu-id="ce5c7-140">以 [XML 命名空間](https://www.w3.org/TR/1999/REC-xml-names-19990114/)所定義的有效完整名稱。</span><span class="sxs-lookup"><span data-stu-id="ce5c7-140">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="ce5c7-141">如果未指定命名空間，則會假設為預設命名空間。</span><span class="sxs-lookup"><span data-stu-id="ce5c7-141">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="ce5c7-142">選項的名稱。</span><span class="sxs-lookup"><span data-stu-id="ce5c7-142">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="ce5c7-143">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="ce5c7-143">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="ce5c7-144">string</span><span class="sxs-lookup"><span data-stu-id="ce5c7-144">string</span></span><br/> | <span data-ttu-id="ce5c7-145">n/a</span><span class="sxs-lookup"><span data-stu-id="ce5c7-145">n/a</span></span><br/>        | <span data-ttu-id="ce5c7-146">True、False。</span><span class="sxs-lookup"><span data-stu-id="ce5c7-146">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="ce5c7-147">定義選項，當選取此選項時，會停用此功能。</span><span class="sxs-lookup"><span data-stu-id="ce5c7-147">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="ce5c7-148">可延伸標記語言 (XML)  (XML) 內容</span><span class="sxs-lookup"><span data-stu-id="ce5c7-148">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="ce5c7-149">公用列印架構關鍵字是在 https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords 命名空間中定義。</span><span class="sxs-lookup"><span data-stu-id="ce5c7-149">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="ce5c7-150">此關鍵字的 public 可延伸標記語言 (XML)  (XML) 內容定義如下：</span><span class="sxs-lookup"><span data-stu-id="ce5c7-150">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:DocumentCoverFront">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!-- Specifies no cover will be output -->
  <psf:Option name="psk:NoCover" />
  <!-- Specifies the cover indicated by "CoverFrontSource" should be printed on the back side 
       of the cover sheet.  If a DocumentCoverFrontSource ParameterInit element is not specified, 
       this Option should be ignored. -->
  <psf:Option name="psk:PrintBack">
    <psf:ScoredProperty name="psk:CoverFrontSource">
      <psf:ParameterRef name="psk:DocumentCoverFrontSource" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies the cover indicated by "CoverFrontSource" may be printed on either side 
       of the cover sheet.  If a DocumentCoverFrontSource ParameterInit element is not specified, 
       this Option should be ignored. -->
  <psf:Option name="psk:PrintBoth">
    <psf:ScoredProperty name="psk:CoverFrontSource">
      <psf:ParameterRef name="psk:DocumentCoverFrontSource" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies the cover indicated by "CoverFrontSource" should be printed on the front side 
       of the cover sheet.  If a DocumentCoverFrontSource ParameterInit element is not specified, 
       this Option should be ignored. -->
  <psf:Option name="psk:PrintFront">
    <psf:ScoredProperty name="psk:CoverFrontSource">
      <psf:ParameterRef name="psk:DocumentCoverFrontSource" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies a blank cover sheet should be printed. -->
  <psf:Option name="psk:BlankCover" />
</psf:Feature>    
```

## <a name="related-topics"></a><span data-ttu-id="ce5c7-151">相關主題</span><span class="sxs-lookup"><span data-stu-id="ce5c7-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ce5c7-152">列印架構規格</span><span class="sxs-lookup"><span data-stu-id="ce5c7-152">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




