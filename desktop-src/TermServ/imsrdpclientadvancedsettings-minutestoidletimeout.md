---
title: IMsRdpClientAdvancedSettings MinutesToIdleTimeout 屬性
description: 指定用戶端在沒有使用者輸入的情況下，應維持連線的最大時間長度（以分鐘為單位）。 如果經過指定的時間，控制項就會呼叫 IMsTscAxEvents OnIdleTimeoutNotification 方法。
ms.assetid: 709238ea-45f8-4bdc-9bbe-019d54ca27bf
ms.tgt_platform: multiple
keywords:
- MinutesToIdleTimeout 屬性遠端桌面服務
- MinutesToIdleTimeout 屬性遠端桌面服務，IMsRdpClientAdvancedSettings 介面
- IMsRdpClientAdvancedSettings 介面遠端桌面服務，MinutesToIdleTimeout 屬性
- MinutesToIdleTimeout 屬性遠端桌面服務，IMsRdpClientAdvancedSettings2 介面
- IMsRdpClientAdvancedSettings2 介面遠端桌面服務，MinutesToIdleTimeout 屬性
- MinutesToIdleTimeout 屬性遠端桌面服務，IMsRdpClientAdvancedSettings3 介面
- IMsRdpClientAdvancedSettings3 介面遠端桌面服務，MinutesToIdleTimeout 屬性
- MinutesToIdleTimeout 屬性遠端桌面服務，IMsRdpClientAdvancedSettings4 介面
- IMsRdpClientAdvancedSettings4 介面遠端桌面服務，MinutesToIdleTimeout 屬性
- MinutesToIdleTimeout 屬性遠端桌面服務，IMsRdpClientAdvancedSettings5 介面
- IMsRdpClientAdvancedSettings5 介面遠端桌面服務，MinutesToIdleTimeout 屬性
- MinutesToIdleTimeout 屬性遠端桌面服務，IMsRdpClientAdvancedSettings6 介面
- IMsRdpClientAdvancedSettings6 介面遠端桌面服務，MinutesToIdleTimeout 屬性
- MinutesToIdleTimeout 屬性遠端桌面服務，IMsRdpClientAdvancedSettings7 介面
- IMsRdpClientAdvancedSettings7 介面遠端桌面服務，MinutesToIdleTimeout 屬性
- MinutesToIdleTimeout 屬性遠端桌面服務，IMsRdpClientAdvancedSettings8 介面
- IMsRdpClientAdvancedSettings8 介面遠端桌面服務，MinutesToIdleTimeout 屬性
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.MinutesToIdleTimeout
- IMsRdpClientAdvancedSettings.get_MinutesToIdleTimeout
- IMsRdpClientAdvancedSettings.put_MinutesToIdleTimeout
- IMsRdpClientAdvancedSettings2.MinutesToIdleTimeout
- IMsRdpClientAdvancedSettings2.get_MinutesToIdleTimeout
- IMsRdpClientAdvancedSettings2.put_MinutesToIdleTimeout
- IMsRdpClientAdvancedSettings3.MinutesToIdleTimeout
- IMsRdpClientAdvancedSettings3.get_MinutesToIdleTimeout
- IMsRdpClientAdvancedSettings3.put_MinutesToIdleTimeout
- IMsRdpClientAdvancedSettings4.MinutesToIdleTimeout
- IMsRdpClientAdvancedSettings4.get_MinutesToIdleTimeout
- IMsRdpClientAdvancedSettings4.put_MinutesToIdleTimeout
- IMsRdpClientAdvancedSettings5.MinutesToIdleTimeout
- IMsRdpClientAdvancedSettings5.get_MinutesToIdleTimeout
- IMsRdpClientAdvancedSettings5.put_MinutesToIdleTimeout
- IMsRdpClientAdvancedSettings6.MinutesToIdleTimeout
- IMsRdpClientAdvancedSettings6.get_MinutesToIdleTimeout
- IMsRdpClientAdvancedSettings6.put_MinutesToIdleTimeout
- IMsRdpClientAdvancedSettings7.MinutesToIdleTimeout
- IMsRdpClientAdvancedSettings7.get_MinutesToIdleTimeout
- IMsRdpClientAdvancedSettings7.put_MinutesToIdleTimeout
- IMsRdpClientAdvancedSettings8.MinutesToIdleTimeout
- IMsRdpClientAdvancedSettings8.get_MinutesToIdleTimeout
- IMsRdpClientAdvancedSettings8.put_MinutesToIdleTimeout
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8b5e42258ed670ac0323723cafe7b2792f8c5bd6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106965893"
---
# <a name="imsrdpclientadvancedsettingsminutestoidletimeout-property"></a><span data-ttu-id="c47e7-121">IMsRdpClientAdvancedSettings：： MinutesToIdleTimeout 屬性</span><span class="sxs-lookup"><span data-stu-id="c47e7-121">IMsRdpClientAdvancedSettings::MinutesToIdleTimeout property</span></span>

