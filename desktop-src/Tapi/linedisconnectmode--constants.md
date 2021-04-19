---
description: LINEDISCONNECTMODE \_ 位旗標常數描述遠端中斷連接要求的不同原因。 在撥號狀態轉換為已中斷連線之後，中斷連線模式可作為應用程式的撥號狀態。
ms.assetid: 1b26f13c-b0bf-4d2c-8514-f0c376e36bcd
title: 'LINEDISCONNECTMODE_ 的常數 (Tapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c70ba70175685e2c264343f9345227ee64c206f4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990973"
---
# <a name="linedisconnectmode_-constants"></a><span data-ttu-id="522a1-104">LINEDISCONNECTMODE \_ 常數</span><span class="sxs-lookup"><span data-stu-id="522a1-104">LINEDISCONNECTMODE\_ Constants</span></span>

<span data-ttu-id="522a1-105">**LINEDISCONNECTMODE \_** 位旗標常數描述遠端中斷連接要求的不同原因。</span><span class="sxs-lookup"><span data-stu-id="522a1-105">The **LINEDISCONNECTMODE\_** bit-flag constants describe different reasons for a remote disconnect request.</span></span> <span data-ttu-id="522a1-106">在撥號狀態轉換為已中斷連線之後，中斷連線模式可作為應用程式的撥號狀態。</span><span class="sxs-lookup"><span data-stu-id="522a1-106">A disconnect mode is available as call status to the application after the call state transitions to disconnected.</span></span>

<dl> <dt>

<span data-ttu-id="522a1-107"><span id="LINEDISCONNECTMODE_BADADDRESS"></span><span id="linedisconnectmode_badaddress"></span>**LINEDISCONNECTMODE \_ BADADDRESS**</span><span class="sxs-lookup"><span data-stu-id="522a1-107"><span id="LINEDISCONNECTMODE_BADADDRESS"></span><span id="linedisconnectmode_badaddress"></span>**LINEDISCONNECTMODE\_BADADDRESS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="522a1-108">目的地位址無效。</span><span class="sxs-lookup"><span data-stu-id="522a1-108">The destination address is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="522a1-109"><span id="LINEDISCONNECTMODE_BLOCKED"></span><span id="linedisconnectmode_blocked"></span>**LINEDISCONNECTMODE 已 \_ 封鎖**</span><span class="sxs-lookup"><span data-stu-id="522a1-109"><span id="LINEDISCONNECTMODE_BLOCKED"></span><span id="linedisconnectmode_blocked"></span>**LINEDISCONNECTMODE\_BLOCKED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="522a1-110">無法連接呼叫，因為目的地位址未接受來自來源位址的呼叫。</span><span class="sxs-lookup"><span data-stu-id="522a1-110">The call could not be connected because calls from the origination address are not being accepted at the destination address.</span></span> <span data-ttu-id="522a1-111">這與 LINEDISCONNECTMODE 拒絕的不同之處在于 \_ ，封鎖是在網路中實 (被動拒絕) ，而拒絕是在目的地設備 (主動拒絕) 中執行。</span><span class="sxs-lookup"><span data-stu-id="522a1-111">This differs from LINEDISCONNECTMODE\_REJECT in that blocking is implemented in the network (a passive reject) while a rejection is implemented in the destination equipment (an active reject).</span></span> <span data-ttu-id="522a1-112">封鎖可能是因為來源位址的特定排除，或是目的地只接受一組選取的來源位址 (關閉的使用者群組) 的呼叫。</span><span class="sxs-lookup"><span data-stu-id="522a1-112">The blocking can be due to a specific exclusion of the origination address, or because the destination accepts calls from only a selected set of origination address (closed user group).</span></span> <span data-ttu-id="522a1-113"> (TAPI 2.0 版和更新版本) </span><span class="sxs-lookup"><span data-stu-id="522a1-113">(TAPI versions 2.0 and later)</span></span>

