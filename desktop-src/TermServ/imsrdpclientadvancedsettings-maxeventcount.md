---
title: IMsRdpClientAdvancedSettings maxEventCount 屬性
description: 不支援這個屬性。 |IMsRdpClientAdvancedSettings maxEventCount 屬性
ms.assetid: d7b5951d-8cc3-48b4-af1b-1f547afbc6ae
ms.tgt_platform: multiple
keywords:
- maxEventCount 屬性遠端桌面服務
- maxEventCount 屬性遠端桌面服務，IMsRdpClientAdvancedSettings 介面
- IMsRdpClientAdvancedSettings 介面遠端桌面服務，maxEventCount 屬性
- maxEventCount 屬性遠端桌面服務，IMsRdpClientAdvancedSettings2 介面
- IMsRdpClientAdvancedSettings2 介面遠端桌面服務，maxEventCount 屬性
- maxEventCount 屬性遠端桌面服務，IMsRdpClientAdvancedSettings3 介面
- IMsRdpClientAdvancedSettings3 介面遠端桌面服務，maxEventCount 屬性
- maxEventCount 屬性遠端桌面服務，IMsRdpClientAdvancedSettings4 介面
- IMsRdpClientAdvancedSettings4 介面遠端桌面服務，maxEventCount 屬性
- maxEventCount 屬性遠端桌面服務，IMsRdpClientAdvancedSettings5 介面
- IMsRdpClientAdvancedSettings5 介面遠端桌面服務，maxEventCount 屬性
- maxEventCount 屬性遠端桌面服務，IMsRdpClientAdvancedSettings6 介面
- IMsRdpClientAdvancedSettings6 介面遠端桌面服務，maxEventCount 屬性
- maxEventCount 屬性遠端桌面服務，IMsRdpClientAdvancedSettings7 介面
- IMsRdpClientAdvancedSettings7 介面遠端桌面服務，maxEventCount 屬性
- maxEventCount 屬性遠端桌面服務，IMsRdpClientAdvancedSettings8 介面
- IMsRdpClientAdvancedSettings8 介面遠端桌面服務，maxEventCount 屬性
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.maxEventCount
- IMsRdpClientAdvancedSettings.get_maxEventCount
- IMsRdpClientAdvancedSettings.put_maxEventCount
- IMsRdpClientAdvancedSettings2.maxEventCount
- IMsRdpClientAdvancedSettings2.get_maxEventCount
- IMsRdpClientAdvancedSettings2.put_maxEventCount
- IMsRdpClientAdvancedSettings3.maxEventCount
- IMsRdpClientAdvancedSettings3.get_maxEventCount
- IMsRdpClientAdvancedSettings3.put_maxEventCount
- IMsRdpClientAdvancedSettings4.maxEventCount
- IMsRdpClientAdvancedSettings4.get_maxEventCount
- IMsRdpClientAdvancedSettings4.put_maxEventCount
- IMsRdpClientAdvancedSettings5.maxEventCount
- IMsRdpClientAdvancedSettings5.get_maxEventCount
- IMsRdpClientAdvancedSettings5.put_maxEventCount
- IMsRdpClientAdvancedSettings6.maxEventCount
- IMsRdpClientAdvancedSettings6.get_maxEventCount
- IMsRdpClientAdvancedSettings6.put_maxEventCount
- IMsRdpClientAdvancedSettings7.maxEventCount
- IMsRdpClientAdvancedSettings7.get_maxEventCount
- IMsRdpClientAdvancedSettings7.put_maxEventCount
- IMsRdpClientAdvancedSettings8.maxEventCount
- IMsRdpClientAdvancedSettings8.get_maxEventCount
- IMsRdpClientAdvancedSettings8.put_maxEventCount
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb305d4a81b3c4dd9eb53dceab5a4e685c57c060
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "103853660"
---
# <a name="imsrdpclientadvancedsettingsmaxeventcount-property"></a><span data-ttu-id="e3662-121">IMsRdpClientAdvancedSettings：： maxEventCount 屬性</span><span class="sxs-lookup"><span data-stu-id="e3662-121">IMsRdpClientAdvancedSettings::maxEventCount property</span></span>

