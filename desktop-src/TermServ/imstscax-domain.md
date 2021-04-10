---
title: IMsTscAx 網域屬性
description: 指定目前使用者登入的網域。
ms.assetid: 5d9a2048-5f5d-43ca-a8b8-400dac7d7472
ms.tgt_platform: multiple
keywords:
- 網域屬性遠端桌面服務
- 網域屬性遠端桌面服務、IMsTscAx 介面
- IMsTscAx 介面遠端桌面服務，網域屬性
- 網域屬性遠端桌面服務、IMsRdpClient 介面
- IMsRdpClient 介面遠端桌面服務，網域屬性
- 網域屬性遠端桌面服務、IMsRdpClient2 介面
- IMsRdpClient2 介面遠端桌面服務，網域屬性
- 網域屬性遠端桌面服務、IMsRdpClient3 介面
- IMsRdpClient3 介面遠端桌面服務，網域屬性
- 網域屬性遠端桌面服務、IMsRdpClient4 介面
- IMsRdpClient4 介面遠端桌面服務，網域屬性
- 網域屬性遠端桌面服務、IMsRdpClient5 介面
- IMsRdpClient5 介面遠端桌面服務，網域屬性
- 網域屬性遠端桌面服務、IMsRdpClient6 介面
- IMsRdpClient6 介面遠端桌面服務，網域屬性
- 網域屬性遠端桌面服務、IMsRdpClient7 介面
- IMsRdpClient7 介面遠端桌面服務，網域屬性
- 網域屬性遠端桌面服務、IMsRdpClient8 介面
- IMsRdpClient8 介面遠端桌面服務，網域屬性
- 網域屬性遠端桌面服務、IMsRdpClient9 介面
- IMsRdpClient9 介面遠端桌面服務，網域屬性
topic_type:
- apiref
api_name:
- IMsTscAx.Domain
- IMsTscAx.get_Domain
- IMsTscAx.put_Domain
- IMsRdpClient.Domain
- IMsRdpClient.get_Domain
- IMsRdpClient.put_Domain
- IMsRdpClient2.Domain
- IMsRdpClient2.get_Domain
- IMsRdpClient2.put_Domain
- IMsRdpClient3.Domain
- IMsRdpClient3.get_Domain
- IMsRdpClient3.put_Domain
- IMsRdpClient4.Domain
- IMsRdpClient4.get_Domain
- IMsRdpClient4.put_Domain
- IMsRdpClient5.Domain
- IMsRdpClient5.get_Domain
- IMsRdpClient5.put_Domain
- IMsRdpClient6.Domain
- IMsRdpClient6.get_Domain
- IMsRdpClient6.put_Domain
- IMsRdpClient7.Domain
- IMsRdpClient7.get_Domain
- IMsRdpClient7.put_Domain
- IMsRdpClient8.Domain
- IMsRdpClient8.get_Domain
- IMsRdpClient8.put_Domain
- IMsRdpClient9.Domain
- IMsRdpClient9.get_Domain
- IMsRdpClient9.put_Domain
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: faf95c02de10fe8db38a53b75d4d20cf796020f8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934971"
---
# <a name="imstscaxdomain-property"></a><span data-ttu-id="ae4fb-124">IMsTscAx：:D omain 屬性</span><span class="sxs-lookup"><span data-stu-id="ae4fb-124">IMsTscAx::Domain property</span></span>

<span data-ttu-id="ae4fb-125">指定目前使用者登入的網域。</span><span class="sxs-lookup"><span data-stu-id="ae4fb-125">Specifies the domain to which the current user logs on.</span></span>

<span data-ttu-id="ae4fb-126">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="ae4fb-126">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="ae4fb-127">Syntax</span><span class="sxs-lookup"><span data-stu-id="ae4fb-127">Syntax</span></span>


```C++
HRESULT put_Domain(
  [in]  BSTR newVal
);

HRESULT get_Domain(
  [out] BSTR *pDomain
);
```



## <a name="property-value"></a><span data-ttu-id="ae4fb-128">屬性值</span><span class="sxs-lookup"><span data-stu-id="ae4fb-128">Property value</span></span>

<span data-ttu-id="ae4fb-129">新的功能變數名稱。</span><span class="sxs-lookup"><span data-stu-id="ae4fb-129">The new domain name.</span></span>

## <a name="error-codes"></a><span data-ttu-id="ae4fb-130">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="ae4fb-130">Error codes</span></span>

<span data-ttu-id="ae4fb-131">如果成功，則傳回 **S \_ OK** 。</span><span class="sxs-lookup"><span data-stu-id="ae4fb-131">Return **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="ae4fb-132">備註</span><span class="sxs-lookup"><span data-stu-id="ae4fb-132">Remarks</span></span>

<span data-ttu-id="ae4fb-133">設定 **網域** 屬性是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="ae4fb-133">Setting the **Domain** property is optional.</span></span> <span data-ttu-id="ae4fb-134">如果未設定，則使用者可以在連接期間出現 [Windows 登入] 對話方塊時選擇網域。</span><span class="sxs-lookup"><span data-stu-id="ae4fb-134">If it is not set, the user can choose a domain when the Windows Logon dialog box appears during the connection.</span></span>

