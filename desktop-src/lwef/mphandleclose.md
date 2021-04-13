---
title: 'MpHandleClose 函式 (MpClient) '
description: 關閉 MpManagerOpen、MpScanStart、MpThreatOpen 或 MpUpdateStart 所傳回的控制碼。
ms.assetid: 335776E2-7598-4DC1-92AB-B49B35222EF6
keywords:
- MpHandleClose 函式舊版 Windows 環境功能
topic_type:
- apiref
api_name:
- MpHandleClose
api_location:
- MpClient.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 43c937548c8e1d3b98aa2e3d10d7577f8c69c1c5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509227"
---
# <a name="mphandleclose-function"></a><span data-ttu-id="c61ce-104">MpHandleClose 函式</span><span class="sxs-lookup"><span data-stu-id="c61ce-104">MpHandleClose function</span></span>

<span data-ttu-id="c61ce-105">關閉 [**MpManagerOpen**](mpmanageropen.md)、 [**MpScanStart**](mpscanstart.md)、 [**MpThreatOpen**](mpthreatopen.md)或 [**MpUpdateStart**](mpupdatestart.md)所傳回的控制碼。</span><span class="sxs-lookup"><span data-stu-id="c61ce-105">Closes the handle returned by [**MpManagerOpen**](mpmanageropen.md), [**MpScanStart**](mpscanstart.md), [**MpThreatOpen**](mpthreatopen.md), or [**MpUpdateStart**](mpupdatestart.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="c61ce-106">語法</span><span class="sxs-lookup"><span data-stu-id="c61ce-106">Syntax</span></span>


```C++
HRESULT WINAPI MpHandleClose(
  _In_ MPHANDLE hMpHandle
);
```



## <a name="parameters"></a><span data-ttu-id="c61ce-107">參數</span><span class="sxs-lookup"><span data-stu-id="c61ce-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c61ce-108">*hMpHandle* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c61ce-108">*hMpHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c61ce-109">類型： **MPHANDLE**</span><span class="sxs-lookup"><span data-stu-id="c61ce-109">Type: **MPHANDLE**</span></span>

<span data-ttu-id="c61ce-110">要關閉的控制碼。</span><span class="sxs-lookup"><span data-stu-id="c61ce-110">Handle to close.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c61ce-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="c61ce-111">Return value</span></span>

<span data-ttu-id="c61ce-112">類型： **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="c61ce-112">Type: **HRESULT**</span></span>

<span data-ttu-id="c61ce-113">如果函式成功，則傳回值為 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="c61ce-113">If the function succeeds the return value is **S\_OK**.</span></span>

<span data-ttu-id="c61ce-114">如果函式失敗，則傳回值會是失敗的 **HRESULT** 程式碼。</span><span class="sxs-lookup"><span data-stu-id="c61ce-114">If the function fails then the return value is a failed **HRESULT** code.</span></span> <span data-ttu-id="c61ce-115">呼叫端可以使用 [**MpErrorMessageFormat**](mperrormessageformat.md) 函數來取得錯誤訊息的一般描述。</span><span class="sxs-lookup"><span data-stu-id="c61ce-115">The caller can use the [**MpErrorMessageFormat**](mperrormessageformat.md) function to get a generic description of the error message.</span></span>

<span data-ttu-id="c61ce-116">函數可以傳回下列特定的錯誤：</span><span class="sxs-lookup"><span data-stu-id="c61ce-116">The following specific error can be returned by the function:</span></span>

| <span data-ttu-id="c61ce-117">傳回碼</span><span class="sxs-lookup"><span data-stu-id="c61ce-117">Return Code</span></span>             | <span data-ttu-id="c61ce-118">Description</span><span class="sxs-lookup"><span data-stu-id="c61ce-118">Description</span></span>                      |
|-------------------------|----------------------------------|
| <span data-ttu-id="c61ce-119">E \_ WIN \_ 不正確 \_ 控制碼</span><span class="sxs-lookup"><span data-stu-id="c61ce-119">E\_WIN\_INVALID\_HANDLE</span></span> | <span data-ttu-id="c61ce-120">指定的控制碼無效。</span><span class="sxs-lookup"><span data-stu-id="c61ce-120">The specified handle is invalid.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="c61ce-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="c61ce-121">Requirements</span></span>



| <span data-ttu-id="c61ce-122">需求</span><span class="sxs-lookup"><span data-stu-id="c61ce-122">Requirement</span></span> | <span data-ttu-id="c61ce-123">值</span><span class="sxs-lookup"><span data-stu-id="c61ce-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c61ce-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c61ce-124">Minimum supported client</span></span><br/> | <span data-ttu-id="c61ce-125">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c61ce-125">Windows 8 \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="c61ce-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c61ce-126">Minimum supported server</span></span><br/> | <span data-ttu-id="c61ce-127">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c61ce-127">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="c61ce-128">標頭</span><span class="sxs-lookup"><span data-stu-id="c61ce-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="c61ce-129"><dt>MpClient。h</dt></span><span class="sxs-lookup"><span data-stu-id="c61ce-129"><dt>MpClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="c61ce-130">DLL</span><span class="sxs-lookup"><span data-stu-id="c61ce-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c61ce-131"><dt>MpClient.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c61ce-131"><dt>MpClient.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c61ce-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c61ce-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c61ce-133">**MpErrorMessageFormat**</span><span class="sxs-lookup"><span data-stu-id="c61ce-133">**MpErrorMessageFormat**</span></span>](mperrormessageformat.md)
</dt> <dt>

[<span data-ttu-id="c61ce-134">**MpManagerOpen**</span><span class="sxs-lookup"><span data-stu-id="c61ce-134">**MpManagerOpen**</span></span>](mpmanageropen.md)
</dt> <dt>

[<span data-ttu-id="c61ce-135">**MpScanStart**</span><span class="sxs-lookup"><span data-stu-id="c61ce-135">**MpScanStart**</span></span>](mpscanstart.md)
</dt> <dt>

[<span data-ttu-id="c61ce-136">**MpThreatOpen**</span><span class="sxs-lookup"><span data-stu-id="c61ce-136">**MpThreatOpen**</span></span>](mpthreatopen.md)
</dt> </dl>

 

 





