---
description: LINECALLPARAMFLAGS \_ 常數描述有關呼叫的各種狀態旗標。
ms.assetid: f323ec9f-5bab-4b5d-93ef-8a552ee0d591
title: 'LINECALLPARAMFLAGS_ 的常數 (Tapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e70fe2721e6fce0ac509b50290b1ec3788f3c89
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106983963"
---
# <a name="linecallparamflags_-constants"></a><span data-ttu-id="c3817-103">LINECALLPARAMFLAGS \_ 常數</span><span class="sxs-lookup"><span data-stu-id="c3817-103">LINECALLPARAMFLAGS\_ Constants</span></span>

<span data-ttu-id="c3817-104">**LINECALLPARAMFLAGS \_** 常數描述有關呼叫的各種狀態旗標。</span><span class="sxs-lookup"><span data-stu-id="c3817-104">The **LINECALLPARAMFLAGS\_** constants describe various status flags about a call.</span></span>

<dl> <dt>

<span data-ttu-id="c3817-105"><span id="LINECALLPARAMFLAGS_BLOCKID"></span><span id="linecallparamflags_blockid"></span>**LINECALLPARAMFLAGS \_ 區塊識別碼**</span><span class="sxs-lookup"><span data-stu-id="c3817-105"><span id="LINECALLPARAMFLAGS_BLOCKID"></span><span id="linecallparamflags_blockid"></span>**LINECALLPARAMFLAGS\_BLOCKID**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="c3817-106">建立者身分識別應該隱藏 (區塊呼叫端識別碼) 。</span><span class="sxs-lookup"><span data-stu-id="c3817-106">The originator identity should be concealed (block caller ID).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c3817-107"><span id="LINECALLPARAMFLAGS_DESTOFFHOOK"></span><span id="linecallparamflags_destoffhook"></span>**LINECALLPARAMFLAGS \_ DESTOFFHOOK**</span><span class="sxs-lookup"><span data-stu-id="c3817-107"><span id="LINECALLPARAMFLAGS_DESTOFFHOOK"></span><span id="linecallparamflags_destoffhook"></span>**LINECALLPARAMFLAGS\_DESTOFFHOOK**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="c3817-108">呼叫方的電話應該會自動 offhook。</span><span class="sxs-lookup"><span data-stu-id="c3817-108">The called party's phone should be automatically taken offhook.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c3817-109"><span id="LINECALLPARAMFLAGS_IDLE"></span><span id="linecallparamflags_idle"></span>**LINECALLPARAMFLAGS \_ 閒置**</span><span class="sxs-lookup"><span data-stu-id="c3817-109"><span id="LINECALLPARAMFLAGS_IDLE"></span><span id="linecallparamflags_idle"></span>**LINECALLPARAMFLAGS\_IDLE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="c3817-110">呼叫應源自閒置通話的外觀，而不是聯結進行中的呼叫。</span><span class="sxs-lookup"><span data-stu-id="c3817-110">The call should be originated on an idle call appearance and not join a call in progress.</span></span> <span data-ttu-id="c3817-111">使用 [**lineMakeCall**](/windows/desktop/api/Tapi/nf-tapi-linemakecall) 函式時，如果 \_ 未設定 LINECALLPARAMFLAGS 閒置值，而且該行有現有的呼叫，則函式會在需要進行新的呼叫時，中斷至現有的呼叫。</span><span class="sxs-lookup"><span data-stu-id="c3817-111">When using the [**lineMakeCall**](/windows/desktop/api/Tapi/nf-tapi-linemakecall) function, if the LINECALLPARAMFLAGS\_IDLE value is not set and there is an existing call on the line, the function breaks into the existing call if necessary to make the new call.</span></span> <span data-ttu-id="c3817-112">如果沒有任何現有的呼叫，此函式會依指定進行新的呼叫。</span><span class="sxs-lookup"><span data-stu-id="c3817-112">If there is no existing call, the function makes the new call as specified.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c3817-113"><span id="LINECALLPARAMFLAGS_NOHOLDCONFERENCE"></span><span id="linecallparamflags_noholdconference"></span>**LINECALLPARAMFLAGS \_ NOHOLDCONFERENCE**</span><span class="sxs-lookup"><span data-stu-id="c3817-113"><span id="LINECALLPARAMFLAGS_NOHOLDCONFERENCE"></span><span id="linecallparamflags_noholdconference"></span>**LINECALLPARAMFLAGS\_NOHOLDCONFERENCE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="c3817-114">這個位只會搭配 [**lineSetupConference**](/windows/desktop/api/Tapi/nf-tapi-linesetupconference) 和 [**linePrepareAddToConference**](/windows/desktop/api/Tapi/nf-tapi-lineprepareaddtoconference)使用。</span><span class="sxs-lookup"><span data-stu-id="c3817-114">This bit is used only in conjunction with [**lineSetupConference**](/windows/desktop/api/Tapi/nf-tapi-linesetupconference) and [**linePrepareAddToConference**](/windows/desktop/api/Tapi/nf-tapi-lineprepareaddtoconference).</span></span> <span data-ttu-id="c3817-115">要使用目前的呼叫 conferenced 的位址，是在 [**LINECALLPARAMS**](/windows/desktop/api/Tapi/ns-tapi-linecallparams)的 **TargetAddress** 成員中指定。</span><span class="sxs-lookup"><span data-stu-id="c3817-115">The address to be conferenced with the current call is specified in the **TargetAddress** member in [**LINECALLPARAMS**](/windows/desktop/api/Tapi/ns-tapi-linecallparams).</span></span> <span data-ttu-id="c3817-116">諮詢電話不會實際從交換器中繪製撥號音，但會透過各種不同的通話建立狀態進行 (例如，撥接、繼續) 。</span><span class="sxs-lookup"><span data-stu-id="c3817-116">The consultation call does not physically draw dial tone from the switch, but will progress through various call establishment states (for example, dialing, proceeding).</span></span> <span data-ttu-id="c3817-117">當諮詢通話達到線上狀態時，就會自動建立會議;原先保持線上狀態的原始呼叫會進入 conferenced 狀態;諮詢通話進入 conferenced 狀態;hConfCall 會進入 [已連線] 狀態。</span><span class="sxs-lookup"><span data-stu-id="c3817-117">When the consultation call reaches the connected state, the conference is automatically established; the original call, which had remained in the connected state, enters the conferenced state; the consultation call enters the conferenced state; the hConfCall enters the connected state.</span></span> <span data-ttu-id="c3817-118">如果諮詢通話失敗 (進入已中斷連線的狀態，並在閒置) 之後進入閒置狀態，則 hConfCall 也會進入閒置狀態，而原始呼叫 (可能是現有的會議，在 **linePrepareAddToConference**) 會保持線上狀態。</span><span class="sxs-lookup"><span data-stu-id="c3817-118">If the consultation call fails (enters the disconnected state followed by idle), the hConfCall also enters the idle state, and the original call (which may have been an existing conference, in the case of **linePrepareAddToConference**) remains in the connected state.</span></span> <span data-ttu-id="c3817-119">原始的合作物件 (或合作物件) 不會察覺到通話是否已舉 servicerequeststatusenum.onhold。</span><span class="sxs-lookup"><span data-stu-id="c3817-119">The original party (or parties) never perceive the call has having gone onhold.</span></span> <span data-ttu-id="c3817-120">這項功能通常用來在需要監視與 irate 呼叫者的互動時，將監督員新增至 ACD 代理程式通話。</span><span class="sxs-lookup"><span data-stu-id="c3817-120">This feature is often used to add a supervisor to an ACD agent call when necessary to monitor interactions with an irate caller.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c3817-121"><span id="LINECALLPARAMFLAGS_ONESTEPTRANSFER"></span><span id="linecallparamflags_onesteptransfer"></span>**LINECALLPARAMFLAGS \_ ONESTEPTRANSFER**</span><span class="sxs-lookup"><span data-stu-id="c3817-121"><span id="LINECALLPARAMFLAGS_ONESTEPTRANSFER"></span><span id="linecallparamflags_onesteptransfer"></span>**LINECALLPARAMFLAGS\_ONESTEPTRANSFER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="c3817-122">這個位只會與 [**lineSetupTransfer**](/windows/desktop/api/Tapi/nf-tapi-linesetuptransfer)搭配使用。</span><span class="sxs-lookup"><span data-stu-id="c3817-122">This bit is used only in conjunction with [**lineSetupTransfer**](/windows/desktop/api/Tapi/nf-tapi-linesetuptransfer).</span></span> <span data-ttu-id="c3817-123">它結合了 **lineSetupTransfer** 的作業，後面接著 [**lineDial**](/windows/desktop/api/Tapi/nf-tapi-linedial) 的諮詢通話，成為單一步驟。</span><span class="sxs-lookup"><span data-stu-id="c3817-123">It combines the operation of **lineSetupTransfer** followed by [**lineDial**](/windows/desktop/api/Tapi/nf-tapi-linedial) on the consultation call into a single step.</span></span> <span data-ttu-id="c3817-124">要撥號的位址是在 [**LINECALLPARAMS**](/windows/desktop/api/Tapi/ns-tapi-linecallparams)的 **TargetAddress** 成員中指定。</span><span class="sxs-lookup"><span data-stu-id="c3817-124">The address to be dialed is specified in the **TargetAddress** member in [**LINECALLPARAMS**](/windows/desktop/api/Tapi/ns-tapi-linecallparams).</span></span> <span data-ttu-id="c3817-125">原始呼叫會處於 *onholdpendingtransfer* 狀態，就像是正常呼叫 **lineSetupTransfer** 一樣，並且會正常建立諮詢通話。</span><span class="sxs-lookup"><span data-stu-id="c3817-125">The original call is placed in *onholdpendingtransfer* state, just as if **lineSetupTransfer** were called normally, and the consultation call is established normally.</span></span> <span data-ttu-id="c3817-126">應用程式仍然必須呼叫 [**lineCompleteTransfer**](/windows/desktop/api/Tapi/nf-tapi-linecompletetransfer) 來影響傳送。</span><span class="sxs-lookup"><span data-stu-id="c3817-126">The application must still call [**lineCompleteTransfer**](/windows/desktop/api/Tapi/nf-tapi-linecompletetransfer) to effect the transfer.</span></span> <span data-ttu-id="c3817-127">這項功能通常是在透過協力廠商呼叫控制連結叫用來自伺服器的傳輸時使用，因為這類連結通常不支援一般的雙步驟程式。</span><span class="sxs-lookup"><span data-stu-id="c3817-127">This feature is often used when invoking a transfer from a server over a third-party call control link, because such links frequently do not support the normal two-step process.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c3817-128"><span id="LINECALLPARAMFLAGS_ORIGOFFHOOK"></span><span id="linecallparamflags_origoffhook"></span>**LINECALLPARAMFLAGS \_ ORIGOFFHOOK**</span><span class="sxs-lookup"><span data-stu-id="c3817-128"><span id="LINECALLPARAMFLAGS_ORIGOFFHOOK"></span><span id="linecallparamflags_origoffhook"></span>**LINECALLPARAMFLAGS\_ORIGOFFHOOK**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="c3817-129">建立者的電話應該會自動取得 offhook。</span><span class="sxs-lookup"><span data-stu-id="c3817-129">The originator's phone should be automatically taken offhook.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c3817-130"><span id="LINECALLPARAMFLAGS_PREDICTIVEDIAL"></span><span id="linecallparamflags_predictivedial"></span>**LINECALLPARAMFLAGS \_ PREDICTIVEDIAL**</span><span class="sxs-lookup"><span data-stu-id="c3817-130"><span id="LINECALLPARAMFLAGS_PREDICTIVEDIAL"></span><span id="linecallparamflags_predictivedial"></span>**LINECALLPARAMFLAGS\_PREDICTIVEDIAL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="c3817-131">只有在呼叫具有預測撥號功能的位址時，才會使用此位 (LINEADDRCAPFLAGS \_ PREDICTIVEDIALER 在 [**LINEADDRESSCAPS**](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps)) 的 **dwAddrCapFlags** 成員中。</span><span class="sxs-lookup"><span data-stu-id="c3817-131">This bit is used only when placing a call on an address with predictive dialing capability (LINEADDRCAPFLAGS\_PREDICTIVEDIALER is on in the **dwAddrCapFlags** member in [**LINEADDRESSCAPS**](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps)).</span></span> <span data-ttu-id="c3817-132">您必須開啟此位，才能啟用裝置的增強通話進度和/或媒體裝置監視功能。</span><span class="sxs-lookup"><span data-stu-id="c3817-132">The bit must be on to enable the enhanced call progress and/or media device monitoring capabilities of the device.</span></span> <span data-ttu-id="c3817-133">如果沒有開啟此位，則會在沒有增強通話進度或媒體類型監視的情況下進行呼叫，而且不會根據撥號狀態起始自動傳輸。</span><span class="sxs-lookup"><span data-stu-id="c3817-133">If this bit is not on, the call will be placed without enhanced call progress or media type monitoring, and no automatic transfer will be initiated based on call state.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c3817-134"><span id="LINECALLPARAMFLAGS_SECURE"></span><span id="linecallparamflags_secure"></span>**LINECALLPARAMFLAGS \_ 安全**</span><span class="sxs-lookup"><span data-stu-id="c3817-134"><span id="LINECALLPARAMFLAGS_SECURE"></span><span id="linecallparamflags_secure"></span>**LINECALLPARAMFLAGS\_SECURE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="c3817-135">呼叫應該設定為安全的。</span><span class="sxs-lookup"><span data-stu-id="c3817-135">The call should be set up as secure.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c3817-136">備註</span><span class="sxs-lookup"><span data-stu-id="c3817-136">Remarks</span></span>

