---
title: 'IMsTscAx 連接屬性 (Tsvirtualchannels .h) '
description: 抓取目前控制項的連接狀態。
ms.assetid: f6f65ef6-d321-4362-b192-1ea5ffd2b712
ms.tgt_platform: multiple
keywords:
- 連接的屬性遠端桌面服務
- 連接屬性遠端桌面服務，IMsTscAx 介面
- IMsTscAx 介面遠端桌面服務，連接屬性
- 連接屬性遠端桌面服務，IMsRdpClient 介面
- IMsRdpClient 介面遠端桌面服務，連接屬性
- 連接屬性遠端桌面服務，IMsRdpClient2 介面
- IMsRdpClient2 介面遠端桌面服務，連接屬性
- 連接屬性遠端桌面服務，IMsRdpClient3 介面
- IMsRdpClient3 介面遠端桌面服務，連接屬性
- 連接屬性遠端桌面服務，IMsRdpClient4 介面
- IMsRdpClient4 介面遠端桌面服務，連接屬性
- 連接屬性遠端桌面服務，IMsRdpClient5 介面
- IMsRdpClient5 介面遠端桌面服務，連接屬性
- 連接屬性遠端桌面服務，IMsRdpClient6 介面
- IMsRdpClient6 介面遠端桌面服務，連接屬性
- 連接屬性遠端桌面服務，IMsRdpClient7 介面
- IMsRdpClient7 介面遠端桌面服務，連接屬性
- 連接屬性遠端桌面服務，IMsRdpClient8 介面
- IMsRdpClient8 介面遠端桌面服務，連接屬性
- 連接屬性遠端桌面服務，IMsRdpClient9 介面
- IMsRdpClient9 介面遠端桌面服務，連接屬性
topic_type:
- apiref
api_name:
- IMsTscAx.Connected
- IMsTscAx.get_Connected
- IMsRdpClient.Connected
- IMsRdpClient.get_Connected
- IMsRdpClient2.Connected
- IMsRdpClient2.get_Connected
- IMsRdpClient3.Connected
- IMsRdpClient3.get_Connected
- IMsRdpClient4.Connected
- IMsRdpClient4.get_Connected
- IMsRdpClient5.Connected
- IMsRdpClient5.get_Connected
- IMsRdpClient6.Connected
- IMsRdpClient6.get_Connected
- IMsRdpClient7.Connected
- IMsRdpClient7.get_Connected
- IMsRdpClient8.Connected
- IMsRdpClient8.get_Connected
- IMsRdpClient9.Connected
- IMsRdpClient9.get_Connected
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 883ba670ab9a6b5d4e4a065c35f263734929ba02
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106969218"
---
# <a name="imstscaxconnected-property"></a><span data-ttu-id="fda85-124">IMsTscAx：： Connected 屬性</span><span class="sxs-lookup"><span data-stu-id="fda85-124">IMsTscAx::Connected property</span></span>

<span data-ttu-id="fda85-125">抓取目前控制項的連接狀態。</span><span class="sxs-lookup"><span data-stu-id="fda85-125">Retrieves the connection state of the current control.</span></span>

<span data-ttu-id="fda85-126">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="fda85-126">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="fda85-127">語法</span><span class="sxs-lookup"><span data-stu-id="fda85-127">Syntax</span></span>


```C++
HRESULT get_Connected(
  [out] short *pIsConnected
);
```



## <a name="property-value"></a><span data-ttu-id="fda85-128">屬性值</span><span class="sxs-lookup"><span data-stu-id="fda85-128">Property value</span></span>

<span data-ttu-id="fda85-129">指出控制項的連接狀態。</span><span class="sxs-lookup"><span data-stu-id="fda85-129">Indicates the connection state of the control.</span></span> <span data-ttu-id="fda85-130">這可以是下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="fda85-130">This can be one of the following values.</span></span>

<dt>

<span data-ttu-id="fda85-131">0</span><span class="sxs-lookup"><span data-stu-id="fda85-131">0</span></span>
</dt> <dd>

<span data-ttu-id="fda85-132">控制項未連接。</span><span class="sxs-lookup"><span data-stu-id="fda85-132">The control is not connected.</span></span>

</dd> <dt>

<span data-ttu-id="fda85-133">1</span><span class="sxs-lookup"><span data-stu-id="fda85-133">1</span></span>
</dt> <dd>

<span data-ttu-id="fda85-134">控制項已連接。</span><span class="sxs-lookup"><span data-stu-id="fda85-134">The control is connected.</span></span>

</dd> <dt>

<span data-ttu-id="fda85-135">2</span><span class="sxs-lookup"><span data-stu-id="fda85-135">2</span></span>
</dt> <dd>

