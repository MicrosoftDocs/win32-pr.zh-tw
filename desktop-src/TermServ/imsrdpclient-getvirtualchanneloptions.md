---
title: IMsRdpClient GetVirtualChannelOptions 方法
description: 抓取為虛擬通道設定的選項。
ms.assetid: d2ec9fb2-c0dc-49f1-a86b-d7abca13a322
ms.tgt_platform: multiple
keywords:
- GetVirtualChannelOptions 方法遠端桌面服務
- GetVirtualChannelOptions 方法遠端桌面服務，IMsRdpClient 介面
- IMsRdpClient 介面遠端桌面服務，GetVirtualChannelOptions 方法
- GetVirtualChannelOptions 方法遠端桌面服務，IMsRdpClient2 介面
- IMsRdpClient2 介面遠端桌面服務，GetVirtualChannelOptions 方法
- GetVirtualChannelOptions 方法遠端桌面服務，IMsRdpClient3 介面
- IMsRdpClient3 介面遠端桌面服務，GetVirtualChannelOptions 方法
- GetVirtualChannelOptions 方法遠端桌面服務，IMsRdpClient4 介面
- IMsRdpClient4 介面遠端桌面服務，GetVirtualChannelOptions 方法
- GetVirtualChannelOptions 方法遠端桌面服務，IMsRdpClient5 介面
- IMsRdpClient5 介面遠端桌面服務，GetVirtualChannelOptions 方法
- GetVirtualChannelOptions 方法遠端桌面服務，IMsRdpClient6 介面
- IMsRdpClient6 介面遠端桌面服務，GetVirtualChannelOptions 方法
- GetVirtualChannelOptions 方法遠端桌面服務，IMsRdpClient7 介面
- IMsRdpClient7 介面遠端桌面服務，GetVirtualChannelOptions 方法
- GetVirtualChannelOptions 方法遠端桌面服務，IMsRdpClient8 介面
- IMsRdpClient8 介面遠端桌面服務，GetVirtualChannelOptions 方法
- GetVirtualChannelOptions 方法遠端桌面服務，IMsRdpClient9 介面
- IMsRdpClient9 介面遠端桌面服務，GetVirtualChannelOptions 方法
- GetVirtualChannelOptions 方法遠端桌面服務，IMsRdpClient10 介面
- IMsRdpClient10 介面遠端桌面服務，GetVirtualChannelOptions 方法
topic_type:
- apiref
api_name:
- IMsRdpClient.GetVirtualChannelOptions
- IMsRdpClient2.GetVirtualChannelOptions
- IMsRdpClient3.GetVirtualChannelOptions
- IMsRdpClient4.GetVirtualChannelOptions
- IMsRdpClient5.GetVirtualChannelOptions
- IMsRdpClient6.GetVirtualChannelOptions
- IMsRdpClient7.GetVirtualChannelOptions
- IMsRdpClient8.GetVirtualChannelOptions
- IMsRdpClient9.GetVirtualChannelOptions
- IMsRdpClient10.GetVirtualChannelOptions
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 71548002ebc67dae8dc1a49e8144da3de608afb2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106980292"
---
# <a name="imsrdpclientgetvirtualchanneloptions-method"></a><span data-ttu-id="f068c-124">IMsRdpClient：： GetVirtualChannelOptions 方法</span><span class="sxs-lookup"><span data-stu-id="f068c-124">IMsRdpClient::GetVirtualChannelOptions method</span></span>

<span data-ttu-id="f068c-125">抓取為虛擬通道設定的選項。</span><span class="sxs-lookup"><span data-stu-id="f068c-125">Retrieves the options set for a virtual channel.</span></span>

## <a name="syntax"></a><span data-ttu-id="f068c-126">語法</span><span class="sxs-lookup"><span data-stu-id="f068c-126">Syntax</span></span>


```C++
HRESULT GetVirtualChannelOptions(
  [in]  BSTR ChanName,
  [out] LONG *pChanOptions
);
```



## <a name="parameters"></a><span data-ttu-id="f068c-127">參數</span><span class="sxs-lookup"><span data-stu-id="f068c-127">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f068c-128">*ChanName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f068c-128">*ChanName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f068c-129">呼叫 [**CreateVirtualChannels**](imstscax-createvirtualchannels.md) 方法時所指定的虛擬通道名稱。</span><span class="sxs-lookup"><span data-stu-id="f068c-129">The name of a virtual channel that was specified in the call to [**CreateVirtualChannels**](imstscax-createvirtualchannels.md) method.</span></span>

</dd> <dt>

