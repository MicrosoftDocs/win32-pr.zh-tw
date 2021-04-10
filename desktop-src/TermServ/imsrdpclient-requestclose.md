---
title: IMsRdpClient RequestClose 方法
description: 要求遠端桌面 ActiveX 控制項正常關機。
ms.assetid: 0b930a00-f134-4da2-a752-8fd131a22043
ms.tgt_platform: multiple
keywords:
- RequestClose 方法遠端桌面服務
- RequestClose 方法遠端桌面服務，IMsRdpClient 介面
- IMsRdpClient 介面遠端桌面服務，RequestClose 方法
- RequestClose 方法遠端桌面服務，IMsRdpClient2 介面
- IMsRdpClient2 介面遠端桌面服務，RequestClose 方法
- RequestClose 方法遠端桌面服務，IMsRdpClient3 介面
- IMsRdpClient3 介面遠端桌面服務，RequestClose 方法
- RequestClose 方法遠端桌面服務，IMsRdpClient4 介面
- IMsRdpClient4 介面遠端桌面服務，RequestClose 方法
- RequestClose 方法遠端桌面服務，IMsRdpClient5 介面
- IMsRdpClient5 介面遠端桌面服務，RequestClose 方法
- RequestClose 方法遠端桌面服務，IMsRdpClient6 介面
- IMsRdpClient6 介面遠端桌面服務，RequestClose 方法
- RequestClose 方法遠端桌面服務，IMsRdpClient7 介面
- IMsRdpClient7 介面遠端桌面服務，RequestClose 方法
- RequestClose 方法遠端桌面服務，IMsRdpClient8 介面
- IMsRdpClient8 介面遠端桌面服務，RequestClose 方法
- RequestClose 方法遠端桌面服務，IMsRdpClient9 介面
- IMsRdpClient9 介面遠端桌面服務，RequestClose 方法
- RequestClose 方法遠端桌面服務，IMsRdpClient10 介面
- IMsRdpClient10 介面遠端桌面服務，RequestClose 方法
topic_type:
- apiref
api_name:
- IMsRdpClient.RequestClose
- IMsRdpClient2.RequestClose
- IMsRdpClient3.RequestClose
- IMsRdpClient4.RequestClose
- IMsRdpClient5.RequestClose
- IMsRdpClient6.RequestClose
- IMsRdpClient7.RequestClose
- IMsRdpClient8.RequestClose
- IMsRdpClient9.RequestClose
- IMsRdpClient10.RequestClose
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1679b08680b962cdbff57e9bbbd1c392607d8709
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685676"
---
# <a name="imsrdpclientrequestclose-method"></a><span data-ttu-id="23e0a-124">IMsRdpClient：： RequestClose 方法</span><span class="sxs-lookup"><span data-stu-id="23e0a-124">IMsRdpClient::RequestClose method</span></span>

<span data-ttu-id="23e0a-125">要求遠端桌面 ActiveX 控制項正常關機。</span><span class="sxs-lookup"><span data-stu-id="23e0a-125">Requests a graceful shutdown of the Remote Desktop ActiveX control.</span></span> <span data-ttu-id="23e0a-126">正常關機可以包括結束使用者的遠端桌面服務會話，但不會將遠端桌面工作階段主機 (RD 工作階段主機) 伺服器。</span><span class="sxs-lookup"><span data-stu-id="23e0a-126">A graceful shutdown can include ending the user's Remote Desktop Services session but it does not shut down the Remote Desktop Session Host (RD Session Host) server.</span></span>

## <a name="syntax"></a><span data-ttu-id="23e0a-127">語法</span><span class="sxs-lookup"><span data-stu-id="23e0a-127">Syntax</span></span>


```C++
HRESULT RequestClose(
  [out] ControlCloseStatus *pCloseStatus
);
```



## <a name="parameters"></a><span data-ttu-id="23e0a-128">參數</span><span class="sxs-lookup"><span data-stu-id="23e0a-128">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="23e0a-129">*pCloseStatus* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="23e0a-129">*pCloseStatus* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="23e0a-130">[**ControlCloseStatus**](controlclosestatus.md)列舉中的值，指出應用程式是否可以立即關閉控制項。</span><span class="sxs-lookup"><span data-stu-id="23e0a-130">Value from the [**ControlCloseStatus**](controlclosestatus.md) enumeration that indicates whether the application can close the control immediately.</span></span> <span data-ttu-id="23e0a-131">以下是可能值的清單。</span><span class="sxs-lookup"><span data-stu-id="23e0a-131">Following is a list of possible values.</span></span>

<dt>

<span id="controlCloseCanProceed"></span><span id="controlclosecanproceed"></span><span id="CONTROLCLOSECANPROCEED"></span>

