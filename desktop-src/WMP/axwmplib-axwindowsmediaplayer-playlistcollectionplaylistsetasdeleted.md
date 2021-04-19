---
title: AxWindowsMediaPlayer 物件的 PlaylistCollectionPlaylistSetAsDeleted 事件
description: PlaylistCollectionPlaylistSetAsDeleted 事件已保留供日後使用。
ms.assetid: 6c0a4d2c-e965-4a88-acd4-2a2a12265e36
keywords:
- AxWindowsMediaPlayer 物件的 PlaylistCollectionPlaylistSetAsDeleted 事件 Windows Media Player
topic_type:
- apiref
api_name:
- PlaylistCollectionPlaylistSetAsDeleted Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bf432ede40298abed98cdf0c5b02b0a192f7b3a9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107000964"
---
# <a name="playlistcollectionplaylistsetasdeleted-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="6a474-104">AxWindowsMediaPlayer 物件的 PlaylistCollectionPlaylistSetAsDeleted 事件</span><span class="sxs-lookup"><span data-stu-id="6a474-104">PlaylistCollectionPlaylistSetAsDeleted Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="6a474-105">PlaylistCollectionPlaylistSetAsDeleted 事件已保留供日後使用。</span><span class="sxs-lookup"><span data-stu-id="6a474-105">The PlaylistCollectionPlaylistSetAsDeleted event is reserved for future use.</span></span>

``` syntax
[C#]
private void player_PlaylistCollectionPlaylistSetAsDeleted(
  object sender,
  _WMPOCXEvents_PlaylistCollectionPlaylistSetAsDeletedEvent e
)

[Visual Basic]
Private Sub player_PlaylistCollectionPlaylistSetAsDeleted(
  sender As Object,
  e As _WMPOCXEvents_PlaylistCollectionPlaylistSetAsDeletedEvent
) Handles player.PlaylistCollectionPlaylistSetAsDeleted
```

## <a name="event-data"></a><span data-ttu-id="6a474-106">事件資料</span><span class="sxs-lookup"><span data-stu-id="6a474-106">Event Data</span></span>

<span data-ttu-id="6a474-107">與這個事件相關聯的處理常式屬於 **AxWMPLib 型別。 \_WMPOCXEvents \_ PlaylistCollectionPlaylistSetAsDeletedEventHandler**。</span><span class="sxs-lookup"><span data-stu-id="6a474-107">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_PlaylistCollectionPlaylistSetAsDeletedEventHandler**.</span></span> <span data-ttu-id="6a474-108">這個處理常式會接收 AxWMPLib 型別的引數 **。 \_WMPOCXEvents \_ PlaylistCollectionPlaylistSetAsDeletedEvent**，其中包含與這個事件相關的下列屬性。</span><span class="sxs-lookup"><span data-stu-id="6a474-108">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_PlaylistCollectionPlaylistSetAsDeletedEvent**, which contains the following properties related to this event.</span></span>



| <span data-ttu-id="6a474-109">屬性</span><span class="sxs-lookup"><span data-stu-id="6a474-109">Property</span></span>         | <span data-ttu-id="6a474-110">描述</span><span class="sxs-lookup"><span data-stu-id="6a474-110">Description</span></span>                                 |
|------------------|---------------------------------------------|
| <span data-ttu-id="6a474-111">bstrPlaylistName</span><span class="sxs-lookup"><span data-stu-id="6a474-111">bstrPlaylistName</span></span> | <span data-ttu-id="6a474-112">**System.string** 不支援。</span><span class="sxs-lookup"><span data-stu-id="6a474-112">**System.String** Not supported.</span></span><br/>  |
| <span data-ttu-id="6a474-113">varfIsDeleted</span><span class="sxs-lookup"><span data-stu-id="6a474-113">varfIsDeleted</span></span>    | <span data-ttu-id="6a474-114"> System.string不支援。</span><span class="sxs-lookup"><span data-stu-id="6a474-114">**System.Boolean** Not supported.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="6a474-115">備註</span><span class="sxs-lookup"><span data-stu-id="6a474-115">Remarks</span></span>

<span data-ttu-id="6a474-116">此事件已保留供日後使用。</span><span class="sxs-lookup"><span data-stu-id="6a474-116">This event is reserved for future use.</span></span>

## <a name="requirements"></a><span data-ttu-id="6a474-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="6a474-117">Requirements</span></span>



| <span data-ttu-id="6a474-118">需求</span><span class="sxs-lookup"><span data-stu-id="6a474-118">Requirement</span></span> | <span data-ttu-id="6a474-119">值</span><span class="sxs-lookup"><span data-stu-id="6a474-119">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6a474-120">版本</span><span class="sxs-lookup"><span data-stu-id="6a474-120">Version</span></span><br/>   | <span data-ttu-id="6a474-121">Windows Media Player 9 系列或更新版本</span><span class="sxs-lookup"><span data-stu-id="6a474-121">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="6a474-122">命名空間</span><span class="sxs-lookup"><span data-stu-id="6a474-122">Namespace</span></span><br/> | <span data-ttu-id="6a474-123">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="6a474-123">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="6a474-124">組件</span><span class="sxs-lookup"><span data-stu-id="6a474-124">Assembly</span></span><br/>  | <dl> <span data-ttu-id="6a474-125"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll) </dt></span><span class="sxs-lookup"><span data-stu-id="6a474-125"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6a474-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6a474-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6a474-127">**AxWindowsMediaPlayer 物件 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="6a474-127">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> </dl>

 

 





