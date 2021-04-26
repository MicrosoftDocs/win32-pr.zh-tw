---
description: 本主題並非最新的。 如需最新資訊，請參閱列印架構規格。
ms.assetid: 752cccf7-1f95-4597-b0e2-a96fd22ffeef
title: DocumentCollate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 959613299c53996ce7d66171d2da1518f28b9298
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/26/2021
ms.locfileid: "107993995"
---
# <a name="documentcollate"></a><span data-ttu-id="40d5c-104">DocumentCollate</span><span class="sxs-lookup"><span data-stu-id="40d5c-104">DocumentCollate</span></span>

<span data-ttu-id="40d5c-105">本主題並非最新的。</span><span class="sxs-lookup"><span data-stu-id="40d5c-105">This topic is not current.</span></span> <span data-ttu-id="40d5c-106">如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。</span><span class="sxs-lookup"><span data-stu-id="40d5c-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="40d5c-107">描述輸出的排序特性。</span><span class="sxs-lookup"><span data-stu-id="40d5c-107">Describes the collating characteristics of the output.</span></span> <span data-ttu-id="40d5c-108">每一份個別檔中的所有頁面都會進行定序。</span><span class="sxs-lookup"><span data-stu-id="40d5c-108">All pages in each individual document are collated.</span></span> <span data-ttu-id="40d5c-109">DocumentCollate 和 JobCollateAlldocuments 互斥。</span><span class="sxs-lookup"><span data-stu-id="40d5c-109">DocumentCollate and JobCollateAlldocuments are mutually exclusive.</span></span> <span data-ttu-id="40d5c-110">無論是否已執行這兩個關鍵字的行為和執行，都是由驅動程式所決定。</span><span class="sxs-lookup"><span data-stu-id="40d5c-110">The behavior and implementation of whether both or only one of these keywords is implemented is left to the driver.</span></span>

<span data-ttu-id="40d5c-111">以下是執行 Collate 時應遵循的規則</span><span class="sxs-lookup"><span data-stu-id="40d5c-111">The following are the rules which should be followed for Collate implementation</span></span>

## <a name="element-definition-and-rules"></a><span data-ttu-id="40d5c-112">元素定義和規則</span><span class="sxs-lookup"><span data-stu-id="40d5c-112">Element Definition and Rules</span></span>

<span data-ttu-id="40d5c-113">您必須先遵循 JobCollateAllDocument 的規則，然後套用適用于 DocumentCollate 的規則，才能讓案例運作。</span><span class="sxs-lookup"><span data-stu-id="40d5c-113">You must first follow the rules for JobCollateAllDocument, and then apply rules for DocumentCollate for the scenarios to work.</span></span> <span data-ttu-id="40d5c-114">請注意，在「PrintTicket 至 Devmode」轉換設定中（此驅動程式不支援 JobCollateAllDocuments），會由驅動程式選擇適當的行為來採取 (JobCollateAllDocuments = ON 或 OFF) 。</span><span class="sxs-lookup"><span data-stu-id="40d5c-114">Note that in a PrintTicket to Devmode conversion setting, where JobCollateAllDocuments is not supported by the driver, it is up to the driver to choose the appropriate behavior to take (JobCollateAllDocuments = ON or OFF).</span></span> <span data-ttu-id="40d5c-115">此外，您也可以根據其他的 PrintTicket 設定來變更選擇。</span><span class="sxs-lookup"><span data-stu-id="40d5c-115">Also, the choice can be changed depending on other PrintTicket settings.</span></span>

### <a name="jobcollatealldocuments"></a><span data-ttu-id="40d5c-116">JobCollateAllDocuments</span><span class="sxs-lookup"><span data-stu-id="40d5c-116">JobCollateAllDocuments</span></span>

<span data-ttu-id="40d5c-117">ON：列印 (DocumentCopiesAllPages) 每份檔的複本，重複 JobCopiesAllDocuments 時間。</span><span class="sxs-lookup"><span data-stu-id="40d5c-117">ON: Print (DocumentCopiesAllPages) copies of each document, repeat JobCopiesAllDocuments times.</span></span>

<span data-ttu-id="40d5c-118">OFF：對於每份檔，列印 (JobCopiesAllDocuments x DocumentCopiesAllPages) 會一起複製。</span><span class="sxs-lookup"><span data-stu-id="40d5c-118">OFF: For each document, print (JobCopiesAllDocuments x DocumentCopiesAllPages) copies together.</span></span>

### <a name="documentcollate"></a><span data-ttu-id="40d5c-119">DocumentCollate</span><span class="sxs-lookup"><span data-stu-id="40d5c-119">DocumentCollate</span></span>

<span data-ttu-id="40d5c-120">ON：適用于所有複本 (JobCopiesAllDocuments x) DocumentCopiesAllPages 檔中連續列印的檔，該檔中的分頁表。</span><span class="sxs-lookup"><span data-stu-id="40d5c-120">ON: For all copies (JobCopiesAllDocuments x DocumentCopiesAllPages) of a document printed contiguously, collate sheets in that document.</span></span>

<span data-ttu-id="40d5c-121">OFF：針對 (JobCopiesAllDocuments x DocumentCopiesAllPages 的所有複本，) 連續列印，將每個工作表 (JobCopiesAllDocuments x DocumentCopiesAllPages) 的所有複本一起列印。</span><span class="sxs-lookup"><span data-stu-id="40d5c-121">OFF: For all copies (JobCopiesAllDocuments x DocumentCopiesAllPages) printed contiguously, print all copies (JobCopiesAllDocuments x DocumentCopiesAllPages) of each sheet together.</span></span>

