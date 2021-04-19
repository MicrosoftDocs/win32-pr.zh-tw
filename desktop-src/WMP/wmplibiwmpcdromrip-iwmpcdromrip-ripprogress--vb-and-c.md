---
title: IWMPCdromRip ripProgress 屬性
description: RipProgress 屬性會取得 CD 翻錄進度（完成的百分比）。
ms.assetid: 00d4f074-a16d-4c5f-930f-4411b90303f1
keywords:
- ripProgress 屬性 Windows Media Player
- ripProgress 屬性 Windows Media Player，IWMPCdromRip 介面
- IWMPCdromRip 介面 Windows Media Player，ripProgress 屬性
topic_type:
- apiref
api_name:
- IWMPCdromRip.ripProgress
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 113b9fc716698156aa4f7731a7b19888e0edf438
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106987170"
---
# <a name="iwmpcdromripripprogress-property"></a><span data-ttu-id="a1d7b-106">IWMPCdromRip：： ripProgress 屬性</span><span class="sxs-lookup"><span data-stu-id="a1d7b-106">IWMPCdromRip::ripProgress property</span></span>

<span data-ttu-id="a1d7b-107">**RipProgress** 屬性會取得 CD 翻錄進度（完成的百分比）。</span><span class="sxs-lookup"><span data-stu-id="a1d7b-107">The **ripProgress** property gets the CD ripping progress as percent complete.</span></span>

## <a name="syntax"></a><span data-ttu-id="a1d7b-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="a1d7b-108">Syntax</span></span>


```CSharp
public System.Int32 ripProgress {get; set;}
```


```VB

Public ReadOnly Property ripProgress As System.Int32
```





## <a name="property-value"></a><span data-ttu-id="a1d7b-109">屬性值</span><span class="sxs-lookup"><span data-stu-id="a1d7b-109">Property value</span></span>

<span data-ttu-id="a1d7b-110">作為進度值的 **system.object** 。</span><span class="sxs-lookup"><span data-stu-id="a1d7b-110">A **System.Int32** that is the progress value.</span></span> <span data-ttu-id="a1d7b-111">進度值的範圍是從0到100。</span><span class="sxs-lookup"><span data-stu-id="a1d7b-111">Progress values range from 0 to 100.</span></span>

## <a name="remarks"></a><span data-ttu-id="a1d7b-112">備註</span><span class="sxs-lookup"><span data-stu-id="a1d7b-112">Remarks</span></span>

<span data-ttu-id="a1d7b-113">進度值代表整個翻錄進程的完成百分比。</span><span class="sxs-lookup"><span data-stu-id="a1d7b-113">The progress value represents the completed percentage of the entire ripping process.</span></span> <span data-ttu-id="a1d7b-114">若要判斷特定追蹤的進度，請使用 [IWMPMedia getItemInfo](wmplibiwmpplaylist-iwmpplaylist-getiteminfo--vb-and-c.md) 搭配 **RipProgress** 作為屬性名稱。</span><span class="sxs-lookup"><span data-stu-id="a1d7b-114">To determine the progress of a specific track, use [IWMPMedia.getItemInfo](wmplibiwmpplaylist-iwmpplaylist-getiteminfo--vb-and-c.md) with **RipProgress** as the attribute name.</span></span> <span data-ttu-id="a1d7b-115">若要取得目前正在翻錄之追蹤的索引，請使用 "CurrentRipTrackIndex" 做為屬性名稱來呼叫 IWMPPlaylist. getItemInfo。</span><span class="sxs-lookup"><span data-stu-id="a1d7b-115">To get the index of the track currently being ripped, call IWMPPlaylist.getItemInfo with "CurrentRipTrackIndex" as the attribute name.</span></span>

## <a name="requirements"></a><span data-ttu-id="a1d7b-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="a1d7b-116">Requirements</span></span>



| <span data-ttu-id="a1d7b-117">需求</span><span class="sxs-lookup"><span data-stu-id="a1d7b-117">Requirement</span></span> | <span data-ttu-id="a1d7b-118">值</span><span class="sxs-lookup"><span data-stu-id="a1d7b-118">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a1d7b-119">版本</span><span class="sxs-lookup"><span data-stu-id="a1d7b-119">Version</span></span><br/>   | <span data-ttu-id="a1d7b-120">Windows Media Player 11。</span><span class="sxs-lookup"><span data-stu-id="a1d7b-120">Windows Media Player 11.</span></span><br/>                                                                                    |
| <span data-ttu-id="a1d7b-121">命名空間</span><span class="sxs-lookup"><span data-stu-id="a1d7b-121">Namespace</span></span><br/> | <span data-ttu-id="a1d7b-122">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="a1d7b-122">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="a1d7b-123">組件</span><span class="sxs-lookup"><span data-stu-id="a1d7b-123">Assembly</span></span><br/>  | <dl> <span data-ttu-id="a1d7b-124"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll) </dt></span><span class="sxs-lookup"><span data-stu-id="a1d7b-124"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a1d7b-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a1d7b-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a1d7b-126">**IWMPCdromRip 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="a1d7b-126">**IWMPCdromRip Interface (VB and C#)**</span></span>](iwmpcdromrip--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="a1d7b-127">**將 CD 翻錄**</span><span class="sxs-lookup"><span data-stu-id="a1d7b-127">**Ripping a CD**</span></span>](ripping-a-cd.md)
</dt> </dl>

 

 