<span data-ttu-id="522a1-114">LINEDISCONNECTMODE \_ 封鎖適用于封鎖回應。</span><span class="sxs-lookup"><span data-stu-id="522a1-114">LINEDISCONNECTMODE\_BLOCKED is appropriate as a blocklisted response.</span></span> <span data-ttu-id="522a1-115">例如，數據機已收到答案、未偵測到回電超過6秒、無法連接定義的次數、判斷電話號碼不是有效的電話號碼，而且會發出 ' 封鎖 ' 回應。</span><span class="sxs-lookup"><span data-stu-id="522a1-115">For example, a modem has received an answer, gone more than six seconds without detecting Ringback, failed to connect a defined number of times, determines that the phone number is not valid to call, and issues a 'blocklisted' response.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="522a1-116"><span id="LINEDISCONNECTMODE_BUSY"></span><span id="linedisconnectmode_busy"></span>**LINEDISCONNECTMODE \_ 忙碌**</span><span class="sxs-lookup"><span data-stu-id="522a1-116"><span id="LINEDISCONNECTMODE_BUSY"></span><span id="linedisconnectmode_busy"></span>**LINEDISCONNECTMODE\_BUSY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="522a1-117">遠端使用者的工作站忙碌中。</span><span class="sxs-lookup"><span data-stu-id="522a1-117">The remote user's station is busy.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="522a1-118"><span id="LINEDISCONNECTMODE_CANCELLED"></span><span id="linedisconnectmode_cancelled"></span>**LINEDISCONNECTMODE 已 \_ 取消**</span><span class="sxs-lookup"><span data-stu-id="522a1-118"><span id="LINEDISCONNECTMODE_CANCELLED"></span><span id="linedisconnectmode_cancelled"></span>**LINEDISCONNECTMODE\_CANCELLED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="522a1-119">呼叫已取消。</span><span class="sxs-lookup"><span data-stu-id="522a1-119">The call was cancelled.</span></span> <span data-ttu-id="522a1-120"> (TAPI 2.0 版和更新版本) </span><span class="sxs-lookup"><span data-stu-id="522a1-120">(TAPI versions 2.0 and later)</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="522a1-121"><span id="LINEDISCONNECTMODE_CONGESTION"></span><span id="linedisconnectmode_congestion"></span>**LINEDISCONNECTMODE \_ 擁塞**</span><span class="sxs-lookup"><span data-stu-id="522a1-121"><span id="LINEDISCONNECTMODE_CONGESTION"></span><span id="linedisconnectmode_congestion"></span>**LINEDISCONNECTMODE\_CONGESTION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="522a1-122">網路擁塞。</span><span class="sxs-lookup"><span data-stu-id="522a1-122">The network is congested.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="522a1-123"><span id="LINEDISCONNECTMODE_DONOTDISTURB"></span><span id="linedisconnectmode_donotdisturb"></span>**LINEDISCONNECTMODE \_ DONOTDISTURB**</span><span class="sxs-lookup"><span data-stu-id="522a1-123"><span id="LINEDISCONNECTMODE_DONOTDISTURB"></span><span id="linedisconnectmode_donotdisturb"></span>**LINEDISCONNECTMODE\_DONOTDISTURB**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="522a1-124">因為目的地已叫用「請勿打擾」功能，所以無法連線。</span><span class="sxs-lookup"><span data-stu-id="522a1-124">The call could not be connected because the destination has invoked the Do Not Disturb feature.</span></span> <span data-ttu-id="522a1-125"> (TAPI 2.0 版和更新版本) </span><span class="sxs-lookup"><span data-stu-id="522a1-125">(TAPI versions 2.0 and later)</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="522a1-126"><span id="LINEDISCONNECTMODE_FORWARDED"></span><span id="linedisconnectmode_forwarded"></span>**LINEDISCONNECTMODE \_ 轉送**</span><span class="sxs-lookup"><span data-stu-id="522a1-126"><span id="LINEDISCONNECTMODE_FORWARDED"></span><span id="linedisconnectmode_forwarded"></span>**LINEDISCONNECTMODE\_FORWARDED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="522a1-127">呼叫是由參數轉寄。</span><span class="sxs-lookup"><span data-stu-id="522a1-127">The call was forwarded by the switch.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="522a1-128"><span id="LINEDISCONNECTMODE_INCOMPATIBLE"></span><span id="linedisconnectmode_incompatible"></span>**LINEDISCONNECTMODE \_ 不相容**</span><span class="sxs-lookup"><span data-stu-id="522a1-128"><span id="LINEDISCONNECTMODE_INCOMPATIBLE"></span><span id="linedisconnectmode_incompatible"></span>**LINEDISCONNECTMODE\_INCOMPATIBLE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="522a1-129">遠端使用者的工作站設備與要求的撥號類型不相容。</span><span class="sxs-lookup"><span data-stu-id="522a1-129">The remote user's station equipment is incompatible with the type of call requested.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="522a1-130"><span id="LINEDISCONNECTMODE_NOANSWER"></span><span id="linedisconnectmode_noanswer"></span>**LINEDISCONNECTMODE \_ NOANSWER**</span><span class="sxs-lookup"><span data-stu-id="522a1-130"><span id="LINEDISCONNECTMODE_NOANSWER"></span><span id="linedisconnectmode_noanswer"></span>**LINEDISCONNECTMODE\_NOANSWER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="522a1-131">遠端使用者的工作站沒有回應。</span><span class="sxs-lookup"><span data-stu-id="522a1-131">The remote user's station does not answer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="522a1-132"><span id="LINEDISCONNECTMODE_NODIALTONE"></span><span id="linedisconnectmode_nodialtone"></span>**LINEDISCONNECTMODE \_ NODIALTONE**</span><span class="sxs-lookup"><span data-stu-id="522a1-132"><span id="LINEDISCONNECTMODE_NODIALTONE"></span><span id="linedisconnectmode_nodialtone"></span>**LINEDISCONNECTMODE\_NODIALTONE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="522a1-133">在服務提供者定義的超時時間內偵測到撥號音，在撥號期間的某個時間點會出現一次， (例如在無限制的字串) 中的 "W"。</span><span class="sxs-lookup"><span data-stu-id="522a1-133">A dial tone was not detected within a service-provider defined timeout, at a point during dialing when one was expected (such as at a "W" in the dialable string).</span></span> <span data-ttu-id="522a1-134">如果沒有服務提供者定義的超時時間，或在 [**LINEDIALPARAMS**](/windows/desktop/api/Tapi/ns-tapi-linedialparams)結構的 **dwWaitForDialTone** 成員中未指定值，也可能會發生這種情況。</span><span class="sxs-lookup"><span data-stu-id="522a1-134">This can also occur without a service-provider-defined timeout period or without a value specified in the **dwWaitForDialTone** member of the [**LINEDIALPARAMS**](/windows/desktop/api/Tapi/ns-tapi-linedialparams) structure.</span></span> <span data-ttu-id="522a1-135"> (TAPI 1.4 版和更新版本) </span><span class="sxs-lookup"><span data-stu-id="522a1-135">(TAPI versions 1.4 and later)</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="522a1-136"><span id="LINEDISCONNECTMODE_NORMAL"></span><span id="linedisconnectmode_normal"></span>**LINEDISCONNECTMODE \_ 正常**</span><span class="sxs-lookup"><span data-stu-id="522a1-136"><span id="LINEDISCONNECTMODE_NORMAL"></span><span id="linedisconnectmode_normal"></span>**LINEDISCONNECTMODE\_NORMAL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="522a1-137">這是遠端方的一般中斷連接要求。</span><span class="sxs-lookup"><span data-stu-id="522a1-137">This is a normal disconnect request by the remote party.</span></span> <span data-ttu-id="522a1-138">呼叫已正常終止。</span><span class="sxs-lookup"><span data-stu-id="522a1-138">The call was terminated normally.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="522a1-139"><span id="LINEDISCONNECTMODE_NUMBERCHANGED"></span><span id="linedisconnectmode_numberchanged"></span>**LINEDISCONNECTMODE \_ NUMBERCHANGED**</span><span class="sxs-lookup"><span data-stu-id="522a1-139"><span id="LINEDISCONNECTMODE_NUMBERCHANGED"></span><span id="linedisconnectmode_numberchanged"></span>**LINEDISCONNECTMODE\_NUMBERCHANGED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="522a1-140">因為目的地號碼已變更，但未提供自動重新導向至新的數位，所以無法連接此呼叫。</span><span class="sxs-lookup"><span data-stu-id="522a1-140">The call could not be connected because the destination number has been changed, but automatic redirection to the new number is not provided.</span></span> <span data-ttu-id="522a1-141"> (TAPI 2.0 版和更新版本) </span><span class="sxs-lookup"><span data-stu-id="522a1-141">(TAPI versions 2.0 and later)</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="522a1-142"><span id="LINEDISCONNECTMODE_OUTOFORDER"></span><span id="linedisconnectmode_outoforder"></span>**LINEDISCONNECTMODE \_ OUTOFORDER**</span><span class="sxs-lookup"><span data-stu-id="522a1-142"><span id="LINEDISCONNECTMODE_OUTOFORDER"></span><span id="linedisconnectmode_outoforder"></span>**LINEDISCONNECTMODE\_OUTOFORDER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="522a1-143">無法連線或中斷連線，因為目的地裝置未按順序 (硬體故障) 。</span><span class="sxs-lookup"><span data-stu-id="522a1-143">The call could not be connected or was disconnected because the destination device is out of order (hardware failure).</span></span> <span data-ttu-id="522a1-144"> (TAPI 2.0 版和更新版本) </span><span class="sxs-lookup"><span data-stu-id="522a1-144">(TAPI versions 2.0 and later)</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="522a1-145"><span id="LINEDISCONNECTMODE_PICKUP"></span><span id="linedisconnectmode_pickup"></span>**LINEDISCONNECTMODE \_ 取貨**</span><span class="sxs-lookup"><span data-stu-id="522a1-145"><span id="LINEDISCONNECTMODE_PICKUP"></span><span id="linedisconnectmode_pickup"></span>**LINEDISCONNECTMODE\_PICKUP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="522a1-146">已從其他位置挑選呼叫。</span><span class="sxs-lookup"><span data-stu-id="522a1-146">The call was picked up from elsewhere.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="522a1-147"><span id="LINEDISCONNECTMODE_QOSUNAVAIL"></span><span id="linedisconnectmode_qosunavail"></span>**LINEDISCONNECTMODE \_ QOSUNAVAIL**</span><span class="sxs-lookup"><span data-stu-id="522a1-147"><span id="LINEDISCONNECTMODE_QOSUNAVAIL"></span><span id="linedisconnectmode_qosunavail"></span>**LINEDISCONNECTMODE\_QOSUNAVAIL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="522a1-148">無法連接或中斷連線，因為無法取得或維持最小服務品質。</span><span class="sxs-lookup"><span data-stu-id="522a1-148">The call could not be connected or was disconnected because the minimum quality of service could not be obtained or sustained.</span></span> <span data-ttu-id="522a1-149">這與 LINEDISCONNECTMODE \_ 不相容，因為缺少資源可能是目的地的暫時性狀況。</span><span class="sxs-lookup"><span data-stu-id="522a1-149">This differs from LINEDISCONNECTMODE\_INCOMPATIBLE in that the lack of resources may be a temporary condition at the destination.</span></span> <span data-ttu-id="522a1-150"> (TAPI 2.0 版和更新版本) </span><span class="sxs-lookup"><span data-stu-id="522a1-150">(TAPI versions 2.0 and later)</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="522a1-151"><span id="LINEDISCONNECTMODE_REJECT"></span><span id="linedisconnectmode_reject"></span>**LINEDISCONNECTMODE \_ 拒絕**</span><span class="sxs-lookup"><span data-stu-id="522a1-151"><span id="LINEDISCONNECTMODE_REJECT"></span><span id="linedisconnectmode_reject"></span>**LINEDISCONNECTMODE\_REJECT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="522a1-152">遠端使用者已拒絕呼叫。</span><span class="sxs-lookup"><span data-stu-id="522a1-152">The remote user has rejected the call.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="522a1-153"><span id="LINEDISCONNECTMODE_TEMPFAILURE"></span><span id="linedisconnectmode_tempfailure"></span>**LINEDISCONNECTMODE \_ TEMPFAILURE**</span><span class="sxs-lookup"><span data-stu-id="522a1-153"><span id="LINEDISCONNECTMODE_TEMPFAILURE"></span><span id="linedisconnectmode_tempfailure"></span>**LINEDISCONNECTMODE\_TEMPFAILURE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="522a1-154">因為網路發生暫時性失敗，所以無法連線或中斷連線的呼叫;呼叫可以稍後 rerun，且預期最終會完成。</span><span class="sxs-lookup"><span data-stu-id="522a1-154">The call could not be connected or was disconnected because of a temporary failure in the network; the call can be reattempted later and is expected to eventually complete.</span></span> <span data-ttu-id="522a1-155"> (TAPI 2.0 版和更新版本) </span><span class="sxs-lookup"><span data-stu-id="522a1-155">(TAPI versions 2.0 and later)</span></span>

