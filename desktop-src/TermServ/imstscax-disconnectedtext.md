---
title: IMsTscAx DisconnectedText 屬性
description: 指定在連接結束之前，顯示在控制項中央的文字。
ms.assetid: ec7efe7a-8fb9-4c45-8e16-78951365de13
ms.tgt_platform: multiple
keywords:
- DisconnectedText 屬性遠端桌面服務
- DisconnectedText 屬性遠端桌面服務，IMsTscAx 介面
- IMsTscAx 介面遠端桌面服務，DisconnectedText 屬性
- DisconnectedText 屬性遠端桌面服務，IMsRdpClient 介面
- IMsRdpClient 介面遠端桌面服務，DisconnectedText 屬性
- DisconnectedText 屬性遠端桌面服務，IMsRdpClient2 介面
- IMsRdpClient2 介面遠端桌面服務，DisconnectedText 屬性
- DisconnectedText 屬性遠端桌面服務，IMsRdpClient3 介面
- IMsRdpClient3 介面遠端桌面服務，DisconnectedText 屬性
- DisconnectedText 屬性遠端桌面服務，IMsRdpClient4 介面
- IMsRdpClient4 介面遠端桌面服務，DisconnectedText 屬性
- DisconnectedText 屬性遠端桌面服務，IMsRdpClient5 介面
- IMsRdpClient5 介面遠端桌面服務，DisconnectedText 屬性
- DisconnectedText 屬性遠端桌面服務，IMsRdpClient6 介面
- IMsRdpClient6 介面遠端桌面服務，DisconnectedText 屬性
- DisconnectedText 屬性遠端桌面服務，IMsRdpClient7 介面
- IMsRdpClient7 介面遠端桌面服務，DisconnectedText 屬性
- DisconnectedText 屬性遠端桌面服務，IMsRdpClient8 介面
- IMsRdpClient8 介面遠端桌面服務，DisconnectedText 屬性
- DisconnectedText 屬性遠端桌面服務，IMsRdpClient9 介面
- IMsRdpClient9 介面遠端桌面服務，DisconnectedText 屬性
topic_type:
- apiref
api_name:
- IMsTscAx.DisconnectedText
- IMsTscAx.get_DisconnectedText
- IMsTscAx.put_DisconnectedText
- IMsRdpClient.DisconnectedText
- IMsRdpClient.get_DisconnectedText
- IMsRdpClient.put_DisconnectedText
- IMsRdpClient2.DisconnectedText
- IMsRdpClient2.get_DisconnectedText
- IMsRdpClient2.put_DisconnectedText
- IMsRdpClient3.DisconnectedText
- IMsRdpClient3.get_DisconnectedText
- IMsRdpClient3.put_DisconnectedText
- IMsRdpClient4.DisconnectedText
- IMsRdpClient4.get_DisconnectedText
- IMsRdpClient4.put_DisconnectedText
- IMsRdpClient5.DisconnectedText
- IMsRdpClient5.get_DisconnectedText
- IMsRdpClient5.put_DisconnectedText
- IMsRdpClient6.DisconnectedText
- IMsRdpClient6.get_DisconnectedText
- IMsRdpClient6.put_DisconnectedText
- IMsRdpClient7.DisconnectedText
- IMsRdpClient7.get_DisconnectedText
- IMsRdpClient7.put_DisconnectedText
- IMsRdpClient8.DisconnectedText
- IMsRdpClient8.get_DisconnectedText
- IMsRdpClient8.put_DisconnectedText
- IMsRdpClient9.DisconnectedText
- IMsRdpClient9.get_DisconnectedText
- IMsRdpClient9.put_DisconnectedText
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4768e639cbfb1543e06c03f2d9e6566d0adb147e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686064"
---
# <a name="imstscaxdisconnectedtext-property"></a><span data-ttu-id="0d715-124">IMsTscAx：:D isconnectedText 屬性</span><span class="sxs-lookup"><span data-stu-id="0d715-124">IMsTscAx::DisconnectedText property</span></span>

<span data-ttu-id="0d715-125">指定在連接結束之前，顯示在控制項中央的文字。</span><span class="sxs-lookup"><span data-stu-id="0d715-125">Specifies the text that appears centered in the control before a connection is terminated.</span></span>

<span data-ttu-id="0d715-126">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="0d715-126">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="0d715-127">Syntax</span><span class="sxs-lookup"><span data-stu-id="0d715-127">Syntax</span></span>


```C++
HRESULT put_DisconnectedText(
  [in]  BSTR newVal
);

HRESULT get_DisconnectedText(
  [out] BSTR *pDisconnectedText
);
```



## <a name="property-value"></a><span data-ttu-id="0d715-128">屬性值</span><span class="sxs-lookup"><span data-stu-id="0d715-128">Property value</span></span>

<span data-ttu-id="0d715-129">新的顯示文字。</span><span class="sxs-lookup"><span data-stu-id="0d715-129">The new display text.</span></span>

## <a name="error-codes"></a><span data-ttu-id="0d715-130">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="0d715-130">Error codes</span></span>

<span data-ttu-id="0d715-131">如果成功，則傳回 **S \_ OK** 。</span><span class="sxs-lookup"><span data-stu-id="0d715-131">Return **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="0d715-132">備註</span><span class="sxs-lookup"><span data-stu-id="0d715-132">Remarks</span></span>

