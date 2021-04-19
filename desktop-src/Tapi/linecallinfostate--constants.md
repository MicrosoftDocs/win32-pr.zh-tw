---
description: LINECALLINFOSTATE \_ 位旗標常數描述可在行 CALLINFO 訊息中通知哪些應用程式的各種呼叫資訊專案 \_ 。
ms.assetid: c216d9b7-8e2f-4604-ba93-1d9e1a5d23fc
title: 'LINECALLINFOSTATE_ 的常數 (Tapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9f560cfd6ba65929a9f6cf5c9aa6cd8bc2f48b24
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106998377"
---
# <a name="linecallinfostate_-constants"></a><span data-ttu-id="5df7b-103">LINECALLINFOSTATE \_ 常數</span><span class="sxs-lookup"><span data-stu-id="5df7b-103">LINECALLINFOSTATE\_ Constants</span></span>

<span data-ttu-id="5df7b-104">**LINECALLINFOSTATE \_** 位旗標常數描述可在 [**行 \_ CALLINFO**](line-callinfo.md)訊息中通知哪些應用程式的各種呼叫資訊專案。</span><span class="sxs-lookup"><span data-stu-id="5df7b-104">The **LINECALLINFOSTATE\_** bit-flag constants describe various call information items about which an application can be notified in the [**LINE\_CALLINFO**](line-callinfo.md) message.</span></span>

<dl> <dt>

