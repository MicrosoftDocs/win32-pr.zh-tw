---
title: IMsTscAx DesktopWidth 屬性
description: 以圖元為單位，指定初始遠端桌面上的目前控制項寬度（以圖元為單位）。
ms.assetid: 3b349f6c-d068-4047-b8b5-29d022894729
ms.tgt_platform: multiple
keywords:
- DesktopWidth 屬性遠端桌面服務
- DesktopWidth 屬性遠端桌面服務，IMsTscAx 介面
- IMsTscAx 介面遠端桌面服務，DesktopWidth 屬性
- DesktopWidth 屬性遠端桌面服務，IMsRdpClient 介面
- IMsRdpClient 介面遠端桌面服務，DesktopWidth 屬性
- DesktopWidth 屬性遠端桌面服務，IMsRdpClient2 介面
- IMsRdpClient2 介面遠端桌面服務，DesktopWidth 屬性
- DesktopWidth 屬性遠端桌面服務，IMsRdpClient3 介面
- IMsRdpClient3 介面遠端桌面服務，DesktopWidth 屬性
- DesktopWidth 屬性遠端桌面服務，IMsRdpClient4 介面
- IMsRdpClient4 介面遠端桌面服務，DesktopWidth 屬性
- DesktopWidth 屬性遠端桌面服務，IMsRdpClient5 介面
- IMsRdpClient5 介面遠端桌面服務，DesktopWidth 屬性
- DesktopWidth 屬性遠端桌面服務，IMsRdpClient6 介面
- IMsRdpClient6 介面遠端桌面服務，DesktopWidth 屬性
- DesktopWidth 屬性遠端桌面服務，IMsRdpClient7 介面
- IMsRdpClient7 介面遠端桌面服務，DesktopWidth 屬性
- DesktopWidth 屬性遠端桌面服務，IMsRdpClient8 介面
- IMsRdpClient8 介面遠端桌面服務，DesktopWidth 屬性
- DesktopWidth 屬性遠端桌面服務，IMsRdpClient9 介面
- IMsRdpClient9 介面遠端桌面服務，DesktopWidth 屬性
topic_type:
- apiref
api_name:
- IMsTscAx.DesktopWidth
- IMsTscAx.get_DesktopWidth
- IMsTscAx.put_DesktopWidth
- IMsRdpClient.DesktopWidth
- IMsRdpClient.get_DesktopWidth
- IMsRdpClient.put_DesktopWidth
- IMsRdpClient2.DesktopWidth
- IMsRdpClient2.get_DesktopWidth
- IMsRdpClient2.put_DesktopWidth
- IMsRdpClient3.DesktopWidth
- IMsRdpClient3.get_DesktopWidth
- IMsRdpClient3.put_DesktopWidth
- IMsRdpClient4.DesktopWidth
- IMsRdpClient4.get_DesktopWidth
- IMsRdpClient4.put_DesktopWidth
- IMsRdpClient5.DesktopWidth
- IMsRdpClient5.get_DesktopWidth
- IMsRdpClient5.put_DesktopWidth
- IMsRdpClient6.DesktopWidth
- IMsRdpClient6.get_DesktopWidth
- IMsRdpClient6.put_DesktopWidth
- IMsRdpClient7.DesktopWidth
- IMsRdpClient7.get_DesktopWidth
- IMsRdpClient7.put_DesktopWidth
- IMsRdpClient8.DesktopWidth
- IMsRdpClient8.get_DesktopWidth
- IMsRdpClient8.put_DesktopWidth
- IMsRdpClient9.DesktopWidth
- IMsRdpClient9.get_DesktopWidth
- IMsRdpClient9.put_DesktopWidth
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 16cd1391c6aeb27d9ec0f87317b06e9084337fbb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508555"
---
# <a name="imstscaxdesktopwidth-property"></a><span data-ttu-id="bd821-124">IMsTscAx：:D esktopWidth 屬性</span><span class="sxs-lookup"><span data-stu-id="bd821-124">IMsTscAx::DesktopWidth property</span></span>

<span data-ttu-id="bd821-125">以圖元為單位，指定初始遠端桌面上的目前控制項寬度（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="bd821-125">Specifies the current control's width, in pixels, on the initial remote desktop.</span></span>

<span data-ttu-id="bd821-126">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="bd821-126">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="bd821-127">Syntax</span><span class="sxs-lookup"><span data-stu-id="bd821-127">Syntax</span></span>


```C++
HRESULT put_DesktopWidth(
  [in]  LONG newVal
);

HRESULT get_DesktopWidth(
  [out] LONG *pVal
);
```



## <a name="property-value"></a><span data-ttu-id="bd821-128">屬性值</span><span class="sxs-lookup"><span data-stu-id="bd821-128">Property value</span></span>

<span data-ttu-id="bd821-129">新的寬度（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="bd821-129">The new width, in pixels.</span></span>

## <a name="error-codes"></a><span data-ttu-id="bd821-130">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="bd821-130">Error codes</span></span>

<span data-ttu-id="bd821-131">如果成功，則傳回 **S \_ OK** 。</span><span class="sxs-lookup"><span data-stu-id="bd821-131">Return **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="bd821-132">備註</span><span class="sxs-lookup"><span data-stu-id="bd821-132">Remarks</span></span>