<span data-ttu-id="23e0a-132"><span id="controlCloseCanProceed"></span><span id="controlclosecanproceed"></span><span id="CONTROLCLOSECANPROCEED"></span>**controlCloseCanProceed** (0x0000) </span><span class="sxs-lookup"><span data-stu-id="23e0a-132"><span id="controlCloseCanProceed"></span><span id="controlclosecanproceed"></span><span id="CONTROLCLOSECANPROCEED"></span>**controlCloseCanProceed** (0x0000)</span></span>


</dt> <dd>

<span data-ttu-id="23e0a-133">容器應用程式可以繼續立即關閉控制項。</span><span class="sxs-lookup"><span data-stu-id="23e0a-133">The container application can proceed to close the control immediately.</span></span> <span data-ttu-id="23e0a-134">這個值也可以表示連接已經結束。</span><span class="sxs-lookup"><span data-stu-id="23e0a-134">This value can also indicate that the connection has already terminated.</span></span>

</dd> <dt>

<span id="controlCloseWaitForEvents"></span><span id="controlclosewaitforevents"></span><span id="CONTROLCLOSEWAITFOREVENTS"></span>

<span data-ttu-id="23e0a-135"><span id="controlCloseWaitForEvents"></span><span id="controlclosewaitforevents"></span><span id="CONTROLCLOSEWAITFOREVENTS"></span>**controlCloseWaitForEvents** (0x0001) </span><span class="sxs-lookup"><span data-stu-id="23e0a-135"><span id="controlCloseWaitForEvents"></span><span id="controlclosewaitforevents"></span><span id="CONTROLCLOSEWAITFOREVENTS"></span>**controlCloseWaitForEvents** (0x0001)</span></span>


</dt> <dd>

<span data-ttu-id="23e0a-136">容器應用程式不應立即關閉控制項;應用程式應該等候下列備註區段中所述的其中一個事件在關閉之前發生。</span><span class="sxs-lookup"><span data-stu-id="23e0a-136">The container application should not close the control immediately; the application should wait for one of the events described in the following Remarks section to occur before closing.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="23e0a-137">傳回值</span><span class="sxs-lookup"><span data-stu-id="23e0a-137">Return value</span></span>

<span data-ttu-id="23e0a-138">如果成功，則傳回 **S \_ OK** 。</span><span class="sxs-lookup"><span data-stu-id="23e0a-138">Return **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="23e0a-139">備註</span><span class="sxs-lookup"><span data-stu-id="23e0a-139">Remarks</span></span>

<span data-ttu-id="23e0a-140">如果 *pCloseStatus* 參數等於 **controlCloseWaitForEvents**，應用程式應該在應用程式關閉控制項之前，等候下列其中一個事件發生：</span><span class="sxs-lookup"><span data-stu-id="23e0a-140">If the *pCloseStatus* parameter is equal to **controlCloseWaitForEvents**, the application should wait for one of the following events to occur before the application closes the control:</span></span>

-   <span data-ttu-id="23e0a-141">[**IMsTscAxEvents：： OnDisconnected**](imstscaxevents-ondisconnected.md)。</span><span class="sxs-lookup"><span data-stu-id="23e0a-141">[**IMsTscAxEvents::OnDisconnected**](imstscaxevents-ondisconnected.md).</span></span> <span data-ttu-id="23e0a-142">如果使用者未登入遠端桌面服務的會話，則應用程式可以呼叫 [**DestroyWindow**](/windows/desktop/api/winuser/nf-winuser-destroywindow) 函式來摧毀所有視窗，然後關閉控制項。</span><span class="sxs-lookup"><span data-stu-id="23e0a-142">If the user is not logged on to the Remote Desktop Services session, the application can call the [**DestroyWindow**](/windows/desktop/api/winuser/nf-winuser-destroywindow) function to destroy all windows and then close the control.</span></span>
-   <span data-ttu-id="23e0a-143">[**IMsTscAxEvents：： OnConfirmClose**](imstscaxevents-onconfirmclose.md)。</span><span class="sxs-lookup"><span data-stu-id="23e0a-143">[**IMsTscAxEvents::OnConfirmClose**](imstscaxevents-onconfirmclose.md).</span></span> <span data-ttu-id="23e0a-144">如果使用者登入遠端桌面服務會話，控制項就會引發 **OnConfirmClose** 事件。</span><span class="sxs-lookup"><span data-stu-id="23e0a-144">If the user is logged on to the Remote Desktop Services session, the control fires an **OnConfirmClose** event.</span></span> <span data-ttu-id="23e0a-145">此事件可讓應用程式提示使用者是否要關閉連接。</span><span class="sxs-lookup"><span data-stu-id="23e0a-145">This event allows the application to prompt the user about whether to close the connection.</span></span> <span data-ttu-id="23e0a-146">如果使用者對提示回復 [是]，容器應用程式可以呼叫 [**DestroyWindow**](/windows/desktop/api/winuser/nf-winuser-destroywindow) 來終結所有視窗，然後關閉控制項。</span><span class="sxs-lookup"><span data-stu-id="23e0a-146">If the user replies yes to the prompt, the container application can call [**DestroyWindow**](/windows/desktop/api/winuser/nf-winuser-destroywindow) to destroy all windows, and close the control.</span></span>

