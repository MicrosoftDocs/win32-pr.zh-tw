---
title: MediaCollection. getByAlbum 方法
description: GetByAlbum 方法會從指定的專輯抓取包含媒體專案的播放清單。
ms.assetid: e7e72f0e-e0ae-4bbd-a8b7-966f0fc50059
keywords:
- getByAlbum 方法 Windows Media Player
- getByAlbum 方法 Windows Media Player，MediaCollection 類別
- MediaCollection 類別 Windows Media Player，getByAlbum 方法
topic_type:
- apiref
api_name:
- MediaCollection.getByAlbum
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d94cdfa880288893e9659b73b01bc754ac59bbf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107000422"
---
# <a name="mediacollectiongetbyalbum-method"></a><span data-ttu-id="975f3-106">MediaCollection. getByAlbum 方法</span><span class="sxs-lookup"><span data-stu-id="975f3-106">MediaCollection.getByAlbum method</span></span>

<span data-ttu-id="975f3-107">**GetByAlbum** 方法會從指定的專輯抓取包含媒體專案的播放清單。</span><span class="sxs-lookup"><span data-stu-id="975f3-107">The **GetByAlbum** method retrieves a playlist containing the media items from the specified album.</span></span>

## <a name="syntax"></a><span data-ttu-id="975f3-108">語法</span><span class="sxs-lookup"><span data-stu-id="975f3-108">Syntax</span></span>


```JScript
retVal = MediaCollection.getByAlbum(
  album
)
```



## <a name="parameters"></a><span data-ttu-id="975f3-109">參數</span><span class="sxs-lookup"><span data-stu-id="975f3-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="975f3-110">*專輯* \[在\]</span><span class="sxs-lookup"><span data-stu-id="975f3-110">*album* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="975f3-111">包含專輯名稱的 **字串**。</span><span class="sxs-lookup"><span data-stu-id="975f3-111">**String** containing the name of the album.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="975f3-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="975f3-112">Return value</span></span>

<span data-ttu-id="975f3-113">這個方法會傳回 **播放清單** 物件。</span><span class="sxs-lookup"><span data-stu-id="975f3-113">This method returns a **Playlist** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="975f3-114">備註</span><span class="sxs-lookup"><span data-stu-id="975f3-114">Remarks</span></span>

<span data-ttu-id="975f3-115">若要使用此方法，需要有程式庫的讀取權限。</span><span class="sxs-lookup"><span data-stu-id="975f3-115">To use this method, read access to the library is required.</span></span> <span data-ttu-id="975f3-116">如需詳細資訊，請參閱連結 [庫存取](library-access.md)。</span><span class="sxs-lookup"><span data-stu-id="975f3-116">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="975f3-117">範例</span><span class="sxs-lookup"><span data-stu-id="975f3-117">Examples</span></span>

<span data-ttu-id="975f3-118">下列範例會使用 *MediaCollection*。**getByAlbum** 以取得媒體專案的播放清單。</span><span class="sxs-lookup"><span data-stu-id="975f3-118">The following example uses *MediaCollection*.**getByAlbum** to retrieve a playlist of media items.</span></span> <span data-ttu-id="975f3-119">播放清單中包含使用者在名為 GetAlbum 的 HTML 文字輸入元素中所指定之專輯的專案。</span><span class="sxs-lookup"><span data-stu-id="975f3-119">The playlist contains items with the album specified by the user in an HTML TEXT input element named GetAlbum.</span></span> <span data-ttu-id="975f3-120">使用 ID = "Player" 建立 **player** 物件。</span><span class="sxs-lookup"><span data-stu-id="975f3-120">The **Player** object was created with ID = "Player".</span></span>


```JScript
<!-- Use an HTML BUTTON element to create the playlist and 
then play the digital media items. -->
<INPUT TYPE = "BUTTON"
       NAME = "PlayAlbum" 
       ID = "PlayAlbum"  
       VALUE = "Play Album"

onClick = "
    /* Retrieve the album title text from the user. */
    var album = GetAlbum.value;

    /* Create the playlist using getByAlbum. */
    var pl = Player.mediaCollection.getByAlbum(album);

    /* Make the new playlist the current playlist. */
    Player.currentPlaylist = pl;

    /* Play the media in the new playlist. */
    Player.controls.play();
">

```



## <a name="requirements"></a><span data-ttu-id="975f3-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="975f3-121">Requirements</span></span>



| <span data-ttu-id="975f3-122">需求</span><span class="sxs-lookup"><span data-stu-id="975f3-122">Requirement</span></span> | <span data-ttu-id="975f3-123">值</span><span class="sxs-lookup"><span data-stu-id="975f3-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="975f3-124">版本</span><span class="sxs-lookup"><span data-stu-id="975f3-124">Version</span></span><br/> | <span data-ttu-id="975f3-125">Windows Media Player 7.0 版或更新版本。</span><span class="sxs-lookup"><span data-stu-id="975f3-125">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="975f3-126">DLL</span><span class="sxs-lookup"><span data-stu-id="975f3-126">DLL</span></span><br/>     | <dl> <span data-ttu-id="975f3-127"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="975f3-127"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="975f3-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="975f3-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="975f3-129">**MediaCollection 物件**</span><span class="sxs-lookup"><span data-stu-id="975f3-129">**MediaCollection Object**</span></span>](mediacollection-object.md)
</dt> <dt>

[<span data-ttu-id="975f3-130">**播放清單物件**</span><span class="sxs-lookup"><span data-stu-id="975f3-130">**Playlist Object**</span></span>](playlist-object.md)
</dt> <dt>

[<span data-ttu-id="975f3-131">**設定. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="975f3-131">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="975f3-132">**設定. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="975f3-132">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





