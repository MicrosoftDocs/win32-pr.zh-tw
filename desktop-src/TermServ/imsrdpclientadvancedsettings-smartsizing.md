---
title: IMsRdpClientAdvancedSettings SmartSizing 屬性
description: 指定是否應調整顯示器大小以符合控制項的工作區。 請注意，當 SmartSizing 屬性已啟用時，不會顯示捲軸。
ms.assetid: d0b93129-5f84-49c5-bf8c-048075ac1481
ms.tgt_platform: multiple
keywords:
- SmartSizing 屬性遠端桌面服務
- SmartSizing 屬性遠端桌面服務，IMsRdpClientAdvancedSettings 介面
- IMsRdpClientAdvancedSettings 介面遠端桌面服務，SmartSizing 屬性
- SmartSizing 屬性遠端桌面服務，IMsRdpClientAdvancedSettings2 介面
- IMsRdpClientAdvancedSettings2 介面遠端桌面服務，SmartSizing 屬性
- SmartSizing 屬性遠端桌面服務，IMsRdpClientAdvancedSettings3 介面
- IMsRdpClientAdvancedSettings3 介面遠端桌面服務，SmartSizing 屬性
- SmartSizing 屬性遠端桌面服務，IMsRdpClientAdvancedSettings4 介面
- IMsRdpClientAdvancedSettings4 介面遠端桌面服務，SmartSizing 屬性
- SmartSizing 屬性遠端桌面服務，IMsRdpClientAdvancedSettings5 介面
- IMsRdpClientAdvancedSettings5 介面遠端桌面服務，SmartSizing 屬性
- SmartSizing 屬性遠端桌面服務，IMsRdpClientAdvancedSettings6 介面
- IMsRdpClientAdvancedSettings6 介面遠端桌面服務，SmartSizing 屬性
- SmartSizing 屬性遠端桌面服務，IMsRdpClientAdvancedSettings7 介面
- IMsRdpClientAdvancedSettings7 介面遠端桌面服務，SmartSizing 屬性
- SmartSizing 屬性遠端桌面服務，IMsRdpClientAdvancedSettings8 介面
- IMsRdpClientAdvancedSettings8 介面遠端桌面服務，SmartSizing 屬性
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.SmartSizing
- IMsRdpClientAdvancedSettings.get_SmartSizing
- IMsRdpClientAdvancedSettings.put_SmartSizing
- IMsRdpClientAdvancedSettings2.SmartSizing
- IMsRdpClientAdvancedSettings2.get_SmartSizing
- IMsRdpClientAdvancedSettings2.put_SmartSizing
- IMsRdpClientAdvancedSettings3.SmartSizing
- IMsRdpClientAdvancedSettings3.get_SmartSizing
- IMsRdpClientAdvancedSettings3.put_SmartSizing
- IMsRdpClientAdvancedSettings4.SmartSizing
- IMsRdpClientAdvancedSettings4.get_SmartSizing
- IMsRdpClientAdvancedSettings4.put_SmartSizing
- IMsRdpClientAdvancedSettings5.SmartSizing
- IMsRdpClientAdvancedSettings5.get_SmartSizing
- IMsRdpClientAdvancedSettings5.put_SmartSizing
- IMsRdpClientAdvancedSettings6.SmartSizing
- IMsRdpClientAdvancedSettings6.get_SmartSizing
- IMsRdpClientAdvancedSettings6.put_SmartSizing
- IMsRdpClientAdvancedSettings7.SmartSizing
- IMsRdpClientAdvancedSettings7.get_SmartSizing
- IMsRdpClientAdvancedSettings7.put_SmartSizing
- IMsRdpClientAdvancedSettings8.SmartSizing
- IMsRdpClientAdvancedSettings8.get_SmartSizing
- IMsRdpClientAdvancedSettings8.put_SmartSizing
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 49ec2a825725e01d876b9e8658f215de6595f32f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104383890"
---
# <a name="imsrdpclientadvancedsettingssmartsizing-property"></a><span data-ttu-id="ab4cb-121">IMsRdpClientAdvancedSettings：： SmartSizing 屬性</span><span class="sxs-lookup"><span data-stu-id="ab4cb-121">IMsRdpClientAdvancedSettings::SmartSizing property</span></span>