<span data-ttu-id="522a1-156">LINEDISCONNECTMODE \_ TEMPFAILURE 適合作為延遲的回應。</span><span class="sxs-lookup"><span data-stu-id="522a1-156">LINEDISCONNECTMODE\_TEMPFAILURE is appropriate as a delayed response.</span></span> <span data-ttu-id="522a1-157">例如，在特定的時間週期內，數據機取得忙碌的信號或對等太多次，最後不應該再次呼叫該數位，直到定義的時間已過，併發出「延遲」的回應。</span><span class="sxs-lookup"><span data-stu-id="522a1-157">For example, a modem getting a busy signal or equivalent too many times in a particular time period concludes that the number should not be called again until a defined time has elapsed and issues a 'delayed' response.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="522a1-158"><span id="LINEDISCONNECTMODE_UNAVAIL"></span><span id="linedisconnectmode_unavail"></span>**LINEDISCONNECTMODE \_ UNAVAIL**</span><span class="sxs-lookup"><span data-stu-id="522a1-158"><span id="LINEDISCONNECTMODE_UNAVAIL"></span><span id="linedisconnectmode_unavail"></span>**LINEDISCONNECTMODE\_UNAVAIL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="522a1-159">中斷連線的原因無法使用，稍後將不會變成已知。</span><span class="sxs-lookup"><span data-stu-id="522a1-159">The reason for the disconnect is unavailable and will not become known later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="522a1-160"><span id="LINEDISCONNECTMODE_UNKNOWN"></span><span id="linedisconnectmode_unknown"></span>**LINEDISCONNECTMODE \_ 不明**</span><span class="sxs-lookup"><span data-stu-id="522a1-160"><span id="LINEDISCONNECTMODE_UNKNOWN"></span><span id="linedisconnectmode_unknown"></span>**LINEDISCONNECTMODE\_UNKNOWN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="522a1-161">中斷連線要求的原因不明，但稍後可能會變成已知。</span><span class="sxs-lookup"><span data-stu-id="522a1-161">The reason for the disconnect request is unknown but may become known later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="522a1-162"><span id="LINEDISCONNECTMODE_UNREACHABLE"></span><span id="linedisconnectmode_unreachable"></span>**LINEDISCONNECTMODE \_ 無法連線**</span><span class="sxs-lookup"><span data-stu-id="522a1-162"><span id="LINEDISCONNECTMODE_UNREACHABLE"></span><span id="linedisconnectmode_unreachable"></span>**LINEDISCONNECTMODE\_UNREACHABLE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="522a1-163">無法連線到遠端使用者。</span><span class="sxs-lookup"><span data-stu-id="522a1-163">The remote user could not be reached.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="522a1-164">備註</span><span class="sxs-lookup"><span data-stu-id="522a1-164">Remarks</span></span>