<span data-ttu-id="c47e7-122">指定用戶端在沒有使用者輸入的情況下，應維持連線的最大時間長度（以分鐘為單位）。</span><span class="sxs-lookup"><span data-stu-id="c47e7-122">Specifies the maximum length of time, in minutes, that the client should remain connected without user input.</span></span> <span data-ttu-id="c47e7-123">如果經過指定的時間，控制項會呼叫 [**IMsTscAxEvents：： OnIdleTimeoutNotification**](imstscaxevents-onidletimeoutnotification.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="c47e7-123">If the specified time elapses, the control calls the [**IMsTscAxEvents::OnIdleTimeoutNotification**](imstscaxevents-onidletimeoutnotification.md) method.</span></span>

<span data-ttu-id="c47e7-124">在需要中斷閒置會話連線的情況下，您可以使用此屬性。例如，在 kiosk 環境中。</span><span class="sxs-lookup"><span data-stu-id="c47e7-124">You can use this property in a situation where you need to disconnect an idle session; for example, in a kiosk environment.</span></span>

<span data-ttu-id="c47e7-125">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="c47e7-125">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="c47e7-126">Syntax</span><span class="sxs-lookup"><span data-stu-id="c47e7-126">Syntax</span></span>


```C++
HRESULT put_MinutesToIdleTimeout(
  [in]  LONG minutesToIdleTimeout
);

HRESULT get_MinutesToIdleTimeout(
  [out] LONG *pminutesToIdleTimeout
);
```



## <a name="property-value"></a><span data-ttu-id="c47e7-127">屬性值</span><span class="sxs-lookup"><span data-stu-id="c47e7-127">Property value</span></span>

<span data-ttu-id="c47e7-128">新的時間（以分鐘為單位）。</span><span class="sxs-lookup"><span data-stu-id="c47e7-128">The new time, in minutes.</span></span> <span data-ttu-id="c47e7-129">預設值為零，它會停用此功能。</span><span class="sxs-lookup"><span data-stu-id="c47e7-129">The default value is zero, which disables the feature.</span></span> <span data-ttu-id="c47e7-130">最大值為240，代表4小時。</span><span class="sxs-lookup"><span data-stu-id="c47e7-130">The maximum value is 240, which represents 4 hours.</span></span>

## <a name="error-codes"></a><span data-ttu-id="c47e7-131">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="c47e7-131">Error codes</span></span>

<span data-ttu-id="c47e7-132">如果成功，則傳回 **S \_ OK** 。</span><span class="sxs-lookup"><span data-stu-id="c47e7-132">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="c47e7-133">備註</span><span class="sxs-lookup"><span data-stu-id="c47e7-133">Remarks</span></span>

<span data-ttu-id="c47e7-134">如需遠端桌面網頁連線的詳細資訊，請參閱 [遠端桌面網頁連線的需求](requirements-for-remote-desktop-web-connection.md)。</span><span class="sxs-lookup"><span data-stu-id="c47e7-134">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c47e7-135">規格需求</span><span class="sxs-lookup"><span data-stu-id="c47e7-135">Requirements</span></span>



| <span data-ttu-id="c47e7-136">需求</span><span class="sxs-lookup"><span data-stu-id="c47e7-136">Requirement</span></span> | <span data-ttu-id="c47e7-137">值</span><span class="sxs-lookup"><span data-stu-id="c47e7-137">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c47e7-138">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c47e7-138">Minimum supported client</span></span><br/> | <span data-ttu-id="c47e7-139">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c47e7-139">Windows Vista</span></span><br/>                                                                        |
| <span data-ttu-id="c47e7-140">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c47e7-140">Minimum supported server</span></span><br/> | <span data-ttu-id="c47e7-141">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c47e7-141">Windows Server 2008</span></span><br/>                                                                  |
| <span data-ttu-id="c47e7-142">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="c47e7-142">Type library</span></span><br/>             | <dl> <span data-ttu-id="c47e7-143"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c47e7-143"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="c47e7-144">DLL</span><span class="sxs-lookup"><span data-stu-id="c47e7-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c47e7-145"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c47e7-145"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="c47e7-146">IID</span><span class="sxs-lookup"><span data-stu-id="c47e7-146">IID</span></span><br/>                      | <span data-ttu-id="c47e7-147">IID \_ IMsRdpClientAdvancedSettings 定義為3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span><span class="sxs-lookup"><span data-stu-id="c47e7-147">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c47e7-148">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c47e7-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c47e7-149">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="c47e7-149">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="c47e7-150">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="c47e7-150">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="c47e7-151">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="c47e7-151">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="c47e7-152">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="c47e7-152">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="c47e7-153">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="c47e7-153">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="c47e7-154">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="c47e7-154">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="c47e7-155">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="c47e7-155">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="c47e7-156">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="c47e7-156">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





