---
title: IWMPPlaylistCollection remove 方法
description: Remove 方法會從文件庫中移除播放清單。 |IWMPPlaylistCollection remove 方法
ms.assetid: 40c8ee1d-13fa-40d9-9532-4dc8383c4eb3
keywords:
- 移除方法 Windows Media Player
- remove 方法 Windows Media Player，IWMPPlaylistCollection 介面
- IWMPPlaylistCollection 介面 Windows Media Player、remove 方法
topic_type:
- apiref
api_name:
- IWMPPlaylistCollection.remove
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c99fbaa2f60c769599bd6173b8e38f4d99e9f42d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990851"
---
# <a name="iwmpplaylistcollectionremove-method"></a><span data-ttu-id="da911-107">IWMPPlaylistCollection：： remove 方法</span><span class="sxs-lookup"><span data-stu-id="da911-107">IWMPPlaylistCollection::remove method</span></span>

<span data-ttu-id="da911-108">**Remove** 方法會從文件庫中移除播放清單。</span><span class="sxs-lookup"><span data-stu-id="da911-108">The **remove** method removes a playlist from the library.</span></span>

## <a name="syntax"></a><span data-ttu-id="da911-109">語法</span><span class="sxs-lookup"><span data-stu-id="da911-109">Syntax</span></span>


```CSharp
public void remove(
  IWMPPlaylist pItem
);
```


```VB

Public Sub remove( _
  ByVal pItem As IWMPPlaylist _
)
Implements IWMPPlaylistCollection.remove
```





## <a name="parameters"></a><span data-ttu-id="da911-110">參數</span><span class="sxs-lookup"><span data-stu-id="da911-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="da911-111">*pItem* \[在\]</span><span class="sxs-lookup"><span data-stu-id="da911-111">*pItem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="da911-112">此方法將移除之播放清單的 **WMPLib IWMPPlaylist** 介面。</span><span class="sxs-lookup"><span data-stu-id="da911-112">A **WMPLib.IWMPPlaylist** interface for the playlist that this method will remove.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="da911-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="da911-113">Return value</span></span>

<span data-ttu-id="da911-114">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="da911-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="da911-115">備註</span><span class="sxs-lookup"><span data-stu-id="da911-115">Remarks</span></span>

<span data-ttu-id="da911-116">在呼叫這個方法之前，您必須擁有程式庫的完整存取權。</span><span class="sxs-lookup"><span data-stu-id="da911-116">Before calling this method, you must have full access to the library.</span></span> <span data-ttu-id="da911-117">如需詳細資訊，請參閱連結 [庫存取](library-access.md)。</span><span class="sxs-lookup"><span data-stu-id="da911-117">For more information, see [Library Access](library-access.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="da911-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="da911-118">Requirements</span></span>



| <span data-ttu-id="da911-119">需求</span><span class="sxs-lookup"><span data-stu-id="da911-119">Requirement</span></span> | <span data-ttu-id="da911-120">值</span><span class="sxs-lookup"><span data-stu-id="da911-120">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="da911-121">版本</span><span class="sxs-lookup"><span data-stu-id="da911-121">Version</span></span><br/>   | <span data-ttu-id="da911-122">Windows Media Player  9  系列或更新的版本。</span><span class="sxs-lookup"><span data-stu-id="da911-122">Windows Media Player 9 Series or later.</span></span><br/>                                                                     |
| <span data-ttu-id="da911-123">命名空間</span><span class="sxs-lookup"><span data-stu-id="da911-123">Namespace</span></span><br/> | <span data-ttu-id="da911-124">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="da911-124">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="da911-125">組件</span><span class="sxs-lookup"><span data-stu-id="da911-125">Assembly</span></span><br/>  | <dl> <span data-ttu-id="da911-126"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll) </dt></span><span class="sxs-lookup"><span data-stu-id="da911-126"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="da911-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="da911-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="da911-128">**IWMPPlaylist 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="da911-128">**IWMPPlaylist Interface (VB and C#)**</span></span>](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="da911-129">**IWMPPlaylistCollection 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="da911-129">**IWMPPlaylistCollection Interface (VB and C#)**</span></span>](iwmpplaylistcollection--vb-and-c.md)
</dt> </dl>

 

 





