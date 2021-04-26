---
description: 本主題並非最新的。 如需最新資訊，請參閱列印架構規格。
ms.assetid: f0b2192d-4bb7-4ba2-8dd0-35a20183ea31
title: DocumentSeparatorSheet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb6bd0d58c5b361b167d22c672b7e080e4498d3e
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/26/2021
ms.locfileid: "107997055"
---
# <a name="documentseparatorsheet"></a><span data-ttu-id="9e561-104">DocumentSeparatorSheet</span><span class="sxs-lookup"><span data-stu-id="9e561-104">DocumentSeparatorSheet</span></span>

<span data-ttu-id="9e561-105">本主題並非最新的。</span><span class="sxs-lookup"><span data-stu-id="9e561-105">This topic is not current.</span></span> <span data-ttu-id="9e561-106">如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。</span><span class="sxs-lookup"><span data-stu-id="9e561-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="9e561-107">描述檔的分隔表用法。</span><span class="sxs-lookup"><span data-stu-id="9e561-107">Describes the separator sheet usage for a document.</span></span> <span data-ttu-id="9e561-108">分隔表應該會出現在輸出中，如下列指定的選項所示。</span><span class="sxs-lookup"><span data-stu-id="9e561-108">Separator sheets should appear in the output as indicated by the Option specified below.</span></span>

-   [<span data-ttu-id="9e561-109">項目資訊</span><span class="sxs-lookup"><span data-stu-id="9e561-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="9e561-110">結構化內容</span><span class="sxs-lookup"><span data-stu-id="9e561-110">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="9e561-111">可延伸標記語言 (XML)  (XML) 內容</span><span class="sxs-lookup"><span data-stu-id="9e561-111">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="9e561-112">項目資訊</span><span class="sxs-lookup"><span data-stu-id="9e561-112">Element Information</span></span>



| <span data-ttu-id="9e561-113">Name</span><span class="sxs-lookup"><span data-stu-id="9e561-113">Name</span></span> | <span data-ttu-id="9e561-114">值</span><span class="sxs-lookup"><span data-stu-id="9e561-114">Value</span></span> |
|----------------------------|---------------------|
| <span data-ttu-id="9e561-115">項目類型</span><span class="sxs-lookup"><span data-stu-id="9e561-115">Element Type</span></span> <br/>   | <span data-ttu-id="9e561-116">功能</span><span class="sxs-lookup"><span data-stu-id="9e561-116">Feature</span></span><br/>  |
| <span data-ttu-id="9e561-117">範圍前置詞</span><span class="sxs-lookup"><span data-stu-id="9e561-117">Scoping Prefix</span></span> <br/> | <span data-ttu-id="9e561-118">文件</span><span class="sxs-lookup"><span data-stu-id="9e561-118">Document</span></span><br/> |
| <span data-ttu-id="9e561-119">注意</span><span class="sxs-lookup"><span data-stu-id="9e561-119">Notes</span></span> <br/>          | <span data-ttu-id="9e561-120">None</span><span class="sxs-lookup"><span data-stu-id="9e561-120">None</span></span><br/>     |



 

## <a name="structural-content"></a><span data-ttu-id="9e561-121">結構化內容</span><span class="sxs-lookup"><span data-stu-id="9e561-121">Structural Content</span></span>

<span data-ttu-id="9e561-122">此元素的 XML 結構為：</span><span class="sxs-lookup"><span data-stu-id="9e561-122">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:DocumentSeparatorSheet">
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

## <a name="structure-variables"></a><span data-ttu-id="9e561-123">結構變數</span><span class="sxs-lookup"><span data-stu-id="9e561-123">Structure Variables</span></span>

<span data-ttu-id="9e561-124">下表概述 XML 結構中所定義之變數的特性。</span><span class="sxs-lookup"><span data-stu-id="9e561-124">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="9e561-125">Name</span><span class="sxs-lookup"><span data-stu-id="9e561-125">Name</span></span>                               | <span data-ttu-id="9e561-126">資料類型</span><span class="sxs-lookup"><span data-stu-id="9e561-126">Data type</span></span>         | <span data-ttu-id="9e561-127">單位</span><span class="sxs-lookup"><span data-stu-id="9e561-127">Unit</span></span>                  | <span data-ttu-id="9e561-128">支援的值</span><span class="sxs-lookup"><span data-stu-id="9e561-128">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="9e561-129">總結</span><span class="sxs-lookup"><span data-stu-id="9e561-129">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="9e561-130">\_選項名稱\_</span><span class="sxs-lookup"><span data-stu-id="9e561-130">\_OptionName\_</span></span><br/>          | <span data-ttu-id="9e561-131">字串</span><span class="sxs-lookup"><span data-stu-id="9e561-131">string</span></span><br/> | <span data-ttu-id="9e561-132">字元</span><span class="sxs-lookup"><span data-stu-id="9e561-132">characters</span></span><br/> | <span data-ttu-id="9e561-133">以 [XML 命名空間](https://www.w3.org/TR/1999/REC-xml-names-19990114/)所定義的有效完整名稱。</span><span class="sxs-lookup"><span data-stu-id="9e561-133">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="9e561-134">如果未指定命名空間，則會假設為預設命名空間。</span><span class="sxs-lookup"><span data-stu-id="9e561-134">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="9e561-135">選項的名稱。</span><span class="sxs-lookup"><span data-stu-id="9e561-135">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="9e561-136">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="9e561-136">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="9e561-137">字串</span><span class="sxs-lookup"><span data-stu-id="9e561-137">string</span></span><br/> | <span data-ttu-id="9e561-138">n/a</span><span class="sxs-lookup"><span data-stu-id="9e561-138">n/a</span></span><br/>        | <span data-ttu-id="9e561-139">True、False。</span><span class="sxs-lookup"><span data-stu-id="9e561-139">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="9e561-140">定義選項，當選取此選項時，會停用此功能。</span><span class="sxs-lookup"><span data-stu-id="9e561-140">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="9e561-141">可延伸標記語言 (XML)  (XML) 內容</span><span class="sxs-lookup"><span data-stu-id="9e561-141">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="9e561-142">公用列印架構關鍵字是在 https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords 命名空間中定義。</span><span class="sxs-lookup"><span data-stu-id="9e561-142">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="9e561-143">此關鍵字的 public 可延伸標記語言 (XML)  (XML) 內容定義如下：</span><span class="sxs-lookup"><span data-stu-id="9e561-143">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:DocumentSeparatorSheet">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!-- Specifies a separator sheet at the start and end of the document. -->
  <psf:Option name="psk:BothSheets" />
  <!-- Specifies a separator sheet at the end of the document. -->
  <psf:Option name="psk:EndSheet" />
  <!-- Specifies no separator sheet(s). -->
  <psf:Option name="psk:None" />
  <!-- Specifies a separator sheet at the start of the document. -->
  <psf:Option name="psk:StartSheet" />
</psf:Feature>
    
```

## <a name="related-topics"></a><span data-ttu-id="9e561-144">相關主題</span><span class="sxs-lookup"><span data-stu-id="9e561-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9e561-145">列印架構規格</span><span class="sxs-lookup"><span data-stu-id="9e561-145">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