<span data-ttu-id="5df7b-105"><span id="LINECALLINFOSTATE_APPSPECIFIC"></span><span id="linecallinfostate_appspecific"></span>**LINECALLINFOSTATE \_ APPSPECIFIC**</span><span class="sxs-lookup"><span data-stu-id="5df7b-105"><span id="LINECALLINFOSTATE_APPSPECIFIC"></span><span id="linecallinfostate_appspecific"></span>**LINECALLINFOSTATE\_APPSPECIFIC**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5df7b-106">呼叫資訊記錄的應用程式特定欄位。</span><span class="sxs-lookup"><span data-stu-id="5df7b-106">The application-specific field of the call-information record.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5df7b-107"><span id="LINECALLINFOSTATE_BEARERMODE"></span><span id="linecallinfostate_bearermode"></span>**LINECALLINFOSTATE \_ BEARERMODE**</span><span class="sxs-lookup"><span data-stu-id="5df7b-107"><span id="LINECALLINFOSTATE_BEARERMODE"></span><span id="linecallinfostate_bearermode"></span>**LINECALLINFOSTATE\_BEARERMODE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5df7b-108">通話資訊記錄的持有人模式欄位。</span><span class="sxs-lookup"><span data-stu-id="5df7b-108">The bearer mode field of the call-information record.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5df7b-109"><span id="LINECALLINFOSTATE_CALLDATA"></span><span id="linecallinfostate_calldata"></span>**LINECALLINFOSTATE \_ CALLDATA**</span><span class="sxs-lookup"><span data-stu-id="5df7b-109"><span id="LINECALLINFOSTATE_CALLDATA"></span><span id="linecallinfostate_calldata"></span>**LINECALLINFOSTATE\_CALLDATA**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5df7b-110">[**LINECALLINFO**](/windows/desktop/api/Tapi/ns-tapi-linecallinfo)中的 **CallData** 成員已更新。</span><span class="sxs-lookup"><span data-stu-id="5df7b-110">The **CallData** member in [**LINECALLINFO**](/windows/desktop/api/Tapi/ns-tapi-linecallinfo) has been updated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5df7b-111"><span id="LINECALLINFOSTATE_CALLEDID"></span><span id="linecallinfostate_calledid"></span>**LINECALLINFOSTATE \_ CALLEDID**</span><span class="sxs-lookup"><span data-stu-id="5df7b-111"><span id="LINECALLINFOSTATE_CALLEDID"></span><span id="linecallinfostate_calledid"></span>**LINECALLINFOSTATE\_CALLEDID**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5df7b-112">呼叫資訊記錄的其中一個 calledID 相關欄位。</span><span class="sxs-lookup"><span data-stu-id="5df7b-112">One of the calledID-related fields of the call-information record.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5df7b-113"><span id="LINECALLINFOSTATE_CALLERID"></span><span id="linecallinfostate_callerid"></span>**LINECALLINFOSTATE \_ CALLERID**</span><span class="sxs-lookup"><span data-stu-id="5df7b-113"><span id="LINECALLINFOSTATE_CALLERID"></span><span id="linecallinfostate_callerid"></span>**LINECALLINFOSTATE\_CALLERID**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5df7b-114">呼叫資訊記錄的其中一個 callerID 相關欄位。</span><span class="sxs-lookup"><span data-stu-id="5df7b-114">One of the callerID-related fields of the call-information record.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5df7b-115"><span id="LINECALLINFOSTATE_CALLID"></span><span id="linecallinfostate_callid"></span>**LINECALLINFOSTATE \_ CALLID**</span><span class="sxs-lookup"><span data-stu-id="5df7b-115"><span id="LINECALLINFOSTATE_CALLID"></span><span id="linecallinfostate_callid"></span>**LINECALLINFOSTATE\_CALLID**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5df7b-116">呼叫資訊記錄的呼叫識別碼欄位。</span><span class="sxs-lookup"><span data-stu-id="5df7b-116">The call ID field of the call-information record.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5df7b-117"><span id="LINECALLINFOSTATE_CHARGINGINFO"></span><span id="linecallinfostate_charginginfo"></span>**LINECALLINFOSTATE \_ CHARGINGINFO**</span><span class="sxs-lookup"><span data-stu-id="5df7b-117"><span id="LINECALLINFOSTATE_CHARGINGINFO"></span><span id="linecallinfostate_charginginfo"></span>**LINECALLINFOSTATE\_CHARGINGINFO**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5df7b-118">通話資訊記錄的收費資訊。</span><span class="sxs-lookup"><span data-stu-id="5df7b-118">The charging information of the call-information record.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5df7b-119"><span id="LINECALLINFOSTATE_COMPLETIONID"></span><span id="linecallinfostate_completionid"></span>**LINECALLINFOSTATE \_ COMPLETIONID**</span><span class="sxs-lookup"><span data-stu-id="5df7b-119"><span id="LINECALLINFOSTATE_COMPLETIONID"></span><span id="linecallinfostate_completionid"></span>**LINECALLINFOSTATE\_COMPLETIONID**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5df7b-120">呼叫資訊記錄的完成識別碼欄位。</span><span class="sxs-lookup"><span data-stu-id="5df7b-120">The completion identifier field of the call-information record.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5df7b-121"><span id="LINECALLINFOSTATE_CONNECTEDID"></span><span id="linecallinfostate_connectedid"></span>**LINECALLINFOSTATE \_ CONNECTEDID**</span><span class="sxs-lookup"><span data-stu-id="5df7b-121"><span id="LINECALLINFOSTATE_CONNECTEDID"></span><span id="linecallinfostate_connectedid"></span>**LINECALLINFOSTATE\_CONNECTEDID**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5df7b-122">呼叫資訊記錄的其中一個 connectedID 相關欄位。</span><span class="sxs-lookup"><span data-stu-id="5df7b-122">One of the connectedID-related fields of the call-information record.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5df7b-123"><span id="LINECALLINFOSTATE_DEVSPECIFIC"></span><span id="linecallinfostate_devspecific"></span>**LINECALLINFOSTATE \_ DEVSPECIFIC**</span><span class="sxs-lookup"><span data-stu-id="5df7b-123"><span id="LINECALLINFOSTATE_DEVSPECIFIC"></span><span id="linecallinfostate_devspecific"></span>**LINECALLINFOSTATE\_DEVSPECIFIC**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5df7b-124">通話資訊記錄的裝置特定欄位。</span><span class="sxs-lookup"><span data-stu-id="5df7b-124">The device-specific field of the call-information record.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5df7b-125"><span id="LINECALLINFOSTATE_DIALPARAMS"></span><span id="linecallinfostate_dialparams"></span>**LINECALLINFOSTATE \_ DIALPARAMS**</span><span class="sxs-lookup"><span data-stu-id="5df7b-125"><span id="LINECALLINFOSTATE_DIALPARAMS"></span><span id="linecallinfostate_dialparams"></span>**LINECALLINFOSTATE\_DIALPARAMS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5df7b-126">通話資訊記錄的撥號參數。</span><span class="sxs-lookup"><span data-stu-id="5df7b-126">The dial parameters of the call-information record.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5df7b-127"><span id="LINECALLINFOSTATE_DISPLAY"></span><span id="linecallinfostate_display"></span>**LINECALLINFOSTATE \_ 顯示**</span><span class="sxs-lookup"><span data-stu-id="5df7b-127"><span id="LINECALLINFOSTATE_DISPLAY"></span><span id="linecallinfostate_display"></span>**LINECALLINFOSTATE\_DISPLAY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5df7b-128">呼叫資訊記錄的顯示欄位。</span><span class="sxs-lookup"><span data-stu-id="5df7b-128">The display field of the call-information record.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5df7b-129"><span id="LINECALLINFOSTATE_HIGHLEVELCOMP"></span><span id="linecallinfostate_highlevelcomp"></span>**LINECALLINFOSTATE \_ HIGHLEVELCOMP**</span><span class="sxs-lookup"><span data-stu-id="5df7b-129"><span id="LINECALLINFOSTATE_HIGHLEVELCOMP"></span><span id="linecallinfostate_highlevelcomp"></span>**LINECALLINFOSTATE\_HIGHLEVELCOMP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5df7b-130">呼叫資訊記錄的高層級相容性欄位。</span><span class="sxs-lookup"><span data-stu-id="5df7b-130">The high level compatibility field of the call-information record.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5df7b-131"><span id="LINECALLINFOSTATE_LOWLEVELCOMP"></span><span id="linecallinfostate_lowlevelcomp"></span>**LINECALLINFOSTATE \_ LOWLEVELCOMP**</span><span class="sxs-lookup"><span data-stu-id="5df7b-131"><span id="LINECALLINFOSTATE_LOWLEVELCOMP"></span><span id="linecallinfostate_lowlevelcomp"></span>**LINECALLINFOSTATE\_LOWLEVELCOMP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5df7b-132">呼叫資訊記錄的低層級相容性欄位。</span><span class="sxs-lookup"><span data-stu-id="5df7b-132">The low level compatibility field of the call-information record.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5df7b-133"><span id="LINECALLINFOSTATE_MEDIAMODE"></span><span id="linecallinfostate_mediamode"></span>**LINECALLINFOSTATE \_ MEDIAMODE**</span><span class="sxs-lookup"><span data-stu-id="5df7b-133"><span id="LINECALLINFOSTATE_MEDIAMODE"></span><span id="linecallinfostate_mediamode"></span>**LINECALLINFOSTATE\_MEDIAMODE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5df7b-134">呼叫資訊記錄的 [媒體類型] 欄位。</span><span class="sxs-lookup"><span data-stu-id="5df7b-134">The media type field of the call-information record.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5df7b-135"><span id="LINECALLINFOSTATE_MONITORMODES"></span><span id="linecallinfostate_monitormodes"></span>**LINECALLINFOSTATE \_ MONITORMODES**</span><span class="sxs-lookup"><span data-stu-id="5df7b-135"><span id="LINECALLINFOSTATE_MONITORMODES"></span><span id="linecallinfostate_monitormodes"></span>**LINECALLINFOSTATE\_MONITORMODES**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5df7b-136">通話資訊記錄中的一或多個數位、語氣或媒體監視欄位。</span><span class="sxs-lookup"><span data-stu-id="5df7b-136">One or more of the digit, tone, or media monitoring fields in the call-information record.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5df7b-137"><span id="LINECALLINFOSTATE_NUMMONITORS"></span><span id="linecallinfostate_nummonitors"></span>**LINECALLINFOSTATE \_ NUMMONITORS**</span><span class="sxs-lookup"><span data-stu-id="5df7b-137"><span id="LINECALLINFOSTATE_NUMMONITORS"></span><span id="linecallinfostate_nummonitors"></span>**LINECALLINFOSTATE\_NUMMONITORS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5df7b-138">呼叫資訊記錄中的 [監視器數目] 欄位已變更。</span><span class="sxs-lookup"><span data-stu-id="5df7b-138">The number of monitors field in the call-information record has changed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5df7b-139"><span id="LINECALLINFOSTATE_NUMOWNERDECR"></span><span id="linecallinfostate_numownerdecr"></span>**LINECALLINFOSTATE \_ NUMOWNERDECR**</span><span class="sxs-lookup"><span data-stu-id="5df7b-139"><span id="LINECALLINFOSTATE_NUMOWNERDECR"></span><span id="linecallinfostate_numownerdecr"></span>**LINECALLINFOSTATE\_NUMOWNERDECR**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5df7b-140">呼叫資訊記錄中的 [擁有者] 欄位數目已減少。</span><span class="sxs-lookup"><span data-stu-id="5df7b-140">The number of owner field in the call-information record was decreased.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5df7b-141"><span id="LINECALLINFOSTATE_NUMOWNERINCR"></span><span id="linecallinfostate_numownerincr"></span>**LINECALLINFOSTATE \_ NUMOWNERINCR**</span><span class="sxs-lookup"><span data-stu-id="5df7b-141"><span id="LINECALLINFOSTATE_NUMOWNERINCR"></span><span id="linecallinfostate_numownerincr"></span>**LINECALLINFOSTATE\_NUMOWNERINCR**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5df7b-142">呼叫資訊記錄中的 [擁有者] 欄位數目已增加。</span><span class="sxs-lookup"><span data-stu-id="5df7b-142">The number of owner field in the call-information record was increased.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5df7b-143"><span id="LINECALLINFOSTATE_ORIGIN"></span><span id="linecallinfostate_origin"></span>**LINECALLINFOSTATE \_ 來源**</span><span class="sxs-lookup"><span data-stu-id="5df7b-143"><span id="LINECALLINFOSTATE_ORIGIN"></span><span id="linecallinfostate_origin"></span>**LINECALLINFOSTATE\_ORIGIN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5df7b-144">呼叫資訊記錄的原始欄位。</span><span class="sxs-lookup"><span data-stu-id="5df7b-144">The origin field of the call-information record.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5df7b-145"><span id="LINECALLINFOSTATE_OTHER"></span><span id="linecallinfostate_other"></span>**LINECALLINFOSTATE \_ 其他**</span><span class="sxs-lookup"><span data-stu-id="5df7b-145"><span id="LINECALLINFOSTATE_OTHER"></span><span id="linecallinfostate_other"></span>**LINECALLINFOSTATE\_OTHER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5df7b-146">呼叫下列以外的資訊專案已變更。</span><span class="sxs-lookup"><span data-stu-id="5df7b-146">Call information items other than those listed below have changed.</span></span> <span data-ttu-id="5df7b-147">應用程式應該檢查目前的呼叫資訊，以判斷哪些專案已經變更。</span><span class="sxs-lookup"><span data-stu-id="5df7b-147">The application should check the current call information to determine which items have changed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5df7b-148"><span id="LINECALLINFOSTATE_QOS"></span><span id="linecallinfostate_qos"></span>**LINECALLINFOSTATE \_ QOS**</span><span class="sxs-lookup"><span data-stu-id="5df7b-148"><span id="LINECALLINFOSTATE_QOS"></span><span id="linecallinfostate_qos"></span>**LINECALLINFOSTATE\_QOS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5df7b-149">[**LINECALLINFO**](/windows/desktop/api/Tapi/ns-tapi-linecallinfo)中有一或多個 **QOS** 成員已更新。</span><span class="sxs-lookup"><span data-stu-id="5df7b-149">One or more of the **QOS** members in [**LINECALLINFO**](/windows/desktop/api/Tapi/ns-tapi-linecallinfo) has been updated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5df7b-150"><span id="LINECALLINFOSTATE_RATE"></span><span id="linecallinfostate_rate"></span>**LINECALLINFOSTATE \_ 率**</span><span class="sxs-lookup"><span data-stu-id="5df7b-150"><span id="LINECALLINFOSTATE_RATE"></span><span id="linecallinfostate_rate"></span>**LINECALLINFOSTATE\_RATE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5df7b-151">通話資訊記錄的費率欄位。</span><span class="sxs-lookup"><span data-stu-id="5df7b-151">The rate field of the call-information record.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5df7b-152"><span id="LINECALLINFOSTATE_REASON"></span><span id="linecallinfostate_reason"></span>**LINECALLINFOSTATE \_ 原因**</span><span class="sxs-lookup"><span data-stu-id="5df7b-152"><span id="LINECALLINFOSTATE_REASON"></span><span id="linecallinfostate_reason"></span>**LINECALLINFOSTATE\_REASON**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5df7b-153">呼叫資訊記錄的 [原因] 欄位。</span><span class="sxs-lookup"><span data-stu-id="5df7b-153">The reason field of the call-information record.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5df7b-154"><span id="LINECALLINFOSTATE_REDIRECTINGID"></span><span id="linecallinfostate_redirectingid"></span>**LINECALLINFOSTATE \_ REDIRECTINGID**</span><span class="sxs-lookup"><span data-stu-id="5df7b-154"><span id="LINECALLINFOSTATE_REDIRECTINGID"></span><span id="linecallinfostate_redirectingid"></span>**LINECALLINFOSTATE\_REDIRECTINGID**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5df7b-155">重新導向呼叫之位置的位址識別碼。</span><span class="sxs-lookup"><span data-stu-id="5df7b-155">The address identifier of the location that redirected a call.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5df7b-156"><span id="LINECALLINFOSTATE_REDIRECTIONID"></span><span id="linecallinfostate_redirectionid"></span>**LINECALLINFOSTATE \_ REDIRECTIONID**</span><span class="sxs-lookup"><span data-stu-id="5df7b-156"><span id="LINECALLINFOSTATE_REDIRECTIONID"></span><span id="linecallinfostate_redirectionid"></span>**LINECALLINFOSTATE\_REDIRECTIONID**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5df7b-157">已重新導向呼叫之位置的位址識別碼。</span><span class="sxs-lookup"><span data-stu-id="5df7b-157">The address identifier of the location to which a call has been redirected.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5df7b-158"><span id="LINECALLINFOSTATE_RELATEDCALLID"></span><span id="linecallinfostate_relatedcallid"></span>**LINECALLINFOSTATE \_ RELATEDCALLID**</span><span class="sxs-lookup"><span data-stu-id="5df7b-158"><span id="LINECALLINFOSTATE_RELATEDCALLID"></span><span id="linecallinfostate_relatedcallid"></span>**LINECALLINFOSTATE\_RELATEDCALLID**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5df7b-159">呼叫資訊記錄的相關呼叫識別碼欄位。</span><span class="sxs-lookup"><span data-stu-id="5df7b-159">The related call ID field of the call-information record.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5df7b-160"><span id="LINECALLINFOSTATE_TERMINAL"></span><span id="linecallinfostate_terminal"></span>**LINECALLINFOSTATE \_ 終端機**</span><span class="sxs-lookup"><span data-stu-id="5df7b-160"><span id="LINECALLINFOSTATE_TERMINAL"></span><span id="linecallinfostate_terminal"></span>**LINECALLINFOSTATE\_TERMINAL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5df7b-161">通話資訊記錄的終端機模式資訊。</span><span class="sxs-lookup"><span data-stu-id="5df7b-161">The terminal mode information of the call-information record.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5df7b-162"><span id="LINECALLINFOSTATE_TREATMENT"></span><span id="linecallinfostate_treatment"></span>**LINECALLINFOSTATE \_ 處理**</span><span class="sxs-lookup"><span data-stu-id="5df7b-162"><span id="LINECALLINFOSTATE_TREATMENT"></span><span id="linecallinfostate_treatment"></span>**LINECALLINFOSTATE\_TREATMENT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5df7b-163">[**LINECALLINFO**](/windows/desktop/api/Tapi/ns-tapi-linecallinfo)中的 **CallTreatment** 成員已更新。</span><span class="sxs-lookup"><span data-stu-id="5df7b-163">The **CallTreatment** member in [**LINECALLINFO**](/windows/desktop/api/Tapi/ns-tapi-linecallinfo) has been updated.</span></span> <span data-ttu-id="5df7b-164">這可能是為了回應 [**lineSetCallTreatment**](/windows/desktop/api/Tapi/nf-tapi-linesetcalltreatment) 函式、撥號狀態變更、呼叫 "vector" 或控制呼叫的其他腳本，或在完成錄製的訊息時， (通常會指出「無回應」或「音樂」 ) 的變更。</span><span class="sxs-lookup"><span data-stu-id="5df7b-164">This can occur in response to a [**lineSetCallTreatment**](/windows/desktop/api/Tapi/nf-tapi-linesetcalltreatment) function, a call state change, a call "vector" or other script controlling the call, or upon completion of playback of a recorded message (ordinarily, indicating a change to "silence" or "music").</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5df7b-165"><span id="LINECALLINFOSTATE_TRUNK"></span><span id="linecallinfostate_trunk"></span>**LINECALLINFOSTATE \_ 主幹**</span><span class="sxs-lookup"><span data-stu-id="5df7b-165"><span id="LINECALLINFOSTATE_TRUNK"></span><span id="linecallinfostate_trunk"></span>**LINECALLINFOSTATE\_TRUNK**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5df7b-166">呼叫資訊記錄的主幹欄位。</span><span class="sxs-lookup"><span data-stu-id="5df7b-166">The trunk field of the call-information record.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5df7b-167"><span id="LINECALLINFOSTATE_USERUSERINFO"></span><span id="linecallinfostate_useruserinfo"></span>**LINECALLINFOSTATE \_ USERUSERINFO**</span><span class="sxs-lookup"><span data-stu-id="5df7b-167"><span id="LINECALLINFOSTATE_USERUSERINFO"></span><span id="linecallinfostate_useruserinfo"></span>**LINECALLINFOSTATE\_USERUSERINFO**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5df7b-168">通話資訊記錄的使用者資訊。</span><span class="sxs-lookup"><span data-stu-id="5df7b-168">The user-user information of the call-information record.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5df7b-169">備註</span><span class="sxs-lookup"><span data-stu-id="5df7b-169">Remarks</span></span>

