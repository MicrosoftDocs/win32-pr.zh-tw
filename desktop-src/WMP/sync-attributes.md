---
title: 同步屬性
description: Sync01 至 Sync16 屬性是32位值的字串表示，當它與多達16部可攜式裝置的其中一個同步播放清單時，Windows Media Player 會使用這些值。
ms.assetid: b9ae3420-aa09-4969-8637-f16d438942f3
keywords:
- 同步屬性 Windows Media Player
topic_type:
- apiref
api_name:
- Sync
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5af26ae563a38efcc40b0bcd319c5fc62b4776dc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107001546"
---
# <a name="sync-attributes"></a><span data-ttu-id="323a8-104">同步屬性</span><span class="sxs-lookup"><span data-stu-id="323a8-104">Sync Attributes</span></span>

<span data-ttu-id="323a8-105">**Sync01** 至 **Sync16** 屬性是32位值的字串表示，當它與多達16部可攜式裝置的其中一個同步播放清單時，Windows Media Player 會使用這些值。</span><span class="sxs-lookup"><span data-stu-id="323a8-105">The **Sync01** through **Sync16** attributes are string representations of 32-bit values that Windows Media Player uses when it synchronizes playlists with one of up to 16 portable devices.</span></span>

## <a name="applies-to"></a><span data-ttu-id="323a8-106">套用至</span><span class="sxs-lookup"><span data-stu-id="323a8-106">Applies To</span></span>

-   [<span data-ttu-id="323a8-107">播放清單</span><span class="sxs-lookup"><span data-stu-id="323a8-107">Playlists</span></span>](playlist-attributes-ref.md)

## <a name="remarks"></a><span data-ttu-id="323a8-108">備註</span><span class="sxs-lookup"><span data-stu-id="323a8-108">Remarks</span></span>

<span data-ttu-id="323a8-109">這些都是讀取/寫入屬性。</span><span class="sxs-lookup"><span data-stu-id="323a8-109">These are read/write attributes.</span></span> <span data-ttu-id="323a8-110">值為零表示 Windows Media Player 不應該與相關聯的裝置同步播放清單。</span><span class="sxs-lookup"><span data-stu-id="323a8-110">A value of zero indicates that Windows Media Player should not synchronize the playlist with the associated device.</span></span> <span data-ttu-id="323a8-111">大於零的值表示指定播放清單的同步處理優先權。</span><span class="sxs-lookup"><span data-stu-id="323a8-111">A value greater than zero indicates a synchronization priority for the given playlist.</span></span>

<span data-ttu-id="323a8-112">根據使用者輸入，Windows Media Player 會為文件庫中的每個播放清單設定這個屬性。</span><span class="sxs-lookup"><span data-stu-id="323a8-112">Based on user input, Windows Media Player sets this attribute for each of the playlists in the library.</span></span> <span data-ttu-id="323a8-113">當 Windows Media Player 嘗試同步播放播放清單與可攜式裝置時，它會檢查每個播放清單來比較代表裝置合作關係的 **同步**_XX_ 屬性值。</span><span class="sxs-lookup"><span data-stu-id="323a8-113">When Windows Media Player attempts to synchronize a playlist with a portable device, it examines each playlist to compare the values for the **Sync**_XX_ attributes that represent the device partnership.</span></span> <span data-ttu-id="323a8-114">具有較低 **同步**_XX_ 值的播放清單會獲得較高的同步處理優先權。</span><span class="sxs-lookup"><span data-stu-id="323a8-114">Playlists that have lower **Sync**_XX_ values receive higher synchronization priority.</span></span>

<span data-ttu-id="323a8-115">例如，程式庫可能包含下列四個播放清單和個別的 **同步**_XX_ 值：</span><span class="sxs-lookup"><span data-stu-id="323a8-115">For example, the library might contain the following four playlists and respective **Sync**_XX_ values:</span></span>



