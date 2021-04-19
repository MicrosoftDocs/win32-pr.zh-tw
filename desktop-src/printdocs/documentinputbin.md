---
description: 本主題並非最新的。 如需最新資訊，請參閱列印架構規格。
ms.assetid: 334503d7-c044-41f7-b6aa-892b002b7a4e
title: DocumentInputBin
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95a4459f621ac4455a69e891c2eeda6f785b6d8b
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/06/2021
ms.locfileid: "106990005"
---
# <a name="documentinputbin"></a><span data-ttu-id="124dd-104">DocumentInputBin</span><span class="sxs-lookup"><span data-stu-id="124dd-104">DocumentInputBin</span></span>

<span data-ttu-id="124dd-105">本主題並非最新的。</span><span class="sxs-lookup"><span data-stu-id="124dd-105">This topic is not current.</span></span> <span data-ttu-id="124dd-106">如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。</span><span class="sxs-lookup"><span data-stu-id="124dd-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="124dd-107">描述裝置中已安裝的輸入 bin，或裝置支援的 bin 完整清單。</span><span class="sxs-lookup"><span data-stu-id="124dd-107">Describes the installed input bin in a device or the full list of supported bins for a device.</span></span> <span data-ttu-id="124dd-108">JobInputBin、DocumentInputBin 和 PageInputBin 關鍵字都是互斥的。</span><span class="sxs-lookup"><span data-stu-id="124dd-108">The JobInputBin, DocumentInputBin, and PageInputBin keywords are mutually exclusive.</span></span> <span data-ttu-id="124dd-109">這兩者不能同時在 PrintTicket 或列印功能檔中指定。</span><span class="sxs-lookup"><span data-stu-id="124dd-109">Both should not be specified simultaneously in a PrintTicket or Print Capabilities document.</span></span>

