---
title: MediaCollection. getByGenre 方法
description: GetByGenre 方法會使用指定的類型，來抓取媒體專案的播放清單。
ms.assetid: 022a0c52-93e1-4ab4-90a7-632bcd6fc004
keywords:
- getByGenre 方法 Windows Media Player
- getByGenre 方法 Windows Media Player，MediaCollection 類別
- MediaCollection 類別 Windows Media Player，getByGenre 方法
topic_type:
- apiref
api_name:
- MediaCollection.getByGenre
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b73cd7fe9bb3efa9115e2ba5d01b6d12c89898d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106997656"
---
# <a name="mediacollectiongetbygenre-method"></a><span data-ttu-id="7dd8e-106">MediaCollection. getByGenre 方法</span><span class="sxs-lookup"><span data-stu-id="7dd8e-106">MediaCollection.getByGenre method</span></span>

<span data-ttu-id="7dd8e-107">**GetByGenre** 方法會使用指定的類型，來抓取媒體專案的播放清單。</span><span class="sxs-lookup"><span data-stu-id="7dd8e-107">The **getByGenre** method retrieves a playlist of the media items with the specified genre.</span></span>

## <a name="syntax"></a><span data-ttu-id="7dd8e-108">語法</span><span class="sxs-lookup"><span data-stu-id="7dd8e-108">Syntax</span></span>


```JScript
retVal = MediaCollection.getByGenre(
  genre
)
```



## <a name="parameters"></a><span data-ttu-id="7dd8e-109">參數</span><span class="sxs-lookup"><span data-stu-id="7dd8e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7dd8e-110">內容類型 \[在\]</span><span class="sxs-lookup"><span data-stu-id="7dd8e-110">*genre* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7dd8e-111">包含類型名稱的 **字串**。</span><span class="sxs-lookup"><span data-stu-id="7dd8e-111">**String** containing the name of the genre.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7dd8e-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="7dd8e-112">Return value</span></span>

<span data-ttu-id="7dd8e-113">這個方法會傳回 **播放清單** 物件。</span><span class="sxs-lookup"><span data-stu-id="7dd8e-113">This method returns a **Playlist** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="7dd8e-114">備註</span><span class="sxs-lookup"><span data-stu-id="7dd8e-114">Remarks</span></span>

<span data-ttu-id="7dd8e-115">若要使用此方法，需要有程式庫的讀取權限。</span><span class="sxs-lookup"><span data-stu-id="7dd8e-115">To use this method, read access to the library is required.</span></span> <span data-ttu-id="7dd8e-116">如需詳細資訊，請參閱連結 [庫存取](library-access.md)。</span><span class="sxs-lookup"><span data-stu-id="7dd8e-116">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="7dd8e-117">範例</span><span class="sxs-lookup"><span data-stu-id="7dd8e-117">Examples</span></span>

<span data-ttu-id="7dd8e-118">下列 JScript 範例會使用 *MediaCollection*。**getByGenre** 以取得媒體專案的播放清單。</span><span class="sxs-lookup"><span data-stu-id="7dd8e-118">The following JScript example uses *MediaCollection*.**getByGenre** to retrieve a playlist of media items.</span></span> <span data-ttu-id="7dd8e-119">播放清單中包含使用者在名為 GetGenre 的 HTML 文字輸入元素中所指定之類型的專案。</span><span class="sxs-lookup"><span data-stu-id="7dd8e-119">The playlist contains items with the genre specified by the user in an HTML TEXT input element named GetGenre.</span></span> <span data-ttu-id="7dd8e-120">使用 ID = "Player" 建立 **player** 物件。</span><span class="sxs-lookup"><span data-stu-id="7dd8e-120">The **Player** object was created with ID = "Player".</span></span>


```JScript
<!-- Use an HTML BUTTON element to create the playlist and play 
the media items. -->
<INPUT TYPE = "BUTTON"  
       NAME = "PlayGenre"  
       ID = "PlayGenre"  
       VALUE = "Play Genre"

onClick = "
    /* Retrieve the genre text from the user. */
    var genre = GetGenre.value;

    /* Create the playlist using getByGenre. */
    var pl = Player.mediaCollection.getByGenre(genre);

    /* Make the new playlist the current playlist. */
    Player.currentPlaylist = pl;

    /* Play the digital media item in the new playlist. */
    Player.controls.play();
">

```



## <a name="requirements"></a><span data-ttu-id="7dd8e-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="7dd8e-121">Requirements</span></span>



| <span data-ttu-id="7dd8e-122">需求</span><span class="sxs-lookup"><span data-stu-id="7dd8e-122">Requirement</span></span> | <span data-ttu-id="7dd8e-123">值</span><span class="sxs-lookup"><span data-stu-id="7dd8e-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="7dd8e-124">版本</span><span class="sxs-lookup"><span data-stu-id="7dd8e-124">Version</span></span><br/> | <span data-ttu-id="7dd8e-125">Windows Media Player 7.0 版或更新版本。</span><span class="sxs-lookup"><span data-stu-id="7dd8e-125">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="7dd8e-126">DLL</span><span class="sxs-lookup"><span data-stu-id="7dd8e-126">DLL</span></span><br/>     | <dl> <span data-ttu-id="7dd8e-127"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7dd8e-127"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7dd8e-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7dd8e-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7dd8e-129">**MediaCollection 物件**</span><span class="sxs-lookup"><span data-stu-id="7dd8e-129">**MediaCollection Object**</span></span>](mediacollection-object.md)
</dt> <dt>

[<span data-ttu-id="7dd8e-130">**播放清單物件**</span><span class="sxs-lookup"><span data-stu-id="7dd8e-130">**Playlist Object**</span></span>](playlist-object.md)
</dt> <dt>

[<span data-ttu-id="7dd8e-131">**設定. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="7dd8e-131">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="7dd8e-132">**設定. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="7dd8e-132">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





