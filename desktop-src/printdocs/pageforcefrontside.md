---
description: 本主題並非最新的。 如需最新資訊，請參閱列印架構規格。
ms.assetid: 0658c808-f050-41f3-90b6-2a013b616b58
title: PageForceFrontSide
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e363050034137bcfb3ff2b779ecda05200865312
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/26/2021
ms.locfileid: "107996935"
---
# <a name="pageforcefrontside"></a><span data-ttu-id="0702b-104">PageForceFrontSide</span><span class="sxs-lookup"><span data-stu-id="0702b-104">PageForceFrontSide</span></span>

<span data-ttu-id="0702b-105">本主題並非最新的。</span><span class="sxs-lookup"><span data-stu-id="0702b-105">This topic is not current.</span></span> <span data-ttu-id="0702b-106">如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。</span><span class="sxs-lookup"><span data-stu-id="0702b-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="0702b-107">強制輸出出現在媒體工作表的前方。</span><span class="sxs-lookup"><span data-stu-id="0702b-107">Forces the output to appear on the front of a media sheet.</span></span> <span data-ttu-id="0702b-108">與每一邊具有不同表面的媒體工作表相關。</span><span class="sxs-lookup"><span data-stu-id="0702b-108">Relevant to media sheets with different surfaces on each side.</span></span> <span data-ttu-id="0702b-109">如果這項功能幹擾處理選項 (例如 DocumentDuplex) ，則 PageForceFrontSide 會優先使用該功能所套用的特定頁面。</span><span class="sxs-lookup"><span data-stu-id="0702b-109">In cases where this feature interferes with processing options (such as DocumentDuplex), PageForceFrontSide takes precedence for the specific page to which the feature applies.</span></span>

-   [<span data-ttu-id="0702b-110">項目資訊</span><span class="sxs-lookup"><span data-stu-id="0702b-110">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="0702b-111">結構化內容</span><span class="sxs-lookup"><span data-stu-id="0702b-111">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="0702b-112">可延伸標記語言 (XML)  (XML) 內容</span><span class="sxs-lookup"><span data-stu-id="0702b-112">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="0702b-113">項目資訊</span><span class="sxs-lookup"><span data-stu-id="0702b-113">Element Information</span></span>



| <span data-ttu-id="0702b-114">Name</span><span class="sxs-lookup"><span data-stu-id="0702b-114">Name</span></span> | <span data-ttu-id="0702b-115">值</span><span class="sxs-lookup"><span data-stu-id="0702b-115">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="0702b-116">項目類型</span><span class="sxs-lookup"><span data-stu-id="0702b-116">Element Type</span></span> <br/>   | <span data-ttu-id="0702b-117">功能</span><span class="sxs-lookup"><span data-stu-id="0702b-117">Feature</span></span><br/> |
| <span data-ttu-id="0702b-118">範圍前置詞</span><span class="sxs-lookup"><span data-stu-id="0702b-118">Scoping Prefix</span></span> <br/> | <span data-ttu-id="0702b-119">頁面</span><span class="sxs-lookup"><span data-stu-id="0702b-119">Page</span></span><br/>    |
| <span data-ttu-id="0702b-120">注意</span><span class="sxs-lookup"><span data-stu-id="0702b-120">Notes</span></span> <br/>          | <span data-ttu-id="0702b-121">None</span><span class="sxs-lookup"><span data-stu-id="0702b-121">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="0702b-122">結構化內容</span><span class="sxs-lookup"><span data-stu-id="0702b-122">Structural Content</span></span>

<span data-ttu-id="0702b-123">此元素的 XML 結構為：</span><span class="sxs-lookup"><span data-stu-id="0702b-123">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="0702b-124">結構變數</span><span class="sxs-lookup"><span data-stu-id="0702b-124">Structure Variables</span></span>

<span data-ttu-id="0702b-125">下表概述 XML 結構中所定義之變數的特性。</span><span class="sxs-lookup"><span data-stu-id="0702b-125">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="0702b-126">Name</span><span class="sxs-lookup"><span data-stu-id="0702b-126">Name</span></span>                               | <span data-ttu-id="0702b-127">資料類型</span><span class="sxs-lookup"><span data-stu-id="0702b-127">Data type</span></span>         | <span data-ttu-id="0702b-128">單位</span><span class="sxs-lookup"><span data-stu-id="0702b-128">Unit</span></span>                  | <span data-ttu-id="0702b-129">支援的值</span><span class="sxs-lookup"><span data-stu-id="0702b-129">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="0702b-130">總結</span><span class="sxs-lookup"><span data-stu-id="0702b-130">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="0702b-131">\_選項名稱\_</span><span class="sxs-lookup"><span data-stu-id="0702b-131">\_OptionName\_</span></span><br/>          | <span data-ttu-id="0702b-132">字串</span><span class="sxs-lookup"><span data-stu-id="0702b-132">string</span></span><br/> | <span data-ttu-id="0702b-133">字元</span><span class="sxs-lookup"><span data-stu-id="0702b-133">characters</span></span><br/> | <span data-ttu-id="0702b-134">以 [XML 命名空間](https://www.w3.org/TR/1999/REC-xml-names-19990114/)所定義的有效完整名稱。</span><span class="sxs-lookup"><span data-stu-id="0702b-134">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="0702b-135">如果未指定命名空間，則會假設為預設命名空間。</span><span class="sxs-lookup"><span data-stu-id="0702b-135">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="0702b-136">選項的名稱。</span><span class="sxs-lookup"><span data-stu-id="0702b-136">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="0702b-137">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="0702b-137">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="0702b-138">字串</span><span class="sxs-lookup"><span data-stu-id="0702b-138">string</span></span><br/> | <span data-ttu-id="0702b-139">n/a</span><span class="sxs-lookup"><span data-stu-id="0702b-139">n/a</span></span><br/>        | <span data-ttu-id="0702b-140">True、False。</span><span class="sxs-lookup"><span data-stu-id="0702b-140">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="0702b-141">定義選項，當選取此選項時，會停用此功能。</span><span class="sxs-lookup"><span data-stu-id="0702b-141">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="0702b-142">可延伸標記語言 (XML)  (XML) 內容</span><span class="sxs-lookup"><span data-stu-id="0702b-142">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="0702b-143">公用列印架構關鍵字是在 https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords 命名空間中定義。</span><span class="sxs-lookup"><span data-stu-id="0702b-143">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="0702b-144">此關鍵字的 public 可延伸標記語言 (XML)  (XML) 內容定義如下：</span><span class="sxs-lookup"><span data-stu-id="0702b-144">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="0702b-145">相關主題</span><span class="sxs-lookup"><span data-stu-id="0702b-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0702b-146">列印架構規格</span><span class="sxs-lookup"><span data-stu-id="0702b-146">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




