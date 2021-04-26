---
description: 本主題並非最新的。 如需最新資訊，請參閱列印架構規格。
ms.assetid: 78eb3119-a52f-4ff8-83bb-903e181c8a11
title: PageInputBin
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f74e75653f7c6cbc6a586b80b3e8217286ce7c36
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/26/2021
ms.locfileid: "107993765"
---
# <a name="pageinputbin"></a><span data-ttu-id="335b6-104">PageInputBin</span><span class="sxs-lookup"><span data-stu-id="335b6-104">PageInputBin</span></span>

<span data-ttu-id="335b6-105">本主題並非最新的。</span><span class="sxs-lookup"><span data-stu-id="335b6-105">This topic is not current.</span></span> <span data-ttu-id="335b6-106">如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。</span><span class="sxs-lookup"><span data-stu-id="335b6-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="335b6-107">描述裝置中已安裝的輸入 bin，或裝置支援的 bin 完整清單。</span><span class="sxs-lookup"><span data-stu-id="335b6-107">Describes the installed input bin in a device or the full list of supported bins for a device.</span></span> <span data-ttu-id="335b6-108">允許以每頁為基礎的輸入 bin 規格。</span><span class="sxs-lookup"><span data-stu-id="335b6-108">Allows specification of input bin on a per page basis.</span></span> <span data-ttu-id="335b6-109">JobInputBin、DocumentInputBin 和 PageInputBin 關鍵字都是互斥的。</span><span class="sxs-lookup"><span data-stu-id="335b6-109">The JobInputBin, DocumentInputBin, and PageInputBin keywords are mutually exclusive.</span></span> <span data-ttu-id="335b6-110">這兩者不能同時在 PrintTicket 或列印功能檔中指定。</span><span class="sxs-lookup"><span data-stu-id="335b6-110">Both should not be specified simultaneously in a PrintTicket or Print Capabilities document.</span></span>

