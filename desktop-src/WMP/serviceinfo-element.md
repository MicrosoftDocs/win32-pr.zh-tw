---
title: ServiceInfo 元素
description: 請注意，本節將說明針對線上商店使用而設計的功能。 不支援在線上商店的內容之外使用這項功能。 ServiceInfo 元素是 ServiceInfo.xml 檔的主要元素。
ms.assetid: d2f9e642-143e-405d-8588-c78e4355b9b9
keywords:
- ServiceInfo 元素 Windows Media Player
topic_type:
- apiref
api_name:
- ServiceInfo Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7ac41edd4ae8548ecdb6d3ef6631fba5d6175762
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106989605"
---
# <a name="serviceinfo-element"></a><span data-ttu-id="14a70-106">ServiceInfo 元素</span><span class="sxs-lookup"><span data-stu-id="14a70-106">ServiceInfo Element</span></span>

> [!Note]  
> <span data-ttu-id="14a70-107">本章節描述專為線上商店使用而設計的功能。</span><span class="sxs-lookup"><span data-stu-id="14a70-107">This section describes functionality designed for use by online stores.</span></span> <span data-ttu-id="14a70-108">不支援在線上商店的內容之外使用這項功能。</span><span class="sxs-lookup"><span data-stu-id="14a70-108">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="14a70-109">**ServiceInfo** 元素是 ServiceInfo.xml 檔的主要元素。</span><span class="sxs-lookup"><span data-stu-id="14a70-109">The **ServiceInfo** element is the main element for the ServiceInfo.xml document.</span></span>

``` syntax
<ServiceInfo
    Version = 1.00
    Key = "service key"
    ContentPartner = "true|false"
/>
```

## <a name="attributes"></a><span data-ttu-id="14a70-110">屬性</span><span class="sxs-lookup"><span data-stu-id="14a70-110">Attributes</span></span>



| <span data-ttu-id="14a70-111">詞彙</span><span class="sxs-lookup"><span data-stu-id="14a70-111">Term</span></span>                                                                                                                                             | <span data-ttu-id="14a70-112">描述</span><span class="sxs-lookup"><span data-stu-id="14a70-112">Description</span></span>                                                                                                                                                                                                                                                    |
|--------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="14a70-113"><span id="Version__optional_"></span><span id="version__optional_"></span><span id="VERSION__OPTIONAL_"></span>**版本** (選用) </span><span class="sxs-lookup"><span data-stu-id="14a70-113"><span id="Version__optional_"></span><span id="version__optional_"></span><span id="VERSION__OPTIONAL_"></span>**Version** (optional)</span></span><br/> | <span data-ttu-id="14a70-114">ServiceInfo.xml 檔的版本。</span><span class="sxs-lookup"><span data-stu-id="14a70-114">Version of the ServiceInfo.xml file.</span></span> <span data-ttu-id="14a70-115">Windows Media Player 支援1.00 版。</span><span class="sxs-lookup"><span data-stu-id="14a70-115">Version 1.00 is supported for Windows Media Player.</span></span><br/>                                                                                                                                                            |
| <span data-ttu-id="14a70-116"><span id="Key__required_"></span><span id="key__required_"></span><span id="KEY__REQUIRED_"></span>需要 (**金鑰**) </span><span class="sxs-lookup"><span data-stu-id="14a70-116"><span id="Key__required_"></span><span id="key__required_"></span><span id="KEY__REQUIRED_"></span>**Key** (required)</span></span><br/>                 | <span data-ttu-id="14a70-117">可唯一識別線上商店的服務金鑰字串。</span><span class="sxs-lookup"><span data-stu-id="14a70-117">The service key string that uniquely identifies the online store.</span></span><br/>                                                                                                                                                                                   |
| <span data-ttu-id="14a70-118"><span id="ContentPartner"></span><span id="contentpartner"></span><span id="CONTENTPARTNER"></span>**ContentPartner**</span><span class="sxs-lookup"><span data-stu-id="14a70-118"><span id="ContentPartner"></span><span id="contentpartner"></span><span id="CONTENTPARTNER"></span>**ContentPartner**</span></span><br/>                 | <span data-ttu-id="14a70-119">指出線上商店是否為類型1存放區。</span><span class="sxs-lookup"><span data-stu-id="14a70-119">Indicates whether the online store is a type 1 store.</span></span> <span data-ttu-id="14a70-120">值為 "true" 表示存放區為類型1存放區。</span><span class="sxs-lookup"><span data-stu-id="14a70-120">A value of "true" indicates that the store is a type 1 store.</span></span> <span data-ttu-id="14a70-121">值為 "false" 表示存放區不是類型1存放區;也就是說，它是類型2存放區。</span><span class="sxs-lookup"><span data-stu-id="14a70-121">A value of "false" indicates that the store is not a type 1 store; that is, it is a type 2 store.</span></span> <span data-ttu-id="14a70-122">預設值為 "false"。</span><span class="sxs-lookup"><span data-stu-id="14a70-122">The default value is "false".</span></span><br/> |



 

