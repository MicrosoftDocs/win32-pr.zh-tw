---
title: IWMPControls currentMarker 屬性
description: CurrentMarker 屬性會取得或設定目前的標記編號。
ms.assetid: faf8c32a-66de-47ce-aa3d-6699d9f9bdda
keywords:
- currentMarker 屬性 Windows Media Player
- currentMarker 屬性 Windows Media Player，IWMPControls 介面
- IWMPControls 介面 Windows Media Player，currentMarker 屬性
topic_type:
- apiref
api_name:
- IWMPControls.currentMarker
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bfbcea42594b15b8da08248d38b5d8f72a1de29d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106996053"
---
# <a name="iwmpcontrolscurrentmarker-property"></a><span data-ttu-id="5b3d2-106">IWMPControls：： currentMarker 屬性</span><span class="sxs-lookup"><span data-stu-id="5b3d2-106">IWMPControls::currentMarker property</span></span>

<span data-ttu-id="5b3d2-107">**CurrentMarker** 屬性會取得或設定目前的標記編號。</span><span class="sxs-lookup"><span data-stu-id="5b3d2-107">The **currentMarker** property gets or sets the current marker number.</span></span>

## <a name="syntax"></a><span data-ttu-id="5b3d2-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="5b3d2-108">Syntax</span></span>


```CSharp
public System.Int32 currentMarker {get; set;}
```


```VB

Public Property currentMarker As System.Int32
```





## <a name="property-value"></a><span data-ttu-id="5b3d2-109">屬性值</span><span class="sxs-lookup"><span data-stu-id="5b3d2-109">Property value</span></span>

<span data-ttu-id="5b3d2-110">System.string **，這是標記編號。**</span><span class="sxs-lookup"><span data-stu-id="5b3d2-110">A **System.Int32** that is the marker number.</span></span>

## <a name="remarks"></a><span data-ttu-id="5b3d2-111">備註</span><span class="sxs-lookup"><span data-stu-id="5b3d2-111">Remarks</span></span>

<span data-ttu-id="5b3d2-112">設定 **currentMarker** 會導致播放從指定的標記開始。</span><span class="sxs-lookup"><span data-stu-id="5b3d2-112">Setting **currentMarker** causes playback to start from the specified marker.</span></span> <span data-ttu-id="5b3d2-113">嘗試設定 **currentMarker** 之前，請先判斷檔案是否有標記，以及它有多少使用 **IWMPMedia. markerCount**。</span><span class="sxs-lookup"><span data-stu-id="5b3d2-113">Before attempting to set **currentMarker**, determine whether a file has markers and how many it has by using **IWMPMedia.markerCount**.</span></span> <span data-ttu-id="5b3d2-114">如果檔案沒有標記，請將 **currentMarker** 設定為任何值，但不會產生錯誤。</span><span class="sxs-lookup"><span data-stu-id="5b3d2-114">If a file has no markers, setting **currentMarker** to anything but zero results in an error.</span></span> <span data-ttu-id="5b3d2-115">將 **currentMarker** 設定為大於 **markerCount** 的數位也會導致錯誤。</span><span class="sxs-lookup"><span data-stu-id="5b3d2-115">Setting **currentMarker** to a number higher than **markerCount** also results in an error.</span></span>

<span data-ttu-id="5b3d2-116">**CurrentMarker** 屬性一律會傳回目前的或最後一個標記，這表示實際的檔案位置可以是目前標記或下一個標記之前的位置。</span><span class="sxs-lookup"><span data-stu-id="5b3d2-116">The **currentMarker** property always returns the current or last marker, which means the actual file position can be either at the current marker or before the next marker.</span></span> <span data-ttu-id="5b3d2-117">標記從1開始編號，因此，如果檔案有標記，您可以將 **currentMarker** 設定為零，將檔案位置變更為零。</span><span class="sxs-lookup"><span data-stu-id="5b3d2-117">Markers are numbered beginning at 1, so if a file has markers, you can set **currentMarker** to zero to change the file position to zero.</span></span>

<span data-ttu-id="5b3d2-118">在目前的媒體專案設定 (使用 **AxWindowsMediaPlayer. URL** 或 **AxWindowsMediaPlayer. currentMedia**) 之前， **currentMarker** 會傳回零。</span><span class="sxs-lookup"><span data-stu-id="5b3d2-118">Until the current media item is set (using **AxWindowsMediaPlayer.URL** or **AxWindowsMediaPlayer.currentMedia**), **currentMarker** returns zero.</span></span>

