---
description: '\_當電話裝置的狀態變更時，TAPI 會將電話狀態訊息傳送至應用程式。'
ms.assetid: 74e74b62-8387-4056-83e6-2350b3da4077
title: 'PHONE_STATE 訊息 (Tapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5db52f16d6c377087fd6ccadc5e70b5bb2865da2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106985732"
---
# <a name="phone_state-message"></a><span data-ttu-id="e23bb-103">電話 \_ 狀態訊息</span><span class="sxs-lookup"><span data-stu-id="e23bb-103">PHONE\_STATE message</span></span>

<span data-ttu-id="e23bb-104">當電話裝置的狀態變更時，TAPI 會將 **電話 \_ 狀態** 消息傳送至應用程式。</span><span class="sxs-lookup"><span data-stu-id="e23bb-104">TAPI sends the **PHONE\_STATE** message to an application whenever the status of a phone device changes.</span></span>


```C++
            
```



## <a name="parameters"></a><span data-ttu-id="e23bb-105">參數</span><span class="sxs-lookup"><span data-stu-id="e23bb-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e23bb-106">*hPhone*</span><span class="sxs-lookup"><span data-stu-id="e23bb-106">*hPhone*</span></span> 
</dt> <dd>

<span data-ttu-id="e23bb-107">手機裝置的控制碼。</span><span class="sxs-lookup"><span data-stu-id="e23bb-107">A handle to the phone device.</span></span>

</dd> <dt>

<span data-ttu-id="e23bb-108">*dwCallbackInstance*</span><span class="sxs-lookup"><span data-stu-id="e23bb-108">*dwCallbackInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="e23bb-109">開啟手機裝置時提供的應用程式回呼實例。</span><span class="sxs-lookup"><span data-stu-id="e23bb-109">The application's callback instance provided when opening the phone device.</span></span>

</dd> <dt>

