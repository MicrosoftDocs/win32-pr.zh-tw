---
title: AxWindowsMediaPlayer. currentPlaylist 屬性
description: CurrentPlaylist 屬性會取得或設定目前的 IWMPPlaylist 介面，以提供簡單的方式來組織和動作清單中的媒體專案。
ms.assetid: d5a9f126-a628-499c-a012-8a47c6c987ef
keywords:
- currentPlaylist 屬性 Windows Media Player
- currentPlaylist 屬性 Windows Media Player，AxWindowsMediaPlayer 類別
- AxWindowsMediaPlayer 類別 Windows Media Player，currentPlaylist 屬性
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.currentPlaylist
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a0f5b91a2e65b81fd1f13da0bad5f77c5ea1415
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999297"
---
# <a name="axwindowsmediaplayercurrentplaylist-property"></a><span data-ttu-id="d8709-106">AxWindowsMediaPlayer. currentPlaylist 屬性</span><span class="sxs-lookup"><span data-stu-id="d8709-106">AxWindowsMediaPlayer.currentPlaylist property</span></span>

<span data-ttu-id="d8709-107">CurrentPlaylist 屬性會取得或設定目前的 **IWMPPlaylist** 介面，以提供簡單的方式來組織和動作清單中的媒體專案。</span><span class="sxs-lookup"><span data-stu-id="d8709-107">The currentPlaylist property gets or sets the current **IWMPPlaylist** interface that provides an easy way to organize and manipulate media items in a list.</span></span>

## <a name="syntax"></a><span data-ttu-id="d8709-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="d8709-108">Syntax</span></span>


```CSharp
public IWMPPlaylist currentPlaylist {get; set;}
```


```VB

Public Property currentPlaylist As IWMPPlaylist
```





## <a name="property-value"></a><span data-ttu-id="d8709-109">屬性值</span><span class="sxs-lookup"><span data-stu-id="d8709-109">Property value</span></span>

<span data-ttu-id="d8709-110">提供目前播放清單存取權的 WMPLib. IWMPPlaylist 介面。</span><span class="sxs-lookup"><span data-stu-id="d8709-110">The WMPLib.IWMPPlaylist interface that provides access to the current playlist.</span></span>

## <a name="remarks"></a><span data-ttu-id="d8709-111">備註</span><span class="sxs-lookup"><span data-stu-id="d8709-111">Remarks</span></span>

<span data-ttu-id="d8709-112">如果 IWMPSettings 的屬性 (也可透過 AxWindowsMediaPlayer 存取。**autoStart**) 為 true，每當您設定 **currentPlaylist** 時，就會自動開始播放。</span><span class="sxs-lookup"><span data-stu-id="d8709-112">If the IWMPSettings.autoStart property (also accessed via AxWindowsMediaPlayer.settings.**autoStart**) is true, playback begins automatically whenever you set **currentPlaylist**.</span></span>

<span data-ttu-id="d8709-113">這個屬性會採用 IWMPPlaylist 介面，這可以透過數種方式取得，例如從 *IWMPPlaylistArray* 取得值。**專案** 或 *IWMPPlaylistCollection*。**[]** 屬性。</span><span class="sxs-lookup"><span data-stu-id="d8709-113">This property takes an IWMPPlaylist interface, which can be acquired in several ways, such as by getting the value from the *IWMPPlaylistArray*.**Item** or *IWMPPlaylistCollection*.**newPlaylist** properties.</span></span> <span data-ttu-id="d8709-114">若要使用檔案名載入 **播放清單** 專案，請設定 URL 屬性，或使用 AxWindowsMediaPlayer。**[]**。</span><span class="sxs-lookup"><span data-stu-id="d8709-114">To load a **playlist** item using a file name, set the URL property or use AxWindowsMediaPlayer.**newPlaylist**.</span></span>

## <a name="examples"></a><span data-ttu-id="d8709-115">範例</span><span class="sxs-lookup"><span data-stu-id="d8709-115">Examples</span></span>

