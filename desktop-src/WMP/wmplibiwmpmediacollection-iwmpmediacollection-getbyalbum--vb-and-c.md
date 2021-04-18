---
title: IWMPMediaCollection getByAlbum 方法
description: GetByAlbum 方法會傳回 IWMPPlaylist 介面，此介面可讓您從指定的專輯存取媒體專案。
ms.assetid: 26f004c0-de46-4792-8212-9d4ac749bb21
keywords:
- getByAlbum 方法 Windows Media Player
- getByAlbum 方法 Windows Media Player，IWMPMediaCollection 介面
- IWMPMediaCollection 介面 Windows Media Player，getByAlbum 方法
topic_type:
- apiref
api_name:
- IWMPMediaCollection.getByAlbum
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c455e9bd61038a4d72bb6537d7c62b30a5d0b733
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106996321"
---
# <a name="iwmpmediacollectiongetbyalbum-method"></a><span data-ttu-id="b87ed-106">IWMPMediaCollection：： getByAlbum 方法</span><span class="sxs-lookup"><span data-stu-id="b87ed-106">IWMPMediaCollection::getByAlbum method</span></span>

<span data-ttu-id="b87ed-107">**GetByAlbum** 方法會傳回 **IWMPPlaylist** 介面，此介面可讓您從指定的專輯存取媒體專案。</span><span class="sxs-lookup"><span data-stu-id="b87ed-107">The **getByAlbum** method returns an **IWMPPlaylist** interface that provides access to media items from the specified album.</span></span>

## <a name="syntax"></a><span data-ttu-id="b87ed-108">語法</span><span class="sxs-lookup"><span data-stu-id="b87ed-108">Syntax</span></span>


```CSharp
public IWMPPlaylist getByAlbum(
  System.String bstrAlbum
);
```


```VB

Public Function getByAlbum( _
  ByVal bstrAlbum As System.String _
) As IWMPPlaylist
Implements IWMPMediaCollection.getByAlbum
```





## <a name="parameters"></a><span data-ttu-id="b87ed-109">參數</span><span class="sxs-lookup"><span data-stu-id="b87ed-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b87ed-110">*bstrAlbum* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b87ed-110">*bstrAlbum* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b87ed-111">表示專輯標題的 **system.string** 。</span><span class="sxs-lookup"><span data-stu-id="b87ed-111">The **System.String** that is the title of the album.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b87ed-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="b87ed-112">Return value</span></span>

<span data-ttu-id="b87ed-113">抓取之媒體專案的 **WMPLib IWMPPlaylist** 介面。</span><span class="sxs-lookup"><span data-stu-id="b87ed-113">A **WMPLib.IWMPPlaylist** interface for the retrieved media items.</span></span>

## <a name="remarks"></a><span data-ttu-id="b87ed-114">備註</span><span class="sxs-lookup"><span data-stu-id="b87ed-114">Remarks</span></span>

<span data-ttu-id="b87ed-115">在呼叫這個方法之前，您必須擁有程式庫的讀取權限。</span><span class="sxs-lookup"><span data-stu-id="b87ed-115">Before calling this method, you must have read access to the library.</span></span> <span data-ttu-id="b87ed-116">如需詳細資訊，請參閱連結 [庫存取](library-access.md)。</span><span class="sxs-lookup"><span data-stu-id="b87ed-116">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="b87ed-117">您有兩種方式可以取出 **IWMPMediaCollection** 介面，而 **getByAlbum** 方法的行為取決於您所使用的兩種方式。</span><span class="sxs-lookup"><span data-stu-id="b87ed-117">There are two ways you ways you can retrieve an **IWMPMediaCollection** interface, and the behavior of the **getByAlbum** method depends on which of those two ways you use.</span></span> <span data-ttu-id="b87ed-118">如果您藉由呼叫 [AxWindowsMediaPlayer](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md)來取出介面，則 **getByAlbum** 方法會傳回媒體櫃中的所有媒體專案。</span><span class="sxs-lookup"><span data-stu-id="b87ed-118">If you retrieve the interface by calling [AxWindowsMediaPlayer.mediaCollection](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md), then the **getByAlbum** method returns all the media items in the library.</span></span> <span data-ttu-id="b87ed-119">但是，如果您藉由呼叫 [IWMPLibrary](wmplibiwmplibrary-iwmplibrary-mediacollection--vb-and-c.md)來取出介面，則 **getByAlbum** 方法只會傳回程式庫中屬於指定之專輯的音訊專案。</span><span class="sxs-lookup"><span data-stu-id="b87ed-119">However, if you retrieve the interface by calling [IWMPLibrary.mediaCollection](wmplibiwmplibrary-iwmplibrary-mediacollection--vb-and-c.md), then the **getByAlbum** method returns only the audio items in the library that belong to the specified album.</span></span>

