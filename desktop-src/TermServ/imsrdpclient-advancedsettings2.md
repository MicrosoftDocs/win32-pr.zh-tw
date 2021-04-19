---
title: IMsRdpClient AdvancedSettings2 屬性
description: 捕獲 IMsRdpClientAdvancedSettings 介面的指標。 介面可以用來設定用戶端控制項的 advanced 設定。
ms.assetid: 207b625c-fc2b-41ad-9339-9f3c3b8eeab7
ms.tgt_platform: multiple
keywords:
- AdvancedSettings2 屬性遠端桌面服務
- AdvancedSettings2 屬性遠端桌面服務，IMsRdpClient 介面
- IMsRdpClient 介面遠端桌面服務，AdvancedSettings2 屬性
- AdvancedSettings2 屬性遠端桌面服務，IMsRdpClient2 介面
- IMsRdpClient2 介面遠端桌面服務，AdvancedSettings2 屬性
- AdvancedSettings2 屬性遠端桌面服務，IMsRdpClient3 介面
- IMsRdpClient3 介面遠端桌面服務，AdvancedSettings2 屬性
- AdvancedSettings2 屬性遠端桌面服務，IMsRdpClient4 介面
- IMsRdpClient4 介面遠端桌面服務，AdvancedSettings2 屬性
- AdvancedSettings2 屬性遠端桌面服務，IMsRdpClient5 介面
- IMsRdpClient5 介面遠端桌面服務，AdvancedSettings2 屬性
- AdvancedSettings2 屬性遠端桌面服務，IMsRdpClient6 介面
- IMsRdpClient6 介面遠端桌面服務，AdvancedSettings2 屬性
- AdvancedSettings2 屬性遠端桌面服務，IMsRdpClient7 介面
- IMsRdpClient7 介面遠端桌面服務，AdvancedSettings2 屬性
- AdvancedSettings2 屬性遠端桌面服務，IMsRdpClient8 介面
- IMsRdpClient8 介面遠端桌面服務，AdvancedSettings2 屬性
- AdvancedSettings2 屬性遠端桌面服務，IMsRdpClient9 介面
- IMsRdpClient9 介面遠端桌面服務，AdvancedSettings2 屬性
- AdvancedSettings2 屬性遠端桌面服務，IMsRdpClient10 介面
- IMsRdpClient10 介面遠端桌面服務，AdvancedSettings2 屬性
topic_type:
- apiref
api_name:
- IMsRdpClient.AdvancedSettings2
- IMsRdpClient.get_AdvancedSettings2
- IMsRdpClient2.AdvancedSettings2
- IMsRdpClient2.get_AdvancedSettings2
- IMsRdpClient3.AdvancedSettings2
- IMsRdpClient3.get_AdvancedSettings2
- IMsRdpClient4.AdvancedSettings2
- IMsRdpClient4.get_AdvancedSettings2
- IMsRdpClient5.AdvancedSettings2
- IMsRdpClient5.get_AdvancedSettings2
- IMsRdpClient6.AdvancedSettings2
- IMsRdpClient6.get_AdvancedSettings2
- IMsRdpClient7.AdvancedSettings2
- IMsRdpClient7.get_AdvancedSettings2
- IMsRdpClient8.AdvancedSettings2
- IMsRdpClient8.get_AdvancedSettings2
- IMsRdpClient9.AdvancedSettings2
- IMsRdpClient9.get_AdvancedSettings2
- IMsRdpClient10.AdvancedSettings2
- IMsRdpClient10.get_AdvancedSettings2
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 683d56d5e9501114b1e60635ca406b4509d2032b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106966950"
---
# <a name="imsrdpclientadvancedsettings2-property"></a><span data-ttu-id="6731b-125">IMsRdpClient：： AdvancedSettings2 屬性</span><span class="sxs-lookup"><span data-stu-id="6731b-125">IMsRdpClient::AdvancedSettings2 property</span></span>

<span data-ttu-id="6731b-126">捕獲 [**IMsRdpClientAdvancedSettings**](imsrdpclientadvancedsettings-interface.md) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="6731b-126">Retrieves a pointer to the [**IMsRdpClientAdvancedSettings**](imsrdpclientadvancedsettings-interface.md) interface.</span></span> <span data-ttu-id="6731b-127">介面可以用來設定用戶端控制項的 advanced 設定。</span><span class="sxs-lookup"><span data-stu-id="6731b-127">The interface can be used to set advanced settings for the client control.</span></span>

<span data-ttu-id="6731b-128">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="6731b-128">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="6731b-129">語法</span><span class="sxs-lookup"><span data-stu-id="6731b-129">Syntax</span></span>


