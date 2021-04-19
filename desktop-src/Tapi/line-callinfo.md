---
description: '\_當指定之呼叫的相關呼叫資訊已變更時，就會傳送 TAPI 線路 CALLINFO 訊息。 應用程式可以叫用 lineGetCallInfo 來判斷目前的呼叫資訊。'
ms.assetid: eb882409-6842-434e-9f93-61cf0c11d1d0
title: 'LINE_CALLINFO 訊息 (Tapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6005ab5383816ead440f5a1a7d580bfaccb5c1f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995301"
---
# <a name="line_callinfo-message"></a><span data-ttu-id="fe98a-104">行 \_ CALLINFO 訊息</span><span class="sxs-lookup"><span data-stu-id="fe98a-104">LINE\_CALLINFO message</span></span>

<span data-ttu-id="fe98a-105">當指定之呼叫的相關呼叫資訊已變更時，就會傳送 TAPI **線路 \_ CALLINFO** 訊息。</span><span class="sxs-lookup"><span data-stu-id="fe98a-105">The TAPI **LINE\_CALLINFO** message is sent when the call information about the specified call has changed.</span></span> <span data-ttu-id="fe98a-106">應用程式可以叫用 [**lineGetCallInfo**](/windows/desktop/api/Tapi/nf-tapi-linegetcallinfo) 來判斷目前的呼叫資訊。</span><span class="sxs-lookup"><span data-stu-id="fe98a-106">The application can invoke [**lineGetCallInfo**](/windows/desktop/api/Tapi/nf-tapi-linegetcallinfo) to determine the current call information.</span></span>


```C++
            
```



## <a name="parameters"></a><span data-ttu-id="fe98a-107">參數</span><span class="sxs-lookup"><span data-stu-id="fe98a-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fe98a-108">*hDevice*</span><span class="sxs-lookup"><span data-stu-id="fe98a-108">*hDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="fe98a-109">呼叫的控制碼。</span><span class="sxs-lookup"><span data-stu-id="fe98a-109">A handle to the call.</span></span>

</dd> <dt>

<span data-ttu-id="fe98a-110">*dwCallbackInstance*</span><span class="sxs-lookup"><span data-stu-id="fe98a-110">*dwCallbackInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="fe98a-111">開啟呼叫的行時所提供的回呼實例。</span><span class="sxs-lookup"><span data-stu-id="fe98a-111">The callback instance supplied when opening the call's line.</span></span>

</dd> <dt>

