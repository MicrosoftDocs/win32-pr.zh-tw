---
title: 'IMsTscAx 伺服器屬性 (Asptlb .h) '
description: 指定目前控制項所連接的伺服器名稱。
ms.assetid: 81118ddd-2662-47f5-8e9d-9c2a5056820b
ms.tgt_platform: multiple
keywords:
- 伺服器屬性遠端桌面服務
- 伺服器屬性遠端桌面服務、IMsTscAx 介面
- IMsTscAx 介面遠端桌面服務，伺服器屬性
- 伺服器屬性遠端桌面服務、IMsRdpClient 介面
- IMsRdpClient 介面遠端桌面服務，伺服器屬性
- 伺服器屬性遠端桌面服務、IMsRdpClient2 介面
- IMsRdpClient2 介面遠端桌面服務，伺服器屬性
- 伺服器屬性遠端桌面服務、IMsRdpClient3 介面
- IMsRdpClient3 介面遠端桌面服務，伺服器屬性
- 伺服器屬性遠端桌面服務、IMsRdpClient4 介面
- IMsRdpClient4 介面遠端桌面服務，伺服器屬性
- 伺服器屬性遠端桌面服務、IMsRdpClient5 介面
- IMsRdpClient5 介面遠端桌面服務，伺服器屬性
- 伺服器屬性遠端桌面服務、IMsRdpClient6 介面
- IMsRdpClient6 介面遠端桌面服務，伺服器屬性
- 伺服器屬性遠端桌面服務、IMsRdpClient7 介面
- IMsRdpClient7 介面遠端桌面服務，伺服器屬性
- 伺服器屬性遠端桌面服務、IMsRdpClient8 介面
- IMsRdpClient8 介面遠端桌面服務，伺服器屬性
- 伺服器屬性遠端桌面服務、IMsRdpClient9 介面
- IMsRdpClient9 介面遠端桌面服務，伺服器屬性
topic_type:
- apiref
api_name:
- IMsTscAx.Server
- IMsTscAx.get_Server
- IMsTscAx.put_Server
- IMsRdpClient.Server
- IMsRdpClient.get_Server
- IMsRdpClient.put_Server
- IMsRdpClient2.Server
- IMsRdpClient2.get_Server
- IMsRdpClient2.put_Server
- IMsRdpClient3.Server
- IMsRdpClient3.get_Server
- IMsRdpClient3.put_Server
- IMsRdpClient4.Server
- IMsRdpClient4.get_Server
- IMsRdpClient4.put_Server
- IMsRdpClient5.Server
- IMsRdpClient5.get_Server
- IMsRdpClient5.put_Server
- IMsRdpClient6.Server
- IMsRdpClient6.get_Server
- IMsRdpClient6.put_Server
- IMsRdpClient7.Server
- IMsRdpClient7.get_Server
- IMsRdpClient7.put_Server
- IMsRdpClient8.Server
- IMsRdpClient8.get_Server
- IMsRdpClient8.put_Server
- IMsRdpClient9.Server
- IMsRdpClient9.get_Server
- IMsRdpClient9.put_Server
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d7b7be04c149e2ac10c1a3e905678bd2b5f663cd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103933997"
---
# <a name="imstscaxserver-property"></a><span data-ttu-id="2b7dc-124">IMsTscAx：： Server 屬性</span><span class="sxs-lookup"><span data-stu-id="2b7dc-124">IMsTscAx::Server property</span></span>

<span data-ttu-id="2b7dc-125">指定目前控制項所連接的伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="2b7dc-125">Specifies the name of the server to which the current control is connected.</span></span>

<span data-ttu-id="2b7dc-126">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="2b7dc-126">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="2b7dc-127">Syntax</span><span class="sxs-lookup"><span data-stu-id="2b7dc-127">Syntax</span></span>


```C++
HRESULT put_Server(
  [in]  BSTR newVal
);

HRESULT get_Server(
  [out] BSTR *pServer
);
```



## <a name="property-value"></a><span data-ttu-id="2b7dc-128">屬性值</span><span class="sxs-lookup"><span data-stu-id="2b7dc-128">Property value</span></span>

<span data-ttu-id="2b7dc-129">新的伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="2b7dc-129">The new server name.</span></span> <span data-ttu-id="2b7dc-130">此參數可以是 DNS 名稱或 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="2b7dc-130">This parameter can be a DNS name or IP address.</span></span>

## <a name="error-codes"></a><span data-ttu-id="2b7dc-131">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="2b7dc-131">Error codes</span></span>

<span data-ttu-id="2b7dc-132">如果方法成功，則會傳回 **S \_ OK** 。</span><span class="sxs-lookup"><span data-stu-id="2b7dc-132">If the methods succeed, **S\_OK** is returned.</span></span> <span data-ttu-id="2b7dc-133">任何其他 **HRESULT** 值都表示呼叫失敗。</span><span class="sxs-lookup"><span data-stu-id="2b7dc-133">Any other **HRESULT** value indicates that the call failed.</span></span>

## <a name="remarks"></a><span data-ttu-id="2b7dc-134">備註</span><span class="sxs-lookup"><span data-stu-id="2b7dc-134">Remarks</span></span>

<span data-ttu-id="2b7dc-135">呼叫 [**Connect**](imstscax-connect.md) 方法之前，必須先設定這個屬性。</span><span class="sxs-lookup"><span data-stu-id="2b7dc-135">This property must be set before calling the [**Connect**](imstscax-connect.md) method.</span></span> <span data-ttu-id="2b7dc-136">它是唯一必須在連接之前設定的屬性。</span><span class="sxs-lookup"><span data-stu-id="2b7dc-136">It is the only property that must be set before connecting.</span></span>

