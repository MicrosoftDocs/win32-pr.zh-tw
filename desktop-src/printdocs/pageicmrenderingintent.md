---
description: 閱讀 PageICMRenderingIntent 使用者可設定的元素。 本主題並非最新的。 如需最新資訊，請參閱列印架構規格。
ms.assetid: df11ee89-fe62-4fe5-a1d6-0f925360ca39
title: PageICMRenderingIntent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab595bac5a7136510335167c37bc36d8a7e44056
ms.sourcegitcommit: 998d50f6def8a25850fc113fc8a2df903c829c5e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/09/2021
ms.locfileid: "113549176"
---
# <a name="pageicmrenderingintent"></a><span data-ttu-id="1f790-105">PageICMRenderingIntent</span><span class="sxs-lookup"><span data-stu-id="1f790-105">PageICMRenderingIntent</span></span>

<span data-ttu-id="1f790-106">本主題並非最新的。</span><span class="sxs-lookup"><span data-stu-id="1f790-106">This topic is not current.</span></span> <span data-ttu-id="1f790-107">如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。</span><span class="sxs-lookup"><span data-stu-id="1f790-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="1f790-108">描述 ICC v2 規格所定義的轉譯意圖。</span><span class="sxs-lookup"><span data-stu-id="1f790-108">Describes the rendering intent as defined by the ICC v2 Specification.</span></span> <span data-ttu-id="1f790-109">如果影像或圖形元素具有指定轉譯意圖的內嵌設定檔，則應該忽略此值。</span><span class="sxs-lookup"><span data-stu-id="1f790-109">This value should be ignored if an image or graphical element has an embedded profile that specifies the Rendering intent.</span></span>

-   [<span data-ttu-id="1f790-110">項目資訊</span><span class="sxs-lookup"><span data-stu-id="1f790-110">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="1f790-111">結構化內容</span><span class="sxs-lookup"><span data-stu-id="1f790-111">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="1f790-112">可延伸標記語言 (XML)  (XML) 內容</span><span class="sxs-lookup"><span data-stu-id="1f790-112">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="1f790-113">項目資訊</span><span class="sxs-lookup"><span data-stu-id="1f790-113">Element Information</span></span>



| <span data-ttu-id="1f790-114">Name</span><span class="sxs-lookup"><span data-stu-id="1f790-114">Name</span></span> | <span data-ttu-id="1f790-115">值</span><span class="sxs-lookup"><span data-stu-id="1f790-115">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="1f790-116">項目類型</span><span class="sxs-lookup"><span data-stu-id="1f790-116">Element Type</span></span> <br/>   | <span data-ttu-id="1f790-117">功能</span><span class="sxs-lookup"><span data-stu-id="1f790-117">Feature</span></span><br/> |
| <span data-ttu-id="1f790-118">範圍前置詞</span><span class="sxs-lookup"><span data-stu-id="1f790-118">Scoping Prefix</span></span> <br/> | <span data-ttu-id="1f790-119">頁面</span><span class="sxs-lookup"><span data-stu-id="1f790-119">Page</span></span><br/>    |
| <span data-ttu-id="1f790-120">注意</span><span class="sxs-lookup"><span data-stu-id="1f790-120">Notes</span></span> <br/>          | <span data-ttu-id="1f790-121">None</span><span class="sxs-lookup"><span data-stu-id="1f790-121">None</span></span> <br/>   |



 

## <a name="structural-content"></a><span data-ttu-id="1f790-122">結構化內容</span><span class="sxs-lookup"><span data-stu-id="1f790-122">Structural Content</span></span>

<span data-ttu-id="1f790-123">此元素的 XML 結構為：</span><span class="sxs-lookup"><span data-stu-id="1f790-123">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:PageICMRenderingIntent">
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

## <a name="structure-variables"></a><span data-ttu-id="1f790-124">結構變數</span><span class="sxs-lookup"><span data-stu-id="1f790-124">Structure Variables</span></span>

<span data-ttu-id="1f790-125">下表概述 XML 結構中所定義之變數的特性。</span><span class="sxs-lookup"><span data-stu-id="1f790-125">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="1f790-126">Name</span><span class="sxs-lookup"><span data-stu-id="1f790-126">Name</span></span>                               | <span data-ttu-id="1f790-127">資料類型</span><span class="sxs-lookup"><span data-stu-id="1f790-127">Data type</span></span>         | <span data-ttu-id="1f790-128">單位</span><span class="sxs-lookup"><span data-stu-id="1f790-128">Unit</span></span>                  | <span data-ttu-id="1f790-129">支援的值</span><span class="sxs-lookup"><span data-stu-id="1f790-129">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="1f790-130">摘要</span><span class="sxs-lookup"><span data-stu-id="1f790-130">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="1f790-131">\_選項名稱\_</span><span class="sxs-lookup"><span data-stu-id="1f790-131">\_OptionName\_</span></span><br/>          | <span data-ttu-id="1f790-132">string</span><span class="sxs-lookup"><span data-stu-id="1f790-132">string</span></span><br/> | <span data-ttu-id="1f790-133">字元</span><span class="sxs-lookup"><span data-stu-id="1f790-133">characters</span></span><br/> | <span data-ttu-id="1f790-134">以 [XML 命名空間](https://www.w3.org/TR/1999/REC-xml-names-19990114/)所定義的有效完整名稱。</span><span class="sxs-lookup"><span data-stu-id="1f790-134">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="1f790-135">如果未指定命名空間，則會假設為預設命名空間。</span><span class="sxs-lookup"><span data-stu-id="1f790-135">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="1f790-136">選項的名稱。</span><span class="sxs-lookup"><span data-stu-id="1f790-136">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="1f790-137">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="1f790-137">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="1f790-138">string</span><span class="sxs-lookup"><span data-stu-id="1f790-138">string</span></span><br/> | <span data-ttu-id="1f790-139">n/a</span><span class="sxs-lookup"><span data-stu-id="1f790-139">n/a</span></span><br/>        | <span data-ttu-id="1f790-140">True、False。</span><span class="sxs-lookup"><span data-stu-id="1f790-140">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="1f790-141">定義選項，當選取此選項時，會停用此功能。</span><span class="sxs-lookup"><span data-stu-id="1f790-141">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="1f790-142">可延伸標記語言 (XML)  (XML) 內容</span><span class="sxs-lookup"><span data-stu-id="1f790-142">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="1f790-143">公用列印架構關鍵字是在 https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords 命名空間中定義。</span><span class="sxs-lookup"><span data-stu-id="1f790-143">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="1f790-144">此關鍵字的 public 可延伸標記語言 (XML)  (XML) 內容定義如下：</span><span class="sxs-lookup"><span data-stu-id="1f790-144">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:PageICMRenderingIntent">
  <psf:Property name="SelectionType">
    <psf:Value xsi:type="xs:string">PickOne</psf:Value>
  </psf:Property>
  <!--Absolute Colorimetric Rendering intent-->
  <psf:Option name="psk:AbsoluteColorimetric" />
  <!--Relative Colorimetric Rendering intent -->
  <psf:Option name="psk:RelativeColorimetric" />
  <!--Photographs Rendering intent -->
  <psf:Option name="psk:Photographs" />
  <!--Business Graphics Rendering intent -->
  <psf:Option name="psk:BusinessGraphics" />
</psf:Feature>
```

## <a name="related-topics"></a><span data-ttu-id="1f790-145">相關主題</span><span class="sxs-lookup"><span data-stu-id="1f790-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1f790-146">列印架構規格</span><span class="sxs-lookup"><span data-stu-id="1f790-146">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




