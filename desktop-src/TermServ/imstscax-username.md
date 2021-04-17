---
title: IMsTscAx UserName 屬性
description: 指定使用者名稱登入認證。
ms.assetid: 9be25003-b9aa-41bb-a5a9-512546175114
ms.tgt_platform: multiple
keywords:
- UserName 屬性遠端桌面服務
- UserName 屬性遠端桌面服務，IMsTscAx 介面
- IMsTscAx 介面遠端桌面服務，使用者名稱屬性
- UserName 屬性遠端桌面服務，IMsRdpClient 介面
- IMsRdpClient 介面遠端桌面服務，使用者名稱屬性
- UserName 屬性遠端桌面服務，IMsRdpClient2 介面
- IMsRdpClient2 介面遠端桌面服務，使用者名稱屬性
- UserName 屬性遠端桌面服務，IMsRdpClient3 介面
- IMsRdpClient3 介面遠端桌面服務，使用者名稱屬性
- UserName 屬性遠端桌面服務，IMsRdpClient4 介面
- IMsRdpClient4 介面遠端桌面服務，使用者名稱屬性
- UserName 屬性遠端桌面服務，IMsRdpClient5 介面
- IMsRdpClient5 介面遠端桌面服務，使用者名稱屬性
- UserName 屬性遠端桌面服務，IMsRdpClient6 介面
- IMsRdpClient6 介面遠端桌面服務，使用者名稱屬性
- UserName 屬性遠端桌面服務，IMsRdpClient7 介面
- IMsRdpClient7 介面遠端桌面服務，使用者名稱屬性
- UserName 屬性遠端桌面服務，IMsRdpClient8 介面
- IMsRdpClient8 介面遠端桌面服務，使用者名稱屬性
- UserName 屬性遠端桌面服務，IMsRdpClient9 介面
- IMsRdpClient9 介面遠端桌面服務，使用者名稱屬性
topic_type:
- apiref
api_name:
- IMsTscAx.UserName
- IMsTscAx.get_UserName
- IMsTscAx.put_UserName
- IMsRdpClient.UserName
- IMsRdpClient.get_UserName
- IMsRdpClient.put_UserName
- IMsRdpClient2.UserName
- IMsRdpClient2.get_UserName
- IMsRdpClient2.put_UserName
- IMsRdpClient3.UserName
- IMsRdpClient3.get_UserName
- IMsRdpClient3.put_UserName
- IMsRdpClient4.UserName
- IMsRdpClient4.get_UserName
- IMsRdpClient4.put_UserName
- IMsRdpClient5.UserName
- IMsRdpClient5.get_UserName
- IMsRdpClient5.put_UserName
- IMsRdpClient6.UserName
- IMsRdpClient6.get_UserName
- IMsRdpClient6.put_UserName
- IMsRdpClient7.UserName
- IMsRdpClient7.get_UserName
- IMsRdpClient7.put_UserName
- IMsRdpClient8.UserName
- IMsRdpClient8.get_UserName
- IMsRdpClient8.put_UserName
- IMsRdpClient9.UserName
- IMsRdpClient9.get_UserName
- IMsRdpClient9.put_UserName
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a94a7f7d9fe5d6532de55f36a50094205fe1d4ac
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466849"
---
# <a name="imstscaxusername-property"></a><span data-ttu-id="a0601-124">IMsTscAx：： UserName 屬性</span><span class="sxs-lookup"><span data-stu-id="a0601-124">IMsTscAx::UserName property</span></span>

<span data-ttu-id="a0601-125">指定使用者名稱登入認證。</span><span class="sxs-lookup"><span data-stu-id="a0601-125">Specifies the user name logon credential.</span></span>

<span data-ttu-id="a0601-126">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="a0601-126">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="a0601-127">Syntax</span><span class="sxs-lookup"><span data-stu-id="a0601-127">Syntax</span></span>


```C++
HRESULT put_UserName(
  [in]  BSTR newVal
);

HRESULT get_UserName(
  [out] BSTR *pUserName
);
```



## <a name="property-value"></a><span data-ttu-id="a0601-128">屬性值</span><span class="sxs-lookup"><span data-stu-id="a0601-128">Property value</span></span>

<span data-ttu-id="a0601-129">新的使用者名稱。</span><span class="sxs-lookup"><span data-stu-id="a0601-129">The new user name.</span></span>

## <a name="error-codes"></a><span data-ttu-id="a0601-130">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="a0601-130">Error codes</span></span>

<span data-ttu-id="a0601-131">如果成功，則傳回 **S \_ OK** 。</span><span class="sxs-lookup"><span data-stu-id="a0601-131">Return **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="a0601-132">備註</span><span class="sxs-lookup"><span data-stu-id="a0601-132">Remarks</span></span>

<span data-ttu-id="a0601-133">設定 **UserName** 屬性是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="a0601-133">Setting the **UserName** property is optional.</span></span> <span data-ttu-id="a0601-134">如果未指定，則使用者可以在連接期間出現 [Windows 登入] 對話方塊時，提供使用者名稱。</span><span class="sxs-lookup"><span data-stu-id="a0601-134">If it is not specified, the user can provide a user name when the Windows Logon dialog box appears during connection.</span></span>

