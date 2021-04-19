---
title: IWMPMediaCollection add 方法
description: Add 方法會將新的媒體專案或播放清單新增至程式庫。 |IWMPMediaCollection add 方法
ms.assetid: a3539646-797b-4481-a31e-86771f3633a9
keywords:
- 新增方法 Windows Media Player
- 新增方法 Windows Media Player，IWMPMediaCollection 介面
- IWMPMediaCollection 介面 Windows Media Player，add 方法
topic_type:
- apiref
api_name:
- IWMPMediaCollection.add
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7953067281e394df71a1a53c874cb80837a5f35d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106988647"
---
# <a name="iwmpmediacollectionadd-method"></a><span data-ttu-id="58324-107">IWMPMediaCollection：： add 方法</span><span class="sxs-lookup"><span data-stu-id="58324-107">IWMPMediaCollection::add method</span></span>

<span data-ttu-id="58324-108">**Add** 方法會將新的媒體專案或播放清單新增至程式庫。</span><span class="sxs-lookup"><span data-stu-id="58324-108">The **add** method adds a new media item or playlist to the library.</span></span>

## <a name="syntax"></a><span data-ttu-id="58324-109">語法</span><span class="sxs-lookup"><span data-stu-id="58324-109">Syntax</span></span>


```CSharp
public IWMPMedia add(
  System.String bstrURL
);
```


```VB

Public Function add( _
  ByVal bstrURL As System.String _
) As IWMPMedia
Implements IWMPMediaCollection.add
```





## <a name="parameters"></a><span data-ttu-id="58324-110">參數</span><span class="sxs-lookup"><span data-stu-id="58324-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="58324-111">*bstrURL* \[在\]</span><span class="sxs-lookup"><span data-stu-id="58324-111">*bstrURL* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="58324-112">指定媒體專案或播放清單位置之 URL 的 **system.string** 。</span><span class="sxs-lookup"><span data-stu-id="58324-112">A **System.String** that is the URL that specifies the location of the media item or playlist.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="58324-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="58324-113">Return value</span></span>

<span data-ttu-id="58324-114">所加入之專案或播放清單的 **WMPLib. IWMPMedia** 介面。</span><span class="sxs-lookup"><span data-stu-id="58324-114">The **WMPLib.IWMPMedia** interface for the added item or playlist.</span></span>

## <a name="remarks"></a><span data-ttu-id="58324-115">備註</span><span class="sxs-lookup"><span data-stu-id="58324-115">Remarks</span></span>

<span data-ttu-id="58324-116">這個方法會在指定路徑的情況下，將現有的媒體專案或播放清單載入至程式庫。</span><span class="sxs-lookup"><span data-stu-id="58324-116">This method loads an existing media item or playlist into the library, given a path.</span></span> <span data-ttu-id="58324-117">這個方法不會移動或變更檔案。</span><span class="sxs-lookup"><span data-stu-id="58324-117">This method does not move or change the file.</span></span> <span data-ttu-id="58324-118">如果指定了不正確本機路徑，這個方法將會失敗，但在新增至程式庫之前，不會檢查媒體專案的有效性。</span><span class="sxs-lookup"><span data-stu-id="58324-118">This method fails if given an invalid local path, but media items themselves are not checked for validity before they are added to the library.</span></span>

<span data-ttu-id="58324-119">這個方法會接受靜態和自動播放清單檔案。</span><span class="sxs-lookup"><span data-stu-id="58324-119">This method accepts both static and auto playlist files.</span></span> <span data-ttu-id="58324-120">**IWMPPlaylistCollection. importPlaylist** 方法也可以用來將靜態播放清單新增至程式庫。</span><span class="sxs-lookup"><span data-stu-id="58324-120">The **IWMPPlaylistCollection.importPlaylist** method can also be used to add a static playlist to the library.</span></span>