-   [<span data-ttu-id="124dd-110">項目資訊</span><span class="sxs-lookup"><span data-stu-id="124dd-110">Element Information</span></span>](#element-information)

-   [<span data-ttu-id="124dd-111">結構化內容</span><span class="sxs-lookup"><span data-stu-id="124dd-111">Structural Content</span></span>](#structural-content)

-   [<span data-ttu-id="124dd-112">XML 內容</span><span class="sxs-lookup"><span data-stu-id="124dd-112">XML Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="124dd-113">項目資訊</span><span class="sxs-lookup"><span data-stu-id="124dd-113">Element Information</span></span>



| <span data-ttu-id="124dd-114">Name</span><span class="sxs-lookup"><span data-stu-id="124dd-114">Name</span></span>                       |                                                                                                                                |
|----------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="124dd-115">項目類型</span><span class="sxs-lookup"><span data-stu-id="124dd-115">Element Type</span></span> <br/>   | <span data-ttu-id="124dd-116">功能</span><span class="sxs-lookup"><span data-stu-id="124dd-116">Feature</span></span><br/>                                                                                                             |
| <span data-ttu-id="124dd-117">範圍前置詞</span><span class="sxs-lookup"><span data-stu-id="124dd-117">Scoping Prefix</span></span> <br/> | <span data-ttu-id="124dd-118">文件</span><span class="sxs-lookup"><span data-stu-id="124dd-118">Document</span></span><br/>                                                                                                            |
| <span data-ttu-id="124dd-119">備註</span><span class="sxs-lookup"><span data-stu-id="124dd-119">Notes</span></span> <br/>          | <span data-ttu-id="124dd-120">目前未安裝的支援的 bin 應該在 PrintCapabilities 檔中標示為受限制。</span><span class="sxs-lookup"><span data-stu-id="124dd-120">Supported bins that are not currently installed should be flagged as constrained in the PrintCapabilities document.</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="124dd-121">結構化內容</span><span class="sxs-lookup"><span data-stu-id="124dd-121">Structural Content</span></span>

<span data-ttu-id="124dd-122">此元素的 XML 結構為：</span><span class="sxs-lookup"><span data-stu-id="124dd-122">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="124dd-123">結構變數</span><span class="sxs-lookup"><span data-stu-id="124dd-123">Structure Variables</span></span>

<span data-ttu-id="124dd-124">下表概述 XML 結構中所定義之變數的特性。</span><span class="sxs-lookup"><span data-stu-id="124dd-124">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="124dd-125">Name</span><span class="sxs-lookup"><span data-stu-id="124dd-125">Name</span></span>                                   | <span data-ttu-id="124dd-126">資料類型</span><span class="sxs-lookup"><span data-stu-id="124dd-126">Data type</span></span>          | <span data-ttu-id="124dd-127">單位</span><span class="sxs-lookup"><span data-stu-id="124dd-127">Unit</span></span>                  | <span data-ttu-id="124dd-128">支援的值</span><span class="sxs-lookup"><span data-stu-id="124dd-128">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="124dd-129">總結</span><span class="sxs-lookup"><span data-stu-id="124dd-129">Summary</span></span>                                                                             |
|----------------------------------------|--------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="124dd-130">\_選項名稱\_</span><span class="sxs-lookup"><span data-stu-id="124dd-130">\_OptionName\_</span></span><br/>              | <span data-ttu-id="124dd-131">字串</span><span class="sxs-lookup"><span data-stu-id="124dd-131">string</span></span><br/>  | <span data-ttu-id="124dd-132">字元</span><span class="sxs-lookup"><span data-stu-id="124dd-132">characters</span></span><br/> | <span data-ttu-id="124dd-133">以 [XML 命名空間](https://www.w3.org/TR/1999/REC-xml-names-19990114/)所定義的有效完整名稱。</span><span class="sxs-lookup"><span data-stu-id="124dd-133">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="124dd-134">如果未指定命名空間，則會假設為預設命名空間。</span><span class="sxs-lookup"><span data-stu-id="124dd-134">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="124dd-135">選項的名稱。</span><span class="sxs-lookup"><span data-stu-id="124dd-135">The name of the option.</span></span><br/>                                                  |
| <span data-ttu-id="124dd-136">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="124dd-136">\_IdentityOptionValue\_</span></span><br/>     | <span data-ttu-id="124dd-137">字串</span><span class="sxs-lookup"><span data-stu-id="124dd-137">string</span></span><br/>  | <span data-ttu-id="124dd-138">n/a</span><span class="sxs-lookup"><span data-stu-id="124dd-138">n/a</span></span><br/>        | <span data-ttu-id="124dd-139">True、False。</span><span class="sxs-lookup"><span data-stu-id="124dd-139">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="124dd-140">定義選項，當選取此選項時，會停用此功能。</span><span class="sxs-lookup"><span data-stu-id="124dd-140">Defines an Option which when selected would disable this feature.</span></span><br/>        |
| <span data-ttu-id="124dd-141">\_EnvelopeOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="124dd-141">\_EnvelopeOptionValue\_</span></span><br/>     | <span data-ttu-id="124dd-142">字串</span><span class="sxs-lookup"><span data-stu-id="124dd-142">string</span></span><br/>  | <span data-ttu-id="124dd-143">n/a</span><span class="sxs-lookup"><span data-stu-id="124dd-143">n/a</span></span><br/>        | <span data-ttu-id="124dd-144">True、False。</span><span class="sxs-lookup"><span data-stu-id="124dd-144">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="124dd-145">定義選項，當選取此選項時，會停用此功能。</span><span class="sxs-lookup"><span data-stu-id="124dd-145">Defines an Option which when selected would disable this feature.</span></span><br/>        |
| <span data-ttu-id="124dd-146">\_BinTypeValue\_</span><span class="sxs-lookup"><span data-stu-id="124dd-146">\_BinTypeValue\_</span></span><br/>            | <span data-ttu-id="124dd-147">字串</span><span class="sxs-lookup"><span data-stu-id="124dd-147">string</span></span><br/>  | <span data-ttu-id="124dd-148">n/a</span><span class="sxs-lookup"><span data-stu-id="124dd-148">n/a</span></span><br/>        | <span data-ttu-id="124dd-149">ContinuousFeed, SheetFeed.</span><span class="sxs-lookup"><span data-stu-id="124dd-149">ContinuousFeed, SheetFeed.</span></span><br/>                                                                                                                                                 | <span data-ttu-id="124dd-150">指定 bin 的類型。</span><span class="sxs-lookup"><span data-stu-id="124dd-150">Specifies the type of the bin.</span></span><br/>                                           |
| <span data-ttu-id="124dd-151">\_FeedTypeValue\_</span><span class="sxs-lookup"><span data-stu-id="124dd-151">\_FeedTypeValue\_</span></span><br/>           | <span data-ttu-id="124dd-152">字串</span><span class="sxs-lookup"><span data-stu-id="124dd-152">string</span></span><br/>  | <span data-ttu-id="124dd-153">n/a</span><span class="sxs-lookup"><span data-stu-id="124dd-153">n/a</span></span><br/>        | <span data-ttu-id="124dd-154">自動、手動。</span><span class="sxs-lookup"><span data-stu-id="124dd-154">Automatic, Manual.</span></span><br/>                                                                                                                                                         | <span data-ttu-id="124dd-155">指定 bin 的摘要機制。</span><span class="sxs-lookup"><span data-stu-id="124dd-155">Specifies the feed mechanism of the bin.</span></span><br/>                                 |
| <span data-ttu-id="124dd-156">\_MediaCapacityValue\_</span><span class="sxs-lookup"><span data-stu-id="124dd-156">\_MediaCapacityValue\_</span></span><br/>      | <span data-ttu-id="124dd-157">整數</span><span class="sxs-lookup"><span data-stu-id="124dd-157">integer</span></span><br/> | <span data-ttu-id="124dd-158">床單</span><span class="sxs-lookup"><span data-stu-id="124dd-158">sheets</span></span><br/>     | <span data-ttu-id="124dd-159">裝置允許的最大整數條件約束。</span><span class="sxs-lookup"><span data-stu-id="124dd-159">Maximum integer constraint allowed by device.</span></span><br/>                                                                                                                              | <span data-ttu-id="124dd-160">指定 bin 是否為高容量 bin (定性) 。</span><span class="sxs-lookup"><span data-stu-id="124dd-160">Specifies whether the bin is a high capacity bin (qualitative).</span></span><br/>          |
| <span data-ttu-id="124dd-161">\_MediaSizeAutoSenseValue\_</span><span class="sxs-lookup"><span data-stu-id="124dd-161">\_MediaSizeAutoSenseValue\_</span></span><br/> | <span data-ttu-id="124dd-162">字串</span><span class="sxs-lookup"><span data-stu-id="124dd-162">string</span></span><br/>  | <span data-ttu-id="124dd-163">n/a</span><span class="sxs-lookup"><span data-stu-id="124dd-163">n/a</span></span><br/>        | <span data-ttu-id="124dd-164">支援、無。</span><span class="sxs-lookup"><span data-stu-id="124dd-164">Supported, None.</span></span><br/>                                                                                                                                                           | <span data-ttu-id="124dd-165">指定裝置的媒體大小自動感知功能。</span><span class="sxs-lookup"><span data-stu-id="124dd-165">Specifies the media size auto sense capability of the device.</span></span><br/>            |
| <span data-ttu-id="124dd-166">\_MediaTypeAutoSenseValue\_</span><span class="sxs-lookup"><span data-stu-id="124dd-166">\_MediaTypeAutoSenseValue\_</span></span><br/> | <span data-ttu-id="124dd-167">字串</span><span class="sxs-lookup"><span data-stu-id="124dd-167">string</span></span><br/>  | <span data-ttu-id="124dd-168">n/a</span><span class="sxs-lookup"><span data-stu-id="124dd-168">n/a</span></span><br/>        | <span data-ttu-id="124dd-169">支援、無。</span><span class="sxs-lookup"><span data-stu-id="124dd-169">Supported, None.</span></span><br/>                                                                                                                                                           | <span data-ttu-id="124dd-170">以 (完整層級) 的頁面數目指定媒體容量。</span><span class="sxs-lookup"><span data-stu-id="124dd-170">Specifies the media capacity in number of pages (full level) of the bin.</span></span><br/> |
| <span data-ttu-id="124dd-171">\_MediaPathValue\_</span><span class="sxs-lookup"><span data-stu-id="124dd-171">\_MediaPathValue\_</span></span><br/>          | <span data-ttu-id="124dd-172">字串</span><span class="sxs-lookup"><span data-stu-id="124dd-172">string</span></span><br/>  | <span data-ttu-id="124dd-173">n/a</span><span class="sxs-lookup"><span data-stu-id="124dd-173">n/a</span></span><br/>        | <span data-ttu-id="124dd-174">直接、Serpentine。</span><span class="sxs-lookup"><span data-stu-id="124dd-174">Straight, Serpentine.</span></span><br/>                                                                                                                                                      | <span data-ttu-id="124dd-175">指定媒體路徑的特性。</span><span class="sxs-lookup"><span data-stu-id="124dd-175">Specifies the characteristics of the media path.</span></span><br/>                         |
| <span data-ttu-id="124dd-176">\_FeedFaceValue\_</span><span class="sxs-lookup"><span data-stu-id="124dd-176">\_FeedFaceValue\_</span></span><br/>           | <span data-ttu-id="124dd-177">字串</span><span class="sxs-lookup"><span data-stu-id="124dd-177">string</span></span><br/>  | <span data-ttu-id="124dd-178">n/a</span><span class="sxs-lookup"><span data-stu-id="124dd-178">n/a</span></span><br/>        | <span data-ttu-id="124dd-179">FaceUp, FaceDown</span><span class="sxs-lookup"><span data-stu-id="124dd-179">FaceUp, FaceDown</span></span><br/>                                                                                                                                                           | <span data-ttu-id="124dd-180">指定是否要將媒體列印面朝上或朝下。</span><span class="sxs-lookup"><span data-stu-id="124dd-180">Specifies whether media is to be printed face up or face down.</span></span><br/>           |
| <span data-ttu-id="124dd-181">\_FeedDirectionValue\_</span><span class="sxs-lookup"><span data-stu-id="124dd-181">\_FeedDirectionValue\_</span></span><br/>      | <span data-ttu-id="124dd-182">字串</span><span class="sxs-lookup"><span data-stu-id="124dd-182">string</span></span><br/>  | <span data-ttu-id="124dd-183">n/a</span><span class="sxs-lookup"><span data-stu-id="124dd-183">n/a</span></span><br/>        | <span data-ttu-id="124dd-184">LongEdgeFirst, ShortEdgeFirst</span><span class="sxs-lookup"><span data-stu-id="124dd-184">LongEdgeFirst, ShortEdgeFirst</span></span><br/>                                                                                                                                              | <span data-ttu-id="124dd-185">指定是否要先將媒體送入較長的第一或短邊緣。</span><span class="sxs-lookup"><span data-stu-id="124dd-185">Specifies whether media is fed long edge first or short edge first.</span></span><br/>      |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="124dd-186">可延伸標記語言 (XML)  (XML) 內容</span><span class="sxs-lookup"><span data-stu-id="124dd-186">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="124dd-187">公用列印架構關鍵字是在 https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords 命名空間中定義。</span><span class="sxs-lookup"><span data-stu-id="124dd-187">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="124dd-188">此關鍵字的 public 可延伸標記語言 (XML)  (XML) 內容定義如下：</span><span class="sxs-lookup"><span data-stu-id="124dd-188">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="124dd-189">相關主題</span><span class="sxs-lookup"><span data-stu-id="124dd-189">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="124dd-190">列印架構規格</span><span class="sxs-lookup"><span data-stu-id="124dd-190">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




