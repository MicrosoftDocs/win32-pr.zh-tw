---
description: 瞭解 DocumentCollate 元素，其描述輸出的排序特性。
ms.assetid: 752cccf7-1f95-4597-b0e2-a96fd22ffeef
title: DocumentCollate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4c3036cc64265ea8f88bfcc46aea0149f8af5ad
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/19/2021
ms.locfileid: "112409451"
---
# <a name="documentcollate"></a><span data-ttu-id="4325e-103">DocumentCollate</span><span class="sxs-lookup"><span data-stu-id="4325e-103">DocumentCollate</span></span>

<span data-ttu-id="4325e-104">本主題並非最新的。</span><span class="sxs-lookup"><span data-stu-id="4325e-104">This topic is not current.</span></span> <span data-ttu-id="4325e-105">如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。</span><span class="sxs-lookup"><span data-stu-id="4325e-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="4325e-106">描述輸出的排序特性。</span><span class="sxs-lookup"><span data-stu-id="4325e-106">Describes the collating characteristics of the output.</span></span> <span data-ttu-id="4325e-107">每一份個別檔中的所有頁面都會進行定序。</span><span class="sxs-lookup"><span data-stu-id="4325e-107">All pages in each individual document are collated.</span></span> <span data-ttu-id="4325e-108">DocumentCollate 和 JobCollateAlldocuments 互斥。</span><span class="sxs-lookup"><span data-stu-id="4325e-108">DocumentCollate and JobCollateAlldocuments are mutually exclusive.</span></span> <span data-ttu-id="4325e-109">無論是否已執行這兩個關鍵字的行為和執行，都是由驅動程式所決定。</span><span class="sxs-lookup"><span data-stu-id="4325e-109">The behavior and implementation of whether both or only one of these keywords is implemented is left to the driver.</span></span>

<span data-ttu-id="4325e-110">以下是執行 Collate 時應遵循的規則</span><span class="sxs-lookup"><span data-stu-id="4325e-110">The following are the rules which should be followed for Collate implementation</span></span>

## <a name="element-definition-and-rules"></a><span data-ttu-id="4325e-111">元素定義和規則</span><span class="sxs-lookup"><span data-stu-id="4325e-111">Element Definition and Rules</span></span>

<span data-ttu-id="4325e-112">您必須先遵循 JobCollateAllDocument 的規則，然後套用適用于 DocumentCollate 的規則，才能讓案例運作。</span><span class="sxs-lookup"><span data-stu-id="4325e-112">You must first follow the rules for JobCollateAllDocument, and then apply rules for DocumentCollate for the scenarios to work.</span></span> <span data-ttu-id="4325e-113">請注意，在「PrintTicket 至 Devmode」轉換設定中（此驅動程式不支援 JobCollateAllDocuments），會由驅動程式選擇適當的行為來採取 (JobCollateAllDocuments = ON 或 OFF) 。</span><span class="sxs-lookup"><span data-stu-id="4325e-113">Note that in a PrintTicket to Devmode conversion setting, where JobCollateAllDocuments is not supported by the driver, it is up to the driver to choose the appropriate behavior to take (JobCollateAllDocuments = ON or OFF).</span></span> <span data-ttu-id="4325e-114">此外，您也可以根據其他的 PrintTicket 設定來變更選擇。</span><span class="sxs-lookup"><span data-stu-id="4325e-114">Also, the choice can be changed depending on other PrintTicket settings.</span></span>

### <a name="jobcollatealldocuments"></a><span data-ttu-id="4325e-115">JobCollateAllDocuments</span><span class="sxs-lookup"><span data-stu-id="4325e-115">JobCollateAllDocuments</span></span>

<span data-ttu-id="4325e-116">ON：列印 (DocumentCopiesAllPages) 每份檔的複本，重複 JobCopiesAllDocuments 時間。</span><span class="sxs-lookup"><span data-stu-id="4325e-116">ON: Print (DocumentCopiesAllPages) copies of each document, repeat JobCopiesAllDocuments times.</span></span>

<span data-ttu-id="4325e-117">OFF：對於每份檔，列印 (JobCopiesAllDocuments x DocumentCopiesAllPages) 會一起複製。</span><span class="sxs-lookup"><span data-stu-id="4325e-117">OFF: For each document, print (JobCopiesAllDocuments x DocumentCopiesAllPages) copies together.</span></span>

### <a name="documentcollate"></a><span data-ttu-id="4325e-118">DocumentCollate</span><span class="sxs-lookup"><span data-stu-id="4325e-118">DocumentCollate</span></span>

<span data-ttu-id="4325e-119">ON：適用于所有複本 (JobCopiesAllDocuments x) DocumentCopiesAllPages 檔中連續列印的檔，該檔中的分頁表。</span><span class="sxs-lookup"><span data-stu-id="4325e-119">ON: For all copies (JobCopiesAllDocuments x DocumentCopiesAllPages) of a document printed contiguously, collate sheets in that document.</span></span>

<span data-ttu-id="4325e-120">OFF：針對 (JobCopiesAllDocuments x DocumentCopiesAllPages 的所有複本，) 連續列印，將每個工作表 (JobCopiesAllDocuments x DocumentCopiesAllPages) 的所有複本一起列印。</span><span class="sxs-lookup"><span data-stu-id="4325e-120">OFF: For all copies (JobCopiesAllDocuments x DocumentCopiesAllPages) printed contiguously, print all copies (JobCopiesAllDocuments x DocumentCopiesAllPages) of each sheet together.</span></span>

