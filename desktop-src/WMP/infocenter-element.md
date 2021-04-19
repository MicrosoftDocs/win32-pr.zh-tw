---
title: 資訊中心元素
description: 請注意，本節將說明針對線上商店使用而設計的功能。 |資訊中心元素
ms.assetid: 1a9cc513-5dd1-46d8-9409-16413695b4c8
keywords:
- 資訊中心元素 Windows Media Player
topic_type:
- apiref
api_name:
- InfoCenter Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ef62e0f6b41090642400a7f0a8b88af72818da4c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990528"
---
# <a name="infocenter-element"></a><span data-ttu-id="30144-105">資訊中心元素</span><span class="sxs-lookup"><span data-stu-id="30144-105">InfoCenter Element</span></span>

> [!Note]  
> <span data-ttu-id="30144-106">本章節描述專為線上商店使用而設計的功能。</span><span class="sxs-lookup"><span data-stu-id="30144-106">This section describes functionality designed for use by online stores.</span></span> <span data-ttu-id="30144-107">不支援在線上商店的內容之外使用這項功能。</span><span class="sxs-lookup"><span data-stu-id="30144-107">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="30144-108">**資訊中心** 元素會指定網頁的 URL，Windows Media Player 在線上商店為使用中時，于 **現在播放** 的資訊中心視圖功能中顯示。</span><span class="sxs-lookup"><span data-stu-id="30144-108">The **InfoCenter** element specifies the URL of the webpage that Windows Media Player displays in the Info Center View feature of **Now Playing** when the online store is active.</span></span>

``` syntax
<InfoCenter
    URL = "URL"
/>
```

## <a name="attributes"></a><span data-ttu-id="30144-109">屬性</span><span class="sxs-lookup"><span data-stu-id="30144-109">Attributes</span></span>

<dl> <dt>

<span data-ttu-id="30144-110"><span id="URL__required_"></span><span id="url__required_"></span><span id="URL__REQUIRED_"></span>需要 (**URL**) </span><span class="sxs-lookup"><span data-stu-id="30144-110"><span id="URL__required_"></span><span id="url__required_"></span><span id="URL__REQUIRED_"></span>**URL** (required)</span></span>
</dt> <dd>

<span data-ttu-id="30144-111">Windows Media Player 顯示之網頁的 URL。</span><span class="sxs-lookup"><span data-stu-id="30144-111">URL for the webpage that Windows Media Player displays.</span></span>

</dd> </dl>

## <a name="parentchild-elements"></a><span data-ttu-id="30144-112">父/子項目</span><span class="sxs-lookup"><span data-stu-id="30144-112">Parent/Child Elements</span></span>



| <span data-ttu-id="30144-113">階層</span><span class="sxs-lookup"><span data-stu-id="30144-113">Hierarchy</span></span>       | <span data-ttu-id="30144-114">元素</span><span class="sxs-lookup"><span data-stu-id="30144-114">Element</span></span>         |
|-----------------|-----------------|
| <span data-ttu-id="30144-115">父元素</span><span class="sxs-lookup"><span data-stu-id="30144-115">Parent elements</span></span> | <span data-ttu-id="30144-116">**ServiceInfo**</span><span class="sxs-lookup"><span data-stu-id="30144-116">**ServiceInfo**</span></span> |
| <span data-ttu-id="30144-117">子元素</span><span class="sxs-lookup"><span data-stu-id="30144-117">Child elements</span></span>  | <span data-ttu-id="30144-118">無</span><span class="sxs-lookup"><span data-stu-id="30144-118">None</span></span>            |



 

## <a name="remarks"></a><span data-ttu-id="30144-119">備註</span><span class="sxs-lookup"><span data-stu-id="30144-119">Remarks</span></span>

<span data-ttu-id="30144-120">使用者控制資訊中心視圖的作用中。</span><span class="sxs-lookup"><span data-stu-id="30144-120">The user controls when Info Center View is active.</span></span>

<span data-ttu-id="30144-121">若要取得目前播放之媒體專案的相關資訊，您必須在網頁中內嵌 Windows Media Player 控制項的實例，並使用 Player 物件模型。</span><span class="sxs-lookup"><span data-stu-id="30144-121">To retrieve information about the currently playing media item, you must embed an instance of Windows Media Player control in your webpage and use the Player object model.</span></span>