<span data-ttu-id="c3817-137">無延伸。</span><span class="sxs-lookup"><span data-stu-id="c3817-137">No extensibility.</span></span> <span data-ttu-id="c3817-138">所有32位都是保留的。</span><span class="sxs-lookup"><span data-stu-id="c3817-138">All 32 bits are reserved.</span></span>

## <a name="requirements"></a><span data-ttu-id="c3817-139">規格需求</span><span class="sxs-lookup"><span data-stu-id="c3817-139">Requirements</span></span>



| <span data-ttu-id="c3817-140">需求</span><span class="sxs-lookup"><span data-stu-id="c3817-140">Requirement</span></span> | <span data-ttu-id="c3817-141">值</span><span class="sxs-lookup"><span data-stu-id="c3817-141">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="c3817-142">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="c3817-142">TAPI version</span></span><br/> | <span data-ttu-id="c3817-143">需要 TAPI 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="c3817-143">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="c3817-144">標頭</span><span class="sxs-lookup"><span data-stu-id="c3817-144">Header</span></span><br/>       | <dl> <span data-ttu-id="c3817-145"><dt>Tapi</dt></span><span class="sxs-lookup"><span data-stu-id="c3817-145"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c3817-146">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c3817-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c3817-147">**LINEADDRESSCAPS**</span><span class="sxs-lookup"><span data-stu-id="c3817-147">**LINEADDRESSCAPS**</span></span>](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps)
</dt> <dt>

