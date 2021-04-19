---
title: IWMPMedia isMemberOf 方法
description: IsMemberOf 方法會傳回值，指出指定的媒體專案是否為指定播放清單的成員。
ms.assetid: 491e0dd5-38e5-47a5-9c94-f1d27d297f8d
keywords:
- isMemberOf 方法 Windows Media Player
- isMemberOf 方法 Windows Media Player，IWMPMedia 介面
- IWMPMedia 介面 Windows Media Player，isMemberOf 方法
topic_type:
- apiref
api_name:
- IWMPMedia.isMemberOf
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f627e9b2f0e1c4b226dda13d280d521ad52df2ee
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107000967"
---
# <a name="iwmpmediaismemberof-method"></a><span data-ttu-id="8f3f1-106">IWMPMedia：： isMemberOf 方法</span><span class="sxs-lookup"><span data-stu-id="8f3f1-106">IWMPMedia::isMemberOf method</span></span>

<span data-ttu-id="8f3f1-107">**IsMemberOf** 方法會傳回值，指出指定的媒體專案是否為指定播放清單的成員。</span><span class="sxs-lookup"><span data-stu-id="8f3f1-107">The **isMemberOf** method returns a value indicating whether the specified media item is a member of the specified playlist.</span></span>

## <a name="syntax"></a><span data-ttu-id="8f3f1-108">語法</span><span class="sxs-lookup"><span data-stu-id="8f3f1-108">Syntax</span></span>


```CSharp
public System.Boolean isMemberOf(
  IWMPPlaylist pPlaylist
);
```


```VB

Public Function isMemberOf( _
  ByVal pPlaylist As IWMPPlaylist _
) As System.Boolean
Implements IWMPMedia.isMemberOf
```





## <a name="parameters"></a><span data-ttu-id="8f3f1-109">參數</span><span class="sxs-lookup"><span data-stu-id="8f3f1-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8f3f1-110">*pPlaylist* \[在\]</span><span class="sxs-lookup"><span data-stu-id="8f3f1-110">*pPlaylist* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8f3f1-111">**WMPLib IWMPPlaylist** 介面。</span><span class="sxs-lookup"><span data-stu-id="8f3f1-111">A **WMPLib.IWMPPlaylist** interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8f3f1-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="8f3f1-112">Return value</span></span>

<span data-ttu-id="8f3f1-113">System.string **值，** 指出媒體專案是否為播放清單的成員。</span><span class="sxs-lookup"><span data-stu-id="8f3f1-113">A **System.Boolean** value that indicates whether the media item is a member of the playlist.</span></span>

## <a name="remarks"></a><span data-ttu-id="8f3f1-114">備註</span><span class="sxs-lookup"><span data-stu-id="8f3f1-114">Remarks</span></span>

<span data-ttu-id="8f3f1-115">這個方法無法檢查透過 **IWMPMediaCollection** 介面取出的播放清單。</span><span class="sxs-lookup"><span data-stu-id="8f3f1-115">This method cannot check playlists retrieved through the **IWMPMediaCollection** interface.</span></span> <span data-ttu-id="8f3f1-116">若要測試媒體專案是否為特定命名播放清單的成員，請使用 **AxWindowsMediaPlayer. playlistCollection** 屬性取出播放清單集合。</span><span class="sxs-lookup"><span data-stu-id="8f3f1-116">To test whether a media item is a member of a particular named playlist, retrieve the playlist collection with the **AxWindowsMediaPlayer.playlistCollection** property.</span></span> <span data-ttu-id="8f3f1-117">一旦您取得集合，請呼叫 **IWMPPlaylistCollection. getByName** 方法來取出個別播放清單。</span><span class="sxs-lookup"><span data-stu-id="8f3f1-117">Once you retrieve the collection, retrieve the individual playlist by calling the **IWMPPlaylistCollection.getByName** method.</span></span>

