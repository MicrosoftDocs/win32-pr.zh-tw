---
title: IMsRdpClientNonScriptable NotifyRedirectDeviceChange 方法
description: 通知遠端桌面 ActiveX 控制項的裝置重新導向模組，表示系統上已發生裝置變更。 這個方法會 \_ 將 WM DEVICECHANGE 通知傳遞給控制項。
ms.assetid: 36323831-06e0-4e47-8a6c-06367119298f
ms.tgt_platform: multiple
keywords:
- NotifyRedirectDeviceChange 方法遠端桌面服務
- NotifyRedirectDeviceChange 方法遠端桌面服務，IMsRdpClientNonScriptable 介面
- IMsRdpClientNonScriptable 介面遠端桌面服務，NotifyRedirectDeviceChange 方法
- NotifyRedirectDeviceChange 方法遠端桌面服務，IMsRdpClientNonScriptable2 介面
- IMsRdpClientNonScriptable2 介面遠端桌面服務，NotifyRedirectDeviceChange 方法
- NotifyRedirectDeviceChange 方法遠端桌面服務，IMsRdpClientNonScriptable3 介面
- IMsRdpClientNonScriptable3 介面遠端桌面服務，NotifyRedirectDeviceChange 方法
- NotifyRedirectDeviceChange 方法遠端桌面服務，IMsRdpClientNonScriptable4 介面
- IMsRdpClientNonScriptable4 介面遠端桌面服務，NotifyRedirectDeviceChange 方法
- NotifyRedirectDeviceChange 方法遠端桌面服務，IMsRdpClientNonScriptable5 介面
- IMsRdpClientNonScriptable5 介面遠端桌面服務，NotifyRedirectDeviceChange 方法
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable.NotifyRedirectDeviceChange
- IMsRdpClientNonScriptable2.NotifyRedirectDeviceChange
- IMsRdpClientNonScriptable3.NotifyRedirectDeviceChange
- IMsRdpClientNonScriptable4.NotifyRedirectDeviceChange
- IMsRdpClientNonScriptable5.NotifyRedirectDeviceChange
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7357fcb5e31eeeb0de5791425b8d9fada4365ab8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103935039"
---
# <a name="imsrdpclientnonscriptablenotifyredirectdevicechange-method"></a><span data-ttu-id="aa6aa-115">IMsRdpClientNonScriptable：： NotifyRedirectDeviceChange 方法</span><span class="sxs-lookup"><span data-stu-id="aa6aa-115">IMsRdpClientNonScriptable::NotifyRedirectDeviceChange method</span></span>

<span data-ttu-id="aa6aa-116">通知遠端桌面 ActiveX 控制項的裝置重新導向模組，表示系統上已發生裝置變更。</span><span class="sxs-lookup"><span data-stu-id="aa6aa-116">Notifies the device redirection module of the Remote Desktop ActiveX control that a device change has occurred on the system.</span></span> <span data-ttu-id="aa6aa-117">這個方法會將 [**WM \_ DEVICECHANGE**](/windows/desktop/DevIO/wm-devicechange) 通知傳遞給控制項。</span><span class="sxs-lookup"><span data-stu-id="aa6aa-117">This method passes [**WM\_DEVICECHANGE**](/windows/desktop/DevIO/wm-devicechange) notifications to the control.</span></span>

## <a name="syntax"></a><span data-ttu-id="aa6aa-118">語法</span><span class="sxs-lookup"><span data-stu-id="aa6aa-118">Syntax</span></span>


```C++
HRESULT NotifyRedirectDeviceChange(
  [in] WPARAM wParam,
  [in] LPARAM lParam
);
```



## <a name="parameters"></a><span data-ttu-id="aa6aa-119">參數</span><span class="sxs-lookup"><span data-stu-id="aa6aa-119">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aa6aa-120">*wParam* \[在\]</span><span class="sxs-lookup"><span data-stu-id="aa6aa-120">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aa6aa-121">指定裝置事件。</span><span class="sxs-lookup"><span data-stu-id="aa6aa-121">Specifies the device event.</span></span> <span data-ttu-id="aa6aa-122">此參數可以是下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="aa6aa-122">This parameter can be one of the following values.</span></span>