[<span data-ttu-id="c3817-148">**LINECALLPARAMS**</span><span class="sxs-lookup"><span data-stu-id="c3817-148">**LINECALLPARAMS**</span></span>](/windows/desktop/api/Tapi/ns-tapi-linecallparams)
</dt> <dt>

[<span data-ttu-id="c3817-149">**lineCompleteTransfer**</span><span class="sxs-lookup"><span data-stu-id="c3817-149">**lineCompleteTransfer**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linecompletetransfer)
</dt> <dt>

[<span data-ttu-id="c3817-150">**lineDial**</span><span class="sxs-lookup"><span data-stu-id="c3817-150">**lineDial**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linedial)
</dt> <dt>

[<span data-ttu-id="c3817-151">**lineMakeCall**</span><span class="sxs-lookup"><span data-stu-id="c3817-151">**lineMakeCall**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linemakecall)
</dt> <dt>

[<span data-ttu-id="c3817-152">**linePrepareAddToConference**</span><span class="sxs-lookup"><span data-stu-id="c3817-152">**linePrepareAddToConference**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineprepareaddtoconference)
</dt> <dt>

[<span data-ttu-id="c3817-153">**lineSetupConference**</span><span class="sxs-lookup"><span data-stu-id="c3817-153">**lineSetupConference**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linesetupconference)
</dt> <dt>

[<span data-ttu-id="c3817-154">**lineSetupTransfer**</span><span class="sxs-lookup"><span data-stu-id="c3817-154">**lineSetupTransfer**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linesetuptransfer)
</dt> </dl>

 

 




