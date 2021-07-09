---
description: 閱讀 PageOrientation 使用者可設定的元素。 本主題並非最新的。 如需最新資訊，請參閱列印架構規格。
ms.assetid: 52f02fc1-56fb-404d-8939-df3a4b21570d
title: PageOrientation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6f0af08fcd29f34bb55bd16b1eac50487e96ffb
ms.sourcegitcommit: 998d50f6def8a25850fc113fc8a2df903c829c5e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/09/2021
ms.locfileid: "113549116"
---
# <a name="pageorientation"></a><span data-ttu-id="27d1d-105">PageOrientation</span><span class="sxs-lookup"><span data-stu-id="27d1d-105">PageOrientation</span></span>

<span data-ttu-id="27d1d-106">本主題並非最新的。</span><span class="sxs-lookup"><span data-stu-id="27d1d-106">This topic is not current.</span></span> <span data-ttu-id="27d1d-107">如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。</span><span class="sxs-lookup"><span data-stu-id="27d1d-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="27d1d-108">描述實體媒體工作表的方向。</span><span class="sxs-lookup"><span data-stu-id="27d1d-108">Describes the orientation of the physical media sheet.</span></span>



| <span data-ttu-id="27d1d-109">選項</span><span class="sxs-lookup"><span data-stu-id="27d1d-109">Option</span></span>                       | <span data-ttu-id="27d1d-110">定義</span><span class="sxs-lookup"><span data-stu-id="27d1d-110">Definition</span></span>                                                                                              |
|------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="27d1d-111">橫向</span><span class="sxs-lookup"><span data-stu-id="27d1d-111">Landscape</span></span> <br/>        | <span data-ttu-id="27d1d-112">內容會在頁面90上旋轉？相對於標準 (直向) 方向的角度。</span><span class="sxs-lookup"><span data-stu-id="27d1d-112">Content is rotated on the page 90??degrees CCW relative to standard (portrait) orientation.</span></span><br/>  |
| <span data-ttu-id="27d1d-113">直向</span><span class="sxs-lookup"><span data-stu-id="27d1d-113">Portrait</span></span> <br/>         | <span data-ttu-id="27d1d-114">標準方向。</span><span class="sxs-lookup"><span data-stu-id="27d1d-114">Standard Orientation.</span></span><br/>                                                                        |
| <span data-ttu-id="27d1d-115">ReverseLandscape</span><span class="sxs-lookup"><span data-stu-id="27d1d-115">ReverseLandscape</span></span> <br/> | <span data-ttu-id="27d1d-116">內容會在頁面270上旋轉？相對於標準 (直向) 方向的角度。</span><span class="sxs-lookup"><span data-stu-id="27d1d-116">Content is rotated on the page 270??degrees CCW relative to standard (portrait) orientation.</span></span><br/> |
| <span data-ttu-id="27d1d-117">ReversePortrait</span><span class="sxs-lookup"><span data-stu-id="27d1d-117">ReversePortrait</span></span> <br/>  | <span data-ttu-id="27d1d-118">內容會在頁面180上旋轉？相對於標準 (縱向) 方向的度數。</span><span class="sxs-lookup"><span data-stu-id="27d1d-118">Content is rotated on the page 180??degrees relative to standard (portrait) orientation.</span></span><br/>     |



 