<dt>

<span id="DBT_CONFIGCHANGECANCELED"></span><span id="dbt_configchangecanceled"></span>

<span data-ttu-id="aa6aa-123"><span id="DBT_CONFIGCHANGECANCELED"></span><span id="dbt_configchangecanceled"></span>**DBT \_ CONFIGCHANGECANCELED**</span><span class="sxs-lookup"><span data-stu-id="aa6aa-123"><span id="DBT_CONFIGCHANGECANCELED"></span><span id="dbt_configchangecanceled"></span>**DBT\_CONFIGCHANGECANCELED**</span></span>


</dt> <dd>

<span data-ttu-id="aa6aa-124">已取消變更目前設定 (dock 或取消停駐) 的要求。</span><span class="sxs-lookup"><span data-stu-id="aa6aa-124">A request to change the current configuration (dock or undock) has been canceled.</span></span>

</dd> <dt>

<span id="DBT_CONFIGCHANGED"></span><span id="dbt_configchanged"></span>

<span data-ttu-id="aa6aa-125"><span id="DBT_CONFIGCHANGED"></span><span id="dbt_configchanged"></span>**DBT \_ CONFIGCHANGED**</span><span class="sxs-lookup"><span data-stu-id="aa6aa-125"><span id="DBT_CONFIGCHANGED"></span><span id="dbt_configchanged"></span>**DBT\_CONFIGCHANGED**</span></span>


</dt> <dd>

<span data-ttu-id="aa6aa-126">目前的設定因 dock 或取消停駐而變更。</span><span class="sxs-lookup"><span data-stu-id="aa6aa-126">The current configuration has changed due to a dock or undock.</span></span>

</dd> <dt>

<span id="DBT_CUSTOMEVENT"></span><span id="dbt_customevent"></span>

<span data-ttu-id="aa6aa-127"><span id="DBT_CUSTOMEVENT"></span><span id="dbt_customevent"></span>**DBT \_ CUSTOMEVENT**</span><span class="sxs-lookup"><span data-stu-id="aa6aa-127"><span id="DBT_CUSTOMEVENT"></span><span id="dbt_customevent"></span>**DBT\_CUSTOMEVENT**</span></span>


</dt> <dd>

<span data-ttu-id="aa6aa-128">發生自訂事件。</span><span class="sxs-lookup"><span data-stu-id="aa6aa-128">A custom event has occurred.</span></span>

</dd> <dt>

<span id="DBT_DEVICEARRIVAL"></span><span id="dbt_devicearrival"></span>

<span data-ttu-id="aa6aa-129"><span id="DBT_DEVICEARRIVAL"></span><span id="dbt_devicearrival"></span>**DBT \_ DEVICEARRIVAL**</span><span class="sxs-lookup"><span data-stu-id="aa6aa-129"><span id="DBT_DEVICEARRIVAL"></span><span id="dbt_devicearrival"></span>**DBT\_DEVICEARRIVAL**</span></span>


</dt> <dd>

<span data-ttu-id="aa6aa-130">已插入裝置，而且現在已可供使用。</span><span class="sxs-lookup"><span data-stu-id="aa6aa-130">A device has been inserted and is now available.</span></span>

</dd> <dt>

<span id="DBT_DEVICEQUERYREMOVE"></span><span id="dbt_devicequeryremove"></span>

<span data-ttu-id="aa6aa-131"><span id="DBT_DEVICEQUERYREMOVE"></span><span id="dbt_devicequeryremove"></span>**DBT \_ DEVICEQUERYREMOVE**</span><span class="sxs-lookup"><span data-stu-id="aa6aa-131"><span id="DBT_DEVICEQUERYREMOVE"></span><span id="dbt_devicequeryremove"></span>**DBT\_DEVICEQUERYREMOVE**</span></span>


</dt> <dd>

<span data-ttu-id="aa6aa-132">要求許可權以移除裝置。</span><span class="sxs-lookup"><span data-stu-id="aa6aa-132">Permission is requested to remove a device.</span></span> <span data-ttu-id="aa6aa-133">任何應用程式都可以拒絕此要求，並取消移除。</span><span class="sxs-lookup"><span data-stu-id="aa6aa-133">Any application can deny this request and cancel the removal.</span></span>

