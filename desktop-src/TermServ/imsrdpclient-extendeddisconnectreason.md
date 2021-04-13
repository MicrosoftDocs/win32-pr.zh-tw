---
title: IMsRdpClient ExtendedDisconnectReason 屬性
description: 包含控制項中斷連接原因的延伸資訊。
ms.assetid: 5729992f-6695-44c0-8cf0-0d6b4cbddb62
ms.tgt_platform: multiple
keywords:
- ExtendedDisconnectReason 屬性遠端桌面服務
- ExtendedDisconnectReason 屬性遠端桌面服務，IMsRdpClient 介面
- IMsRdpClient 介面遠端桌面服務，ExtendedDisconnectReason 屬性
- ExtendedDisconnectReason 屬性遠端桌面服務，IMsRdpClient2 介面
- IMsRdpClient2 介面遠端桌面服務，ExtendedDisconnectReason 屬性
- ExtendedDisconnectReason 屬性遠端桌面服務，IMsRdpClient3 介面
- IMsRdpClient3 介面遠端桌面服務，ExtendedDisconnectReason 屬性
- ExtendedDisconnectReason 屬性遠端桌面服務，IMsRdpClient4 介面
- IMsRdpClient4 介面遠端桌面服務，ExtendedDisconnectReason 屬性
- ExtendedDisconnectReason 屬性遠端桌面服務，IMsRdpClient5 介面
- IMsRdpClient5 介面遠端桌面服務，ExtendedDisconnectReason 屬性
- ExtendedDisconnectReason 屬性遠端桌面服務，IMsRdpClient6 介面
- IMsRdpClient6 介面遠端桌面服務，ExtendedDisconnectReason 屬性
- ExtendedDisconnectReason 屬性遠端桌面服務，IMsRdpClient7 介面
- IMsRdpClient7 介面遠端桌面服務，ExtendedDisconnectReason 屬性
- ExtendedDisconnectReason 屬性遠端桌面服務，IMsRdpClient8 介面
- IMsRdpClient8 介面遠端桌面服務，ExtendedDisconnectReason 屬性
- ExtendedDisconnectReason 屬性遠端桌面服務，IMsRdpClient9 介面
- IMsRdpClient9 介面遠端桌面服務，ExtendedDisconnectReason 屬性
- ExtendedDisconnectReason 屬性遠端桌面服務，IMsRdpClient10 介面
- IMsRdpClient10 介面遠端桌面服務，ExtendedDisconnectReason 屬性
topic_type:
- apiref
api_name:
- IMsRdpClient.ExtendedDisconnectReason
- IMsRdpClient.get_ExtendedDisconnectReason
- IMsRdpClient2.ExtendedDisconnectReason
- IMsRdpClient2.get_ExtendedDisconnectReason
- IMsRdpClient3.ExtendedDisconnectReason
- IMsRdpClient3.get_ExtendedDisconnectReason
- IMsRdpClient4.ExtendedDisconnectReason
- IMsRdpClient4.get_ExtendedDisconnectReason
- IMsRdpClient5.ExtendedDisconnectReason
- IMsRdpClient5.get_ExtendedDisconnectReason
- IMsRdpClient6.ExtendedDisconnectReason
- IMsRdpClient6.get_ExtendedDisconnectReason
- IMsRdpClient7.ExtendedDisconnectReason
- IMsRdpClient7.get_ExtendedDisconnectReason
- IMsRdpClient8.ExtendedDisconnectReason
- IMsRdpClient8.get_ExtendedDisconnectReason
- IMsRdpClient9.ExtendedDisconnectReason
- IMsRdpClient9.get_ExtendedDisconnectReason
- IMsRdpClient10.ExtendedDisconnectReason
- IMsRdpClient10.get_ExtendedDisconnectReason
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b94c2612b231e24aaec855b6ebd1f9a0498b63c3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509283"
---
# <a name="imsrdpclientextendeddisconnectreason-property"></a><span data-ttu-id="851ff-124">IMsRdpClient：： ExtendedDisconnectReason 屬性</span><span class="sxs-lookup"><span data-stu-id="851ff-124">IMsRdpClient::ExtendedDisconnectReason property</span></span>

<span data-ttu-id="851ff-125">包含控制項中斷連接原因的延伸資訊。</span><span class="sxs-lookup"><span data-stu-id="851ff-125">Contains extended information about the control's reason for disconnection.</span></span>

<span data-ttu-id="851ff-126">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="851ff-126">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="851ff-127">語法</span><span class="sxs-lookup"><span data-stu-id="851ff-127">Syntax</span></span>


```C++
HRESULT get_ExtendedDisconnectReason(
  [out] ExtendedDisconnectReasonCode *pExtendedDisconnectReason
);
```



## <a name="property-value"></a><span data-ttu-id="851ff-128">屬性值</span><span class="sxs-lookup"><span data-stu-id="851ff-128">Property value</span></span>

