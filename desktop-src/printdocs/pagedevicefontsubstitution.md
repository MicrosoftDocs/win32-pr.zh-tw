---
description: 本主題並非最新的。 如需最新資訊，請參閱列印架構規格。
ms.assetid: 741aa729-35c3-43c2-93d8-e25ed508cfa6
title: PageDeviceFontSubstitution
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f40b86d6d81603e2ff9929275571ff6be72d839b
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/26/2021
ms.locfileid: "107995585"
---
# <a name="pagedevicefontsubstitution"></a><span data-ttu-id="bfa3a-104">PageDeviceFontSubstitution</span><span class="sxs-lookup"><span data-stu-id="bfa3a-104">PageDeviceFontSubstitution</span></span>

<span data-ttu-id="bfa3a-105">本主題並非最新的。</span><span class="sxs-lookup"><span data-stu-id="bfa3a-105">This topic is not current.</span></span> <span data-ttu-id="bfa3a-106">如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。</span><span class="sxs-lookup"><span data-stu-id="bfa3a-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="bfa3a-107">描述裝置字型替代的啟用/停用狀態。</span><span class="sxs-lookup"><span data-stu-id="bfa3a-107">Describes the enabled/disabled state of device font substitution.</span></span>

-   [<span data-ttu-id="bfa3a-108">項目資訊</span><span class="sxs-lookup"><span data-stu-id="bfa3a-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="bfa3a-109">結構化內容</span><span class="sxs-lookup"><span data-stu-id="bfa3a-109">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="bfa3a-110">可延伸標記語言 (XML)  (XML) 內容</span><span class="sxs-lookup"><span data-stu-id="bfa3a-110">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="bfa3a-111">項目資訊</span><span class="sxs-lookup"><span data-stu-id="bfa3a-111">Element Information</span></span>



| <span data-ttu-id="bfa3a-112">Name</span><span class="sxs-lookup"><span data-stu-id="bfa3a-112">Name</span></span> | <span data-ttu-id="bfa3a-113">值</span><span class="sxs-lookup"><span data-stu-id="bfa3a-113">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="bfa3a-114">項目類型</span><span class="sxs-lookup"><span data-stu-id="bfa3a-114">Element Type</span></span> <br/>   | <span data-ttu-id="bfa3a-115">功能</span><span class="sxs-lookup"><span data-stu-id="bfa3a-115">Feature</span></span><br/> |
| <span data-ttu-id="bfa3a-116">範圍前置詞</span><span class="sxs-lookup"><span data-stu-id="bfa3a-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="bfa3a-117">頁面</span><span class="sxs-lookup"><span data-stu-id="bfa3a-117">Page</span></span><br/>    |
| <span data-ttu-id="bfa3a-118">注意</span><span class="sxs-lookup"><span data-stu-id="bfa3a-118">Notes</span></span> <br/>          | <span data-ttu-id="bfa3a-119">None</span><span class="sxs-lookup"><span data-stu-id="bfa3a-119">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="bfa3a-120">結構化內容</span><span class="sxs-lookup"><span data-stu-id="bfa3a-120">Structural Content</span></span>

<span data-ttu-id="bfa3a-121">此元素的 XML 結構為：</span><span class="sxs-lookup"><span data-stu-id="bfa3a-121">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:PageDeviceFontSubstitution">
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

## <a name="structure-variables"></a><span data-ttu-id="bfa3a-122">結構變數</span><span class="sxs-lookup"><span data-stu-id="bfa3a-122">Structure Variables</span></span>

<span data-ttu-id="bfa3a-123">下表概述 XML 結構中所定義之變數的特性。</span><span class="sxs-lookup"><span data-stu-id="bfa3a-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="bfa3a-124">Name</span><span class="sxs-lookup"><span data-stu-id="bfa3a-124">Name</span></span>                               | <span data-ttu-id="bfa3a-125">資料類型</span><span class="sxs-lookup"><span data-stu-id="bfa3a-125">Data type</span></span>         | <span data-ttu-id="bfa3a-126">單位</span><span class="sxs-lookup"><span data-stu-id="bfa3a-126">Unit</span></span>                  | <span data-ttu-id="bfa3a-127">支援的值</span><span class="sxs-lookup"><span data-stu-id="bfa3a-127">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="bfa3a-128">總結</span><span class="sxs-lookup"><span data-stu-id="bfa3a-128">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="bfa3a-129">\_選項名稱\_</span><span class="sxs-lookup"><span data-stu-id="bfa3a-129">\_OptionName\_</span></span><br/>          | <span data-ttu-id="bfa3a-130">字串</span><span class="sxs-lookup"><span data-stu-id="bfa3a-130">string</span></span><br/> | <span data-ttu-id="bfa3a-131">字元</span><span class="sxs-lookup"><span data-stu-id="bfa3a-131">characters</span></span><br/> | <span data-ttu-id="bfa3a-132">以 [XML 命名空間](https://www.w3.org/TR/1999/REC-xml-names-19990114/)所定義的有效完整名稱。</span><span class="sxs-lookup"><span data-stu-id="bfa3a-132">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="bfa3a-133">如果未指定命名空間，則會假設為預設命名空間。</span><span class="sxs-lookup"><span data-stu-id="bfa3a-133">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="bfa3a-134">選項的名稱。</span><span class="sxs-lookup"><span data-stu-id="bfa3a-134">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="bfa3a-135">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="bfa3a-135">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="bfa3a-136">字串</span><span class="sxs-lookup"><span data-stu-id="bfa3a-136">string</span></span><br/> | <span data-ttu-id="bfa3a-137">n/a</span><span class="sxs-lookup"><span data-stu-id="bfa3a-137">n/a</span></span><br/>        | <span data-ttu-id="bfa3a-138">True、False。</span><span class="sxs-lookup"><span data-stu-id="bfa3a-138">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="bfa3a-139">定義選項，當選取此選項時，會停用此功能。</span><span class="sxs-lookup"><span data-stu-id="bfa3a-139">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="bfa3a-140">可延伸標記語言 (XML)  (XML) 內容</span><span class="sxs-lookup"><span data-stu-id="bfa3a-140">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="bfa3a-141">公用列印架構關鍵字是在 https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords 命名空間中定義。</span><span class="sxs-lookup"><span data-stu-id="bfa3a-141">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="bfa3a-142">此關鍵字的 public 可延伸標記語言 (XML)  (XML) 內容定義如下：</span><span class="sxs-lookup"><span data-stu-id="bfa3a-142">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:PageDeviceFontSubstitution">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!--Page device font substitution is off -->
  <psf:Option name="psk:Off" />
  <!--Page device font substitution is on -->
  <psf:Option name="psk:On" />
</psf:Feature>    
```

## <a name="related-topics"></a><span data-ttu-id="bfa3a-143">相關主題</span><span class="sxs-lookup"><span data-stu-id="bfa3a-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bfa3a-144">列印架構規格</span><span class="sxs-lookup"><span data-stu-id="bfa3a-144">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




