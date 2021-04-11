---
title: IMsTscAx AdvancedSettings 屬性
description: 捕獲 IMsTscAdvancedSettings 介面指標。
ms.assetid: 1c0e2216-0c65-48ad-b0f6-3a766c8fa44e
ms.tgt_platform: multiple
keywords:
- AdvancedSettings 屬性遠端桌面服務
- AdvancedSettings 屬性遠端桌面服務，IMsTscAx 介面
- IMsTscAx 介面遠端桌面服務，AdvancedSettings 屬性
- AdvancedSettings 屬性遠端桌面服務，IMsRdpClient 介面
- IMsRdpClient 介面遠端桌面服務，AdvancedSettings 屬性
- AdvancedSettings 屬性遠端桌面服務，IMsRdpClient2 介面
- IMsRdpClient2 介面遠端桌面服務，AdvancedSettings 屬性
- AdvancedSettings 屬性遠端桌面服務，IMsRdpClient3 介面
- IMsRdpClient3 介面遠端桌面服務，AdvancedSettings 屬性
- AdvancedSettings 屬性遠端桌面服務，IMsRdpClient4 介面
- IMsRdpClient4 介面遠端桌面服務，AdvancedSettings 屬性
- AdvancedSettings 屬性遠端桌面服務，IMsRdpClient5 介面
- IMsRdpClient5 介面遠端桌面服務，AdvancedSettings 屬性
- AdvancedSettings 屬性遠端桌面服務，IMsRdpClient6 介面
- IMsRdpClient6 介面遠端桌面服務，AdvancedSettings 屬性
- AdvancedSettings 屬性遠端桌面服務，IMsRdpClient7 介面
- IMsRdpClient7 介面遠端桌面服務，AdvancedSettings 屬性
- AdvancedSettings 屬性遠端桌面服務，IMsRdpClient8 介面
- IMsRdpClient8 介面遠端桌面服務，AdvancedSettings 屬性
- AdvancedSettings 屬性遠端桌面服務，IMsRdpClient9 介面
- IMsRdpClient9 介面遠端桌面服務，AdvancedSettings 屬性
topic_type:
- apiref
api_name:
- IMsTscAx.AdvancedSettings
- IMsTscAx.get_AdvancedSettings
- IMsRdpClient.AdvancedSettings
- IMsRdpClient.get_AdvancedSettings
- IMsRdpClient2.AdvancedSettings
- IMsRdpClient2.get_AdvancedSettings
- IMsRdpClient3.AdvancedSettings
- IMsRdpClient3.get_AdvancedSettings
- IMsRdpClient4.AdvancedSettings
- IMsRdpClient4.get_AdvancedSettings
- IMsRdpClient5.AdvancedSettings
- IMsRdpClient5.get_AdvancedSettings
- IMsRdpClient6.AdvancedSettings
- IMsRdpClient6.get_AdvancedSettings
- IMsRdpClient7.AdvancedSettings
- IMsRdpClient7.get_AdvancedSettings
- IMsRdpClient8.AdvancedSettings
- IMsRdpClient8.get_AdvancedSettings
- IMsRdpClient9.AdvancedSettings
- IMsRdpClient9.get_AdvancedSettings
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 98bb6b1d581704a0638a47310004777f020ce9bc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934368"
---
# <a name="imstscaxadvancedsettings-property"></a><span data-ttu-id="f7e10-124">IMsTscAx：： AdvancedSettings 屬性</span><span class="sxs-lookup"><span data-stu-id="f7e10-124">IMsTscAx::AdvancedSettings property</span></span>

<span data-ttu-id="f7e10-125">捕獲 [**IMsTscAdvancedSettings**](imstscadvancedsettings-interface.md) 介面指標。</span><span class="sxs-lookup"><span data-stu-id="f7e10-125">Retrieves an [**IMsTscAdvancedSettings**](imstscadvancedsettings-interface.md) interface pointer.</span></span>

<span data-ttu-id="f7e10-126">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="f7e10-126">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="f7e10-127">語法</span><span class="sxs-lookup"><span data-stu-id="f7e10-127">Syntax</span></span>


