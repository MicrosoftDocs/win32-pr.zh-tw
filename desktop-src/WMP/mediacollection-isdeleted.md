---
title: MediaCollection. isDeleted 方法
description: IsDeleted 方法會抓取值，指出指定的媒體專案是否位於 [刪除的專案] 資料夾中。
ms.assetid: bb3ce9c9-9e43-45a5-8802-dc6783cf2ad7
keywords:
- isDeleted 方法 Windows Media Player
- isDeleted 方法 Windows Media Player，MediaCollection 類別
- MediaCollection 類別 Windows Media Player，isDeleted 方法
topic_type:
- apiref
api_name:
- MediaCollection.isDeleted
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bd3cdc27c84c88eb65df5b7635f34c79c1b4fe82
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106989780"
---
# <a name="mediacollectionisdeleted-method"></a><span data-ttu-id="e5543-106">MediaCollection. isDeleted 方法</span><span class="sxs-lookup"><span data-stu-id="e5543-106">MediaCollection.isDeleted method</span></span>

<span data-ttu-id="e5543-107">**IsDeleted** 方法會抓取值，指出指定的媒體專案是否位於 [刪除的專案] 資料夾中。</span><span class="sxs-lookup"><span data-stu-id="e5543-107">The **isDeleted** method retrieves a value indicating whether the specified media item is in the deleted items folder.</span></span>

## <a name="syntax"></a><span data-ttu-id="e5543-108">語法</span><span class="sxs-lookup"><span data-stu-id="e5543-108">Syntax</span></span>


```JScript
bRetVal = MediaCollection.isDeleted(
  item
)
```



## <a name="parameters"></a><span data-ttu-id="e5543-109">參數</span><span class="sxs-lookup"><span data-stu-id="e5543-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e5543-110">*專案* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e5543-110">*item* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e5543-111">可能會刪除的 **媒體** 物件。</span><span class="sxs-lookup"><span data-stu-id="e5543-111">**Media** object that might be deleted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e5543-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="e5543-112">Return value</span></span>

<span data-ttu-id="e5543-113">這個方法會傳回 **布林值**。</span><span class="sxs-lookup"><span data-stu-id="e5543-113">This method returns a **Boolean**.</span></span>

## <a name="remarks"></a><span data-ttu-id="e5543-114">備註</span><span class="sxs-lookup"><span data-stu-id="e5543-114">Remarks</span></span>

<span data-ttu-id="e5543-115">若要使用此方法，需要有程式庫的讀取權限。</span><span class="sxs-lookup"><span data-stu-id="e5543-115">To use this method, read access to the library is required.</span></span> <span data-ttu-id="e5543-116">如需詳細資訊，請參閱連結 [庫存取](library-access.md)。</span><span class="sxs-lookup"><span data-stu-id="e5543-116">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="e5543-117">**Windows Media Player 10** 行動裝置版：這個方法一律會傳回 **false**。</span><span class="sxs-lookup"><span data-stu-id="e5543-117">**Windows Media Player 10 Mobile:** This method always returns **false**.</span></span>

## <a name="examples"></a><span data-ttu-id="e5543-118">範例</span><span class="sxs-lookup"><span data-stu-id="e5543-118">Examples</span></span>

<span data-ttu-id="e5543-119">下列 JScript 範例會使用 *MediaCollection*。**isDeleted** ，測試儲存在名為 mediaObject 的變數中的特定媒體專案是否在 [刪除的專案] 資料夾中。</span><span class="sxs-lookup"><span data-stu-id="e5543-119">The following JScript example uses *MediaCollection*.**isDeleted** to test whether a particular media item, stored in the variable named mediaObject, is in the deleted items folder.</span></span> <span data-ttu-id="e5543-120">如果媒體專案尚未刪除，則會移至 [已刪除的專案] 資料夾。</span><span class="sxs-lookup"><span data-stu-id="e5543-120">If the media item has not been deleted already, it is moved to the deleted items folder.</span></span> <span data-ttu-id="e5543-121">使用 ID = "Player" 建立 **player** 物件。</span><span class="sxs-lookup"><span data-stu-id="e5543-121">The **Player** object was created with ID = "Player".</span></span>


```JScript
// Test whether the media item is in the deleted items folder.
if (!Player.mediaCollection.isDeleted(mediaObject)){

    // The media item is available to be deleted, move it to 
    // the deleted items folder.
    Player.mediaCollection.setDeleted(mediaObject, true);

    // Inform the user that the operation succeeded.
    alert("Media item moved to deleted items folder.");}

else
    // Tell the user the operation is unnecessary.
    alert("Item is already deleted!");
}

```



## <a name="requirements"></a><span data-ttu-id="e5543-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="e5543-122">Requirements</span></span>



| <span data-ttu-id="e5543-123">需求</span><span class="sxs-lookup"><span data-stu-id="e5543-123">Requirement</span></span> | <span data-ttu-id="e5543-124">值</span><span class="sxs-lookup"><span data-stu-id="e5543-124">Value</span></span> |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e5543-125">版本</span><span class="sxs-lookup"><span data-stu-id="e5543-125">Version</span></span><br/> | <span data-ttu-id="e5543-126">適用于 Windows XP 的 Windows Media Player 7.0 版、Windows Media Player 7.1 版或 Windows Media Player。</span><span class="sxs-lookup"><span data-stu-id="e5543-126">Windows Media Player version 7.0, Windows Media Player version 7.1, or Windows Media Player for Windows XP.</span></span> <span data-ttu-id="e5543-127">Windows Media Player 9 系列或更新版本不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="e5543-127">This method is not supported for Windows Media Player 9 Series or later.</span></span><br/> |
| <span data-ttu-id="e5543-128">DLL</span><span class="sxs-lookup"><span data-stu-id="e5543-128">DLL</span></span><br/>     | <dl> <span data-ttu-id="e5543-129"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e5543-129"><dt>Wmp.dll</dt></span></span> </dl>                                                                                                              |



## <a name="see-also"></a><span data-ttu-id="e5543-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e5543-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e5543-131">**媒體物件**</span><span class="sxs-lookup"><span data-stu-id="e5543-131">**Media Object**</span></span>](media-object.md)
</dt> <dt>

[<span data-ttu-id="e5543-132">**MediaCollection 物件**</span><span class="sxs-lookup"><span data-stu-id="e5543-132">**MediaCollection Object**</span></span>](mediacollection-object.md)
</dt> <dt>

[<span data-ttu-id="e5543-133">**MediaCollection.setDeleted**</span><span class="sxs-lookup"><span data-stu-id="e5543-133">**MediaCollection.setDeleted**</span></span>](mediacollection-setdeleted.md)
</dt> <dt>

[<span data-ttu-id="e5543-134">**設定. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="e5543-134">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="e5543-135">**設定. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="e5543-135">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





