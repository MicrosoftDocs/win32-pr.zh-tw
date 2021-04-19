---
title: MediaCollection. getAll 方法
description: GetAll 方法會抓取包含媒體櫃中所有媒體專案的播放清單。
ms.assetid: c22532ee-5714-4762-966f-7dc6543384f4
keywords:
- getAll 方法 Windows Media Player
- getAll 方法 Windows Media Player，MediaCollection 類別
- MediaCollection 類別 Windows Media Player，getAll 方法
topic_type:
- apiref
api_name:
- MediaCollection.getAll
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1681cd533be4084123cb80cdcc199ab5e1ce2981
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993560"
---
# <a name="mediacollectiongetall-method"></a><span data-ttu-id="faf7c-106">MediaCollection. getAll 方法</span><span class="sxs-lookup"><span data-stu-id="faf7c-106">MediaCollection.getAll method</span></span>

<span data-ttu-id="faf7c-107">**GetAll** 方法會抓取包含媒體櫃中所有媒體專案的播放清單。</span><span class="sxs-lookup"><span data-stu-id="faf7c-107">The **getAll** method retrieves a playlist containing all media items in the library.</span></span>

## <a name="syntax"></a><span data-ttu-id="faf7c-108">語法</span><span class="sxs-lookup"><span data-stu-id="faf7c-108">Syntax</span></span>


```JScript
retVal = MediaCollection.getAll()
```



## <a name="parameters"></a><span data-ttu-id="faf7c-109">參數</span><span class="sxs-lookup"><span data-stu-id="faf7c-109">Parameters</span></span>

<span data-ttu-id="faf7c-110">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="faf7c-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="faf7c-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="faf7c-111">Return value</span></span>

<span data-ttu-id="faf7c-112">這個方法會傳回 **播放清單** 物件。</span><span class="sxs-lookup"><span data-stu-id="faf7c-112">This method returns a **Playlist** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="faf7c-113">備註</span><span class="sxs-lookup"><span data-stu-id="faf7c-113">Remarks</span></span>

<span data-ttu-id="faf7c-114">若要使用此方法，需要有程式庫的讀取權限。</span><span class="sxs-lookup"><span data-stu-id="faf7c-114">To use this method, read access to the library is required.</span></span> <span data-ttu-id="faf7c-115">如需詳細資訊，請參閱連結 [庫存取](library-access.md)。</span><span class="sxs-lookup"><span data-stu-id="faf7c-115">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="faf7c-116">範例</span><span class="sxs-lookup"><span data-stu-id="faf7c-116">Examples</span></span>

<span data-ttu-id="faf7c-117">下列 JScript 範例會使用 *MediaCollection*。從媒體集合隨機播放媒體專案的 **getAll** 。</span><span class="sxs-lookup"><span data-stu-id="faf7c-117">The following JScript example uses *MediaCollection*.**getAll** to play media items randomly from the media collection.</span></span> <span data-ttu-id="faf7c-118">使用 ID = "Player" 建立 **player** 物件。</span><span class="sxs-lookup"><span data-stu-id="faf7c-118">The **Player** object was created with ID = "Player".</span></span>


```JScript
// Store the count of all media items in the media collection.
var count = Player.mediaCollection.getAll().count;

// Generate a random number using the media count.
var rand = Math.random() * count;

// Round down the random number to the nearest integer.
rand = Math.floor(rand);

// Make the random media item the current media item.
Player.currentMedia = Player.mediaCollection.getAll().item(rand);

// Play the media item.
// Player.controls.play();

```



## <a name="requirements"></a><span data-ttu-id="faf7c-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="faf7c-119">Requirements</span></span>



| <span data-ttu-id="faf7c-120">需求</span><span class="sxs-lookup"><span data-stu-id="faf7c-120">Requirement</span></span> | <span data-ttu-id="faf7c-121">值</span><span class="sxs-lookup"><span data-stu-id="faf7c-121">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="faf7c-122">版本</span><span class="sxs-lookup"><span data-stu-id="faf7c-122">Version</span></span><br/> | <span data-ttu-id="faf7c-123">Windows Media Player 7.0 版或更新版本。</span><span class="sxs-lookup"><span data-stu-id="faf7c-123">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="faf7c-124">DLL</span><span class="sxs-lookup"><span data-stu-id="faf7c-124">DLL</span></span><br/>     | <dl> <span data-ttu-id="faf7c-125"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="faf7c-125"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="faf7c-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="faf7c-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="faf7c-127">**MediaCollection 物件**</span><span class="sxs-lookup"><span data-stu-id="faf7c-127">**MediaCollection Object**</span></span>](mediacollection-object.md)
</dt> <dt>

[<span data-ttu-id="faf7c-128">**播放清單物件**</span><span class="sxs-lookup"><span data-stu-id="faf7c-128">**Playlist Object**</span></span>](playlist-object.md)
</dt> <dt>

[<span data-ttu-id="faf7c-129">**設定. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="faf7c-129">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="faf7c-130">**設定. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="faf7c-130">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





