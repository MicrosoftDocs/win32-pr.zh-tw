---
title: IMsRdpClientAdvancedSettings GrabFocusOnConnect 屬性
description: 指定用戶端控制項在連接時是否應該具有焦點。
ms.assetid: c67fc284-6e07-4749-84bf-70c0ae4d1b2b
ms.tgt_platform: multiple
keywords:
- GrabFocusOnConnect 屬性遠端桌面服務
- GrabFocusOnConnect 屬性遠端桌面服務，IMsRdpClientAdvancedSettings 介面
- IMsRdpClientAdvancedSettings 介面遠端桌面服務，GrabFocusOnConnect 屬性
- GrabFocusOnConnect 屬性遠端桌面服務，IMsRdpClientAdvancedSettings2 介面
- IMsRdpClientAdvancedSettings2 介面遠端桌面服務，GrabFocusOnConnect 屬性
- GrabFocusOnConnect 屬性遠端桌面服務，IMsRdpClientAdvancedSettings3 介面
- IMsRdpClientAdvancedSettings3 介面遠端桌面服務，GrabFocusOnConnect 屬性
- GrabFocusOnConnect 屬性遠端桌面服務，IMsRdpClientAdvancedSettings4 介面
- IMsRdpClientAdvancedSettings4 介面遠端桌面服務，GrabFocusOnConnect 屬性
- GrabFocusOnConnect 屬性遠端桌面服務，IMsRdpClientAdvancedSettings5 介面
- IMsRdpClientAdvancedSettings5 介面遠端桌面服務，GrabFocusOnConnect 屬性
- GrabFocusOnConnect 屬性遠端桌面服務，IMsRdpClientAdvancedSettings6 介面
- IMsRdpClientAdvancedSettings6 介面遠端桌面服務，GrabFocusOnConnect 屬性
- GrabFocusOnConnect 屬性遠端桌面服務，IMsRdpClientAdvancedSettings7 介面
- IMsRdpClientAdvancedSettings7 介面遠端桌面服務，GrabFocusOnConnect 屬性
- GrabFocusOnConnect 屬性遠端桌面服務，IMsRdpClientAdvancedSettings8 介面
- IMsRdpClientAdvancedSettings8 介面遠端桌面服務，GrabFocusOnConnect 屬性
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.GrabFocusOnConnect
- IMsRdpClientAdvancedSettings.get_GrabFocusOnConnect
- IMsRdpClientAdvancedSettings.put_GrabFocusOnConnect
- IMsRdpClientAdvancedSettings2.GrabFocusOnConnect
- IMsRdpClientAdvancedSettings2.get_GrabFocusOnConnect
- IMsRdpClientAdvancedSettings2.put_GrabFocusOnConnect
- IMsRdpClientAdvancedSettings3.GrabFocusOnConnect
- IMsRdpClientAdvancedSettings3.get_GrabFocusOnConnect
- IMsRdpClientAdvancedSettings3.put_GrabFocusOnConnect
- IMsRdpClientAdvancedSettings4.GrabFocusOnConnect
- IMsRdpClientAdvancedSettings4.get_GrabFocusOnConnect
- IMsRdpClientAdvancedSettings4.put_GrabFocusOnConnect
- IMsRdpClientAdvancedSettings5.GrabFocusOnConnect
- IMsRdpClientAdvancedSettings5.get_GrabFocusOnConnect
- IMsRdpClientAdvancedSettings5.put_GrabFocusOnConnect
- IMsRdpClientAdvancedSettings6.GrabFocusOnConnect
- IMsRdpClientAdvancedSettings6.get_GrabFocusOnConnect
- IMsRdpClientAdvancedSettings6.put_GrabFocusOnConnect
- IMsRdpClientAdvancedSettings7.GrabFocusOnConnect
- IMsRdpClientAdvancedSettings7.get_GrabFocusOnConnect
- IMsRdpClientAdvancedSettings7.put_GrabFocusOnConnect
- IMsRdpClientAdvancedSettings8.GrabFocusOnConnect
- IMsRdpClientAdvancedSettings8.get_GrabFocusOnConnect
- IMsRdpClientAdvancedSettings8.put_GrabFocusOnConnect
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e7fb04c00bd7aaaf4de1252d961206ffee0e6b9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106968379"
---
# <a name="imsrdpclientadvancedsettingsgrabfocusonconnect-property"></a><span data-ttu-id="6ab1a-120">IMsRdpClientAdvancedSettings：： GrabFocusOnConnect 屬性</span><span class="sxs-lookup"><span data-stu-id="6ab1a-120">IMsRdpClientAdvancedSettings::GrabFocusOnConnect property</span></span>

