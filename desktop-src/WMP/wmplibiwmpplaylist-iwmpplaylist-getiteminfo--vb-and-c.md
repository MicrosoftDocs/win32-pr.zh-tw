---
title: IWMPPlaylist getItemInfo 方法
description: GetItemInfo 方法會傳回依名稱指定的播放清單屬性值。
ms.assetid: 62e882d6-66bb-450c-9700-b99d30dd42fa
keywords:
- getItemInfo 方法 Windows Media Player
- getItemInfo 方法 Windows Media Player，IWMPPlaylist 介面
- IWMPPlaylist 介面 Windows Media Player，getItemInfo 方法
topic_type:
- apiref
api_name:
- IWMPPlaylist.getItemInfo
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ced433b13f5af2d1df8c12dba023b7fbb55c5f7d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990077"
---
# <a name="iwmpplaylistgetiteminfo-method"></a><span data-ttu-id="6722d-106">IWMPPlaylist：： getItemInfo 方法</span><span class="sxs-lookup"><span data-stu-id="6722d-106">IWMPPlaylist::getItemInfo method</span></span>

<span data-ttu-id="6722d-107">**GetItemInfo** 方法會傳回依名稱指定的播放清單屬性值。</span><span class="sxs-lookup"><span data-stu-id="6722d-107">The **getItemInfo** method returns the value of a playlist attribute specified by name.</span></span>

## <a name="syntax"></a><span data-ttu-id="6722d-108">語法</span><span class="sxs-lookup"><span data-stu-id="6722d-108">Syntax</span></span>


```CSharp
public System.String getItemInfo(
  System.String bstrName
);
```


```VB

Public Function getItemInfo( _
  ByVal bstrName As System.String _
) As System.String
Implements IWMPPlaylist.getItemInfo
```





## <a name="parameters"></a><span data-ttu-id="6722d-109">參數</span><span class="sxs-lookup"><span data-stu-id="6722d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6722d-110">*bstrName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6722d-110">*bstrName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6722d-111">**System.string** ，這是播放清單屬性的名稱。</span><span class="sxs-lookup"><span data-stu-id="6722d-111">A **System.String** that is the name of the playlist attribute.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6722d-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="6722d-112">Return value</span></span>

<span data-ttu-id="6722d-113">**System.string** ，這是播放清單屬性的值。</span><span class="sxs-lookup"><span data-stu-id="6722d-113">A **System.String** that is the value of the playlist attribute.</span></span>

## <a name="remarks"></a><span data-ttu-id="6722d-114">備註</span><span class="sxs-lookup"><span data-stu-id="6722d-114">Remarks</span></span>

<span data-ttu-id="6722d-115">使用這個方法之前，您必須擁有程式庫的讀取權限。</span><span class="sxs-lookup"><span data-stu-id="6722d-115">Before using this method, you must have read access to the library.</span></span> <span data-ttu-id="6722d-116">如需詳細資訊，請參閱連結 [庫存取](library-access.md)。</span><span class="sxs-lookup"><span data-stu-id="6722d-116">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="6722d-117">如需使用這個屬性的範例程式碼，請參閱 [attributeCount](wmplibiwmpplaylist-iwmpplaylist-attributecount--vb-and-c.md) 屬性。</span><span class="sxs-lookup"><span data-stu-id="6722d-117">See the [attributeCount](wmplibiwmpplaylist-iwmpplaylist-attributecount--vb-and-c.md) property for example code that uses this property.</span></span>

## <a name="requirements"></a><span data-ttu-id="6722d-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="6722d-118">Requirements</span></span>



| <span data-ttu-id="6722d-119">需求</span><span class="sxs-lookup"><span data-stu-id="6722d-119">Requirement</span></span> | <span data-ttu-id="6722d-120">值</span><span class="sxs-lookup"><span data-stu-id="6722d-120">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6722d-121">版本</span><span class="sxs-lookup"><span data-stu-id="6722d-121">Version</span></span><br/>   | <span data-ttu-id="6722d-122">Windows Media Player 9 系列或更新版本</span><span class="sxs-lookup"><span data-stu-id="6722d-122">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="6722d-123">命名空間</span><span class="sxs-lookup"><span data-stu-id="6722d-123">Namespace</span></span><br/> | <span data-ttu-id="6722d-124">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="6722d-124">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="6722d-125">組件</span><span class="sxs-lookup"><span data-stu-id="6722d-125">Assembly</span></span><br/>  | <dl> <span data-ttu-id="6722d-126"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll) </dt></span><span class="sxs-lookup"><span data-stu-id="6722d-126"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6722d-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6722d-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6722d-128">**IWMPPlaylist 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="6722d-128">**IWMPPlaylist Interface (VB and C#)**</span></span>](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="6722d-129">**IWMPPlaylist. setItemInfo (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="6722d-129">**IWMPPlaylist.setItemInfo (VB and C#)**</span></span>](wmplibiwmpplaylist-iwmpplaylist-setiteminfo--vb-and-c.md)
</dt> </dl>

 

 