<span data-ttu-id="fe98a-112">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="fe98a-112">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="fe98a-113">已變更的呼叫資訊專案。</span><span class="sxs-lookup"><span data-stu-id="fe98a-113">The call information item that has changed.</span></span> <span data-ttu-id="fe98a-114">可以是一或多個 [**LINECALLINFOSTATE \_ 常數**](linecallinfostate--constants.md)。</span><span class="sxs-lookup"><span data-stu-id="fe98a-114">Can be one or more of the [**LINECALLINFOSTATE\_ constants**](linecallinfostate--constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="fe98a-115">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="fe98a-115">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="fe98a-116">未使用的。</span><span class="sxs-lookup"><span data-stu-id="fe98a-116">Unused.</span></span>

</dd> <dt>

<span data-ttu-id="fe98a-117">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="fe98a-117">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="fe98a-118">未使用的。</span><span class="sxs-lookup"><span data-stu-id="fe98a-118">Unused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fe98a-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="fe98a-119">Return value</span></span>

<span data-ttu-id="fe98a-120">沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="fe98a-120">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="fe98a-121">備註</span><span class="sxs-lookup"><span data-stu-id="fe98a-121">Remarks</span></span>

<span data-ttu-id="fe98a-122">具有 *NumOwnersIncr*、 *NumOwnersDecr* 和/或 *NumMonitorsChanged* 指示的 **行 \_ CALLINFO** 訊息會傳送給已經有呼叫控制碼的應用程式。</span><span class="sxs-lookup"><span data-stu-id="fe98a-122">A **LINE\_CALLINFO** message with a *NumOwnersIncr*, *NumOwnersDecr*, and/or *NumMonitorsChanged* indication is sent to applications that already have a handle for the call.</span></span> <span data-ttu-id="fe98a-123">這可能是因為另一個應用程式將擁有權或 monitorship 變更為使用 [**lineOpen**](/windows/desktop/api/Tapi/nf-tapi-lineopen)、 [**lineClose**](/windows/desktop/api/Tapi/nf-tapi-lineclose)、 [**lineShutdown**](/windows/desktop/api/Tapi/nf-tapi-lineshutdown)、 [**lineSetCallPrivilege**](/windows/desktop/api/Tapi/nf-tapi-linesetcallprivilege)、 [**lineGetNewCalls**](/windows/desktop/api/Tapi/nf-tapi-linegetnewcalls)和 [**lineGetConfRelatedCalls**](/windows/desktop/api/Tapi/nf-tapi-linegetconfrelatedcalls)的呼叫所造成。</span><span class="sxs-lookup"><span data-stu-id="fe98a-123">This can be the result of another application changing ownership or monitorship to a call with [**lineOpen**](/windows/desktop/api/Tapi/nf-tapi-lineopen), [**lineClose**](/windows/desktop/api/Tapi/nf-tapi-lineclose), [**lineShutdown**](/windows/desktop/api/Tapi/nf-tapi-lineshutdown), [**lineSetCallPrivilege**](/windows/desktop/api/Tapi/nf-tapi-linesetcallprivilege), [**lineGetNewCalls**](/windows/desktop/api/Tapi/nf-tapi-linegetnewcalls), and [**lineGetConfRelatedCalls**](/windows/desktop/api/Tapi/nf-tapi-linegetconfrelatedcalls).</span></span>

<span data-ttu-id="fe98a-124">在 [**行 \_ CALLSTATE**](line-callstate.md)訊息中提供新呼叫的通知時，不會傳送這些 **行 \_ CALLINFO** 訊息，因為呼叫資訊已在 \_ 傳送 CALLSTATE 訊息行時反映正確的擁有者和監視器數目。</span><span class="sxs-lookup"><span data-stu-id="fe98a-124">These **LINE\_CALLINFO** messages are not sent when a notification of a new call is provided in a [**LINE\_CALLSTATE**](line-callstate.md) message, because the call information already reflects the correct number of owners and monitors at the time the LINE\_CALLSTATE messages are sent.</span></span> <span data-ttu-id="fe98a-125">**行 \_** 透過 LINECALLSTATE 的未知機制，透過 TAPI 提供的呼叫來監視，也會抑制 CALLINFO 訊息 \_ 。</span><span class="sxs-lookup"><span data-stu-id="fe98a-125">**LINE\_CALLINFO** messages are also suppressed in the case where a call is offered by TAPI to monitors through the LINECALLSTATE\_UNKNOWN mechanism.</span></span>

> [!Note]  
> <span data-ttu-id="fe98a-126">導致擁有者或監視器數目變更的應用程式 (例如，藉由叫用 [**lineDeallocateCall**](/windows/desktop/api/Tapi/nf-tapi-linedeallocatecall) 或 [**LineSetCallPrivilege**](/windows/desktop/api/Tapi/nf-tapi-linesetcallprivilege)) 不會收到訊息，指出已完成變更。</span><span class="sxs-lookup"><span data-stu-id="fe98a-126">The application that causes a change in the number of owners or monitors (for example, by invoking [**lineDeallocateCall**](/windows/desktop/api/Tapi/nf-tapi-linedeallocatecall) or [**lineSetCallPrivilege**](/windows/desktop/api/Tapi/nf-tapi-linesetcallprivilege)) does not itself receive a message indicating that the change has been done.</span></span>

 

<span data-ttu-id="fe98a-127">呼叫進入 *閒置* 狀態之後，就不會傳送呼叫的 **行 \_ CALLINFO** 訊息。</span><span class="sxs-lookup"><span data-stu-id="fe98a-127">No **LINE\_CALLINFO** messages are sent for a call after the call has entered the *idle* state.</span></span> <span data-ttu-id="fe98a-128">具體而言，擁有者和監視數目的變更並不會回報，因為應用程式會解除配置其閒置呼叫的控制碼。</span><span class="sxs-lookup"><span data-stu-id="fe98a-128">Specifically, changes in the number of owners and monitors are not reported as applications deallocate their handles for the idle call.</span></span>

## <a name="requirements"></a><span data-ttu-id="fe98a-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="fe98a-129">Requirements</span></span>



| <span data-ttu-id="fe98a-130">需求</span><span class="sxs-lookup"><span data-stu-id="fe98a-130">Requirement</span></span> | <span data-ttu-id="fe98a-131">值</span><span class="sxs-lookup"><span data-stu-id="fe98a-131">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="fe98a-132">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="fe98a-132">TAPI version</span></span><br/> | <span data-ttu-id="fe98a-133">需要 TAPI 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="fe98a-133">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="fe98a-134">標頭</span><span class="sxs-lookup"><span data-stu-id="fe98a-134">Header</span></span><br/>       | <dl> <span data-ttu-id="fe98a-135"><dt>Tapi</dt></span><span class="sxs-lookup"><span data-stu-id="fe98a-135"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fe98a-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fe98a-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fe98a-137">**lineClose**</span><span class="sxs-lookup"><span data-stu-id="fe98a-137">**lineClose**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineclose)
</dt> <dt>

[<span data-ttu-id="fe98a-138">**lineDeallocateCall**</span><span class="sxs-lookup"><span data-stu-id="fe98a-138">**lineDeallocateCall**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linedeallocatecall)
</dt> <dt>

[<span data-ttu-id="fe98a-139">**lineGetCallInfo**</span><span class="sxs-lookup"><span data-stu-id="fe98a-139">**lineGetCallInfo**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetcallinfo)
</dt> <dt>

[<span data-ttu-id="fe98a-140">**lineGetConfRelatedCalls**</span><span class="sxs-lookup"><span data-stu-id="fe98a-140">**lineGetConfRelatedCalls**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetconfrelatedcalls)
</dt> <dt>

[<span data-ttu-id="fe98a-141">**lineGetNewCalls**</span><span class="sxs-lookup"><span data-stu-id="fe98a-141">**lineGetNewCalls**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetnewcalls)
</dt> <dt>

[<span data-ttu-id="fe98a-142">**lineOpen**</span><span class="sxs-lookup"><span data-stu-id="fe98a-142">**lineOpen**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineopen)
</dt> <dt>

[<span data-ttu-id="fe98a-143">**lineSetCallPrivilege**</span><span class="sxs-lookup"><span data-stu-id="fe98a-143">**lineSetCallPrivilege**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linesetcallprivilege)
</dt> <dt>

[<span data-ttu-id="fe98a-144">**lineShutdown**</span><span class="sxs-lookup"><span data-stu-id="fe98a-144">**lineShutdown**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineshutdown)
</dt> </dl>

 

 