## <a name="parentchild-elements"></a><span data-ttu-id="14a70-123">父/子項目</span><span class="sxs-lookup"><span data-stu-id="14a70-123">Parent/Child Elements</span></span>



| <span data-ttu-id="14a70-124">階層</span><span class="sxs-lookup"><span data-stu-id="14a70-124">Hierarchy</span></span>       | <span data-ttu-id="14a70-125">元素</span><span class="sxs-lookup"><span data-stu-id="14a70-125">Element</span></span>                                                                                                                                                                            |
|-----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="14a70-126">父元素</span><span class="sxs-lookup"><span data-stu-id="14a70-126">Parent elements</span></span> | <span data-ttu-id="14a70-127">無</span><span class="sxs-lookup"><span data-stu-id="14a70-127">None</span></span>                                                                                                                                                                               |
| <span data-ttu-id="14a70-128">子元素</span><span class="sxs-lookup"><span data-stu-id="14a70-128">Child elements</span></span>  | <span data-ttu-id="14a70-129">**AlbumInfo**、 **BuyCD**、 **Color**、 **Description**、 **FriendlyName**、 **HTMLView**、 **Image**、 **資訊中心**、 **Install**、 **ServiceTask1**、 **ServiceTask2**、 **ServiceTask3**</span><span class="sxs-lookup"><span data-stu-id="14a70-129">**AlbumInfo**, **BuyCD**, **Color**, **Description**, **FriendlyName**, **HTMLView**, **Image**, **InfoCenter**, **Install**, **ServiceTask1**, **ServiceTask2**, **ServiceTask3**</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="14a70-130">備註</span><span class="sxs-lookup"><span data-stu-id="14a70-130">Remarks</span></span>

<span data-ttu-id="14a70-131">下表詳細說明以 URL 要求傳送的參數。</span><span class="sxs-lookup"><span data-stu-id="14a70-131">The following table details the parameters sent with the URL request.</span></span> <span data-ttu-id="14a70-132">其他可能存在於舊版相容性的用途。</span><span class="sxs-lookup"><span data-stu-id="14a70-132">Others may be present for legacy compatibility purposes.</span></span> <span data-ttu-id="14a70-133">要求也會包含您使用 Windows Media Player 安裝程式的 ServiceExtra 命令列參數指定的任何參數。</span><span class="sxs-lookup"><span data-stu-id="14a70-133">The request will also include any parameters you specified using the ServiceExtra command-line parameter of Windows Media Player setup.</span></span>



