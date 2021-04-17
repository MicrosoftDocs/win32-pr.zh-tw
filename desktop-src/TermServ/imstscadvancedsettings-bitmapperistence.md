---
title: IMsTscAdvancedSettings BitmapPeristence 屬性
description: 指定是否啟用點陣圖快取。
ms.assetid: 8cabeae8-26bc-4d33-82cc-47bb201d79b6
ms.tgt_platform: multiple
keywords:
- BitmapPeristence 屬性遠端桌面服務
- BitmapPeristence 屬性遠端桌面服務，IMsTscAdvancedSettings 介面
- IMsTscAdvancedSettings 介面遠端桌面服務，BitmapPeristence 屬性
- BitmapPeristence 屬性遠端桌面服務，IMsRdpClientAdvancedSettings 介面
- IMsRdpClientAdvancedSettings 介面遠端桌面服務，BitmapPeristence 屬性
- BitmapPeristence 屬性遠端桌面服務，IMsRdpClientAdvancedSettings2 介面
- IMsRdpClientAdvancedSettings2 介面遠端桌面服務，BitmapPeristence 屬性
- BitmapPeristence 屬性遠端桌面服務，IMsRdpClientAdvancedSettings3 介面
- IMsRdpClientAdvancedSettings3 介面遠端桌面服務，BitmapPeristence 屬性
- BitmapPeristence 屬性遠端桌面服務，IMsRdpClientAdvancedSettings4 介面
- IMsRdpClientAdvancedSettings4 介面遠端桌面服務，BitmapPeristence 屬性
- BitmapPeristence 屬性遠端桌面服務，IMsRdpClientAdvancedSettings5 介面
- IMsRdpClientAdvancedSettings5 介面遠端桌面服務，BitmapPeristence 屬性
- BitmapPeristence 屬性遠端桌面服務，IMsRdpClientAdvancedSettings6 介面
- IMsRdpClientAdvancedSettings6 介面遠端桌面服務，BitmapPeristence 屬性
- BitmapPeristence 屬性遠端桌面服務，IMsRdpClientAdvancedSettings7 介面
- IMsRdpClientAdvancedSettings7 介面遠端桌面服務，BitmapPeristence 屬性
- BitmapPeristence 屬性遠端桌面服務，IMsRdpClientAdvancedSettings8 介面
- IMsRdpClientAdvancedSettings8 介面遠端桌面服務，BitmapPeristence 屬性
topic_type:
- apiref
api_name:
- IMsTscAdvancedSettings.BitmapPeristence
- IMsTscAdvancedSettings.get_BitmapPeristence
- IMsTscAdvancedSettings.put_BitmapPeristence
- IMsRdpClientAdvancedSettings.BitmapPeristence
- IMsRdpClientAdvancedSettings.get_BitmapPeristence
- IMsRdpClientAdvancedSettings.put_BitmapPeristence
- IMsRdpClientAdvancedSettings2.BitmapPeristence
- IMsRdpClientAdvancedSettings2.get_BitmapPeristence
- IMsRdpClientAdvancedSettings2.put_BitmapPeristence
- IMsRdpClientAdvancedSettings3.BitmapPeristence
- IMsRdpClientAdvancedSettings3.get_BitmapPeristence
- IMsRdpClientAdvancedSettings3.put_BitmapPeristence
- IMsRdpClientAdvancedSettings4.BitmapPeristence
- IMsRdpClientAdvancedSettings4.get_BitmapPeristence
- IMsRdpClientAdvancedSettings4.put_BitmapPeristence
- IMsRdpClientAdvancedSettings5.BitmapPeristence
- IMsRdpClientAdvancedSettings5.get_BitmapPeristence
- IMsRdpClientAdvancedSettings5.put_BitmapPeristence
- IMsRdpClientAdvancedSettings6.BitmapPeristence
- IMsRdpClientAdvancedSettings6.get_BitmapPeristence
- IMsRdpClientAdvancedSettings6.put_BitmapPeristence
- IMsRdpClientAdvancedSettings7.BitmapPeristence
- IMsRdpClientAdvancedSettings7.get_BitmapPeristence
- IMsRdpClientAdvancedSettings7.put_BitmapPeristence
- IMsRdpClientAdvancedSettings8.BitmapPeristence
- IMsRdpClientAdvancedSettings8.get_BitmapPeristence
- IMsRdpClientAdvancedSettings8.put_BitmapPeristence
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a543d24b200d8fa484939d5ffeabfeeac0b5f73f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466852"
---
# <a name="imstscadvancedsettingsbitmapperistence-property"></a><span data-ttu-id="253b1-122">IMsTscAdvancedSettings：： BitmapPeristence 屬性</span><span class="sxs-lookup"><span data-stu-id="253b1-122">IMsTscAdvancedSettings::BitmapPeristence property</span></span>

