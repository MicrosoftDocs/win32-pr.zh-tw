---
title: IMsRdpClientAdvancedSettings BitmapPersistence 屬性
description: 指定是否應該使用持續性點陣圖快取。 持續性快取可以改善效能，但需要額外的磁碟空間。
ms.assetid: ffaa9277-9dd7-4b2a-9de5-009b7e8766bc
ms.tgt_platform: multiple
keywords:
- BitmapPersistence 屬性遠端桌面服務
- BitmapPersistence 屬性遠端桌面服務，IMsRdpClientAdvancedSettings 介面
- IMsRdpClientAdvancedSettings 介面遠端桌面服務，BitmapPersistence 屬性
- BitmapPersistence 屬性遠端桌面服務，IMsRdpClientAdvancedSettings2 介面
- IMsRdpClientAdvancedSettings2 介面遠端桌面服務，BitmapPersistence 屬性
- BitmapPersistence 屬性遠端桌面服務，IMsRdpClientAdvancedSettings3 介面
- IMsRdpClientAdvancedSettings3 介面遠端桌面服務，BitmapPersistence 屬性
- BitmapPersistence 屬性遠端桌面服務，IMsRdpClientAdvancedSettings4 介面
- IMsRdpClientAdvancedSettings4 介面遠端桌面服務，BitmapPersistence 屬性
- BitmapPersistence 屬性遠端桌面服務，IMsRdpClientAdvancedSettings5 介面
- IMsRdpClientAdvancedSettings5 介面遠端桌面服務，BitmapPersistence 屬性
- BitmapPersistence 屬性遠端桌面服務，IMsRdpClientAdvancedSettings6 介面
- IMsRdpClientAdvancedSettings6 介面遠端桌面服務，BitmapPersistence 屬性
- BitmapPersistence 屬性遠端桌面服務，IMsRdpClientAdvancedSettings7 介面
- IMsRdpClientAdvancedSettings7 介面遠端桌面服務，BitmapPersistence 屬性
- BitmapPersistence 屬性遠端桌面服務，IMsRdpClientAdvancedSettings8 介面
- IMsRdpClientAdvancedSettings8 介面遠端桌面服務，BitmapPersistence 屬性
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.BitmapPersistence
- IMsRdpClientAdvancedSettings.get_BitmapPersistence
- IMsRdpClientAdvancedSettings.put_BitmapPersistence
- IMsRdpClientAdvancedSettings2.BitmapPersistence
- IMsRdpClientAdvancedSettings2.get_BitmapPersistence
- IMsRdpClientAdvancedSettings2.put_BitmapPersistence
- IMsRdpClientAdvancedSettings3.BitmapPersistence
- IMsRdpClientAdvancedSettings3.get_BitmapPersistence
- IMsRdpClientAdvancedSettings3.put_BitmapPersistence
- IMsRdpClientAdvancedSettings4.BitmapPersistence
- IMsRdpClientAdvancedSettings4.get_BitmapPersistence
- IMsRdpClientAdvancedSettings4.put_BitmapPersistence
- IMsRdpClientAdvancedSettings5.BitmapPersistence
- IMsRdpClientAdvancedSettings5.get_BitmapPersistence
- IMsRdpClientAdvancedSettings5.put_BitmapPersistence
- IMsRdpClientAdvancedSettings6.BitmapPersistence
- IMsRdpClientAdvancedSettings6.get_BitmapPersistence
- IMsRdpClientAdvancedSettings6.put_BitmapPersistence
- IMsRdpClientAdvancedSettings7.BitmapPersistence
- IMsRdpClientAdvancedSettings7.get_BitmapPersistence
- IMsRdpClientAdvancedSettings7.put_BitmapPersistence
- IMsRdpClientAdvancedSettings8.BitmapPersistence
- IMsRdpClientAdvancedSettings8.get_BitmapPersistence
- IMsRdpClientAdvancedSettings8.put_BitmapPersistence
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 65795b5217c785befe0db6ac529d5760a6211d4d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384322"
---
# <a name="imsrdpclientadvancedsettingsbitmappersistence-property"></a><span data-ttu-id="46d32-121">IMsRdpClientAdvancedSettings：： BitmapPersistence 屬性</span><span class="sxs-lookup"><span data-stu-id="46d32-121">IMsRdpClientAdvancedSettings::BitmapPersistence property</span></span>

