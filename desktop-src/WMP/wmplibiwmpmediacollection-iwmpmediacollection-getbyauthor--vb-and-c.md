---
title: IWMPMediaCollection getByAuthor 方法
description: GetByAuthor 方法會傳回 IWMPPlaylist 介面，以提供指定作者存取媒體專案的許可權。
ms.assetid: eb3793f6-bad1-4c80-991e-c6d0093ae57f
keywords:
- getByAuthor 方法 Windows Media Player
- getByAuthor 方法 Windows Media Player，IWMPMediaCollection 介面
- IWMPMediaCollection 介面 Windows Media Player，getByAuthor 方法
topic_type:
- apiref
api_name:
- IWMPMediaCollection.getByAuthor
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e594de010a65c15088e2a31a3ccbac2ac5a1fc6e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999738"
---
# <a name="iwmpmediacollectiongetbyauthor-method"></a><span data-ttu-id="c7eca-106">IWMPMediaCollection：： getByAuthor 方法</span><span class="sxs-lookup"><span data-stu-id="c7eca-106">IWMPMediaCollection::getByAuthor method</span></span>

<span data-ttu-id="c7eca-107">`getByAuthor`方法會傳回 **IWMPPlaylist** 介面，以提供指定作者存取媒體專案的許可權。</span><span class="sxs-lookup"><span data-stu-id="c7eca-107">The `getByAuthor` method returns an **IWMPPlaylist** interface that provides access to the media items by the specified author.</span></span>

## <a name="syntax"></a><span data-ttu-id="c7eca-108">語法</span><span class="sxs-lookup"><span data-stu-id="c7eca-108">Syntax</span></span>


```CSharp
public IWMPPlaylist getByAuthor(
  System.String bstrAuthor
);
```


```VB

Public Function getByAuthor( _
  ByVal bstrAuthor As System.String _
) As IWMPPlaylist
Implements IWMPMediaCollection.getByAuthor
```





## <a name="parameters"></a><span data-ttu-id="c7eca-109">參數</span><span class="sxs-lookup"><span data-stu-id="c7eca-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c7eca-110">*bstrAuthor* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c7eca-110">*bstrAuthor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c7eca-111">**System.string** ，也就是作者的名稱。</span><span class="sxs-lookup"><span data-stu-id="c7eca-111">The **System.String** that is the name of the author.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c7eca-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="c7eca-112">Return value</span></span>

<span data-ttu-id="c7eca-113">抓取之媒體專案的 **WMPLib IWMPPlaylist** 介面。</span><span class="sxs-lookup"><span data-stu-id="c7eca-113">A **WMPLib.IWMPPlaylist** interface for the retrieved media items.</span></span>

## <a name="remarks"></a><span data-ttu-id="c7eca-114">備註</span><span class="sxs-lookup"><span data-stu-id="c7eca-114">Remarks</span></span>

<span data-ttu-id="c7eca-115">在呼叫這個方法之前，您必須擁有程式庫的讀取權限。</span><span class="sxs-lookup"><span data-stu-id="c7eca-115">Before calling this method, you must have read access to the library.</span></span> <span data-ttu-id="c7eca-116">如需詳細資訊，請參閱連結 [庫存取](library-access.md)。</span><span class="sxs-lookup"><span data-stu-id="c7eca-116">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="c7eca-117">您有兩種方式可以取出 **IWMPMediaCollection** 介面，而方法的行為 `getByAuthor` 取決於您所使用的兩種方法。</span><span class="sxs-lookup"><span data-stu-id="c7eca-117">There are two ways you ways you can retrieve an **IWMPMediaCollection** interface, and the behavior of the `getByAuthor` method depends on which of those two ways you use.</span></span> <span data-ttu-id="c7eca-118">如果您藉由呼叫 [AxWindowsMediaPlayer](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md)來取出介面，則方法會傳回 `getByAuthor` 媒體櫃中的所有媒體專案。</span><span class="sxs-lookup"><span data-stu-id="c7eca-118">If you retrieve the interface by calling [AxWindowsMediaPlayer.mediaCollection](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md), then the `getByAuthor` method returns all the media items in the library.</span></span> <span data-ttu-id="c7eca-119">但是，如果您藉由呼叫 [IWMPLibrary](wmplibiwmplibrary-iwmplibrary-mediacollection--vb-and-c.md)來取出介面，則方法只會傳回連結 `getByAuthor` 庫中具有指定之屬性和值的音訊專案。</span><span class="sxs-lookup"><span data-stu-id="c7eca-119">However, if you retrieve the interface by calling [IWMPLibrary.mediaCollection](wmplibiwmplibrary-iwmplibrary-mediacollection--vb-and-c.md), then the `getByAuthor` method returns only the audio items in the library that have the specified attribute and value.</span></span>

