---
title: IWMPMediaCollection getMediaAtom 方法
description: GetMediaAtom 方法會傳回一組可用屬性中指定屬性的索引。
ms.assetid: 01e3d073-677b-4939-96d3-63ae96eaa25d
keywords:
- getMediaAtom 方法 Windows Media Player
- getMediaAtom 方法 Windows Media Player，IWMPMediaCollection 介面
- IWMPMediaCollection 介面 Windows Media Player，getMediaAtom 方法
topic_type:
- apiref
api_name:
- IWMPMediaCollection.getMediaAtom
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 08487cf60c351ff4f8e0741209655cb78c30c3f4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999730"
---
# <a name="iwmpmediacollectiongetmediaatom-method"></a><span data-ttu-id="2905e-106">IWMPMediaCollection：： getMediaAtom 方法</span><span class="sxs-lookup"><span data-stu-id="2905e-106">IWMPMediaCollection::getMediaAtom method</span></span>

<span data-ttu-id="2905e-107">方法會傳回 `getMediaAtom` 一組可用屬性中指定屬性的索引。</span><span class="sxs-lookup"><span data-stu-id="2905e-107">The `getMediaAtom` method returns the index of a specified attribute within the set of available attributes.</span></span>

## <a name="syntax"></a><span data-ttu-id="2905e-108">語法</span><span class="sxs-lookup"><span data-stu-id="2905e-108">Syntax</span></span>


```CSharp
public System.Int32 getMediaAtom(
  System.String bstrItemName
);
```


```VB

Public Function getMediaAtom( _
  ByVal bstrItemName As System.String _
) As System.Int32
Implements IWMPMediaCollection.getMediaAtom
```





## <a name="parameters"></a><span data-ttu-id="2905e-109">參數</span><span class="sxs-lookup"><span data-stu-id="2905e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2905e-110">*bstrItemName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2905e-110">*bstrItemName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2905e-111">**System.string** ，此為應抓取索引的專案名稱。</span><span class="sxs-lookup"><span data-stu-id="2905e-111">The **System.String** that is the name of the item for which the index should be retrieved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2905e-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="2905e-112">Return value</span></span>

<span data-ttu-id="2905e-113">做為索引的 **system.object** 。</span><span class="sxs-lookup"><span data-stu-id="2905e-113">The **System.Int32** that is the index.</span></span>

## <a name="remarks"></a><span data-ttu-id="2905e-114">備註</span><span class="sxs-lookup"><span data-stu-id="2905e-114">Remarks</span></span>

<span data-ttu-id="2905e-115">使用這個方法取出的索引編號可以傳遞給 **IWMPMedia. getItemInfoByAtom** 以存取屬性值。</span><span class="sxs-lookup"><span data-stu-id="2905e-115">The index number retrieved with this method can be passed to the **IWMPMedia.getItemInfoByAtom** to access attribute values.</span></span> <span data-ttu-id="2905e-116">使用大型播放清單時，這項技術通常更有效率，而不是透過 **IWMPMedia. getItemInfo** 存取屬性值。</span><span class="sxs-lookup"><span data-stu-id="2905e-116">This technique is generally more efficient when working with large playlists than accessing an attribute value by name through **IWMPMedia.getItemInfo**.</span></span>

<span data-ttu-id="2905e-117">在呼叫這個方法之前，您必須擁有程式庫的讀取權限。</span><span class="sxs-lookup"><span data-stu-id="2905e-117">Before calling this method, you must have read access to the library.</span></span> <span data-ttu-id="2905e-118">如需詳細資訊，請參閱連結 [庫存取](library-access.md)。</span><span class="sxs-lookup"><span data-stu-id="2905e-118">For more information, see [Library Access](library-access.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="2905e-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="2905e-119">Requirements</span></span>



| <span data-ttu-id="2905e-120">需求</span><span class="sxs-lookup"><span data-stu-id="2905e-120">Requirement</span></span> | <span data-ttu-id="2905e-121">值</span><span class="sxs-lookup"><span data-stu-id="2905e-121">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2905e-122">版本</span><span class="sxs-lookup"><span data-stu-id="2905e-122">Version</span></span><br/>   | <span data-ttu-id="2905e-123">Windows Media Player 9 系列或更新版本</span><span class="sxs-lookup"><span data-stu-id="2905e-123">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="2905e-124">命名空間</span><span class="sxs-lookup"><span data-stu-id="2905e-124">Namespace</span></span><br/> | <span data-ttu-id="2905e-125">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="2905e-125">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="2905e-126">組件</span><span class="sxs-lookup"><span data-stu-id="2905e-126">Assembly</span></span><br/>  | <dl> <span data-ttu-id="2905e-127"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll) </dt></span><span class="sxs-lookup"><span data-stu-id="2905e-127"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2905e-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2905e-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2905e-129">**IWMPMedia. getItemInfo (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="2905e-129">**IWMPMedia.getItemInfo (VB and C#)**</span></span>](wmplibiwmpmedia-iwmpmedia-getiteminfo--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="2905e-130">**IWMPMedia. getItemInfoByAtom (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="2905e-130">**IWMPMedia.getItemInfoByAtom (VB and C#)**</span></span>](wmplibiwmpmedia-iwmpmedia-getiteminfobyatom--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="2905e-131">**IWMPMediaCollection 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="2905e-131">**IWMPMediaCollection Interface (VB and C#)**</span></span>](iwmpmediacollection--vb-and-c.md)
</dt> </dl>

 

 





