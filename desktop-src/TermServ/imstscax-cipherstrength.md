---
title: IMsTscAx CipherStrength 屬性
description: 抓取目前控制項的最大加密強度。
ms.assetid: 94efe3e5-4074-4187-b58a-b812f37f3622
ms.tgt_platform: multiple
keywords:
- CipherStrength 屬性遠端桌面服務
- CipherStrength 屬性遠端桌面服務，IMsTscAx 介面
- IMsTscAx 介面遠端桌面服務，CipherStrength 屬性
- CipherStrength 屬性遠端桌面服務，IMsRdpClient 介面
- IMsRdpClient 介面遠端桌面服務，CipherStrength 屬性
- CipherStrength 屬性遠端桌面服務，IMsRdpClient2 介面
- IMsRdpClient2 介面遠端桌面服務，CipherStrength 屬性
- CipherStrength 屬性遠端桌面服務，IMsRdpClient3 介面
- IMsRdpClient3 介面遠端桌面服務，CipherStrength 屬性
- CipherStrength 屬性遠端桌面服務，IMsRdpClient4 介面
- IMsRdpClient4 介面遠端桌面服務，CipherStrength 屬性
- CipherStrength 屬性遠端桌面服務，IMsRdpClient5 介面
- IMsRdpClient5 介面遠端桌面服務，CipherStrength 屬性
- CipherStrength 屬性遠端桌面服務，IMsRdpClient6 介面
- IMsRdpClient6 介面遠端桌面服務，CipherStrength 屬性
- CipherStrength 屬性遠端桌面服務，IMsRdpClient7 介面
- IMsRdpClient7 介面遠端桌面服務，CipherStrength 屬性
- CipherStrength 屬性遠端桌面服務，IMsRdpClient8 介面
- IMsRdpClient8 介面遠端桌面服務，CipherStrength 屬性
- CipherStrength 屬性遠端桌面服務，IMsRdpClient9 介面
- IMsRdpClient9 介面遠端桌面服務，CipherStrength 屬性
topic_type:
- apiref
api_name:
- IMsTscAx.CipherStrength
- IMsTscAx.get_CipherStrength
- IMsRdpClient.CipherStrength
- IMsRdpClient.get_CipherStrength
- IMsRdpClient2.CipherStrength
- IMsRdpClient2.get_CipherStrength
- IMsRdpClient3.CipherStrength
- IMsRdpClient3.get_CipherStrength
- IMsRdpClient4.CipherStrength
- IMsRdpClient4.get_CipherStrength
- IMsRdpClient5.CipherStrength
- IMsRdpClient5.get_CipherStrength
- IMsRdpClient6.CipherStrength
- IMsRdpClient6.get_CipherStrength
- IMsRdpClient7.CipherStrength
- IMsRdpClient7.get_CipherStrength
- IMsRdpClient8.CipherStrength
- IMsRdpClient8.get_CipherStrength
- IMsRdpClient9.CipherStrength
- IMsRdpClient9.get_CipherStrength
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 401cf3796d349aaa6764eae46a371a9d485f763c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384033"
---
# <a name="imstscaxcipherstrength-property"></a><span data-ttu-id="e40e2-124">IMsTscAx：： CipherStrength 屬性</span><span class="sxs-lookup"><span data-stu-id="e40e2-124">IMsTscAx::CipherStrength property</span></span>

<span data-ttu-id="e40e2-125">抓取目前控制項的最大加密強度。</span><span class="sxs-lookup"><span data-stu-id="e40e2-125">Retrieves the maximum encryption strength of the current control.</span></span>

<span data-ttu-id="e40e2-126">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="e40e2-126">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="e40e2-127">語法</span><span class="sxs-lookup"><span data-stu-id="e40e2-127">Syntax</span></span>


```C++
HRESULT get_CipherStrength(
  [out] LONG *pCipherStrength
);
```



## <a name="property-value"></a><span data-ttu-id="e40e2-128">屬性值</span><span class="sxs-lookup"><span data-stu-id="e40e2-128">Property value</span></span>

<span data-ttu-id="e40e2-129">加密強度。</span><span class="sxs-lookup"><span data-stu-id="e40e2-129">The encryption strength.</span></span>

