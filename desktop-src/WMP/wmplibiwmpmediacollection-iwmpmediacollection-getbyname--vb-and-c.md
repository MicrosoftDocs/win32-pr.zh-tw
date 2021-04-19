---
title: IWMPMediaCollection getByName 方法
description: GetByName 方法會傳回 IWMPPlaylist 介面，以提供具有指定名稱之媒體專案的存取權。
ms.assetid: 137e938c-eb9f-4a87-8962-880e71a11ca2
keywords:
- getByName 方法 Windows Media Player
- getByName 方法 Windows Media Player，IWMPMediaCollection 介面
- IWMPMediaCollection 介面 Windows Media Player，getByName 方法
topic_type:
- apiref
api_name:
- IWMPMediaCollection.getByName
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64c68e2a5359eadf9c6212571ed948c103c01bdf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995090"
---
# <a name="iwmpmediacollectiongetbyname-method"></a><span data-ttu-id="31684-106">IWMPMediaCollection：： getByName 方法</span><span class="sxs-lookup"><span data-stu-id="31684-106">IWMPMediaCollection::getByName method</span></span>

<span data-ttu-id="31684-107">`getByName`方法會傳回 **IWMPPlaylist** 介面，以提供具有指定名稱之媒體專案的存取權。</span><span class="sxs-lookup"><span data-stu-id="31684-107">The `getByName` method returns an **IWMPPlaylist** interface that provides access to media items with the specified name.</span></span>

## <a name="syntax"></a><span data-ttu-id="31684-108">語法</span><span class="sxs-lookup"><span data-stu-id="31684-108">Syntax</span></span>


```CSharp
public IWMPPlaylist getByName(
  System.String bstrName
);
```


```VB

Public Function getByName( _
  ByVal bstrName As System.String _
) As IWMPPlaylist
Implements IWMPMediaCollection.getByName
```





## <a name="parameters"></a><span data-ttu-id="31684-109">參數</span><span class="sxs-lookup"><span data-stu-id="31684-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="31684-110">*bstrName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="31684-110">*bstrName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="31684-111">指定之名稱的 **system.string** 。</span><span class="sxs-lookup"><span data-stu-id="31684-111">The **System.String** that is the specified name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="31684-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="31684-112">Return value</span></span>

<span data-ttu-id="31684-113">抓取之媒體專案的 **WMPLib IWMPPlaylist** 介面。</span><span class="sxs-lookup"><span data-stu-id="31684-113">A **WMPLib.IWMPPlaylist** interface for the retrieved media items.</span></span>

## <a name="remarks"></a><span data-ttu-id="31684-114">備註</span><span class="sxs-lookup"><span data-stu-id="31684-114">Remarks</span></span>

<span data-ttu-id="31684-115">在呼叫這個方法之前，您必須擁有程式庫的讀取權限。</span><span class="sxs-lookup"><span data-stu-id="31684-115">Before calling this method, you must have read access to the library.</span></span> <span data-ttu-id="31684-116">如需詳細資訊，請參閱連結 [庫存取](library-access.md)。</span><span class="sxs-lookup"><span data-stu-id="31684-116">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="31684-117">您有兩種方式可以取出 **IWMPMediaCollection** 介面，而方法的行為 `getByName` 取決於您所使用的兩種方法。</span><span class="sxs-lookup"><span data-stu-id="31684-117">There are two ways you ways you can retrieve an **IWMPMediaCollection** interface, and the behavior of the `getByName` method depends on which of those two ways you use.</span></span> <span data-ttu-id="31684-118">如果您藉由呼叫 [AxWindowsMediaPlayer](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md)來取出介面，則方法會傳回 `getByName` 媒體櫃中的所有媒體專案。</span><span class="sxs-lookup"><span data-stu-id="31684-118">If you retrieve the interface by calling [AxWindowsMediaPlayer.mediaCollection](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md), then the `getByName` method returns all the media items in the library.</span></span> <span data-ttu-id="31684-119">但是，如果您藉由呼叫 [IWMPLibrary](wmplibiwmplibrary-iwmplibrary-mediacollection--vb-and-c.md)來取出介面，則方法只會傳回連結 `getByName` 庫中具有指定之屬性和值的音訊專案。</span><span class="sxs-lookup"><span data-stu-id="31684-119">However, if you retrieve the interface by calling [IWMPLibrary.mediaCollection](wmplibiwmplibrary-iwmplibrary-mediacollection--vb-and-c.md), then the `getByName` method returns only the audio items in the library that have the specified attribute and value.</span></span>

