---
title: 'MpThreatOpen 函式 (MpClient) '
description: 針對取得威脅的目的，傳回列舉控制碼。
ms.assetid: E1178F0C-E9C0-4532-AE9B-452770600DF2
keywords:
- MpThreatOpen 函式舊版 Windows 環境功能
topic_type:
- apiref
api_name:
- MpThreatOpen
api_location:
- MpClient.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ca30435f9d7cba32771a2445d8a1156f0edaa9b1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106996182"
---
# <a name="mpthreatopen-function"></a><span data-ttu-id="a722b-104">MpThreatOpen 函式</span><span class="sxs-lookup"><span data-stu-id="a722b-104">MpThreatOpen function</span></span>

<span data-ttu-id="a722b-105">針對取得威脅的目的，傳回列舉控制碼。</span><span class="sxs-lookup"><span data-stu-id="a722b-105">Returns an enumeration handle for the purpose of retrieving threats.</span></span> <span data-ttu-id="a722b-106">這項功能可用來開啟特定掃描偵測到的威脅、系統中的所有作用中威脅、威脅消毒的歷程記錄，或簽章資料庫中出現的所有威脅。</span><span class="sxs-lookup"><span data-stu-id="a722b-106">This function can be used to open threats detected by a specific scan, all the active threats in the system, the history of threat disinfection, or all the threats present in the signature database.</span></span>

## <a name="syntax"></a><span data-ttu-id="a722b-107">語法</span><span class="sxs-lookup"><span data-stu-id="a722b-107">Syntax</span></span>


```C++
HRESULT WINAPI MpThreatOpen(
  _In_  MPHANDLE        hScanHandle,
  _In_  MPTHREAT_SOURCE ThreatSource,
  _In_  MPTHREAT_TYPE   ThreatType,
  _Out_ PMPHANDLE       phThreatEnumHandle
);
```



## <a name="parameters"></a><span data-ttu-id="a722b-108">參數</span><span class="sxs-lookup"><span data-stu-id="a722b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a722b-109">*hScanHandle* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a722b-109">*hScanHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a722b-110">類型： **MPHANDLE**</span><span class="sxs-lookup"><span data-stu-id="a722b-110">Type: **MPHANDLE**</span></span>

<span data-ttu-id="a722b-111">可以是 [**MpScanStart**](mpscanstart.md) 函式所傳回之已完成掃描工作的控制碼。</span><span class="sxs-lookup"><span data-stu-id="a722b-111">Can be a handle to a completed scan operation, returned by the [**MpScanStart**](mpscanstart.md) function.</span></span> <span data-ttu-id="a722b-112">或者，您可以將此參數設定為 [**MpManagerOpen**](mpmanageropen.md) 所傳回的 malware protection manager 介面控制碼，以列舉系統中的所有作用中威脅、威脅消毒的歷程記錄，或簽章資料庫中的威脅。</span><span class="sxs-lookup"><span data-stu-id="a722b-112">Alternately, this parameter can be set to the malware protection manager interface handle returned by [**MpManagerOpen**](mpmanageropen.md) to enumerate all active threats in the system, the history of threat disinfection, or threats from signature database.</span></span>

</dd> <dt>

<span data-ttu-id="a722b-113">*ThreatSource* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a722b-113">*ThreatSource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a722b-114">類型： **MPTHREAT \_ 來源**</span><span class="sxs-lookup"><span data-stu-id="a722b-114">Type: **MPTHREAT\_SOURCE**</span></span>

<span data-ttu-id="a722b-115">用來控制威脅列舉的來源。</span><span class="sxs-lookup"><span data-stu-id="a722b-115">Used to control the source of threat enumeration.</span></span> <span data-ttu-id="a722b-116">此參數的可能值為：</span><span class="sxs-lookup"><span data-stu-id="a722b-116">The possible values for this parameter are:</span></span>



