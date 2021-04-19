---
title: MediaCollection. setDeleted 方法
description: SetDeleted 方法會將指定的媒體專案移到 [刪除的專案] 資料夾。 |MediaCollection. setDeleted 方法
ms.assetid: 3e3c9a16-37e1-41b4-8593-58aaf4541eb9
keywords:
- setDeleted 方法 Windows Media Player
- setDeleted 方法 Windows Media Player，MediaCollection 類別
- MediaCollection 類別 Windows Media Player，setDeleted 方法
topic_type:
- apiref
api_name:
- MediaCollection.setDeleted
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f545953899883933286f3c38def62d9f254dfdc0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106997688"
---
# <a name="mediacollectionsetdeleted-method"></a><span data-ttu-id="503cd-107">MediaCollection. setDeleted 方法</span><span class="sxs-lookup"><span data-stu-id="503cd-107">MediaCollection.setDeleted method</span></span>

<span data-ttu-id="503cd-108">**SetDeleted** 方法會將指定的媒體專案移到 [刪除的專案] 資料夾。</span><span class="sxs-lookup"><span data-stu-id="503cd-108">The **setDeleted** method moves the specified media item to the deleted items folder.</span></span>

## <a name="syntax"></a><span data-ttu-id="503cd-109">語法</span><span class="sxs-lookup"><span data-stu-id="503cd-109">Syntax</span></span>


```JScript
MediaCollection.setDeleted(
  item,
  true
)
```



## <a name="parameters"></a><span data-ttu-id="503cd-110">參數</span><span class="sxs-lookup"><span data-stu-id="503cd-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="503cd-111">*專案* \[在\]</span><span class="sxs-lookup"><span data-stu-id="503cd-111">*item* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="503cd-112">正在移動的 **媒體** 物件。</span><span class="sxs-lookup"><span data-stu-id="503cd-112">**Media** object being moved.</span></span>

</dd> <dt>

<span data-ttu-id="503cd-113">*true* \[在\]</span><span class="sxs-lookup"><span data-stu-id="503cd-113">*true* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="503cd-114">一律指定此值。</span><span class="sxs-lookup"><span data-stu-id="503cd-114">Always specify this value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="503cd-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="503cd-115">Return value</span></span>

<span data-ttu-id="503cd-116">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="503cd-116">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="503cd-117">備註</span><span class="sxs-lookup"><span data-stu-id="503cd-117">Remarks</span></span>

<span data-ttu-id="503cd-118">這個方法不會將檔案從使用者的電腦移除。</span><span class="sxs-lookup"><span data-stu-id="503cd-118">This method does not remove files from the user's computer.</span></span>

<span data-ttu-id="503cd-119">若要使用此方法，需要有程式庫的完整存取權。</span><span class="sxs-lookup"><span data-stu-id="503cd-119">To use this method, full access to the library is required.</span></span> <span data-ttu-id="503cd-120">如需詳細資訊，請參閱連結 [庫存取](library-access.md)。</span><span class="sxs-lookup"><span data-stu-id="503cd-120">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="503cd-121">**Windows Media Player 10** 行動裝置版：不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="503cd-121">**Windows Media Player 10 Mobile:** This method is not supported.</span></span>

## <a name="examples"></a><span data-ttu-id="503cd-122">範例</span><span class="sxs-lookup"><span data-stu-id="503cd-122">Examples</span></span>

<span data-ttu-id="503cd-123">下列 JScript 範例會使用 *MediaCollection*。**setDeleted** ，將儲存在名為 mediaObject 的變數中的特定媒體專案移至 [已刪除的專案] 資料夾。</span><span class="sxs-lookup"><span data-stu-id="503cd-123">The following JScript example uses *MediaCollection*.**setDeleted** to move a particular media item, stored in the variable named mediaObject, to the deleted items folder.</span></span> <span data-ttu-id="503cd-124">*MediaCollection*。**isDeleted** 方法會先測試是否已刪除專案。</span><span class="sxs-lookup"><span data-stu-id="503cd-124">The *MediaCollection*.**isDeleted** method first tests whether the item has already been deleted.</span></span> <span data-ttu-id="503cd-125">使用 ID = "Player" 建立 **player** 物件。</span><span class="sxs-lookup"><span data-stu-id="503cd-125">The **Player** object was created with ID = "Player".</span></span>


```JScript
// Test whether the media item is in the deleted items folder.
if (!Player.mediaCollection.isDeleted(mediaObject)){

    // The item is available to be deleted; move it to 
    // the deleted items folder.
    Player.mediaCollection.setDeleted(mediaObject, true);

    // Inform the user that the operation succeeded.
    alert("Item moved to deleted items folder.");}

else
    // Tell the user the operation is unnecessary.
    alert("Item is already deleted!");
}

```



## <a name="requirements"></a><span data-ttu-id="503cd-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="503cd-126">Requirements</span></span>



| <span data-ttu-id="503cd-127">需求</span><span class="sxs-lookup"><span data-stu-id="503cd-127">Requirement</span></span> | <span data-ttu-id="503cd-128">值</span><span class="sxs-lookup"><span data-stu-id="503cd-128">Value</span></span> |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="503cd-129">版本</span><span class="sxs-lookup"><span data-stu-id="503cd-129">Version</span></span><br/> | <span data-ttu-id="503cd-130">適用于 Windows XP 的 Windows Media Player 7.0 版、Windows Media Player 7.1 版或 Windows Media Player。</span><span class="sxs-lookup"><span data-stu-id="503cd-130">Windows Media Player version 7.0, Windows Media Player version 7.1, or Windows Media Player for Windows XP.</span></span> <span data-ttu-id="503cd-131">Windows Media Player 9 系列或更新版本不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="503cd-131">This method is not supported for Windows Media Player 9 Series or later.</span></span><br/> |
| <span data-ttu-id="503cd-132">DLL</span><span class="sxs-lookup"><span data-stu-id="503cd-132">DLL</span></span><br/>     | <dl> <span data-ttu-id="503cd-133"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="503cd-133"><dt>Wmp.dll</dt></span></span> </dl>                                                                                                              |



## <a name="see-also"></a><span data-ttu-id="503cd-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="503cd-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="503cd-135">**媒體物件**</span><span class="sxs-lookup"><span data-stu-id="503cd-135">**Media Object**</span></span>](media-object.md)
</dt> <dt>

[<span data-ttu-id="503cd-136">**MediaCollection 物件**</span><span class="sxs-lookup"><span data-stu-id="503cd-136">**MediaCollection Object**</span></span>](mediacollection-object.md)
</dt> <dt>

[<span data-ttu-id="503cd-137">**MediaCollection. isDeleted**</span><span class="sxs-lookup"><span data-stu-id="503cd-137">**MediaCollection.isDeleted**</span></span>](mediacollection-isdeleted.md)
</dt> <dt>

[<span data-ttu-id="503cd-138">**設定. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="503cd-138">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="503cd-139">**設定. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="503cd-139">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





