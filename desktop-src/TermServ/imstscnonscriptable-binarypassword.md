---
title: IMsTscNonScriptable BinaryPassword 屬性
description: 這個屬性不再可供使用。 |IMsTscNonScriptable BinaryPassword 屬性
ms.assetid: b3be7323-a75f-4ec2-9d58-e8ff3338d6ff
ms.tgt_platform: multiple
keywords:
- BinaryPassword 屬性遠端桌面服務
- BinaryPassword 屬性遠端桌面服務，IMsTscNonScriptable 介面
- IMsTscNonScriptable 介面遠端桌面服務，BinaryPassword 屬性
- BinaryPassword 屬性遠端桌面服務，MsTscAx 物件
- MsTscAx 物件遠端桌面服務、BinaryPassword 屬性
- BinaryPassword 屬性遠端桌面服務，IMsRdpClientNonScriptable 介面
- IMsRdpClientNonScriptable 介面遠端桌面服務，BinaryPassword 屬性
- BinaryPassword 屬性遠端桌面服務，IMsRdpClientNonScriptable2 介面
- IMsRdpClientNonScriptable2 介面遠端桌面服務，BinaryPassword 屬性
- BinaryPassword 屬性遠端桌面服務，IMsRdpClientNonScriptable3 介面
- IMsRdpClientNonScriptable3 介面遠端桌面服務，BinaryPassword 屬性
- BinaryPassword 屬性遠端桌面服務，IMsRdpClientNonScriptable4 介面
- IMsRdpClientNonScriptable4 介面遠端桌面服務，BinaryPassword 屬性
- BinaryPassword 屬性遠端桌面服務，IMsRdpClientNonScriptable5 介面
- IMsRdpClientNonScriptable5 介面遠端桌面服務，BinaryPassword 屬性
topic_type:
- apiref
api_name:
- IMsTscNonScriptable.BinaryPassword
- IMsTscNonScriptable.get_BinaryPassword
- IMsTscNonScriptable.put_BinaryPassword
- MsTscAx.BinaryPassword
- IMsRdpClientNonScriptable.BinaryPassword
- IMsRdpClientNonScriptable.get_BinaryPassword
- IMsRdpClientNonScriptable.put_BinaryPassword
- IMsRdpClientNonScriptable2.BinaryPassword
- IMsRdpClientNonScriptable2.get_BinaryPassword
- IMsRdpClientNonScriptable2.put_BinaryPassword
- IMsRdpClientNonScriptable3.BinaryPassword
- IMsRdpClientNonScriptable3.get_BinaryPassword
- IMsRdpClientNonScriptable3.put_BinaryPassword
- IMsRdpClientNonScriptable4.BinaryPassword
- IMsRdpClientNonScriptable4.get_BinaryPassword
- IMsRdpClientNonScriptable4.put_BinaryPassword
- IMsRdpClientNonScriptable5.BinaryPassword
- IMsRdpClientNonScriptable5.get_BinaryPassword
- IMsRdpClientNonScriptable5.put_BinaryPassword
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a1d6eab2a3902968ef4d4c953a8da8b9c884a497
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "106993817"
---
# <a name="imstscnonscriptablebinarypassword-property"></a><span data-ttu-id="1202d-119">IMsTscNonScriptable：： BinaryPassword 屬性</span><span class="sxs-lookup"><span data-stu-id="1202d-119">IMsTscNonScriptable::BinaryPassword property</span></span>

<span data-ttu-id="1202d-120">這個屬性不再可供使用。</span><span class="sxs-lookup"><span data-stu-id="1202d-120">This property is no longer available for use.</span></span>

<span data-ttu-id="1202d-121">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="1202d-121">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="1202d-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="1202d-122">Syntax</span></span>


```C++
HRESULT put_BinaryPassword(
  [in]  BSTR newPassword
);

HRESULT get_BinaryPassword(
  [out] BSTR *pBinaryPassword
);
```



## <a name="property-value"></a><span data-ttu-id="1202d-123">屬性值</span><span class="sxs-lookup"><span data-stu-id="1202d-123">Property value</span></span>

<span data-ttu-id="1202d-124">新的密碼部分，採用二進位編碼格式。</span><span class="sxs-lookup"><span data-stu-id="1202d-124">The new password part, in binary encoded format.</span></span>