</dd> <dt>

<span id="DBT_DEVICEQUERYREMOVEFAILED"></span><span id="dbt_devicequeryremovefailed"></span>

<span data-ttu-id="aa6aa-134"><span id="DBT_DEVICEQUERYREMOVEFAILED"></span><span id="dbt_devicequeryremovefailed"></span>**DBT \_ DEVICEQUERYREMOVEFAILED**</span><span class="sxs-lookup"><span data-stu-id="aa6aa-134"><span id="DBT_DEVICEQUERYREMOVEFAILED"></span><span id="dbt_devicequeryremovefailed"></span>**DBT\_DEVICEQUERYREMOVEFAILED**</span></span>


</dt> <dd>

<span data-ttu-id="aa6aa-135">移除裝置的要求已取消。</span><span class="sxs-lookup"><span data-stu-id="aa6aa-135">A request to remove a device has been canceled.</span></span>

</dd> <dt>

<span id="DBT_DEVICEREMOVECOMPLETE"></span><span id="dbt_deviceremovecomplete"></span>

<span data-ttu-id="aa6aa-136"><span id="DBT_DEVICEREMOVECOMPLETE"></span><span id="dbt_deviceremovecomplete"></span>**DBT \_ DEVICEREMOVECOMPLETE**</span><span class="sxs-lookup"><span data-stu-id="aa6aa-136"><span id="DBT_DEVICEREMOVECOMPLETE"></span><span id="dbt_deviceremovecomplete"></span>**DBT\_DEVICEREMOVECOMPLETE**</span></span>


</dt> <dd>

<span data-ttu-id="aa6aa-137">裝置已移除。</span><span class="sxs-lookup"><span data-stu-id="aa6aa-137">A device has been removed.</span></span>

</dd> <dt>

<span id="DBT_DEVICEREMOVEPENDING"></span><span id="dbt_deviceremovepending"></span>

<span data-ttu-id="aa6aa-138"><span id="DBT_DEVICEREMOVEPENDING"></span><span id="dbt_deviceremovepending"></span>**DBT \_ DEVICEREMOVEPENDING**</span><span class="sxs-lookup"><span data-stu-id="aa6aa-138"><span id="DBT_DEVICEREMOVEPENDING"></span><span id="dbt_deviceremovepending"></span>**DBT\_DEVICEREMOVEPENDING**</span></span>


</dt> <dd>

<span data-ttu-id="aa6aa-139">即將移除裝置。</span><span class="sxs-lookup"><span data-stu-id="aa6aa-139">A device is about to be removed.</span></span> <span data-ttu-id="aa6aa-140">無法拒絕移除。</span><span class="sxs-lookup"><span data-stu-id="aa6aa-140">The removal cannot be denied.</span></span>

</dd> <dt>

<span id="DBT_DEVICETYPESPECIFIC"></span><span id="dbt_devicetypespecific"></span>

<span data-ttu-id="aa6aa-141"><span id="DBT_DEVICETYPESPECIFIC"></span><span id="dbt_devicetypespecific"></span>**DBT \_ DEVICETYPESPECIFIC**</span><span class="sxs-lookup"><span data-stu-id="aa6aa-141"><span id="DBT_DEVICETYPESPECIFIC"></span><span id="dbt_devicetypespecific"></span>**DBT\_DEVICETYPESPECIFIC**</span></span>


</dt> <dd>

<span data-ttu-id="aa6aa-142">發生裝置特定事件。</span><span class="sxs-lookup"><span data-stu-id="aa6aa-142">A device-specific event has occurred.</span></span>

</dd> <dt>

<span id="DBT_DEVNODES_CHANGED"></span><span id="dbt_devnodes_changed"></span>

<span data-ttu-id="aa6aa-143"><span id="DBT_DEVNODES_CHANGED"></span><span id="dbt_devnodes_changed"></span>**DBT \_ DEVNODES \_ 已變更**</span><span class="sxs-lookup"><span data-stu-id="aa6aa-143"><span id="DBT_DEVNODES_CHANGED"></span><span id="dbt_devnodes_changed"></span>**DBT\_DEVNODES\_CHANGED**</span></span>


