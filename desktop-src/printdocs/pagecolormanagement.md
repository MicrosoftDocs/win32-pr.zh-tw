---
description: 深入瞭解 PageColorManagement 使用者可設定的元素。 本主題並非最新的。 如需最新資訊，請參閱列印架構規格。
ms.assetid: 27408582-9c39-4d39-8314-a495d1c7766d
title: PageColorManagement
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 685794f1c9bb64c8bb3e966c4ec03bcac8821369
ms.sourcegitcommit: 998d50f6def8a25850fc113fc8a2df903c829c5e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/09/2021
ms.locfileid: "113549226"
---
# <a name="pagecolormanagement"></a><span data-ttu-id="9c5f6-105">PageColorManagement</span><span class="sxs-lookup"><span data-stu-id="9c5f6-105">PageColorManagement</span></span>

<span data-ttu-id="9c5f6-106">本主題並非最新的。</span><span class="sxs-lookup"><span data-stu-id="9c5f6-106">This topic is not current.</span></span> <span data-ttu-id="9c5f6-107">如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。</span><span class="sxs-lookup"><span data-stu-id="9c5f6-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="9c5f6-108">設定目前頁面的色彩管理。</span><span class="sxs-lookup"><span data-stu-id="9c5f6-108">Configures color management for the current page.</span></span> <span data-ttu-id="9c5f6-109">在填充碼 DM ICMMethod 新增系統中，這會被視為自動 \_ 。</span><span class="sxs-lookup"><span data-stu-id="9c5f6-109">This is considered automatic in SHIM - DM\_ICMMethod Add System.</span></span> <span data-ttu-id="9c5f6-110">描述哪個元件應該執行色彩管理 (例如驅動程式) 。</span><span class="sxs-lookup"><span data-stu-id="9c5f6-110">Describes what component should perform color management (i.e. Driver).</span></span>