<span data-ttu-id="d8709-116">下列範例會抓取媒體櫃中的第一個播放清單，並使用 currentPlaylist 屬性將取出的播放清單設定為目前的播放清單，並顯示其名稱。</span><span class="sxs-lookup"><span data-stu-id="d8709-116">The following example retrieves the first playlist in the library and uses the currentPlaylist property to set the retrieved playlist as the current playlist, and display its name.</span></span> <span data-ttu-id="d8709-117">AxWMPLib. AxWindowsMediaPlayer 物件是以名為 player 的變數來表示。</span><span class="sxs-lookup"><span data-stu-id="d8709-117">The AxWMPLib.AxWindowsMediaPlayer object is represented by the variable named player.</span></span>


```CSharp
// Get an interface to the first playlist from the library. 
WMPLib.IWMPPlaylist firstPlaylist = player.playlistCollection.getAll().Item(0);

// Make the retrieved playlist the current playlist.
player.currentPlaylist = firstPlaylist;

// Display the name of the current playlist.
currentPlaylistLabel.Text = ("Found first playlist. Name = " + player.currentPlaylist.name);
```


```VB

' Get an interface to the first playlist from the library. 
Dim firstPlaylist As WMPLib.IWMPPlaylist = player.playlistCollection.getAll().Item(0)

&#39; Make the retrieved playlist the current playlist.
player.currentPlaylist = firstPlaylist

&#39; Display the name of the current playlist.
currentPlaylistLabel.Text = (&quot;Found first playlist. Name = &quot; + player.currentPlaylist.name)
```





## <a name="requirements"></a><span data-ttu-id="d8709-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="d8709-118">Requirements</span></span>



| <span data-ttu-id="d8709-119">需求</span><span class="sxs-lookup"><span data-stu-id="d8709-119">Requirement</span></span> | <span data-ttu-id="d8709-120">值</span><span class="sxs-lookup"><span data-stu-id="d8709-120">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d8709-121">版本</span><span class="sxs-lookup"><span data-stu-id="d8709-121">Version</span></span><br/>   | <span data-ttu-id="d8709-122">Windows Media Player 9 系列或更新版本</span><span class="sxs-lookup"><span data-stu-id="d8709-122">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="d8709-123">命名空間</span><span class="sxs-lookup"><span data-stu-id="d8709-123">Namespace</span></span><br/> | <span data-ttu-id="d8709-124">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="d8709-124">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="d8709-125">組件</span><span class="sxs-lookup"><span data-stu-id="d8709-125">Assembly</span></span><br/>  | <dl> <span data-ttu-id="d8709-126"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll) </dt></span><span class="sxs-lookup"><span data-stu-id="d8709-126"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d8709-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d8709-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d8709-128">**AxWindowsMediaPlayer 物件 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="d8709-128">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

<span data-ttu-id="d8709-129">[**AxWindowsMediaPlayer. [] (VB 和 c # )**](axwmplib-axwindowsmediaplayer-newplaylist.md)</span><span class="sxs-lookup"><span data-stu-id="d8709-129">[**AxWindowsMediaPlayer.newPlaylist (VB and C#)**](axwmplib-axwindowsmediaplayer-newplaylist.md)</span></span>
</dt> <dt>

[<span data-ttu-id="d8709-130">**AxWindowsMediaPlayer VB 和 c # 的 (設定 )**</span><span class="sxs-lookup"><span data-stu-id="d8709-130">**AxWindowsMediaPlayer.settings (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-settings--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="d8709-131">**IWMPPlaylist 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="d8709-131">**IWMPPlaylist Interface (VB and C#)**</span></span>](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="d8709-132">**IWMPPlaylistArray (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="d8709-132">**IWMPPlaylistArray.Item (VB and C#)**</span></span>](wmplibiwmpplaylistarray-iwmpplaylistarray-item--vb-and-c.md)
</dt> <dt>

<span data-ttu-id="d8709-133">[**IWMPPlaylistCollection. [] (VB 和 c # )**](wmplibiwmpplaylistcollection-iwmpplaylistcollection-newplaylist--vb-and-c.md)</span><span class="sxs-lookup"><span data-stu-id="d8709-133">[**IWMPPlaylistCollection.newPlaylist (VB and C#)**](wmplibiwmpplaylistcollection-iwmpplaylistcollection-newplaylist--vb-and-c.md)</span></span>
</dt> <dt>

[<span data-ttu-id="d8709-134">**IWMPSettings (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="d8709-134">**IWMPSettings.autoStart (VB and C#)**</span></span>](wmplibiwmpsettings-iwmpsettings-autostart--vb-and-c.md)
</dt> </dl>

 

 





