---
title: MediaCollection. getByAuthor 方法
description: GetByAuthor 方法會依指定的作者來抓取媒體專案的播放清單。
ms.assetid: 8f9b3ee3-a809-4d24-81ce-adad63e5347c
keywords:
- getByAuthor 方法 Windows Media Player
- getByAuthor 方法 Windows Media Player，MediaCollection 類別
- MediaCollection 類別 Windows Media Player，getByAuthor 方法
topic_type:
- apiref
api_name:
- MediaCollection.getByAuthor
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b7eae0928250e37e76bf3a39f38b43bef8a5691c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106985956"
---
# <a name="mediacollectiongetbyauthor-method"></a><span data-ttu-id="ab828-106">MediaCollection. getByAuthor 方法</span><span class="sxs-lookup"><span data-stu-id="ab828-106">MediaCollection.getByAuthor method</span></span>

<span data-ttu-id="ab828-107">**GetByAuthor** 方法會依指定的作者來抓取媒體專案的播放清單。</span><span class="sxs-lookup"><span data-stu-id="ab828-107">The **getByAuthor** method retrieves a playlist of the media items by the specified author.</span></span>

## <a name="syntax"></a><span data-ttu-id="ab828-108">語法</span><span class="sxs-lookup"><span data-stu-id="ab828-108">Syntax</span></span>


```JScript
retVal = MediaCollection.getByAuthor(
  author
)
```



## <a name="parameters"></a><span data-ttu-id="ab828-109">參數</span><span class="sxs-lookup"><span data-stu-id="ab828-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ab828-110">*作者* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ab828-110">*author* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ab828-111">包含作者名稱的 **字串**。</span><span class="sxs-lookup"><span data-stu-id="ab828-111">**String** containing the name of the author.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ab828-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="ab828-112">Return value</span></span>

<span data-ttu-id="ab828-113">這個方法會傳回 **播放清單** 物件。</span><span class="sxs-lookup"><span data-stu-id="ab828-113">This method returns a **Playlist** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="ab828-114">備註</span><span class="sxs-lookup"><span data-stu-id="ab828-114">Remarks</span></span>

<span data-ttu-id="ab828-115">若要使用此方法，需要有程式庫的讀取權限。</span><span class="sxs-lookup"><span data-stu-id="ab828-115">To use this method, read access to the library is required.</span></span> <span data-ttu-id="ab828-116">如需詳細資訊，請參閱連結 [庫存取](library-access.md)。</span><span class="sxs-lookup"><span data-stu-id="ab828-116">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="ab828-117">範例</span><span class="sxs-lookup"><span data-stu-id="ab828-117">Examples</span></span>

<span data-ttu-id="ab828-118">下列 JScript 範例會使用 *MediaCollection*。**getByAuthor** 以取得媒體專案的播放清單。</span><span class="sxs-lookup"><span data-stu-id="ab828-118">The following JScript example uses *MediaCollection*.**getByAuthor** to retrieve a playlist of media items.</span></span> <span data-ttu-id="ab828-119">播放清單包含的專案符合使用者在名為 GetAuthor 的 HTML 文字輸入元素中所指定的作者。</span><span class="sxs-lookup"><span data-stu-id="ab828-119">The playlist contains items matching the author specified by the user in an HTML TEXT input element named GetAuthor.</span></span> <span data-ttu-id="ab828-120">使用 ID = "Player" 建立 **player** 物件。</span><span class="sxs-lookup"><span data-stu-id="ab828-120">The **Player** object was created with ID = "Player".</span></span>


```JScript
<!-- Use an HTML BUTTON element to create the playlist and play the media items. -->
<INPUT TYPE = "BUTTON"  NAME = "PlayAuthor"  
       ID = "PlayAuthor"  
       VALUE = "Play Author"

onClick = "
    /* Retrieve the author name text from the user. */
    var author = GetAuthor.value;

    /* Create the playlist by using getByAuthor. */
    var pl = Player.mediaCollection.getByAuthor(Author);

    /* Make the new playlist the current playlist. */
    Player.currentPlaylist = pl;

    /* Play the media items in the new playlist. */
               Player.controls.play();
">

```



## <a name="requirements"></a><span data-ttu-id="ab828-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="ab828-121">Requirements</span></span>



| <span data-ttu-id="ab828-122">需求</span><span class="sxs-lookup"><span data-stu-id="ab828-122">Requirement</span></span> | <span data-ttu-id="ab828-123">值</span><span class="sxs-lookup"><span data-stu-id="ab828-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ab828-124">版本</span><span class="sxs-lookup"><span data-stu-id="ab828-124">Version</span></span><br/> | <span data-ttu-id="ab828-125">Windows Media Player 7.0 版或更新版本。</span><span class="sxs-lookup"><span data-stu-id="ab828-125">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="ab828-126">DLL</span><span class="sxs-lookup"><span data-stu-id="ab828-126">DLL</span></span><br/>     | <dl> <span data-ttu-id="ab828-127"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ab828-127"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ab828-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ab828-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ab828-129">**MediaCollection 物件**</span><span class="sxs-lookup"><span data-stu-id="ab828-129">**MediaCollection Object**</span></span>](mediacollection-object.md)
</dt> <dt>

[<span data-ttu-id="ab828-130">**播放清單物件**</span><span class="sxs-lookup"><span data-stu-id="ab828-130">**Playlist Object**</span></span>](playlist-object.md)
</dt> <dt>

[<span data-ttu-id="ab828-131">**設定. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="ab828-131">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="ab828-132">**設定. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="ab828-132">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





