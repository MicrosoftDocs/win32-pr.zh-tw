---
title: CDTrackEnabled 屬性
description: CDTrackEnabled 屬性會指出是否已啟用播放軌。
ms.assetid: ebbc42bd-2d6c-47ae-9a3f-c6256b120d35
keywords:
- CDTrackEnabled 屬性 Windows Media Player
topic_type:
- apiref
api_name:
- CDTrackEnabled
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c81c231dbdfc432ea7aa510a19b1f85e0826c836
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984449"
---
# <a name="cdtrackenabled-attribute"></a><span data-ttu-id="ebad3-104">CDTrackEnabled 屬性</span><span class="sxs-lookup"><span data-stu-id="ebad3-104">CDTrackEnabled Attribute</span></span>

<span data-ttu-id="ebad3-105">**CDTrackEnabled** 屬性會指出是否已啟用播放軌。</span><span class="sxs-lookup"><span data-stu-id="ebad3-105">The **CDTrackEnabled** attribute indicates whether the track is enabled for playback.</span></span>

## <a name="applies-to"></a><span data-ttu-id="ebad3-106">套用至</span><span class="sxs-lookup"><span data-stu-id="ebad3-106">Applies To</span></span>

-   [<span data-ttu-id="ebad3-107">CD 曲目</span><span class="sxs-lookup"><span data-stu-id="ebad3-107">CD Tracks</span></span>](cd-track-attributes.md)

## <a name="remarks"></a><span data-ttu-id="ebad3-108">備註</span><span class="sxs-lookup"><span data-stu-id="ebad3-108">Remarks</span></span>

<span data-ttu-id="ebad3-109">這個屬性只會儲存在程式庫快取中。</span><span class="sxs-lookup"><span data-stu-id="ebad3-109">This attribute is stored only in the library cache.</span></span>

<span data-ttu-id="ebad3-110">在 Windows Media Player 中播放 CD 時，使用者可以選取曲目並指定不應該播放。</span><span class="sxs-lookup"><span data-stu-id="ebad3-110">When playing a CD in Windows Media Player, the user may select a track and specify that it should not be played.</span></span> <span data-ttu-id="ebad3-111">如果可以播放此追蹤，這個屬性的值就是 True; 如果使用者指定不應該播放此播放軌，則為 False。</span><span class="sxs-lookup"><span data-stu-id="ebad3-111">This value of this attribute is True if the track can be played, or False if the user specified that the track should not be played.</span></span>

<span data-ttu-id="ebad3-112">若要判斷是否可以變更這個屬性的值，請使用 [isReadOnlyItem](media-isreadonlyitem.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="ebad3-112">To determine whether you can change the value of this attribute, use the [Media.isReadOnlyItem](media-isreadonlyitem.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="ebad3-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="ebad3-113">Requirements</span></span>



| <span data-ttu-id="ebad3-114">需求</span><span class="sxs-lookup"><span data-stu-id="ebad3-114">Requirement</span></span> | <span data-ttu-id="ebad3-115">值</span><span class="sxs-lookup"><span data-stu-id="ebad3-115">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="ebad3-116">版本</span><span class="sxs-lookup"><span data-stu-id="ebad3-116">Version</span></span><br/> | <span data-ttu-id="ebad3-117">Windows Media Player 9 系列或更新版本</span><span class="sxs-lookup"><span data-stu-id="ebad3-117">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ebad3-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ebad3-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ebad3-119">**屬性參考**</span><span class="sxs-lookup"><span data-stu-id="ebad3-119">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> </dl>

 

 