<span data-ttu-id="e3662-122">不支援這個屬性。</span><span class="sxs-lookup"><span data-stu-id="e3662-122">This property is not supported.</span></span>

<span data-ttu-id="e3662-123">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="e3662-123">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="e3662-124">Syntax</span><span class="sxs-lookup"><span data-stu-id="e3662-124">Syntax</span></span>


```C++
HRESULT put_maxEventCount(
  [in]  LONG maxEventCount
);

HRESULT get_maxEventCount(
  [out] LONG pmaxEventCount
);
```



## <a name="property-value"></a><span data-ttu-id="e3662-125">屬性值</span><span class="sxs-lookup"><span data-stu-id="e3662-125">Property value</span></span>

<span data-ttu-id="e3662-126">新的事件計數。</span><span class="sxs-lookup"><span data-stu-id="e3662-126">The new event count.</span></span> <span data-ttu-id="e3662-127">預設值為 100。</span><span class="sxs-lookup"><span data-stu-id="e3662-127">The default is 100.</span></span>

## <a name="error-codes"></a><span data-ttu-id="e3662-128">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="e3662-128">Error codes</span></span>

<span data-ttu-id="e3662-129">傳回 **\_ FALSE**。</span><span class="sxs-lookup"><span data-stu-id="e3662-129">Returns **S\_FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="e3662-130">備註</span><span class="sxs-lookup"><span data-stu-id="e3662-130">Remarks</span></span>

<span data-ttu-id="e3662-131">如需遠端桌面網頁連線的詳細資訊，請參閱 [遠端桌面網頁連線的需求](requirements-for-remote-desktop-web-connection.md)。</span><span class="sxs-lookup"><span data-stu-id="e3662-131">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e3662-132">規格需求</span><span class="sxs-lookup"><span data-stu-id="e3662-132">Requirements</span></span>



| <span data-ttu-id="e3662-133">需求</span><span class="sxs-lookup"><span data-stu-id="e3662-133">Requirement</span></span> | <span data-ttu-id="e3662-134">值</span><span class="sxs-lookup"><span data-stu-id="e3662-134">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e3662-135">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e3662-135">Minimum supported client</span></span><br/> | <span data-ttu-id="e3662-136">都不支援</span><span class="sxs-lookup"><span data-stu-id="e3662-136">None supported</span></span><br/>                                                                       |
| <span data-ttu-id="e3662-137">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e3662-137">Minimum supported server</span></span><br/> | <span data-ttu-id="e3662-138">都不支援</span><span class="sxs-lookup"><span data-stu-id="e3662-138">None supported</span></span><br/>                                                                       |
| <span data-ttu-id="e3662-139">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="e3662-139">End of client support</span></span><br/>    | <span data-ttu-id="e3662-140">都不支援</span><span class="sxs-lookup"><span data-stu-id="e3662-140">None supported</span></span><br/>                                                                       |
| <span data-ttu-id="e3662-141">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="e3662-141">End of server support</span></span><br/>    | <span data-ttu-id="e3662-142">都不支援</span><span class="sxs-lookup"><span data-stu-id="e3662-142">None supported</span></span><br/>                                                                       |
| <span data-ttu-id="e3662-143">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="e3662-143">Type library</span></span><br/>             | <dl> <span data-ttu-id="e3662-144"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e3662-144"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="e3662-145">DLL</span><span class="sxs-lookup"><span data-stu-id="e3662-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e3662-146"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e3662-146"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="e3662-147">IID</span><span class="sxs-lookup"><span data-stu-id="e3662-147">IID</span></span><br/>                      | <span data-ttu-id="e3662-148">IID \_ IMsRdpClientAdvancedSettings 定義為3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span><span class="sxs-lookup"><span data-stu-id="e3662-148">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e3662-149">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e3662-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e3662-150">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="e3662-150">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="e3662-151">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="e3662-151">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="e3662-152">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="e3662-152">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="e3662-153">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="e3662-153">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="e3662-154">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="e3662-154">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="e3662-155">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="e3662-155">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="e3662-156">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="e3662-156">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="e3662-157">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="e3662-157">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





