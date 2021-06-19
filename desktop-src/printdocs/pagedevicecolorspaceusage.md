---
description: 檢查 PageDeviceColorSpaceUsage 使用者可設定的元素。 本主題並非最新的。 如需最新資訊，請參閱列印架構規格。
ms.assetid: c529c731-fcf0-463e-a251-6a05215e4d23
title: PageDeviceColorSpaceUsage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30b81a37d103d3ce5f1cbb1fb8c032a18d495c2c
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/19/2021
ms.locfileid: "112396663"
---
# <a name="pagedevicecolorspaceusage"></a><span data-ttu-id="6685c-105">PageDeviceColorSpaceUsage</span><span class="sxs-lookup"><span data-stu-id="6685c-105">PageDeviceColorSpaceUsage</span></span>

<span data-ttu-id="6685c-106">本主題並非最新的。</span><span class="sxs-lookup"><span data-stu-id="6685c-106">This topic is not current.</span></span> <span data-ttu-id="6685c-107">如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。</span><span class="sxs-lookup"><span data-stu-id="6685c-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="6685c-108">搭配 PageDeviceColorSpaceProfileURI 參數使用時，此參數會定義裝置色彩空間中所呈現之元素的轉譯行為。</span><span class="sxs-lookup"><span data-stu-id="6685c-108">In conjunction with the PageDeviceColorSpaceProfileURI parameter, this parameter defines the rendering behavior for elements presented in a device color space.</span></span>

