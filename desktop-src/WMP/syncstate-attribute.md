---
title: SyncState 屬性
description: SyncState 屬性是32位值的字串表示，當它與可攜式裝置同步播放清單時，Windows Media Player 使用此值。
ms.assetid: affc3d1c-7fe6-4811-acfc-57285cb181ca
keywords:
- SyncState 屬性 Windows Media Player
topic_type:
- apiref
api_name:
- SyncState
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a948f6c649d548b375ccb676134177b0273c85c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994606"
---
# <a name="syncstate-attribute"></a><span data-ttu-id="12655-104">SyncState 屬性</span><span class="sxs-lookup"><span data-stu-id="12655-104">SyncState Attribute</span></span>

<span data-ttu-id="12655-105">**SyncState** 屬性是32位值的字串表示，當它與可攜式裝置同步播放清單時，Windows Media Player 使用此值。</span><span class="sxs-lookup"><span data-stu-id="12655-105">The **SyncState** attribute is a string representation of a 32-bit value that Windows Media Player uses when it synchronizes playlists with portable devices.</span></span>

## <a name="applies-to"></a><span data-ttu-id="12655-106">套用至</span><span class="sxs-lookup"><span data-stu-id="12655-106">Applies To</span></span>

-   [<span data-ttu-id="12655-107">音訊專案</span><span class="sxs-lookup"><span data-stu-id="12655-107">Audio Items</span></span>](audio-item-attributes.md)
-   [<span data-ttu-id="12655-108">其他專案</span><span class="sxs-lookup"><span data-stu-id="12655-108">Other Items</span></span>](other-item-attributes.md)
-   [<span data-ttu-id="12655-109">相片專案</span><span class="sxs-lookup"><span data-stu-id="12655-109">Photo Items</span></span>](photo-item-attributes.md)
-   [<span data-ttu-id="12655-110">影片專案</span><span class="sxs-lookup"><span data-stu-id="12655-110">Video Items</span></span>](video-item-attributes.md)

## <a name="remarks"></a><span data-ttu-id="12655-111">備註</span><span class="sxs-lookup"><span data-stu-id="12655-111">Remarks</span></span>

<span data-ttu-id="12655-112">這個屬性是由 16 2 位值所組成，每個值都會指定可攜式裝置的同步處理狀態。</span><span class="sxs-lookup"><span data-stu-id="12655-112">This attribute consists of sixteen 2-bit values, each of which specifies the synchronization state of a portable device.</span></span> <span data-ttu-id="12655-113">此32位值 (MSB) 最重要的位會對應至裝置16。</span><span class="sxs-lookup"><span data-stu-id="12655-113">The most significant bit (MSB) of this 32-bit value corresponds to device 16.</span></span> <span data-ttu-id="12655-114"> (LSB) 相對於裝置1最不重要的位。</span><span class="sxs-lookup"><span data-stu-id="12655-114">The least significant bit (LSB) corresponds to device 1.</span></span>

<span data-ttu-id="12655-115">每個2位值的 MSB 會指出 Windows Media Player 是否與對應的裝置同步處理內容。</span><span class="sxs-lookup"><span data-stu-id="12655-115">The MSB of each 2-bit value indicates whether Windows Media Player synchronized the content with the corresponding device.</span></span> <span data-ttu-id="12655-116">值為1表示它已完成。</span><span class="sxs-lookup"><span data-stu-id="12655-116">A value of 1 indicates that it did.</span></span> <span data-ttu-id="12655-117">值為0表示它不是。</span><span class="sxs-lookup"><span data-stu-id="12655-117">A value of 0 indicates that it did not.</span></span>

<span data-ttu-id="12655-118">如果 MSB 為0，則 LSB 會指定同步處理失敗的原因。</span><span class="sxs-lookup"><span data-stu-id="12655-118">If the MSB is 0, the LSB specifies why the synchronization failed.</span></span> <span data-ttu-id="12655-119">LSB 中的值為1，表示沒有足夠的可用空間來容納內容。</span><span class="sxs-lookup"><span data-stu-id="12655-119">A value of 1 in the LSB indicates that there was not enough free space for the content.</span></span> <span data-ttu-id="12655-120">LSB 中的值為0，表示某些其他原因導致無法同步處理。</span><span class="sxs-lookup"><span data-stu-id="12655-120">A value of 0 in the LSB indicates some other reason prevented synchronization.</span></span>

<span data-ttu-id="12655-121">若要取得指定裝置的同步處理狀態，請執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="12655-121">To retrieve the synchronization state of a given device, you should do the following:</span></span>

1.  <span data-ttu-id="12655-122">叫用 **IWMPSyncDevice：： get \_ 狀態** ，以判斷指定的裝置是否已同步處理。</span><span class="sxs-lookup"><span data-stu-id="12655-122">Invoke **IWMPSyncDevice::get\_status** to determine whether a given device is synchronized.</span></span>
2.  <span data-ttu-id="12655-123">如果已同步處理，請叫用 **IWMPSyncDevice：： get \_ partnershipIndex** ，以在 **SyncState** 屬性中取得裝置位組的索引。</span><span class="sxs-lookup"><span data-stu-id="12655-123">If it is synchronized, invoke **IWMPSyncDevice::get\_partnershipIndex** to retrieve the index of the device's bit pair in the **SyncState** attribute.</span></span>
3.  <span data-ttu-id="12655-124">使用這個索引，將 **SyncState** 屬性的對應位組加上遮罩，並檢查結果以判斷播放清單與裝置的同步處理狀態。</span><span class="sxs-lookup"><span data-stu-id="12655-124">Using this index, mask the corresponding bit pair of the **SyncState** attribute and examine the result to determine the synchronization state of the playlist with the device.</span></span>

<span data-ttu-id="12655-125">若要判斷是否可以變更這個屬性的值，請使用 [isReadOnlyItem](media-isreadonlyitem.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="12655-125">To determine whether you can change the value of this attribute, use the [Media.isReadOnlyItem](media-isreadonlyitem.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="12655-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="12655-126">Requirements</span></span>



| <span data-ttu-id="12655-127">需求</span><span class="sxs-lookup"><span data-stu-id="12655-127">Requirement</span></span> | <span data-ttu-id="12655-128">值</span><span class="sxs-lookup"><span data-stu-id="12655-128">Value</span></span> |
|--------------------|---------------------------------------------|
| <span data-ttu-id="12655-129">版本</span><span class="sxs-lookup"><span data-stu-id="12655-129">Version</span></span><br/> | <span data-ttu-id="12655-130">Windows Media Player 10 或更新版本</span><span class="sxs-lookup"><span data-stu-id="12655-130">Windows Media Player 10 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="12655-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="12655-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="12655-132">**屬性參考**</span><span class="sxs-lookup"><span data-stu-id="12655-132">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> <dt>

[<span data-ttu-id="12655-133">**判斷播放清單同步處理狀態**</span><span class="sxs-lookup"><span data-stu-id="12655-133">**Determining Playlist Synchronization State**</span></span>](determining-playlist-synchronization-state.md)
</dt> <dt>

[<span data-ttu-id="12655-134">**IWMPSyncDevice：： get \_ partnershipIndex**</span><span class="sxs-lookup"><span data-stu-id="12655-134">**IWMPSyncDevice::get\_partnershipIndex**</span></span>](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-get_partnershipindex)
</dt> <dt>

[<span data-ttu-id="12655-135">**IWMPSyncDevice：： get \_ 狀態**</span><span class="sxs-lookup"><span data-stu-id="12655-135">**IWMPSyncDevice::get\_status**</span></span>](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-get_status)
</dt> </dl>

 

 





