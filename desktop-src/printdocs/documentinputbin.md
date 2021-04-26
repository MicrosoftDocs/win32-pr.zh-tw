---
description: 本主題並非最新的。 如需最新資訊，請參閱列印架構規格。
ms.assetid: 334503d7-c044-41f7-b6aa-892b002b7a4e
title: DocumentInputBin
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57890492ed5f0b575e6d462351282dd199f34f45
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/26/2021
ms.locfileid: "107997765"
---
# <a name="documentinputbin"></a><span data-ttu-id="920ba-104">DocumentInputBin</span><span class="sxs-lookup"><span data-stu-id="920ba-104">DocumentInputBin</span></span>

<span data-ttu-id="920ba-105">本主題並非最新的。</span><span class="sxs-lookup"><span data-stu-id="920ba-105">This topic is not current.</span></span> <span data-ttu-id="920ba-106">如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。</span><span class="sxs-lookup"><span data-stu-id="920ba-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="920ba-107">描述裝置中已安裝的輸入 bin，或裝置支援的 bin 完整清單。</span><span class="sxs-lookup"><span data-stu-id="920ba-107">Describes the installed input bin in a device or the full list of supported bins for a device.</span></span> <span data-ttu-id="920ba-108">JobInputBin、DocumentInputBin 和 PageInputBin 關鍵字都是互斥的。</span><span class="sxs-lookup"><span data-stu-id="920ba-108">The JobInputBin, DocumentInputBin, and PageInputBin keywords are mutually exclusive.</span></span> <span data-ttu-id="920ba-109">這兩者不能同時在 PrintTicket 或列印功能檔中指定。</span><span class="sxs-lookup"><span data-stu-id="920ba-109">Both should not be specified simultaneously in a PrintTicket or Print Capabilities document.</span></span>

