---
title: IWMPMedia sourceURL 屬性
description: SourceURL 屬性會取得媒體專案的 URL。
ms.assetid: adaef82c-eeed-4cce-859b-c54b9c8fa085
keywords:
- sourceURL 屬性 Windows Media Player
- sourceURL 屬性 Windows Media Player，IWMPMedia 介面
- IWMPMedia 介面 Windows Media Player，sourceURL 屬性
topic_type:
- apiref
api_name:
- IWMPMedia.sourceURL
- IWMPMedia.get_sourceURL
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d9ad2cdb2c0a67f65f7b0cf722d1b613307806d7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106992935"
---
# <a name="iwmpmediasourceurl-property"></a><span data-ttu-id="6c645-106">IWMPMedia：： sourceURL 屬性</span><span class="sxs-lookup"><span data-stu-id="6c645-106">IWMPMedia::sourceURL property</span></span>

<span data-ttu-id="6c645-107">**SourceURL** 屬性會取得媒體專案的 URL。</span><span class="sxs-lookup"><span data-stu-id="6c645-107">The **sourceURL** property gets the URL of the media item.</span></span>

<span data-ttu-id="6c645-108">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="6c645-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="6c645-109">語法</span><span class="sxs-lookup"><span data-stu-id="6c645-109">Syntax</span></span>


```CSharp
public System.String sourceURL {get;}
```


```VB

Public ReadOnly Property sourceURL As System.String
```





## <a name="property-value"></a><span data-ttu-id="6c645-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="6c645-110">Property value</span></span>

<span data-ttu-id="6c645-111">作為來源 URL 的 **system.string** 。</span><span class="sxs-lookup"><span data-stu-id="6c645-111">A **System.String** that is the source URL.</span></span>

## <a name="examples"></a><span data-ttu-id="6c645-112">範例</span><span class="sxs-lookup"><span data-stu-id="6c645-112">Examples</span></span>

<span data-ttu-id="6c645-113">下列範例會使用 **sourceURL** 來取出「所有音樂」播放清單中第一個媒體專案的 URL;媒體專案的 URL 接著會指派給 player 物件 URL 屬性。</span><span class="sxs-lookup"><span data-stu-id="6c645-113">The following example uses **sourceURL** to retrieve the URL of the first media item in the "All Music" playlist; the URL of the media item is then assigned to the player object URL property.</span></span> <span data-ttu-id="6c645-114">**AxWMPLib. AxWindowsMediaPlayer** 物件是以名為 player 的變數來表示。</span><span class="sxs-lookup"><span data-stu-id="6c645-114">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Get an interface to the All Music Playlist. 
WMPLib.IWMPPlaylist pl = player.playlistCollection.getByName("All Music").Item(0);

// Store a WMPLib.IWMPMedia3 interface to the first media item in the playlist. 
WMPLib.IWMPMedia3 media = (WMPLib.IWMPMedia3)pl.get_Item(0);

// Change the URL property of the player to the URL of the media item.
player.URL = media.sourceURL;

// Play the media item.
player.Ctlcontrols.play();
```


```VB

' Get an interface to the All Music Playlist. 
Dim pl As WMPLib.IWMPPlaylist = player.playlistCollection.getByName(&quot;All Music&quot;).Item(0)

&#39; Store a WMPLib.IWMPMedia3 interface to the first media item in the playlist. 
Dim media As WMPLib.IWMPMedia3 = pl.Item(0)

&#39; Change the URL property of the player to the URL of the media item.
player.URL = Media.sourceURL

&#39; Play the media item.
player.Ctlcontrols.play()
```





## <a name="requirements"></a><span data-ttu-id="6c645-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="6c645-115">Requirements</span></span>



| <span data-ttu-id="6c645-116">需求</span><span class="sxs-lookup"><span data-stu-id="6c645-116">Requirement</span></span> | <span data-ttu-id="6c645-117">值</span><span class="sxs-lookup"><span data-stu-id="6c645-117">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6c645-118">版本</span><span class="sxs-lookup"><span data-stu-id="6c645-118">Version</span></span><br/>   | <span data-ttu-id="6c645-119">Windows Media Player 9 系列或更新版本</span><span class="sxs-lookup"><span data-stu-id="6c645-119">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="6c645-120">命名空間</span><span class="sxs-lookup"><span data-stu-id="6c645-120">Namespace</span></span><br/> | <span data-ttu-id="6c645-121">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="6c645-121">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="6c645-122">組件</span><span class="sxs-lookup"><span data-stu-id="6c645-122">Assembly</span></span><br/>  | <dl> <span data-ttu-id="6c645-123"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll) </dt></span><span class="sxs-lookup"><span data-stu-id="6c645-123"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6c645-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6c645-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c645-125">**IWMPMedia 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="6c645-125">**IWMPMedia Interface (VB and C#)**</span></span>](iwmpmedia--vb-and-c.md)
</dt> </dl>

 

 





