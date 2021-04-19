---
description: LINEANSWERMODE \_ 位旗標常數描述如何藉由在同一行上接聽另一個供應專案呼叫，來影響線路裝置上現有的使用中呼叫。
ms.assetid: 35f63d92-970f-4fb8-aba9-179fc7de70f4
title: 'LINEANSWERMODE_ 的常數 (Tapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 658d5b1265d28f8cb719719e4303fde97d3fff3e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984439"
---
# <a name="lineanswermode_-constants"></a><span data-ttu-id="db9fd-103">LINEANSWERMODE \_ 常數</span><span class="sxs-lookup"><span data-stu-id="db9fd-103">LINEANSWERMODE\_ Constants</span></span>

<span data-ttu-id="db9fd-104">**LINEANSWERMODE \_** 位旗標常數描述如何藉由在同一行上接聽另一個供應專案呼叫，來影響線路裝置上現有的使用 *中呼叫。*</span><span class="sxs-lookup"><span data-stu-id="db9fd-104">The **LINEANSWERMODE\_** bit-flag constants describe how an existing active call on a line device is affected by answering another *offering* call on the same line.</span></span>

<dl> <dt>

<span data-ttu-id="db9fd-105"><span id="LINEANSWERMODE_DROP"></span><span id="lineanswermode_drop"></span>**LINEANSWERMODE \_ DROP**</span><span class="sxs-lookup"><span data-stu-id="db9fd-105"><span id="LINEANSWERMODE_DROP"></span><span id="lineanswermode_drop"></span>**LINEANSWERMODE\_DROP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="db9fd-106">將會自動卸載目前作用中的呼叫。</span><span class="sxs-lookup"><span data-stu-id="db9fd-106">The currently active call will automatically be dropped.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="db9fd-107"><span id="LINEANSWERMODE_HOLD"></span><span id="lineanswermode_hold"></span>**LINEANSWERMODE \_ 保存**</span><span class="sxs-lookup"><span data-stu-id="db9fd-107"><span id="LINEANSWERMODE_HOLD"></span><span id="lineanswermode_hold"></span>**LINEANSWERMODE\_HOLD**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="db9fd-108">目前作用中的呼叫會自動置於保留狀態。</span><span class="sxs-lookup"><span data-stu-id="db9fd-108">The currently active call will automatically be placed on hold.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="db9fd-109"><span id="LINEANSWERMODE_NONE"></span><span id="lineanswermode_none"></span>**LINEANSWERMODE \_ 無**</span><span class="sxs-lookup"><span data-stu-id="db9fd-109"><span id="LINEANSWERMODE_NONE"></span><span id="lineanswermode_none"></span>**LINEANSWERMODE\_NONE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="db9fd-110">在同一行上回答另一個呼叫不會影響該行上的現有使用中呼叫。</span><span class="sxs-lookup"><span data-stu-id="db9fd-110">Answering another call on the same line has no effect on the existing active call on the line.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="db9fd-111">備註</span><span class="sxs-lookup"><span data-stu-id="db9fd-111">Remarks</span></span>

<span data-ttu-id="db9fd-112">無延伸。</span><span class="sxs-lookup"><span data-stu-id="db9fd-112">No extensibility.</span></span> <span data-ttu-id="db9fd-113">所有32位都是保留的。</span><span class="sxs-lookup"><span data-stu-id="db9fd-113">All 32 bits are reserved.</span></span>

<span data-ttu-id="db9fd-114">如果 (提供的呼叫會在另一個呼叫已在使用中時) ，則會叫用 [**lineAnswer**](/windows/desktop/api/Tapi/nf-tapi-lineanswer)，將新的呼叫連接至。</span><span class="sxs-lookup"><span data-stu-id="db9fd-114">If a call comes in (is offered) at the time another call is already active, the new call is connected to by invoking [**lineAnswer**](/windows/desktop/api/Tapi/nf-tapi-lineanswer).</span></span> <span data-ttu-id="db9fd-115">對現有使用中的呼叫所造成的影響，取決於該行的裝置功能。</span><span class="sxs-lookup"><span data-stu-id="db9fd-115">The effect this has on the existing active call depends on the line's device capabilities.</span></span> <span data-ttu-id="db9fd-116">第一個呼叫可能不受影響，可能會自動卸載，或可能會自動放置。</span><span class="sxs-lookup"><span data-stu-id="db9fd-116">The first call may be unaffected, it may automatically be dropped, or it may automatically be placed on hold.</span></span>

## <a name="requirements"></a><span data-ttu-id="db9fd-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="db9fd-117">Requirements</span></span>



| <span data-ttu-id="db9fd-118">需求</span><span class="sxs-lookup"><span data-stu-id="db9fd-118">Requirement</span></span> | <span data-ttu-id="db9fd-119">值</span><span class="sxs-lookup"><span data-stu-id="db9fd-119">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="db9fd-120">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="db9fd-120">TAPI version</span></span><br/> | <span data-ttu-id="db9fd-121">需要 TAPI 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="db9fd-121">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="db9fd-122">標頭</span><span class="sxs-lookup"><span data-stu-id="db9fd-122">Header</span></span><br/>       | <dl> <span data-ttu-id="db9fd-123"><dt>Tapi</dt></span><span class="sxs-lookup"><span data-stu-id="db9fd-123"><dt>Tapi.h</dt></span></span> </dl> |



 

 




