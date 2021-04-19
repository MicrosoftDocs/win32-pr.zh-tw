---
title: MediaCollection 新增方法
description: Add 方法會將新的媒體專案或播放清單新增至程式庫。 |MediaCollection 新增方法
ms.assetid: 8adf93d1-368b-4916-937f-342901a1592b
keywords:
- 新增方法 Windows Media Player
- 新增方法 Windows Media Player、MediaCollection 類別
- MediaCollection 類別 Windows Media Player，add 方法
topic_type:
- apiref
api_name:
- MediaCollection.add
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7731a42c8e1317355b129acb6921676c0a33f4a3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984344"
---
# <a name="mediacollectionadd-method"></a><span data-ttu-id="c35b0-107">MediaCollection 新增方法</span><span class="sxs-lookup"><span data-stu-id="c35b0-107">MediaCollection.add method</span></span>

<span data-ttu-id="c35b0-108">**Add** 方法會將新的媒體專案或播放清單新增至程式庫。</span><span class="sxs-lookup"><span data-stu-id="c35b0-108">The **add** method adds a new media item or playlist to the library.</span></span>

## <a name="syntax"></a><span data-ttu-id="c35b0-109">語法</span><span class="sxs-lookup"><span data-stu-id="c35b0-109">Syntax</span></span>


```JScript
retVal = MediaCollection.add(
  path
)
```



## <a name="parameters"></a><span data-ttu-id="c35b0-110">參數</span><span class="sxs-lookup"><span data-stu-id="c35b0-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c35b0-111">*路徑* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c35b0-111">*path* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c35b0-112">包含路徑的 **字串**。</span><span class="sxs-lookup"><span data-stu-id="c35b0-112">**String** containing the path.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c35b0-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="c35b0-113">Return value</span></span>

<span data-ttu-id="c35b0-114">這個方法會傳回 **媒體** 物件。</span><span class="sxs-lookup"><span data-stu-id="c35b0-114">This method returns a **Media** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="c35b0-115">備註</span><span class="sxs-lookup"><span data-stu-id="c35b0-115">Remarks</span></span>

<span data-ttu-id="c35b0-116">這個方法會將現有的媒體專案或播放清單載入至程式庫，並提供檔案的路徑。</span><span class="sxs-lookup"><span data-stu-id="c35b0-116">This method loads an existing media item or playlist into the library, given a path to a file.</span></span> <span data-ttu-id="c35b0-117">這個方法不會移動或變更檔案。</span><span class="sxs-lookup"><span data-stu-id="c35b0-117">This method does not move or change the file.</span></span> <span data-ttu-id="c35b0-118">如果指定了不正確本機路徑，這個方法將會失敗，但在將數位媒體檔案新增至程式庫之前，不會檢查數位媒體檔案的有效性。</span><span class="sxs-lookup"><span data-stu-id="c35b0-118">This method fails if given an invalid local path, but digital media files are not checked for validity before they are added to the library.</span></span>

<span data-ttu-id="c35b0-119">這個方法會接受靜態和自動播放清單檔案。</span><span class="sxs-lookup"><span data-stu-id="c35b0-119">This method accepts both static and auto playlist files.</span></span> <span data-ttu-id="c35b0-120">*PlaylistCollection*。**importPlaylist** 方法也可以用來將靜態播放清單新增至程式庫。</span><span class="sxs-lookup"><span data-stu-id="c35b0-120">The *PlaylistCollection*.**importPlaylist** method can also be used to add a static playlist to the library.</span></span>

<span data-ttu-id="c35b0-121">若要使用此方法，需要有程式庫的完整存取權。</span><span class="sxs-lookup"><span data-stu-id="c35b0-121">To use this method, full access to the library is required.</span></span> <span data-ttu-id="c35b0-122">如需詳細資訊，請參閱連結 [庫存取](library-access.md)。</span><span class="sxs-lookup"><span data-stu-id="c35b0-122">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="c35b0-123">範例</span><span class="sxs-lookup"><span data-stu-id="c35b0-123">Examples</span></span>

<span data-ttu-id="c35b0-124">下列 Microsoft JScript 範例會將三個媒體物件新增至 Windows Media Player 媒體集合。</span><span class="sxs-lookup"><span data-stu-id="c35b0-124">The following Microsoft JScript example adds three media objects to the Windows Media Player media collection.</span></span> <span data-ttu-id="c35b0-125">使用 ID = "Player" 建立 **player** 物件。</span><span class="sxs-lookup"><span data-stu-id="c35b0-125">The **Player** object was created with ID="Player".</span></span>


```JScript
// Adding a media object using a website.
Player.mediaCollection.add("https://www.proseware.com/Media/Laure.wma");

// Adding a media object from a local network.
// You must add an escape sequence of a backslash for 
// every original backslash.
Player.mediaCollection.add("\\\\yourservername\\Public\\Jeanne.wma");

// Adding a media object from a file on a local drive.
// Be sure to add appropriate escape sequences.
Player.mediaCollection.add("C:\\WMSDK\\WMPSDK\\docs\\samples\\media\\house.wma");
```



## <a name="requirements"></a><span data-ttu-id="c35b0-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="c35b0-126">Requirements</span></span>



| <span data-ttu-id="c35b0-127">需求</span><span class="sxs-lookup"><span data-stu-id="c35b0-127">Requirement</span></span> | <span data-ttu-id="c35b0-128">值</span><span class="sxs-lookup"><span data-stu-id="c35b0-128">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c35b0-129">版本</span><span class="sxs-lookup"><span data-stu-id="c35b0-129">Version</span></span><br/> | <span data-ttu-id="c35b0-130">Windows Media Player 7.0 版或更新版本。</span><span class="sxs-lookup"><span data-stu-id="c35b0-130">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="c35b0-131">DLL</span><span class="sxs-lookup"><span data-stu-id="c35b0-131">DLL</span></span><br/>     | <dl> <span data-ttu-id="c35b0-132"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c35b0-132"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c35b0-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c35b0-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c35b0-134">**管理播放清單**</span><span class="sxs-lookup"><span data-stu-id="c35b0-134">**Managing Playlists**</span></span>](managing-playlists.md)
</dt> <dt>

[<span data-ttu-id="c35b0-135">**媒體物件**</span><span class="sxs-lookup"><span data-stu-id="c35b0-135">**Media Object**</span></span>](media-object.md)
</dt> <dt>

[<span data-ttu-id="c35b0-136">**MediaCollection 物件**</span><span class="sxs-lookup"><span data-stu-id="c35b0-136">**MediaCollection Object**</span></span>](mediacollection-object.md)
</dt> <dt>

[<span data-ttu-id="c35b0-137">**MediaCollection。移除**</span><span class="sxs-lookup"><span data-stu-id="c35b0-137">**MediaCollection.remove**</span></span>](mediacollection-remove.md)
</dt> <dt>

[<span data-ttu-id="c35b0-138">**PlaylistCollection.importPlaylist**</span><span class="sxs-lookup"><span data-stu-id="c35b0-138">**PlaylistCollection.importPlaylist**</span></span>](playlistcollection-importplaylist.md)
</dt> <dt>

[<span data-ttu-id="c35b0-139">**設定. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="c35b0-139">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="c35b0-140">**設定. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="c35b0-140">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





