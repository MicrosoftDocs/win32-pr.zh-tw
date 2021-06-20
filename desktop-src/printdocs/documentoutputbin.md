---
description: 深入瞭解 DocumentOutputBin，它會說明裝置支援的 bin 完整清單，並可讓您以每個檔為基礎來指定輸出 bin。
ms.assetid: 73840548-f68b-4af8-acb4-6f7faa2e8879
title: DocumentOutputBin
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2afc20f15aed8d3076afb79d755c54791573b393
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/19/2021
ms.locfileid: "112409241"
---
# <a name="documentoutputbin"></a><span data-ttu-id="3c755-103">DocumentOutputBin</span><span class="sxs-lookup"><span data-stu-id="3c755-103">DocumentOutputBin</span></span>

<span data-ttu-id="3c755-104">本主題並非最新的。</span><span class="sxs-lookup"><span data-stu-id="3c755-104">This topic is not current.</span></span> <span data-ttu-id="3c755-105">如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。</span><span class="sxs-lookup"><span data-stu-id="3c755-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="3c755-106">描述裝置支援的 bin 完整清單。</span><span class="sxs-lookup"><span data-stu-id="3c755-106">Describes the full list of supported bins for the device.</span></span> <span data-ttu-id="3c755-107">允許以每個檔為基礎來指定輸出 bin。</span><span class="sxs-lookup"><span data-stu-id="3c755-107">Allows specification of output bin on a per document basis.</span></span> <span data-ttu-id="3c755-108">JobOutputBin、DocumentOutputBin 和 PageOutputBin 關鍵字都是互斥或列印功能檔中的唯一一項指定。</span><span class="sxs-lookup"><span data-stu-id="3c755-108">The JobOutputBin, DocumentOutputBin and PageOutputBin keywords are mutually exclusive only one should be specified in a PrintTicket or Print Capabilities document.</span></span>

