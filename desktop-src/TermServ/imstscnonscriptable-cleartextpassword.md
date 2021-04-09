---
title: IMsTscNonScriptable ClearTextPassword 屬性
description: 以純文字格式設定遠端桌面 ActiveX 控制項密碼。
ms.assetid: 93d35b10-5c92-4ab7-a32a-328ba6fcf16b
ms.tgt_platform: multiple
keywords:
- ClearTextPassword 屬性遠端桌面服務
- ClearTextPassword 屬性遠端桌面服務，IMsTscNonScriptable 介面
- IMsTscNonScriptable 介面遠端桌面服務，ClearTextPassword 屬性
- ClearTextPassword 屬性遠端桌面服務，IMsRdpClientNonScriptable 介面
- IMsRdpClientNonScriptable 介面遠端桌面服務，ClearTextPassword 屬性
- ClearTextPassword 屬性遠端桌面服務，IMsRdpClientNonScriptable2 介面
- IMsRdpClientNonScriptable2 介面遠端桌面服務，ClearTextPassword 屬性
- ClearTextPassword 屬性遠端桌面服務，IMsRdpClientNonScriptable3 介面
- IMsRdpClientNonScriptable3 介面遠端桌面服務，ClearTextPassword 屬性
- ClearTextPassword 屬性遠端桌面服務，IMsRdpClientNonScriptable4 介面
- IMsRdpClientNonScriptable4 介面遠端桌面服務，ClearTextPassword 屬性
- ClearTextPassword 屬性遠端桌面服務，IMsRdpClientNonScriptable5 介面
- IMsRdpClientNonScriptable5 介面遠端桌面服務，ClearTextPassword 屬性
- ClearTextPassword 屬性遠端桌面服務，MsRdpClient6 物件
- MsRdpClient6 物件遠端桌面服務、ClearTextPassword 屬性
- ClearTextPassword 屬性遠端桌面服務，MsRdpClient7 物件
- MsRdpClient7 物件遠端桌面服務、ClearTextPassword 屬性
- ClearTextPassword 屬性遠端桌面服務，MsRdpClient8 物件
- MsRdpClient8 物件遠端桌面服務、ClearTextPassword 屬性
- ClearTextPassword 屬性遠端桌面服務，MsRdpClient9 物件
- MsRdpClient9 物件遠端桌面服務、ClearTextPassword 屬性
topic_type:
- apiref
api_name:
- IMsTscNonScriptable.ClearTextPassword
- IMsTscNonScriptable.put_ClearTextPassword
- IMsRdpClientNonScriptable.ClearTextPassword
- IMsRdpClientNonScriptable.put_ClearTextPassword
- IMsRdpClientNonScriptable2.ClearTextPassword
- IMsRdpClientNonScriptable2.put_ClearTextPassword
- IMsRdpClientNonScriptable3.ClearTextPassword
- IMsRdpClientNonScriptable3.put_ClearTextPassword
- IMsRdpClientNonScriptable4.ClearTextPassword
- IMsRdpClientNonScriptable4.put_ClearTextPassword
- IMsRdpClientNonScriptable5.ClearTextPassword
- IMsRdpClientNonScriptable5.put_ClearTextPassword
- MsRdpClient6.ClearTextPassword
- MsRdpClient7.ClearTextPassword
- MsRdpClient8.ClearTextPassword
- MsRdpClient9.ClearTextPassword
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1aad33d7d85c6a5c331efe8383815e079150fb65
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686440"
---
# <a name="imstscnonscriptablecleartextpassword-property"></a><span data-ttu-id="fae89-124">IMsTscNonScriptable：： ClearTextPassword 屬性</span><span class="sxs-lookup"><span data-stu-id="fae89-124">IMsTscNonScriptable::ClearTextPassword property</span></span>

<span data-ttu-id="fae89-125">以純文字格式設定遠端桌面 ActiveX 控制項密碼。</span><span class="sxs-lookup"><span data-stu-id="fae89-125">Sets the Remote Desktop ActiveX control password in plaintext format.</span></span>

<span data-ttu-id="fae89-126">此屬性是唯寫的。</span><span class="sxs-lookup"><span data-stu-id="fae89-126">This property is write-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="fae89-127">Syntax</span><span class="sxs-lookup"><span data-stu-id="fae89-127">Syntax</span></span>


```C++
HRESULT put_ClearTextPassword(
  [in] BSTR newClearTextPass
);
```



## <a name="property-value"></a><span data-ttu-id="fae89-128">屬性值</span><span class="sxs-lookup"><span data-stu-id="fae89-128">Property value</span></span>

<span data-ttu-id="fae89-129">要用來連接的密碼（以純文字格式指定）。</span><span class="sxs-lookup"><span data-stu-id="fae89-129">The password to be used to connect, specified in plaintext format.</span></span>

## <a name="error-codes"></a><span data-ttu-id="fae89-130">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="fae89-130">Error codes</span></span>

