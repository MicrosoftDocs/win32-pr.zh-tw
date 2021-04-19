---
title: IWMPMediaCollection getByAttribute 方法
description: GetByAttribute 方法會傳回 IWMPPlaylist 介面，這個介面會對應到具有指定值的指定屬性。
ms.assetid: ece70a2c-38bc-4652-8319-efcde5f9720a
keywords:
- getByAttribute 方法 Windows Media Player
- getByAttribute 方法 Windows Media Player，IWMPMediaCollection 介面
- IWMPMediaCollection 介面 Windows Media Player，getByAttribute 方法
topic_type:
- apiref
api_name:
- IWMPMediaCollection.getByAttribute
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dd7adba98fbfa450cd938b56ec6d91598b918d0d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993679"
---
# <a name="iwmpmediacollectiongetbyattribute-method"></a><span data-ttu-id="45fc5-106">IWMPMediaCollection：： getByAttribute 方法</span><span class="sxs-lookup"><span data-stu-id="45fc5-106">IWMPMediaCollection::getByAttribute method</span></span>

<span data-ttu-id="45fc5-107">**GetByAttribute** 方法會傳回 **IWMPPlaylist** 介面，這個介面會對應到具有指定值的指定屬性。</span><span class="sxs-lookup"><span data-stu-id="45fc5-107">The **getByAttribute** method returns an **IWMPPlaylist** interface that corresponds to the specified attribute having the specified value.</span></span>

## <a name="syntax"></a><span data-ttu-id="45fc5-108">語法</span><span class="sxs-lookup"><span data-stu-id="45fc5-108">Syntax</span></span>


```CSharp
public IWMPPlaylist getByAttribute(
  System.String bstrAttribute,
  System.String bstrValue
);
```


```VB

Public Function getByAttribute( _
  ByVal bstrAttribute As System.String, _
  ByVal bstrValue As System.String _
) As IWMPPlaylist
Implements IWMPMediaCollection.getByAttribute
```





## <a name="parameters"></a><span data-ttu-id="45fc5-109">參數</span><span class="sxs-lookup"><span data-stu-id="45fc5-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="45fc5-110">*bstrAttribute* \[在\]</span><span class="sxs-lookup"><span data-stu-id="45fc5-110">*bstrAttribute* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="45fc5-111">指定之屬性的 **system.string** 。</span><span class="sxs-lookup"><span data-stu-id="45fc5-111">The **System.String** that is the specified attribute.</span></span>

</dd> <dt>

<span data-ttu-id="45fc5-112">*bstrValue* \[在\]</span><span class="sxs-lookup"><span data-stu-id="45fc5-112">*bstrValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="45fc5-113">指定之值的 **system.string** 。</span><span class="sxs-lookup"><span data-stu-id="45fc5-113">The **System.String** that is the specified value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="45fc5-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="45fc5-114">Return value</span></span>

<span data-ttu-id="45fc5-115">抓取之媒體專案的 **WMPLib IWMPPlaylist** 介面。</span><span class="sxs-lookup"><span data-stu-id="45fc5-115">A **WMPLib.IWMPPlaylist** interface for the retrieved media items.</span></span>

## <a name="remarks"></a><span data-ttu-id="45fc5-116">備註</span><span class="sxs-lookup"><span data-stu-id="45fc5-116">Remarks</span></span>

<span data-ttu-id="45fc5-117">這個方法可以用來建立符合程式庫中屬性值之媒體專案的一般查詢。</span><span class="sxs-lookup"><span data-stu-id="45fc5-117">This method can be used to create a generic query for media items that match a value for an attribute in the library.</span></span> <span data-ttu-id="45fc5-118">在使用者定義的屬性中，這非常有用。</span><span class="sxs-lookup"><span data-stu-id="45fc5-118">This is useful in the case of user-defined attributes.</span></span> <span data-ttu-id="45fc5-119">如果屬性不存在，則會產生錯誤。</span><span class="sxs-lookup"><span data-stu-id="45fc5-119">If the attribute does not exist, an error will result.</span></span>

<span data-ttu-id="45fc5-120">您可以使用這個方法來取得特定類型的所有媒體專案。</span><span class="sxs-lookup"><span data-stu-id="45fc5-120">You can use this method to retrieve all of the media items of a specific type.</span></span> <span data-ttu-id="45fc5-121">使用屬性名稱 **媒體** 名稱和下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="45fc5-121">Use the attribute name **MediaType** and one of the following values.</span></span>



