---
title: MediaCollection. getByName 方法
description: GetByName 方法會抓取具有指定名稱的媒體專案播放清單。
ms.assetid: f9395a4f-06d6-438b-b7c5-7a063abdf59f
keywords:
- getByName 方法 Windows Media Player
- getByName 方法 Windows Media Player，MediaCollection 類別
- MediaCollection 類別 Windows Media Player，getByName 方法
topic_type:
- apiref
api_name:
- MediaCollection.getByName
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 01a3fc6e34b508fa094f79d2fbbd1d44ab712789
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106992885"
---
# <a name="mediacollectiongetbyname-method"></a><span data-ttu-id="a41e1-106">MediaCollection. getByName 方法</span><span class="sxs-lookup"><span data-stu-id="a41e1-106">MediaCollection.getByName method</span></span>

<span data-ttu-id="a41e1-107">**GetByName** 方法會抓取具有指定名稱的媒體專案播放清單。</span><span class="sxs-lookup"><span data-stu-id="a41e1-107">The **getByName** method retrieves a playlist of the media items with the specified name.</span></span>

## <a name="syntax"></a><span data-ttu-id="a41e1-108">語法</span><span class="sxs-lookup"><span data-stu-id="a41e1-108">Syntax</span></span>


```JScript
retVal = MediaCollection.getByName(
  name
)
```



## <a name="parameters"></a><span data-ttu-id="a41e1-109">參數</span><span class="sxs-lookup"><span data-stu-id="a41e1-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a41e1-110">*名稱* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a41e1-110">*name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a41e1-111">包含名稱的 **字串**。</span><span class="sxs-lookup"><span data-stu-id="a41e1-111">**String** containing the name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a41e1-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="a41e1-112">Return value</span></span>

<span data-ttu-id="a41e1-113">這個方法會傳回 **播放清單** 物件。</span><span class="sxs-lookup"><span data-stu-id="a41e1-113">This method returns a **Playlist** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="a41e1-114">備註</span><span class="sxs-lookup"><span data-stu-id="a41e1-114">Remarks</span></span>

<span data-ttu-id="a41e1-115">若要使用此方法，需要有程式庫的讀取權限。</span><span class="sxs-lookup"><span data-stu-id="a41e1-115">To use this method, read access to the library is required.</span></span> <span data-ttu-id="a41e1-116">如需詳細資訊，請參閱連結 [庫存取](library-access.md)。</span><span class="sxs-lookup"><span data-stu-id="a41e1-116">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="a41e1-117">範例</span><span class="sxs-lookup"><span data-stu-id="a41e1-117">Examples</span></span>

<span data-ttu-id="a41e1-118">下列 JScript 範例會使用 *MediaCollection*。**getByName** 從程式庫取出三個專案。</span><span class="sxs-lookup"><span data-stu-id="a41e1-118">The following JScript example uses *MediaCollection*.**getByName** to retrieve three items from the library.</span></span> <span data-ttu-id="a41e1-119">接著會將每個專案附加至目前的播放清單。</span><span class="sxs-lookup"><span data-stu-id="a41e1-119">Each item is then appended to the current playlist.</span></span> <span data-ttu-id="a41e1-120">使用 ID = "Player" 建立 **player** 物件。</span><span class="sxs-lookup"><span data-stu-id="a41e1-120">The **Player** object was created with ID="Player".</span></span>


```JScript
// In each case, use the name exactly as it appears in the library.
// Windows Media Player does not include file name extensions or file paths
// in the name. Internet URLs include the entire path, but not the 
// file name extension.

// Get a playlist object that contains an Internet URL.
var One = Player.mediaCollection.getByName("https://www.proseware.com/Media/Laure");
 
// Get a playlist object that contains a file on a network server.
var Two = Player.mediaCollection.getByName("Jeanne");

// Get a playlist object that contains a file on a local drive.
var Three = Player.mediaCollection.getByName("house");

// Append each item to the current playlist. Since each playlist retrieved
// using getByName contains one digital media item, use Playlist.item with
// an index of zero to reference that item.
Player.currentPlaylist.appendItem(One.item(0));
Player.currentPlaylist.appendItem(Two.item(0));
Player.currentPlaylist.appendItem(Three.item(0));

```



## <a name="requirements"></a><span data-ttu-id="a41e1-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="a41e1-121">Requirements</span></span>



| <span data-ttu-id="a41e1-122">需求</span><span class="sxs-lookup"><span data-stu-id="a41e1-122">Requirement</span></span> | <span data-ttu-id="a41e1-123">值</span><span class="sxs-lookup"><span data-stu-id="a41e1-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a41e1-124">版本</span><span class="sxs-lookup"><span data-stu-id="a41e1-124">Version</span></span><br/> | <span data-ttu-id="a41e1-125">Windows Media Player 7.0 版或更新版本。</span><span class="sxs-lookup"><span data-stu-id="a41e1-125">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="a41e1-126">DLL</span><span class="sxs-lookup"><span data-stu-id="a41e1-126">DLL</span></span><br/>     | <dl> <span data-ttu-id="a41e1-127"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a41e1-127"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a41e1-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a41e1-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a41e1-129">**MediaCollection 物件**</span><span class="sxs-lookup"><span data-stu-id="a41e1-129">**MediaCollection Object**</span></span>](mediacollection-object.md)
</dt> <dt>

[<span data-ttu-id="a41e1-130">**播放清單物件**</span><span class="sxs-lookup"><span data-stu-id="a41e1-130">**Playlist Object**</span></span>](playlist-object.md)
</dt> <dt>

[<span data-ttu-id="a41e1-131">**設定. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="a41e1-131">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="a41e1-132">**設定. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="a41e1-132">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