## <a name="error-codes"></a><span data-ttu-id="e40e2-130">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="e40e2-130">Error codes</span></span>

<span data-ttu-id="e40e2-131">如果成功，則傳回 **S \_ OK** 。</span><span class="sxs-lookup"><span data-stu-id="e40e2-131">Return **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="e40e2-132">備註</span><span class="sxs-lookup"><span data-stu-id="e40e2-132">Remarks</span></span>

<span data-ttu-id="e40e2-133">針對遠端桌面網頁連線，加密強度一律為128，因為遠端桌面 ActiveX 控制項支援最多（含）128位的加密。</span><span class="sxs-lookup"><span data-stu-id="e40e2-133">For Remote Desktop Web Connection, the cipher strength is always 128 because the Remote Desktop ActiveX control supports encryption up to and including 128 bits.</span></span> <span data-ttu-id="e40e2-134">128位控制項仍可連接至56位加密遠端桌面工作階段主機 (RD 工作階段主機) 伺服器。</span><span class="sxs-lookup"><span data-stu-id="e40e2-134">The 128-bit control can still connect to 56 bit encryption Remote Desktop Session Host (RD Session Host) servers.</span></span>

<span data-ttu-id="e40e2-135">如需遠端桌面網頁連線的詳細資訊，請參閱 [遠端桌面網頁連線的需求](requirements-for-remote-desktop-web-connection.md)。</span><span class="sxs-lookup"><span data-stu-id="e40e2-135">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e40e2-136">規格需求</span><span class="sxs-lookup"><span data-stu-id="e40e2-136">Requirements</span></span>



| <span data-ttu-id="e40e2-137">需求</span><span class="sxs-lookup"><span data-stu-id="e40e2-137">Requirement</span></span> | <span data-ttu-id="e40e2-138">值</span><span class="sxs-lookup"><span data-stu-id="e40e2-138">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e40e2-139">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e40e2-139">Minimum supported client</span></span><br/> | <span data-ttu-id="e40e2-140">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e40e2-140">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="e40e2-141">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e40e2-141">Minimum supported server</span></span><br/> | <span data-ttu-id="e40e2-142">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e40e2-142">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="e40e2-143">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="e40e2-143">Type library</span></span><br/>             | <dl> <span data-ttu-id="e40e2-144"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e40e2-144"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="e40e2-145">DLL</span><span class="sxs-lookup"><span data-stu-id="e40e2-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e40e2-146"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e40e2-146"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="e40e2-147">IID</span><span class="sxs-lookup"><span data-stu-id="e40e2-147">IID</span></span><br/>                      | <span data-ttu-id="e40e2-148">IID \_ IMsTscAx 定義為8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span><span class="sxs-lookup"><span data-stu-id="e40e2-148">IID\_IMsTscAx is defined as 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="e40e2-149">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e40e2-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e40e2-150">**IMsRdpClient**</span><span class="sxs-lookup"><span data-stu-id="e40e2-150">**IMsRdpClient**</span></span>](imsrdpclient-interface.md)
</dt> <dt>

[<span data-ttu-id="e40e2-151">**IMsRdpClient2**</span><span class="sxs-lookup"><span data-stu-id="e40e2-151">**IMsRdpClient2**</span></span>](imsrdpclient2.md)
</dt> <dt>

[<span data-ttu-id="e40e2-152">**IMsRdpClient3**</span><span class="sxs-lookup"><span data-stu-id="e40e2-152">**IMsRdpClient3**</span></span>](imsrdpclient3.md)
</dt> <dt>

[<span data-ttu-id="e40e2-153">**IMsRdpClient4**</span><span class="sxs-lookup"><span data-stu-id="e40e2-153">**IMsRdpClient4**</span></span>](imsrdpclient4.md)
</dt> <dt>

[<span data-ttu-id="e40e2-154">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="e40e2-154">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="e40e2-155">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="e40e2-155">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="e40e2-156">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="e40e2-156">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="e40e2-157">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="e40e2-157">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="e40e2-158">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="e40e2-158">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="e40e2-159">**IMsTscAx**</span><span class="sxs-lookup"><span data-stu-id="e40e2-159">**IMsTscAx**</span></span>](imstscax-interface.md)
</dt> </dl>

 

 





