---
title: MoveItem 方法
description: MoveItem 方法會變更播放清單中專案的位置。
ms.assetid: 82a8de86-4419-48a7-89f8-f7b9084b51d4
keywords:
- moveItem 方法 Windows Media Player
- moveItem 方法 Windows Media Player，播放清單類別
- 播放清單類別 Windows Media Player，moveItem 方法
topic_type:
- apiref
api_name:
- Playlist.moveItem
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 06e2e48b2987af4becd8c07357ff2eecf137f31d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999390"
---
# <a name="playlistmoveitem-method"></a><span data-ttu-id="9b23c-106">MoveItem 方法</span><span class="sxs-lookup"><span data-stu-id="9b23c-106">Playlist.moveItem method</span></span>

<span data-ttu-id="9b23c-107">**MoveItem** 方法會變更播放清單中專案的位置。</span><span class="sxs-lookup"><span data-stu-id="9b23c-107">The **moveItem** method changes the location of an item in the playlist.</span></span>

## <a name="syntax"></a><span data-ttu-id="9b23c-108">語法</span><span class="sxs-lookup"><span data-stu-id="9b23c-108">Syntax</span></span>


```JScript
Playlist.moveItem(
  oldIndex,
  newIndex
)
```



## <a name="parameters"></a><span data-ttu-id="9b23c-109">參數</span><span class="sxs-lookup"><span data-stu-id="9b23c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9b23c-110">*oldIndex* \[在\]</span><span class="sxs-lookup"><span data-stu-id="9b23c-110">*oldIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9b23c-111">包含舊索引的 (**長**) **數目**。</span><span class="sxs-lookup"><span data-stu-id="9b23c-111">**Number** (**long**) containing the old index.</span></span>

</dd> <dt>

<span data-ttu-id="9b23c-112">*newIndex* \[在\]</span><span class="sxs-lookup"><span data-stu-id="9b23c-112">*newIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9b23c-113">包含新索引的 (**長**) **數目**。</span><span class="sxs-lookup"><span data-stu-id="9b23c-113">**Number** (**long**) containing the new index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9b23c-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="9b23c-114">Return value</span></span>

<span data-ttu-id="9b23c-115">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="9b23c-115">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="9b23c-116">備註</span><span class="sxs-lookup"><span data-stu-id="9b23c-116">Remarks</span></span>

<span data-ttu-id="9b23c-117">儲存在程式庫中的播放清單可以在您的控制項之外變更。</span><span class="sxs-lookup"><span data-stu-id="9b23c-117">Playlists stored in the library can change outside your control.</span></span> <span data-ttu-id="9b23c-118">請務必監視並處理所有適當的播放清單相關事件，讓播放清單中的專案順序不會意外變更。</span><span class="sxs-lookup"><span data-stu-id="9b23c-118">Be sure to monitor and handle all appropriate playlist-related events so that the order of items in the playlist does not change unexpectedly.</span></span>

<span data-ttu-id="9b23c-119">若要使用此方法，需要有程式庫的完整存取權。</span><span class="sxs-lookup"><span data-stu-id="9b23c-119">To use this method, full access to the library is required.</span></span> <span data-ttu-id="9b23c-120">如需詳細資訊，請參閱連結 [庫存取](library-access.md)。</span><span class="sxs-lookup"><span data-stu-id="9b23c-120">For more information, see [Library Access](library-access.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="9b23c-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="9b23c-121">Requirements</span></span>



| <span data-ttu-id="9b23c-122">需求</span><span class="sxs-lookup"><span data-stu-id="9b23c-122">Requirement</span></span> | <span data-ttu-id="9b23c-123">值</span><span class="sxs-lookup"><span data-stu-id="9b23c-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="9b23c-124">版本</span><span class="sxs-lookup"><span data-stu-id="9b23c-124">Version</span></span><br/> | <span data-ttu-id="9b23c-125">Windows Media Player 7.0 版或更新版本。</span><span class="sxs-lookup"><span data-stu-id="9b23c-125">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="9b23c-126">DLL</span><span class="sxs-lookup"><span data-stu-id="9b23c-126">DLL</span></span><br/>     | <dl> <span data-ttu-id="9b23c-127"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9b23c-127"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9b23c-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9b23c-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9b23c-129">**播放清單物件**</span><span class="sxs-lookup"><span data-stu-id="9b23c-129">**Playlist Object**</span></span>](playlist-object.md)
</dt> <dt>

[<span data-ttu-id="9b23c-130">**設定. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="9b23c-130">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="9b23c-131">**設定. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="9b23c-131">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





