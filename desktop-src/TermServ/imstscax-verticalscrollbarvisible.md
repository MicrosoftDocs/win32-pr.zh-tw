---
title: IMsTscAx VerticalScrollBarVisible 屬性
description: 指出控制項是否顯示垂直捲動條。
ms.assetid: b31e2db3-b367-4900-a2c6-51fd794341c2
ms.tgt_platform: multiple
keywords:
- VerticalScrollBarVisible 屬性遠端桌面服務
- VerticalScrollBarVisible 屬性遠端桌面服務，IMsTscAx 介面
- IMsTscAx 介面遠端桌面服務，VerticalScrollBarVisible 屬性
- VerticalScrollBarVisible 屬性遠端桌面服務，IMsRdpClient 介面
- IMsRdpClient 介面遠端桌面服務，VerticalScrollBarVisible 屬性
- VerticalScrollBarVisible 屬性遠端桌面服務，IMsRdpClient2 介面
- IMsRdpClient2 介面遠端桌面服務，VerticalScrollBarVisible 屬性
- VerticalScrollBarVisible 屬性遠端桌面服務，IMsRdpClient3 介面
- IMsRdpClient3 介面遠端桌面服務，VerticalScrollBarVisible 屬性
- VerticalScrollBarVisible 屬性遠端桌面服務，IMsRdpClient4 介面
- IMsRdpClient4 介面遠端桌面服務，VerticalScrollBarVisible 屬性
- VerticalScrollBarVisible 屬性遠端桌面服務，IMsRdpClient5 介面
- IMsRdpClient5 介面遠端桌面服務，VerticalScrollBarVisible 屬性
- VerticalScrollBarVisible 屬性遠端桌面服務，IMsRdpClient6 介面
- IMsRdpClient6 介面遠端桌面服務，VerticalScrollBarVisible 屬性
- VerticalScrollBarVisible 屬性遠端桌面服務，IMsRdpClient7 介面
- IMsRdpClient7 介面遠端桌面服務，VerticalScrollBarVisible 屬性
- VerticalScrollBarVisible 屬性遠端桌面服務，IMsRdpClient8 介面
- IMsRdpClient8 介面遠端桌面服務，VerticalScrollBarVisible 屬性
- VerticalScrollBarVisible 屬性遠端桌面服務，IMsRdpClient9 介面
- IMsRdpClient9 介面遠端桌面服務，VerticalScrollBarVisible 屬性
topic_type:
- apiref
api_name:
- IMsTscAx.VerticalScrollBarVisible
- IMsTscAx.get_VerticalScrollBarVisible
- IMsRdpClient.VerticalScrollBarVisible
- IMsRdpClient.get_VerticalScrollBarVisible
- IMsRdpClient2.VerticalScrollBarVisible
- IMsRdpClient2.get_VerticalScrollBarVisible
- IMsRdpClient3.VerticalScrollBarVisible
- IMsRdpClient3.get_VerticalScrollBarVisible
- IMsRdpClient4.VerticalScrollBarVisible
- IMsRdpClient4.get_VerticalScrollBarVisible
- IMsRdpClient5.VerticalScrollBarVisible
- IMsRdpClient5.get_VerticalScrollBarVisible
- IMsRdpClient6.VerticalScrollBarVisible
- IMsRdpClient6.get_VerticalScrollBarVisible
- IMsRdpClient7.VerticalScrollBarVisible
- IMsRdpClient7.get_VerticalScrollBarVisible
- IMsRdpClient8.VerticalScrollBarVisible
- IMsRdpClient8.get_VerticalScrollBarVisible
- IMsRdpClient9.VerticalScrollBarVisible
- IMsRdpClient9.get_VerticalScrollBarVisible
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1365a0ab6d4a1411d78496cf157f3bc49fe5db15
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464681"
---
# <a name="imstscaxverticalscrollbarvisible-property"></a><span data-ttu-id="db88f-124">IMsTscAx：： VerticalScrollBarVisible 屬性</span><span class="sxs-lookup"><span data-stu-id="db88f-124">IMsTscAx::VerticalScrollBarVisible property</span></span>

<span data-ttu-id="db88f-125">指出控制項是否顯示垂直捲動條。</span><span class="sxs-lookup"><span data-stu-id="db88f-125">Indicates whether the control displays a vertical scroll bar.</span></span>

<span data-ttu-id="db88f-126">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="db88f-126">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="db88f-127">語法</span><span class="sxs-lookup"><span data-stu-id="db88f-127">Syntax</span></span>


