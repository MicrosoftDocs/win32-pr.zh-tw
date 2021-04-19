---
title: IWMPPlaylist removeItem 方法
description: RemoveItem 方法會從播放清單中移除指定的媒體專案。
ms.assetid: 8b5a4c34-863d-4963-97c8-cc5aa2223ab5
keywords:
- removeItem 方法 Windows Media Player
- removeItem 方法 Windows Media Player，IWMPPlaylist 介面
- IWMPPlaylist 介面 Windows Media Player，removeItem 方法
topic_type:
- apiref
api_name:
- IWMPPlaylist.removeItem
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec845b7657e04f17c47119dd169032ebe5815786
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106997678"
---
# <a name="iwmpplaylistremoveitem-method"></a><span data-ttu-id="8bd17-106">IWMPPlaylist：： removeItem 方法</span><span class="sxs-lookup"><span data-stu-id="8bd17-106">IWMPPlaylist::removeItem method</span></span>

<span data-ttu-id="8bd17-107">**RemoveItem** 方法會從播放清單中移除指定的媒體專案。</span><span class="sxs-lookup"><span data-stu-id="8bd17-107">The **removeItem** method removes the specified media item from the playlist.</span></span>

## <a name="syntax"></a><span data-ttu-id="8bd17-108">語法</span><span class="sxs-lookup"><span data-stu-id="8bd17-108">Syntax</span></span>


```CSharp
public void removeItem(
  IWMPMedia pIWMPMedia
);
```


```VB

Public Sub removeItem( _
  ByVal pIWMPMedia As IWMPMedia _
)
Implements IWMPPlaylist.removeItem
```





## <a name="parameters"></a><span data-ttu-id="8bd17-109">參數</span><span class="sxs-lookup"><span data-stu-id="8bd17-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8bd17-110">*pIWMPMedia* \[在\]</span><span class="sxs-lookup"><span data-stu-id="8bd17-110">*pIWMPMedia* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8bd17-111">代表要從播放清單中移除之媒體專案的 **WMPLib IWMPMedia** 介面。</span><span class="sxs-lookup"><span data-stu-id="8bd17-111">A **WMPLib.IWMPMedia** interface that represents the media item to remove from the playlist.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8bd17-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="8bd17-112">Return value</span></span>

<span data-ttu-id="8bd17-113">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="8bd17-113">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="8bd17-114">備註</span><span class="sxs-lookup"><span data-stu-id="8bd17-114">Remarks</span></span>

<span data-ttu-id="8bd17-115">如果移除的專案是目前播放的播放軌，播放會停止，且播放清單中的下一個專案會變成目前的播放軌。</span><span class="sxs-lookup"><span data-stu-id="8bd17-115">If the item removed is the currently playing track, playback stops and the next item in the playlist becomes the current one.</span></span>

<span data-ttu-id="8bd17-116">如果沒有下一個專案，則會使用前一個專案。</span><span class="sxs-lookup"><span data-stu-id="8bd17-116">If there is no next item, the previous item is used.</span></span> <span data-ttu-id="8bd17-117">如果沒有其他專案，則 **AxWindowsMediaPlayer. currentMedia** 屬性會傳回 **Null**。</span><span class="sxs-lookup"><span data-stu-id="8bd17-117">If there are no other items, then the **AxWindowsMediaPlayer.currentMedia** property will return **NULL**.</span></span>

<span data-ttu-id="8bd17-118">在呼叫這個方法之前，您必須擁有程式庫的完整存取權。</span><span class="sxs-lookup"><span data-stu-id="8bd17-118">Before calling this method, you must have full access to the library.</span></span> <span data-ttu-id="8bd17-119">如需詳細資訊，請參閱連結 [庫存取](library-access.md)。</span><span class="sxs-lookup"><span data-stu-id="8bd17-119">For more information, see [Library Access](library-access.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="8bd17-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="8bd17-120">Requirements</span></span>



| <span data-ttu-id="8bd17-121">需求</span><span class="sxs-lookup"><span data-stu-id="8bd17-121">Requirement</span></span> | <span data-ttu-id="8bd17-122">值</span><span class="sxs-lookup"><span data-stu-id="8bd17-122">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8bd17-123">版本</span><span class="sxs-lookup"><span data-stu-id="8bd17-123">Version</span></span><br/>   | <span data-ttu-id="8bd17-124">Windows Media Player 9 系列或更新版本</span><span class="sxs-lookup"><span data-stu-id="8bd17-124">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="8bd17-125">命名空間</span><span class="sxs-lookup"><span data-stu-id="8bd17-125">Namespace</span></span><br/> | <span data-ttu-id="8bd17-126">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="8bd17-126">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="8bd17-127">組件</span><span class="sxs-lookup"><span data-stu-id="8bd17-127">Assembly</span></span><br/>  | <dl> <span data-ttu-id="8bd17-128"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll) </dt></span><span class="sxs-lookup"><span data-stu-id="8bd17-128"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8bd17-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8bd17-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8bd17-130">**AxWindowsMediaPlayer. currentMedia (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="8bd17-130">**AxWindowsMediaPlayer.currentMedia (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-currentmedia--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="8bd17-131">**IWMPMedia 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="8bd17-131">**IWMPMedia Interface (VB and C#)**</span></span>](iwmpmedia--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="8bd17-132">**IWMPPlaylist 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="8bd17-132">**IWMPPlaylist Interface (VB and C#)**</span></span>](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="8bd17-133">**IWMPPlaylist. insertItem (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="8bd17-133">**IWMPPlaylist.insertItem (VB and C#)**</span></span>](wmplibiwmpplaylist-iwmpplaylist-insertitem--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="8bd17-134">**IWMPPlaylist (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="8bd17-134">**IWMPPlaylist.Item (VB and C#)**</span></span>](iwmpplaylist-item--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="8bd17-135">**IWMPSettings2. mediaAccessRights (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="8bd17-135">**IWMPSettings2.mediaAccessRights (VB and C#)**</span></span>](wmplibiwmpsettings2-iwmpsettings2-mediaaccessrights--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="8bd17-136">**IWMPSettings2. requestMediaAccessRights (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="8bd17-136">**IWMPSettings2.requestMediaAccessRights (VB and C#)**</span></span>](wmplibiwmpsettings2-iwmpsettings2-requestmediaaccessrights--vb-and-c.md)
</dt> </dl>

 

 





