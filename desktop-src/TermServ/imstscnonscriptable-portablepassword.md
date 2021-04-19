---
title: IMsTscNonScriptable PortablePassword 屬性
description: 這個屬性不再可供使用。 |IMsTscNonScriptable PortablePassword 屬性
ms.assetid: 8d831ed3-1f4a-41a9-b283-507c5d9eea22
ms.tgt_platform: multiple
keywords:
- PortablePassword 屬性遠端桌面服務
- PortablePassword 屬性遠端桌面服務，IMsTscNonScriptable 介面
- IMsTscNonScriptable 介面遠端桌面服務，PortablePassword 屬性
- PortablePassword 屬性遠端桌面服務，MsTscAx 物件
- MsTscAx 物件遠端桌面服務、PortablePassword 屬性
- PortablePassword 屬性遠端桌面服務，IMsRdpClientNonScriptable 介面
- IMsRdpClientNonScriptable 介面遠端桌面服務，PortablePassword 屬性
- PortablePassword 屬性遠端桌面服務，IMsRdpClientNonScriptable2 介面
- IMsRdpClientNonScriptable2 介面遠端桌面服務，PortablePassword 屬性
- PortablePassword 屬性遠端桌面服務，IMsRdpClientNonScriptable3 介面
- IMsRdpClientNonScriptable3 介面遠端桌面服務，PortablePassword 屬性
- PortablePassword 屬性遠端桌面服務，IMsRdpClientNonScriptable4 介面
- IMsRdpClientNonScriptable4 介面遠端桌面服務，PortablePassword 屬性
- PortablePassword 屬性遠端桌面服務，IMsRdpClientNonScriptable5 介面
- IMsRdpClientNonScriptable5 介面遠端桌面服務，PortablePassword 屬性
topic_type:
- apiref
api_name:
- IMsTscNonScriptable.PortablePassword
- IMsTscNonScriptable.get_PortablePassword
- IMsTscNonScriptable.put_PortablePassword
- MsTscAx.PortablePassword
- IMsRdpClientNonScriptable.PortablePassword
- IMsRdpClientNonScriptable.get_PortablePassword
- IMsRdpClientNonScriptable.put_PortablePassword
- IMsRdpClientNonScriptable2.PortablePassword
- IMsRdpClientNonScriptable2.get_PortablePassword
- IMsRdpClientNonScriptable2.put_PortablePassword
- IMsRdpClientNonScriptable3.PortablePassword
- IMsRdpClientNonScriptable3.get_PortablePassword
- IMsRdpClientNonScriptable3.put_PortablePassword
- IMsRdpClientNonScriptable4.PortablePassword
- IMsRdpClientNonScriptable4.get_PortablePassword
- IMsRdpClientNonScriptable4.put_PortablePassword
- IMsRdpClientNonScriptable5.PortablePassword
- IMsRdpClientNonScriptable5.get_PortablePassword
- IMsRdpClientNonScriptable5.put_PortablePassword
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5259e83087287395e6114bb8ffe3eb7e859ab52
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "106981962"
---
# <a name="imstscnonscriptableportablepassword-property"></a><span data-ttu-id="c84df-119">IMsTscNonScriptable：:P ortablePassword 屬性</span><span class="sxs-lookup"><span data-stu-id="c84df-119">IMsTscNonScriptable::PortablePassword property</span></span>

<span data-ttu-id="c84df-120">這個屬性不再可供使用。</span><span class="sxs-lookup"><span data-stu-id="c84df-120">This property is no longer available for use.</span></span>

<span data-ttu-id="c84df-121">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="c84df-121">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="c84df-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="c84df-122">Syntax</span></span>


```C++
HRESULT put_PortablePassword(
  [in]  BSTR newPortablePassVal
);

HRESULT get_PortablePassword(
  [out] BSTR *pPortablePass
);
```



## <a name="property-value"></a><span data-ttu-id="c84df-123">屬性值</span><span class="sxs-lookup"><span data-stu-id="c84df-123">Property value</span></span>

<span data-ttu-id="c84df-124">以可移植編碼格式的新密碼部分。</span><span class="sxs-lookup"><span data-stu-id="c84df-124">The new password part, in portable encoded format.</span></span>

