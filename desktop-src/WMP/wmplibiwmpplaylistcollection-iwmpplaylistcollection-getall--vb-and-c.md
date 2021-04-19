---
title: IWMPPlaylistCollection getAll 方法
description: GetAll 方法會傳回 IWMPPlaylistArray 介面，此介面可讓您存取媒體櫃中的所有播放清單。
ms.assetid: d36dbc5c-ccb0-400a-ab5b-918598c218f1
keywords:
- getAll 方法 Windows Media Player
- getAll 方法 Windows Media Player，IWMPPlaylistCollection 介面
- IWMPPlaylistCollection 介面 Windows Media Player，getAll 方法
topic_type:
- apiref
api_name:
- IWMPPlaylistCollection.getAll
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a4260f5c960650cf6c04a1dd8b39d887f711fb8a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106980104"
---
# <a name="iwmpplaylistcollectiongetall-method"></a><span data-ttu-id="4aa1f-106">IWMPPlaylistCollection：： getAll 方法</span><span class="sxs-lookup"><span data-stu-id="4aa1f-106">IWMPPlaylistCollection::getAll method</span></span>

<span data-ttu-id="4aa1f-107">**GetAll** 方法會傳回 **IWMPPlaylistArray** 介面，此介面可讓您存取媒體櫃中的所有播放清單。</span><span class="sxs-lookup"><span data-stu-id="4aa1f-107">The **getAll** method returns an **IWMPPlaylistArray** interface that provides access to all of the playlists in the library.</span></span>

## <a name="syntax"></a><span data-ttu-id="4aa1f-108">語法</span><span class="sxs-lookup"><span data-stu-id="4aa1f-108">Syntax</span></span>


```CSharp
public IWMPPlaylistArray getAll();
```


```VB

Public Function getAll() As IWMPPlaylistArray
Implements IWMPPlaylistCollection.getAll
```





## <a name="parameters"></a><span data-ttu-id="4aa1f-109">參數</span><span class="sxs-lookup"><span data-stu-id="4aa1f-109">Parameters</span></span>

<span data-ttu-id="4aa1f-110">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="4aa1f-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="4aa1f-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="4aa1f-111">Return value</span></span>

<span data-ttu-id="4aa1f-112">已抓取之播放清單陣列的 **WMPLib IWMPPlaylistArray** 介面。</span><span class="sxs-lookup"><span data-stu-id="4aa1f-112">A **WMPLib.IWMPPlaylistArray** interface for the retrieved array of playlists.</span></span>

## <a name="remarks"></a><span data-ttu-id="4aa1f-113">備註</span><span class="sxs-lookup"><span data-stu-id="4aa1f-113">Remarks</span></span>

<span data-ttu-id="4aa1f-114">在呼叫這個方法之前，您必須擁有程式庫的讀取權限。</span><span class="sxs-lookup"><span data-stu-id="4aa1f-114">Before calling this method, you must have read access to the library.</span></span> <span data-ttu-id="4aa1f-115">如需詳細資訊，請參閱連結 [庫存取](library-access.md)。</span><span class="sxs-lookup"><span data-stu-id="4aa1f-115">For more information, see [Library Access](library-access.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="4aa1f-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="4aa1f-116">Requirements</span></span>



| <span data-ttu-id="4aa1f-117">需求</span><span class="sxs-lookup"><span data-stu-id="4aa1f-117">Requirement</span></span> | <span data-ttu-id="4aa1f-118">值</span><span class="sxs-lookup"><span data-stu-id="4aa1f-118">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4aa1f-119">版本</span><span class="sxs-lookup"><span data-stu-id="4aa1f-119">Version</span></span><br/>   | <span data-ttu-id="4aa1f-120">Windows Media Player  9  系列或更新的版本。</span><span class="sxs-lookup"><span data-stu-id="4aa1f-120">Windows Media Player 9 Series or later.</span></span><br/>                                                                     |
| <span data-ttu-id="4aa1f-121">命名空間</span><span class="sxs-lookup"><span data-stu-id="4aa1f-121">Namespace</span></span><br/> | <span data-ttu-id="4aa1f-122">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="4aa1f-122">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="4aa1f-123">組件</span><span class="sxs-lookup"><span data-stu-id="4aa1f-123">Assembly</span></span><br/>  | <dl> <span data-ttu-id="4aa1f-124"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll) </dt></span><span class="sxs-lookup"><span data-stu-id="4aa1f-124"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4aa1f-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4aa1f-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4aa1f-126">**IWMPPlaylistArray 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="4aa1f-126">**IWMPPlaylistArray Interface (VB and C#)**</span></span>](iwmpplaylistarray--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="4aa1f-127">**IWMPPlaylistCollection 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="4aa1f-127">**IWMPPlaylistCollection Interface (VB and C#)**</span></span>](iwmpplaylistcollection--vb-and-c.md)
</dt> </dl>

 

 





