---
description: 深入瞭解 PageOutputQuality 使用者可設定的元素。 本主題並非最新的。 如需最新資訊，請參閱列印架構規格。
ms.assetid: 4720f812-a71a-458f-85fa-7885cca0dbbb
title: PageOutputQuality
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8001d8ffd6bb3ead50a27b9ea36c9849c475576f
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/19/2021
ms.locfileid: "112395585"
---
# <a name="pageoutputquality"></a><span data-ttu-id="754d4-105">PageOutputQuality</span><span class="sxs-lookup"><span data-stu-id="754d4-105">PageOutputQuality</span></span>

<span data-ttu-id="754d4-106">本主題並非最新的。</span><span class="sxs-lookup"><span data-stu-id="754d4-106">This topic is not current.</span></span> <span data-ttu-id="754d4-107">如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。</span><span class="sxs-lookup"><span data-stu-id="754d4-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="754d4-108">描述輸出的品質等級。</span><span class="sxs-lookup"><span data-stu-id="754d4-108">Describes the quality level of the output.</span></span>

-   [<span data-ttu-id="754d4-109">項目資訊</span><span class="sxs-lookup"><span data-stu-id="754d4-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="754d4-110">結構化內容</span><span class="sxs-lookup"><span data-stu-id="754d4-110">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="754d4-111">可延伸標記語言 (XML)  (XML) 內容</span><span class="sxs-lookup"><span data-stu-id="754d4-111">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="754d4-112">項目資訊</span><span class="sxs-lookup"><span data-stu-id="754d4-112">Element Information</span></span>



| <span data-ttu-id="754d4-113">Name</span><span class="sxs-lookup"><span data-stu-id="754d4-113">Name</span></span> | <span data-ttu-id="754d4-114">值</span><span class="sxs-lookup"><span data-stu-id="754d4-114">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="754d4-115">項目類型</span><span class="sxs-lookup"><span data-stu-id="754d4-115">Element Type</span></span> <br/>   | <span data-ttu-id="754d4-116">功能</span><span class="sxs-lookup"><span data-stu-id="754d4-116">Feature</span></span><br/> |
| <span data-ttu-id="754d4-117">範圍前置詞</span><span class="sxs-lookup"><span data-stu-id="754d4-117">Scoping Prefix</span></span> <br/> | <span data-ttu-id="754d4-118">頁面</span><span class="sxs-lookup"><span data-stu-id="754d4-118">Page</span></span><br/>    |
| <span data-ttu-id="754d4-119">注意</span><span class="sxs-lookup"><span data-stu-id="754d4-119">Notes</span></span> <br/>          | <span data-ttu-id="754d4-120">None</span><span class="sxs-lookup"><span data-stu-id="754d4-120">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="754d4-121">結構化內容</span><span class="sxs-lookup"><span data-stu-id="754d4-121">Structural Content</span></span>

<span data-ttu-id="754d4-122">此元素的 XML 結構為：</span><span class="sxs-lookup"><span data-stu-id="754d4-122">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:PageOutputQuality">
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

## <a name="structure-variables"></a><span data-ttu-id="754d4-123">結構變數</span><span class="sxs-lookup"><span data-stu-id="754d4-123">Structure Variables</span></span>

<span data-ttu-id="754d4-124">下表概述 XML 結構中所定義之變數的特性。</span><span class="sxs-lookup"><span data-stu-id="754d4-124">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="754d4-125">Name</span><span class="sxs-lookup"><span data-stu-id="754d4-125">Name</span></span>                               | <span data-ttu-id="754d4-126">資料類型</span><span class="sxs-lookup"><span data-stu-id="754d4-126">Data type</span></span>         | <span data-ttu-id="754d4-127">單位</span><span class="sxs-lookup"><span data-stu-id="754d4-127">Unit</span></span>                  | <span data-ttu-id="754d4-128">支援的值</span><span class="sxs-lookup"><span data-stu-id="754d4-128">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="754d4-129">總結</span><span class="sxs-lookup"><span data-stu-id="754d4-129">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="754d4-130">\_選項名稱\_</span><span class="sxs-lookup"><span data-stu-id="754d4-130">\_OptionName\_</span></span><br/>          | <span data-ttu-id="754d4-131">string</span><span class="sxs-lookup"><span data-stu-id="754d4-131">string</span></span><br/> | <span data-ttu-id="754d4-132">字元</span><span class="sxs-lookup"><span data-stu-id="754d4-132">characters</span></span><br/> | <span data-ttu-id="754d4-133">以 [XML 命名空間](https://www.w3.org/TR/1999/REC-xml-names-19990114/)所定義的有效完整名稱。</span><span class="sxs-lookup"><span data-stu-id="754d4-133">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="754d4-134">如果未指定命名空間，則會假設為預設命名空間。</span><span class="sxs-lookup"><span data-stu-id="754d4-134">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="754d4-135">選項的名稱。</span><span class="sxs-lookup"><span data-stu-id="754d4-135">The name of the option</span></span><br/>                                            |
| <span data-ttu-id="754d4-136">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="754d4-136">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="754d4-137">string</span><span class="sxs-lookup"><span data-stu-id="754d4-137">string</span></span><br/> | <span data-ttu-id="754d4-138">n/a</span><span class="sxs-lookup"><span data-stu-id="754d4-138">n/a</span></span><br/>        | <span data-ttu-id="754d4-139">True、False</span><span class="sxs-lookup"><span data-stu-id="754d4-139">True, False</span></span><br/>                                                                                                                                                                | <span data-ttu-id="754d4-140">定義選項，當選取此選項時，會停用此功能。</span><span class="sxs-lookup"><span data-stu-id="754d4-140">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="754d4-141">可延伸標記語言 (XML)  (XML) 內容</span><span class="sxs-lookup"><span data-stu-id="754d4-141">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="754d4-142">公用列印架構關鍵字是在 https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords 命名空間中定義。</span><span class="sxs-lookup"><span data-stu-id="754d4-142">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="754d4-143">此關鍵字的 public 可延伸標記語言 (XML)  (XML) 內容定義如下：</span><span class="sxs-lookup"><span data-stu-id="754d4-143">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:PageOutputQuality">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!-- Specifies the intent for automatic output (allow the client to automatically choose the best settings). -->
  <psf:Option name="psk:Automatic" />
  <!-- Specifies the intent for draft output (balanced for draft quality text and graphics). -->
  <psf:Option name="psk:Draft" />
  <!-- Specifies the intent for fax output (balanced for standard fax quality). -->
  <psf:Option name="psk:Fax" />
  <!-- Specifies the intent for high quality output (balanced for high quality text and graphics). -->
  <psf:Option name="psk:High" />
  <!-- Specifies the intent for normal output (balanced for good quality text and graphics). -->
  <psf:Option name="psk:Normal" />
  <!-- Specifies the intent for photographic output (images should have the highest quality). -->
  <psf:Option name="psk:Photographic" />
  <!-- Specifies the intent for text only output (graphics may output poorly or not at all). -->
  <psf:Option name="psk:Text" />
</psf:Feature>
    
```

## <a name="related-topics"></a><span data-ttu-id="754d4-144">相關主題</span><span class="sxs-lookup"><span data-stu-id="754d4-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="754d4-145">列印架構規格</span><span class="sxs-lookup"><span data-stu-id="754d4-145">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




