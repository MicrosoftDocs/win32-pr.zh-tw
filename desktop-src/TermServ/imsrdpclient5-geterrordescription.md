---
title: IMsRdpClient5 GetErrorDescription 方法
description: 抓取會話中斷連接事件的錯誤描述。
ms.assetid: 8c8f7b10-7f79-4586-845e-e99f5ca81905
ms.tgt_platform: multiple
keywords:
- GetErrorDescription 方法遠端桌面服務
- GetErrorDescription 方法遠端桌面服務，IMsRdpClient5 介面
- IMsRdpClient5 介面遠端桌面服務，GetErrorDescription 方法
- GetErrorDescription 方法遠端桌面服務，IMsRdpClient6 介面
- IMsRdpClient6 介面遠端桌面服務，GetErrorDescription 方法
- GetErrorDescription 方法遠端桌面服務，IMsRdpClient7 介面
- IMsRdpClient7 介面遠端桌面服務，GetErrorDescription 方法
- GetErrorDescription 方法遠端桌面服務，IMsRdpClient8 介面
- IMsRdpClient8 介面遠端桌面服務，GetErrorDescription 方法
- GetErrorDescription 方法遠端桌面服務，IMsRdpClient9 介面
- IMsRdpClient9 介面遠端桌面服務，GetErrorDescription 方法
- GetErrorDescription 方法遠端桌面服務，IMsRdpClient10 介面
- IMsRdpClient10 介面遠端桌面服務，GetErrorDescription 方法
topic_type:
- apiref
api_name:
- IMsRdpClient5.GetErrorDescription
- IMsRdpClient6.GetErrorDescription
- IMsRdpClient7.GetErrorDescription
- IMsRdpClient8.GetErrorDescription
- IMsRdpClient9.GetErrorDescription
- IMsRdpClient10.GetErrorDescription
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c402a0128286964ddeb1c53cd805e4ef6414bfb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104385174"
---
# <a name="imsrdpclient5geterrordescription-method"></a><span data-ttu-id="1f35b-116">IMsRdpClient5：： GetErrorDescription 方法</span><span class="sxs-lookup"><span data-stu-id="1f35b-116">IMsRdpClient5::GetErrorDescription method</span></span>

<span data-ttu-id="1f35b-117">抓取會話中斷連接事件的錯誤描述。</span><span class="sxs-lookup"><span data-stu-id="1f35b-117">Retrieves the error description for the session disconnect events.</span></span>

## <a name="syntax"></a><span data-ttu-id="1f35b-118">語法</span><span class="sxs-lookup"><span data-stu-id="1f35b-118">Syntax</span></span>


```C++
HRESULT GetErrorDescription(
  [in]  UINT disconnectReason,
  [in]  UINT extendedDisconnectReason,
  [out] BSTR *pBstrErrorMsg
);
```



## <a name="parameters"></a><span data-ttu-id="1f35b-119">參數</span><span class="sxs-lookup"><span data-stu-id="1f35b-119">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1f35b-120">*disconnectReason* \[在\]</span><span class="sxs-lookup"><span data-stu-id="1f35b-120">*disconnectReason* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1f35b-121">中斷連接原因。</span><span class="sxs-lookup"><span data-stu-id="1f35b-121">The disconnect reason.</span></span>

</dd> <dt>

<span data-ttu-id="1f35b-122">*extendedDisconnectReason* \[在\]</span><span class="sxs-lookup"><span data-stu-id="1f35b-122">*extendedDisconnectReason* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1f35b-123">提供有關起始中斷連接原因的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="1f35b-123">Provides detailed information about why a disconnect was initiated.</span></span>

</dd> <dt>

<span data-ttu-id="1f35b-124">*pBstrErrorMsg* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="1f35b-124">*pBstrErrorMsg* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1f35b-125">接收錯誤訊息正文之 **BSTR** 變數的指標。</span><span class="sxs-lookup"><span data-stu-id="1f35b-125">A pointer to a **BSTR** variable that receives the error message text.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1f35b-126">傳回值</span><span class="sxs-lookup"><span data-stu-id="1f35b-126">Return value</span></span>

<span data-ttu-id="1f35b-127">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="1f35b-127">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="1f35b-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="1f35b-128">Requirements</span></span>



| <span data-ttu-id="1f35b-129">需求</span><span class="sxs-lookup"><span data-stu-id="1f35b-129">Requirement</span></span> | <span data-ttu-id="1f35b-130">值</span><span class="sxs-lookup"><span data-stu-id="1f35b-130">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1f35b-131">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1f35b-131">Minimum supported client</span></span><br/> | <span data-ttu-id="1f35b-132">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1f35b-132">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="1f35b-133">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1f35b-133">Minimum supported server</span></span><br/> | <span data-ttu-id="1f35b-134">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1f35b-134">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="1f35b-135">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="1f35b-135">Type library</span></span><br/>             | <dl> <span data-ttu-id="1f35b-136"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1f35b-136"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="1f35b-137">DLL</span><span class="sxs-lookup"><span data-stu-id="1f35b-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1f35b-138"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1f35b-138"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="1f35b-139">IID</span><span class="sxs-lookup"><span data-stu-id="1f35b-139">IID</span></span><br/>                      | <span data-ttu-id="1f35b-140">IID \_ IMsRdpClient5 定義為4eb5335b-6429-477d-b922-e06a28ecd8bf</span><span class="sxs-lookup"><span data-stu-id="1f35b-140">IID\_IMsRdpClient5 is defined as 4eb5335b-6429-477d-b922-e06a28ecd8bf</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="1f35b-141">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1f35b-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1f35b-142">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="1f35b-142">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="1f35b-143">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="1f35b-143">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="1f35b-144">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="1f35b-144">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="1f35b-145">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="1f35b-145">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="1f35b-146">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="1f35b-146">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="1f35b-147">**IMsRdpClient10**</span><span class="sxs-lookup"><span data-stu-id="1f35b-147">**IMsRdpClient10**</span></span>](imsrdpclient10.md)
</dt> </dl>

 

 





