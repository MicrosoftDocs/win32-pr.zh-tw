---
title: HTMLView 元素
description: 請注意，本節將說明針對線上商店使用而設計的功能。 不支援在線上商店的內容之外使用這項功能。 HTMLView 元素會指定 HTMLView 網頁的基底 URL。
ms.assetid: 741db1ed-9452-4cae-9185-15668abe06b3
keywords:
- HTMLView 元素 Windows Media Player
topic_type:
- apiref
api_name:
- HTMLView Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f11a60e41b7f78be3440e16a7d2b3934f75e8ee3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106989596"
---
# <a name="htmlview-element"></a><span data-ttu-id="412bb-106">HTMLView 元素</span><span class="sxs-lookup"><span data-stu-id="412bb-106">HTMLView Element</span></span>

> [!Note]  
> <span data-ttu-id="412bb-107">本章節描述專為線上商店使用而設計的功能。</span><span class="sxs-lookup"><span data-stu-id="412bb-107">This section describes functionality designed for use by online stores.</span></span> <span data-ttu-id="412bb-108">不支援在線上商店的內容之外使用這項功能。</span><span class="sxs-lookup"><span data-stu-id="412bb-108">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="412bb-109">**HTMLView** 元素會指定 HTMLView 網頁的基底 URL。</span><span class="sxs-lookup"><span data-stu-id="412bb-109">The **HTMLView** element specifies the base URL of an HTMLView webpage.</span></span>

``` syntax
<HTMLView
    BaseURL = "URL"
/>
```

## <a name="attributes"></a><span data-ttu-id="412bb-110">屬性</span><span class="sxs-lookup"><span data-stu-id="412bb-110">Attributes</span></span>

<dl> <dt>

<span data-ttu-id="412bb-111"><span id="BaseURL__required_"></span><span id="baseurl__required_"></span><span id="BASEURL__REQUIRED_"></span>**BaseURL** (必要) </span><span class="sxs-lookup"><span data-stu-id="412bb-111"><span id="BaseURL__required_"></span><span id="baseurl__required_"></span><span id="BASEURL__REQUIRED_"></span>**BaseURL** (required)</span></span>
</dt> <dd>

<span data-ttu-id="412bb-112">Windows Media Player 顯示之 HTMLView 網頁的基底 URL。</span><span class="sxs-lookup"><span data-stu-id="412bb-112">Base URL for the HTMLView webpage that Windows Media Player displays.</span></span>

</dd> </dl>

## <a name="parentchild-elements"></a><span data-ttu-id="412bb-113">父/子項目</span><span class="sxs-lookup"><span data-stu-id="412bb-113">Parent/Child Elements</span></span>



| <span data-ttu-id="412bb-114">階層</span><span class="sxs-lookup"><span data-stu-id="412bb-114">Hierarchy</span></span>       | <span data-ttu-id="412bb-115">元素</span><span class="sxs-lookup"><span data-stu-id="412bb-115">Element</span></span>         |
|-----------------|-----------------|
| <span data-ttu-id="412bb-116">父元素</span><span class="sxs-lookup"><span data-stu-id="412bb-116">Parent elements</span></span> | <span data-ttu-id="412bb-117">**ServiceInfo**</span><span class="sxs-lookup"><span data-stu-id="412bb-117">**ServiceInfo**</span></span> |
| <span data-ttu-id="412bb-118">子元素</span><span class="sxs-lookup"><span data-stu-id="412bb-118">Child elements</span></span>  | <span data-ttu-id="412bb-119">無</span><span class="sxs-lookup"><span data-stu-id="412bb-119">None</span></span>            |



 

## <a name="remarks"></a><span data-ttu-id="412bb-120">備註</span><span class="sxs-lookup"><span data-stu-id="412bb-120">Remarks</span></span>

<span data-ttu-id="412bb-121">您可以使用此元素，將 HTMLView 功能與您的線上商店整合。</span><span class="sxs-lookup"><span data-stu-id="412bb-121">You can use this element to integrate the HTMLView feature with your online store.</span></span> <span data-ttu-id="412bb-122">如果目前線上商店所指定的 URL 網域與 HTMLView 網頁的網域相符，就會在沒有使用者介入的情況下， **立即播放** 的參數，並顯示 HTMLView 內容。</span><span class="sxs-lookup"><span data-stu-id="412bb-122">If the domain of the URL specified by the current online store matches the one for the HTMLView webpage, the switch to **Now Playing** happens without user intervention and the HTMLView content is displayed.</span></span> <span data-ttu-id="412bb-123">否則，Windows Media Player 會提示使用者顯示 HTMLView 內容的許可權。</span><span class="sxs-lookup"><span data-stu-id="412bb-123">Otherwise, Windows Media Player prompts the user for permission to show the HTMLView content.</span></span>

<span data-ttu-id="412bb-124">例如，如果 HTMLView 網頁的 URL 為 https://www.proseware.com/html/HTMLView.htm ，而且 **BaseURL** 屬性的 url 指定為 https://www.proseware.com ，則會顯示 HTMLView 網頁，而不會提示使用者。</span><span class="sxs-lookup"><span data-stu-id="412bb-124">For example, if the URL for the HTMLView webpage is https://www.proseware.com/html/HTMLView.htm and the URL for the **BaseURL** attribute is specified as https://www.proseware.com, the HTMLView webpage displays without prompting the user.</span></span>

## <a name="requirements"></a><span data-ttu-id="412bb-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="412bb-125">Requirements</span></span>



| <span data-ttu-id="412bb-126">需求</span><span class="sxs-lookup"><span data-stu-id="412bb-126">Requirement</span></span> | <span data-ttu-id="412bb-127">值</span><span class="sxs-lookup"><span data-stu-id="412bb-127">Value</span></span> |
|--------------------|---------------------------------------------|
| <span data-ttu-id="412bb-128">版本</span><span class="sxs-lookup"><span data-stu-id="412bb-128">Version</span></span><br/> | <span data-ttu-id="412bb-129">Windows Media Player 10 或更新版本</span><span class="sxs-lookup"><span data-stu-id="412bb-129">Windows Media Player 10 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="412bb-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="412bb-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="412bb-131">**顯示 Windows Media Player 中的網頁**</span><span class="sxs-lookup"><span data-stu-id="412bb-131">**Displaying Web Pages in Windows Media Player**</span></span>](displaying-web-pages-in-windows-media-player.md)
</dt> <dt>

[<span data-ttu-id="412bb-132">**類型1線上商店的範例 ServiceInfo 檔**</span><span class="sxs-lookup"><span data-stu-id="412bb-132">**Example ServiceInfo Document for a Type 1 Online Store**</span></span>](example-serviceinfo-document-for-a-type-1-online-store.md)
</dt> <dt>

[<span data-ttu-id="412bb-133">**Type 2 線上商店的範例 ServiceInfo 檔**</span><span class="sxs-lookup"><span data-stu-id="412bb-133">**Example ServiceInfo Document for a Type 2 Online Store**</span></span>](example-serviceinfo-document-for-a-type-2-online-store.md)
</dt> <dt>

[<span data-ttu-id="412bb-134">**PARAM 元素**</span><span class="sxs-lookup"><span data-stu-id="412bb-134">**PARAM Element**</span></span>](param-element.md)
</dt> <dt>

[<span data-ttu-id="412bb-135">**ServiceInfo 檔**</span><span class="sxs-lookup"><span data-stu-id="412bb-135">**ServiceInfo Document**</span></span>](serviceinfo-document.md)
</dt> </dl>

 

 





