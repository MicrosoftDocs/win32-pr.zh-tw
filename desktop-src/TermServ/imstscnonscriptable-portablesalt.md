---
title: IMsTscNonScriptable PortableSalt 屬性
description: 這個屬性不再受到支援。
ms.assetid: 1f123ec8-27b6-4637-9c57-fe32a224be8a
ms.tgt_platform: multiple
keywords:
- PortableSalt 屬性遠端桌面服務
- PortableSalt 屬性遠端桌面服務，IMsTscNonScriptable 介面
- IMsTscNonScriptable 介面遠端桌面服務，PortableSalt 屬性
- PortableSalt 屬性遠端桌面服務，MsTscAx 物件
- MsTscAx 物件遠端桌面服務、PortableSalt 屬性
- PortableSalt 屬性遠端桌面服務，IMsRdpClientNonScriptable 介面
- IMsRdpClientNonScriptable 介面遠端桌面服務，PortableSalt 屬性
- PortableSalt 屬性遠端桌面服務，IMsRdpClientNonScriptable2 介面
- IMsRdpClientNonScriptable2 介面遠端桌面服務，PortableSalt 屬性
- PortableSalt 屬性遠端桌面服務，IMsRdpClientNonScriptable3 介面
- IMsRdpClientNonScriptable3 介面遠端桌面服務，PortableSalt 屬性
- PortableSalt 屬性遠端桌面服務，IMsRdpClientNonScriptable4 介面
- IMsRdpClientNonScriptable4 介面遠端桌面服務，PortableSalt 屬性
- PortableSalt 屬性遠端桌面服務，IMsRdpClientNonScriptable5 介面
- IMsRdpClientNonScriptable5 介面遠端桌面服務，PortableSalt 屬性
topic_type:
- apiref
api_name:
- IMsTscNonScriptable.PortableSalt
- IMsTscNonScriptable.get_PortableSalt
- IMsTscNonScriptable.put_PortableSalt
- MsTscAx.PortableSalt
- IMsRdpClientNonScriptable.PortableSalt
- IMsRdpClientNonScriptable.get_PortableSalt
- IMsRdpClientNonScriptable.put_PortableSalt
- IMsRdpClientNonScriptable2.PortableSalt
- IMsRdpClientNonScriptable2.get_PortableSalt
- IMsRdpClientNonScriptable2.put_PortableSalt
- IMsRdpClientNonScriptable3.PortableSalt
- IMsRdpClientNonScriptable3.get_PortableSalt
- IMsRdpClientNonScriptable3.put_PortableSalt
- IMsRdpClientNonScriptable4.PortableSalt
- IMsRdpClientNonScriptable4.get_PortableSalt
- IMsRdpClientNonScriptable4.put_PortableSalt
- IMsRdpClientNonScriptable5.PortableSalt
- IMsRdpClientNonScriptable5.get_PortableSalt
- IMsRdpClientNonScriptable5.put_PortableSalt
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0162073b8361cc89f7ab2e33f60406c0db935bdb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686129"
---
# <a name="imstscnonscriptableportablesalt-property"></a><span data-ttu-id="73993-118">IMsTscNonScriptable：:P ortableSalt 屬性</span><span class="sxs-lookup"><span data-stu-id="73993-118">IMsTscNonScriptable::PortableSalt property</span></span>

<span data-ttu-id="73993-119">這個屬性不再受到支援。</span><span class="sxs-lookup"><span data-stu-id="73993-119">This property is no longer supported.</span></span>

<span data-ttu-id="73993-120">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="73993-120">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="73993-121">Syntax</span><span class="sxs-lookup"><span data-stu-id="73993-121">Syntax</span></span>


```C++
HRESULT put_PortableSalt(
  [in]  BSTR newPortableSalt
);

HRESULT get_PortableSalt(
  [out] BSTR *pPortableSalt
);
```



## <a name="property-value"></a><span data-ttu-id="73993-122">屬性值</span><span class="sxs-lookup"><span data-stu-id="73993-122">Property value</span></span>

<span data-ttu-id="73993-123">便攜編碼密碼的新便攜 salt 部分。</span><span class="sxs-lookup"><span data-stu-id="73993-123">The new portable salt part for a portable encoded password.</span></span>

## <a name="error-codes"></a><span data-ttu-id="73993-124">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="73993-124">Error codes</span></span>

