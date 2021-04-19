---
title: IMsRdpClientAdvancedSettings AcceleratorPassthrough 屬性
description: 指定是否應將鍵盤快速鍵傳遞到伺服器。
ms.assetid: ad0053bc-e3a9-4cd5-a409-fab3e24ffffa
ms.tgt_platform: multiple
keywords:
- AcceleratorPassthrough 屬性遠端桌面服務
- AcceleratorPassthrough 屬性遠端桌面服務，IMsRdpClientAdvancedSettings 介面
- IMsRdpClientAdvancedSettings 介面遠端桌面服務，AcceleratorPassthrough 屬性
- AcceleratorPassthrough 屬性遠端桌面服務，IMsRdpClientAdvancedSettings2 介面
- IMsRdpClientAdvancedSettings2 介面遠端桌面服務，AcceleratorPassthrough 屬性
- AcceleratorPassthrough 屬性遠端桌面服務，IMsRdpClientAdvancedSettings3 介面
- IMsRdpClientAdvancedSettings3 介面遠端桌面服務，AcceleratorPassthrough 屬性
- AcceleratorPassthrough 屬性遠端桌面服務，IMsRdpClientAdvancedSettings4 介面
- IMsRdpClientAdvancedSettings4 介面遠端桌面服務，AcceleratorPassthrough 屬性
- AcceleratorPassthrough 屬性遠端桌面服務，IMsRdpClientAdvancedSettings5 介面
- IMsRdpClientAdvancedSettings5 介面遠端桌面服務，AcceleratorPassthrough 屬性
- AcceleratorPassthrough 屬性遠端桌面服務，IMsRdpClientAdvancedSettings6 介面
- IMsRdpClientAdvancedSettings6 介面遠端桌面服務，AcceleratorPassthrough 屬性
- AcceleratorPassthrough 屬性遠端桌面服務，IMsRdpClientAdvancedSettings7 介面
- IMsRdpClientAdvancedSettings7 介面遠端桌面服務，AcceleratorPassthrough 屬性
- AcceleratorPassthrough 屬性遠端桌面服務，IMsRdpClientAdvancedSettings8 介面
- IMsRdpClientAdvancedSettings8 介面遠端桌面服務，AcceleratorPassthrough 屬性
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.AcceleratorPassthrough
- IMsRdpClientAdvancedSettings.get_AcceleratorPassthrough
- IMsRdpClientAdvancedSettings.put_AcceleratorPassthrough
- IMsRdpClientAdvancedSettings2.AcceleratorPassthrough
- IMsRdpClientAdvancedSettings2.get_AcceleratorPassthrough
- IMsRdpClientAdvancedSettings2.put_AcceleratorPassthrough
- IMsRdpClientAdvancedSettings3.AcceleratorPassthrough
- IMsRdpClientAdvancedSettings3.get_AcceleratorPassthrough
- IMsRdpClientAdvancedSettings3.put_AcceleratorPassthrough
- IMsRdpClientAdvancedSettings4.AcceleratorPassthrough
- IMsRdpClientAdvancedSettings4.get_AcceleratorPassthrough
- IMsRdpClientAdvancedSettings4.put_AcceleratorPassthrough
- IMsRdpClientAdvancedSettings5.AcceleratorPassthrough
- IMsRdpClientAdvancedSettings5.get_AcceleratorPassthrough
- IMsRdpClientAdvancedSettings5.put_AcceleratorPassthrough
- IMsRdpClientAdvancedSettings6.AcceleratorPassthrough
- IMsRdpClientAdvancedSettings6.get_AcceleratorPassthrough
- IMsRdpClientAdvancedSettings6.put_AcceleratorPassthrough
- IMsRdpClientAdvancedSettings7.AcceleratorPassthrough
- IMsRdpClientAdvancedSettings7.get_AcceleratorPassthrough
- IMsRdpClientAdvancedSettings7.put_AcceleratorPassthrough
- IMsRdpClientAdvancedSettings8.AcceleratorPassthrough
- IMsRdpClientAdvancedSettings8.get_AcceleratorPassthrough
- IMsRdpClientAdvancedSettings8.put_AcceleratorPassthrough
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c252c5c0477f331b66cf65b93ed2cab844fb88e8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106966300"
---
# <a name="imsrdpclientadvancedsettingsacceleratorpassthrough-property"></a><span data-ttu-id="ccf71-120">IMsRdpClientAdvancedSettings：： AcceleratorPassthrough 屬性</span><span class="sxs-lookup"><span data-stu-id="ccf71-120">IMsRdpClientAdvancedSettings::AcceleratorPassthrough property</span></span>

