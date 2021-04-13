---
title: 'MpManagerStatusQuery 函式 (MpClient) '
description: '傳回惡意程式碼防護管理員各元件的相關狀態資訊。 |MpManagerStatusQuery 函式 (MpClient) '
ms.assetid: E993FD8B-A35D-41C1-9522-1B9F0BC10B3D
keywords:
- MpManagerStatusQuery 函式舊版 Windows 環境功能
topic_type:
- apiref
api_name:
- MpManagerStatusQuery
api_location:
- MpClient.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad2e28bab1794b53695872310a3a7cf5d088f1a1
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104321876"
---
# <a name="mpmanagerstatusquery-function"></a><span data-ttu-id="4e493-105">MpManagerStatusQuery 函式</span><span class="sxs-lookup"><span data-stu-id="4e493-105">MpManagerStatusQuery function</span></span>

<span data-ttu-id="4e493-106">\[**MpManagerStatusQuery** 不受支援，未來可能會變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="4e493-106">\[**MpManagerStatusQuery** is not supported and may be altered or unavailable in the future.</span></span> <span data-ttu-id="4e493-107">相反地，請使用 [**MpManagerStatusQueryEx**](mpmanagerstatusqueryex.md)。\]</span><span class="sxs-lookup"><span data-stu-id="4e493-107">Instead, use [**MpManagerStatusQueryEx**](mpmanagerstatusqueryex.md).\]</span></span>

<span data-ttu-id="4e493-108">傳回惡意程式碼防護管理員各元件的相關狀態資訊。</span><span class="sxs-lookup"><span data-stu-id="4e493-108">Returns status information about various components of the malware protection manager.</span></span>

## <a name="syntax"></a><span data-ttu-id="4e493-109">語法</span><span class="sxs-lookup"><span data-stu-id="4e493-109">Syntax</span></span>


```C++
HRESULT WINAPI MpManagerStatusQuery(
  _In_  MPHANDLE       hMpHandle,
  _Out_ PMPSTATUS_INFO pStatusInfo
);
```



## <a name="parameters"></a><span data-ttu-id="4e493-110">參數</span><span class="sxs-lookup"><span data-stu-id="4e493-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4e493-111">*hMpHandle* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4e493-111">*hMpHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4e493-112">類型： **MPHANDLE**</span><span class="sxs-lookup"><span data-stu-id="4e493-112">Type: **MPHANDLE**</span></span>

<span data-ttu-id="4e493-113">惡意程式碼防護管理員介面的控制碼。</span><span class="sxs-lookup"><span data-stu-id="4e493-113">Handle to the malware protection manager interface.</span></span> <span data-ttu-id="4e493-114">[**MpManagerOpen**](mpmanageropen.md)函數會傳回這個控制碼。</span><span class="sxs-lookup"><span data-stu-id="4e493-114">This handle is returned by the [**MpManagerOpen**](mpmanageropen.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="4e493-115">*pStatusInfo* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="4e493-115">*pStatusInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4e493-116">類型： **PMPSTATUS \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="4e493-116">Type: **PMPSTATUS\_INFO**</span></span>

<span data-ttu-id="4e493-117">結構的指標，此結構會傳回有關上次掃描、作用中威脅和各種元件狀態的狀態資訊。</span><span class="sxs-lookup"><span data-stu-id="4e493-117">Pointer to a structure that returns status information regarding last scans, active threats and various component status.</span></span> <span data-ttu-id="4e493-118">請參閱 [**MPSTATUS \_ 資訊**](mpstatus-info.md)。</span><span class="sxs-lookup"><span data-stu-id="4e493-118">See [**MPSTATUS\_INFO**](mpstatus-info.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4e493-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="4e493-119">Return value</span></span>

<span data-ttu-id="4e493-120">類型： **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="4e493-120">Type: **HRESULT**</span></span>

<span data-ttu-id="4e493-121">如果函式成功，則傳回值為 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="4e493-121">If the function succeeds the return value is **S\_OK**.</span></span> <span data-ttu-id="4e493-122">即使反惡意程式碼服務不在執行中，此函式呼叫仍會成功。</span><span class="sxs-lookup"><span data-stu-id="4e493-122">This function call is guaranteed to succeed even if an AntiMalware service is not running.</span></span>

<span data-ttu-id="4e493-123">如果函式失敗，則傳回值會是失敗的 **HRESULT** 程式碼。</span><span class="sxs-lookup"><span data-stu-id="4e493-123">If the function fails then the return value is a failed **HRESULT** code.</span></span> <span data-ttu-id="4e493-124">呼叫端可以使用 [**MpErrorMessageFormat**](mperrormessageformat.md) 函數來取得錯誤訊息的一般描述。</span><span class="sxs-lookup"><span data-stu-id="4e493-124">The caller can use the [**MpErrorMessageFormat**](mperrormessageformat.md) function to get a generic description of the error message.</span></span>

## <a name="requirements"></a><span data-ttu-id="4e493-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="4e493-125">Requirements</span></span>



| <span data-ttu-id="4e493-126">需求</span><span class="sxs-lookup"><span data-stu-id="4e493-126">Requirement</span></span> | <span data-ttu-id="4e493-127">值</span><span class="sxs-lookup"><span data-stu-id="4e493-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4e493-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4e493-128">Minimum supported client</span></span><br/> | <span data-ttu-id="4e493-129">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4e493-129">Windows 8 \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="4e493-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4e493-130">Minimum supported server</span></span><br/> | <span data-ttu-id="4e493-131">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4e493-131">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="4e493-132">標頭</span><span class="sxs-lookup"><span data-stu-id="4e493-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="4e493-133"><dt>MpClient。h</dt></span><span class="sxs-lookup"><span data-stu-id="4e493-133"><dt>MpClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="4e493-134">DLL</span><span class="sxs-lookup"><span data-stu-id="4e493-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4e493-135"><dt>MpClient.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4e493-135"><dt>MpClient.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4e493-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4e493-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4e493-137">**MpErrorMessageFormat**</span><span class="sxs-lookup"><span data-stu-id="4e493-137">**MpErrorMessageFormat**</span></span>](mperrormessageformat.md)
</dt> <dt>

[<span data-ttu-id="4e493-138">**MpManagerOpen**</span><span class="sxs-lookup"><span data-stu-id="4e493-138">**MpManagerOpen**</span></span>](mpmanageropen.md)
</dt> <dt>

[<span data-ttu-id="4e493-139">**MpManagerStatusQueryEx**</span><span class="sxs-lookup"><span data-stu-id="4e493-139">**MpManagerStatusQueryEx**</span></span>](mpmanagerstatusqueryex.md)
</dt> <dt>

[<span data-ttu-id="4e493-140">**MPSTATUS \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="4e493-140">**MPSTATUS\_INFO**</span></span>](mpstatus-info.md)
</dt> </dl>

 

 





