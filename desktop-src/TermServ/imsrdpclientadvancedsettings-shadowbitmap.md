---
title: IMsRdpClientAdvancedSettings ShadowBitmap 屬性
description: 指定是否應該使用陰影點陣圖。
ms.assetid: b329e367-7579-466d-877a-16253f85e5a2
ms.tgt_platform: multiple
keywords:
- ShadowBitmap 屬性遠端桌面服務
- ShadowBitmap 屬性遠端桌面服務，IMsRdpClientAdvancedSettings 介面
- IMsRdpClientAdvancedSettings 介面遠端桌面服務，ShadowBitmap 屬性
- ShadowBitmap 屬性遠端桌面服務，IMsRdpClientAdvancedSettings2 介面
- IMsRdpClientAdvancedSettings2 介面遠端桌面服務，ShadowBitmap 屬性
- ShadowBitmap 屬性遠端桌面服務，IMsRdpClientAdvancedSettings3 介面
- IMsRdpClientAdvancedSettings3 介面遠端桌面服務，ShadowBitmap 屬性
- ShadowBitmap 屬性遠端桌面服務，IMsRdpClientAdvancedSettings4 介面
- IMsRdpClientAdvancedSettings4 介面遠端桌面服務，ShadowBitmap 屬性
- ShadowBitmap 屬性遠端桌面服務，IMsRdpClientAdvancedSettings5 介面
- IMsRdpClientAdvancedSettings5 介面遠端桌面服務，ShadowBitmap 屬性
- ShadowBitmap 屬性遠端桌面服務，IMsRdpClientAdvancedSettings6 介面
- IMsRdpClientAdvancedSettings6 介面遠端桌面服務，ShadowBitmap 屬性
- ShadowBitmap 屬性遠端桌面服務，IMsRdpClientAdvancedSettings7 介面
- IMsRdpClientAdvancedSettings7 介面遠端桌面服務，ShadowBitmap 屬性
- ShadowBitmap 屬性遠端桌面服務，IMsRdpClientAdvancedSettings8 介面
- IMsRdpClientAdvancedSettings8 介面遠端桌面服務，ShadowBitmap 屬性
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.ShadowBitmap
- IMsRdpClientAdvancedSettings.get_ShadowBitmap
- IMsRdpClientAdvancedSettings.put_ShadowBitmap
- IMsRdpClientAdvancedSettings2.ShadowBitmap
- IMsRdpClientAdvancedSettings2.get_ShadowBitmap
- IMsRdpClientAdvancedSettings2.put_ShadowBitmap
- IMsRdpClientAdvancedSettings3.ShadowBitmap
- IMsRdpClientAdvancedSettings3.get_ShadowBitmap
- IMsRdpClientAdvancedSettings3.put_ShadowBitmap
- IMsRdpClientAdvancedSettings4.ShadowBitmap
- IMsRdpClientAdvancedSettings4.get_ShadowBitmap
- IMsRdpClientAdvancedSettings4.put_ShadowBitmap
- IMsRdpClientAdvancedSettings5.ShadowBitmap
- IMsRdpClientAdvancedSettings5.get_ShadowBitmap
- IMsRdpClientAdvancedSettings5.put_ShadowBitmap
- IMsRdpClientAdvancedSettings6.ShadowBitmap
- IMsRdpClientAdvancedSettings6.get_ShadowBitmap
- IMsRdpClientAdvancedSettings6.put_ShadowBitmap
- IMsRdpClientAdvancedSettings7.ShadowBitmap
- IMsRdpClientAdvancedSettings7.get_ShadowBitmap
- IMsRdpClientAdvancedSettings7.put_ShadowBitmap
- IMsRdpClientAdvancedSettings8.ShadowBitmap
- IMsRdpClientAdvancedSettings8.get_ShadowBitmap
- IMsRdpClientAdvancedSettings8.put_ShadowBitmap
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fc6c43862b498fe5828d2746666c5e414de4c71e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464317"
---
# <a name="imsrdpclientadvancedsettingsshadowbitmap-property"></a><span data-ttu-id="89767-120">IMsRdpClientAdvancedSettings：： ShadowBitmap 屬性</span><span class="sxs-lookup"><span data-stu-id="89767-120">IMsRdpClientAdvancedSettings::ShadowBitmap property</span></span>

<span data-ttu-id="89767-121">\[不支援這個屬性。</span><span class="sxs-lookup"><span data-stu-id="89767-121">\[This property is not supported.</span></span> <span data-ttu-id="89767-122">從 Windows Server 2008 和 Windows 7 開始，對 **ShadowBitmap** 的呼叫一律會傳回 **\_ FALSE**。\]</span><span class="sxs-lookup"><span data-stu-id="89767-122">Starting with Windows Server 2008 and Windows 7, calls to **ShadowBitmap** always return **S\_FALSE**.\]</span></span>

