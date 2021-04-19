---
title: IWMPCdrom 播放清單屬性
description: 播放清單屬性會取得 IWMPPlaylist 介面，此介面代表 cd 光碟機或 DVD 的根層級標題專案中的曲目。
ms.assetid: 09c3db45-6586-4a5b-b72c-77c64473bdd0
keywords:
- 播放清單屬性 Windows Media Player
- 播放清單屬性 Windows Media Player，IWMPCdrom 介面
- IWMPCdrom 介面 Windows Media Player、播放清單屬性
topic_type:
- apiref
api_name:
- IWMPCdrom.Playlist
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a386881c8416f4ea1881f3ccd68ee4291aa3fa84
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106985575"
---
# <a name="iwmpcdromplaylist-property"></a><span data-ttu-id="3de21-106">IWMPCdrom：:P laylist 屬性</span><span class="sxs-lookup"><span data-stu-id="3de21-106">IWMPCdrom::Playlist property</span></span>

<span data-ttu-id="3de21-107">**播放清單** 屬性會取得 **IWMPPlaylist** 介面，此介面代表 cd 光碟機或 DVD 的根層級標題專案中的曲目。</span><span class="sxs-lookup"><span data-stu-id="3de21-107">The **Playlist** property gets an **IWMPPlaylist** interface representing the tracks on the CD currently in the CD drive or the root-level title entries for a DVD.</span></span>

## <a name="syntax"></a><span data-ttu-id="3de21-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="3de21-108">Syntax</span></span>


```CSharp
public IWMPPlaylist Playlist {get; set;}
```


```VB

Public ReadOnly Property Playlist As IWMPPlaylist
```





## <a name="property-value"></a><span data-ttu-id="3de21-109">屬性值</span><span class="sxs-lookup"><span data-stu-id="3de21-109">Property value</span></span>

<span data-ttu-id="3de21-110">**WMPLib IWMPPlaylist** 介面。</span><span class="sxs-lookup"><span data-stu-id="3de21-110">A **WMPLib.IWMPPlaylist** interface.</span></span>

## <a name="remarks"></a><span data-ttu-id="3de21-111">備註</span><span class="sxs-lookup"><span data-stu-id="3de21-111">Remarks</span></span>

<span data-ttu-id="3de21-112">通常，以 DVD 為基礎的內容會組織成標題。</span><span class="sxs-lookup"><span data-stu-id="3de21-112">Typically, DVD-based content organized into titles.</span></span> <span data-ttu-id="3de21-113">每個標題都包含一或多個章節。</span><span class="sxs-lookup"><span data-stu-id="3de21-113">Each title contains one or more chapters.</span></span> <span data-ttu-id="3de21-114">每個 DVD 的撰寫方式都不同，因此使用標題和章節的方式是由內容作者決定。</span><span class="sxs-lookup"><span data-stu-id="3de21-114">Each DVD is authored differently, so how titles and chapters are used is up to the content author.</span></span>

<span data-ttu-id="3de21-115">若是 DVD，這個屬性會取得播放清單，其中包含做為 **IWMPMedia** 介面（名為 "DVD"）的第一個專案。</span><span class="sxs-lookup"><span data-stu-id="3de21-115">For a DVD, this property gets a playlist that contains as the first item an **IWMPMedia** interface named "DVD".</span></span> <span data-ttu-id="3de21-116">此介面代表 DVD 媒體。</span><span class="sxs-lookup"><span data-stu-id="3de21-116">This interface represents the DVD media.</span></span> <span data-ttu-id="3de21-117">如果播放專案是在插入新 DVD 之後第一次播放，播放該專案會導致 DVD 播放，或在 DVD 與最後一張 DVD 相同時繼續播放。</span><span class="sxs-lookup"><span data-stu-id="3de21-117">Playing the item results in the DVD playing from the beginning if it is the first play after inserting a new DVD, or resuming playback if the DVD is the same as the last DVD viewed.</span></span> <span data-ttu-id="3de21-118">在播放期間將這個專案設定為目前的專案，會從一開始就播放 DVD。</span><span class="sxs-lookup"><span data-stu-id="3de21-118">Setting this item as the current item during playback results in the DVD playing from the beginning.</span></span>