-   [<span data-ttu-id="335b6-111">項目資訊</span><span class="sxs-lookup"><span data-stu-id="335b6-111">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="335b6-112">結構化內容</span><span class="sxs-lookup"><span data-stu-id="335b6-112">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="335b6-113">可延伸標記語言 (XML)  (XML) 內容</span><span class="sxs-lookup"><span data-stu-id="335b6-113">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="335b6-114">項目資訊</span><span class="sxs-lookup"><span data-stu-id="335b6-114">Element Information</span></span>



| <span data-ttu-id="335b6-115">Name</span><span class="sxs-lookup"><span data-stu-id="335b6-115">Name</span></span> | <span data-ttu-id="335b6-116">值</span><span class="sxs-lookup"><span data-stu-id="335b6-116">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="335b6-117">項目類型</span><span class="sxs-lookup"><span data-stu-id="335b6-117">Element Type</span></span> <br/>   | <span data-ttu-id="335b6-118">功能</span><span class="sxs-lookup"><span data-stu-id="335b6-118">Feature</span></span><br/> |
| <span data-ttu-id="335b6-119">範圍前置詞</span><span class="sxs-lookup"><span data-stu-id="335b6-119">Scoping Prefix</span></span> <br/> | <span data-ttu-id="335b6-120">頁面</span><span class="sxs-lookup"><span data-stu-id="335b6-120">Page</span></span><br/>    |
| <span data-ttu-id="335b6-121">注意</span><span class="sxs-lookup"><span data-stu-id="335b6-121">Notes</span></span> <br/>          | <span data-ttu-id="335b6-122">None</span><span class="sxs-lookup"><span data-stu-id="335b6-122">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="335b6-123">結構化內容</span><span class="sxs-lookup"><span data-stu-id="335b6-123">Structural Content</span></span>

<span data-ttu-id="335b6-124">此元素的 XML 結構為：</span><span class="sxs-lookup"><span data-stu-id="335b6-124">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:PageInputBin">
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

## <a name="structure-variables"></a><span data-ttu-id="335b6-125">結構變數</span><span class="sxs-lookup"><span data-stu-id="335b6-125">Structure Variables</span></span>

<span data-ttu-id="335b6-126">下表概述 XML 結構中所定義之變數的特性。</span><span class="sxs-lookup"><span data-stu-id="335b6-126">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="335b6-127">Name</span><span class="sxs-lookup"><span data-stu-id="335b6-127">Name</span></span>                                   | <span data-ttu-id="335b6-128">資料類型</span><span class="sxs-lookup"><span data-stu-id="335b6-128">Data type</span></span>          | <span data-ttu-id="335b6-129">單位</span><span class="sxs-lookup"><span data-stu-id="335b6-129">Unit</span></span>                  | <span data-ttu-id="335b6-130">支援的值</span><span class="sxs-lookup"><span data-stu-id="335b6-130">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="335b6-131">總結</span><span class="sxs-lookup"><span data-stu-id="335b6-131">Summary</span></span>                                                                             |
|----------------------------------------|--------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="335b6-132">\_選項名稱\_</span><span class="sxs-lookup"><span data-stu-id="335b6-132">\_OptionName\_</span></span><br/>              | <span data-ttu-id="335b6-133">字串</span><span class="sxs-lookup"><span data-stu-id="335b6-133">string</span></span><br/>  | <span data-ttu-id="335b6-134">字元</span><span class="sxs-lookup"><span data-stu-id="335b6-134">characters</span></span><br/> | <span data-ttu-id="335b6-135">以 [XML 命名空間](https://www.w3.org/TR/1999/REC-xml-names-19990114/)所定義的有效完整名稱。</span><span class="sxs-lookup"><span data-stu-id="335b6-135">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="335b6-136">如果未指定命名空間，則會假設為預設命名空間。</span><span class="sxs-lookup"><span data-stu-id="335b6-136">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="335b6-137">選項的名稱。</span><span class="sxs-lookup"><span data-stu-id="335b6-137">The name of the option.</span></span><br/>                                                  |
| <span data-ttu-id="335b6-138">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="335b6-138">\_IdentityOptionValue\_</span></span><br/>     | <span data-ttu-id="335b6-139">字串</span><span class="sxs-lookup"><span data-stu-id="335b6-139">string</span></span><br/>  | <span data-ttu-id="335b6-140">n/a</span><span class="sxs-lookup"><span data-stu-id="335b6-140">n/a</span></span><br/>        | <span data-ttu-id="335b6-141">True、False。</span><span class="sxs-lookup"><span data-stu-id="335b6-141">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="335b6-142">定義選項，當選取此選項時，會停用此功能。</span><span class="sxs-lookup"><span data-stu-id="335b6-142">Defines an Option which when selected would disable this feature.</span></span><br/>        |
| <span data-ttu-id="335b6-143">\_EnvelopeOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="335b6-143">\_EnvelopeOptionValue\_</span></span><br/>     | <span data-ttu-id="335b6-144">字串</span><span class="sxs-lookup"><span data-stu-id="335b6-144">string</span></span><br/>  | <span data-ttu-id="335b6-145">n/a</span><span class="sxs-lookup"><span data-stu-id="335b6-145">n/a</span></span><br/>        | <span data-ttu-id="335b6-146">True、False。</span><span class="sxs-lookup"><span data-stu-id="335b6-146">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="335b6-147">定義選項，當選取此選項時，會停用此功能。</span><span class="sxs-lookup"><span data-stu-id="335b6-147">Defines an Option which when selected would disable this feature.</span></span><br/>        |
| <span data-ttu-id="335b6-148">\_BinTypeValue\_</span><span class="sxs-lookup"><span data-stu-id="335b6-148">\_BinTypeValue\_</span></span><br/>            | <span data-ttu-id="335b6-149">字串</span><span class="sxs-lookup"><span data-stu-id="335b6-149">string</span></span><br/>  | <span data-ttu-id="335b6-150">n/a</span><span class="sxs-lookup"><span data-stu-id="335b6-150">n/a</span></span><br/>        | <span data-ttu-id="335b6-151">ContinuousFeed, SheetFeed.</span><span class="sxs-lookup"><span data-stu-id="335b6-151">ContinuousFeed, SheetFeed.</span></span><br/>                                                                                                                                                 | <span data-ttu-id="335b6-152">指定 bin 的類型。</span><span class="sxs-lookup"><span data-stu-id="335b6-152">Specifies the type of the bin.</span></span><br/>                                           |
| <span data-ttu-id="335b6-153">\_FeedTypeValue\_</span><span class="sxs-lookup"><span data-stu-id="335b6-153">\_FeedTypeValue\_</span></span><br/>           | <span data-ttu-id="335b6-154">字串</span><span class="sxs-lookup"><span data-stu-id="335b6-154">string</span></span><br/>  | <span data-ttu-id="335b6-155">n/a</span><span class="sxs-lookup"><span data-stu-id="335b6-155">n/a</span></span><br/>        | <span data-ttu-id="335b6-156">自動、手動。</span><span class="sxs-lookup"><span data-stu-id="335b6-156">Automatic, Manual.</span></span><br/>                                                                                                                                                         | <span data-ttu-id="335b6-157">指定 bin 的摘要機制。</span><span class="sxs-lookup"><span data-stu-id="335b6-157">Specifies the feed mechanism of the bin.</span></span><br/>                                 |
| <span data-ttu-id="335b6-158">\_MediaCapacityValue\_</span><span class="sxs-lookup"><span data-stu-id="335b6-158">\_MediaCapacityValue\_</span></span><br/>      | <span data-ttu-id="335b6-159">字串</span><span class="sxs-lookup"><span data-stu-id="335b6-159">string</span></span><br/>  | <span data-ttu-id="335b6-160">n/a</span><span class="sxs-lookup"><span data-stu-id="335b6-160">n/a</span></span><br/>        | <span data-ttu-id="335b6-161">高、標準。</span><span class="sxs-lookup"><span data-stu-id="335b6-161">High, Standard.</span></span><br/>                                                                                                                                                            | <span data-ttu-id="335b6-162">指定 bin 是否為高容量 bin (定性) 。</span><span class="sxs-lookup"><span data-stu-id="335b6-162">Specifies whether the bin is a high capacity bin (qualitative).</span></span><br/>          |
| <span data-ttu-id="335b6-163">\_MediaSizeAutoSenseValue\_</span><span class="sxs-lookup"><span data-stu-id="335b6-163">\_MediaSizeAutoSenseValue\_</span></span><br/> | <span data-ttu-id="335b6-164">字串</span><span class="sxs-lookup"><span data-stu-id="335b6-164">string</span></span><br/>  | <span data-ttu-id="335b6-165">n/a</span><span class="sxs-lookup"><span data-stu-id="335b6-165">n/a</span></span><br/>        | <span data-ttu-id="335b6-166">支援、無。</span><span class="sxs-lookup"><span data-stu-id="335b6-166">Supported, None.</span></span><br/>                                                                                                                                                           | <span data-ttu-id="335b6-167">指定裝置的媒體大小自動感知功能。</span><span class="sxs-lookup"><span data-stu-id="335b6-167">Specifies the media size auto sense capability of device.</span></span><br/>                |
| <span data-ttu-id="335b6-168">\_MediaTypeAutoSenseValue\_</span><span class="sxs-lookup"><span data-stu-id="335b6-168">\_MediaTypeAutoSenseValue\_</span></span><br/> | <span data-ttu-id="335b6-169">字串</span><span class="sxs-lookup"><span data-stu-id="335b6-169">string</span></span><br/>  | <span data-ttu-id="335b6-170">n/a</span><span class="sxs-lookup"><span data-stu-id="335b6-170">n/a</span></span><br/>        | <span data-ttu-id="335b6-171">支援、無。</span><span class="sxs-lookup"><span data-stu-id="335b6-171">Supported, None.</span></span><br/>                                                                                                                                                           | <span data-ttu-id="335b6-172">指定裝置的媒體類型自動感知功能。</span><span class="sxs-lookup"><span data-stu-id="335b6-172">Specifies the media type auto sense capability of device.</span></span><br/>                |
| <span data-ttu-id="335b6-173">\_MediaSheetCapacityValue\_</span><span class="sxs-lookup"><span data-stu-id="335b6-173">\_MediaSheetCapacityValue\_</span></span><br/> | <span data-ttu-id="335b6-174">整數</span><span class="sxs-lookup"><span data-stu-id="335b6-174">integer</span></span><br/> | <span data-ttu-id="335b6-175">床單</span><span class="sxs-lookup"><span data-stu-id="335b6-175">sheets</span></span><br/>     | <span data-ttu-id="335b6-176">裝置允許的最大整數條件約束。</span><span class="sxs-lookup"><span data-stu-id="335b6-176">Maximum integer constraint allowed by device.</span></span><br/>                                                                                                                              | <span data-ttu-id="335b6-177">以 (完整層級) 的頁面數目指定媒體容量。</span><span class="sxs-lookup"><span data-stu-id="335b6-177">Specifies the Media capacity in number of pages (full level) of the bin.</span></span><br/> |
| <span data-ttu-id="335b6-178">\_MediaPathValue\_</span><span class="sxs-lookup"><span data-stu-id="335b6-178">\_MediaPathValue\_</span></span><br/>          | <span data-ttu-id="335b6-179">字串</span><span class="sxs-lookup"><span data-stu-id="335b6-179">string</span></span><br/>  | <span data-ttu-id="335b6-180">n/a</span><span class="sxs-lookup"><span data-stu-id="335b6-180">n/a</span></span><br/>        | <span data-ttu-id="335b6-181">直接、Serpentine。</span><span class="sxs-lookup"><span data-stu-id="335b6-181">Straight, Serpentine.</span></span><br/>                                                                                                                                                      | <span data-ttu-id="335b6-182">指定媒體路徑的特性。</span><span class="sxs-lookup"><span data-stu-id="335b6-182">Specifies the characteristics of the media path.</span></span><br/>                         |
| <span data-ttu-id="335b6-183">\_FeedFaceValue\_</span><span class="sxs-lookup"><span data-stu-id="335b6-183">\_FeedFaceValue\_</span></span><br/>           | <span data-ttu-id="335b6-184">字串</span><span class="sxs-lookup"><span data-stu-id="335b6-184">string</span></span><br/>  | <span data-ttu-id="335b6-185">n/a</span><span class="sxs-lookup"><span data-stu-id="335b6-185">n/a</span></span><br/>        | <span data-ttu-id="335b6-186">FaceUp, FaceDown</span><span class="sxs-lookup"><span data-stu-id="335b6-186">FaceUp, FaceDown</span></span><br/>                                                                                                                                                           | <span data-ttu-id="335b6-187">指定是否要將媒體列印面朝上或朝下。</span><span class="sxs-lookup"><span data-stu-id="335b6-187">Specifies whether media is to be printed face up or face down.</span></span><br/>           |
| <span data-ttu-id="335b6-188">\_FeedDirectionValue\_</span><span class="sxs-lookup"><span data-stu-id="335b6-188">\_FeedDirectionValue\_</span></span><br/>      | <span data-ttu-id="335b6-189">字串</span><span class="sxs-lookup"><span data-stu-id="335b6-189">string</span></span><br/>  | <span data-ttu-id="335b6-190">n/a</span><span class="sxs-lookup"><span data-stu-id="335b6-190">n/a</span></span><br/>        | <span data-ttu-id="335b6-191">LongEdgeFirst, ShortEdgeFirst</span><span class="sxs-lookup"><span data-stu-id="335b6-191">LongEdgeFirst, ShortEdgeFirst</span></span><br/>                                                                                                                                              | <span data-ttu-id="335b6-192">指定是否要先將媒體送入較長的第一或短邊緣。</span><span class="sxs-lookup"><span data-stu-id="335b6-192">Specifies whether media is fed long edge first or short edge first.</span></span><br/>      |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="335b6-193">可延伸標記語言 (XML)  (XML) 內容</span><span class="sxs-lookup"><span data-stu-id="335b6-193">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="335b6-194">公用列印架構關鍵字是在 https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords 命名空間中定義。</span><span class="sxs-lookup"><span data-stu-id="335b6-194">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="335b6-195">此關鍵字的 public 可延伸標記語言 (XML)  (XML) 內容定義如下：</span><span class="sxs-lookup"><span data-stu-id="335b6-195">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:PageInputBin">
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

## <a name="related-topics"></a><span data-ttu-id="335b6-196">相關主題</span><span class="sxs-lookup"><span data-stu-id="335b6-196">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="335b6-197">列印架構規格</span><span class="sxs-lookup"><span data-stu-id="335b6-197">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