| <span data-ttu-id="45fc5-122">值</span><span class="sxs-lookup"><span data-stu-id="45fc5-122">Value</span></span>    | <span data-ttu-id="45fc5-123">描述</span><span class="sxs-lookup"><span data-stu-id="45fc5-123">Description</span></span>                                               |
|----------|-----------------------------------------------------------|
| <span data-ttu-id="45fc5-124">音訊</span><span class="sxs-lookup"><span data-stu-id="45fc5-124">audio</span></span>    | <span data-ttu-id="45fc5-125">音樂和其他僅限音訊的專案</span><span class="sxs-lookup"><span data-stu-id="45fc5-125">Music and other audio-only items</span></span>                          |
| <span data-ttu-id="45fc5-126">其他</span><span class="sxs-lookup"><span data-stu-id="45fc5-126">other</span></span>    | <span data-ttu-id="45fc5-127">其他專案，例如 .asf 檔案或資料流程的 URL。</span><span class="sxs-lookup"><span data-stu-id="45fc5-127">Other items, such as an .asf file or the URL of a stream.</span></span> |
| <span data-ttu-id="45fc5-128">相片</span><span class="sxs-lookup"><span data-stu-id="45fc5-128">photo</span></span>    | <span data-ttu-id="45fc5-129">相片專案。</span><span class="sxs-lookup"><span data-stu-id="45fc5-129">Photo items.</span></span> <span data-ttu-id="45fc5-130">需要 Windows Media Player 10。</span><span class="sxs-lookup"><span data-stu-id="45fc5-130">Requires Windows Media Player 10.</span></span>            |
| <span data-ttu-id="45fc5-131">播放清單</span><span class="sxs-lookup"><span data-stu-id="45fc5-131">playlist</span></span> | <span data-ttu-id="45fc5-132">以媒體專案表示的播放清單。</span><span class="sxs-lookup"><span data-stu-id="45fc5-132">Playlists represented as media items.</span></span>                     |
| <span data-ttu-id="45fc5-133">radio</span><span class="sxs-lookup"><span data-stu-id="45fc5-133">radio</span></span>    | <span data-ttu-id="45fc5-134">無線電站專案。</span><span class="sxs-lookup"><span data-stu-id="45fc5-134">Radio station items.</span></span> <span data-ttu-id="45fc5-135">Windows Media Player 10 未使用。</span><span class="sxs-lookup"><span data-stu-id="45fc5-135">Not used by Windows Media Player 10.</span></span> |
| <span data-ttu-id="45fc5-136">影片</span><span class="sxs-lookup"><span data-stu-id="45fc5-136">video</span></span>    | <span data-ttu-id="45fc5-137">影片專案。</span><span class="sxs-lookup"><span data-stu-id="45fc5-137">Video items.</span></span>                                              |



 

<span data-ttu-id="45fc5-138">在呼叫這個方法之前，您必須擁有程式庫的讀取權限。</span><span class="sxs-lookup"><span data-stu-id="45fc5-138">Before calling this method, you must have read access to the library.</span></span> <span data-ttu-id="45fc5-139">如需詳細資訊，請參閱連結 [庫存取](library-access.md)。</span><span class="sxs-lookup"><span data-stu-id="45fc5-139">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="45fc5-140">如需 Windows Media Player 所支援之屬性的詳細資訊，請參閱 [屬性參考](attribute-reference.md)。</span><span class="sxs-lookup"><span data-stu-id="45fc5-140">For information about the attributes supported by Windows Media Player, see the [Attribute Reference](attribute-reference.md).</span></span>

