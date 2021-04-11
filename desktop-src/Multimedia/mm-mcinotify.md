---
title: 'MM_MCINOTIFY 訊息 (Mmsystem .h) '
description: MM \_ MCINOTIFY 訊息會通知應用程式，MCI 裝置已完成操作。 MCI 裝置只會在使用 MCI 通知旗標時傳送此訊息 \_ 。
ms.assetid: a0840130-2969-4ce5-b098-3e45401eebb1
keywords:
- MM_MCINOTIFY message Windows 多媒體
topic_type:
- apiref
api_name:
- MM_MCINOTIFY
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 96ee62c4a2b6e17bf5ad6d719dcb7d6e992a2f2e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104711"
---
# <a name="mm_mcinotify-message"></a><span data-ttu-id="316d2-105">MM \_ MCINOTIFY 訊息</span><span class="sxs-lookup"><span data-stu-id="316d2-105">MM\_MCINOTIFY message</span></span>

<span data-ttu-id="316d2-106">**MM \_ MCINOTIFY** 訊息會通知應用程式，MCI 裝置已完成操作。</span><span class="sxs-lookup"><span data-stu-id="316d2-106">The **MM\_MCINOTIFY** message notifies an application that an MCI device has completed an operation.</span></span> <span data-ttu-id="316d2-107">MCI 裝置只會在使用 MCI 通知旗標時傳送此訊息 \_ 。</span><span class="sxs-lookup"><span data-stu-id="316d2-107">MCI devices send this message only when the MCI\_NOTIFY flag is used.</span></span>


```C++
MM_MCINOTIFY 
wParam = (WPARAM) wFlags 
lParam = (LONG) lDevID
```



## <a name="parameters"></a><span data-ttu-id="316d2-108">參數</span><span class="sxs-lookup"><span data-stu-id="316d2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="316d2-109"><span id="wFlags"></span><span id="wflags"></span><span id="WFLAGS"></span>*wFlags*</span><span class="sxs-lookup"><span data-stu-id="316d2-109"><span id="wFlags"></span><span id="wflags"></span><span id="WFLAGS"></span>*wFlags*</span></span>
</dt> <dd>

<span data-ttu-id="316d2-110">通知的原因。</span><span class="sxs-lookup"><span data-stu-id="316d2-110">Reason for the notification.</span></span> <span data-ttu-id="316d2-111">系統會定義下列值：</span><span class="sxs-lookup"><span data-stu-id="316d2-111">The following values are defined:</span></span>



| <span data-ttu-id="316d2-112">需求</span><span class="sxs-lookup"><span data-stu-id="316d2-112">Requirement</span></span> | <span data-ttu-id="316d2-113">值</span><span class="sxs-lookup"><span data-stu-id="316d2-113">Value</span></span> |
|-------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="316d2-114">MCI \_ 通知已 \_ 中止</span><span class="sxs-lookup"><span data-stu-id="316d2-114">MCI\_NOTIFY\_ABORTED</span></span>    | <span data-ttu-id="316d2-115">裝置收到命令，導致無法符合目前的條件來起始回呼函式。</span><span class="sxs-lookup"><span data-stu-id="316d2-115">The device received a command that prevented the current conditions for initiating the callback function from being met.</span></span> <span data-ttu-id="316d2-116">如果新的命令中斷目前的命令，而且它也要求通知，則裝置只會傳送此訊息，而不會將 MCI \_ 通知 \_ 取代</span><span class="sxs-lookup"><span data-stu-id="316d2-116">If a new command interrupts the current command and it also requests notification, the device sends this message only and not MCI\_NOTIFY\_SUPERSEDED</span></span> |
| <span data-ttu-id="316d2-117">MCI \_ 通知 \_ 失敗</span><span class="sxs-lookup"><span data-stu-id="316d2-117">MCI\_NOTIFY\_FAILURE</span></span>    | <span data-ttu-id="316d2-118">裝置執行命令時發生裝置錯誤。</span><span class="sxs-lookup"><span data-stu-id="316d2-118">A device error occurred while the device was executing the command.</span></span>                                                                                                                                                                                                            |
| <span data-ttu-id="316d2-119">MCI \_ 通知 \_ 成功</span><span class="sxs-lookup"><span data-stu-id="316d2-119">MCI\_NOTIFY\_SUCCESSFUL</span></span> | <span data-ttu-id="316d2-120">已符合起始回呼函數的條件。</span><span class="sxs-lookup"><span data-stu-id="316d2-120">The conditions initiating the callback function have been met.</span></span>                                                                                                                                                                                                                 |
| <span data-ttu-id="316d2-121">已 \_ 取代 MCI 通知 \_</span><span class="sxs-lookup"><span data-stu-id="316d2-121">MCI\_NOTIFY\_SUPERSEDED</span></span> | <span data-ttu-id="316d2-122">裝置收到另一個命令，並已設定「通知」旗標，且目前已取代初始回呼函式的條件。</span><span class="sxs-lookup"><span data-stu-id="316d2-122">The device received another command with the "notify" flag set and the current conditions for initiating the callback function have been superseded.</span></span>                                                                                                                           |



 

