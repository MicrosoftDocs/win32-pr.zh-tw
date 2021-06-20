---
description: 深入瞭解 JobDeviceLanguage 元素，其描述從驅動程式傳送資料到實體裝置所支援的裝置語言。
ms.assetid: 3894d9fa-2bf7-447a-bac3-e72a0fdb7187
title: JobDeviceLanguage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b7bf56018a2b395ec5aa182336a89d8872057e7
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/19/2021
ms.locfileid: "112408992"
---
# <a name="jobdevicelanguage"></a><span data-ttu-id="2fe1d-103">JobDeviceLanguage</span><span class="sxs-lookup"><span data-stu-id="2fe1d-103">JobDeviceLanguage</span></span>

<span data-ttu-id="2fe1d-104">本主題並非最新的。</span><span class="sxs-lookup"><span data-stu-id="2fe1d-104">This topic is not current.</span></span> <span data-ttu-id="2fe1d-105">如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。</span><span class="sxs-lookup"><span data-stu-id="2fe1d-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="2fe1d-106">描述從驅動程式將資料傳送至實體裝置所支援的裝置語言。</span><span class="sxs-lookup"><span data-stu-id="2fe1d-106">Describes the device languages supported for sending data from driver to physical device.</span></span> <span data-ttu-id="2fe1d-107">這通常稱為「分頁描述語言」。</span><span class="sxs-lookup"><span data-stu-id="2fe1d-107">This is often called "Page Description Language".</span></span> <span data-ttu-id="2fe1d-108">此關鍵字定義驅動程式和實體裝置支援的分頁描述語言。</span><span class="sxs-lookup"><span data-stu-id="2fe1d-108">This keyword defines what page description language is supported by the driver and physical device.</span></span>