| <span data-ttu-id="323a8-116">播放清單名稱</span><span class="sxs-lookup"><span data-stu-id="323a8-116">Playlist Name</span></span> | <span data-ttu-id="323a8-117">Sync01 值</span><span class="sxs-lookup"><span data-stu-id="323a8-117">Sync01 Value</span></span> |
|---------------|--------------|
| <span data-ttu-id="323a8-118">GymMusic. .WPL</span><span class="sxs-lookup"><span data-stu-id="323a8-118">GymMusic.WPL</span></span>  | <span data-ttu-id="323a8-119">0x0000000D</span><span class="sxs-lookup"><span data-stu-id="323a8-119">0x0000000D</span></span>   |
| <span data-ttu-id="323a8-120">放寬 .WPL</span><span class="sxs-lookup"><span data-stu-id="323a8-120">Relax.WPL</span></span>     | <span data-ttu-id="323a8-121">0x00000020</span><span class="sxs-lookup"><span data-stu-id="323a8-121">0x00000020</span></span>   |
| <span data-ttu-id="323a8-122">DriveHome. .WPL</span><span class="sxs-lookup"><span data-stu-id="323a8-122">DriveHome.WPL</span></span> | <span data-ttu-id="323a8-123">0x00000001</span><span class="sxs-lookup"><span data-stu-id="323a8-123">0x00000001</span></span>   |
| <span data-ttu-id="323a8-124">NoGo. .WPL</span><span class="sxs-lookup"><span data-stu-id="323a8-124">NoGo.WPL</span></span>      | <span data-ttu-id="323a8-125">0x00000000</span><span class="sxs-lookup"><span data-stu-id="323a8-125">0x00000000</span></span>   |



 

<span data-ttu-id="323a8-126">當 Windows Media Player 同步處理與屬性相關聯的裝置時，它會以下列順序同步處理播放清單：</span><span class="sxs-lookup"><span data-stu-id="323a8-126">When Windows Media Player synchronizes the device associated with the attribute, it will synchronize the playlists in the following order:</span></span>

1.  <span data-ttu-id="323a8-127">DriveHome. .WPL</span><span class="sxs-lookup"><span data-stu-id="323a8-127">DriveHome.WPL</span></span>
2.  <span data-ttu-id="323a8-128">GymMusic. .WPL</span><span class="sxs-lookup"><span data-stu-id="323a8-128">GymMusic.WPL</span></span>
3.  <span data-ttu-id="323a8-129">放寬 .WPL</span><span class="sxs-lookup"><span data-stu-id="323a8-129">Relax.WPL</span></span>

<span data-ttu-id="323a8-130">若要判斷是否可以變更這個屬性的值，請使用 [isReadOnlyItem](media-isreadonlyitem.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="323a8-130">To determine whether you can change the value of this attribute, use the [Media.isReadOnlyItem](media-isreadonlyitem.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="323a8-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="323a8-131">Requirements</span></span>



| <span data-ttu-id="323a8-132">需求</span><span class="sxs-lookup"><span data-stu-id="323a8-132">Requirement</span></span> | <span data-ttu-id="323a8-133">值</span><span class="sxs-lookup"><span data-stu-id="323a8-133">Value</span></span> |
|--------------------|---------------------------------------------|
| <span data-ttu-id="323a8-134">版本</span><span class="sxs-lookup"><span data-stu-id="323a8-134">Version</span></span><br/> | <span data-ttu-id="323a8-135">Windows Media Player 10 或更新版本</span><span class="sxs-lookup"><span data-stu-id="323a8-135">Windows Media Player 10 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="323a8-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="323a8-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="323a8-137">**屬性參考**</span><span class="sxs-lookup"><span data-stu-id="323a8-137">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> <dt>

[<span data-ttu-id="323a8-138">**列舉同步播放清單**</span><span class="sxs-lookup"><span data-stu-id="323a8-138">**Enumerating Synchronization Playlists**</span></span>](enumerating-synchronization-playlists.md)
</dt> </dl>

 

 





