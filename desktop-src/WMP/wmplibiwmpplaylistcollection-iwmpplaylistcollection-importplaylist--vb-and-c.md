---
title: IWMPPlaylistCollection importPlaylist 方法
description: ImportPlaylist 方法會將靜態播放清單新增至程式庫。 |IWMPPlaylistCollection importPlaylist 方法
ms.assetid: 7a64e618-920d-419d-8769-612ab5dff49b
keywords:
- importPlaylist 方法 Windows Media Player
- importPlaylist 方法 Windows Media Player，IWMPPlaylistCollection 介面
- IWMPPlaylistCollection 介面 Windows Media Player，importPlaylist 方法
topic_type:
- apiref
api_name:
- IWMPPlaylistCollection.importPlaylist
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad3ca727155d6ae859123d427812d93ebaa0b05c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106989691"
---
# <a name="iwmpplaylistcollectionimportplaylist-method"></a><span data-ttu-id="b8820-107">IWMPPlaylistCollection：： importPlaylist 方法</span><span class="sxs-lookup"><span data-stu-id="b8820-107">IWMPPlaylistCollection::importPlaylist method</span></span>

<span data-ttu-id="b8820-108">**ImportPlaylist** 方法會將靜態播放清單新增至程式庫。</span><span class="sxs-lookup"><span data-stu-id="b8820-108">The **importPlaylist** method adds a static playlist to the library.</span></span>

## <a name="syntax"></a><span data-ttu-id="b8820-109">語法</span><span class="sxs-lookup"><span data-stu-id="b8820-109">Syntax</span></span>


```CSharp
public IWMPPlaylist importPlaylist(
  IWMPPlaylist pItem
);
```


```VB

Public Function importPlaylist( _
  ByVal pItem As IWMPPlaylist _
) As IWMPPlaylist
Implements IWMPPlaylistCollection.importPlaylist
```





## <a name="parameters"></a><span data-ttu-id="b8820-110">參數</span><span class="sxs-lookup"><span data-stu-id="b8820-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b8820-111">*pItem* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b8820-111">*pItem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b8820-112">此方法將新增之播放清單的 **WMPLib IWMPPlaylist** 介面。</span><span class="sxs-lookup"><span data-stu-id="b8820-112">A **WMPLib.IWMPPlaylist** interface for the playlist that this method will add.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b8820-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="b8820-113">Return value</span></span>

<span data-ttu-id="b8820-114">已新增播放清單的 **WMPLib IWMPPlaylist** 介面。</span><span class="sxs-lookup"><span data-stu-id="b8820-114">A **WMPLib.IWMPPlaylist** interface for the added playlist.</span></span>

## <a name="remarks"></a><span data-ttu-id="b8820-115">備註</span><span class="sxs-lookup"><span data-stu-id="b8820-115">Remarks</span></span>

<span data-ttu-id="b8820-116">未包含任何媒體專案的播放清單，無法使用此方法新增至程式庫。</span><span class="sxs-lookup"><span data-stu-id="b8820-116">Playlists that do not contain any media items cannot be added to the library by using this method.</span></span> <span data-ttu-id="b8820-117">若要在程式庫中建立空的播放清單，請使用 **[]** 方法。</span><span class="sxs-lookup"><span data-stu-id="b8820-117">To create an empty playlist in the library, use the **newPlaylist** method.</span></span> <span data-ttu-id="b8820-118">然後，您可以使用 **IWMPPlaylist. appendItem** 或 **IWMPPlaylist**，以媒體專案填滿產生的播放清單。</span><span class="sxs-lookup"><span data-stu-id="b8820-118">You can then fill the resulting playlist with media items by using **IWMPPlaylist.appendItem** or **IWMPPlaylist.insertItem**.</span></span>

