---
title: IWMPCdromBurn burnProgress 屬性
description: BurnProgress 屬性會取得完成百分比的 CD 燒錄進度。
ms.assetid: 831cc55d-bd26-4328-a715-1a1fa48d7a40
keywords:
- burnProgress 屬性 Windows Media Player
- burnProgress 屬性 Windows Media Player，IWMPCdromBurn 介面
- IWMPCdromBurn 介面 Windows Media Player，burnProgress 屬性
topic_type:
- apiref
api_name:
- IWMPCdromBurn.burnProgress
- IWMPCdromBurn.get_burnProgress
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 835c8c1091941437c226427ddb3ef53e8c577b5d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994763"
---
# <a name="iwmpcdromburnburnprogress-property"></a><span data-ttu-id="fe433-106">IWMPCdromBurn：： burnProgress 屬性</span><span class="sxs-lookup"><span data-stu-id="fe433-106">IWMPCdromBurn::burnProgress property</span></span>

<span data-ttu-id="fe433-107">**BurnProgress** 屬性會取得完成百分比的 CD 燒錄進度。</span><span class="sxs-lookup"><span data-stu-id="fe433-107">The **burnProgress** property gets the CD burning progress as percent complete.</span></span>

<span data-ttu-id="fe433-108">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="fe433-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="fe433-109">語法</span><span class="sxs-lookup"><span data-stu-id="fe433-109">Syntax</span></span>


```CSharp
public System.Int32 burnProgress {get;}
```


```VB

Public ReadOnly Property burnProgress As System.Int32
```





## <a name="property-value"></a><span data-ttu-id="fe433-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="fe433-110">Property value</span></span>

<span data-ttu-id="fe433-111">作為進度值的 **system.object** 。</span><span class="sxs-lookup"><span data-stu-id="fe433-111">A **System.Int32** that is the progress value.</span></span> <span data-ttu-id="fe433-112">進度值的範圍是從0到100。</span><span class="sxs-lookup"><span data-stu-id="fe433-112">Progress values range from 0 to 100.</span></span>

## <a name="remarks"></a><span data-ttu-id="fe433-113">備註</span><span class="sxs-lookup"><span data-stu-id="fe433-113">Remarks</span></span>

<span data-ttu-id="fe433-114">進度值代表整個燒錄流程的完成百分比，包括任何預備作業。</span><span class="sxs-lookup"><span data-stu-id="fe433-114">The progress value represents the completed percentage of the entire burning process, including any staging operations.</span></span>

## <a name="requirements"></a><span data-ttu-id="fe433-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="fe433-115">Requirements</span></span>



| <span data-ttu-id="fe433-116">需求</span><span class="sxs-lookup"><span data-stu-id="fe433-116">Requirement</span></span> | <span data-ttu-id="fe433-117">值</span><span class="sxs-lookup"><span data-stu-id="fe433-117">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fe433-118">版本</span><span class="sxs-lookup"><span data-stu-id="fe433-118">Version</span></span><br/>   | <span data-ttu-id="fe433-119">Windows Media Player 11</span><span class="sxs-lookup"><span data-stu-id="fe433-119">Windows Media Player 11</span></span><br/>                                                                                     |
| <span data-ttu-id="fe433-120">命名空間</span><span class="sxs-lookup"><span data-stu-id="fe433-120">Namespace</span></span><br/> | <span data-ttu-id="fe433-121">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="fe433-121">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="fe433-122">組件</span><span class="sxs-lookup"><span data-stu-id="fe433-122">Assembly</span></span><br/>  | <dl> <span data-ttu-id="fe433-123"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll) </dt></span><span class="sxs-lookup"><span data-stu-id="fe433-123"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fe433-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fe433-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fe433-125">**IWMPCdromBurn 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="fe433-125">**IWMPCdromBurn Interface (VB and C#)**</span></span>](iwmpcdromburn--vb-and-c.md)
</dt> </dl>

 

 