<span data-ttu-id="3de21-119">播放清單中) **IWMPMedia** 介面所代表的其他 (專案，是以嵌套播放清單表示的 DVD 標題。</span><span class="sxs-lookup"><span data-stu-id="3de21-119">Additional items (represented by **IWMPMedia** interfaces) in the playlist are DVD titles that are represented by nested playlists.</span></span> <span data-ttu-id="3de21-120">當您將 **IWMPControls** 設定為等於這些嵌套播放清單專案的其中一個時，Windows Media Player 會在首次播放開始之後，自動將嵌套播放清單設定為目前的播放清單。</span><span class="sxs-lookup"><span data-stu-id="3de21-120">When you set **IWMPControls.currentItem** to equal one of these nested playlist items, Windows Media Player automatically sets the nested playlist as the current playlist after chapter playback begins.</span></span> <span data-ttu-id="3de21-121">然後，您可以使用 **IWMPPlaylist** 介面屬性、方法和相關事件來處理 DVD 章節，也就是播放清單專案。</span><span class="sxs-lookup"><span data-stu-id="3de21-121">You can then use the **IWMPPlaylist** interface properties, methods and associated events to work with DVD chapters, which are also playlist items.</span></span>

<span data-ttu-id="3de21-122">若要取得這個屬性的值，需要有程式庫的讀取權限。</span><span class="sxs-lookup"><span data-stu-id="3de21-122">To retrieve the value of this property, read access to the library is required.</span></span> <span data-ttu-id="3de21-123">如需詳細資訊，請參閱連結 [庫存取](library-access.md)。</span><span class="sxs-lookup"><span data-stu-id="3de21-123">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="3de21-124">範例</span><span class="sxs-lookup"><span data-stu-id="3de21-124">Examples</span></span>

<span data-ttu-id="3de21-125">下列範例會使用 **播放** 清單來填滿名為 myText 的多行文字方塊，以及目前位於第一個 CD 光碟機的音訊 CD 的曲目清單。</span><span class="sxs-lookup"><span data-stu-id="3de21-125">The following example uses **Playlist** to fill a multi-line text box, named myText, with the track list of the audio CD currently in the first CD drive.</span></span> <span data-ttu-id="3de21-126">**AxWMPLib. AxWindowsMediaPlayer** 物件是以名為 player 的變數來表示。</span><span class="sxs-lookup"><span data-stu-id="3de21-126">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Get an interface that provides access to the CD playlist.
WMPLib.IWMPPlaylist playlist = player.cdromCollection.Item(0).Playlist;

// Create a string array to hold the track list.
String[] trackList = new String[playlist.count];

// Iterate through the CD playlist.
for (int i = 0; i < playlist.count; i++)
{
    trackList[i]= playlist.get_Item(i).name;
}

// Display the list of CD tracks in a multi-line text box.
myText.Lines = trackList;
```


```VB

'  Get an interface that provides access to the CD playlist.
Dim playlist As WMPLib.IWMPPlaylist = player.cdromCollection.Item(0).Playlist

&#39;  Create a string array to hold the track list.
Dim trackList(playlist.count) As String

&#39;  Iterate through the CD playlist.
For i As Integer = 0 To (playlist.count - 1)

    trackList(i) = playlist.Item(i).name

Next i

&#39;  Display the list of CD tracks in a multi-line text box.
myText.Lines = trackList
```





## <a name="requirements"></a><span data-ttu-id="3de21-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="3de21-127">Requirements</span></span>



| <span data-ttu-id="3de21-128">需求</span><span class="sxs-lookup"><span data-stu-id="3de21-128">Requirement</span></span> | <span data-ttu-id="3de21-129">值</span><span class="sxs-lookup"><span data-stu-id="3de21-129">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3de21-130">版本</span><span class="sxs-lookup"><span data-stu-id="3de21-130">Version</span></span><br/>   | <span data-ttu-id="3de21-131">Windows Media Player 9 系列或更新版本</span><span class="sxs-lookup"><span data-stu-id="3de21-131">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="3de21-132">命名空間</span><span class="sxs-lookup"><span data-stu-id="3de21-132">Namespace</span></span><br/> | <span data-ttu-id="3de21-133">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="3de21-133">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="3de21-134">組件</span><span class="sxs-lookup"><span data-stu-id="3de21-134">Assembly</span></span><br/>  | <dl> <span data-ttu-id="3de21-135"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll) </dt></span><span class="sxs-lookup"><span data-stu-id="3de21-135"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3de21-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3de21-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3de21-137">**IWMPCdrom 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="3de21-137">**IWMPCdrom Interface (VB and C#)**</span></span>](iwmpcdrom--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="3de21-138">**IWMPControls. currentItem (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="3de21-138">**IWMPControls.currentItem (VB and C#)**</span></span>](wmplibiwmpcontrols-iwmpcontrols-currentitem--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="3de21-139">**IWMPMedia 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="3de21-139">**IWMPMedia Interface (VB and C#)**</span></span>](iwmpmedia--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="3de21-140">**IWMPPlaylist 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="3de21-140">**IWMPPlaylist Interface (VB and C#)**</span></span>](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="3de21-141">**IWMPSettings2. mediaAccessRights (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="3de21-141">**IWMPSettings2.mediaAccessRights (VB and C#)**</span></span>](wmplibiwmpsettings2-iwmpsettings2-mediaaccessrights--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="3de21-142">**IWMPSettings2. requestMediaAccessRights (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="3de21-142">**IWMPSettings2.requestMediaAccessRights (VB and C#)**</span></span>](wmplibiwmpsettings2-iwmpsettings2-requestmediaaccessrights--vb-and-c.md)
</dt> </dl>

 

 





