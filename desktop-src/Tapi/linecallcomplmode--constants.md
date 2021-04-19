---
description: LINECALLCOMPLMODE \_ 位旗標常數描述呼叫可以完成的不同方式。
ms.assetid: 68f755a1-586b-4c5b-b8e8-c8b40eb71685
title: 'LINECALLCOMPLMODE_ 的常數 (Tapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 373a66b6ce13b7bfba00303bea824f542bf0016a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106998787"
---
# <a name="linecallcomplmode_-constants"></a><span data-ttu-id="7372a-103">LINECALLCOMPLMODE \_ 常數</span><span class="sxs-lookup"><span data-stu-id="7372a-103">LINECALLCOMPLMODE\_ Constants</span></span>

<span data-ttu-id="7372a-104">**LINECALLCOMPLMODE \_** 位旗標常數描述呼叫可以完成的不同方式。</span><span class="sxs-lookup"><span data-stu-id="7372a-104">The **LINECALLCOMPLMODE\_** bit-flag constants describe different ways in which a call can be completed.</span></span>

<dl> <dt>

<span data-ttu-id="7372a-105"><span id="LINECALLCOMPLMODE_CALLBACK"></span><span id="linecallcomplmode_callback"></span>**LINECALLCOMPLMODE \_ 回呼**</span><span class="sxs-lookup"><span data-stu-id="7372a-105"><span id="LINECALLCOMPLMODE_CALLBACK"></span><span id="linecallcomplmode_callback"></span>**LINECALLCOMPLMODE\_CALLBACK**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7372a-106">要求被呼叫的工作站傳回閒置時的呼叫。</span><span class="sxs-lookup"><span data-stu-id="7372a-106">Requests the called station to return the call when it returns to idle.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7372a-107"><span id="LINECALLCOMPLMODE_CAMPON"></span><span id="linecallcomplmode_campon"></span>**LINECALLCOMPLMODE \_ CAMPON**</span><span class="sxs-lookup"><span data-stu-id="7372a-107"><span id="LINECALLCOMPLMODE_CAMPON"></span><span id="linecallcomplmode_campon"></span>**LINECALLCOMPLMODE\_CAMPON**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7372a-108">將呼叫排在佇列中，直到呼叫可以完成為止。</span><span class="sxs-lookup"><span data-stu-id="7372a-108">Queues the call until the call can be completed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7372a-109"><span id="LINECALLCOMPLMODE_INTRUDE"></span><span id="linecallcomplmode_intrude"></span>**LINECALLCOMPLMODE \_ INTRUDE**</span><span class="sxs-lookup"><span data-stu-id="7372a-109"><span id="LINECALLCOMPLMODE_INTRUDE"></span><span id="linecallcomplmode_intrude"></span>**LINECALLCOMPLMODE\_INTRUDE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7372a-110">將應用程式新增至) 中被呼叫的工作站 (barge 的現有呼叫。</span><span class="sxs-lookup"><span data-stu-id="7372a-110">Adds the application to the existing call at the called station (barge in).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7372a-111"><span id="LINECALLCOMPLMODE_MESSAGE"></span><span id="linecallcomplmode_message"></span>**LINECALLCOMPLMODE \_ 訊息**</span><span class="sxs-lookup"><span data-stu-id="7372a-111"><span id="LINECALLCOMPLMODE_MESSAGE"></span><span id="linecallcomplmode_message"></span>**LINECALLCOMPLMODE\_MESSAGE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7372a-112">留下一小段預先定義的訊息給被呼叫的工作站 (讓 Word 呼叫) 。</span><span class="sxs-lookup"><span data-stu-id="7372a-112">Leaves a short predefined message for the called station (Leave Word Calling).</span></span> <span data-ttu-id="7372a-113">要傳送的訊息會分開指定。</span><span class="sxs-lookup"><span data-stu-id="7372a-113">The message to be sent is specified separately.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7372a-114">備註</span><span class="sxs-lookup"><span data-stu-id="7372a-114">Remarks</span></span>

<span data-ttu-id="7372a-115">無延伸。</span><span class="sxs-lookup"><span data-stu-id="7372a-115">No extensibility.</span></span> <span data-ttu-id="7372a-116">所有32位都是保留的。</span><span class="sxs-lookup"><span data-stu-id="7372a-116">All 32 bits are reserved.</span></span>

## <a name="requirements"></a><span data-ttu-id="7372a-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="7372a-117">Requirements</span></span>



| <span data-ttu-id="7372a-118">需求</span><span class="sxs-lookup"><span data-stu-id="7372a-118">Requirement</span></span> | <span data-ttu-id="7372a-119">值</span><span class="sxs-lookup"><span data-stu-id="7372a-119">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="7372a-120">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="7372a-120">TAPI version</span></span><br/> | <span data-ttu-id="7372a-121">需要 TAPI 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="7372a-121">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="7372a-122">標頭</span><span class="sxs-lookup"><span data-stu-id="7372a-122">Header</span></span><br/>       | <dl> <span data-ttu-id="7372a-123"><dt>Tapi</dt></span><span class="sxs-lookup"><span data-stu-id="7372a-123"><dt>Tapi.h</dt></span></span> </dl> |



 

 




