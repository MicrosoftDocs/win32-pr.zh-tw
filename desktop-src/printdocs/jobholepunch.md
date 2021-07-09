---
description: 取得 JobHolePunch 使用者可設定元素的相關資訊。 本主題並非最新的。 如需最新資訊，請參閱列印架構規格。
ms.assetid: 26e9e7d6-7c01-4687-aa64-7aea867b4e58
title: JobHolePunch
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c82a36784ab6a1fb5eb0c8d682c45cce574ee9e
ms.sourcegitcommit: 998d50f6def8a25850fc113fc8a2df903c829c5e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/09/2021
ms.locfileid: "113549356"
---
# <a name="jobholepunch"></a><span data-ttu-id="221fc-105">JobHolePunch</span><span class="sxs-lookup"><span data-stu-id="221fc-105">JobHolePunch</span></span>

<span data-ttu-id="221fc-106">本主題並非最新的。</span><span class="sxs-lookup"><span data-stu-id="221fc-106">This topic is not current.</span></span> <span data-ttu-id="221fc-107">如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。</span><span class="sxs-lookup"><span data-stu-id="221fc-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="221fc-108">描述輸出的打孔特性。</span><span class="sxs-lookup"><span data-stu-id="221fc-108">Describes the hole punching characteristics of the output.</span></span> <span data-ttu-id="221fc-109">所有檔都會一起打孔。</span><span class="sxs-lookup"><span data-stu-id="221fc-109">All documents are punched together.</span></span> <span data-ttu-id="221fc-110">JobHolePunch 和 DocumentHolePunch 關鍵字是互斥的。</span><span class="sxs-lookup"><span data-stu-id="221fc-110">The JobHolePunch and DocumentHolePunch keywords are mutually exclusive.</span></span> <span data-ttu-id="221fc-111">這兩者不能同時在 PrintTicket 或列印功能檔中指定。</span><span class="sxs-lookup"><span data-stu-id="221fc-111">Both should not be specified simultaneously in a PrintTicket or Print Capabilities document.</span></span>

-   [<span data-ttu-id="221fc-112">項目資訊</span><span class="sxs-lookup"><span data-stu-id="221fc-112">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="221fc-113">結構化內容</span><span class="sxs-lookup"><span data-stu-id="221fc-113">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="221fc-114">可延伸標記語言 (XML)  (XML) 內容</span><span class="sxs-lookup"><span data-stu-id="221fc-114">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="221fc-115">項目資訊</span><span class="sxs-lookup"><span data-stu-id="221fc-115">Element Information</span></span>



| <span data-ttu-id="221fc-116">Name</span><span class="sxs-lookup"><span data-stu-id="221fc-116">Name</span></span> | <span data-ttu-id="221fc-117">值</span><span class="sxs-lookup"><span data-stu-id="221fc-117">Value</span></span> |
|----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="221fc-118">項目類型</span><span class="sxs-lookup"><span data-stu-id="221fc-118">Element Type</span></span> <br/>   | <span data-ttu-id="221fc-119">功能</span><span class="sxs-lookup"><span data-stu-id="221fc-119">Feature</span></span><br/>                                                                                                                              |
| <span data-ttu-id="221fc-120">範圍前置詞</span><span class="sxs-lookup"><span data-stu-id="221fc-120">Scoping Prefix</span></span> <br/> | <span data-ttu-id="221fc-121">工作 (Job)</span><span class="sxs-lookup"><span data-stu-id="221fc-121">Job</span></span><br/>                                                                                                                                  |
| <span data-ttu-id="221fc-122">備註</span><span class="sxs-lookup"><span data-stu-id="221fc-122">Notes</span></span> <br/>          | <span data-ttu-id="221fc-123">頂端、底部、左方和右邊都是相對於 PageImageableSize，其中下拉式功能表是以 X 軸和 y 軸的原點表示。</span><span class="sxs-lookup"><span data-stu-id="221fc-123">Top, Bottom, Left, and Right are relative to the PageImageableSize, where TopLeft is denoted by the origin of the x-axis and y-axis.</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="221fc-124">結構化內容</span><span class="sxs-lookup"><span data-stu-id="221fc-124">Structural Content</span></span>

<span data-ttu-id="221fc-125">此元素的 XML 結構為：</span><span class="sxs-lookup"><span data-stu-id="221fc-125">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:JobHolePunch">
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

## <a name="structure-variables"></a><span data-ttu-id="221fc-126">結構變數</span><span class="sxs-lookup"><span data-stu-id="221fc-126">Structure Variables</span></span>

<span data-ttu-id="221fc-127">下表概述 XML 結構中所定義之變數的特性。</span><span class="sxs-lookup"><span data-stu-id="221fc-127">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="221fc-128">Name</span><span class="sxs-lookup"><span data-stu-id="221fc-128">Name</span></span>                               | <span data-ttu-id="221fc-129">資料類型</span><span class="sxs-lookup"><span data-stu-id="221fc-129">Data type</span></span>         | <span data-ttu-id="221fc-130">單位</span><span class="sxs-lookup"><span data-stu-id="221fc-130">Unit</span></span>                  | <span data-ttu-id="221fc-131">支援的值</span><span class="sxs-lookup"><span data-stu-id="221fc-131">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="221fc-132">摘要</span><span class="sxs-lookup"><span data-stu-id="221fc-132">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="221fc-133">\_選項名稱\_</span><span class="sxs-lookup"><span data-stu-id="221fc-133">\_OptionName\_</span></span><br/>          | <span data-ttu-id="221fc-134">string</span><span class="sxs-lookup"><span data-stu-id="221fc-134">string</span></span><br/> | <span data-ttu-id="221fc-135">字元</span><span class="sxs-lookup"><span data-stu-id="221fc-135">characters</span></span><br/> | <span data-ttu-id="221fc-136">以 [XML 命名空間](https://www.w3.org/TR/1999/REC-xml-names-19990114/)所定義的有效完整名稱。</span><span class="sxs-lookup"><span data-stu-id="221fc-136">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="221fc-137">如果未指定命名空間，則會假設為預設命名空間。</span><span class="sxs-lookup"><span data-stu-id="221fc-137">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="221fc-138">選項的名稱。</span><span class="sxs-lookup"><span data-stu-id="221fc-138">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="221fc-139">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="221fc-139">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="221fc-140">string</span><span class="sxs-lookup"><span data-stu-id="221fc-140">string</span></span><br/> | <span data-ttu-id="221fc-141">n/a</span><span class="sxs-lookup"><span data-stu-id="221fc-141">n/a</span></span><br/>        | <span data-ttu-id="221fc-142">True、False。</span><span class="sxs-lookup"><span data-stu-id="221fc-142">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="221fc-143">定義選項，當選取此選項時，會停用此功能。</span><span class="sxs-lookup"><span data-stu-id="221fc-143">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="221fc-144">可延伸標記語言 (XML)  (XML) 內容</span><span class="sxs-lookup"><span data-stu-id="221fc-144">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="221fc-145">公用列印架構關鍵字是在 https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords 命名空間中定義。</span><span class="sxs-lookup"><span data-stu-id="221fc-145">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="221fc-146">此關鍵字的 public 可延伸標記語言 (XML)  (XML) 內容定義如下：</span><span class="sxs-lookup"><span data-stu-id="221fc-146">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:JobHolePunch">
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

## <a name="related-topics"></a><span data-ttu-id="221fc-147">相關主題</span><span class="sxs-lookup"><span data-stu-id="221fc-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="221fc-148">列印架構規格</span><span class="sxs-lookup"><span data-stu-id="221fc-148">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




