---
title: IMsRdpClient 全螢幕屬性
description: 判斷用戶端控制項是否處於全螢幕模式。
ms.assetid: 64fe2835-c00e-4d21-812d-dcf160147d93
ms.tgt_platform: multiple
keywords:
- 全螢幕屬性遠端桌面服務
- 全螢幕屬性遠端桌面服務、IMsRdpClient 介面
- IMsRdpClient 介面遠端桌面服務、全螢幕屬性
- 全螢幕屬性遠端桌面服務、IMsRdpClient2 介面
- IMsRdpClient2 介面遠端桌面服務、全螢幕屬性
- 全螢幕屬性遠端桌面服務、IMsRdpClient3 介面
- IMsRdpClient3 介面遠端桌面服務、全螢幕屬性
- 全螢幕屬性遠端桌面服務、IMsRdpClient4 介面
- IMsRdpClient4 介面遠端桌面服務、全螢幕屬性
- 全螢幕屬性遠端桌面服務、IMsRdpClient5 介面
- IMsRdpClient5 介面遠端桌面服務、全螢幕屬性
- 全螢幕屬性遠端桌面服務、IMsRdpClient6 介面
- IMsRdpClient6 介面遠端桌面服務、全螢幕屬性
- 全螢幕屬性遠端桌面服務、IMsRdpClient7 介面
- IMsRdpClient7 介面遠端桌面服務、全螢幕屬性
- 全螢幕屬性遠端桌面服務、IMsRdpClient8 介面
- IMsRdpClient8 介面遠端桌面服務、全螢幕屬性
- 全螢幕屬性遠端桌面服務、IMsRdpClient9 介面
- IMsRdpClient9 介面遠端桌面服務、全螢幕屬性
- 全螢幕屬性遠端桌面服務、IMsRdpClient10 介面
- IMsRdpClient10 介面遠端桌面服務、全螢幕屬性
topic_type:
- apiref
api_name:
- IMsRdpClient.FullScreen
- IMsRdpClient.get_FullScreen
- IMsRdpClient.put_FullScreen
- IMsRdpClient2.FullScreen
- IMsRdpClient2.get_FullScreen
- IMsRdpClient2.put_FullScreen
- IMsRdpClient3.FullScreen
- IMsRdpClient3.get_FullScreen
- IMsRdpClient3.put_FullScreen
- IMsRdpClient4.FullScreen
- IMsRdpClient4.get_FullScreen
- IMsRdpClient4.put_FullScreen
- IMsRdpClient5.FullScreen
- IMsRdpClient5.get_FullScreen
- IMsRdpClient5.put_FullScreen
- IMsRdpClient6.FullScreen
- IMsRdpClient6.get_FullScreen
- IMsRdpClient6.put_FullScreen
- IMsRdpClient7.FullScreen
- IMsRdpClient7.get_FullScreen
- IMsRdpClient7.put_FullScreen
- IMsRdpClient8.FullScreen
- IMsRdpClient8.get_FullScreen
- IMsRdpClient8.put_FullScreen
- IMsRdpClient9.FullScreen
- IMsRdpClient9.get_FullScreen
- IMsRdpClient9.put_FullScreen
- IMsRdpClient10.FullScreen
- IMsRdpClient10.get_FullScreen
- IMsRdpClient10.put_FullScreen
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1adbc8e11d2cc4fb4a8071372777a01d81b5edad
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105875"
---
# <a name="imsrdpclientfullscreen-property"></a><span data-ttu-id="da52f-124">IMsRdpClient：：全螢幕屬性</span><span class="sxs-lookup"><span data-stu-id="da52f-124">IMsRdpClient::FullScreen property</span></span>

<span data-ttu-id="da52f-125">判斷用戶端控制項是否處於全螢幕模式。</span><span class="sxs-lookup"><span data-stu-id="da52f-125">Determines whether the client control is in full-screen mode.</span></span>

<span data-ttu-id="da52f-126">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="da52f-126">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="da52f-127">Syntax</span><span class="sxs-lookup"><span data-stu-id="da52f-127">Syntax</span></span>


```C++
HRESULT put_FullScreen(
  [in]  VARIANT_BOOL fFullScreen
);

HRESULT get_FullScreen(
  [out] VARIANT_BOOL *pfFullScreen
);
```



## <a name="property-value"></a><span data-ttu-id="da52f-128">屬性值</span><span class="sxs-lookup"><span data-stu-id="da52f-128">Property value</span></span>

<span data-ttu-id="da52f-129">**True** 表示輸入全螢幕模式， **False** 則會離開全螢幕模式並返回視窗模式。</span><span class="sxs-lookup"><span data-stu-id="da52f-129">**True** to enter full-screen mode, **False** to leave full-screen mode and return to window mode.</span></span>

## <a name="error-codes"></a><span data-ttu-id="da52f-130">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="da52f-130">Error codes</span></span>