<span data-ttu-id="fae89-131">如果成功，則傳回 **S \_ OK** 。</span><span class="sxs-lookup"><span data-stu-id="fae89-131">Return **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="fae89-132">備註</span><span class="sxs-lookup"><span data-stu-id="fae89-132">Remarks</span></span>

<span data-ttu-id="fae89-133">密碼會傳遞至安全加密 RDP 通道中的伺服器。</span><span class="sxs-lookup"><span data-stu-id="fae89-133">The password is passed to the server in the safely encrypted RDP communications channel.</span></span> <span data-ttu-id="fae89-134">設定純文字密碼之後，無法以純文字格式抓取。</span><span class="sxs-lookup"><span data-stu-id="fae89-134">After a plaintext password is set, it cannot be retrieved in plaintext format.</span></span>

<span data-ttu-id="fae89-135">只有當遠端桌面 ActiveX 控制項不是處於線上狀態時，才能設定 **ClearTextPassword** 屬性。</span><span class="sxs-lookup"><span data-stu-id="fae89-135">The **ClearTextPassword** property can only be set when the Remote Desktop ActiveX control is not in the connected state.</span></span> <span data-ttu-id="fae89-136">如果控制項已連接，則設定這個屬性會失敗。</span><span class="sxs-lookup"><span data-stu-id="fae89-136">Setting this property fails if the control is connected.</span></span> <span data-ttu-id="fae89-137">若要檢查連接狀態，請取出 [**IMsTscAx：： connected**](imstscax-connected.md) 屬性。</span><span class="sxs-lookup"><span data-stu-id="fae89-137">To check for the connected state, retrieve the [**IMsTscAx::Connected**](imstscax-connected.md) property.</span></span>

<span data-ttu-id="fae89-138">您也可以呼叫這個方法來設定純文字密碼，然後將它轉換成可移植編碼的密碼或二進位 (nonportable) 編碼的密碼。</span><span class="sxs-lookup"><span data-stu-id="fae89-138">You can also call this method to set a plaintext password before converting it to either a portable encoded password or to a binary (nonportable) encoded password.</span></span> <span data-ttu-id="fae89-139">不過請注意，編碼的密碼不應被安全地加密。</span><span class="sxs-lookup"><span data-stu-id="fae89-139">Note however that encoded passwords should not be considered securely encrypted.</span></span>

<span data-ttu-id="fae89-140">如果您第一次呼叫此方法來設定純文字格式的密碼，則可以將密碼轉換成編碼格式。</span><span class="sxs-lookup"><span data-stu-id="fae89-140">If you first call this method to set a password in plaintext format, you can then convert the password to encoded format.</span></span>

<span data-ttu-id="fae89-141">**將純文字密碼轉換成編碼格式**</span><span class="sxs-lookup"><span data-stu-id="fae89-141">**To convert a plaintext password to encoded format**</span></span>

1.  <span data-ttu-id="fae89-142">在 **ClearTextPassword** 屬性中，以純文字格式設定密碼。</span><span class="sxs-lookup"><span data-stu-id="fae89-142">Set the password in plaintext format in the **ClearTextPassword** property.</span></span>
2.  <span data-ttu-id="fae89-143">若要以二進位格式取出密碼 (nonportable) 編碼格式，請取出 [**BinaryPassword**](imstscnonscriptable-binarypassword.md) 屬性和 [**BinarySalt**](imstscnonscriptable-binarysalt.md) 屬性。</span><span class="sxs-lookup"><span data-stu-id="fae89-143">To retrieve the password in binary (nonportable) encoded format, retrieve the [**BinaryPassword**](imstscnonscriptable-binarypassword.md) property and the [**BinarySalt**](imstscnonscriptable-binarysalt.md) properties.</span></span> <span data-ttu-id="fae89-144">編碼的密碼部分和 salt 部分都需要以二進位編碼格式設定密碼。</span><span class="sxs-lookup"><span data-stu-id="fae89-144">Both the encoded password part and the salt part are required to set a password in binary encoded format.</span></span>
3.  <span data-ttu-id="fae89-145">若要以可移植的編碼格式取得密碼，請取出 [**PortablePassword**](imstscnonscriptable-portablepassword.md) 方法和 [**PortableSalt**](imstscnonscriptable-portablesalt.md) 屬性。</span><span class="sxs-lookup"><span data-stu-id="fae89-145">To retrieve the password in portable encoded format, retrieve the [**PortablePassword**](imstscnonscriptable-portablepassword.md) method and the [**PortableSalt**](imstscnonscriptable-portablesalt.md) properties.</span></span> <span data-ttu-id="fae89-146">這兩個元件都需要以可移植編碼格式設定密碼。</span><span class="sxs-lookup"><span data-stu-id="fae89-146">Both parts are required to set a password in portable encoded format.</span></span>

