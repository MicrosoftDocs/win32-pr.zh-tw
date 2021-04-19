---
description: '\_線路裝置的狀態變更時，會傳送 TAPI 線路 LINEDEVSTATE 訊息。 應用程式可以叫用 lineGetLineDevStatus，以判斷該行的新狀態。'
ms.assetid: 15f616de-db47-4577-9a47-94f9292253dd
title: 'LINE_LINEDEVSTATE 訊息 (Tapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 079e4494b7eb2e1bfe46b5470138e4e9f44fbb0b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106981288"
---
# <a name="line_linedevstate-message"></a><span data-ttu-id="90615-104">行 \_ LINEDEVSTATE 訊息</span><span class="sxs-lookup"><span data-stu-id="90615-104">LINE\_LINEDEVSTATE message</span></span>

<span data-ttu-id="90615-105">線路裝置的狀態變更時，會傳送 TAPI **線路 \_ LINEDEVSTATE** 訊息。</span><span class="sxs-lookup"><span data-stu-id="90615-105">The TAPI **LINE\_LINEDEVSTATE** message is sent when the state of a line device has changed.</span></span> <span data-ttu-id="90615-106">應用程式可以叫用 [**lineGetLineDevStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetlinedevstatus) ，以判斷該行的新狀態。</span><span class="sxs-lookup"><span data-stu-id="90615-106">The application can invoke [**lineGetLineDevStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetlinedevstatus) to determine the new status of the line.</span></span>


```C++
            
```



## <a name="parameters"></a><span data-ttu-id="90615-107">參數</span><span class="sxs-lookup"><span data-stu-id="90615-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="90615-108">*hDevice*</span><span class="sxs-lookup"><span data-stu-id="90615-108">*hDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="90615-109">線路裝置的控制碼。</span><span class="sxs-lookup"><span data-stu-id="90615-109">A handle to the line device.</span></span> <span data-ttu-id="90615-110">當 *dwParam1* 為 LINEDEVSTATE 重新初始化時，此參數為 **Null** \_ 。</span><span class="sxs-lookup"><span data-stu-id="90615-110">This parameter is **NULL** when *dwParam1* is LINEDEVSTATE\_REINIT.</span></span>

</dd> <dt>

