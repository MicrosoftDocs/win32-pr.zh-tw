---
title: IMsRdpClientAdvancedSettings singleConnectionTimeout 屬性
description: 指定用戶端控制項等候 IP 位址連線的最大時間長度（以秒為單位）。
ms.assetid: 57fb2397-8229-4446-88fd-e75cb96c7ac5
ms.tgt_platform: multiple
keywords:
- singleConnectionTimeout 屬性遠端桌面服務
- singleConnectionTimeout 屬性遠端桌面服務，IMsRdpClientAdvancedSettings 介面
- IMsRdpClientAdvancedSettings 介面遠端桌面服務，singleConnectionTimeout 屬性
- singleConnectionTimeout 屬性遠端桌面服務，IMsRdpClientAdvancedSettings2 介面
- IMsRdpClientAdvancedSettings2 介面遠端桌面服務，singleConnectionTimeout 屬性
- singleConnectionTimeout 屬性遠端桌面服務，IMsRdpClientAdvancedSettings3 介面
- IMsRdpClientAdvancedSettings3 介面遠端桌面服務，singleConnectionTimeout 屬性
- singleConnectionTimeout 屬性遠端桌面服務，IMsRdpClientAdvancedSettings4 介面
- IMsRdpClientAdvancedSettings4 介面遠端桌面服務，singleConnectionTimeout 屬性
- singleConnectionTimeout 屬性遠端桌面服務，IMsRdpClientAdvancedSettings5 介面
- IMsRdpClientAdvancedSettings5 介面遠端桌面服務，singleConnectionTimeout 屬性
- singleConnectionTimeout 屬性遠端桌面服務，IMsRdpClientAdvancedSettings6 介面
- IMsRdpClientAdvancedSettings6 介面遠端桌面服務，singleConnectionTimeout 屬性
- singleConnectionTimeout 屬性遠端桌面服務，IMsRdpClientAdvancedSettings7 介面
- IMsRdpClientAdvancedSettings7 介面遠端桌面服務，singleConnectionTimeout 屬性
- singleConnectionTimeout 屬性遠端桌面服務，IMsRdpClientAdvancedSettings8 介面
- IMsRdpClientAdvancedSettings8 介面遠端桌面服務，singleConnectionTimeout 屬性
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.singleConnectionTimeout
- IMsRdpClientAdvancedSettings.get_singleConnectionTimeout
- IMsRdpClientAdvancedSettings.put_singleConnectionTimeout
- IMsRdpClientAdvancedSettings2.singleConnectionTimeout
- IMsRdpClientAdvancedSettings2.get_singleConnectionTimeout
- IMsRdpClientAdvancedSettings2.put_singleConnectionTimeout
- IMsRdpClientAdvancedSettings3.singleConnectionTimeout
- IMsRdpClientAdvancedSettings3.get_singleConnectionTimeout
- IMsRdpClientAdvancedSettings3.put_singleConnectionTimeout
- IMsRdpClientAdvancedSettings4.singleConnectionTimeout
- IMsRdpClientAdvancedSettings4.get_singleConnectionTimeout
- IMsRdpClientAdvancedSettings4.put_singleConnectionTimeout
- IMsRdpClientAdvancedSettings5.singleConnectionTimeout
- IMsRdpClientAdvancedSettings5.get_singleConnectionTimeout
- IMsRdpClientAdvancedSettings5.put_singleConnectionTimeout
- IMsRdpClientAdvancedSettings6.singleConnectionTimeout
- IMsRdpClientAdvancedSettings6.get_singleConnectionTimeout
- IMsRdpClientAdvancedSettings6.put_singleConnectionTimeout
- IMsRdpClientAdvancedSettings7.singleConnectionTimeout
- IMsRdpClientAdvancedSettings7.get_singleConnectionTimeout
- IMsRdpClientAdvancedSettings7.put_singleConnectionTimeout
- IMsRdpClientAdvancedSettings8.singleConnectionTimeout
- IMsRdpClientAdvancedSettings8.get_singleConnectionTimeout
- IMsRdpClientAdvancedSettings8.put_singleConnectionTimeout
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55a0d2eb34235c874b4408e5e4c6f0a349a1ab93
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104383893"
---
# <a name="imsrdpclientadvancedsettingssingleconnectiontimeout-property"></a><span data-ttu-id="eb8eb-120">IMsRdpClientAdvancedSettings：： singleConnectionTimeout 屬性</span><span class="sxs-lookup"><span data-stu-id="eb8eb-120">IMsRdpClientAdvancedSettings::singleConnectionTimeout property</span></span>

