---
title: IWMPMediaCollection getByGenre 方法
description: GetByGenre 方法會傳回 IWMPPlaylist 介面，以提供指定之內容類型的媒體專案存取權。
ms.assetid: 0681e5a2-b56d-4c33-95ce-d9ef3cd5473d
keywords:
- getByGenre 方法 Windows Media Player
- getByGenre 方法 Windows Media Player，IWMPMediaCollection 介面
- IWMPMediaCollection 介面 Windows Media Player，getByGenre 方法
topic_type:
- apiref
api_name:
- IWMPMediaCollection.getByGenre
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4eb6477a4cd212f354f5af3ab7e50fc2a87092cb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106976246"
---
# <a name="iwmpmediacollectiongetbygenre-method"></a><span data-ttu-id="ccad7-106">IWMPMediaCollection：： getByGenre 方法</span><span class="sxs-lookup"><span data-stu-id="ccad7-106">IWMPMediaCollection::getByGenre method</span></span>

<span data-ttu-id="ccad7-107">`getByGenre`方法會傳回 **IWMPPlaylist** 介面，以提供指定之內容類型的媒體專案存取權。</span><span class="sxs-lookup"><span data-stu-id="ccad7-107">The `getByGenre` method returns an **IWMPPlaylist** interface that provides access to media items of the specified genre.</span></span>

## <a name="syntax"></a><span data-ttu-id="ccad7-108">語法</span><span class="sxs-lookup"><span data-stu-id="ccad7-108">Syntax</span></span>


```CSharp
public IWMPPlaylist getByGenre(
  System.String bstrGenre
);
```


```VB

Public Function getByGenre( _
  ByVal bstrGenre As System.String _
) As IWMPPlaylist
Implements IWMPMediaCollection.getByGenre
```





## <a name="parameters"></a><span data-ttu-id="ccad7-109">參數</span><span class="sxs-lookup"><span data-stu-id="ccad7-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ccad7-110">*bstrGenre* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ccad7-110">*bstrGenre* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ccad7-111">**System.string** ，此為類型的名稱。</span><span class="sxs-lookup"><span data-stu-id="ccad7-111">The **System.String** that is the name of the genre.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ccad7-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="ccad7-112">Return value</span></span>

<span data-ttu-id="ccad7-113">抓取之媒體專案的 **WMPLib IWMPPlaylist** 介面。</span><span class="sxs-lookup"><span data-stu-id="ccad7-113">A **WMPLib.IWMPPlaylist** interface for the retrieved media items.</span></span>

## <a name="remarks"></a><span data-ttu-id="ccad7-114">備註</span><span class="sxs-lookup"><span data-stu-id="ccad7-114">Remarks</span></span>

<span data-ttu-id="ccad7-115">在呼叫這個方法之前，您必須擁有程式庫的讀取權限。</span><span class="sxs-lookup"><span data-stu-id="ccad7-115">Before calling this method, you must have read access to the library.</span></span> <span data-ttu-id="ccad7-116">如需詳細資訊，請參閱連結 [庫存取](library-access.md)。</span><span class="sxs-lookup"><span data-stu-id="ccad7-116">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="ccad7-117">您有兩種方式可以取出 **IWMPMediaCollection** 介面，而方法的行為 `getByGenre` 取決於您所使用的兩種方法。</span><span class="sxs-lookup"><span data-stu-id="ccad7-117">There are two ways you ways you can retrieve an **IWMPMediaCollection** interface, and the behavior of the `getByGenre` method depends on which of those two ways you use.</span></span> <span data-ttu-id="ccad7-118">如果您藉由呼叫 [AxWindowsMediaPlayer](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md)來取出介面，則方法會傳回 `getByGenre` 媒體櫃中的所有媒體專案。</span><span class="sxs-lookup"><span data-stu-id="ccad7-118">If you retrieve the interface by calling [AxWindowsMediaPlayer.mediaCollection](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md), then the `getByGenre` method returns all the media items in the library.</span></span> <span data-ttu-id="ccad7-119">但是，如果您藉由呼叫 [IWMPLibrary](wmplibiwmplibrary-iwmplibrary-mediacollection--vb-and-c.md)來取出介面，則方法只會傳回連結 `getByGenre` 庫中具有指定之屬性和值的音訊專案。</span><span class="sxs-lookup"><span data-stu-id="ccad7-119">However, if you retrieve the interface by calling [IWMPLibrary.mediaCollection](wmplibiwmplibrary-iwmplibrary-mediacollection--vb-and-c.md), then the `getByGenre` method returns only the audio items in the library that have the specified attribute and value.</span></span>