<span data-ttu-id="58324-121">在呼叫這個方法之前，您必須擁有程式庫的完整存取權。</span><span class="sxs-lookup"><span data-stu-id="58324-121">Before calling this method, you must have full access to the library.</span></span> <span data-ttu-id="58324-122">如需詳細資訊，請參閱連結 [庫存取](library-access.md)。</span><span class="sxs-lookup"><span data-stu-id="58324-122">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="58324-123">範例</span><span class="sxs-lookup"><span data-stu-id="58324-123">Examples</span></span>

<span data-ttu-id="58324-124">下列範例會將三個媒體物件新增至 Windows Media Player 媒體集合。</span><span class="sxs-lookup"><span data-stu-id="58324-124">The following example adds three media objects to the Windows Media Player media collection.</span></span> <span data-ttu-id="58324-125">AxWMPLib. AxWindowsMediaPlayer 物件是以名為 player 的變數來表示。</span><span class="sxs-lookup"><span data-stu-id="58324-125">The AxWMPLib.AxWindowsMediaPlayer object is represented by the variable named player.</span></span>


```CSharp
// Adding a media object using a website.
player.mediaCollection.add("https://www.proseware.com/Media/Laure.wma");

// Adding a media object from a local network.
// Either use the @ symbol to denote a quoted string literal or add additional
// backlashes as an escape for every original backslash.
player.mediaCollection.add(@"\\yourservername\Public\Jeanne.wma");

// Adding a media object from a file on a local drive.
// Either use the @ symbol to denote a quoted string literal or add additional
// backlashes as an escape for every original backslash.
player.mediaCollection.add(@"C:\WMSDK\WMPSDK\samples\media\house.wma");
```


```VB

' Adding a media object using a website.
player.mediaCollection.add(&quot;http:&#39;www.proseware.com/Media/Laure.wma&quot;)

&#39; Adding a media object from a local network.
player.mediaCollection.add(&quot;\\yourservername\Public\Jeanne.wma&quot;)

&#39; Adding a media object from a file on a local drive.
player.mediaCollection.add(&quot;C:\WMSDK\WMPSDK\samples\media\house.wma&quot;)
```





## <a name="requirements"></a><span data-ttu-id="58324-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="58324-126">Requirements</span></span>



| <span data-ttu-id="58324-127">需求</span><span class="sxs-lookup"><span data-stu-id="58324-127">Requirement</span></span> | <span data-ttu-id="58324-128">值</span><span class="sxs-lookup"><span data-stu-id="58324-128">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="58324-129">版本</span><span class="sxs-lookup"><span data-stu-id="58324-129">Version</span></span><br/>   | <span data-ttu-id="58324-130">Windows Media Player 9 系列或更新版本</span><span class="sxs-lookup"><span data-stu-id="58324-130">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="58324-131">命名空間</span><span class="sxs-lookup"><span data-stu-id="58324-131">Namespace</span></span><br/> | <span data-ttu-id="58324-132">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="58324-132">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="58324-133">組件</span><span class="sxs-lookup"><span data-stu-id="58324-133">Assembly</span></span><br/>  | <dl> <span data-ttu-id="58324-134"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll) </dt></span><span class="sxs-lookup"><span data-stu-id="58324-134"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="58324-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="58324-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="58324-136">**IWMPMediaCollection 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="58324-136">**IWMPMediaCollection Interface (VB and C#)**</span></span>](iwmpmediacollection--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="58324-137">**IWMPMediaCollection。移除 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="58324-137">**IWMPMediaCollection.remove (VB and C#)**</span></span>](wmplibiwmpmediacollection-iwmpmediacollection-remove--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="58324-138">**IWMPPlaylistCollection. importPlaylist (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="58324-138">**IWMPPlaylistCollection.importPlaylist (VB and C#)**</span></span>](wmplibiwmpplaylistcollection-iwmpplaylistcollection-importplaylist--vb-and-c.md)
</dt> </dl>

 

 





