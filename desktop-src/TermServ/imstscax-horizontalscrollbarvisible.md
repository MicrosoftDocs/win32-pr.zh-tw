---
title: IMsTscAx HorizontalScrollBarVisible 屬性
description: 指出控制項是否已顯示水準捲軸。
ms.assetid: d3c22c5f-321f-476e-bcdb-224eb988a7bb
ms.tgt_platform: multiple
keywords:
- HorizontalScrollBarVisible 屬性遠端桌面服務
- HorizontalScrollBarVisible 屬性遠端桌面服務，IMsTscAx 介面
- IMsTscAx 介面遠端桌面服務，HorizontalScrollBarVisible 屬性
- HorizontalScrollBarVisible 屬性遠端桌面服務，IMsRdpClient 介面
- IMsRdpClient 介面遠端桌面服務，HorizontalScrollBarVisible 屬性
- HorizontalScrollBarVisible 屬性遠端桌面服務，IMsRdpClient2 介面
- IMsRdpClient2 介面遠端桌面服務，HorizontalScrollBarVisible 屬性
- HorizontalScrollBarVisible 屬性遠端桌面服務，IMsRdpClient3 介面
- IMsRdpClient3 介面遠端桌面服務，HorizontalScrollBarVisible 屬性
- HorizontalScrollBarVisible 屬性遠端桌面服務，IMsRdpClient4 介面
- IMsRdpClient4 介面遠端桌面服務，HorizontalScrollBarVisible 屬性
- HorizontalScrollBarVisible 屬性遠端桌面服務，IMsRdpClient5 介面
- IMsRdpClient5 介面遠端桌面服務，HorizontalScrollBarVisible 屬性
- HorizontalScrollBarVisible 屬性遠端桌面服務，IMsRdpClient6 介面
- IMsRdpClient6 介面遠端桌面服務，HorizontalScrollBarVisible 屬性
- HorizontalScrollBarVisible 屬性遠端桌面服務，IMsRdpClient7 介面
- IMsRdpClient7 介面遠端桌面服務，HorizontalScrollBarVisible 屬性
- HorizontalScrollBarVisible 屬性遠端桌面服務，IMsRdpClient8 介面
- IMsRdpClient8 介面遠端桌面服務，HorizontalScrollBarVisible 屬性
- HorizontalScrollBarVisible 屬性遠端桌面服務，IMsRdpClient9 介面
- IMsRdpClient9 介面遠端桌面服務，HorizontalScrollBarVisible 屬性
topic_type:
- apiref
api_name:
- IMsTscAx.HorizontalScrollBarVisible
- IMsTscAx.get_HorizontalScrollBarVisible
- IMsRdpClient.HorizontalScrollBarVisible
- IMsRdpClient.get_HorizontalScrollBarVisible
- IMsRdpClient2.HorizontalScrollBarVisible
- IMsRdpClient2.get_HorizontalScrollBarVisible
- IMsRdpClient3.HorizontalScrollBarVisible
- IMsRdpClient3.get_HorizontalScrollBarVisible
- IMsRdpClient4.HorizontalScrollBarVisible
- IMsRdpClient4.get_HorizontalScrollBarVisible
- IMsRdpClient5.HorizontalScrollBarVisible
- IMsRdpClient5.get_HorizontalScrollBarVisible
- IMsRdpClient6.HorizontalScrollBarVisible
- IMsRdpClient6.get_HorizontalScrollBarVisible
- IMsRdpClient7.HorizontalScrollBarVisible
- IMsRdpClient7.get_HorizontalScrollBarVisible
- IMsRdpClient8.HorizontalScrollBarVisible
- IMsRdpClient8.get_HorizontalScrollBarVisible
- IMsRdpClient9.HorizontalScrollBarVisible
- IMsRdpClient9.get_HorizontalScrollBarVisible
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 08fa2abb97a28af013e5791bcbd643f3f479d5c6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025022"
---
# <a name="imstscaxhorizontalscrollbarvisible-property"></a><span data-ttu-id="2aa42-124">IMsTscAx：： HorizontalScrollBarVisible 屬性</span><span class="sxs-lookup"><span data-stu-id="2aa42-124">IMsTscAx::HorizontalScrollBarVisible property</span></span>

<span data-ttu-id="2aa42-125">指出控制項是否已顯示水準捲軸。</span><span class="sxs-lookup"><span data-stu-id="2aa42-125">Indicates whether the control has displayed a horizontal scroll bar.</span></span>

<span data-ttu-id="2aa42-126">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="2aa42-126">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="2aa42-127">語法</span><span class="sxs-lookup"><span data-stu-id="2aa42-127">Syntax</span></span>


