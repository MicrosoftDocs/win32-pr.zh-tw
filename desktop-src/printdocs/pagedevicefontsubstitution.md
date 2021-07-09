---
description: 檢查 PageDeviceFontSubstitution 使用者可設定的元素。 本主題並非最新的。 如需最新資訊，請參閱列印架構規格。
ms.assetid: 741aa729-35c3-43c2-93d8-e25ed508cfa6
title: PageDeviceFontSubstitution
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4dc5650c687a4c96e6c54ef7ea0631e77407e874
ms.sourcegitcommit: 998d50f6def8a25850fc113fc8a2df903c829c5e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/09/2021
ms.locfileid: "113549196"
---
# <a name="pagedevicefontsubstitution"></a><span data-ttu-id="e1688-105">PageDeviceFontSubstitution</span><span class="sxs-lookup"><span data-stu-id="e1688-105">PageDeviceFontSubstitution</span></span>

<span data-ttu-id="e1688-106">本主題並非最新的。</span><span class="sxs-lookup"><span data-stu-id="e1688-106">This topic is not current.</span></span> <span data-ttu-id="e1688-107">如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。</span><span class="sxs-lookup"><span data-stu-id="e1688-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="e1688-108">描述裝置字型替代的啟用/停用狀態。</span><span class="sxs-lookup"><span data-stu-id="e1688-108">Describes the enabled/disabled state of device font substitution.</span></span>

-   [<span data-ttu-id="e1688-109">項目資訊</span><span class="sxs-lookup"><span data-stu-id="e1688-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="e1688-110">結構化內容</span><span class="sxs-lookup"><span data-stu-id="e1688-110">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="e1688-111">可延伸標記語言 (XML)  (XML) 內容</span><span class="sxs-lookup"><span data-stu-id="e1688-111">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="e1688-112">項目資訊</span><span class="sxs-lookup"><span data-stu-id="e1688-112">Element Information</span></span>



| <span data-ttu-id="e1688-113">Name</span><span class="sxs-lookup"><span data-stu-id="e1688-113">Name</span></span> | <span data-ttu-id="e1688-114">值</span><span class="sxs-lookup"><span data-stu-id="e1688-114">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="e1688-115">項目類型</span><span class="sxs-lookup"><span data-stu-id="e1688-115">Element Type</span></span> <br/>   | <span data-ttu-id="e1688-116">功能</span><span class="sxs-lookup"><span data-stu-id="e1688-116">Feature</span></span><br/> |
| <span data-ttu-id="e1688-117">範圍前置詞</span><span class="sxs-lookup"><span data-stu-id="e1688-117">Scoping Prefix</span></span> <br/> | <span data-ttu-id="e1688-118">頁面</span><span class="sxs-lookup"><span data-stu-id="e1688-118">Page</span></span><br/>    |
| <span data-ttu-id="e1688-119">注意</span><span class="sxs-lookup"><span data-stu-id="e1688-119">Notes</span></span> <br/>          | <span data-ttu-id="e1688-120">None</span><span class="sxs-lookup"><span data-stu-id="e1688-120">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="e1688-121">結構化內容</span><span class="sxs-lookup"><span data-stu-id="e1688-121">Structural Content</span></span>

<span data-ttu-id="e1688-122">此元素的 XML 結構為：</span><span class="sxs-lookup"><span data-stu-id="e1688-122">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="e1688-123">結構變數</span><span class="sxs-lookup"><span data-stu-id="e1688-123">Structure Variables</span></span>

<span data-ttu-id="e1688-124">下表概述 XML 結構中所定義之變數的特性。</span><span class="sxs-lookup"><span data-stu-id="e1688-124">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="e1688-125">Name</span><span class="sxs-lookup"><span data-stu-id="e1688-125">Name</span></span>                               | <span data-ttu-id="e1688-126">資料類型</span><span class="sxs-lookup"><span data-stu-id="e1688-126">Data type</span></span>         | <span data-ttu-id="e1688-127">單位</span><span class="sxs-lookup"><span data-stu-id="e1688-127">Unit</span></span>                  | <span data-ttu-id="e1688-128">支援的值</span><span class="sxs-lookup"><span data-stu-id="e1688-128">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="e1688-129">摘要</span><span class="sxs-lookup"><span data-stu-id="e1688-129">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="e1688-130">\_選項名稱\_</span><span class="sxs-lookup"><span data-stu-id="e1688-130">\_OptionName\_</span></span><br/>          | <span data-ttu-id="e1688-131">string</span><span class="sxs-lookup"><span data-stu-id="e1688-131">string</span></span><br/> | <span data-ttu-id="e1688-132">字元</span><span class="sxs-lookup"><span data-stu-id="e1688-132">characters</span></span><br/> | <span data-ttu-id="e1688-133">以 [XML 命名空間](https://www.w3.org/TR/1999/REC-xml-names-19990114/)所定義的有效完整名稱。</span><span class="sxs-lookup"><span data-stu-id="e1688-133">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="e1688-134">如果未指定命名空間，則會假設為預設命名空間。</span><span class="sxs-lookup"><span data-stu-id="e1688-134">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="e1688-135">選項的名稱。</span><span class="sxs-lookup"><span data-stu-id="e1688-135">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="e1688-136">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="e1688-136">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="e1688-137">string</span><span class="sxs-lookup"><span data-stu-id="e1688-137">string</span></span><br/> | <span data-ttu-id="e1688-138">n/a</span><span class="sxs-lookup"><span data-stu-id="e1688-138">n/a</span></span><br/>        | <span data-ttu-id="e1688-139">True、False。</span><span class="sxs-lookup"><span data-stu-id="e1688-139">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="e1688-140">定義選項，當選取此選項時，會停用此功能。</span><span class="sxs-lookup"><span data-stu-id="e1688-140">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="e1688-141">可延伸標記語言 (XML)  (XML) 內容</span><span class="sxs-lookup"><span data-stu-id="e1688-141">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="e1688-142">公用列印架構關鍵字是在 https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords 命名空間中定義。</span><span class="sxs-lookup"><span data-stu-id="e1688-142">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="e1688-143">此關鍵字的 public 可延伸標記語言 (XML)  (XML) 內容定義如下：</span><span class="sxs-lookup"><span data-stu-id="e1688-143">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="e1688-144">相關主題</span><span class="sxs-lookup"><span data-stu-id="e1688-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e1688-145">列印架構規格</span><span class="sxs-lookup"><span data-stu-id="e1688-145">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




