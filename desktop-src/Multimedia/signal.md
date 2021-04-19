---
title: 信號命令
description: 信號命令會將 MCISIGNAL 訊息傳送給應用程式，以識別工作區中的指定位置 \_ 。 數位影片裝置辨識此命令。 MCIAVI 一次只支援一個作用中的信號。
ms.assetid: 3d10eac0-fd1a-41ee-98fa-2518642c7339
keywords:
- 發出命令 Windows 多媒體
topic_type:
- apiref
api_name:
- signal
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4fd96b8970ebbb6502306c6d2d5fd8c49f172cad
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106979682"
---
# <a name="signal-command"></a><span data-ttu-id="7ad10-106">信號命令</span><span class="sxs-lookup"><span data-stu-id="7ad10-106">signal command</span></span>

<span data-ttu-id="7ad10-107">信號命令會將 [ \_ MCISIGNAL](mm-mcisignal.md) 訊息傳送給應用程式，以識別工作區中的指定位置。</span><span class="sxs-lookup"><span data-stu-id="7ad10-107">The signal command identifies a specified position in the workspace by sending the application an [MM\_MCISIGNAL](mm-mcisignal.md) message.</span></span> <span data-ttu-id="7ad10-108">數位影片裝置辨識此命令。</span><span class="sxs-lookup"><span data-stu-id="7ad10-108">Digital-video devices recognize this command.</span></span> <span data-ttu-id="7ad10-109">MCIAVI 一次只支援一個作用中的信號。</span><span class="sxs-lookup"><span data-stu-id="7ad10-109">MCIAVI supports only one active signal at a time.</span></span>