<span data-ttu-id="eb8eb-121">指定用戶端控制項等候 IP 位址連線的最大時間長度（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="eb8eb-121">Specifies the maximum length of time, in seconds, that the client control waits for a connection to an IP address.</span></span>

<span data-ttu-id="eb8eb-122">在連接期間，控制項可能會嘗試連接至多個 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="eb8eb-122">During connection, the control may attempt to connect to multiple IP addresses.</span></span>

<span data-ttu-id="eb8eb-123">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="eb8eb-123">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="eb8eb-124">Syntax</span><span class="sxs-lookup"><span data-stu-id="eb8eb-124">Syntax</span></span>


```C++
HRESULT put_singleConnectionTimeout(
  [in]  LONG singleConnectionTimeout
);

HRESULT get_singleConnectionTimeout(
  [out] LONG *psingleConnectionTimeout
);
```



## <a name="property-value"></a><span data-ttu-id="eb8eb-125">屬性值</span><span class="sxs-lookup"><span data-stu-id="eb8eb-125">Property value</span></span>

<span data-ttu-id="eb8eb-126">新的時間（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="eb8eb-126">The new time, in seconds.</span></span> <span data-ttu-id="eb8eb-127">最大值為600。</span><span class="sxs-lookup"><span data-stu-id="eb8eb-127">The maximum value is 600.</span></span>

## <a name="error-codes"></a><span data-ttu-id="eb8eb-128">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="eb8eb-128">Error codes</span></span>

<span data-ttu-id="eb8eb-129">如果成功，則傳回 **S \_ OK** 。</span><span class="sxs-lookup"><span data-stu-id="eb8eb-129">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="eb8eb-130">備註</span><span class="sxs-lookup"><span data-stu-id="eb8eb-130">Remarks</span></span>

<span data-ttu-id="eb8eb-131">如需遠端桌面網頁連線的詳細資訊，請參閱 [遠端桌面網頁連線的需求](requirements-for-remote-desktop-web-connection.md)。</span><span class="sxs-lookup"><span data-stu-id="eb8eb-131">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="eb8eb-132">規格需求</span><span class="sxs-lookup"><span data-stu-id="eb8eb-132">Requirements</span></span>



| <span data-ttu-id="eb8eb-133">需求</span><span class="sxs-lookup"><span data-stu-id="eb8eb-133">Requirement</span></span> | <span data-ttu-id="eb8eb-134">值</span><span class="sxs-lookup"><span data-stu-id="eb8eb-134">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eb8eb-135">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="eb8eb-135">Minimum supported client</span></span><br/> | <span data-ttu-id="eb8eb-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="eb8eb-136">Windows Vista</span></span><br/>                                                                        |
| <span data-ttu-id="eb8eb-137">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="eb8eb-137">Minimum supported server</span></span><br/> | <span data-ttu-id="eb8eb-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="eb8eb-138">Windows Server 2008</span></span><br/>                                                                  |
| <span data-ttu-id="eb8eb-139">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="eb8eb-139">Type library</span></span><br/>             | <dl> <span data-ttu-id="eb8eb-140"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="eb8eb-140"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="eb8eb-141">DLL</span><span class="sxs-lookup"><span data-stu-id="eb8eb-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="eb8eb-142"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="eb8eb-142"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="eb8eb-143">IID</span><span class="sxs-lookup"><span data-stu-id="eb8eb-143">IID</span></span><br/>                      | <span data-ttu-id="eb8eb-144">IID \_ IMsRdpClientAdvancedSettings 定義為3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span><span class="sxs-lookup"><span data-stu-id="eb8eb-144">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="eb8eb-145">另請參閱</span><span class="sxs-lookup"><span data-stu-id="eb8eb-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eb8eb-146">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="eb8eb-146">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="eb8eb-147">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="eb8eb-147">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="eb8eb-148">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="eb8eb-148">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="eb8eb-149">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="eb8eb-149">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="eb8eb-150">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="eb8eb-150">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="eb8eb-151">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="eb8eb-151">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="eb8eb-152">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="eb8eb-152">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="eb8eb-153">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="eb8eb-153">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="eb8eb-154">**overallConnectionTimeout**</span><span class="sxs-lookup"><span data-stu-id="eb8eb-154">**overallConnectionTimeout**</span></span>](imsrdpclientadvancedsettings-overallconnectiontimeout.md)
</dt> </dl>

 

 





