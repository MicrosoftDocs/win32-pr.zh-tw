---
title: IMsTscAx FullScreenTitle 屬性
description: 指定當控制項處於全螢幕模式時，所顯示的視窗標題。
ms.assetid: 441aea43-2d1c-44b7-a74f-e375e711fb4f
ms.tgt_platform: multiple
keywords:
- FullScreenTitle 屬性遠端桌面服務
- FullScreenTitle 屬性遠端桌面服務，IMsTscAx 介面
- IMsTscAx 介面遠端桌面服務，FullScreenTitle 屬性
- FullScreenTitle 屬性遠端桌面服務，IMsRdpClient 介面
- IMsRdpClient 介面遠端桌面服務，FullScreenTitle 屬性
- FullScreenTitle 屬性遠端桌面服務，IMsRdpClient2 介面
- IMsRdpClient2 介面遠端桌面服務，FullScreenTitle 屬性
- FullScreenTitle 屬性遠端桌面服務，IMsRdpClient3 介面
- IMsRdpClient3 介面遠端桌面服務，FullScreenTitle 屬性
- FullScreenTitle 屬性遠端桌面服務，IMsRdpClient4 介面
- IMsRdpClient4 介面遠端桌面服務，FullScreenTitle 屬性
- FullScreenTitle 屬性遠端桌面服務，IMsRdpClient5 介面
- IMsRdpClient5 介面遠端桌面服務，FullScreenTitle 屬性
- FullScreenTitle 屬性遠端桌面服務，IMsRdpClient6 介面
- IMsRdpClient6 介面遠端桌面服務，FullScreenTitle 屬性
- FullScreenTitle 屬性遠端桌面服務，IMsRdpClient7 介面
- IMsRdpClient7 介面遠端桌面服務，FullScreenTitle 屬性
- FullScreenTitle 屬性遠端桌面服務，IMsRdpClient8 介面
- IMsRdpClient8 介面遠端桌面服務，FullScreenTitle 屬性
- FullScreenTitle 屬性遠端桌面服務，IMsRdpClient9 介面
- IMsRdpClient9 介面遠端桌面服務，FullScreenTitle 屬性
topic_type:
- apiref
api_name:
- IMsTscAx.FullScreenTitle
- IMsTscAx.put_FullScreenTitle
- IMsRdpClient.FullScreenTitle
- IMsRdpClient.put_FullScreenTitle
- IMsRdpClient2.FullScreenTitle
- IMsRdpClient2.put_FullScreenTitle
- IMsRdpClient3.FullScreenTitle
- IMsRdpClient3.put_FullScreenTitle
- IMsRdpClient4.FullScreenTitle
- IMsRdpClient4.put_FullScreenTitle
- IMsRdpClient5.FullScreenTitle
- IMsRdpClient5.put_FullScreenTitle
- IMsRdpClient6.FullScreenTitle
- IMsRdpClient6.put_FullScreenTitle
- IMsRdpClient7.FullScreenTitle
- IMsRdpClient7.put_FullScreenTitle
- IMsRdpClient8.FullScreenTitle
- IMsRdpClient8.put_FullScreenTitle
- IMsRdpClient9.FullScreenTitle
- IMsRdpClient9.put_FullScreenTitle
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1384d1582f4f0089df55030c22471438575bd072
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104327"
---
# <a name="imstscaxfullscreentitle-property"></a><span data-ttu-id="aa211-124">IMsTscAx：： FullScreenTitle 屬性</span><span class="sxs-lookup"><span data-stu-id="aa211-124">IMsTscAx::FullScreenTitle property</span></span>

<span data-ttu-id="aa211-125">指定當控制項處於全螢幕模式時，所顯示的視窗標題。</span><span class="sxs-lookup"><span data-stu-id="aa211-125">Specifies the window title displayed when the control is in full-screen mode.</span></span>

<span data-ttu-id="aa211-126">此屬性是唯寫的。</span><span class="sxs-lookup"><span data-stu-id="aa211-126">This property is write-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="aa211-127">Syntax</span><span class="sxs-lookup"><span data-stu-id="aa211-127">Syntax</span></span>


```C++
HRESULT put_FullScreenTitle(
  [in] BSTR fullScreenTitle
);
```



## <a name="property-value"></a><span data-ttu-id="aa211-128">屬性值</span><span class="sxs-lookup"><span data-stu-id="aa211-128">Property value</span></span>

<span data-ttu-id="aa211-129">視窗標題。</span><span class="sxs-lookup"><span data-stu-id="aa211-129">The window title.</span></span> <span data-ttu-id="aa211-130">這個字串的最大長度為最大 \_ 路徑-1 個字元。</span><span class="sxs-lookup"><span data-stu-id="aa211-130">The maximum length of this string is MAX\_PATH-1 characters.</span></span>

