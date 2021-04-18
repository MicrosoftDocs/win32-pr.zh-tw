---
title: IWMPControls playItem 方法
description: PlayItem 方法會播放指定的媒體專案。 |IWMPControls playItem 方法
ms.assetid: ddd4e4f7-475c-4964-a623-9123ed66be8e
keywords:
- playItem 方法 Windows Media Player
- playItem 方法 Windows Media Player，IWMPControls 介面
- IWMPControls 介面 Windows Media Player，playItem 方法
topic_type:
- apiref
api_name:
- IWMPControls.playItem
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b2ac11f93409128eccc88c1d916144615d77476
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106996466"
---
# <a name="iwmpcontrolsplayitem-method"></a><span data-ttu-id="a3621-107">IWMPControls：:p layItem 方法</span><span class="sxs-lookup"><span data-stu-id="a3621-107">IWMPControls::playItem method</span></span>

<span data-ttu-id="a3621-108">**PlayItem** 方法會播放指定的媒體專案。</span><span class="sxs-lookup"><span data-stu-id="a3621-108">The **playItem** method plays the specified media item.</span></span>

## <a name="syntax"></a><span data-ttu-id="a3621-109">語法</span><span class="sxs-lookup"><span data-stu-id="a3621-109">Syntax</span></span>


```CSharp
public void playItem(
  IWMPMedia pIWMPMedia
);
```


```VB

Public Sub playItem( _
  ByVal pIWMPMedia As IWMPMedia _
)
Implements IWMPControls.playItem
```





## <a name="parameters"></a><span data-ttu-id="a3621-110">參數</span><span class="sxs-lookup"><span data-stu-id="a3621-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a3621-111">*pIWMPMedia* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a3621-111">*pIWMPMedia* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a3621-112">媒體專案的 **WMPLib IWMPMedia** 介面。</span><span class="sxs-lookup"><span data-stu-id="a3621-112">A **WMPLib.IWMPMedia** interface to the media item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a3621-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="a3621-113">Return value</span></span>

<span data-ttu-id="a3621-114">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="a3621-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a3621-115">備註</span><span class="sxs-lookup"><span data-stu-id="a3621-115">Remarks</span></span>

<span data-ttu-id="a3621-116">不論 **IWMPSettings** 的值為何，媒體專案都會自動載入並播放。</span><span class="sxs-lookup"><span data-stu-id="a3621-116">The media item will load and play automatically, regardless of the value of the **IWMPSettings.autoStart** property.</span></span> <span data-ttu-id="a3621-117">若要載入專案而不自動播放，請將 **IWMPSettings** 設定為 **false** ，並將值指派給 **AxWindowsMediaPlayer**，之後可以呼叫 **IWMPControls** 來開始播放專案。</span><span class="sxs-lookup"><span data-stu-id="a3621-117">To load an item without playing it automatically, set **IWMPSettings.autoStart** to **false** and assign a value to **AxWindowsMediaPlayer.URL**, after which **IWMPControls.play** can be called to start playing the item.</span></span>

<span data-ttu-id="a3621-118">注意</span><span class="sxs-lookup"><span data-stu-id="a3621-118">Note</span></span>

<span data-ttu-id="a3621-119">**playItem** 僅適用于 **AxWindowsMediaPlayer. currentPlaylist** 中的專案。</span><span class="sxs-lookup"><span data-stu-id="a3621-119">**playItem** works only with items in **AxWindowsMediaPlayer.currentPlaylist**.</span></span> <span data-ttu-id="a3621-120">不支援使用已儲存媒體專案的參考來呼叫 **playItem** 。</span><span class="sxs-lookup"><span data-stu-id="a3621-120">Calling **playItem** with a reference to a saved media item is not supported.</span></span>

## <a name="examples"></a><span data-ttu-id="a3621-121">範例</span><span class="sxs-lookup"><span data-stu-id="a3621-121">Examples</span></span>

<span data-ttu-id="a3621-122">下列範例會使用 **playItem** 來播放目前播放清單中的媒體專案。</span><span class="sxs-lookup"><span data-stu-id="a3621-122">The following example uses **playItem** to play a media item from the current playlist.</span></span> <span data-ttu-id="a3621-123">您可以根據播放清單中的位置，選擇要播放的專案。</span><span class="sxs-lookup"><span data-stu-id="a3621-123">The item to play is chosen based upon its position in the playlist.</span></span> <span data-ttu-id="a3621-124">**AxWMPLib. AxWindowsMediaPlayer** 物件是以名為 player 的變數來表示。</span><span class="sxs-lookup"><span data-stu-id="a3621-124">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Declare a variable to hold the position of the media item 
// in the current playlist. An arbitrary value is supplied here.
int index = 3;

// Get the media item at the fourth position in the current playlist.
WMPLib.IWMPMedia media = player.currentPlaylist.get_Item(index);

// Play the media item.
player.Ctlcontrols.playItem(media);
```


```VB

' Declare a variable to hold the position of the media item 
&#39; in the current playlist. An arbitrary value is supplied here.
Dim index As Integer = 3

&#39; Get the media item at the fourth position in the current playlist.
Dim Media As WMPLib.IWMPMedia = player.currentPlaylist.Item(index)

&#39; Play the media item.
player.Ctlcontrols.playItem(Media)
```





## <a name="requirements"></a><span data-ttu-id="a3621-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="a3621-125">Requirements</span></span>



| <span data-ttu-id="a3621-126">需求</span><span class="sxs-lookup"><span data-stu-id="a3621-126">Requirement</span></span> | <span data-ttu-id="a3621-127">值</span><span class="sxs-lookup"><span data-stu-id="a3621-127">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a3621-128">版本</span><span class="sxs-lookup"><span data-stu-id="a3621-128">Version</span></span><br/>   | <span data-ttu-id="a3621-129">Windows Media Player 9 系列或更新版本</span><span class="sxs-lookup"><span data-stu-id="a3621-129">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="a3621-130">命名空間</span><span class="sxs-lookup"><span data-stu-id="a3621-130">Namespace</span></span><br/> | <span data-ttu-id="a3621-131">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="a3621-131">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="a3621-132">組件</span><span class="sxs-lookup"><span data-stu-id="a3621-132">Assembly</span></span><br/>  | <dl> <span data-ttu-id="a3621-133"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll) </dt></span><span class="sxs-lookup"><span data-stu-id="a3621-133"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a3621-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a3621-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a3621-135">**AxWindowsMediaPlayer. currentPlaylist (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="a3621-135">**AxWindowsMediaPlayer.currentPlaylist (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-currentplaylist--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="a3621-136">**AxWindowsMediaPlayer (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="a3621-136">**AxWindowsMediaPlayer.URL (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-url--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="a3621-137">**IWMPControls 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="a3621-137">**IWMPControls Interface (VB and C#)**</span></span>](iwmpcontrols--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="a3621-138">**IWMPControls (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="a3621-138">**IWMPControls.play (VB and C#)**</span></span>](wmplibiwmpcontrols-iwmpcontrols-play--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="a3621-139">**IWMPPlaylist (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="a3621-139">**IWMPPlaylist.Item (VB and C#)**</span></span>](iwmpplaylist-item--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="a3621-140">**IWMPSettings (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="a3621-140">**IWMPSettings.autoStart (VB and C#)**</span></span>](wmplibiwmpsettings-iwmpsettings-autostart--vb-and-c.md)
</dt> </dl>

 

 





