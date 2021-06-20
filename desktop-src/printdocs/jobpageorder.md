---
description: 深入瞭解 JobPageOrder 元素，其定義輸出的實體頁面順序。
ms.assetid: 0c255d50-8b0e-4ecd-876d-eaaccdca7b27
title: JobPageOrder
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa2216330034c458095af7e67ff0904100126451
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/19/2021
ms.locfileid: "112408741"
---
# <a name="jobpageorder"></a><span data-ttu-id="ab0af-103">JobPageOrder</span><span class="sxs-lookup"><span data-stu-id="ab0af-103">JobPageOrder</span></span>

<span data-ttu-id="ab0af-104">本主題並非最新的。</span><span class="sxs-lookup"><span data-stu-id="ab0af-104">This topic is not current.</span></span> <span data-ttu-id="ab0af-105">如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。</span><span class="sxs-lookup"><span data-stu-id="ab0af-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="ab0af-106">定義輸出的實體頁面順序。</span><span class="sxs-lookup"><span data-stu-id="ab0af-106">Defines the order of physical pages for the output.</span></span>

-   [<span data-ttu-id="ab0af-107">項目資訊</span><span class="sxs-lookup"><span data-stu-id="ab0af-107">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="ab0af-108">結構化內容</span><span class="sxs-lookup"><span data-stu-id="ab0af-108">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="ab0af-109">可延伸標記語言 (XML)  (XML) 內容</span><span class="sxs-lookup"><span data-stu-id="ab0af-109">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="ab0af-110">項目資訊</span><span class="sxs-lookup"><span data-stu-id="ab0af-110">Element Information</span></span>



| <span data-ttu-id="ab0af-111">Name</span><span class="sxs-lookup"><span data-stu-id="ab0af-111">Name</span></span> | <span data-ttu-id="ab0af-112">值</span><span class="sxs-lookup"><span data-stu-id="ab0af-112">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="ab0af-113">項目類型</span><span class="sxs-lookup"><span data-stu-id="ab0af-113">Element Type</span></span> <br/>   | <span data-ttu-id="ab0af-114">功能</span><span class="sxs-lookup"><span data-stu-id="ab0af-114">Feature</span></span><br/> |
| <span data-ttu-id="ab0af-115">範圍前置詞</span><span class="sxs-lookup"><span data-stu-id="ab0af-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="ab0af-116">工作 (Job)</span><span class="sxs-lookup"><span data-stu-id="ab0af-116">Job</span></span><br/>     |
| <span data-ttu-id="ab0af-117">注意</span><span class="sxs-lookup"><span data-stu-id="ab0af-117">Notes</span></span> <br/>          | <span data-ttu-id="ab0af-118">None</span><span class="sxs-lookup"><span data-stu-id="ab0af-118">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="ab0af-119">結構化內容</span><span class="sxs-lookup"><span data-stu-id="ab0af-119">Structural Content</span></span>

<span data-ttu-id="ab0af-120">此元素的 XML 結構為：</span><span class="sxs-lookup"><span data-stu-id="ab0af-120">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:JobPageOrder">
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

## <a name="structure-variables"></a><span data-ttu-id="ab0af-121">結構變數</span><span class="sxs-lookup"><span data-stu-id="ab0af-121">Structure Variables</span></span>

<span data-ttu-id="ab0af-122">下表概述 XML 結構中所定義之變數的特性。</span><span class="sxs-lookup"><span data-stu-id="ab0af-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="ab0af-123">Name</span><span class="sxs-lookup"><span data-stu-id="ab0af-123">Name</span></span>                               | <span data-ttu-id="ab0af-124">資料類型</span><span class="sxs-lookup"><span data-stu-id="ab0af-124">Data type</span></span>         | <span data-ttu-id="ab0af-125">單位</span><span class="sxs-lookup"><span data-stu-id="ab0af-125">Unit</span></span>                  | <span data-ttu-id="ab0af-126">支援的值</span><span class="sxs-lookup"><span data-stu-id="ab0af-126">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="ab0af-127">總結</span><span class="sxs-lookup"><span data-stu-id="ab0af-127">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="ab0af-128">\_選項名稱\_</span><span class="sxs-lookup"><span data-stu-id="ab0af-128">\_OptionName\_</span></span><br/>          | <span data-ttu-id="ab0af-129">string</span><span class="sxs-lookup"><span data-stu-id="ab0af-129">string</span></span><br/> | <span data-ttu-id="ab0af-130">字元</span><span class="sxs-lookup"><span data-stu-id="ab0af-130">characters</span></span><br/> | <span data-ttu-id="ab0af-131">以 [XML 命名空間](https://www.w3.org/TR/1999/REC-xml-names-19990114/)所定義的有效完整名稱。</span><span class="sxs-lookup"><span data-stu-id="ab0af-131">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="ab0af-132">如果未指定命名空間，則會假設為預設命名空間。</span><span class="sxs-lookup"><span data-stu-id="ab0af-132">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="ab0af-133">選項的名稱。</span><span class="sxs-lookup"><span data-stu-id="ab0af-133">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="ab0af-134">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="ab0af-134">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="ab0af-135">string</span><span class="sxs-lookup"><span data-stu-id="ab0af-135">string</span></span><br/> | <span data-ttu-id="ab0af-136">n/a</span><span class="sxs-lookup"><span data-stu-id="ab0af-136">n/a</span></span><br/>        | <span data-ttu-id="ab0af-137">True、False。</span><span class="sxs-lookup"><span data-stu-id="ab0af-137">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="ab0af-138">定義選項，當選取此選項時，會停用此功能。</span><span class="sxs-lookup"><span data-stu-id="ab0af-138">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="ab0af-139">可延伸標記語言 (XML)  (XML) 內容</span><span class="sxs-lookup"><span data-stu-id="ab0af-139">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="ab0af-140">公用列印架構關鍵字是在 https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords 命名空間中定義。</span><span class="sxs-lookup"><span data-stu-id="ab0af-140">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="ab0af-141">此關鍵字的 public 可延伸標記語言 (XML)  (XML) 內容定義如下：</span><span class="sxs-lookup"><span data-stu-id="ab0af-141">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:JobPageOrder">
  <psf:Property name="psf:SelectionType">
   <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!-- Specifies front to back page order. -->
  <psf:Option name="psk:Standard" />
  <!-- Specifies back to front page order. -->
  <psf:Option name="psk:Reverse" />
</psf:Feature>
```

## <a name="related-topics"></a><span data-ttu-id="ab0af-142">相關主題</span><span class="sxs-lookup"><span data-stu-id="ab0af-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ab0af-143">列印架構規格</span><span class="sxs-lookup"><span data-stu-id="ab0af-143">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




