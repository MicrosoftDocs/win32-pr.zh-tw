---
title: 'MpUpdateControl 函式 (MpClient) '
description: 允許透過 MpUpdateStart 以非同步方式啟動的簽章更新作業控制。
ms.assetid: 2780E472-6E8D-4839-88EE-46E3448C6BF5
keywords:
- MpUpdateControl 函式舊版 Windows 環境功能
topic_type:
- apiref
api_name:
- MpUpdateControl
api_location:
- MpClient.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 91ea28c6ace349fd04fb9241d7eddbe7c1e5fbbe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465933"
---
# <a name="mpupdatecontrol-function"></a><span data-ttu-id="563b2-104">MpUpdateControl 函式</span><span class="sxs-lookup"><span data-stu-id="563b2-104">MpUpdateControl function</span></span>

<span data-ttu-id="563b2-105">允許透過 [**MpUpdateStart**](mpupdatestart.md)以非同步方式啟動的簽章更新作業控制。</span><span class="sxs-lookup"><span data-stu-id="563b2-105">Allows the control of a signature update operation that was asynchronously initiated via [**MpUpdateStart**](mpupdatestart.md).</span></span> <span data-ttu-id="563b2-106">呼叫此函式需要系統管理員許可權，因為它允許取消整個系統的簽章更新。</span><span class="sxs-lookup"><span data-stu-id="563b2-106">Calling this function requires administrator privilege as it allows the cancellation of a system-wide signature update.</span></span>

## <a name="syntax"></a><span data-ttu-id="563b2-107">語法</span><span class="sxs-lookup"><span data-stu-id="563b2-107">Syntax</span></span>


```C++
HRESULT WINAPI MpUpdateControl(
  _In_ MPHANDLE  hUpdateHandle,
  _In_ MPCONTROL UpdateControl
);
```



## <a name="parameters"></a><span data-ttu-id="563b2-108">參數</span><span class="sxs-lookup"><span data-stu-id="563b2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="563b2-109">*hUpdateHandle* \[在\]</span><span class="sxs-lookup"><span data-stu-id="563b2-109">*hUpdateHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="563b2-110">類型： **MPHANDLE**</span><span class="sxs-lookup"><span data-stu-id="563b2-110">Type: **MPHANDLE**</span></span>

<span data-ttu-id="563b2-111">非同步簽名更新作業的控制碼。</span><span class="sxs-lookup"><span data-stu-id="563b2-111">Handle to an asynchronous signature update operation.</span></span> <span data-ttu-id="563b2-112">[**MpScanStart**](mpscanstart.md)函數會傳回這個控制碼。</span><span class="sxs-lookup"><span data-stu-id="563b2-112">This handle is returned by the [**MpScanStart**](mpscanstart.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="563b2-113">*UpdateControl* \[在\]</span><span class="sxs-lookup"><span data-stu-id="563b2-113">*UpdateControl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="563b2-114">類型： **mpcontrol.log**</span><span class="sxs-lookup"><span data-stu-id="563b2-114">Type: **MPCONTROL**</span></span>

<span data-ttu-id="563b2-115">指定 signature update control 選項。</span><span class="sxs-lookup"><span data-stu-id="563b2-115">Specifies the signature update control option.</span></span> <span data-ttu-id="563b2-116">它必須是下列值：</span><span class="sxs-lookup"><span data-stu-id="563b2-116">It must be the following value:</span></span>



| <span data-ttu-id="563b2-117">值</span><span class="sxs-lookup"><span data-stu-id="563b2-117">Value</span></span>                                                                                                                                                               | <span data-ttu-id="563b2-118">意義</span><span class="sxs-lookup"><span data-stu-id="563b2-118">Meaning</span></span>                                          |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| <span id="MPCONTROL_ABORT"></span><span id="mpcontrol_abort"></span><dl> <span data-ttu-id="563b2-119"><dt>**MPCONTROL.LOG \_ 中止**</dt></span><span class="sxs-lookup"><span data-stu-id="563b2-119"><dt>**MPCONTROL\_ABORT**</dt></span></span> </dl> | <span data-ttu-id="563b2-120">中止簽章更新作業。</span><span class="sxs-lookup"><span data-stu-id="563b2-120">Abort the signature update operation.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="563b2-121">傳回值</span><span class="sxs-lookup"><span data-stu-id="563b2-121">Return value</span></span>

<span data-ttu-id="563b2-122">類型： **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="563b2-122">Type: **HRESULT**</span></span>

<span data-ttu-id="563b2-123">如果函式成功，則傳回值為 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="563b2-123">If the function succeeds the return value is **S\_OK**.</span></span>

<span data-ttu-id="563b2-124">如果函式失敗，則傳回值會是失敗的 **HRESULT** 程式碼。</span><span class="sxs-lookup"><span data-stu-id="563b2-124">If the function fails then the return value is a failed **HRESULT** code.</span></span> <span data-ttu-id="563b2-125">呼叫端可以使用 [**MpErrorMessageFormat**](mperrormessageformat.md) 函數來取得錯誤訊息的一般描述。</span><span class="sxs-lookup"><span data-stu-id="563b2-125">The caller can use the [**MpErrorMessageFormat**](mperrormessageformat.md) function to get a generic description of the error message.</span></span>

## <a name="requirements"></a><span data-ttu-id="563b2-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="563b2-126">Requirements</span></span>



| <span data-ttu-id="563b2-127">需求</span><span class="sxs-lookup"><span data-stu-id="563b2-127">Requirement</span></span> | <span data-ttu-id="563b2-128">值</span><span class="sxs-lookup"><span data-stu-id="563b2-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="563b2-129">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="563b2-129">Minimum supported client</span></span><br/> | <span data-ttu-id="563b2-130">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="563b2-130">Windows 8 \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="563b2-131">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="563b2-131">Minimum supported server</span></span><br/> | <span data-ttu-id="563b2-132">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="563b2-132">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="563b2-133">標頭</span><span class="sxs-lookup"><span data-stu-id="563b2-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="563b2-134"><dt>MpClient。h</dt></span><span class="sxs-lookup"><span data-stu-id="563b2-134"><dt>MpClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="563b2-135">DLL</span><span class="sxs-lookup"><span data-stu-id="563b2-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="563b2-136"><dt>MpClient.dll</dt></span><span class="sxs-lookup"><span data-stu-id="563b2-136"><dt>MpClient.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="563b2-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="563b2-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="563b2-138">**MpErrorMessageFormat**</span><span class="sxs-lookup"><span data-stu-id="563b2-138">**MpErrorMessageFormat**</span></span>](mperrormessageformat.md)
</dt> <dt>

[<span data-ttu-id="563b2-139">**MpScanStart**</span><span class="sxs-lookup"><span data-stu-id="563b2-139">**MpScanStart**</span></span>](mpscanstart.md)
</dt> </dl>

 

 





