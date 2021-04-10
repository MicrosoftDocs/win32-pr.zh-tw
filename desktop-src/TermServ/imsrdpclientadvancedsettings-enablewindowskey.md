---
title: IMsRdpClientAdvancedSettings EnableWindowsKey 屬性
description: 指定是否可以在遠端會話中使用 Windows 金鑰。
ms.assetid: fcf0460d-3cd1-4da4-8009-0b1256adf312
ms.tgt_platform: multiple
keywords:
- EnableWindowsKey 屬性遠端桌面服務
- EnableWindowsKey 屬性遠端桌面服務，IMsRdpClientAdvancedSettings 介面
- IMsRdpClientAdvancedSettings 介面遠端桌面服務，EnableWindowsKey 屬性
- EnableWindowsKey 屬性遠端桌面服務，IMsRdpClientAdvancedSettings2 介面
- IMsRdpClientAdvancedSettings2 介面遠端桌面服務，EnableWindowsKey 屬性
- EnableWindowsKey 屬性遠端桌面服務，IMsRdpClientAdvancedSettings3 介面
- IMsRdpClientAdvancedSettings3 介面遠端桌面服務，EnableWindowsKey 屬性
- EnableWindowsKey 屬性遠端桌面服務，IMsRdpClientAdvancedSettings4 介面
- IMsRdpClientAdvancedSettings4 介面遠端桌面服務，EnableWindowsKey 屬性
- EnableWindowsKey 屬性遠端桌面服務，IMsRdpClientAdvancedSettings5 介面
- IMsRdpClientAdvancedSettings5 介面遠端桌面服務，EnableWindowsKey 屬性
- EnableWindowsKey 屬性遠端桌面服務，IMsRdpClientAdvancedSettings6 介面
- IMsRdpClientAdvancedSettings6 介面遠端桌面服務，EnableWindowsKey 屬性
- EnableWindowsKey 屬性遠端桌面服務，IMsRdpClientAdvancedSettings7 介面
- IMsRdpClientAdvancedSettings7 介面遠端桌面服務，EnableWindowsKey 屬性
- EnableWindowsKey 屬性遠端桌面服務，IMsRdpClientAdvancedSettings8 介面
- IMsRdpClientAdvancedSettings8 介面遠端桌面服務，EnableWindowsKey 屬性
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.EnableWindowsKey
- IMsRdpClientAdvancedSettings.get_EnableWindowsKey
- IMsRdpClientAdvancedSettings.put_EnableWindowsKey
- IMsRdpClientAdvancedSettings2.EnableWindowsKey
- IMsRdpClientAdvancedSettings2.get_EnableWindowsKey
- IMsRdpClientAdvancedSettings2.put_EnableWindowsKey
- IMsRdpClientAdvancedSettings3.EnableWindowsKey
- IMsRdpClientAdvancedSettings3.get_EnableWindowsKey
- IMsRdpClientAdvancedSettings3.put_EnableWindowsKey
- IMsRdpClientAdvancedSettings4.EnableWindowsKey
- IMsRdpClientAdvancedSettings4.get_EnableWindowsKey
- IMsRdpClientAdvancedSettings4.put_EnableWindowsKey
- IMsRdpClientAdvancedSettings5.EnableWindowsKey
- IMsRdpClientAdvancedSettings5.get_EnableWindowsKey
- IMsRdpClientAdvancedSettings5.put_EnableWindowsKey
- IMsRdpClientAdvancedSettings6.EnableWindowsKey
- IMsRdpClientAdvancedSettings6.get_EnableWindowsKey
- IMsRdpClientAdvancedSettings6.put_EnableWindowsKey
- IMsRdpClientAdvancedSettings7.EnableWindowsKey
- IMsRdpClientAdvancedSettings7.get_EnableWindowsKey
- IMsRdpClientAdvancedSettings7.put_EnableWindowsKey
- IMsRdpClientAdvancedSettings8.EnableWindowsKey
- IMsRdpClientAdvancedSettings8.get_EnableWindowsKey
- IMsRdpClientAdvancedSettings8.put_EnableWindowsKey
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e31571e44d6b391250c32268750b25a76105eb2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686357"
---
# <a name="imsrdpclientadvancedsettingsenablewindowskey-property"></a><span data-ttu-id="32cc1-120">IMsRdpClientAdvancedSettings：： EnableWindowsKey 屬性</span><span class="sxs-lookup"><span data-stu-id="32cc1-120">IMsRdpClientAdvancedSettings::EnableWindowsKey property</span></span>

