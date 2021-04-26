---
description: 本主題並非最新的。 如需最新資訊，請參閱列印架構規格。
ms.assetid: 52f02fc1-56fb-404d-8939-df3a4b21570d
title: PageOrientation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01a94fb97ad1e64c7f55fd9520ed8a648a74f550
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/26/2021
ms.locfileid: "107997535"
---
# <a name="pageorientation"></a><span data-ttu-id="3f0f0-104">PageOrientation</span><span class="sxs-lookup"><span data-stu-id="3f0f0-104">PageOrientation</span></span>

<span data-ttu-id="3f0f0-105">本主題並非最新的。</span><span class="sxs-lookup"><span data-stu-id="3f0f0-105">This topic is not current.</span></span> <span data-ttu-id="3f0f0-106">如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。</span><span class="sxs-lookup"><span data-stu-id="3f0f0-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="3f0f0-107">描述實體媒體工作表的方向。</span><span class="sxs-lookup"><span data-stu-id="3f0f0-107">Describes the orientation of the physical media sheet.</span></span>



| <span data-ttu-id="3f0f0-108">選項</span><span class="sxs-lookup"><span data-stu-id="3f0f0-108">Option</span></span>                       | <span data-ttu-id="3f0f0-109">定義</span><span class="sxs-lookup"><span data-stu-id="3f0f0-109">Definition</span></span>                                                                                              |
|------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3f0f0-110">橫向</span><span class="sxs-lookup"><span data-stu-id="3f0f0-110">Landscape</span></span> <br/>        | <span data-ttu-id="3f0f0-111">內容會在頁面90上旋轉？相對於標準 (直向) 方向的角度。</span><span class="sxs-lookup"><span data-stu-id="3f0f0-111">Content is rotated on the page 90??degrees CCW relative to standard (portrait) orientation.</span></span><br/>  |
| <span data-ttu-id="3f0f0-112">直向</span><span class="sxs-lookup"><span data-stu-id="3f0f0-112">Portrait</span></span> <br/>         | <span data-ttu-id="3f0f0-113">標準方向。</span><span class="sxs-lookup"><span data-stu-id="3f0f0-113">Standard Orientation.</span></span><br/>                                                                        |
| <span data-ttu-id="3f0f0-114">ReverseLandscape</span><span class="sxs-lookup"><span data-stu-id="3f0f0-114">ReverseLandscape</span></span> <br/> | <span data-ttu-id="3f0f0-115">內容會在頁面270上旋轉？相對於標準 (直向) 方向的角度。</span><span class="sxs-lookup"><span data-stu-id="3f0f0-115">Content is rotated on the page 270??degrees CCW relative to standard (portrait) orientation.</span></span><br/> |
| <span data-ttu-id="3f0f0-116">ReversePortrait</span><span class="sxs-lookup"><span data-stu-id="3f0f0-116">ReversePortrait</span></span> <br/>  | <span data-ttu-id="3f0f0-117">內容會在頁面180上旋轉？相對於標準 (縱向) 方向的度數。</span><span class="sxs-lookup"><span data-stu-id="3f0f0-117">Content is rotated on the page 180??degrees relative to standard (portrait) orientation.</span></span><br/>     |



 