```C++
HRESULT get_HorizontalScrollBarVisible(
  [out] BOOL *pfHScrollVisible
);
```



## <a name="property-value"></a><span data-ttu-id="2aa42-128">屬性值</span><span class="sxs-lookup"><span data-stu-id="2aa42-128">Property value</span></span>

<span data-ttu-id="2aa42-129">如果有水準捲軸，則此參數的值為 **TRUE** ，否則為 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="2aa42-129">The value of this parameter is **TRUE** if the horizontal scroll bar is visible, and **FALSE** otherwise.</span></span>

## <a name="error-codes"></a><span data-ttu-id="2aa42-130">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="2aa42-130">Error codes</span></span>

<span data-ttu-id="2aa42-131">如果成功，則傳回 **S \_ OK** 。</span><span class="sxs-lookup"><span data-stu-id="2aa42-131">Return **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="2aa42-132">備註</span><span class="sxs-lookup"><span data-stu-id="2aa42-132">Remarks</span></span>

<span data-ttu-id="2aa42-133">如果控制項的寬度小於桌面寬度，控制項會自動顯示水準捲軸。</span><span class="sxs-lookup"><span data-stu-id="2aa42-133">The control automatically displays a horizontal scroll bar if the width of the control is less than the desktop width.</span></span>

<span data-ttu-id="2aa42-134">如需遠端桌面網頁連線的詳細資訊，請參閱 [遠端桌面網頁連線的需求](requirements-for-remote-desktop-web-connection.md)。</span><span class="sxs-lookup"><span data-stu-id="2aa42-134">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="2aa42-135">規格需求</span><span class="sxs-lookup"><span data-stu-id="2aa42-135">Requirements</span></span>



| <span data-ttu-id="2aa42-136">需求</span><span class="sxs-lookup"><span data-stu-id="2aa42-136">Requirement</span></span> | <span data-ttu-id="2aa42-137">值</span><span class="sxs-lookup"><span data-stu-id="2aa42-137">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2aa42-138">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2aa42-138">Minimum supported client</span></span><br/> | <span data-ttu-id="2aa42-139">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2aa42-139">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="2aa42-140">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2aa42-140">Minimum supported server</span></span><br/> | <span data-ttu-id="2aa42-141">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2aa42-141">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="2aa42-142">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="2aa42-142">Type library</span></span><br/>             | <dl> <span data-ttu-id="2aa42-143"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2aa42-143"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="2aa42-144">DLL</span><span class="sxs-lookup"><span data-stu-id="2aa42-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2aa42-145"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2aa42-145"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="2aa42-146">IID</span><span class="sxs-lookup"><span data-stu-id="2aa42-146">IID</span></span><br/>                      | <span data-ttu-id="2aa42-147">IID \_ IMsTscAx 定義為8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span><span class="sxs-lookup"><span data-stu-id="2aa42-147">IID\_IMsTscAx is defined as 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="2aa42-148">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2aa42-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2aa42-149">**IMsRdpClient**</span><span class="sxs-lookup"><span data-stu-id="2aa42-149">**IMsRdpClient**</span></span>](imsrdpclient-interface.md)
</dt> <dt>

[<span data-ttu-id="2aa42-150">**IMsRdpClient2**</span><span class="sxs-lookup"><span data-stu-id="2aa42-150">**IMsRdpClient2**</span></span>](imsrdpclient2.md)
</dt> <dt>

[<span data-ttu-id="2aa42-151">**IMsRdpClient3**</span><span class="sxs-lookup"><span data-stu-id="2aa42-151">**IMsRdpClient3**</span></span>](imsrdpclient3.md)
</dt> <dt>

[<span data-ttu-id="2aa42-152">**IMsRdpClient4**</span><span class="sxs-lookup"><span data-stu-id="2aa42-152">**IMsRdpClient4**</span></span>](imsrdpclient4.md)
</dt> <dt>

[<span data-ttu-id="2aa42-153">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="2aa42-153">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="2aa42-154">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="2aa42-154">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="2aa42-155">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="2aa42-155">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="2aa42-156">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="2aa42-156">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="2aa42-157">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="2aa42-157">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="2aa42-158">**IMsTscAx**</span><span class="sxs-lookup"><span data-stu-id="2aa42-158">**IMsTscAx**</span></span>](imstscax-interface.md)
</dt> <dt>

[<span data-ttu-id="2aa42-159">**VerticalScrollBarVisible**</span><span class="sxs-lookup"><span data-stu-id="2aa42-159">**VerticalScrollBarVisible**</span></span>](imstscax-verticalscrollbarvisible.md)
</dt> </dl>

 

 