<span data-ttu-id="522a1-165">您可以為裝置專屬的延伸模組指派高序位16位。</span><span class="sxs-lookup"><span data-stu-id="522a1-165">The high-order 16 bits can be assigned for device-specific extensions.</span></span> <span data-ttu-id="522a1-166">低序位16位是保留的。</span><span class="sxs-lookup"><span data-stu-id="522a1-166">The low-order 16 bits are reserved.</span></span>

<span data-ttu-id="522a1-167">針對指定呼叫的遠端中斷連接要求會導致撥號狀態轉換為已中斷連線的狀態，並將 [**一行 \_ CALLSTATE**](line-callstate.md) 訊息傳送至應用程式。</span><span class="sxs-lookup"><span data-stu-id="522a1-167">A remote disconnect request for a given call results in the call state transitioning to the disconnected state and a [**LINE\_CALLSTATE**](line-callstate.md) message is sent to the application.</span></span> <span data-ttu-id="522a1-168">LINEDISCONNECTMODE \_ 資訊會提供遠端中斷連線要求的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="522a1-168">The LINEDISCONNECTMODE\_ information provides details about the remote disconnect request.</span></span> <span data-ttu-id="522a1-169">當呼叫處於中斷線上狀態時，就可以在呼叫的 [**LINECALLSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linecallstatus) 結構中使用它。</span><span class="sxs-lookup"><span data-stu-id="522a1-169">It is available in the call's [**LINECALLSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linecallstatus) structure when the call is in the disconnected state.</span></span> <span data-ttu-id="522a1-170">當通話處於這種狀態時，仍然可以使用應用程式來查詢呼叫的資訊和狀態。</span><span class="sxs-lookup"><span data-stu-id="522a1-170">While a call is in this state, the application is still allowed to query the call's information and status.</span></span> <span data-ttu-id="522a1-171">例如，在遠端中斷的情況下收到的使用者使用者資訊可供使用。</span><span class="sxs-lookup"><span data-stu-id="522a1-171">For example, user-user information that is received as part of the remote disconnect is available then.</span></span> <span data-ttu-id="522a1-172">應用程式可以藉由卸載呼叫來清除中斷連線的呼叫。</span><span class="sxs-lookup"><span data-stu-id="522a1-172">The application can clear a disconnected call by dropping the call.</span></span>

