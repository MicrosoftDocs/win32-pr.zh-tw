---
title: IMsRdpClientAdvancedSettings EnableMouse 屬性
description: 不支援這個屬性。 |IMsRdpClientAdvancedSettings EnableMouse 屬性
ms.assetid: 4f60fdfc-e1b9-4ac2-98e4-49331b072883
ms.tgt_platform: multiple
keywords:
- EnableMouse 屬性遠端桌面服務
- EnableMouse 屬性遠端桌面服務，IMsRdpClientAdvancedSettings 介面
- IMsRdpClientAdvancedSettings 介面遠端桌面服務，EnableMouse 屬性
- EnableMouse 屬性遠端桌面服務，IMsRdpClientAdvancedSettings2 介面
- IMsRdpClientAdvancedSettings2 介面遠端桌面服務，EnableMouse 屬性
- EnableMouse 屬性遠端桌面服務，IMsRdpClientAdvancedSettings3 介面
- IMsRdpClientAdvancedSettings3 介面遠端桌面服務，EnableMouse 屬性
- EnableMouse 屬性遠端桌面服務，IMsRdpClientAdvancedSettings4 介面
- IMsRdpClientAdvancedSettings4 介面遠端桌面服務，EnableMouse 屬性
- EnableMouse 屬性遠端桌面服務，IMsRdpClientAdvancedSettings5 介面
- IMsRdpClientAdvancedSettings5 介面遠端桌面服務，EnableMouse 屬性
- EnableMouse 屬性遠端桌面服務，IMsRdpClientAdvancedSettings6 介面
- IMsRdpClientAdvancedSettings6 介面遠端桌面服務，EnableMouse 屬性
- EnableMouse 屬性遠端桌面服務，IMsRdpClientAdvancedSettings7 介面
- IMsRdpClientAdvancedSettings7 介面遠端桌面服務，EnableMouse 屬性
- EnableMouse 屬性遠端桌面服務，IMsRdpClientAdvancedSettings8 介面
- IMsRdpClientAdvancedSettings8 介面遠端桌面服務，EnableMouse 屬性
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.EnableMouse
- IMsRdpClientAdvancedSettings.get_EnableMouse
- IMsRdpClientAdvancedSettings.put_EnableMouse
- IMsRdpClientAdvancedSettings2.EnableMouse
- IMsRdpClientAdvancedSettings2.get_EnableMouse
- IMsRdpClientAdvancedSettings2.put_EnableMouse
- IMsRdpClientAdvancedSettings3.EnableMouse
- IMsRdpClientAdvancedSettings3.get_EnableMouse
- IMsRdpClientAdvancedSettings3.put_EnableMouse
- IMsRdpClientAdvancedSettings4.EnableMouse
- IMsRdpClientAdvancedSettings4.get_EnableMouse
- IMsRdpClientAdvancedSettings4.put_EnableMouse
- IMsRdpClientAdvancedSettings5.EnableMouse
- IMsRdpClientAdvancedSettings5.get_EnableMouse
- IMsRdpClientAdvancedSettings5.put_EnableMouse
- IMsRdpClientAdvancedSettings6.EnableMouse
- IMsRdpClientAdvancedSettings6.get_EnableMouse
- IMsRdpClientAdvancedSettings6.put_EnableMouse
- IMsRdpClientAdvancedSettings7.EnableMouse
- IMsRdpClientAdvancedSettings7.get_EnableMouse
- IMsRdpClientAdvancedSettings7.put_EnableMouse
- IMsRdpClientAdvancedSettings8.EnableMouse
- IMsRdpClientAdvancedSettings8.get_EnableMouse
- IMsRdpClientAdvancedSettings8.put_EnableMouse
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0495ba7b48e431efe5746f40b353b5c1ad701d6a
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "103945784"
---
# <a name="imsrdpclientadvancedsettingsenablemouse-property"></a><span data-ttu-id="0d10f-121">IMsRdpClientAdvancedSettings：： EnableMouse 屬性</span><span class="sxs-lookup"><span data-stu-id="0d10f-121">IMsRdpClientAdvancedSettings::EnableMouse property</span></span>