## <a name="error-codes"></a><span data-ttu-id="aa211-131">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="aa211-131">Error codes</span></span>

<span data-ttu-id="aa211-132">如果成功，則傳回 **S \_ OK** 。</span><span class="sxs-lookup"><span data-stu-id="aa211-132">Return **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="aa211-133">備註</span><span class="sxs-lookup"><span data-stu-id="aa211-133">Remarks</span></span>

<span data-ttu-id="aa211-134">這個屬性是在以全螢幕模式開啟連接時，用來設定控制項視窗的標題。</span><span class="sxs-lookup"><span data-stu-id="aa211-134">This property is used to set the title of the control's window when the connection is opened in full-screen mode.</span></span> <span data-ttu-id="aa211-135">請勿將此屬性用於容器處理的全螢幕模式。</span><span class="sxs-lookup"><span data-stu-id="aa211-135">Do not use this property for container-handled full-screen mode.</span></span> <span data-ttu-id="aa211-136">當呼叫 [**IMsTscAdvancedSettings：:p \_ ContainerHandledFullScreen**](imstscadvancedsettings-containerhandledfullscreen.md) 方法時，[容器] 視窗會顯示視窗標題。</span><span class="sxs-lookup"><span data-stu-id="aa211-136">When the [**IMsTscAdvancedSettings::put\_ContainerHandledFullScreen**](imstscadvancedsettings-containerhandledfullscreen.md) method is called, the container window displays the window title.</span></span>

<span data-ttu-id="aa211-137">如需遠端桌面網頁連線的詳細資訊，請參閱 [遠端桌面網頁連線的需求](requirements-for-remote-desktop-web-connection.md)。</span><span class="sxs-lookup"><span data-stu-id="aa211-137">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="aa211-138">規格需求</span><span class="sxs-lookup"><span data-stu-id="aa211-138">Requirements</span></span>



| <span data-ttu-id="aa211-139">需求</span><span class="sxs-lookup"><span data-stu-id="aa211-139">Requirement</span></span> | <span data-ttu-id="aa211-140">值</span><span class="sxs-lookup"><span data-stu-id="aa211-140">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="aa211-141">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="aa211-141">Minimum supported client</span></span><br/> | <span data-ttu-id="aa211-142">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="aa211-142">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="aa211-143">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="aa211-143">Minimum supported server</span></span><br/> | <span data-ttu-id="aa211-144">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="aa211-144">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="aa211-145">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="aa211-145">Type library</span></span><br/>             | <dl> <span data-ttu-id="aa211-146"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="aa211-146"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="aa211-147">DLL</span><span class="sxs-lookup"><span data-stu-id="aa211-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="aa211-148"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="aa211-148"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="aa211-149">IID</span><span class="sxs-lookup"><span data-stu-id="aa211-149">IID</span></span><br/>                      | <span data-ttu-id="aa211-150">IID \_ IMsTscAx 定義為8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span><span class="sxs-lookup"><span data-stu-id="aa211-150">IID\_IMsTscAx is defined as 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="aa211-151">另請參閱</span><span class="sxs-lookup"><span data-stu-id="aa211-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aa211-152">**IMsRdpClient**</span><span class="sxs-lookup"><span data-stu-id="aa211-152">**IMsRdpClient**</span></span>](imsrdpclient-interface.md)
</dt> <dt>

[<span data-ttu-id="aa211-153">**IMsRdpClient2**</span><span class="sxs-lookup"><span data-stu-id="aa211-153">**IMsRdpClient2**</span></span>](imsrdpclient2.md)
</dt> <dt>

[<span data-ttu-id="aa211-154">**IMsRdpClient3**</span><span class="sxs-lookup"><span data-stu-id="aa211-154">**IMsRdpClient3**</span></span>](imsrdpclient3.md)
</dt> <dt>

[<span data-ttu-id="aa211-155">**IMsRdpClient4**</span><span class="sxs-lookup"><span data-stu-id="aa211-155">**IMsRdpClient4**</span></span>](imsrdpclient4.md)
</dt> <dt>

[<span data-ttu-id="aa211-156">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="aa211-156">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="aa211-157">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="aa211-157">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="aa211-158">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="aa211-158">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="aa211-159">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="aa211-159">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="aa211-160">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="aa211-160">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="aa211-161">**IMsTscAx**</span><span class="sxs-lookup"><span data-stu-id="aa211-161">**IMsTscAx**</span></span>](imstscax-interface.md)
</dt> </dl>

 

 





