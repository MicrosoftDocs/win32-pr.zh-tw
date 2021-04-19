---
title: IMsRdpClientAdvancedSettings DisplayConnectionBar 屬性
description: 指定是否使用連接列。 預設值為 VARIANT \_ TRUE，可啟用屬性。
ms.assetid: 251c0322-5589-423d-9694-004f847c173b
ms.tgt_platform: multiple
keywords:
- DisplayConnectionBar 屬性遠端桌面服務
- DisplayConnectionBar 屬性遠端桌面服務，IMsRdpClientAdvancedSettings 介面
- IMsRdpClientAdvancedSettings 介面遠端桌面服務，DisplayConnectionBar 屬性
- DisplayConnectionBar 屬性遠端桌面服務，IMsRdpClientAdvancedSettings2 介面
- IMsRdpClientAdvancedSettings2 介面遠端桌面服務，DisplayConnectionBar 屬性
- DisplayConnectionBar 屬性遠端桌面服務，IMsRdpClientAdvancedSettings3 介面
- IMsRdpClientAdvancedSettings3 介面遠端桌面服務，DisplayConnectionBar 屬性
- DisplayConnectionBar 屬性遠端桌面服務，IMsRdpClientAdvancedSettings4 介面
- IMsRdpClientAdvancedSettings4 介面遠端桌面服務，DisplayConnectionBar 屬性
- DisplayConnectionBar 屬性遠端桌面服務，IMsRdpClientAdvancedSettings5 介面
- IMsRdpClientAdvancedSettings5 介面遠端桌面服務，DisplayConnectionBar 屬性
- DisplayConnectionBar 屬性遠端桌面服務，IMsRdpClientAdvancedSettings6 介面
- IMsRdpClientAdvancedSettings6 介面遠端桌面服務，DisplayConnectionBar 屬性
- DisplayConnectionBar 屬性遠端桌面服務，IMsRdpClientAdvancedSettings7 介面
- IMsRdpClientAdvancedSettings7 介面遠端桌面服務，DisplayConnectionBar 屬性
- DisplayConnectionBar 屬性遠端桌面服務，IMsRdpClientAdvancedSettings8 介面
- IMsRdpClientAdvancedSettings8 介面遠端桌面服務，DisplayConnectionBar 屬性
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.DisplayConnectionBar
- IMsRdpClientAdvancedSettings.get_DisplayConnectionBar
- IMsRdpClientAdvancedSettings.put_DisplayConnectionBar
- IMsRdpClientAdvancedSettings2.DisplayConnectionBar
- IMsRdpClientAdvancedSettings2.get_DisplayConnectionBar
- IMsRdpClientAdvancedSettings2.put_DisplayConnectionBar
- IMsRdpClientAdvancedSettings3.DisplayConnectionBar
- IMsRdpClientAdvancedSettings3.get_DisplayConnectionBar
- IMsRdpClientAdvancedSettings3.put_DisplayConnectionBar
- IMsRdpClientAdvancedSettings4.DisplayConnectionBar
- IMsRdpClientAdvancedSettings4.get_DisplayConnectionBar
- IMsRdpClientAdvancedSettings4.put_DisplayConnectionBar
- IMsRdpClientAdvancedSettings5.DisplayConnectionBar
- IMsRdpClientAdvancedSettings5.get_DisplayConnectionBar
- IMsRdpClientAdvancedSettings5.put_DisplayConnectionBar
- IMsRdpClientAdvancedSettings6.DisplayConnectionBar
- IMsRdpClientAdvancedSettings6.get_DisplayConnectionBar
- IMsRdpClientAdvancedSettings6.put_DisplayConnectionBar
- IMsRdpClientAdvancedSettings7.DisplayConnectionBar
- IMsRdpClientAdvancedSettings7.get_DisplayConnectionBar
- IMsRdpClientAdvancedSettings7.put_DisplayConnectionBar
- IMsRdpClientAdvancedSettings8.DisplayConnectionBar
- IMsRdpClientAdvancedSettings8.get_DisplayConnectionBar
- IMsRdpClientAdvancedSettings8.put_DisplayConnectionBar
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 39dd85d0c8fd578931ed9ca8b85ac7a5ca01981e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106967725"
---
# <a name="imsrdpclientadvancedsettingsdisplayconnectionbar-property"></a><span data-ttu-id="af97c-121">IMsRdpClientAdvancedSettings：:D isplayConnectionBar 屬性</span><span class="sxs-lookup"><span data-stu-id="af97c-121">IMsRdpClientAdvancedSettings::DisplayConnectionBar property</span></span>

