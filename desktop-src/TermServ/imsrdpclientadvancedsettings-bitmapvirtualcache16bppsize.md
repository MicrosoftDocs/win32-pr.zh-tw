---
title: IMsRdpClientAdvancedSettings BitmapVirtualCache16BppSize 屬性
description: 指定持續性點陣圖快取檔案的大小（以 mb 為單位），以用於每圖元15和16位的高色彩設定。
ms.assetid: f2558c88-d60f-4be3-9941-8e0e18bbb778
ms.tgt_platform: multiple
keywords:
- BitmapVirtualCache16BppSize 屬性遠端桌面服務
- BitmapVirtualCache16BppSize 屬性遠端桌面服務，IMsRdpClientAdvancedSettings 介面
- IMsRdpClientAdvancedSettings 介面遠端桌面服務，BitmapVirtualCache16BppSize 屬性
- BitmapVirtualCache16BppSize 屬性遠端桌面服務，IMsRdpClientAdvancedSettings2 介面
- IMsRdpClientAdvancedSettings2 介面遠端桌面服務，BitmapVirtualCache16BppSize 屬性
- BitmapVirtualCache16BppSize 屬性遠端桌面服務，IMsRdpClientAdvancedSettings3 介面
- IMsRdpClientAdvancedSettings3 介面遠端桌面服務，BitmapVirtualCache16BppSize 屬性
- BitmapVirtualCache16BppSize 屬性遠端桌面服務，IMsRdpClientAdvancedSettings4 介面
- IMsRdpClientAdvancedSettings4 介面遠端桌面服務，BitmapVirtualCache16BppSize 屬性
- BitmapVirtualCache16BppSize 屬性遠端桌面服務，IMsRdpClientAdvancedSettings5 介面
- IMsRdpClientAdvancedSettings5 介面遠端桌面服務，BitmapVirtualCache16BppSize 屬性
- BitmapVirtualCache16BppSize 屬性遠端桌面服務，IMsRdpClientAdvancedSettings6 介面
- IMsRdpClientAdvancedSettings6 介面遠端桌面服務，BitmapVirtualCache16BppSize 屬性
- BitmapVirtualCache16BppSize 屬性遠端桌面服務，IMsRdpClientAdvancedSettings7 介面
- IMsRdpClientAdvancedSettings7 介面遠端桌面服務，BitmapVirtualCache16BppSize 屬性
- BitmapVirtualCache16BppSize 屬性遠端桌面服務，IMsRdpClientAdvancedSettings8 介面
- IMsRdpClientAdvancedSettings8 介面遠端桌面服務，BitmapVirtualCache16BppSize 屬性
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.BitmapVirtualCache16BppSize
- IMsRdpClientAdvancedSettings.get_BitmapVirtualCache16BppSize
- IMsRdpClientAdvancedSettings.put_BitmapVirtualCache16BppSize
- IMsRdpClientAdvancedSettings2.BitmapVirtualCache16BppSize
- IMsRdpClientAdvancedSettings2.get_BitmapVirtualCache16BppSize
- IMsRdpClientAdvancedSettings2.put_BitmapVirtualCache16BppSize
- IMsRdpClientAdvancedSettings3.BitmapVirtualCache16BppSize
- IMsRdpClientAdvancedSettings3.get_BitmapVirtualCache16BppSize
- IMsRdpClientAdvancedSettings3.put_BitmapVirtualCache16BppSize
- IMsRdpClientAdvancedSettings4.BitmapVirtualCache16BppSize
- IMsRdpClientAdvancedSettings4.get_BitmapVirtualCache16BppSize
- IMsRdpClientAdvancedSettings4.put_BitmapVirtualCache16BppSize
- IMsRdpClientAdvancedSettings5.BitmapVirtualCache16BppSize
- IMsRdpClientAdvancedSettings5.get_BitmapVirtualCache16BppSize
- IMsRdpClientAdvancedSettings5.put_BitmapVirtualCache16BppSize
- IMsRdpClientAdvancedSettings6.BitmapVirtualCache16BppSize
- IMsRdpClientAdvancedSettings6.get_BitmapVirtualCache16BppSize
- IMsRdpClientAdvancedSettings6.put_BitmapVirtualCache16BppSize
- IMsRdpClientAdvancedSettings7.BitmapVirtualCache16BppSize
- IMsRdpClientAdvancedSettings7.get_BitmapVirtualCache16BppSize
- IMsRdpClientAdvancedSettings7.put_BitmapVirtualCache16BppSize
- IMsRdpClientAdvancedSettings8.BitmapVirtualCache16BppSize
- IMsRdpClientAdvancedSettings8.get_BitmapVirtualCache16BppSize
- IMsRdpClientAdvancedSettings8.put_BitmapVirtualCache16BppSize
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5fd0a11a1cf3b313c1f6f2c12d1a73b61c6f45a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106967714"
---
# <a name="imsrdpclientadvancedsettingsbitmapvirtualcache16bppsize-property"></a><span data-ttu-id="2587e-120">IMsRdpClientAdvancedSettings：： BitmapVirtualCache16BppSize 屬性</span><span class="sxs-lookup"><span data-stu-id="2587e-120">IMsRdpClientAdvancedSettings::BitmapVirtualCache16BppSize property</span></span>