<span data-ttu-id="5df7b-170">無延伸。</span><span class="sxs-lookup"><span data-stu-id="5df7b-170">No extensibility.</span></span> <span data-ttu-id="5df7b-171">所有32位都是保留的。</span><span class="sxs-lookup"><span data-stu-id="5df7b-171">All 32 bits are reserved.</span></span>

<span data-ttu-id="5df7b-172">當此資料結構中發生變更時，會將 [**行 \_ CALLINFO**](line-callinfo.md) 訊息傳送至應用程式。</span><span class="sxs-lookup"><span data-stu-id="5df7b-172">When changes occur in this data structure, a [**LINE\_CALLINFO**](line-callinfo.md) message is sent to the application.</span></span> <span data-ttu-id="5df7b-173">此訊息的參數是呼叫的控制碼，以及已變更之資訊專案的指示。</span><span class="sxs-lookup"><span data-stu-id="5df7b-173">The parameters to this message are a handle to the call and an indication of the information item that has changed.</span></span> <span data-ttu-id="5df7b-174">[**LINEADDRESSCAPS**](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps)資料結構也會指出這些呼叫資訊元素對位址上的每個呼叫都有效。</span><span class="sxs-lookup"><span data-stu-id="5df7b-174">The [**LINEADDRESSCAPS**](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps) data structure also indicates which of these call information elements are valid for every call on the address.</span></span>

