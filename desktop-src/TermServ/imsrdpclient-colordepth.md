---
title: IMsRdpClient ColorDepth 屬性
description: 色彩深度 (控制項連接的每圖元) 位數。
ms.assetid: 9ba4d8fe-20cd-40e9-a71a-0dce0ddd29fc
ms.tgt_platform: multiple
keywords:
- ColorDepth 屬性遠端桌面服務
- ColorDepth 屬性遠端桌面服務，IMsRdpClient 介面
- IMsRdpClient 介面遠端桌面服務，ColorDepth 屬性
- ColorDepth 屬性遠端桌面服務，IMsRdpClient2 介面
- IMsRdpClient2 介面遠端桌面服務，ColorDepth 屬性
- ColorDepth 屬性遠端桌面服務，IMsRdpClient3 介面
- IMsRdpClient3 介面遠端桌面服務，ColorDepth 屬性
- ColorDepth 屬性遠端桌面服務，IMsRdpClient4 介面
- IMsRdpClient4 介面遠端桌面服務，ColorDepth 屬性
- ColorDepth 屬性遠端桌面服務，IMsRdpClient5 介面
- IMsRdpClient5 介面遠端桌面服務，ColorDepth 屬性
- ColorDepth 屬性遠端桌面服務，IMsRdpClient6 介面
- IMsRdpClient6 介面遠端桌面服務，ColorDepth 屬性
- ColorDepth 屬性遠端桌面服務，IMsRdpClient7 介面
- IMsRdpClient7 介面遠端桌面服務，ColorDepth 屬性
- ColorDepth 屬性遠端桌面服務，IMsRdpClient8 介面
- IMsRdpClient8 介面遠端桌面服務，ColorDepth 屬性
- ColorDepth 屬性遠端桌面服務，IMsRdpClient9 介面
- IMsRdpClient9 介面遠端桌面服務，ColorDepth 屬性
- ColorDepth 屬性遠端桌面服務，IMsRdpClient10 介面
- IMsRdpClient10 介面遠端桌面服務，ColorDepth 屬性
topic_type:
- apiref
api_name:
- IMsRdpClient.ColorDepth
- IMsRdpClient.get_ColorDepth
- IMsRdpClient.put_ColorDepth
- IMsRdpClient2.ColorDepth
- IMsRdpClient2.get_ColorDepth
- IMsRdpClient2.put_ColorDepth
- IMsRdpClient3.ColorDepth
- IMsRdpClient3.get_ColorDepth
- IMsRdpClient3.put_ColorDepth
- IMsRdpClient4.ColorDepth
- IMsRdpClient4.get_ColorDepth
- IMsRdpClient4.put_ColorDepth
- IMsRdpClient5.ColorDepth
- IMsRdpClient5.get_ColorDepth
- IMsRdpClient5.put_ColorDepth
- IMsRdpClient6.ColorDepth
- IMsRdpClient6.get_ColorDepth
- IMsRdpClient6.put_ColorDepth
- IMsRdpClient7.ColorDepth
- IMsRdpClient7.get_ColorDepth
- IMsRdpClient7.put_ColorDepth
- IMsRdpClient8.ColorDepth
- IMsRdpClient8.get_ColorDepth
- IMsRdpClient8.put_ColorDepth
- IMsRdpClient9.ColorDepth
- IMsRdpClient9.get_ColorDepth
- IMsRdpClient9.put_ColorDepth
- IMsRdpClient10.ColorDepth
- IMsRdpClient10.get_ColorDepth
- IMsRdpClient10.put_ColorDepth
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d5099deff3913d23173a466245cbf08fd5b95a6a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105876"
---
# <a name="imsrdpclientcolordepth-property"></a><span data-ttu-id="aa97a-124">IMsRdpClient：： ColorDepth 屬性</span><span class="sxs-lookup"><span data-stu-id="aa97a-124">IMsRdpClient::ColorDepth property</span></span>

<span data-ttu-id="aa97a-125">色彩深度 (控制項連接的每圖元) 位數。</span><span class="sxs-lookup"><span data-stu-id="aa97a-125">The color depth (in bits per pixel) for the control's connection.</span></span>

<span data-ttu-id="aa97a-126">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="aa97a-126">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="aa97a-127">Syntax</span><span class="sxs-lookup"><span data-stu-id="aa97a-127">Syntax</span></span>


```C++
HRESULT put_ColorDepth(
  [in]  LONG colorDepth
);

HRESULT get_ColorDepth(
  [out] LONG pcolorDepth
);
```



## <a name="property-value"></a><span data-ttu-id="aa97a-128">屬性值</span><span class="sxs-lookup"><span data-stu-id="aa97a-128">Property value</span></span>