<span data-ttu-id="89767-123">指定是否應該使用陰影點陣圖。</span><span class="sxs-lookup"><span data-stu-id="89767-123">Specifies if shadow bitmaps should be used.</span></span>

<span data-ttu-id="89767-124">在全螢幕模式中，一律會停用陰影點陣圖，因此當處於全螢幕模式時，這個屬性不會有任何作用。</span><span class="sxs-lookup"><span data-stu-id="89767-124">Shadow bitmaps are always disabled in full-screen mode, therefore this property has no effect when in full-screen mode.</span></span>

<span data-ttu-id="89767-125">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="89767-125">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="89767-126">Syntax</span><span class="sxs-lookup"><span data-stu-id="89767-126">Syntax</span></span>


```C++
HRESULT put_ShadowBitmap(
  [in]  LONG shadowBitmap
);

HRESULT get_ShadowBitmap(
  [out] LONG *pshadowBitmap
);
```



## <a name="property-value"></a><span data-ttu-id="89767-127">屬性值</span><span class="sxs-lookup"><span data-stu-id="89767-127">Property value</span></span>

<span data-ttu-id="89767-128">將此參數設定為0，以停用此功能或非零值以啟用此功能。</span><span class="sxs-lookup"><span data-stu-id="89767-128">Set this parameter to 0 to disable the feature or a nonzero value to enable the feature.</span></span> <span data-ttu-id="89767-129">停用這項功能通常可以改善效能，但可能會在繪製畫面時產生成品。</span><span class="sxs-lookup"><span data-stu-id="89767-129">Disabling this feature typically improves performance but can result in artifacts when painting screens.</span></span>

## <a name="remarks"></a><span data-ttu-id="89767-130">備註</span><span class="sxs-lookup"><span data-stu-id="89767-130">Remarks</span></span>

<span data-ttu-id="89767-131">如需遠端桌面網頁連線的詳細資訊，請參閱 [遠端桌面網頁連線的需求](requirements-for-remote-desktop-web-connection.md)。</span><span class="sxs-lookup"><span data-stu-id="89767-131">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="89767-132">規格需求</span><span class="sxs-lookup"><span data-stu-id="89767-132">Requirements</span></span>



| <span data-ttu-id="89767-133">需求</span><span class="sxs-lookup"><span data-stu-id="89767-133">Requirement</span></span> | <span data-ttu-id="89767-134">值</span><span class="sxs-lookup"><span data-stu-id="89767-134">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="89767-135">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="89767-135">Minimum supported client</span></span><br/> | <span data-ttu-id="89767-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="89767-136">Windows Vista</span></span><br/>                                                                        |
| <span data-ttu-id="89767-137">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="89767-137">Minimum supported server</span></span><br/> | <span data-ttu-id="89767-138">都不支援</span><span class="sxs-lookup"><span data-stu-id="89767-138">None supported</span></span><br/>                                                                       |
| <span data-ttu-id="89767-139">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="89767-139">End of client support</span></span><br/>    | <span data-ttu-id="89767-140">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="89767-140">Windows Vista</span></span><br/>                                                                        |
| <span data-ttu-id="89767-141">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="89767-141">End of server support</span></span><br/>    | <span data-ttu-id="89767-142">都不支援</span><span class="sxs-lookup"><span data-stu-id="89767-142">None supported</span></span><br/>                                                                       |
| <span data-ttu-id="89767-143">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="89767-143">Type library</span></span><br/>             | <dl> <span data-ttu-id="89767-144"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="89767-144"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="89767-145">DLL</span><span class="sxs-lookup"><span data-stu-id="89767-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="89767-146"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="89767-146"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="89767-147">IID</span><span class="sxs-lookup"><span data-stu-id="89767-147">IID</span></span><br/>                      | <span data-ttu-id="89767-148">IID \_ IMsRdpClientAdvancedSettings 定義為3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span><span class="sxs-lookup"><span data-stu-id="89767-148">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="89767-149">另請參閱</span><span class="sxs-lookup"><span data-stu-id="89767-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="89767-150">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="89767-150">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="89767-151">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="89767-151">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="89767-152">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="89767-152">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="89767-153">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="89767-153">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="89767-154">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="89767-154">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="89767-155">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="89767-155">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="89767-156">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="89767-156">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="89767-157">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="89767-157">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





