---
description: 本主題並非最新的。 如需最新資訊，請參閱列印架構規格。
ms.assetid: 3e0e2cb2-cb51-446d-a6ff-f76aa8c305f6
title: PageMediaColor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 60c9a314bf435664d121fd35e588b62903da323e
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/26/2021
ms.locfileid: "107994505"
---
# <a name="pagemediacolor"></a><span data-ttu-id="11e6d-104">PageMediaColor</span><span class="sxs-lookup"><span data-stu-id="11e6d-104">PageMediaColor</span></span>

<span data-ttu-id="11e6d-105">本主題並非最新的。</span><span class="sxs-lookup"><span data-stu-id="11e6d-105">This topic is not current.</span></span> <span data-ttu-id="11e6d-106">如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。</span><span class="sxs-lookup"><span data-stu-id="11e6d-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="11e6d-107">描述媒體色彩選項以及每個選項的特性。</span><span class="sxs-lookup"><span data-stu-id="11e6d-107">Describes the Media Color options and the characteristics of each option.</span></span>

-   [<span data-ttu-id="11e6d-108">項目資訊</span><span class="sxs-lookup"><span data-stu-id="11e6d-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="11e6d-109">結構化內容</span><span class="sxs-lookup"><span data-stu-id="11e6d-109">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="11e6d-110">可延伸標記語言 (XML)  (XML) 內容</span><span class="sxs-lookup"><span data-stu-id="11e6d-110">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="11e6d-111">項目資訊</span><span class="sxs-lookup"><span data-stu-id="11e6d-111">Element Information</span></span>



| <span data-ttu-id="11e6d-112">Name</span><span class="sxs-lookup"><span data-stu-id="11e6d-112">Name</span></span> | <span data-ttu-id="11e6d-113">值</span><span class="sxs-lookup"><span data-stu-id="11e6d-113">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="11e6d-114">項目類型</span><span class="sxs-lookup"><span data-stu-id="11e6d-114">Element Type</span></span> <br/>   | <span data-ttu-id="11e6d-115">功能</span><span class="sxs-lookup"><span data-stu-id="11e6d-115">Feature</span></span><br/> |
| <span data-ttu-id="11e6d-116">範圍前置詞</span><span class="sxs-lookup"><span data-stu-id="11e6d-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="11e6d-117">頁面</span><span class="sxs-lookup"><span data-stu-id="11e6d-117">Page</span></span><br/>    |
| <span data-ttu-id="11e6d-118">注意</span><span class="sxs-lookup"><span data-stu-id="11e6d-118">Notes</span></span> <br/>          | <span data-ttu-id="11e6d-119">None</span><span class="sxs-lookup"><span data-stu-id="11e6d-119">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="11e6d-120">結構化內容</span><span class="sxs-lookup"><span data-stu-id="11e6d-120">Structural Content</span></span>

<span data-ttu-id="11e6d-121">此元素的 XML 結構為：</span><span class="sxs-lookup"><span data-stu-id="11e6d-121">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:PageMediaColor">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option name="psk:_OptionName_">
    <psf:Property name="psf:IdentityOption">
      <psf:Value xsi:type="xs:string">_IdentityOptionValue_</psf:Value>
    </psf:Property>
    <psf:ScoredProperty name="psk:MediaColorsRGB">
      <psf:Value xsi:type="xs:string">_MediaColorsRGBValue_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature>
      
```

## <a name="structure-variables"></a><span data-ttu-id="11e6d-122">結構變數</span><span class="sxs-lookup"><span data-stu-id="11e6d-122">Structure Variables</span></span>

<span data-ttu-id="11e6d-123">下表概述 XML 結構中所定義之變數的特性。</span><span class="sxs-lookup"><span data-stu-id="11e6d-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="11e6d-124">Name</span><span class="sxs-lookup"><span data-stu-id="11e6d-124">Name</span></span>                               | <span data-ttu-id="11e6d-125">資料類型</span><span class="sxs-lookup"><span data-stu-id="11e6d-125">Data type</span></span>         | <span data-ttu-id="11e6d-126">單位</span><span class="sxs-lookup"><span data-stu-id="11e6d-126">Unit</span></span>                  | <span data-ttu-id="11e6d-127">支援的值</span><span class="sxs-lookup"><span data-stu-id="11e6d-127">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="11e6d-128">總結</span><span class="sxs-lookup"><span data-stu-id="11e6d-128">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="11e6d-129">\_選項名稱\_</span><span class="sxs-lookup"><span data-stu-id="11e6d-129">\_OptionName\_</span></span><br/>          | <span data-ttu-id="11e6d-130">字串</span><span class="sxs-lookup"><span data-stu-id="11e6d-130">string</span></span><br/> | <span data-ttu-id="11e6d-131">字元</span><span class="sxs-lookup"><span data-stu-id="11e6d-131">characters</span></span><br/> | <span data-ttu-id="11e6d-132">以 [XML 命名空間](https://www.w3.org/TR/1999/REC-xml-names-19990114/)所定義的有效完整名稱。</span><span class="sxs-lookup"><span data-stu-id="11e6d-132">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="11e6d-133">如果未指定命名空間，則會假設為預設命名空間。</span><span class="sxs-lookup"><span data-stu-id="11e6d-133">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="11e6d-134">選項的名稱。</span><span class="sxs-lookup"><span data-stu-id="11e6d-134">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="11e6d-135">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="11e6d-135">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="11e6d-136">字串</span><span class="sxs-lookup"><span data-stu-id="11e6d-136">string</span></span><br/> | <span data-ttu-id="11e6d-137">n/a</span><span class="sxs-lookup"><span data-stu-id="11e6d-137">n/a</span></span><br/>        | <span data-ttu-id="11e6d-138">True、False。</span><span class="sxs-lookup"><span data-stu-id="11e6d-138">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="11e6d-139">定義選項，當選取此選項時，會停用此功能。</span><span class="sxs-lookup"><span data-stu-id="11e6d-139">Defines an Option which when selected would disable this feature.</span></span><br/> |
| <span data-ttu-id="11e6d-140">\_MediaColorsRGBValue\_</span><span class="sxs-lookup"><span data-stu-id="11e6d-140">\_MediaColorsRGBValue\_</span></span><br/> | <span data-ttu-id="11e6d-141">字串</span><span class="sxs-lookup"><span data-stu-id="11e6d-141">string</span></span><br/> | <span data-ttu-id="11e6d-142">sRGB 色彩</span><span class="sxs-lookup"><span data-stu-id="11e6d-142">sRGB Color</span></span><br/> | <span data-ttu-id="11e6d-143">\#AARRGGBB，其中 A、R、G、B 代表十六進位數位。</span><span class="sxs-lookup"><span data-stu-id="11e6d-143">\#AARRGGBB where A, R, G, B represent hexadecimal digits.</span></span><br/>                                                                                                                  | <span data-ttu-id="11e6d-144">定義實體媒體工作表的 sRGB 色彩。</span><span class="sxs-lookup"><span data-stu-id="11e6d-144">Defines the sRGB color for the physical media sheet.</span></span> <br/>             |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="11e6d-145">可延伸標記語言 (XML)  (XML) 內容</span><span class="sxs-lookup"><span data-stu-id="11e6d-145">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="11e6d-146">公用列印架構關鍵字是在 `https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords` 命名空間中定義。</span><span class="sxs-lookup"><span data-stu-id="11e6d-146">The public Print Schema keywords are defined in the `https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords` namespace.</span></span> <span data-ttu-id="11e6d-147">此關鍵字的 public 可延伸標記語言 (XML)  (XML) 內容定義如下：</span><span class="sxs-lookup"><span data-stu-id="11e6d-147">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:PageMediaColor">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option name="psk:Black">
    <psf:ScoredProperty name="psk:MediaColorsRGB">
      <psf:Value xsi:type="xs:string">#FF000000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:Blue">
    <psf:ScoredProperty name="psk:MediaColorsRGB">
      <psf:Value xsi:type="xs:string">#FF0000FF</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:Brown">
    <psf:ScoredProperty name="psk:MediaColorsRGB">
      <psf:Value xsi:type="xs:string">#FFA52A2A</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:Gold">
    <psf:ScoredProperty name="psk:MediaColorsRGB">
      <psf:Value xsi:type="xs:string">#FFFFD700</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:GoldenRod">
    <psf:ScoredProperty name="psk:MediaColorsRGB">
      <psf:Value xsi:type="xs:string">#FFDAA520</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:Gray">
    <psf:ScoredProperty name="psk:MediaColorsRGB">
      <psf:Value xsi:type="xs:string">#FF808080</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:Green">
    <psf:ScoredProperty name="psk:MediaColorsRGB">
      <psf:Value xsi:type="xs:string">#FF008000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:Ivory">
    <psf:ScoredProperty name="psk:MediaColorsRGB">
      <psf:Value xsi:type="xs:string">#FFFFFFF0</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:NoColor">
    <psf:ScoredProperty name="psk:MediaColorsRGB">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:Orange">
    <psf:ScoredProperty name="psk:MediaColorsRGB">
      <psf:Value xsi:type="xs:string">#FFFFA500</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:Pink">
    <psf:ScoredProperty name="psk:MediaColorsRGB">
      <psf:Value xsi:type="xs:string">#FFFFC0CB</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:Red">
    <psf:ScoredProperty name="psk:MediaColorsRGB">
      <psf:Value xsi:type="xs:string">#FFFF0000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:Silver">
    <psf:ScoredProperty name="psk:MediaColorsRGB">
      <psf:Value xsi:type="xs:string">#FFC0C0C0</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:Turquoise">
    <psf:ScoredProperty name="psk:MediaColorsRGB">
      <psf:Value xsi:type="xs:string">#FF40E0D0</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:Violet">
    <psf:ScoredProperty name="psk:MediaColorsRGB">
      <psf:Value xsi:type="xs:string">#FFEE82EE</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:White">
    <psf:ScoredProperty name="psk:MediaColorsRGB">
      <psf:Value xsi:type="xs:string">#FFFFFFFF</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:Yellow">
    <psf:ScoredProperty name="psk:MediaColorsRGB">
      <psf:Value xsi:type="xs:string">#FFFFFF00</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies a custom page color. -->
  <psf:Option name="psk:Custom">
    <psf:ScoredProperty name="psk:MediaColorsRGB">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature>
```

## <a name="related-topics"></a><span data-ttu-id="11e6d-148">相關主題</span><span class="sxs-lookup"><span data-stu-id="11e6d-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="11e6d-149">列印架構規格</span><span class="sxs-lookup"><span data-stu-id="11e6d-149">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>
