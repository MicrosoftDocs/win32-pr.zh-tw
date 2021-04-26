---
description: 本主題並非最新的。 如需最新資訊，請參閱列印架構規格。
ms.assetid: fd16bd46-32e3-4896-ac5c-03c1bf6ad515
title: JobAccountingSheet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30ffb70ba0ac1a78eefc1024d8e93dc642439aed
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/26/2021
ms.locfileid: "107998425"
---
# <a name="jobaccountingsheet"></a><span data-ttu-id="7b699-104">JobAccountingSheet</span><span class="sxs-lookup"><span data-stu-id="7b699-104">JobAccountingSheet</span></span>

<span data-ttu-id="7b699-105">本主題並非最新的。</span><span class="sxs-lookup"><span data-stu-id="7b699-105">This topic is not current.</span></span> <span data-ttu-id="7b699-106">如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。</span><span class="sxs-lookup"><span data-stu-id="7b699-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="7b699-107">描述要為作業輸出的帳戶處理工作表。</span><span class="sxs-lookup"><span data-stu-id="7b699-107">Describes the accounting sheet to be output for the job.</span></span> <span data-ttu-id="7b699-108">會計工作表應該會輸出在預設 PageMediaSize 上，並使用預設 PageMediaType。</span><span class="sxs-lookup"><span data-stu-id="7b699-108">The accounting sheet should be output on the default PageMediaSize and using the default PageMediaType.</span></span> <span data-ttu-id="7b699-109">會計工作表應該與作業的其餘部分隔離。</span><span class="sxs-lookup"><span data-stu-id="7b699-109">The accounting sheet should to be isolated from the remainder of the job.</span></span> <span data-ttu-id="7b699-110">這表示任何 (（例如 JobDuplex、JobStaple 或) JobBinding）的精加工或處理選項都不應該包含會計表。</span><span class="sxs-lookup"><span data-stu-id="7b699-110">This means that any finishing or processing options (such as JobDuplex, JobStaple, or JobBinding) should not include the accounting sheet.</span></span> <span data-ttu-id="7b699-111">帳戶處理工作表可能會在工作的第一頁或最後一頁的情況下，以實施者的意願進行。</span><span class="sxs-lookup"><span data-stu-id="7b699-111">The accounting sheet may occur as the first or last page of the job at the implementer's discretion.</span></span>

