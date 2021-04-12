---
title: IMsTscAdvancedSettings ContainerHandledFullScreen 屬性
description: 指定是否啟用容器處理的全螢幕模式。
ms.assetid: 67679323-4a74-4d91-abd0-607415295f3d
ms.tgt_platform: multiple
keywords:
- ContainerHandledFullScreen 屬性遠端桌面服務
- ContainerHandledFullScreen 屬性遠端桌面服務，IMsTscAdvancedSettings 介面
- IMsTscAdvancedSettings 介面遠端桌面服務，ContainerHandledFullScreen 屬性
- ContainerHandledFullScreen 屬性遠端桌面服務，IMsRdpClientAdvancedSettings 介面
- IMsRdpClientAdvancedSettings 介面遠端桌面服務，ContainerHandledFullScreen 屬性
- ContainerHandledFullScreen 屬性遠端桌面服務，IMsRdpClientAdvancedSettings2 介面
- IMsRdpClientAdvancedSettings2 介面遠端桌面服務，ContainerHandledFullScreen 屬性
- ContainerHandledFullScreen 屬性遠端桌面服務，IMsRdpClientAdvancedSettings3 介面
- IMsRdpClientAdvancedSettings3 介面遠端桌面服務，ContainerHandledFullScreen 屬性
- ContainerHandledFullScreen 屬性遠端桌面服務，IMsRdpClientAdvancedSettings4 介面
- IMsRdpClientAdvancedSettings4 介面遠端桌面服務，ContainerHandledFullScreen 屬性
- ContainerHandledFullScreen 屬性遠端桌面服務，IMsRdpClientAdvancedSettings5 介面
- IMsRdpClientAdvancedSettings5 介面遠端桌面服務，ContainerHandledFullScreen 屬性
- ContainerHandledFullScreen 屬性遠端桌面服務，IMsRdpClientAdvancedSettings6 介面
- IMsRdpClientAdvancedSettings6 介面遠端桌面服務，ContainerHandledFullScreen 屬性
- ContainerHandledFullScreen 屬性遠端桌面服務，IMsRdpClientAdvancedSettings7 介面
- IMsRdpClientAdvancedSettings7 介面遠端桌面服務，ContainerHandledFullScreen 屬性
- ContainerHandledFullScreen 屬性遠端桌面服務，IMsRdpClientAdvancedSettings8 介面
- IMsRdpClientAdvancedSettings8 介面遠端桌面服務，ContainerHandledFullScreen 屬性
topic_type:
- apiref
api_name:
- IMsTscAdvancedSettings.ContainerHandledFullScreen
- IMsTscAdvancedSettings.get_ContainerHandledFullScreen
- IMsTscAdvancedSettings.put_ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings.ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings.get_ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings.put_ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings2.ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings2.get_ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings2.put_ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings3.ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings3.get_ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings3.put_ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings4.ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings4.get_ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings4.put_ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings5.ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings5.get_ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings5.put_ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings6.ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings6.get_ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings6.put_ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings7.ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings7.get_ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings7.put_ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings8.ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings8.get_ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings8.put_ContainerHandledFullScreen
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4a7442ce16e2ff30ca2d9b3bd529d37382d1df41
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384889"
---
# <a name="imstscadvancedsettingscontainerhandledfullscreen-property"></a><span data-ttu-id="061cb-122">IMsTscAdvancedSettings：： ContainerHandledFullScreen 屬性</span><span class="sxs-lookup"><span data-stu-id="061cb-122">IMsTscAdvancedSettings::ContainerHandledFullScreen property</span></span>

<span data-ttu-id="061cb-123">指定是否啟用容器處理的全螢幕模式。</span><span class="sxs-lookup"><span data-stu-id="061cb-123">Specifies whether the container-handled full-screen mode is enabled.</span></span>

> [!Note]  
> <span data-ttu-id="061cb-124">當遠端桌面 ActiveX 控制項可以安全地進行腳本處理時， **ContainerHandledFullScreen** 屬性的值不會有任何作用，並且會在嘗試變更值時傳回 **S \_ FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="061cb-124">The value of the **ContainerHandledFullScreen** property has no effect when the Remote Desktop ActiveX control is safe for scripting, and returns **S\_FALSE** when an attempt is made to change the value.</span></span>

 

<span data-ttu-id="061cb-125">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="061cb-125">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="061cb-126">Syntax</span><span class="sxs-lookup"><span data-stu-id="061cb-126">Syntax</span></span>


```C++
HRESULT put_ContainerHandledFullScreen(
  [in]  BOOL ContainerHandledFullScreen
);

HRESULT get_ContainerHandledFullScreen(
  [out] BOOL *pContainerHandledFullScreen
);
```



## <a name="property-value"></a><span data-ttu-id="061cb-127">屬性值</span><span class="sxs-lookup"><span data-stu-id="061cb-127">Property value</span></span>

<span data-ttu-id="061cb-128">將此參數設定為 **TRUE** ，以啟用模式或其他值以停用模式。</span><span class="sxs-lookup"><span data-stu-id="061cb-128">Set this parameter to **TRUE** to enable the mode or another value to disable the mode.</span></span>

## <a name="error-codes"></a><span data-ttu-id="061cb-129">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="061cb-129">Error codes</span></span>

