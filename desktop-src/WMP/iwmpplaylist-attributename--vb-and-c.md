---
title: 'IWMPPlaylist. attributeName (VB 和 C ) '
description: AttributeName 屬性 (get \_ attributeName 方法 In C \ ) 取得索引所指定之播放清單屬性的名稱。
ms.assetid: bb436657-5156-437e-af58-6497ad3b311b
keywords:
- IWMPPlaylist. attributeName (VB 和 C ) Windows Media Player
topic_type:
- apiref
api_name:
- IWMPPlaylist.attributeName (VB and C )
api_location:
- Interop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 727d58a0cf875ed29efe9235448c1d597e81656a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106992777"
---
# <a name="iwmpplaylistattributename-vb-and-c"></a><span data-ttu-id="1f3a6-104">IWMPPlaylist. attributeName (VB 和 c # ) </span><span class="sxs-lookup"><span data-stu-id="1f3a6-104">IWMPPlaylist.attributeName (VB and C#)</span></span>

<span data-ttu-id="1f3a6-105">**AttributeName** 屬性 (c # 中的 **get \_ attributeName** 方法 ) 取得索引所指定之播放清單屬性的名稱。</span><span class="sxs-lookup"><span data-stu-id="1f3a6-105">The **attributeName** property (the **get\_attributeName** method in C#) gets the name of a playlist attribute specified by an index.</span></span>


```
[Visual Basic]
ReadOnly Property attributeName(
  lIndex As System.Int32
) As System.String
```




```
[C#]
System.String get_attributeName(
  System.Int32 lIndex
);
```



## <a name="parameters"></a><span data-ttu-id="1f3a6-106">參數</span><span class="sxs-lookup"><span data-stu-id="1f3a6-106">Parameters</span></span>

<span data-ttu-id="1f3a6-107">*lIndex*</span><span class="sxs-lookup"><span data-stu-id="1f3a6-107">*lIndex*</span></span>

<span data-ttu-id="1f3a6-108">表示播放清單屬性索引的 **system.string。**</span><span class="sxs-lookup"><span data-stu-id="1f3a6-108">A **System.Int32** that is the index of the playlist attribute.</span></span>

## <a name="return-value"></a><span data-ttu-id="1f3a6-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="1f3a6-109">Return Value</span></span>

<span data-ttu-id="1f3a6-110">**System.string** ，這是播放清單屬性的名稱。</span><span class="sxs-lookup"><span data-stu-id="1f3a6-110">A **System.String** that is the name of the playlist attribute.</span></span>

## <a name="remarks"></a><span data-ttu-id="1f3a6-111">備註</span><span class="sxs-lookup"><span data-stu-id="1f3a6-111">Remarks</span></span>

<span data-ttu-id="1f3a6-112">**IWMPPlaylist** 在使用參數的 Visual Basic 中，attributeName 是唯讀屬性，而在 c # 中則稱為 **IWMPPlaylist. get \_ attributeName** 方法。</span><span class="sxs-lookup"><span data-stu-id="1f3a6-112">**IWMPPlaylist.attributeName** is a read-only property in Visual Basic that takes a parameter, while in C# it is referred to as the **IWMPPlaylist.get\_attributeName** method.</span></span>

<span data-ttu-id="1f3a6-113">**IWMPPlaylist. attributeCount** 屬性會傳回與播放清單相關聯的屬性數目。</span><span class="sxs-lookup"><span data-stu-id="1f3a6-113">The number of attributes associated with a playlist is returned by the **IWMPPlaylist.attributeCount** property.</span></span>

<span data-ttu-id="1f3a6-114">這個屬性所傳回的名稱可以提供給 **setItemInfo** 或 **getItemInfo** 方法，以指定或抓取指名屬性的值。</span><span class="sxs-lookup"><span data-stu-id="1f3a6-114">The name returned by this property can be supplied to the **setItemInfo** or **getItemInfo** methods to specify or retrieve a value for the named attribute.</span></span>

<span data-ttu-id="1f3a6-115">使用這個屬性之前，您必須擁有程式庫的讀取權限。</span><span class="sxs-lookup"><span data-stu-id="1f3a6-115">Before using this property, you must have read access to the library.</span></span> <span data-ttu-id="1f3a6-116">如需詳細資訊，請參閱連結 [庫存取](library-access.md)。</span><span class="sxs-lookup"><span data-stu-id="1f3a6-116">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="1f3a6-117">如需 Windows Media Player 所支援之屬性的詳細資訊，請參閱 [屬性參考](attribute-reference.md)。</span><span class="sxs-lookup"><span data-stu-id="1f3a6-117">For more information about attributes supported by Windows Media Player, see the [Attribute Reference](attribute-reference.md).</span></span>

## <a name="examples"></a><span data-ttu-id="1f3a6-118">範例</span><span class="sxs-lookup"><span data-stu-id="1f3a6-118">Examples</span></span>

<span data-ttu-id="1f3a6-119">如需使用這個屬性的範例程式碼，請參閱 [attributeCount](wmplibiwmpplaylist-iwmpplaylist-attributecount--vb-and-c.md) 屬性。</span><span class="sxs-lookup"><span data-stu-id="1f3a6-119">See the [attributeCount](wmplibiwmpplaylist-iwmpplaylist-attributecount--vb-and-c.md) property for example code that uses this property.</span></span>

## <a name="requirements"></a><span data-ttu-id="1f3a6-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="1f3a6-120">Requirements</span></span>



| <span data-ttu-id="1f3a6-121">需求</span><span class="sxs-lookup"><span data-stu-id="1f3a6-121">Requirement</span></span> | <span data-ttu-id="1f3a6-122">值</span><span class="sxs-lookup"><span data-stu-id="1f3a6-122">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1f3a6-123">版本</span><span class="sxs-lookup"><span data-stu-id="1f3a6-123">Version</span></span><br/>   | <span data-ttu-id="1f3a6-124">Windows Media Player 9 系列或更新版本</span><span class="sxs-lookup"><span data-stu-id="1f3a6-124">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="1f3a6-125">命名空間</span><span class="sxs-lookup"><span data-stu-id="1f3a6-125">Namespace</span></span><br/> | <span data-ttu-id="1f3a6-126">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="1f3a6-126">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="1f3a6-127">組件</span><span class="sxs-lookup"><span data-stu-id="1f3a6-127">Assembly</span></span><br/>  | <dl> <span data-ttu-id="1f3a6-128"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll) </dt></span><span class="sxs-lookup"><span data-stu-id="1f3a6-128"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1f3a6-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1f3a6-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1f3a6-130">**IWMPPlaylist 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="1f3a6-130">**IWMPPlaylist Interface (VB and C#)**</span></span>](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="1f3a6-131">**IWMPPlaylist. attributeCount (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="1f3a6-131">**IWMPPlaylist.attributeCount (VB and C#)**</span></span>](wmplibiwmpplaylist-iwmpplaylist-attributecount--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="1f3a6-132">**IWMPPlaylist. getItemInfo (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="1f3a6-132">**IWMPPlaylist.getItemInfo (VB and C#)**</span></span>](wmplibiwmpplaylist-iwmpplaylist-getiteminfo--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="1f3a6-133">**IWMPPlaylist. setItemInfo (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="1f3a6-133">**IWMPPlaylist.setItemInfo (VB and C#)**</span></span>](wmplibiwmpplaylist-iwmpplaylist-setiteminfo--vb-and-c.md)
</dt> </dl>

 

 





