---
title: IWMPMedia getItemInfoByAtom 方法
description: GetItemInfoByAtom 方法會傳回具有指定之索引編號的屬性值。
ms.assetid: d9a4b737-add1-4bbd-8e03-e58f45d65a62
keywords:
- getItemInfoByAtom 方法 Windows Media Player
- getItemInfoByAtom 方法 Windows Media Player，IWMPMedia 介面
- IWMPMedia 介面 Windows Media Player，getItemInfoByAtom 方法
topic_type:
- apiref
api_name:
- IWMPMedia.getItemInfoByAtom
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb37243960360120fbfe508a39db31e37728ac39
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999496"
---
# <a name="iwmpmediagetiteminfobyatom-method"></a><span data-ttu-id="8d8e0-106">IWMPMedia：： getItemInfoByAtom 方法</span><span class="sxs-lookup"><span data-stu-id="8d8e0-106">IWMPMedia::getItemInfoByAtom method</span></span>

<span data-ttu-id="8d8e0-107">**GetItemInfoByAtom** 方法會傳回具有指定之索引編號的屬性值。</span><span class="sxs-lookup"><span data-stu-id="8d8e0-107">The **getItemInfoByAtom** method returns the value of the attribute with the specified index number.</span></span>

## <a name="syntax"></a><span data-ttu-id="8d8e0-108">語法</span><span class="sxs-lookup"><span data-stu-id="8d8e0-108">Syntax</span></span>


```CSharp
public System.String getItemInfoByAtom(
  System.Int32 lAtom
);
```


```VB

Public Function getItemInfoByAtom( _
  ByVal lAtom As System.Int32 _
) As System.String
Implements IWMPMedia.getItemInfoByAtom
```





## <a name="parameters"></a><span data-ttu-id="8d8e0-109">參數</span><span class="sxs-lookup"><span data-stu-id="8d8e0-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8d8e0-110">*lAtom* \[在\]</span><span class="sxs-lookup"><span data-stu-id="8d8e0-110">*lAtom* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8d8e0-111">指定所要求屬性位於可用屬性集合內之索引的 **system.object。**</span><span class="sxs-lookup"><span data-stu-id="8d8e0-111">A **System.Int32** that specifies the index at which the requested attribute resides within the set of available attributes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8d8e0-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="8d8e0-112">Return value</span></span>

<span data-ttu-id="8d8e0-113">**System.string** ，此為屬性的值。</span><span class="sxs-lookup"><span data-stu-id="8d8e0-113">A **System.String** that is the value of the attribute.</span></span>

## <a name="remarks"></a><span data-ttu-id="8d8e0-114">備註</span><span class="sxs-lookup"><span data-stu-id="8d8e0-114">Remarks</span></span>

<span data-ttu-id="8d8e0-115">這個方法可以用來使用屬性索引編號來取得特定媒體專案的中繼資料。</span><span class="sxs-lookup"><span data-stu-id="8d8e0-115">This method can be used to retrieve metadata for a specific media item by using an attribute index number.</span></span> <span data-ttu-id="8d8e0-116">**AttributeCount** 屬性可以用來判斷媒體專案可用的屬性數目。</span><span class="sxs-lookup"><span data-stu-id="8d8e0-116">The **attributeCount** property can be used to determine the number of attributes available for the media item.</span></span>

<span data-ttu-id="8d8e0-117">**IWMPMediaCollection** 介面的 **getMediaAtom** 方法也可以用來取得特定屬性的索引。</span><span class="sxs-lookup"><span data-stu-id="8d8e0-117">The **getMediaAtom** method of the **IWMPMediaCollection** interface can also be used to retrieve the index of a particular attribute.</span></span> <span data-ttu-id="8d8e0-118">這項技術通常比使用大型播放清單時的 **getItemInfo** 或 **getItemInfoByType** 方法更有效率。</span><span class="sxs-lookup"><span data-stu-id="8d8e0-118">This technique is generally more efficient than the **getItemInfo** or **getItemInfoByType** methods when working with large playlists.</span></span>

<span data-ttu-id="8d8e0-119">在呼叫這個方法之前，您必須擁有程式庫的讀取權限。</span><span class="sxs-lookup"><span data-stu-id="8d8e0-119">Before calling this method, you must have read access to the library.</span></span> <span data-ttu-id="8d8e0-120">如需詳細資訊，請參閱連結 [庫存取](library-access.md)。</span><span class="sxs-lookup"><span data-stu-id="8d8e0-120">For more information, see [Library Access](library-access.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="8d8e0-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="8d8e0-121">Requirements</span></span>



| <span data-ttu-id="8d8e0-122">需求</span><span class="sxs-lookup"><span data-stu-id="8d8e0-122">Requirement</span></span> | <span data-ttu-id="8d8e0-123">值</span><span class="sxs-lookup"><span data-stu-id="8d8e0-123">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8d8e0-124">版本</span><span class="sxs-lookup"><span data-stu-id="8d8e0-124">Version</span></span><br/>   | <span data-ttu-id="8d8e0-125">Windows Media Player 9 系列或更新版本</span><span class="sxs-lookup"><span data-stu-id="8d8e0-125">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="8d8e0-126">命名空間</span><span class="sxs-lookup"><span data-stu-id="8d8e0-126">Namespace</span></span><br/> | <span data-ttu-id="8d8e0-127">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="8d8e0-127">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="8d8e0-128">組件</span><span class="sxs-lookup"><span data-stu-id="8d8e0-128">Assembly</span></span><br/>  | <dl> <span data-ttu-id="8d8e0-129"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll) </dt></span><span class="sxs-lookup"><span data-stu-id="8d8e0-129"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8d8e0-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8d8e0-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8d8e0-131">**IWMPMedia 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="8d8e0-131">**IWMPMedia Interface (VB and C#)**</span></span>](iwmpmedia--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="8d8e0-132">**IWMPMedia. attributeCount (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="8d8e0-132">**IWMPMedia.attributeCount (VB and C#)**</span></span>](wmplibiwmpmedia-iwmpmedia-attributecount--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="8d8e0-133">**IWMPMedia. getItemInfo (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="8d8e0-133">**IWMPMedia.getItemInfo (VB and C#)**</span></span>](wmplibiwmpmedia-iwmpmedia-getiteminfo--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="8d8e0-134">**IWMPMedia. setItemInfo (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="8d8e0-134">**IWMPMedia.setItemInfo (VB and C#)**</span></span>](wmplibiwmpmedia-iwmpmedia-setiteminfo--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="8d8e0-135">**IWMPMedia3. getItemInfoByType (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="8d8e0-135">**IWMPMedia3.getItemInfoByType (VB and C#)**</span></span>](wmplibiwmpmedia3-iwmpmedia3-getiteminfobytype--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="8d8e0-136">**IWMPMediaCollection. getMediaAtom (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="8d8e0-136">**IWMPMediaCollection.getMediaAtom (VB and C#)**</span></span>](wmplibiwmpmediacollection-iwmpmediacollection-getmediaatom--vb-and-c.md)
</dt> </dl>

 

 





