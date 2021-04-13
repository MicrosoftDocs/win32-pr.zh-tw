---
title: IMsTscAx Version 屬性
description: 指定目前控制項的版本號碼。
ms.assetid: 91ddeb4c-9d61-41e7-af96-95b0c4884682
ms.tgt_platform: multiple
keywords:
- Version 屬性遠端桌面服務
- Version 屬性遠端桌面服務，IMsTscAx 介面
- IMsTscAx 介面遠端桌面服務，Version 屬性
- Version 屬性遠端桌面服務，IMsRdpClient 介面
- IMsRdpClient 介面遠端桌面服務，Version 屬性
- Version 屬性遠端桌面服務，IMsRdpClient2 介面
- IMsRdpClient2 介面遠端桌面服務，Version 屬性
- Version 屬性遠端桌面服務，IMsRdpClient3 介面
- IMsRdpClient3 介面遠端桌面服務，Version 屬性
- Version 屬性遠端桌面服務，IMsRdpClient4 介面
- IMsRdpClient4 介面遠端桌面服務，Version 屬性
- Version 屬性遠端桌面服務，IMsRdpClient5 介面
- IMsRdpClient5 介面遠端桌面服務，Version 屬性
- Version 屬性遠端桌面服務，IMsRdpClient6 介面
- IMsRdpClient6 介面遠端桌面服務，Version 屬性
- Version 屬性遠端桌面服務，IMsRdpClient7 介面
- IMsRdpClient7 介面遠端桌面服務，Version 屬性
- Version 屬性遠端桌面服務，IMsRdpClient8 介面
- IMsRdpClient8 介面遠端桌面服務，Version 屬性
- Version 屬性遠端桌面服務，IMsRdpClient9 介面
- IMsRdpClient9 介面遠端桌面服務，Version 屬性
topic_type:
- apiref
api_name:
- IMsTscAx.Version
- IMsTscAx.get_Version
- IMsRdpClient.Version
- IMsRdpClient.get_Version
- IMsRdpClient2.Version
- IMsRdpClient2.get_Version
- IMsRdpClient3.Version
- IMsRdpClient3.get_Version
- IMsRdpClient4.Version
- IMsRdpClient4.get_Version
- IMsRdpClient5.Version
- IMsRdpClient5.get_Version
- IMsRdpClient6.Version
- IMsRdpClient6.get_Version
- IMsRdpClient7.Version
- IMsRdpClient7.get_Version
- IMsRdpClient8.Version
- IMsRdpClient8.get_Version
- IMsRdpClient9.Version
- IMsRdpClient9.get_Version
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff25f274d1f076c9c4119648ccb9cc6d82f43b33
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465321"
---
# <a name="imstscaxversion-property"></a><span data-ttu-id="ae074-124">IMsTscAx：： Version 屬性</span><span class="sxs-lookup"><span data-stu-id="ae074-124">IMsTscAx::Version property</span></span>

<span data-ttu-id="ae074-125">指定目前控制項的版本號碼。</span><span class="sxs-lookup"><span data-stu-id="ae074-125">Specifies the version number of the current control.</span></span>

<span data-ttu-id="ae074-126">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="ae074-126">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="ae074-127">語法</span><span class="sxs-lookup"><span data-stu-id="ae074-127">Syntax</span></span>


```C++
HRESULT get_Version(
  [out] BSTR *pVersion
);
```



## <a name="property-value"></a><span data-ttu-id="ae074-128">屬性值</span><span class="sxs-lookup"><span data-stu-id="ae074-128">Property value</span></span>

<span data-ttu-id="ae074-129">版本號碼。</span><span class="sxs-lookup"><span data-stu-id="ae074-129">The version number.</span></span>

## <a name="error-codes"></a><span data-ttu-id="ae074-130">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="ae074-130">Error codes</span></span>

