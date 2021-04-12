---
title: IMsRdpClient SetVirtualChannelOptions 方法
description: 設定遠端桌面 ActiveX 控制項的虛擬通道選項。
ms.assetid: c74c3917-5766-4d5b-8458-b051eb91cb28
ms.tgt_platform: multiple
keywords:
- SetVirtualChannelOptions 方法遠端桌面服務
- SetVirtualChannelOptions 方法遠端桌面服務，IMsRdpClient 介面
- IMsRdpClient 介面遠端桌面服務，SetVirtualChannelOptions 方法
- SetVirtualChannelOptions 方法遠端桌面服務，IMsRdpClient2 介面
- IMsRdpClient2 介面遠端桌面服務，SetVirtualChannelOptions 方法
- SetVirtualChannelOptions 方法遠端桌面服務，IMsRdpClient3 介面
- IMsRdpClient3 介面遠端桌面服務，SetVirtualChannelOptions 方法
- SetVirtualChannelOptions 方法遠端桌面服務，IMsRdpClient4 介面
- IMsRdpClient4 介面遠端桌面服務，SetVirtualChannelOptions 方法
- SetVirtualChannelOptions 方法遠端桌面服務，IMsRdpClient5 介面
- IMsRdpClient5 介面遠端桌面服務，SetVirtualChannelOptions 方法
- SetVirtualChannelOptions 方法遠端桌面服務，IMsRdpClient6 介面
- IMsRdpClient6 介面遠端桌面服務，SetVirtualChannelOptions 方法
- SetVirtualChannelOptions 方法遠端桌面服務，IMsRdpClient7 介面
- IMsRdpClient7 介面遠端桌面服務，SetVirtualChannelOptions 方法
- SetVirtualChannelOptions 方法遠端桌面服務，IMsRdpClient8 介面
- IMsRdpClient8 介面遠端桌面服務，SetVirtualChannelOptions 方法
- SetVirtualChannelOptions 方法遠端桌面服務，IMsRdpClient9 介面
- IMsRdpClient9 介面遠端桌面服務，SetVirtualChannelOptions 方法
- SetVirtualChannelOptions 方法遠端桌面服務，IMsRdpClient10 介面
- IMsRdpClient10 介面遠端桌面服務，SetVirtualChannelOptions 方法
topic_type:
- apiref
api_name:
- IMsRdpClient.SetVirtualChannelOptions
- IMsRdpClient2.SetVirtualChannelOptions
- IMsRdpClient3.SetVirtualChannelOptions
- IMsRdpClient4.SetVirtualChannelOptions
- IMsRdpClient5.SetVirtualChannelOptions
- IMsRdpClient6.SetVirtualChannelOptions
- IMsRdpClient7.SetVirtualChannelOptions
- IMsRdpClient8.SetVirtualChannelOptions
- IMsRdpClient9.SetVirtualChannelOptions
- IMsRdpClient10.SetVirtualChannelOptions
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 10e727fd3486b9d1b31fb3a421ea6ff268949790
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384202"
---
# <a name="imsrdpclientsetvirtualchanneloptions-method"></a><span data-ttu-id="66f9b-124">IMsRdpClient：： SetVirtualChannelOptions 方法</span><span class="sxs-lookup"><span data-stu-id="66f9b-124">IMsRdpClient::SetVirtualChannelOptions method</span></span>

<span data-ttu-id="66f9b-125">設定遠端桌面 ActiveX 控制項的虛擬通道選項。</span><span class="sxs-lookup"><span data-stu-id="66f9b-125">Sets the virtual channel options for the Remote Desktop ActiveX control.</span></span>

<span data-ttu-id="66f9b-126">請在呼叫 [**CreateVirtualChannels**](imstscax-createvirtualchannels.md) 方法之後，但在使用 [**Connect**](imstscax-connect.md) 方法建立連接之前呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="66f9b-126">Call this method after calling the [**CreateVirtualChannels**](imstscax-createvirtualchannels.md) method, but before establishing a connection with the [**Connect**](imstscax-connect.md) method.</span></span> <span data-ttu-id="66f9b-127">這個方法會在使用 **CreateVirtualChannels** 建立的虛擬通道上設定其他選項。</span><span class="sxs-lookup"><span data-stu-id="66f9b-127">This method sets additional options on virtual channels that have been created with **CreateVirtualChannels**.</span></span>

