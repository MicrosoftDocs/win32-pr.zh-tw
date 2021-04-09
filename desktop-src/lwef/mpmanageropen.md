---
title: 'MpManagerOpen 函式 (MpClient) '
description: 在本機電腦上建立與惡意程式碼防護管理員的連接。
ms.assetid: 40513A74-AFCC-4E22-9B78-D46FEB575A00
keywords:
- MpManagerOpen 函式舊版 Windows 環境功能
topic_type:
- apiref
api_name:
- MpManagerOpen
api_location:
- MpClient.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af432cc7d91530fd3d37176592f7f457b31b6314
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686328"
---
# <a name="mpmanageropen-function"></a><span data-ttu-id="3a5b2-104">MpManagerOpen 函式</span><span class="sxs-lookup"><span data-stu-id="3a5b2-104">MpManagerOpen function</span></span>

<span data-ttu-id="3a5b2-105">在本機電腦上建立與惡意程式碼防護管理員的連接。</span><span class="sxs-lookup"><span data-stu-id="3a5b2-105">Establishes a connection to the malware protection manager on the local computer.</span></span>

## <a name="syntax"></a><span data-ttu-id="3a5b2-106">語法</span><span class="sxs-lookup"><span data-stu-id="3a5b2-106">Syntax</span></span>


```C++
HRESULT WINAPI MpManagerOpen(
  _In_  DWORD     dwReserved,
  _Out_ PMPHANDLE phMpHandle
);
```



## <a name="parameters"></a><span data-ttu-id="3a5b2-107">參數</span><span class="sxs-lookup"><span data-stu-id="3a5b2-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3a5b2-108">*>dwreserved* \[在\]</span><span class="sxs-lookup"><span data-stu-id="3a5b2-108">*dwReserved* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3a5b2-109">類型： **DWORD**</span><span class="sxs-lookup"><span data-stu-id="3a5b2-109">Type: **DWORD**</span></span>

<span data-ttu-id="3a5b2-110">保留供未來使用。</span><span class="sxs-lookup"><span data-stu-id="3a5b2-110">Reserved for future use.</span></span> <span data-ttu-id="3a5b2-111">必須設定為 0。</span><span class="sxs-lookup"><span data-stu-id="3a5b2-111">Must be set to 0.</span></span>

</dd> <dt>

<span data-ttu-id="3a5b2-112">*phMpHandle* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="3a5b2-112">*phMpHandle* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3a5b2-113">類型： **PMPHANDLE**</span><span class="sxs-lookup"><span data-stu-id="3a5b2-113">Type: **PMPHANDLE**</span></span>

<span data-ttu-id="3a5b2-114">惡意程式碼防護管理員介面的控制碼。</span><span class="sxs-lookup"><span data-stu-id="3a5b2-114">Handle to the malware protection manager interface.</span></span> <span data-ttu-id="3a5b2-115">您必須使用 [**MpHandleClose**](mphandleclose.md) 函式來關閉此控制碼。</span><span class="sxs-lookup"><span data-stu-id="3a5b2-115">This handle must be closed with the [**MpHandleClose**](mphandleclose.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3a5b2-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="3a5b2-116">Return value</span></span>

<span data-ttu-id="3a5b2-117">類型： **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="3a5b2-117">Type: **HRESULT**</span></span>

<span data-ttu-id="3a5b2-118">如果函式成功，則傳回值為 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="3a5b2-118">If the function succeeds the return value is **S\_OK**.</span></span> <span data-ttu-id="3a5b2-119">即使反惡意程式碼服務不在執行中，此函式呼叫仍會成功。</span><span class="sxs-lookup"><span data-stu-id="3a5b2-119">This function call is guaranteed to succeed even if an AntiMalware service is not running.</span></span>

<span data-ttu-id="3a5b2-120">如果函式失敗，則傳回值會是失敗的 **HRESULT** 程式碼。</span><span class="sxs-lookup"><span data-stu-id="3a5b2-120">If the function fails then the return value is a failed **HRESULT** code.</span></span> <span data-ttu-id="3a5b2-121">呼叫端可以使用 [**MpErrorMessageFormat**](mperrormessageformat.md) 函數來取得錯誤訊息的一般描述。</span><span class="sxs-lookup"><span data-stu-id="3a5b2-121">The caller can use the [**MpErrorMessageFormat**](mperrormessageformat.md) function to get a generic description of the error message.</span></span>

## <a name="requirements"></a><span data-ttu-id="3a5b2-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="3a5b2-122">Requirements</span></span>



| <span data-ttu-id="3a5b2-123">需求</span><span class="sxs-lookup"><span data-stu-id="3a5b2-123">Requirement</span></span> | <span data-ttu-id="3a5b2-124">值</span><span class="sxs-lookup"><span data-stu-id="3a5b2-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3a5b2-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3a5b2-125">Minimum supported client</span></span><br/> | <span data-ttu-id="3a5b2-126">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3a5b2-126">Windows 8 \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="3a5b2-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3a5b2-127">Minimum supported server</span></span><br/> | <span data-ttu-id="3a5b2-128">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3a5b2-128">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="3a5b2-129">標頭</span><span class="sxs-lookup"><span data-stu-id="3a5b2-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="3a5b2-130"><dt>MpClient。h</dt></span><span class="sxs-lookup"><span data-stu-id="3a5b2-130"><dt>MpClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="3a5b2-131">DLL</span><span class="sxs-lookup"><span data-stu-id="3a5b2-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3a5b2-132"><dt>MpClient.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3a5b2-132"><dt>MpClient.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3a5b2-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3a5b2-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3a5b2-134">**MpErrorMessageFormat**</span><span class="sxs-lookup"><span data-stu-id="3a5b2-134">**MpErrorMessageFormat**</span></span>](mperrormessageformat.md)
</dt> <dt>

[<span data-ttu-id="3a5b2-135">**MpHandleClose**</span><span class="sxs-lookup"><span data-stu-id="3a5b2-135">**MpHandleClose**</span></span>](mphandleclose.md)
</dt> </dl>

 

 