<span data-ttu-id="fae89-147">遵循上述三個步驟之後，您可以藉由設定 [**BinaryPassword**](imstscnonscriptable-binarypassword.md) 和 [**BinarySalt**](imstscnonscriptable-binarysalt.md) 屬性，或 [**PortablePassword**](imstscnonscriptable-portablepassword.md) 和 [**PortableSalt**](imstscnonscriptable-portablesalt.md) 屬性來設定編碼格式的密碼。</span><span class="sxs-lookup"><span data-stu-id="fae89-147">After following the preceding three steps, you can set the password in encoded format by setting the [**BinaryPassword**](imstscnonscriptable-binarypassword.md) and [**BinarySalt**](imstscnonscriptable-binarysalt.md) properties, or [**PortablePassword**](imstscnonscriptable-portablepassword.md) and [**PortableSalt**](imstscnonscriptable-portablesalt.md) properties.</span></span> <span data-ttu-id="fae89-148">這兩個元件都是必要的。</span><span class="sxs-lookup"><span data-stu-id="fae89-148">Both parts are required.</span></span>

<span data-ttu-id="fae89-149">若要啟用自動登入，您也必須設定使用者 [**名稱**](imstscax-username.md) 和 [**網域**](imstscax-domain.md) 屬性。</span><span class="sxs-lookup"><span data-stu-id="fae89-149">To enable automatic logon, you must also set the [**UserName**](imstscax-username.md) and [**Domain**](imstscax-domain.md) properties.</span></span> <span data-ttu-id="fae89-150">如果密碼無法驗證使用者，則會在伺服器上顯示 [Windows 登入] 對話方塊，提示使用者輸入密碼。</span><span class="sxs-lookup"><span data-stu-id="fae89-150">If the password fails to authenticate the user, the Windows Logon dialog box is displayed at the server to prompt the user for the password.</span></span>

<span data-ttu-id="fae89-151">如需遠端桌面網頁連線的詳細資訊，請參閱 [遠端桌面網頁連線的需求](requirements-for-remote-desktop-web-connection.md)。</span><span class="sxs-lookup"><span data-stu-id="fae89-151">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="fae89-152">規格需求</span><span class="sxs-lookup"><span data-stu-id="fae89-152">Requirements</span></span>



| <span data-ttu-id="fae89-153">需求</span><span class="sxs-lookup"><span data-stu-id="fae89-153">Requirement</span></span> | <span data-ttu-id="fae89-154">值</span><span class="sxs-lookup"><span data-stu-id="fae89-154">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="fae89-155">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="fae89-155">Minimum supported client</span></span><br/> | <span data-ttu-id="fae89-156">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="fae89-156">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="fae89-157">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="fae89-157">Minimum supported server</span></span><br/> | <span data-ttu-id="fae89-158">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fae89-158">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="fae89-159">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="fae89-159">Type library</span></span><br/>             | <dl> <span data-ttu-id="fae89-160"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fae89-160"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="fae89-161">DLL</span><span class="sxs-lookup"><span data-stu-id="fae89-161">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fae89-162"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fae89-162"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="fae89-163">IID</span><span class="sxs-lookup"><span data-stu-id="fae89-163">IID</span></span><br/>                      | <span data-ttu-id="fae89-164">IID \_ IMsTscNonScriptable 定義為 c1e6743a-41c1-4a74-832a-0dd06c1c7a0e</span><span class="sxs-lookup"><span data-stu-id="fae89-164">IID\_IMsTscNonScriptable is defined as c1e6743a-41c1-4a74-832a-0dd06c1c7a0e</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="fae89-165">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fae89-165">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fae89-166">**IMsRdpClientNonScriptable**</span><span class="sxs-lookup"><span data-stu-id="fae89-166">**IMsRdpClientNonScriptable**</span></span>](imsrdpclientnonscriptable-interface.md)
</dt> <dt>

[<span data-ttu-id="fae89-167">**IMsRdpClientNonScriptable2**</span><span class="sxs-lookup"><span data-stu-id="fae89-167">**IMsRdpClientNonScriptable2**</span></span>](imsrdpclientnonscriptable2.md)
</dt> <dt>

[<span data-ttu-id="fae89-168">**IMsRdpClientNonScriptable3**</span><span class="sxs-lookup"><span data-stu-id="fae89-168">**IMsRdpClientNonScriptable3**</span></span>](imsrdpclientnonscriptable3.md)
</dt> <dt>

[<span data-ttu-id="fae89-169">**IMsRdpClientNonScriptable4**</span><span class="sxs-lookup"><span data-stu-id="fae89-169">**IMsRdpClientNonScriptable4**</span></span>](imsrdpclientnonscriptable4.md)
</dt> <dt>

[<span data-ttu-id="fae89-170">**IMsRdpClientNonScriptable5**</span><span class="sxs-lookup"><span data-stu-id="fae89-170">**IMsRdpClientNonScriptable5**</span></span>](imsrdpclientnonscriptable5.md)
</dt> <dt>

[<span data-ttu-id="fae89-171">**IMsTscNonScriptable**</span><span class="sxs-lookup"><span data-stu-id="fae89-171">**IMsTscNonScriptable**</span></span>](imstscnonscriptable-interface.md)
</dt> </dl>

 

 