## <a name="syntax"></a><span data-ttu-id="66f9b-128">語法</span><span class="sxs-lookup"><span data-stu-id="66f9b-128">Syntax</span></span>


```C++
HRESULT SetVirtualChannelOptions(
  [in] BSTR ChanName,
  [in] LONG chanOptions
);
```



## <a name="parameters"></a><span data-ttu-id="66f9b-129">參數</span><span class="sxs-lookup"><span data-stu-id="66f9b-129">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="66f9b-130">*ChanName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="66f9b-130">*ChanName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="66f9b-131">呼叫 [**CreateVirtualChannels**](imstscax-createvirtualchannels.md) 方法時所指定的虛擬通道名稱。</span><span class="sxs-lookup"><span data-stu-id="66f9b-131">The name of the virtual channel that was specified in the call to the [**CreateVirtualChannels**](imstscax-createvirtualchannels.md) method.</span></span>

</dd> <dt>

<span data-ttu-id="66f9b-132">*chanOptions* \[在\]</span><span class="sxs-lookup"><span data-stu-id="66f9b-132">*chanOptions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="66f9b-133">要為 *ChanName* 參數指定的虛擬通道設定的選項。</span><span class="sxs-lookup"><span data-stu-id="66f9b-133">The options to set for the virtual channel specified by the *ChanName* parameter.</span></span> <span data-ttu-id="66f9b-134">如需可能選項的描述，請參閱 [**通道 \_ 定義**](/windows/desktop/api/Pchannel/ns-pchannel-tagchannel_def)。</span><span class="sxs-lookup"><span data-stu-id="66f9b-134">For a description of possible options, see [**CHANNEL\_DEF**](/windows/desktop/api/Pchannel/ns-pchannel-tagchannel_def).</span></span> <span data-ttu-id="66f9b-135">如需詳細資訊，請參閱接下來的＜備註＞一節。</span><span class="sxs-lookup"><span data-stu-id="66f9b-135">For more information, see the following Remarks section.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="66f9b-136">傳回值</span><span class="sxs-lookup"><span data-stu-id="66f9b-136">Return value</span></span>

<span data-ttu-id="66f9b-137">如果成功，則傳回 **S \_ OK** 。</span><span class="sxs-lookup"><span data-stu-id="66f9b-137">Return **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="66f9b-138">備註</span><span class="sxs-lookup"><span data-stu-id="66f9b-138">Remarks</span></span>

<span data-ttu-id="66f9b-139">使用這個方法的範例，是藉由設定 **通道 \_ 選項 \_ 遠端 \_ 控制 \_ 持續** 旗標，將通道宣告為遠端控制持續性。</span><span class="sxs-lookup"><span data-stu-id="66f9b-139">An example of using this method would be to declare the channel as remote control persistent by setting the **CHANNEL\_OPTION\_REMOTE\_CONTROL\_PERSISTENT** flag.</span></span> <span data-ttu-id="66f9b-140">這表示當遠端控制連接到用戶端的會話或中斷連線時，就不會關閉通道。</span><span class="sxs-lookup"><span data-stu-id="66f9b-140">This means that the channel would not be closed when a remote control connects to or disconnects from the session connected to the client.</span></span> <span data-ttu-id="66f9b-141">如需詳細資訊，請參閱 [遠端控制持續性虛擬通道](remote-control-persistent-virtual-channels.md)。</span><span class="sxs-lookup"><span data-stu-id="66f9b-141">For more information, see [Remote Control Persistent Virtual Channels](remote-control-persistent-virtual-channels.md).</span></span>