</dd> <dt>

<span data-ttu-id="316d2-123"><span id="lDevID"></span><span id="ldevid"></span><span id="LDEVID"></span>*lDevID*</span><span class="sxs-lookup"><span data-stu-id="316d2-123"><span id="lDevID"></span><span id="ldevid"></span><span id="LDEVID"></span>*lDevID*</span></span>
</dt> <dd>

<span data-ttu-id="316d2-124">起始回呼函數的裝置識別碼。</span><span class="sxs-lookup"><span data-stu-id="316d2-124">Identifier of the device initiating the callback function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="316d2-125">傳回值</span><span class="sxs-lookup"><span data-stu-id="316d2-125">Return Value</span></span>

<span data-ttu-id="316d2-126">如果成功則傳回零，否則會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="316d2-126">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="316d2-127">備註</span><span class="sxs-lookup"><span data-stu-id="316d2-127">Remarks</span></span>

<span data-ttu-id="316d2-128">如需 MCI 通知旗標的詳細資訊 \_ ，請參閱 [通知旗](the-notify-flag.md)標。</span><span class="sxs-lookup"><span data-stu-id="316d2-128">For more information about the MCI\_NOTIFY flag, see [The Notify Flag](the-notify-flag.md).</span></span>

<span data-ttu-id="316d2-129">\_ \_ 當命令的動作完成時，裝置會以 **MM \_ MCINOTIFY** 傳回 MCI 通知成功旗標。</span><span class="sxs-lookup"><span data-stu-id="316d2-129">A device returns the MCI\_NOTIFY\_SUCCESSFUL flag with **MM\_MCINOTIFY** when the action for a command finishes.</span></span> <span data-ttu-id="316d2-130">例如，當裝置完成播放時，CD 音訊裝置會使用此旗標來取得 [**play**](play.md) ( [**MCI \_ play**](mci-play.md)) 命令的通知。</span><span class="sxs-lookup"><span data-stu-id="316d2-130">For example, a CD audio device uses this flag for notification for the [**play**](play.md) ( [**MCI\_PLAY**](mci-play.md)) command when the device finishes playing.</span></span> <span data-ttu-id="316d2-131">只有當 **播放** 命令到達指定的結束位置或到達媒體的結尾時，才會成功。</span><span class="sxs-lookup"><span data-stu-id="316d2-131">The **play** command is successful only when it reaches the specified end position or reaches the end of the media.</span></span> <span data-ttu-id="316d2-132">同樣地， [**搜尋**](seek.md) ( [**mci \_ 搜尋**](mci-seek.md)) 和 [**記錄**](record.md) ( [**mci \_ 記錄**](mci-record.md)) 命令不會讓 mci \_ 通知 \_ 成功，直到到達指定的結束位置或到達媒體的結尾為止。</span><span class="sxs-lookup"><span data-stu-id="316d2-132">Similarly, the [**seek**](seek.md) ( [**MCI\_SEEK**](mci-seek.md)) and [**record**](record.md) ( [**MCI\_RECORD**](mci-record.md)) commands do not return MCI\_NOTIFY\_SUCCESSFUL until they reach the specified end position or reach the end of the media.</span></span>

