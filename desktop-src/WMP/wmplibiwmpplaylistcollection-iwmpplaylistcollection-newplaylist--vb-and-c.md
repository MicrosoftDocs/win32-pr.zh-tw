---
title: IWMPPlaylistCollection [] 方法
description: '[] 方法會傳回程式庫中新的空白播放清單的 IWMPPlaylist 介面。'
ms.assetid: cc0cb356-9a90-421c-8d1a-b79585f71124
keywords:
- '[] 方法 Windows Media Player'
- '[] 方法 Windows Media Player，IWMPPlaylistCollection 介面'
- IWMPPlaylistCollection 介面 Windows Media Player，[] 方法
topic_type:
- apiref
api_name:
- IWMPPlaylistCollection.newPlaylist
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bbc455c5815cee1aaac139886bca1d847ddc62b2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106981098"
---
# <a name="iwmpplaylistcollectionnewplaylist-method"></a><span data-ttu-id="bf6fa-106">IWMPPlaylistCollection：： [] 方法</span><span class="sxs-lookup"><span data-stu-id="bf6fa-106">IWMPPlaylistCollection::newPlaylist method</span></span>

<span data-ttu-id="bf6fa-107">**[]** 方法會傳回程式庫中新的空白播放清單的 **IWMPPlaylist** 介面。</span><span class="sxs-lookup"><span data-stu-id="bf6fa-107">The **newPlaylist** method returns an **IWMPPlaylist** interface for a new, empty playlist in the library.</span></span>

## <a name="syntax"></a><span data-ttu-id="bf6fa-108">語法</span><span class="sxs-lookup"><span data-stu-id="bf6fa-108">Syntax</span></span>


```CSharp
public IWMPPlaylist newPlaylist(
  System.String bstrName
);
```


```VB

Public Function newPlaylist( _
  ByVal bstrName As System.String _
) As IWMPPlaylist
Implements IWMPPlaylistCollection.newPlaylist
```





## <a name="parameters"></a><span data-ttu-id="bf6fa-109">參數</span><span class="sxs-lookup"><span data-stu-id="bf6fa-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bf6fa-110">*bstrName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="bf6fa-110">*bstrName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bf6fa-111">**System.string** ，這是新播放清單的名稱。</span><span class="sxs-lookup"><span data-stu-id="bf6fa-111">A **System.String** that is the name of the new playlist.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bf6fa-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="bf6fa-112">Return value</span></span>

<span data-ttu-id="bf6fa-113">新播放清單的 **WMPLib IWMPPlaylist** 介面。</span><span class="sxs-lookup"><span data-stu-id="bf6fa-113">A **WMPLib.IWMPPlaylist** interface for the new playlist.</span></span>

## <a name="remarks"></a><span data-ttu-id="bf6fa-114">備註</span><span class="sxs-lookup"><span data-stu-id="bf6fa-114">Remarks</span></span>

<span data-ttu-id="bf6fa-115">這個方法會在文件庫中建立空的播放清單。</span><span class="sxs-lookup"><span data-stu-id="bf6fa-115">This method creates an empty playlist in the library.</span></span> <span data-ttu-id="bf6fa-116">若要以媒體專案填滿播放清單，請使用 **IWMPPlaylist. appendItem** 或 **IWMPPlaylist. insertItem**。</span><span class="sxs-lookup"><span data-stu-id="bf6fa-116">To fill the playlist with media items, use **IWMPPlaylist.appendItem** or **IWMPPlaylist.insertItem**.</span></span>

<span data-ttu-id="bf6fa-117">程式庫中允許有多個具有相同名稱的播放清單。</span><span class="sxs-lookup"><span data-stu-id="bf6fa-117">Multiple playlists having the same name are permitted in the library.</span></span> <span data-ttu-id="bf6fa-118">若要避免使用這個方法建立重複的播放清單名稱，請使用 **getByName** 方法和 **IWMPPlaylistArray** 來探索具有特定名稱的播放清單是否已存在。</span><span class="sxs-lookup"><span data-stu-id="bf6fa-118">To avoid creating a duplicate playlist name with this method, use the **getByName** method and **IWMPPlaylistArray.count** to discover whether a playlist with a particular name already exists.</span></span>

<span data-ttu-id="bf6fa-119">播放清單名稱中不允許前置和尾端空格，並且會自動從 *bstrName* 參數指定的值中移除。</span><span class="sxs-lookup"><span data-stu-id="bf6fa-119">Leading and trailing spaces are not permitted in playlist names, and are automatically removed from the value specified for the *bstrName* parameter.</span></span>

