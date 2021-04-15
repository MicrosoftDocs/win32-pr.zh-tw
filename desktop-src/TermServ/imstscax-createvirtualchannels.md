---
title: IMsTscAx CreateVirtualChannels 方法
description: 針對每個指定的虛擬通道名稱建立用戶端虛擬通道物件。
ms.assetid: 3afd2f1c-abd5-4f85-93fb-6d1173f09b07
ms.tgt_platform: multiple
keywords:
- CreateVirtualChannels 方法遠端桌面服務
- CreateVirtualChannels 方法遠端桌面服務，IMsTscAx 介面
- IMsTscAx 介面遠端桌面服務，CreateVirtualChannels 方法
- CreateVirtualChannels 方法遠端桌面服務，IMsRdpClient 介面
- IMsRdpClient 介面遠端桌面服務，CreateVirtualChannels 方法
- CreateVirtualChannels 方法遠端桌面服務，IMsRdpClient2 介面
- IMsRdpClient2 介面遠端桌面服務，CreateVirtualChannels 方法
- CreateVirtualChannels 方法遠端桌面服務，IMsRdpClient3 介面
- IMsRdpClient3 介面遠端桌面服務，CreateVirtualChannels 方法
- CreateVirtualChannels 方法遠端桌面服務，IMsRdpClient4 介面
- IMsRdpClient4 介面遠端桌面服務，CreateVirtualChannels 方法
- CreateVirtualChannels 方法遠端桌面服務，IMsRdpClient5 介面
- IMsRdpClient5 介面遠端桌面服務，CreateVirtualChannels 方法
- CreateVirtualChannels 方法遠端桌面服務，IMsRdpClient6 介面
- IMsRdpClient6 介面遠端桌面服務，CreateVirtualChannels 方法
- CreateVirtualChannels 方法遠端桌面服務，IMsRdpClient7 介面
- IMsRdpClient7 介面遠端桌面服務，CreateVirtualChannels 方法
- CreateVirtualChannels 方法遠端桌面服務，IMsRdpClient8 介面
- IMsRdpClient8 介面遠端桌面服務，CreateVirtualChannels 方法
- CreateVirtualChannels 方法遠端桌面服務，IMsRdpClient9 介面
- IMsRdpClient9 介面遠端桌面服務，CreateVirtualChannels 方法
topic_type:
- apiref
api_name:
- IMsTscAx.CreateVirtualChannels
- IMsRdpClient.CreateVirtualChannels
- IMsRdpClient2.CreateVirtualChannels
- IMsRdpClient3.CreateVirtualChannels
- IMsRdpClient4.CreateVirtualChannels
- IMsRdpClient5.CreateVirtualChannels
- IMsRdpClient6.CreateVirtualChannels
- IMsRdpClient7.CreateVirtualChannels
- IMsRdpClient8.CreateVirtualChannels
- IMsRdpClient9.CreateVirtualChannels
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d59c185763ddd3685e5e566f88e26a6aa6211b4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465985"
---
# <a name="imstscaxcreatevirtualchannels-method"></a><span data-ttu-id="e0fc1-124">IMsTscAx：： CreateVirtualChannels 方法</span><span class="sxs-lookup"><span data-stu-id="e0fc1-124">IMsTscAx::CreateVirtualChannels method</span></span>

<span data-ttu-id="e0fc1-125">針對每個指定的虛擬通道名稱建立用戶端虛擬通道物件。</span><span class="sxs-lookup"><span data-stu-id="e0fc1-125">Creates a client-side virtual channel object for each specified virtual channel name.</span></span>

## <a name="syntax"></a><span data-ttu-id="e0fc1-126">語法</span><span class="sxs-lookup"><span data-stu-id="e0fc1-126">Syntax</span></span>


```C++
HRESULT CreateVirtualChannels(
  [in] BSTR newVal
);
```



## <a name="parameters"></a><span data-ttu-id="e0fc1-127">參數</span><span class="sxs-lookup"><span data-stu-id="e0fc1-127">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e0fc1-128">*newVal* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e0fc1-128">*newVal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e0fc1-129">有效虛擬通道名稱的逗號分隔清單。</span><span class="sxs-lookup"><span data-stu-id="e0fc1-129">A comma-separated list of valid virtual channel names.</span></span> <span data-ttu-id="e0fc1-130">這份清單中每個名稱的長度最少可以是一個，最多七個字母字元。</span><span class="sxs-lookup"><span data-stu-id="e0fc1-130">The length of each name in this list can be a minimum of one and a maximum of seven alphabetical characters.</span></span> <span data-ttu-id="e0fc1-131">整個字串的長度最少為1，最多可為300個字母字元。</span><span class="sxs-lookup"><span data-stu-id="e0fc1-131">The length of the entire string can be a minimum of one and a maximum of 300 alphabetical characters.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e0fc1-132">傳回值</span><span class="sxs-lookup"><span data-stu-id="e0fc1-132">Return value</span></span>

