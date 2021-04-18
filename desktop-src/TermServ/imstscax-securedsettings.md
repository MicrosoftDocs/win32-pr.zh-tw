---
title: IMsTscAx SecuredSettings 屬性
description: 捕獲 IMsTscSecuredSettings 介面指標。
ms.assetid: 64d4059b-e617-449d-a733-c19c1d281132
ms.tgt_platform: multiple
keywords:
- SecuredSettings 屬性遠端桌面服務
- SecuredSettings 屬性遠端桌面服務，IMsTscAx 介面
- IMsTscAx 介面遠端桌面服務，SecuredSettings 屬性
- SecuredSettings 屬性遠端桌面服務，IMsRdpClient 介面
- IMsRdpClient 介面遠端桌面服務，SecuredSettings 屬性
- SecuredSettings 屬性遠端桌面服務，IMsRdpClient2 介面
- IMsRdpClient2 介面遠端桌面服務，SecuredSettings 屬性
- SecuredSettings 屬性遠端桌面服務，IMsRdpClient3 介面
- IMsRdpClient3 介面遠端桌面服務，SecuredSettings 屬性
- SecuredSettings 屬性遠端桌面服務，IMsRdpClient4 介面
- IMsRdpClient4 介面遠端桌面服務，SecuredSettings 屬性
- SecuredSettings 屬性遠端桌面服務，IMsRdpClient5 介面
- IMsRdpClient5 介面遠端桌面服務，SecuredSettings 屬性
- SecuredSettings 屬性遠端桌面服務，IMsRdpClient6 介面
- IMsRdpClient6 介面遠端桌面服務，SecuredSettings 屬性
- SecuredSettings 屬性遠端桌面服務，IMsRdpClient7 介面
- IMsRdpClient7 介面遠端桌面服務，SecuredSettings 屬性
- SecuredSettings 屬性遠端桌面服務，IMsRdpClient8 介面
- IMsRdpClient8 介面遠端桌面服務，SecuredSettings 屬性
- SecuredSettings 屬性遠端桌面服務，IMsRdpClient9 介面
- IMsRdpClient9 介面遠端桌面服務，SecuredSettings 屬性
topic_type:
- apiref
api_name:
- IMsTscAx.SecuredSettings
- IMsTscAx.get_SecuredSettings
- IMsRdpClient.SecuredSettings
- IMsRdpClient.get_SecuredSettings
- IMsRdpClient2.SecuredSettings
- IMsRdpClient2.get_SecuredSettings
- IMsRdpClient3.SecuredSettings
- IMsRdpClient3.get_SecuredSettings
- IMsRdpClient4.SecuredSettings
- IMsRdpClient4.get_SecuredSettings
- IMsRdpClient5.SecuredSettings
- IMsRdpClient5.get_SecuredSettings
- IMsRdpClient6.SecuredSettings
- IMsRdpClient6.get_SecuredSettings
- IMsRdpClient7.SecuredSettings
- IMsRdpClient7.get_SecuredSettings
- IMsRdpClient8.SecuredSettings
- IMsRdpClient8.get_SecuredSettings
- IMsRdpClient9.SecuredSettings
- IMsRdpClient9.get_SecuredSettings
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6610448d822fe75082c225686dc6d809229a325f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103685"
---
# <a name="imstscaxsecuredsettings-property"></a><span data-ttu-id="75d6f-124">IMsTscAx：： SecuredSettings 屬性</span><span class="sxs-lookup"><span data-stu-id="75d6f-124">IMsTscAx::SecuredSettings property</span></span>

<span data-ttu-id="75d6f-125">捕獲 [**IMsTscSecuredSettings**](imstscsecuredsettings-interface.md) 介面指標。</span><span class="sxs-lookup"><span data-stu-id="75d6f-125">Retrieves an [**IMsTscSecuredSettings**](imstscsecuredsettings-interface.md) interface pointer.</span></span>

<span data-ttu-id="75d6f-126">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="75d6f-126">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="75d6f-127">語法</span><span class="sxs-lookup"><span data-stu-id="75d6f-127">Syntax</span></span>


```C++
HRESULT get_SecuredSettings(
  [out] IMsTscSecuredSettings **ppSecuredSettings
);
```



## <a name="property-value"></a><span data-ttu-id="75d6f-128">屬性值</span><span class="sxs-lookup"><span data-stu-id="75d6f-128">Property value</span></span>

<span data-ttu-id="75d6f-129">[**IMsTscSecuredSettings**](imstscsecuredsettings-interface.md)介面指標。</span><span class="sxs-lookup"><span data-stu-id="75d6f-129">An [**IMsTscSecuredSettings**](imstscsecuredsettings-interface.md) interface pointer.</span></span>

## <a name="error-codes"></a><span data-ttu-id="75d6f-130">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="75d6f-130">Error codes</span></span>

