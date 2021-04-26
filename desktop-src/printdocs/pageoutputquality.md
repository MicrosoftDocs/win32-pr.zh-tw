---
description: 本主題並非最新的。 如需最新資訊，請參閱列印架構規格。
ms.assetid: 4720f812-a71a-458f-85fa-7885cca0dbbb
title: PageOutputQuality
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c63238c290d6b8f0bb208e94e52dc66c8d2e6be
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/26/2021
ms.locfileid: "107994475"
---
# <a name="pageoutputquality"></a><span data-ttu-id="7bd57-104">PageOutputQuality</span><span class="sxs-lookup"><span data-stu-id="7bd57-104">PageOutputQuality</span></span>

<span data-ttu-id="7bd57-105">本主題並非最新的。</span><span class="sxs-lookup"><span data-stu-id="7bd57-105">This topic is not current.</span></span> <span data-ttu-id="7bd57-106">如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。</span><span class="sxs-lookup"><span data-stu-id="7bd57-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="7bd57-107">描述輸出的品質等級。</span><span class="sxs-lookup"><span data-stu-id="7bd57-107">Describes the quality level of the output.</span></span>

-   [<span data-ttu-id="7bd57-108">項目資訊</span><span class="sxs-lookup"><span data-stu-id="7bd57-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="7bd57-109">結構化內容</span><span class="sxs-lookup"><span data-stu-id="7bd57-109">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="7bd57-110">可延伸標記語言 (XML)  (XML) 內容</span><span class="sxs-lookup"><span data-stu-id="7bd57-110">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="7bd57-111">項目資訊</span><span class="sxs-lookup"><span data-stu-id="7bd57-111">Element Information</span></span>



| <span data-ttu-id="7bd57-112">Name</span><span class="sxs-lookup"><span data-stu-id="7bd57-112">Name</span></span> | <span data-ttu-id="7bd57-113">值</span><span class="sxs-lookup"><span data-stu-id="7bd57-113">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="7bd57-114">項目類型</span><span class="sxs-lookup"><span data-stu-id="7bd57-114">Element Type</span></span> <br/>   | <span data-ttu-id="7bd57-115">功能</span><span class="sxs-lookup"><span data-stu-id="7bd57-115">Feature</span></span><br/> |
| <span data-ttu-id="7bd57-116">範圍前置詞</span><span class="sxs-lookup"><span data-stu-id="7bd57-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="7bd57-117">頁面</span><span class="sxs-lookup"><span data-stu-id="7bd57-117">Page</span></span><br/>    |
| <span data-ttu-id="7bd57-118">注意</span><span class="sxs-lookup"><span data-stu-id="7bd57-118">Notes</span></span> <br/>          | <span data-ttu-id="7bd57-119">None</span><span class="sxs-lookup"><span data-stu-id="7bd57-119">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="7bd57-120">結構化內容</span><span class="sxs-lookup"><span data-stu-id="7bd57-120">Structural Content</span></span>

<span data-ttu-id="7bd57-121">此元素的 XML 結構為：</span><span class="sxs-lookup"><span data-stu-id="7bd57-121">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="7bd57-122">結構變數</span><span class="sxs-lookup"><span data-stu-id="7bd57-122">Structure Variables</span></span>

<span data-ttu-id="7bd57-123">下表概述 XML 結構中所定義之變數的特性。</span><span class="sxs-lookup"><span data-stu-id="7bd57-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="7bd57-124">Name</span><span class="sxs-lookup"><span data-stu-id="7bd57-124">Name</span></span>                               | <span data-ttu-id="7bd57-125">資料類型</span><span class="sxs-lookup"><span data-stu-id="7bd57-125">Data type</span></span>         | <span data-ttu-id="7bd57-126">單位</span><span class="sxs-lookup"><span data-stu-id="7bd57-126">Unit</span></span>                  | <span data-ttu-id="7bd57-127">支援的值</span><span class="sxs-lookup"><span data-stu-id="7bd57-127">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="7bd57-128">總結</span><span class="sxs-lookup"><span data-stu-id="7bd57-128">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="7bd57-129">\_選項名稱\_</span><span class="sxs-lookup"><span data-stu-id="7bd57-129">\_OptionName\_</span></span><br/>          | <span data-ttu-id="7bd57-130">字串</span><span class="sxs-lookup"><span data-stu-id="7bd57-130">string</span></span><br/> | <span data-ttu-id="7bd57-131">字元</span><span class="sxs-lookup"><span data-stu-id="7bd57-131">characters</span></span><br/> | <span data-ttu-id="7bd57-132">以 [XML 命名空間](https://www.w3.org/TR/1999/REC-xml-names-19990114/)所定義的有效完整名稱。</span><span class="sxs-lookup"><span data-stu-id="7bd57-132">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="7bd57-133">如果未指定命名空間，則會假設為預設命名空間。</span><span class="sxs-lookup"><span data-stu-id="7bd57-133">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="7bd57-134">選項的名稱。</span><span class="sxs-lookup"><span data-stu-id="7bd57-134">The name of the option</span></span><br/>                                            |
| <span data-ttu-id="7bd57-135">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="7bd57-135">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="7bd57-136">字串</span><span class="sxs-lookup"><span data-stu-id="7bd57-136">string</span></span><br/> | <span data-ttu-id="7bd57-137">n/a</span><span class="sxs-lookup"><span data-stu-id="7bd57-137">n/a</span></span><br/>        | <span data-ttu-id="7bd57-138">True、False</span><span class="sxs-lookup"><span data-stu-id="7bd57-138">True, False</span></span><br/>                                                                                                                                                                | <span data-ttu-id="7bd57-139">定義選項，當選取此選項時，會停用此功能。</span><span class="sxs-lookup"><span data-stu-id="7bd57-139">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="7bd57-140">可延伸標記語言 (XML)  (XML) 內容</span><span class="sxs-lookup"><span data-stu-id="7bd57-140">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="7bd57-141">公用列印架構關鍵字是在 https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords 命名空間中定義。</span><span class="sxs-lookup"><span data-stu-id="7bd57-141">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="7bd57-142">此關鍵字的 public 可延伸標記語言 (XML)  (XML) 內容定義如下：</span><span class="sxs-lookup"><span data-stu-id="7bd57-142">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="7bd57-143">相關主題</span><span class="sxs-lookup"><span data-stu-id="7bd57-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7bd57-144">列印架構規格</span><span class="sxs-lookup"><span data-stu-id="7bd57-144">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