</dt> <dd>

<span data-ttu-id="aa6aa-144">已在系統中新增或移除裝置。</span><span class="sxs-lookup"><span data-stu-id="aa6aa-144">A device has been added to or removed from the system.</span></span>

</dd> <dt>

<span id="DBT_QUERYCHANGECONFIG"></span><span id="dbt_querychangeconfig"></span>

<span data-ttu-id="aa6aa-145"><span id="DBT_QUERYCHANGECONFIG"></span><span id="dbt_querychangeconfig"></span>**DBT \_ QUERYCHANGECONFIG**</span><span class="sxs-lookup"><span data-stu-id="aa6aa-145"><span id="DBT_QUERYCHANGECONFIG"></span><span id="dbt_querychangeconfig"></span>**DBT\_QUERYCHANGECONFIG**</span></span>


</dt> <dd>

<span data-ttu-id="aa6aa-146">已要求許可權來變更目前的設定 (dock 或移除) 。</span><span class="sxs-lookup"><span data-stu-id="aa6aa-146">Permission is requested to change the current configuration (dock or undock).</span></span>

</dd> <dt>

<span id="DBT_USERDEFINED"></span><span id="dbt_userdefined"></span>

<span data-ttu-id="aa6aa-147"><span id="DBT_USERDEFINED"></span><span id="dbt_userdefined"></span>**DBT 的 \_ 使用者**</span><span class="sxs-lookup"><span data-stu-id="aa6aa-147"><span id="DBT_USERDEFINED"></span><span id="dbt_userdefined"></span>**DBT\_USERDEFINED**</span></span>


</dt> <dd>

<span data-ttu-id="aa6aa-148">此訊息的意義是使用者定義的。</span><span class="sxs-lookup"><span data-stu-id="aa6aa-148">The meaning of this message is user-defined.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="aa6aa-149">*lParam* \[在\]</span><span class="sxs-lookup"><span data-stu-id="aa6aa-149">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aa6aa-150">包含事件特定資料之結構的指標。</span><span class="sxs-lookup"><span data-stu-id="aa6aa-150">Pointer to a structure that contains event-specific data.</span></span> <span data-ttu-id="aa6aa-151">其格式取決於 *wParam* 參數的值。</span><span class="sxs-lookup"><span data-stu-id="aa6aa-151">Its format depends on the value of the *wParam* parameter.</span></span> <span data-ttu-id="aa6aa-152">如需詳細資訊，請參閱每個事件的檔。</span><span class="sxs-lookup"><span data-stu-id="aa6aa-152">For more information, refer to the documentation for each event.</span></span> <span data-ttu-id="aa6aa-153">如需詳細資訊，請參閱 [裝置事件種類](/windows/desktop/DevIO/device-event-types)。</span><span class="sxs-lookup"><span data-stu-id="aa6aa-153">For more information, see [Device Event Types](/windows/desktop/DevIO/device-event-types).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aa6aa-154">傳回值</span><span class="sxs-lookup"><span data-stu-id="aa6aa-154">Return value</span></span>

<span data-ttu-id="aa6aa-155">如果成功，則傳回 **S \_ OK** 。</span><span class="sxs-lookup"><span data-stu-id="aa6aa-155">Return **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="aa6aa-156">備註</span><span class="sxs-lookup"><span data-stu-id="aa6aa-156">Remarks</span></span>

<span data-ttu-id="aa6aa-157">允許動態新增或移除裝置的容器應用程式，應該在其最上層視窗中處理 [**WM \_ DEVICECHANGE**](/windows/desktop/DevIO/wm-devicechange) 訊息，並使用 **NotifyRedirectDeviceChange** 方法將訊息轉送至控制項。</span><span class="sxs-lookup"><span data-stu-id="aa6aa-157">A container application that allows dynamic addition or removal of devices should process the [**WM\_DEVICECHANGE**](/windows/desktop/DevIO/wm-devicechange) message in its top level window and forward the message to the control using the **NotifyRedirectDeviceChange** method.</span></span> <span data-ttu-id="aa6aa-158">動態裝置變更的範例是當系統正在執行時，新增或移除重新導向的磁片磁碟機。</span><span class="sxs-lookup"><span data-stu-id="aa6aa-158">An example of a dynamic device change is when a redirected disk drive is added or removed while the system is running.</span></span>