-   [<span data-ttu-id="40d5c-122">項目資訊</span><span class="sxs-lookup"><span data-stu-id="40d5c-122">Element Information</span></span>](#element-information)

-   [<span data-ttu-id="40d5c-123">結構化內容</span><span class="sxs-lookup"><span data-stu-id="40d5c-123">Structural Content</span></span>](#structural-content)

-   [<span data-ttu-id="40d5c-124">XML 內容</span><span class="sxs-lookup"><span data-stu-id="40d5c-124">XML Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="40d5c-125">項目資訊</span><span class="sxs-lookup"><span data-stu-id="40d5c-125">Element Information</span></span>



| <span data-ttu-id="40d5c-126">Name</span><span class="sxs-lookup"><span data-stu-id="40d5c-126">Name</span></span> | <span data-ttu-id="40d5c-127">值</span><span class="sxs-lookup"><span data-stu-id="40d5c-127">Value</span></span> |
|----------------------------|---------------------|
| <span data-ttu-id="40d5c-128">項目類型</span><span class="sxs-lookup"><span data-stu-id="40d5c-128">Element Type</span></span> <br/>   | <span data-ttu-id="40d5c-129">功能</span><span class="sxs-lookup"><span data-stu-id="40d5c-129">Feature</span></span><br/>  |
| <span data-ttu-id="40d5c-130">範圍前置詞</span><span class="sxs-lookup"><span data-stu-id="40d5c-130">Scoping Prefix</span></span> <br/> | <span data-ttu-id="40d5c-131">文件</span><span class="sxs-lookup"><span data-stu-id="40d5c-131">Document</span></span><br/> |
| <span data-ttu-id="40d5c-132">注意</span><span class="sxs-lookup"><span data-stu-id="40d5c-132">Notes</span></span> <br/>          | <span data-ttu-id="40d5c-133">None</span><span class="sxs-lookup"><span data-stu-id="40d5c-133">None</span></span><br/>     |



 

## <a name="structural-content"></a><span data-ttu-id="40d5c-134">結構化內容</span><span class="sxs-lookup"><span data-stu-id="40d5c-134">Structural Content</span></span>

<span data-ttu-id="40d5c-135">此元素的 XML 結構為：</span><span class="sxs-lookup"><span data-stu-id="40d5c-135">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:DocumentCollate">
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

## <a name="structure-variables"></a><span data-ttu-id="40d5c-136">結構變數</span><span class="sxs-lookup"><span data-stu-id="40d5c-136">Structure Variables</span></span>

<span data-ttu-id="40d5c-137">下表概述 XML 結構中所定義之變數的特性。</span><span class="sxs-lookup"><span data-stu-id="40d5c-137">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="40d5c-138">Name</span><span class="sxs-lookup"><span data-stu-id="40d5c-138">Name</span></span>                               | <span data-ttu-id="40d5c-139">資料類型</span><span class="sxs-lookup"><span data-stu-id="40d5c-139">Data type</span></span>         | <span data-ttu-id="40d5c-140">單位</span><span class="sxs-lookup"><span data-stu-id="40d5c-140">Unit</span></span>                  | <span data-ttu-id="40d5c-141">支援的值</span><span class="sxs-lookup"><span data-stu-id="40d5c-141">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="40d5c-142">總結</span><span class="sxs-lookup"><span data-stu-id="40d5c-142">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="40d5c-143">\_選項名稱\_</span><span class="sxs-lookup"><span data-stu-id="40d5c-143">\_OptionName\_</span></span><br/>          | <span data-ttu-id="40d5c-144">字串</span><span class="sxs-lookup"><span data-stu-id="40d5c-144">string</span></span><br/> | <span data-ttu-id="40d5c-145">字元</span><span class="sxs-lookup"><span data-stu-id="40d5c-145">characters</span></span><br/> | <span data-ttu-id="40d5c-146">以 [XML 命名空間](https://www.w3.org/TR/1999/REC-xml-names-19990114/)所定義的有效完整名稱。</span><span class="sxs-lookup"><span data-stu-id="40d5c-146">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="40d5c-147">如果未指定命名空間，則會假設為預設命名空間。</span><span class="sxs-lookup"><span data-stu-id="40d5c-147">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="40d5c-148">選項的名稱。</span><span class="sxs-lookup"><span data-stu-id="40d5c-148">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="40d5c-149">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="40d5c-149">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="40d5c-150">字串</span><span class="sxs-lookup"><span data-stu-id="40d5c-150">string</span></span><br/> | <span data-ttu-id="40d5c-151">n/a</span><span class="sxs-lookup"><span data-stu-id="40d5c-151">n/a</span></span><br/>        | <span data-ttu-id="40d5c-152">True、False。</span><span class="sxs-lookup"><span data-stu-id="40d5c-152">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="40d5c-153">定義選項，當選取此選項時，會停用此功能。</span><span class="sxs-lookup"><span data-stu-id="40d5c-153">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="40d5c-154">可延伸標記語言 (XML)  (XML) 內容</span><span class="sxs-lookup"><span data-stu-id="40d5c-154">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="40d5c-155">公用列印架構關鍵字是在 https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords 命名空間中定義。</span><span class="sxs-lookup"><span data-stu-id="40d5c-155">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="40d5c-156">此關鍵字的 public 可延伸標記語言 (XML)  (XML) 內容定義如下：</span><span class="sxs-lookup"><span data-stu-id="40d5c-156">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:DocumentCollate">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!-- Specifies collating.  -->
  <psf:Option name="psk:Collated" />
  <!-- Specifies no collating. -->
  <psf:Option name="psk:Uncollated" />
</psf:Feature>
```

## <a name="related-topics"></a><span data-ttu-id="40d5c-157">相關主題</span><span class="sxs-lookup"><span data-stu-id="40d5c-157">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="40d5c-158">列印架構規格</span><span class="sxs-lookup"><span data-stu-id="40d5c-158">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