-   [<span data-ttu-id="7b699-112">項目資訊</span><span class="sxs-lookup"><span data-stu-id="7b699-112">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="7b699-113">結構化內容</span><span class="sxs-lookup"><span data-stu-id="7b699-113">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="7b699-114">可延伸標記語言 (XML)  (XML) 內容</span><span class="sxs-lookup"><span data-stu-id="7b699-114">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="7b699-115">項目資訊</span><span class="sxs-lookup"><span data-stu-id="7b699-115">Element Information</span></span>



| <span data-ttu-id="7b699-116">Name</span><span class="sxs-lookup"><span data-stu-id="7b699-116">Name</span></span> | <span data-ttu-id="7b699-117">值</span><span class="sxs-lookup"><span data-stu-id="7b699-117">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="7b699-118">項目類型</span><span class="sxs-lookup"><span data-stu-id="7b699-118">Element Type</span></span> <br/>   | <span data-ttu-id="7b699-119">功能</span><span class="sxs-lookup"><span data-stu-id="7b699-119">Feature</span></span><br/> |
| <span data-ttu-id="7b699-120">範圍前置詞</span><span class="sxs-lookup"><span data-stu-id="7b699-120">Scoping Prefix</span></span> <br/> | <span data-ttu-id="7b699-121">工作 (Job)</span><span class="sxs-lookup"><span data-stu-id="7b699-121">Job</span></span><br/>     |
| <span data-ttu-id="7b699-122">注意</span><span class="sxs-lookup"><span data-stu-id="7b699-122">Notes</span></span> <br/>          | <span data-ttu-id="7b699-123">None</span><span class="sxs-lookup"><span data-stu-id="7b699-123">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="7b699-124">結構化內容</span><span class="sxs-lookup"><span data-stu-id="7b699-124">Structural Content</span></span>

<span data-ttu-id="7b699-125">此元素的 XML 結構為：</span><span class="sxs-lookup"><span data-stu-id="7b699-125">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:JobAccountingSheet">
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

## <a name="structure-variables"></a><span data-ttu-id="7b699-126">結構變數</span><span class="sxs-lookup"><span data-stu-id="7b699-126">Structure Variables</span></span>

<span data-ttu-id="7b699-127">下表概述 XML 結構中所定義之變數的特性。</span><span class="sxs-lookup"><span data-stu-id="7b699-127">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="7b699-128">Name</span><span class="sxs-lookup"><span data-stu-id="7b699-128">Name</span></span>                               | <span data-ttu-id="7b699-129">資料類型</span><span class="sxs-lookup"><span data-stu-id="7b699-129">Data type</span></span>         | <span data-ttu-id="7b699-130">單位</span><span class="sxs-lookup"><span data-stu-id="7b699-130">Unit</span></span>                  | <span data-ttu-id="7b699-131">支援的值</span><span class="sxs-lookup"><span data-stu-id="7b699-131">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="7b699-132">總結</span><span class="sxs-lookup"><span data-stu-id="7b699-132">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="7b699-133">\_選項名稱\_</span><span class="sxs-lookup"><span data-stu-id="7b699-133">\_OptionName\_</span></span><br/>          | <span data-ttu-id="7b699-134">字串</span><span class="sxs-lookup"><span data-stu-id="7b699-134">string</span></span><br/> | <span data-ttu-id="7b699-135">字元</span><span class="sxs-lookup"><span data-stu-id="7b699-135">characters</span></span><br/> | <span data-ttu-id="7b699-136">以 [XML 命名空間](https://www.w3.org/TR/1999/REC-xml-names-19990114/)所定義的有效完整名稱。</span><span class="sxs-lookup"><span data-stu-id="7b699-136">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="7b699-137">如果未指定命名空間，則會假設為預設命名空間。</span><span class="sxs-lookup"><span data-stu-id="7b699-137">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="7b699-138">選項的名稱。</span><span class="sxs-lookup"><span data-stu-id="7b699-138">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="7b699-139">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="7b699-139">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="7b699-140">字串</span><span class="sxs-lookup"><span data-stu-id="7b699-140">string</span></span><br/> | <span data-ttu-id="7b699-141">n/a</span><span class="sxs-lookup"><span data-stu-id="7b699-141">n/a</span></span><br/>        | <span data-ttu-id="7b699-142">True、False。</span><span class="sxs-lookup"><span data-stu-id="7b699-142">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="7b699-143">定義選項，當選取此選項時，會停用此功能。</span><span class="sxs-lookup"><span data-stu-id="7b699-143">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="7b699-144">可延伸標記語言 (XML)  (XML) 內容</span><span class="sxs-lookup"><span data-stu-id="7b699-144">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="7b699-145">公用列印架構關鍵字是在 https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords 命名空間中定義。</span><span class="sxs-lookup"><span data-stu-id="7b699-145">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="7b699-146">此關鍵字的 public 可延伸標記語言 (XML)  (XML) 內容定義如下：</span><span class="sxs-lookup"><span data-stu-id="7b699-146">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:JobAccountingSheet">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!-- Specifies no accounting sheet will be output. -->
  <psf:Option name="psk:None" />
  <!-- Specifies the standard (device defined) accounting sheet should be output. -->
  <psf:Option name="psk:Standard" />
</psf:Feature>
        
```

## <a name="related-topics"></a><span data-ttu-id="7b699-147">相關主題</span><span class="sxs-lookup"><span data-stu-id="7b699-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7b699-148">列印架構規格</span><span class="sxs-lookup"><span data-stu-id="7b699-148">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




