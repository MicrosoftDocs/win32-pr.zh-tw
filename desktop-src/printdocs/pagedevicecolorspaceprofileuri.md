---
description: 本主題並非最新的。 如需最新資訊，請參閱列印架構規格。
ms.assetid: ab26850e-554a-4a1b-9250-edb0b4e17fe2
title: PageDeviceColorSpaceProfileURI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20a1b4cf607ddf880311659e562647ba583a2951
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/26/2021
ms.locfileid: "107995675"
---
# <a name="pagedevicecolorspaceprofileuri"></a><span data-ttu-id="f0f3d-104">PageDeviceColorSpaceProfileURI</span><span class="sxs-lookup"><span data-stu-id="f0f3d-104">PageDeviceColorSpaceProfileURI</span></span>

<span data-ttu-id="f0f3d-105">本主題並非最新的。</span><span class="sxs-lookup"><span data-stu-id="f0f3d-105">This topic is not current.</span></span> <span data-ttu-id="f0f3d-106">如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。</span><span class="sxs-lookup"><span data-stu-id="f0f3d-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="f0f3d-107">針對包含在 XPS 檔中的 ICC 設定檔，指定套件根目錄的相對 URI。</span><span class="sxs-lookup"><span data-stu-id="f0f3d-107">Specifies a relative URI to the package root to an ICC profile contained in an XPS Document.</span></span> <span data-ttu-id="f0f3d-108">此選項的處理取決於 PageDeviceColorSpaceUsage 功能的設定。</span><span class="sxs-lookup"><span data-stu-id="f0f3d-108">The processing of this option depends of the setting of the PageDeviceColorSpaceUsage feature.</span></span> <span data-ttu-id="f0f3d-109">使用該設定檔的所有元素都會假設已經在適當的裝置色彩空間中，而且不會在驅動程式或裝置中進行色彩管理。</span><span class="sxs-lookup"><span data-stu-id="f0f3d-109">All elements using that profile are assumed to be already in the appropriate device color space, and will not be color managed in the driver or device.</span></span>