-   [<span data-ttu-id="3c755-109">項目資訊</span><span class="sxs-lookup"><span data-stu-id="3c755-109">Element Information</span></span>](#element-information)

-   [<span data-ttu-id="3c755-110">結構化內容</span><span class="sxs-lookup"><span data-stu-id="3c755-110">Structural Content</span></span>](#structural-content)

-   [<span data-ttu-id="3c755-111">XML 內容</span><span class="sxs-lookup"><span data-stu-id="3c755-111">XML Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="3c755-112">項目資訊</span><span class="sxs-lookup"><span data-stu-id="3c755-112">Element Information</span></span>



| <span data-ttu-id="3c755-113">Name</span><span class="sxs-lookup"><span data-stu-id="3c755-113">Name</span></span> | <span data-ttu-id="3c755-114">值</span><span class="sxs-lookup"><span data-stu-id="3c755-114">Value</span></span> |
|----------------------------|---------------------|
| <span data-ttu-id="3c755-115">項目類型</span><span class="sxs-lookup"><span data-stu-id="3c755-115">Element Type</span></span> <br/>   | <span data-ttu-id="3c755-116">功能</span><span class="sxs-lookup"><span data-stu-id="3c755-116">Feature</span></span><br/>  |
| <span data-ttu-id="3c755-117">範圍前置詞</span><span class="sxs-lookup"><span data-stu-id="3c755-117">Scoping Prefix</span></span> <br/> | <span data-ttu-id="3c755-118">文件</span><span class="sxs-lookup"><span data-stu-id="3c755-118">Document</span></span><br/> |
| <span data-ttu-id="3c755-119">注意</span><span class="sxs-lookup"><span data-stu-id="3c755-119">Notes</span></span> <br/>          | <span data-ttu-id="3c755-120">None</span><span class="sxs-lookup"><span data-stu-id="3c755-120">None</span></span><br/>     |



 

## <a name="structural-content"></a><span data-ttu-id="3c755-121">結構化內容</span><span class="sxs-lookup"><span data-stu-id="3c755-121">Structural Content</span></span>

<span data-ttu-id="3c755-122">此元素的 XML 結構為：</span><span class="sxs-lookup"><span data-stu-id="3c755-122">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:DocumentOutputBin">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option name="psk:_OptionName_">
    <psf:Property name="psf:IdentityOption">
      <psf:Value xsi:type="xs:string">_IdentityOptionValue_</psf:Value>
    </psf:Property>
    <psf:ScoredProperty name="psk:BinType">
      <psf:Value xsi:type="xs:string">_BinTypeValue_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSheetCapacity">
      <psf:Value xsi:type="xs:integer">_MediaSheetCapacityValue_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature>
      
```

## <a name="structure-variables"></a><span data-ttu-id="3c755-123">結構變數</span><span class="sxs-lookup"><span data-stu-id="3c755-123">Structure Variables</span></span>

<span data-ttu-id="3c755-124">下表概述 XML 結構中所定義之變數的特性。</span><span class="sxs-lookup"><span data-stu-id="3c755-124">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="3c755-125">Name</span><span class="sxs-lookup"><span data-stu-id="3c755-125">Name</span></span>                                   | <span data-ttu-id="3c755-126">資料類型</span><span class="sxs-lookup"><span data-stu-id="3c755-126">Data type</span></span>          | <span data-ttu-id="3c755-127">單位</span><span class="sxs-lookup"><span data-stu-id="3c755-127">Unit</span></span>                  | <span data-ttu-id="3c755-128">支援的值</span><span class="sxs-lookup"><span data-stu-id="3c755-128">Supported values</span></span>                                                                                                                                                             | <span data-ttu-id="3c755-129">總結</span><span class="sxs-lookup"><span data-stu-id="3c755-129">Summary</span></span>                                                                             |
|----------------------------------------|--------------------|-----------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="3c755-130">\_選項名稱\_</span><span class="sxs-lookup"><span data-stu-id="3c755-130">\_OptionName\_</span></span><br/>              | <span data-ttu-id="3c755-131">string</span><span class="sxs-lookup"><span data-stu-id="3c755-131">string</span></span><br/>  | <span data-ttu-id="3c755-132">字元</span><span class="sxs-lookup"><span data-stu-id="3c755-132">characters</span></span><br/> | <span data-ttu-id="3c755-133">由定義的有效完整名稱 https://www.w3.org/TR/1999/REC-xml-names-19990114/\#dt-qname 。</span><span class="sxs-lookup"><span data-stu-id="3c755-133">Valid fully qualified name as defined by https://www.w3.org/TR/1999/REC-xml-names-19990114/\#dt-qname.</span></span> <span data-ttu-id="3c755-134">如果未指定命名空間，則會假設為預設命名空間。</span><span class="sxs-lookup"><span data-stu-id="3c755-134">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="3c755-135">選項的名稱。</span><span class="sxs-lookup"><span data-stu-id="3c755-135">The name of the option.</span></span><br/>                                                  |
| <span data-ttu-id="3c755-136">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="3c755-136">\_IdentityOptionValue\_</span></span><br/>     | <span data-ttu-id="3c755-137">string</span><span class="sxs-lookup"><span data-stu-id="3c755-137">string</span></span><br/>  | <span data-ttu-id="3c755-138">n/a</span><span class="sxs-lookup"><span data-stu-id="3c755-138">n/a</span></span><br/>        | <span data-ttu-id="3c755-139">True、False。</span><span class="sxs-lookup"><span data-stu-id="3c755-139">True, False.</span></span><br/>                                                                                                                                                      | <span data-ttu-id="3c755-140">定義選項，當選取此選項時，會停用此功能。</span><span class="sxs-lookup"><span data-stu-id="3c755-140">Defines an Option which when selected would disable this feature.</span></span><br/>        |
| <span data-ttu-id="3c755-141">\_BinTypeValue\_</span><span class="sxs-lookup"><span data-stu-id="3c755-141">\_BinTypeValue\_</span></span><br/>            | <span data-ttu-id="3c755-142">string</span><span class="sxs-lookup"><span data-stu-id="3c755-142">string</span></span><br/>  | <span data-ttu-id="3c755-143">n/a</span><span class="sxs-lookup"><span data-stu-id="3c755-143">n/a</span></span><br/>        | <span data-ttu-id="3c755-144">信箱、排序器、堆疊器、分頁裝訂器、無。</span><span class="sxs-lookup"><span data-stu-id="3c755-144">MailBox, Sorter, Stacker, Finisher, None.</span></span><br/>                                                                                                                         | <span data-ttu-id="3c755-145">指定 bin 的一般類型。</span><span class="sxs-lookup"><span data-stu-id="3c755-145">Specifies the general type of the bin.</span></span><br/>                                   |
| <span data-ttu-id="3c755-146">\_MediaSheetCapacityValue\_</span><span class="sxs-lookup"><span data-stu-id="3c755-146">\_MediaSheetCapacityValue\_</span></span><br/> | <span data-ttu-id="3c755-147">整數</span><span class="sxs-lookup"><span data-stu-id="3c755-147">integer</span></span><br/> | <span data-ttu-id="3c755-148">床單</span><span class="sxs-lookup"><span data-stu-id="3c755-148">sheets</span></span><br/>     | <span data-ttu-id="3c755-149">大於 0。</span><span class="sxs-lookup"><span data-stu-id="3c755-149">Greater than 0.</span></span><br/>                                                                                                                                                   | <span data-ttu-id="3c755-150">以 (完整層級) 的頁面數目指定媒體容量。</span><span class="sxs-lookup"><span data-stu-id="3c755-150">Specifies the Media capacity in number of pages (full level) of the bin.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="3c755-151">可延伸標記語言 (XML)  (XML) 內容</span><span class="sxs-lookup"><span data-stu-id="3c755-151">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="3c755-152">公用列印架構關鍵字是在 https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords 命名空間中定義。</span><span class="sxs-lookup"><span data-stu-id="3c755-152">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="3c755-153">此關鍵字的 public 可延伸標記語言 (XML)  (XML) 內容定義如下：</span><span class="sxs-lookup"><span data-stu-id="3c755-153">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:DocumentOutputBin">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option>
    <!--Specifies type of output bin-->
    <psf:ScoredProperty name="psk:BinType">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <!--Specifies media capacity for output bin-->
    <psf:ScoredProperty name="psk:MediaSheetCapacity">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature>    
```

## <a name="related-topics"></a><span data-ttu-id="3c755-154">相關主題</span><span class="sxs-lookup"><span data-stu-id="3c755-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3c755-155">列印架構規格</span><span class="sxs-lookup"><span data-stu-id="3c755-155">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




