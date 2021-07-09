---
description: 深入瞭解 PageForceFrontSide 使用者可設定的元素。 本主題並非最新的。 如需最新資訊，請參閱列印架構規格。
ms.assetid: 0658c808-f050-41f3-90b6-2a013b616b58
title: PageForceFrontSide
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79f22e9ec52b7cee72e8f3a479d161e9abb765c4
ms.sourcegitcommit: 998d50f6def8a25850fc113fc8a2df903c829c5e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/09/2021
ms.locfileid: "113549186"
---
# <a name="pageforcefrontside"></a><span data-ttu-id="d0f45-105">PageForceFrontSide</span><span class="sxs-lookup"><span data-stu-id="d0f45-105">PageForceFrontSide</span></span>

<span data-ttu-id="d0f45-106">本主題並非最新的。</span><span class="sxs-lookup"><span data-stu-id="d0f45-106">This topic is not current.</span></span> <span data-ttu-id="d0f45-107">如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。</span><span class="sxs-lookup"><span data-stu-id="d0f45-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="d0f45-108">強制輸出出現在媒體工作表的前方。</span><span class="sxs-lookup"><span data-stu-id="d0f45-108">Forces the output to appear on the front of a media sheet.</span></span> <span data-ttu-id="d0f45-109">與每一邊具有不同表面的媒體工作表相關。</span><span class="sxs-lookup"><span data-stu-id="d0f45-109">Relevant to media sheets with different surfaces on each side.</span></span> <span data-ttu-id="d0f45-110">如果這項功能幹擾處理選項 (例如 DocumentDuplex) ，則 PageForceFrontSide 會優先使用該功能所套用的特定頁面。</span><span class="sxs-lookup"><span data-stu-id="d0f45-110">In cases where this feature interferes with processing options (such as DocumentDuplex), PageForceFrontSide takes precedence for the specific page to which the feature applies.</span></span>

-   [<span data-ttu-id="d0f45-111">項目資訊</span><span class="sxs-lookup"><span data-stu-id="d0f45-111">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="d0f45-112">結構化內容</span><span class="sxs-lookup"><span data-stu-id="d0f45-112">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="d0f45-113">可延伸標記語言 (XML)  (XML) 內容</span><span class="sxs-lookup"><span data-stu-id="d0f45-113">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="d0f45-114">項目資訊</span><span class="sxs-lookup"><span data-stu-id="d0f45-114">Element Information</span></span>



| <span data-ttu-id="d0f45-115">Name</span><span class="sxs-lookup"><span data-stu-id="d0f45-115">Name</span></span> | <span data-ttu-id="d0f45-116">值</span><span class="sxs-lookup"><span data-stu-id="d0f45-116">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="d0f45-117">項目類型</span><span class="sxs-lookup"><span data-stu-id="d0f45-117">Element Type</span></span> <br/>   | <span data-ttu-id="d0f45-118">功能</span><span class="sxs-lookup"><span data-stu-id="d0f45-118">Feature</span></span><br/> |
| <span data-ttu-id="d0f45-119">範圍前置詞</span><span class="sxs-lookup"><span data-stu-id="d0f45-119">Scoping Prefix</span></span> <br/> | <span data-ttu-id="d0f45-120">頁面</span><span class="sxs-lookup"><span data-stu-id="d0f45-120">Page</span></span><br/>    |
| <span data-ttu-id="d0f45-121">注意</span><span class="sxs-lookup"><span data-stu-id="d0f45-121">Notes</span></span> <br/>          | <span data-ttu-id="d0f45-122">None</span><span class="sxs-lookup"><span data-stu-id="d0f45-122">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="d0f45-123">結構化內容</span><span class="sxs-lookup"><span data-stu-id="d0f45-123">Structural Content</span></span>

<span data-ttu-id="d0f45-124">此元素的 XML 結構為：</span><span class="sxs-lookup"><span data-stu-id="d0f45-124">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:PageForceFrontSide">
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

## <a name="structure-variables"></a><span data-ttu-id="d0f45-125">結構變數</span><span class="sxs-lookup"><span data-stu-id="d0f45-125">Structure Variables</span></span>

<span data-ttu-id="d0f45-126">下表概述 XML 結構中所定義之變數的特性。</span><span class="sxs-lookup"><span data-stu-id="d0f45-126">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="d0f45-127">Name</span><span class="sxs-lookup"><span data-stu-id="d0f45-127">Name</span></span>                               | <span data-ttu-id="d0f45-128">資料類型</span><span class="sxs-lookup"><span data-stu-id="d0f45-128">Data type</span></span>         | <span data-ttu-id="d0f45-129">單位</span><span class="sxs-lookup"><span data-stu-id="d0f45-129">Unit</span></span>                  | <span data-ttu-id="d0f45-130">支援的值</span><span class="sxs-lookup"><span data-stu-id="d0f45-130">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="d0f45-131">摘要</span><span class="sxs-lookup"><span data-stu-id="d0f45-131">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="d0f45-132">\_選項名稱\_</span><span class="sxs-lookup"><span data-stu-id="d0f45-132">\_OptionName\_</span></span><br/>          | <span data-ttu-id="d0f45-133">string</span><span class="sxs-lookup"><span data-stu-id="d0f45-133">string</span></span><br/> | <span data-ttu-id="d0f45-134">字元</span><span class="sxs-lookup"><span data-stu-id="d0f45-134">characters</span></span><br/> | <span data-ttu-id="d0f45-135">以 [XML 命名空間](https://www.w3.org/TR/1999/REC-xml-names-19990114/)所定義的有效完整名稱。</span><span class="sxs-lookup"><span data-stu-id="d0f45-135">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="d0f45-136">如果未指定命名空間，則會假設為預設命名空間。</span><span class="sxs-lookup"><span data-stu-id="d0f45-136">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="d0f45-137">選項的名稱。</span><span class="sxs-lookup"><span data-stu-id="d0f45-137">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="d0f45-138">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="d0f45-138">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="d0f45-139">string</span><span class="sxs-lookup"><span data-stu-id="d0f45-139">string</span></span><br/> | <span data-ttu-id="d0f45-140">n/a</span><span class="sxs-lookup"><span data-stu-id="d0f45-140">n/a</span></span><br/>        | <span data-ttu-id="d0f45-141">True、False。</span><span class="sxs-lookup"><span data-stu-id="d0f45-141">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="d0f45-142">定義選項，當選取此選項時，會停用此功能。</span><span class="sxs-lookup"><span data-stu-id="d0f45-142">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="d0f45-143">可延伸標記語言 (XML)  (XML) 內容</span><span class="sxs-lookup"><span data-stu-id="d0f45-143">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="d0f45-144">公用列印架構關鍵字是在 https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords 命名空間中定義。</span><span class="sxs-lookup"><span data-stu-id="d0f45-144">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="d0f45-145">此關鍵字的 public 可延伸標記語言 (XML)  (XML) 內容定義如下：</span><span class="sxs-lookup"><span data-stu-id="d0f45-145">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:PageForceFrontSide">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!-- Specifies output is restricted to the front side of the sheet. -->
  <psf:Option name="psk:ForceFrontSide" />
  <!-- Specifies no output restrictions.  -->
  <psf:Option name="psk:None" />
</psf:Feature>    
```

## <a name="related-topics"></a><span data-ttu-id="d0f45-146">相關主題</span><span class="sxs-lookup"><span data-stu-id="d0f45-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d0f45-147">列印架構規格</span><span class="sxs-lookup"><span data-stu-id="d0f45-147">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