<span data-ttu-id="0d715-133">設定 **DisconnectedText** 屬性是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="0d715-133">Setting the **DisconnectedText** property is optional.</span></span> <span data-ttu-id="0d715-134">如果未指定，則在建立連接之前，控制項會顯示空白。</span><span class="sxs-lookup"><span data-stu-id="0d715-134">If it is not specified the control appears blank before a connection is established.</span></span>

<span data-ttu-id="0d715-135">只有當控制項不是處於連接狀態時，才能設定這個屬性。</span><span class="sxs-lookup"><span data-stu-id="0d715-135">This property can be set only if the control is not in the connected state.</span></span> <span data-ttu-id="0d715-136">如果在連接控制項之後呼叫這個方法，方法會傳回 **E \_ FAIL** 。</span><span class="sxs-lookup"><span data-stu-id="0d715-136">The method returns **E\_FAIL** if it is called after the control is connected.</span></span> <span data-ttu-id="0d715-137">您可以藉由回應 [**IMsTscAxEvents**](imstscaxevents-interface.md) 中的連接事件，或檢查 [**連接**](imstscax-connected.md) 的屬性來檢查控制項是否已連接。</span><span class="sxs-lookup"><span data-stu-id="0d715-137">You can check if the control is connected by responding to connection events in [**IMsTscAxEvents**](imstscaxevents-interface.md) or examining the [**Connected**](imstscax-connected.md) property.</span></span>

<span data-ttu-id="0d715-138">這個方法會配置 *pDisconnectedText* 參數所指向之緩衝區所需的記憶體。</span><span class="sxs-lookup"><span data-stu-id="0d715-138">This method allocates the memory required for the buffer pointed to by the *pDisconnectedText* parameter.</span></span> <span data-ttu-id="0d715-139">呼叫 C/c + + 應用程式時，必須透過呼叫 [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) 函式來釋放記憶體。</span><span class="sxs-lookup"><span data-stu-id="0d715-139">Calling C/C++ applications must free the memory with a call to the [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) function.</span></span> <span data-ttu-id="0d715-140">Visual Basic 和腳本用戶端都不需要這麼做。</span><span class="sxs-lookup"><span data-stu-id="0d715-140">This is not required for Visual Basic and scripting clients.</span></span>

<span data-ttu-id="0d715-141">如需遠端桌面網頁連線的詳細資訊，請參閱 [遠端桌面網頁連線的需求](requirements-for-remote-desktop-web-connection.md)。</span><span class="sxs-lookup"><span data-stu-id="0d715-141">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="0d715-142">規格需求</span><span class="sxs-lookup"><span data-stu-id="0d715-142">Requirements</span></span>



| <span data-ttu-id="0d715-143">需求</span><span class="sxs-lookup"><span data-stu-id="0d715-143">Requirement</span></span> | <span data-ttu-id="0d715-144">值</span><span class="sxs-lookup"><span data-stu-id="0d715-144">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0d715-145">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0d715-145">Minimum supported client</span></span><br/> | <span data-ttu-id="0d715-146">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0d715-146">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="0d715-147">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0d715-147">Minimum supported server</span></span><br/> | <span data-ttu-id="0d715-148">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0d715-148">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="0d715-149">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="0d715-149">Type library</span></span><br/>             | <dl> <span data-ttu-id="0d715-150"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0d715-150"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="0d715-151">DLL</span><span class="sxs-lookup"><span data-stu-id="0d715-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0d715-152"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0d715-152"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="0d715-153">IID</span><span class="sxs-lookup"><span data-stu-id="0d715-153">IID</span></span><br/>                      | <span data-ttu-id="0d715-154">IID \_ IMsTscAx 定義為8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span><span class="sxs-lookup"><span data-stu-id="0d715-154">IID\_IMsTscAx is defined as 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="0d715-155">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0d715-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d715-156">**IMsRdpClient**</span><span class="sxs-lookup"><span data-stu-id="0d715-156">**IMsRdpClient**</span></span>](imsrdpclient-interface.md)
</dt> <dt>

[<span data-ttu-id="0d715-157">**IMsRdpClient2**</span><span class="sxs-lookup"><span data-stu-id="0d715-157">**IMsRdpClient2**</span></span>](imsrdpclient2.md)
</dt> <dt>

[<span data-ttu-id="0d715-158">**IMsRdpClient3**</span><span class="sxs-lookup"><span data-stu-id="0d715-158">**IMsRdpClient3**</span></span>](imsrdpclient3.md)
</dt> <dt>

[<span data-ttu-id="0d715-159">**IMsRdpClient4**</span><span class="sxs-lookup"><span data-stu-id="0d715-159">**IMsRdpClient4**</span></span>](imsrdpclient4.md)
</dt> <dt>

[<span data-ttu-id="0d715-160">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="0d715-160">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="0d715-161">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="0d715-161">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="0d715-162">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="0d715-162">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="0d715-163">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="0d715-163">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="0d715-164">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="0d715-164">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="0d715-165">**IMsTscAx**</span><span class="sxs-lookup"><span data-stu-id="0d715-165">**IMsTscAx**</span></span>](imstscax-interface.md)
</dt> </dl>

 