## <a name="error-codes"></a><span data-ttu-id="c84df-125">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="c84df-125">Error codes</span></span>

<span data-ttu-id="c84df-126">傳回 **E \_ >notimpl**。</span><span class="sxs-lookup"><span data-stu-id="c84df-126">Returns **E\_NOTIMPL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="c84df-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="c84df-127">Requirements</span></span>



| <span data-ttu-id="c84df-128">需求</span><span class="sxs-lookup"><span data-stu-id="c84df-128">Requirement</span></span> | <span data-ttu-id="c84df-129">值</span><span class="sxs-lookup"><span data-stu-id="c84df-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c84df-130">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c84df-130">Minimum supported client</span></span><br/> | <span data-ttu-id="c84df-131">都不支援</span><span class="sxs-lookup"><span data-stu-id="c84df-131">None supported</span></span><br/>                                                              |
| <span data-ttu-id="c84df-132">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c84df-132">Minimum supported server</span></span><br/> | <span data-ttu-id="c84df-133">都不支援</span><span class="sxs-lookup"><span data-stu-id="c84df-133">None supported</span></span><br/>                                                              |
| <span data-ttu-id="c84df-134">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="c84df-134">End of client support</span></span><br/>    | <span data-ttu-id="c84df-135">都不支援</span><span class="sxs-lookup"><span data-stu-id="c84df-135">None supported</span></span><br/>                                                              |
| <span data-ttu-id="c84df-136">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="c84df-136">End of server support</span></span><br/>    | <span data-ttu-id="c84df-137">都不支援</span><span class="sxs-lookup"><span data-stu-id="c84df-137">None supported</span></span><br/>                                                              |
| <span data-ttu-id="c84df-138">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="c84df-138">Type library</span></span><br/>             | <dl> <span data-ttu-id="c84df-139"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c84df-139"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="c84df-140">DLL</span><span class="sxs-lookup"><span data-stu-id="c84df-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c84df-141"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c84df-141"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="c84df-142">IID</span><span class="sxs-lookup"><span data-stu-id="c84df-142">IID</span></span><br/>                      | <span data-ttu-id="c84df-143">IID \_ IMsTscNonScriptable 定義為 c1e6743a-41c1-4a74-832a-0dd06c1c7a0e</span><span class="sxs-lookup"><span data-stu-id="c84df-143">IID\_IMsTscNonScriptable is defined as c1e6743a-41c1-4a74-832a-0dd06c1c7a0e</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c84df-144">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c84df-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c84df-145">**IMsRdpClientNonScriptable**</span><span class="sxs-lookup"><span data-stu-id="c84df-145">**IMsRdpClientNonScriptable**</span></span>](imsrdpclientnonscriptable-interface.md)
</dt> <dt>

[<span data-ttu-id="c84df-146">**IMsRdpClientNonScriptable2**</span><span class="sxs-lookup"><span data-stu-id="c84df-146">**IMsRdpClientNonScriptable2**</span></span>](imsrdpclientnonscriptable2.md)
</dt> <dt>

[<span data-ttu-id="c84df-147">**IMsRdpClientNonScriptable3**</span><span class="sxs-lookup"><span data-stu-id="c84df-147">**IMsRdpClientNonScriptable3**</span></span>](imsrdpclientnonscriptable3.md)
</dt> <dt>

[<span data-ttu-id="c84df-148">**IMsRdpClientNonScriptable4**</span><span class="sxs-lookup"><span data-stu-id="c84df-148">**IMsRdpClientNonScriptable4**</span></span>](imsrdpclientnonscriptable4.md)
</dt> <dt>

[<span data-ttu-id="c84df-149">**IMsRdpClientNonScriptable5**</span><span class="sxs-lookup"><span data-stu-id="c84df-149">**IMsRdpClientNonScriptable5**</span></span>](imsrdpclientnonscriptable5.md)
</dt> <dt>

[<span data-ttu-id="c84df-150">**IMsTscNonScriptable**</span><span class="sxs-lookup"><span data-stu-id="c84df-150">**IMsTscNonScriptable**</span></span>](imstscnonscriptable-interface.md)
</dt> </dl>

 

 