<span data-ttu-id="ae074-131">如果成功，則傳回 **S \_ OK** 。</span><span class="sxs-lookup"><span data-stu-id="ae074-131">Return **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="ae074-132">備註</span><span class="sxs-lookup"><span data-stu-id="ae074-132">Remarks</span></span>

<span data-ttu-id="ae074-133">這個方法會配置 *pVersion* 參數所指向之緩衝區所需的記憶體。</span><span class="sxs-lookup"><span data-stu-id="ae074-133">This method allocates the memory required for the buffer pointed to by the *pVersion* parameter.</span></span> <span data-ttu-id="ae074-134">呼叫 C/c + + 應用程式時，必須透過呼叫 [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) 函式來釋放記憶體。</span><span class="sxs-lookup"><span data-stu-id="ae074-134">Calling C/C++ applications must free the memory with a call to the [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) function.</span></span> <span data-ttu-id="ae074-135">Visual Basic 和腳本用戶端都不需要這麼做。</span><span class="sxs-lookup"><span data-stu-id="ae074-135">This is not required for Visual Basic and scripting clients.</span></span>

<span data-ttu-id="ae074-136">如需遠端桌面網頁連線的詳細資訊，請參閱 [遠端桌面網頁連線的需求](requirements-for-remote-desktop-web-connection.md)。</span><span class="sxs-lookup"><span data-stu-id="ae074-136">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ae074-137">規格需求</span><span class="sxs-lookup"><span data-stu-id="ae074-137">Requirements</span></span>



| <span data-ttu-id="ae074-138">需求</span><span class="sxs-lookup"><span data-stu-id="ae074-138">Requirement</span></span> | <span data-ttu-id="ae074-139">值</span><span class="sxs-lookup"><span data-stu-id="ae074-139">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ae074-140">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ae074-140">Minimum supported client</span></span><br/> | <span data-ttu-id="ae074-141">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ae074-141">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="ae074-142">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ae074-142">Minimum supported server</span></span><br/> | <span data-ttu-id="ae074-143">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ae074-143">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="ae074-144">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="ae074-144">Type library</span></span><br/>             | <dl> <span data-ttu-id="ae074-145"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ae074-145"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="ae074-146">DLL</span><span class="sxs-lookup"><span data-stu-id="ae074-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ae074-147"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ae074-147"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="ae074-148">IID</span><span class="sxs-lookup"><span data-stu-id="ae074-148">IID</span></span><br/>                      | <span data-ttu-id="ae074-149">IID \_ IMsTscAx 定義為8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span><span class="sxs-lookup"><span data-stu-id="ae074-149">IID\_IMsTscAx is defined as 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="ae074-150">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ae074-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ae074-151">**IMsRdpClient**</span><span class="sxs-lookup"><span data-stu-id="ae074-151">**IMsRdpClient**</span></span>](imsrdpclient-interface.md)
</dt> <dt>

[<span data-ttu-id="ae074-152">**IMsRdpClient2**</span><span class="sxs-lookup"><span data-stu-id="ae074-152">**IMsRdpClient2**</span></span>](imsrdpclient2.md)
</dt> <dt>

[<span data-ttu-id="ae074-153">**IMsRdpClient3**</span><span class="sxs-lookup"><span data-stu-id="ae074-153">**IMsRdpClient3**</span></span>](imsrdpclient3.md)
</dt> <dt>

[<span data-ttu-id="ae074-154">**IMsRdpClient4**</span><span class="sxs-lookup"><span data-stu-id="ae074-154">**IMsRdpClient4**</span></span>](imsrdpclient4.md)
</dt> <dt>

[<span data-ttu-id="ae074-155">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="ae074-155">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="ae074-156">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="ae074-156">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="ae074-157">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="ae074-157">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="ae074-158">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="ae074-158">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="ae074-159">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="ae074-159">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="ae074-160">**IMsTscAx**</span><span class="sxs-lookup"><span data-stu-id="ae074-160">**IMsTscAx**</span></span>](imstscax-interface.md)
</dt> </dl>

 