<span data-ttu-id="bd821-133">設定 **DesktopWidth** 屬性是選擇性的，但必須在呼叫 [**Connect**](imstscax-connect.md) 方法之前設定。</span><span class="sxs-lookup"><span data-stu-id="bd821-133">Setting the **DesktopWidth** property is optional, but it must be set before calling the [**Connect**](imstscax-connect.md) method.</span></span> <span data-ttu-id="bd821-134">如果未指定桌面寬度，或設定為零，則會將桌面寬度設定為控制項的寬度。</span><span class="sxs-lookup"><span data-stu-id="bd821-134">If a desktop width is not specified, or is set to zero, the desktop width is set to the width of the control.</span></span> <span data-ttu-id="bd821-135">最小值和最大值取決於遠端桌面用戶端的作業系統版本。</span><span class="sxs-lookup"><span data-stu-id="bd821-135">The minimum and maximum values are dependent upon the operating system version of the Remote Desktop client.</span></span>

<dl> <dt>

<span data-ttu-id="bd821-136"><span id="_"></span>Windows 8/Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="bd821-136"><span id="_"></span>Windows 8/Windows Server 2012</span></span>
</dt> <dd>

<span data-ttu-id="bd821-137">200最小值8192，最大值</span><span class="sxs-lookup"><span data-stu-id="bd821-137">200 minimum, 8192 maximum</span></span>

</dd> <dt>

<span data-ttu-id="bd821-138"><span id="_"></span>Windows 7/Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bd821-138"><span id="_"></span>Windows 7/Windows Server 2008</span></span>
</dt> <dd>

<span data-ttu-id="bd821-139">200最小值2048，最大值</span><span class="sxs-lookup"><span data-stu-id="bd821-139">200 minimum, 2048 maximum</span></span>

</dd> <dt>

<span data-ttu-id="bd821-140">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="bd821-140">Windows Vista</span></span>
</dt> <dd>

<span data-ttu-id="bd821-141">200最小值1200，最大值</span><span class="sxs-lookup"><span data-stu-id="bd821-141">200 minimum, 1200 maximum</span></span>

</dd> </dl>

<span data-ttu-id="bd821-142">建立連線之後，控制項寬度的任何變更都不會變更遠端桌面的寬度。</span><span class="sxs-lookup"><span data-stu-id="bd821-142">After a connection is established, any changes to the control's width do not change the width of the remote desktop.</span></span> <span data-ttu-id="bd821-143">相反地，控制項會在適當的情況下，顯示捲軸或將遠端桌面置中。</span><span class="sxs-lookup"><span data-stu-id="bd821-143">Instead, the control brings up scroll bars or centers the remote desktop, as appropriate.</span></span> <span data-ttu-id="bd821-144">若要變更使用中連接的桌面大小，請使用 [**IMsRdpClient8：： Reconnect**](imsrdpclient8-reconnect.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="bd821-144">To change the desktop size of an active connection, use the [**IMsRdpClient8::Reconnect**](imsrdpclient8-reconnect.md) method.</span></span>

<span data-ttu-id="bd821-145">如需遠端桌面網頁連線的詳細資訊，請參閱 [遠端桌面網頁連線的需求](requirements-for-remote-desktop-web-connection.md)。</span><span class="sxs-lookup"><span data-stu-id="bd821-145">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="bd821-146">規格需求</span><span class="sxs-lookup"><span data-stu-id="bd821-146">Requirements</span></span>



| <span data-ttu-id="bd821-147">需求</span><span class="sxs-lookup"><span data-stu-id="bd821-147">Requirement</span></span> | <span data-ttu-id="bd821-148">值</span><span class="sxs-lookup"><span data-stu-id="bd821-148">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="bd821-149">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="bd821-149">Minimum supported client</span></span><br/> | <span data-ttu-id="bd821-150">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="bd821-150">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="bd821-151">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="bd821-151">Minimum supported server</span></span><br/> | <span data-ttu-id="bd821-152">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bd821-152">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="bd821-153">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="bd821-153">Type library</span></span><br/>             | <dl> <span data-ttu-id="bd821-154"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bd821-154"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="bd821-155">DLL</span><span class="sxs-lookup"><span data-stu-id="bd821-155">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bd821-156"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bd821-156"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="bd821-157">IID</span><span class="sxs-lookup"><span data-stu-id="bd821-157">IID</span></span><br/>                      | <span data-ttu-id="bd821-158">IID \_ IMsTscAx 定義為8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span><span class="sxs-lookup"><span data-stu-id="bd821-158">IID\_IMsTscAx is defined as 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="bd821-159">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bd821-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bd821-160">**IMsRdpClient**</span><span class="sxs-lookup"><span data-stu-id="bd821-160">**IMsRdpClient**</span></span>](imsrdpclient-interface.md)
</dt> <dt>

[<span data-ttu-id="bd821-161">**IMsRdpClient2**</span><span class="sxs-lookup"><span data-stu-id="bd821-161">**IMsRdpClient2**</span></span>](imsrdpclient2.md)
</dt> <dt>

[<span data-ttu-id="bd821-162">**IMsRdpClient3**</span><span class="sxs-lookup"><span data-stu-id="bd821-162">**IMsRdpClient3**</span></span>](imsrdpclient3.md)
</dt> <dt>

[<span data-ttu-id="bd821-163">**IMsRdpClient4**</span><span class="sxs-lookup"><span data-stu-id="bd821-163">**IMsRdpClient4**</span></span>](imsrdpclient4.md)
</dt> <dt>

[<span data-ttu-id="bd821-164">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="bd821-164">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="bd821-165">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="bd821-165">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="bd821-166">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="bd821-166">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="bd821-167">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="bd821-167">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="bd821-168">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="bd821-168">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="bd821-169">**IMsTscAx**</span><span class="sxs-lookup"><span data-stu-id="bd821-169">**IMsTscAx**</span></span>](imstscax-interface.md)
</dt> </dl>

 

 