-   [<span data-ttu-id="3f0f0-118">項目資訊</span><span class="sxs-lookup"><span data-stu-id="3f0f0-118">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="3f0f0-119">結構化內容</span><span class="sxs-lookup"><span data-stu-id="3f0f0-119">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="3f0f0-120">可延伸標記語言 (XML)  (XML) 內容</span><span class="sxs-lookup"><span data-stu-id="3f0f0-120">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="3f0f0-121">項目資訊</span><span class="sxs-lookup"><span data-stu-id="3f0f0-121">Element Information</span></span>



| <span data-ttu-id="3f0f0-122">Name</span><span class="sxs-lookup"><span data-stu-id="3f0f0-122">Name</span></span> | <span data-ttu-id="3f0f0-123">值</span><span class="sxs-lookup"><span data-stu-id="3f0f0-123">Value</span></span> |
|----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3f0f0-124">項目類型</span><span class="sxs-lookup"><span data-stu-id="3f0f0-124">Element Type</span></span> <br/>   | <span data-ttu-id="3f0f0-125">功能</span><span class="sxs-lookup"><span data-stu-id="3f0f0-125">Feature</span></span><br/>                                                                                                                                                                                      |
| <span data-ttu-id="3f0f0-126">範圍前置詞</span><span class="sxs-lookup"><span data-stu-id="3f0f0-126">Scoping Prefix</span></span> <br/> | <span data-ttu-id="3f0f0-127">頁面</span><span class="sxs-lookup"><span data-stu-id="3f0f0-127">Page</span></span><br/>                                                                                                                                                                                         |
| <span data-ttu-id="3f0f0-128">備註</span><span class="sxs-lookup"><span data-stu-id="3f0f0-128">Notes</span></span> <br/>          | <span data-ttu-id="3f0f0-129">如果印表機裝置只能支援一種橫向方向，而且此方向稱為「反向橫向」，則頁面方向仍會被視為「橫向」。</span><span class="sxs-lookup"><span data-stu-id="3f0f0-129">If a Printer Device can only support one landscape direction and this direction is referred to as "Reverse Landscape", then the page orientation will still be considered to be "Landscape".</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="3f0f0-130">結構化內容</span><span class="sxs-lookup"><span data-stu-id="3f0f0-130">Structural Content</span></span>

<span data-ttu-id="3f0f0-131">此元素的 XML 結構為：</span><span class="sxs-lookup"><span data-stu-id="3f0f0-131">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="3f0f0-132">結構變數</span><span class="sxs-lookup"><span data-stu-id="3f0f0-132">Structure Variables</span></span>

<span data-ttu-id="3f0f0-133">下表概述 XML 結構中所定義之變數的特性。</span><span class="sxs-lookup"><span data-stu-id="3f0f0-133">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="3f0f0-134">Name</span><span class="sxs-lookup"><span data-stu-id="3f0f0-134">Name</span></span>                               | <span data-ttu-id="3f0f0-135">資料類型</span><span class="sxs-lookup"><span data-stu-id="3f0f0-135">Data type</span></span>         | <span data-ttu-id="3f0f0-136">單位</span><span class="sxs-lookup"><span data-stu-id="3f0f0-136">Unit</span></span>                  | <span data-ttu-id="3f0f0-137">支援的值</span><span class="sxs-lookup"><span data-stu-id="3f0f0-137">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="3f0f0-138">總結</span><span class="sxs-lookup"><span data-stu-id="3f0f0-138">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="3f0f0-139">\_選項名稱\_</span><span class="sxs-lookup"><span data-stu-id="3f0f0-139">\_OptionName\_</span></span><br/>          | <span data-ttu-id="3f0f0-140">字串</span><span class="sxs-lookup"><span data-stu-id="3f0f0-140">string</span></span><br/> | <span data-ttu-id="3f0f0-141">字元</span><span class="sxs-lookup"><span data-stu-id="3f0f0-141">characters</span></span><br/> | <span data-ttu-id="3f0f0-142">以 [XML 命名空間](https://www.w3.org/TR/1999/REC-xml-names-19990114/)所定義的有效完整名稱。</span><span class="sxs-lookup"><span data-stu-id="3f0f0-142">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="3f0f0-143">如果未指定命名空間，則會假設為預設命名空間。</span><span class="sxs-lookup"><span data-stu-id="3f0f0-143">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="3f0f0-144">選項的名稱。</span><span class="sxs-lookup"><span data-stu-id="3f0f0-144">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="3f0f0-145">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="3f0f0-145">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="3f0f0-146">字串</span><span class="sxs-lookup"><span data-stu-id="3f0f0-146">string</span></span><br/> | <span data-ttu-id="3f0f0-147">n/a</span><span class="sxs-lookup"><span data-stu-id="3f0f0-147">n/a</span></span><br/>        | <span data-ttu-id="3f0f0-148">True、False。</span><span class="sxs-lookup"><span data-stu-id="3f0f0-148">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="3f0f0-149">定義選項，當選取此選項時，會停用此功能。</span><span class="sxs-lookup"><span data-stu-id="3f0f0-149">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="3f0f0-150">可延伸標記語言 (XML)  (XML) 內容</span><span class="sxs-lookup"><span data-stu-id="3f0f0-150">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="3f0f0-151">公用列印架構關鍵字是在 https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords 命名空間中定義。</span><span class="sxs-lookup"><span data-stu-id="3f0f0-151">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="3f0f0-152">此關鍵字的 public 可延伸標記語言 (XML)  (XML) 內容定義如下：</span><span class="sxs-lookup"><span data-stu-id="3f0f0-152">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="3f0f0-153">相關主題</span><span class="sxs-lookup"><span data-stu-id="3f0f0-153">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3f0f0-154">列印架構規格</span><span class="sxs-lookup"><span data-stu-id="3f0f0-154">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




