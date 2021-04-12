---
title: IMsTscAx ConnectingText 屬性
description: 指定控制項連接時，顯示在控制項中央的文字。
ms.assetid: 9bc82074-988f-491b-80e3-00c3f7ba437a
ms.tgt_platform: multiple
keywords:
- ConnectingText 屬性遠端桌面服務
- ConnectingText 屬性遠端桌面服務，IMsTscAx 介面
- IMsTscAx 介面遠端桌面服務，ConnectingText 屬性
- ConnectingText 屬性遠端桌面服務，IMsRdpClient 介面
- IMsRdpClient 介面遠端桌面服務，ConnectingText 屬性
- ConnectingText 屬性遠端桌面服務，IMsRdpClient2 介面
- IMsRdpClient2 介面遠端桌面服務，ConnectingText 屬性
- ConnectingText 屬性遠端桌面服務，IMsRdpClient3 介面
- IMsRdpClient3 介面遠端桌面服務，ConnectingText 屬性
- ConnectingText 屬性遠端桌面服務，IMsRdpClient4 介面
- IMsRdpClient4 介面遠端桌面服務，ConnectingText 屬性
- ConnectingText 屬性遠端桌面服務，IMsRdpClient5 介面
- IMsRdpClient5 介面遠端桌面服務，ConnectingText 屬性
- ConnectingText 屬性遠端桌面服務，IMsRdpClient6 介面
- IMsRdpClient6 介面遠端桌面服務，ConnectingText 屬性
- ConnectingText 屬性遠端桌面服務，IMsRdpClient7 介面
- IMsRdpClient7 介面遠端桌面服務，ConnectingText 屬性
- ConnectingText 屬性遠端桌面服務，IMsRdpClient8 介面
- IMsRdpClient8 介面遠端桌面服務，ConnectingText 屬性
- ConnectingText 屬性遠端桌面服務，IMsRdpClient9 介面
- IMsRdpClient9 介面遠端桌面服務，ConnectingText 屬性
topic_type:
- apiref
api_name:
- IMsTscAx.ConnectingText
- IMsTscAx.get_ConnectingText
- IMsTscAx.put_ConnectingText
- IMsRdpClient.ConnectingText
- IMsRdpClient.get_ConnectingText
- IMsRdpClient.put_ConnectingText
- IMsRdpClient2.ConnectingText
- IMsRdpClient2.get_ConnectingText
- IMsRdpClient2.put_ConnectingText
- IMsRdpClient3.ConnectingText
- IMsRdpClient3.get_ConnectingText
- IMsRdpClient3.put_ConnectingText
- IMsRdpClient4.ConnectingText
- IMsRdpClient4.get_ConnectingText
- IMsRdpClient4.put_ConnectingText
- IMsRdpClient5.ConnectingText
- IMsRdpClient5.get_ConnectingText
- IMsRdpClient5.put_ConnectingText
- IMsRdpClient6.ConnectingText
- IMsRdpClient6.get_ConnectingText
- IMsRdpClient6.put_ConnectingText
- IMsRdpClient7.ConnectingText
- IMsRdpClient7.get_ConnectingText
- IMsRdpClient7.put_ConnectingText
- IMsRdpClient8.ConnectingText
- IMsRdpClient8.get_ConnectingText
- IMsRdpClient8.put_ConnectingText
- IMsRdpClient9.ConnectingText
- IMsRdpClient9.get_ConnectingText
- IMsRdpClient9.put_ConnectingText
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 433da7d159f1fe5bf44114a0b76ed9b4d807046f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384981"
---
# <a name="imstscaxconnectingtext-property"></a><span data-ttu-id="5a293-124">IMsTscAx：： ConnectingText 屬性</span><span class="sxs-lookup"><span data-stu-id="5a293-124">IMsTscAx::ConnectingText property</span></span>

<span data-ttu-id="5a293-125">指定控制項連接時，顯示在控制項中央的文字。</span><span class="sxs-lookup"><span data-stu-id="5a293-125">Specifies the text that appears centered in the control while the control is connecting.</span></span>

<span data-ttu-id="5a293-126">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="5a293-126">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="5a293-127">Syntax</span><span class="sxs-lookup"><span data-stu-id="5a293-127">Syntax</span></span>


```C++
HRESULT put_ConnectingText(
  [in]  BSTR newVal
);

HRESULT get_ConnectingText(
  [out] BSTR *pConnectingText
);
```



## <a name="property-value"></a><span data-ttu-id="5a293-128">屬性值</span><span class="sxs-lookup"><span data-stu-id="5a293-128">Property value</span></span>

<span data-ttu-id="5a293-129">新的顯示文字。</span><span class="sxs-lookup"><span data-stu-id="5a293-129">The new display text.</span></span>

## <a name="error-codes"></a><span data-ttu-id="5a293-130">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="5a293-130">Error codes</span></span>

<span data-ttu-id="5a293-131">如果成功，則傳回 **S \_ OK** 。</span><span class="sxs-lookup"><span data-stu-id="5a293-131">Return **S\_OK** if successful.</span></span>

<span data-ttu-id="5a293-132">如果發生錯誤，則傳回非零的 **HRESULT** 。</span><span class="sxs-lookup"><span data-stu-id="5a293-132">Return a nonzero **HRESULT** if an error occurs.</span></span>

## <a name="remarks"></a><span data-ttu-id="5a293-133">備註</span><span class="sxs-lookup"><span data-stu-id="5a293-133">Remarks</span></span>