| <span data-ttu-id="14a70-134">Name</span><span class="sxs-lookup"><span data-stu-id="14a70-134">Name</span></span>         | <span data-ttu-id="14a70-135">值</span><span class="sxs-lookup"><span data-stu-id="14a70-135">Value</span></span>                                                                                                                                                               |
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="14a70-136">*大地 水準面*</span><span class="sxs-lookup"><span data-stu-id="14a70-136">*geoid*</span></span>      | <span data-ttu-id="14a70-137">Windows 地理位置識別碼。</span><span class="sxs-lookup"><span data-stu-id="14a70-137">Windows geographical location ID.</span></span> <span data-ttu-id="14a70-138">在主控台的 [地區及語言選項] 設定的 [ **位置** ] 區域中，使用者會指定位置識別碼。</span><span class="sxs-lookup"><span data-stu-id="14a70-138">The location ID is specified by the user in the **Location** area of the Regional and Language Options settings in Control Panel.</span></span> |
| <span data-ttu-id="14a70-139">*locale*</span><span class="sxs-lookup"><span data-stu-id="14a70-139">*locale*</span></span>     | <span data-ttu-id="14a70-140">Windows Media Player 地區設定識別碼。</span><span class="sxs-lookup"><span data-stu-id="14a70-140">Windows Media Player locale ID.</span></span>                                                                                                                                     |
| <span data-ttu-id="14a70-141">*userlocale*</span><span class="sxs-lookup"><span data-stu-id="14a70-141">*userlocale*</span></span> | <span data-ttu-id="14a70-142">Windows 地區設定識別碼。</span><span class="sxs-lookup"><span data-stu-id="14a70-142">Windows locale ID.</span></span> <span data-ttu-id="14a70-143">地區設定是由使用者在主控台的 [地區及語言選項] 設定的 [ **標準] 和 [格式** ] 區域中所指定。</span><span class="sxs-lookup"><span data-stu-id="14a70-143">The locale is specified by the user in the **Standards and Formats** area of the Regional and Language Options settings in Control Panel.</span></span>        |
| <span data-ttu-id="14a70-144">*version*</span><span class="sxs-lookup"><span data-stu-id="14a70-144">*version*</span></span>    | <span data-ttu-id="14a70-145">使用下列格式的 Windows Media Player 版本號碼： 10.0. x. x. x. x. x. x. x. x. x。</span><span class="sxs-lookup"><span data-stu-id="14a70-145">Windows Media Player version number using the following format: 10.0.x.xxxx or 11.0.x.xxxx.</span></span>                                                                         |



 

## <a name="requirements"></a><span data-ttu-id="14a70-146">規格需求</span><span class="sxs-lookup"><span data-stu-id="14a70-146">Requirements</span></span>



| <span data-ttu-id="14a70-147">需求</span><span class="sxs-lookup"><span data-stu-id="14a70-147">Requirement</span></span> | <span data-ttu-id="14a70-148">值</span><span class="sxs-lookup"><span data-stu-id="14a70-148">Value</span></span> |
|--------------------|----------------------------------------------|
| <span data-ttu-id="14a70-149">版本</span><span class="sxs-lookup"><span data-stu-id="14a70-149">Version</span></span><br/> | <span data-ttu-id="14a70-150">Windows Media Player 10 或更新版本。</span><span class="sxs-lookup"><span data-stu-id="14a70-150">Windows Media Player 10 or later.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="14a70-151">另請參閱</span><span class="sxs-lookup"><span data-stu-id="14a70-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="14a70-152">**類型1線上商店的範例 ServiceInfo 檔**</span><span class="sxs-lookup"><span data-stu-id="14a70-152">**Example ServiceInfo Document for a Type 1 Online Store**</span></span>](example-serviceinfo-document-for-a-type-1-online-store.md)
</dt> <dt>

[<span data-ttu-id="14a70-153">**Type 2 線上商店的範例 ServiceInfo 檔**</span><span class="sxs-lookup"><span data-stu-id="14a70-153">**Example ServiceInfo Document for a Type 2 Online Store**</span></span>](example-serviceinfo-document-for-a-type-2-online-store.md)
</dt> <dt>

[<span data-ttu-id="14a70-154">**ServiceInfo 檔**</span><span class="sxs-lookup"><span data-stu-id="14a70-154">**ServiceInfo Document**</span></span>](serviceinfo-document.md)
</dt> </dl>

 

 