<span data-ttu-id="66f9b-142">如需遠端桌面網頁連線的詳細資訊，請參閱 [遠端桌面網頁連線的需求](requirements-for-remote-desktop-web-connection.md)。</span><span class="sxs-lookup"><span data-stu-id="66f9b-142">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="66f9b-143">規格需求</span><span class="sxs-lookup"><span data-stu-id="66f9b-143">Requirements</span></span>



| <span data-ttu-id="66f9b-144">需求</span><span class="sxs-lookup"><span data-stu-id="66f9b-144">Requirement</span></span> | <span data-ttu-id="66f9b-145">值</span><span class="sxs-lookup"><span data-stu-id="66f9b-145">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="66f9b-146">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="66f9b-146">Minimum supported client</span></span><br/> | <span data-ttu-id="66f9b-147">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="66f9b-147">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="66f9b-148">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="66f9b-148">Minimum supported server</span></span><br/> | <span data-ttu-id="66f9b-149">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="66f9b-149">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="66f9b-150">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="66f9b-150">Type library</span></span><br/>             | <dl> <span data-ttu-id="66f9b-151"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="66f9b-151"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="66f9b-152">DLL</span><span class="sxs-lookup"><span data-stu-id="66f9b-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="66f9b-153"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="66f9b-153"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="66f9b-154">IID</span><span class="sxs-lookup"><span data-stu-id="66f9b-154">IID</span></span><br/>                      | <span data-ttu-id="66f9b-155">IID \_ IMsRdpClient 定義為92b4a539-7115-4b7c-a5a9-e5d9efc2780a</span><span class="sxs-lookup"><span data-stu-id="66f9b-155">IID\_IMsRdpClient is defined as 92b4a539-7115-4b7c-a5a9-e5d9efc2780a</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="66f9b-156">另請參閱</span><span class="sxs-lookup"><span data-stu-id="66f9b-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="66f9b-157">**IMsRdpClient**</span><span class="sxs-lookup"><span data-stu-id="66f9b-157">**IMsRdpClient**</span></span>](imsrdpclient-interface.md)
</dt> <dt>

[<span data-ttu-id="66f9b-158">**IMsRdpClient2**</span><span class="sxs-lookup"><span data-stu-id="66f9b-158">**IMsRdpClient2**</span></span>](imsrdpclient2.md)
</dt> <dt>

[<span data-ttu-id="66f9b-159">**IMsRdpClient3**</span><span class="sxs-lookup"><span data-stu-id="66f9b-159">**IMsRdpClient3**</span></span>](imsrdpclient3.md)
</dt> <dt>

[<span data-ttu-id="66f9b-160">**IMsRdpClient4**</span><span class="sxs-lookup"><span data-stu-id="66f9b-160">**IMsRdpClient4**</span></span>](imsrdpclient4.md)
</dt> <dt>

[<span data-ttu-id="66f9b-161">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="66f9b-161">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="66f9b-162">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="66f9b-162">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="66f9b-163">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="66f9b-163">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="66f9b-164">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="66f9b-164">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="66f9b-165">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="66f9b-165">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="66f9b-166">**IMsRdpClient10**</span><span class="sxs-lookup"><span data-stu-id="66f9b-166">**IMsRdpClient10**</span></span>](imsrdpclient10.md)
</dt> <dt>

[<span data-ttu-id="66f9b-167">**通道 \_ 定義**</span><span class="sxs-lookup"><span data-stu-id="66f9b-167">**CHANNEL\_DEF**</span></span>](/windows/desktop/api/Pchannel/ns-pchannel-tagchannel_def)
</dt> <dt>

[<span data-ttu-id="66f9b-168">**CreateVirtualChannels**</span><span class="sxs-lookup"><span data-stu-id="66f9b-168">**CreateVirtualChannels**</span></span>](imstscax-createvirtualchannels.md)
</dt> <dt>

[<span data-ttu-id="66f9b-169">**GetVirtualChannelOptions**</span><span class="sxs-lookup"><span data-stu-id="66f9b-169">**GetVirtualChannelOptions**</span></span>](imsrdpclient-getvirtualchanneloptions.md)
</dt> </dl>

 

 





