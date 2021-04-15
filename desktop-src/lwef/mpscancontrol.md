---
title: 'MpScanControl 函式 (MpClient) '
description: 允許透過 MpScanStart 以非同步方式起始的掃描控制。
ms.assetid: 00855686-8C46-4B58-829C-AEAB53888704
keywords:
- MpScanControl 函式舊版 Windows 環境功能
topic_type:
- apiref
api_name:
- MpScanControl
api_location:
- MpClient.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce74736c4ca8c589e2ffa5570f2b6666838d820f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465161"
---
# <a name="mpscancontrol-function"></a><span data-ttu-id="656ea-104">MpScanControl 函式</span><span class="sxs-lookup"><span data-stu-id="656ea-104">MpScanControl function</span></span>

<span data-ttu-id="656ea-105">允許透過 [**MpScanStart**](mpscanstart.md)以非同步方式起始的掃描控制。</span><span class="sxs-lookup"><span data-stu-id="656ea-105">Allows the control of a scan that was asynchronously initiated via [**MpScanStart**](mpscanstart.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="656ea-106">語法</span><span class="sxs-lookup"><span data-stu-id="656ea-106">Syntax</span></span>


```C++
HRESULT WINAPI MpScanControl(
  _In_ MPHANDLE  hScanHandle,
  _In_ MPCONTROL ScanControl
);
```



## <a name="parameters"></a><span data-ttu-id="656ea-107">參數</span><span class="sxs-lookup"><span data-stu-id="656ea-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="656ea-108">*hScanHandle* \[在\]</span><span class="sxs-lookup"><span data-stu-id="656ea-108">*hScanHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="656ea-109">類型： **MPHANDLE**</span><span class="sxs-lookup"><span data-stu-id="656ea-109">Type: **MPHANDLE**</span></span>

<span data-ttu-id="656ea-110">非同步掃描操作的控制碼。</span><span class="sxs-lookup"><span data-stu-id="656ea-110">Handle to an asynchronous scan operation.</span></span> <span data-ttu-id="656ea-111">[**MpScanStart**](mpscanstart.md)函數會傳回這個控制碼。</span><span class="sxs-lookup"><span data-stu-id="656ea-111">This handle is returned by the [**MpScanStart**](mpscanstart.md) function.</span></span> <span data-ttu-id="656ea-112">此參數也可以設定為 [**MpManagerOpen**](mpmanageropen.md) 函式所傳回的 malware protection manager 介面控制碼，以控制系統起始的掃描，在這種情況下，呼叫端必須具有系統管理許可權。</span><span class="sxs-lookup"><span data-stu-id="656ea-112">This parameter can also be set to the malware protection manager interface handle returned by [**MpManagerOpen**](mpmanageropen.md) function to control a system initiated scan, in which case the caller must have administrative privilege.</span></span>

</dd> <dt>

<span data-ttu-id="656ea-113">*ScanControl* \[在\]</span><span class="sxs-lookup"><span data-stu-id="656ea-113">*ScanControl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="656ea-114">類型： **mpcontrol.log**</span><span class="sxs-lookup"><span data-stu-id="656ea-114">Type: **MPCONTROL**</span></span>

<span data-ttu-id="656ea-115">指定掃描控制選項。</span><span class="sxs-lookup"><span data-stu-id="656ea-115">Specifies a scan control option.</span></span> <span data-ttu-id="656ea-116">此參數必須是下列其中一個控制項選項：</span><span class="sxs-lookup"><span data-stu-id="656ea-116">This parameter must be one of the following control options:</span></span>



| <span data-ttu-id="656ea-117">值</span><span class="sxs-lookup"><span data-stu-id="656ea-117">Value</span></span>                                                                                                                                                                  | <span data-ttu-id="656ea-118">意義</span><span class="sxs-lookup"><span data-stu-id="656ea-118">Meaning</span></span>                                      |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <span id="MPCONTROL_ABORT"></span><span id="mpcontrol_abort"></span><dl> <span data-ttu-id="656ea-119"><dt>**MPCONTROL.LOG \_ 中止**</dt></span><span class="sxs-lookup"><span data-stu-id="656ea-119"><dt>**MPCONTROL\_ABORT**</dt></span></span> </dl>    | <span data-ttu-id="656ea-120">中止掃描工作。</span><span class="sxs-lookup"><span data-stu-id="656ea-120">Abort the scan operation.</span></span><br/>         |
| <span id="MPCONTROL_PAUSE"></span><span id="mpcontrol_pause"></span><dl> <span data-ttu-id="656ea-121"><dt>**MPCONTROL.LOG \_ 暫停**</dt></span><span class="sxs-lookup"><span data-stu-id="656ea-121"><dt>**MPCONTROL\_PAUSE**</dt></span></span> </dl>    | <span data-ttu-id="656ea-122">暫停掃描工作。</span><span class="sxs-lookup"><span data-stu-id="656ea-122">Pause the scan operation.</span></span><br/>         |
| <span id="MPCONTROL_RESUME"></span><span id="mpcontrol_resume"></span><dl> <span data-ttu-id="656ea-123"><dt>**MPCONTROL.LOG \_ RESUME**</dt></span><span class="sxs-lookup"><span data-stu-id="656ea-123"><dt>**MPCONTROL\_RESUME**</dt></span></span> </dl> | <span data-ttu-id="656ea-124">繼續暫停的掃描工作。</span><span class="sxs-lookup"><span data-stu-id="656ea-124">Resume the paused scan operation.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="656ea-125">傳回值</span><span class="sxs-lookup"><span data-stu-id="656ea-125">Return value</span></span>

<span data-ttu-id="656ea-126">類型： **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="656ea-126">Type: **HRESULT**</span></span>

<span data-ttu-id="656ea-127">如果函式成功，則傳回值為 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="656ea-127">If the function succeeds the return value is **S\_OK**.</span></span>

<span data-ttu-id="656ea-128">如果函式失敗，則傳回值會是失敗的 **HRESULT** 程式碼。</span><span class="sxs-lookup"><span data-stu-id="656ea-128">If the function fails then the return value is a failed **HRESULT** code.</span></span> <span data-ttu-id="656ea-129">呼叫端可以使用 [**MpErrorMessageFormat**](mperrormessageformat.md) 函數來取得錯誤訊息的一般描述。</span><span class="sxs-lookup"><span data-stu-id="656ea-129">The caller can use the [**MpErrorMessageFormat**](mperrormessageformat.md) function to get a generic description of the error message.</span></span>

## <a name="requirements"></a><span data-ttu-id="656ea-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="656ea-130">Requirements</span></span>



| <span data-ttu-id="656ea-131">需求</span><span class="sxs-lookup"><span data-stu-id="656ea-131">Requirement</span></span> | <span data-ttu-id="656ea-132">值</span><span class="sxs-lookup"><span data-stu-id="656ea-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="656ea-133">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="656ea-133">Minimum supported client</span></span><br/> | <span data-ttu-id="656ea-134">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="656ea-134">Windows 8 \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="656ea-135">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="656ea-135">Minimum supported server</span></span><br/> | <span data-ttu-id="656ea-136">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="656ea-136">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="656ea-137">標頭</span><span class="sxs-lookup"><span data-stu-id="656ea-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="656ea-138"><dt>MpClient。h</dt></span><span class="sxs-lookup"><span data-stu-id="656ea-138"><dt>MpClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="656ea-139">DLL</span><span class="sxs-lookup"><span data-stu-id="656ea-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="656ea-140"><dt>MpClient.dll</dt></span><span class="sxs-lookup"><span data-stu-id="656ea-140"><dt>MpClient.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="656ea-141">另請參閱</span><span class="sxs-lookup"><span data-stu-id="656ea-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="656ea-142">**MpErrorMessageFormat**</span><span class="sxs-lookup"><span data-stu-id="656ea-142">**MpErrorMessageFormat**</span></span>](mperrormessageformat.md)
</dt> <dt>

[<span data-ttu-id="656ea-143">**MpManagerOpen**</span><span class="sxs-lookup"><span data-stu-id="656ea-143">**MpManagerOpen**</span></span>](mpmanageropen.md)
</dt> <dt>

[<span data-ttu-id="656ea-144">**MpScanStart**</span><span class="sxs-lookup"><span data-stu-id="656ea-144">**MpScanStart**</span></span>](mpscanstart.md)
</dt> </dl>

 

 





