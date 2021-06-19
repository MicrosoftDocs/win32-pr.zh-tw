---
description: 閱讀 PageNegativeImage 使用者可設定的元素。 本主題並非最新的。 如需最新資訊，請參閱列印架構規格。
ms.assetid: 4f6ff85c-8cad-4b9b-8a1d-ce41ed7dfbed
title: PageNegativeImage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a1e1a9de2d82135adb82c68f45785ee3763e41a
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/19/2021
ms.locfileid: "112395653"
---
# <a name="pagenegativeimage"></a><span data-ttu-id="7b934-105">PageNegativeImage</span><span class="sxs-lookup"><span data-stu-id="7b934-105">PageNegativeImage</span></span>

<span data-ttu-id="7b934-106">本主題並非最新的。</span><span class="sxs-lookup"><span data-stu-id="7b934-106">This topic is not current.</span></span> <span data-ttu-id="7b934-107">如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。</span><span class="sxs-lookup"><span data-stu-id="7b934-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="7b934-108">描述輸出的負設定。</span><span class="sxs-lookup"><span data-stu-id="7b934-108">Describes the negative setting of the output.</span></span>

-   [<span data-ttu-id="7b934-109">項目資訊</span><span class="sxs-lookup"><span data-stu-id="7b934-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="7b934-110">結構化內容</span><span class="sxs-lookup"><span data-stu-id="7b934-110">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="7b934-111">可延伸標記語言 (XML)  (XML) 內容</span><span class="sxs-lookup"><span data-stu-id="7b934-111">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="7b934-112">項目資訊</span><span class="sxs-lookup"><span data-stu-id="7b934-112">Element Information</span></span>



| <span data-ttu-id="7b934-113">Name</span><span class="sxs-lookup"><span data-stu-id="7b934-113">Name</span></span> | <span data-ttu-id="7b934-114">值</span><span class="sxs-lookup"><span data-stu-id="7b934-114">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="7b934-115">項目類型</span><span class="sxs-lookup"><span data-stu-id="7b934-115">Element Type</span></span> <br/>   | <span data-ttu-id="7b934-116">功能</span><span class="sxs-lookup"><span data-stu-id="7b934-116">Feature</span></span><br/> |
| <span data-ttu-id="7b934-117">範圍前置詞</span><span class="sxs-lookup"><span data-stu-id="7b934-117">Scoping Prefix</span></span> <br/> | <span data-ttu-id="7b934-118">頁面</span><span class="sxs-lookup"><span data-stu-id="7b934-118">Page</span></span><br/>    |
| <span data-ttu-id="7b934-119">注意</span><span class="sxs-lookup"><span data-stu-id="7b934-119">Notes</span></span> <br/>          | <span data-ttu-id="7b934-120">None</span><span class="sxs-lookup"><span data-stu-id="7b934-120">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="7b934-121">結構化內容</span><span class="sxs-lookup"><span data-stu-id="7b934-121">Structural Content</span></span>

<span data-ttu-id="7b934-122">此元素的 XML 結構為：</span><span class="sxs-lookup"><span data-stu-id="7b934-122">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:PageNegativeImage">
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

## <a name="structure-variables"></a><span data-ttu-id="7b934-123">結構變數</span><span class="sxs-lookup"><span data-stu-id="7b934-123">Structure Variables</span></span>

<span data-ttu-id="7b934-124">下表概述 XML 結構中所定義之變數的特性。</span><span class="sxs-lookup"><span data-stu-id="7b934-124">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="7b934-125">Name</span><span class="sxs-lookup"><span data-stu-id="7b934-125">Name</span></span>                               | <span data-ttu-id="7b934-126">資料類型</span><span class="sxs-lookup"><span data-stu-id="7b934-126">Data type</span></span>         | <span data-ttu-id="7b934-127">單位</span><span class="sxs-lookup"><span data-stu-id="7b934-127">Unit</span></span>                  | <span data-ttu-id="7b934-128">支援的值</span><span class="sxs-lookup"><span data-stu-id="7b934-128">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="7b934-129">總結</span><span class="sxs-lookup"><span data-stu-id="7b934-129">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="7b934-130">\_選項名稱\_</span><span class="sxs-lookup"><span data-stu-id="7b934-130">\_OptionName\_</span></span><br/>          | <span data-ttu-id="7b934-131">string</span><span class="sxs-lookup"><span data-stu-id="7b934-131">string</span></span><br/> | <span data-ttu-id="7b934-132">字元</span><span class="sxs-lookup"><span data-stu-id="7b934-132">characters</span></span><br/> | <span data-ttu-id="7b934-133">以 [XML 命名空間](https://www.w3.org/TR/1999/REC-xml-names-19990114/)所定義的有效完整名稱。</span><span class="sxs-lookup"><span data-stu-id="7b934-133">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="7b934-134">如果未指定命名空間，則會假設為預設命名空間。</span><span class="sxs-lookup"><span data-stu-id="7b934-134">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="7b934-135">選項的名稱。</span><span class="sxs-lookup"><span data-stu-id="7b934-135">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="7b934-136">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="7b934-136">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="7b934-137">string</span><span class="sxs-lookup"><span data-stu-id="7b934-137">string</span></span><br/> | <span data-ttu-id="7b934-138">n/a</span><span class="sxs-lookup"><span data-stu-id="7b934-138">n/a</span></span><br/>        | <span data-ttu-id="7b934-139">True、False。</span><span class="sxs-lookup"><span data-stu-id="7b934-139">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="7b934-140">定義選項，當選取此選項時，會停用此功能。</span><span class="sxs-lookup"><span data-stu-id="7b934-140">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="7b934-141">可延伸標記語言 (XML)  (XML) 內容</span><span class="sxs-lookup"><span data-stu-id="7b934-141">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="7b934-142">公用列印架構關鍵字是在 https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords 命名空間中定義。</span><span class="sxs-lookup"><span data-stu-id="7b934-142">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="7b934-143">此關鍵字的 public 可延伸標記語言 (XML)  (XML) 內容定義如下：</span><span class="sxs-lookup"><span data-stu-id="7b934-143">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:PageNegativeImage">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!-- Specifies the output should be the negative image. -->
  <psf:Option name="psk:Negative" />
  <!-- Specifies the output should be the non-negative image. -->
  <psf:Option name="psk:None" />
</psf:Feature>
    
```

## <a name="related-topics"></a><span data-ttu-id="7b934-144">相關主題</span><span class="sxs-lookup"><span data-stu-id="7b934-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7b934-145">列印架構規格</span><span class="sxs-lookup"><span data-stu-id="7b934-145">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