```C++
HRESULT get_AdvancedSettings(
  [out] IMsTscAdvancedSettings **ppAdvSettings
);
```



## <a name="property-value"></a><span data-ttu-id="f7e10-128">屬性值</span><span class="sxs-lookup"><span data-stu-id="f7e10-128">Property value</span></span>

<span data-ttu-id="f7e10-129">[**IMsTscAdvancedSettings**](imstscadvancedsettings-interface.md)介面指標。</span><span class="sxs-lookup"><span data-stu-id="f7e10-129">An [**IMsTscAdvancedSettings**](imstscadvancedsettings-interface.md) interface pointer.</span></span>

## <a name="error-codes"></a><span data-ttu-id="f7e10-130">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="f7e10-130">Error codes</span></span>

<span data-ttu-id="f7e10-131">如果成功，則傳回 **S \_ OK** 。</span><span class="sxs-lookup"><span data-stu-id="f7e10-131">Return **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="f7e10-132">備註</span><span class="sxs-lookup"><span data-stu-id="f7e10-132">Remarks</span></span>

<span data-ttu-id="f7e10-133">如需遠端桌面網頁連線的詳細資訊，請參閱 [遠端桌面網頁連線的需求](requirements-for-remote-desktop-web-connection.md)。</span><span class="sxs-lookup"><span data-stu-id="f7e10-133">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f7e10-134">規格需求</span><span class="sxs-lookup"><span data-stu-id="f7e10-134">Requirements</span></span>



| <span data-ttu-id="f7e10-135">需求</span><span class="sxs-lookup"><span data-stu-id="f7e10-135">Requirement</span></span> | <span data-ttu-id="f7e10-136">值</span><span class="sxs-lookup"><span data-stu-id="f7e10-136">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f7e10-137">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f7e10-137">Minimum supported client</span></span><br/> | <span data-ttu-id="f7e10-138">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f7e10-138">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="f7e10-139">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f7e10-139">Minimum supported server</span></span><br/> | <span data-ttu-id="f7e10-140">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f7e10-140">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="f7e10-141">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="f7e10-141">Type library</span></span><br/>             | <dl> <span data-ttu-id="f7e10-142"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f7e10-142"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="f7e10-143">DLL</span><span class="sxs-lookup"><span data-stu-id="f7e10-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f7e10-144"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f7e10-144"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="f7e10-145">IID</span><span class="sxs-lookup"><span data-stu-id="f7e10-145">IID</span></span><br/>                      | <span data-ttu-id="f7e10-146">IID \_ IMsTscAx 定義為8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span><span class="sxs-lookup"><span data-stu-id="f7e10-146">IID\_IMsTscAx is defined as 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="f7e10-147">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f7e10-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f7e10-148">**IMsRdpClient**</span><span class="sxs-lookup"><span data-stu-id="f7e10-148">**IMsRdpClient**</span></span>](imsrdpclient-interface.md)
</dt> <dt>

[<span data-ttu-id="f7e10-149">**IMsRdpClient2**</span><span class="sxs-lookup"><span data-stu-id="f7e10-149">**IMsRdpClient2**</span></span>](imsrdpclient2.md)
</dt> <dt>

[<span data-ttu-id="f7e10-150">**IMsRdpClient3**</span><span class="sxs-lookup"><span data-stu-id="f7e10-150">**IMsRdpClient3**</span></span>](imsrdpclient3.md)
</dt> <dt>

[<span data-ttu-id="f7e10-151">**IMsRdpClient4**</span><span class="sxs-lookup"><span data-stu-id="f7e10-151">**IMsRdpClient4**</span></span>](imsrdpclient4.md)
</dt> <dt>

[<span data-ttu-id="f7e10-152">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="f7e10-152">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="f7e10-153">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="f7e10-153">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="f7e10-154">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="f7e10-154">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="f7e10-155">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="f7e10-155">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="f7e10-156">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="f7e10-156">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="f7e10-157">**IMsTscAx**</span><span class="sxs-lookup"><span data-stu-id="f7e10-157">**IMsTscAx**</span></span>](imstscax-interface.md)
</dt> </dl>

 

 