<span data-ttu-id="5a293-134">連接文字的範例是「正在連接到伺服器 ...」。</span><span class="sxs-lookup"><span data-stu-id="5a293-134">An example of connection text is "Connecting to server ...".</span></span>

<span data-ttu-id="5a293-135">設定 **ConnectingText** 屬性是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="5a293-135">Setting the **ConnectingText** property is optional.</span></span> <span data-ttu-id="5a293-136">如果未設定，則在建立連接之前，控制項會顯示空白。</span><span class="sxs-lookup"><span data-stu-id="5a293-136">If it is not set, the control appears blank before a connection is established.</span></span>

<span data-ttu-id="5a293-137">只有當控制項不是處於連接狀態時，才能設定這個屬性。</span><span class="sxs-lookup"><span data-stu-id="5a293-137">This property can be set only if the control is not in the connected state.</span></span> <span data-ttu-id="5a293-138">如果在連接控制項時呼叫它，它會傳回 **E \_ FAIL** 。</span><span class="sxs-lookup"><span data-stu-id="5a293-138">It returns **E\_FAIL** if it is called when the control is connected.</span></span> <span data-ttu-id="5a293-139">您可以藉由回應 [**IMsTscAxEvents**](imstscaxevents-interface.md) 中的連接事件，或檢查 [**連接**](imstscax-connected.md) 的屬性來檢查控制項是否已連接。</span><span class="sxs-lookup"><span data-stu-id="5a293-139">You can check if the control is connected by responding to connection events in [**IMsTscAxEvents**](imstscaxevents-interface.md) or examining the [**Connected**](imstscax-connected.md) property.</span></span>

<span data-ttu-id="5a293-140">**Get \_ ConnectingText** 屬性方法會配置 *pConnectingText* 參數所指向之緩衝區所需的記憶體。</span><span class="sxs-lookup"><span data-stu-id="5a293-140">The **get\_ConnectingText** property method allocates the memory required for the buffer pointed to by the *pConnectingText* parameter.</span></span> <span data-ttu-id="5a293-141">呼叫 C/c + + 應用程式時，必須透過呼叫 [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) 函式來釋放記憶體。</span><span class="sxs-lookup"><span data-stu-id="5a293-141">Calling C/C++ applications must free the memory with a call to the [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) function.</span></span> <span data-ttu-id="5a293-142">Visual Basic 和腳本用戶端都不需要這麼做。</span><span class="sxs-lookup"><span data-stu-id="5a293-142">This is not required for Visual Basic and scripting clients.</span></span>

<span data-ttu-id="5a293-143">如需遠端桌面網頁連線的詳細資訊，請參閱 [遠端桌面網頁連線的需求](requirements-for-remote-desktop-web-connection.md)。</span><span class="sxs-lookup"><span data-stu-id="5a293-143">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="5a293-144">規格需求</span><span class="sxs-lookup"><span data-stu-id="5a293-144">Requirements</span></span>



| <span data-ttu-id="5a293-145">需求</span><span class="sxs-lookup"><span data-stu-id="5a293-145">Requirement</span></span> | <span data-ttu-id="5a293-146">值</span><span class="sxs-lookup"><span data-stu-id="5a293-146">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5a293-147">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5a293-147">Minimum supported client</span></span><br/> | <span data-ttu-id="5a293-148">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5a293-148">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="5a293-149">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5a293-149">Minimum supported server</span></span><br/> | <span data-ttu-id="5a293-150">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5a293-150">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="5a293-151">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="5a293-151">Type library</span></span><br/>             | <dl> <span data-ttu-id="5a293-152"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5a293-152"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="5a293-153">DLL</span><span class="sxs-lookup"><span data-stu-id="5a293-153">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5a293-154"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5a293-154"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="5a293-155">IID</span><span class="sxs-lookup"><span data-stu-id="5a293-155">IID</span></span><br/>                      | <span data-ttu-id="5a293-156">IID \_ IMsTscAx 定義為8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span><span class="sxs-lookup"><span data-stu-id="5a293-156">IID\_IMsTscAx is defined as 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="5a293-157">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5a293-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5a293-158">**IMsRdpClient**</span><span class="sxs-lookup"><span data-stu-id="5a293-158">**IMsRdpClient**</span></span>](imsrdpclient-interface.md)
</dt> <dt>

[<span data-ttu-id="5a293-159">**IMsRdpClient2**</span><span class="sxs-lookup"><span data-stu-id="5a293-159">**IMsRdpClient2**</span></span>](imsrdpclient2.md)
</dt> <dt>

[<span data-ttu-id="5a293-160">**IMsRdpClient3**</span><span class="sxs-lookup"><span data-stu-id="5a293-160">**IMsRdpClient3**</span></span>](imsrdpclient3.md)
</dt> <dt>

[<span data-ttu-id="5a293-161">**IMsRdpClient4**</span><span class="sxs-lookup"><span data-stu-id="5a293-161">**IMsRdpClient4**</span></span>](imsrdpclient4.md)
</dt> <dt>

[<span data-ttu-id="5a293-162">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="5a293-162">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="5a293-163">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="5a293-163">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="5a293-164">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="5a293-164">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="5a293-165">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="5a293-165">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="5a293-166">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="5a293-166">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="5a293-167">**IMsTscAx**</span><span class="sxs-lookup"><span data-stu-id="5a293-167">**IMsTscAx**</span></span>](imstscax-interface.md)
</dt> </dl>

 

