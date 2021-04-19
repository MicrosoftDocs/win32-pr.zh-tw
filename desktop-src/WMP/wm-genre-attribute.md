---
title: WM/內容類型屬性
description: WM/內容屬性是內容的內容類型。
ms.assetid: 4b1b0512-d8fd-402a-a5f0-1002c64194f4
keywords:
- WM/內容類型屬性 Windows Media Player
topic_type:
- apiref
api_name:
- WM/Genre
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aae4a0c6ae27e85fa1ed147a3173c4cc31b20f1b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106989775"
---
# <a name="wmgenre-attribute"></a><span data-ttu-id="b9484-104">WM/內容類型屬性</span><span class="sxs-lookup"><span data-stu-id="b9484-104">WM/Genre Attribute</span></span>

<span data-ttu-id="b9484-105">**WM/** 內容屬性是內容的內容類型。</span><span class="sxs-lookup"><span data-stu-id="b9484-105">The **WM/Genre** attribute is the genre of the content.</span></span>

## <a name="applies-to"></a><span data-ttu-id="b9484-106">套用至</span><span class="sxs-lookup"><span data-stu-id="b9484-106">Applies To</span></span>

-   [<span data-ttu-id="b9484-107">音訊專案</span><span class="sxs-lookup"><span data-stu-id="b9484-107">Audio Items</span></span>](audio-item-attributes.md)
-   [<span data-ttu-id="b9484-108">CD 播放清單</span><span class="sxs-lookup"><span data-stu-id="b9484-108">CD Playlists</span></span>](cd-playlist-attributes.md)
-   [<span data-ttu-id="b9484-109">CD 曲目</span><span class="sxs-lookup"><span data-stu-id="b9484-109">CD Tracks</span></span>](cd-track-attributes.md)
-   [<span data-ttu-id="b9484-110">常用的 Windows Media 檔案屬性</span><span class="sxs-lookup"><span data-stu-id="b9484-110">Commonly Used Windows Media File Attributes</span></span>](commonly-used-windows-media-file-attributes.md)
-   [<span data-ttu-id="b9484-111">DVD</span><span class="sxs-lookup"><span data-stu-id="b9484-111">DVDs</span></span>](dvd-attributes.md)
-   [<span data-ttu-id="b9484-112">其他專案</span><span class="sxs-lookup"><span data-stu-id="b9484-112">Other Items</span></span>](other-item-attributes.md)
-   [<span data-ttu-id="b9484-113">播放清單</span><span class="sxs-lookup"><span data-stu-id="b9484-113">Playlists</span></span>](playlist-attributes-ref.md)
-   [<span data-ttu-id="b9484-114">影片專案</span><span class="sxs-lookup"><span data-stu-id="b9484-114">Video Items</span></span>](video-item-attributes.md)

## <a name="remarks"></a><span data-ttu-id="b9484-115">備註</span><span class="sxs-lookup"><span data-stu-id="b9484-115">Remarks</span></span>

<span data-ttu-id="b9484-116">這個屬性會儲存在程式庫 (或快取) 和數位媒體檔案中。</span><span class="sxs-lookup"><span data-stu-id="b9484-116">This attribute is stored in both the library (or cache) and the digital media file.</span></span>

<span data-ttu-id="b9484-117">這個屬性可以有多個值。</span><span class="sxs-lookup"><span data-stu-id="b9484-117">This attribute may have multiple values.</span></span> <span data-ttu-id="b9484-118">若要取得多重值屬性的所有值，您必須使用 **getItemInfoByType** 方法，而不是 **getItemInfo** 方法。</span><span class="sxs-lookup"><span data-stu-id="b9484-118">To retrieve all of the values for a multi-valued attribute, you must use the **Media.getItemInfoByType** method, not the **Media.getItemInfo** method.</span></span>

<span data-ttu-id="b9484-119">內容 **類型是此** 屬性的別名。</span><span class="sxs-lookup"><span data-stu-id="b9484-119">**Genre** is an alias for this attribute.</span></span>

<span data-ttu-id="b9484-120">這個屬性的 Windows Media Format SDK 常數是 g \_ wszWMGenre。</span><span class="sxs-lookup"><span data-stu-id="b9484-120">The Windows Media Format SDK constant for this attribute is g\_wszWMGenre.</span></span>

<span data-ttu-id="b9484-121">若要判斷是否可以變更這個屬性的值，請使用 [isReadOnlyItem](media-isreadonlyitem.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="b9484-121">To determine whether you can change the value of this attribute, use the [Media.isReadOnlyItem](media-isreadonlyitem.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="b9484-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="b9484-122">Requirements</span></span>



| <span data-ttu-id="b9484-123">需求</span><span class="sxs-lookup"><span data-stu-id="b9484-123">Requirement</span></span> | <span data-ttu-id="b9484-124">值</span><span class="sxs-lookup"><span data-stu-id="b9484-124">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="b9484-125">版本</span><span class="sxs-lookup"><span data-stu-id="b9484-125">Version</span></span><br/> | <span data-ttu-id="b9484-126">Windows Media Player 9 系列或更新版本</span><span class="sxs-lookup"><span data-stu-id="b9484-126">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b9484-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b9484-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b9484-128">**屬性參考**</span><span class="sxs-lookup"><span data-stu-id="b9484-128">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> <dt>

[<span data-ttu-id="b9484-129">**GetItemInfoByType**</span><span class="sxs-lookup"><span data-stu-id="b9484-129">**Media.getItemInfoByType**</span></span>](media-getiteminfobytype.md)
</dt> </dl>

 

 





