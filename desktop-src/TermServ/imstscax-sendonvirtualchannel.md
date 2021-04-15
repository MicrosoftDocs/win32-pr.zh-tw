---
title: IMsTscAx SendOnVirtualChannel 方法
description: 透過先前使用 CreateVirtualChannels 方法建立的虛擬通道，將資料傳送至遠端桌面工作階段主機 (RD 工作階段主機) 伺服器。
ms.assetid: 795ef508-bdf7-4897-84b1-931615262293
ms.tgt_platform: multiple
keywords:
- SendOnVirtualChannel 方法遠端桌面服務
- SendOnVirtualChannel 方法遠端桌面服務，IMsTscAx 介面
- IMsTscAx 介面遠端桌面服務，SendOnVirtualChannel 方法
- SendOnVirtualChannel 方法遠端桌面服務，IMsRdpClient 介面
- IMsRdpClient 介面遠端桌面服務，SendOnVirtualChannel 方法
- SendOnVirtualChannel 方法遠端桌面服務，IMsRdpClient2 介面
- IMsRdpClient2 介面遠端桌面服務，SendOnVirtualChannel 方法
- SendOnVirtualChannel 方法遠端桌面服務，IMsRdpClient3 介面
- IMsRdpClient3 介面遠端桌面服務，SendOnVirtualChannel 方法
- SendOnVirtualChannel 方法遠端桌面服務，IMsRdpClient4 介面
- IMsRdpClient4 介面遠端桌面服務，SendOnVirtualChannel 方法
- SendOnVirtualChannel 方法遠端桌面服務，IMsRdpClient5 介面
- IMsRdpClient5 介面遠端桌面服務，SendOnVirtualChannel 方法
- SendOnVirtualChannel 方法遠端桌面服務，IMsRdpClient6 介面
- IMsRdpClient6 介面遠端桌面服務，SendOnVirtualChannel 方法
- SendOnVirtualChannel 方法遠端桌面服務，IMsRdpClient7 介面
- IMsRdpClient7 介面遠端桌面服務，SendOnVirtualChannel 方法
- SendOnVirtualChannel 方法遠端桌面服務，IMsRdpClient8 介面
- IMsRdpClient8 介面遠端桌面服務，SendOnVirtualChannel 方法
- SendOnVirtualChannel 方法遠端桌面服務，IMsRdpClient9 介面
- IMsRdpClient9 介面遠端桌面服務，SendOnVirtualChannel 方法
topic_type:
- apiref
api_name:
- IMsTscAx.SendOnVirtualChannel
- IMsRdpClient.SendOnVirtualChannel
- IMsRdpClient2.SendOnVirtualChannel
- IMsRdpClient3.SendOnVirtualChannel
- IMsRdpClient4.SendOnVirtualChannel
- IMsRdpClient5.SendOnVirtualChannel
- IMsRdpClient6.SendOnVirtualChannel
- IMsRdpClient7.SendOnVirtualChannel
- IMsRdpClient8.SendOnVirtualChannel
- IMsRdpClient9.SendOnVirtualChannel
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c1371ae17978601a3194f755dd364d9227b8fc28
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464572"
---
# <a name="imstscaxsendonvirtualchannel-method"></a><span data-ttu-id="8e265-124">IMsTscAx：： SendOnVirtualChannel 方法</span><span class="sxs-lookup"><span data-stu-id="8e265-124">IMsTscAx::SendOnVirtualChannel method</span></span>