<span data-ttu-id="6ab1a-121">指定用戶端控制項在連接時是否應該具有焦點。</span><span class="sxs-lookup"><span data-stu-id="6ab1a-121">Specifies if the client control should have the focus while connecting.</span></span> <span data-ttu-id="6ab1a-122">控制項不會嘗試從在不同進程中執行的視窗抓取焦點。</span><span class="sxs-lookup"><span data-stu-id="6ab1a-122">The control will not attempt to grab focus from a window running in a different process.</span></span>

<span data-ttu-id="6ab1a-123">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="6ab1a-123">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="6ab1a-124">Syntax</span><span class="sxs-lookup"><span data-stu-id="6ab1a-124">Syntax</span></span>


```C++
HRESULT put_GrabFocusOnConnect(
  [in]  VARIANT_BOOL fGrabFocusOnConnect
);

HRESULT get_GrabFocusOnConnect(
  [out] VARIANT_BOOL pfGrabFocusOnConnect
);
```



## <a name="property-value"></a><span data-ttu-id="6ab1a-125">屬性值</span><span class="sxs-lookup"><span data-stu-id="6ab1a-125">Property value</span></span>

<span data-ttu-id="6ab1a-126">將此參數設定為 **VARIANT \_ FALSE** ，以停用此功能或 **variant \_ TRUE** 來啟用此功能。</span><span class="sxs-lookup"><span data-stu-id="6ab1a-126">Set this parameter to **VARIANT\_FALSE** to disable the feature or **VARIANT\_TRUE** to enable the feature.</span></span> <span data-ttu-id="6ab1a-127">將這個屬性設定為 **VARIANT \_ FALSE** ，可防止控制項在連接時抓取焦點。</span><span class="sxs-lookup"><span data-stu-id="6ab1a-127">Setting this property to **VARIANT\_FALSE** prevents the control from grabbing focus when connecting.</span></span>

## <a name="error-codes"></a><span data-ttu-id="6ab1a-128">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="6ab1a-128">Error codes</span></span>

<span data-ttu-id="6ab1a-129">如果成功，則傳回 **S \_ OK** 。</span><span class="sxs-lookup"><span data-stu-id="6ab1a-129">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="6ab1a-130">備註</span><span class="sxs-lookup"><span data-stu-id="6ab1a-130">Remarks</span></span>

<span data-ttu-id="6ab1a-131">如需遠端桌面網頁連線的詳細資訊，請參閱 [遠端桌面網頁連線的需求](requirements-for-remote-desktop-web-connection.md)。</span><span class="sxs-lookup"><span data-stu-id="6ab1a-131">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6ab1a-132">規格需求</span><span class="sxs-lookup"><span data-stu-id="6ab1a-132">Requirements</span></span>



| <span data-ttu-id="6ab1a-133">需求</span><span class="sxs-lookup"><span data-stu-id="6ab1a-133">Requirement</span></span> | <span data-ttu-id="6ab1a-134">值</span><span class="sxs-lookup"><span data-stu-id="6ab1a-134">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6ab1a-135">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6ab1a-135">Minimum supported client</span></span><br/> | <span data-ttu-id="6ab1a-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6ab1a-136">Windows Vista</span></span><br/>                                                                        |
| <span data-ttu-id="6ab1a-137">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6ab1a-137">Minimum supported server</span></span><br/> | <span data-ttu-id="6ab1a-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6ab1a-138">Windows Server 2008</span></span><br/>                                                                  |
| <span data-ttu-id="6ab1a-139">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="6ab1a-139">Type library</span></span><br/>             | <dl> <span data-ttu-id="6ab1a-140"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6ab1a-140"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="6ab1a-141">DLL</span><span class="sxs-lookup"><span data-stu-id="6ab1a-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6ab1a-142"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6ab1a-142"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="6ab1a-143">IID</span><span class="sxs-lookup"><span data-stu-id="6ab1a-143">IID</span></span><br/>                      | <span data-ttu-id="6ab1a-144">IID \_ IMsRdpClientAdvancedSettings 定義為3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span><span class="sxs-lookup"><span data-stu-id="6ab1a-144">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="6ab1a-145">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6ab1a-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6ab1a-146">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="6ab1a-146">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="6ab1a-147">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="6ab1a-147">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="6ab1a-148">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="6ab1a-148">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="6ab1a-149">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="6ab1a-149">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="6ab1a-150">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="6ab1a-150">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="6ab1a-151">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="6ab1a-151">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="6ab1a-152">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="6ab1a-152">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="6ab1a-153">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="6ab1a-153">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





