---
description: 取得 PageInputBin 使用者可設定元素的相關資訊。 本主題並非最新的。 如需最新資訊，請參閱列印架構規格。
ms.assetid: 78eb3119-a52f-4ff8-83bb-903e181c8a11
title: PageInputBin
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc53d377106b95b26e694d531af2952cea98a8b1
ms.sourcegitcommit: 998d50f6def8a25850fc113fc8a2df903c829c5e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/09/2021
ms.locfileid: "113549166"
---
# <a name="pageinputbin"></a><span data-ttu-id="9479c-105">PageInputBin</span><span class="sxs-lookup"><span data-stu-id="9479c-105">PageInputBin</span></span>

<span data-ttu-id="9479c-106">本主題並非最新的。</span><span class="sxs-lookup"><span data-stu-id="9479c-106">This topic is not current.</span></span> <span data-ttu-id="9479c-107">如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。</span><span class="sxs-lookup"><span data-stu-id="9479c-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="9479c-108">描述裝置中已安裝的輸入 bin，或裝置支援的 bin 完整清單。</span><span class="sxs-lookup"><span data-stu-id="9479c-108">Describes the installed input bin in a device or the full list of supported bins for a device.</span></span> <span data-ttu-id="9479c-109">允許以每頁為基礎的輸入 bin 規格。</span><span class="sxs-lookup"><span data-stu-id="9479c-109">Allows specification of input bin on a per page basis.</span></span> <span data-ttu-id="9479c-110">JobInputBin、DocumentInputBin 和 PageInputBin 關鍵字都是互斥的。</span><span class="sxs-lookup"><span data-stu-id="9479c-110">The JobInputBin, DocumentInputBin, and PageInputBin keywords are mutually exclusive.</span></span> <span data-ttu-id="9479c-111">這兩者不能同時在 PrintTicket 或列印功能檔中指定。</span><span class="sxs-lookup"><span data-stu-id="9479c-111">Both should not be specified simultaneously in a PrintTicket or Print Capabilities document.</span></span>