| <span data-ttu-id="a722b-117">值</span><span class="sxs-lookup"><span data-stu-id="a722b-117">Value</span></span>                                                                                                                                                                                                 | <span data-ttu-id="a722b-118">意義</span><span class="sxs-lookup"><span data-stu-id="a722b-118">Meaning</span></span>                                                                                                            |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| <span id="MPTHREAT_SOURCE_SCAN"></span><span id="mpthreat_source_scan"></span><dl> <span data-ttu-id="a722b-119"><dt>**MPTHREAT \_ 來源 \_ 掃描**</dt></span><span class="sxs-lookup"><span data-stu-id="a722b-119"><dt>**MPTHREAT\_SOURCE\_SCAN**</dt></span></span> </dl>                   | <span data-ttu-id="a722b-120">與特定掃描控制碼相關聯的威脅。</span><span class="sxs-lookup"><span data-stu-id="a722b-120">Threats that are associated with the specific scan handle.</span></span><br/>                                              |
| <span id="MPTHREAT_SOURCE_ACTIVE"></span><span id="mpthreat_source_active"></span><dl> <span data-ttu-id="a722b-121"><dt>**MPTHREAT \_ 來源 \_ 有效**</dt></span><span class="sxs-lookup"><span data-stu-id="a722b-121"><dt>**MPTHREAT\_SOURCE\_ACTIVE**</dt></span></span> </dl>             | <span data-ttu-id="a722b-122">系統中目前作用中的威脅。</span><span class="sxs-lookup"><span data-stu-id="a722b-122">Threats that are currently active in the system.</span></span><br/>                                                        |
| <span id="MPTHREAT_SOURCE_HISTORY"></span><span id="mpthreat_source_history"></span><dl> <span data-ttu-id="a722b-123"><dt>**MPTHREAT \_ 來源歷程 \_ 記錄**</dt></span><span class="sxs-lookup"><span data-stu-id="a722b-123"><dt>**MPTHREAT\_SOURCE\_HISTORY**</dt></span></span> </dl>          | <span data-ttu-id="a722b-124">以歷程記錄方式處理和保留的威脅。</span><span class="sxs-lookup"><span data-stu-id="a722b-124">Threats that are acted upon and preserved as a history.</span></span><br/>                                                 |
| <span id="MPTHREAT_SOURCE_QUARANTINE"></span><span id="mpthreat_source_quarantine"></span><dl> <span data-ttu-id="a722b-125"><dt>**MPTHREAT \_ 來源 \_ 隔離**</dt></span><span class="sxs-lookup"><span data-stu-id="a722b-125"><dt>**MPTHREAT\_SOURCE\_QUARANTINE**</dt></span></span> </dl> | <span data-ttu-id="a722b-126">已隔離的威脅。</span><span class="sxs-lookup"><span data-stu-id="a722b-126">Threats that are quarantined.</span></span><br/>                                                                           |
| <span id="MPTHREAT_SOURCE_SIGNATURE"></span><span id="mpthreat_source_signature"></span><dl> <span data-ttu-id="a722b-127"><dt>**MPTHREAT \_ 來源簽章 \_**</dt></span><span class="sxs-lookup"><span data-stu-id="a722b-127"><dt>**MPTHREAT\_SOURCE\_SIGNATURE**</dt></span></span> </dl>    | <span data-ttu-id="a722b-128">可以使用目前的簽章資料庫偵測到的威脅。</span><span class="sxs-lookup"><span data-stu-id="a722b-128">Threats that are possible to detect with the current signature database.</span></span><br/>                                |
| <span id="MPTHREAT_SOURCE_STATE"></span><span id="mpthreat_source_state"></span><dl> <span data-ttu-id="a722b-129"><dt>**MPTHREAT \_ 來源 \_ 狀態**</dt></span><span class="sxs-lookup"><span data-stu-id="a722b-129"><dt>**MPTHREAT\_SOURCE\_STATE**</dt></span></span> </dl>                | <span data-ttu-id="a722b-130">最近所採取的威脅。</span><span class="sxs-lookup"><span data-stu-id="a722b-130">Threats that have been acted upon recently.</span></span> <span data-ttu-id="a722b-131"> ( 「最近」是由可設定的內部設定所定義。 ) </span><span class="sxs-lookup"><span data-stu-id="a722b-131">("Recently" is defined by a configurable internal setting.)</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="a722b-132">*ThreatType* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a722b-132">*ThreatType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a722b-133">類型： **MPTHREAT \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="a722b-133">Type: **MPTHREAT\_TYPE**</span></span>

