---
title: 'MpErrorMessageFormat 函式 (MpClient) '
description: 根據錯誤碼傳回格式化的錯誤訊息。
ms.assetid: C125FCE4-3BB0-4608-BBF3-E7FEF17D0807
keywords:
- MpErrorMessageFormat 函式舊版 Windows 環境功能
topic_type:
- apiref
api_name:
- MpErrorMessageFormat
api_location:
- MpClient.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a3499b3be885b29135d22b470da4143cfb23ea6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934953"
---
# <a name="mperrormessageformat-function"></a><span data-ttu-id="97670-104">MpErrorMessageFormat 函式</span><span class="sxs-lookup"><span data-stu-id="97670-104">MpErrorMessageFormat function</span></span>

<span data-ttu-id="97670-105">根據錯誤碼傳回格式化的錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="97670-105">Returns a formatted error message based on an error code.</span></span>

## <a name="syntax"></a><span data-ttu-id="97670-106">語法</span><span class="sxs-lookup"><span data-stu-id="97670-106">Syntax</span></span>


```C++
HRESULT WINAPI MpErrorMessageFormat(
  _In_  MPHANDLE hMpHandle,
  _In_  HRESULT  hrError,
  _Out_ LPWSTR   *pwszErrorDesc
);
```



## <a name="parameters"></a><span data-ttu-id="97670-107">參數</span><span class="sxs-lookup"><span data-stu-id="97670-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="97670-108">*hMpHandle* \[在\]</span><span class="sxs-lookup"><span data-stu-id="97670-108">*hMpHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="97670-109">類型： **MPHANDLE**</span><span class="sxs-lookup"><span data-stu-id="97670-109">Type: **MPHANDLE**</span></span>

