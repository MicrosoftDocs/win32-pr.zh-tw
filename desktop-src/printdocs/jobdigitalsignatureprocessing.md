---
description: 本主題並非最新的。 如需最新資訊，請參閱列印架構規格。
ms.assetid: 0592f7a4-cace-41b0-91e3-2811f72aeb3e
title: JobDigitalSignatureProcessing
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f2c60fd005f42bd3f9861e86156a7da9164a81e
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/06/2021
ms.locfileid: "106986035"
---
# <a name="jobdigitalsignatureprocessing"></a><span data-ttu-id="6187e-104">JobDigitalSignatureProcessing</span><span class="sxs-lookup"><span data-stu-id="6187e-104">JobDigitalSignatureProcessing</span></span>

<span data-ttu-id="6187e-105">本主題並非最新的。</span><span class="sxs-lookup"><span data-stu-id="6187e-105">This topic is not current.</span></span> <span data-ttu-id="6187e-106">如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。</span><span class="sxs-lookup"><span data-stu-id="6187e-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="6187e-107">描述設定整個作業的數位簽章處理。</span><span class="sxs-lookup"><span data-stu-id="6187e-107">Describes configuring the digital signature processing for the entire job.</span></span> <span data-ttu-id="6187e-108">僅適用于包含數位簽章的內容。</span><span class="sxs-lookup"><span data-stu-id="6187e-108">Applicable only to content that contains digital signatures.</span></span>