<span data-ttu-id="ccf71-121">指定是否應將鍵盤快速鍵傳遞到伺服器。</span><span class="sxs-lookup"><span data-stu-id="ccf71-121">Specifies if keyboard accelerators should be passed to the server.</span></span>

<span data-ttu-id="ccf71-122">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="ccf71-122">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="ccf71-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="ccf71-123">Syntax</span></span>


```C++
HRESULT put_AcceleratorPassthrough(
  [in]  LONG acceleratorPassthrough
);

HRESULT get_AcceleratorPassthrough(
  [out] LONG *pacceleratorPassthrough
);
```



## <a name="property-value"></a><span data-ttu-id="ccf71-124">屬性值</span><span class="sxs-lookup"><span data-stu-id="ccf71-124">Property value</span></span>

<span data-ttu-id="ccf71-125">將此參數設定為0，以停用此功能或非零值以啟用此功能。</span><span class="sxs-lookup"><span data-stu-id="ccf71-125">Set this parameter to 0 to disable the feature or a nonzero value to enable the feature.</span></span> <span data-ttu-id="ccf71-126">預設值為非零值。</span><span class="sxs-lookup"><span data-stu-id="ccf71-126">The default is a nonzero value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="ccf71-127">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="ccf71-127">Error codes</span></span>

<span data-ttu-id="ccf71-128">如果成功，則傳回 **S \_ OK** 。</span><span class="sxs-lookup"><span data-stu-id="ccf71-128">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="ccf71-129">備註</span><span class="sxs-lookup"><span data-stu-id="ccf71-129">Remarks</span></span>

<span data-ttu-id="ccf71-130">如需遠端桌面網頁連線的詳細資訊，請參閱 [遠端桌面網頁連線的需求](requirements-for-remote-desktop-web-connection.md)。</span><span class="sxs-lookup"><span data-stu-id="ccf71-130">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ccf71-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="ccf71-131">Requirements</span></span>



| <span data-ttu-id="ccf71-132">需求</span><span class="sxs-lookup"><span data-stu-id="ccf71-132">Requirement</span></span> | <span data-ttu-id="ccf71-133">值</span><span class="sxs-lookup"><span data-stu-id="ccf71-133">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ccf71-134">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ccf71-134">Minimum supported client</span></span><br/> | <span data-ttu-id="ccf71-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ccf71-135">Windows Vista</span></span><br/>                                                                        |
| <span data-ttu-id="ccf71-136">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ccf71-136">Minimum supported server</span></span><br/> | <span data-ttu-id="ccf71-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ccf71-137">Windows Server 2008</span></span><br/>                                                                  |
| <span data-ttu-id="ccf71-138">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="ccf71-138">Type library</span></span><br/>             | <dl> <span data-ttu-id="ccf71-139"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ccf71-139"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="ccf71-140">DLL</span><span class="sxs-lookup"><span data-stu-id="ccf71-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ccf71-141"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ccf71-141"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="ccf71-142">IID</span><span class="sxs-lookup"><span data-stu-id="ccf71-142">IID</span></span><br/>                      | <span data-ttu-id="ccf71-143">IID \_ IMsRdpClientAdvancedSettings 定義為3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span><span class="sxs-lookup"><span data-stu-id="ccf71-143">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ccf71-144">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ccf71-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ccf71-145">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="ccf71-145">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="ccf71-146">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="ccf71-146">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="ccf71-147">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="ccf71-147">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="ccf71-148">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="ccf71-148">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="ccf71-149">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="ccf71-149">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="ccf71-150">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="ccf71-150">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="ccf71-151">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="ccf71-151">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="ccf71-152">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="ccf71-152">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





