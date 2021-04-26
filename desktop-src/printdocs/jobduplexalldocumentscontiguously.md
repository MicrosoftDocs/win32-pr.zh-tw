---
description: 本主題並非最新的。 如需最新資訊，請參閱列印架構規格。
ms.assetid: dd24166c-d5e2-420e-8a8c-e1a25728ab2f
title: JobDuplexAllDocumentsContiguously
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e5ae88213af15b53f71e406b4caf791b80f286f
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/26/2021
ms.locfileid: "107998215"
---
# <a name="jobduplexalldocumentscontiguously"></a><span data-ttu-id="302b0-104">JobDuplexAllDocumentsContiguously</span><span class="sxs-lookup"><span data-stu-id="302b0-104">JobDuplexAllDocumentsContiguously</span></span>

<span data-ttu-id="302b0-105">本主題並非最新的。</span><span class="sxs-lookup"><span data-stu-id="302b0-105">This topic is not current.</span></span> <span data-ttu-id="302b0-106">如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。</span><span class="sxs-lookup"><span data-stu-id="302b0-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="302b0-107">描述輸出的雙工特性。</span><span class="sxs-lookup"><span data-stu-id="302b0-107">Describes the duplex characteristics of the output.</span></span> <span data-ttu-id="302b0-108">雙工功能可在媒體的兩端進行列印。</span><span class="sxs-lookup"><span data-stu-id="302b0-108">The duplex feature allows for printing on both sides of the media.</span></span> <span data-ttu-id="302b0-109">作業中的所有檔都會連續 duplexed 在一起。</span><span class="sxs-lookup"><span data-stu-id="302b0-109">All Documents in the job are duplexed together contiguously.</span></span> <span data-ttu-id="302b0-110">JobDuplexAllDocumentsContiguously 和 DocumentDuplex 互斥。</span><span class="sxs-lookup"><span data-stu-id="302b0-110">JobDuplexAllDocumentsContiguously and DocumentDuplex are mutually exclusive.</span></span> <span data-ttu-id="302b0-111">驅動程式會決定這些關鍵字之間的條件約束處理。</span><span class="sxs-lookup"><span data-stu-id="302b0-111">It is up to the driver to determine constraint handling between these keywords.</span></span>

