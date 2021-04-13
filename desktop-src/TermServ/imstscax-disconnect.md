---
title: IMsTscAx 中斷連線方法
description: 中斷使用中連接。
ms.assetid: 9fcffd45-b293-4650-be8f-1b0d01d592a2
ms.tgt_platform: multiple
keywords:
- 中斷連接方法遠端桌面服務
- 中斷連接方法遠端桌面服務，IMsTscAx 介面
- IMsTscAx 介面遠端桌面服務，中斷連線方法
- 中斷連接方法遠端桌面服務，IMsRdpClient 介面
- IMsRdpClient 介面遠端桌面服務，中斷連線方法
- 中斷連接方法遠端桌面服務，IMsRdpClient2 介面
- IMsRdpClient2 介面遠端桌面服務，中斷連線方法
- 中斷連接方法遠端桌面服務，IMsRdpClient3 介面
- IMsRdpClient3 介面遠端桌面服務，中斷連線方法
- 中斷連接方法遠端桌面服務，IMsRdpClient4 介面
- IMsRdpClient4 介面遠端桌面服務，中斷連線方法
- 中斷連接方法遠端桌面服務，IMsRdpClient5 介面
- IMsRdpClient5 介面遠端桌面服務，中斷連線方法
- 中斷連接方法遠端桌面服務，IMsRdpClient6 介面
- IMsRdpClient6 介面遠端桌面服務，中斷連線方法
- 中斷連接方法遠端桌面服務，IMsRdpClient7 介面
- IMsRdpClient7 介面遠端桌面服務，中斷連線方法
- 中斷連接方法遠端桌面服務，IMsRdpClient8 介面
- IMsRdpClient8 介面遠端桌面服務，中斷連線方法
- 中斷連接方法遠端桌面服務，IMsRdpClient9 介面
- IMsRdpClient9 介面遠端桌面服務，中斷連線方法
topic_type:
- apiref
api_name:
- IMsTscAx.Disconnect
- IMsRdpClient.Disconnect
- IMsRdpClient2.Disconnect
- IMsRdpClient3.Disconnect
- IMsRdpClient4.Disconnect
- IMsRdpClient5.Disconnect
- IMsRdpClient6.Disconnect
- IMsRdpClient7.Disconnect
- IMsRdpClient8.Disconnect
- IMsRdpClient9.Disconnect
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d4f1545a8244209c0b4fa8267fcc8ce2a41e090
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508843"
---
# <a name="imstscaxdisconnect-method"></a><span data-ttu-id="62bd8-124">IMsTscAx：:D isconnect 方法</span><span class="sxs-lookup"><span data-stu-id="62bd8-124">IMsTscAx::Disconnect method</span></span>

<span data-ttu-id="62bd8-125">中斷使用中連接。</span><span class="sxs-lookup"><span data-stu-id="62bd8-125">Disconnects the active connection.</span></span>

## <a name="syntax"></a><span data-ttu-id="62bd8-126">語法</span><span class="sxs-lookup"><span data-stu-id="62bd8-126">Syntax</span></span>


```C++
HRESULT Disconnect();
```



## <a name="parameters"></a><span data-ttu-id="62bd8-127">參數</span><span class="sxs-lookup"><span data-stu-id="62bd8-127">Parameters</span></span>

<span data-ttu-id="62bd8-128">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="62bd8-128">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="62bd8-129">傳回值</span><span class="sxs-lookup"><span data-stu-id="62bd8-129">Return value</span></span>

<span data-ttu-id="62bd8-130">如果成功，則傳回 **S \_ OK** 。</span><span class="sxs-lookup"><span data-stu-id="62bd8-130">Return **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="62bd8-131">備註</span><span class="sxs-lookup"><span data-stu-id="62bd8-131">Remarks</span></span>

<span data-ttu-id="62bd8-132">如果在控制項未連接時呼叫此方法，則此方法會傳回錯誤值。</span><span class="sxs-lookup"><span data-stu-id="62bd8-132">This method returns a failure error value if it is called when the control is not connected.</span></span>