<span data-ttu-id="7ad10-110">若要傳送此命令，請使用 *lpszCommand* 參數設定來呼叫 [**mciSendString**](/previous-versions//dd757161(v=vs.85))函式，如下所示。</span><span class="sxs-lookup"><span data-stu-id="7ad10-110">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("signal %s %s %s"), 
  lpszDeviceID, 
  lpszSignalFlags, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="7ad10-111">參數</span><span class="sxs-lookup"><span data-stu-id="7ad10-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7ad10-112"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span><span class="sxs-lookup"><span data-stu-id="7ad10-112"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="7ad10-113">MCI 裝置的識別碼。</span><span class="sxs-lookup"><span data-stu-id="7ad10-113">Identifier of an MCI device.</span></span> <span data-ttu-id="7ad10-114">開啟裝置時，會指派此識別碼或別名。</span><span class="sxs-lookup"><span data-stu-id="7ad10-114">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="7ad10-115"><span id="lpszSignalFlags"></span><span id="lpszsignalflags"></span><span id="LPSZSIGNALFLAGS"></span>*lpszSignalFlags*</span><span class="sxs-lookup"><span data-stu-id="7ad10-115"><span id="lpszSignalFlags"></span><span id="lpszsignalflags"></span><span id="LPSZSIGNALFLAGS"></span>*lpszSignalFlags*</span></span>
</dt> <dd>

<span data-ttu-id="7ad10-116">下列其中一個旗標。</span><span class="sxs-lookup"><span data-stu-id="7ad10-116">One of the following flags.</span></span>



| <span data-ttu-id="7ad10-117">值</span><span class="sxs-lookup"><span data-stu-id="7ad10-117">Value</span></span>            | <span data-ttu-id="7ad10-118">意義</span><span class="sxs-lookup"><span data-stu-id="7ad10-118">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7ad10-119">在位置</span><span class="sxs-lookup"><span data-stu-id="7ad10-119">at position</span></span>      | <span data-ttu-id="7ad10-120">指定要叫用信號的框架。</span><span class="sxs-lookup"><span data-stu-id="7ad10-120">Specifies the frame to invoke a signal.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="7ad10-121">cancel</span><span class="sxs-lookup"><span data-stu-id="7ad10-121">cancel</span></span>           | <span data-ttu-id="7ad10-122">移除工作區中的信號。</span><span class="sxs-lookup"><span data-stu-id="7ad10-122">Removes signals from the workspace.</span></span> <span data-ttu-id="7ad10-123">您可以使用 "uservalue" 旗標來指定個別信號。</span><span class="sxs-lookup"><span data-stu-id="7ad10-123">An individual signal is specified by using the "uservalue" flag.</span></span> <span data-ttu-id="7ad10-124">如果未使用 "cancel" 來指定 "uservalue" 旗標，則裝置會取消所有信號。</span><span class="sxs-lookup"><span data-stu-id="7ad10-124">If the "uservalue" flag is not specified by using "cancel", the device cancels all signals.</span></span> <span data-ttu-id="7ad10-125">「取消」旗標與「at」、「每個」和「傳回位置」旗標不相容。</span><span class="sxs-lookup"><span data-stu-id="7ad10-125">The "cancel" flag is incompatible with the "at", "every", and "return position" flags.</span></span>                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="7ad10-126">每個 *間隔*</span><span class="sxs-lookup"><span data-stu-id="7ad10-126">every *interval*</span></span> | <span data-ttu-id="7ad10-127">指定信號的期間。</span><span class="sxs-lookup"><span data-stu-id="7ad10-127">Specifies the period of the signals.</span></span> <span data-ttu-id="7ad10-128">*間隔* 值是以目前時間格式指定。如果搭配 "at"*位置* 使用，則會在工作區中放置信號，並在 *位置* 放置一個信號標記。</span><span class="sxs-lookup"><span data-stu-id="7ad10-128">The *interval* value is specified in the current time format.If used with "at" *position*, signals are placed throughout the workspace with one signal mark placed at *position*.</span></span><br/> <span data-ttu-id="7ad10-129">如果沒有 "at" 旗標，則會在工作區中放置信號，並在目前位置有一個信號。</span><span class="sxs-lookup"><span data-stu-id="7ad10-129">Without the "at" flag, signals are placed throughout the workspace with one signal at the current position.</span></span><br/> <span data-ttu-id="7ad10-130">如果省略此旗標，則只會標示 "at" 旗標所指定的位置。</span><span class="sxs-lookup"><span data-stu-id="7ad10-130">If this flag is omitted, only the position indicated by the "at" flag is marked.</span></span><br/> <span data-ttu-id="7ad10-131">如果 *間隔* 值小於裝置所支援的最小頻率，則會使用其最小值。</span><span class="sxs-lookup"><span data-stu-id="7ad10-131">If the *interval* value is less than the minimum frequency supported by a device, it will use its minimum value.</span></span><br/> |
| <span data-ttu-id="7ad10-132">傳回位置</span><span class="sxs-lookup"><span data-stu-id="7ad10-132">return position</span></span>  | <span data-ttu-id="7ad10-133">指出裝置應該傳送位置值，而不是傳送信號訊息中的 "uservalue" 識別碼。</span><span class="sxs-lookup"><span data-stu-id="7ad10-133">Indicates the device should send the position value instead of the "uservalue" identifier in the signaling message.</span></span> <span data-ttu-id="7ad10-134">"Uservalue" 識別碼仍然可以用來取消或重新定義信號標記。</span><span class="sxs-lookup"><span data-stu-id="7ad10-134">The "uservalue" identifier can still be used to cancel or to redefine the signal marks.</span></span>                                                                                                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="7ad10-135">uservalue *識別碼*</span><span class="sxs-lookup"><span data-stu-id="7ad10-135">uservalue *id*</span></span>   | <span data-ttu-id="7ad10-136">指定使用信號訊息回報的識別碼。</span><span class="sxs-lookup"><span data-stu-id="7ad10-136">Specifies an identifier that is reported back with the signaling message.</span></span> <span data-ttu-id="7ad10-137">此識別碼會作為可與其他 **信號** 命令搭配使用以參考此 **信號** 設定的識別碼。</span><span class="sxs-lookup"><span data-stu-id="7ad10-137">This identifier acts as an identifier that can be used with other **signal** commands to reference this **signal** setting.</span></span> <span data-ttu-id="7ad10-138">如果省略，預設值為零。</span><span class="sxs-lookup"><span data-stu-id="7ad10-138">If omitted, the default value is zero.</span></span>                                                                                                                                                                                                                                                                                                                                     |



 

</dd> <dt>

<span data-ttu-id="7ad10-139"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span><span class="sxs-lookup"><span data-stu-id="7ad10-139"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="7ad10-140">可以是「等候」、「通知」、「測試」或它們的組合。</span><span class="sxs-lookup"><span data-stu-id="7ad10-140">Can be "wait", "notify", "test", or a combination of these.</span></span> <span data-ttu-id="7ad10-141">如需這些旗標的詳細資訊，請參閱 [Wait、Notify 和 Test 旗標](the-wait-notify-and-test-flags.md)。</span><span class="sxs-lookup"><span data-stu-id="7ad10-141">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7ad10-142">傳回值</span><span class="sxs-lookup"><span data-stu-id="7ad10-142">Return Value</span></span>

<span data-ttu-id="7ad10-143">如果成功則傳回零，否則會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="7ad10-143">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="7ad10-144">備註</span><span class="sxs-lookup"><span data-stu-id="7ad10-144">Remarks</span></span>

<span data-ttu-id="7ad10-145">用於命令完成訊息通知的視窗控制碼也會用來發出信號。</span><span class="sxs-lookup"><span data-stu-id="7ad10-145">The window handle used for notification of command completion messages is also used for signaling.</span></span>

## <a name="requirements"></a><span data-ttu-id="7ad10-146">規格需求</span><span class="sxs-lookup"><span data-stu-id="7ad10-146">Requirements</span></span>



| <span data-ttu-id="7ad10-147">需求</span><span class="sxs-lookup"><span data-stu-id="7ad10-147">Requirement</span></span> | <span data-ttu-id="7ad10-148">值</span><span class="sxs-lookup"><span data-stu-id="7ad10-148">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="7ad10-149">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7ad10-149">Minimum supported client</span></span><br/> | <span data-ttu-id="7ad10-150">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7ad10-150">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="7ad10-151">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7ad10-151">Minimum supported server</span></span><br/> | <span data-ttu-id="7ad10-152">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7ad10-152">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="7ad10-153">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7ad10-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7ad10-154">Mci</span><span class="sxs-lookup"><span data-stu-id="7ad10-154">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="7ad10-155">MCI 命令字串</span><span class="sxs-lookup"><span data-stu-id="7ad10-155">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> <dt>

[<span data-ttu-id="7ad10-156">MM \_ MCISIGNAL</span><span class="sxs-lookup"><span data-stu-id="7ad10-156">MM\_MCISIGNAL</span></span>](mm-mcisignal.md)
</dt> </dl>

 