<span data-ttu-id="af97c-122">指定是否使用連接列。</span><span class="sxs-lookup"><span data-stu-id="af97c-122">Specifies whether to use the connection bar.</span></span> <span data-ttu-id="af97c-123">預設值為 **VARIANT \_ TRUE**，可啟用屬性。</span><span class="sxs-lookup"><span data-stu-id="af97c-123">The default value is **VARIANT\_TRUE**, which enables the property.</span></span> <span data-ttu-id="af97c-124">在安全腳本環境中將這個屬性設定為 **VARIANT \_ FALSE** ， **會傳回 E \_ FAIL**。</span><span class="sxs-lookup"><span data-stu-id="af97c-124">Setting this property to **VARIANT\_FALSE** in a safe scripting environment returns **E\_FAIL**.</span></span>

<span data-ttu-id="af97c-125">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="af97c-125">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="af97c-126">Syntax</span><span class="sxs-lookup"><span data-stu-id="af97c-126">Syntax</span></span>


```C++
HRESULT put_DisplayConnectionBar(
  [in]  VARIANT_BOOL fDisplayConnectionBar
);

HRESULT get_DisplayConnectionBar(
  [out] VARIANT_BOOL *pfDisplayConnectionBar
);
```



## <a name="property-value"></a><span data-ttu-id="af97c-127">屬性值</span><span class="sxs-lookup"><span data-stu-id="af97c-127">Property value</span></span>

<span data-ttu-id="af97c-128">將此參數設定為 **VARIANT \_ FALSE** ，以停用此功能或 **variant \_ TRUE** 來啟用此功能。</span><span class="sxs-lookup"><span data-stu-id="af97c-128">Set this parameter to **VARIANT\_FALSE** to disable the feature or **VARIANT\_TRUE** to enable the feature.</span></span> <span data-ttu-id="af97c-129">預設值為 **VARIANT \_ TRUE**。</span><span class="sxs-lookup"><span data-stu-id="af97c-129">The default value is **VARIANT\_TRUE**.</span></span>

## <a name="error-codes"></a><span data-ttu-id="af97c-130">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="af97c-130">Error codes</span></span>

<span data-ttu-id="af97c-131">如果成功，則傳回 **S \_ OK** 。</span><span class="sxs-lookup"><span data-stu-id="af97c-131">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="af97c-132">備註</span><span class="sxs-lookup"><span data-stu-id="af97c-132">Remarks</span></span>

<span data-ttu-id="af97c-133">如需遠端桌面網頁連線的詳細資訊，請參閱 [遠端桌面網頁連線的需求](requirements-for-remote-desktop-web-connection.md)。</span><span class="sxs-lookup"><span data-stu-id="af97c-133">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="af97c-134">規格需求</span><span class="sxs-lookup"><span data-stu-id="af97c-134">Requirements</span></span>



| <span data-ttu-id="af97c-135">需求</span><span class="sxs-lookup"><span data-stu-id="af97c-135">Requirement</span></span> | <span data-ttu-id="af97c-136">值</span><span class="sxs-lookup"><span data-stu-id="af97c-136">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="af97c-137">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="af97c-137">Minimum supported client</span></span><br/> | <span data-ttu-id="af97c-138">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="af97c-138">Windows Vista</span></span><br/>                                                                        |
| <span data-ttu-id="af97c-139">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="af97c-139">Minimum supported server</span></span><br/> | <span data-ttu-id="af97c-140">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="af97c-140">Windows Server 2008</span></span><br/>                                                                  |
| <span data-ttu-id="af97c-141">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="af97c-141">Type library</span></span><br/>             | <dl> <span data-ttu-id="af97c-142"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="af97c-142"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="af97c-143">DLL</span><span class="sxs-lookup"><span data-stu-id="af97c-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="af97c-144"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="af97c-144"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="af97c-145">IID</span><span class="sxs-lookup"><span data-stu-id="af97c-145">IID</span></span><br/>                      | <span data-ttu-id="af97c-146">IID \_ IMsRdpClientAdvancedSettings 定義為3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span><span class="sxs-lookup"><span data-stu-id="af97c-146">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="af97c-147">另請參閱</span><span class="sxs-lookup"><span data-stu-id="af97c-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="af97c-148">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="af97c-148">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="af97c-149">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="af97c-149">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="af97c-150">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="af97c-150">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="af97c-151">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="af97c-151">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="af97c-152">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="af97c-152">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="af97c-153">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="af97c-153">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="af97c-154">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="af97c-154">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="af97c-155">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="af97c-155">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





