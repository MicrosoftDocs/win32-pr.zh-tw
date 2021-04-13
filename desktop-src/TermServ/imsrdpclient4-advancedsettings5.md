---
title: IMsRdpClient4 AdvancedSettings5 屬性
description: 捕獲 IMsRdpClientAdvancedSettings4 介面的指標。
ms.assetid: 2dd0cc5f-7822-485f-8b3f-12407af1e091
ms.tgt_platform: multiple
keywords:
- AdvancedSettings5 屬性遠端桌面服務
- AdvancedSettings5 屬性遠端桌面服務，IMsRdpClient4 介面
- IMsRdpClient4 介面遠端桌面服務，AdvancedSettings5 屬性
- AdvancedSettings5 屬性遠端桌面服務，IMsRdpClient5 介面
- IMsRdpClient5 介面遠端桌面服務，AdvancedSettings5 屬性
- AdvancedSettings5 屬性遠端桌面服務，IMsRdpClient6 介面
- IMsRdpClient6 介面遠端桌面服務，AdvancedSettings5 屬性
- AdvancedSettings5 屬性遠端桌面服務，IMsRdpClient7 介面
- IMsRdpClient7 介面遠端桌面服務，AdvancedSettings5 屬性
- AdvancedSettings5 屬性遠端桌面服務，IMsRdpClient8 介面
- IMsRdpClient8 介面遠端桌面服務，AdvancedSettings5 屬性
- AdvancedSettings5 屬性遠端桌面服務，IMsRdpClient9 介面
- IMsRdpClient9 介面遠端桌面服務，AdvancedSettings5 屬性
- AdvancedSettings5 屬性遠端桌面服務，IMsRdpClient10 介面
- IMsRdpClient10 介面遠端桌面服務，AdvancedSettings5 屬性
topic_type:
- apiref
api_name:
- IMsRdpClient4.AdvancedSettings5
- IMsRdpClient4.get_AdvancedSettings5
- IMsRdpClient5.AdvancedSettings5
- IMsRdpClient5.get_AdvancedSettings5
- IMsRdpClient6.AdvancedSettings5
- IMsRdpClient6.get_AdvancedSettings5
- IMsRdpClient7.AdvancedSettings5
- IMsRdpClient7.get_AdvancedSettings5
- IMsRdpClient8.AdvancedSettings5
- IMsRdpClient8.get_AdvancedSettings5
- IMsRdpClient9.AdvancedSettings5
- IMsRdpClient9.get_AdvancedSettings5
- IMsRdpClient10.AdvancedSettings5
- IMsRdpClient10.get_AdvancedSettings5
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ad96588b2109375aed23c1024ef925936cb3368
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509403"
---
# <a name="imsrdpclient4advancedsettings5-property"></a><span data-ttu-id="e5849-118">IMsRdpClient4：： AdvancedSettings5 屬性</span><span class="sxs-lookup"><span data-stu-id="e5849-118">IMsRdpClient4::AdvancedSettings5 property</span></span>

<span data-ttu-id="e5849-119">捕獲 [**IMsRdpClientAdvancedSettings4**](imsrdpclientadvancedsettings4.md) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="e5849-119">Retrieves a pointer to an [**IMsRdpClientAdvancedSettings4**](imsrdpclientadvancedsettings4.md) interface.</span></span>

<span data-ttu-id="e5849-120">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="e5849-120">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="e5849-121">語法</span><span class="sxs-lookup"><span data-stu-id="e5849-121">Syntax</span></span>


```C++
HRESULT get_AdvancedSettings5(
  [out] IMsRdpClientAdvancedSettings4 **ppAdvSettings
);
```



## <a name="property-value"></a><span data-ttu-id="e5849-122">屬性值</span><span class="sxs-lookup"><span data-stu-id="e5849-122">Property value</span></span>