<span data-ttu-id="522a1-173">為了回溯相容性，服務提供者必須負責檢查該行上的已協商 API 版本，如果未在協商版本上支援，則不使用此 LINEDISCONNECTMODE \_ 值 (LINEDISCONNECTMODE \_ NORMAL 或 \_ UNKNOWN 可改為使用) 。</span><span class="sxs-lookup"><span data-stu-id="522a1-173">For backward compatibility, it is the responsibility of the service provider to examine the negotiated API version on the line, and to not use this LINEDISCONNECTMODE\_ value if it is not supported on the negotiated version (LINEDISCONNECTMODE\_NORMAL or \_UNKNOWN could be used instead).</span></span>

## <a name="requirements"></a><span data-ttu-id="522a1-174">規格需求</span><span class="sxs-lookup"><span data-stu-id="522a1-174">Requirements</span></span>



| <span data-ttu-id="522a1-175">需求</span><span class="sxs-lookup"><span data-stu-id="522a1-175">Requirement</span></span> | <span data-ttu-id="522a1-176">值</span><span class="sxs-lookup"><span data-stu-id="522a1-176">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="522a1-177">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="522a1-177">TAPI version</span></span><br/> | <span data-ttu-id="522a1-178">需要 TAPI 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="522a1-178">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="522a1-179">標頭</span><span class="sxs-lookup"><span data-stu-id="522a1-179">Header</span></span><br/>       | <dl> <span data-ttu-id="522a1-180"><dt>Tapi</dt></span><span class="sxs-lookup"><span data-stu-id="522a1-180"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="522a1-181">另請參閱</span><span class="sxs-lookup"><span data-stu-id="522a1-181">See also</span></span>

<dl> <dt>

[<span data-ttu-id="522a1-182">**行 \_ CALLSTATE**</span><span class="sxs-lookup"><span data-stu-id="522a1-182">**LINE\_CALLSTATE**</span></span>](line-callstate.md)
</dt> <dt>

[<span data-ttu-id="522a1-183">**LINECALLSTATUS**</span><span class="sxs-lookup"><span data-stu-id="522a1-183">**LINECALLSTATUS**</span></span>](/windows/desktop/api/Tapi/ns-tapi-linecallstatus)
</dt> <dt>

[<span data-ttu-id="522a1-184">**LINEDIALPARAMS**</span><span class="sxs-lookup"><span data-stu-id="522a1-184">**LINEDIALPARAMS**</span></span>](/windows/desktop/api/Tapi/ns-tapi-linedialparams)
</dt> </dl>

 

 