<span data-ttu-id="f068c-130">*pChanOptions* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="f068c-130">*pChanOptions* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f068c-131">為 *ChanName* 參數所指定的虛擬通道設定的選項。</span><span class="sxs-lookup"><span data-stu-id="f068c-131">The options set for the virtual channel specified by the *ChanName* parameter.</span></span> <span data-ttu-id="f068c-132">如需可能選項的描述，請參閱 [**通道 \_ 定義**](/windows/desktop/api/Pchannel/ns-pchannel-tagchannel_def)。</span><span class="sxs-lookup"><span data-stu-id="f068c-132">For a description of possible options, see [**CHANNEL\_DEF**](/windows/desktop/api/Pchannel/ns-pchannel-tagchannel_def).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f068c-133">傳回值</span><span class="sxs-lookup"><span data-stu-id="f068c-133">Return value</span></span>

<span data-ttu-id="f068c-134">如果成功，則傳回 **S \_ OK** 。</span><span class="sxs-lookup"><span data-stu-id="f068c-134">Return **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="f068c-135">備註</span><span class="sxs-lookup"><span data-stu-id="f068c-135">Remarks</span></span>

<span data-ttu-id="f068c-136">如需遠端桌面網頁連線的詳細資訊，請參閱 [遠端桌面網頁連線的需求](requirements-for-remote-desktop-web-connection.md)。</span><span class="sxs-lookup"><span data-stu-id="f068c-136">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f068c-137">規格需求</span><span class="sxs-lookup"><span data-stu-id="f068c-137">Requirements</span></span>



| <span data-ttu-id="f068c-138">需求</span><span class="sxs-lookup"><span data-stu-id="f068c-138">Requirement</span></span> | <span data-ttu-id="f068c-139">值</span><span class="sxs-lookup"><span data-stu-id="f068c-139">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f068c-140">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f068c-140">Minimum supported client</span></span><br/> | <span data-ttu-id="f068c-141">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f068c-141">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="f068c-142">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f068c-142">Minimum supported server</span></span><br/> | <span data-ttu-id="f068c-143">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f068c-143">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="f068c-144">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="f068c-144">Type library</span></span><br/>             | <dl> <span data-ttu-id="f068c-145"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f068c-145"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="f068c-146">DLL</span><span class="sxs-lookup"><span data-stu-id="f068c-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f068c-147"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f068c-147"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="f068c-148">IID</span><span class="sxs-lookup"><span data-stu-id="f068c-148">IID</span></span><br/>                      | <span data-ttu-id="f068c-149">IID \_ IMsRdpClient 定義為92b4a539-7115-4b7c-a5a9-e5d9efc2780a</span><span class="sxs-lookup"><span data-stu-id="f068c-149">IID\_IMsRdpClient is defined as 92b4a539-7115-4b7c-a5a9-e5d9efc2780a</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="f068c-150">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f068c-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f068c-151">**IMsRdpClient**</span><span class="sxs-lookup"><span data-stu-id="f068c-151">**IMsRdpClient**</span></span>](imsrdpclient-interface.md)
</dt> <dt>

[<span data-ttu-id="f068c-152">**IMsRdpClient2**</span><span class="sxs-lookup"><span data-stu-id="f068c-152">**IMsRdpClient2**</span></span>](imsrdpclient2.md)
</dt> <dt>

[<span data-ttu-id="f068c-153">**IMsRdpClient3**</span><span class="sxs-lookup"><span data-stu-id="f068c-153">**IMsRdpClient3**</span></span>](imsrdpclient3.md)
</dt> <dt>

[<span data-ttu-id="f068c-154">**IMsRdpClient4**</span><span class="sxs-lookup"><span data-stu-id="f068c-154">**IMsRdpClient4**</span></span>](imsrdpclient4.md)
</dt> <dt>

[<span data-ttu-id="f068c-155">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="f068c-155">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="f068c-156">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="f068c-156">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="f068c-157">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="f068c-157">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="f068c-158">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="f068c-158">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="f068c-159">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="f068c-159">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="f068c-160">**IMsRdpClient10**</span><span class="sxs-lookup"><span data-stu-id="f068c-160">**IMsRdpClient10**</span></span>](imsrdpclient10.md)
</dt> <dt>

[<span data-ttu-id="f068c-161">**通道 \_ 定義**</span><span class="sxs-lookup"><span data-stu-id="f068c-161">**CHANNEL\_DEF**</span></span>](/windows/desktop/api/Pchannel/ns-pchannel-tagchannel_def)
</dt> <dt>

[<span data-ttu-id="f068c-162">**CreateVirtualChannels**</span><span class="sxs-lookup"><span data-stu-id="f068c-162">**CreateVirtualChannels**</span></span>](imstscax-createvirtualchannels.md)
</dt> <dt>

[<span data-ttu-id="f068c-163">**SetVirtualChannelOptions**</span><span class="sxs-lookup"><span data-stu-id="f068c-163">**SetVirtualChannelOptions**</span></span>](imsrdpclient-setvirtualchanneloptions.md)
</dt> </dl>

 

 