<span data-ttu-id="30144-122">下表詳細說明以 URL 要求傳送的參數。</span><span class="sxs-lookup"><span data-stu-id="30144-122">The following table details the parameters sent with the URL request.</span></span> <span data-ttu-id="30144-123">其他可能存在於舊版相容性的用途。</span><span class="sxs-lookup"><span data-stu-id="30144-123">Others may be present for legacy compatibility purposes.</span></span>



| <span data-ttu-id="30144-124">Name</span><span class="sxs-lookup"><span data-stu-id="30144-124">Name</span></span>         | <span data-ttu-id="30144-125">值</span><span class="sxs-lookup"><span data-stu-id="30144-125">Value</span></span>                                                                                                                                                               |
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="30144-126">*大地 水準面*</span><span class="sxs-lookup"><span data-stu-id="30144-126">*geoid*</span></span>      | <span data-ttu-id="30144-127">Windows 地理位置識別碼。</span><span class="sxs-lookup"><span data-stu-id="30144-127">Windows geographical location ID.</span></span> <span data-ttu-id="30144-128">在主控台的 [地區及語言選項] 設定的 [ **位置** ] 區域中，使用者會指定位置識別碼。</span><span class="sxs-lookup"><span data-stu-id="30144-128">The location ID is specified by the user in the **Location** area of the Regional and Language Options settings in Control Panel.</span></span> |
| <span data-ttu-id="30144-129">*locale*</span><span class="sxs-lookup"><span data-stu-id="30144-129">*locale*</span></span>     | <span data-ttu-id="30144-130">Windows Media Player 地區設定識別碼。</span><span class="sxs-lookup"><span data-stu-id="30144-130">Windows Media Player locale ID.</span></span>                                                                                                                                     |
| <span data-ttu-id="30144-131">*userlocale*</span><span class="sxs-lookup"><span data-stu-id="30144-131">*userlocale*</span></span> | <span data-ttu-id="30144-132">Windows 地區設定識別碼。</span><span class="sxs-lookup"><span data-stu-id="30144-132">Windows locale ID.</span></span> <span data-ttu-id="30144-133">地區設定是由使用者在主控台的 [地區及語言選項] 設定的 [ **標準] 和 [格式** ] 區域中所指定。</span><span class="sxs-lookup"><span data-stu-id="30144-133">The locale is specified by the user in the **Standards and Formats** area of the Regional and Language Options settings in Control Panel.</span></span>        |
| <span data-ttu-id="30144-134">*version*</span><span class="sxs-lookup"><span data-stu-id="30144-134">*version*</span></span>    | <span data-ttu-id="30144-135">使用下列格式的 Windows Media Player 版本號碼： 10.0. x. x. x. x. x. x. x. x. x。</span><span class="sxs-lookup"><span data-stu-id="30144-135">Windows Media Player version number using the following format: 10.0.x.xxxx or 11.0.x.xxxx.</span></span>                                                                         |



 

## <a name="requirements"></a><span data-ttu-id="30144-136">規格需求</span><span class="sxs-lookup"><span data-stu-id="30144-136">Requirements</span></span>



| <span data-ttu-id="30144-137">需求</span><span class="sxs-lookup"><span data-stu-id="30144-137">Requirement</span></span> | <span data-ttu-id="30144-138">值</span><span class="sxs-lookup"><span data-stu-id="30144-138">Value</span></span> |
|--------------------|----------------------------------------------|
| <span data-ttu-id="30144-139">版本</span><span class="sxs-lookup"><span data-stu-id="30144-139">Version</span></span><br/> | <span data-ttu-id="30144-140">Windows Media Player 10 或更新版本。</span><span class="sxs-lookup"><span data-stu-id="30144-140">Windows Media Player 10 or later.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="30144-141">另請參閱</span><span class="sxs-lookup"><span data-stu-id="30144-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="30144-142">**類型1線上商店的範例 ServiceInfo 檔**</span><span class="sxs-lookup"><span data-stu-id="30144-142">**Example ServiceInfo Document for a Type 1 Online Store**</span></span>](example-serviceinfo-document-for-a-type-1-online-store.md)
</dt> <dt>

[<span data-ttu-id="30144-143">**Type 2 線上商店的範例 ServiceInfo 檔**</span><span class="sxs-lookup"><span data-stu-id="30144-143">**Example ServiceInfo Document for a Type 2 Online Store**</span></span>](example-serviceinfo-document-for-a-type-2-online-store.md)
</dt> <dt>

[<span data-ttu-id="30144-144">**ServiceInfo 檔**</span><span class="sxs-lookup"><span data-stu-id="30144-144">**ServiceInfo Document**</span></span>](serviceinfo-document.md)
</dt> </dl>

 

 