## <a name="examples"></a><span data-ttu-id="5b3d2-119">範例</span><span class="sxs-lookup"><span data-stu-id="5b3d2-119">Examples</span></span>

<span data-ttu-id="5b3d2-120">下列範例會使用 **currentMarker** ，從對應至清單方塊（已填入標記識別項）之 SelectedIndex 屬性的標記開始播放影片。</span><span class="sxs-lookup"><span data-stu-id="5b3d2-120">The following example uses **currentMarker** to start video playback from the marker that corresponds to the SelectedIndex property of a list box which has been filled with marker identifiers.</span></span> <span data-ttu-id="5b3d2-121">**AxWMPLib. AxWindowsMediaPlayer** 物件是以名為 player 的變數來表示。</span><span class="sxs-lookup"><span data-stu-id="5b3d2-121">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Fill the list box with the marker identifiers of the current media item.
markers.Items.Add("Begining");
markers.Items.Add("Sunrise");
markers.Items.Add("Car chase");
markers.Items.Add("Happy ending");

// Set the currentMarker to the marker selected from the list box.
private void markers_OnSelectedIndexChanged(object sender, System.EventArgs e)
{
    int selectedMarker = ((System.Windows.Forms.ListBox)sender).SelectedIndex;

    player.Ctlcontrols.currentMarker = selectedMarker;
}
```


```VB

' Fill the list box with the marker identifiers of the current media item.
markers.Items.Add(&quot;Begining&quot;)
markers.Items.Add(&quot;Sunrise&quot;)
markers.Items.Add(&quot;Car chase&quot;)
markers.Items.Add(&quot;Happy ending&quot;)

&#39; Set the currentMarker to the marker selected from the list box.
Public Sub markers_SelectedIndexChanged(ByVal sender As Object, ByVal e As System.EventArgs) Handles markers.SelectedIndexChanged

    Dim lb As System.Windows.Forms.ListBox = sender
    Dim selectedMarker As Integer = lb.SelectedIndex

    player.Ctlcontrols.currentMarker = selectedMarker

End Sub
```





## <a name="requirements"></a><span data-ttu-id="5b3d2-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="5b3d2-122">Requirements</span></span>



| <span data-ttu-id="5b3d2-123">需求</span><span class="sxs-lookup"><span data-stu-id="5b3d2-123">Requirement</span></span> | <span data-ttu-id="5b3d2-124">值</span><span class="sxs-lookup"><span data-stu-id="5b3d2-124">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5b3d2-125">版本</span><span class="sxs-lookup"><span data-stu-id="5b3d2-125">Version</span></span><br/>   | <span data-ttu-id="5b3d2-126">Windows Media Player 9 系列或更新版本</span><span class="sxs-lookup"><span data-stu-id="5b3d2-126">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="5b3d2-127">命名空間</span><span class="sxs-lookup"><span data-stu-id="5b3d2-127">Namespace</span></span><br/> | <span data-ttu-id="5b3d2-128">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="5b3d2-128">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="5b3d2-129">組件</span><span class="sxs-lookup"><span data-stu-id="5b3d2-129">Assembly</span></span><br/>  | <dl> <span data-ttu-id="5b3d2-130"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll) </dt></span><span class="sxs-lookup"><span data-stu-id="5b3d2-130"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5b3d2-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5b3d2-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5b3d2-132">**AxWindowsMediaPlayer. currentMedia (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="5b3d2-132">**AxWindowsMediaPlayer.currentMedia (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-currentmedia--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="5b3d2-133">**AxWindowsMediaPlayer (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="5b3d2-133">**AxWindowsMediaPlayer.URL (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-url--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="5b3d2-134">**IWMPControls 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="5b3d2-134">**IWMPControls Interface (VB and C#)**</span></span>](iwmpcontrols--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="5b3d2-135">**IWMPMedia. markerCount (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="5b3d2-135">**IWMPMedia.markerCount (VB and C#)**</span></span>](wmplibiwmpmedia-iwmpmedia-markercount--vb-and-c.md)
</dt> </dl>

 

 