-   [<span data-ttu-id="2fe1d-109">項目資訊</span><span class="sxs-lookup"><span data-stu-id="2fe1d-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="2fe1d-110">結構化內容</span><span class="sxs-lookup"><span data-stu-id="2fe1d-110">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="2fe1d-111">可延伸標記語言 (XML)  (XML) 內容</span><span class="sxs-lookup"><span data-stu-id="2fe1d-111">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="2fe1d-112">項目資訊</span><span class="sxs-lookup"><span data-stu-id="2fe1d-112">Element Information</span></span>



| <span data-ttu-id="2fe1d-113">Name</span><span class="sxs-lookup"><span data-stu-id="2fe1d-113">Name</span></span> | <span data-ttu-id="2fe1d-114">值</span><span class="sxs-lookup"><span data-stu-id="2fe1d-114">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="2fe1d-115">項目類型</span><span class="sxs-lookup"><span data-stu-id="2fe1d-115">Element Type</span></span> <br/>   | <span data-ttu-id="2fe1d-116">功能</span><span class="sxs-lookup"><span data-stu-id="2fe1d-116">Feature</span></span><br/> |
| <span data-ttu-id="2fe1d-117">範圍前置詞</span><span class="sxs-lookup"><span data-stu-id="2fe1d-117">Scoping Prefix</span></span> <br/> | <span data-ttu-id="2fe1d-118">工作 (Job)</span><span class="sxs-lookup"><span data-stu-id="2fe1d-118">Job</span></span><br/>     |
| <span data-ttu-id="2fe1d-119">注意</span><span class="sxs-lookup"><span data-stu-id="2fe1d-119">Notes</span></span> <br/>          | <span data-ttu-id="2fe1d-120">None</span><span class="sxs-lookup"><span data-stu-id="2fe1d-120">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="2fe1d-121">結構化內容</span><span class="sxs-lookup"><span data-stu-id="2fe1d-121">Structural Content</span></span>

<span data-ttu-id="2fe1d-122">此元素的 XML 結構為：</span><span class="sxs-lookup"><span data-stu-id="2fe1d-122">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:JobDeviceLanguage">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option name="psk:_OptionName_">
    <psf:Property name="psf:IdentityOption">
      <psf:Value xsi:type="xs:string">_IdentityOptionValue_</psf:Value>
    </psf:Property>
    <psf:ScoredProperty name="psk:LanguageLevel">
      <psf:Value xsi:type="xs:string">_value_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageEncoding">
      <psf:Value xsi:type="xs:string">_LanguageEncodingValue_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageVersion">
      <psf:Value xsi:type="xs:string">_LanguageVersionValue_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature>
      
```

## <a name="structure-variables"></a><span data-ttu-id="2fe1d-123">結構變數</span><span class="sxs-lookup"><span data-stu-id="2fe1d-123">Structure Variables</span></span>

<span data-ttu-id="2fe1d-124">下表概述 XML 結構中所定義之變數的特性。</span><span class="sxs-lookup"><span data-stu-id="2fe1d-124">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="2fe1d-125">Name</span><span class="sxs-lookup"><span data-stu-id="2fe1d-125">Name</span></span>                                 | <span data-ttu-id="2fe1d-126">資料類型</span><span class="sxs-lookup"><span data-stu-id="2fe1d-126">Data type</span></span>         | <span data-ttu-id="2fe1d-127">單位</span><span class="sxs-lookup"><span data-stu-id="2fe1d-127">Unit</span></span>                  | <span data-ttu-id="2fe1d-128">支援的值</span><span class="sxs-lookup"><span data-stu-id="2fe1d-128">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="2fe1d-129">總結</span><span class="sxs-lookup"><span data-stu-id="2fe1d-129">Summary</span></span>                                                                      |
|--------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="2fe1d-130">\_選項名稱\_</span><span class="sxs-lookup"><span data-stu-id="2fe1d-130">\_OptionName\_</span></span><br/>            | <span data-ttu-id="2fe1d-131">string</span><span class="sxs-lookup"><span data-stu-id="2fe1d-131">string</span></span><br/> | <span data-ttu-id="2fe1d-132">字元</span><span class="sxs-lookup"><span data-stu-id="2fe1d-132">characters</span></span><br/> | <span data-ttu-id="2fe1d-133">以 [XML 命名空間](https://www.w3.org/TR/1999/REC-xml-names-19990114/)所定義的有效完整名稱。</span><span class="sxs-lookup"><span data-stu-id="2fe1d-133">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="2fe1d-134">如果未指定命名空間，則會假設為預設命名空間。</span><span class="sxs-lookup"><span data-stu-id="2fe1d-134">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="2fe1d-135">選項的名稱。</span><span class="sxs-lookup"><span data-stu-id="2fe1d-135">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="2fe1d-136">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="2fe1d-136">\_IdentityOptionValue\_</span></span><br/>   | <span data-ttu-id="2fe1d-137">string</span><span class="sxs-lookup"><span data-stu-id="2fe1d-137">string</span></span><br/> | <span data-ttu-id="2fe1d-138">n/a</span><span class="sxs-lookup"><span data-stu-id="2fe1d-138">n/a</span></span><br/>        | <span data-ttu-id="2fe1d-139">True、False。</span><span class="sxs-lookup"><span data-stu-id="2fe1d-139">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="2fe1d-140">定義選項，當選取此選項時，會停用此功能。</span><span class="sxs-lookup"><span data-stu-id="2fe1d-140">Defines an Option which when selected would disable this feature.</span></span><br/> |
| <span data-ttu-id="2fe1d-141">\_LanguageLevelValue\_</span><span class="sxs-lookup"><span data-stu-id="2fe1d-141">\_LanguageLevelValue\_</span></span><br/>    | <span data-ttu-id="2fe1d-142">string</span><span class="sxs-lookup"><span data-stu-id="2fe1d-142">string</span></span><br/> | <span data-ttu-id="2fe1d-143">n/a</span><span class="sxs-lookup"><span data-stu-id="2fe1d-143">n/a</span></span><br/>        | <span data-ttu-id="2fe1d-144">無。</span><span class="sxs-lookup"><span data-stu-id="2fe1d-144">None.</span></span><br/>                                                                                                                                                                      | <span data-ttu-id="2fe1d-145">指定語言層級 (例如 PS 層級 2) 。</span><span class="sxs-lookup"><span data-stu-id="2fe1d-145">Specifies the language level (for example, PS Level 2).</span></span><br/>           |
| <span data-ttu-id="2fe1d-146">\_LanguageEncodingValue\_</span><span class="sxs-lookup"><span data-stu-id="2fe1d-146">\_LanguageEncodingValue\_</span></span><br/> | <span data-ttu-id="2fe1d-147">string</span><span class="sxs-lookup"><span data-stu-id="2fe1d-147">string</span></span><br/> | <span data-ttu-id="2fe1d-148">n/a</span><span class="sxs-lookup"><span data-stu-id="2fe1d-148">n/a</span></span><br/>        | <span data-ttu-id="2fe1d-149">無。</span><span class="sxs-lookup"><span data-stu-id="2fe1d-149">None.</span></span><br/>                                                                                                                                                                      | <span data-ttu-id="2fe1d-150">指定語言編碼 (例如 ISOLatin1) 。</span><span class="sxs-lookup"><span data-stu-id="2fe1d-150">Specifies the language encoding (for example, ISOLatin1).</span></span><br/>         |
| <span data-ttu-id="2fe1d-151">\_LanguageVersionValue\_</span><span class="sxs-lookup"><span data-stu-id="2fe1d-151">\_LanguageVersionValue\_</span></span><br/>  | <span data-ttu-id="2fe1d-152">string</span><span class="sxs-lookup"><span data-stu-id="2fe1d-152">string</span></span><br/> | <span data-ttu-id="2fe1d-153">n/a</span><span class="sxs-lookup"><span data-stu-id="2fe1d-153">n/a</span></span><br/>        | <span data-ttu-id="2fe1d-154">無。</span><span class="sxs-lookup"><span data-stu-id="2fe1d-154">None.</span></span><br/>                                                                                                                                                                      | <span data-ttu-id="2fe1d-155">指定語言版本。</span><span class="sxs-lookup"><span data-stu-id="2fe1d-155">Specifies the language version.</span></span><br/>                                   |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="2fe1d-156">可延伸標記語言 (XML)  (XML) 內容</span><span class="sxs-lookup"><span data-stu-id="2fe1d-156">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="2fe1d-157">公用列印架構關鍵字是在 https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords 命名空間中定義。</span><span class="sxs-lookup"><span data-stu-id="2fe1d-157">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="2fe1d-158">此關鍵字的 public 可延伸標記語言 (XML)  (XML) 內容定義如下：</span><span class="sxs-lookup"><span data-stu-id="2fe1d-158">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:JobDeviceLanguage">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!--Specifies device language is XPS-->
  <psf:Option name="psk:XPS">
    <psf:ScoredProperty name="psk:LanguageLevel">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageEncoding">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageVersion">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!--Specifies device language is PC-PR201 -->
  <psf:Option name="psk:_201PL">
    <psf:ScoredProperty name="psk:LanguageLevel">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageEncoding">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageVersion">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!--Specified device language is ART -->
  <psf:Option name="psk:ART">
    <psf:ScoredProperty name="psk:LanguageLevel">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageEncoding">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageVersion">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!--Specified device language is ASCII -->
  <psf:Option name="psk:ASCII">
    <psf:ScoredProperty name="psk:LanguageLevel">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageEncoding">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageVersion">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!--Specified device language is CaPSL-->
  <psf:Option name="psk:CaPSL">
    <psf:ScoredProperty name="psk:LanguageLevel">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageEncoding">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageVersion">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!--Specified device language is ESC/P2-->
  <psf:Option name="psk:ESCP2">
    <psf:ScoredProperty name="psk:LanguageLevel">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageEncoding">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageVersion">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!--Specified device language is ESC/Page-->
  <psf:Option name="psk:ESCPage">
    <psf:ScoredProperty name="psk:LanguageLevel">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageEncoding">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageVersion">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!--Specified device language is HP-GL/2-->
  <psf:Option name="psk:HPGL2">
    <psf:ScoredProperty name="psk:LanguageLevel">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageEncoding">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageVersion">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!--Specified device language is KPDL -->
  <psf:Option name="psk:KPDL">
    <psf:ScoredProperty name="psk:LanguageLevel">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageEncoding">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageVersion">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!--Specified device language is KS -->
  <psf:Option name="psk:KS">
    <psf:ScoredProperty name="psk:LanguageLevel">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageEncoding">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageVersion">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!--Specified device language is KSSM -->
  <psf:Option name="psk:KSSM">
    <psf:ScoredProperty name="psk:LanguageLevel">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageEncoding">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageVersion">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!--Specified device language is PCL -->
  <psf:Option name="psk:PCL">
    <psf:ScoredProperty name="psk:LanguageLevel">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageEncoding">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageVersion">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!--Specified device language is PCL5c -->
  <psf:Option name="psk:PCL5c">
    <psf:ScoredProperty name="LanguageLevel">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageEncoding">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageVersion">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!--Specified device language is PCL5e -->
  <psf:Option name="psk:PCL5e">
    <psf:ScoredProperty name="psk:LanguageLevel">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageEncoding">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageVersion">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!--Specified device language is PCL-XL -->
  <psf:Option name="psk:PCL-XL">
    <psf:ScoredProperty name="psk:LanguageLevel">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageEncoding">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageVersion">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!--Specified device language is PostScript -->
  <psf:Option name="psk:PostScript">
    <psf:ScoredProperty name="psk:LanguageLevel">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageEncoding">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageVersion">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!--Specified device language is PPDS -->
  <psf:Option name="psk:PPDS">
    <psf:ScoredProperty name="psk:LanguageLevel">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageEncoding">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageVersion">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!--Specified device language is RPDL -->
  <psf:Option name="psk:RPDL">
    <psf:ScoredProperty name="psk:LanguageLevel">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageEncoding">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageVersion">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!--Specified device language is RTL -->
  <psf:Option name="psk:RTL">
    <psf:ScoredProperty name="psk:LanguageLevel">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageEncoding">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageVersion">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature>    
```

## <a name="related-topics"></a><span data-ttu-id="2fe1d-159">相關主題</span><span class="sxs-lookup"><span data-stu-id="2fe1d-159">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2fe1d-160">列印架構規格</span><span class="sxs-lookup"><span data-stu-id="2fe1d-160">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