<span data-ttu-id="fda85-136">控制項正在建立連接。</span><span class="sxs-lookup"><span data-stu-id="fda85-136">The control is establishing a connection.</span></span>

</dd> </dl>

## <a name="error-codes"></a><span data-ttu-id="fda85-137">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="fda85-137">Error codes</span></span>

<span data-ttu-id="fda85-138">如果成功，則傳回 **S \_ OK** 。</span><span class="sxs-lookup"><span data-stu-id="fda85-138">Return **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="fda85-139">備註</span><span class="sxs-lookup"><span data-stu-id="fda85-139">Remarks</span></span>

<span data-ttu-id="fda85-140">判斷控制項連接狀態的慣用方式是回應 [**IMsTscAxEvents**](imstscaxevents-interface.md)中的連接事件。</span><span class="sxs-lookup"><span data-stu-id="fda85-140">The preferred way to determine the control's connection state is to respond to the connection events in [**IMsTscAxEvents**](imstscaxevents-interface.md).</span></span>

<span data-ttu-id="fda85-141">如需遠端桌面網頁連線的詳細資訊，請參閱 [遠端桌面網頁連線的需求](requirements-for-remote-desktop-web-connection.md)。</span><span class="sxs-lookup"><span data-stu-id="fda85-141">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="fda85-142">規格需求</span><span class="sxs-lookup"><span data-stu-id="fda85-142">Requirements</span></span>



| <span data-ttu-id="fda85-143">需求</span><span class="sxs-lookup"><span data-stu-id="fda85-143">Requirement</span></span> | <span data-ttu-id="fda85-144">值</span><span class="sxs-lookup"><span data-stu-id="fda85-144">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fda85-145">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="fda85-145">Minimum supported client</span></span><br/> | <span data-ttu-id="fda85-146">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="fda85-146">Windows Vista</span></span><br/>                                                                       |
| <span data-ttu-id="fda85-147">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="fda85-147">Minimum supported server</span></span><br/> | <span data-ttu-id="fda85-148">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fda85-148">Windows Server 2008</span></span><br/>                                                                 |
| <span data-ttu-id="fda85-149">標頭</span><span class="sxs-lookup"><span data-stu-id="fda85-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="fda85-150"><dt>Tsvirtualchannels。h</dt></span><span class="sxs-lookup"><span data-stu-id="fda85-150"><dt>Tsvirtualchannels.h</dt></span></span> </dl> |
| <span data-ttu-id="fda85-151">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="fda85-151">Type library</span></span><br/>             | <dl> <span data-ttu-id="fda85-152"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fda85-152"><dt>MsTscAx.dll</dt></span></span> </dl>         |
| <span data-ttu-id="fda85-153">DLL</span><span class="sxs-lookup"><span data-stu-id="fda85-153">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fda85-154"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fda85-154"><dt>MsTscAx.dll</dt></span></span> </dl>         |
| <span data-ttu-id="fda85-155">IID</span><span class="sxs-lookup"><span data-stu-id="fda85-155">IID</span></span><br/>                      | <span data-ttu-id="fda85-156">IID \_ IMsTscAx 定義為8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span><span class="sxs-lookup"><span data-stu-id="fda85-156">IID\_IMsTscAx is defined as 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span></span><br/>                    |



## <a name="see-also"></a><span data-ttu-id="fda85-157">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fda85-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fda85-158">**IMsRdpClient**</span><span class="sxs-lookup"><span data-stu-id="fda85-158">**IMsRdpClient**</span></span>](imsrdpclient-interface.md)
</dt> <dt>

[<span data-ttu-id="fda85-159">**IMsRdpClient2**</span><span class="sxs-lookup"><span data-stu-id="fda85-159">**IMsRdpClient2**</span></span>](imsrdpclient2.md)
</dt> <dt>

[<span data-ttu-id="fda85-160">**IMsRdpClient3**</span><span class="sxs-lookup"><span data-stu-id="fda85-160">**IMsRdpClient3**</span></span>](imsrdpclient3.md)
</dt> <dt>

[<span data-ttu-id="fda85-161">**IMsRdpClient4**</span><span class="sxs-lookup"><span data-stu-id="fda85-161">**IMsRdpClient4**</span></span>](imsrdpclient4.md)
</dt> <dt>

[<span data-ttu-id="fda85-162">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="fda85-162">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="fda85-163">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="fda85-163">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="fda85-164">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="fda85-164">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="fda85-165">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="fda85-165">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="fda85-166">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="fda85-166">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="fda85-167">**IMsTscAx**</span><span class="sxs-lookup"><span data-stu-id="fda85-167">**IMsTscAx**</span></span>](imstscax-interface.md)
</dt> </dl>

 

 





