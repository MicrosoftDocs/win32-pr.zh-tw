---
title: IMsRdpClient2 AdvancedSettings3 屬性
description: 捕獲 IMsRdpClientAdvancedSettings2 介面的指標。 介面可以用來設定用戶端控制項的 advanced 設定。
ms.assetid: 69353bfa-973e-4c6a-8f7e-1b9514be2539
ms.tgt_platform: multiple
keywords:
- AdvancedSettings3 屬性遠端桌面服務
- AdvancedSettings3 屬性遠端桌面服務，IMsRdpClient2 介面
- IMsRdpClient2 介面遠端桌面服務，AdvancedSettings3 屬性
- AdvancedSettings3 屬性遠端桌面服務，IMsRdpClient3 介面
- IMsRdpClient3 介面遠端桌面服務，AdvancedSettings3 屬性
- AdvancedSettings3 屬性遠端桌面服務，IMsRdpClient4 介面
- IMsRdpClient4 介面遠端桌面服務，AdvancedSettings3 屬性
- AdvancedSettings3 屬性遠端桌面服務，IMsRdpClient5 介面
- IMsRdpClient5 介面遠端桌面服務，AdvancedSettings3 屬性
- AdvancedSettings3 屬性遠端桌面服務，IMsRdpClient6 介面
- IMsRdpClient6 介面遠端桌面服務，AdvancedSettings3 屬性
- AdvancedSettings3 屬性遠端桌面服務，IMsRdpClient7 介面
- IMsRdpClient7 介面遠端桌面服務，AdvancedSettings3 屬性
- AdvancedSettings3 屬性遠端桌面服務，IMsRdpClient8 介面
- IMsRdpClient8 介面遠端桌面服務，AdvancedSettings3 屬性
- AdvancedSettings3 屬性遠端桌面服務，IMsRdpClient9 介面
- IMsRdpClient9 介面遠端桌面服務，AdvancedSettings3 屬性
- AdvancedSettings3 屬性遠端桌面服務，IMsRdpClient10 介面
- IMsRdpClient10 介面遠端桌面服務，AdvancedSettings3 屬性
topic_type:
- apiref
api_name:
- IMsRdpClient2.AdvancedSettings3
- IMsRdpClient2.get_AdvancedSettings3
- IMsRdpClient3.AdvancedSettings3
- IMsRdpClient3.get_AdvancedSettings3
- IMsRdpClient4.AdvancedSettings3
- IMsRdpClient4.get_AdvancedSettings3
- IMsRdpClient5.AdvancedSettings3
- IMsRdpClient5.get_AdvancedSettings3
- IMsRdpClient6.AdvancedSettings3
- IMsRdpClient6.get_AdvancedSettings3
- IMsRdpClient7.AdvancedSettings3
- IMsRdpClient7.get_AdvancedSettings3
- IMsRdpClient8.AdvancedSettings3
- IMsRdpClient8.get_AdvancedSettings3
- IMsRdpClient9.AdvancedSettings3
- IMsRdpClient9.get_AdvancedSettings3
- IMsRdpClient10.AdvancedSettings3
- IMsRdpClient10.get_AdvancedSettings3
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf16d56eaff321d313e3a27eb6dd774ef67e13ca
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104317303"
---
# <a name="imsrdpclient2advancedsettings3-property"></a><span data-ttu-id="c4a80-123">IMsRdpClient2：： AdvancedSettings3 屬性</span><span class="sxs-lookup"><span data-stu-id="c4a80-123">IMsRdpClient2::AdvancedSettings3 property</span></span>

<span data-ttu-id="c4a80-124">捕獲 [**IMsRdpClientAdvancedSettings2**](imsrdpclientadvancedsettings2.md) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="c4a80-124">Retrieves a pointer to the [**IMsRdpClientAdvancedSettings2**](imsrdpclientadvancedsettings2.md) interface.</span></span> <span data-ttu-id="c4a80-125">介面可以用來設定用戶端控制項的 advanced 設定。</span><span class="sxs-lookup"><span data-stu-id="c4a80-125">The interface can be used to set advanced settings for the client control.</span></span>

<span data-ttu-id="c4a80-126">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="c4a80-126">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="c4a80-127">語法</span><span class="sxs-lookup"><span data-stu-id="c4a80-127">Syntax</span></span>