<span data-ttu-id="aa97a-129">色彩深度。</span><span class="sxs-lookup"><span data-stu-id="aa97a-129">The color depth.</span></span> <span data-ttu-id="aa97a-130">值包括8、15、16、24和32位的每個圖元。</span><span class="sxs-lookup"><span data-stu-id="aa97a-130">Values include 8, 15, 16, 24, and 32 bits per pixel.</span></span>

## <a name="error-codes"></a><span data-ttu-id="aa97a-131">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="aa97a-131">Error codes</span></span>

<span data-ttu-id="aa97a-132">如果方法成功，則會傳回 **S \_ OK** 。</span><span class="sxs-lookup"><span data-stu-id="aa97a-132">If the methods succeed, **S\_OK** is returned.</span></span> <span data-ttu-id="aa97a-133">任何其他 **HRESULT** 值都表示呼叫失敗。</span><span class="sxs-lookup"><span data-stu-id="aa97a-133">Any other **HRESULT** value indicates that the call failed.</span></span>

## <a name="remarks"></a><span data-ttu-id="aa97a-134">備註</span><span class="sxs-lookup"><span data-stu-id="aa97a-134">Remarks</span></span>

<span data-ttu-id="aa97a-135">連接控制項時，無法設定這個屬性。</span><span class="sxs-lookup"><span data-stu-id="aa97a-135">This property cannot be set when the control is connected.</span></span>

<span data-ttu-id="aa97a-136">如需遠端桌面網頁連線的詳細資訊，請參閱 [遠端桌面網頁連線的需求](requirements-for-remote-desktop-web-connection.md)。</span><span class="sxs-lookup"><span data-stu-id="aa97a-136">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="aa97a-137">規格需求</span><span class="sxs-lookup"><span data-stu-id="aa97a-137">Requirements</span></span>



| <span data-ttu-id="aa97a-138">需求</span><span class="sxs-lookup"><span data-stu-id="aa97a-138">Requirement</span></span> | <span data-ttu-id="aa97a-139">值</span><span class="sxs-lookup"><span data-stu-id="aa97a-139">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="aa97a-140">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="aa97a-140">Minimum supported client</span></span><br/> | <span data-ttu-id="aa97a-141">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="aa97a-141">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="aa97a-142">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="aa97a-142">Minimum supported server</span></span><br/> | <span data-ttu-id="aa97a-143">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="aa97a-143">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="aa97a-144">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="aa97a-144">Type library</span></span><br/>             | <dl> <span data-ttu-id="aa97a-145"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="aa97a-145"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="aa97a-146">DLL</span><span class="sxs-lookup"><span data-stu-id="aa97a-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="aa97a-147"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="aa97a-147"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="aa97a-148">IID</span><span class="sxs-lookup"><span data-stu-id="aa97a-148">IID</span></span><br/>                      | <span data-ttu-id="aa97a-149">IID \_ IMsRdpClient 定義為92b4a539-7115-4b7c-a5a9-e5d9efc2780a</span><span class="sxs-lookup"><span data-stu-id="aa97a-149">IID\_IMsRdpClient is defined as 92b4a539-7115-4b7c-a5a9-e5d9efc2780a</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="aa97a-150">另請參閱</span><span class="sxs-lookup"><span data-stu-id="aa97a-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aa97a-151">**IMsRdpClient**</span><span class="sxs-lookup"><span data-stu-id="aa97a-151">**IMsRdpClient**</span></span>](imsrdpclient-interface.md)
</dt> <dt>

[<span data-ttu-id="aa97a-152">**IMsRdpClient2**</span><span class="sxs-lookup"><span data-stu-id="aa97a-152">**IMsRdpClient2**</span></span>](imsrdpclient2.md)
</dt> <dt>

[<span data-ttu-id="aa97a-153">**IMsRdpClient3**</span><span class="sxs-lookup"><span data-stu-id="aa97a-153">**IMsRdpClient3**</span></span>](imsrdpclient3.md)
</dt> <dt>

[<span data-ttu-id="aa97a-154">**IMsRdpClient4**</span><span class="sxs-lookup"><span data-stu-id="aa97a-154">**IMsRdpClient4**</span></span>](imsrdpclient4.md)
</dt> <dt>

[<span data-ttu-id="aa97a-155">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="aa97a-155">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="aa97a-156">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="aa97a-156">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="aa97a-157">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="aa97a-157">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="aa97a-158">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="aa97a-158">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="aa97a-159">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="aa97a-159">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="aa97a-160">**IMsRdpClient10**</span><span class="sxs-lookup"><span data-stu-id="aa97a-160">**IMsRdpClient10**</span></span>](imsrdpclient10.md)
</dt> </dl>

 

 