<span data-ttu-id="bf6fa-120">在呼叫這個方法之前，您必須擁有程式庫的完整存取權。</span><span class="sxs-lookup"><span data-stu-id="bf6fa-120">Before calling this method, you must have full access to the library.</span></span> <span data-ttu-id="bf6fa-121">如需詳細資訊，請參閱連結 [庫存取](library-access.md)。</span><span class="sxs-lookup"><span data-stu-id="bf6fa-121">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="bf6fa-122">範例</span><span class="sxs-lookup"><span data-stu-id="bf6fa-122">Examples</span></span>

<span data-ttu-id="bf6fa-123">下列範例會建立名為 "ThreeList" 的新空白播放清單，並將其新增至播放清單集合，並將介面傳回給它。</span><span class="sxs-lookup"><span data-stu-id="bf6fa-123">The following example creates a new empty playlist called "ThreeList", adds it to the playlist collection, and returns an interface to it.</span></span> <span data-ttu-id="bf6fa-124">**AxWMPLib. AxWindowsMediaPlayer** 物件是以名為 player 的變數來表示。</span><span class="sxs-lookup"><span data-stu-id="bf6fa-124">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Add a new empty playlist, named ThreeList, to the playlist collection.
WMPLib.IWMPPlaylist newList = player.playlistCollection.newPlaylist("ThreeList");
```


```VB

'  Add a new empty playlist, named ThreeList, to the playlist collection.
Dim newList As WMPLib.IWMPPlaylist = player.playlistCollection.newPlaylist(&quot;ThreeList&quot;)
```





## <a name="requirements"></a><span data-ttu-id="bf6fa-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="bf6fa-125">Requirements</span></span>



| <span data-ttu-id="bf6fa-126">需求</span><span class="sxs-lookup"><span data-stu-id="bf6fa-126">Requirement</span></span> | <span data-ttu-id="bf6fa-127">值</span><span class="sxs-lookup"><span data-stu-id="bf6fa-127">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bf6fa-128">版本</span><span class="sxs-lookup"><span data-stu-id="bf6fa-128">Version</span></span><br/>   | <span data-ttu-id="bf6fa-129">Windows Media Player  9  系列或更新的版本。</span><span class="sxs-lookup"><span data-stu-id="bf6fa-129">Windows Media Player 9 Series or later.</span></span><br/>                                                                     |
| <span data-ttu-id="bf6fa-130">命名空間</span><span class="sxs-lookup"><span data-stu-id="bf6fa-130">Namespace</span></span><br/> | <span data-ttu-id="bf6fa-131">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="bf6fa-131">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="bf6fa-132">組件</span><span class="sxs-lookup"><span data-stu-id="bf6fa-132">Assembly</span></span><br/>  | <dl> <span data-ttu-id="bf6fa-133"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll) </dt></span><span class="sxs-lookup"><span data-stu-id="bf6fa-133"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bf6fa-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bf6fa-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bf6fa-135">**IWMPPlaylist 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="bf6fa-135">**IWMPPlaylist Interface (VB and C#)**</span></span>](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="bf6fa-136">**IWMPPlaylist. appendItem (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="bf6fa-136">**IWMPPlaylist.appendItem (VB and C#)**</span></span>](wmplibiwmpplaylist-iwmpplaylist-appenditem--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="bf6fa-137">**IWMPPlaylist. insertItem (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="bf6fa-137">**IWMPPlaylist.insertItem (VB and C#)**</span></span>](wmplibiwmpplaylist-iwmpplaylist-insertitem--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="bf6fa-138">**IWMPPlaylistArray (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="bf6fa-138">**IWMPPlaylistArray.count (VB and C#)**</span></span>](wmplibiwmpplaylistarray-iwmpplaylistarray-count--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="bf6fa-139">**IWMPPlaylistCollection 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="bf6fa-139">**IWMPPlaylistCollection Interface (VB and C#)**</span></span>](iwmpplaylistcollection--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="bf6fa-140">**IWMPPlaylistCollection. getByName (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="bf6fa-140">**IWMPPlaylistCollection.getByName (VB and C#)**</span></span>](wmplibiwmpplaylistcollection-iwmpplaylistcollection-getbyname--vb-and-c.md)
</dt> </dl>

 

 