<span data-ttu-id="da52f-131">如果方法成功，則會傳回 **S \_ OK** 。</span><span class="sxs-lookup"><span data-stu-id="da52f-131">If the methods succeed, **S\_OK** is returned.</span></span> <span data-ttu-id="da52f-132">任何其他 **HRESULT** 值都表示呼叫失敗。</span><span class="sxs-lookup"><span data-stu-id="da52f-132">Any other **HRESULT** value indicates that the call failed.</span></span>

## <a name="remarks"></a><span data-ttu-id="da52f-133">備註</span><span class="sxs-lookup"><span data-stu-id="da52f-133">Remarks</span></span>

<span data-ttu-id="da52f-134">連接控制項時，您可以設定這個屬性。</span><span class="sxs-lookup"><span data-stu-id="da52f-134">You can set this property when the control is connected.</span></span>

<span data-ttu-id="da52f-135">您必須先呼叫 [**IMsRdpClientNonScriptable3：:p 的 \_ ConnectionBarText**](imsrdpclientnonscriptable3-connectionbartext.md) 方法，然後再呼叫 [**IMsTscSecuredSettings：:p 的 \_ 全像全螢幕**](imstscsecuredsettings-fullscreen.md) 方法或 **IMsRdpClient：:p 的 ui \_ 全螢幕** 方式。</span><span class="sxs-lookup"><span data-stu-id="da52f-135">You must call the [**IMsRdpClientNonScriptable3::put\_ConnectionBarText**](imsrdpclientnonscriptable3-connectionbartext.md) method before you call the [**IMsTscSecuredSettings::put\_Fullscreen**](imstscsecuredsettings-fullscreen.md) method or the **IMsRdpClient::put\_Fullscreen** method.</span></span>

<span data-ttu-id="da52f-136">如需遠端桌面網頁連線的詳細資訊，請參閱 [遠端桌面網頁連線的需求](requirements-for-remote-desktop-web-connection.md)。</span><span class="sxs-lookup"><span data-stu-id="da52f-136">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="da52f-137">規格需求</span><span class="sxs-lookup"><span data-stu-id="da52f-137">Requirements</span></span>



| <span data-ttu-id="da52f-138">需求</span><span class="sxs-lookup"><span data-stu-id="da52f-138">Requirement</span></span> | <span data-ttu-id="da52f-139">值</span><span class="sxs-lookup"><span data-stu-id="da52f-139">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="da52f-140">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="da52f-140">Minimum supported client</span></span><br/> | <span data-ttu-id="da52f-141">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="da52f-141">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="da52f-142">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="da52f-142">Minimum supported server</span></span><br/> | <span data-ttu-id="da52f-143">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="da52f-143">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="da52f-144">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="da52f-144">Type library</span></span><br/>             | <dl> <span data-ttu-id="da52f-145"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="da52f-145"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="da52f-146">DLL</span><span class="sxs-lookup"><span data-stu-id="da52f-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="da52f-147"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="da52f-147"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="da52f-148">IID</span><span class="sxs-lookup"><span data-stu-id="da52f-148">IID</span></span><br/>                      | <span data-ttu-id="da52f-149">IID \_ IMsRdpClient 定義為92b4a539-7115-4b7c-a5a9-e5d9efc2780a</span><span class="sxs-lookup"><span data-stu-id="da52f-149">IID\_IMsRdpClient is defined as 92b4a539-7115-4b7c-a5a9-e5d9efc2780a</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="da52f-150">另請參閱</span><span class="sxs-lookup"><span data-stu-id="da52f-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="da52f-151">**IMsRdpClient**</span><span class="sxs-lookup"><span data-stu-id="da52f-151">**IMsRdpClient**</span></span>](imsrdpclient-interface.md)
</dt> <dt>

[<span data-ttu-id="da52f-152">**IMsRdpClient2**</span><span class="sxs-lookup"><span data-stu-id="da52f-152">**IMsRdpClient2**</span></span>](imsrdpclient2.md)
</dt> <dt>

[<span data-ttu-id="da52f-153">**IMsRdpClient3**</span><span class="sxs-lookup"><span data-stu-id="da52f-153">**IMsRdpClient3**</span></span>](imsrdpclient3.md)
</dt> <dt>

[<span data-ttu-id="da52f-154">**IMsRdpClient4**</span><span class="sxs-lookup"><span data-stu-id="da52f-154">**IMsRdpClient4**</span></span>](imsrdpclient4.md)
</dt> <dt>

[<span data-ttu-id="da52f-155">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="da52f-155">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="da52f-156">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="da52f-156">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="da52f-157">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="da52f-157">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="da52f-158">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="da52f-158">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="da52f-159">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="da52f-159">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="da52f-160">**IMsRdpClient10**</span><span class="sxs-lookup"><span data-stu-id="da52f-160">**IMsRdpClient10**</span></span>](imsrdpclient10.md)
</dt> </dl>

 

 





