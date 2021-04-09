---
title: 'MpThreatEnumerate 函式 (MpClient) '
description: 傳回列舉清單中下一個威脅的相關資訊。 您可以重複呼叫這個函式，直到所有威脅的列舉都完成為止。
ms.assetid: 33244F4F-4FB7-4FA7-BC56-B9A30ABC3644
keywords:
- MpThreatEnumerate 函式舊版 Windows 環境功能
topic_type:
- apiref
api_name:
- MpThreatEnumerate
api_location:
- MpClient.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: acdbb7971371015a401c1a951ace8c55869fd405
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934743"
---
# <a name="mpthreatenumerate-function"></a><span data-ttu-id="27bfd-105">MpThreatEnumerate 函式</span><span class="sxs-lookup"><span data-stu-id="27bfd-105">MpThreatEnumerate function</span></span>

<span data-ttu-id="27bfd-106">傳回列舉清單中下一個威脅的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="27bfd-106">Returns information about the next threat in the enumeration list.</span></span> <span data-ttu-id="27bfd-107">您可以重複呼叫這個函式，直到所有威脅的列舉都完成為止。</span><span class="sxs-lookup"><span data-stu-id="27bfd-107">This function can be called repeatedly until the enumeration of all the threats is complete.</span></span>

## <a name="syntax"></a><span data-ttu-id="27bfd-108">語法</span><span class="sxs-lookup"><span data-stu-id="27bfd-108">Syntax</span></span>


```C++
HRESULT WINAPI MpThreatEnumerate(
  _In_  MPHANDLE       hThreatEnumHandle,
  _Out_ PMPTHREAT_INFO *ppThreatInfo
);
```



## <a name="parameters"></a><span data-ttu-id="27bfd-109">參數</span><span class="sxs-lookup"><span data-stu-id="27bfd-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="27bfd-110">*hThreatEnumHandle* \[在\]</span><span class="sxs-lookup"><span data-stu-id="27bfd-110">*hThreatEnumHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="27bfd-111">類型： **MPHANDLE**</span><span class="sxs-lookup"><span data-stu-id="27bfd-111">Type: **MPHANDLE**</span></span>

<span data-ttu-id="27bfd-112">[**MpThreatOpen**](mpthreatopen.md)所傳回的威脅列舉內容控制碼。</span><span class="sxs-lookup"><span data-stu-id="27bfd-112">Handle to a threat enumeration context returned by [**MpThreatOpen**](mpthreatopen.md).</span></span>

</dd> <dt>

<span data-ttu-id="27bfd-113">*ppThreatInfo* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="27bfd-113">*ppThreatInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="27bfd-114">類型： \**PMPTHREAT \_ INFO \** _</span><span class="sxs-lookup"><span data-stu-id="27bfd-114">Type: \**PMPTHREAT\_INFO\** _</span></span>

<span data-ttu-id="27bfd-115">傳回威脅資訊結構的指標 [_ *MPTHREAT \_ 資訊* \*](mpthreat-info.md)。</span><span class="sxs-lookup"><span data-stu-id="27bfd-115">Returns a pointer to a threat information structure, [_ *MPTHREAT\_INFO*\*](mpthreat-info.md).</span></span> <span data-ttu-id="27bfd-116">結構包含威脅識別碼、名稱和嚴重性等資訊。</span><span class="sxs-lookup"><span data-stu-id="27bfd-116">The structure contains information such as threat id, name, and severity.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="27bfd-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="27bfd-117">Return value</span></span>

<span data-ttu-id="27bfd-118">類型： **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="27bfd-118">Type: **HRESULT**</span></span>

<span data-ttu-id="27bfd-119">如果函式成功，則傳回值為 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="27bfd-119">If the function succeeds the return value is **S\_OK**.</span></span>

<span data-ttu-id="27bfd-120">如果沒有其他專案可傳回傳回值，則為 **\_ FALSE**。</span><span class="sxs-lookup"><span data-stu-id="27bfd-120">If there are no more items to return the return value is **S\_FALSE**.</span></span>

<span data-ttu-id="27bfd-121">如果函式失敗，則傳回值會是失敗的 **HRESULT** 程式碼。</span><span class="sxs-lookup"><span data-stu-id="27bfd-121">If the function fails then the return value is a failed **HRESULT** code.</span></span> <span data-ttu-id="27bfd-122">呼叫端可以使用 [**MpErrorMessageFormat**](mperrormessageformat.md) 函數來取得錯誤訊息的一般描述。</span><span class="sxs-lookup"><span data-stu-id="27bfd-122">The caller can use the [**MpErrorMessageFormat**](mperrormessageformat.md) function to get a generic description of the error message.</span></span>

## <a name="requirements"></a><span data-ttu-id="27bfd-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="27bfd-123">Requirements</span></span>



| <span data-ttu-id="27bfd-124">需求</span><span class="sxs-lookup"><span data-stu-id="27bfd-124">Requirement</span></span> | <span data-ttu-id="27bfd-125">值</span><span class="sxs-lookup"><span data-stu-id="27bfd-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="27bfd-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="27bfd-126">Minimum supported client</span></span><br/> | <span data-ttu-id="27bfd-127">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="27bfd-127">Windows 8 \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="27bfd-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="27bfd-128">Minimum supported server</span></span><br/> | <span data-ttu-id="27bfd-129">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="27bfd-129">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="27bfd-130">標頭</span><span class="sxs-lookup"><span data-stu-id="27bfd-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="27bfd-131"><dt>MpClient。h</dt></span><span class="sxs-lookup"><span data-stu-id="27bfd-131"><dt>MpClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="27bfd-132">DLL</span><span class="sxs-lookup"><span data-stu-id="27bfd-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="27bfd-133"><dt>MpClient.dll</dt></span><span class="sxs-lookup"><span data-stu-id="27bfd-133"><dt>MpClient.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="27bfd-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="27bfd-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="27bfd-135">**MpErrorMessageFormat**</span><span class="sxs-lookup"><span data-stu-id="27bfd-135">**MpErrorMessageFormat**</span></span>](mperrormessageformat.md)
</dt> <dt>

[<span data-ttu-id="27bfd-136">**MpThreatOpen**</span><span class="sxs-lookup"><span data-stu-id="27bfd-136">**MpThreatOpen**</span></span>](mpthreatopen.md)
</dt> <dt>

[<span data-ttu-id="27bfd-137">**MPTHREAT \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="27bfd-137">**MPTHREAT\_INFO**</span></span>](mpthreat-info.md)
</dt> </dl>

 

 





