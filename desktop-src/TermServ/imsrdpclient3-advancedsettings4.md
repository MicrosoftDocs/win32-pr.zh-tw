---
title: IMsRdpClient3 AdvancedSettings4 屬性
description: 捕獲 IMsRdpClientAdvancedSettings3 介面的指標。
ms.assetid: 30935099-7f33-4745-8a31-f9a28ab78b63
ms.tgt_platform: multiple
keywords:
- AdvancedSettings4 屬性遠端桌面服務
- AdvancedSettings4 屬性遠端桌面服務，IMsRdpClient3 介面
- IMsRdpClient3 介面遠端桌面服務，AdvancedSettings4 屬性
- AdvancedSettings4 屬性遠端桌面服務，IMsRdpClient4 介面
- IMsRdpClient4 介面遠端桌面服務，AdvancedSettings4 屬性
- AdvancedSettings4 屬性遠端桌面服務，IMsRdpClient5 介面
- IMsRdpClient5 介面遠端桌面服務，AdvancedSettings4 屬性
- AdvancedSettings4 屬性遠端桌面服務，IMsRdpClient6 介面
- IMsRdpClient6 介面遠端桌面服務，AdvancedSettings4 屬性
- AdvancedSettings4 屬性遠端桌面服務，IMsRdpClient7 介面
- IMsRdpClient7 介面遠端桌面服務，AdvancedSettings4 屬性
- AdvancedSettings4 屬性遠端桌面服務，IMsRdpClient8 介面
- IMsRdpClient8 介面遠端桌面服務，AdvancedSettings4 屬性
- AdvancedSettings4 屬性遠端桌面服務，IMsRdpClient9 介面
- IMsRdpClient9 介面遠端桌面服務，AdvancedSettings4 屬性
- AdvancedSettings4 屬性遠端桌面服務，IMsRdpClient10 介面
- IMsRdpClient10 介面遠端桌面服務，AdvancedSettings4 屬性
topic_type:
- apiref
api_name:
- IMsRdpClient3.AdvancedSettings4
- IMsRdpClient3.get_AdvancedSettings4
- IMsRdpClient4.AdvancedSettings4
- IMsRdpClient4.get_AdvancedSettings4
- IMsRdpClient5.AdvancedSettings4
- IMsRdpClient5.get_AdvancedSettings4
- IMsRdpClient6.AdvancedSettings4
- IMsRdpClient6.get_AdvancedSettings4
- IMsRdpClient7.AdvancedSettings4
- IMsRdpClient7.get_AdvancedSettings4
- IMsRdpClient8.AdvancedSettings4
- IMsRdpClient8.get_AdvancedSettings4
- IMsRdpClient9.AdvancedSettings4
- IMsRdpClient9.get_AdvancedSettings4
- IMsRdpClient10.AdvancedSettings4
- IMsRdpClient10.get_AdvancedSettings4
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c7a229c28b645e7920212a04cc44ca5a9ce42be3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843220"
---
# <a name="imsrdpclient3advancedsettings4-property"></a><span data-ttu-id="e1192-120">IMsRdpClient3：： AdvancedSettings4 屬性</span><span class="sxs-lookup"><span data-stu-id="e1192-120">IMsRdpClient3::AdvancedSettings4 property</span></span>

<span data-ttu-id="e1192-121">捕獲 [**IMsRdpClientAdvancedSettings3**](imsrdpclientadvancedsettings3.md) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="e1192-121">Retrieves a pointer to the [**IMsRdpClientAdvancedSettings3**](imsrdpclientadvancedsettings3.md) interface.</span></span>

<span data-ttu-id="e1192-122">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="e1192-122">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="e1192-123">語法</span><span class="sxs-lookup"><span data-stu-id="e1192-123">Syntax</span></span>


```C++
HRESULT get_AdvancedSettings4(
  [out] IMsRdpClientAdvancedSettings3 **ppAdvSettings
);
```



## <a name="property-value"></a><span data-ttu-id="e1192-124">屬性值</span><span class="sxs-lookup"><span data-stu-id="e1192-124">Property value</span></span>

