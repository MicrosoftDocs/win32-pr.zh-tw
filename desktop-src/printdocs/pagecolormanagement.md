---
description: 本主題並非最新的。 如需最新資訊，請參閱列印架構規格。
ms.assetid: 27408582-9c39-4d39-8314-a495d1c7766d
title: PageColorManagement
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83ae8d161035d23149759345e8eb139dd3fb7a48
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/06/2021
ms.locfileid: "107000535"
---
# <a name="pagecolormanagement"></a><span data-ttu-id="4c3c2-104">PageColorManagement</span><span class="sxs-lookup"><span data-stu-id="4c3c2-104">PageColorManagement</span></span>

<span data-ttu-id="4c3c2-105">本主題並非最新的。</span><span class="sxs-lookup"><span data-stu-id="4c3c2-105">This topic is not current.</span></span> <span data-ttu-id="4c3c2-106">如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。</span><span class="sxs-lookup"><span data-stu-id="4c3c2-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="4c3c2-107">設定目前頁面的色彩管理。</span><span class="sxs-lookup"><span data-stu-id="4c3c2-107">Configures color management for the current page.</span></span> <span data-ttu-id="4c3c2-108">在填充碼 DM ICMMethod 新增系統中，這會被視為自動 \_ 。</span><span class="sxs-lookup"><span data-stu-id="4c3c2-108">This is considered automatic in SHIM - DM\_ICMMethod Add System.</span></span> <span data-ttu-id="4c3c2-109">描述哪個元件應該執行色彩管理 (例如驅動程式) 。</span><span class="sxs-lookup"><span data-stu-id="4c3c2-109">Describes what component should perform color management (i.e. Driver).</span></span>

-   [<span data-ttu-id="4c3c2-110">項目資訊</span><span class="sxs-lookup"><span data-stu-id="4c3c2-110">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="4c3c2-111">結構化內容</span><span class="sxs-lookup"><span data-stu-id="4c3c2-111">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="4c3c2-112">可延伸標記語言 (XML)  (XML) 內容</span><span class="sxs-lookup"><span data-stu-id="4c3c2-112">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="4c3c2-113">項目資訊</span><span class="sxs-lookup"><span data-stu-id="4c3c2-113">Element Information</span></span>



| <span data-ttu-id="4c3c2-114">Name</span><span class="sxs-lookup"><span data-stu-id="4c3c2-114">Name</span></span>                       |                    |
|----------------------------|--------------------|
| <span data-ttu-id="4c3c2-115">項目類型</span><span class="sxs-lookup"><span data-stu-id="4c3c2-115">Element Type</span></span> <br/>   | <span data-ttu-id="4c3c2-116">功能</span><span class="sxs-lookup"><span data-stu-id="4c3c2-116">Feature</span></span><br/> |
| <span data-ttu-id="4c3c2-117">範圍前置詞</span><span class="sxs-lookup"><span data-stu-id="4c3c2-117">Scoping Prefix</span></span> <br/> | <span data-ttu-id="4c3c2-118">頁面</span><span class="sxs-lookup"><span data-stu-id="4c3c2-118">Page</span></span><br/>    |
| <span data-ttu-id="4c3c2-119">注意</span><span class="sxs-lookup"><span data-stu-id="4c3c2-119">Notes</span></span> <br/>          | <span data-ttu-id="4c3c2-120">None</span><span class="sxs-lookup"><span data-stu-id="4c3c2-120">None</span></span> <br/>   |



 

## <a name="structural-content"></a><span data-ttu-id="4c3c2-121">結構化內容</span><span class="sxs-lookup"><span data-stu-id="4c3c2-121">Structural Content</span></span>

<span data-ttu-id="4c3c2-122">此元素的 XML 結構為：</span><span class="sxs-lookup"><span data-stu-id="4c3c2-122">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="4c3c2-123">結構變數</span><span class="sxs-lookup"><span data-stu-id="4c3c2-123">Structure Variables</span></span>

<span data-ttu-id="4c3c2-124">下表概述 XML 結構中所定義之變數的特性。</span><span class="sxs-lookup"><span data-stu-id="4c3c2-124">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="4c3c2-125">Name</span><span class="sxs-lookup"><span data-stu-id="4c3c2-125">Name</span></span>                               | <span data-ttu-id="4c3c2-126">資料類型</span><span class="sxs-lookup"><span data-stu-id="4c3c2-126">Data type</span></span>         | <span data-ttu-id="4c3c2-127">單位</span><span class="sxs-lookup"><span data-stu-id="4c3c2-127">Unit</span></span>                  | <span data-ttu-id="4c3c2-128">支援的值</span><span class="sxs-lookup"><span data-stu-id="4c3c2-128">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="4c3c2-129">總結</span><span class="sxs-lookup"><span data-stu-id="4c3c2-129">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="4c3c2-130">\_選項名稱\_</span><span class="sxs-lookup"><span data-stu-id="4c3c2-130">\_OptionName\_</span></span><br/>          | <span data-ttu-id="4c3c2-131">字串</span><span class="sxs-lookup"><span data-stu-id="4c3c2-131">string</span></span><br/> | <span data-ttu-id="4c3c2-132">字元</span><span class="sxs-lookup"><span data-stu-id="4c3c2-132">characters</span></span><br/> | <span data-ttu-id="4c3c2-133">以 [XML 命名空間](https://www.w3.org/TR/1999/REC-xml-names-19990114/)所定義的有效完整名稱。</span><span class="sxs-lookup"><span data-stu-id="4c3c2-133">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="4c3c2-134">如果未指定命名空間，則會假設為預設命名空間。</span><span class="sxs-lookup"><span data-stu-id="4c3c2-134">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="4c3c2-135">選項的名稱。</span><span class="sxs-lookup"><span data-stu-id="4c3c2-135">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="4c3c2-136">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="4c3c2-136">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="4c3c2-137">字串</span><span class="sxs-lookup"><span data-stu-id="4c3c2-137">string</span></span><br/> | <span data-ttu-id="4c3c2-138">n/a</span><span class="sxs-lookup"><span data-stu-id="4c3c2-138">n/a</span></span><br/>        | <span data-ttu-id="4c3c2-139">True、False。</span><span class="sxs-lookup"><span data-stu-id="4c3c2-139">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="4c3c2-140">定義選項，當選取此選項時，會停用此功能。</span><span class="sxs-lookup"><span data-stu-id="4c3c2-140">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="4c3c2-141">可延伸標記語言 (XML)  (XML) 內容</span><span class="sxs-lookup"><span data-stu-id="4c3c2-141">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="4c3c2-142">公用列印架構關鍵字是在 https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords 命名空間中定義。</span><span class="sxs-lookup"><span data-stu-id="4c3c2-142">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="4c3c2-143">此關鍵字的 public 可延伸標記語言 (XML)  (XML) 內容定義如下：</span><span class="sxs-lookup"><span data-stu-id="4c3c2-143">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="4c3c2-144">相關主題</span><span class="sxs-lookup"><span data-stu-id="4c3c2-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4c3c2-145">列印架構規格</span><span class="sxs-lookup"><span data-stu-id="4c3c2-145">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




