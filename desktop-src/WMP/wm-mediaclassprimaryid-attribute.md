---
title: WM/MediaClassPrimaryID 屬性
description: WM/MediaClassPrimaryID 屬性是 GUID，用來指定其中一種主要媒體類別音樂、非音樂音訊、影片或其他。
ms.assetid: eb78f4a9-7c18-4cad-bb34-fd1ff15bad4f
keywords:
- WM/MediaClassPrimaryID 屬性 Windows Media Player
topic_type:
- apiref
api_name:
- WM/MediaClassPrimaryID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5107a2c4e04e9424bf0a20a7d4cf7b8edef80492
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994038"
---
# <a name="wmmediaclassprimaryid-attribute"></a><span data-ttu-id="8ca67-104">WM/MediaClassPrimaryID 屬性</span><span class="sxs-lookup"><span data-stu-id="8ca67-104">WM/MediaClassPrimaryID Attribute</span></span>

<span data-ttu-id="8ca67-105">**WM/MediaClassPrimaryID** 屬性是指定其中一個主要媒體類別的 GUID：音樂、非音樂音訊、影片或其他。</span><span class="sxs-lookup"><span data-stu-id="8ca67-105">The **WM/MediaClassPrimaryID** attribute is a GUID specifying one of the primary media classes: music, non-music audio, video, or other.</span></span>

## <a name="applies-to"></a><span data-ttu-id="8ca67-106">套用至</span><span class="sxs-lookup"><span data-stu-id="8ca67-106">Applies To</span></span>

-   [<span data-ttu-id="8ca67-107">音訊專案</span><span class="sxs-lookup"><span data-stu-id="8ca67-107">Audio Items</span></span>](audio-item-attributes.md)
-   [<span data-ttu-id="8ca67-108">常用的 Windows Media 檔案屬性</span><span class="sxs-lookup"><span data-stu-id="8ca67-108">Commonly Used Windows Media File Attributes</span></span>](commonly-used-windows-media-file-attributes.md)
-   [<span data-ttu-id="8ca67-109">其他專案</span><span class="sxs-lookup"><span data-stu-id="8ca67-109">Other Items</span></span>](other-item-attributes.md)
-   [<span data-ttu-id="8ca67-110">相片專案</span><span class="sxs-lookup"><span data-stu-id="8ca67-110">Photo Items</span></span>](photo-item-attributes.md)
-   [<span data-ttu-id="8ca67-111">播放清單</span><span class="sxs-lookup"><span data-stu-id="8ca67-111">Playlists</span></span>](playlist-attributes-ref.md)
-   [<span data-ttu-id="8ca67-112">單選項目</span><span class="sxs-lookup"><span data-stu-id="8ca67-112">Radio Items</span></span>](radio-item-attributes.md)
-   [<span data-ttu-id="8ca67-113">影片專案</span><span class="sxs-lookup"><span data-stu-id="8ca67-113">Video Items</span></span>](video-item-attributes.md)

## <a name="remarks"></a><span data-ttu-id="8ca67-114">備註</span><span class="sxs-lookup"><span data-stu-id="8ca67-114">Remarks</span></span>

<span data-ttu-id="8ca67-115">這個屬性會儲存在文件庫和數位媒體檔案中。</span><span class="sxs-lookup"><span data-stu-id="8ca67-115">This attribute is stored in both the library and the digital media file.</span></span>

<span data-ttu-id="8ca67-116">**MediaClassPrimaryID** 是此屬性的別名。</span><span class="sxs-lookup"><span data-stu-id="8ca67-116">**MediaClassPrimaryID** is an alias for this attribute.</span></span>

<span data-ttu-id="8ca67-117">這個屬性的 Windows Media Format SDK 常數是 g \_ wszWMMediaClassPrimaryID。</span><span class="sxs-lookup"><span data-stu-id="8ca67-117">The Windows Media Format SDK constant for this attribute is g\_wszWMMediaClassPrimaryID.</span></span>

<span data-ttu-id="8ca67-118">若要判斷是否可以變更這個屬性的值，請使用 [isReadOnlyItem](media-isreadonlyitem.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="8ca67-118">To determine whether you can change the value of this attribute, use the [Media.isReadOnlyItem](media-isreadonlyitem.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="8ca67-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="8ca67-119">Requirements</span></span>



| <span data-ttu-id="8ca67-120">需求</span><span class="sxs-lookup"><span data-stu-id="8ca67-120">Requirement</span></span> | <span data-ttu-id="8ca67-121">值</span><span class="sxs-lookup"><span data-stu-id="8ca67-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8ca67-122">版本</span><span class="sxs-lookup"><span data-stu-id="8ca67-122">Version</span></span><br/> | <span data-ttu-id="8ca67-123">Windows Media Player 9 系列或更新版本 (只有 Windows Media Player 10 或更新版本才支援相片專案) </span><span class="sxs-lookup"><span data-stu-id="8ca67-123">Windows Media Player 9 Series or later (The photo item is supported only in Windows Media Player 10 or later)</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="8ca67-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8ca67-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8ca67-125">**屬性參考**</span><span class="sxs-lookup"><span data-stu-id="8ca67-125">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> </dl>

 

 