<span data-ttu-id="e0fc1-133">如果成功，則傳回 **S \_ OK** 。</span><span class="sxs-lookup"><span data-stu-id="e0fc1-133">Returns **S\_OK** if successful.</span></span> <span data-ttu-id="e0fc1-134">如果傳遞的參數不符合指定的準則，則會傳回 **E \_ INVALIDARG** 。</span><span class="sxs-lookup"><span data-stu-id="e0fc1-134">Returns **E\_INVALIDARG** if the parameter that is passed does not meet the criteria that is specified.</span></span>

## <a name="remarks"></a><span data-ttu-id="e0fc1-135">備註</span><span class="sxs-lookup"><span data-stu-id="e0fc1-135">Remarks</span></span>

<span data-ttu-id="e0fc1-136">呼叫 [**連接**](imstscax-connect.md) 方法之前，請先呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="e0fc1-136">Call this method before calling the [**Connect**](imstscax-connect.md) method.</span></span>

<span data-ttu-id="e0fc1-137">如需虛擬通道命名限制的相關資訊，請參閱 [虛擬通道用戶端註冊](virtual-channel-client-registration.md) 。</span><span class="sxs-lookup"><span data-stu-id="e0fc1-137">Refer to [Virtual Channel Client Registration](virtual-channel-client-registration.md) for information about virtual channel naming restrictions.</span></span>

<span data-ttu-id="e0fc1-138">如需遠端桌面網頁連線的詳細資訊，請參閱 [遠端桌面網頁連線的需求](requirements-for-remote-desktop-web-connection.md)。</span><span class="sxs-lookup"><span data-stu-id="e0fc1-138">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e0fc1-139">規格需求</span><span class="sxs-lookup"><span data-stu-id="e0fc1-139">Requirements</span></span>



| <span data-ttu-id="e0fc1-140">需求</span><span class="sxs-lookup"><span data-stu-id="e0fc1-140">Requirement</span></span> | <span data-ttu-id="e0fc1-141">值</span><span class="sxs-lookup"><span data-stu-id="e0fc1-141">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e0fc1-142">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e0fc1-142">Minimum supported client</span></span><br/> | <span data-ttu-id="e0fc1-143">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e0fc1-143">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="e0fc1-144">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e0fc1-144">Minimum supported server</span></span><br/> | <span data-ttu-id="e0fc1-145">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e0fc1-145">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="e0fc1-146">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="e0fc1-146">Type library</span></span><br/>             | <dl> <span data-ttu-id="e0fc1-147"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e0fc1-147"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="e0fc1-148">DLL</span><span class="sxs-lookup"><span data-stu-id="e0fc1-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e0fc1-149"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e0fc1-149"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="e0fc1-150">IID</span><span class="sxs-lookup"><span data-stu-id="e0fc1-150">IID</span></span><br/>                      | <span data-ttu-id="e0fc1-151">IID \_ IMsTscAx 定義為8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span><span class="sxs-lookup"><span data-stu-id="e0fc1-151">IID\_IMsTscAx is defined as 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="e0fc1-152">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e0fc1-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e0fc1-153">**IMsRdpClient**</span><span class="sxs-lookup"><span data-stu-id="e0fc1-153">**IMsRdpClient**</span></span>](imsrdpclient-interface.md)
</dt> <dt>

[<span data-ttu-id="e0fc1-154">**IMsRdpClient2**</span><span class="sxs-lookup"><span data-stu-id="e0fc1-154">**IMsRdpClient2**</span></span>](imsrdpclient2.md)
</dt> <dt>

[<span data-ttu-id="e0fc1-155">**IMsRdpClient3**</span><span class="sxs-lookup"><span data-stu-id="e0fc1-155">**IMsRdpClient3**</span></span>](imsrdpclient3.md)
</dt> <dt>

[<span data-ttu-id="e0fc1-156">**IMsRdpClient4**</span><span class="sxs-lookup"><span data-stu-id="e0fc1-156">**IMsRdpClient4**</span></span>](imsrdpclient4.md)
</dt> <dt>

[<span data-ttu-id="e0fc1-157">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="e0fc1-157">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="e0fc1-158">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="e0fc1-158">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="e0fc1-159">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="e0fc1-159">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="e0fc1-160">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="e0fc1-160">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="e0fc1-161">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="e0fc1-161">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="e0fc1-162">**IMsTscAx**</span><span class="sxs-lookup"><span data-stu-id="e0fc1-162">**IMsTscAx**</span></span>](imstscax-interface.md)
</dt> </dl>

 

 





