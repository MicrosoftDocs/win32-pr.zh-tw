---
title: 'DownloadStatus 元素 (Msfeeds) '
description: '請注意，本節將說明針對線上商店使用而設計的功能。 |DownloadStatus 元素 (Msfeeds) '
ms.assetid: 08d9719a-390d-454a-935e-27812c0f3599
keywords:
- DownloadStatus 元素 Windows Media Player
topic_type:
- apiref
api_name:
- DownloadStatus Element
api_location:
- msfeeds.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 431da810a9591d891fca914a9ecb6d3146a651d8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106987172"
---
# <a name="downloadstatus-element"></a><span data-ttu-id="b2501-105">DownloadStatus 元素</span><span class="sxs-lookup"><span data-stu-id="b2501-105">DownloadStatus Element</span></span>

> [!Note]  
> <span data-ttu-id="b2501-106">本章節描述專為線上商店使用而設計的功能。</span><span class="sxs-lookup"><span data-stu-id="b2501-106">This section describes functionality designed for use by online stores.</span></span> <span data-ttu-id="b2501-107">不支援在線上商店的內容之外使用這項功能。</span><span class="sxs-lookup"><span data-stu-id="b2501-107">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="b2501-108">**DownloadStatus** 元素會指定 Windows Media Player 顯示為連結的 URL，讓使用者能夠查看下載狀態。</span><span class="sxs-lookup"><span data-stu-id="b2501-108">The **DownloadStatus** element specifies a URL the Windows Media Player displays as a link to enable users to view download status.</span></span>

``` syntax
<DownloadStatus
    URL = "URL"
/>
```

## <a name="attributes"></a><span data-ttu-id="b2501-109">屬性</span><span class="sxs-lookup"><span data-stu-id="b2501-109">Attributes</span></span>

<dl> <dt>

<span data-ttu-id="b2501-110"><span id="URL"></span><span id="url"></span>Url</span><span class="sxs-lookup"><span data-stu-id="b2501-110"><span id="URL"></span><span id="url"></span>URL</span></span>
</dt> <dd>

<span data-ttu-id="b2501-111">線上商店顯示的網頁 URL，可向使用者顯示下載狀態。</span><span class="sxs-lookup"><span data-stu-id="b2501-111">URL for the webpage that the online store displays to show download status to the user.</span></span>

</dd> </dl>

## <a name="parentchild-elements"></a><span data-ttu-id="b2501-112">父/子項目</span><span class="sxs-lookup"><span data-stu-id="b2501-112">Parent/Child Elements</span></span>



| <span data-ttu-id="b2501-113">階層</span><span class="sxs-lookup"><span data-stu-id="b2501-113">Hierarchy</span></span>       | <span data-ttu-id="b2501-114">元素</span><span class="sxs-lookup"><span data-stu-id="b2501-114">Element</span></span>         |
|-----------------|-----------------|
| <span data-ttu-id="b2501-115">父元素</span><span class="sxs-lookup"><span data-stu-id="b2501-115">Parent elements</span></span> | <span data-ttu-id="b2501-116">**ServiceInfo**</span><span class="sxs-lookup"><span data-stu-id="b2501-116">**ServiceInfo**</span></span> |
| <span data-ttu-id="b2501-117">子元素</span><span class="sxs-lookup"><span data-stu-id="b2501-117">Child elements</span></span>  | <span data-ttu-id="b2501-118">無</span><span class="sxs-lookup"><span data-stu-id="b2501-118">None</span></span>            |



 

## <a name="remarks"></a><span data-ttu-id="b2501-119">備註</span><span class="sxs-lookup"><span data-stu-id="b2501-119">Remarks</span></span>

<span data-ttu-id="b2501-120">Windows Media Player 會在下載進行時向使用者顯示訊息。</span><span class="sxs-lookup"><span data-stu-id="b2501-120">Windows Media Player displays a message to users when a download is in progress.</span></span> <span data-ttu-id="b2501-121">如果目前作用中的服務定義了下載狀態 URL，使用者可以按一下郵件內文。</span><span class="sxs-lookup"><span data-stu-id="b2501-121">If the current active services defines a download status URL, the user can click the message text.</span></span> <span data-ttu-id="b2501-122">當使用者按一下訊息時，播放程式會流覽至 **DownloadStatus** 元素所指定的 URL，讓目前的使用中存放區可以提供進行中下載的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="b2501-122">When the user clicks the message, the Player navigates to the URL specified by the **DownloadStatus** element so the current active store can provide details about downloads in progress.</span></span>

## <a name="requirements"></a><span data-ttu-id="b2501-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="b2501-123">Requirements</span></span>



| <span data-ttu-id="b2501-124">需求</span><span class="sxs-lookup"><span data-stu-id="b2501-124">Requirement</span></span> | <span data-ttu-id="b2501-125">值</span><span class="sxs-lookup"><span data-stu-id="b2501-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="b2501-126">版本</span><span class="sxs-lookup"><span data-stu-id="b2501-126">Version</span></span><br/> | <span data-ttu-id="b2501-127">Windows Media Player 10 或更新版本</span><span class="sxs-lookup"><span data-stu-id="b2501-127">Windows Media Player 10 or later</span></span><br/>                                          |
| <span data-ttu-id="b2501-128">標頭</span><span class="sxs-lookup"><span data-stu-id="b2501-128">Header</span></span><br/>  | <dl> <span data-ttu-id="b2501-129"><dt>Msfeeds。h</dt></span><span class="sxs-lookup"><span data-stu-id="b2501-129"><dt>Msfeeds.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b2501-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b2501-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b2501-131">**類型1線上商店的範例 ServiceInfo 檔**</span><span class="sxs-lookup"><span data-stu-id="b2501-131">**Example ServiceInfo Document for a Type 1 Online Store**</span></span>](example-serviceinfo-document-for-a-type-1-online-store.md)
</dt> <dt>

[<span data-ttu-id="b2501-132">**Type 2 線上商店的範例 ServiceInfo 檔**</span><span class="sxs-lookup"><span data-stu-id="b2501-132">**Example ServiceInfo Document for a Type 2 Online Store**</span></span>](example-serviceinfo-document-for-a-type-2-online-store.md)
</dt> <dt>

[<span data-ttu-id="b2501-133">**ServiceInfo 檔**</span><span class="sxs-lookup"><span data-stu-id="b2501-133">**ServiceInfo Document**</span></span>](serviceinfo-document.md)
</dt> </dl>

 

 





