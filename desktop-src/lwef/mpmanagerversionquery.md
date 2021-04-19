---
title: 'MpManagerVersionQuery 函式 (MpClient) '
description: 傳回惡意程式碼防護管理員各元件的版本資訊。
ms.assetid: 47DE12BF-D7A4-468B-B0E7-79B5C27E56F5
keywords:
- MpManagerVersionQuery 函式舊版 Windows 環境功能
topic_type:
- apiref
api_name:
- MpManagerVersionQuery
api_location:
- MpClient.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a841a83d8ceb828de0a5a9cd80f5f5bdc7f5c914
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106969185"
---
# <a name="mpmanagerversionquery-function"></a><span data-ttu-id="b22d1-104">MpManagerVersionQuery 函式</span><span class="sxs-lookup"><span data-stu-id="b22d1-104">MpManagerVersionQuery function</span></span>

<span data-ttu-id="b22d1-105">傳回惡意程式碼防護管理員各元件的版本資訊。</span><span class="sxs-lookup"><span data-stu-id="b22d1-105">Returns version information about various components of the malware protection manager.</span></span>

## <a name="syntax"></a><span data-ttu-id="b22d1-106">語法</span><span class="sxs-lookup"><span data-stu-id="b22d1-106">Syntax</span></span>


```C++
HRESULT WINAPI MpManagerVersionQuery(
  _In_  MPHANDLE        hMpHandle,
  _Out_ PMPVERSION_INFO pVersionInfo
);
```



## <a name="parameters"></a><span data-ttu-id="b22d1-107">參數</span><span class="sxs-lookup"><span data-stu-id="b22d1-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b22d1-108">*hMpHandle* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b22d1-108">*hMpHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b22d1-109">類型： **MPHANDLE**</span><span class="sxs-lookup"><span data-stu-id="b22d1-109">Type: **MPHANDLE**</span></span>

<span data-ttu-id="b22d1-110">惡意程式碼防護管理員介面的控制碼。</span><span class="sxs-lookup"><span data-stu-id="b22d1-110">Handle to the malware protection manager interface.</span></span> <span data-ttu-id="b22d1-111">[**MpManagerOpen**](mpmanageropen.md)函數會傳回這個控制碼。</span><span class="sxs-lookup"><span data-stu-id="b22d1-111">This handle is returned by the [**MpManagerOpen**](mpmanageropen.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="b22d1-112">*pVersionInfo* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="b22d1-112">*pVersionInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b22d1-113">類型： **PMPVERSION \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="b22d1-113">Type: **PMPVERSION\_INFO**</span></span>

<span data-ttu-id="b22d1-114">結構的指標，其中包含有關惡意程式碼防護管理員各元件的版本資訊。</span><span class="sxs-lookup"><span data-stu-id="b22d1-114">Pointer to a structure that contains version information about various components of the malware protection manager.</span></span> <span data-ttu-id="b22d1-115">請參閱 [**MPVERSION \_ 資訊**](mpversion-info.md)。</span><span class="sxs-lookup"><span data-stu-id="b22d1-115">See [**MPVERSION\_INFO**](mpversion-info.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b22d1-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="b22d1-116">Return value</span></span>

<span data-ttu-id="b22d1-117">類型： **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="b22d1-117">Type: **HRESULT**</span></span>

<span data-ttu-id="b22d1-118">如果函式成功，則傳回值為 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="b22d1-118">If the function succeeds the return value is **S\_OK**.</span></span>

<span data-ttu-id="b22d1-119">如果函式失敗，則傳回值會是失敗的 **HRESULT** 程式碼。</span><span class="sxs-lookup"><span data-stu-id="b22d1-119">If the function fails then the return value is a failed **HRESULT** code.</span></span> <span data-ttu-id="b22d1-120">呼叫端可以使用 [**MpErrorMessageFormat**](mperrormessageformat.md) 函數來取得錯誤訊息的一般描述。</span><span class="sxs-lookup"><span data-stu-id="b22d1-120">The caller can use the [**MpErrorMessageFormat**](mperrormessageformat.md) function to get a generic description of the error message.</span></span>

## <a name="requirements"></a><span data-ttu-id="b22d1-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="b22d1-121">Requirements</span></span>



| <span data-ttu-id="b22d1-122">需求</span><span class="sxs-lookup"><span data-stu-id="b22d1-122">Requirement</span></span> | <span data-ttu-id="b22d1-123">值</span><span class="sxs-lookup"><span data-stu-id="b22d1-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b22d1-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b22d1-124">Minimum supported client</span></span><br/> | <span data-ttu-id="b22d1-125">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b22d1-125">Windows 8 \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="b22d1-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b22d1-126">Minimum supported server</span></span><br/> | <span data-ttu-id="b22d1-127">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b22d1-127">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="b22d1-128">標頭</span><span class="sxs-lookup"><span data-stu-id="b22d1-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="b22d1-129"><dt>MpClient。h</dt></span><span class="sxs-lookup"><span data-stu-id="b22d1-129"><dt>MpClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="b22d1-130">DLL</span><span class="sxs-lookup"><span data-stu-id="b22d1-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b22d1-131"><dt>MpClient.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b22d1-131"><dt>MpClient.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b22d1-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b22d1-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b22d1-133">**MpErrorMessageFormat**</span><span class="sxs-lookup"><span data-stu-id="b22d1-133">**MpErrorMessageFormat**</span></span>](mperrormessageformat.md)
</dt> <dt>

[<span data-ttu-id="b22d1-134">**MpManagerOpen**</span><span class="sxs-lookup"><span data-stu-id="b22d1-134">**MpManagerOpen**</span></span>](mpmanageropen.md)
</dt> <dt>

[<span data-ttu-id="b22d1-135">**MPVERSION \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="b22d1-135">**MPVERSION\_INFO**</span></span>](mpversion-info.md)
</dt> </dl>

 

 