<span data-ttu-id="90615-111">*dwCallbackInstance*</span><span class="sxs-lookup"><span data-stu-id="90615-111">*dwCallbackInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="90615-112">開啟行時所提供的回呼實例。</span><span class="sxs-lookup"><span data-stu-id="90615-112">The callback instance supplied when opening the line.</span></span> <span data-ttu-id="90615-113">如果 *dwParam1* 參數為 LINEDEVSTATE \_ 重新初始化，則 *dwCallbackInstance* 參數無效，並設定為零。</span><span class="sxs-lookup"><span data-stu-id="90615-113">If the *dwParam1* parameter is LINEDEVSTATE\_REINIT, the *dwCallbackInstance* parameter is not valid and is set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="90615-114">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="90615-114">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="90615-115">已變更的行裝置狀態專案。</span><span class="sxs-lookup"><span data-stu-id="90615-115">The line device status item that has changed.</span></span> <span data-ttu-id="90615-116">參數可以是一或多個 [**LINEDEVSTATE \_ 常數**](linedevstate--constants.md)。</span><span class="sxs-lookup"><span data-stu-id="90615-116">The parameter can be one or more of the [**LINEDEVSTATE\_ constants**](linedevstate--constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="90615-117">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="90615-117">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="90615-118">此參數的解讀取決於 *dwParam1* 的值。</span><span class="sxs-lookup"><span data-stu-id="90615-118">The interpretation of this parameter depends on the value of *dwParam1*.</span></span> <span data-ttu-id="90615-119">如果 *dwParam1* 是 LINEDEVSTATE \_ 響鈴，則 *dwParam2* 會包含環形模式，而參數會使用它來指示線路響鈴。</span><span class="sxs-lookup"><span data-stu-id="90615-119">If *dwParam1* is LINEDEVSTATE\_RINGING, *dwParam2* contains the ring mode with which the switch instructs the line to ring.</span></span> <span data-ttu-id="90615-120">有效的環形模式是在一到 **dwNumRingModes** 範圍內的數位，其中 **dwNumRingModes** 是行裝置功能。</span><span class="sxs-lookup"><span data-stu-id="90615-120">Valid ring modes are numbers in the range one to **dwNumRingModes**, where **dwNumRingModes** is a line device capability.</span></span>

<span data-ttu-id="90615-121">如果 *dwParam1* 是 LINEDEVSTATE \_ 重新初始化，而且由於將新的 API 訊息轉譯為重新初始化訊息而導致 TAPI 發出訊息，則 *dwParam2* 會包含原始訊息的 *dwMsg* 參數 (例如， [**line \_ CREATE**](line-create.md) 或 line \_ LINEDEVSTATE) 。</span><span class="sxs-lookup"><span data-stu-id="90615-121">If *dwParam1* is LINEDEVSTATE\_REINIT, and the message was issued by TAPI as a result of translation of a new API message into a REINIT message, then *dwParam2* contains the *dwMsg* parameter of the original message (for example, [**LINE\_CREATE**](line-create.md) or LINE\_LINEDEVSTATE).</span></span> <span data-ttu-id="90615-122">如果 *dwParam2* 為零，這表示重新初始化訊息是 "REAL" 重新初始化訊息，要求應用程式以最早的便利性呼叫 [**lineShutdown**](/windows/desktop/api/Tapi/nf-tapi-lineshutdown) 。</span><span class="sxs-lookup"><span data-stu-id="90615-122">If *dwParam2* is zero, this indicates that the REINIT message is a "real" REINIT message that requires the application to call [**lineShutdown**](/windows/desktop/api/Tapi/nf-tapi-lineshutdown) at its earliest convenience.</span></span>

</dd> <dt>

<span data-ttu-id="90615-123">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="90615-123">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="90615-124">此參數的解讀取決於 *dwParam1* 的值。</span><span class="sxs-lookup"><span data-stu-id="90615-124">The interpretation of this parameter depends on the value of *dwParam1*.</span></span> <span data-ttu-id="90615-125">如果 *dwParam1* 是 LINEDEVSTATE \_ 響鈴， *dwParam3* 就會包含此環形事件的響鈴計數。</span><span class="sxs-lookup"><span data-stu-id="90615-125">If *dwParam1* is LINEDEVSTATE\_RINGING, *dwParam3* contains the ring count for this ring event.</span></span> <span data-ttu-id="90615-126">響鈴計數從零開始。</span><span class="sxs-lookup"><span data-stu-id="90615-126">The ring count starts at zero.</span></span>

<span data-ttu-id="90615-127">如果 *dwParam1* 是 LINEDEVSTATE \_ 重新初始化，且訊息是由 TAPI 因為將新的 API 訊息轉譯為重新初始化訊息而發出，則 *dwParam3* 包含原始訊息的 *dwParam1* 參數 (例如，LINEDEVSTATE \_ TRANSLATECHANGE 或其他 LINEDEVSTATE \_ 值（如果 *dwParam2* 為 line \_ LINEDEVSTATE）或新的裝置識別碼（如果 *dwParam2* 是行 [**\_ 建立**](line-create.md)) ）。</span><span class="sxs-lookup"><span data-stu-id="90615-127">If *dwParam1* is LINEDEVSTATE\_REINIT, and the message was issued by TAPI as a result of translation of a new API message into a REINIT message, then *dwParam3* contains the *dwParam1* parameter of the original message (for example, LINEDEVSTATE\_TRANSLATECHANGE or some other LINEDEVSTATE\_ value, if *dwParam2* is LINE\_LINEDEVSTATE, or the new device identifier, if *dwParam2* is [**LINE\_CREATE**](line-create.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="90615-128">傳回值</span><span class="sxs-lookup"><span data-stu-id="90615-128">Return value</span></span>

<span data-ttu-id="90615-129">沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="90615-129">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="90615-130">備註</span><span class="sxs-lookup"><span data-stu-id="90615-130">Remarks</span></span>

<span data-ttu-id="90615-131">您可以使用 [**lineSetStatusMessages**](/windows/desktop/api/Tapi/nf-tapi-linesetstatusmessages)來控制 **行 \_ LINEDEVSTATE** 訊息的傳送。</span><span class="sxs-lookup"><span data-stu-id="90615-131">The sending of the **LINE\_LINEDEVSTATE** message can be controlled with [**lineSetStatusMessages**](/windows/desktop/api/Tapi/nf-tapi-linesetstatusmessages).</span></span> <span data-ttu-id="90615-132">應用程式可以指出其想要收到通知的狀態專案變更。</span><span class="sxs-lookup"><span data-stu-id="90615-132">An application can indicate status item changes about which it wants to be notified.</span></span> <span data-ttu-id="90615-133">預設會停用所有狀態報表，但 \_ 不能停用 LINEDEVSTATE 重新初始化。</span><span class="sxs-lookup"><span data-stu-id="90615-133">By default, all status reporting is disabled except for LINEDEVSTATE\_REINIT, which cannot be disabled.</span></span> <span data-ttu-id="90615-134">這則訊息會傳送至具有該行控制碼的所有應用程式，包括呼叫 [**lineOpen**](/windows/desktop/api/Tapi/nf-tapi-lineopen) 且 *dwPrivileges* 參數設定為 LINECALLPRIVILEGE \_ NONE、LINECALLPRIVILEGE \_ OWNER、LINECALLPRIVILEGE \_ MONITOR 或允許的組合。</span><span class="sxs-lookup"><span data-stu-id="90615-134">This message is sent to all applications that have a handle to the line, including those that called [**lineOpen**](/windows/desktop/api/Tapi/nf-tapi-lineopen) with the *dwPrivileges* parameter set to LINECALLPRIVILEGE\_NONE, LINECALLPRIVILEGE\_OWNER, LINECALLPRIVILEGE\_MONITOR, or permitted combinations of these.</span></span>

## <a name="requirements"></a><span data-ttu-id="90615-135">規格需求</span><span class="sxs-lookup"><span data-stu-id="90615-135">Requirements</span></span>



| <span data-ttu-id="90615-136">需求</span><span class="sxs-lookup"><span data-stu-id="90615-136">Requirement</span></span> | <span data-ttu-id="90615-137">值</span><span class="sxs-lookup"><span data-stu-id="90615-137">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="90615-138">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="90615-138">TAPI version</span></span><br/> | <span data-ttu-id="90615-139">需要 TAPI 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="90615-139">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="90615-140">標頭</span><span class="sxs-lookup"><span data-stu-id="90615-140">Header</span></span><br/>       | <dl> <span data-ttu-id="90615-141"><dt>Tapi</dt></span><span class="sxs-lookup"><span data-stu-id="90615-141"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="90615-142">另請參閱</span><span class="sxs-lookup"><span data-stu-id="90615-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="90615-143">**行 \_ 關閉**</span><span class="sxs-lookup"><span data-stu-id="90615-143">**LINE\_CLOSE**</span></span>](line-close.md)
</dt> <dt>

[<span data-ttu-id="90615-144">**行 \_ 建立**</span><span class="sxs-lookup"><span data-stu-id="90615-144">**LINE\_CREATE**</span></span>](line-create.md)
</dt> <dt>

[<span data-ttu-id="90615-145">**LINEDEVCAPS**</span><span class="sxs-lookup"><span data-stu-id="90615-145">**LINEDEVCAPS**</span></span>](/windows/desktop/api/Tapi/ns-tapi-linedevcaps)
</dt> <dt>

[<span data-ttu-id="90615-146">**lineGetDevCaps**</span><span class="sxs-lookup"><span data-stu-id="90615-146">**lineGetDevCaps**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetdevcaps)
</dt> <dt>

[<span data-ttu-id="90615-147">**lineGetDevConfig**</span><span class="sxs-lookup"><span data-stu-id="90615-147">**lineGetDevConfig**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetdevconfig)
</dt> <dt>

[<span data-ttu-id="90615-148">**lineGetTranslateCaps**</span><span class="sxs-lookup"><span data-stu-id="90615-148">**lineGetTranslateCaps**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegettranslatecaps)
</dt> <dt>

[<span data-ttu-id="90615-149">**lineInitialize**</span><span class="sxs-lookup"><span data-stu-id="90615-149">**lineInitialize**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineinitialize)
</dt> <dt>

[<span data-ttu-id="90615-150">**lineOpen**</span><span class="sxs-lookup"><span data-stu-id="90615-150">**lineOpen**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineopen)
</dt> <dt>

[<span data-ttu-id="90615-151">**lineSetStatusMessages**</span><span class="sxs-lookup"><span data-stu-id="90615-151">**lineSetStatusMessages**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linesetstatusmessages)
</dt> <dt>

[<span data-ttu-id="90615-152">**lineShutdown**</span><span class="sxs-lookup"><span data-stu-id="90615-152">**lineShutdown**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineshutdown)
</dt> <dt>

[<span data-ttu-id="90615-153">**LINETRANSLATECAPS**</span><span class="sxs-lookup"><span data-stu-id="90615-153">**LINETRANSLATECAPS**</span></span>](/windows/desktop/api/Tapi/ns-tapi-linetranslatecaps)
</dt> <dt>

[<span data-ttu-id="90615-154">**lineUncompleteCall**</span><span class="sxs-lookup"><span data-stu-id="90615-154">**lineUncompleteCall**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineuncompletecall)
</dt> </dl>

 

 




