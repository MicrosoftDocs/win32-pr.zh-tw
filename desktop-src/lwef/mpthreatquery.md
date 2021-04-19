---
title: 'MpThreatQuery 函式 (MpClient) '
description: 用來查詢靜態 (（例如嚴重性和類別）) 或當地語系化的 (例如類別描述和建議) 特定威脅的相關資訊。
ms.assetid: A06854B2-8444-46A4-A53F-FD5FEAFF47B7
keywords:
- MpThreatQuery 函式舊版 Windows 環境功能
topic_type:
- apiref
api_name:
- MpThreatQuery
api_location:
- MpClient.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 21d38a3734f9d98f3bd61143d4fe58bd606c7508
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106966101"
---
# <a name="mpthreatquery-function"></a><span data-ttu-id="6463c-104">MpThreatQuery 函式</span><span class="sxs-lookup"><span data-stu-id="6463c-104">MpThreatQuery function</span></span>

<span data-ttu-id="6463c-105">用來查詢靜態 (（例如嚴重性和類別）) 或當地語系化的 (例如類別描述和建議) 特定威脅的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="6463c-105">Used to query static (such as severity and category) or localized (such as category description and advice) information about a particular threat.</span></span>

## <a name="syntax"></a><span data-ttu-id="6463c-106">語法</span><span class="sxs-lookup"><span data-stu-id="6463c-106">Syntax</span></span>


```C++
HRESULT WINAPI MpThreatQuery(
  _In_      MPHANDLE                 hMpHandle,
  _In_      MPTHREAT_ID              ThreatID,
  _Out_     PMPTHREAT_INFO           *ppThreatInfo,
  _Out_opt_ PMPTHREAT_LOCALIZED_INFO *ppThreatLocalizedInfo
);
```



## <a name="parameters"></a><span data-ttu-id="6463c-107">參數</span><span class="sxs-lookup"><span data-stu-id="6463c-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6463c-108">*hMpHandle* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6463c-108">*hMpHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6463c-109">類型： **MPHANDLE**</span><span class="sxs-lookup"><span data-stu-id="6463c-109">Type: **MPHANDLE**</span></span>