<span data-ttu-id="2587e-121">指定持續性點陣圖快取檔案的大小（以 mb 為單位），以用於每圖元15和16位的高色彩設定。</span><span class="sxs-lookup"><span data-stu-id="2587e-121">Specifies the size, in megabytes, of the persistent bitmap cache file to use for the 15 and 16 bits-per-pixel high-color settings.</span></span>

<span data-ttu-id="2587e-122">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="2587e-122">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="2587e-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="2587e-123">Syntax</span></span>


```C++
HRESULT put_BitmapVirtualCache16BppSize(
  [in]  LONG bitmapVirtualCache16BppSize
);

HRESULT get_BitmapVirtualCache16BppSize(
  [out] LONG *pbitmapVirtualCache16BppSize
);
```



## <a name="property-value"></a><span data-ttu-id="2587e-124">屬性值</span><span class="sxs-lookup"><span data-stu-id="2587e-124">Property value</span></span>

<span data-ttu-id="2587e-125">新的快取大小。</span><span class="sxs-lookup"><span data-stu-id="2587e-125">The new cache size.</span></span> <span data-ttu-id="2587e-126">有效值為1到32（含），預設值為20。</span><span class="sxs-lookup"><span data-stu-id="2587e-126">The valid values are 1 to 32 inclusive, and the default value is 20.</span></span> <span data-ttu-id="2587e-127">請注意，所有虛擬快取檔案的大小上限為 128 MB。</span><span class="sxs-lookup"><span data-stu-id="2587e-127">Note that the maximum size for all virtual cache files is 128 MB.</span></span>

## <a name="error-codes"></a><span data-ttu-id="2587e-128">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="2587e-128">Error codes</span></span>

<span data-ttu-id="2587e-129">如果成功，則傳回 **S \_ OK** 。</span><span class="sxs-lookup"><span data-stu-id="2587e-129">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="2587e-130">備註</span><span class="sxs-lookup"><span data-stu-id="2587e-130">Remarks</span></span>

<span data-ttu-id="2587e-131">相關屬性包含 **BitmapVirtualCacheSize** 和 **BitmapVirtualCache24BppSize** 屬性。</span><span class="sxs-lookup"><span data-stu-id="2587e-131">Related properties include the **BitmapVirtualCacheSize** and **BitmapVirtualCache24BppSize** properties.</span></span>

<span data-ttu-id="2587e-132">如需遠端桌面網頁連線的詳細資訊，請參閱 [遠端桌面網頁連線的需求](requirements-for-remote-desktop-web-connection.md)。</span><span class="sxs-lookup"><span data-stu-id="2587e-132">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="2587e-133">規格需求</span><span class="sxs-lookup"><span data-stu-id="2587e-133">Requirements</span></span>



| <span data-ttu-id="2587e-134">需求</span><span class="sxs-lookup"><span data-stu-id="2587e-134">Requirement</span></span> | <span data-ttu-id="2587e-135">值</span><span class="sxs-lookup"><span data-stu-id="2587e-135">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2587e-136">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2587e-136">Minimum supported client</span></span><br/> | <span data-ttu-id="2587e-137">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2587e-137">Windows Vista</span></span><br/>                                                                        |
| <span data-ttu-id="2587e-138">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2587e-138">Minimum supported server</span></span><br/> | <span data-ttu-id="2587e-139">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2587e-139">Windows Server 2008</span></span><br/>                                                                  |
| <span data-ttu-id="2587e-140">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="2587e-140">Type library</span></span><br/>             | <dl> <span data-ttu-id="2587e-141"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2587e-141"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="2587e-142">DLL</span><span class="sxs-lookup"><span data-stu-id="2587e-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2587e-143"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2587e-143"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="2587e-144">IID</span><span class="sxs-lookup"><span data-stu-id="2587e-144">IID</span></span><br/>                      | <span data-ttu-id="2587e-145">IID \_ IMsRdpClientAdvancedSettings 定義為3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span><span class="sxs-lookup"><span data-stu-id="2587e-145">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="2587e-146">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2587e-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2587e-147">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="2587e-147">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="2587e-148">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="2587e-148">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="2587e-149">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="2587e-149">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="2587e-150">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="2587e-150">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="2587e-151">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="2587e-151">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="2587e-152">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="2587e-152">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="2587e-153">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="2587e-153">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="2587e-154">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="2587e-154">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