<span data-ttu-id="aa6aa-159">如需遠端桌面網頁連線的詳細資訊，請參閱 [遠端桌面網頁連線的需求](requirements-for-remote-desktop-web-connection.md)。</span><span class="sxs-lookup"><span data-stu-id="aa6aa-159">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="aa6aa-160">規格需求</span><span class="sxs-lookup"><span data-stu-id="aa6aa-160">Requirements</span></span>



| <span data-ttu-id="aa6aa-161">需求</span><span class="sxs-lookup"><span data-stu-id="aa6aa-161">Requirement</span></span> | <span data-ttu-id="aa6aa-162">值</span><span class="sxs-lookup"><span data-stu-id="aa6aa-162">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="aa6aa-163">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="aa6aa-163">Minimum supported client</span></span><br/> | <span data-ttu-id="aa6aa-164">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="aa6aa-164">Windows Vista</span></span><br/>                                                                     |
| <span data-ttu-id="aa6aa-165">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="aa6aa-165">Minimum supported server</span></span><br/> | <span data-ttu-id="aa6aa-166">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="aa6aa-166">Windows Server 2008</span></span><br/>                                                               |
| <span data-ttu-id="aa6aa-167">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="aa6aa-167">Type library</span></span><br/>             | <dl> <span data-ttu-id="aa6aa-168"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="aa6aa-168"><dt>MsTscAx.dll</dt></span></span> </dl>       |
| <span data-ttu-id="aa6aa-169">DLL</span><span class="sxs-lookup"><span data-stu-id="aa6aa-169">DLL</span></span><br/>                      | <dl> <span data-ttu-id="aa6aa-170"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="aa6aa-170"><dt>MsTscAx.dll</dt></span></span> </dl>       |
| <span data-ttu-id="aa6aa-171">IID</span><span class="sxs-lookup"><span data-stu-id="aa6aa-171">IID</span></span><br/>                      | <span data-ttu-id="aa6aa-172">IID \_ IMsRdpClientNonScriptable 定義為2f079c4c-87b2-4afd-97ab-20cdb43038ae</span><span class="sxs-lookup"><span data-stu-id="aa6aa-172">IID\_IMsRdpClientNonScriptable is defined as 2f079c4c-87b2-4afd-97ab-20cdb43038ae</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="aa6aa-173">另請參閱</span><span class="sxs-lookup"><span data-stu-id="aa6aa-173">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aa6aa-174">**IMsRdpClientNonScriptable2**</span><span class="sxs-lookup"><span data-stu-id="aa6aa-174">**IMsRdpClientNonScriptable2**</span></span>](imsrdpclientnonscriptable2.md)
</dt> <dt>

[<span data-ttu-id="aa6aa-175">**IMsRdpClientNonScriptable3**</span><span class="sxs-lookup"><span data-stu-id="aa6aa-175">**IMsRdpClientNonScriptable3**</span></span>](imsrdpclientnonscriptable3.md)
</dt> <dt>

[<span data-ttu-id="aa6aa-176">**IMsRdpClientNonScriptable4**</span><span class="sxs-lookup"><span data-stu-id="aa6aa-176">**IMsRdpClientNonScriptable4**</span></span>](imsrdpclientnonscriptable4.md)
</dt> <dt>

[<span data-ttu-id="aa6aa-177">**IMsRdpClientNonScriptable5**</span><span class="sxs-lookup"><span data-stu-id="aa6aa-177">**IMsRdpClientNonScriptable5**</span></span>](imsrdpclientnonscriptable5.md)
</dt> <dt>

[<span data-ttu-id="aa6aa-178">**IMsRdpClientNonScriptable**</span><span class="sxs-lookup"><span data-stu-id="aa6aa-178">**IMsRdpClientNonScriptable**</span></span>](imsrdpclientnonscriptable-interface.md)
</dt> </dl>

 