<span data-ttu-id="97670-110">惡意程式碼防護管理員介面的控制碼。</span><span class="sxs-lookup"><span data-stu-id="97670-110">Handle to the malware protection manager interface.</span></span> <span data-ttu-id="97670-111">[**MpManagerOpen**](mpmanageropen.md)函數會傳回這個控制碼。</span><span class="sxs-lookup"><span data-stu-id="97670-111">This handle is returned by the [**MpManagerOpen**](mpmanageropen.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="97670-112">*hrError* \[在\]</span><span class="sxs-lookup"><span data-stu-id="97670-112">*hrError* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="97670-113">類型： **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="97670-113">Type: **HRESULT**</span></span>

<span data-ttu-id="97670-114">以 **HRESULT** 為基礎的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="97670-114">An **HRESULT**-based error code.</span></span>

</dd> <dt>

<span data-ttu-id="97670-115">*pwszErrorDesc* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="97670-115">*pwszErrorDesc* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="97670-116">類型： \**LPWSTR \** _</span><span class="sxs-lookup"><span data-stu-id="97670-116">Type: \**LPWSTR\** _</span></span>

<span data-ttu-id="97670-117">根據 _hrError \* 傳回格式化的錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="97670-117">Returns a formatted error message based on _hrError\*.</span></span> <span data-ttu-id="97670-118">您必須使用 [**MpFreeMemory**](mpfreememory.md)來釋放這個字串。</span><span class="sxs-lookup"><span data-stu-id="97670-118">This string must be freed using [**MpFreeMemory**](mpfreememory.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="97670-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="97670-119">Return value</span></span>

<span data-ttu-id="97670-120">類型： **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="97670-120">Type: **HRESULT**</span></span>

<span data-ttu-id="97670-121">如果函式成功，則傳回值為 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="97670-121">If the function succeeds the return value is **S\_OK**.</span></span>

<span data-ttu-id="97670-122">如果函式失敗，則傳回值會是失敗的 **HRESULT** 程式碼。</span><span class="sxs-lookup"><span data-stu-id="97670-122">If the function fails then the return value is a failed **HRESULT** code.</span></span>

## <a name="remarks"></a><span data-ttu-id="97670-123">備註</span><span class="sxs-lookup"><span data-stu-id="97670-123">Remarks</span></span>

<span data-ttu-id="97670-124">除了惡意程式碼防護函式所傳回的特定錯誤碼之外，此函數還能夠格式化系統錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="97670-124">This function is capable of formatting system error codes in addition to specific error codes returned by malware protection functions.</span></span> <span data-ttu-id="97670-125">惡意程式碼防護功能特定的 **HRESULT** 錯誤碼有0x50 的功能。</span><span class="sxs-lookup"><span data-stu-id="97670-125">The **HRESULT** error codes specific to malware protection functions have a facility of 0x50.</span></span> <span data-ttu-id="97670-126">以下是可由各種惡意程式碼防護功能傳回的惡意程式碼防護特定錯誤碼的清單。</span><span class="sxs-lookup"><span data-stu-id="97670-126">Below is a list of a subset of the malware protection-specific error codes that can be returned by various malware protection functions.</span></span> <span data-ttu-id="97670-127">使用 **\_ 來自 \_ MP \_ 狀態** 的宏 HRESULT，可將下列錯誤碼轉換成 **HRESULT**。</span><span class="sxs-lookup"><span data-stu-id="97670-127">Using the macro **HRESULT\_FROM\_MP\_STATUS**, the following error codes can be converted to **HRESULT**.</span></span> <span data-ttu-id="97670-128">另請參閱 [Forefront Client Security 反惡意程式碼引擎錯誤碼](https://support.microsoft.com/kb/939359) ，以取得其他可能錯誤碼的清單。</span><span class="sxs-lookup"><span data-stu-id="97670-128">See also [Forefront Client Security anti-malware engine error codes](https://support.microsoft.com/kb/939359) for a list of other possible error codes.</span></span>



| <span data-ttu-id="97670-129">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="97670-129">Error Code</span></span>                              | <span data-ttu-id="97670-130">描述</span><span class="sxs-lookup"><span data-stu-id="97670-130">Description</span></span>                                                                                                                 |
|-----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="97670-131">錯誤 \_ MP \_ NOENGINE</span><span class="sxs-lookup"><span data-stu-id="97670-131">ERROR\_MP\_NOENGINE</span></span>                     | <span data-ttu-id="97670-132">未在反惡意程式碼服務中載入引擎以執行要求的操作。</span><span class="sxs-lookup"><span data-stu-id="97670-132">No engine is loaded in antimalware service to perform the requested operation.</span></span>                                              |
| <span data-ttu-id="97670-133">錯誤 \_ MP \_ 沒有 \_ 記憶體</span><span class="sxs-lookup"><span data-stu-id="97670-133">ERROR\_MP\_NO\_MEMORY</span></span>                   | <span data-ttu-id="97670-134">反惡意程式碼引擎發生記憶體不足的情況。</span><span class="sxs-lookup"><span data-stu-id="97670-134">The antimalware engine has encountered a no memory situation.</span></span>                                                               |
| <span data-ttu-id="97670-135">錯誤 \_ MP \_ 移除 \_ 失敗</span><span class="sxs-lookup"><span data-stu-id="97670-135">ERROR\_MP\_REMOVE\_FAILED</span></span>               | <span data-ttu-id="97670-136">特定威脅的移除作業失敗。</span><span class="sxs-lookup"><span data-stu-id="97670-136">Remove operation failed for a specific threat.</span></span>                                                                              |
| <span data-ttu-id="97670-137">錯誤 \_ MP \_ 隔離 \_ 失敗</span><span class="sxs-lookup"><span data-stu-id="97670-137">ERROR\_MP\_QUARANTINE\_FAILED</span></span>           | <span data-ttu-id="97670-138">特定威脅的隔離操作失敗。</span><span class="sxs-lookup"><span data-stu-id="97670-138">Quarantine operation failed for a specific threat.</span></span>                                                                          |
| <span data-ttu-id="97670-139">\_ \_ \_ \_ 找不到錯誤 MP 威脅</span><span class="sxs-lookup"><span data-stu-id="97670-139">ERROR\_MP\_THREAT\_NOT\_FOUND</span></span>           | <span data-ttu-id="97670-140">系統中已不再有特定威脅。</span><span class="sxs-lookup"><span data-stu-id="97670-140">The specific threat no longer exists in the system.</span></span>                                                                         |
| <span data-ttu-id="97670-141">\_ \_ \_ 不支援錯誤 MP \_ 移除</span><span class="sxs-lookup"><span data-stu-id="97670-141">ERROR\_MP\_REMOVE\_NOT\_SUPPORTED</span></span>       | <span data-ttu-id="97670-142">不支援對容器類型內的特定威脅進行移除操作。</span><span class="sxs-lookup"><span data-stu-id="97670-142">Remove operation for a specific threat inside the container type is not supported.</span></span>                                          |
| <span data-ttu-id="97670-143">錯誤 \_ MP \_ 移除 \_ 不可變的 \_ 容器</span><span class="sxs-lookup"><span data-stu-id="97670-143">ERROR\_MP\_REMOVE\_IMMUTABLE\_CONTAINER</span></span> | <span data-ttu-id="97670-144">由於引擎原則，不支援在已封鎖容器內的特定威脅移除作業。</span><span class="sxs-lookup"><span data-stu-id="97670-144">Due to engine policy, a remove operation of a specific threat inside a blocked container is not supported.</span></span> <span data-ttu-id="97670-145"> (Mail 封存。 ) </span><span class="sxs-lookup"><span data-stu-id="97670-145">(Mail archives.)</span></span> |
| <span data-ttu-id="97670-146">錯誤 \_ MP \_ BADDB \_ OLDENGINE</span><span class="sxs-lookup"><span data-stu-id="97670-146">ERROR\_MP\_BADDB\_OLDENGINE</span></span>             | <span data-ttu-id="97670-147">簽章更新要求 (s) ，提供了較舊的引擎或簽章檔案。</span><span class="sxs-lookup"><span data-stu-id="97670-147">Signature update request provided an older engine or signature files(s).</span></span>                                                    |



 

## <a name="requirements"></a><span data-ttu-id="97670-148">規格需求</span><span class="sxs-lookup"><span data-stu-id="97670-148">Requirements</span></span>



| <span data-ttu-id="97670-149">需求</span><span class="sxs-lookup"><span data-stu-id="97670-149">Requirement</span></span> | <span data-ttu-id="97670-150">值</span><span class="sxs-lookup"><span data-stu-id="97670-150">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="97670-151">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="97670-151">Minimum supported client</span></span><br/> | <span data-ttu-id="97670-152">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="97670-152">Windows 8 \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="97670-153">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="97670-153">Minimum supported server</span></span><br/> | <span data-ttu-id="97670-154">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="97670-154">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="97670-155">標頭</span><span class="sxs-lookup"><span data-stu-id="97670-155">Header</span></span><br/>                   | <dl> <span data-ttu-id="97670-156"><dt>MpClient。h</dt></span><span class="sxs-lookup"><span data-stu-id="97670-156"><dt>MpClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="97670-157">DLL</span><span class="sxs-lookup"><span data-stu-id="97670-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="97670-158"><dt>MpClient.dll</dt></span><span class="sxs-lookup"><span data-stu-id="97670-158"><dt>MpClient.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="97670-159">另請參閱</span><span class="sxs-lookup"><span data-stu-id="97670-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="97670-160">**MpFreeMemory**</span><span class="sxs-lookup"><span data-stu-id="97670-160">**MpFreeMemory**</span></span>](mpfreememory.md)
</dt> <dt>

[<span data-ttu-id="97670-161">**MpManagerOpen**</span><span class="sxs-lookup"><span data-stu-id="97670-161">**MpManagerOpen**</span></span>](mpmanageropen.md)
</dt> <dt>

[<span data-ttu-id="97670-162">Forefront Client Security 反惡意程式碼引擎錯誤碼</span><span class="sxs-lookup"><span data-stu-id="97670-162">Forefront Client Security anti-malware engine error codes</span></span>](https://support.microsoft.com/kb/939359)
</dt> </dl>

 

 