<span data-ttu-id="b8820-119">如果您將此方法傳遞給自動播放清單，則查詢會執行一次，並將結果以靜態播放清單的形式新增至程式庫。</span><span class="sxs-lookup"><span data-stu-id="b8820-119">If you pass this method an auto playlist, the query is executed once and the result is added to the library as a static playlist.</span></span> <span data-ttu-id="b8820-120">若要將自動播放清單新增至程式庫並保留其自動行為，請使用 **IWMPMediaCollection。**</span><span class="sxs-lookup"><span data-stu-id="b8820-120">To add an auto playlist to the library and preserve its automatic behavior, use **IWMPMediaCollection.add**.</span></span> <span data-ttu-id="b8820-121">如需詳細資訊，請參閱 [靜態和自動播放清單](static-and-auto-playlists.md)。</span><span class="sxs-lookup"><span data-stu-id="b8820-121">For more information, see [Static and Auto Playlists](static-and-auto-playlists.md).</span></span>

<span data-ttu-id="b8820-122">在呼叫這個方法之前，您必須擁有程式庫的讀取權限。</span><span class="sxs-lookup"><span data-stu-id="b8820-122">Before calling this method, you must have read access to the library.</span></span> <span data-ttu-id="b8820-123">如需詳細資訊，請參閱連結 [庫存取](library-access.md)。</span><span class="sxs-lookup"><span data-stu-id="b8820-123">For more information, see [Library Access](library-access.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b8820-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="b8820-124">Requirements</span></span>



| <span data-ttu-id="b8820-125">需求</span><span class="sxs-lookup"><span data-stu-id="b8820-125">Requirement</span></span> | <span data-ttu-id="b8820-126">值</span><span class="sxs-lookup"><span data-stu-id="b8820-126">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b8820-127">版本</span><span class="sxs-lookup"><span data-stu-id="b8820-127">Version</span></span><br/>   | <span data-ttu-id="b8820-128">Windows Media Player  9  系列或更新的版本。</span><span class="sxs-lookup"><span data-stu-id="b8820-128">Windows Media Player 9 Series or later.</span></span><br/>                                                                     |
| <span data-ttu-id="b8820-129">命名空間</span><span class="sxs-lookup"><span data-stu-id="b8820-129">Namespace</span></span><br/> | <span data-ttu-id="b8820-130">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="b8820-130">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="b8820-131">組件</span><span class="sxs-lookup"><span data-stu-id="b8820-131">Assembly</span></span><br/>  | <dl> <span data-ttu-id="b8820-132"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll) </dt></span><span class="sxs-lookup"><span data-stu-id="b8820-132"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b8820-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b8820-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b8820-134">**IWMPMediaCollection：新增 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="b8820-134">**IWMPMediaCollection.add (VB and C#)**</span></span>](wmplibiwmpmediacollection-iwmpmediacollection-add--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="b8820-135">**IWMPPlaylist 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="b8820-135">**IWMPPlaylist Interface (VB and C#)**</span></span>](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="b8820-136">**IWMPPlaylist. appendItem (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="b8820-136">**IWMPPlaylist.appendItem (VB and C#)**</span></span>](wmplibiwmpplaylist-iwmpplaylist-appenditem--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="b8820-137">**IWMPPlaylist. insertItem (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="b8820-137">**IWMPPlaylist.insertItem (VB and C#)**</span></span>](wmplibiwmpplaylist-iwmpplaylist-insertitem--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="b8820-138">**IWMPPlaylistCollection 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="b8820-138">**IWMPPlaylistCollection Interface (VB and C#)**</span></span>](iwmpplaylistcollection--vb-and-c.md)
</dt> <dt>

<span data-ttu-id="b8820-139">[**IWMPPlaylistCollection. [] (VB 和 c # )**](wmplibiwmpplaylistcollection-iwmpplaylistcollection-newplaylist--vb-and-c.md)</span><span class="sxs-lookup"><span data-stu-id="b8820-139">[**IWMPPlaylistCollection.newPlaylist (VB and C#)**](wmplibiwmpplaylistcollection-iwmpplaylistcollection-newplaylist--vb-and-c.md)</span></span>
</dt> </dl>

 

 





