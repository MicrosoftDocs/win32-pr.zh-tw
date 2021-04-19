---
description: LINECALLPRIVILEGE \_ 位旗標常數描述具有呼叫控制碼的應用程式可能需要對應的呼叫之存取權限或許可權的種類。
ms.assetid: a58b7e9e-696e-4421-9b31-1ba8afe6e03b
title: 'LINECALLPRIVILEGE_ 的常數 (Tapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac2569ec255d2da3ad384292eb87afaa285f54b5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106991011"
---
# <a name="linecallprivilege_-constants"></a><span data-ttu-id="51bf5-103">LINECALLPRIVILEGE \_ 常數</span><span class="sxs-lookup"><span data-stu-id="51bf5-103">LINECALLPRIVILEGE\_ Constants</span></span>

<span data-ttu-id="51bf5-104">**LINECALLPRIVILEGE \_** 位旗標常數描述具有呼叫控制碼的應用程式可能需要對應的呼叫之存取權限或許可權的種類。</span><span class="sxs-lookup"><span data-stu-id="51bf5-104">The **LINECALLPRIVILEGE\_** bit-flag constants describe the kinds of access rights or privileges an application with a call handle may have to the corresponding call.</span></span>

<dl> <dt>

<span data-ttu-id="51bf5-105"><span id="LINECALLPRIVILEGE_MONITOR"></span><span id="linecallprivilege_monitor"></span>**LINECALLPRIVILEGE \_ 監視**</span><span class="sxs-lookup"><span data-stu-id="51bf5-105"><span id="LINECALLPRIVILEGE_MONITOR"></span><span id="linecallprivilege_monitor"></span>**LINECALLPRIVILEGE\_MONITOR**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="51bf5-106">應用程式具有呼叫的監視器許可權。</span><span class="sxs-lookup"><span data-stu-id="51bf5-106">The application has monitor privileges to the call.</span></span> <span data-ttu-id="51bf5-107">這些許可權可讓應用程式監視狀態變更，以及查詢有關呼叫的資訊和狀態。</span><span class="sxs-lookup"><span data-stu-id="51bf5-107">These privileges allow the application to monitor state changes and query information and status about the call.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="51bf5-108"><span id="LINECALLPRIVILEGE_NONE"></span><span id="linecallprivilege_none"></span>**LINECALLPRIVILEGE \_ 無**</span><span class="sxs-lookup"><span data-stu-id="51bf5-108"><span id="LINECALLPRIVILEGE_NONE"></span><span id="linecallprivilege_none"></span>**LINECALLPRIVILEGE\_NONE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="51bf5-109">應用程式沒有呼叫的許可權。</span><span class="sxs-lookup"><span data-stu-id="51bf5-109">The application has no privileges to the call.</span></span> <span data-ttu-id="51bf5-110">應用程式的控制碼是 void，不應該使用。</span><span class="sxs-lookup"><span data-stu-id="51bf5-110">The application's handle is void and should not be used.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="51bf5-111"><span id="LINECALLPRIVILEGE_OWNER"></span><span id="linecallprivilege_owner"></span>**LINECALLPRIVILEGE \_ 擁有者**</span><span class="sxs-lookup"><span data-stu-id="51bf5-111"><span id="LINECALLPRIVILEGE_OWNER"></span><span id="linecallprivilege_owner"></span>**LINECALLPRIVILEGE\_OWNER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="51bf5-112">應用程式具有呼叫的擁有者許可權。</span><span class="sxs-lookup"><span data-stu-id="51bf5-112">The application has owner privileges to the call.</span></span> <span data-ttu-id="51bf5-113">這些許可權可讓應用程式以影響撥號狀態的方式來操作呼叫。</span><span class="sxs-lookup"><span data-stu-id="51bf5-113">These privileges allow the application to manipulate the call in ways that affect the state of the call.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="51bf5-114">備註</span><span class="sxs-lookup"><span data-stu-id="51bf5-114">Remarks</span></span>

<span data-ttu-id="51bf5-115">無延伸。</span><span class="sxs-lookup"><span data-stu-id="51bf5-115">No extensibility.</span></span> <span data-ttu-id="51bf5-116">所有32位都是保留的。</span><span class="sxs-lookup"><span data-stu-id="51bf5-116">All 32 bits are reserved.</span></span>

<span data-ttu-id="51bf5-117">第一次提供呼叫控制碼給應用程式，或每當該應用程式的呼叫許可權遭到修改時，就會將 [**行 \_ CALLSTATE**](line-callstate.md) 訊息傳送至應用程式。</span><span class="sxs-lookup"><span data-stu-id="51bf5-117">When a call handle is first provided to an application or whenever call privileges of that application are modified, the [**LINE\_CALLSTATE**](line-callstate.md) message is sent to the application.</span></span> <span data-ttu-id="51bf5-118">當應用程式進行呼叫時，如果接收應用程式還沒有具有擁有者許可權的控制碼，則此訊息會通知應用程式其對呼叫的新許可權。</span><span class="sxs-lookup"><span data-stu-id="51bf5-118">When an application hands off a call, and if the receiving application does not already have a handle with owner privileges, then this message informs the application about its new privileges to the call.</span></span>

## <a name="requirements"></a><span data-ttu-id="51bf5-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="51bf5-119">Requirements</span></span>



| <span data-ttu-id="51bf5-120">需求</span><span class="sxs-lookup"><span data-stu-id="51bf5-120">Requirement</span></span> | <span data-ttu-id="51bf5-121">值</span><span class="sxs-lookup"><span data-stu-id="51bf5-121">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="51bf5-122">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="51bf5-122">TAPI version</span></span><br/> | <span data-ttu-id="51bf5-123">需要 TAPI 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="51bf5-123">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="51bf5-124">標頭</span><span class="sxs-lookup"><span data-stu-id="51bf5-124">Header</span></span><br/>       | <dl> <span data-ttu-id="51bf5-125"><dt>Tapi</dt></span><span class="sxs-lookup"><span data-stu-id="51bf5-125"><dt>Tapi.h</dt></span></span> </dl> |



 

 