<span data-ttu-id="e23bb-110">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="e23bb-110">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="e23bb-111">已變更的電話狀態。</span><span class="sxs-lookup"><span data-stu-id="e23bb-111">The phone state that has changed.</span></span> <span data-ttu-id="e23bb-112">此參數會使用其中一個 [**PHONESTATE \_ 常數**](phonestate--constants.md)。</span><span class="sxs-lookup"><span data-stu-id="e23bb-112">This parameter uses one of the [**PHONESTATE\_ constants**](phonestate--constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="e23bb-113">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="e23bb-113">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="e23bb-114">詳細說明狀態變更的電話狀態相關資訊。</span><span class="sxs-lookup"><span data-stu-id="e23bb-114">Phone state-dependent information detailing the status change.</span></span> <span data-ttu-id="e23bb-115">如果在 *dwParam1* 中設定了多個旗標，則不會使用這個參數，因為多個狀態專案已變更。</span><span class="sxs-lookup"><span data-stu-id="e23bb-115">This parameter is not used if multiple flags are set in *dwParam1*, because multiple status items have changed.</span></span> <span data-ttu-id="e23bb-116">應用程式應該叫用 [**phoneGetStatus**](/windows/desktop/api/Tapi/nf-tapi-phonegetstatus) 來取得一組完整的資訊。</span><span class="sxs-lookup"><span data-stu-id="e23bb-116">The application should invoke [**phoneGetStatus**](/windows/desktop/api/Tapi/nf-tapi-phonegetstatus) to obtain a complete set of information.</span></span>

<span data-ttu-id="e23bb-117">如果 *dwParam1* 是 PHONESTATE \_ OWNER， *dwParam2* 就會包含新的擁有者數目。</span><span class="sxs-lookup"><span data-stu-id="e23bb-117">If *dwParam1* is PHONESTATE\_OWNER, *dwParam2* contains the new number of owners.</span></span>

<span data-ttu-id="e23bb-118">如果 *dwParam1* 是 PHONESTATE \_ 監視器， *dwParam2* 就會包含新的監視器數目。</span><span class="sxs-lookup"><span data-stu-id="e23bb-118">If *dwParam1* is PHONESTATE\_MONITORS, *dwParam2* contains the new number of monitors.</span></span>

<span data-ttu-id="e23bb-119">如果 *dwParam1* 為 PHONESTATE \_ 燈，則 *dwParam2* 包含已變更之燈泡的按鈕/燈泡識別碼。</span><span class="sxs-lookup"><span data-stu-id="e23bb-119">If *dwParam1* is PHONESTATE\_LAMP, *dwParam2* contains the button/lamp identifier of the lamp that has changed.</span></span>

<span data-ttu-id="e23bb-120">如果 *dwParam1* 是 PHONESTATE \_ RINGMODE， *dwParam2* 就會包含新的響鈴模式。</span><span class="sxs-lookup"><span data-stu-id="e23bb-120">If *dwParam1* is PHONESTATE\_RINGMODE, *dwParam2* contains the new ring mode.</span></span>

<span data-ttu-id="e23bb-121">如果 *dwParam1* 是 PHONESTATE \_ 的話筒、喇叭或耳機， *dwParam2* 就會包含該 hookswitch 裝置的新 hookswitch 模式。</span><span class="sxs-lookup"><span data-stu-id="e23bb-121">If *dwParam1* is PHONESTATE\_HANDSET, SPEAKER or HEADSET, *dwParam2* contains the new hookswitch mode of that hookswitch device.</span></span> <span data-ttu-id="e23bb-122">此參數會使用其中一個 [**PHONEHOOKSWITCHMODE \_ 常數**](phonehookswitchmode--constants.md)。</span><span class="sxs-lookup"><span data-stu-id="e23bb-122">This parameter uses one of the [**PHONEHOOKSWITCHMODE\_ constants**](phonehookswitchmode--constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="e23bb-123">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="e23bb-123">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="e23bb-124">未使用的。</span><span class="sxs-lookup"><span data-stu-id="e23bb-124">Unused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e23bb-125">傳回值</span><span class="sxs-lookup"><span data-stu-id="e23bb-125">Return value</span></span>

<span data-ttu-id="e23bb-126">沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="e23bb-126">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e23bb-127">備註</span><span class="sxs-lookup"><span data-stu-id="e23bb-127">Remarks</span></span>

<span data-ttu-id="e23bb-128">您可以使用 [**phoneSetStatusMessages**](/windows/desktop/api/Tapi/nf-tapi-phonesetstatusmessages)和 [**phoneGetStatusMessages**](/windows/desktop/api/Tapi/nf-tapi-phonegetstatusmessages)來控制和查詢傳送 **電話 \_ 狀態** 訊息至應用程式。</span><span class="sxs-lookup"><span data-stu-id="e23bb-128">Sending the **PHONE\_STATE** message to the application can be controlled and queried using [**phoneSetStatusMessages**](/windows/desktop/api/Tapi/nf-tapi-phonesetstatusmessages) and [**phoneGetStatusMessages**](/windows/desktop/api/Tapi/nf-tapi-phonegetstatusmessages).</span></span> <span data-ttu-id="e23bb-129">依預設，此訊息會針對所有狀態變更停用，但 PHONESTATE \_ 重新初始化除外，但無法停用。</span><span class="sxs-lookup"><span data-stu-id="e23bb-129">By default, this message is disabled for all state changes except for PHONESTATE\_REINIT, which cannot be disabled.</span></span> <span data-ttu-id="e23bb-130">此訊息會傳送至所有具有電話控制碼的應用程式，包括呼叫 [**phoneOpen**](/windows/desktop/api/Tapi/nf-tapi-phoneopen) 的應用程式，並將 *dwPrivileges* 參數設定為 PHONEPRIVILEGE \_ 擁有者或 PHONEPRIVILEGE \_ 監視器。</span><span class="sxs-lookup"><span data-stu-id="e23bb-130">This message is sent to all applications that have a handle to the phone, including those that called [**phoneOpen**](/windows/desktop/api/Tapi/nf-tapi-phoneopen) with the *dwPrivileges* parameter set to PHONEPRIVILEGE\_OWNER or PHONEPRIVILEGE\_MONITOR.</span></span>

<span data-ttu-id="e23bb-131">具有擁有者和/或監視器指示的 **電話 \_ 狀態** 消息，會傳送至已經有手機控制碼的應用程式。</span><span class="sxs-lookup"><span data-stu-id="e23bb-131">A **PHONE\_STATE** message with an Owners and/or Monitors indication is sent to applications that already have a handle for the phone.</span></span> <span data-ttu-id="e23bb-132">這可能是因為另一個應用程式使用 [**phoneOpen**](/windows/desktop/api/Tapi/nf-tapi-phoneopen)、 [**phoneClose**](/windows/desktop/api/Tapi/nf-tapi-phoneclose) 或 [**phoneShutdown**](/windows/desktop/api/Tapi/nf-tapi-phoneshutdown)來變更電話裝置的擁有權或 monitorship。</span><span class="sxs-lookup"><span data-stu-id="e23bb-132">This can be the result of another application changing ownership or monitorship of the phone device with [**phoneOpen**](/windows/desktop/api/Tapi/nf-tapi-phoneopen), [**phoneClose**](/windows/desktop/api/Tapi/nf-tapi-phoneclose) or [**phoneShutdown**](/windows/desktop/api/Tapi/nf-tapi-phoneshutdown).</span></span>

## <a name="requirements"></a><span data-ttu-id="e23bb-133">規格需求</span><span class="sxs-lookup"><span data-stu-id="e23bb-133">Requirements</span></span>



| <span data-ttu-id="e23bb-134">需求</span><span class="sxs-lookup"><span data-stu-id="e23bb-134">Requirement</span></span> | <span data-ttu-id="e23bb-135">值</span><span class="sxs-lookup"><span data-stu-id="e23bb-135">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="e23bb-136">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="e23bb-136">TAPI version</span></span><br/> | <span data-ttu-id="e23bb-137">需要 TAPI 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="e23bb-137">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="e23bb-138">標頭</span><span class="sxs-lookup"><span data-stu-id="e23bb-138">Header</span></span><br/>       | <dl> <span data-ttu-id="e23bb-139"><dt>Tapi</dt></span><span class="sxs-lookup"><span data-stu-id="e23bb-139"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e23bb-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e23bb-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e23bb-141">**電話 \_ 關閉**</span><span class="sxs-lookup"><span data-stu-id="e23bb-141">**PHONE\_CLOSE**</span></span>](phone-close.md)
</dt> <dt>

[<span data-ttu-id="e23bb-142">**PHONECAPS**</span><span class="sxs-lookup"><span data-stu-id="e23bb-142">**PHONECAPS**</span></span>](/windows/desktop/api/Tapi/ns-tapi-phonecaps)
</dt> <dt>

[<span data-ttu-id="e23bb-143">**phoneClose**</span><span class="sxs-lookup"><span data-stu-id="e23bb-143">**phoneClose**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phoneclose)
</dt> <dt>

[<span data-ttu-id="e23bb-144">**phoneGetDevCaps**</span><span class="sxs-lookup"><span data-stu-id="e23bb-144">**phoneGetDevCaps**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phonegetdevcaps)
</dt> <dt>

[<span data-ttu-id="e23bb-145">**phoneGetStatus**</span><span class="sxs-lookup"><span data-stu-id="e23bb-145">**phoneGetStatus**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phonegetstatus)
</dt> <dt>

[<span data-ttu-id="e23bb-146">**phoneGetStatusMessages**</span><span class="sxs-lookup"><span data-stu-id="e23bb-146">**phoneGetStatusMessages**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phonegetstatusmessages)
</dt> <dt>

[<span data-ttu-id="e23bb-147">**phoneInitialize**</span><span class="sxs-lookup"><span data-stu-id="e23bb-147">**phoneInitialize**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phoneinitialize)
</dt> <dt>

[<span data-ttu-id="e23bb-148">**phoneInitializeEx**</span><span class="sxs-lookup"><span data-stu-id="e23bb-148">**phoneInitializeEx**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phoneinitializeexa)
</dt> <dt>

[<span data-ttu-id="e23bb-149">**phoneOpen**</span><span class="sxs-lookup"><span data-stu-id="e23bb-149">**phoneOpen**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phoneopen)
</dt> <dt>

[<span data-ttu-id="e23bb-150">**phoneSetStatusMessages**</span><span class="sxs-lookup"><span data-stu-id="e23bb-150">**phoneSetStatusMessages**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phonesetstatusmessages)
</dt> <dt>

[<span data-ttu-id="e23bb-151">**phoneShutdown**</span><span class="sxs-lookup"><span data-stu-id="e23bb-151">**phoneShutdown**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phoneshutdown)
</dt> </dl>

 

 




