---
title: IWMPPlaylistCollection isDeleted 方法
description: IsDeleted 方法會傳回值，指出指定的播放清單是否在 [刪除的專案] 資料夾中。
ms.assetid: 02bc4b9f-6149-4fe2-8417-6484b22f2d74
keywords:
- isDeleted 方法 Windows Media Player
- isDeleted 方法 Windows Media Player，IWMPPlaylistCollection 介面
- IWMPPlaylistCollection 介面 Windows Media Player，isDeleted 方法
topic_type:
- apiref
api_name:
- IWMPPlaylistCollection.isDeleted
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d4ce4a314378c5a4a211a52b99ea1b36ae1fda8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107000651"
---
# <a name="iwmpplaylistcollectionisdeleted-method"></a><span data-ttu-id="a9d5f-106">IWMPPlaylistCollection：： isDeleted 方法</span><span class="sxs-lookup"><span data-stu-id="a9d5f-106">IWMPPlaylistCollection::isDeleted method</span></span>

<span data-ttu-id="a9d5f-107">**IsDeleted** 方法會傳回值，指出指定的播放清單是否在 [刪除的專案] 資料夾中。</span><span class="sxs-lookup"><span data-stu-id="a9d5f-107">The **isDeleted** method returns a value indicating whether the specified playlist is in the deleted items folder.</span></span>

## <a name="syntax"></a><span data-ttu-id="a9d5f-108">語法</span><span class="sxs-lookup"><span data-stu-id="a9d5f-108">Syntax</span></span>


```CSharp
public System.Boolean isDeleted(
  IWMPPlaylist pItem
);
```


```VB

Public Function isDeleted( _
  ByVal pItem As IWMPPlaylist _
) As System.Boolean
Implements IWMPPlaylistCollection.isDeleted
```





## <a name="parameters"></a><span data-ttu-id="a9d5f-109">參數</span><span class="sxs-lookup"><span data-stu-id="a9d5f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a9d5f-110">*pItem* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a9d5f-110">*pItem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a9d5f-111">所查詢播放清單的 **WMPLib IWMPPlaylist** 介面。</span><span class="sxs-lookup"><span data-stu-id="a9d5f-111">A **WMPLib.IWMPPlaylist** interface for the queried playlist.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a9d5f-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="a9d5f-112">Return value</span></span>

<span data-ttu-id="a9d5f-113">指定播放清單是否已刪除的 **布林值** 。</span><span class="sxs-lookup"><span data-stu-id="a9d5f-113">A **System.Boolean** that specifies whether the playlist was deleted.</span></span>

## <a name="requirements"></a><span data-ttu-id="a9d5f-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="a9d5f-114">Requirements</span></span>



| <span data-ttu-id="a9d5f-115">需求</span><span class="sxs-lookup"><span data-stu-id="a9d5f-115">Requirement</span></span> | <span data-ttu-id="a9d5f-116">值</span><span class="sxs-lookup"><span data-stu-id="a9d5f-116">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a9d5f-117">版本</span><span class="sxs-lookup"><span data-stu-id="a9d5f-117">Version</span></span><br/>   | <span data-ttu-id="a9d5f-118">Windows Media Player  9  系列或更新的版本。</span><span class="sxs-lookup"><span data-stu-id="a9d5f-118">Windows Media Player 9 Series or later.</span></span><br/>                                                                     |
| <span data-ttu-id="a9d5f-119">命名空間</span><span class="sxs-lookup"><span data-stu-id="a9d5f-119">Namespace</span></span><br/> | <span data-ttu-id="a9d5f-120">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="a9d5f-120">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="a9d5f-121">組件</span><span class="sxs-lookup"><span data-stu-id="a9d5f-121">Assembly</span></span><br/>  | <dl> <span data-ttu-id="a9d5f-122"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll) </dt></span><span class="sxs-lookup"><span data-stu-id="a9d5f-122"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a9d5f-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a9d5f-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a9d5f-124">**IWMPPlaylist 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="a9d5f-124">**IWMPPlaylist Interface (VB and C#)**</span></span>](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="a9d5f-125">**IWMPPlaylistCollection 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="a9d5f-125">**IWMPPlaylistCollection Interface (VB and C#)**</span></span>](iwmpplaylistcollection--vb-and-c.md)
</dt> </dl>

 

 





