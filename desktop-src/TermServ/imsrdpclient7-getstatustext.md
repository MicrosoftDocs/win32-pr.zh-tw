---
title: 'IMsRdpClient7 GetStatusText 方法 (Openservice .h) '
description: 抓取指定狀態碼的狀態文字。
ms.assetid: 1da2280a-c26d-4caa-b227-c289055f3aa9
ms.tgt_platform: multiple
keywords:
- GetStatusText 方法遠端桌面服務
- GetStatusText 方法遠端桌面服務，IMsRdpClient7 介面
- IMsRdpClient7 介面遠端桌面服務，GetStatusText 方法
- GetStatusText 方法遠端桌面服務，IMsRdpClient8 介面
- IMsRdpClient8 介面遠端桌面服務，GetStatusText 方法
- GetStatusText 方法遠端桌面服務，IMsRdpClient9 介面
- IMsRdpClient9 介面遠端桌面服務，GetStatusText 方法
- GetStatusText 方法遠端桌面服務，IMsRdpClient10 介面
- IMsRdpClient10 介面遠端桌面服務，GetStatusText 方法
topic_type:
- apiref
api_name:
- IMsRdpClient7.GetStatusText
- IMsRdpClient8.GetStatusText
- IMsRdpClient9.GetStatusText
- IMsRdpClient10.GetStatusText
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 820628bfba59ec980e5128b9d9df3ee21b49a064
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686068"
---
# <a name="imsrdpclient7getstatustext-method"></a><span data-ttu-id="13355-112">IMsRdpClient7：： GetStatusText 方法</span><span class="sxs-lookup"><span data-stu-id="13355-112">IMsRdpClient7::GetStatusText method</span></span>

<span data-ttu-id="13355-113">抓取指定狀態碼的狀態文字。</span><span class="sxs-lookup"><span data-stu-id="13355-113">Retrieves the status text for the specified status code.</span></span>

## <a name="syntax"></a><span data-ttu-id="13355-114">語法</span><span class="sxs-lookup"><span data-stu-id="13355-114">Syntax</span></span>


```C++
HRESULT GetStatusText(
  [in]          UINT statusCode,
  [out, retval] BSTR *pBstrStatusText
);
```



## <a name="parameters"></a><span data-ttu-id="13355-115">參數</span><span class="sxs-lookup"><span data-stu-id="13355-115">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="13355-116">*statusCode* \[在\]</span><span class="sxs-lookup"><span data-stu-id="13355-116">*statusCode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="13355-117">指定要取得其文字之狀態碼的 **UINT** 。</span><span class="sxs-lookup"><span data-stu-id="13355-117">A **UINT** that specifies the status code to retrieve the text for.</span></span>

</dd> <dt>

<span data-ttu-id="13355-118">*pBstrStatusText* \[退出，retval\]</span><span class="sxs-lookup"><span data-stu-id="13355-118">*pBstrStatusText* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="13355-119">接收狀態文字之 **BSTR** 的位址。</span><span class="sxs-lookup"><span data-stu-id="13355-119">The address of a **BSTR** that receives the status text.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="13355-120">傳回值</span><span class="sxs-lookup"><span data-stu-id="13355-120">Return value</span></span>

<span data-ttu-id="13355-121">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="13355-121">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="13355-122">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="13355-122">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="13355-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="13355-123">Requirements</span></span>



| <span data-ttu-id="13355-124">需求</span><span class="sxs-lookup"><span data-stu-id="13355-124">Requirement</span></span> | <span data-ttu-id="13355-125">值</span><span class="sxs-lookup"><span data-stu-id="13355-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="13355-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="13355-126">Minimum supported client</span></span><br/> | <span data-ttu-id="13355-127">Windows 7</span><span class="sxs-lookup"><span data-stu-id="13355-127">Windows 7</span></span><br/>                                                                     |
| <span data-ttu-id="13355-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="13355-128">Minimum supported server</span></span><br/> | <span data-ttu-id="13355-129">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="13355-129">Windows Server 2008 R2</span></span><br/>                                                        |
| <span data-ttu-id="13355-130">標頭</span><span class="sxs-lookup"><span data-stu-id="13355-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="13355-131"><dt>Openservice。h</dt></span><span class="sxs-lookup"><span data-stu-id="13355-131"><dt>Openservice.h</dt></span></span> </dl> |
| <span data-ttu-id="13355-132">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="13355-132">Type library</span></span><br/>             | <dl> <span data-ttu-id="13355-133"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="13355-133"><dt>MsTscAx.dll</dt></span></span> </dl>   |
| <span data-ttu-id="13355-134">DLL</span><span class="sxs-lookup"><span data-stu-id="13355-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="13355-135"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="13355-135"><dt>MsTscAx.dll</dt></span></span> </dl>   |
| <span data-ttu-id="13355-136">IID</span><span class="sxs-lookup"><span data-stu-id="13355-136">IID</span></span><br/>                      | <span data-ttu-id="13355-137">IID \_ IMsRdpClient7 定義為 b2a5b5ce-3461-444a-91d4-add26d070638</span><span class="sxs-lookup"><span data-stu-id="13355-137">IID\_IMsRdpClient7 is defined as b2a5b5ce-3461-444a-91d4-add26d070638</span></span><br/>         |



## <a name="see-also"></a><span data-ttu-id="13355-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="13355-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="13355-139">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="13355-139">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="13355-140">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="13355-140">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="13355-141">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="13355-141">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="13355-142">**IMsRdpClient10**</span><span class="sxs-lookup"><span data-stu-id="13355-142">**IMsRdpClient10**</span></span>](imsrdpclient10.md)
</dt> </dl>

 

 





