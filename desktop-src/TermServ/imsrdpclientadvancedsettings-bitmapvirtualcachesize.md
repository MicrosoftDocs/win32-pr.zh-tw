---
title: IMsRdpClientAdvancedSettings BitmapVirtualCacheSize 屬性
description: 指定持續性點陣圖快取檔案的大小（以 mb 為單位），以用於每圖元8位的色彩。
ms.assetid: 4efcabd2-8671-40a3-ad12-af0b2b6e495a
ms.tgt_platform: multiple
keywords:
- BitmapVirtualCacheSize 屬性遠端桌面服務
- BitmapVirtualCacheSize 屬性遠端桌面服務，IMsRdpClientAdvancedSettings 介面
- IMsRdpClientAdvancedSettings 介面遠端桌面服務，BitmapVirtualCacheSize 屬性
- BitmapVirtualCacheSize 屬性遠端桌面服務，IMsRdpClientAdvancedSettings2 介面
- IMsRdpClientAdvancedSettings2 介面遠端桌面服務，BitmapVirtualCacheSize 屬性
- BitmapVirtualCacheSize 屬性遠端桌面服務，IMsRdpClientAdvancedSettings3 介面
- IMsRdpClientAdvancedSettings3 介面遠端桌面服務，BitmapVirtualCacheSize 屬性
- BitmapVirtualCacheSize 屬性遠端桌面服務，IMsRdpClientAdvancedSettings4 介面
- IMsRdpClientAdvancedSettings4 介面遠端桌面服務，BitmapVirtualCacheSize 屬性
- BitmapVirtualCacheSize 屬性遠端桌面服務，IMsRdpClientAdvancedSettings5 介面
- IMsRdpClientAdvancedSettings5 介面遠端桌面服務，BitmapVirtualCacheSize 屬性
- BitmapVirtualCacheSize 屬性遠端桌面服務，IMsRdpClientAdvancedSettings6 介面
- IMsRdpClientAdvancedSettings6 介面遠端桌面服務，BitmapVirtualCacheSize 屬性
- BitmapVirtualCacheSize 屬性遠端桌面服務，IMsRdpClientAdvancedSettings7 介面
- IMsRdpClientAdvancedSettings7 介面遠端桌面服務，BitmapVirtualCacheSize 屬性
- BitmapVirtualCacheSize 屬性遠端桌面服務，IMsRdpClientAdvancedSettings8 介面
- IMsRdpClientAdvancedSettings8 介面遠端桌面服務，BitmapVirtualCacheSize 屬性
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.BitmapVirtualCacheSize
- IMsRdpClientAdvancedSettings.get_BitmapVirtualCacheSize
- IMsRdpClientAdvancedSettings.put_BitmapVirtualCacheSize
- IMsRdpClientAdvancedSettings2.BitmapVirtualCacheSize
- IMsRdpClientAdvancedSettings2.get_BitmapVirtualCacheSize
- IMsRdpClientAdvancedSettings2.put_BitmapVirtualCacheSize
- IMsRdpClientAdvancedSettings3.BitmapVirtualCacheSize
- IMsRdpClientAdvancedSettings3.get_BitmapVirtualCacheSize
- IMsRdpClientAdvancedSettings3.put_BitmapVirtualCacheSize
- IMsRdpClientAdvancedSettings4.BitmapVirtualCacheSize
- IMsRdpClientAdvancedSettings4.get_BitmapVirtualCacheSize
- IMsRdpClientAdvancedSettings4.put_BitmapVirtualCacheSize
- IMsRdpClientAdvancedSettings5.BitmapVirtualCacheSize
- IMsRdpClientAdvancedSettings5.get_BitmapVirtualCacheSize
- IMsRdpClientAdvancedSettings5.put_BitmapVirtualCacheSize
- IMsRdpClientAdvancedSettings6.BitmapVirtualCacheSize
- IMsRdpClientAdvancedSettings6.get_BitmapVirtualCacheSize
- IMsRdpClientAdvancedSettings6.put_BitmapVirtualCacheSize
- IMsRdpClientAdvancedSettings7.BitmapVirtualCacheSize
- IMsRdpClientAdvancedSettings7.get_BitmapVirtualCacheSize
- IMsRdpClientAdvancedSettings7.put_BitmapVirtualCacheSize
- IMsRdpClientAdvancedSettings8.BitmapVirtualCacheSize
- IMsRdpClientAdvancedSettings8.get_BitmapVirtualCacheSize
- IMsRdpClientAdvancedSettings8.put_BitmapVirtualCacheSize
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb652c0f235cf7438b49e68a544188ac4622acad
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024820"
---
# <a name="imsrdpclientadvancedsettingsbitmapvirtualcachesize-property"></a><span data-ttu-id="0757e-120">IMsRdpClientAdvancedSettings：： BitmapVirtualCacheSize 屬性</span><span class="sxs-lookup"><span data-stu-id="0757e-120">IMsRdpClientAdvancedSettings::BitmapVirtualCacheSize property</span></span>