<span data-ttu-id="8e265-125">透過先前使用 [**CreateVirtualChannels**](imstscax-createvirtualchannels.md) 方法建立的虛擬通道，將資料傳送至遠端桌面工作階段主機 (RD 工作階段主機) 伺服器。</span><span class="sxs-lookup"><span data-stu-id="8e265-125">Sends data to the Remote Desktop Session Host (RD Session Host) server over a virtual channel that was created previously by using the [**CreateVirtualChannels**](imstscax-createvirtualchannels.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="8e265-126">語法</span><span class="sxs-lookup"><span data-stu-id="8e265-126">Syntax</span></span>


```C++
HRESULT SendOnVirtualChannel(
  [in] BSTR ChanName,
  [in] BSTR ChanData
);
```



## <a name="parameters"></a><span data-ttu-id="8e265-127">參數</span><span class="sxs-lookup"><span data-stu-id="8e265-127">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8e265-128">*ChanName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="8e265-128">*ChanName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8e265-129">呼叫 [**CreateVirtualChannels**](imstscax-createvirtualchannels.md)時所指定的虛擬通道名稱。</span><span class="sxs-lookup"><span data-stu-id="8e265-129">The virtual channel name that was specified in the call to [**CreateVirtualChannels**](imstscax-createvirtualchannels.md).</span></span>

</dd> <dt>

<span data-ttu-id="8e265-130">*ChanData* \[在\]</span><span class="sxs-lookup"><span data-stu-id="8e265-130">*ChanData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8e265-131">要透過虛擬通道傳送的資料，以 **BSTR** 形式傳送。</span><span class="sxs-lookup"><span data-stu-id="8e265-131">The data to send over the virtual channel, in **BSTR** form.</span></span> <span data-ttu-id="8e265-132">這項資料不會限制為以 null 結束的字串。</span><span class="sxs-lookup"><span data-stu-id="8e265-132">There is no restriction that this data must be null-terminated strings.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8e265-133">傳回值</span><span class="sxs-lookup"><span data-stu-id="8e265-133">Return value</span></span>

<span data-ttu-id="8e265-134">如果成功，則傳回 **S \_ OK** 。</span><span class="sxs-lookup"><span data-stu-id="8e265-134">Return **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="8e265-135">備註</span><span class="sxs-lookup"><span data-stu-id="8e265-135">Remarks</span></span>

<span data-ttu-id="8e265-136">如需虛擬通道命名限制的相關資訊，請參閱 [虛擬通道用戶端註冊](virtual-channel-client-registration.md) 。</span><span class="sxs-lookup"><span data-stu-id="8e265-136">Refer to [Virtual Channel Client Registration](virtual-channel-client-registration.md) for information about virtual channel naming restrictions.</span></span>

<span data-ttu-id="8e265-137">如需遠端桌面網頁連線的詳細資訊，請參閱 [遠端桌面網頁連線的需求](requirements-for-remote-desktop-web-connection.md)。</span><span class="sxs-lookup"><span data-stu-id="8e265-137">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="8e265-138">規格需求</span><span class="sxs-lookup"><span data-stu-id="8e265-138">Requirements</span></span>



| <span data-ttu-id="8e265-139">需求</span><span class="sxs-lookup"><span data-stu-id="8e265-139">Requirement</span></span> | <span data-ttu-id="8e265-140">值</span><span class="sxs-lookup"><span data-stu-id="8e265-140">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8e265-141">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8e265-141">Minimum supported client</span></span><br/> | <span data-ttu-id="8e265-142">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8e265-142">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="8e265-143">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8e265-143">Minimum supported server</span></span><br/> | <span data-ttu-id="8e265-144">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8e265-144">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="8e265-145">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="8e265-145">Type library</span></span><br/>             | <dl> <span data-ttu-id="8e265-146"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8e265-146"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="8e265-147">DLL</span><span class="sxs-lookup"><span data-stu-id="8e265-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8e265-148"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8e265-148"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="8e265-149">IID</span><span class="sxs-lookup"><span data-stu-id="8e265-149">IID</span></span><br/>                      | <span data-ttu-id="8e265-150">IID \_ IMsTscAx 定義為8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span><span class="sxs-lookup"><span data-stu-id="8e265-150">IID\_IMsTscAx is defined as 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="8e265-151">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8e265-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8e265-152">**IMsRdpClient**</span><span class="sxs-lookup"><span data-stu-id="8e265-152">**IMsRdpClient**</span></span>](imsrdpclient-interface.md)
</dt> <dt>

[<span data-ttu-id="8e265-153">**IMsRdpClient2**</span><span class="sxs-lookup"><span data-stu-id="8e265-153">**IMsRdpClient2**</span></span>](imsrdpclient2.md)
</dt> <dt>

[<span data-ttu-id="8e265-154">**IMsRdpClient3**</span><span class="sxs-lookup"><span data-stu-id="8e265-154">**IMsRdpClient3**</span></span>](imsrdpclient3.md)
</dt> <dt>

[<span data-ttu-id="8e265-155">**IMsRdpClient4**</span><span class="sxs-lookup"><span data-stu-id="8e265-155">**IMsRdpClient4**</span></span>](imsrdpclient4.md)
</dt> <dt>

[<span data-ttu-id="8e265-156">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="8e265-156">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="8e265-157">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="8e265-157">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="8e265-158">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="8e265-158">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="8e265-159">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="8e265-159">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="8e265-160">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="8e265-160">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="8e265-161">**CreateVirtualChannels**</span><span class="sxs-lookup"><span data-stu-id="8e265-161">**CreateVirtualChannels**</span></span>](imstscax-createvirtualchannels.md)
</dt> <dt>

[<span data-ttu-id="8e265-162">**IMsTscAx**</span><span class="sxs-lookup"><span data-stu-id="8e265-162">**IMsTscAx**</span></span>](imstscax-interface.md)
</dt> </dl>

 

 