## <a name="examples"></a><span data-ttu-id="c7eca-120">範例</span><span class="sxs-lookup"><span data-stu-id="c7eca-120">Examples</span></span>

<span data-ttu-id="c7eca-121">下列範例會在 `getByAuthor` 使用者按一下按鈕時，使用來建立媒體專案的播放清單。</span><span class="sxs-lookup"><span data-stu-id="c7eca-121">The following example uses `getByAuthor` to create a playlist of media items when the user clicks a button.</span></span> <span data-ttu-id="c7eca-122">播放清單包含符合使用者在文字方塊中指定之作者名稱的專案。</span><span class="sxs-lookup"><span data-stu-id="c7eca-122">The playlist contains items matching the author's name specified by the user in a text box.</span></span> <span data-ttu-id="c7eca-123">**AxWMPLib. AxWindowsMediaPlayer** 物件是以名為 player 的變數來表示。</span><span class="sxs-lookup"><span data-stu-id="c7eca-123">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
private void playAuthor_Click(object sender, System.EventArgs e)
{ 
    // ...Add code to ensure that the text box contains a valid value.
 
    // Retrieve the author's name from the text box. 
    string author = getAuthor.Text;

    // Create the playlist using getByAuthor. 
    WMPLib.IWMPPlaylist pl = player.mediaCollection.getByAuthor(author);

    // Make the new playlist the current playlist. 
    player.currentPlaylist = pl;

    // Play the media in the current playlist. 
    player.Ctlcontrols.play();
}
```


```VB

Public Sub playAuthor_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles playAuthor.Click

    &#39; ...Add code to ensure that the text box contains a valid value.

    &#39; Retrieve the author&#39;s name from the text box. 
    Dim author As String = getAuthor.Text

    &#39; Create the playlist using getByAuthor. 
    Dim pl As WMPLib.IWMPPlaylist = player.mediaCollection.getByAuthor(author)

    &#39; Make the new playlist the current playlist. 
    player.currentPlaylist = pl

    &#39; Play the media in the current playlist. 
    player.Ctlcontrols.play()

End Sub
```





## <a name="requirements"></a><span data-ttu-id="c7eca-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="c7eca-124">Requirements</span></span>



| <span data-ttu-id="c7eca-125">需求</span><span class="sxs-lookup"><span data-stu-id="c7eca-125">Requirement</span></span> | <span data-ttu-id="c7eca-126">值</span><span class="sxs-lookup"><span data-stu-id="c7eca-126">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c7eca-127">版本</span><span class="sxs-lookup"><span data-stu-id="c7eca-127">Version</span></span><br/>   | <span data-ttu-id="c7eca-128">Windows Media Player 9 系列或更新版本</span><span class="sxs-lookup"><span data-stu-id="c7eca-128">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="c7eca-129">命名空間</span><span class="sxs-lookup"><span data-stu-id="c7eca-129">Namespace</span></span><br/> | <span data-ttu-id="c7eca-130">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="c7eca-130">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="c7eca-131">組件</span><span class="sxs-lookup"><span data-stu-id="c7eca-131">Assembly</span></span><br/>  | <dl> <span data-ttu-id="c7eca-132"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll) </dt></span><span class="sxs-lookup"><span data-stu-id="c7eca-132"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c7eca-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c7eca-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c7eca-134">**IWMPMediaCollection 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="c7eca-134">**IWMPMediaCollection Interface (VB and C#)**</span></span>](iwmpmediacollection--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="c7eca-135">**IWMPPlaylist 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="c7eca-135">**IWMPPlaylist Interface (VB and C#)**</span></span>](iwmpplaylist--vb-and-c.md)
</dt> </dl>

 

 





