---
description: LINEBUSYMODE \_ 位旗標常數描述交換器或網路可以產生的不同忙碌信號。 這些忙碌的信號通常表示進行呼叫所需的不同資源目前正在使用中。
ms.assetid: 4a3fa79f-7a7a-4f9b-9353-e6c5ca4fcb4e
title: 'LINEBUSYMODE_ 的常數 (Tapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c996ad4e6142cc8312983945ae4c716ee0b35ed
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999713"
---
# <a name="linebusymode_-constants"></a><span data-ttu-id="96376-104">LINEBUSYMODE \_ 常數</span><span class="sxs-lookup"><span data-stu-id="96376-104">LINEBUSYMODE\_ Constants</span></span>

<span data-ttu-id="96376-105">**LINEBUSYMODE \_** 位旗標常數描述交換器或網路可以產生的不同忙碌信號。</span><span class="sxs-lookup"><span data-stu-id="96376-105">The **LINEBUSYMODE\_** bit-flag constants describe different busy signals that the switch or network can generate.</span></span> <span data-ttu-id="96376-106">這些忙碌的信號通常表示進行呼叫所需的不同資源目前正在使用中。</span><span class="sxs-lookup"><span data-stu-id="96376-106">These busy signals typically indicate that a different resource that is required to make a call is currently in use.</span></span>

<dl> <dt>

<span data-ttu-id="96376-107"><span id="LINEBUSYMODE_STATION"></span><span id="linebusymode_station"></span>**LINEBUSYMODE \_ 站**</span><span class="sxs-lookup"><span data-stu-id="96376-107"><span id="LINEBUSYMODE_STATION"></span><span id="linebusymode_station"></span>**LINEBUSYMODE\_STATION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="96376-108">忙碌信號表示被呼叫的合作物件的工作站忙碌中。</span><span class="sxs-lookup"><span data-stu-id="96376-108">The busy signal indicates that the called party's station is busy.</span></span> <span data-ttu-id="96376-109">這通常會以 *正常* 忙碌的聲音來發出信號。</span><span class="sxs-lookup"><span data-stu-id="96376-109">This is usually signaled with a *normal* busy tone.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="96376-110"><span id="LINEBUSYMODE_TRUNK"></span><span id="linebusymode_trunk"></span>**LINEBUSYMODE \_ 主幹**</span><span class="sxs-lookup"><span data-stu-id="96376-110"><span id="LINEBUSYMODE_TRUNK"></span><span id="linebusymode_trunk"></span>**LINEBUSYMODE\_TRUNK**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="96376-111">忙碌信號表示主幹或電路忙碌中。</span><span class="sxs-lookup"><span data-stu-id="96376-111">The busy signal indicates that a trunk or circuit is busy.</span></span> <span data-ttu-id="96376-112">這通常會以 *快速* 忙碌的聲音來發出信號。</span><span class="sxs-lookup"><span data-stu-id="96376-112">This is usually signaled with a *fast* busy tone.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="96376-113"><span id="LINEBUSYMODE_UNKNOWN"></span><span id="linebusymode_unknown"></span>**LINEBUSYMODE \_ 不明**</span><span class="sxs-lookup"><span data-stu-id="96376-113"><span id="LINEBUSYMODE_UNKNOWN"></span><span id="linebusymode_unknown"></span>**LINEBUSYMODE\_UNKNOWN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="96376-114">忙碌信號的特定模式目前未知，但稍後可能會變成已知。</span><span class="sxs-lookup"><span data-stu-id="96376-114">The busy signal's specific mode is currently unknown but may become known later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="96376-115"><span id="LINEBUSYMODE_UNAVAIL"></span><span id="linebusymode_unavail"></span>**LINEBUSYMODE \_ UNAVAIL**</span><span class="sxs-lookup"><span data-stu-id="96376-115"><span id="LINEBUSYMODE_UNAVAIL"></span><span id="linebusymode_unavail"></span>**LINEBUSYMODE\_UNAVAIL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="96376-116">忙碌信號的特定模式無法使用，而且將不會變成已知。</span><span class="sxs-lookup"><span data-stu-id="96376-116">The busy signal's specific mode is unavailable and will not become known.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="96376-117">備註</span><span class="sxs-lookup"><span data-stu-id="96376-117">Remarks</span></span>

<span data-ttu-id="96376-118">您可以為裝置專屬的延伸模組指派高序位16位。</span><span class="sxs-lookup"><span data-stu-id="96376-118">The high-order 16 bits can be assigned for device-specific extensions.</span></span> <span data-ttu-id="96376-119">低序位16位是保留的。</span><span class="sxs-lookup"><span data-stu-id="96376-119">The low-order 16 bits are reserved.</span></span>

> [!Note]  
> <span data-ttu-id="96376-120">忙碌信號可能會以 inband 音或頻外訊息的形式傳送。</span><span class="sxs-lookup"><span data-stu-id="96376-120">Busy signals can be sent as inband tones or out-of-band messages.</span></span> <span data-ttu-id="96376-121">TAPI 不會假設特定的信號機制。</span><span class="sxs-lookup"><span data-stu-id="96376-121">TAPI makes no assumption about the specific signaling mechanism.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="96376-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="96376-122">Requirements</span></span>



| <span data-ttu-id="96376-123">需求</span><span class="sxs-lookup"><span data-stu-id="96376-123">Requirement</span></span> | <span data-ttu-id="96376-124">值</span><span class="sxs-lookup"><span data-stu-id="96376-124">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="96376-125">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="96376-125">TAPI version</span></span><br/> | <span data-ttu-id="96376-126">需要 TAPI 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="96376-126">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="96376-127">標頭</span><span class="sxs-lookup"><span data-stu-id="96376-127">Header</span></span><br/>       | <dl> <span data-ttu-id="96376-128"><dt>Tapi</dt></span><span class="sxs-lookup"><span data-stu-id="96376-128"><dt>Tapi.h</dt></span></span> </dl> |



 

 




