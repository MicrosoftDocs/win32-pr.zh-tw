---
title: Author 屬性
description: Author 屬性是與內容相關聯之媒體演出者或動作專案的名稱。
ms.assetid: 6621a955-dd6b-4725-9690-0cc96e73d94f
keywords:
- Author 屬性 Windows Media Player
topic_type:
- apiref
api_name:
- Author
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e94ef73679aa3869a9a3d87b926b7f38464b1001
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106976143"
---
# <a name="author-attribute"></a><span data-ttu-id="317dc-104">Author 屬性</span><span class="sxs-lookup"><span data-stu-id="317dc-104">Author Attribute</span></span>

<span data-ttu-id="317dc-105">**Author** 屬性是與內容相關聯之媒體演出者或動作專案的名稱。</span><span class="sxs-lookup"><span data-stu-id="317dc-105">The **Author** attribute is the name of a media artist or actor associated with the content.</span></span>

## <a name="applies-to"></a><span data-ttu-id="317dc-106">套用至</span><span class="sxs-lookup"><span data-stu-id="317dc-106">Applies To</span></span>

-   [<span data-ttu-id="317dc-107">音訊專案</span><span class="sxs-lookup"><span data-stu-id="317dc-107">Audio Items</span></span>](audio-item-attributes.md)
-   [<span data-ttu-id="317dc-108">CD 播放清單</span><span class="sxs-lookup"><span data-stu-id="317dc-108">CD Playlists</span></span>](cd-playlist-attributes.md)
-   [<span data-ttu-id="317dc-109">CD 曲目</span><span class="sxs-lookup"><span data-stu-id="317dc-109">CD Tracks</span></span>](cd-track-attributes.md)
-   [<span data-ttu-id="317dc-110">常用的 Windows Media 檔案</span><span class="sxs-lookup"><span data-stu-id="317dc-110">Commonly Used Windows Media Files</span></span>](commonly-used-windows-media-file-attributes.md)
-   [<span data-ttu-id="317dc-111">DVD</span><span class="sxs-lookup"><span data-stu-id="317dc-111">DVDs</span></span>](dvd-attributes.md)
-   [<span data-ttu-id="317dc-112">GetItemInfoByType</span><span class="sxs-lookup"><span data-stu-id="317dc-112">Media.getItemInfoByType</span></span>](media-getiteminfobytype.md)
-   [<span data-ttu-id="317dc-113">相片專案</span><span class="sxs-lookup"><span data-stu-id="317dc-113">Photo Items</span></span>](photo-item-attributes.md)
-   [<span data-ttu-id="317dc-114">播放清單</span><span class="sxs-lookup"><span data-stu-id="317dc-114">Playlists</span></span>](playlist-attributes-ref.md)
-   [<span data-ttu-id="317dc-115">單選項目</span><span class="sxs-lookup"><span data-stu-id="317dc-115">Radio Items</span></span>](radio-item-attributes.md)
-   [<span data-ttu-id="317dc-116">影片專案</span><span class="sxs-lookup"><span data-stu-id="317dc-116">Video Items</span></span>](video-item-attributes.md)

## <a name="remarks"></a><span data-ttu-id="317dc-117">備註</span><span class="sxs-lookup"><span data-stu-id="317dc-117">Remarks</span></span>

<span data-ttu-id="317dc-118">這個屬性會儲存在程式庫 (或快取) 和媒體檔案中。</span><span class="sxs-lookup"><span data-stu-id="317dc-118">This attribute is stored in both the library (or cache) and the media file.</span></span>

<span data-ttu-id="317dc-119">這個屬性可以有多個值。</span><span class="sxs-lookup"><span data-stu-id="317dc-119">This attribute may have multiple values.</span></span> <span data-ttu-id="317dc-120">若要取得多重值屬性的所有值，您必須使用 *媒體*。**getItemInfoByType** 方法，而不是 *媒體*。**getItemInfo** 方法。</span><span class="sxs-lookup"><span data-stu-id="317dc-120">To retrieve all of the values for a multi-valued attribute, you must use the *Media*.**getItemInfoByType** method, not the *Media*.**getItemInfo** method.</span></span>

<span data-ttu-id="317dc-121">這個屬性的 Windows Media Format SDK 常數是 g \_ wszWMAuthor。</span><span class="sxs-lookup"><span data-stu-id="317dc-121">The Windows Media Format SDK constant for this attribute is g\_wszWMAuthor.</span></span>

<span data-ttu-id="317dc-122">**執行者** 和 **演出者** 是這個屬性的別名。</span><span class="sxs-lookup"><span data-stu-id="317dc-122">**Actor** and **Artist** are aliases for this attribute.</span></span>

<span data-ttu-id="317dc-123">若要判斷是否可以變更這個屬性的值，請使用 [isReadOnlyItem](media-isreadonlyitem.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="317dc-123">To determine whether you can change the value of this attribute, use the [Media.isReadOnlyItem](media-isreadonlyitem.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="317dc-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="317dc-124">Requirements</span></span>



| <span data-ttu-id="317dc-125">需求</span><span class="sxs-lookup"><span data-stu-id="317dc-125">Requirement</span></span> | <span data-ttu-id="317dc-126">值</span><span class="sxs-lookup"><span data-stu-id="317dc-126">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="317dc-127">版本</span><span class="sxs-lookup"><span data-stu-id="317dc-127">Version</span></span><br/> | <span data-ttu-id="317dc-128">Windows Media Player 9 系列或更新版本</span><span class="sxs-lookup"><span data-stu-id="317dc-128">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="317dc-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="317dc-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="317dc-130">**屬性參考**</span><span class="sxs-lookup"><span data-stu-id="317dc-130">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> </dl>

 

 