<span data-ttu-id="8f3f1-118">在呼叫這個方法之前，您必須擁有程式庫的讀取權限。</span><span class="sxs-lookup"><span data-stu-id="8f3f1-118">Before calling this method, you must have read access to the library.</span></span> <span data-ttu-id="8f3f1-119">如需詳細資訊，請參閱連結 [庫存取](library-access.md)。</span><span class="sxs-lookup"><span data-stu-id="8f3f1-119">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="8f3f1-120">範例</span><span class="sxs-lookup"><span data-stu-id="8f3f1-120">Examples</span></span>

<span data-ttu-id="8f3f1-121">下列範例會使用 **isMemberOf** 來測試目前的媒體專案是否為名為所有音樂的播放清單的成員。</span><span class="sxs-lookup"><span data-stu-id="8f3f1-121">The following example uses **isMemberOf** to test whether the current media item is a member of the playlist named All Music.</span></span> <span data-ttu-id="8f3f1-122">如果不是，則會將目前的媒體專案附加至播放清單。</span><span class="sxs-lookup"><span data-stu-id="8f3f1-122">If it is not, the current media item is appended to the playlist.</span></span> <span data-ttu-id="8f3f1-123">**AxWMPLib. AxWindowsMediaPlayer** 物件是以名為 player 的變數來表示。</span><span class="sxs-lookup"><span data-stu-id="8f3f1-123">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Get an interface to the playlist named All Music.
WMPLib.IWMPPlaylist sPlaylist = player.playlistCollection.getByName("All Music").Item(0);

// Test whether the current media item is a member of the All Music playlist.
// If it is not a member, append the current media item to the playlist.
if (player.currentMedia.isMemberOf(sPlaylist) == false)
{
    sPlaylist.appendItem(player.currentMedia);
}
```


```VB

' Get an interface to the playlist named All Music.
Dim sPlaylist As WMPLib.IWMPPlaylist = player.playlistCollection.getByName(&quot;All Music&quot;).Item(0)

&#39; Test whether the current media item is a member of the All Music playlist.
&#39; If it is not a member, then append the current media item to the playlist.
If (player.currentMedia.isMemberOf(sPlaylist) = False) Then

    sPlaylist.appendItem(player.currentMedia)

End If
```





## <a name="requirements"></a><span data-ttu-id="8f3f1-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="8f3f1-124">Requirements</span></span>



| <span data-ttu-id="8f3f1-125">需求</span><span class="sxs-lookup"><span data-stu-id="8f3f1-125">Requirement</span></span> | <span data-ttu-id="8f3f1-126">值</span><span class="sxs-lookup"><span data-stu-id="8f3f1-126">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8f3f1-127">版本</span><span class="sxs-lookup"><span data-stu-id="8f3f1-127">Version</span></span><br/>   | <span data-ttu-id="8f3f1-128">Windows Media Player 9 系列或更新版本</span><span class="sxs-lookup"><span data-stu-id="8f3f1-128">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="8f3f1-129">命名空間</span><span class="sxs-lookup"><span data-stu-id="8f3f1-129">Namespace</span></span><br/> | <span data-ttu-id="8f3f1-130">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="8f3f1-130">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="8f3f1-131">組件</span><span class="sxs-lookup"><span data-stu-id="8f3f1-131">Assembly</span></span><br/>  | <dl> <span data-ttu-id="8f3f1-132"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll) </dt></span><span class="sxs-lookup"><span data-stu-id="8f3f1-132"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8f3f1-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8f3f1-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8f3f1-134">**AxWindowsMediaPlayer. playlistCollection (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="8f3f1-134">**AxWindowsMediaPlayer.playlistCollection (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-playlistcollection--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="8f3f1-135">**IWMPMedia 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="8f3f1-135">**IWMPMedia Interface (VB and C#)**</span></span>](iwmpmedia--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="8f3f1-136">**IWMPPlaylist 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="8f3f1-136">**IWMPPlaylist Interface (VB and C#)**</span></span>](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="8f3f1-137">**IWMPPlaylistCollection. getByName (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="8f3f1-137">**IWMPPlaylistCollection.getByName (VB and C#)**</span></span>](wmplibiwmpplaylistcollection-iwmpplaylistcollection-getbyname--vb-and-c.md)
</dt> </dl>

 

 





