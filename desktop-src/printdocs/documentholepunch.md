---
description: 瞭解 DocumentHolePunch 元素，其描述輸出的打孔特性。
ms.assetid: 46fd5e22-a2f3-424d-8c2f-2d5ac089a230
title: DocumentHolePunch
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 760559d3bb155030ff72a616096e5a860ba0d6b0
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/19/2021
ms.locfileid: "112409290"
---
# <a name="documentholepunch"></a><span data-ttu-id="6728b-103">DocumentHolePunch</span><span class="sxs-lookup"><span data-stu-id="6728b-103">DocumentHolePunch</span></span>

<span data-ttu-id="6728b-104">本主題並非最新的。</span><span class="sxs-lookup"><span data-stu-id="6728b-104">This topic is not current.</span></span> <span data-ttu-id="6728b-105">如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。</span><span class="sxs-lookup"><span data-stu-id="6728b-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="6728b-106">描述輸出的打孔特性。</span><span class="sxs-lookup"><span data-stu-id="6728b-106">Describes the hole punching characteristics of the output.</span></span> <span data-ttu-id="6728b-107">每份檔都是分開的。</span><span class="sxs-lookup"><span data-stu-id="6728b-107">Each document is punched separately.</span></span> <span data-ttu-id="6728b-108">JobHolePunch 和 DocumentHolePunch 關鍵字是互斥的。</span><span class="sxs-lookup"><span data-stu-id="6728b-108">The JobHolePunch and DocumentHolePunch keywords are mutually exclusive.</span></span> <span data-ttu-id="6728b-109">這兩者不能同時在 PrintTicket 或列印功能檔中指定。</span><span class="sxs-lookup"><span data-stu-id="6728b-109">Both should not be specified simultaneously in a PrintTicket or Print Capabilities document.</span></span>

