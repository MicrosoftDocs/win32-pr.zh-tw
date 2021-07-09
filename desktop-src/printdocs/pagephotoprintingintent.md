---
description: 檢查 PagePhotoPrintingIntent 使用者可設定的元素。 本主題並非最新的。 如需最新資訊，請參閱列印架構規格。
ms.assetid: f9a00828-52df-449e-914b-4c6cd7c29f3a
title: PagePhotoPrintingIntent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d1cf9ae587062efc68b953f5931b55147940b1b
ms.sourcegitcommit: 998d50f6def8a25850fc113fc8a2df903c829c5e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/09/2021
ms.locfileid: "113548976"
---
# <a name="pagephotoprintingintent"></a><span data-ttu-id="9fa41-105">PagePhotoPrintingIntent</span><span class="sxs-lookup"><span data-stu-id="9fa41-105">PagePhotoPrintingIntent</span></span>

<span data-ttu-id="9fa41-106">本主題並非最新的。</span><span class="sxs-lookup"><span data-stu-id="9fa41-106">This topic is not current.</span></span> <span data-ttu-id="9fa41-107">如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。</span><span class="sxs-lookup"><span data-stu-id="9fa41-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="9fa41-108">指出驅動程式進行相片列印設定的高層級意圖。</span><span class="sxs-lookup"><span data-stu-id="9fa41-108">Indicates a high-level intent to the driver for population of photo printing settings.</span></span> <span data-ttu-id="9fa41-109">這些設定會處理使用者在列印相片時可能會指定的預期輸出品質。</span><span class="sxs-lookup"><span data-stu-id="9fa41-109">These settings deal with the expected output quality a user may specify when printing photos.</span></span>