```C++
HRESULT get_VerticalScrollBarVisible(
  [out] BOOL *pfVScrollVisible
);
```



## <a name="property-value"></a><span data-ttu-id="db88f-128">屬性值</span><span class="sxs-lookup"><span data-stu-id="db88f-128">Property value</span></span>

<span data-ttu-id="db88f-129">如果可以看到垂直捲動條，則此參數的值為 **TRUE** ，否則為 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="db88f-129">The value of this parameter is **TRUE** if the vertical scroll bar is visible, and **FALSE** otherwise.</span></span>

## <a name="error-codes"></a><span data-ttu-id="db88f-130">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="db88f-130">Error codes</span></span>

<span data-ttu-id="db88f-131">如果成功，則傳回 **S \_ OK** 。</span><span class="sxs-lookup"><span data-stu-id="db88f-131">Return **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="db88f-132">備註</span><span class="sxs-lookup"><span data-stu-id="db88f-132">Remarks</span></span>

<span data-ttu-id="db88f-133">如果目前控制項的高度小於桌面的高度，控制項會自動顯示垂直捲動條。</span><span class="sxs-lookup"><span data-stu-id="db88f-133">The control automatically displays a vertical scroll bar if the height of the current control is less than the height of the desktop.</span></span>

<span data-ttu-id="db88f-134">如需遠端桌面網頁連線的詳細資訊，請參閱 [遠端桌面網頁連線的需求](requirements-for-remote-desktop-web-connection.md)。</span><span class="sxs-lookup"><span data-stu-id="db88f-134">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="db88f-135">規格需求</span><span class="sxs-lookup"><span data-stu-id="db88f-135">Requirements</span></span>



| <span data-ttu-id="db88f-136">需求</span><span class="sxs-lookup"><span data-stu-id="db88f-136">Requirement</span></span> | <span data-ttu-id="db88f-137">值</span><span class="sxs-lookup"><span data-stu-id="db88f-137">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="db88f-138">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="db88f-138">Minimum supported client</span></span><br/> | <span data-ttu-id="db88f-139">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="db88f-139">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="db88f-140">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="db88f-140">Minimum supported server</span></span><br/> | <span data-ttu-id="db88f-141">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="db88f-141">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="db88f-142">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="db88f-142">Type library</span></span><br/>             | <dl> <span data-ttu-id="db88f-143"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="db88f-143"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="db88f-144">DLL</span><span class="sxs-lookup"><span data-stu-id="db88f-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="db88f-145"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="db88f-145"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="db88f-146">IID</span><span class="sxs-lookup"><span data-stu-id="db88f-146">IID</span></span><br/>                      | <span data-ttu-id="db88f-147">IID \_ IMsTscAx 定義為8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span><span class="sxs-lookup"><span data-stu-id="db88f-147">IID\_IMsTscAx is defined as 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="db88f-148">另請參閱</span><span class="sxs-lookup"><span data-stu-id="db88f-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="db88f-149">**IMsRdpClient**</span><span class="sxs-lookup"><span data-stu-id="db88f-149">**IMsRdpClient**</span></span>](imsrdpclient-interface.md)
</dt> <dt>

[<span data-ttu-id="db88f-150">**IMsRdpClient2**</span><span class="sxs-lookup"><span data-stu-id="db88f-150">**IMsRdpClient2**</span></span>](imsrdpclient2.md)
</dt> <dt>

[<span data-ttu-id="db88f-151">**IMsRdpClient3**</span><span class="sxs-lookup"><span data-stu-id="db88f-151">**IMsRdpClient3**</span></span>](imsrdpclient3.md)
</dt> <dt>

[<span data-ttu-id="db88f-152">**IMsRdpClient4**</span><span class="sxs-lookup"><span data-stu-id="db88f-152">**IMsRdpClient4**</span></span>](imsrdpclient4.md)
</dt> <dt>

[<span data-ttu-id="db88f-153">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="db88f-153">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="db88f-154">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="db88f-154">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="db88f-155">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="db88f-155">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="db88f-156">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="db88f-156">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="db88f-157">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="db88f-157">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="db88f-158">**HorizontalScrollBarVisible**</span><span class="sxs-lookup"><span data-stu-id="db88f-158">**HorizontalScrollBarVisible**</span></span>](imstscax-horizontalscrollbarvisible.md)
</dt> <dt>

[<span data-ttu-id="db88f-159">**IMsTscAx**</span><span class="sxs-lookup"><span data-stu-id="db88f-159">**IMsTscAx**</span></span>](imstscax-interface.md)
</dt> </dl>

 

 