<span data-ttu-id="253b1-123">指定是否啟用點陣圖快取。</span><span class="sxs-lookup"><span data-stu-id="253b1-123">Specifies whether bitmap caching is enabled.</span></span> <span data-ttu-id="253b1-124">持續性快取可以改善效能，但需要額外的磁碟空間。</span><span class="sxs-lookup"><span data-stu-id="253b1-124">Persistent caching can improve performance but requires additional disk space.</span></span>

> [!Note]  
> <span data-ttu-id="253b1-125">屬性名稱及其參數的拼寫錯誤是在控制項的發行版本中。</span><span class="sxs-lookup"><span data-stu-id="253b1-125">The spelling error in the name of the property and its parameter is in the released version of the control.</span></span>

 

<span data-ttu-id="253b1-126">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="253b1-126">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="253b1-127">Syntax</span><span class="sxs-lookup"><span data-stu-id="253b1-127">Syntax</span></span>


```C++
HRESULT put_BitmapPeristence(
  [in]  LONG bitmapPeristence
);

HRESULT get_BitmapPeristence(
  [out] LONG *pbitmapPeristence
);
```



## <a name="property-value"></a><span data-ttu-id="253b1-128">屬性值</span><span class="sxs-lookup"><span data-stu-id="253b1-128">Property value</span></span>

<span data-ttu-id="253b1-129">將此參數設定為0可停用快取，或設定為非零值以啟用快取。</span><span class="sxs-lookup"><span data-stu-id="253b1-129">Set this parameter to 0 to disable caching or a nonzero value to enable caching.</span></span>

## <a name="error-codes"></a><span data-ttu-id="253b1-130">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="253b1-130">Error codes</span></span>

<span data-ttu-id="253b1-131">如果成功，則傳回 **S \_ OK** 。</span><span class="sxs-lookup"><span data-stu-id="253b1-131">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="253b1-132">備註</span><span class="sxs-lookup"><span data-stu-id="253b1-132">Remarks</span></span>

<span data-ttu-id="253b1-133">如需遠端桌面網頁連線的詳細資訊，請參閱 [遠端桌面網頁連線的需求](requirements-for-remote-desktop-web-connection.md)。</span><span class="sxs-lookup"><span data-stu-id="253b1-133">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="253b1-134">規格需求</span><span class="sxs-lookup"><span data-stu-id="253b1-134">Requirements</span></span>



| <span data-ttu-id="253b1-135">需求</span><span class="sxs-lookup"><span data-stu-id="253b1-135">Requirement</span></span> | <span data-ttu-id="253b1-136">值</span><span class="sxs-lookup"><span data-stu-id="253b1-136">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="253b1-137">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="253b1-137">Minimum supported client</span></span><br/> | <span data-ttu-id="253b1-138">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="253b1-138">Windows Vista</span></span><br/>                                                                  |
| <span data-ttu-id="253b1-139">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="253b1-139">Minimum supported server</span></span><br/> | <span data-ttu-id="253b1-140">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="253b1-140">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="253b1-141">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="253b1-141">Type library</span></span><br/>             | <dl> <span data-ttu-id="253b1-142"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="253b1-142"><dt>MsTscAx.dll</dt></span></span> </dl>    |
| <span data-ttu-id="253b1-143">DLL</span><span class="sxs-lookup"><span data-stu-id="253b1-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="253b1-144"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="253b1-144"><dt>MsTscAx.dll</dt></span></span> </dl>    |
| <span data-ttu-id="253b1-145">IID</span><span class="sxs-lookup"><span data-stu-id="253b1-145">IID</span></span><br/>                      | <span data-ttu-id="253b1-146">IID \_ IMsTscAdvancedSettings 定義為809945cc-4b3b-4a92-a6b0-dbf9b5f2ef2d</span><span class="sxs-lookup"><span data-stu-id="253b1-146">IID\_IMsTscAdvancedSettings is defined as 809945cc-4b3b-4a92-a6b0-dbf9b5f2ef2d</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="253b1-147">另請參閱</span><span class="sxs-lookup"><span data-stu-id="253b1-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="253b1-148">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="253b1-148">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="253b1-149">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="253b1-149">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="253b1-150">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="253b1-150">**IMsRdpClientAdvancedSettings3**</span></span>](imsrdpclientadvancedsettings3.md)
</dt> <dt>

[<span data-ttu-id="253b1-151">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="253b1-151">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="253b1-152">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="253b1-152">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="253b1-153">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="253b1-153">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="253b1-154">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="253b1-154">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="253b1-155">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="253b1-155">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="253b1-156">**IMsTscAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="253b1-156">**IMsTscAdvancedSettings**</span></span>](imstscadvancedsettings-interface.md)
</dt> </dl>

 

 