<span data-ttu-id="316d2-133">裝置 \_ \_ 只會在收到命令以防止通知條件出現時，才會以 **MM \_ MCINOTIFY** 傳回 MCI 通知已中止旗標。</span><span class="sxs-lookup"><span data-stu-id="316d2-133">A device returns the MCI\_NOTIFY\_ABORTED flag with **MM\_MCINOTIFY** only when it receives a command that prevents it from meeting the notification conditions.</span></span> <span data-ttu-id="316d2-134">例如， [**播放**](play.md) 命令不會中止先前 **播放** 命令的通知，前提是新的命令不會變更播放方向或變更結束位置。</span><span class="sxs-lookup"><span data-stu-id="316d2-134">For example, the [**play**](play.md) command would not abort notification for a previous **play** command provided that the new command does not change the play direction or change the ending position.</span></span> <span data-ttu-id="316d2-135">[**搜尋**](seek.md)和 [**記錄**](record.md)命令的行為類似。</span><span class="sxs-lookup"><span data-stu-id="316d2-135">The [**seek**](seek.md) and [**record**](record.md) commands behave similarly.</span></span> <span data-ttu-id="316d2-136">\_ \_ 當使用 [**pause**](pause.md) ( [**MCI \_ pause**](mci-pause.md)) 命令暫停播放或錄製時，mci 也不會傳送 mci 通知。</span><span class="sxs-lookup"><span data-stu-id="316d2-136">MCI also does not send MCI\_NOTIFY\_ABORTED when playback or recording is paused with the [**pause**](pause.md) ( [**MCI\_PAUSE**](mci-pause.md)) command.</span></span> <span data-ttu-id="316d2-137">傳送 [**resume**](resume.md) ( [**MCI \_ resume**](mci-resume.md)) 命令可讓它們繼續符合回呼條件。</span><span class="sxs-lookup"><span data-stu-id="316d2-137">Sending the [**resume**](resume.md) ( [**MCI\_RESUME**](mci-resume.md)) command allows them to continue to meet the callback conditions.</span></span>

<span data-ttu-id="316d2-138">當您的應用程式要求命令的通知時，請檢查 [**mciSendString**](/previous-versions//dd757161(v=vs.85)) 或 [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) 函數的錯誤傳回。</span><span class="sxs-lookup"><span data-stu-id="316d2-138">When your application requests notification for a command, check the error return of the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) or [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) functions.</span></span> <span data-ttu-id="316d2-139">如果這些函式遇到錯誤並傳回非零值，則 MCI 不會設定命令的通知。</span><span class="sxs-lookup"><span data-stu-id="316d2-139">If these functions encounter an error and return a nonzero value, MCI will not set notification for the command.</span></span>

## <a name="requirements"></a><span data-ttu-id="316d2-140">規格需求</span><span class="sxs-lookup"><span data-stu-id="316d2-140">Requirements</span></span>



| <span data-ttu-id="316d2-141">需求</span><span class="sxs-lookup"><span data-stu-id="316d2-141">Requirement</span></span> | <span data-ttu-id="316d2-142">值</span><span class="sxs-lookup"><span data-stu-id="316d2-142">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="316d2-143">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="316d2-143">Minimum supported client</span></span><br/> | <span data-ttu-id="316d2-144">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="316d2-144">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="316d2-145">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="316d2-145">Minimum supported server</span></span><br/> | <span data-ttu-id="316d2-146">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="316d2-146">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="316d2-147">標頭</span><span class="sxs-lookup"><span data-stu-id="316d2-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="316d2-148"><dt>Mmsystem (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="316d2-148"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="316d2-149">另請參閱</span><span class="sxs-lookup"><span data-stu-id="316d2-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="316d2-150">Mci</span><span class="sxs-lookup"><span data-stu-id="316d2-150">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="316d2-151">MCI 訊息</span><span class="sxs-lookup"><span data-stu-id="316d2-151">MCI Messages</span></span>](mci-messages.md)
</dt> <dt>

[<span data-ttu-id="316d2-152">**暫停**</span><span class="sxs-lookup"><span data-stu-id="316d2-152">**pause**</span></span>](pause.md)
</dt> <dt>

[<span data-ttu-id="316d2-153">**玩**</span><span class="sxs-lookup"><span data-stu-id="316d2-153">**play**</span></span>](play.md)
</dt> <dt>

[<span data-ttu-id="316d2-154">**記錄**</span><span class="sxs-lookup"><span data-stu-id="316d2-154">**record**</span></span>](record.md)
</dt> <dt>

[<span data-ttu-id="316d2-155">**恢復**</span><span class="sxs-lookup"><span data-stu-id="316d2-155">**resume**</span></span>](resume.md)
</dt> <dt>

[<span data-ttu-id="316d2-156">**尋求**</span><span class="sxs-lookup"><span data-stu-id="316d2-156">**seek**</span></span>](seek.md)
</dt> </dl>

 

