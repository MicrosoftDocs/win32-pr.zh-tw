---
description: 本主題並非最新的。 如需最新資訊，請參閱列印架構規格。
ms.assetid: 741aa729-35c3-43c2-93d8-e25ed508cfa6
title: PageDeviceFontSubstitution
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08d076d9175f078efed9dbd8d5ae0b59cf296142
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/06/2021
ms.locfileid: "104514385"
---
# <a name="pagedevicefontsubstitution"></a><span data-ttu-id="100d4-104">PageDeviceFontSubstitution</span><span class="sxs-lookup"><span data-stu-id="100d4-104">PageDeviceFontSubstitution</span></span>

<span data-ttu-id="100d4-105">本主題並非最新的。</span><span class="sxs-lookup"><span data-stu-id="100d4-105">This topic is not current.</span></span> <span data-ttu-id="100d4-106">如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。</span><span class="sxs-lookup"><span data-stu-id="100d4-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="100d4-107">描述裝置字型替代的啟用/停用狀態。</span><span class="sxs-lookup"><span data-stu-id="100d4-107">Describes the enabled/disabled state of device font substitution.</span></span>

-   [<span data-ttu-id="100d4-108">項目資訊</span><span class="sxs-lookup"><span data-stu-id="100d4-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="100d4-109">結構化內容</span><span class="sxs-lookup"><span data-stu-id="100d4-109">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="100d4-110">可延伸標記語言 (XML)  (XML) 內容</span><span class="sxs-lookup"><span data-stu-id="100d4-110">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="100d4-111">項目資訊</span><span class="sxs-lookup"><span data-stu-id="100d4-111">Element Information</span></span>



| <span data-ttu-id="100d4-112">Name</span><span class="sxs-lookup"><span data-stu-id="100d4-112">Name</span></span>                       |                    |
|----------------------------|--------------------|
| <span data-ttu-id="100d4-113">項目類型</span><span class="sxs-lookup"><span data-stu-id="100d4-113">Element Type</span></span> <br/>   | <span data-ttu-id="100d4-114">功能</span><span class="sxs-lookup"><span data-stu-id="100d4-114">Feature</span></span><br/> |
| <span data-ttu-id="100d4-115">範圍前置詞</span><span class="sxs-lookup"><span data-stu-id="100d4-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="100d4-116">頁面</span><span class="sxs-lookup"><span data-stu-id="100d4-116">Page</span></span><br/>    |
| <span data-ttu-id="100d4-117">注意</span><span class="sxs-lookup"><span data-stu-id="100d4-117">Notes</span></span> <br/>          | <span data-ttu-id="100d4-118">None</span><span class="sxs-lookup"><span data-stu-id="100d4-118">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="100d4-119">結構化內容</span><span class="sxs-lookup"><span data-stu-id="100d4-119">Structural Content</span></span>

<span data-ttu-id="100d4-120">此元素的 XML 結構為：</span><span class="sxs-lookup"><span data-stu-id="100d4-120">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="100d4-121">結構變數</span><span class="sxs-lookup"><span data-stu-id="100d4-121">Structure Variables</span></span>

<span data-ttu-id="100d4-122">下表概述 XML 結構中所定義之變數的特性。</span><span class="sxs-lookup"><span data-stu-id="100d4-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="100d4-123">Name</span><span class="sxs-lookup"><span data-stu-id="100d4-123">Name</span></span>                               | <span data-ttu-id="100d4-124">資料類型</span><span class="sxs-lookup"><span data-stu-id="100d4-124">Data type</span></span>         | <span data-ttu-id="100d4-125">單位</span><span class="sxs-lookup"><span data-stu-id="100d4-125">Unit</span></span>                  | <span data-ttu-id="100d4-126">支援的值</span><span class="sxs-lookup"><span data-stu-id="100d4-126">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="100d4-127">總結</span><span class="sxs-lookup"><span data-stu-id="100d4-127">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="100d4-128">\_選項名稱\_</span><span class="sxs-lookup"><span data-stu-id="100d4-128">\_OptionName\_</span></span><br/>          | <span data-ttu-id="100d4-129">字串</span><span class="sxs-lookup"><span data-stu-id="100d4-129">string</span></span><br/> | <span data-ttu-id="100d4-130">字元</span><span class="sxs-lookup"><span data-stu-id="100d4-130">characters</span></span><br/> | <span data-ttu-id="100d4-131">以 [XML 命名空間](https://www.w3.org/TR/1999/REC-xml-names-19990114/)所定義的有效完整名稱。</span><span class="sxs-lookup"><span data-stu-id="100d4-131">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="100d4-132">如果未指定命名空間，則會假設為預設命名空間。</span><span class="sxs-lookup"><span data-stu-id="100d4-132">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="100d4-133">選項的名稱。</span><span class="sxs-lookup"><span data-stu-id="100d4-133">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="100d4-134">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="100d4-134">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="100d4-135">字串</span><span class="sxs-lookup"><span data-stu-id="100d4-135">string</span></span><br/> | <span data-ttu-id="100d4-136">n/a</span><span class="sxs-lookup"><span data-stu-id="100d4-136">n/a</span></span><br/>        | <span data-ttu-id="100d4-137">True、False。</span><span class="sxs-lookup"><span data-stu-id="100d4-137">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="100d4-138">定義選項，當選取此選項時，會停用此功能。</span><span class="sxs-lookup"><span data-stu-id="100d4-138">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="100d4-139">可延伸標記語言 (XML)  (XML) 內容</span><span class="sxs-lookup"><span data-stu-id="100d4-139">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="100d4-140">公用列印架構關鍵字是在 https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords 命名空間中定義。</span><span class="sxs-lookup"><span data-stu-id="100d4-140">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="100d4-141">此關鍵字的 public 可延伸標記語言 (XML)  (XML) 內容定義如下：</span><span class="sxs-lookup"><span data-stu-id="100d4-141">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="100d4-142">相關主題</span><span class="sxs-lookup"><span data-stu-id="100d4-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="100d4-143">列印架構規格</span><span class="sxs-lookup"><span data-stu-id="100d4-143">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