## <a name="examples"></a><span data-ttu-id="31684-120">範例</span><span class="sxs-lookup"><span data-stu-id="31684-120">Examples</span></span>

<span data-ttu-id="31684-121">下列範例會使用 `getByName` 從程式庫取出三個專案。</span><span class="sxs-lookup"><span data-stu-id="31684-121">The following example uses `getByName` to retrieve three items from the library.</span></span> <span data-ttu-id="31684-122">接著會將每個專案附加至目前的播放清單。</span><span class="sxs-lookup"><span data-stu-id="31684-122">Each item is then appended to the current playlist.</span></span> <span data-ttu-id="31684-123">**AxWMPLib. AxWindowsMediaPlayer** 物件是以名為 player 的變數來表示。</span><span class="sxs-lookup"><span data-stu-id="31684-123">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// In each case, use the name exactly as it appears in the library.
// Windows Media Player does not include file name extensions or file paths
// in the name. Internet URLs include the entire path, but not the 
// file name extension.

// Get an interface to a playlist that contains an Internet URL.
WMPLib.IWMPPlaylist one = player.mediaCollection.getByName("https://www.proseware.com/Media/Laure");

// Get an interface to a playlist that contains a file on a network server.
WMPLib.IWMPPlaylist two = player.mediaCollection.getByName("Jeanne");

// Get an interface to a playlist that contains a file on a local drive.
WMPLib.IWMPPlaylist three = player.mediaCollection.getByName("house");

// Append each item to the current playlist. Since each playlist retrieved
// using getByName contains one digital media item, use the get_Item
// method with an index of zero to reference that item.
player.currentPlaylist.appendItem(one.get_Item(0));
player.currentPlaylist.appendItem(two.get_Item(0));
player.currentPlaylist.appendItem(three.get_Item(0));
```


```VB

' In each case, use the name exactly as it appears in the library.
&#39; Windows Media Player does not include file name extensions or file paths
&#39; in the name. Internet URLs include the entire path, but not the 
&#39; file name extension.

&#39; Get an interface to a playlist that contains an Internet URL.
Dim one As WMPLib.IWMPPlaylist = player.mediaCollection.getByName(&quot;https://www.proseware.com/Media/Laure&quot;)

&#39; Get an interface to a playlist that contains a file on a network server.
Dim two As WMPLib.IWMPPlaylist = player.mediaCollection.getByName(&quot;Jeanne&quot;)

&#39; Get an interface to a playlist that contains a file on a local drive.
Dim three As WMPLib.IWMPPlaylist = player.mediaCollection.getByName(&quot;house&quot;)

&#39; Append each item to the current playlist. Since each playlist retrieved
&#39; using getByName contains one digital media item, use the Item
&#39; property with an index of zero to reference that item.
player.currentPlaylist.appendItem(one.Item(0))
player.currentPlaylist.appendItem(two.Item(0))
player.currentPlaylist.appendItem(three.Item(0))
```





## <a name="requirements"></a><span data-ttu-id="31684-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="31684-124">Requirements</span></span>



| <span data-ttu-id="31684-125">需求</span><span class="sxs-lookup"><span data-stu-id="31684-125">Requirement</span></span> | <span data-ttu-id="31684-126">值</span><span class="sxs-lookup"><span data-stu-id="31684-126">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="31684-127">版本</span><span class="sxs-lookup"><span data-stu-id="31684-127">Version</span></span><br/>   | <span data-ttu-id="31684-128">Windows Media Player 9 系列或更新版本</span><span class="sxs-lookup"><span data-stu-id="31684-128">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="31684-129">命名空間</span><span class="sxs-lookup"><span data-stu-id="31684-129">Namespace</span></span><br/> | <span data-ttu-id="31684-130">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="31684-130">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="31684-131">組件</span><span class="sxs-lookup"><span data-stu-id="31684-131">Assembly</span></span><br/>  | <dl> <span data-ttu-id="31684-132"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll) </dt></span><span class="sxs-lookup"><span data-stu-id="31684-132"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="31684-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="31684-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="31684-134">**IWMPMediaCollection 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="31684-134">**IWMPMediaCollection Interface (VB and C#)**</span></span>](iwmpmediacollection--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="31684-135">**IWMPPlaylist 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="31684-135">**IWMPPlaylist Interface (VB and C#)**</span></span>](iwmpplaylist--vb-and-c.md)
</dt> </dl>

 

 





