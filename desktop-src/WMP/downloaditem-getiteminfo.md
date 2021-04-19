---
title: DownloadItem. getItemInfo 方法
description: 請注意，本節將說明針對線上商店使用而設計的功能。 不支援在線上商店的內容之外使用這項功能。 GetItemInfo 方法會抓取下載專案的屬性值。
ms.assetid: da885611-b4a0-4264-8b32-13cc6f87d6e9
keywords:
- getItemInfo 方法 Windows Media Player
- getItemInfo 方法 Windows Media Player，DownloadItem 類別
- DownloadItem 類別 Windows Media Player，getItemInfo 方法
topic_type:
- apiref
api_name:
- DownloadItem.getItemInfo
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1367e5c7a8990a9172ee758d2b811b9074ed02fc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106992860"
---
# <a name="downloaditemgetiteminfo-method"></a><span data-ttu-id="ba1e5-108">DownloadItem. getItemInfo 方法</span><span class="sxs-lookup"><span data-stu-id="ba1e5-108">DownloadItem.getItemInfo method</span></span>

> [!Note]  
> <span data-ttu-id="ba1e5-109">本章節描述專為線上商店使用而設計的功能。</span><span class="sxs-lookup"><span data-stu-id="ba1e5-109">This section describes functionality designed for use by online stores.</span></span> <span data-ttu-id="ba1e5-110">不支援在線上商店的內容之外使用這項功能。</span><span class="sxs-lookup"><span data-stu-id="ba1e5-110">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="ba1e5-111">**GetItemInfo** 方法會抓取下載專案的屬性值。</span><span class="sxs-lookup"><span data-stu-id="ba1e5-111">The **getItemInfo** method retrieves the value of an attribute for the download item.</span></span>

## <a name="syntax"></a><span data-ttu-id="ba1e5-112">語法</span><span class="sxs-lookup"><span data-stu-id="ba1e5-112">Syntax</span></span>


```JScript
strRetVal = DownloadItem.getItemInfo(
  itemname
)
```



## <a name="parameters"></a><span data-ttu-id="ba1e5-113">參數</span><span class="sxs-lookup"><span data-stu-id="ba1e5-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ba1e5-114">的是 \[在\]</span><span class="sxs-lookup"><span data-stu-id="ba1e5-114">*itemname* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ba1e5-115">包含屬性名稱的 **字串**。</span><span class="sxs-lookup"><span data-stu-id="ba1e5-115">**String** containing the attribute name.</span></span> <span data-ttu-id="ba1e5-116">支援的值為 AlbumArtist、專輯、Duration、WM/Provider、Title、UserRating 和 WM/TrackNumber。</span><span class="sxs-lookup"><span data-stu-id="ba1e5-116">Supported values are AlbumArtist, Album, Duration, WM/Provider, Title, UserRating, and WM/TrackNumber.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ba1e5-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="ba1e5-117">Return value</span></span>

<span data-ttu-id="ba1e5-118">這個方法會傳回 **字串** ，其中 *包含依元素* 指定的屬性值。</span><span class="sxs-lookup"><span data-stu-id="ba1e5-118">This method returns a **String** containing the value of the attribute specified by *itemname*.</span></span>

## <a name="remarks"></a><span data-ttu-id="ba1e5-119">備註</span><span class="sxs-lookup"><span data-stu-id="ba1e5-119">Remarks</span></span>

<span data-ttu-id="ba1e5-120">這個方法會使用 BITS 描述字串來抓取指定的屬性。</span><span class="sxs-lookup"><span data-stu-id="ba1e5-120">This method retrieves attributes specified using the BITS description string.</span></span> <span data-ttu-id="ba1e5-121">請參閱 [WINDOWS MEDIA PLAYER BITS 作業慣例](windows-media-player-bits-job-convention.md)。</span><span class="sxs-lookup"><span data-stu-id="ba1e5-121">See [Windows Media Player BITS Job Convention](windows-media-player-bits-job-convention.md).</span></span>

<span data-ttu-id="ba1e5-122">此方法支援背景下載。</span><span class="sxs-lookup"><span data-stu-id="ba1e5-122">This method is supported for background downloading.</span></span> <span data-ttu-id="ba1e5-123">使用即時下載時，您的程式碼不應呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="ba1e5-123">Your code should not call this method when using real-time downloading.</span></span>

<span data-ttu-id="ba1e5-124">這個方法可以取得目前 Windows Media Player 會話期間所新增之 BITS 工作的資訊。</span><span class="sxs-lookup"><span data-stu-id="ba1e5-124">This method can retrieve information for BITS jobs added during the current Windows Media Player session only.</span></span>

## <a name="requirements"></a><span data-ttu-id="ba1e5-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="ba1e5-125">Requirements</span></span>



| <span data-ttu-id="ba1e5-126">需求</span><span class="sxs-lookup"><span data-stu-id="ba1e5-126">Requirement</span></span> | <span data-ttu-id="ba1e5-127">值</span><span class="sxs-lookup"><span data-stu-id="ba1e5-127">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ba1e5-128">版本</span><span class="sxs-lookup"><span data-stu-id="ba1e5-128">Version</span></span><br/> | <span data-ttu-id="ba1e5-129">Windows Media Player 10 或更新版本</span><span class="sxs-lookup"><span data-stu-id="ba1e5-129">Windows Media Player 10 or later</span></span><br/>                                        |
| <span data-ttu-id="ba1e5-130">DLL</span><span class="sxs-lookup"><span data-stu-id="ba1e5-130">DLL</span></span><br/>     | <dl> <span data-ttu-id="ba1e5-131"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ba1e5-131"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ba1e5-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ba1e5-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ba1e5-133">**DownloadItem。類型**</span><span class="sxs-lookup"><span data-stu-id="ba1e5-133">**DownloadItem.type**</span></span>](downloaditem-type.md)
</dt> <dt>

[<span data-ttu-id="ba1e5-134">**DownloadItem 物件**</span><span class="sxs-lookup"><span data-stu-id="ba1e5-134">**DownloadItem Object**</span></span>](downloaditem-object.md)
</dt> </dl>

 

 





