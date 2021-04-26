---
description: 本主題並非最新的。 如需最新資訊，請參閱列印架構規格。
ms.assetid: 73840548-f68b-4af8-acb4-6f7faa2e8879
title: DocumentOutputBin
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96f6d16ca000e76b01cd2c3165054d7acc81351b
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/26/2021
ms.locfileid: "107997135"
---
# <a name="documentoutputbin"></a><span data-ttu-id="45db8-104">DocumentOutputBin</span><span class="sxs-lookup"><span data-stu-id="45db8-104">DocumentOutputBin</span></span>

<span data-ttu-id="45db8-105">本主題並非最新的。</span><span class="sxs-lookup"><span data-stu-id="45db8-105">This topic is not current.</span></span> <span data-ttu-id="45db8-106">如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。</span><span class="sxs-lookup"><span data-stu-id="45db8-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="45db8-107">描述裝置支援的 bin 完整清單。</span><span class="sxs-lookup"><span data-stu-id="45db8-107">Describes the full list of supported bins for the device.</span></span> <span data-ttu-id="45db8-108">允許以每個檔為基礎來指定輸出 bin。</span><span class="sxs-lookup"><span data-stu-id="45db8-108">Allows specification of output bin on a per document basis.</span></span> <span data-ttu-id="45db8-109">JobOutputBin、DocumentOutputBin 和 PageOutputBin 關鍵字都是互斥或列印功能檔中的唯一一項指定。</span><span class="sxs-lookup"><span data-stu-id="45db8-109">The JobOutputBin, DocumentOutputBin and PageOutputBin keywords are mutually exclusive only one should be specified in a PrintTicket or Print Capabilities document.</span></span>