<span data-ttu-id="a722b-134">用來根據偵測類型篩選列舉的威脅。</span><span class="sxs-lookup"><span data-stu-id="a722b-134">Used to filter enumerated threats based on the detection type.</span></span> <span data-ttu-id="a722b-135">此參數的可能值為：</span><span class="sxs-lookup"><span data-stu-id="a722b-135">The possible values for this parameter are:</span></span>



| <span data-ttu-id="a722b-136">值</span><span class="sxs-lookup"><span data-stu-id="a722b-136">Value</span></span>                                                                                                                                                                                           | <span data-ttu-id="a722b-137">意義</span><span class="sxs-lookup"><span data-stu-id="a722b-137">Meaning</span></span>                                                                                                       |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span id="MPTHREAT_TYPE_KNOWNBAD"></span><span id="mpthreat_type_knownbad"></span><dl> <span data-ttu-id="a722b-138"><dt>**MPTHREAT \_ 類型 \_ KNOWNBAD**</dt></span><span class="sxs-lookup"><span data-stu-id="a722b-138"><dt>**MPTHREAT\_TYPE\_KNOWNBAD**</dt></span></span> </dl>       | <span data-ttu-id="a722b-139">偵測是根據特定的簽章、模擬或其他威脅偵測方法來執行。</span><span class="sxs-lookup"><span data-stu-id="a722b-139">Detection is performed based on a specific signature, emulation, or other threat detection method.</span></span><br/> |
| <span id="MPTHREAT_TYPE_SUSPICIOUS"></span><span id="mpthreat_type_suspicious"></span><dl> <span data-ttu-id="a722b-140"><dt>**MPTHREAT \_ 類型 \_ 可疑**</dt></span><span class="sxs-lookup"><span data-stu-id="a722b-140"><dt>**MPTHREAT\_TYPE\_SUSPICIOUS**</dt></span></span> </dl> | <span data-ttu-id="a722b-141">偵測是根據行為監視來執行。</span><span class="sxs-lookup"><span data-stu-id="a722b-141">Detection is performed based on behavior monitoring.</span></span><br/>                                               |
| <span id="MPTHREAT_TYPE_UNKNOWN"></span><span id="mpthreat_type_unknown"></span><dl> <span data-ttu-id="a722b-142"><dt>**未知的 MPTHREAT \_ 類型 \_**</dt></span><span class="sxs-lookup"><span data-stu-id="a722b-142"><dt>**MPTHREAT\_TYPE\_UNKNOWN**</dt></span></span> </dl>          | <span data-ttu-id="a722b-143">偵測是根據 (非分類) 的未知威脅來執行。</span><span class="sxs-lookup"><span data-stu-id="a722b-143">Detection is performed based on unknown threats (unclassified).</span></span><br/>                                    |
| <span id="MPTHREAT_TYPE_KNOWNGOOD"></span><span id="mpthreat_type_knowngood"></span><dl> <span data-ttu-id="a722b-144"><dt>**MPTHREAT \_ 類型 \_ KNOWNGOOD**</dt></span><span class="sxs-lookup"><span data-stu-id="a722b-144"><dt>**MPTHREAT\_TYPE\_KNOWNGOOD**</dt></span></span> </dl>    | <span data-ttu-id="a722b-145">偵測是根據已知的安全威脅來執行。</span><span class="sxs-lookup"><span data-stu-id="a722b-145">Detection is performed based on known safe threats.</span></span><br/>                                                |
| <span id="MPTHREAT_TYPE_NIS"></span><span id="mpthreat_type_nis"></span><dl> <span data-ttu-id="a722b-146"><dt>**MPTHREAT \_ 類型 \_ NIS**</dt></span><span class="sxs-lookup"><span data-stu-id="a722b-146"><dt>**MPTHREAT\_TYPE\_NIS**</dt></span></span> </dl>                      | <span data-ttu-id="a722b-147">偵測是根據 NIS 威脅執行。</span><span class="sxs-lookup"><span data-stu-id="a722b-147">Detection is performed based on NIS threats.</span></span><br/>                                                       |



 

</dd> <dt>

<span data-ttu-id="a722b-148">*phThreatEnumHandle* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="a722b-148">*phThreatEnumHandle* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a722b-149">類型： **PMPHANDLE**</span><span class="sxs-lookup"><span data-stu-id="a722b-149">Type: **PMPHANDLE**</span></span>