-   [<span data-ttu-id="6728b-110">項目資訊</span><span class="sxs-lookup"><span data-stu-id="6728b-110">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="6728b-111">結構化內容</span><span class="sxs-lookup"><span data-stu-id="6728b-111">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="6728b-112">可延伸標記語言 (XML)  (XML) 內容</span><span class="sxs-lookup"><span data-stu-id="6728b-112">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="6728b-113">項目資訊</span><span class="sxs-lookup"><span data-stu-id="6728b-113">Element Information</span></span>



| <span data-ttu-id="6728b-114">Name</span><span class="sxs-lookup"><span data-stu-id="6728b-114">Name</span></span> | <span data-ttu-id="6728b-115">值</span><span class="sxs-lookup"><span data-stu-id="6728b-115">Value</span></span> |
|----------------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="6728b-116">項目類型</span><span class="sxs-lookup"><span data-stu-id="6728b-116">Element Type</span></span> <br/>   | <span data-ttu-id="6728b-117">功能</span><span class="sxs-lookup"><span data-stu-id="6728b-117">Feature</span></span><br/>                                                             |
| <span data-ttu-id="6728b-118">範圍前置詞</span><span class="sxs-lookup"><span data-stu-id="6728b-118">Scoping Prefix</span></span> <br/> | <span data-ttu-id="6728b-119">文件</span><span class="sxs-lookup"><span data-stu-id="6728b-119">Document</span></span><br/>                                                            |
| <span data-ttu-id="6728b-120">備註</span><span class="sxs-lookup"><span data-stu-id="6728b-120">Notes</span></span> <br/>          | <span data-ttu-id="6728b-121">頂端、底部、左方和右邊都是相對於 PageImageableSize。</span><span class="sxs-lookup"><span data-stu-id="6728b-121">Top, Bottom, Left, and Right are relative to the PageImageableSize.</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="6728b-122">結構化內容</span><span class="sxs-lookup"><span data-stu-id="6728b-122">Structural Content</span></span>

<span data-ttu-id="6728b-123">此元素的 XML 結構為：</span><span class="sxs-lookup"><span data-stu-id="6728b-123">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:DocumentHolePunch">
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

## <a name="structure-variables"></a><span data-ttu-id="6728b-124">結構變數</span><span class="sxs-lookup"><span data-stu-id="6728b-124">Structure Variables</span></span>

<span data-ttu-id="6728b-125">下表概述 XML 結構中所定義之變數的特性。</span><span class="sxs-lookup"><span data-stu-id="6728b-125">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="6728b-126">Name</span><span class="sxs-lookup"><span data-stu-id="6728b-126">Name</span></span>                               | <span data-ttu-id="6728b-127">資料類型</span><span class="sxs-lookup"><span data-stu-id="6728b-127">Data type</span></span>         | <span data-ttu-id="6728b-128">單位</span><span class="sxs-lookup"><span data-stu-id="6728b-128">Unit</span></span>                  | <span data-ttu-id="6728b-129">支援的值</span><span class="sxs-lookup"><span data-stu-id="6728b-129">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="6728b-130">總結</span><span class="sxs-lookup"><span data-stu-id="6728b-130">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="6728b-131">\_選項名稱\_</span><span class="sxs-lookup"><span data-stu-id="6728b-131">\_OptionName\_</span></span><br/>          | <span data-ttu-id="6728b-132">string</span><span class="sxs-lookup"><span data-stu-id="6728b-132">string</span></span><br/> | <span data-ttu-id="6728b-133">字元</span><span class="sxs-lookup"><span data-stu-id="6728b-133">characters</span></span><br/> | <span data-ttu-id="6728b-134">以 [XML 命名空間](https://www.w3.org/TR/1999/REC-xml-names-19990114/)所定義的有效完整名稱。</span><span class="sxs-lookup"><span data-stu-id="6728b-134">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="6728b-135">如果未指定命名空間，則會假設為預設命名空間。</span><span class="sxs-lookup"><span data-stu-id="6728b-135">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="6728b-136">選項的名稱。</span><span class="sxs-lookup"><span data-stu-id="6728b-136">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="6728b-137">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="6728b-137">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="6728b-138">string</span><span class="sxs-lookup"><span data-stu-id="6728b-138">string</span></span><br/> | <span data-ttu-id="6728b-139">n/a</span><span class="sxs-lookup"><span data-stu-id="6728b-139">n/a</span></span><br/>        | <span data-ttu-id="6728b-140">True、False。</span><span class="sxs-lookup"><span data-stu-id="6728b-140">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="6728b-141">定義選項，當選取此選項時，會停用此功能。</span><span class="sxs-lookup"><span data-stu-id="6728b-141">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="6728b-142">可延伸標記語言 (XML)  (XML) 內容</span><span class="sxs-lookup"><span data-stu-id="6728b-142">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="6728b-143">公用列印架構關鍵字是在 https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords 命名空間中定義。</span><span class="sxs-lookup"><span data-stu-id="6728b-143">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="6728b-144">此關鍵字的 public 可延伸標記語言 (XML)  (XML) 內容定義如下：</span><span class="sxs-lookup"><span data-stu-id="6728b-144">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:DocumentHolePunch">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!-- Specifies hole(s) along the bottom edge. -->
  <psf:Option name="psk:BottomEdge" />
  <!-- Specifies hole(s) along the left edge. -->
  <psf:Option name="psk:LeftEdge" />
  <!-- Specifies no hole punching. -->
  <psf:Option name="psk:None" />
  <!-- Specifies hole(s) along the right edge. -->
  <psf:Option name="psk:RightEdge" />
  <!-- Specifies hole(s) along the top edge. -->
  <psf:Option name="psk:TopEdge" />
</psf:Feature>    
```

## <a name="related-topics"></a><span data-ttu-id="6728b-145">相關主題</span><span class="sxs-lookup"><span data-stu-id="6728b-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6728b-146">列印架構規格</span><span class="sxs-lookup"><span data-stu-id="6728b-146">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