-   [<span data-ttu-id="4325e-121">項目資訊</span><span class="sxs-lookup"><span data-stu-id="4325e-121">Element Information</span></span>](#element-information)

-   [<span data-ttu-id="4325e-122">結構化內容</span><span class="sxs-lookup"><span data-stu-id="4325e-122">Structural Content</span></span>](#structural-content)

-   [<span data-ttu-id="4325e-123">XML 內容</span><span class="sxs-lookup"><span data-stu-id="4325e-123">XML Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="4325e-124">項目資訊</span><span class="sxs-lookup"><span data-stu-id="4325e-124">Element Information</span></span>



| <span data-ttu-id="4325e-125">Name</span><span class="sxs-lookup"><span data-stu-id="4325e-125">Name</span></span> | <span data-ttu-id="4325e-126">值</span><span class="sxs-lookup"><span data-stu-id="4325e-126">Value</span></span> |
|----------------------------|---------------------|
| <span data-ttu-id="4325e-127">項目類型</span><span class="sxs-lookup"><span data-stu-id="4325e-127">Element Type</span></span> <br/>   | <span data-ttu-id="4325e-128">功能</span><span class="sxs-lookup"><span data-stu-id="4325e-128">Feature</span></span><br/>  |
| <span data-ttu-id="4325e-129">範圍前置詞</span><span class="sxs-lookup"><span data-stu-id="4325e-129">Scoping Prefix</span></span> <br/> | <span data-ttu-id="4325e-130">文件</span><span class="sxs-lookup"><span data-stu-id="4325e-130">Document</span></span><br/> |
| <span data-ttu-id="4325e-131">注意</span><span class="sxs-lookup"><span data-stu-id="4325e-131">Notes</span></span> <br/>          | <span data-ttu-id="4325e-132">None</span><span class="sxs-lookup"><span data-stu-id="4325e-132">None</span></span><br/>     |



 

## <a name="structural-content"></a><span data-ttu-id="4325e-133">結構化內容</span><span class="sxs-lookup"><span data-stu-id="4325e-133">Structural Content</span></span>

<span data-ttu-id="4325e-134">此元素的 XML 結構為：</span><span class="sxs-lookup"><span data-stu-id="4325e-134">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="4325e-135">結構變數</span><span class="sxs-lookup"><span data-stu-id="4325e-135">Structure Variables</span></span>

<span data-ttu-id="4325e-136">下表概述 XML 結構中所定義之變數的特性。</span><span class="sxs-lookup"><span data-stu-id="4325e-136">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="4325e-137">Name</span><span class="sxs-lookup"><span data-stu-id="4325e-137">Name</span></span>                               | <span data-ttu-id="4325e-138">資料類型</span><span class="sxs-lookup"><span data-stu-id="4325e-138">Data type</span></span>         | <span data-ttu-id="4325e-139">單位</span><span class="sxs-lookup"><span data-stu-id="4325e-139">Unit</span></span>                  | <span data-ttu-id="4325e-140">支援的值</span><span class="sxs-lookup"><span data-stu-id="4325e-140">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="4325e-141">總結</span><span class="sxs-lookup"><span data-stu-id="4325e-141">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="4325e-142">\_選項名稱\_</span><span class="sxs-lookup"><span data-stu-id="4325e-142">\_OptionName\_</span></span><br/>          | <span data-ttu-id="4325e-143">string</span><span class="sxs-lookup"><span data-stu-id="4325e-143">string</span></span><br/> | <span data-ttu-id="4325e-144">字元</span><span class="sxs-lookup"><span data-stu-id="4325e-144">characters</span></span><br/> | <span data-ttu-id="4325e-145">以 [XML 命名空間](https://www.w3.org/TR/1999/REC-xml-names-19990114/)所定義的有效完整名稱。</span><span class="sxs-lookup"><span data-stu-id="4325e-145">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="4325e-146">如果未指定命名空間，則會假設為預設命名空間。</span><span class="sxs-lookup"><span data-stu-id="4325e-146">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="4325e-147">選項的名稱。</span><span class="sxs-lookup"><span data-stu-id="4325e-147">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="4325e-148">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="4325e-148">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="4325e-149">string</span><span class="sxs-lookup"><span data-stu-id="4325e-149">string</span></span><br/> | <span data-ttu-id="4325e-150">n/a</span><span class="sxs-lookup"><span data-stu-id="4325e-150">n/a</span></span><br/>        | <span data-ttu-id="4325e-151">True、False。</span><span class="sxs-lookup"><span data-stu-id="4325e-151">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="4325e-152">定義選項，當選取此選項時，會停用此功能。</span><span class="sxs-lookup"><span data-stu-id="4325e-152">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="4325e-153">可延伸標記語言 (XML)  (XML) 內容</span><span class="sxs-lookup"><span data-stu-id="4325e-153">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="4325e-154">公用列印架構關鍵字是在 https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords 命名空間中定義。</span><span class="sxs-lookup"><span data-stu-id="4325e-154">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="4325e-155">此關鍵字的 public 可延伸標記語言 (XML)  (XML) 內容定義如下：</span><span class="sxs-lookup"><span data-stu-id="4325e-155">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="4325e-156">相關主題</span><span class="sxs-lookup"><span data-stu-id="4325e-156">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4325e-157">列印架構規格</span><span class="sxs-lookup"><span data-stu-id="4325e-157">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




