---
title: IMsTscAx Connect 方法
description: 使用目前在控制項上設定的屬性起始連接。
ms.assetid: 9bcbdc13-6c66-4737-82a4-98329f173743
ms.tgt_platform: multiple
keywords:
- Connect 方法遠端桌面服務
- Connect 方法遠端桌面服務，IMsTscAx 介面
- IMsTscAx 介面遠端桌面服務，Connect 方法
- Connect 方法遠端桌面服務，IMsRdpClient 介面
- IMsRdpClient 介面遠端桌面服務，Connect 方法
- Connect 方法遠端桌面服務，IMsRdpClient2 介面
- IMsRdpClient2 介面遠端桌面服務，Connect 方法
- Connect 方法遠端桌面服務，IMsRdpClient3 介面
- IMsRdpClient3 介面遠端桌面服務，Connect 方法
- Connect 方法遠端桌面服務，IMsRdpClient4 介面
- IMsRdpClient4 介面遠端桌面服務，Connect 方法
- Connect 方法遠端桌面服務，IMsRdpClient5 介面
- IMsRdpClient5 介面遠端桌面服務，Connect 方法
- Connect 方法遠端桌面服務，IMsRdpClient6 介面
- IMsRdpClient6 介面遠端桌面服務，Connect 方法
- Connect 方法遠端桌面服務，IMsRdpClient7 介面
- IMsRdpClient7 介面遠端桌面服務，Connect 方法
- Connect 方法遠端桌面服務，IMsRdpClient8 介面
- IMsRdpClient8 介面遠端桌面服務，Connect 方法
- Connect 方法遠端桌面服務，IMsRdpClient9 介面
- IMsRdpClient9 介面遠端桌面服務，Connect 方法
topic_type:
- apiref
api_name:
- IMsTscAx.Connect
- IMsRdpClient.Connect
- IMsRdpClient2.Connect
- IMsRdpClient3.Connect
- IMsRdpClient4.Connect
- IMsRdpClient5.Connect
- IMsRdpClient6.Connect
- IMsRdpClient7.Connect
- IMsRdpClient8.Connect
- IMsRdpClient9.Connect
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c267b24c3dd27dd875d895674d98e1350f757c82
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934121"
---
# <a name="imstscaxconnect-method"></a><span data-ttu-id="09e93-124">IMsTscAx：： Connect 方法</span><span class="sxs-lookup"><span data-stu-id="09e93-124">IMsTscAx::Connect method</span></span>

<span data-ttu-id="09e93-125">使用目前在控制項上設定的屬性起始連接。</span><span class="sxs-lookup"><span data-stu-id="09e93-125">Initiates a connection using the properties currently set on the control.</span></span>

## <a name="syntax"></a><span data-ttu-id="09e93-126">語法</span><span class="sxs-lookup"><span data-stu-id="09e93-126">Syntax</span></span>


```C++
HRESULT Connect();
```



## <a name="parameters"></a><span data-ttu-id="09e93-127">參數</span><span class="sxs-lookup"><span data-stu-id="09e93-127">Parameters</span></span>

<span data-ttu-id="09e93-128">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="09e93-128">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="09e93-129">傳回值</span><span class="sxs-lookup"><span data-stu-id="09e93-129">Return value</span></span>

<span data-ttu-id="09e93-130">如果成功，則傳回 **S \_ OK** 。</span><span class="sxs-lookup"><span data-stu-id="09e93-130">Return **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="09e93-131">備註</span><span class="sxs-lookup"><span data-stu-id="09e93-131">Remarks</span></span>

<span data-ttu-id="09e93-132">唯一必要的屬性是伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="09e93-132">The only required property is the server name.</span></span> <span data-ttu-id="09e93-133">請參閱 [**伺服器**](imstscax-server.md) 屬性。</span><span class="sxs-lookup"><span data-stu-id="09e93-133">Refer to the [**Server**](imstscax-server.md) property.</span></span>

