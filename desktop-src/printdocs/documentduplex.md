---
description: 本主題並非最新的。 如需最新資訊，請參閱列印架構規格。
ms.assetid: dadc52e8-1733-4267-85aa-33d0ddd3dfa2
title: DocumentDuplex
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb2d65ac1007b8413f9e5e6cc12802e0ac27dac3
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/06/2021
ms.locfileid: "104195847"
---
# <a name="documentduplex"></a><span data-ttu-id="ad32f-104">DocumentDuplex</span><span class="sxs-lookup"><span data-stu-id="ad32f-104">DocumentDuplex</span></span>

<span data-ttu-id="ad32f-105">本主題並非最新的。</span><span class="sxs-lookup"><span data-stu-id="ad32f-105">This topic is not current.</span></span> <span data-ttu-id="ad32f-106">如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。</span><span class="sxs-lookup"><span data-stu-id="ad32f-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="ad32f-107">描述輸出的雙工特性。</span><span class="sxs-lookup"><span data-stu-id="ad32f-107">Describes the duplex characteristics of the output.</span></span> <span data-ttu-id="ad32f-108">雙工功能可在媒體的兩端進行列印。</span><span class="sxs-lookup"><span data-stu-id="ad32f-108">The duplex feature allows for printing on both sides of the media.</span></span> <span data-ttu-id="ad32f-109">每份檔都是分開 duplexed。</span><span class="sxs-lookup"><span data-stu-id="ad32f-109">Each document is duplexed separately.</span></span> <span data-ttu-id="ad32f-110">DocumentDuplex 和 JobDuplexAllDocumentsContiguously 互斥。</span><span class="sxs-lookup"><span data-stu-id="ad32f-110">DocumentDuplex and JobDuplexAllDocumentsContiguously are mutually exclusive.</span></span> <span data-ttu-id="ad32f-111">驅動程式會決定這些關鍵字之間的條件約束處理。</span><span class="sxs-lookup"><span data-stu-id="ad32f-111">It is up to the driver to determine constraint handling between these keywords.</span></span>