## <a name="examples"></a><span data-ttu-id="ccad7-120">範例</span><span class="sxs-lookup"><span data-stu-id="ccad7-120">Examples</span></span>

<span data-ttu-id="ccad7-121">下列範例會在 `getByGenre` 使用者按一下按鈕時，使用來取得媒體專案的播放清單。</span><span class="sxs-lookup"><span data-stu-id="ccad7-121">The following example uses `getByGenre` to retrieve a playlist of media items when the user clicks a button.</span></span> <span data-ttu-id="ccad7-122">播放清單中包含使用者在文字方塊中指定之類型的專案。</span><span class="sxs-lookup"><span data-stu-id="ccad7-122">The playlist contains items with the genre specified by the user in a text box.</span></span> <span data-ttu-id="ccad7-123">**AxWMPLib. AxWindowsMediaPlayer** 物件是以名為 player 的變數來表示。</span><span class="sxs-lookup"><span data-stu-id="ccad7-123">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
private void playGenre_Click(object sender, System.EventArgs e)
{ 
    // ...Add code to ensure that the text box contains a valid value.
 
    // Retrieve the genre that the user entered in the text box. 
    string genre = getGenre.Text;

    // Create the playlist using getByGenre. 
    WMPLib.IWMPPlaylist pl = player.mediaCollection.getByGenre(genre);

    // Make the new playlist the current playlist. 
    player.currentPlaylist = pl;

    // Play the media in the current playlist. 
    player.Ctlcontrols.play();
}
```


```VB

Public Sub playGenre_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles playGenre.Click

    &#39; ...Add code to ensure that the text box contains a valid value.

    &#39; Retrieve the genre that the user entered in the text box. 
    Dim genre As String = getGenre.Text

    &#39; Create the playlist using getByGenre. 
    Dim pl As WMPLib.IWMPPlaylist = player.mediaCollection.getByGenre(genre)

    &#39; Make the new playlist the current playlist. 
    player.currentPlaylist = pl

    &#39; Play the media in the current playlist. 
    player.Ctlcontrols.play()

End Sub
```





## <a name="requirements"></a><span data-ttu-id="ccad7-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="ccad7-124">Requirements</span></span>



| <span data-ttu-id="ccad7-125">需求</span><span class="sxs-lookup"><span data-stu-id="ccad7-125">Requirement</span></span> | <span data-ttu-id="ccad7-126">值</span><span class="sxs-lookup"><span data-stu-id="ccad7-126">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ccad7-127">版本</span><span class="sxs-lookup"><span data-stu-id="ccad7-127">Version</span></span><br/>   | <span data-ttu-id="ccad7-128">Windows Media Player 9 系列或更新版本</span><span class="sxs-lookup"><span data-stu-id="ccad7-128">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="ccad7-129">命名空間</span><span class="sxs-lookup"><span data-stu-id="ccad7-129">Namespace</span></span><br/> | <span data-ttu-id="ccad7-130">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="ccad7-130">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="ccad7-131">組件</span><span class="sxs-lookup"><span data-stu-id="ccad7-131">Assembly</span></span><br/>  | <dl> <span data-ttu-id="ccad7-132"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll) </dt></span><span class="sxs-lookup"><span data-stu-id="ccad7-132"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ccad7-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ccad7-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ccad7-134">**IWMPMediaCollection 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="ccad7-134">**IWMPMediaCollection Interface (VB and C#)**</span></span>](iwmpmediacollection--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="ccad7-135">**IWMPPlaylist 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="ccad7-135">**IWMPPlaylist Interface (VB and C#)**</span></span>](iwmpplaylist--vb-and-c.md)
</dt> </dl>

 

 