## <a name="examples"></a><span data-ttu-id="b87ed-120">範例</span><span class="sxs-lookup"><span data-stu-id="b87ed-120">Examples</span></span>

<span data-ttu-id="b87ed-121">下列範例會使用 **getByAlbum** ，在使用者按一下按鈕時，建立媒體專案的播放清單。</span><span class="sxs-lookup"><span data-stu-id="b87ed-121">The following example uses **getByAlbum** to create a playlist of media items when the user clicks a button.</span></span> <span data-ttu-id="b87ed-122">播放清單中包含使用者在文字方塊中指定之專輯的專案。</span><span class="sxs-lookup"><span data-stu-id="b87ed-122">The playlist contains items with the album specified by the user in a text box.</span></span> <span data-ttu-id="b87ed-123">**AxWMPLib. AxWindowsMediaPlayer** 物件是以名為 player 的變數來表示。</span><span class="sxs-lookup"><span data-stu-id="b87ed-123">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
private void playAlbum_Click(object sender, System.EventArgs e)
{ 
    // ...Add code to ensure that the text box contains a valid value.
 
    // Retrieve the album title text that the user entered in the text box. 
    string album = getAlbum.Text;

    // Create the playlist using getByAlbum. 
    WMPLib.IWMPPlaylist pl = player.mediaCollection.getByAlbum(album);

    // Make the new playlist the current playlist. 
    player.currentPlaylist = pl;

    // Play the media in the current playlist. 
    player.Ctlcontrols.play();
}
```


```VB

Public Sub playAlbum_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles playAlbum.Click

    &#39; ...Add code to ensure that the text box contains a valid value.

    &#39; Retrieve the album title text that the user entered in the text box. 
    Dim album As String = getAlbum.Text

    &#39; Create the playlist using getByAlbum. 
    Dim pl As WMPLib.IWMPPlaylist = player.mediaCollection.getByAlbum(album)

    &#39; Make the new playlist the current playlist. 
    player.currentPlaylist = pl

    &#39; Play the media in the current playlist. 
    player.Ctlcontrols.play()

End Sub
```





## <a name="requirements"></a><span data-ttu-id="b87ed-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="b87ed-124">Requirements</span></span>



| <span data-ttu-id="b87ed-125">需求</span><span class="sxs-lookup"><span data-stu-id="b87ed-125">Requirement</span></span> | <span data-ttu-id="b87ed-126">值</span><span class="sxs-lookup"><span data-stu-id="b87ed-126">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b87ed-127">版本</span><span class="sxs-lookup"><span data-stu-id="b87ed-127">Version</span></span><br/>   | <span data-ttu-id="b87ed-128">Windows Media Player 9 系列或更新版本</span><span class="sxs-lookup"><span data-stu-id="b87ed-128">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="b87ed-129">命名空間</span><span class="sxs-lookup"><span data-stu-id="b87ed-129">Namespace</span></span><br/> | <span data-ttu-id="b87ed-130">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="b87ed-130">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="b87ed-131">組件</span><span class="sxs-lookup"><span data-stu-id="b87ed-131">Assembly</span></span><br/>  | <dl> <span data-ttu-id="b87ed-132"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll) </dt></span><span class="sxs-lookup"><span data-stu-id="b87ed-132"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b87ed-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b87ed-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b87ed-134">**IWMPMediaCollection 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="b87ed-134">**IWMPMediaCollection Interface (VB and C#)**</span></span>](iwmpmediacollection--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="b87ed-135">**IWMPPlaylist 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="b87ed-135">**IWMPPlaylist Interface (VB and C#)**</span></span>](iwmpplaylist--vb-and-c.md)
</dt> </dl>

 

 