<span data-ttu-id="45fc5-141">您有兩種方式可以取出 **IWMPMediaCollection** 介面，而 **getByAttribute** 方法的行為取決於您所使用的兩種方式。</span><span class="sxs-lookup"><span data-stu-id="45fc5-141">There are two ways you ways you can retrieve an **IWMPMediaCollection** interface, and the behavior of the **getByAttribute** method depends on which of those two ways you use.</span></span> <span data-ttu-id="45fc5-142">如果您藉由呼叫 [AxWindowsMediaPlayer](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md)來取出介面，則 **getByAttribute** 方法會傳回媒體櫃中的所有媒體專案。</span><span class="sxs-lookup"><span data-stu-id="45fc5-142">If you retrieve the interface by calling [AxWindowsMediaPlayer.mediaCollection](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md), then the **getByAttribute** method returns all the media items in the library.</span></span> <span data-ttu-id="45fc5-143">但是，如果您藉由呼叫 [IWMPLibrary](wmplibiwmplibrary-iwmplibrary-mediacollection--vb-and-c.md)來取出介面，則 **getByAttribute** 方法只會傳回程式庫中具有指定之屬性和值的音訊專案。</span><span class="sxs-lookup"><span data-stu-id="45fc5-143">However, if you retrieve the interface by calling [IWMPLibrary.mediaCollection](wmplibiwmplibrary-iwmplibrary-mediacollection--vb-and-c.md), then the **getByAttribute** method returns only the audio items in the library that have the specified attribute and value.</span></span>

## <a name="examples"></a><span data-ttu-id="45fc5-144">範例</span><span class="sxs-lookup"><span data-stu-id="45fc5-144">Examples</span></span>

<span data-ttu-id="45fc5-145">下列程式碼範例會使用 **getByAttribute** ，以名為 Triode 48 的演出者播放媒體櫃中的所有內容。</span><span class="sxs-lookup"><span data-stu-id="45fc5-145">The following code example uses **getByAttribute** to play all content from the library by the artist named Triode 48.</span></span> <span data-ttu-id="45fc5-146">**AxWMPLib. AxWindowsMediaPlayer** 物件是以名為 player 的變數來表示。</span><span class="sxs-lookup"><span data-stu-id="45fc5-146">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Get an interface to a playlist that contains media items by a particular artist.
WMPLib.IWMPPlaylist pl = player.mediaCollection.getByAttribute("Artist", "Triode 48");

// Make the new playlist the current one.
player.currentPlaylist = pl;

// Play the media items in the current playlist. 
player.Ctlcontrols.play();
```


```VB

' Get an interface to a playlist that contains media items by a particular artist.
Dim pl As WMPLib.IWMPPlaylist = player.mediaCollection.getByAttribute(&quot;Artist&quot;, &quot;Triode 48&quot;)

&#39; Make the new playlist the current one.
player.currentPlaylist = pl

&#39; Play the media items in the current playlist. 
player.Ctlcontrols.play()
```





## <a name="requirements"></a><span data-ttu-id="45fc5-147">規格需求</span><span class="sxs-lookup"><span data-stu-id="45fc5-147">Requirements</span></span>



| <span data-ttu-id="45fc5-148">需求</span><span class="sxs-lookup"><span data-stu-id="45fc5-148">Requirement</span></span> | <span data-ttu-id="45fc5-149">值</span><span class="sxs-lookup"><span data-stu-id="45fc5-149">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="45fc5-150">版本</span><span class="sxs-lookup"><span data-stu-id="45fc5-150">Version</span></span><br/>   | <span data-ttu-id="45fc5-151">Windows Media Player 9 系列或更新版本</span><span class="sxs-lookup"><span data-stu-id="45fc5-151">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="45fc5-152">命名空間</span><span class="sxs-lookup"><span data-stu-id="45fc5-152">Namespace</span></span><br/> | <span data-ttu-id="45fc5-153">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="45fc5-153">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="45fc5-154">組件</span><span class="sxs-lookup"><span data-stu-id="45fc5-154">Assembly</span></span><br/>  | <dl> <span data-ttu-id="45fc5-155"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll) </dt></span><span class="sxs-lookup"><span data-stu-id="45fc5-155"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="45fc5-156">另請參閱</span><span class="sxs-lookup"><span data-stu-id="45fc5-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="45fc5-157">**IWMPMediaCollection 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="45fc5-157">**IWMPMediaCollection Interface (VB and C#)**</span></span>](iwmpmediacollection--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="45fc5-158">**IWMPPlaylist 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="45fc5-158">**IWMPPlaylist Interface (VB and C#)**</span></span>](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="45fc5-159">**IWMPPlaylistCollection. getAll (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="45fc5-159">**IWMPPlaylistCollection.getAll (VB and C#)**</span></span>](wmplibiwmpplaylistcollection-iwmpplaylistcollection-getall--vb-and-c.md)
</dt> </dl>

 

 





