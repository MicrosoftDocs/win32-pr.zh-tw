---
title: IMsTscAx SecuredSettingsEnabled 屬性
description: 指出 IMsTscSecuredSettings 介面是否可供使用。 亦即，包含控制項的網頁目前是否為其中一個允許的 Internet Explorer URL 安全性區域。
ms.assetid: 0747eab0-9d62-4c10-b02d-fc65ca2f752e
ms.tgt_platform: multiple
keywords:
- SecuredSettingsEnabled 屬性遠端桌面服務
- SecuredSettingsEnabled 屬性遠端桌面服務，IMsTscAx 介面
- IMsTscAx 介面遠端桌面服務，SecuredSettingsEnabled 屬性
- SecuredSettingsEnabled 屬性遠端桌面服務，IMsRdpClient 介面
- IMsRdpClient 介面遠端桌面服務，SecuredSettingsEnabled 屬性
- SecuredSettingsEnabled 屬性遠端桌面服務，IMsRdpClient2 介面
- IMsRdpClient2 介面遠端桌面服務，SecuredSettingsEnabled 屬性
- SecuredSettingsEnabled 屬性遠端桌面服務，IMsRdpClient3 介面
- IMsRdpClient3 介面遠端桌面服務，SecuredSettingsEnabled 屬性
- SecuredSettingsEnabled 屬性遠端桌面服務，IMsRdpClient4 介面
- IMsRdpClient4 介面遠端桌面服務，SecuredSettingsEnabled 屬性
- SecuredSettingsEnabled 屬性遠端桌面服務，IMsRdpClient5 介面
- IMsRdpClient5 介面遠端桌面服務，SecuredSettingsEnabled 屬性
- SecuredSettingsEnabled 屬性遠端桌面服務，IMsRdpClient6 介面
- IMsRdpClient6 介面遠端桌面服務，SecuredSettingsEnabled 屬性
- SecuredSettingsEnabled 屬性遠端桌面服務，IMsRdpClient7 介面
- IMsRdpClient7 介面遠端桌面服務，SecuredSettingsEnabled 屬性
- SecuredSettingsEnabled 屬性遠端桌面服務，IMsRdpClient8 介面
- IMsRdpClient8 介面遠端桌面服務，SecuredSettingsEnabled 屬性
- SecuredSettingsEnabled 屬性遠端桌面服務，IMsRdpClient9 介面
- IMsRdpClient9 介面遠端桌面服務，SecuredSettingsEnabled 屬性
topic_type:
- apiref
api_name:
- IMsTscAx.SecuredSettingsEnabled
- IMsTscAx.get_SecuredSettingsEnabled
- IMsRdpClient.SecuredSettingsEnabled
- IMsRdpClient.get_SecuredSettingsEnabled
- IMsRdpClient2.SecuredSettingsEnabled
- IMsRdpClient2.get_SecuredSettingsEnabled
- IMsRdpClient3.SecuredSettingsEnabled
- IMsRdpClient3.get_SecuredSettingsEnabled
- IMsRdpClient4.SecuredSettingsEnabled
- IMsRdpClient4.get_SecuredSettingsEnabled
- IMsRdpClient5.SecuredSettingsEnabled
- IMsRdpClient5.get_SecuredSettingsEnabled
- IMsRdpClient6.SecuredSettingsEnabled
- IMsRdpClient6.get_SecuredSettingsEnabled
- IMsRdpClient7.SecuredSettingsEnabled
- IMsRdpClient7.get_SecuredSettingsEnabled
- IMsRdpClient8.SecuredSettingsEnabled
- IMsRdpClient8.get_SecuredSettingsEnabled
- IMsRdpClient9.SecuredSettingsEnabled
- IMsRdpClient9.get_SecuredSettingsEnabled
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de0601ac64ab0ca55f3d92ec460861a4347f70b7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106980291"
---
# <a name="imstscaxsecuredsettingsenabled-property"></a><span data-ttu-id="60d2f-125">IMsTscAx：： SecuredSettingsEnabled 屬性</span><span class="sxs-lookup"><span data-stu-id="60d2f-125">IMsTscAx::SecuredSettingsEnabled property</span></span>

<span data-ttu-id="60d2f-126">指出 [**IMsTscSecuredSettings**](imstscsecuredsettings-interface.md) 介面是否可供使用。</span><span class="sxs-lookup"><span data-stu-id="60d2f-126">Indicates whether the [**IMsTscSecuredSettings**](imstscsecuredsettings-interface.md) interface is available.</span></span> <span data-ttu-id="60d2f-127">亦即，包含控制項的網頁目前是否為其中一個允許的 Internet Explorer URL 安全性區域。</span><span class="sxs-lookup"><span data-stu-id="60d2f-127">That is, whether the webpage containing the control is currently in one of the allowed Internet Explorer URL security zones.</span></span>

<span data-ttu-id="60d2f-128">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="60d2f-128">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="60d2f-129">語法</span><span class="sxs-lookup"><span data-stu-id="60d2f-129">Syntax</span></span>


```C++
HRESULT get_SecuredSettingsEnabled(
  [out] BOOL *pSecuredSettingsEnabled
);
```



