---
title: IWMPPlaylist count 屬性
description: Count 屬性會取得播放清單中的媒體專案數目。
ms.assetid: dbff3c86-2d42-4d47-a5cb-b8199efac728
keywords:
- count 屬性 Windows Media Player
- count 屬性 Windows Media Player，IWMPPlaylist 介面
- IWMPPlaylist 介面 Windows Media Player，count 屬性
topic_type:
- apiref
api_name:
- IWMPPlaylist.count
- IWMPPlaylist.get_count
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56d988fefc436b65652d2b0765320ca289417c9c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993586"
---
# <a name="iwmpplaylistcount-property"></a><span data-ttu-id="b3265-106">IWMPPlaylist：： count 屬性</span><span class="sxs-lookup"><span data-stu-id="b3265-106">IWMPPlaylist::count property</span></span>

<span data-ttu-id="b3265-107">**Count** 屬性會取得播放清單中的媒體專案數目。</span><span class="sxs-lookup"><span data-stu-id="b3265-107">The **count** property gets the number of media items in a playlist.</span></span>

<span data-ttu-id="b3265-108">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="b3265-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="b3265-109">語法</span><span class="sxs-lookup"><span data-stu-id="b3265-109">Syntax</span></span>


```CSharp
public System.Int32 count {get;}
```


```VB

Public ReadOnly Property count As System.Int32
```





## <a name="property-value"></a><span data-ttu-id="b3265-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="b3265-110">Property value</span></span>

<span data-ttu-id="b3265-111">一 **種** system.string，也就是播放清單中的媒體專案數目。</span><span class="sxs-lookup"><span data-stu-id="b3265-111">A **System.Int32** that is the number of media items in the playlist.</span></span>

## <a name="remarks"></a><span data-ttu-id="b3265-112">備註</span><span class="sxs-lookup"><span data-stu-id="b3265-112">Remarks</span></span>

<span data-ttu-id="b3265-113">使用這個屬性之前，您必須擁有程式庫的讀取權限。</span><span class="sxs-lookup"><span data-stu-id="b3265-113">Before using this property, you must have read access to the library.</span></span> <span data-ttu-id="b3265-114">如需詳細資訊，請參閱連結 [庫存取](library-access.md)。</span><span class="sxs-lookup"><span data-stu-id="b3265-114">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="b3265-115">如需使用這個屬性的範例程式碼，請參閱 [attributeCount](wmplibiwmpplaylist-iwmpplaylist-attributecount--vb-and-c.md) 屬性。</span><span class="sxs-lookup"><span data-stu-id="b3265-115">See the [attributeCount](wmplibiwmpplaylist-iwmpplaylist-attributecount--vb-and-c.md) property for example code that uses this property.</span></span>

## <a name="requirements"></a><span data-ttu-id="b3265-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="b3265-116">Requirements</span></span>



| <span data-ttu-id="b3265-117">需求</span><span class="sxs-lookup"><span data-stu-id="b3265-117">Requirement</span></span> | <span data-ttu-id="b3265-118">值</span><span class="sxs-lookup"><span data-stu-id="b3265-118">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b3265-119">版本</span><span class="sxs-lookup"><span data-stu-id="b3265-119">Version</span></span><br/>   | <span data-ttu-id="b3265-120">Windows Media Player 9 系列或更新版本</span><span class="sxs-lookup"><span data-stu-id="b3265-120">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="b3265-121">命名空間</span><span class="sxs-lookup"><span data-stu-id="b3265-121">Namespace</span></span><br/> | <span data-ttu-id="b3265-122">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="b3265-122">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="b3265-123">組件</span><span class="sxs-lookup"><span data-stu-id="b3265-123">Assembly</span></span><br/>  | <dl> <span data-ttu-id="b3265-124"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll) </dt></span><span class="sxs-lookup"><span data-stu-id="b3265-124"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b3265-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b3265-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b3265-126">**IWMPPlaylist 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="b3265-126">**IWMPPlaylist Interface (VB and C#)**</span></span>](iwmpplaylist--vb-and-c.md)
</dt> </dl>

 

 