-   [<span data-ttu-id="27d1d-119">項目資訊</span><span class="sxs-lookup"><span data-stu-id="27d1d-119">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="27d1d-120">結構化內容</span><span class="sxs-lookup"><span data-stu-id="27d1d-120">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="27d1d-121">可延伸標記語言 (XML)  (XML) 內容</span><span class="sxs-lookup"><span data-stu-id="27d1d-121">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="27d1d-122">項目資訊</span><span class="sxs-lookup"><span data-stu-id="27d1d-122">Element Information</span></span>



| <span data-ttu-id="27d1d-123">Name</span><span class="sxs-lookup"><span data-stu-id="27d1d-123">Name</span></span> | <span data-ttu-id="27d1d-124">值</span><span class="sxs-lookup"><span data-stu-id="27d1d-124">Value</span></span> |
|----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="27d1d-125">項目類型</span><span class="sxs-lookup"><span data-stu-id="27d1d-125">Element Type</span></span> <br/>   | <span data-ttu-id="27d1d-126">功能</span><span class="sxs-lookup"><span data-stu-id="27d1d-126">Feature</span></span><br/>                                                                                                                                                                                      |
| <span data-ttu-id="27d1d-127">範圍前置詞</span><span class="sxs-lookup"><span data-stu-id="27d1d-127">Scoping Prefix</span></span> <br/> | <span data-ttu-id="27d1d-128">頁面</span><span class="sxs-lookup"><span data-stu-id="27d1d-128">Page</span></span><br/>                                                                                                                                                                                         |
| <span data-ttu-id="27d1d-129">備註</span><span class="sxs-lookup"><span data-stu-id="27d1d-129">Notes</span></span> <br/>          | <span data-ttu-id="27d1d-130">如果印表機裝置只能支援一種橫向方向，而且此方向稱為「反向橫向」，則頁面方向仍會被視為「橫向」。</span><span class="sxs-lookup"><span data-stu-id="27d1d-130">If a Printer Device can only support one landscape direction and this direction is referred to as "Reverse Landscape", then the page orientation will still be considered to be "Landscape".</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="27d1d-131">結構化內容</span><span class="sxs-lookup"><span data-stu-id="27d1d-131">Structural Content</span></span>

<span data-ttu-id="27d1d-132">此元素的 XML 結構為：</span><span class="sxs-lookup"><span data-stu-id="27d1d-132">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:PageOrientation">
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

## <a name="structure-variables"></a><span data-ttu-id="27d1d-133">結構變數</span><span class="sxs-lookup"><span data-stu-id="27d1d-133">Structure Variables</span></span>

<span data-ttu-id="27d1d-134">下表概述 XML 結構中所定義之變數的特性。</span><span class="sxs-lookup"><span data-stu-id="27d1d-134">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="27d1d-135">Name</span><span class="sxs-lookup"><span data-stu-id="27d1d-135">Name</span></span>                               | <span data-ttu-id="27d1d-136">資料類型</span><span class="sxs-lookup"><span data-stu-id="27d1d-136">Data type</span></span>         | <span data-ttu-id="27d1d-137">單位</span><span class="sxs-lookup"><span data-stu-id="27d1d-137">Unit</span></span>                  | <span data-ttu-id="27d1d-138">支援的值</span><span class="sxs-lookup"><span data-stu-id="27d1d-138">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="27d1d-139">摘要</span><span class="sxs-lookup"><span data-stu-id="27d1d-139">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="27d1d-140">\_選項名稱\_</span><span class="sxs-lookup"><span data-stu-id="27d1d-140">\_OptionName\_</span></span><br/>          | <span data-ttu-id="27d1d-141">string</span><span class="sxs-lookup"><span data-stu-id="27d1d-141">string</span></span><br/> | <span data-ttu-id="27d1d-142">字元</span><span class="sxs-lookup"><span data-stu-id="27d1d-142">characters</span></span><br/> | <span data-ttu-id="27d1d-143">以 [XML 命名空間](https://www.w3.org/TR/1999/REC-xml-names-19990114/)所定義的有效完整名稱。</span><span class="sxs-lookup"><span data-stu-id="27d1d-143">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="27d1d-144">如果未指定命名空間，則會假設為預設命名空間。</span><span class="sxs-lookup"><span data-stu-id="27d1d-144">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="27d1d-145">選項的名稱。</span><span class="sxs-lookup"><span data-stu-id="27d1d-145">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="27d1d-146">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="27d1d-146">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="27d1d-147">string</span><span class="sxs-lookup"><span data-stu-id="27d1d-147">string</span></span><br/> | <span data-ttu-id="27d1d-148">n/a</span><span class="sxs-lookup"><span data-stu-id="27d1d-148">n/a</span></span><br/>        | <span data-ttu-id="27d1d-149">True、False。</span><span class="sxs-lookup"><span data-stu-id="27d1d-149">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="27d1d-150">定義選項，當選取此選項時，會停用此功能。</span><span class="sxs-lookup"><span data-stu-id="27d1d-150">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="27d1d-151">可延伸標記語言 (XML)  (XML) 內容</span><span class="sxs-lookup"><span data-stu-id="27d1d-151">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="27d1d-152">公用列印架構關鍵字是在 https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords 命名空間中定義。</span><span class="sxs-lookup"><span data-stu-id="27d1d-152">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="27d1d-153">此關鍵字的 public 可延伸標記語言 (XML)  (XML) 內容定義如下：</span><span class="sxs-lookup"><span data-stu-id="27d1d-153">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:PageOrientation">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!-- Content is rotated on the page 90??degrees CCW relative to standard (portrait) orientation.??-->
  <psf:Option name="psk:Landscape" />
  <!-- Standard Orientation-->
  <psf:Option name="psk:Portrait" />
  <!-- Content is rotated on the page 270??degrees CCW relative to standard (portrait) orientation??-->
  <psf:Option name="psk:ReverseLandscape" />
  <!-- Content is rotated on the page 180??degrees relative to standard (portrait) orientation??-->
  <psf:Option name="psk:ReversePortrait" />
</psf:Feature>
    
```

## <a name="related-topics"></a><span data-ttu-id="27d1d-154">相關主題</span><span class="sxs-lookup"><span data-stu-id="27d1d-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="27d1d-155">列印架構規格</span><span class="sxs-lookup"><span data-stu-id="27d1d-155">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