<span data-ttu-id="a0601-135">只有當控制項不是處於連接狀態時，才能設定這個屬性。</span><span class="sxs-lookup"><span data-stu-id="a0601-135">This property can be set only if the control is not in the connected state.</span></span> <span data-ttu-id="a0601-136">如果在連接控制項時呼叫它，它會傳回 **E \_ FAIL** 。</span><span class="sxs-lookup"><span data-stu-id="a0601-136">It returns **E\_FAIL** if it is called when the control is connected.</span></span> <span data-ttu-id="a0601-137">您可以藉由回應 [**IMsTscAxEvents**](imstscaxevents-interface.md) 中的連接事件，或檢查 [**連接**](imstscax-connected.md) 的屬性來檢查控制項是否已連接。</span><span class="sxs-lookup"><span data-stu-id="a0601-137">You can check if the control is connected by responding to connection events in [**IMsTscAxEvents**](imstscaxevents-interface.md) or examining the [**Connected**](imstscax-connected.md) property.</span></span>

<span data-ttu-id="a0601-138">**取得使用者 \_ 名稱** 屬性方法會配置 *pVersion* 參數所指向之緩衝區所需的記憶體。</span><span class="sxs-lookup"><span data-stu-id="a0601-138">The **get\_UserName** property method allocates the memory required for the buffer pointed to by the *pVersion* parameter.</span></span> <span data-ttu-id="a0601-139">呼叫 C/c + + 應用程式時，必須透過呼叫 [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) 函式來釋放記憶體。</span><span class="sxs-lookup"><span data-stu-id="a0601-139">Calling C/C++ applications must free the memory with a call to the [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) function.</span></span> <span data-ttu-id="a0601-140">Visual Basic 和腳本用戶端都不需要這麼做。</span><span class="sxs-lookup"><span data-stu-id="a0601-140">This is not required for Visual Basic and scripting clients.</span></span>

<span data-ttu-id="a0601-141">如需遠端桌面網頁連線的詳細資訊，請參閱 [遠端桌面網頁連線的需求](requirements-for-remote-desktop-web-connection.md)。</span><span class="sxs-lookup"><span data-stu-id="a0601-141">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a0601-142">規格需求</span><span class="sxs-lookup"><span data-stu-id="a0601-142">Requirements</span></span>



| <span data-ttu-id="a0601-143">需求</span><span class="sxs-lookup"><span data-stu-id="a0601-143">Requirement</span></span> | <span data-ttu-id="a0601-144">值</span><span class="sxs-lookup"><span data-stu-id="a0601-144">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a0601-145">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a0601-145">Minimum supported client</span></span><br/> | <span data-ttu-id="a0601-146">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a0601-146">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="a0601-147">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a0601-147">Minimum supported server</span></span><br/> | <span data-ttu-id="a0601-148">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a0601-148">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="a0601-149">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="a0601-149">Type library</span></span><br/>             | <dl> <span data-ttu-id="a0601-150"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a0601-150"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="a0601-151">DLL</span><span class="sxs-lookup"><span data-stu-id="a0601-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a0601-152"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a0601-152"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="a0601-153">IID</span><span class="sxs-lookup"><span data-stu-id="a0601-153">IID</span></span><br/>                      | <span data-ttu-id="a0601-154">IID \_ IMsTscAx 定義為8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span><span class="sxs-lookup"><span data-stu-id="a0601-154">IID\_IMsTscAx is defined as 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="a0601-155">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a0601-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a0601-156">**IMsRdpClient**</span><span class="sxs-lookup"><span data-stu-id="a0601-156">**IMsRdpClient**</span></span>](imsrdpclient-interface.md)
</dt> <dt>

[<span data-ttu-id="a0601-157">**IMsRdpClient2**</span><span class="sxs-lookup"><span data-stu-id="a0601-157">**IMsRdpClient2**</span></span>](imsrdpclient2.md)
</dt> <dt>

[<span data-ttu-id="a0601-158">**IMsRdpClient3**</span><span class="sxs-lookup"><span data-stu-id="a0601-158">**IMsRdpClient3**</span></span>](imsrdpclient3.md)
</dt> <dt>

[<span data-ttu-id="a0601-159">**IMsRdpClient4**</span><span class="sxs-lookup"><span data-stu-id="a0601-159">**IMsRdpClient4**</span></span>](imsrdpclient4.md)
</dt> <dt>

[<span data-ttu-id="a0601-160">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="a0601-160">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="a0601-161">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="a0601-161">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="a0601-162">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="a0601-162">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="a0601-163">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="a0601-163">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="a0601-164">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="a0601-164">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="a0601-165">**IMsTscAx**</span><span class="sxs-lookup"><span data-stu-id="a0601-165">**IMsTscAx**</span></span>](imstscax-interface.md)
</dt> </dl>

 