<span data-ttu-id="75d6f-131">如果成功，則傳回 **S \_ OK** 。</span><span class="sxs-lookup"><span data-stu-id="75d6f-131">Return **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="75d6f-132">備註</span><span class="sxs-lookup"><span data-stu-id="75d6f-132">Remarks</span></span>

<span data-ttu-id="75d6f-133">如果控制項裝載在網頁中，且目前的 Internet Explorer URL 安全性區域不允許抓取介面位址，則這個方法會傳回 **E \_ FAIL**。</span><span class="sxs-lookup"><span data-stu-id="75d6f-133">If the control is hosted in a webpage and the current Internet Explorer URL security zone does not permit the retrieval of the interface address, this method returns **E\_FAIL**.</span></span>

<span data-ttu-id="75d6f-134">如需 [**IMsTscSecuredSettings**](imstscsecuredsettings-interface.md)介面可用性的限制，請參閱 [**SecuredSettingsEnabled**](imstscax-securedsettingsenabled.md) 。</span><span class="sxs-lookup"><span data-stu-id="75d6f-134">Refer to [**SecuredSettingsEnabled**](imstscax-securedsettingsenabled.md) for restrictions on the availability of the [**IMsTscSecuredSettings**](imstscsecuredsettings-interface.md) interface.</span></span>

<span data-ttu-id="75d6f-135">如需遠端桌面網頁連線的詳細資訊，請參閱 [遠端桌面網頁連線的需求](requirements-for-remote-desktop-web-connection.md)。</span><span class="sxs-lookup"><span data-stu-id="75d6f-135">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="75d6f-136">規格需求</span><span class="sxs-lookup"><span data-stu-id="75d6f-136">Requirements</span></span>



| <span data-ttu-id="75d6f-137">需求</span><span class="sxs-lookup"><span data-stu-id="75d6f-137">Requirement</span></span> | <span data-ttu-id="75d6f-138">值</span><span class="sxs-lookup"><span data-stu-id="75d6f-138">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="75d6f-139">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="75d6f-139">Minimum supported client</span></span><br/> | <span data-ttu-id="75d6f-140">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="75d6f-140">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="75d6f-141">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="75d6f-141">Minimum supported server</span></span><br/> | <span data-ttu-id="75d6f-142">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="75d6f-142">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="75d6f-143">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="75d6f-143">Type library</span></span><br/>             | <dl> <span data-ttu-id="75d6f-144"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="75d6f-144"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="75d6f-145">DLL</span><span class="sxs-lookup"><span data-stu-id="75d6f-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="75d6f-146"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="75d6f-146"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="75d6f-147">IID</span><span class="sxs-lookup"><span data-stu-id="75d6f-147">IID</span></span><br/>                      | <span data-ttu-id="75d6f-148">IID \_ IMsTscAx 定義為8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span><span class="sxs-lookup"><span data-stu-id="75d6f-148">IID\_IMsTscAx is defined as 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="75d6f-149">另請參閱</span><span class="sxs-lookup"><span data-stu-id="75d6f-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="75d6f-150">**IMsRdpClient**</span><span class="sxs-lookup"><span data-stu-id="75d6f-150">**IMsRdpClient**</span></span>](imsrdpclient-interface.md)
</dt> <dt>

[<span data-ttu-id="75d6f-151">**IMsRdpClient2**</span><span class="sxs-lookup"><span data-stu-id="75d6f-151">**IMsRdpClient2**</span></span>](imsrdpclient2.md)
</dt> <dt>

[<span data-ttu-id="75d6f-152">**IMsRdpClient3**</span><span class="sxs-lookup"><span data-stu-id="75d6f-152">**IMsRdpClient3**</span></span>](imsrdpclient3.md)
</dt> <dt>

[<span data-ttu-id="75d6f-153">**IMsRdpClient4**</span><span class="sxs-lookup"><span data-stu-id="75d6f-153">**IMsRdpClient4**</span></span>](imsrdpclient4.md)
</dt> <dt>

[<span data-ttu-id="75d6f-154">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="75d6f-154">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="75d6f-155">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="75d6f-155">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="75d6f-156">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="75d6f-156">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="75d6f-157">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="75d6f-157">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="75d6f-158">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="75d6f-158">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="75d6f-159">**IMsTscAx**</span><span class="sxs-lookup"><span data-stu-id="75d6f-159">**IMsTscAx**</span></span>](imstscax-interface.md)
</dt> <dt>

[<span data-ttu-id="75d6f-160">**IMsTscSecuredSettings**</span><span class="sxs-lookup"><span data-stu-id="75d6f-160">**IMsTscSecuredSettings**</span></span>](imstscsecuredsettings-interface.md)
</dt> </dl>

 

 