<span data-ttu-id="a722b-150">傳回識別列舉內容的威脅列舉控制碼。</span><span class="sxs-lookup"><span data-stu-id="a722b-150">Returned threat enumeration handle which identifies the enumeration context.</span></span> <span data-ttu-id="a722b-151">您可以使用此控制碼來列舉使用 [**MpThreatEnumerate**](mpthreatenumerate.md)的威脅資訊。</span><span class="sxs-lookup"><span data-stu-id="a722b-151">This handle can be used to enumerate threat information using [**MpThreatEnumerate**](mpthreatenumerate.md).</span></span> <span data-ttu-id="a722b-152">控制碼必須使用 [**MpHandleClose**](mphandleclose.md) 函式來關閉。</span><span class="sxs-lookup"><span data-stu-id="a722b-152">The handle must be closed with the [**MpHandleClose**](mphandleclose.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a722b-153">傳回值</span><span class="sxs-lookup"><span data-stu-id="a722b-153">Return value</span></span>

<span data-ttu-id="a722b-154">類型： **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="a722b-154">Type: **HRESULT**</span></span>

<span data-ttu-id="a722b-155">如果函式成功，則傳回值為 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="a722b-155">If the function succeeds the return value is **S\_OK**.</span></span>

<span data-ttu-id="a722b-156">如果函式失敗，則傳回值會是失敗的 **HRESULT** 程式碼。</span><span class="sxs-lookup"><span data-stu-id="a722b-156">If the function fails then the return value is a failed **HRESULT** code.</span></span> <span data-ttu-id="a722b-157">呼叫端可以使用 [**MpErrorMessageFormat**](mperrormessageformat.md) 函數來取得錯誤訊息的一般描述。</span><span class="sxs-lookup"><span data-stu-id="a722b-157">The caller can use the [**MpErrorMessageFormat**](mperrormessageformat.md) function to get a generic description of the error message.</span></span>

## <a name="requirements"></a><span data-ttu-id="a722b-158">規格需求</span><span class="sxs-lookup"><span data-stu-id="a722b-158">Requirements</span></span>



| <span data-ttu-id="a722b-159">需求</span><span class="sxs-lookup"><span data-stu-id="a722b-159">Requirement</span></span> | <span data-ttu-id="a722b-160">值</span><span class="sxs-lookup"><span data-stu-id="a722b-160">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a722b-161">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a722b-161">Minimum supported client</span></span><br/> | <span data-ttu-id="a722b-162">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a722b-162">Windows 8 \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="a722b-163">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a722b-163">Minimum supported server</span></span><br/> | <span data-ttu-id="a722b-164">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a722b-164">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="a722b-165">標頭</span><span class="sxs-lookup"><span data-stu-id="a722b-165">Header</span></span><br/>                   | <dl> <span data-ttu-id="a722b-166"><dt>MpClient。h</dt></span><span class="sxs-lookup"><span data-stu-id="a722b-166"><dt>MpClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="a722b-167">DLL</span><span class="sxs-lookup"><span data-stu-id="a722b-167">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a722b-168"><dt>MpClient.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a722b-168"><dt>MpClient.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a722b-169">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a722b-169">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a722b-170">**MpErrorMessageFormat**</span><span class="sxs-lookup"><span data-stu-id="a722b-170">**MpErrorMessageFormat**</span></span>](mperrormessageformat.md)
</dt> <dt>

[<span data-ttu-id="a722b-171">**MpHandleClose**</span><span class="sxs-lookup"><span data-stu-id="a722b-171">**MpHandleClose**</span></span>](mphandleclose.md)
</dt> <dt>

[<span data-ttu-id="a722b-172">**MpManagerOpen**</span><span class="sxs-lookup"><span data-stu-id="a722b-172">**MpManagerOpen**</span></span>](mpmanageropen.md)
</dt> <dt>

[<span data-ttu-id="a722b-173">**MpScanStart**</span><span class="sxs-lookup"><span data-stu-id="a722b-173">**MpScanStart**</span></span>](mpscanstart.md)
</dt> <dt>

[<span data-ttu-id="a722b-174">**MpThreatEnumerate**</span><span class="sxs-lookup"><span data-stu-id="a722b-174">**MpThreatEnumerate**</span></span>](mpthreatenumerate.md)
</dt> </dl>

 

 





