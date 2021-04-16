---
title: IMsRdpClient SecuredSettings2 屬性
description: 捕獲 IMsRdpClientSecuredSettings 介面的指標。 這個介面可以用來設定用戶端控制項的安全設定。
ms.assetid: f570a3f6-70ae-45fd-ba20-75c9f4d2f5ca
ms.tgt_platform: multiple
keywords:
- SecuredSettings2 屬性遠端桌面服務
- SecuredSettings2 屬性遠端桌面服務，IMsRdpClient 介面
- IMsRdpClient 介面遠端桌面服務，SecuredSettings2 屬性
- SecuredSettings2 屬性遠端桌面服務，IMsRdpClient2 介面
- IMsRdpClient2 介面遠端桌面服務，SecuredSettings2 屬性
- SecuredSettings2 屬性遠端桌面服務，IMsRdpClient3 介面
- IMsRdpClient3 介面遠端桌面服務，SecuredSettings2 屬性
- SecuredSettings2 屬性遠端桌面服務，IMsRdpClient4 介面
- IMsRdpClient4 介面遠端桌面服務，SecuredSettings2 屬性
- SecuredSettings2 屬性遠端桌面服務，IMsRdpClient5 介面
- IMsRdpClient5 介面遠端桌面服務，SecuredSettings2 屬性
- SecuredSettings2 屬性遠端桌面服務，IMsRdpClient6 介面
- IMsRdpClient6 介面遠端桌面服務，SecuredSettings2 屬性
- SecuredSettings2 屬性遠端桌面服務，IMsRdpClient7 介面
- IMsRdpClient7 介面遠端桌面服務，SecuredSettings2 屬性
- SecuredSettings2 屬性遠端桌面服務，IMsRdpClient8 介面
- IMsRdpClient8 介面遠端桌面服務，SecuredSettings2 屬性
- SecuredSettings2 屬性遠端桌面服務，IMsRdpClient9 介面
- IMsRdpClient9 介面遠端桌面服務，SecuredSettings2 屬性
- SecuredSettings2 屬性遠端桌面服務，IMsRdpClient10 介面
- IMsRdpClient10 介面遠端桌面服務，SecuredSettings2 屬性
topic_type:
- apiref
api_name:
- IMsRdpClient.SecuredSettings2
- IMsRdpClient.get_SecuredSettings2
- IMsRdpClient2.SecuredSettings2
- IMsRdpClient2.get_SecuredSettings2
- IMsRdpClient3.SecuredSettings2
- IMsRdpClient3.get_SecuredSettings2
- IMsRdpClient4.SecuredSettings2
- IMsRdpClient4.get_SecuredSettings2
- IMsRdpClient5.SecuredSettings2
- IMsRdpClient5.get_SecuredSettings2
- IMsRdpClient6.SecuredSettings2
- IMsRdpClient6.get_SecuredSettings2
- IMsRdpClient7.SecuredSettings2
- IMsRdpClient7.get_SecuredSettings2
- IMsRdpClient8.SecuredSettings2
- IMsRdpClient8.get_SecuredSettings2
- IMsRdpClient9.SecuredSettings2
- IMsRdpClient9.get_SecuredSettings2
- IMsRdpClient10.SecuredSettings2
- IMsRdpClient10.get_SecuredSettings2
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 39e26d9d7a7b2ac776166c251e5a2ab9923297f0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508300"
---
# <a name="imsrdpclientsecuredsettings2-property"></a><span data-ttu-id="30948-125">IMsRdpClient：： SecuredSettings2 屬性</span><span class="sxs-lookup"><span data-stu-id="30948-125">IMsRdpClient::SecuredSettings2 property</span></span>

<span data-ttu-id="30948-126">捕獲 [**IMsRdpClientSecuredSettings**](imsrdpclientsecuredsettings-interface.md) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="30948-126">Retrieves a pointer to the [**IMsRdpClientSecuredSettings**](imsrdpclientsecuredsettings-interface.md) interface.</span></span> <span data-ttu-id="30948-127">這個介面可以用來設定用戶端控制項的安全設定。</span><span class="sxs-lookup"><span data-stu-id="30948-127">This interface can be used to set secured settings for the client control.</span></span>

<span data-ttu-id="30948-128">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="30948-128">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="30948-129">語法</span><span class="sxs-lookup"><span data-stu-id="30948-129">Syntax</span></span>


```C++
HRESULT get_SecuredSettings2(
  [out] IMsRdpClientSecuredSettings **ppSecuredSettings
);
```



## <a name="property-value"></a><span data-ttu-id="30948-130">屬性值</span><span class="sxs-lookup"><span data-stu-id="30948-130">Property value</span></span>