<span data-ttu-id="6463c-110">惡意程式碼防護管理員介面的控制碼。</span><span class="sxs-lookup"><span data-stu-id="6463c-110">Handle to the malware protection manager interface.</span></span> <span data-ttu-id="6463c-111">[**MpManagerOpen**](mpmanageropen.md)函數會傳回這個控制碼。</span><span class="sxs-lookup"><span data-stu-id="6463c-111">This handle is returned by the [**MpManagerOpen**](mpmanageropen.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="6463c-112">*ThreatID* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6463c-112">*ThreatID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6463c-113">類型： **MPTHREAT \_ 識別碼**</span><span class="sxs-lookup"><span data-stu-id="6463c-113">Type: **MPTHREAT\_ID**</span></span>

<span data-ttu-id="6463c-114">要求資訊的威脅識別碼。</span><span class="sxs-lookup"><span data-stu-id="6463c-114">Threat identifier for which information is requested.</span></span>

</dd> <dt>

<span data-ttu-id="6463c-115">*ppThreatInfo* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="6463c-115">*ppThreatInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6463c-116">類型： \**PMPTHREAT \_ INFO \** _</span><span class="sxs-lookup"><span data-stu-id="6463c-116">Type: \**PMPTHREAT\_INFO\** _</span></span>

<span data-ttu-id="6463c-117">傳回威脅資訊結構的指標 [_ *MPTHREAT \_ 資訊* \*](mpthreat-info.md)。</span><span class="sxs-lookup"><span data-stu-id="6463c-117">Returns a pointer to a threat information structure, [_ *MPTHREAT\_INFO*\*](mpthreat-info.md).</span></span> <span data-ttu-id="6463c-118">結構包含威脅識別碼、名稱和嚴重性等資訊。</span><span class="sxs-lookup"><span data-stu-id="6463c-118">The structure contains information such as threat id, name, and severity.</span></span>

</dd> <dt>

<span data-ttu-id="6463c-119">*ppThreatLocalizedInfo* \[out、optional\]</span><span class="sxs-lookup"><span data-stu-id="6463c-119">*ppThreatLocalizedInfo* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="6463c-120">類型： \**PMPTHREAT \_ 當地語系化 \_ 的 \* 資訊* _</span><span class="sxs-lookup"><span data-stu-id="6463c-120">Type: \**PMPTHREAT\_LOCALIZED\_INFO\** _</span></span>

<span data-ttu-id="6463c-121">傳回結構的指標，其中包含有關威脅的當地語系化資訊。</span><span class="sxs-lookup"><span data-stu-id="6463c-121">Returns a pointer to a structure containing localized information about the threat.</span></span> <span data-ttu-id="6463c-122">如果您對威脅的當地語系化資訊不感興趣，您可以傳遞 _ \*Null\*\*。</span><span class="sxs-lookup"><span data-stu-id="6463c-122">You can pass _ *NULL*\* if you are not interested in localized information about the threat.</span></span> <span data-ttu-id="6463c-123">請參閱 [**MPTHREAT \_ 當地語系化 \_ 資訊**](mpthreat-localized-info.md)。</span><span class="sxs-lookup"><span data-stu-id="6463c-123">See [**MPTHREAT\_LOCALIZED\_INFO**](mpthreat-localized-info.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6463c-124">傳回值</span><span class="sxs-lookup"><span data-stu-id="6463c-124">Return value</span></span>

<span data-ttu-id="6463c-125">類型： **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="6463c-125">Type: **HRESULT**</span></span>

<span data-ttu-id="6463c-126">如果函式成功，則傳回值為 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="6463c-126">If the function succeeds the return value is **S\_OK**.</span></span>

<span data-ttu-id="6463c-127">如果函式失敗，則傳回值會是失敗的 **HRESULT** 程式碼。</span><span class="sxs-lookup"><span data-stu-id="6463c-127">If the function fails then the return value is a failed **HRESULT** code.</span></span> <span data-ttu-id="6463c-128">呼叫端可以使用 [**MpErrorMessageFormat**](mperrormessageformat.md) 函數來取得錯誤訊息的一般描述。</span><span class="sxs-lookup"><span data-stu-id="6463c-128">The caller can use the [**MpErrorMessageFormat**](mperrormessageformat.md) function to get a generic description of the error message.</span></span>

## <a name="requirements"></a><span data-ttu-id="6463c-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="6463c-129">Requirements</span></span>



| <span data-ttu-id="6463c-130">需求</span><span class="sxs-lookup"><span data-stu-id="6463c-130">Requirement</span></span> | <span data-ttu-id="6463c-131">值</span><span class="sxs-lookup"><span data-stu-id="6463c-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6463c-132">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6463c-132">Minimum supported client</span></span><br/> | <span data-ttu-id="6463c-133">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6463c-133">Windows 8 \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="6463c-134">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6463c-134">Minimum supported server</span></span><br/> | <span data-ttu-id="6463c-135">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6463c-135">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="6463c-136">標頭</span><span class="sxs-lookup"><span data-stu-id="6463c-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="6463c-137"><dt>MpClient。h</dt></span><span class="sxs-lookup"><span data-stu-id="6463c-137"><dt>MpClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="6463c-138">DLL</span><span class="sxs-lookup"><span data-stu-id="6463c-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6463c-139"><dt>MpClient.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6463c-139"><dt>MpClient.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6463c-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6463c-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6463c-141">**MpErrorMessageFormat**</span><span class="sxs-lookup"><span data-stu-id="6463c-141">**MpErrorMessageFormat**</span></span>](mperrormessageformat.md)
</dt> <dt>

[<span data-ttu-id="6463c-142">**MpManagerOpen**</span><span class="sxs-lookup"><span data-stu-id="6463c-142">**MpManagerOpen**</span></span>](mpmanageropen.md)
</dt> <dt>

[<span data-ttu-id="6463c-143">**MPTHREAT \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="6463c-143">**MPTHREAT\_INFO**</span></span>](mpthreat-info.md)
</dt> <dt>

[<span data-ttu-id="6463c-144">**MPTHREAT \_ 當地語系化的 \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="6463c-144">**MPTHREAT\_LOCALIZED\_INFO**</span></span>](mpthreat-localized-info.md)
</dt> </dl>

 

 





