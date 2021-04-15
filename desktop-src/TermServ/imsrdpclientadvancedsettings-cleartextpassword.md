---
title: IMsRdpClientAdvancedSettings ClearTextPassword 屬性
description: 指定要連接的密碼。 如需詳細資訊，請參閱 IMsTscNonScriptable 介面。
ms.assetid: 9bb12dd6-f74c-488d-b6e5-4f96346610a1
ms.tgt_platform: multiple
keywords:
- ClearTextPassword 屬性遠端桌面服務
- ClearTextPassword 屬性遠端桌面服務，IMsRdpClientAdvancedSettings 介面
- IMsRdpClientAdvancedSettings 介面遠端桌面服務，ClearTextPassword 屬性
- ClearTextPassword 屬性遠端桌面服務，IMsRdpClientAdvancedSettings2 介面
- IMsRdpClientAdvancedSettings2 介面遠端桌面服務，ClearTextPassword 屬性
- ClearTextPassword 屬性遠端桌面服務，IMsRdpClientAdvancedSettings3 介面
- IMsRdpClientAdvancedSettings3 介面遠端桌面服務，ClearTextPassword 屬性
- ClearTextPassword 屬性遠端桌面服務，IMsRdpClientAdvancedSettings4 介面
- IMsRdpClientAdvancedSettings4 介面遠端桌面服務，ClearTextPassword 屬性
- ClearTextPassword 屬性遠端桌面服務，IMsRdpClientAdvancedSettings5 介面
- IMsRdpClientAdvancedSettings5 介面遠端桌面服務，ClearTextPassword 屬性
- ClearTextPassword 屬性遠端桌面服務，IMsRdpClientAdvancedSettings6 介面
- IMsRdpClientAdvancedSettings6 介面遠端桌面服務，ClearTextPassword 屬性
- ClearTextPassword 屬性遠端桌面服務，IMsRdpClientAdvancedSettings7 介面
- IMsRdpClientAdvancedSettings7 介面遠端桌面服務，ClearTextPassword 屬性
- ClearTextPassword 屬性遠端桌面服務，IMsRdpClientAdvancedSettings8 介面
- IMsRdpClientAdvancedSettings8 介面遠端桌面服務，ClearTextPassword 屬性
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.ClearTextPassword
- IMsRdpClientAdvancedSettings.put_ClearTextPassword
- IMsRdpClientAdvancedSettings2.ClearTextPassword
- IMsRdpClientAdvancedSettings2.put_ClearTextPassword
- IMsRdpClientAdvancedSettings3.ClearTextPassword
- IMsRdpClientAdvancedSettings3.put_ClearTextPassword
- IMsRdpClientAdvancedSettings4.ClearTextPassword
- IMsRdpClientAdvancedSettings4.put_ClearTextPassword
- IMsRdpClientAdvancedSettings5.ClearTextPassword
- IMsRdpClientAdvancedSettings5.put_ClearTextPassword
- IMsRdpClientAdvancedSettings6.ClearTextPassword
- IMsRdpClientAdvancedSettings6.put_ClearTextPassword
- IMsRdpClientAdvancedSettings7.ClearTextPassword
- IMsRdpClientAdvancedSettings7.put_ClearTextPassword
- IMsRdpClientAdvancedSettings8.ClearTextPassword
- IMsRdpClientAdvancedSettings8.put_ClearTextPassword
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6943913193b2ecc9ed6ab31728d0274fb9ddd231
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465137"
---
# <a name="imsrdpclientadvancedsettingscleartextpassword-property"></a><span data-ttu-id="f5013-121">IMsRdpClientAdvancedSettings：： ClearTextPassword 屬性</span><span class="sxs-lookup"><span data-stu-id="f5013-121">IMsRdpClientAdvancedSettings::ClearTextPassword property</span></span>

