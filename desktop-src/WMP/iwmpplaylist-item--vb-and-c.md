---
title: 'IWMPPlaylist (VB 和 C ) '
description: 專案屬性 (\_ C \ ) 中的 get 專案方法會取得指定索引處之媒體專案的介面。
ms.assetid: 874663e2-0b89-4ef7-9d4a-3a334482b352
keywords:
- " (VB 和 C ) Windows Media Player 的 IWMPPlaylist 專案"
topic_type:
- apiref
api_name:
- IWMPPlaylist.Item (VB and C )
api_location:
- Interop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d1318f37c3f590eec2c97252e2f484b0d1bc6d83
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106997625"
---
# <a name="iwmpplaylistitem-vb-and-c"></a><span data-ttu-id="dc0d7-104">IWMPPlaylist (VB 和 c # ) </span><span class="sxs-lookup"><span data-stu-id="dc0d7-104">IWMPPlaylist.Item (VB and C#)</span></span>

<span data-ttu-id="dc0d7-105">**Item** 屬性 (c # 中的 **get \_ Item** 方法 ) 取得位於指定索引之媒體專案的介面。</span><span class="sxs-lookup"><span data-stu-id="dc0d7-105">The **Item** property (the **get\_Item** method in C#) gets an interface to the media item at the specified index.</span></span>


```
[Visual Basic]
ReadOnly Property Item(
  lIndex As System.Int32
) As IWMPMedia
```




```
[C#]
IWMPMedia get_Item (
  System.Int32 lIndex 
);
```



## <a name="parameters"></a><span data-ttu-id="dc0d7-106">參數</span><span class="sxs-lookup"><span data-stu-id="dc0d7-106">Parameters</span></span>

<span data-ttu-id="dc0d7-107">*lIndex*</span><span class="sxs-lookup"><span data-stu-id="dc0d7-107">*lIndex*</span></span>

<span data-ttu-id="dc0d7-108">在播放清單中的媒體專案索引的 **system.object** 。</span><span class="sxs-lookup"><span data-stu-id="dc0d7-108">A **System.Int32** that is the index of the media item in the playlist.</span></span>

## <a name="property-value"></a><span data-ttu-id="dc0d7-109">屬性值</span><span class="sxs-lookup"><span data-stu-id="dc0d7-109">Property Value</span></span>

<span data-ttu-id="dc0d7-110">**WMPLib. IWMPMedia** 介面，可讓您存取指定之索引處的媒體專案。</span><span class="sxs-lookup"><span data-stu-id="dc0d7-110">An **WMPLib.IWMPMedia** interface that provides access to the media item at the specified index.</span></span>

## <a name="remarks"></a><span data-ttu-id="dc0d7-111">備註</span><span class="sxs-lookup"><span data-stu-id="dc0d7-111">Remarks</span></span>

<span data-ttu-id="dc0d7-112">**IWMPPlaylist** 在使用參數的 Visual Basic 中是唯讀屬性，而在 c # 中則稱為 **IWMPPlaylist. get \_ Item** 方法。</span><span class="sxs-lookup"><span data-stu-id="dc0d7-112">**IWMPPlaylist.Item** is a read-only property in Visual Basic that takes a parameter, while in C# it is referred to as the **IWMPPlaylist.get\_Item** method.</span></span>

## <a name="examples"></a><span data-ttu-id="dc0d7-113">範例</span><span class="sxs-lookup"><span data-stu-id="dc0d7-113">Examples</span></span>

<span data-ttu-id="dc0d7-114">下列範例會使用 Item 屬性 (c # 中的 **get \_ Item** 方法 ) ，根據使用者選取 **專案** 從播放清單抓取媒體專案。</span><span class="sxs-lookup"><span data-stu-id="dc0d7-114">The following example uses the **Item** property (the **get\_Item** method in C#) to retrieve a media item from a playlist based on a user selection.</span></span> <span data-ttu-id="dc0d7-115">清單方塊是以名稱 weblist 所建立，並填入播放清單中稱為 audioPlaylist 的標題。</span><span class="sxs-lookup"><span data-stu-id="dc0d7-115">A list box was created with the name weblist, and filled with the titles from the playlist called audioPlaylist.</span></span> <span data-ttu-id="dc0d7-116">**AxWMPLib. AxWindowsMediaPlayer** 物件是以名為 player 的變數來表示。</span><span class="sxs-lookup"><span data-stu-id="dc0d7-116">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
private void weblist_SelectedIndexChanged(object sender, System.EventArgs e)
{
    // Store the index of the selected item in the list box.
    int index = ((System.Windows.Forms.ListBox)sender).SelectedIndex;

    // Store the corresponding media item from the playlist.
    WMPLib.IWMPMedia listItem = audioPlaylist.get_Item(index);

    // Set the player URL to the URL of the selected media item.
    player.URL = listItem.sourceURL;
}
```


```VB

Public Sub weblist_SelectedIndexChanged(ByVal sender As Object, ByVal e As System.EventArgs) Handles weblist.SelectedIndexChanged

    &#39; Store the index of the selected item in the list box.
    Dim lb As System.Windows.Forms.ListBox = sender
    Dim index As Integer = lb.SelectedIndex

    &#39; Store the corresponding media item from the playlist.
    Dim listItem As WMPLib.IWMPMedia = audioPlaylist.Item(index)

    &#39; Set the player URL to the URL of the selected media item.
    player.URL = listItem.sourceURL

End Sub
```





## <a name="requirements"></a><span data-ttu-id="dc0d7-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="dc0d7-117">Requirements</span></span>



| <span data-ttu-id="dc0d7-118">需求</span><span class="sxs-lookup"><span data-stu-id="dc0d7-118">Requirement</span></span> | <span data-ttu-id="dc0d7-119">值</span><span class="sxs-lookup"><span data-stu-id="dc0d7-119">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dc0d7-120">版本</span><span class="sxs-lookup"><span data-stu-id="dc0d7-120">Version</span></span><br/>   | <span data-ttu-id="dc0d7-121">Windows Media Player 9 系列或更新版本</span><span class="sxs-lookup"><span data-stu-id="dc0d7-121">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="dc0d7-122">命名空間</span><span class="sxs-lookup"><span data-stu-id="dc0d7-122">Namespace</span></span><br/> | <span data-ttu-id="dc0d7-123">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="dc0d7-123">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="dc0d7-124">組件</span><span class="sxs-lookup"><span data-stu-id="dc0d7-124">Assembly</span></span><br/>  | <dl> <span data-ttu-id="dc0d7-125"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll) </dt></span><span class="sxs-lookup"><span data-stu-id="dc0d7-125"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dc0d7-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="dc0d7-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dc0d7-127">**IWMPMedia 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="dc0d7-127">**IWMPMedia Interface (VB and C#)**</span></span>](iwmpmedia--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="dc0d7-128">**IWMPPlaylist 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="dc0d7-128">**IWMPPlaylist Interface (VB and C#)**</span></span>](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="dc0d7-129">**IWMPPlaylist. insertItem (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="dc0d7-129">**IWMPPlaylist.insertItem (VB and C#)**</span></span>](wmplibiwmpplaylist-iwmpplaylist-insertitem--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="dc0d7-130">**IWMPPlaylist. removeItem (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="dc0d7-130">**IWMPPlaylist.removeItem (VB and C#)**</span></span>](wmplibiwmpplaylist-iwmpplaylist-removeitem--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="dc0d7-131">**IWMPSettings2. mediaAccessRights (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="dc0d7-131">**IWMPSettings2.mediaAccessRights (VB and C#)**</span></span>](wmplibiwmpsettings2-iwmpsettings2-mediaaccessrights--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="dc0d7-132">**IWMPSettings2. requestMediaAccessRights (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="dc0d7-132">**IWMPSettings2.requestMediaAccessRights (VB and C#)**</span></span>](wmplibiwmpsettings2-iwmpsettings2-requestmediaaccessrights--vb-and-c.md)
</dt> </dl>

 

 





