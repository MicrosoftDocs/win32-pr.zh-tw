---
description: 取得 PagePoster 使用者可設定元素的相關資訊。 本主題並非最新的。 如需最新資訊，請參閱列印架構規格。
ms.assetid: 66a3ac9a-674e-4f16-a2d8-8f5b753f876c
title: PagePoster
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72b8bb7b57074fe058c7cc5be8dd609577ceb6c1
ms.sourcegitcommit: 998d50f6def8a25850fc113fc8a2df903c829c5e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/09/2021
ms.locfileid: "113548966"
---
# <a name="pageposter"></a><span data-ttu-id="c7e3d-105">PagePoster</span><span class="sxs-lookup"><span data-stu-id="c7e3d-105">PagePoster</span></span>

<span data-ttu-id="c7e3d-106">本主題並非最新的。</span><span class="sxs-lookup"><span data-stu-id="c7e3d-106">This topic is not current.</span></span> <span data-ttu-id="c7e3d-107">如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。</span><span class="sxs-lookup"><span data-stu-id="c7e3d-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="c7e3d-108">描述單一頁面至多個實體媒體工作表的輸出。</span><span class="sxs-lookup"><span data-stu-id="c7e3d-108">Describes the output of a single page to multiple physical media sheets.</span></span>

-   [<span data-ttu-id="c7e3d-109">項目資訊</span><span class="sxs-lookup"><span data-stu-id="c7e3d-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="c7e3d-110">結構化內容</span><span class="sxs-lookup"><span data-stu-id="c7e3d-110">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="c7e3d-111">可延伸標記語言 (XML)  (XML) 內容</span><span class="sxs-lookup"><span data-stu-id="c7e3d-111">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="c7e3d-112">項目資訊</span><span class="sxs-lookup"><span data-stu-id="c7e3d-112">Element Information</span></span>



| <span data-ttu-id="c7e3d-113">Name</span><span class="sxs-lookup"><span data-stu-id="c7e3d-113">Name</span></span> | <span data-ttu-id="c7e3d-114">值</span><span class="sxs-lookup"><span data-stu-id="c7e3d-114">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="c7e3d-115">項目類型</span><span class="sxs-lookup"><span data-stu-id="c7e3d-115">Element Type</span></span> <br/>   | <span data-ttu-id="c7e3d-116">功能</span><span class="sxs-lookup"><span data-stu-id="c7e3d-116">Feature</span></span><br/> |
| <span data-ttu-id="c7e3d-117">範圍前置詞</span><span class="sxs-lookup"><span data-stu-id="c7e3d-117">Scoping Prefix</span></span> <br/> | <span data-ttu-id="c7e3d-118">頁面</span><span class="sxs-lookup"><span data-stu-id="c7e3d-118">Page</span></span><br/>    |
| <span data-ttu-id="c7e3d-119">注意</span><span class="sxs-lookup"><span data-stu-id="c7e3d-119">Notes</span></span> <br/>          | <span data-ttu-id="c7e3d-120">None</span><span class="sxs-lookup"><span data-stu-id="c7e3d-120">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="c7e3d-121">結構化內容</span><span class="sxs-lookup"><span data-stu-id="c7e3d-121">Structural Content</span></span>

<span data-ttu-id="c7e3d-122">此元素的 XML 結構為：</span><span class="sxs-lookup"><span data-stu-id="c7e3d-122">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:PagePoster">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option name="psk:_OptionName_">
    <psf:Property name="psf:IdentityOption">
      <psf:Value xsi:type="xs:string">_IdentityOptionValue_</psf:Value>
    </psf:Property>
    <psf:ScoredProperty name="psk:SheetsPerPage">
      <psf:Value xsi:type="xs:integer">_SheetsPerPageValue_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature>
      
```

## <a name="structure-variables"></a><span data-ttu-id="c7e3d-123">結構變數</span><span class="sxs-lookup"><span data-stu-id="c7e3d-123">Structure Variables</span></span>

<span data-ttu-id="c7e3d-124">下表概述 XML 結構中所定義之變數的特性。</span><span class="sxs-lookup"><span data-stu-id="c7e3d-124">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="c7e3d-125">Name</span><span class="sxs-lookup"><span data-stu-id="c7e3d-125">Name</span></span>                               | <span data-ttu-id="c7e3d-126">資料類型</span><span class="sxs-lookup"><span data-stu-id="c7e3d-126">Data type</span></span>          | <span data-ttu-id="c7e3d-127">單位</span><span class="sxs-lookup"><span data-stu-id="c7e3d-127">Unit</span></span>                  | <span data-ttu-id="c7e3d-128">支援的值</span><span class="sxs-lookup"><span data-stu-id="c7e3d-128">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="c7e3d-129">摘要</span><span class="sxs-lookup"><span data-stu-id="c7e3d-129">Summary</span></span>                                                                      |
|------------------------------------|--------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="c7e3d-130">\_選項名稱\_</span><span class="sxs-lookup"><span data-stu-id="c7e3d-130">\_OptionName\_</span></span><br/>          | <span data-ttu-id="c7e3d-131">string</span><span class="sxs-lookup"><span data-stu-id="c7e3d-131">string</span></span><br/>  | <span data-ttu-id="c7e3d-132">字元</span><span class="sxs-lookup"><span data-stu-id="c7e3d-132">characters</span></span><br/> | <span data-ttu-id="c7e3d-133">以 [XML 命名空間](https://www.w3.org/TR/1999/REC-xml-names-19990114/)所定義的有效完整名稱。</span><span class="sxs-lookup"><span data-stu-id="c7e3d-133">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="c7e3d-134">如果未指定命名空間，則會假設為預設命名空間。</span><span class="sxs-lookup"><span data-stu-id="c7e3d-134">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="c7e3d-135">選項的名稱。</span><span class="sxs-lookup"><span data-stu-id="c7e3d-135">The name of the option</span></span><br/>                                            |
| <span data-ttu-id="c7e3d-136">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="c7e3d-136">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="c7e3d-137">string</span><span class="sxs-lookup"><span data-stu-id="c7e3d-137">string</span></span><br/>  | <span data-ttu-id="c7e3d-138">n/a</span><span class="sxs-lookup"><span data-stu-id="c7e3d-138">n/a</span></span><br/>        | <span data-ttu-id="c7e3d-139">True、False</span><span class="sxs-lookup"><span data-stu-id="c7e3d-139">True, False</span></span><br/>                                                                                                                                                                | <span data-ttu-id="c7e3d-140">定義選項，當選取此選項時，會停用此功能。</span><span class="sxs-lookup"><span data-stu-id="c7e3d-140">Defines an Option which when selected would disable this feature.</span></span><br/> |
| <span data-ttu-id="c7e3d-141">\_SheetsPerPageValue\_</span><span class="sxs-lookup"><span data-stu-id="c7e3d-141">\_SheetsPerPageValue\_</span></span><br/>  | <span data-ttu-id="c7e3d-142">整數</span><span class="sxs-lookup"><span data-stu-id="c7e3d-142">integer</span></span><br/> | <span data-ttu-id="c7e3d-143">頁面</span><span class="sxs-lookup"><span data-stu-id="c7e3d-143">pages</span></span><br/>      | <span data-ttu-id="c7e3d-144">大於或等於0。</span><span class="sxs-lookup"><span data-stu-id="c7e3d-144">Greater than or equal to 0.</span></span><br/>                                                                                                                                                | <span data-ttu-id="c7e3d-145">指定每個邏輯頁面的實體工作表數目。</span><span class="sxs-lookup"><span data-stu-id="c7e3d-145">Specifies the number of physical sheets per logical page.</span></span><br/>         |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="c7e3d-146">可延伸標記語言 (XML)  (XML) 內容</span><span class="sxs-lookup"><span data-stu-id="c7e3d-146">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="c7e3d-147">公用列印架構關鍵字是在 https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords 命名空間中定義。</span><span class="sxs-lookup"><span data-stu-id="c7e3d-147">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="c7e3d-148">此關鍵字的 public 可延伸標記語言 (XML)  (XML) 內容定義如下：</span><span class="sxs-lookup"><span data-stu-id="c7e3d-148">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:PagePoster">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!-- Specifies media sheets per page. -->
  <psf:Option>
    <psf:ScoredProperty name="psk:SheetsPerPage">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature>
```

## <a name="related-topics"></a><span data-ttu-id="c7e3d-149">相關主題</span><span class="sxs-lookup"><span data-stu-id="c7e3d-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c7e3d-150">列印架構規格</span><span class="sxs-lookup"><span data-stu-id="c7e3d-150">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