<span data-ttu-id="0d10f-122">不支援這個屬性。</span><span class="sxs-lookup"><span data-stu-id="0d10f-122">This property is not supported.</span></span>

<span data-ttu-id="0d10f-123">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="0d10f-123">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="0d10f-124">Syntax</span><span class="sxs-lookup"><span data-stu-id="0d10f-124">Syntax</span></span>


```C++
HRESULT put_EnableMouse(
  [in]  LONG enableMouse
);

HRESULT get_EnableMouse(
  [out] LONG *penableMouse
);
```



## <a name="property-value"></a><span data-ttu-id="0d10f-125">屬性值</span><span class="sxs-lookup"><span data-stu-id="0d10f-125">Property value</span></span>

<span data-ttu-id="0d10f-126">將此參數設定為0，以停用此功能或非零值以啟用此功能。</span><span class="sxs-lookup"><span data-stu-id="0d10f-126">Set this parameter to 0 to disable the feature or a nonzero value to enable the feature.</span></span>

## <a name="error-codes"></a><span data-ttu-id="0d10f-127">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="0d10f-127">Error codes</span></span>

<span data-ttu-id="0d10f-128">傳回 **\_ FALSE**。</span><span class="sxs-lookup"><span data-stu-id="0d10f-128">Returns **S\_FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="0d10f-129">備註</span><span class="sxs-lookup"><span data-stu-id="0d10f-129">Remarks</span></span>

<span data-ttu-id="0d10f-130">如需遠端桌面網頁連線的詳細資訊，請參閱 [遠端桌面網頁連線的需求](requirements-for-remote-desktop-web-connection.md)。</span><span class="sxs-lookup"><span data-stu-id="0d10f-130">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="0d10f-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="0d10f-131">Requirements</span></span>



| <span data-ttu-id="0d10f-132">需求</span><span class="sxs-lookup"><span data-stu-id="0d10f-132">Requirement</span></span> | <span data-ttu-id="0d10f-133">值</span><span class="sxs-lookup"><span data-stu-id="0d10f-133">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0d10f-134">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0d10f-134">Minimum supported client</span></span><br/> | <span data-ttu-id="0d10f-135">都不支援</span><span class="sxs-lookup"><span data-stu-id="0d10f-135">None supported</span></span><br/>                                                                       |
| <span data-ttu-id="0d10f-136">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0d10f-136">Minimum supported server</span></span><br/> | <span data-ttu-id="0d10f-137">都不支援</span><span class="sxs-lookup"><span data-stu-id="0d10f-137">None supported</span></span><br/>                                                                       |
| <span data-ttu-id="0d10f-138">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="0d10f-138">End of client support</span></span><br/>    | <span data-ttu-id="0d10f-139">都不支援</span><span class="sxs-lookup"><span data-stu-id="0d10f-139">None supported</span></span><br/>                                                                       |
| <span data-ttu-id="0d10f-140">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="0d10f-140">End of server support</span></span><br/>    | <span data-ttu-id="0d10f-141">都不支援</span><span class="sxs-lookup"><span data-stu-id="0d10f-141">None supported</span></span><br/>                                                                       |
| <span data-ttu-id="0d10f-142">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="0d10f-142">Type library</span></span><br/>             | <dl> <span data-ttu-id="0d10f-143"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0d10f-143"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="0d10f-144">DLL</span><span class="sxs-lookup"><span data-stu-id="0d10f-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0d10f-145"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0d10f-145"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="0d10f-146">IID</span><span class="sxs-lookup"><span data-stu-id="0d10f-146">IID</span></span><br/>                      | <span data-ttu-id="0d10f-147">IID \_ IMsRdpClientAdvancedSettings 定義為3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span><span class="sxs-lookup"><span data-stu-id="0d10f-147">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="0d10f-148">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0d10f-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d10f-149">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="0d10f-149">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="0d10f-150">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="0d10f-150">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="0d10f-151">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="0d10f-151">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="0d10f-152">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="0d10f-152">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="0d10f-153">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="0d10f-153">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="0d10f-154">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="0d10f-154">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="0d10f-155">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="0d10f-155">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="0d10f-156">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="0d10f-156">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