-   [<span data-ttu-id="9fa41-110">項目資訊</span><span class="sxs-lookup"><span data-stu-id="9fa41-110">Element Information</span></span>](#element-information)

-   [<span data-ttu-id="9fa41-111">結構化內容</span><span class="sxs-lookup"><span data-stu-id="9fa41-111">Structural Content</span></span>](#structural-content)

-   [<span data-ttu-id="9fa41-112">XML 內容</span><span class="sxs-lookup"><span data-stu-id="9fa41-112">XML Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="9fa41-113">項目資訊</span><span class="sxs-lookup"><span data-stu-id="9fa41-113">Element Information</span></span>



| <span data-ttu-id="9fa41-114">Name</span><span class="sxs-lookup"><span data-stu-id="9fa41-114">Name</span></span> | <span data-ttu-id="9fa41-115">值</span><span class="sxs-lookup"><span data-stu-id="9fa41-115">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="9fa41-116">項目類型</span><span class="sxs-lookup"><span data-stu-id="9fa41-116">Element Type</span></span> <br/>   | <span data-ttu-id="9fa41-117">功能</span><span class="sxs-lookup"><span data-stu-id="9fa41-117">Feature</span></span><br/> |
| <span data-ttu-id="9fa41-118">範圍前置詞</span><span class="sxs-lookup"><span data-stu-id="9fa41-118">Scoping Prefix</span></span> <br/> | <span data-ttu-id="9fa41-119">頁面</span><span class="sxs-lookup"><span data-stu-id="9fa41-119">Page</span></span><br/>    |
| <span data-ttu-id="9fa41-120">注意</span><span class="sxs-lookup"><span data-stu-id="9fa41-120">Notes</span></span> <br/>          | <span data-ttu-id="9fa41-121">None</span><span class="sxs-lookup"><span data-stu-id="9fa41-121">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="9fa41-122">結構化內容</span><span class="sxs-lookup"><span data-stu-id="9fa41-122">Structural Content</span></span>

<span data-ttu-id="9fa41-123">此元素的 XML 結構為：</span><span class="sxs-lookup"><span data-stu-id="9fa41-123">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:PagePhotoPrintingIntent">  
  <psf:Property name="SelectionType">
    <psf:Value xsi:type="xs:string">PickOne</psf:Value>
  </psf:Property>
  <psf:Option name="psk:_OptionName_">
    <psf:Property name="psf:IdentityOption">
    <psf:Value xsi:type="xs:string">_IdentityOptionValue_</psf:Value>
  </psf:Property>
</psf:Feature>
      
```

## <a name="structure-variables"></a><span data-ttu-id="9fa41-124">結構變數</span><span class="sxs-lookup"><span data-stu-id="9fa41-124">Structure Variables</span></span>

<span data-ttu-id="9fa41-125">下表概述 XML 結構中所定義之變數的特性。</span><span class="sxs-lookup"><span data-stu-id="9fa41-125">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="9fa41-126">Name</span><span class="sxs-lookup"><span data-stu-id="9fa41-126">Name</span></span>                               | <span data-ttu-id="9fa41-127">資料類型</span><span class="sxs-lookup"><span data-stu-id="9fa41-127">Data type</span></span>         | <span data-ttu-id="9fa41-128">單位</span><span class="sxs-lookup"><span data-stu-id="9fa41-128">Unit</span></span>                  | <span data-ttu-id="9fa41-129">支援的值</span><span class="sxs-lookup"><span data-stu-id="9fa41-129">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="9fa41-130">摘要</span><span class="sxs-lookup"><span data-stu-id="9fa41-130">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="9fa41-131">\_選項名稱\_</span><span class="sxs-lookup"><span data-stu-id="9fa41-131">\_OptionName\_</span></span><br/>          | <span data-ttu-id="9fa41-132">string</span><span class="sxs-lookup"><span data-stu-id="9fa41-132">string</span></span><br/> | <span data-ttu-id="9fa41-133">字元</span><span class="sxs-lookup"><span data-stu-id="9fa41-133">characters</span></span><br/> | <span data-ttu-id="9fa41-134">以 [XML 命名空間](https://www.w3.org/TR/1999/REC-xml-names-19990114/)所定義的有效完整名稱。</span><span class="sxs-lookup"><span data-stu-id="9fa41-134">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="9fa41-135">如果未指定命名空間，則會假設為預設命名空間。</span><span class="sxs-lookup"><span data-stu-id="9fa41-135">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="9fa41-136">選項的名稱。</span><span class="sxs-lookup"><span data-stu-id="9fa41-136">The name of the option</span></span><br/>                                            |
| <span data-ttu-id="9fa41-137">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="9fa41-137">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="9fa41-138">string</span><span class="sxs-lookup"><span data-stu-id="9fa41-138">string</span></span><br/> | <span data-ttu-id="9fa41-139">n/a</span><span class="sxs-lookup"><span data-stu-id="9fa41-139">n/a</span></span><br/>        | <span data-ttu-id="9fa41-140">True、False</span><span class="sxs-lookup"><span data-stu-id="9fa41-140">True, False</span></span><br/>                                                                                                                                                                | <span data-ttu-id="9fa41-141">定義選項，當選取此選項時，會停用此功能。</span><span class="sxs-lookup"><span data-stu-id="9fa41-141">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="9fa41-142">可延伸標記語言 (XML)  (XML) 內容</span><span class="sxs-lookup"><span data-stu-id="9fa41-142">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="9fa41-143">公用列印架構關鍵字是在 https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords 命名空間中定義。</span><span class="sxs-lookup"><span data-stu-id="9fa41-143">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="9fa41-144">此關鍵字的 public 可延伸標記語言 (XML)  (XML) 內容定義如下：</span><span class="sxs-lookup"><span data-stu-id="9fa41-144">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:PagePhotoPrintingIntent">
  <psf:Property name="SelectionType">
    <psf:Value xsi:type="xs:string">PickOne</psf:Value>
  </psf:Property>
  <!-- No Photoprinting Intent (Allows the application to specify no intent resolution.  (PrintTicket settings should not be altered) -->
  <psf:Option name="psk:None" />
  <!-- Best Quality Photoprinting (Provided mostly for marketing reasons; utilizes the highest capabilities of the device) -->
  <psf:Option name="psk:PhotoBest" />
  <!-- Draft Quality Photoprinting (Quick, low ink volume print for proofing purposes) -->
  <psf:Option name="psk:PhotoDraft" />
  <!-- Standard Quality Photoprinting (OEM suggested settings for standard photo-printing) -->
  <psf:Option name="psk:PhotoStandard" />
</psf:Feature>    
```

## <a name="related-topics"></a><span data-ttu-id="9fa41-145">相關主題</span><span class="sxs-lookup"><span data-stu-id="9fa41-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9fa41-146">列印架構規格</span><span class="sxs-lookup"><span data-stu-id="9fa41-146">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