<span data-ttu-id="09e93-134">控制項會以非同步方式連接，因此從 Connect 呼叫傳回時，只會指出已成功初始化連接，而不是已完成。</span><span class="sxs-lookup"><span data-stu-id="09e93-134">The control connects asynchronously, so a return from a Connect call indicates only that the connection has been initiated successfully, not that it has been completed.</span></span> <span data-ttu-id="09e93-135">您應該回應 [**IMsTscAxEvents**](imstscaxevents-interface.md) 介面上的事件，以判斷控制項何時成功連接 (或已中斷連線。 ) </span><span class="sxs-lookup"><span data-stu-id="09e93-135">You should respond to events on the [**IMsTscAxEvents**](imstscaxevents-interface.md) interface to determine when the control has successfully connected (or has been disconnected.)</span></span>

<span data-ttu-id="09e93-136">如果控制項已經連接或處於連接狀態，則這個方法會傳回 **E \_ FAIL** 。</span><span class="sxs-lookup"><span data-stu-id="09e93-136">This method returns **E\_FAIL** if it is called while the control is already connected or in the connecting state.</span></span>

<span data-ttu-id="09e93-137">呼叫 **Connect** 之後，您就無法再設定大部分的控制項屬性，直到控制項返回已中斷連線的狀態。</span><span class="sxs-lookup"><span data-stu-id="09e93-137">After **Connect** has been called, most of the control properties can no longer be set until the control returns to the disconnected state.</span></span>

<span data-ttu-id="09e93-138">如需遠端桌面網頁連線的詳細資訊，請參閱 [遠端桌面網頁連線的需求](requirements-for-remote-desktop-web-connection.md)。</span><span class="sxs-lookup"><span data-stu-id="09e93-138">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="09e93-139">規格需求</span><span class="sxs-lookup"><span data-stu-id="09e93-139">Requirements</span></span>



| <span data-ttu-id="09e93-140">需求</span><span class="sxs-lookup"><span data-stu-id="09e93-140">Requirement</span></span> | <span data-ttu-id="09e93-141">值</span><span class="sxs-lookup"><span data-stu-id="09e93-141">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="09e93-142">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="09e93-142">Minimum supported client</span></span><br/> | <span data-ttu-id="09e93-143">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="09e93-143">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="09e93-144">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="09e93-144">Minimum supported server</span></span><br/> | <span data-ttu-id="09e93-145">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="09e93-145">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="09e93-146">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="09e93-146">Type library</span></span><br/>             | <dl> <span data-ttu-id="09e93-147"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="09e93-147"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="09e93-148">DLL</span><span class="sxs-lookup"><span data-stu-id="09e93-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="09e93-149"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="09e93-149"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="09e93-150">IID</span><span class="sxs-lookup"><span data-stu-id="09e93-150">IID</span></span><br/>                      | <span data-ttu-id="09e93-151">IID \_ IMsTscAx 定義為8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span><span class="sxs-lookup"><span data-stu-id="09e93-151">IID\_IMsTscAx is defined as 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="09e93-152">另請參閱</span><span class="sxs-lookup"><span data-stu-id="09e93-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="09e93-153">**IMsRdpClient**</span><span class="sxs-lookup"><span data-stu-id="09e93-153">**IMsRdpClient**</span></span>](imsrdpclient-interface.md)
</dt> <dt>

[<span data-ttu-id="09e93-154">**IMsRdpClient2**</span><span class="sxs-lookup"><span data-stu-id="09e93-154">**IMsRdpClient2**</span></span>](imsrdpclient2.md)
</dt> <dt>

[<span data-ttu-id="09e93-155">**IMsRdpClient3**</span><span class="sxs-lookup"><span data-stu-id="09e93-155">**IMsRdpClient3**</span></span>](imsrdpclient3.md)
</dt> <dt>

[<span data-ttu-id="09e93-156">**IMsRdpClient4**</span><span class="sxs-lookup"><span data-stu-id="09e93-156">**IMsRdpClient4**</span></span>](imsrdpclient4.md)
</dt> <dt>

[<span data-ttu-id="09e93-157">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="09e93-157">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="09e93-158">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="09e93-158">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="09e93-159">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="09e93-159">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="09e93-160">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="09e93-160">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="09e93-161">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="09e93-161">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="09e93-162">**中斷連線**</span><span class="sxs-lookup"><span data-stu-id="09e93-162">**Disconnect**</span></span>](imstscax-disconnect.md)
</dt> <dt>

[<span data-ttu-id="09e93-163">**IMsTscAx**</span><span class="sxs-lookup"><span data-stu-id="09e93-163">**IMsTscAx**</span></span>](imstscax-interface.md)
</dt> </dl>

 

 