-   [<span data-ttu-id="f0f3d-110">項目資訊</span><span class="sxs-lookup"><span data-stu-id="f0f3d-110">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="f0f3d-111">結構內容</span><span class="sxs-lookup"><span data-stu-id="f0f3d-111">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="f0f3d-112">項目資訊</span><span class="sxs-lookup"><span data-stu-id="f0f3d-112">Element Information</span></span>



| <span data-ttu-id="f0f3d-113">Name</span><span class="sxs-lookup"><span data-stu-id="f0f3d-113">Name</span></span> | <span data-ttu-id="f0f3d-114">值</span><span class="sxs-lookup"><span data-stu-id="f0f3d-114">Value</span></span> |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f0f3d-115">項目類型</span><span class="sxs-lookup"><span data-stu-id="f0f3d-115">Element Type</span></span> <br/>   | <span data-ttu-id="f0f3d-116">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="f0f3d-116">ParameterDef</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="f0f3d-117">範圍前置詞</span><span class="sxs-lookup"><span data-stu-id="f0f3d-117">Scoping Prefix</span></span> <br/> | <span data-ttu-id="f0f3d-118">頁面</span><span class="sxs-lookup"><span data-stu-id="f0f3d-118">Page</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="f0f3d-119">備註</span><span class="sxs-lookup"><span data-stu-id="f0f3d-119">Notes</span></span> <br/>          | <span data-ttu-id="f0f3d-120">這僅適用于 XPS 檔，不應該用於任意 PrintTickets。</span><span class="sxs-lookup"><span data-stu-id="f0f3d-120">This applies to XPS Documents only and should not be used in arbitrary PrintTickets.</span></span><br/> <span data-ttu-id="f0f3d-121">符合 XPS 規範的取用者必須在列印功能檔或 PrintTicket 中，強制資源的 URI 參考（例如影像或色彩設定檔）必須參考元件名稱， (在包含結果 PrintTicket 的相同 XPS 檔封裝內的封裝根目錄) 的相對 URI。</span><span class="sxs-lookup"><span data-stu-id="f0f3d-121">XPS-compliant consumers MUST enforce that a URI reference to a resource such as an image or color profile in either a Print Capabilities document or PrintTicket MUST refer to a part name (a relative URI to the package root) within the same XPS Document package that contains the resultant PrintTicket.</span></span> <span data-ttu-id="f0f3d-122">相容的 XPS 取用者不能使用不符合元件名稱語法規范的 URI。</span><span class="sxs-lookup"><span data-stu-id="f0f3d-122">A compliant XPS consumer MUST NOT use a URI that is not compliant with the part name syntax.</span></span> <span data-ttu-id="f0f3d-123">這些設定是 XPS 專用的。</span><span class="sxs-lookup"><span data-stu-id="f0f3d-123">These settings are XPS specific.</span></span> <br/> <span data-ttu-id="f0f3d-124">在列印功能檔或 PrintTicket 中參考的 Uri 不得解析為 Url。</span><span class="sxs-lookup"><span data-stu-id="f0f3d-124">URIs which are referenced in either a Print Capabilities document or PrintTicket MUST NOT be resolved as URLs.</span></span> <span data-ttu-id="f0f3d-125">這是不安全的，因為它們可能無法如預期地解決，而且可能會產生驅動程式和作業系統的有害安全性風險。</span><span class="sxs-lookup"><span data-stu-id="f0f3d-125">This is unsafe as they may not resolve as intended and may create harmful security risks for the driver and operating system.</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="f0f3d-126">結構內容</span><span class="sxs-lookup"><span data-stu-id="f0f3d-126">Structure Content</span></span>

<span data-ttu-id="f0f3d-127">此元素的 XML 結構為：</span><span class="sxs-lookup"><span data-stu-id="f0f3d-127">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageDeviceColorSpaceProfileURI">
  <psf:Property name="psf:DataType">
    <psf:Value xsi:type="xs:string">xs:string</psf:Value>
  </psf:Property>
  <psf:Property name="psf:DefaultValue">
    <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MaxLength">
    <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MinLength">
    <psf:Value xsi:type="xs:integer">1</psf:Value>
  </psf:Property>
  <psf:Property name="psf:Mandatory">
    <psf:Value xsi:type="xs:string">psk:Conditional</psf:Value>
  </psf:Property>
  <psf:Property name="psf:UnitType">
    <psf:Value xsi:type="xs:string">characters</psf:Value>
  </psf:Property>
</psf:ParameterDef>
```

## <a name="structure-properties"></a><span data-ttu-id="f0f3d-128">結構屬性</span><span class="sxs-lookup"><span data-stu-id="f0f3d-128">Structure Properties</span></span>

<span data-ttu-id="f0f3d-129">下表概述 XML 結構中所定義之變數的特性。</span><span class="sxs-lookup"><span data-stu-id="f0f3d-129">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="f0f3d-130">屬性</span><span class="sxs-lookup"><span data-stu-id="f0f3d-130">Property</span></span>                | <span data-ttu-id="f0f3d-131">xsi:type</span><span class="sxs-lookup"><span data-stu-id="f0f3d-131">xsi:type</span></span>           | <span data-ttu-id="f0f3d-132">值</span><span class="sxs-lookup"><span data-stu-id="f0f3d-132">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="f0f3d-133">DataType</span><span class="sxs-lookup"><span data-stu-id="f0f3d-133">DataType</span></span><br/>     | <span data-ttu-id="f0f3d-134">字串</span><span class="sxs-lookup"><span data-stu-id="f0f3d-134">string</span></span><br/>  | <span data-ttu-id="f0f3d-135">xs:string</span><span class="sxs-lookup"><span data-stu-id="f0f3d-135">xs:string</span></span><br/>       |
| <span data-ttu-id="f0f3d-136">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="f0f3d-136">DefaultValue</span></span><br/> | <span data-ttu-id="f0f3d-137">字串</span><span class="sxs-lookup"><span data-stu-id="f0f3d-137">string</span></span><br/>  | <span data-ttu-id="f0f3d-138">未定義</span><span class="sxs-lookup"><span data-stu-id="f0f3d-138">undefined</span></span><br/>       |
| <span data-ttu-id="f0f3d-139">MaxLength</span><span class="sxs-lookup"><span data-stu-id="f0f3d-139">MaxLength</span></span><br/>    | <span data-ttu-id="f0f3d-140">整數</span><span class="sxs-lookup"><span data-stu-id="f0f3d-140">integer</span></span><br/> | <span data-ttu-id="f0f3d-141">未定義</span><span class="sxs-lookup"><span data-stu-id="f0f3d-141">undefined</span></span><br/>       |
| <span data-ttu-id="f0f3d-142">MinLength</span><span class="sxs-lookup"><span data-stu-id="f0f3d-142">MinLength</span></span><br/>    | <span data-ttu-id="f0f3d-143">整數</span><span class="sxs-lookup"><span data-stu-id="f0f3d-143">integer</span></span><br/> | <span data-ttu-id="f0f3d-144">1</span><span class="sxs-lookup"><span data-stu-id="f0f3d-144">1</span></span><br/>               |
| <span data-ttu-id="f0f3d-145">強制性</span><span class="sxs-lookup"><span data-stu-id="f0f3d-145">Mandatory</span></span><br/>    | <span data-ttu-id="f0f3d-146">字串</span><span class="sxs-lookup"><span data-stu-id="f0f3d-146">string</span></span><br/>  | <span data-ttu-id="f0f3d-147">psk：條件式</span><span class="sxs-lookup"><span data-stu-id="f0f3d-147">psk:Conditional</span></span><br/> |
| <span data-ttu-id="f0f3d-148">Unittype.pixel 表示</span><span class="sxs-lookup"><span data-stu-id="f0f3d-148">UnitType</span></span><br/>     | <span data-ttu-id="f0f3d-149">字串</span><span class="sxs-lookup"><span data-stu-id="f0f3d-149">string</span></span><br/>  | <span data-ttu-id="f0f3d-150">字元</span><span class="sxs-lookup"><span data-stu-id="f0f3d-150">characters</span></span><br/>      |



 

## <a name="related-topics"></a><span data-ttu-id="f0f3d-151">相關主題</span><span class="sxs-lookup"><span data-stu-id="f0f3d-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f0f3d-152">列印架構規格</span><span class="sxs-lookup"><span data-stu-id="f0f3d-152">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




