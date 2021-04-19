---
title: IWMPPlaylist insertItem 方法
description: InsertItem 方法會將媒體專案插入播放清單中的指定位置。
ms.assetid: 6e472f0a-13df-41d9-8e6f-8430d87fe978
keywords:
- insertItem 方法 Windows Media Player
- insertItem 方法 Windows Media Player，IWMPPlaylist 介面
- IWMPPlaylist 介面 Windows Media Player，insertItem 方法
topic_type:
- apiref
api_name:
- IWMPPlaylist.insertItem
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b1ef167a5f3931f34d4cd6fb91b3d044affb9484
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984368"
---
# <a name="iwmpplaylistinsertitem-method"></a><span data-ttu-id="49b24-106">IWMPPlaylist：： insertItem 方法</span><span class="sxs-lookup"><span data-stu-id="49b24-106">IWMPPlaylist::insertItem method</span></span>

<span data-ttu-id="49b24-107">**InsertItem** 方法會將媒體專案插入播放清單中的指定位置。</span><span class="sxs-lookup"><span data-stu-id="49b24-107">The **insertItem** method inserts a media item at a specified location in a playlist.</span></span>

## <a name="syntax"></a><span data-ttu-id="49b24-108">語法</span><span class="sxs-lookup"><span data-stu-id="49b24-108">Syntax</span></span>


```CSharp
public void insertItem(
  System.Int32 lIndex,
  IWMPMedia pIWMPMedia
);
```


```VB

Public Sub insertItem( _
  ByVal lIndex As System.Int32, _
  ByVal pIWMPMedia As IWMPMedia _
)
Implements IWMPPlaylist.insertItem
```





## <a name="parameters"></a><span data-ttu-id="49b24-109">參數</span><span class="sxs-lookup"><span data-stu-id="49b24-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="49b24-110">*lIndex* \[在\]</span><span class="sxs-lookup"><span data-stu-id="49b24-110">*lIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="49b24-111">以零為基底的索引，也就是媒體專案將插入播放清單中的位置 **。**</span><span class="sxs-lookup"><span data-stu-id="49b24-111">A **System.Int32** that is the zero-based index at which the media item will be inserted in the playlist.</span></span>

</dd> <dt>

<span data-ttu-id="49b24-112">*pIWMPMedia* \[在\]</span><span class="sxs-lookup"><span data-stu-id="49b24-112">*pIWMPMedia* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="49b24-113">代表要插入之媒體專案的 **WMPLib IWMPMedia** 介面。</span><span class="sxs-lookup"><span data-stu-id="49b24-113">A **WMPLib.IWMPMedia** interface that represents the media item to be inserted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="49b24-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="49b24-114">Return value</span></span>

<span data-ttu-id="49b24-115">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="49b24-115">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="49b24-116">備註</span><span class="sxs-lookup"><span data-stu-id="49b24-116">Remarks</span></span>

<span data-ttu-id="49b24-117">插入專案之後的所有媒體專案都會增加一個索引。</span><span class="sxs-lookup"><span data-stu-id="49b24-117">All media items after the inserted item will have their indexes increased by one.</span></span>

<span data-ttu-id="49b24-118">在呼叫這個方法之前，您必須擁有程式庫的完整存取權。</span><span class="sxs-lookup"><span data-stu-id="49b24-118">Before calling this method, you must have full access to the library.</span></span> <span data-ttu-id="49b24-119">如需詳細資訊，請參閱連結 [庫存取](library-access.md)。</span><span class="sxs-lookup"><span data-stu-id="49b24-119">For more information, see [Library Access](library-access.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="49b24-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="49b24-120">Requirements</span></span>



| <span data-ttu-id="49b24-121">需求</span><span class="sxs-lookup"><span data-stu-id="49b24-121">Requirement</span></span> | <span data-ttu-id="49b24-122">值</span><span class="sxs-lookup"><span data-stu-id="49b24-122">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="49b24-123">版本</span><span class="sxs-lookup"><span data-stu-id="49b24-123">Version</span></span><br/>   | <span data-ttu-id="49b24-124">Windows Media Player 9 系列或更新版本</span><span class="sxs-lookup"><span data-stu-id="49b24-124">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="49b24-125">命名空間</span><span class="sxs-lookup"><span data-stu-id="49b24-125">Namespace</span></span><br/> | <span data-ttu-id="49b24-126">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="49b24-126">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="49b24-127">組件</span><span class="sxs-lookup"><span data-stu-id="49b24-127">Assembly</span></span><br/>  | <dl> <span data-ttu-id="49b24-128"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll) </dt></span><span class="sxs-lookup"><span data-stu-id="49b24-128"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="49b24-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="49b24-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="49b24-130">**IWMPMedia 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="49b24-130">**IWMPMedia Interface (VB and C#)**</span></span>](iwmpmedia--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="49b24-131">**IWMPPlaylist 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="49b24-131">**IWMPPlaylist Interface (VB and C#)**</span></span>](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="49b24-132">**IWMPPlaylist. removeItem (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="49b24-132">**IWMPPlaylist.removeItem (VB and C#)**</span></span>](wmplibiwmpplaylist-iwmpplaylist-removeitem--vb-and-c.md)
</dt> </dl>

 

 





