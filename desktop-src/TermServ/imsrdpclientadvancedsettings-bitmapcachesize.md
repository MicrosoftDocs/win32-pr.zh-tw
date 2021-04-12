---
title: IMsRdpClientAdvancedSettings BitmapCacheSize 屬性
description: 點陣圖快取檔案的大小（以 kb 為單位），用於每圖元8位的點陣圖。
ms.assetid: a2a4b739-0fa3-4a76-87ae-3cba913b7703
ms.tgt_platform: multiple
keywords:
- BitmapCacheSize 屬性遠端桌面服務
- BitmapCacheSize 屬性遠端桌面服務，IMsRdpClientAdvancedSettings 介面
- IMsRdpClientAdvancedSettings 介面遠端桌面服務，BitmapCacheSize 屬性
- BitmapCacheSize 屬性遠端桌面服務，IMsRdpClientAdvancedSettings2 介面
- IMsRdpClientAdvancedSettings2 介面遠端桌面服務，BitmapCacheSize 屬性
- BitmapCacheSize 屬性遠端桌面服務，IMsRdpClientAdvancedSettings3 介面
- IMsRdpClientAdvancedSettings3 介面遠端桌面服務，BitmapCacheSize 屬性
- BitmapCacheSize 屬性遠端桌面服務，IMsRdpClientAdvancedSettings4 介面
- IMsRdpClientAdvancedSettings4 介面遠端桌面服務，BitmapCacheSize 屬性
- BitmapCacheSize 屬性遠端桌面服務，IMsRdpClientAdvancedSettings5 介面
- IMsRdpClientAdvancedSettings5 介面遠端桌面服務，BitmapCacheSize 屬性
- BitmapCacheSize 屬性遠端桌面服務，IMsRdpClientAdvancedSettings6 介面
- IMsRdpClientAdvancedSettings6 介面遠端桌面服務，BitmapCacheSize 屬性
- BitmapCacheSize 屬性遠端桌面服務，IMsRdpClientAdvancedSettings7 介面
- IMsRdpClientAdvancedSettings7 介面遠端桌面服務，BitmapCacheSize 屬性
- BitmapCacheSize 屬性遠端桌面服務，IMsRdpClientAdvancedSettings8 介面
- IMsRdpClientAdvancedSettings8 介面遠端桌面服務，BitmapCacheSize 屬性
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.BitmapCacheSize
- IMsRdpClientAdvancedSettings.get_BitmapCacheSize
- IMsRdpClientAdvancedSettings.put_BitmapCacheSize
- IMsRdpClientAdvancedSettings2.BitmapCacheSize
- IMsRdpClientAdvancedSettings2.get_BitmapCacheSize
- IMsRdpClientAdvancedSettings2.put_BitmapCacheSize
- IMsRdpClientAdvancedSettings3.BitmapCacheSize
- IMsRdpClientAdvancedSettings3.get_BitmapCacheSize
- IMsRdpClientAdvancedSettings3.put_BitmapCacheSize
- IMsRdpClientAdvancedSettings4.BitmapCacheSize
- IMsRdpClientAdvancedSettings4.get_BitmapCacheSize
- IMsRdpClientAdvancedSettings4.put_BitmapCacheSize
- IMsRdpClientAdvancedSettings5.BitmapCacheSize
- IMsRdpClientAdvancedSettings5.get_BitmapCacheSize
- IMsRdpClientAdvancedSettings5.put_BitmapCacheSize
- IMsRdpClientAdvancedSettings6.BitmapCacheSize
- IMsRdpClientAdvancedSettings6.get_BitmapCacheSize
- IMsRdpClientAdvancedSettings6.put_BitmapCacheSize
- IMsRdpClientAdvancedSettings7.BitmapCacheSize
- IMsRdpClientAdvancedSettings7.get_BitmapCacheSize
- IMsRdpClientAdvancedSettings7.put_BitmapCacheSize
- IMsRdpClientAdvancedSettings8.BitmapCacheSize
- IMsRdpClientAdvancedSettings8.get_BitmapCacheSize
- IMsRdpClientAdvancedSettings8.put_BitmapCacheSize
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a38376bb0b06bd4efea36d3c4cad4e4aec0f35b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384325"
---
# <a name="imsrdpclientadvancedsettingsbitmapcachesize-property"></a><span data-ttu-id="10d94-120">IMsRdpClientAdvancedSettings：： BitmapCacheSize 屬性</span><span class="sxs-lookup"><span data-stu-id="10d94-120">IMsRdpClientAdvancedSettings::BitmapCacheSize property</span></span>