<span data-ttu-id="46d32-122">指定是否應該使用持續性點陣圖快取。</span><span class="sxs-lookup"><span data-stu-id="46d32-122">Specifies if persistent bitmap caching should be used.</span></span> <span data-ttu-id="46d32-123">持續性快取可以改善效能，但需要額外的磁碟空間。</span><span class="sxs-lookup"><span data-stu-id="46d32-123">Persistent caching can improve performance but requires additional disk space.</span></span>

<span data-ttu-id="46d32-124">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="46d32-124">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="46d32-125">Syntax</span><span class="sxs-lookup"><span data-stu-id="46d32-125">Syntax</span></span>


```C++
HRESULT put_BitmapPersistence(
  [in]  LONG bitmapPeristence
);

HRESULT get_BitmapPersistence(
  [out] LONG *pbitmapPeristence
);
```



## <a name="property-value"></a><span data-ttu-id="46d32-126">屬性值</span><span class="sxs-lookup"><span data-stu-id="46d32-126">Property value</span></span>

<span data-ttu-id="46d32-127">將此參數設定為0可停用快取，或設定為非零值以啟用快取。</span><span class="sxs-lookup"><span data-stu-id="46d32-127">Set this parameter to 0 to disable caching or a nonzero value to enable caching.</span></span>

> [!Note]  
> <span data-ttu-id="46d32-128">參數名稱中的拼寫錯誤是在控制項的發行版本中。</span><span class="sxs-lookup"><span data-stu-id="46d32-128">The spelling error in the name of the parameter is in the released version of the control.</span></span>

 

## <a name="error-codes"></a><span data-ttu-id="46d32-129">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="46d32-129">Error codes</span></span>

<span data-ttu-id="46d32-130">如果成功，則傳回 **S \_ OK** 。</span><span class="sxs-lookup"><span data-stu-id="46d32-130">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="46d32-131">備註</span><span class="sxs-lookup"><span data-stu-id="46d32-131">Remarks</span></span>

<span data-ttu-id="46d32-132">如需遠端桌面網頁連線的詳細資訊，請參閱 [遠端桌面網頁連線的需求](requirements-for-remote-desktop-web-connection.md)。</span><span class="sxs-lookup"><span data-stu-id="46d32-132">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="46d32-133">規格需求</span><span class="sxs-lookup"><span data-stu-id="46d32-133">Requirements</span></span>



| <span data-ttu-id="46d32-134">需求</span><span class="sxs-lookup"><span data-stu-id="46d32-134">Requirement</span></span> | <span data-ttu-id="46d32-135">值</span><span class="sxs-lookup"><span data-stu-id="46d32-135">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="46d32-136">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="46d32-136">Minimum supported client</span></span><br/> | <span data-ttu-id="46d32-137">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="46d32-137">Windows Vista</span></span><br/>                                                                        |
| <span data-ttu-id="46d32-138">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="46d32-138">Minimum supported server</span></span><br/> | <span data-ttu-id="46d32-139">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="46d32-139">Windows Server 2008</span></span><br/>                                                                  |
| <span data-ttu-id="46d32-140">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="46d32-140">Type library</span></span><br/>             | <dl> <span data-ttu-id="46d32-141"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="46d32-141"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="46d32-142">DLL</span><span class="sxs-lookup"><span data-stu-id="46d32-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="46d32-143"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="46d32-143"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="46d32-144">IID</span><span class="sxs-lookup"><span data-stu-id="46d32-144">IID</span></span><br/>                      | <span data-ttu-id="46d32-145">IID \_ IMsRdpClientAdvancedSettings 定義為3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span><span class="sxs-lookup"><span data-stu-id="46d32-145">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="46d32-146">另請參閱</span><span class="sxs-lookup"><span data-stu-id="46d32-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="46d32-147">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="46d32-147">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="46d32-148">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="46d32-148">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="46d32-149">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="46d32-149">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="46d32-150">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="46d32-150">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="46d32-151">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="46d32-151">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="46d32-152">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="46d32-152">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="46d32-153">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="46d32-153">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="46d32-154">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="46d32-154">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