<span data-ttu-id="30948-131">[**IMsRdpClientSecuredSettings**](imsrdpclientsecuredsettings-interface.md)介面指標。</span><span class="sxs-lookup"><span data-stu-id="30948-131">An [**IMsRdpClientSecuredSettings**](imsrdpclientsecuredsettings-interface.md) interface pointer.</span></span>

## <a name="error-codes"></a><span data-ttu-id="30948-132">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="30948-132">Error codes</span></span>

<span data-ttu-id="30948-133">如果方法成功，則會傳回 **S \_ OK** 。</span><span class="sxs-lookup"><span data-stu-id="30948-133">If the method succeeds, **S\_OK** is returned.</span></span> <span data-ttu-id="30948-134">任何其他 **HRESULT** 值都表示呼叫失敗。</span><span class="sxs-lookup"><span data-stu-id="30948-134">Any other **HRESULT** value indicates that the call failed.</span></span>

## <a name="remarks"></a><span data-ttu-id="30948-135">備註</span><span class="sxs-lookup"><span data-stu-id="30948-135">Remarks</span></span>

<span data-ttu-id="30948-136">如需詳細資訊，請參閱 [**IMsRdpClientSecuredSettings**](imsrdpclientsecuredsettings-interface.md) 介面，並 [提供 RDP 用戶端安全性](providing-for-rdp-client-security.md)。</span><span class="sxs-lookup"><span data-stu-id="30948-136">For more information, see the [**IMsRdpClientSecuredSettings**](imsrdpclientsecuredsettings-interface.md) interface, and [Providing for RDP Client Security](providing-for-rdp-client-security.md).</span></span>

<span data-ttu-id="30948-137">如需遠端桌面網頁連線的詳細資訊，請參閱 [遠端桌面網頁連線的需求](requirements-for-remote-desktop-web-connection.md)。</span><span class="sxs-lookup"><span data-stu-id="30948-137">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="30948-138">規格需求</span><span class="sxs-lookup"><span data-stu-id="30948-138">Requirements</span></span>



| <span data-ttu-id="30948-139">需求</span><span class="sxs-lookup"><span data-stu-id="30948-139">Requirement</span></span> | <span data-ttu-id="30948-140">值</span><span class="sxs-lookup"><span data-stu-id="30948-140">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="30948-141">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="30948-141">Minimum supported client</span></span><br/> | <span data-ttu-id="30948-142">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="30948-142">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="30948-143">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="30948-143">Minimum supported server</span></span><br/> | <span data-ttu-id="30948-144">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="30948-144">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="30948-145">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="30948-145">Type library</span></span><br/>             | <dl> <span data-ttu-id="30948-146"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="30948-146"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="30948-147">DLL</span><span class="sxs-lookup"><span data-stu-id="30948-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="30948-148"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="30948-148"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="30948-149">IID</span><span class="sxs-lookup"><span data-stu-id="30948-149">IID</span></span><br/>                      | <span data-ttu-id="30948-150">IID \_ IMsRdpClient 定義為92b4a539-7115-4b7c-a5a9-e5d9efc2780a</span><span class="sxs-lookup"><span data-stu-id="30948-150">IID\_IMsRdpClient is defined as 92b4a539-7115-4b7c-a5a9-e5d9efc2780a</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="30948-151">另請參閱</span><span class="sxs-lookup"><span data-stu-id="30948-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="30948-152">**IMsRdpClient**</span><span class="sxs-lookup"><span data-stu-id="30948-152">**IMsRdpClient**</span></span>](imsrdpclient-interface.md)
</dt> <dt>

[<span data-ttu-id="30948-153">**IMsRdpClient2**</span><span class="sxs-lookup"><span data-stu-id="30948-153">**IMsRdpClient2**</span></span>](imsrdpclient2.md)
</dt> <dt>

[<span data-ttu-id="30948-154">**IMsRdpClient3**</span><span class="sxs-lookup"><span data-stu-id="30948-154">**IMsRdpClient3**</span></span>](imsrdpclient3.md)
</dt> <dt>

[<span data-ttu-id="30948-155">**IMsRdpClient4**</span><span class="sxs-lookup"><span data-stu-id="30948-155">**IMsRdpClient4**</span></span>](imsrdpclient4.md)
</dt> <dt>

[<span data-ttu-id="30948-156">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="30948-156">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="30948-157">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="30948-157">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="30948-158">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="30948-158">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="30948-159">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="30948-159">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="30948-160">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="30948-160">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="30948-161">**IMsRdpClient10**</span><span class="sxs-lookup"><span data-stu-id="30948-161">**IMsRdpClient10**</span></span>](imsrdpclient10.md)
</dt> </dl>

 

 