## <a name="requirements"></a><span data-ttu-id="5df7b-175">規格需求</span><span class="sxs-lookup"><span data-stu-id="5df7b-175">Requirements</span></span>



| <span data-ttu-id="5df7b-176">需求</span><span class="sxs-lookup"><span data-stu-id="5df7b-176">Requirement</span></span> | <span data-ttu-id="5df7b-177">值</span><span class="sxs-lookup"><span data-stu-id="5df7b-177">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="5df7b-178">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="5df7b-178">TAPI version</span></span><br/> | <span data-ttu-id="5df7b-179">需要 TAPI 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="5df7b-179">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="5df7b-180">標頭</span><span class="sxs-lookup"><span data-stu-id="5df7b-180">Header</span></span><br/>       | <dl> <span data-ttu-id="5df7b-181"><dt>Tapi</dt></span><span class="sxs-lookup"><span data-stu-id="5df7b-181"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5df7b-182">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5df7b-182">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5df7b-183">**行 \_ CALLINFO**</span><span class="sxs-lookup"><span data-stu-id="5df7b-183">**LINE\_CALLINFO**</span></span>](line-callinfo.md)
</dt> <dt>

[<span data-ttu-id="5df7b-184">**LINEADDRESSCAPS**</span><span class="sxs-lookup"><span data-stu-id="5df7b-184">**LINEADDRESSCAPS**</span></span>](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps)
</dt> <dt>

[<span data-ttu-id="5df7b-185">**LINECALLINFO**</span><span class="sxs-lookup"><span data-stu-id="5df7b-185">**LINECALLINFO**</span></span>](/windows/desktop/api/Tapi/ns-tapi-linecallinfo)
</dt> <dt>

[<span data-ttu-id="5df7b-186">**lineSetCallTreatment**</span><span class="sxs-lookup"><span data-stu-id="5df7b-186">**lineSetCallTreatment**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linesetcalltreatment)
</dt> </dl>

 

 