## <a name="property-value"></a><span data-ttu-id="60d2f-130">屬性值</span><span class="sxs-lookup"><span data-stu-id="60d2f-130">Property value</span></span>

<span data-ttu-id="60d2f-131">如果介面可供使用，則這個參數的值為 **TRUE** ，否則為 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="60d2f-131">The value of this parameter is **TRUE** if the interface is available, and **FALSE** otherwise.</span></span>

## <a name="error-codes"></a><span data-ttu-id="60d2f-132">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="60d2f-132">Error codes</span></span>

<span data-ttu-id="60d2f-133">如果成功，則傳回 **S \_ OK** 。</span><span class="sxs-lookup"><span data-stu-id="60d2f-133">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="60d2f-134">備註</span><span class="sxs-lookup"><span data-stu-id="60d2f-134">Remarks</span></span>

<span data-ttu-id="60d2f-135">在抓取 [**SecuredSettings**](imstscax-securedsettings.md)屬性之前，請使用這個方法來查詢 [**IMsTscSecuredSettings**](imstscsecuredsettings-interface.md)介面是否可用。</span><span class="sxs-lookup"><span data-stu-id="60d2f-135">Use this method to query whether the [**IMsTscSecuredSettings**](imstscsecuredsettings-interface.md) interface is available before retrieving the [**SecuredSettings**](imstscax-securedsettings.md) property.</span></span>

<span data-ttu-id="60d2f-136">請參閱 [提供 RDP 用戶端安全性](providing-for-rdp-client-security.md) ，以取得限制的 URL 安全性區域清單。</span><span class="sxs-lookup"><span data-stu-id="60d2f-136">Refer to [Providing for RDP Client Security](providing-for-rdp-client-security.md) for a list of restricted URL security zones.</span></span>

<span data-ttu-id="60d2f-137">如需遠端桌面網頁連線的詳細資訊，請參閱 [遠端桌面網頁連線的需求](requirements-for-remote-desktop-web-connection.md)。</span><span class="sxs-lookup"><span data-stu-id="60d2f-137">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="60d2f-138">規格需求</span><span class="sxs-lookup"><span data-stu-id="60d2f-138">Requirements</span></span>



| <span data-ttu-id="60d2f-139">需求</span><span class="sxs-lookup"><span data-stu-id="60d2f-139">Requirement</span></span> | <span data-ttu-id="60d2f-140">值</span><span class="sxs-lookup"><span data-stu-id="60d2f-140">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="60d2f-141">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="60d2f-141">Minimum supported client</span></span><br/> | <span data-ttu-id="60d2f-142">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="60d2f-142">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="60d2f-143">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="60d2f-143">Minimum supported server</span></span><br/> | <span data-ttu-id="60d2f-144">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="60d2f-144">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="60d2f-145">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="60d2f-145">Type library</span></span><br/>             | <dl> <span data-ttu-id="60d2f-146"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="60d2f-146"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="60d2f-147">DLL</span><span class="sxs-lookup"><span data-stu-id="60d2f-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="60d2f-148"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="60d2f-148"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="60d2f-149">IID</span><span class="sxs-lookup"><span data-stu-id="60d2f-149">IID</span></span><br/>                      | <span data-ttu-id="60d2f-150">IID \_ IMsTscAx 定義為8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span><span class="sxs-lookup"><span data-stu-id="60d2f-150">IID\_IMsTscAx is defined as 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="60d2f-151">另請參閱</span><span class="sxs-lookup"><span data-stu-id="60d2f-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="60d2f-152">**IMsRdpClient**</span><span class="sxs-lookup"><span data-stu-id="60d2f-152">**IMsRdpClient**</span></span>](imsrdpclient-interface.md)
</dt> <dt>

[<span data-ttu-id="60d2f-153">**IMsRdpClient2**</span><span class="sxs-lookup"><span data-stu-id="60d2f-153">**IMsRdpClient2**</span></span>](imsrdpclient2.md)
</dt> <dt>

[<span data-ttu-id="60d2f-154">**IMsRdpClient3**</span><span class="sxs-lookup"><span data-stu-id="60d2f-154">**IMsRdpClient3**</span></span>](imsrdpclient3.md)
</dt> <dt>

[<span data-ttu-id="60d2f-155">**IMsRdpClient4**</span><span class="sxs-lookup"><span data-stu-id="60d2f-155">**IMsRdpClient4**</span></span>](imsrdpclient4.md)
</dt> <dt>

[<span data-ttu-id="60d2f-156">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="60d2f-156">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="60d2f-157">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="60d2f-157">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="60d2f-158">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="60d2f-158">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="60d2f-159">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="60d2f-159">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="60d2f-160">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="60d2f-160">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="60d2f-161">**IMsTscAx**</span><span class="sxs-lookup"><span data-stu-id="60d2f-161">**IMsTscAx**</span></span>](imstscax-interface.md)
</dt> <dt>

[<span data-ttu-id="60d2f-162">**IMsTscSecuredSettings**</span><span class="sxs-lookup"><span data-stu-id="60d2f-162">**IMsTscSecuredSettings**</span></span>](imstscsecuredsettings-interface.md)
</dt> </dl>

 

 