-   [<span data-ttu-id="9479c-112">項目資訊</span><span class="sxs-lookup"><span data-stu-id="9479c-112">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="9479c-113">結構化內容</span><span class="sxs-lookup"><span data-stu-id="9479c-113">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="9479c-114">可延伸標記語言 (XML)  (XML) 內容</span><span class="sxs-lookup"><span data-stu-id="9479c-114">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="9479c-115">項目資訊</span><span class="sxs-lookup"><span data-stu-id="9479c-115">Element Information</span></span>



| <span data-ttu-id="9479c-116">Name</span><span class="sxs-lookup"><span data-stu-id="9479c-116">Name</span></span> | <span data-ttu-id="9479c-117">值</span><span class="sxs-lookup"><span data-stu-id="9479c-117">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="9479c-118">項目類型</span><span class="sxs-lookup"><span data-stu-id="9479c-118">Element Type</span></span> <br/>   | <span data-ttu-id="9479c-119">功能</span><span class="sxs-lookup"><span data-stu-id="9479c-119">Feature</span></span><br/> |
| <span data-ttu-id="9479c-120">範圍前置詞</span><span class="sxs-lookup"><span data-stu-id="9479c-120">Scoping Prefix</span></span> <br/> | <span data-ttu-id="9479c-121">頁面</span><span class="sxs-lookup"><span data-stu-id="9479c-121">Page</span></span><br/>    |
| <span data-ttu-id="9479c-122">注意</span><span class="sxs-lookup"><span data-stu-id="9479c-122">Notes</span></span> <br/>          | <span data-ttu-id="9479c-123">None</span><span class="sxs-lookup"><span data-stu-id="9479c-123">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="9479c-124">結構化內容</span><span class="sxs-lookup"><span data-stu-id="9479c-124">Structural Content</span></span>

<span data-ttu-id="9479c-125">此元素的 XML 結構為：</span><span class="sxs-lookup"><span data-stu-id="9479c-125">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="9479c-126">結構變數</span><span class="sxs-lookup"><span data-stu-id="9479c-126">Structure Variables</span></span>

<span data-ttu-id="9479c-127">下表概述 XML 結構中所定義之變數的特性。</span><span class="sxs-lookup"><span data-stu-id="9479c-127">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="9479c-128">Name</span><span class="sxs-lookup"><span data-stu-id="9479c-128">Name</span></span>                                   | <span data-ttu-id="9479c-129">資料類型</span><span class="sxs-lookup"><span data-stu-id="9479c-129">Data type</span></span>          | <span data-ttu-id="9479c-130">單位</span><span class="sxs-lookup"><span data-stu-id="9479c-130">Unit</span></span>                  | <span data-ttu-id="9479c-131">支援的值</span><span class="sxs-lookup"><span data-stu-id="9479c-131">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="9479c-132">摘要</span><span class="sxs-lookup"><span data-stu-id="9479c-132">Summary</span></span>                                                                             |
|----------------------------------------|--------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="9479c-133">\_選項名稱\_</span><span class="sxs-lookup"><span data-stu-id="9479c-133">\_OptionName\_</span></span><br/>              | <span data-ttu-id="9479c-134">string</span><span class="sxs-lookup"><span data-stu-id="9479c-134">string</span></span><br/>  | <span data-ttu-id="9479c-135">字元</span><span class="sxs-lookup"><span data-stu-id="9479c-135">characters</span></span><br/> | <span data-ttu-id="9479c-136">以 [XML 命名空間](https://www.w3.org/TR/1999/REC-xml-names-19990114/)所定義的有效完整名稱。</span><span class="sxs-lookup"><span data-stu-id="9479c-136">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="9479c-137">如果未指定命名空間，則會假設為預設命名空間。</span><span class="sxs-lookup"><span data-stu-id="9479c-137">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="9479c-138">選項的名稱。</span><span class="sxs-lookup"><span data-stu-id="9479c-138">The name of the option.</span></span><br/>                                                  |
| <span data-ttu-id="9479c-139">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="9479c-139">\_IdentityOptionValue\_</span></span><br/>     | <span data-ttu-id="9479c-140">string</span><span class="sxs-lookup"><span data-stu-id="9479c-140">string</span></span><br/>  | <span data-ttu-id="9479c-141">n/a</span><span class="sxs-lookup"><span data-stu-id="9479c-141">n/a</span></span><br/>        | <span data-ttu-id="9479c-142">True、False。</span><span class="sxs-lookup"><span data-stu-id="9479c-142">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="9479c-143">定義選項，當選取此選項時，會停用此功能。</span><span class="sxs-lookup"><span data-stu-id="9479c-143">Defines an Option which when selected would disable this feature.</span></span><br/>        |
| <span data-ttu-id="9479c-144">\_EnvelopeOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="9479c-144">\_EnvelopeOptionValue\_</span></span><br/>     | <span data-ttu-id="9479c-145">string</span><span class="sxs-lookup"><span data-stu-id="9479c-145">string</span></span><br/>  | <span data-ttu-id="9479c-146">n/a</span><span class="sxs-lookup"><span data-stu-id="9479c-146">n/a</span></span><br/>        | <span data-ttu-id="9479c-147">True、False。</span><span class="sxs-lookup"><span data-stu-id="9479c-147">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="9479c-148">定義選項，當選取此選項時，會停用此功能。</span><span class="sxs-lookup"><span data-stu-id="9479c-148">Defines an Option which when selected would disable this feature.</span></span><br/>        |
| <span data-ttu-id="9479c-149">\_BinTypeValue\_</span><span class="sxs-lookup"><span data-stu-id="9479c-149">\_BinTypeValue\_</span></span><br/>            | <span data-ttu-id="9479c-150">string</span><span class="sxs-lookup"><span data-stu-id="9479c-150">string</span></span><br/>  | <span data-ttu-id="9479c-151">n/a</span><span class="sxs-lookup"><span data-stu-id="9479c-151">n/a</span></span><br/>        | <span data-ttu-id="9479c-152">ContinuousFeed, SheetFeed.</span><span class="sxs-lookup"><span data-stu-id="9479c-152">ContinuousFeed, SheetFeed.</span></span><br/>                                                                                                                                                 | <span data-ttu-id="9479c-153">指定 bin 的類型。</span><span class="sxs-lookup"><span data-stu-id="9479c-153">Specifies the type of the bin.</span></span><br/>                                           |
| <span data-ttu-id="9479c-154">\_FeedTypeValue\_</span><span class="sxs-lookup"><span data-stu-id="9479c-154">\_FeedTypeValue\_</span></span><br/>           | <span data-ttu-id="9479c-155">string</span><span class="sxs-lookup"><span data-stu-id="9479c-155">string</span></span><br/>  | <span data-ttu-id="9479c-156">n/a</span><span class="sxs-lookup"><span data-stu-id="9479c-156">n/a</span></span><br/>        | <span data-ttu-id="9479c-157">自動、手動。</span><span class="sxs-lookup"><span data-stu-id="9479c-157">Automatic, Manual.</span></span><br/>                                                                                                                                                         | <span data-ttu-id="9479c-158">指定 bin 的摘要機制。</span><span class="sxs-lookup"><span data-stu-id="9479c-158">Specifies the feed mechanism of the bin.</span></span><br/>                                 |
| <span data-ttu-id="9479c-159">\_MediaCapacityValue\_</span><span class="sxs-lookup"><span data-stu-id="9479c-159">\_MediaCapacityValue\_</span></span><br/>      | <span data-ttu-id="9479c-160">string</span><span class="sxs-lookup"><span data-stu-id="9479c-160">string</span></span><br/>  | <span data-ttu-id="9479c-161">n/a</span><span class="sxs-lookup"><span data-stu-id="9479c-161">n/a</span></span><br/>        | <span data-ttu-id="9479c-162">高、標準。</span><span class="sxs-lookup"><span data-stu-id="9479c-162">High, Standard.</span></span><br/>                                                                                                                                                            | <span data-ttu-id="9479c-163">指定 bin 是否為高容量 bin (定性) 。</span><span class="sxs-lookup"><span data-stu-id="9479c-163">Specifies whether the bin is a high capacity bin (qualitative).</span></span><br/>          |
| <span data-ttu-id="9479c-164">\_MediaSizeAutoSenseValue\_</span><span class="sxs-lookup"><span data-stu-id="9479c-164">\_MediaSizeAutoSenseValue\_</span></span><br/> | <span data-ttu-id="9479c-165">string</span><span class="sxs-lookup"><span data-stu-id="9479c-165">string</span></span><br/>  | <span data-ttu-id="9479c-166">n/a</span><span class="sxs-lookup"><span data-stu-id="9479c-166">n/a</span></span><br/>        | <span data-ttu-id="9479c-167">支援、無。</span><span class="sxs-lookup"><span data-stu-id="9479c-167">Supported, None.</span></span><br/>                                                                                                                                                           | <span data-ttu-id="9479c-168">指定裝置的媒體大小自動感知功能。</span><span class="sxs-lookup"><span data-stu-id="9479c-168">Specifies the media size auto sense capability of device.</span></span><br/>                |
| <span data-ttu-id="9479c-169">\_MediaTypeAutoSenseValue\_</span><span class="sxs-lookup"><span data-stu-id="9479c-169">\_MediaTypeAutoSenseValue\_</span></span><br/> | <span data-ttu-id="9479c-170">string</span><span class="sxs-lookup"><span data-stu-id="9479c-170">string</span></span><br/>  | <span data-ttu-id="9479c-171">n/a</span><span class="sxs-lookup"><span data-stu-id="9479c-171">n/a</span></span><br/>        | <span data-ttu-id="9479c-172">支援、無。</span><span class="sxs-lookup"><span data-stu-id="9479c-172">Supported, None.</span></span><br/>                                                                                                                                                           | <span data-ttu-id="9479c-173">指定裝置的媒體類型自動感知功能。</span><span class="sxs-lookup"><span data-stu-id="9479c-173">Specifies the media type auto sense capability of device.</span></span><br/>                |
| <span data-ttu-id="9479c-174">\_MediaSheetCapacityValue\_</span><span class="sxs-lookup"><span data-stu-id="9479c-174">\_MediaSheetCapacityValue\_</span></span><br/> | <span data-ttu-id="9479c-175">整數</span><span class="sxs-lookup"><span data-stu-id="9479c-175">integer</span></span><br/> | <span data-ttu-id="9479c-176">床單</span><span class="sxs-lookup"><span data-stu-id="9479c-176">sheets</span></span><br/>     | <span data-ttu-id="9479c-177">裝置允許的最大整數條件約束。</span><span class="sxs-lookup"><span data-stu-id="9479c-177">Maximum integer constraint allowed by device.</span></span><br/>                                                                                                                              | <span data-ttu-id="9479c-178">以 (完整層級) 的頁面數目指定媒體容量。</span><span class="sxs-lookup"><span data-stu-id="9479c-178">Specifies the Media capacity in number of pages (full level) of the bin.</span></span><br/> |
| <span data-ttu-id="9479c-179">\_MediaPathValue\_</span><span class="sxs-lookup"><span data-stu-id="9479c-179">\_MediaPathValue\_</span></span><br/>          | <span data-ttu-id="9479c-180">string</span><span class="sxs-lookup"><span data-stu-id="9479c-180">string</span></span><br/>  | <span data-ttu-id="9479c-181">n/a</span><span class="sxs-lookup"><span data-stu-id="9479c-181">n/a</span></span><br/>        | <span data-ttu-id="9479c-182">直接、Serpentine。</span><span class="sxs-lookup"><span data-stu-id="9479c-182">Straight, Serpentine.</span></span><br/>                                                                                                                                                      | <span data-ttu-id="9479c-183">指定媒體路徑的特性。</span><span class="sxs-lookup"><span data-stu-id="9479c-183">Specifies the characteristics of the media path.</span></span><br/>                         |
| <span data-ttu-id="9479c-184">\_FeedFaceValue\_</span><span class="sxs-lookup"><span data-stu-id="9479c-184">\_FeedFaceValue\_</span></span><br/>           | <span data-ttu-id="9479c-185">string</span><span class="sxs-lookup"><span data-stu-id="9479c-185">string</span></span><br/>  | <span data-ttu-id="9479c-186">n/a</span><span class="sxs-lookup"><span data-stu-id="9479c-186">n/a</span></span><br/>        | <span data-ttu-id="9479c-187">FaceUp, FaceDown</span><span class="sxs-lookup"><span data-stu-id="9479c-187">FaceUp, FaceDown</span></span><br/>                                                                                                                                                           | <span data-ttu-id="9479c-188">指定是否要將媒體列印面朝上或朝下。</span><span class="sxs-lookup"><span data-stu-id="9479c-188">Specifies whether media is to be printed face up or face down.</span></span><br/>           |
| <span data-ttu-id="9479c-189">\_FeedDirectionValue\_</span><span class="sxs-lookup"><span data-stu-id="9479c-189">\_FeedDirectionValue\_</span></span><br/>      | <span data-ttu-id="9479c-190">string</span><span class="sxs-lookup"><span data-stu-id="9479c-190">string</span></span><br/>  | <span data-ttu-id="9479c-191">n/a</span><span class="sxs-lookup"><span data-stu-id="9479c-191">n/a</span></span><br/>        | <span data-ttu-id="9479c-192">LongEdgeFirst, ShortEdgeFirst</span><span class="sxs-lookup"><span data-stu-id="9479c-192">LongEdgeFirst, ShortEdgeFirst</span></span><br/>                                                                                                                                              | <span data-ttu-id="9479c-193">指定是否要先將媒體送入較長的第一或短邊緣。</span><span class="sxs-lookup"><span data-stu-id="9479c-193">Specifies whether media is fed long edge first or short edge first.</span></span><br/>      |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="9479c-194">可延伸標記語言 (XML)  (XML) 內容</span><span class="sxs-lookup"><span data-stu-id="9479c-194">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="9479c-195">公用列印架構關鍵字是在 https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords 命名空間中定義。</span><span class="sxs-lookup"><span data-stu-id="9479c-195">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="9479c-196">此關鍵字的 public 可延伸標記語言 (XML)  (XML) 內容定義如下：</span><span class="sxs-lookup"><span data-stu-id="9479c-196">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="9479c-197">相關主題</span><span class="sxs-lookup"><span data-stu-id="9479c-197">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9479c-198">列印架構規格</span><span class="sxs-lookup"><span data-stu-id="9479c-198">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




