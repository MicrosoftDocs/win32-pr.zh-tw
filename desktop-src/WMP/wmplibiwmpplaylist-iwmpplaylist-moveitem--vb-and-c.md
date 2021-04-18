---
title: IWMPPlaylist moveItem 方法
description: MoveItem 方法會變更播放清單中媒體專案的位置。
ms.assetid: e82c820f-4640-4289-88c1-79a92e520f00
keywords:
- moveItem 方法 Windows Media Player
- moveItem 方法 Windows Media Player，IWMPPlaylist 介面
- IWMPPlaylist 介面 Windows Media Player，moveItem 方法
topic_type:
- apiref
api_name:
- IWMPPlaylist.moveItem
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c2d5be745fc3dcf799eb7203e607e493b284b4b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106976184"
---
# <a name="iwmpplaylistmoveitem-method"></a><span data-ttu-id="308e9-106">IWMPPlaylist：： moveItem 方法</span><span class="sxs-lookup"><span data-stu-id="308e9-106">IWMPPlaylist::moveItem method</span></span>

<span data-ttu-id="308e9-107">**MoveItem** 方法會變更播放清單中媒體專案的位置。</span><span class="sxs-lookup"><span data-stu-id="308e9-107">The **moveItem** method changes the location of a media item in the playlist.</span></span>

## <a name="syntax"></a><span data-ttu-id="308e9-108">語法</span><span class="sxs-lookup"><span data-stu-id="308e9-108">Syntax</span></span>


```CSharp
public void moveItem(
  System.Int32 lIndexOld,
  System.Int32 lIndexNew
);
```


```VB

Public Sub moveItem( _
  ByVal lIndexOld As System.Int32, _
  ByVal lIndexNew As System.Int32 _
)
Implements IWMPPlaylist.moveItem
```





## <a name="parameters"></a><span data-ttu-id="308e9-109">參數</span><span class="sxs-lookup"><span data-stu-id="308e9-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="308e9-110">*lIndexOld* \[在\]</span><span class="sxs-lookup"><span data-stu-id="308e9-110">*lIndexOld* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="308e9-111">是原始索引的 **system.object** 。</span><span class="sxs-lookup"><span data-stu-id="308e9-111">A **System.Int32** that is the original index.</span></span>

</dd> <dt>

<span data-ttu-id="308e9-112">*lIndexNew* \[在\]</span><span class="sxs-lookup"><span data-stu-id="308e9-112">*lIndexNew* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="308e9-113">是新索引的 **system.object** 。</span><span class="sxs-lookup"><span data-stu-id="308e9-113">A **System.Int32** that is the new index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="308e9-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="308e9-114">Return value</span></span>

<span data-ttu-id="308e9-115">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="308e9-115">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="308e9-116">備註</span><span class="sxs-lookup"><span data-stu-id="308e9-116">Remarks</span></span>

<span data-ttu-id="308e9-117">插入專案之後的所有專案都會以1遞增其索引編號。</span><span class="sxs-lookup"><span data-stu-id="308e9-117">All items after the inserted item will have their index numbers increased by one.</span></span>

<span data-ttu-id="308e9-118">在呼叫這個方法之前，您必須擁有程式庫的完整存取權。</span><span class="sxs-lookup"><span data-stu-id="308e9-118">Before calling this method, you must have full access to the library.</span></span> <span data-ttu-id="308e9-119">如需詳細資訊，請參閱連結 [庫存取](library-access.md)。</span><span class="sxs-lookup"><span data-stu-id="308e9-119">For more information, see [Library Access](library-access.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="308e9-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="308e9-120">Requirements</span></span>



| <span data-ttu-id="308e9-121">需求</span><span class="sxs-lookup"><span data-stu-id="308e9-121">Requirement</span></span> | <span data-ttu-id="308e9-122">值</span><span class="sxs-lookup"><span data-stu-id="308e9-122">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="308e9-123">版本</span><span class="sxs-lookup"><span data-stu-id="308e9-123">Version</span></span><br/>   | <span data-ttu-id="308e9-124">Windows Media Player 9 系列或更新版本</span><span class="sxs-lookup"><span data-stu-id="308e9-124">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="308e9-125">命名空間</span><span class="sxs-lookup"><span data-stu-id="308e9-125">Namespace</span></span><br/> | <span data-ttu-id="308e9-126">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="308e9-126">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="308e9-127">組件</span><span class="sxs-lookup"><span data-stu-id="308e9-127">Assembly</span></span><br/>  | <dl> <span data-ttu-id="308e9-128"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll) </dt></span><span class="sxs-lookup"><span data-stu-id="308e9-128"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="308e9-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="308e9-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="308e9-130">**IWMPPlaylist 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="308e9-130">**IWMPPlaylist Interface (VB and C#)**</span></span>](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="308e9-131">**IWMPSettings2. mediaAccessRights (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="308e9-131">**IWMPSettings2.mediaAccessRights (VB and C#)**</span></span>](wmplibiwmpsettings2-iwmpsettings2-mediaaccessrights--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="308e9-132">**IWMPSettings2. requestMediaAccessRights (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="308e9-132">**IWMPSettings2.requestMediaAccessRights (VB and C#)**</span></span>](wmplibiwmpsettings2-iwmpsettings2-requestmediaaccessrights--vb-and-c.md)
</dt> </dl>

 

 