<span data-ttu-id="ae4fb-135">**Get \_ 網域** 方法會配置 *pDomain* 參數所指向之緩衝區所需的記憶體。</span><span class="sxs-lookup"><span data-stu-id="ae4fb-135">The **get\_Domain** method allocates the memory required for the buffer pointed to by the *pDomain* parameter.</span></span> <span data-ttu-id="ae4fb-136">呼叫 C/c + + 應用程式時，必須透過呼叫 [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) 函式來釋放記憶體。</span><span class="sxs-lookup"><span data-stu-id="ae4fb-136">Calling C/C++ applications must free the memory with a call to the [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) function.</span></span> <span data-ttu-id="ae4fb-137">Visual Basic 和腳本用戶端都不需要這麼做。</span><span class="sxs-lookup"><span data-stu-id="ae4fb-137">This is not required for Visual Basic and scripting clients.</span></span>

<span data-ttu-id="ae4fb-138">只有當控制項不是處於連接狀態時，才能設定這個屬性。</span><span class="sxs-lookup"><span data-stu-id="ae4fb-138">This property can be set only if the control is not in the connected state.</span></span> <span data-ttu-id="ae4fb-139">如果在連接控制項時呼叫它，它會傳回 **E \_ FAIL** 。</span><span class="sxs-lookup"><span data-stu-id="ae4fb-139">It returns **E\_FAIL** if it is called when the control is connected.</span></span> <span data-ttu-id="ae4fb-140">您可以藉由回應 [**IMsTscAxEvents**](imstscaxevents-interface.md) 中的連接事件，或檢查 [**連接**](imstscax-connected.md) 的屬性來檢查控制項是否已連接。</span><span class="sxs-lookup"><span data-stu-id="ae4fb-140">You can check if the control is connected by responding to connection events in [**IMsTscAxEvents**](imstscaxevents-interface.md) or examining the [**Connected**](imstscax-connected.md) property.</span></span>

<span data-ttu-id="ae4fb-141">如需遠端桌面網頁連線的詳細資訊，請參閱 [遠端桌面網頁連線的需求](requirements-for-remote-desktop-web-connection.md)。</span><span class="sxs-lookup"><span data-stu-id="ae4fb-141">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ae4fb-142">規格需求</span><span class="sxs-lookup"><span data-stu-id="ae4fb-142">Requirements</span></span>



| <span data-ttu-id="ae4fb-143">需求</span><span class="sxs-lookup"><span data-stu-id="ae4fb-143">Requirement</span></span> | <span data-ttu-id="ae4fb-144">值</span><span class="sxs-lookup"><span data-stu-id="ae4fb-144">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ae4fb-145">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ae4fb-145">Minimum supported client</span></span><br/> | <span data-ttu-id="ae4fb-146">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ae4fb-146">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="ae4fb-147">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ae4fb-147">Minimum supported server</span></span><br/> | <span data-ttu-id="ae4fb-148">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ae4fb-148">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="ae4fb-149">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="ae4fb-149">Type library</span></span><br/>             | <dl> <span data-ttu-id="ae4fb-150"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ae4fb-150"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="ae4fb-151">DLL</span><span class="sxs-lookup"><span data-stu-id="ae4fb-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ae4fb-152"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ae4fb-152"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="ae4fb-153">IID</span><span class="sxs-lookup"><span data-stu-id="ae4fb-153">IID</span></span><br/>                      | <span data-ttu-id="ae4fb-154">IID \_ IMsTscAx 定義為8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span><span class="sxs-lookup"><span data-stu-id="ae4fb-154">IID\_IMsTscAx is defined as 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="ae4fb-155">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ae4fb-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ae4fb-156">**IMsRdpClient**</span><span class="sxs-lookup"><span data-stu-id="ae4fb-156">**IMsRdpClient**</span></span>](imsrdpclient-interface.md)
</dt> <dt>

[<span data-ttu-id="ae4fb-157">**IMsRdpClient2**</span><span class="sxs-lookup"><span data-stu-id="ae4fb-157">**IMsRdpClient2**</span></span>](imsrdpclient2.md)
</dt> <dt>

[<span data-ttu-id="ae4fb-158">**IMsRdpClient3**</span><span class="sxs-lookup"><span data-stu-id="ae4fb-158">**IMsRdpClient3**</span></span>](imsrdpclient3.md)
</dt> <dt>

[<span data-ttu-id="ae4fb-159">**IMsRdpClient4**</span><span class="sxs-lookup"><span data-stu-id="ae4fb-159">**IMsRdpClient4**</span></span>](imsrdpclient4.md)
</dt> <dt>

[<span data-ttu-id="ae4fb-160">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="ae4fb-160">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="ae4fb-161">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="ae4fb-161">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="ae4fb-162">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="ae4fb-162">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="ae4fb-163">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="ae4fb-163">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="ae4fb-164">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="ae4fb-164">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="ae4fb-165">**連線**</span><span class="sxs-lookup"><span data-stu-id="ae4fb-165">**Connected**</span></span>](imstscax-connected.md)
</dt> <dt>

[<span data-ttu-id="ae4fb-166">**IMsTscAx**</span><span class="sxs-lookup"><span data-stu-id="ae4fb-166">**IMsTscAx**</span></span>](imstscax-interface.md)
</dt> <dt>

[<span data-ttu-id="ae4fb-167">**IMsTscAxEvents**</span><span class="sxs-lookup"><span data-stu-id="ae4fb-167">**IMsTscAxEvents**</span></span>](imstscaxevents-interface.md)
</dt> </dl>

 