<span data-ttu-id="851ff-129">[**ExtendedDisconnectReasonCode**](extendeddisconnectreasoncode.md)值的指標，指出用戶端中斷連接的原因。</span><span class="sxs-lookup"><span data-stu-id="851ff-129">Pointer to the [**ExtendedDisconnectReasonCode**](extendeddisconnectreasoncode.md) value indicating the reason for disconnection of the client.</span></span>

## <a name="error-codes"></a><span data-ttu-id="851ff-130">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="851ff-130">Error codes</span></span>

<span data-ttu-id="851ff-131">如果方法成功，則會傳回 **S \_ OK** 。</span><span class="sxs-lookup"><span data-stu-id="851ff-131">If the method succeeds, **S\_OK** is returned.</span></span> <span data-ttu-id="851ff-132">任何其他 **HRESULT** 值都表示呼叫失敗。</span><span class="sxs-lookup"><span data-stu-id="851ff-132">Any other **HRESULT** value indicates that the call failed.</span></span>

## <a name="remarks"></a><span data-ttu-id="851ff-133">備註</span><span class="sxs-lookup"><span data-stu-id="851ff-133">Remarks</span></span>

<span data-ttu-id="851ff-134">通常會在 [**IMsTscAxEvents：： OnDisconnected**](imstscaxevents-ondisconnected.md) 事件處理常式中呼叫這個方法，以取得有關中斷連接事件的其他資訊。</span><span class="sxs-lookup"><span data-stu-id="851ff-134">Typically this method is called in the [**IMsTscAxEvents::OnDisconnected**](imstscaxevents-ondisconnected.md) event handler to retrieve additional information about the disconnection event.</span></span>

<span data-ttu-id="851ff-135">如需遠端桌面網頁連線的詳細資訊，請參閱 [遠端桌面網頁連線的需求](requirements-for-remote-desktop-web-connection.md)。</span><span class="sxs-lookup"><span data-stu-id="851ff-135">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="851ff-136">規格需求</span><span class="sxs-lookup"><span data-stu-id="851ff-136">Requirements</span></span>



| <span data-ttu-id="851ff-137">需求</span><span class="sxs-lookup"><span data-stu-id="851ff-137">Requirement</span></span> | <span data-ttu-id="851ff-138">值</span><span class="sxs-lookup"><span data-stu-id="851ff-138">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="851ff-139">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="851ff-139">Minimum supported client</span></span><br/> | <span data-ttu-id="851ff-140">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="851ff-140">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="851ff-141">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="851ff-141">Minimum supported server</span></span><br/> | <span data-ttu-id="851ff-142">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="851ff-142">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="851ff-143">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="851ff-143">Type library</span></span><br/>             | <dl> <span data-ttu-id="851ff-144"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="851ff-144"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="851ff-145">DLL</span><span class="sxs-lookup"><span data-stu-id="851ff-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="851ff-146"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="851ff-146"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="851ff-147">IID</span><span class="sxs-lookup"><span data-stu-id="851ff-147">IID</span></span><br/>                      | <span data-ttu-id="851ff-148">IID \_ IMsRdpClient 定義為92b4a539-7115-4b7c-a5a9-e5d9efc2780a</span><span class="sxs-lookup"><span data-stu-id="851ff-148">IID\_IMsRdpClient is defined as 92b4a539-7115-4b7c-a5a9-e5d9efc2780a</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="851ff-149">另請參閱</span><span class="sxs-lookup"><span data-stu-id="851ff-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="851ff-150">**IMsRdpClient**</span><span class="sxs-lookup"><span data-stu-id="851ff-150">**IMsRdpClient**</span></span>](imsrdpclient-interface.md)
</dt> <dt>

[<span data-ttu-id="851ff-151">**IMsRdpClient2**</span><span class="sxs-lookup"><span data-stu-id="851ff-151">**IMsRdpClient2**</span></span>](imsrdpclient2.md)
</dt> <dt>

[<span data-ttu-id="851ff-152">**IMsRdpClient3**</span><span class="sxs-lookup"><span data-stu-id="851ff-152">**IMsRdpClient3**</span></span>](imsrdpclient3.md)
</dt> <dt>

[<span data-ttu-id="851ff-153">**IMsRdpClient4**</span><span class="sxs-lookup"><span data-stu-id="851ff-153">**IMsRdpClient4**</span></span>](imsrdpclient4.md)
</dt> <dt>

[<span data-ttu-id="851ff-154">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="851ff-154">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="851ff-155">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="851ff-155">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="851ff-156">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="851ff-156">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="851ff-157">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="851ff-157">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="851ff-158">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="851ff-158">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="851ff-159">**IMsRdpClient10**</span><span class="sxs-lookup"><span data-stu-id="851ff-159">**IMsRdpClient10**</span></span>](imsrdpclient10.md)
</dt> <dt>

[<span data-ttu-id="851ff-160">**IMsTscAxEvents::OnDisconnected**</span><span class="sxs-lookup"><span data-stu-id="851ff-160">**IMsTscAxEvents::OnDisconnected**</span></span>](imstscaxevents-ondisconnected.md)
</dt> </dl>

 

 