## <a name="error-codes"></a><span data-ttu-id="1202d-125">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="1202d-125">Error codes</span></span>

<span data-ttu-id="1202d-126">傳回 **E \_ >notimpl**。</span><span class="sxs-lookup"><span data-stu-id="1202d-126">Returns **E\_NOTIMPL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="1202d-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="1202d-127">Requirements</span></span>



| <span data-ttu-id="1202d-128">需求</span><span class="sxs-lookup"><span data-stu-id="1202d-128">Requirement</span></span> | <span data-ttu-id="1202d-129">值</span><span class="sxs-lookup"><span data-stu-id="1202d-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1202d-130">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1202d-130">Minimum supported client</span></span><br/> | <span data-ttu-id="1202d-131">都不支援</span><span class="sxs-lookup"><span data-stu-id="1202d-131">None supported</span></span><br/>                                                              |
| <span data-ttu-id="1202d-132">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1202d-132">Minimum supported server</span></span><br/> | <span data-ttu-id="1202d-133">都不支援</span><span class="sxs-lookup"><span data-stu-id="1202d-133">None supported</span></span><br/>                                                              |
| <span data-ttu-id="1202d-134">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="1202d-134">End of client support</span></span><br/>    | <span data-ttu-id="1202d-135">都不支援</span><span class="sxs-lookup"><span data-stu-id="1202d-135">None supported</span></span><br/>                                                              |
| <span data-ttu-id="1202d-136">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="1202d-136">End of server support</span></span><br/>    | <span data-ttu-id="1202d-137">都不支援</span><span class="sxs-lookup"><span data-stu-id="1202d-137">None supported</span></span><br/>                                                              |
| <span data-ttu-id="1202d-138">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="1202d-138">Type library</span></span><br/>             | <dl> <span data-ttu-id="1202d-139"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1202d-139"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="1202d-140">DLL</span><span class="sxs-lookup"><span data-stu-id="1202d-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1202d-141"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1202d-141"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="1202d-142">IID</span><span class="sxs-lookup"><span data-stu-id="1202d-142">IID</span></span><br/>                      | <span data-ttu-id="1202d-143">IID \_ IMsTscNonScriptable 定義為 c1e6743a-41c1-4a74-832a-0dd06c1c7a0e</span><span class="sxs-lookup"><span data-stu-id="1202d-143">IID\_IMsTscNonScriptable is defined as c1e6743a-41c1-4a74-832a-0dd06c1c7a0e</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="1202d-144">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1202d-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1202d-145">**IMsRdpClientNonScriptable**</span><span class="sxs-lookup"><span data-stu-id="1202d-145">**IMsRdpClientNonScriptable**</span></span>](imsrdpclientnonscriptable-interface.md)
</dt> <dt>

[<span data-ttu-id="1202d-146">**IMsRdpClientNonScriptable2**</span><span class="sxs-lookup"><span data-stu-id="1202d-146">**IMsRdpClientNonScriptable2**</span></span>](imsrdpclientnonscriptable2.md)
</dt> <dt>

[<span data-ttu-id="1202d-147">**IMsRdpClientNonScriptable3**</span><span class="sxs-lookup"><span data-stu-id="1202d-147">**IMsRdpClientNonScriptable3**</span></span>](imsrdpclientnonscriptable3.md)
</dt> <dt>

[<span data-ttu-id="1202d-148">**IMsRdpClientNonScriptable4**</span><span class="sxs-lookup"><span data-stu-id="1202d-148">**IMsRdpClientNonScriptable4**</span></span>](imsrdpclientnonscriptable4.md)
</dt> <dt>

[<span data-ttu-id="1202d-149">**IMsRdpClientNonScriptable5**</span><span class="sxs-lookup"><span data-stu-id="1202d-149">**IMsRdpClientNonScriptable5**</span></span>](imsrdpclientnonscriptable5.md)
</dt> <dt>

[<span data-ttu-id="1202d-150">**IMsTscNonScriptable**</span><span class="sxs-lookup"><span data-stu-id="1202d-150">**IMsTscNonScriptable**</span></span>](imstscnonscriptable-interface.md)
</dt> </dl>

 

 





