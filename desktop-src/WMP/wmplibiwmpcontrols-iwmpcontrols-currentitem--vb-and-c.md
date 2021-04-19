---
title: IWMPControls currentItem 屬性
description: CurrentItem 屬性會取得或設定播放清單中目前的媒體專案。
ms.assetid: 0a331b1f-95bd-48ea-b951-1ca35cc96865
keywords:
- currentItem 屬性 Windows Media Player
- currentItem 屬性 Windows Media Player，IWMPControls 介面
- IWMPControls 介面 Windows Media Player，currentItem 屬性
topic_type:
- apiref
api_name:
- IWMPControls.currentItem
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aae04eb333e2fd347fa6f88b33ec2482a4dd8fd7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990806"
---
# <a name="iwmpcontrolscurrentitem-property"></a><span data-ttu-id="1d236-106">IWMPControls：： currentItem 屬性</span><span class="sxs-lookup"><span data-stu-id="1d236-106">IWMPControls::currentItem property</span></span>

<span data-ttu-id="1d236-107">**CurrentItem** 屬性會取得或設定播放清單中目前的媒體專案。</span><span class="sxs-lookup"><span data-stu-id="1d236-107">The **currentItem** property gets or sets the current media item in a playlist.</span></span>

## <a name="syntax"></a><span data-ttu-id="1d236-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="1d236-108">Syntax</span></span>


```CSharp
public IWMPMedia currentItem {get; set;}
```


```VB

Public Property currentItem As IWMPMedia
```





## <a name="property-value"></a><span data-ttu-id="1d236-109">屬性值</span><span class="sxs-lookup"><span data-stu-id="1d236-109">Property value</span></span>

<span data-ttu-id="1d236-110">表示媒體專案的 **WMPLib IWMPMedia** 介面。</span><span class="sxs-lookup"><span data-stu-id="1d236-110">A **WMPLib.IWMPMedia** interface that represents the media item.</span></span>

## <a name="remarks"></a><span data-ttu-id="1d236-111">備註</span><span class="sxs-lookup"><span data-stu-id="1d236-111">Remarks</span></span>

<span data-ttu-id="1d236-112">這個屬性只適用于目前播放清單中的專案。</span><span class="sxs-lookup"><span data-stu-id="1d236-112">This property works only with items in the current playlist.</span></span> <span data-ttu-id="1d236-113">不支援將 **currentItem** 設定為儲存媒體專案的介面。</span><span class="sxs-lookup"><span data-stu-id="1d236-113">Setting **currentItem** to the interface of a saved media item is not supported.</span></span>

## <a name="examples"></a><span data-ttu-id="1d236-114">範例</span><span class="sxs-lookup"><span data-stu-id="1d236-114">Examples</span></span>

<span data-ttu-id="1d236-115">下列範例會使用 **currentItem** ，將播放程式的目前媒體專案設定為從清單方塊中選取的專案。</span><span class="sxs-lookup"><span data-stu-id="1d236-115">The following example uses **currentItem** to set the player's current media item to an item selected from a list box.</span></span> <span data-ttu-id="1d236-116">清單方塊已填滿目前播放清單中的所有專案。</span><span class="sxs-lookup"><span data-stu-id="1d236-116">The list box has been filled with all of the items in the current playlist.</span></span> <span data-ttu-id="1d236-117">**AxWMPLib. AxWindowsMediaPlayer** 物件是以名為 player 的變數來表示。</span><span class="sxs-lookup"><span data-stu-id="1d236-117">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
private void playItem_OnSelectedIndexChanged(object sender, System.EventArgs e)
{
    int selectedItem = ((System.Windows.Forms.ListBox)sender).SelectedIndex;

    // Ensure that the previous media item is stopped.
    player.Ctlcontrols.stop();

    // Set the current item to the item selected from the list box.
    player.Ctlcontrols.currentItem = player.currentPlaylist.get_Item(selectedItem);
    
    // Play the current item.
    player.Ctlcontrols.play();
}
```


```VB

Public Sub playItem_SelectedIndexChanged(ByVal sender As Object, ByVal e As System.EventArgs) Handles playItem.SelectedIndexChanged

    Dim lb As System.Windows.Forms.ListBox = sender
    Dim selectedItem As Integer = lb.SelectedIndex

    &#39; Ensure that the previous media item is stopped.
    player.Ctlcontrols.stop()

    &#39; Set the current item to the item selected from the list box.
    player.Ctlcontrols.currentItem = player.currentPlaylist.Item(selectedItem)

    &#39; Play the current item.
    player.Ctlcontrols.play()

End Sub
```





## <a name="requirements"></a><span data-ttu-id="1d236-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="1d236-118">Requirements</span></span>



| <span data-ttu-id="1d236-119">需求</span><span class="sxs-lookup"><span data-stu-id="1d236-119">Requirement</span></span> | <span data-ttu-id="1d236-120">值</span><span class="sxs-lookup"><span data-stu-id="1d236-120">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1d236-121">版本</span><span class="sxs-lookup"><span data-stu-id="1d236-121">Version</span></span><br/>   | <span data-ttu-id="1d236-122">Windows Media Player 9 系列或更新版本</span><span class="sxs-lookup"><span data-stu-id="1d236-122">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="1d236-123">命名空間</span><span class="sxs-lookup"><span data-stu-id="1d236-123">Namespace</span></span><br/> | <span data-ttu-id="1d236-124">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="1d236-124">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="1d236-125">組件</span><span class="sxs-lookup"><span data-stu-id="1d236-125">Assembly</span></span><br/>  | <dl> <span data-ttu-id="1d236-126"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll) </dt></span><span class="sxs-lookup"><span data-stu-id="1d236-126"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1d236-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1d236-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1d236-128">**IWMPControlsInterface (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="1d236-128">**IWMPControlsInterface (VB and C#)**</span></span>](iwmpcontrols--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="1d236-129">**IWMPMediaInterface (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="1d236-129">**IWMPMediaInterface (VB and C#)**</span></span>](iwmpmedia--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="1d236-130">**IWMPPlaylistCollection. getByName (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="1d236-130">**IWMPPlaylistCollection.getByName(VB and C#)**</span></span>](wmplibiwmpplaylistcollection-iwmpplaylistcollection-getbyname--vb-and-c.md)
</dt> </dl>

 

 





