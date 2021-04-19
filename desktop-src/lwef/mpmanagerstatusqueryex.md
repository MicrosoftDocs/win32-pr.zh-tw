---
title: 'MpManagerStatusQueryEx 函式 (MpClient) '
description: '傳回惡意程式碼防護管理員各元件的相關狀態資訊。 |MpManagerStatusQueryEx 函式 (MpClient) '
ms.assetid: 98088AB9-C7CF-46A1-B444-2C0EF882AA66
keywords:
- MpManagerStatusQueryEx 函式舊版 Windows 環境功能
topic_type:
- apiref
api_name:
- MpManagerStatusQueryEx
api_location:
- MpClient.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ca541b5f1aff2e0ba03b88d69c451891c3a174bb
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "106989177"
---
# <a name="mpmanagerstatusqueryex-function"></a><span data-ttu-id="9c2e5-105">MpManagerStatusQueryEx 函式</span><span class="sxs-lookup"><span data-stu-id="9c2e5-105">MpManagerStatusQueryEx function</span></span>

<span data-ttu-id="9c2e5-106">傳回惡意程式碼防護管理員各元件的相關狀態資訊。</span><span class="sxs-lookup"><span data-stu-id="9c2e5-106">Returns status information about various components of the malware protection manager.</span></span>

## <a name="syntax"></a><span data-ttu-id="9c2e5-107">語法</span><span class="sxs-lookup"><span data-stu-id="9c2e5-107">Syntax</span></span>


```C++
HRESULT WINAPI MpManagerStatusQueryEx(
  _In_  MPHANDLE       hMpHandle,
  _In_  DWORD          dwFlag,
  _Out_ PMPSTATUS_INFO pStatusInfo
);
```



## <a name="parameters"></a><span data-ttu-id="9c2e5-108">參數</span><span class="sxs-lookup"><span data-stu-id="9c2e5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9c2e5-109">*hMpHandle* \[在\]</span><span class="sxs-lookup"><span data-stu-id="9c2e5-109">*hMpHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9c2e5-110">類型： **MPHANDLE**</span><span class="sxs-lookup"><span data-stu-id="9c2e5-110">Type: **MPHANDLE**</span></span>

