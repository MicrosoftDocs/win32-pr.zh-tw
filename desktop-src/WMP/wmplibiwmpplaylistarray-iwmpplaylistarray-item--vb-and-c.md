---
title: IWMPPlaylistArray Item 方法
description: Item 方法會傳回 IWMPPlaylist 介面，代表指定索引處的播放清單。
ms.assetid: 5cb4b89f-b679-4d92-a5f9-5d0fe686775d
keywords:
- Item 方法 Windows Media Player
- Item 方法 Windows Media Player，IWMPPlaylistArray 介面
- IWMPPlaylistArray 介面 Windows Media Player，Item 方法
topic_type:
- apiref
api_name:
- IWMPPlaylistArray.Item
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 660e919ef51bbb9584971f25bdf92296d331de23
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999287"
---
# <a name="iwmpplaylistarrayitem-method"></a><span data-ttu-id="51542-106">IWMPPlaylistArray：： Item 方法</span><span class="sxs-lookup"><span data-stu-id="51542-106">IWMPPlaylistArray::Item method</span></span>

<span data-ttu-id="51542-107">**Item** 方法會傳回 **IWMPPlaylist** 介面，代表指定索引處的播放清單。</span><span class="sxs-lookup"><span data-stu-id="51542-107">The **Item** method returns an **IWMPPlaylist** interface representing the playlist at the specified index.</span></span>

## <a name="syntax"></a><span data-ttu-id="51542-108">語法</span><span class="sxs-lookup"><span data-stu-id="51542-108">Syntax</span></span>


```CSharp
public IWMPPlaylist Item(
  System.Int32 lIndex
);
```


```VB

Public Function Item( _
  ByVal lIndex As System.Int32 _
) As IWMPPlaylist
Implements IWMPPlaylistArray.Item
```





## <a name="parameters"></a><span data-ttu-id="51542-109">參數</span><span class="sxs-lookup"><span data-stu-id="51542-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="51542-110">*lIndex* \[在\]</span><span class="sxs-lookup"><span data-stu-id="51542-110">*lIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="51542-111">包含索引的 **system.object** ，此索引會識別該方法應該抓取的播放清單。</span><span class="sxs-lookup"><span data-stu-id="51542-111">A **System.Int32** containing the index that identifies the playlist that the method should retrieve.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="51542-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="51542-112">Return value</span></span>

<span data-ttu-id="51542-113">已抓取播放清單的 **WMPLib IWMPPlaylist** 介面。</span><span class="sxs-lookup"><span data-stu-id="51542-113">A **WMPLib.IWMPPlaylist** interface for the retrieved playlist.</span></span>

## <a name="remarks"></a><span data-ttu-id="51542-114">備註</span><span class="sxs-lookup"><span data-stu-id="51542-114">Remarks</span></span>

<span data-ttu-id="51542-115">在呼叫這個方法之前，您必須擁有程式庫的讀取權限。</span><span class="sxs-lookup"><span data-stu-id="51542-115">Before calling this method, you must have read access to the library.</span></span> <span data-ttu-id="51542-116">如需詳細資訊，請參閱連結 [庫存取](library-access.md)。</span><span class="sxs-lookup"><span data-stu-id="51542-116">For more information, see [Library Access](library-access.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="51542-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="51542-117">Requirements</span></span>



| <span data-ttu-id="51542-118">需求</span><span class="sxs-lookup"><span data-stu-id="51542-118">Requirement</span></span> | <span data-ttu-id="51542-119">值</span><span class="sxs-lookup"><span data-stu-id="51542-119">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="51542-120">版本</span><span class="sxs-lookup"><span data-stu-id="51542-120">Version</span></span><br/>   | <span data-ttu-id="51542-121">Windows Media Player  9  系列或更新的版本。</span><span class="sxs-lookup"><span data-stu-id="51542-121">Windows Media Player 9 Series or later.</span></span><br/>                                                                     |
| <span data-ttu-id="51542-122">命名空間</span><span class="sxs-lookup"><span data-stu-id="51542-122">Namespace</span></span><br/> | <span data-ttu-id="51542-123">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="51542-123">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="51542-124">組件</span><span class="sxs-lookup"><span data-stu-id="51542-124">Assembly</span></span><br/>  | <dl> <span data-ttu-id="51542-125"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll) </dt></span><span class="sxs-lookup"><span data-stu-id="51542-125"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="51542-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="51542-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="51542-127">**IWMPPlaylist 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="51542-127">**IWMPPlaylist Interface (VB and C#)**</span></span>](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="51542-128">**IWMPPlaylistArray 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="51542-128">**IWMPPlaylistArray Interface (VB and C#)**</span></span>](iwmpplaylistarray--vb-and-c.md)
</dt> </dl>

 

 