<span data-ttu-id="73993-125">傳回 **E \_ >notimpl**。</span><span class="sxs-lookup"><span data-stu-id="73993-125">Returns **E\_NOTIMPL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="73993-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="73993-126">Requirements</span></span>



| <span data-ttu-id="73993-127">需求</span><span class="sxs-lookup"><span data-stu-id="73993-127">Requirement</span></span> | <span data-ttu-id="73993-128">值</span><span class="sxs-lookup"><span data-stu-id="73993-128">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="73993-129">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="73993-129">Minimum supported client</span></span><br/> | <span data-ttu-id="73993-130">都不支援</span><span class="sxs-lookup"><span data-stu-id="73993-130">None supported</span></span><br/>                                                              |
| <span data-ttu-id="73993-131">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="73993-131">Minimum supported server</span></span><br/> | <span data-ttu-id="73993-132">都不支援</span><span class="sxs-lookup"><span data-stu-id="73993-132">None supported</span></span><br/>                                                              |
| <span data-ttu-id="73993-133">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="73993-133">End of client support</span></span><br/>    | <span data-ttu-id="73993-134">都不支援</span><span class="sxs-lookup"><span data-stu-id="73993-134">None supported</span></span><br/>                                                              |
| <span data-ttu-id="73993-135">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="73993-135">End of server support</span></span><br/>    | <span data-ttu-id="73993-136">都不支援</span><span class="sxs-lookup"><span data-stu-id="73993-136">None supported</span></span><br/>                                                              |
| <span data-ttu-id="73993-137">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="73993-137">Type library</span></span><br/>             | <dl> <span data-ttu-id="73993-138"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="73993-138"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="73993-139">DLL</span><span class="sxs-lookup"><span data-stu-id="73993-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="73993-140"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="73993-140"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="73993-141">IID</span><span class="sxs-lookup"><span data-stu-id="73993-141">IID</span></span><br/>                      | <span data-ttu-id="73993-142">IID \_ IMsTscNonScriptable 定義為 c1e6743a-41c1-4a74-832a-0dd06c1c7a0e</span><span class="sxs-lookup"><span data-stu-id="73993-142">IID\_IMsTscNonScriptable is defined as c1e6743a-41c1-4a74-832a-0dd06c1c7a0e</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="73993-143">另請參閱</span><span class="sxs-lookup"><span data-stu-id="73993-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="73993-144">**IMsRdpClientNonScriptable**</span><span class="sxs-lookup"><span data-stu-id="73993-144">**IMsRdpClientNonScriptable**</span></span>](imsrdpclientnonscriptable-interface.md)
</dt> <dt>

[<span data-ttu-id="73993-145">**IMsRdpClientNonScriptable2**</span><span class="sxs-lookup"><span data-stu-id="73993-145">**IMsRdpClientNonScriptable2**</span></span>](imsrdpclientnonscriptable2.md)
</dt> <dt>

[<span data-ttu-id="73993-146">**IMsRdpClientNonScriptable3**</span><span class="sxs-lookup"><span data-stu-id="73993-146">**IMsRdpClientNonScriptable3**</span></span>](imsrdpclientnonscriptable3.md)
</dt> <dt>

[<span data-ttu-id="73993-147">**IMsRdpClientNonScriptable4**</span><span class="sxs-lookup"><span data-stu-id="73993-147">**IMsRdpClientNonScriptable4**</span></span>](imsrdpclientnonscriptable4.md)
</dt> <dt>

[<span data-ttu-id="73993-148">**IMsRdpClientNonScriptable5**</span><span class="sxs-lookup"><span data-stu-id="73993-148">**IMsRdpClientNonScriptable5**</span></span>](imsrdpclientnonscriptable5.md)
</dt> <dt>

[<span data-ttu-id="73993-149">**IMsTscNonScriptable**</span><span class="sxs-lookup"><span data-stu-id="73993-149">**IMsTscNonScriptable**</span></span>](imstscnonscriptable-interface.md)
</dt> <dt>

[<span data-ttu-id="73993-150">**PortablePassword**</span><span class="sxs-lookup"><span data-stu-id="73993-150">**PortablePassword**</span></span>](imstscnonscriptable-portablepassword.md)
</dt> </dl>

 

 





