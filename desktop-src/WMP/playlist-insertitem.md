---
title: InsertItem 方法
description: InsertItem 方法會將媒體專案插入播放清單中指定的位置。
ms.assetid: c186abc4-0a15-49d2-bbc4-5660e8cc0a4b
keywords:
- insertItem 方法 Windows Media Player
- insertItem 方法 Windows Media Player，播放清單類別
- 播放清單類別 Windows Media Player，insertItem 方法
topic_type:
- apiref
api_name:
- Playlist.insertItem
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a456b7a359d59958ce7693cc48c16eabba435621
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106985967"
---
# <a name="playlistinsertitem-method"></a><span data-ttu-id="711d4-106">InsertItem 方法</span><span class="sxs-lookup"><span data-stu-id="711d4-106">Playlist.insertItem method</span></span>

<span data-ttu-id="711d4-107">**InsertItem** 方法會將媒體專案插入播放清單中指定的位置。</span><span class="sxs-lookup"><span data-stu-id="711d4-107">The **insertItem** method inserts a media item into the playlist at the specified location.</span></span>

## <a name="syntax"></a><span data-ttu-id="711d4-108">語法</span><span class="sxs-lookup"><span data-stu-id="711d4-108">Syntax</span></span>


```JScript
Playlist.insertItem(
  index,
  item
)
```



## <a name="parameters"></a><span data-ttu-id="711d4-109">參數</span><span class="sxs-lookup"><span data-stu-id="711d4-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="711d4-110">*索引* \[在\]</span><span class="sxs-lookup"><span data-stu-id="711d4-110">*index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="711d4-111">**Number** (**Long**) ，其中包含要在其中加入專案的索引。</span><span class="sxs-lookup"><span data-stu-id="711d4-111">**Number** (**long**) containing the index at which to add the item.</span></span>

</dd> <dt>

<span data-ttu-id="711d4-112">*專案* \[在\]</span><span class="sxs-lookup"><span data-stu-id="711d4-112">*item* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="711d4-113">要插入的 **媒體** 物件。</span><span class="sxs-lookup"><span data-stu-id="711d4-113">**Media** object to insert.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="711d4-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="711d4-114">Return value</span></span>

<span data-ttu-id="711d4-115">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="711d4-115">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="711d4-116">備註</span><span class="sxs-lookup"><span data-stu-id="711d4-116">Remarks</span></span>

<span data-ttu-id="711d4-117">插入專案之後的所有專案都會以1遞增其索引編號。</span><span class="sxs-lookup"><span data-stu-id="711d4-117">All items after the inserted item will have their index numbers increased by one.</span></span>

<span data-ttu-id="711d4-118">若要使用此方法，需要有程式庫的完整存取權。</span><span class="sxs-lookup"><span data-stu-id="711d4-118">To use this method, full access to the library is required.</span></span> <span data-ttu-id="711d4-119">如需詳細資訊，請參閱連結 [庫存取](library-access.md)。</span><span class="sxs-lookup"><span data-stu-id="711d4-119">For more information, see [Library Access](library-access.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="711d4-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="711d4-120">Requirements</span></span>



| <span data-ttu-id="711d4-121">需求</span><span class="sxs-lookup"><span data-stu-id="711d4-121">Requirement</span></span> | <span data-ttu-id="711d4-122">值</span><span class="sxs-lookup"><span data-stu-id="711d4-122">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="711d4-123">版本</span><span class="sxs-lookup"><span data-stu-id="711d4-123">Version</span></span><br/> | <span data-ttu-id="711d4-124">Windows Media Player 7.0 版或更新版本。</span><span class="sxs-lookup"><span data-stu-id="711d4-124">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="711d4-125">DLL</span><span class="sxs-lookup"><span data-stu-id="711d4-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="711d4-126"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="711d4-126"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="711d4-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="711d4-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="711d4-128">**播放清單物件**</span><span class="sxs-lookup"><span data-stu-id="711d4-128">**Playlist Object**</span></span>](playlist-object.md)
</dt> <dt>

[<span data-ttu-id="711d4-129">**播放清單。專案**</span><span class="sxs-lookup"><span data-stu-id="711d4-129">**Playlist.item**</span></span>](playlist-item.md)
</dt> <dt>

[<span data-ttu-id="711d4-130">**播放清單。 removeItem**</span><span class="sxs-lookup"><span data-stu-id="711d4-130">**Playlist.removeItem**</span></span>](playlist-removeitem.md)
</dt> <dt>

[<span data-ttu-id="711d4-131">**設定. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="711d4-131">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="711d4-132">**設定. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="711d4-132">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