-   [<span data-ttu-id="920ba-110">項目資訊</span><span class="sxs-lookup"><span data-stu-id="920ba-110">Element Information</span></span>](#element-information)

-   [<span data-ttu-id="920ba-111">結構化內容</span><span class="sxs-lookup"><span data-stu-id="920ba-111">Structural Content</span></span>](#structural-content)

-   [<span data-ttu-id="920ba-112">XML 內容</span><span class="sxs-lookup"><span data-stu-id="920ba-112">XML Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="920ba-113">項目資訊</span><span class="sxs-lookup"><span data-stu-id="920ba-113">Element Information</span></span>



| <span data-ttu-id="920ba-114">Name</span><span class="sxs-lookup"><span data-stu-id="920ba-114">Name</span></span> | <span data-ttu-id="920ba-115">值</span><span class="sxs-lookup"><span data-stu-id="920ba-115">Value</span></span> |
|----------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="920ba-116">項目類型</span><span class="sxs-lookup"><span data-stu-id="920ba-116">Element Type</span></span> <br/>   | <span data-ttu-id="920ba-117">功能</span><span class="sxs-lookup"><span data-stu-id="920ba-117">Feature</span></span><br/>                                                                                                             |
| <span data-ttu-id="920ba-118">範圍前置詞</span><span class="sxs-lookup"><span data-stu-id="920ba-118">Scoping Prefix</span></span> <br/> | <span data-ttu-id="920ba-119">文件</span><span class="sxs-lookup"><span data-stu-id="920ba-119">Document</span></span><br/>                                                                                                            |
| <span data-ttu-id="920ba-120">備註</span><span class="sxs-lookup"><span data-stu-id="920ba-120">Notes</span></span> <br/>          | <span data-ttu-id="920ba-121">目前未安裝的支援的 bin 應該在 PrintCapabilities 檔中標示為受限制。</span><span class="sxs-lookup"><span data-stu-id="920ba-121">Supported bins that are not currently installed should be flagged as constrained in the PrintCapabilities document.</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="920ba-122">結構化內容</span><span class="sxs-lookup"><span data-stu-id="920ba-122">Structural Content</span></span>

<span data-ttu-id="920ba-123">此元素的 XML 結構為：</span><span class="sxs-lookup"><span data-stu-id="920ba-123">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:DocumentInputBin">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option name="psk:_OptionName_">
    <psf:Property name="psf:IdentityOption">
      <psf:Value xsi:type="xs:string">_IdentityOptionValue_</psf:Value>
    </psf:Property>
    <psf:Property name="psf:_EnvelopeOptionValue_">
      <psf:Value xsi:type="xs:string">_EnvelopeOptionValue_</psf:Value>
    </psf:Property>
    <psf:ScoredProperty name="psk:BinType">
      <psf:Value xsi:type="xs:string">_BinTypeValue_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:FeedType">
      <psf:Value xsi:type="xs:string">_FeedTypeValue_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaCapacity">
      <psf:Value xsi:type="xs:string">_MediaCapacityValue_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeAutoSense">
      <psf:Value xsi:type="xs:string">_MediaSizeAutoSenseValue_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaTypeAutoSense">
      <psf:Value xsi:type="xs:string">_MediaTypeAutoSenseValue_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSheetCapacity">
      <psf:Value xsi:type="xs:integer">_MediaSheetCapacityValue_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaPath">
      <psf:Value xsi:type="xs:string">_MediaPathValue_</psf:Value>
    </psf:ScoredProperty>
    <psf:Property name="psk:FeedFace">
      <psf:Value xsi:type="xs:string">_FeedFaceValue_</psf:Value>
    </psf:Property>
    <psf:Property name="psk:FeedDirection">
      <psf:Value xsi:type="xs:string">_FeedDirectionValue_</psf:Value>
    </psf:Property>
  </psf:Option>
</psf:Feature>
```

## <a name="structure-variables"></a><span data-ttu-id="920ba-124">結構變數</span><span class="sxs-lookup"><span data-stu-id="920ba-124">Structure Variables</span></span>

<span data-ttu-id="920ba-125">下表概述 XML 結構中所定義之變數的特性。</span><span class="sxs-lookup"><span data-stu-id="920ba-125">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="920ba-126">Name</span><span class="sxs-lookup"><span data-stu-id="920ba-126">Name</span></span>                                   | <span data-ttu-id="920ba-127">資料類型</span><span class="sxs-lookup"><span data-stu-id="920ba-127">Data type</span></span>          | <span data-ttu-id="920ba-128">單位</span><span class="sxs-lookup"><span data-stu-id="920ba-128">Unit</span></span>                  | <span data-ttu-id="920ba-129">支援的值</span><span class="sxs-lookup"><span data-stu-id="920ba-129">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="920ba-130">總結</span><span class="sxs-lookup"><span data-stu-id="920ba-130">Summary</span></span>                                                                             |
|----------------------------------------|--------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="920ba-131">\_選項名稱\_</span><span class="sxs-lookup"><span data-stu-id="920ba-131">\_OptionName\_</span></span><br/>              | <span data-ttu-id="920ba-132">字串</span><span class="sxs-lookup"><span data-stu-id="920ba-132">string</span></span><br/>  | <span data-ttu-id="920ba-133">字元</span><span class="sxs-lookup"><span data-stu-id="920ba-133">characters</span></span><br/> | <span data-ttu-id="920ba-134">以 [XML 命名空間](https://www.w3.org/TR/1999/REC-xml-names-19990114/)所定義的有效完整名稱。</span><span class="sxs-lookup"><span data-stu-id="920ba-134">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="920ba-135">如果未指定命名空間，則會假設為預設命名空間。</span><span class="sxs-lookup"><span data-stu-id="920ba-135">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="920ba-136">選項的名稱。</span><span class="sxs-lookup"><span data-stu-id="920ba-136">The name of the option.</span></span><br/>                                                  |
| <span data-ttu-id="920ba-137">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="920ba-137">\_IdentityOptionValue\_</span></span><br/>     | <span data-ttu-id="920ba-138">字串</span><span class="sxs-lookup"><span data-stu-id="920ba-138">string</span></span><br/>  | <span data-ttu-id="920ba-139">n/a</span><span class="sxs-lookup"><span data-stu-id="920ba-139">n/a</span></span><br/>        | <span data-ttu-id="920ba-140">True、False。</span><span class="sxs-lookup"><span data-stu-id="920ba-140">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="920ba-141">定義選項，當選取此選項時，會停用此功能。</span><span class="sxs-lookup"><span data-stu-id="920ba-141">Defines an Option which when selected would disable this feature.</span></span><br/>        |
| <span data-ttu-id="920ba-142">\_EnvelopeOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="920ba-142">\_EnvelopeOptionValue\_</span></span><br/>     | <span data-ttu-id="920ba-143">字串</span><span class="sxs-lookup"><span data-stu-id="920ba-143">string</span></span><br/>  | <span data-ttu-id="920ba-144">n/a</span><span class="sxs-lookup"><span data-stu-id="920ba-144">n/a</span></span><br/>        | <span data-ttu-id="920ba-145">True、False。</span><span class="sxs-lookup"><span data-stu-id="920ba-145">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="920ba-146">定義選項，當選取此選項時，會停用此功能。</span><span class="sxs-lookup"><span data-stu-id="920ba-146">Defines an Option which when selected would disable this feature.</span></span><br/>        |
| <span data-ttu-id="920ba-147">\_BinTypeValue\_</span><span class="sxs-lookup"><span data-stu-id="920ba-147">\_BinTypeValue\_</span></span><br/>            | <span data-ttu-id="920ba-148">字串</span><span class="sxs-lookup"><span data-stu-id="920ba-148">string</span></span><br/>  | <span data-ttu-id="920ba-149">n/a</span><span class="sxs-lookup"><span data-stu-id="920ba-149">n/a</span></span><br/>        | <span data-ttu-id="920ba-150">ContinuousFeed, SheetFeed.</span><span class="sxs-lookup"><span data-stu-id="920ba-150">ContinuousFeed, SheetFeed.</span></span><br/>                                                                                                                                                 | <span data-ttu-id="920ba-151">指定 bin 的類型。</span><span class="sxs-lookup"><span data-stu-id="920ba-151">Specifies the type of the bin.</span></span><br/>                                           |
| <span data-ttu-id="920ba-152">\_FeedTypeValue\_</span><span class="sxs-lookup"><span data-stu-id="920ba-152">\_FeedTypeValue\_</span></span><br/>           | <span data-ttu-id="920ba-153">字串</span><span class="sxs-lookup"><span data-stu-id="920ba-153">string</span></span><br/>  | <span data-ttu-id="920ba-154">n/a</span><span class="sxs-lookup"><span data-stu-id="920ba-154">n/a</span></span><br/>        | <span data-ttu-id="920ba-155">自動、手動。</span><span class="sxs-lookup"><span data-stu-id="920ba-155">Automatic, Manual.</span></span><br/>                                                                                                                                                         | <span data-ttu-id="920ba-156">指定 bin 的摘要機制。</span><span class="sxs-lookup"><span data-stu-id="920ba-156">Specifies the feed mechanism of the bin.</span></span><br/>                                 |
| <span data-ttu-id="920ba-157">\_MediaCapacityValue\_</span><span class="sxs-lookup"><span data-stu-id="920ba-157">\_MediaCapacityValue\_</span></span><br/>      | <span data-ttu-id="920ba-158">整數</span><span class="sxs-lookup"><span data-stu-id="920ba-158">integer</span></span><br/> | <span data-ttu-id="920ba-159">床單</span><span class="sxs-lookup"><span data-stu-id="920ba-159">sheets</span></span><br/>     | <span data-ttu-id="920ba-160">裝置允許的最大整數條件約束。</span><span class="sxs-lookup"><span data-stu-id="920ba-160">Maximum integer constraint allowed by device.</span></span><br/>                                                                                                                              | <span data-ttu-id="920ba-161">指定 bin 是否為高容量 bin (定性) 。</span><span class="sxs-lookup"><span data-stu-id="920ba-161">Specifies whether the bin is a high capacity bin (qualitative).</span></span><br/>          |
| <span data-ttu-id="920ba-162">\_MediaSizeAutoSenseValue\_</span><span class="sxs-lookup"><span data-stu-id="920ba-162">\_MediaSizeAutoSenseValue\_</span></span><br/> | <span data-ttu-id="920ba-163">字串</span><span class="sxs-lookup"><span data-stu-id="920ba-163">string</span></span><br/>  | <span data-ttu-id="920ba-164">n/a</span><span class="sxs-lookup"><span data-stu-id="920ba-164">n/a</span></span><br/>        | <span data-ttu-id="920ba-165">支援、無。</span><span class="sxs-lookup"><span data-stu-id="920ba-165">Supported, None.</span></span><br/>                                                                                                                                                           | <span data-ttu-id="920ba-166">指定裝置的媒體大小自動感知功能。</span><span class="sxs-lookup"><span data-stu-id="920ba-166">Specifies the media size auto sense capability of the device.</span></span><br/>            |
| <span data-ttu-id="920ba-167">\_MediaTypeAutoSenseValue\_</span><span class="sxs-lookup"><span data-stu-id="920ba-167">\_MediaTypeAutoSenseValue\_</span></span><br/> | <span data-ttu-id="920ba-168">字串</span><span class="sxs-lookup"><span data-stu-id="920ba-168">string</span></span><br/>  | <span data-ttu-id="920ba-169">n/a</span><span class="sxs-lookup"><span data-stu-id="920ba-169">n/a</span></span><br/>        | <span data-ttu-id="920ba-170">支援、無。</span><span class="sxs-lookup"><span data-stu-id="920ba-170">Supported, None.</span></span><br/>                                                                                                                                                           | <span data-ttu-id="920ba-171">以 (完整層級) 的頁面數目指定媒體容量。</span><span class="sxs-lookup"><span data-stu-id="920ba-171">Specifies the media capacity in number of pages (full level) of the bin.</span></span><br/> |
| <span data-ttu-id="920ba-172">\_MediaPathValue\_</span><span class="sxs-lookup"><span data-stu-id="920ba-172">\_MediaPathValue\_</span></span><br/>          | <span data-ttu-id="920ba-173">字串</span><span class="sxs-lookup"><span data-stu-id="920ba-173">string</span></span><br/>  | <span data-ttu-id="920ba-174">n/a</span><span class="sxs-lookup"><span data-stu-id="920ba-174">n/a</span></span><br/>        | <span data-ttu-id="920ba-175">直接、Serpentine。</span><span class="sxs-lookup"><span data-stu-id="920ba-175">Straight, Serpentine.</span></span><br/>                                                                                                                                                      | <span data-ttu-id="920ba-176">指定媒體路徑的特性。</span><span class="sxs-lookup"><span data-stu-id="920ba-176">Specifies the characteristics of the media path.</span></span><br/>                         |
| <span data-ttu-id="920ba-177">\_FeedFaceValue\_</span><span class="sxs-lookup"><span data-stu-id="920ba-177">\_FeedFaceValue\_</span></span><br/>           | <span data-ttu-id="920ba-178">字串</span><span class="sxs-lookup"><span data-stu-id="920ba-178">string</span></span><br/>  | <span data-ttu-id="920ba-179">n/a</span><span class="sxs-lookup"><span data-stu-id="920ba-179">n/a</span></span><br/>        | <span data-ttu-id="920ba-180">FaceUp, FaceDown</span><span class="sxs-lookup"><span data-stu-id="920ba-180">FaceUp, FaceDown</span></span><br/>                                                                                                                                                           | <span data-ttu-id="920ba-181">指定是否要將媒體列印面朝上或朝下。</span><span class="sxs-lookup"><span data-stu-id="920ba-181">Specifies whether media is to be printed face up or face down.</span></span><br/>           |
| <span data-ttu-id="920ba-182">\_FeedDirectionValue\_</span><span class="sxs-lookup"><span data-stu-id="920ba-182">\_FeedDirectionValue\_</span></span><br/>      | <span data-ttu-id="920ba-183">字串</span><span class="sxs-lookup"><span data-stu-id="920ba-183">string</span></span><br/>  | <span data-ttu-id="920ba-184">n/a</span><span class="sxs-lookup"><span data-stu-id="920ba-184">n/a</span></span><br/>        | <span data-ttu-id="920ba-185">LongEdgeFirst, ShortEdgeFirst</span><span class="sxs-lookup"><span data-stu-id="920ba-185">LongEdgeFirst, ShortEdgeFirst</span></span><br/>                                                                                                                                              | <span data-ttu-id="920ba-186">指定是否要先將媒體送入較長的第一或短邊緣。</span><span class="sxs-lookup"><span data-stu-id="920ba-186">Specifies whether media is fed long edge first or short edge first.</span></span><br/>      |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="920ba-187">可延伸標記語言 (XML)  (XML) 內容</span><span class="sxs-lookup"><span data-stu-id="920ba-187">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="920ba-188">公用列印架構關鍵字是在 https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords 命名空間中定義。</span><span class="sxs-lookup"><span data-stu-id="920ba-188">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="920ba-189">此關鍵字的 public 可延伸標記語言 (XML)  (XML) 內容定義如下：</span><span class="sxs-lookup"><span data-stu-id="920ba-189">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:DocumentInputBin">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!-- Device will automatically choose best option based on configuration -->
  <psf:Option name="psk:AutoSelect">
    <psf:ScoredProperty name="psk:BinType">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:FeedType">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaCapacity">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeAutoSense">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaTypeAutoSense">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSheetCapacity">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaPath">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:Property name="psk:FeedFace">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:Property>
    <psf:Property name="psk:FeedDirection">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:Property>
  </psf:Option>
  <!--Specifies the default manual feed bin -->
  <psf:Option name="psk:Manual">
    <psf:ScoredProperty name="psk:BinType">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:FeedType">
      <psf:Value xsi:type="xs:string">Manual</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaCapacity">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeAutoSense">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaTypeAutoSense">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSheetCapacity">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaPath">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:Property name="psk:FeedFace">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:Property>
    <psf:Property name="psk:FeedDirection">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:Property>
  </psf:Option>
  <!--Specifies the feed bin is a cassette-->
  <psf:Option name="psk:Cassette">
    <psf:ScoredProperty name="psk:BinType">
      <psf:Value xsi:type="xs:string">SheetFeed</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:FeedType">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaCapacity">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeAutoSense">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaTypeAutoSense">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSheetCapacity">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaPath">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:Property name="psk:FeedFace">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:Property>
    <psf:Property name="psk:FeedDirection">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:Property>
  </psf:Option>
  <!--Specifies the feed bin is a tractor-->
  <psf:Option name="psk:Tractor">
    <psf:ScoredProperty name="psk:BinType">
      <psf:Value xsi:type="xs:string">ContinuousFeed</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:FeedType">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaCapacity">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeAutoSense">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaTypeAutoSense">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSheetCapacity">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaPath">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:Property name="psk:FeedFace">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:Property>
    <psf:Property name="psk:FeedDirection">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:Property>
  </psf:Option>
  <!-- Device Input tray for Inkjet Printers -->
  <psf:Option name="psk:AutoSheetFeeder">
    <psf:ScoredProperty name="psk:BinType">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:FeedType">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaCapacity">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeAutoSense">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaTypeAutoSense">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSheetCapacity">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaPath">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:Property name="psk:FeedFace">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:Property>
    <psf:Property name="psk:FeedDirection">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:Property>
  </psf:Option>
</psf:Feature>
```

## <a name="related-topics"></a><span data-ttu-id="920ba-190">相關主題</span><span class="sxs-lookup"><span data-stu-id="920ba-190">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="920ba-191">列印架構規格</span><span class="sxs-lookup"><span data-stu-id="920ba-191">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