<span data-ttu-id="f5013-122">指定要連接的密碼。</span><span class="sxs-lookup"><span data-stu-id="f5013-122">Specifies the password with which to connect.</span></span> <span data-ttu-id="f5013-123">如需詳細資訊，請參閱 [**IMsTscNonScriptable**](imstscnonscriptable-interface.md) 介面。</span><span class="sxs-lookup"><span data-stu-id="f5013-123">For more information, see the [**IMsTscNonScriptable**](imstscnonscriptable-interface.md) interface.</span></span>

> [!Caution]  
> <span data-ttu-id="f5013-124">雖然可以透過這個屬性取得可編寫腳本的純文字密碼存取權，但開發人員在其應用程式中傳遞密碼時，仍須負責執行每個警告和維護安全性。</span><span class="sxs-lookup"><span data-stu-id="f5013-124">Even though scriptable access to plaintext passwords is available through this property, it is still the responsibility of the developer to exercise every caution and maintain security when passing passwords in their applications.</span></span>

 

<span data-ttu-id="f5013-125">此屬性是唯寫的。</span><span class="sxs-lookup"><span data-stu-id="f5013-125">This property is write-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="f5013-126">Syntax</span><span class="sxs-lookup"><span data-stu-id="f5013-126">Syntax</span></span>


```C++
HRESULT put_ClearTextPassword(
  [in] BSTR clearTextPassword
);
```



## <a name="property-value"></a><span data-ttu-id="f5013-127">屬性值</span><span class="sxs-lookup"><span data-stu-id="f5013-127">Property value</span></span>

<span data-ttu-id="f5013-128">新的密碼。</span><span class="sxs-lookup"><span data-stu-id="f5013-128">The new password.</span></span>

## <a name="error-codes"></a><span data-ttu-id="f5013-129">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="f5013-129">Error codes</span></span>

<span data-ttu-id="f5013-130">如果成功，則傳回 **S \_ OK** 。</span><span class="sxs-lookup"><span data-stu-id="f5013-130">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="f5013-131">備註</span><span class="sxs-lookup"><span data-stu-id="f5013-131">Remarks</span></span>

<span data-ttu-id="f5013-132">如需遠端桌面網頁連線的詳細資訊，請參閱 [遠端桌面網頁連線的需求](requirements-for-remote-desktop-web-connection.md)。</span><span class="sxs-lookup"><span data-stu-id="f5013-132">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f5013-133">規格需求</span><span class="sxs-lookup"><span data-stu-id="f5013-133">Requirements</span></span>



| <span data-ttu-id="f5013-134">需求</span><span class="sxs-lookup"><span data-stu-id="f5013-134">Requirement</span></span> | <span data-ttu-id="f5013-135">值</span><span class="sxs-lookup"><span data-stu-id="f5013-135">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f5013-136">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f5013-136">Minimum supported client</span></span><br/> | <span data-ttu-id="f5013-137">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f5013-137">Windows Vista</span></span><br/>                                                                        |
| <span data-ttu-id="f5013-138">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f5013-138">Minimum supported server</span></span><br/> | <span data-ttu-id="f5013-139">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f5013-139">Windows Server 2008</span></span><br/>                                                                  |
| <span data-ttu-id="f5013-140">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="f5013-140">Type library</span></span><br/>             | <dl> <span data-ttu-id="f5013-141"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f5013-141"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="f5013-142">DLL</span><span class="sxs-lookup"><span data-stu-id="f5013-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f5013-143"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f5013-143"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="f5013-144">IID</span><span class="sxs-lookup"><span data-stu-id="f5013-144">IID</span></span><br/>                      | <span data-ttu-id="f5013-145">IID \_ IMsRdpClientAdvancedSettings 定義為3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span><span class="sxs-lookup"><span data-stu-id="f5013-145">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f5013-146">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f5013-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f5013-147">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="f5013-147">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="f5013-148">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="f5013-148">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="f5013-149">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="f5013-149">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="f5013-150">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="f5013-150">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="f5013-151">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="f5013-151">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="f5013-152">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="f5013-152">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="f5013-153">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="f5013-153">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="f5013-154">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="f5013-154">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