-   [<span data-ttu-id="ad32f-112">項目資訊</span><span class="sxs-lookup"><span data-stu-id="ad32f-112">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="ad32f-113">結構化內容</span><span class="sxs-lookup"><span data-stu-id="ad32f-113">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="ad32f-114">可延伸標記語言 (XML)  (XML) 內容</span><span class="sxs-lookup"><span data-stu-id="ad32f-114">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="ad32f-115">項目資訊</span><span class="sxs-lookup"><span data-stu-id="ad32f-115">Element Information</span></span>



| <span data-ttu-id="ad32f-116">Name</span><span class="sxs-lookup"><span data-stu-id="ad32f-116">Name</span></span>                       |                     |
|----------------------------|---------------------|
| <span data-ttu-id="ad32f-117">項目類型</span><span class="sxs-lookup"><span data-stu-id="ad32f-117">Element Type</span></span> <br/>   | <span data-ttu-id="ad32f-118">功能</span><span class="sxs-lookup"><span data-stu-id="ad32f-118">Feature</span></span><br/>  |
| <span data-ttu-id="ad32f-119">範圍前置詞</span><span class="sxs-lookup"><span data-stu-id="ad32f-119">Scoping Prefix</span></span> <br/> | <span data-ttu-id="ad32f-120">文件</span><span class="sxs-lookup"><span data-stu-id="ad32f-120">Document</span></span><br/> |
| <span data-ttu-id="ad32f-121">注意</span><span class="sxs-lookup"><span data-stu-id="ad32f-121">Notes</span></span> <br/>          | <span data-ttu-id="ad32f-122">None</span><span class="sxs-lookup"><span data-stu-id="ad32f-122">None</span></span><br/>     |



 

## <a name="structural-content"></a><span data-ttu-id="ad32f-123">結構化內容</span><span class="sxs-lookup"><span data-stu-id="ad32f-123">Structural Content</span></span>

<span data-ttu-id="ad32f-124">此元素的 XML 結構如下所示：</span><span class="sxs-lookup"><span data-stu-id="ad32f-124">The XML structure of this element is as follows:</span></span>

``` syntax
<psf:Feature name="psk:DocumentDuplex">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option name="psk:_OptionName_">
    <psf:Property name="psf:IdentityOption">
      <psf:Value xsi:type="xs:string">_IdentityOptionValue_</psf:Value>
    </psf:Property>
    <psf:ScoredProperty name="psk:DuplexMode">
      <psf:Value xsi:type="xs:string">_DuplexModeValue_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature>      
```

## <a name="structure-variables"></a><span data-ttu-id="ad32f-125">結構變數</span><span class="sxs-lookup"><span data-stu-id="ad32f-125">Structure Variables</span></span>

<span data-ttu-id="ad32f-126">下表概述 XML 結構中所定義之變數的特性。</span><span class="sxs-lookup"><span data-stu-id="ad32f-126">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="ad32f-127">Name</span><span class="sxs-lookup"><span data-stu-id="ad32f-127">Name</span></span>                               | <span data-ttu-id="ad32f-128">資料類型</span><span class="sxs-lookup"><span data-stu-id="ad32f-128">Data type</span></span>         | <span data-ttu-id="ad32f-129">單位</span><span class="sxs-lookup"><span data-stu-id="ad32f-129">Unit</span></span>                  | <span data-ttu-id="ad32f-130">支援的值</span><span class="sxs-lookup"><span data-stu-id="ad32f-130">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="ad32f-131">總結</span><span class="sxs-lookup"><span data-stu-id="ad32f-131">Summary</span></span>                                                                                                                                |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ad32f-132">\_選項名稱\_</span><span class="sxs-lookup"><span data-stu-id="ad32f-132">\_OptionName\_</span></span><br/>          | <span data-ttu-id="ad32f-133">字串</span><span class="sxs-lookup"><span data-stu-id="ad32f-133">string</span></span><br/> | <span data-ttu-id="ad32f-134">字元</span><span class="sxs-lookup"><span data-stu-id="ad32f-134">characters</span></span><br/> | <span data-ttu-id="ad32f-135">以 [XML 命名空間](https://www.w3.org/TR/1999/REC-xml-names-19990114/)所定義的有效完整名稱。</span><span class="sxs-lookup"><span data-stu-id="ad32f-135">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="ad32f-136">如果未指定命名空間，則會假設為預設命名空間。</span><span class="sxs-lookup"><span data-stu-id="ad32f-136">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="ad32f-137">選項的名稱。</span><span class="sxs-lookup"><span data-stu-id="ad32f-137">The name of the option.</span></span><br/>                                                                                                     |
| <span data-ttu-id="ad32f-138">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="ad32f-138">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="ad32f-139">字串</span><span class="sxs-lookup"><span data-stu-id="ad32f-139">string</span></span><br/> | <span data-ttu-id="ad32f-140">n/a</span><span class="sxs-lookup"><span data-stu-id="ad32f-140">n/a</span></span><br/>        | <span data-ttu-id="ad32f-141">True、False。</span><span class="sxs-lookup"><span data-stu-id="ad32f-141">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="ad32f-142">定義選項，當選取此選項時，會停用此功能。</span><span class="sxs-lookup"><span data-stu-id="ad32f-142">Defines an Option which when selected would disable this feature.</span></span><br/>                                                           |
| <span data-ttu-id="ad32f-143">\_DuplexModeValue\_</span><span class="sxs-lookup"><span data-stu-id="ad32f-143">\_DuplexModeValue\_</span></span><br/>     | <span data-ttu-id="ad32f-144">字串</span><span class="sxs-lookup"><span data-stu-id="ad32f-144">string</span></span><br/> | <span data-ttu-id="ad32f-145">n/a</span><span class="sxs-lookup"><span data-stu-id="ad32f-145">n/a</span></span><br/>        | <span data-ttu-id="ad32f-146">自動、手動。</span><span class="sxs-lookup"><span data-stu-id="ad32f-146">Automatic, Manual.</span></span><br/>                                                                                                                                                         | <span data-ttu-id="ad32f-147">定義雙工模式。</span><span class="sxs-lookup"><span data-stu-id="ad32f-147">Defines the duplex mode.</span></span> <span data-ttu-id="ad32f-148">自動雙工是由硬體執行。</span><span class="sxs-lookup"><span data-stu-id="ad32f-148">Automatic duplex is performed by hardware.</span></span> <span data-ttu-id="ad32f-149">手動雙工是由軟體和使用者執行。</span><span class="sxs-lookup"><span data-stu-id="ad32f-149">Manual duplexing is performed by software and the user.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="ad32f-150">可延伸標記語言 (XML)  (XML) 內容</span><span class="sxs-lookup"><span data-stu-id="ad32f-150">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="ad32f-151">公用列印架構關鍵字是在 https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords 命名空間中定義。</span><span class="sxs-lookup"><span data-stu-id="ad32f-151">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="ad32f-152">此關鍵字的 public 可延伸標記語言 (XML)  (XML) 內容定義如下：</span><span class="sxs-lookup"><span data-stu-id="ad32f-152">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:DocumentDuplex">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!-- Specifies one sided printing. -->
  <psf:Option name="psk:OneSided" />
  <!-- Specifies two sided printing such that the page is flipped parallel to the MediaSizeWidth direction. -->
  <psf:Option name="psk:TwoSidedShortEdge">
    <psf:ScoredProperty name="psk:DuplexMode">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies two sided printing such that the page is flipped parallel to the MediaSizeHeight direction. -->
  <psf:Option name="psk:TwoSidedLongEdge">
    <psf:ScoredProperty name="psk:DuplexMode">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature>    
```

## <a name="related-topics"></a><span data-ttu-id="ad32f-153">相關主題</span><span class="sxs-lookup"><span data-stu-id="ad32f-153">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ad32f-154">列印架構規格</span><span class="sxs-lookup"><span data-stu-id="ad32f-154">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