```C++
HRESULT get_AdvancedSettings2(
  [out] IMsRdpClientAdvancedSettings **ppAdvSettings
);
```



## <a name="property-value"></a><span data-ttu-id="6731b-130">屬性值</span><span class="sxs-lookup"><span data-stu-id="6731b-130">Property value</span></span>

<span data-ttu-id="6731b-131">[**IMsRdpClientAdvancedSettings**](imsrdpclientadvancedsettings-interface.md)介面的指標。</span><span class="sxs-lookup"><span data-stu-id="6731b-131">Pointer to the [**IMsRdpClientAdvancedSettings**](imsrdpclientadvancedsettings-interface.md) interface.</span></span> <span data-ttu-id="6731b-132">介面可以用來設定用戶端控制項的 advanced 設定。</span><span class="sxs-lookup"><span data-stu-id="6731b-132">The interface can be used to set advanced settings for the client control.</span></span>

## <a name="error-codes"></a><span data-ttu-id="6731b-133">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="6731b-133">Error codes</span></span>

<span data-ttu-id="6731b-134">如果方法成功，則會傳回 **S \_ OK** 。</span><span class="sxs-lookup"><span data-stu-id="6731b-134">If the method succeeds, **S\_OK** is returned.</span></span> <span data-ttu-id="6731b-135">任何其他 **HRESULT** 值都表示呼叫失敗。</span><span class="sxs-lookup"><span data-stu-id="6731b-135">Any other **HRESULT** value indicates that the call failed.</span></span>

## <a name="remarks"></a><span data-ttu-id="6731b-136">備註</span><span class="sxs-lookup"><span data-stu-id="6731b-136">Remarks</span></span>

<span data-ttu-id="6731b-137">如需遠端桌面網頁連線的詳細資訊，請參閱 [遠端桌面網頁連線的需求](requirements-for-remote-desktop-web-connection.md)。</span><span class="sxs-lookup"><span data-stu-id="6731b-137">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6731b-138">規格需求</span><span class="sxs-lookup"><span data-stu-id="6731b-138">Requirements</span></span>



| <span data-ttu-id="6731b-139">需求</span><span class="sxs-lookup"><span data-stu-id="6731b-139">Requirement</span></span> | <span data-ttu-id="6731b-140">值</span><span class="sxs-lookup"><span data-stu-id="6731b-140">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6731b-141">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6731b-141">Minimum supported client</span></span><br/> | <span data-ttu-id="6731b-142">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6731b-142">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="6731b-143">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6731b-143">Minimum supported server</span></span><br/> | <span data-ttu-id="6731b-144">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6731b-144">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="6731b-145">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="6731b-145">Type library</span></span><br/>             | <dl> <span data-ttu-id="6731b-146"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6731b-146"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="6731b-147">DLL</span><span class="sxs-lookup"><span data-stu-id="6731b-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6731b-148"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6731b-148"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="6731b-149">IID</span><span class="sxs-lookup"><span data-stu-id="6731b-149">IID</span></span><br/>                      | <span data-ttu-id="6731b-150">IID \_ IMsRdpClient 定義為92b4a539-7115-4b7c-a5a9-e5d9efc2780a</span><span class="sxs-lookup"><span data-stu-id="6731b-150">IID\_IMsRdpClient is defined as 92b4a539-7115-4b7c-a5a9-e5d9efc2780a</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="6731b-151">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6731b-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6731b-152">**IMsRdpClient**</span><span class="sxs-lookup"><span data-stu-id="6731b-152">**IMsRdpClient**</span></span>](imsrdpclient-interface.md)
</dt> <dt>

[<span data-ttu-id="6731b-153">**IMsRdpClient2**</span><span class="sxs-lookup"><span data-stu-id="6731b-153">**IMsRdpClient2**</span></span>](imsrdpclient2.md)
</dt> <dt>

[<span data-ttu-id="6731b-154">**IMsRdpClient3**</span><span class="sxs-lookup"><span data-stu-id="6731b-154">**IMsRdpClient3**</span></span>](imsrdpclient3.md)
</dt> <dt>

[<span data-ttu-id="6731b-155">**IMsRdpClient4**</span><span class="sxs-lookup"><span data-stu-id="6731b-155">**IMsRdpClient4**</span></span>](imsrdpclient4.md)
</dt> <dt>

[<span data-ttu-id="6731b-156">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="6731b-156">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="6731b-157">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="6731b-157">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="6731b-158">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="6731b-158">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="6731b-159">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="6731b-159">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="6731b-160">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="6731b-160">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="6731b-161">**IMsRdpClient10**</span><span class="sxs-lookup"><span data-stu-id="6731b-161">**IMsRdpClient10**</span></span>](imsrdpclient10.md)
</dt> </dl>

 

 





