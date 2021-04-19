---
title: IWMPPlaylistCollection getByName 方法
description: GetByName 方法會傳回 IWMPPlaylistArray 介面，此介面可讓您存取具有指定名稱的播放清單（如果存在的話）。
ms.assetid: d41afab1-4103-4f59-a432-21a502499444
keywords:
- getByName 方法 Windows Media Player
- getByName 方法 Windows Media Player，IWMPPlaylistCollection 介面
- IWMPPlaylistCollection 介面 Windows Media Player，getByName 方法
topic_type:
- apiref
api_name:
- IWMPPlaylistCollection.getByName
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e51f83b4db019286c04762a081e649fec282135e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994822"
---
# <a name="iwmpplaylistcollectiongetbyname-method"></a><span data-ttu-id="a5b2e-106">IWMPPlaylistCollection：： getByName 方法</span><span class="sxs-lookup"><span data-stu-id="a5b2e-106">IWMPPlaylistCollection::getByName method</span></span>

<span data-ttu-id="a5b2e-107">**GetByName** 方法會傳回 **IWMPPlaylistArray** 介面，此介面可讓您存取具有指定名稱的播放清單（如果存在的話）。</span><span class="sxs-lookup"><span data-stu-id="a5b2e-107">The **getByName** method returns a **IWMPPlaylistArray** interface that provides access to playlists with the specified name, if any exist.</span></span>

## <a name="syntax"></a><span data-ttu-id="a5b2e-108">語法</span><span class="sxs-lookup"><span data-stu-id="a5b2e-108">Syntax</span></span>


```CSharp
public IWMPPlaylistArray getByName(
  System.String bstrName
);
```


```VB

Public Function getByName( _
  ByVal bstrName As System.String _
) As IWMPPlaylistArray
Implements IWMPPlaylistCollection.getByName
```





## <a name="parameters"></a><span data-ttu-id="a5b2e-109">參數</span><span class="sxs-lookup"><span data-stu-id="a5b2e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a5b2e-110">*bstrName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a5b2e-110">*bstrName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a5b2e-111">**System.string** ，這是播放清單的名稱。</span><span class="sxs-lookup"><span data-stu-id="a5b2e-111">A **System.String** that is the name of the playlist.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a5b2e-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="a5b2e-112">Return value</span></span>

<span data-ttu-id="a5b2e-113">已抓取之播放清單陣列的 **WMPLib IWMPPlaylistArray** 介面。</span><span class="sxs-lookup"><span data-stu-id="a5b2e-113">A **WMPLib.IWMPPlaylistArray** interface for the retrieved array of playlists.</span></span>

## <a name="remarks"></a><span data-ttu-id="a5b2e-114">備註</span><span class="sxs-lookup"><span data-stu-id="a5b2e-114">Remarks</span></span>

<span data-ttu-id="a5b2e-115">使用 **IWMPPlaylistArray** 來判斷播放清單是否存在。</span><span class="sxs-lookup"><span data-stu-id="a5b2e-115">Use **IWMPPlaylistArray.count** to determine whether a playlist exists.</span></span> <span data-ttu-id="a5b2e-116">如果 **count** 為零，則陣列是空的。</span><span class="sxs-lookup"><span data-stu-id="a5b2e-116">If **count** is zero, the array is empty.</span></span>

<span data-ttu-id="a5b2e-117">在呼叫這個方法之前，您必須擁有程式庫的讀取權限。</span><span class="sxs-lookup"><span data-stu-id="a5b2e-117">Before calling this method, you must have read access to the library.</span></span> <span data-ttu-id="a5b2e-118">如需詳細資訊，請參閱連結 [庫存取](library-access.md)。</span><span class="sxs-lookup"><span data-stu-id="a5b2e-118">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="a5b2e-119">範例</span><span class="sxs-lookup"><span data-stu-id="a5b2e-119">Examples</span></span>

