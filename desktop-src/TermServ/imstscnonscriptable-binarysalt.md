---
title: IMsTscNonScriptable BinarySalt 屬性
description: 這個屬性不再可供使用。 |IMsTscNonScriptable BinarySalt 屬性
ms.assetid: 7af2e5be-9ddb-46ab-947c-f79ab890d7bc
ms.tgt_platform: multiple
keywords:
- BinarySalt 屬性遠端桌面服務
- BinarySalt 屬性遠端桌面服務，IMsTscNonScriptable 介面
- IMsTscNonScriptable 介面遠端桌面服務，BinarySalt 屬性
- BinarySalt 屬性遠端桌面服務，MsTscAx 物件
- MsTscAx 物件遠端桌面服務、BinarySalt 屬性
- BinarySalt 屬性遠端桌面服務，IMsRdpClientNonScriptable 介面
- IMsRdpClientNonScriptable 介面遠端桌面服務，BinarySalt 屬性
- BinarySalt 屬性遠端桌面服務，IMsRdpClientNonScriptable2 介面
- IMsRdpClientNonScriptable2 介面遠端桌面服務，BinarySalt 屬性
- BinarySalt 屬性遠端桌面服務，IMsRdpClientNonScriptable3 介面
- IMsRdpClientNonScriptable3 介面遠端桌面服務，BinarySalt 屬性
- BinarySalt 屬性遠端桌面服務，IMsRdpClientNonScriptable4 介面
- IMsRdpClientNonScriptable4 介面遠端桌面服務，BinarySalt 屬性
- BinarySalt 屬性遠端桌面服務，IMsRdpClientNonScriptable5 介面
- IMsRdpClientNonScriptable5 介面遠端桌面服務，BinarySalt 屬性
topic_type:
- apiref
api_name:
- IMsTscNonScriptable.BinarySalt
- IMsTscNonScriptable.get_BinarySalt
- IMsTscNonScriptable.put_BinarySalt
- MsTscAx.BinarySalt
- IMsRdpClientNonScriptable.BinarySalt
- IMsRdpClientNonScriptable.get_BinarySalt
- IMsRdpClientNonScriptable.put_BinarySalt
- IMsRdpClientNonScriptable2.BinarySalt
- IMsRdpClientNonScriptable2.get_BinarySalt
- IMsRdpClientNonScriptable2.put_BinarySalt
- IMsRdpClientNonScriptable3.BinarySalt
- IMsRdpClientNonScriptable3.get_BinarySalt
- IMsRdpClientNonScriptable3.put_BinarySalt
- IMsRdpClientNonScriptable4.BinarySalt
- IMsRdpClientNonScriptable4.get_BinarySalt
- IMsRdpClientNonScriptable4.put_BinarySalt
- IMsRdpClientNonScriptable5.BinarySalt
- IMsRdpClientNonScriptable5.get_BinarySalt
- IMsRdpClientNonScriptable5.put_BinarySalt
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3eb13ccb79a9cf2c309a32772a73b393756c7bdd
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "106997608"
---
# <a name="imstscnonscriptablebinarysalt-property"></a><span data-ttu-id="3e1c2-119">IMsTscNonScriptable：： BinarySalt 屬性</span><span class="sxs-lookup"><span data-stu-id="3e1c2-119">IMsTscNonScriptable::BinarySalt property</span></span>

<span data-ttu-id="3e1c2-120">這個屬性不再可供使用。</span><span class="sxs-lookup"><span data-stu-id="3e1c2-120">This property is no longer available for use.</span></span>

<span data-ttu-id="3e1c2-121">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="3e1c2-121">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="3e1c2-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="3e1c2-122">Syntax</span></span>


```C++
HRESULT put_BinarySalt(
  [in]  BSTR newSalt
);

HRESULT get_BinarySalt(
  [out] BSTR *pSalt
);
```



## <a name="property-value"></a><span data-ttu-id="3e1c2-123">屬性值</span><span class="sxs-lookup"><span data-stu-id="3e1c2-123">Property value</span></span>

<span data-ttu-id="3e1c2-124">二進位編碼密碼的新二進位 salt 部分。</span><span class="sxs-lookup"><span data-stu-id="3e1c2-124">The new binary salt part for a binary encoded password.</span></span>

## <a name="error-codes"></a><span data-ttu-id="3e1c2-125">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="3e1c2-125">Error codes</span></span>