<span data-ttu-id="0757e-121">指定持續性點陣圖快取檔案的大小（以 mb 為單位），以用於每圖元8位的色彩。</span><span class="sxs-lookup"><span data-stu-id="0757e-121">Specifies the size, in megabytes, of the persistent bitmap cache file to use for 8-bits-per-pixel color.</span></span>

<span data-ttu-id="0757e-122">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="0757e-122">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="0757e-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="0757e-123">Syntax</span></span>


```C++
HRESULT put_BitmapVirtualCacheSize(
  [in]  LONG bitmapVirtualCacheSize
);

HRESULT get_BitmapVirtualCacheSize(
  [out] LONG *pbitmapVirtualCacheSize
);
```



## <a name="property-value"></a><span data-ttu-id="0757e-124">屬性值</span><span class="sxs-lookup"><span data-stu-id="0757e-124">Property value</span></span>

<span data-ttu-id="0757e-125">新的快取大小。</span><span class="sxs-lookup"><span data-stu-id="0757e-125">The new cache size.</span></span> <span data-ttu-id="0757e-126">有效的值為1到32（含）。</span><span class="sxs-lookup"><span data-stu-id="0757e-126">The valid values are 1 to 32 inclusive.</span></span> <span data-ttu-id="0757e-127">請注意，所有虛擬快取檔案的大小上限為 128 MB。</span><span class="sxs-lookup"><span data-stu-id="0757e-127">Note that the maximum size for all virtual cache files is 128 MB.</span></span>

## <a name="error-codes"></a><span data-ttu-id="0757e-128">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="0757e-128">Error codes</span></span>

<span data-ttu-id="0757e-129">如果成功，則傳回 **S \_ OK** 。</span><span class="sxs-lookup"><span data-stu-id="0757e-129">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="0757e-130">備註</span><span class="sxs-lookup"><span data-stu-id="0757e-130">Remarks</span></span>

<span data-ttu-id="0757e-131">如需遠端桌面網頁連線的詳細資訊，請參閱 [遠端桌面網頁連線的需求](requirements-for-remote-desktop-web-connection.md)。</span><span class="sxs-lookup"><span data-stu-id="0757e-131">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="0757e-132">規格需求</span><span class="sxs-lookup"><span data-stu-id="0757e-132">Requirements</span></span>



| <span data-ttu-id="0757e-133">需求</span><span class="sxs-lookup"><span data-stu-id="0757e-133">Requirement</span></span> | <span data-ttu-id="0757e-134">值</span><span class="sxs-lookup"><span data-stu-id="0757e-134">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0757e-135">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0757e-135">Minimum supported client</span></span><br/> | <span data-ttu-id="0757e-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0757e-136">Windows Vista</span></span><br/>                                                                        |
| <span data-ttu-id="0757e-137">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0757e-137">Minimum supported server</span></span><br/> | <span data-ttu-id="0757e-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0757e-138">Windows Server 2008</span></span><br/>                                                                  |
| <span data-ttu-id="0757e-139">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="0757e-139">Type library</span></span><br/>             | <dl> <span data-ttu-id="0757e-140"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0757e-140"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="0757e-141">DLL</span><span class="sxs-lookup"><span data-stu-id="0757e-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0757e-142"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0757e-142"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="0757e-143">IID</span><span class="sxs-lookup"><span data-stu-id="0757e-143">IID</span></span><br/>                      | <span data-ttu-id="0757e-144">IID \_ IMsRdpClientAdvancedSettings 定義為3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span><span class="sxs-lookup"><span data-stu-id="0757e-144">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="0757e-145">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0757e-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0757e-146">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="0757e-146">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="0757e-147">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="0757e-147">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="0757e-148">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="0757e-148">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="0757e-149">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="0757e-149">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="0757e-150">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="0757e-150">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="0757e-151">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="0757e-151">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="0757e-152">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="0757e-152">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="0757e-153">**BitmapVirtualCache16BppSize**</span><span class="sxs-lookup"><span data-stu-id="0757e-153">**BitmapVirtualCache16BppSize**</span></span>](imsrdpclientadvancedsettings-bitmapvirtualcache16bppsize.md)
</dt> <dt>

[<span data-ttu-id="0757e-154">**BitmapVirtualCache24BppSize**</span><span class="sxs-lookup"><span data-stu-id="0757e-154">**BitmapVirtualCache24BppSize**</span></span>](imsrdpclientadvancedsettings-bitmapvirtualcache24bppsize.md)
</dt> <dt>

[<span data-ttu-id="0757e-155">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="0757e-155">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