<span data-ttu-id="32cc1-121">指定是否可以在遠端會話中使用 Windows 金鑰。</span><span class="sxs-lookup"><span data-stu-id="32cc1-121">Specifies if the Windows key can be used in the remote session.</span></span>

<span data-ttu-id="32cc1-122">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="32cc1-122">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="32cc1-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="32cc1-123">Syntax</span></span>


```C++
HRESULT put_EnableWindowsKey(
  [in]  LONG enableWindowsKey
);

HRESULT get_EnableWindowsKey(
  [out] LONG *penableWindowsKey
);
```



## <a name="property-value"></a><span data-ttu-id="32cc1-124">屬性值</span><span class="sxs-lookup"><span data-stu-id="32cc1-124">Property value</span></span>

<span data-ttu-id="32cc1-125">將此參數設定為0，以停用此功能或非零值以啟用此功能。</span><span class="sxs-lookup"><span data-stu-id="32cc1-125">Set this parameter to 0 to disable the feature or a nonzero value to enable the feature.</span></span>

## <a name="error-codes"></a><span data-ttu-id="32cc1-126">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="32cc1-126">Error codes</span></span>

<span data-ttu-id="32cc1-127">如果成功，則傳回 **S \_ OK** 。</span><span class="sxs-lookup"><span data-stu-id="32cc1-127">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="32cc1-128">備註</span><span class="sxs-lookup"><span data-stu-id="32cc1-128">Remarks</span></span>

<span data-ttu-id="32cc1-129">如需遠端桌面網頁連線的詳細資訊，請參閱 [遠端桌面網頁連線的需求](requirements-for-remote-desktop-web-connection.md)。</span><span class="sxs-lookup"><span data-stu-id="32cc1-129">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="32cc1-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="32cc1-130">Requirements</span></span>



| <span data-ttu-id="32cc1-131">需求</span><span class="sxs-lookup"><span data-stu-id="32cc1-131">Requirement</span></span> | <span data-ttu-id="32cc1-132">值</span><span class="sxs-lookup"><span data-stu-id="32cc1-132">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="32cc1-133">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="32cc1-133">Minimum supported client</span></span><br/> | <span data-ttu-id="32cc1-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="32cc1-134">Windows Vista</span></span><br/>                                                                        |
| <span data-ttu-id="32cc1-135">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="32cc1-135">Minimum supported server</span></span><br/> | <span data-ttu-id="32cc1-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="32cc1-136">Windows Server 2008</span></span><br/>                                                                  |
| <span data-ttu-id="32cc1-137">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="32cc1-137">Type library</span></span><br/>             | <dl> <span data-ttu-id="32cc1-138"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="32cc1-138"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="32cc1-139">DLL</span><span class="sxs-lookup"><span data-stu-id="32cc1-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="32cc1-140"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="32cc1-140"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="32cc1-141">IID</span><span class="sxs-lookup"><span data-stu-id="32cc1-141">IID</span></span><br/>                      | <span data-ttu-id="32cc1-142">IID \_ IMsRdpClientAdvancedSettings 定義為3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span><span class="sxs-lookup"><span data-stu-id="32cc1-142">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="32cc1-143">另請參閱</span><span class="sxs-lookup"><span data-stu-id="32cc1-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="32cc1-144">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="32cc1-144">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="32cc1-145">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="32cc1-145">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="32cc1-146">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="32cc1-146">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="32cc1-147">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="32cc1-147">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="32cc1-148">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="32cc1-148">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="32cc1-149">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="32cc1-149">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="32cc1-150">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="32cc1-150">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="32cc1-151">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="32cc1-151">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