-   [<span data-ttu-id="302b0-112">項目資訊</span><span class="sxs-lookup"><span data-stu-id="302b0-112">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="302b0-113">結構化內容</span><span class="sxs-lookup"><span data-stu-id="302b0-113">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="302b0-114">可延伸標記語言 (XML)  (XML) 內容</span><span class="sxs-lookup"><span data-stu-id="302b0-114">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="302b0-115">項目資訊</span><span class="sxs-lookup"><span data-stu-id="302b0-115">Element Information</span></span>



| <span data-ttu-id="302b0-116">Name</span><span class="sxs-lookup"><span data-stu-id="302b0-116">Name</span></span> | <span data-ttu-id="302b0-117">值</span><span class="sxs-lookup"><span data-stu-id="302b0-117">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="302b0-118">項目類型</span><span class="sxs-lookup"><span data-stu-id="302b0-118">Element Type</span></span> <br/>   | <span data-ttu-id="302b0-119">功能</span><span class="sxs-lookup"><span data-stu-id="302b0-119">Feature</span></span><br/> |
| <span data-ttu-id="302b0-120">範圍前置詞</span><span class="sxs-lookup"><span data-stu-id="302b0-120">Scoping Prefix</span></span> <br/> | <span data-ttu-id="302b0-121">工作 (Job)</span><span class="sxs-lookup"><span data-stu-id="302b0-121">Job</span></span><br/>     |
| <span data-ttu-id="302b0-122">注意</span><span class="sxs-lookup"><span data-stu-id="302b0-122">Notes</span></span> <br/>          | <span data-ttu-id="302b0-123">None</span><span class="sxs-lookup"><span data-stu-id="302b0-123">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="302b0-124">結構化內容</span><span class="sxs-lookup"><span data-stu-id="302b0-124">Structural Content</span></span>

<span data-ttu-id="302b0-125">此元素的 XML 結構為：</span><span class="sxs-lookup"><span data-stu-id="302b0-125">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:JobDuplexAllDocumentsContiguously">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option name="psk:_OptionName_">
    <psf:Property name="psf:IdentityOption">
      <psf:Value xsi:type="xs:string">_IdentityOptionValue_</psf:Value>
    </psf:Property>
    <psf:ScoredProperty name="psk:DuplexMode">
      <psf:Value xsi:type="xs:string">_DuplexModeValue_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature>      
```

## <a name="structure-variables"></a><span data-ttu-id="302b0-126">結構變數</span><span class="sxs-lookup"><span data-stu-id="302b0-126">Structure Variables</span></span>

<span data-ttu-id="302b0-127">下表概述 XML 結構中所定義之變數的特性。</span><span class="sxs-lookup"><span data-stu-id="302b0-127">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="302b0-128">Name</span><span class="sxs-lookup"><span data-stu-id="302b0-128">Name</span></span>                               | <span data-ttu-id="302b0-129">資料類型</span><span class="sxs-lookup"><span data-stu-id="302b0-129">Data type</span></span>         | <span data-ttu-id="302b0-130">單位</span><span class="sxs-lookup"><span data-stu-id="302b0-130">Unit</span></span>                  | <span data-ttu-id="302b0-131">支援的值</span><span class="sxs-lookup"><span data-stu-id="302b0-131">Supported values</span></span>                                                                                                                                                             | <span data-ttu-id="302b0-132">總結</span><span class="sxs-lookup"><span data-stu-id="302b0-132">Summary</span></span>                                                                                                                                |
|------------------------------------|-------------------|-----------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="302b0-133">\_選項名稱\_</span><span class="sxs-lookup"><span data-stu-id="302b0-133">\_OptionName\_</span></span><br/>          | <span data-ttu-id="302b0-134">字串</span><span class="sxs-lookup"><span data-stu-id="302b0-134">string</span></span><br/> | <span data-ttu-id="302b0-135">字元</span><span class="sxs-lookup"><span data-stu-id="302b0-135">characters</span></span><br/> | <span data-ttu-id="302b0-136">由定義的有效完整名稱 https://www.w3.org/TR/1999/REC-xml-names-19990114/\#dt-qname 。</span><span class="sxs-lookup"><span data-stu-id="302b0-136">Valid fully qualified name as defined by https://www.w3.org/TR/1999/REC-xml-names-19990114/\#dt-qname.</span></span> <span data-ttu-id="302b0-137">如果未指定命名空間，則會假設為預設命名空間。</span><span class="sxs-lookup"><span data-stu-id="302b0-137">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="302b0-138">選項的名稱。</span><span class="sxs-lookup"><span data-stu-id="302b0-138">The name of the option.</span></span><br/>                                                                                                     |
| <span data-ttu-id="302b0-139">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="302b0-139">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="302b0-140">字串</span><span class="sxs-lookup"><span data-stu-id="302b0-140">string</span></span><br/> | <span data-ttu-id="302b0-141">n/a</span><span class="sxs-lookup"><span data-stu-id="302b0-141">n/a</span></span><br/>        | <span data-ttu-id="302b0-142">True、False。</span><span class="sxs-lookup"><span data-stu-id="302b0-142">True, False.</span></span><br/>                                                                                                                                                      | <span data-ttu-id="302b0-143">定義選項，當選取此選項時，會停用此功能。</span><span class="sxs-lookup"><span data-stu-id="302b0-143">Defines an Option which when selected would disable this feature.</span></span><br/>                                                           |
| <span data-ttu-id="302b0-144">\_DuplexModeValue\_</span><span class="sxs-lookup"><span data-stu-id="302b0-144">\_DuplexModeValue\_</span></span><br/>     | <span data-ttu-id="302b0-145">字串</span><span class="sxs-lookup"><span data-stu-id="302b0-145">string</span></span><br/> | <span data-ttu-id="302b0-146">n/a</span><span class="sxs-lookup"><span data-stu-id="302b0-146">n/a</span></span><br/>        | <span data-ttu-id="302b0-147">自動、手動。</span><span class="sxs-lookup"><span data-stu-id="302b0-147">Automatic, Manual.</span></span><br/>                                                                                                                                                | <span data-ttu-id="302b0-148">定義雙工模式。</span><span class="sxs-lookup"><span data-stu-id="302b0-148">Defines the duplex mode.</span></span> <span data-ttu-id="302b0-149">自動雙工是由硬體執行。</span><span class="sxs-lookup"><span data-stu-id="302b0-149">Automatic duplex is performed by hardware.</span></span> <span data-ttu-id="302b0-150">手動雙工是由軟體和使用者執行。</span><span class="sxs-lookup"><span data-stu-id="302b0-150">Manual duplexing is performed by software and the user.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="302b0-151">可延伸標記語言 (XML)  (XML) 內容</span><span class="sxs-lookup"><span data-stu-id="302b0-151">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="302b0-152">公用列印架構關鍵字是在 https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords 命名空間中定義。</span><span class="sxs-lookup"><span data-stu-id="302b0-152">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="302b0-153">此關鍵字的 public 可延伸標記語言 (XML)  (XML) 內容定義如下：</span><span class="sxs-lookup"><span data-stu-id="302b0-153">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:JobDuplexAllDocumentsContiguously">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!-- Specifies one sided printing. -->
  <psf:Option name="psk:OneSided" />
  <!-- Specifies two sided printing such that the page is flipped parallel to the MediaSizeWidth direction. -->
  <psf:Option name="psk:TwoSidedShortEdge">
    <psf:ScoredProperty name="psk:DuplexMode">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies two sided printing such that the page is flipped parallel to the MediaSizeHeight direction. -->
  <psf:Option name="psk:TwoSidedLongEdge">
    <psf:ScoredProperty name="psk:DuplexMode">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature>    
```

## <a name="related-topics"></a><span data-ttu-id="302b0-154">相關主題</span><span class="sxs-lookup"><span data-stu-id="302b0-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="302b0-155">列印架構規格</span><span class="sxs-lookup"><span data-stu-id="302b0-155">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