<span data-ttu-id="23e0a-147">**RequestClose** 可讓容器應用程式提示使用者是否要關閉連接。</span><span class="sxs-lookup"><span data-stu-id="23e0a-147">**RequestClose** allows a container application to prompt the user about whether to close a connection.</span></span> <span data-ttu-id="23e0a-148">如需詳細資訊，請參閱 [**IMsTscAxEvents：： OnConfirmClose**](imstscaxevents-onconfirmclose.md)。</span><span class="sxs-lookup"><span data-stu-id="23e0a-148">For more information, see [**IMsTscAxEvents::OnConfirmClose**](imstscaxevents-onconfirmclose.md).</span></span>

<span data-ttu-id="23e0a-149">如需遠端桌面網頁連線的詳細資訊，請參閱 [遠端桌面網頁連線的需求](requirements-for-remote-desktop-web-connection.md)。</span><span class="sxs-lookup"><span data-stu-id="23e0a-149">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="23e0a-150">規格需求</span><span class="sxs-lookup"><span data-stu-id="23e0a-150">Requirements</span></span>



| <span data-ttu-id="23e0a-151">需求</span><span class="sxs-lookup"><span data-stu-id="23e0a-151">Requirement</span></span> | <span data-ttu-id="23e0a-152">值</span><span class="sxs-lookup"><span data-stu-id="23e0a-152">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="23e0a-153">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="23e0a-153">Minimum supported client</span></span><br/> | <span data-ttu-id="23e0a-154">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="23e0a-154">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="23e0a-155">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="23e0a-155">Minimum supported server</span></span><br/> | <span data-ttu-id="23e0a-156">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="23e0a-156">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="23e0a-157">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="23e0a-157">Type library</span></span><br/>             | <dl> <span data-ttu-id="23e0a-158"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="23e0a-158"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="23e0a-159">DLL</span><span class="sxs-lookup"><span data-stu-id="23e0a-159">DLL</span></span><br/>                      | <dl> <span data-ttu-id="23e0a-160"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="23e0a-160"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="23e0a-161">IID</span><span class="sxs-lookup"><span data-stu-id="23e0a-161">IID</span></span><br/>                      | <span data-ttu-id="23e0a-162">IID \_ IMsRdpClient 定義為92b4a539-7115-4b7c-a5a9-e5d9efc2780a</span><span class="sxs-lookup"><span data-stu-id="23e0a-162">IID\_IMsRdpClient is defined as 92b4a539-7115-4b7c-a5a9-e5d9efc2780a</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="23e0a-163">另請參閱</span><span class="sxs-lookup"><span data-stu-id="23e0a-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="23e0a-164">**IMsRdpClient**</span><span class="sxs-lookup"><span data-stu-id="23e0a-164">**IMsRdpClient**</span></span>](imsrdpclient-interface.md)
</dt> <dt>

[<span data-ttu-id="23e0a-165">**IMsRdpClient2**</span><span class="sxs-lookup"><span data-stu-id="23e0a-165">**IMsRdpClient2**</span></span>](imsrdpclient2.md)
</dt> <dt>

[<span data-ttu-id="23e0a-166">**IMsRdpClient3**</span><span class="sxs-lookup"><span data-stu-id="23e0a-166">**IMsRdpClient3**</span></span>](imsrdpclient3.md)
</dt> <dt>

[<span data-ttu-id="23e0a-167">**IMsRdpClient4**</span><span class="sxs-lookup"><span data-stu-id="23e0a-167">**IMsRdpClient4**</span></span>](imsrdpclient4.md)
</dt> <dt>

[<span data-ttu-id="23e0a-168">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="23e0a-168">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="23e0a-169">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="23e0a-169">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="23e0a-170">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="23e0a-170">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="23e0a-171">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="23e0a-171">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="23e0a-172">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="23e0a-172">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="23e0a-173">**IMsRdpClient10**</span><span class="sxs-lookup"><span data-stu-id="23e0a-173">**IMsRdpClient10**</span></span>](imsrdpclient10.md)
</dt> <dt>

[<span data-ttu-id="23e0a-174">**IMsTscAxEvents::OnConfirmClose**</span><span class="sxs-lookup"><span data-stu-id="23e0a-174">**IMsTscAxEvents::OnConfirmClose**</span></span>](imstscaxevents-onconfirmclose.md)
</dt> <dt>

[<span data-ttu-id="23e0a-175">**IMsTscAxEvents::OnDisconnected**</span><span class="sxs-lookup"><span data-stu-id="23e0a-175">**IMsTscAxEvents::OnDisconnected**</span></span>](imstscaxevents-ondisconnected.md)
</dt> </dl>

 