<span data-ttu-id="9c2e5-111">惡意程式碼防護管理員介面的控制碼。</span><span class="sxs-lookup"><span data-stu-id="9c2e5-111">Handle to the malware protection manager interface.</span></span> <span data-ttu-id="9c2e5-112">[**MpManagerOpen**](mpmanageropen.md)函數會傳回這個控制碼。</span><span class="sxs-lookup"><span data-stu-id="9c2e5-112">This handle is returned by the [**MpManagerOpen**](mpmanageropen.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="9c2e5-113">*>dwflag* \[在\]</span><span class="sxs-lookup"><span data-stu-id="9c2e5-113">*dwFlag* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9c2e5-114">類型： **DWORD**</span><span class="sxs-lookup"><span data-stu-id="9c2e5-114">Type: **DWORD**</span></span>

<span data-ttu-id="9c2e5-115">控制傳回的查詢資訊。</span><span class="sxs-lookup"><span data-stu-id="9c2e5-115">Controls which query information is returned.</span></span> <span data-ttu-id="9c2e5-116">某些資訊的成本很高，而且可能不需要。</span><span class="sxs-lookup"><span data-stu-id="9c2e5-116">Some information is expensive and may not be needed.</span></span>



| <span data-ttu-id="9c2e5-117">值</span><span class="sxs-lookup"><span data-stu-id="9c2e5-117">Value</span></span>                                                                                                                                                                                                         | <span data-ttu-id="9c2e5-118">意義</span><span class="sxs-lookup"><span data-stu-id="9c2e5-118">Meaning</span></span>                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <span id="MP_STATUS_QUERY_FLAGS_NONE"></span><span id="mp_status_query_flags_none"></span><dl> <span data-ttu-id="9c2e5-119"><dt>**MP \_ STATUS \_ 查詢 \_ 旗標 \_ 無**</dt></span><span class="sxs-lookup"><span data-stu-id="9c2e5-119"><dt>**MP\_STATUS\_QUERY\_FLAGS\_NONE**</dt></span></span> </dl>       | <span data-ttu-id="9c2e5-120">預設值。</span><span class="sxs-lookup"><span data-stu-id="9c2e5-120">Default.</span></span><br/>                            |
| <span id="MP_STATUS_QUERY_FLAG_NOSTATE"></span><span id="mp_status_query_flag_nostate"></span><dl> <span data-ttu-id="9c2e5-121"><dt>**MP \_ STATUS \_ 查詢 \_ 旗標 \_ NOSTATE**</dt></span><span class="sxs-lookup"><span data-stu-id="9c2e5-121"><dt>**MP\_STATUS\_QUERY\_FLAG\_NOSTATE**</dt></span></span> </dl> | <span data-ttu-id="9c2e5-122">請勿查詢狀態資訊。</span><span class="sxs-lookup"><span data-stu-id="9c2e5-122">Do not query for state information.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="9c2e5-123">*pStatusInfo* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="9c2e5-123">*pStatusInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9c2e5-124">類型： **PMPSTATUS \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="9c2e5-124">Type: **PMPSTATUS\_INFO**</span></span>

<span data-ttu-id="9c2e5-125">結構的指標，此結構會傳回有關上次掃描、作用中威脅和各種元件狀態的狀態資訊。</span><span class="sxs-lookup"><span data-stu-id="9c2e5-125">Pointer to a structure that returns status information regarding last scans, active threats and various component status.</span></span> <span data-ttu-id="9c2e5-126">請參閱 [**MPSTATUS \_ 資訊**](mpstatus-info.md)。</span><span class="sxs-lookup"><span data-stu-id="9c2e5-126">See [**MPSTATUS\_INFO**](mpstatus-info.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9c2e5-127">傳回值</span><span class="sxs-lookup"><span data-stu-id="9c2e5-127">Return value</span></span>

<span data-ttu-id="9c2e5-128">類型： **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="9c2e5-128">Type: **HRESULT**</span></span>

<span data-ttu-id="9c2e5-129">如果函式成功，則傳回值為 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="9c2e5-129">If the function succeeds the return value is **S\_OK**.</span></span> <span data-ttu-id="9c2e5-130">即使反惡意程式碼服務不在執行中，此函式呼叫仍會成功。</span><span class="sxs-lookup"><span data-stu-id="9c2e5-130">This function call is guaranteed to succeed even if an AntiMalware service is not running.</span></span>

<span data-ttu-id="9c2e5-131">如果函式失敗，則傳回值會是失敗的 **HRESULT** 程式碼。</span><span class="sxs-lookup"><span data-stu-id="9c2e5-131">If the function fails then the return value is a failed **HRESULT** code.</span></span> <span data-ttu-id="9c2e5-132">呼叫端可以使用 [**MpErrorMessageFormat**](mperrormessageformat.md) 函數來取得錯誤訊息的一般描述。</span><span class="sxs-lookup"><span data-stu-id="9c2e5-132">The caller can use the [**MpErrorMessageFormat**](mperrormessageformat.md) function to get a generic description of the error message.</span></span>

## <a name="requirements"></a><span data-ttu-id="9c2e5-133">規格需求</span><span class="sxs-lookup"><span data-stu-id="9c2e5-133">Requirements</span></span>



| <span data-ttu-id="9c2e5-134">需求</span><span class="sxs-lookup"><span data-stu-id="9c2e5-134">Requirement</span></span> | <span data-ttu-id="9c2e5-135">值</span><span class="sxs-lookup"><span data-stu-id="9c2e5-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9c2e5-136">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9c2e5-136">Minimum supported client</span></span><br/> | <span data-ttu-id="9c2e5-137">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9c2e5-137">Windows 8 \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="9c2e5-138">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9c2e5-138">Minimum supported server</span></span><br/> | <span data-ttu-id="9c2e5-139">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9c2e5-139">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="9c2e5-140">標頭</span><span class="sxs-lookup"><span data-stu-id="9c2e5-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="9c2e5-141"><dt>MpClient。h</dt></span><span class="sxs-lookup"><span data-stu-id="9c2e5-141"><dt>MpClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="9c2e5-142">DLL</span><span class="sxs-lookup"><span data-stu-id="9c2e5-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9c2e5-143"><dt>MpClient.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9c2e5-143"><dt>MpClient.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9c2e5-144">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9c2e5-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9c2e5-145">**MpErrorMessageFormat**</span><span class="sxs-lookup"><span data-stu-id="9c2e5-145">**MpErrorMessageFormat**</span></span>](mperrormessageformat.md)
</dt> <dt>

[<span data-ttu-id="9c2e5-146">**MpManagerOpen**</span><span class="sxs-lookup"><span data-stu-id="9c2e5-146">**MpManagerOpen**</span></span>](mpmanageropen.md)
</dt> <dt>

[<span data-ttu-id="9c2e5-147">**MPSTATUS \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="9c2e5-147">**MPSTATUS\_INFO**</span></span>](mpstatus-info.md)
</dt> </dl>

 

 