<span data-ttu-id="62bd8-133">您也可以關閉主視窗，將控制項中斷連接。</span><span class="sxs-lookup"><span data-stu-id="62bd8-133">It is also possible to disconnect the control by closing its main window.</span></span> <span data-ttu-id="62bd8-134">例如，如果控制項是裝載在網頁中，就不需要在離開頁面之前呼叫這個方法。控制項的關閉會觸發中斷連接。</span><span class="sxs-lookup"><span data-stu-id="62bd8-134">For example, if the control is hosted in a webpage, it is not necessary to call this method before leaving the page; the closing of the control triggers a disconnection.</span></span>

<span data-ttu-id="62bd8-135">如需遠端桌面網頁連線的詳細資訊，請參閱 [遠端桌面網頁連線的需求](requirements-for-remote-desktop-web-connection.md)。</span><span class="sxs-lookup"><span data-stu-id="62bd8-135">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="62bd8-136">規格需求</span><span class="sxs-lookup"><span data-stu-id="62bd8-136">Requirements</span></span>



| <span data-ttu-id="62bd8-137">需求</span><span class="sxs-lookup"><span data-stu-id="62bd8-137">Requirement</span></span> | <span data-ttu-id="62bd8-138">值</span><span class="sxs-lookup"><span data-stu-id="62bd8-138">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="62bd8-139">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="62bd8-139">Minimum supported client</span></span><br/> | <span data-ttu-id="62bd8-140">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="62bd8-140">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="62bd8-141">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="62bd8-141">Minimum supported server</span></span><br/> | <span data-ttu-id="62bd8-142">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="62bd8-142">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="62bd8-143">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="62bd8-143">Type library</span></span><br/>             | <dl> <span data-ttu-id="62bd8-144"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="62bd8-144"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="62bd8-145">DLL</span><span class="sxs-lookup"><span data-stu-id="62bd8-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="62bd8-146"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="62bd8-146"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="62bd8-147">IID</span><span class="sxs-lookup"><span data-stu-id="62bd8-147">IID</span></span><br/>                      | <span data-ttu-id="62bd8-148">IID \_ IMsTscAx 定義為8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span><span class="sxs-lookup"><span data-stu-id="62bd8-148">IID\_IMsTscAx is defined as 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="62bd8-149">另請參閱</span><span class="sxs-lookup"><span data-stu-id="62bd8-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="62bd8-150">**IMsRdpClient**</span><span class="sxs-lookup"><span data-stu-id="62bd8-150">**IMsRdpClient**</span></span>](imsrdpclient-interface.md)
</dt> <dt>

[<span data-ttu-id="62bd8-151">**IMsRdpClient2**</span><span class="sxs-lookup"><span data-stu-id="62bd8-151">**IMsRdpClient2**</span></span>](imsrdpclient2.md)
</dt> <dt>

[<span data-ttu-id="62bd8-152">**IMsRdpClient3**</span><span class="sxs-lookup"><span data-stu-id="62bd8-152">**IMsRdpClient3**</span></span>](imsrdpclient3.md)
</dt> <dt>

[<span data-ttu-id="62bd8-153">**IMsRdpClient4**</span><span class="sxs-lookup"><span data-stu-id="62bd8-153">**IMsRdpClient4**</span></span>](imsrdpclient4.md)
</dt> <dt>

[<span data-ttu-id="62bd8-154">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="62bd8-154">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="62bd8-155">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="62bd8-155">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="62bd8-156">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="62bd8-156">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="62bd8-157">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="62bd8-157">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="62bd8-158">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="62bd8-158">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="62bd8-159">**連接**</span><span class="sxs-lookup"><span data-stu-id="62bd8-159">**Connect**</span></span>](imstscax-connect.md)
</dt> <dt>

[<span data-ttu-id="62bd8-160">**IMsTscAx**</span><span class="sxs-lookup"><span data-stu-id="62bd8-160">**IMsTscAx**</span></span>](imstscax-interface.md)
</dt> </dl>

 

 