<span data-ttu-id="e1192-125">[**IMsRdpClientAdvancedSettings3**](imsrdpclientadvancedsettings3.md)介面的指標。</span><span class="sxs-lookup"><span data-stu-id="e1192-125">Pointer to the [**IMsRdpClientAdvancedSettings3**](imsrdpclientadvancedsettings3.md) interface.</span></span> <span data-ttu-id="e1192-126">介面可以用來設定用戶端控制項的 advanced 設定。</span><span class="sxs-lookup"><span data-stu-id="e1192-126">The interface can be used to set advanced settings for the client control.</span></span>

## <a name="error-codes"></a><span data-ttu-id="e1192-127">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="e1192-127">Error codes</span></span>

<span data-ttu-id="e1192-128">如果方法成功，則會傳回 **S \_ OK** 。</span><span class="sxs-lookup"><span data-stu-id="e1192-128">If the method succeeds, **S\_OK** is returned.</span></span> <span data-ttu-id="e1192-129">任何其他 **HRESULT** 值都表示呼叫失敗。</span><span class="sxs-lookup"><span data-stu-id="e1192-129">Any other **HRESULT** value indicates that the call failed.</span></span>

## <a name="remarks"></a><span data-ttu-id="e1192-130">備註</span><span class="sxs-lookup"><span data-stu-id="e1192-130">Remarks</span></span>

<span data-ttu-id="e1192-131">連接控制項時，無法設定這個屬性。</span><span class="sxs-lookup"><span data-stu-id="e1192-131">This property cannot be set when the control is connected.</span></span>

<span data-ttu-id="e1192-132">如需遠端桌面網頁連線的詳細資訊，請參閱 [遠端桌面網頁連線的需求](requirements-for-remote-desktop-web-connection.md)。</span><span class="sxs-lookup"><span data-stu-id="e1192-132">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e1192-133">規格需求</span><span class="sxs-lookup"><span data-stu-id="e1192-133">Requirements</span></span>



| <span data-ttu-id="e1192-134">需求</span><span class="sxs-lookup"><span data-stu-id="e1192-134">Requirement</span></span> | <span data-ttu-id="e1192-135">值</span><span class="sxs-lookup"><span data-stu-id="e1192-135">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e1192-136">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e1192-136">Minimum supported client</span></span><br/> | <span data-ttu-id="e1192-137">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e1192-137">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="e1192-138">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e1192-138">Minimum supported server</span></span><br/> | <span data-ttu-id="e1192-139">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e1192-139">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="e1192-140">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="e1192-140">Type library</span></span><br/>             | <dl> <span data-ttu-id="e1192-141"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e1192-141"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="e1192-142">DLL</span><span class="sxs-lookup"><span data-stu-id="e1192-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e1192-143"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e1192-143"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="e1192-144">IID</span><span class="sxs-lookup"><span data-stu-id="e1192-144">IID</span></span><br/>                      | <span data-ttu-id="e1192-145">IID \_ IMsRdpClient3 定義為91b7cbc5-a72e-4fa0-9300-d647d7e897ff</span><span class="sxs-lookup"><span data-stu-id="e1192-145">IID\_IMsRdpClient3 is defined as 91b7cbc5-a72e-4fa0-9300-d647d7e897ff</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="e1192-146">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e1192-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e1192-147">**IMsRdpClient3**</span><span class="sxs-lookup"><span data-stu-id="e1192-147">**IMsRdpClient3**</span></span>](imsrdpclient3.md)
</dt> <dt>

[<span data-ttu-id="e1192-148">**IMsRdpClient4**</span><span class="sxs-lookup"><span data-stu-id="e1192-148">**IMsRdpClient4**</span></span>](imsrdpclient4.md)
</dt> <dt>

[<span data-ttu-id="e1192-149">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="e1192-149">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="e1192-150">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="e1192-150">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="e1192-151">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="e1192-151">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="e1192-152">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="e1192-152">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="e1192-153">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="e1192-153">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="e1192-154">**IMsRdpClient10**</span><span class="sxs-lookup"><span data-stu-id="e1192-154">**IMsRdpClient10**</span></span>](imsrdpclient10.md)
</dt> </dl>

 

 