<span data-ttu-id="10d94-121">點陣圖快取檔案的大小（以 kb 為單位），用於每圖元8位的點陣圖。</span><span class="sxs-lookup"><span data-stu-id="10d94-121">The size, in kilobytes, of the bitmap cache file used for 8-bits-per-pixel bitmaps.</span></span>

<span data-ttu-id="10d94-122">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="10d94-122">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="10d94-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="10d94-123">Syntax</span></span>


```C++
HRESULT put_BitmapCacheSize(
  [in]  LONG bitmapCacheSize
);

HRESULT get_BitmapCacheSize(
  [out] LONG *pbitmapCacheSize
);
```



## <a name="property-value"></a><span data-ttu-id="10d94-124">屬性值</span><span class="sxs-lookup"><span data-stu-id="10d94-124">Property value</span></span>

<span data-ttu-id="10d94-125">新的快取大小（以 kb 為單位）。</span><span class="sxs-lookup"><span data-stu-id="10d94-125">The new cache size, in kilobytes.</span></span> <span data-ttu-id="10d94-126">有效的數值為1到32（含）。</span><span class="sxs-lookup"><span data-stu-id="10d94-126">The valid numeric values are 1 to 32 inclusive.</span></span>

## <a name="error-codes"></a><span data-ttu-id="10d94-127">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="10d94-127">Error codes</span></span>

<span data-ttu-id="10d94-128">如果成功，則傳回 **S \_ OK** 。</span><span class="sxs-lookup"><span data-stu-id="10d94-128">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="10d94-129">備註</span><span class="sxs-lookup"><span data-stu-id="10d94-129">Remarks</span></span>

<span data-ttu-id="10d94-130">如需遠端桌面網頁連線的詳細資訊，請參閱 [遠端桌面網頁連線的需求](requirements-for-remote-desktop-web-connection.md)。</span><span class="sxs-lookup"><span data-stu-id="10d94-130">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="10d94-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="10d94-131">Requirements</span></span>



| <span data-ttu-id="10d94-132">需求</span><span class="sxs-lookup"><span data-stu-id="10d94-132">Requirement</span></span> | <span data-ttu-id="10d94-133">值</span><span class="sxs-lookup"><span data-stu-id="10d94-133">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="10d94-134">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="10d94-134">Minimum supported client</span></span><br/> | <span data-ttu-id="10d94-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="10d94-135">Windows Vista</span></span><br/>                                                                        |
| <span data-ttu-id="10d94-136">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="10d94-136">Minimum supported server</span></span><br/> | <span data-ttu-id="10d94-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="10d94-137">Windows Server 2008</span></span><br/>                                                                  |
| <span data-ttu-id="10d94-138">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="10d94-138">Type library</span></span><br/>             | <dl> <span data-ttu-id="10d94-139"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="10d94-139"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="10d94-140">DLL</span><span class="sxs-lookup"><span data-stu-id="10d94-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="10d94-141"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="10d94-141"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="10d94-142">IID</span><span class="sxs-lookup"><span data-stu-id="10d94-142">IID</span></span><br/>                      | <span data-ttu-id="10d94-143">IID \_ IMsRdpClientAdvancedSettings 定義為3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span><span class="sxs-lookup"><span data-stu-id="10d94-143">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="10d94-144">另請參閱</span><span class="sxs-lookup"><span data-stu-id="10d94-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="10d94-145">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="10d94-145">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="10d94-146">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="10d94-146">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="10d94-147">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="10d94-147">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="10d94-148">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="10d94-148">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="10d94-149">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="10d94-149">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="10d94-150">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="10d94-150">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="10d94-151">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="10d94-151">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="10d94-152">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="10d94-152">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