<span data-ttu-id="a5b2e-120">下列範例會使用 **getByName** 來檢查名為「我的最愛--4 和5星級」之播放清單的播放清單集合。</span><span class="sxs-lookup"><span data-stu-id="a5b2e-120">The following example uses **getByName** to check the playlist collection for a playlist named "Favorites -- 4 and 5 star rated".</span></span> <span data-ttu-id="a5b2e-121">如果有該名稱的播放清單存在， **getByName** 會將它設定為目前的播放清單。</span><span class="sxs-lookup"><span data-stu-id="a5b2e-121">If a playlist by that name exists, **getByName** sets it as the current playlist.</span></span> <span data-ttu-id="a5b2e-122">**AxWMPLib. AxWindowsMediaPlayer** 物件是以名為 player 的變數來表示。</span><span class="sxs-lookup"><span data-stu-id="a5b2e-122">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Get the count of the playlists named "Favorites -- 4 and 5 star rated".
int checkit = player.playlistCollection.getByName("Favorites -- 4 and 5 star rated").count;

// Since duplicate playlist names are allowed, the count returned
// will be either zero (no playlist) or greater than zero (playlist exists).
if (checkit > 0)
{
    // Retrieve a playlist array containing "Favorites -- 4 and 5 star rated".
    // Assume that there is only one playlist with that name, and assign it to the 
    // current playlist.
    player.currentPlaylist = player.playlistCollection.getByName("Favorites -- 4 and 5 star rated").Item(0);
}
```


```VB

'  Get the count of the playlists named &quot;Favorites -- 4 and 5 star rated&quot;.
Dim checkit As Integer = player.playlistCollection.getByName(&quot;Favorites -- 4 and 5 star rated&quot;).count

&#39;  Since duplicate playlist names are allowed, the count returned
&#39;  will be either zero (no playlist) or greater than zero (playlist exists).
If (checkit > 0) Then

    &#39;  Retrieve a playlist array object containing &quot;Favorites -- 4 and 5 star rated&quot;.
    &#39;  Assume that there is only one playlist with that name, and assign it to the 
    &#39;  current playlist.
    player.currentPlaylist = player.playlistCollection.getByName(&quot;Favorites -- 4 and 5 star rated&quot;).Item(0)

End If
```





## <a name="requirements"></a><span data-ttu-id="a5b2e-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="a5b2e-123">Requirements</span></span>



| <span data-ttu-id="a5b2e-124">需求</span><span class="sxs-lookup"><span data-stu-id="a5b2e-124">Requirement</span></span> | <span data-ttu-id="a5b2e-125">值</span><span class="sxs-lookup"><span data-stu-id="a5b2e-125">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a5b2e-126">版本</span><span class="sxs-lookup"><span data-stu-id="a5b2e-126">Version</span></span><br/>   | <span data-ttu-id="a5b2e-127">Windows Media Player  9  系列或更新的版本。</span><span class="sxs-lookup"><span data-stu-id="a5b2e-127">Windows Media Player 9 Series or later.</span></span><br/>                                                                     |
| <span data-ttu-id="a5b2e-128">命名空間</span><span class="sxs-lookup"><span data-stu-id="a5b2e-128">Namespace</span></span><br/> | <span data-ttu-id="a5b2e-129">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="a5b2e-129">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="a5b2e-130">組件</span><span class="sxs-lookup"><span data-stu-id="a5b2e-130">Assembly</span></span><br/>  | <dl> <span data-ttu-id="a5b2e-131"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll) </dt></span><span class="sxs-lookup"><span data-stu-id="a5b2e-131"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a5b2e-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a5b2e-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a5b2e-133">**IWMPPlaylistArray 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="a5b2e-133">**IWMPPlaylistArray Interface (VB and C#)**</span></span>](iwmpplaylistarray--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="a5b2e-134">**IWMPPlaylistArray (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="a5b2e-134">**IWMPPlaylistArray.count (VB and C#)**</span></span>](wmplibiwmpplaylistarray-iwmpplaylistarray-count--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="a5b2e-135">**IWMPPlaylistCollection 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="a5b2e-135">**IWMPPlaylistCollection Interface (VB and C#)**</span></span>](iwmpplaylistcollection--vb-and-c.md)
</dt> </dl>

 

 