```C++
HRESULT get_AdvancedSettings3(
  [out] IMsRdpClientAdvancedSettings2 **ppAdvSettings
);
```



## <a name="property-value"></a><span data-ttu-id="c4a80-128">屬性值</span><span class="sxs-lookup"><span data-stu-id="c4a80-128">Property value</span></span>

<span data-ttu-id="c4a80-129">捕獲 [**IMsRdpClientAdvancedSettings2**](imsrdpclientadvancedsettings2.md) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="c4a80-129">Retrieves a pointer to the [**IMsRdpClientAdvancedSettings2**](imsrdpclientadvancedsettings2.md) interface.</span></span>

## <a name="error-codes"></a><span data-ttu-id="c4a80-130">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="c4a80-130">Error codes</span></span>

<span data-ttu-id="c4a80-131">如果方法成功，則會傳回 **S \_ OK** 。</span><span class="sxs-lookup"><span data-stu-id="c4a80-131">If the method succeeds, **S\_OK** is returned.</span></span> <span data-ttu-id="c4a80-132">任何其他 **HRESULT** 值都表示呼叫失敗。</span><span class="sxs-lookup"><span data-stu-id="c4a80-132">Any other **HRESULT** value indicates that the call failed.</span></span>

## <a name="remarks"></a><span data-ttu-id="c4a80-133">備註</span><span class="sxs-lookup"><span data-stu-id="c4a80-133">Remarks</span></span>

<span data-ttu-id="c4a80-134">如需遠端桌面網頁連線的詳細資訊，請參閱 [遠端桌面網頁連線的需求](requirements-for-remote-desktop-web-connection.md)。</span><span class="sxs-lookup"><span data-stu-id="c4a80-134">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c4a80-135">規格需求</span><span class="sxs-lookup"><span data-stu-id="c4a80-135">Requirements</span></span>



| <span data-ttu-id="c4a80-136">需求</span><span class="sxs-lookup"><span data-stu-id="c4a80-136">Requirement</span></span> | <span data-ttu-id="c4a80-137">值</span><span class="sxs-lookup"><span data-stu-id="c4a80-137">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c4a80-138">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c4a80-138">Minimum supported client</span></span><br/> | <span data-ttu-id="c4a80-139">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c4a80-139">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="c4a80-140">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c4a80-140">Minimum supported server</span></span><br/> | <span data-ttu-id="c4a80-141">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c4a80-141">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="c4a80-142">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="c4a80-142">Type library</span></span><br/>             | <dl> <span data-ttu-id="c4a80-143"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c4a80-143"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="c4a80-144">DLL</span><span class="sxs-lookup"><span data-stu-id="c4a80-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c4a80-145"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c4a80-145"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="c4a80-146">IID</span><span class="sxs-lookup"><span data-stu-id="c4a80-146">IID</span></span><br/>                      | <span data-ttu-id="c4a80-147">IID \_ IMsRdpClient2 定義為 e7e17dc4-3b71-4ba7-a8e6-281ffadca28f</span><span class="sxs-lookup"><span data-stu-id="c4a80-147">IID\_IMsRdpClient2 is defined as e7e17dc4-3b71-4ba7-a8e6-281ffadca28f</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="c4a80-148">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c4a80-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c4a80-149">**IMsRdpClient2**</span><span class="sxs-lookup"><span data-stu-id="c4a80-149">**IMsRdpClient2**</span></span>](imsrdpclient2.md)
</dt> <dt>

[<span data-ttu-id="c4a80-150">**IMsRdpClient3**</span><span class="sxs-lookup"><span data-stu-id="c4a80-150">**IMsRdpClient3**</span></span>](imsrdpclient3.md)
</dt> <dt>

[<span data-ttu-id="c4a80-151">**IMsRdpClient4**</span><span class="sxs-lookup"><span data-stu-id="c4a80-151">**IMsRdpClient4**</span></span>](imsrdpclient4.md)
</dt> <dt>

[<span data-ttu-id="c4a80-152">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="c4a80-152">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="c4a80-153">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="c4a80-153">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="c4a80-154">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="c4a80-154">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="c4a80-155">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="c4a80-155">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="c4a80-156">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="c4a80-156">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="c4a80-157">**IMsRdpClient10**</span><span class="sxs-lookup"><span data-stu-id="c4a80-157">**IMsRdpClient10**</span></span>](imsrdpclient10.md)
</dt> </dl>

 

 