<span data-ttu-id="e5849-123">[**IMsRdpClientAdvancedSettings4**](imsrdpclientadvancedsettings4.md)介面的指標。</span><span class="sxs-lookup"><span data-stu-id="e5849-123">A pointer to the [**IMsRdpClientAdvancedSettings4**](imsrdpclientadvancedsettings4.md) interface.</span></span> <span data-ttu-id="e5849-124">介面可以用來設定用戶端控制項的 advanced 設定。</span><span class="sxs-lookup"><span data-stu-id="e5849-124">The interface can be used to set advanced settings for the client control.</span></span>

## <a name="error-codes"></a><span data-ttu-id="e5849-125">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="e5849-125">Error codes</span></span>

<span data-ttu-id="e5849-126">如果方法成功，則會傳回 **S \_ OK** 。</span><span class="sxs-lookup"><span data-stu-id="e5849-126">If the method succeeds, **S\_OK** is returned.</span></span> <span data-ttu-id="e5849-127">任何其他 **HRESULT** 值都表示呼叫失敗。</span><span class="sxs-lookup"><span data-stu-id="e5849-127">Any other **HRESULT** value indicates that the call failed.</span></span>

## <a name="remarks"></a><span data-ttu-id="e5849-128">備註</span><span class="sxs-lookup"><span data-stu-id="e5849-128">Remarks</span></span>

<span data-ttu-id="e5849-129">連接控制項時，無法設定這個屬性。</span><span class="sxs-lookup"><span data-stu-id="e5849-129">This property cannot be set when the control is connected.</span></span>

<span data-ttu-id="e5849-130">如需遠端桌面網頁連線的詳細資訊，請參閱 [遠端桌面網頁連線的需求](requirements-for-remote-desktop-web-connection.md)。</span><span class="sxs-lookup"><span data-stu-id="e5849-130">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e5849-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="e5849-131">Requirements</span></span>



| <span data-ttu-id="e5849-132">需求</span><span class="sxs-lookup"><span data-stu-id="e5849-132">Requirement</span></span> | <span data-ttu-id="e5849-133">值</span><span class="sxs-lookup"><span data-stu-id="e5849-133">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e5849-134">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e5849-134">Minimum supported client</span></span><br/> | <span data-ttu-id="e5849-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e5849-135">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="e5849-136">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e5849-136">Minimum supported server</span></span><br/> | <span data-ttu-id="e5849-137">Windows Server 2008、Windows Server 2008 SP1</span><span class="sxs-lookup"><span data-stu-id="e5849-137">Windows Server 2008, Windows Server 2008 with SP1</span></span><br/>                           |
| <span data-ttu-id="e5849-138">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="e5849-138">Type library</span></span><br/>             | <dl> <span data-ttu-id="e5849-139"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e5849-139"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="e5849-140">DLL</span><span class="sxs-lookup"><span data-stu-id="e5849-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e5849-141"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e5849-141"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="e5849-142">IID</span><span class="sxs-lookup"><span data-stu-id="e5849-142">IID</span></span><br/>                      | <span data-ttu-id="e5849-143">IMsRdpClient4 定義為095E0738-D97D-488b-B9F6-DD0E8D66C0DE</span><span class="sxs-lookup"><span data-stu-id="e5849-143">IMsRdpClient4 is defined as 095E0738-D97D-488b-B9F6-DD0E8D66C0DE</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="e5849-144">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e5849-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e5849-145">**IMsRdpClient4**</span><span class="sxs-lookup"><span data-stu-id="e5849-145">**IMsRdpClient4**</span></span>](imsrdpclient4.md)
</dt> <dt>

[<span data-ttu-id="e5849-146">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="e5849-146">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="e5849-147">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="e5849-147">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="e5849-148">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="e5849-148">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="e5849-149">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="e5849-149">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="e5849-150">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="e5849-150">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="e5849-151">**IMsRdpClient10**</span><span class="sxs-lookup"><span data-stu-id="e5849-151">**IMsRdpClient10**</span></span>](imsrdpclient10.md)
</dt> </dl>

 

 