<span data-ttu-id="061cb-130">如果成功，則傳回 **S \_ OK** 。</span><span class="sxs-lookup"><span data-stu-id="061cb-130">Returns **S\_OK** if successful.</span></span> <span data-ttu-id="061cb-131">如果不支援，則傳回 **\_ FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="061cb-131">Returns **S\_FALSE** if not supported.</span></span>

## <a name="remarks"></a><span data-ttu-id="061cb-132">備註</span><span class="sxs-lookup"><span data-stu-id="061cb-132">Remarks</span></span>

<span data-ttu-id="061cb-133">當啟用此模式時，目前的容器會將開關處理成全螢幕模式。</span><span class="sxs-lookup"><span data-stu-id="061cb-133">When this mode is enabled, the current container processes the switch into and out of full-screen mode.</span></span> <span data-ttu-id="061cb-134">只有當目前的容器需要對全螢幕模式行為進行廣泛的控制時，才應該使用這個方法。</span><span class="sxs-lookup"><span data-stu-id="061cb-134">This method should be used only if the current container needs extensive control over full-screen mode behavior.</span></span> <span data-ttu-id="061cb-135">設定這個屬性時，控制項不會進入或離開全螢幕模式，以回應全螢幕模式快速鍵組合 (CTRL + ALT + BREAK) ;相反地，會呼叫 [**IMsTscAxEvents：： OnRequestGoFullScreen**](imstscaxevents-onrequestgofullscreen.md) 和 [**IMsTscAxEvents：： OnRequestLeaveFullScreen**](imstscaxevents-onrequestleavefullscreen.md) 事件。</span><span class="sxs-lookup"><span data-stu-id="061cb-135">When this property is set, the control does not enter or leave full-screen mode in response to the full-screen mode shortcut key combination (CTRL+ALT+BREAK); instead, the [**IMsTscAxEvents::OnRequestGoFullScreen**](imstscaxevents-onrequestgofullscreen.md) and [**IMsTscAxEvents::OnRequestLeaveFullScreen**](imstscaxevents-onrequestleavefullscreen.md) events are called.</span></span> <span data-ttu-id="061cb-136">如需這些事件的詳細資訊，請參閱 [**IMsTscAxEvents**](imstscaxevents-interface.md) 。</span><span class="sxs-lookup"><span data-stu-id="061cb-136">See [**IMsTscAxEvents**](imstscaxevents-interface.md) for more information about these events.</span></span>

<span data-ttu-id="061cb-137">大部分的容器應用程式都不需要使用容器處理的全螢幕模式。</span><span class="sxs-lookup"><span data-stu-id="061cb-137">Most container applications will not need to use container-handled full-screen mode.</span></span>

<span data-ttu-id="061cb-138">如需遠端桌面網頁連線的詳細資訊，請參閱 [遠端桌面網頁連線的需求](requirements-for-remote-desktop-web-connection.md)。</span><span class="sxs-lookup"><span data-stu-id="061cb-138">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="061cb-139">規格需求</span><span class="sxs-lookup"><span data-stu-id="061cb-139">Requirements</span></span>



| <span data-ttu-id="061cb-140">需求</span><span class="sxs-lookup"><span data-stu-id="061cb-140">Requirement</span></span> | <span data-ttu-id="061cb-141">值</span><span class="sxs-lookup"><span data-stu-id="061cb-141">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="061cb-142">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="061cb-142">Minimum supported client</span></span><br/> | <span data-ttu-id="061cb-143">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="061cb-143">Windows Vista</span></span><br/>                                                                  |
| <span data-ttu-id="061cb-144">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="061cb-144">Minimum supported server</span></span><br/> | <span data-ttu-id="061cb-145">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="061cb-145">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="061cb-146">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="061cb-146">Type library</span></span><br/>             | <dl> <span data-ttu-id="061cb-147"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="061cb-147"><dt>MsTscAx.dll</dt></span></span> </dl>    |
| <span data-ttu-id="061cb-148">DLL</span><span class="sxs-lookup"><span data-stu-id="061cb-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="061cb-149"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="061cb-149"><dt>MsTscAx.dll</dt></span></span> </dl>    |
| <span data-ttu-id="061cb-150">IID</span><span class="sxs-lookup"><span data-stu-id="061cb-150">IID</span></span><br/>                      | <span data-ttu-id="061cb-151">IID \_ IMsTscAdvancedSettings 定義為809945cc-4b3b-4a92-a6b0-dbf9b5f2ef2d</span><span class="sxs-lookup"><span data-stu-id="061cb-151">IID\_IMsTscAdvancedSettings is defined as 809945cc-4b3b-4a92-a6b0-dbf9b5f2ef2d</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="061cb-152">另請參閱</span><span class="sxs-lookup"><span data-stu-id="061cb-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="061cb-153">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="061cb-153">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="061cb-154">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="061cb-154">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="061cb-155">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="061cb-155">**IMsRdpClientAdvancedSettings3**</span></span>](imsrdpclientadvancedsettings3.md)
</dt> <dt>

[<span data-ttu-id="061cb-156">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="061cb-156">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="061cb-157">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="061cb-157">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="061cb-158">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="061cb-158">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="061cb-159">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="061cb-159">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="061cb-160">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="061cb-160">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="061cb-161">**IMsTscAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="061cb-161">**IMsTscAdvancedSettings**</span></span>](imstscadvancedsettings-interface.md)
</dt> </dl>

 

 