<span data-ttu-id="ab4cb-122">指定是否應調整顯示器大小以符合控制項的工作區。</span><span class="sxs-lookup"><span data-stu-id="ab4cb-122">Specifies if the display should be scaled to fit the client area of the control.</span></span> <span data-ttu-id="ab4cb-123">請注意，當 **SmartSizing** 屬性已啟用時，不會顯示捲軸。</span><span class="sxs-lookup"><span data-stu-id="ab4cb-123">Note that scroll bars do not appear when the **SmartSizing** property is enabled.</span></span>

<span data-ttu-id="ab4cb-124">與大部分其他屬性不同的是，當控制項連線時，可以設定這個屬性。</span><span class="sxs-lookup"><span data-stu-id="ab4cb-124">Unlike most other properties, this property can be set when the control is connected.</span></span>

<span data-ttu-id="ab4cb-125">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="ab4cb-125">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="ab4cb-126">Syntax</span><span class="sxs-lookup"><span data-stu-id="ab4cb-126">Syntax</span></span>


```C++
HRESULT put_SmartSizing(
  [in]  VARIANT_BOOL fSmartSizing
);

HRESULT get_SmartSizing(
  [out] VARIANT_BOOL *pfSmartSizing
);
```



## <a name="property-value"></a><span data-ttu-id="ab4cb-127">屬性值</span><span class="sxs-lookup"><span data-stu-id="ab4cb-127">Property value</span></span>

<span data-ttu-id="ab4cb-128">將此參數設定為 **VARIANT \_ FALSE** ，以停用此功能或 **variant \_ TRUE** 來啟用此功能。</span><span class="sxs-lookup"><span data-stu-id="ab4cb-128">Set this parameter to **VARIANT\_FALSE** to disable the feature or **VARIANT\_TRUE** to enable the feature.</span></span>

## <a name="error-codes"></a><span data-ttu-id="ab4cb-129">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="ab4cb-129">Error codes</span></span>

<span data-ttu-id="ab4cb-130">如果成功，則傳回 **S \_ OK** 。</span><span class="sxs-lookup"><span data-stu-id="ab4cb-130">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="ab4cb-131">備註</span><span class="sxs-lookup"><span data-stu-id="ab4cb-131">Remarks</span></span>

<span data-ttu-id="ab4cb-132">如需遠端桌面網頁連線的詳細資訊，請參閱 [遠端桌面網頁連線的需求](requirements-for-remote-desktop-web-connection.md)。</span><span class="sxs-lookup"><span data-stu-id="ab4cb-132">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ab4cb-133">規格需求</span><span class="sxs-lookup"><span data-stu-id="ab4cb-133">Requirements</span></span>



| <span data-ttu-id="ab4cb-134">需求</span><span class="sxs-lookup"><span data-stu-id="ab4cb-134">Requirement</span></span> | <span data-ttu-id="ab4cb-135">值</span><span class="sxs-lookup"><span data-stu-id="ab4cb-135">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ab4cb-136">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ab4cb-136">Minimum supported client</span></span><br/> | <span data-ttu-id="ab4cb-137">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ab4cb-137">Windows Vista</span></span><br/>                                                                        |
| <span data-ttu-id="ab4cb-138">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ab4cb-138">Minimum supported server</span></span><br/> | <span data-ttu-id="ab4cb-139">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ab4cb-139">Windows Server 2008</span></span><br/>                                                                  |
| <span data-ttu-id="ab4cb-140">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="ab4cb-140">Type library</span></span><br/>             | <dl> <span data-ttu-id="ab4cb-141"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ab4cb-141"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="ab4cb-142">DLL</span><span class="sxs-lookup"><span data-stu-id="ab4cb-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ab4cb-143"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ab4cb-143"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="ab4cb-144">IID</span><span class="sxs-lookup"><span data-stu-id="ab4cb-144">IID</span></span><br/>                      | <span data-ttu-id="ab4cb-145">IID \_ IMsRdpClientAdvancedSettings 定義為3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span><span class="sxs-lookup"><span data-stu-id="ab4cb-145">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ab4cb-146">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ab4cb-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ab4cb-147">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="ab4cb-147">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="ab4cb-148">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="ab4cb-148">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="ab4cb-149">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="ab4cb-149">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="ab4cb-150">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="ab4cb-150">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="ab4cb-151">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="ab4cb-151">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="ab4cb-152">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="ab4cb-152">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="ab4cb-153">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="ab4cb-153">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="ab4cb-154">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="ab4cb-154">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