-   [<span data-ttu-id="6187e-109">項目資訊</span><span class="sxs-lookup"><span data-stu-id="6187e-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="6187e-110">結構化內容</span><span class="sxs-lookup"><span data-stu-id="6187e-110">Structural Content</span></span>](#structural-content)

## <a name="element-information"></a><span data-ttu-id="6187e-111">項目資訊</span><span class="sxs-lookup"><span data-stu-id="6187e-111">Element Information</span></span>



| <span data-ttu-id="6187e-112">Name</span><span class="sxs-lookup"><span data-stu-id="6187e-112">Name</span></span>                       |                    |
|----------------------------|--------------------|
| <span data-ttu-id="6187e-113">項目類型</span><span class="sxs-lookup"><span data-stu-id="6187e-113">Element Type</span></span> <br/>   | <span data-ttu-id="6187e-114">功能</span><span class="sxs-lookup"><span data-stu-id="6187e-114">Feature</span></span><br/> |
| <span data-ttu-id="6187e-115">範圍前置詞</span><span class="sxs-lookup"><span data-stu-id="6187e-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="6187e-116">工作 (Job)</span><span class="sxs-lookup"><span data-stu-id="6187e-116">Job</span></span><br/>     |
| <span data-ttu-id="6187e-117">注意</span><span class="sxs-lookup"><span data-stu-id="6187e-117">Notes</span></span> <br/>          | <span data-ttu-id="6187e-118">None</span><span class="sxs-lookup"><span data-stu-id="6187e-118">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="6187e-119">結構化內容</span><span class="sxs-lookup"><span data-stu-id="6187e-119">Structural Content</span></span>

<span data-ttu-id="6187e-120">此元素的 XML 結構為：</span><span class="sxs-lookup"><span data-stu-id="6187e-120">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:JobDigitalSignatureProcessing">
  <psf:Property name="SelectionType">
    <psf:Value xsi:type="xs:string">PickOne</psf:Value>
  </psf:Property>
  <psf:Option name="psk:_OptionName_">
    <psf:Property name="psf:IdentityOption">
      <psf:Value xsi:type="xs:string">_IdentityOptionValue_</psf:Value>
    </psf:Property>
  </psf:Feature>
```

## <a name="structure-variables"></a><span data-ttu-id="6187e-121">結構變數</span><span class="sxs-lookup"><span data-stu-id="6187e-121">Structure Variables</span></span>

<span data-ttu-id="6187e-122">下表概述 XML 結構中所定義之變數的特性。</span><span class="sxs-lookup"><span data-stu-id="6187e-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="6187e-123">Name</span><span class="sxs-lookup"><span data-stu-id="6187e-123">Name</span></span>                               | <span data-ttu-id="6187e-124">資料類型</span><span class="sxs-lookup"><span data-stu-id="6187e-124">Data type</span></span>         | <span data-ttu-id="6187e-125">單位</span><span class="sxs-lookup"><span data-stu-id="6187e-125">Unit</span></span>                   | <span data-ttu-id="6187e-126">支援的值</span><span class="sxs-lookup"><span data-stu-id="6187e-126">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="6187e-127">總結</span><span class="sxs-lookup"><span data-stu-id="6187e-127">Summary</span></span>                                                                      |
|------------------------------------|-------------------|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="6187e-128">\_選項名稱\_</span><span class="sxs-lookup"><span data-stu-id="6187e-128">\_OptionName\_</span></span><br/>          | <span data-ttu-id="6187e-129">字串</span><span class="sxs-lookup"><span data-stu-id="6187e-129">string</span></span><br/> | <span data-ttu-id="6187e-130">字元</span><span class="sxs-lookup"><span data-stu-id="6187e-130">characters</span></span> <br/> | <span data-ttu-id="6187e-131">以 [XML 命名空間](https://www.w3.org/TR/1999/REC-xml-names-19990114/)所定義的有效完整名稱。</span><span class="sxs-lookup"><span data-stu-id="6187e-131">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="6187e-132">如果未指定命名空間，則會假設為預設命名空間。</span><span class="sxs-lookup"><span data-stu-id="6187e-132">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="6187e-133">選項的名稱。</span><span class="sxs-lookup"><span data-stu-id="6187e-133">The name of the option</span></span><br/>                                            |
| <span data-ttu-id="6187e-134">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="6187e-134">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="6187e-135">字串</span><span class="sxs-lookup"><span data-stu-id="6187e-135">string</span></span><br/> | <span data-ttu-id="6187e-136">n/a</span><span class="sxs-lookup"><span data-stu-id="6187e-136">n/a</span></span><br/>         | <span data-ttu-id="6187e-137">True、False</span><span class="sxs-lookup"><span data-stu-id="6187e-137">True, False</span></span><br/>                                                                                                                                                                | <span data-ttu-id="6187e-138">定義選項，當選取此選項時，會停用此功能。</span><span class="sxs-lookup"><span data-stu-id="6187e-138">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="6187e-139">可延伸標記語言 (XML)  (XML) 內容</span><span class="sxs-lookup"><span data-stu-id="6187e-139">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="6187e-140">公用列印架構關鍵字是在 https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords 命名空間中定義。</span><span class="sxs-lookup"><span data-stu-id="6187e-140">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="6187e-141">此關鍵字的 public 可延伸標記語言 (XML)  (XML) 內容定義如下：</span><span class="sxs-lookup"><span data-stu-id="6187e-141">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:JobDigitalSignatureProcessing">
  <psf:Property name="SelectionType">
    <psf:Value xsi:type="xs:string">PickOne</psf:Value>
  </psf:Property>
  <!-- Print the job regardless of the validity of the digital signatures. Digital signatures MAY be ignored.  -->
  <psf:Option name="psk:PrintInvalidSignatures" />
  <!-- Print the job regardless of the validity of the digital signatures.  In the event an invalid signature is encountered, an error page should print at the end of the job.  Digital signatures MUST not be ignored. -->
  <psf:Option name="psk:PrintInvalidSignaturesWithErrorReport" />
  <!-- Print the job only if all digital signatures are valid.  Digital signatures MUST not be ignored. -->
  <psf:Option name="psk:PrintOnlyValidSignatures" />
</psf:Feature>
```

## <a name="related-topics"></a><span data-ttu-id="6187e-142">相關主題</span><span class="sxs-lookup"><span data-stu-id="6187e-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6187e-143">列印架構規格</span><span class="sxs-lookup"><span data-stu-id="6187e-143">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