-   [<span data-ttu-id="9c5f6-111">項目資訊</span><span class="sxs-lookup"><span data-stu-id="9c5f6-111">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="9c5f6-112">結構化內容</span><span class="sxs-lookup"><span data-stu-id="9c5f6-112">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="9c5f6-113">可延伸標記語言 (XML)  (XML) 內容</span><span class="sxs-lookup"><span data-stu-id="9c5f6-113">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="9c5f6-114">項目資訊</span><span class="sxs-lookup"><span data-stu-id="9c5f6-114">Element Information</span></span>



| <span data-ttu-id="9c5f6-115">Name</span><span class="sxs-lookup"><span data-stu-id="9c5f6-115">Name</span></span> | <span data-ttu-id="9c5f6-116">值</span><span class="sxs-lookup"><span data-stu-id="9c5f6-116">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="9c5f6-117">項目類型</span><span class="sxs-lookup"><span data-stu-id="9c5f6-117">Element Type</span></span> <br/>   | <span data-ttu-id="9c5f6-118">功能</span><span class="sxs-lookup"><span data-stu-id="9c5f6-118">Feature</span></span><br/> |
| <span data-ttu-id="9c5f6-119">範圍前置詞</span><span class="sxs-lookup"><span data-stu-id="9c5f6-119">Scoping Prefix</span></span> <br/> | <span data-ttu-id="9c5f6-120">頁面</span><span class="sxs-lookup"><span data-stu-id="9c5f6-120">Page</span></span><br/>    |
| <span data-ttu-id="9c5f6-121">注意</span><span class="sxs-lookup"><span data-stu-id="9c5f6-121">Notes</span></span> <br/>          | <span data-ttu-id="9c5f6-122">None</span><span class="sxs-lookup"><span data-stu-id="9c5f6-122">None</span></span> <br/>   |



 

## <a name="structural-content"></a><span data-ttu-id="9c5f6-123">結構化內容</span><span class="sxs-lookup"><span data-stu-id="9c5f6-123">Structural Content</span></span>

<span data-ttu-id="9c5f6-124">此元素的 XML 結構為：</span><span class="sxs-lookup"><span data-stu-id="9c5f6-124">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:PageColorManagement">
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

## <a name="structure-variables"></a><span data-ttu-id="9c5f6-125">結構變數</span><span class="sxs-lookup"><span data-stu-id="9c5f6-125">Structure Variables</span></span>

<span data-ttu-id="9c5f6-126">下表概述 XML 結構中所定義之變數的特性。</span><span class="sxs-lookup"><span data-stu-id="9c5f6-126">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="9c5f6-127">Name</span><span class="sxs-lookup"><span data-stu-id="9c5f6-127">Name</span></span>                               | <span data-ttu-id="9c5f6-128">資料類型</span><span class="sxs-lookup"><span data-stu-id="9c5f6-128">Data type</span></span>         | <span data-ttu-id="9c5f6-129">單位</span><span class="sxs-lookup"><span data-stu-id="9c5f6-129">Unit</span></span>                  | <span data-ttu-id="9c5f6-130">支援的值</span><span class="sxs-lookup"><span data-stu-id="9c5f6-130">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="9c5f6-131">摘要</span><span class="sxs-lookup"><span data-stu-id="9c5f6-131">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="9c5f6-132">\_選項名稱\_</span><span class="sxs-lookup"><span data-stu-id="9c5f6-132">\_OptionName\_</span></span><br/>          | <span data-ttu-id="9c5f6-133">string</span><span class="sxs-lookup"><span data-stu-id="9c5f6-133">string</span></span><br/> | <span data-ttu-id="9c5f6-134">字元</span><span class="sxs-lookup"><span data-stu-id="9c5f6-134">characters</span></span><br/> | <span data-ttu-id="9c5f6-135">以 [XML 命名空間](https://www.w3.org/TR/1999/REC-xml-names-19990114/)所定義的有效完整名稱。</span><span class="sxs-lookup"><span data-stu-id="9c5f6-135">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="9c5f6-136">如果未指定命名空間，則會假設為預設命名空間。</span><span class="sxs-lookup"><span data-stu-id="9c5f6-136">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="9c5f6-137">選項的名稱。</span><span class="sxs-lookup"><span data-stu-id="9c5f6-137">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="9c5f6-138">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="9c5f6-138">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="9c5f6-139">string</span><span class="sxs-lookup"><span data-stu-id="9c5f6-139">string</span></span><br/> | <span data-ttu-id="9c5f6-140">n/a</span><span class="sxs-lookup"><span data-stu-id="9c5f6-140">n/a</span></span><br/>        | <span data-ttu-id="9c5f6-141">True、False。</span><span class="sxs-lookup"><span data-stu-id="9c5f6-141">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="9c5f6-142">定義選項，當選取此選項時，會停用此功能。</span><span class="sxs-lookup"><span data-stu-id="9c5f6-142">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="9c5f6-143">可延伸標記語言 (XML)  (XML) 內容</span><span class="sxs-lookup"><span data-stu-id="9c5f6-143">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="9c5f6-144">公用列印架構關鍵字是在 https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords 命名空間中定義。</span><span class="sxs-lookup"><span data-stu-id="9c5f6-144">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="9c5f6-145">此關鍵字的 public 可延伸標記語言 (XML)  (XML) 內容定義如下：</span><span class="sxs-lookup"><span data-stu-id="9c5f6-145">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:PageColorManagement">
  <psf:Property name="SelectionType">
    <psf:Value xsi:type="xs:string">PickOne</psf:Value>
  </psf:Property>
  <!-- Application has performed color management to the destination profile. -->
  <psf:Option name="psk:None" />
  <!--  Application has not performed color management and the device determines color management.-->
  <psf:Option name="psk:Device" />
  <!--  Application has not performed color management and the driver determines color management.-->
  <psf:Option name="psk:Driver" />
  <!--Color management is performed by the system. Not to be used when printing to XPSDrv print drivers -->
  <psf:Option name="psk:System" />
</psf:Feature>
```

## <a name="related-topics"></a><span data-ttu-id="9c5f6-146">相關主題</span><span class="sxs-lookup"><span data-stu-id="9c5f6-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9c5f6-147">列印架構規格</span><span class="sxs-lookup"><span data-stu-id="9c5f6-147">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