<span data-ttu-id="3e1c2-126">傳回 **E \_ >notimpl**。</span><span class="sxs-lookup"><span data-stu-id="3e1c2-126">Returns **E\_NOTIMPL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="3e1c2-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="3e1c2-127">Requirements</span></span>



| <span data-ttu-id="3e1c2-128">需求</span><span class="sxs-lookup"><span data-stu-id="3e1c2-128">Requirement</span></span> | <span data-ttu-id="3e1c2-129">值</span><span class="sxs-lookup"><span data-stu-id="3e1c2-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3e1c2-130">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3e1c2-130">Minimum supported client</span></span><br/> | <span data-ttu-id="3e1c2-131">都不支援</span><span class="sxs-lookup"><span data-stu-id="3e1c2-131">None supported</span></span><br/>                                                              |
| <span data-ttu-id="3e1c2-132">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3e1c2-132">Minimum supported server</span></span><br/> | <span data-ttu-id="3e1c2-133">都不支援</span><span class="sxs-lookup"><span data-stu-id="3e1c2-133">None supported</span></span><br/>                                                              |
| <span data-ttu-id="3e1c2-134">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="3e1c2-134">End of client support</span></span><br/>    | <span data-ttu-id="3e1c2-135">都不支援</span><span class="sxs-lookup"><span data-stu-id="3e1c2-135">None supported</span></span><br/>                                                              |
| <span data-ttu-id="3e1c2-136">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="3e1c2-136">End of server support</span></span><br/>    | <span data-ttu-id="3e1c2-137">都不支援</span><span class="sxs-lookup"><span data-stu-id="3e1c2-137">None supported</span></span><br/>                                                              |
| <span data-ttu-id="3e1c2-138">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="3e1c2-138">Type library</span></span><br/>             | <dl> <span data-ttu-id="3e1c2-139"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3e1c2-139"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="3e1c2-140">DLL</span><span class="sxs-lookup"><span data-stu-id="3e1c2-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3e1c2-141"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3e1c2-141"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="3e1c2-142">IID</span><span class="sxs-lookup"><span data-stu-id="3e1c2-142">IID</span></span><br/>                      | <span data-ttu-id="3e1c2-143">IID \_ IMsTscNonScriptable 定義為 c1e6743a-41c1-4a74-832a-0dd06c1c7a0e</span><span class="sxs-lookup"><span data-stu-id="3e1c2-143">IID\_IMsTscNonScriptable is defined as c1e6743a-41c1-4a74-832a-0dd06c1c7a0e</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="3e1c2-144">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3e1c2-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3e1c2-145">**IMsRdpClientNonScriptable**</span><span class="sxs-lookup"><span data-stu-id="3e1c2-145">**IMsRdpClientNonScriptable**</span></span>](imsrdpclientnonscriptable-interface.md)
</dt> <dt>

[<span data-ttu-id="3e1c2-146">**IMsRdpClientNonScriptable2**</span><span class="sxs-lookup"><span data-stu-id="3e1c2-146">**IMsRdpClientNonScriptable2**</span></span>](imsrdpclientnonscriptable2.md)
</dt> <dt>

[<span data-ttu-id="3e1c2-147">**IMsRdpClientNonScriptable3**</span><span class="sxs-lookup"><span data-stu-id="3e1c2-147">**IMsRdpClientNonScriptable3**</span></span>](imsrdpclientnonscriptable3.md)
</dt> <dt>

[<span data-ttu-id="3e1c2-148">**IMsRdpClientNonScriptable4**</span><span class="sxs-lookup"><span data-stu-id="3e1c2-148">**IMsRdpClientNonScriptable4**</span></span>](imsrdpclientnonscriptable4.md)
</dt> <dt>

[<span data-ttu-id="3e1c2-149">**IMsRdpClientNonScriptable5**</span><span class="sxs-lookup"><span data-stu-id="3e1c2-149">**IMsRdpClientNonScriptable5**</span></span>](imsrdpclientnonscriptable5.md)
</dt> <dt>

[<span data-ttu-id="3e1c2-150">**IMsTscNonScriptable**</span><span class="sxs-lookup"><span data-stu-id="3e1c2-150">**IMsTscNonScriptable**</span></span>](imstscnonscriptable-interface.md)
</dt> </dl>

 

 