<span data-ttu-id="2b7dc-137">只有當控制項不是處於連接狀態時，才能設定這個屬性。</span><span class="sxs-lookup"><span data-stu-id="2b7dc-137">This property can be set only if the control is not in the connected state.</span></span> <span data-ttu-id="2b7dc-138">如果在連接控制項時呼叫這個屬性，則這個屬性會傳回 **E \_ FAIL** 。</span><span class="sxs-lookup"><span data-stu-id="2b7dc-138">This property returns **E\_FAIL** if it is called when the control is connected.</span></span> <span data-ttu-id="2b7dc-139">您可以使用 [**連接**](imstscax-connected.md) 的屬性來檢查連接的狀態。</span><span class="sxs-lookup"><span data-stu-id="2b7dc-139">You can check for the connected state by using the [**Connected**](imstscax-connected.md) property.</span></span>

<span data-ttu-id="2b7dc-140">這個方法會配置 *pServer* 參數所指向之緩衝區所需的記憶體。</span><span class="sxs-lookup"><span data-stu-id="2b7dc-140">This method allocates the memory required for the buffer pointed to by the *pServer* parameter.</span></span> <span data-ttu-id="2b7dc-141">呼叫 C/c + + 應用程式時，必須透過呼叫 [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) 函式來釋放記憶體。</span><span class="sxs-lookup"><span data-stu-id="2b7dc-141">Calling C/C++ applications must free the memory with a call to the [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) function.</span></span> <span data-ttu-id="2b7dc-142">Visual Basic 和腳本用戶端都不需要這麼做。</span><span class="sxs-lookup"><span data-stu-id="2b7dc-142">This is not required for Visual Basic and scripting clients.</span></span>

<span data-ttu-id="2b7dc-143">如需遠端桌面網頁連線的詳細資訊，請參閱 [遠端桌面網頁連線的需求](requirements-for-remote-desktop-web-connection.md)。</span><span class="sxs-lookup"><span data-stu-id="2b7dc-143">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="2b7dc-144">規格需求</span><span class="sxs-lookup"><span data-stu-id="2b7dc-144">Requirements</span></span>



| <span data-ttu-id="2b7dc-145">需求</span><span class="sxs-lookup"><span data-stu-id="2b7dc-145">Requirement</span></span> | <span data-ttu-id="2b7dc-146">值</span><span class="sxs-lookup"><span data-stu-id="2b7dc-146">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2b7dc-147">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2b7dc-147">Minimum supported client</span></span><br/> | <span data-ttu-id="2b7dc-148">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2b7dc-148">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="2b7dc-149">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2b7dc-149">Minimum supported server</span></span><br/> | <span data-ttu-id="2b7dc-150">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2b7dc-150">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="2b7dc-151">標頭</span><span class="sxs-lookup"><span data-stu-id="2b7dc-151">Header</span></span><br/>                   | <dl> <span data-ttu-id="2b7dc-152"><dt>Asptlb。h</dt></span><span class="sxs-lookup"><span data-stu-id="2b7dc-152"><dt>Asptlb.h</dt></span></span> </dl>    |
| <span data-ttu-id="2b7dc-153">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="2b7dc-153">Type library</span></span><br/>             | <dl> <span data-ttu-id="2b7dc-154"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2b7dc-154"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="2b7dc-155">DLL</span><span class="sxs-lookup"><span data-stu-id="2b7dc-155">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2b7dc-156"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2b7dc-156"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="2b7dc-157">IID</span><span class="sxs-lookup"><span data-stu-id="2b7dc-157">IID</span></span><br/>                      | <span data-ttu-id="2b7dc-158">IID \_ IMsTscAx 定義為8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span><span class="sxs-lookup"><span data-stu-id="2b7dc-158">IID\_IMsTscAx is defined as 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="2b7dc-159">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2b7dc-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2b7dc-160">**IMsRdpClient**</span><span class="sxs-lookup"><span data-stu-id="2b7dc-160">**IMsRdpClient**</span></span>](imsrdpclient-interface.md)
</dt> <dt>

[<span data-ttu-id="2b7dc-161">**IMsRdpClient2**</span><span class="sxs-lookup"><span data-stu-id="2b7dc-161">**IMsRdpClient2**</span></span>](imsrdpclient2.md)
</dt> <dt>

[<span data-ttu-id="2b7dc-162">**IMsRdpClient3**</span><span class="sxs-lookup"><span data-stu-id="2b7dc-162">**IMsRdpClient3**</span></span>](imsrdpclient3.md)
</dt> <dt>

[<span data-ttu-id="2b7dc-163">**IMsRdpClient4**</span><span class="sxs-lookup"><span data-stu-id="2b7dc-163">**IMsRdpClient4**</span></span>](imsrdpclient4.md)
</dt> <dt>

[<span data-ttu-id="2b7dc-164">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="2b7dc-164">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="2b7dc-165">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="2b7dc-165">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="2b7dc-166">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="2b7dc-166">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="2b7dc-167">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="2b7dc-167">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="2b7dc-168">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="2b7dc-168">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="2b7dc-169">**IMsTscAx**</span><span class="sxs-lookup"><span data-stu-id="2b7dc-169">**IMsTscAx**</span></span>](imstscax-interface.md)
</dt> </dl>

 

