---
title: IWMPMediaCollection getAll 方法
description: GetAll 方法會傳回 IWMPPlaylist 介面，該介面對應至包含媒體櫃中所有媒體專案的播放清單。
ms.assetid: f2bbb4a4-7397-4c97-afd9-e8ee380af9da
keywords:
- getAll 方法 Windows Media Player
- getAll 方法 Windows Media Player，IWMPMediaCollection 介面
- IWMPMediaCollection 介面 Windows Media Player，getAll 方法
topic_type:
- apiref
api_name:
- IWMPMediaCollection.getAll
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be08548ae29db12ded788f34563ef5e319c27d61
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106989250"
---
# <a name="iwmpmediacollectiongetall-method"></a><span data-ttu-id="95929-106">IWMPMediaCollection：： getAll 方法</span><span class="sxs-lookup"><span data-stu-id="95929-106">IWMPMediaCollection::getAll method</span></span>

<span data-ttu-id="95929-107">**GetAll** 方法會傳回 **IWMPPlaylist** 介面，該介面對應至包含媒體櫃中所有媒體專案的播放清單。</span><span class="sxs-lookup"><span data-stu-id="95929-107">The **getAll** method returns an **IWMPPlaylist** interface that corresponds to the playlist that contains all media items in the library.</span></span>

## <a name="syntax"></a><span data-ttu-id="95929-108">語法</span><span class="sxs-lookup"><span data-stu-id="95929-108">Syntax</span></span>


```CSharp
public IWMPPlaylist getAll();
```


```VB

Public Function getAll() As IWMPPlaylist
Implements IWMPMediaCollection.getAll
```





## <a name="parameters"></a><span data-ttu-id="95929-109">參數</span><span class="sxs-lookup"><span data-stu-id="95929-109">Parameters</span></span>

<span data-ttu-id="95929-110">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="95929-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="95929-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="95929-111">Return value</span></span>

<span data-ttu-id="95929-112">播放清單的 **WMPLib IWMPPlaylist** 介面，其中包含所有要求的媒體專案。</span><span class="sxs-lookup"><span data-stu-id="95929-112">The **WMPLib.IWMPPlaylist** interface for the playlist that contains all of the requested media items.</span></span>

## <a name="remarks"></a><span data-ttu-id="95929-113">備註</span><span class="sxs-lookup"><span data-stu-id="95929-113">Remarks</span></span>

<span data-ttu-id="95929-114">在呼叫這個方法之前，您必須擁有程式庫的讀取權限。</span><span class="sxs-lookup"><span data-stu-id="95929-114">Before calling this method, you must have read access to the library.</span></span> <span data-ttu-id="95929-115">如需詳細資訊，請參閱連結 [庫存取](library-access.md)。</span><span class="sxs-lookup"><span data-stu-id="95929-115">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="95929-116">您有兩種方式可以取出 **IWMPMediaCollection** 介面，而 **getAll** 方法的行為取決於您所使用的兩種方式。</span><span class="sxs-lookup"><span data-stu-id="95929-116">There are two ways you ways you can retrieve an **IWMPMediaCollection** interface, and the behavior of the **getAll** method depends on which of those two ways you use.</span></span> <span data-ttu-id="95929-117">如果您藉由呼叫 [AxWindowsMediaPlayer](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md)來取出介面，則 **getAll** 方法會傳回媒體櫃中的所有媒體專案。</span><span class="sxs-lookup"><span data-stu-id="95929-117">If you retrieve the interface by calling [AxWindowsMediaPlayer.mediaCollection](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md), then the **getAll** method returns all the media items in the library.</span></span> <span data-ttu-id="95929-118">但是，如果您藉由呼叫 [IWMPLibrary](wmplibiwmplibrary-iwmplibrary-mediacollection--vb-and-c.md)來取出介面，則 **getAll** 方法只會傳回媒體櫃中的音訊專案。</span><span class="sxs-lookup"><span data-stu-id="95929-118">However, if you retrieve the interface by calling [IWMPLibrary.mediaCollection](wmplibiwmplibrary-iwmplibrary-mediacollection--vb-and-c.md), then the **getAll** method returns only the audio items in the library.</span></span>

## <a name="examples"></a><span data-ttu-id="95929-119">範例</span><span class="sxs-lookup"><span data-stu-id="95929-119">Examples</span></span>

<span data-ttu-id="95929-120">下列範例會使用 **getAll** ，從媒體集合隨機播放媒體專案。</span><span class="sxs-lookup"><span data-stu-id="95929-120">The following example uses **getAll** to play media items randomly from the media collection.</span></span> <span data-ttu-id="95929-121">**AxWMPLib. AxWindowsMediaPlayer** 物件是以名為 player 的變數來表示。</span><span class="sxs-lookup"><span data-stu-id="95929-121">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Create a random number generator. 
System.Random randGenerator = new System.Random();

// Store the count of all media items in the media collection.
int count = player.mediaCollection.getAll().count;

// Get a random integer using the count as the max value.
int rand = randGenerator.Next(count);

// Make the random media item the current media item.
player.currentMedia = player.mediaCollection.getAll().get_Item(rand);

// Play the media item.
player.Ctlcontrols.play();
```


```VB

' Create a random number generator. 
Dim randGenerator As System.Random = New System.Random()

&#39; Store the count of all media items in the media collection.
Dim count As Integer = player.mediaCollection.getAll().count

&#39; Get a random integer using the count as the max value.
Dim rand As Integer = randGenerator.Next(count)

&#39; Make the random media item the current media item.
player.currentMedia = player.mediaCollection.getAll().Item(rand)

&#39; Play the media item.
player.Ctlcontrols.play()
```





## <a name="requirements"></a><span data-ttu-id="95929-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="95929-122">Requirements</span></span>



| <span data-ttu-id="95929-123">需求</span><span class="sxs-lookup"><span data-stu-id="95929-123">Requirement</span></span> | <span data-ttu-id="95929-124">值</span><span class="sxs-lookup"><span data-stu-id="95929-124">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="95929-125">版本</span><span class="sxs-lookup"><span data-stu-id="95929-125">Version</span></span><br/>   | <span data-ttu-id="95929-126">Windows Media Player 9 系列或更新版本</span><span class="sxs-lookup"><span data-stu-id="95929-126">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="95929-127">命名空間</span><span class="sxs-lookup"><span data-stu-id="95929-127">Namespace</span></span><br/> | <span data-ttu-id="95929-128">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="95929-128">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="95929-129">組件</span><span class="sxs-lookup"><span data-stu-id="95929-129">Assembly</span></span><br/>  | <dl> <span data-ttu-id="95929-130"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll) </dt></span><span class="sxs-lookup"><span data-stu-id="95929-130"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="95929-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="95929-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="95929-132">**IWMPMediaCollection 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="95929-132">**IWMPMediaCollection Interface (VB and C#)**</span></span>](iwmpmediacollection--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="95929-133">**IWMPPlaylist 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="95929-133">**IWMPPlaylist Interface (VB and C#)**</span></span>](iwmpplaylist--vb-and-c.md)
</dt> </dl>

 

 