-   [<span data-ttu-id="45db8-110">項目資訊</span><span class="sxs-lookup"><span data-stu-id="45db8-110">Element Information</span></span>](#element-information)

-   [<span data-ttu-id="45db8-111">結構化內容</span><span class="sxs-lookup"><span data-stu-id="45db8-111">Structural Content</span></span>](#structural-content)

-   [<span data-ttu-id="45db8-112">XML 內容</span><span class="sxs-lookup"><span data-stu-id="45db8-112">XML Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="45db8-113">項目資訊</span><span class="sxs-lookup"><span data-stu-id="45db8-113">Element Information</span></span>



| <span data-ttu-id="45db8-114">Name</span><span class="sxs-lookup"><span data-stu-id="45db8-114">Name</span></span> | <span data-ttu-id="45db8-115">值</span><span class="sxs-lookup"><span data-stu-id="45db8-115">Value</span></span> |
|----------------------------|---------------------|
| <span data-ttu-id="45db8-116">項目類型</span><span class="sxs-lookup"><span data-stu-id="45db8-116">Element Type</span></span> <br/>   | <span data-ttu-id="45db8-117">功能</span><span class="sxs-lookup"><span data-stu-id="45db8-117">Feature</span></span><br/>  |
| <span data-ttu-id="45db8-118">範圍前置詞</span><span class="sxs-lookup"><span data-stu-id="45db8-118">Scoping Prefix</span></span> <br/> | <span data-ttu-id="45db8-119">文件</span><span class="sxs-lookup"><span data-stu-id="45db8-119">Document</span></span><br/> |
| <span data-ttu-id="45db8-120">注意</span><span class="sxs-lookup"><span data-stu-id="45db8-120">Notes</span></span> <br/>          | <span data-ttu-id="45db8-121">None</span><span class="sxs-lookup"><span data-stu-id="45db8-121">None</span></span><br/>     |



 

## <a name="structural-content"></a><span data-ttu-id="45db8-122">結構化內容</span><span class="sxs-lookup"><span data-stu-id="45db8-122">Structural Content</span></span>

<span data-ttu-id="45db8-123">此元素的 XML 結構為：</span><span class="sxs-lookup"><span data-stu-id="45db8-123">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="45db8-124">結構變數</span><span class="sxs-lookup"><span data-stu-id="45db8-124">Structure Variables</span></span>

<span data-ttu-id="45db8-125">下表概述 XML 結構中所定義之變數的特性。</span><span class="sxs-lookup"><span data-stu-id="45db8-125">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="45db8-126">Name</span><span class="sxs-lookup"><span data-stu-id="45db8-126">Name</span></span>                                   | <span data-ttu-id="45db8-127">資料類型</span><span class="sxs-lookup"><span data-stu-id="45db8-127">Data type</span></span>          | <span data-ttu-id="45db8-128">單位</span><span class="sxs-lookup"><span data-stu-id="45db8-128">Unit</span></span>                  | <span data-ttu-id="45db8-129">支援的值</span><span class="sxs-lookup"><span data-stu-id="45db8-129">Supported values</span></span>                                                                                                                                                             | <span data-ttu-id="45db8-130">總結</span><span class="sxs-lookup"><span data-stu-id="45db8-130">Summary</span></span>                                                                             |
|----------------------------------------|--------------------|-----------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="45db8-131">\_選項名稱\_</span><span class="sxs-lookup"><span data-stu-id="45db8-131">\_OptionName\_</span></span><br/>              | <span data-ttu-id="45db8-132">字串</span><span class="sxs-lookup"><span data-stu-id="45db8-132">string</span></span><br/>  | <span data-ttu-id="45db8-133">字元</span><span class="sxs-lookup"><span data-stu-id="45db8-133">characters</span></span><br/> | <span data-ttu-id="45db8-134">由定義的有效完整名稱 https://www.w3.org/TR/1999/REC-xml-names-19990114/\#dt-qname 。</span><span class="sxs-lookup"><span data-stu-id="45db8-134">Valid fully qualified name as defined by https://www.w3.org/TR/1999/REC-xml-names-19990114/\#dt-qname.</span></span> <span data-ttu-id="45db8-135">如果未指定命名空間，則會假設為預設命名空間。</span><span class="sxs-lookup"><span data-stu-id="45db8-135">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="45db8-136">選項的名稱。</span><span class="sxs-lookup"><span data-stu-id="45db8-136">The name of the option.</span></span><br/>                                                  |
| <span data-ttu-id="45db8-137">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="45db8-137">\_IdentityOptionValue\_</span></span><br/>     | <span data-ttu-id="45db8-138">字串</span><span class="sxs-lookup"><span data-stu-id="45db8-138">string</span></span><br/>  | <span data-ttu-id="45db8-139">n/a</span><span class="sxs-lookup"><span data-stu-id="45db8-139">n/a</span></span><br/>        | <span data-ttu-id="45db8-140">True、False。</span><span class="sxs-lookup"><span data-stu-id="45db8-140">True, False.</span></span><br/>                                                                                                                                                      | <span data-ttu-id="45db8-141">定義選項，當選取此選項時，會停用此功能。</span><span class="sxs-lookup"><span data-stu-id="45db8-141">Defines an Option which when selected would disable this feature.</span></span><br/>        |
| <span data-ttu-id="45db8-142">\_BinTypeValue\_</span><span class="sxs-lookup"><span data-stu-id="45db8-142">\_BinTypeValue\_</span></span><br/>            | <span data-ttu-id="45db8-143">字串</span><span class="sxs-lookup"><span data-stu-id="45db8-143">string</span></span><br/>  | <span data-ttu-id="45db8-144">n/a</span><span class="sxs-lookup"><span data-stu-id="45db8-144">n/a</span></span><br/>        | <span data-ttu-id="45db8-145">信箱、排序器、堆疊器、分頁裝訂器、無。</span><span class="sxs-lookup"><span data-stu-id="45db8-145">MailBox, Sorter, Stacker, Finisher, None.</span></span><br/>                                                                                                                         | <span data-ttu-id="45db8-146">指定 bin 的一般類型。</span><span class="sxs-lookup"><span data-stu-id="45db8-146">Specifies the general type of the bin.</span></span><br/>                                   |
| <span data-ttu-id="45db8-147">\_MediaSheetCapacityValue\_</span><span class="sxs-lookup"><span data-stu-id="45db8-147">\_MediaSheetCapacityValue\_</span></span><br/> | <span data-ttu-id="45db8-148">整數</span><span class="sxs-lookup"><span data-stu-id="45db8-148">integer</span></span><br/> | <span data-ttu-id="45db8-149">床單</span><span class="sxs-lookup"><span data-stu-id="45db8-149">sheets</span></span><br/>     | <span data-ttu-id="45db8-150">大於 0。</span><span class="sxs-lookup"><span data-stu-id="45db8-150">Greater than 0.</span></span><br/>                                                                                                                                                   | <span data-ttu-id="45db8-151">以 (完整層級) 的頁面數目指定媒體容量。</span><span class="sxs-lookup"><span data-stu-id="45db8-151">Specifies the Media capacity in number of pages (full level) of the bin.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="45db8-152">可延伸標記語言 (XML)  (XML) 內容</span><span class="sxs-lookup"><span data-stu-id="45db8-152">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="45db8-153">公用列印架構關鍵字是在 https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords 命名空間中定義。</span><span class="sxs-lookup"><span data-stu-id="45db8-153">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="45db8-154">此關鍵字的 public 可延伸標記語言 (XML)  (XML) 內容定義如下：</span><span class="sxs-lookup"><span data-stu-id="45db8-154">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="45db8-155">相關主題</span><span class="sxs-lookup"><span data-stu-id="45db8-155">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="45db8-156">列印架構規格</span><span class="sxs-lookup"><span data-stu-id="45db8-156">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