-   [<span data-ttu-id="6685c-109">項目資訊</span><span class="sxs-lookup"><span data-stu-id="6685c-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="6685c-110">結構化內容</span><span class="sxs-lookup"><span data-stu-id="6685c-110">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="6685c-111">可延伸標記語言 (XML)  (XML) 內容</span><span class="sxs-lookup"><span data-stu-id="6685c-111">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="6685c-112">項目資訊</span><span class="sxs-lookup"><span data-stu-id="6685c-112">Element Information</span></span>



| <span data-ttu-id="6685c-113">Name</span><span class="sxs-lookup"><span data-stu-id="6685c-113">Name</span></span> | <span data-ttu-id="6685c-114">值</span><span class="sxs-lookup"><span data-stu-id="6685c-114">Value</span></span> |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6685c-115">項目類型</span><span class="sxs-lookup"><span data-stu-id="6685c-115">Element Type</span></span> <br/>   | <span data-ttu-id="6685c-116">功能</span><span class="sxs-lookup"><span data-stu-id="6685c-116">Feature</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="6685c-117">範圍前置詞</span><span class="sxs-lookup"><span data-stu-id="6685c-117">Scoping Prefix</span></span> <br/> | <span data-ttu-id="6685c-118">頁面</span><span class="sxs-lookup"><span data-stu-id="6685c-118">Page</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="6685c-119">備註</span><span class="sxs-lookup"><span data-stu-id="6685c-119">Notes</span></span> <br/>          | <span data-ttu-id="6685c-120">這僅適用于 XPS 檔，不應該用於任意 PrintTickets。</span><span class="sxs-lookup"><span data-stu-id="6685c-120">This applies to XPS Documents only and should not be used in arbitrary PrintTickets.</span></span><br/> <span data-ttu-id="6685c-121">符合 XPS 規範的取用者必須在列印功能檔或 PrintTicket 中，強制資源的 URI 參考（例如影像或色彩設定檔）必須參考元件名稱， (在包含結果 PrintTicket 的相同 XPS 檔封裝內的封裝根目錄) 的相對 URI。</span><span class="sxs-lookup"><span data-stu-id="6685c-121">XPS-compliant consumers MUST enforce that a URI reference to a resource such as an image or color profile in either a Print Capabilities document or PrintTicket MUST refer to a part name (a relative URI to the package root) within the same XPS Document package that contains the resultant PrintTicket.</span></span> <span data-ttu-id="6685c-122">相容的 XPS 取用者不能使用不符合元件名稱語法規范的 URI。</span><span class="sxs-lookup"><span data-stu-id="6685c-122">A compliant XPS consumer MUST NOT use a URI that is not compliant with the part name syntax.</span></span> <span data-ttu-id="6685c-123">這些設定是 XPS 專用的。</span><span class="sxs-lookup"><span data-stu-id="6685c-123">These settings are XPS specific.</span></span> <br/> <span data-ttu-id="6685c-124">在列印功能檔或 PrintTicket 中參考的 Uri 不得解析為 Url。</span><span class="sxs-lookup"><span data-stu-id="6685c-124">URIs which are referenced in either a Print Capabilities document or PrintTicket MUST NOT be resolved as URLs.</span></span> <span data-ttu-id="6685c-125">這是不安全的，因為它們可能無法如預期地解決，而且可能會產生驅動程式和作業系統的有害安全性風險。</span><span class="sxs-lookup"><span data-stu-id="6685c-125">This is unsafe as they may not resolve as intended and may create harmful security risks for the driver and operating system.</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="6685c-126">結構化內容</span><span class="sxs-lookup"><span data-stu-id="6685c-126">Structural Content</span></span>

<span data-ttu-id="6685c-127">此元素的 XML 結構為：</span><span class="sxs-lookup"><span data-stu-id="6685c-127">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:PageDeviceColorSpaceUsage">
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

## <a name="structure-variables"></a><span data-ttu-id="6685c-128">結構變數</span><span class="sxs-lookup"><span data-stu-id="6685c-128">Structure Variables</span></span>

<span data-ttu-id="6685c-129">下表概述 XML 結構中所定義之變數的特性。</span><span class="sxs-lookup"><span data-stu-id="6685c-129">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="6685c-130">Name</span><span class="sxs-lookup"><span data-stu-id="6685c-130">Name</span></span>                               | <span data-ttu-id="6685c-131">資料類型</span><span class="sxs-lookup"><span data-stu-id="6685c-131">Data type</span></span>         | <span data-ttu-id="6685c-132">單位</span><span class="sxs-lookup"><span data-stu-id="6685c-132">Unit</span></span>                  | <span data-ttu-id="6685c-133">支援的值</span><span class="sxs-lookup"><span data-stu-id="6685c-133">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="6685c-134">總結</span><span class="sxs-lookup"><span data-stu-id="6685c-134">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="6685c-135">\_選項名稱\_</span><span class="sxs-lookup"><span data-stu-id="6685c-135">\_OptionName\_</span></span><br/>          | <span data-ttu-id="6685c-136">string</span><span class="sxs-lookup"><span data-stu-id="6685c-136">string</span></span><br/> | <span data-ttu-id="6685c-137">字元</span><span class="sxs-lookup"><span data-stu-id="6685c-137">characters</span></span><br/> | <span data-ttu-id="6685c-138">以 [XML 命名空間](https://www.w3.org/TR/1999/REC-xml-names-19990114/)所定義的有效完整名稱。</span><span class="sxs-lookup"><span data-stu-id="6685c-138">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="6685c-139">如果未指定命名空間，則會假設為預設命名空間。</span><span class="sxs-lookup"><span data-stu-id="6685c-139">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="6685c-140">選項的名稱。</span><span class="sxs-lookup"><span data-stu-id="6685c-140">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="6685c-141">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="6685c-141">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="6685c-142">string</span><span class="sxs-lookup"><span data-stu-id="6685c-142">string</span></span><br/> | <span data-ttu-id="6685c-143">n/a</span><span class="sxs-lookup"><span data-stu-id="6685c-143">n/a</span></span><br/>        | <span data-ttu-id="6685c-144">True、False。</span><span class="sxs-lookup"><span data-stu-id="6685c-144">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="6685c-145">定義選項，當選取此選項時，會停用此功能。</span><span class="sxs-lookup"><span data-stu-id="6685c-145">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="6685c-146">可延伸標記語言 (XML)  (XML) 內容</span><span class="sxs-lookup"><span data-stu-id="6685c-146">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="6685c-147">公用列印架構關鍵字是在 https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords 命名空間中定義。</span><span class="sxs-lookup"><span data-stu-id="6685c-147">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="6685c-148">此關鍵字的 public 可延伸標記語言 (XML)  (XML) 內容定義如下：</span><span class="sxs-lookup"><span data-stu-id="6685c-148">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:PageDeviceColorSpaceUsage">
  <psf:Property name="SelectionType">
    <psf:Value xsi:type="xs:string">PickOne</psf:Value>
  </psf:Property>
  <!-- If the device determines that the profile specified by the PageDeviceColorSpaceProfileURI parameter can be used as a device color space profile, all elements using the same profile are treated as already being specified in device color space. All other elements MUST use the profile specified for that element.
If the profile cannot be used as a device color space profile, elements using the profile MUST be color managed like any other element using the color profile. -->
  <psf:Option name="psk:MatchToDefault" />
  <!-- If the profile specified by the PageDeviceColorSpaceProfileURI parameter has a number of channels matching the number of primaries of the device, it SHOULD be used instead of the devices internal color management for all elements. Elements using this profile are assumed to be in device color space and will not be color managed further. -->
  <psf:Option name="psk:OverrideDeviceDefault" />
</psf:Feature>
```

## <a name="related-topics"></a><span data-ttu-id="6685c-149">相關主題</span><span class="sxs-lookup"><span data-stu-id="6685c-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6685c-150">列印架構規格</span><span class="sxs-lookup"><span data-stu-id="6685c-150">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




