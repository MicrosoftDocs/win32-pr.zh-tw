---
title: AxWindowsMediaPlayer. currentMedia 屬性
description: CurrentMedia 屬性會取得或設定對應至目前媒體專案的 IWMPMedia 介面。
ms.assetid: 814ccb1d-713d-4b91-b225-d2199a7c9b6b
keywords:
- currentMedia 屬性 Windows Media Player
- currentMedia 屬性 Windows Media Player，AxWindowsMediaPlayer 類別
- AxWindowsMediaPlayer 類別 Windows Media Player，currentMedia 屬性
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.currentMedia
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3720a36d2a1969c652ed757f31301cf6a9ead706
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106983158"
---
# <a name="axwindowsmediaplayercurrentmedia-property"></a><span data-ttu-id="027ed-106">AxWindowsMediaPlayer. currentMedia 屬性</span><span class="sxs-lookup"><span data-stu-id="027ed-106">AxWindowsMediaPlayer.currentMedia property</span></span>

<span data-ttu-id="027ed-107">CurrentMedia 屬性會取得或設定對應至目前媒體專案的 IWMPMedia 介面。</span><span class="sxs-lookup"><span data-stu-id="027ed-107">The currentMedia property gets or sets the IWMPMedia interface that corresponds to the current media item.</span></span>

## <a name="syntax"></a><span data-ttu-id="027ed-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="027ed-108">Syntax</span></span>


```CSharp
public IWMPMedia currentMedia {get; set;}
```


```VB

Public Property currentMedia As IWMPMedia
```





## <a name="property-value"></a><span data-ttu-id="027ed-109">屬性值</span><span class="sxs-lookup"><span data-stu-id="027ed-109">Property value</span></span>

<span data-ttu-id="027ed-110">WMPLib. IWMPMedia 介面，可提供目前媒體專案的存取權。</span><span class="sxs-lookup"><span data-stu-id="027ed-110">The WMPLib.IWMPMedia interface that provides access to the current media item.</span></span>

## <a name="remarks"></a><span data-ttu-id="027ed-111">備註</span><span class="sxs-lookup"><span data-stu-id="027ed-111">Remarks</span></span>

<span data-ttu-id="027ed-112">如果設定為 AxWindowsMediaPlayer，則為。**autoStart** 屬性為 true，每當您設定 **currentMedia** 時，就會自動開始播放。</span><span class="sxs-lookup"><span data-stu-id="027ed-112">If the AxWindowsMediaPlayer.settings.**autoStart** property is true, playback begins automatically whenever you set **currentMedia**.</span></span>

<span data-ttu-id="027ed-113">您可以 \_ 在 c # ) 中，透過 IWMPPlaylist (IWMPPlaylist. get item 方法取得指定媒體專案的 IWMPMedia 介面。</span><span class="sxs-lookup"><span data-stu-id="027ed-113">You can retrieve an IWMPMedia interface for a given media item through the IWMPPlaylist.Item property (the IWMPPlaylist.get\_Item method in C#).</span></span> <span data-ttu-id="027ed-114">若要使用檔案名載入媒體專案，請設定 URL 屬性，或使用 newMedia。</span><span class="sxs-lookup"><span data-stu-id="027ed-114">To load a media item using a file name, set the URL property or use newMedia.</span></span>

## <a name="examples"></a><span data-ttu-id="027ed-115">範例</span><span class="sxs-lookup"><span data-stu-id="027ed-115">Examples</span></span>

<span data-ttu-id="027ed-116">下列範例會抓取媒體櫃中的第一個媒體專案，並使用 currentMedia 屬性將取出的媒體專案設定為目前的媒體專案，並顯示其名稱。</span><span class="sxs-lookup"><span data-stu-id="027ed-116">The following example retrieves the first media item in the library and uses the currentMedia property to set the retrieved media item as the current media item and display its name.</span></span> <span data-ttu-id="027ed-117">AxWMPLib. AxWindowsMediaPlayer 物件是以名為 player 的變數來表示。</span><span class="sxs-lookup"><span data-stu-id="027ed-117">The AxWMPLib.AxWindowsMediaPlayer object is represented by the variable named player.</span></span>


```CSharp
// Get an interface to the first media item in the library. 
WMPLib.IWMPMedia3 firstMedia = (WMPLib.IWMPMedia3)player.mediaCollection.getAll().get_Item(0);

// Make the retrieved media item the current media item.
player.currentMedia = firstMedia;

// Display the name of the current media item.
currentMediaLabel.Text = ("Found first media item. Name = " + player.currentMedia.name);
```


```VB

' Get an interface to the first media item in the library. 
Dim firstMedia As WMPLib.IWMPMedia3 = player.mediaCollection.getAll().Item(0)

&#39; Make the retrieved media item the current media item.
player.currentMedia = firstMedia

&#39; Display the name of the current media item.
currentMediaLabel.Text = (&quot;Found first media item. Name = &quot; + player.currentMedia.name)
```





## <a name="requirements"></a><span data-ttu-id="027ed-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="027ed-118">Requirements</span></span>



| <span data-ttu-id="027ed-119">需求</span><span class="sxs-lookup"><span data-stu-id="027ed-119">Requirement</span></span> | <span data-ttu-id="027ed-120">值</span><span class="sxs-lookup"><span data-stu-id="027ed-120">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="027ed-121">版本</span><span class="sxs-lookup"><span data-stu-id="027ed-121">Version</span></span><br/>   | <span data-ttu-id="027ed-122">Windows Media Player 9 系列或更新版本</span><span class="sxs-lookup"><span data-stu-id="027ed-122">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="027ed-123">命名空間</span><span class="sxs-lookup"><span data-stu-id="027ed-123">Namespace</span></span><br/> | <span data-ttu-id="027ed-124">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="027ed-124">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="027ed-125">組件</span><span class="sxs-lookup"><span data-stu-id="027ed-125">Assembly</span></span><br/>  | <dl> <span data-ttu-id="027ed-126"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll) </dt></span><span class="sxs-lookup"><span data-stu-id="027ed-126"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="027ed-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="027ed-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="027ed-128">**AxWindowsMediaPlayer 物件 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="027ed-128">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="027ed-129">**AxWindowsMediaPlayer. newMedia (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="027ed-129">**AxWindowsMediaPlayer.newMedia (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-newmedia.md)
</dt> <dt>

[<span data-ttu-id="027ed-130">**AxWindowsMediaPlayer (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="027ed-130">**AxWindowsMediaPlayer.URL (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-url--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="027ed-131">**IWMPMedia 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="027ed-131">**IWMPMedia Interface (VB and C#)**</span></span>](iwmpmedia--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="027ed-132">**IWMPPlaylist (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="027ed-132">**IWMPPlaylist.Item (VB and C#)**</span></span>](iwmpplaylist-item--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="027ed-133">**IWMPSettings (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="027ed-133">**IWMPSettings.autoStart (VB and C#)**</span></span>](wmplibiwmpsettings-iwmpsettings-autostart--vb-and-c.md)
</dt> </dl>

 

 





