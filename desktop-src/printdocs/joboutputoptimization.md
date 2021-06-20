---
description: 深入瞭解 JobOutputOptimization，它會說明工作處理，目的是為了將特定使用案例的輸出優化，如指定的選項所指定。
ms.assetid: 40925dfe-494c-49b5-ae57-de369723ba76
title: JobOutputOptimization
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cdbb65f86b5ed4fd30c056e234b88197d4ab475d
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/19/2021
ms.locfileid: "112408791"
---
# <a name="joboutputoptimization"></a><span data-ttu-id="4f2c0-103">JobOutputOptimization</span><span class="sxs-lookup"><span data-stu-id="4f2c0-103">JobOutputOptimization</span></span>

<span data-ttu-id="4f2c0-104">本主題並非最新的。</span><span class="sxs-lookup"><span data-stu-id="4f2c0-104">This topic is not current.</span></span> <span data-ttu-id="4f2c0-105">如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。</span><span class="sxs-lookup"><span data-stu-id="4f2c0-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="4f2c0-106">描述工作處理，目的是為了將特定使用案例的輸出優化，如指定的選項所指定。</span><span class="sxs-lookup"><span data-stu-id="4f2c0-106">Describes the job processing, intended to optimize the output for particular use scenarios as indicated by the option specified.</span></span>

-   [<span data-ttu-id="4f2c0-107">項目資訊</span><span class="sxs-lookup"><span data-stu-id="4f2c0-107">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="4f2c0-108">結構化內容</span><span class="sxs-lookup"><span data-stu-id="4f2c0-108">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="4f2c0-109">可延伸標記語言 (XML)  (XML) 內容</span><span class="sxs-lookup"><span data-stu-id="4f2c0-109">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="4f2c0-110">項目資訊</span><span class="sxs-lookup"><span data-stu-id="4f2c0-110">Element Information</span></span>



| <span data-ttu-id="4f2c0-111">Name</span><span class="sxs-lookup"><span data-stu-id="4f2c0-111">Name</span></span> | <span data-ttu-id="4f2c0-112">值</span><span class="sxs-lookup"><span data-stu-id="4f2c0-112">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="4f2c0-113">項目類型</span><span class="sxs-lookup"><span data-stu-id="4f2c0-113">Element Type</span></span> <br/>   | <span data-ttu-id="4f2c0-114">功能</span><span class="sxs-lookup"><span data-stu-id="4f2c0-114">Feature</span></span><br/> |
| <span data-ttu-id="4f2c0-115">範圍前置詞</span><span class="sxs-lookup"><span data-stu-id="4f2c0-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="4f2c0-116">工作 (Job)</span><span class="sxs-lookup"><span data-stu-id="4f2c0-116">Job</span></span><br/>     |
| <span data-ttu-id="4f2c0-117">注意</span><span class="sxs-lookup"><span data-stu-id="4f2c0-117">Notes</span></span> <br/>          | <span data-ttu-id="4f2c0-118">None</span><span class="sxs-lookup"><span data-stu-id="4f2c0-118">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="4f2c0-119">結構化內容</span><span class="sxs-lookup"><span data-stu-id="4f2c0-119">Structural Content</span></span>

<span data-ttu-id="4f2c0-120">此元素的 XML 結構為：</span><span class="sxs-lookup"><span data-stu-id="4f2c0-120">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:JobOutputOptimization">
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

## <a name="structure-variables"></a><span data-ttu-id="4f2c0-121">結構變數</span><span class="sxs-lookup"><span data-stu-id="4f2c0-121">Structure Variables</span></span>

<span data-ttu-id="4f2c0-122">下表概述 XML 結構中所定義之變數的特性。</span><span class="sxs-lookup"><span data-stu-id="4f2c0-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="4f2c0-123">Name</span><span class="sxs-lookup"><span data-stu-id="4f2c0-123">Name</span></span>                               | <span data-ttu-id="4f2c0-124">資料類型</span><span class="sxs-lookup"><span data-stu-id="4f2c0-124">Data type</span></span>         | <span data-ttu-id="4f2c0-125">單位</span><span class="sxs-lookup"><span data-stu-id="4f2c0-125">Unit</span></span>                  | <span data-ttu-id="4f2c0-126">支援的值</span><span class="sxs-lookup"><span data-stu-id="4f2c0-126">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="4f2c0-127">總結</span><span class="sxs-lookup"><span data-stu-id="4f2c0-127">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="4f2c0-128">\_選項名稱\_</span><span class="sxs-lookup"><span data-stu-id="4f2c0-128">\_OptionName\_</span></span><br/>          | <span data-ttu-id="4f2c0-129">string</span><span class="sxs-lookup"><span data-stu-id="4f2c0-129">string</span></span><br/> | <span data-ttu-id="4f2c0-130">字元</span><span class="sxs-lookup"><span data-stu-id="4f2c0-130">characters</span></span><br/> | <span data-ttu-id="4f2c0-131">以 [XML 命名空間](https://www.w3.org/TR/1999/REC-xml-names-19990114/)所定義的有效完整名稱。</span><span class="sxs-lookup"><span data-stu-id="4f2c0-131">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="4f2c0-132">如果未指定命名空間，則會假設為預設命名空間。</span><span class="sxs-lookup"><span data-stu-id="4f2c0-132">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="4f2c0-133">選項的名稱。</span><span class="sxs-lookup"><span data-stu-id="4f2c0-133">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="4f2c0-134">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="4f2c0-134">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="4f2c0-135">string</span><span class="sxs-lookup"><span data-stu-id="4f2c0-135">string</span></span><br/> | <span data-ttu-id="4f2c0-136">n/a</span><span class="sxs-lookup"><span data-stu-id="4f2c0-136">n/a</span></span><br/>        | <span data-ttu-id="4f2c0-137">True、False。</span><span class="sxs-lookup"><span data-stu-id="4f2c0-137">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="4f2c0-138">定義選項，當選取此選項時，會停用此功能。</span><span class="sxs-lookup"><span data-stu-id="4f2c0-138">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="4f2c0-139">可延伸標記語言 (XML)  (XML) 內容</span><span class="sxs-lookup"><span data-stu-id="4f2c0-139">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="4f2c0-140">公用列印架構關鍵字是在 https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords 命名空間中定義。</span><span class="sxs-lookup"><span data-stu-id="4f2c0-140">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="4f2c0-141">此關鍵字的 public 可延伸標記語言 (XML)  (XML) 內容定義如下：</span><span class="sxs-lookup"><span data-stu-id="4f2c0-141">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:JobOutputOptimization">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!-- Specifies the job processing be optimized for archive output. -->
  <psf:Option name="psk:ArchiveFormat" />
  <!-- Specifies the job processing be optimized for portability (cross-device) of output. -->
  <psf:Option name="psk:OptimizeForPortability" />
  <!-- Specifies the job processing be optimized for quality of output. -->
  <psf:Option name="psk:OptimizeForQuality" />
  <!-- Specifies the job processing be optimized for speed of output. -->
  <psf:Option name="psk:OptimizeForSpeed" />
  <!-- Specifies the job processing should not be optimized for a particular scenario. -->
  <psf:Option name="psk:None" />
</psf:Feature>
    
```

## <a name="related-topics"></a><span data-ttu-id="4f2c0-142">相關主題</span><span class="sxs-lookup"><span data-stu-id="4f2c0-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4f2c0-143">列印架構規格</span><span class="sxs-lookup"><span data-stu-id="4f2c0-143">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




