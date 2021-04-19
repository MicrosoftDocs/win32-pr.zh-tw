---
title: IWMPPlaylist appendItem 方法
description: AppendItem 方法會將媒體專案新增至播放清單的結尾。
ms.assetid: d659298b-ec4e-4771-8e9b-8cfd7b3e0eb2
keywords:
- appendItem 方法 Windows Media Player
- appendItem 方法 Windows Media Player，IWMPPlaylist 介面
- IWMPPlaylist 介面 Windows Media Player，appendItem 方法
topic_type:
- apiref
api_name:
- IWMPPlaylist.appendItem
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a94e1b515ec6301830af2de06bae32602bdf66e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993623"
---
# <a name="iwmpplaylistappenditem-method"></a><span data-ttu-id="d8c6a-106">IWMPPlaylist：： appendItem 方法</span><span class="sxs-lookup"><span data-stu-id="d8c6a-106">IWMPPlaylist::appendItem method</span></span>

<span data-ttu-id="d8c6a-107">**AppendItem** 方法會將媒體專案新增至播放清單的結尾。</span><span class="sxs-lookup"><span data-stu-id="d8c6a-107">The **appendItem** method adds a media item to the end of a playlist.</span></span>

## <a name="syntax"></a><span data-ttu-id="d8c6a-108">語法</span><span class="sxs-lookup"><span data-stu-id="d8c6a-108">Syntax</span></span>


```CSharp
public void appendItem(
  IWMPMedia pIWMPMedia
);
```


```VB

Public Sub appendItem( _
  ByVal pIWMPMedia As IWMPMedia _
)
Implements IWMPPlaylist.appendItem
```





## <a name="parameters"></a><span data-ttu-id="d8c6a-109">參數</span><span class="sxs-lookup"><span data-stu-id="d8c6a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d8c6a-110">*pIWMPMedia* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d8c6a-110">*pIWMPMedia* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d8c6a-111">代表要附加之媒體專案的 **WMPLib IWMPMedia** 介面。</span><span class="sxs-lookup"><span data-stu-id="d8c6a-111">An **WMPLib.IWMPMedia** interface that represents the media item to be appended.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d8c6a-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="d8c6a-112">Return value</span></span>

<span data-ttu-id="d8c6a-113">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="d8c6a-113">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d8c6a-114">備註</span><span class="sxs-lookup"><span data-stu-id="d8c6a-114">Remarks</span></span>

<span data-ttu-id="d8c6a-115">在呼叫這個方法之前，您必須擁有程式庫的完整存取權。</span><span class="sxs-lookup"><span data-stu-id="d8c6a-115">Before calling this method, you must have full access to the library.</span></span> <span data-ttu-id="d8c6a-116">如需詳細資訊，請參閱連結 [庫存取](library-access.md)。</span><span class="sxs-lookup"><span data-stu-id="d8c6a-116">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="d8c6a-117">範例</span><span class="sxs-lookup"><span data-stu-id="d8c6a-117">Examples</span></span>

<span data-ttu-id="d8c6a-118">下列範例會使用 **appendItem** 將目前的媒體專案新增至名為 "ThreeList" 的播放清單。</span><span class="sxs-lookup"><span data-stu-id="d8c6a-118">The following example uses **appendItem** to add the current media item to the playlist named "ThreeList".</span></span> <span data-ttu-id="d8c6a-119">**AxWMPLib. AxWindowsMediaPlayer** 物件是以名為 player 的變數來表示。</span><span class="sxs-lookup"><span data-stu-id="d8c6a-119">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Get an interface to the current media item.
WMPLib.IWMPMedia currMedia = player.currentMedia;

// Get an interface to the playlist named "ThreeList".
WMPLib.IWMPPlaylist plThreeList = player.playlistCollection.getByName("ThreeList").Item(0);

// Append the media item to the playlist.
plThreeList.appendItem(currMedia);
```


```VB

' Get an interface to the current media item.
Dim currMedia As WMPLib.IWMPMedia = player.currentMedia

&#39; Get an interface to the playlist named &quot;ThreeList&quot;.
Dim plThreeList As WMPLib.IWMPPlaylist = player.playlistCollection.getByName(&quot;ThreeList&quot;).Item(0)

&#39; Append the media item to the playlist.
plThreeList.appendItem(currMedia)
```





## <a name="requirements"></a><span data-ttu-id="d8c6a-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="d8c6a-120">Requirements</span></span>



| <span data-ttu-id="d8c6a-121">需求</span><span class="sxs-lookup"><span data-stu-id="d8c6a-121">Requirement</span></span> | <span data-ttu-id="d8c6a-122">值</span><span class="sxs-lookup"><span data-stu-id="d8c6a-122">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d8c6a-123">版本</span><span class="sxs-lookup"><span data-stu-id="d8c6a-123">Version</span></span><br/>   | <span data-ttu-id="d8c6a-124">Windows Media Player 9 系列或更新版本</span><span class="sxs-lookup"><span data-stu-id="d8c6a-124">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="d8c6a-125">命名空間</span><span class="sxs-lookup"><span data-stu-id="d8c6a-125">Namespace</span></span><br/> | <span data-ttu-id="d8c6a-126">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="d8c6a-126">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="d8c6a-127">組件</span><span class="sxs-lookup"><span data-stu-id="d8c6a-127">Assembly</span></span><br/>  | <dl> <span data-ttu-id="d8c6a-128"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll) </dt></span><span class="sxs-lookup"><span data-stu-id="d8c6a-128"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d8c6a-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d8c6a-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d8c6a-130">**IWMPMedia 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="d8c6a-130">**IWMPMedia Interface (VB and C#)**</span></span>](iwmpmedia--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="d8c6a-131">**IWMPPlaylist 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="d8c6a-131">**IWMPPlaylist Interface (VB and C#)**</span></span>](iwmpplaylist--vb-and-c.md)
</dt> </dl>

 

 





