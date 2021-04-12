---
title: IMsRdpClientAdvancedSettings keepAliveInterval 屬性
description: 指定用戶端將 keep-alive 訊息傳送至伺服器的間隔（以毫秒為單位）。
ms.assetid: 0d1b7d8f-f81c-4591-bb08-adab307e87fe
ms.tgt_platform: multiple
keywords:
- keepAliveInterval 屬性遠端桌面服務
- keepAliveInterval 屬性遠端桌面服務，IMsRdpClientAdvancedSettings 介面
- IMsRdpClientAdvancedSettings 介面遠端桌面服務，keepAliveInterval 屬性
- keepAliveInterval 屬性遠端桌面服務，IMsRdpClientAdvancedSettings2 介面
- IMsRdpClientAdvancedSettings2 介面遠端桌面服務，keepAliveInterval 屬性
- keepAliveInterval 屬性遠端桌面服務，IMsRdpClientAdvancedSettings3 介面
- IMsRdpClientAdvancedSettings3 介面遠端桌面服務，keepAliveInterval 屬性
- keepAliveInterval 屬性遠端桌面服務，IMsRdpClientAdvancedSettings4 介面
- IMsRdpClientAdvancedSettings4 介面遠端桌面服務，keepAliveInterval 屬性
- keepAliveInterval 屬性遠端桌面服務，IMsRdpClientAdvancedSettings5 介面
- IMsRdpClientAdvancedSettings5 介面遠端桌面服務，keepAliveInterval 屬性
- keepAliveInterval 屬性遠端桌面服務，IMsRdpClientAdvancedSettings6 介面
- IMsRdpClientAdvancedSettings6 介面遠端桌面服務，keepAliveInterval 屬性
- keepAliveInterval 屬性遠端桌面服務，IMsRdpClientAdvancedSettings7 介面
- IMsRdpClientAdvancedSettings7 介面遠端桌面服務，keepAliveInterval 屬性
- keepAliveInterval 屬性遠端桌面服務，IMsRdpClientAdvancedSettings8 介面
- IMsRdpClientAdvancedSettings8 介面遠端桌面服務，keepAliveInterval 屬性
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.keepAliveInterval
- IMsRdpClientAdvancedSettings.get_keepAliveInterval
- IMsRdpClientAdvancedSettings.put_keepAliveInterval
- IMsRdpClientAdvancedSettings2.keepAliveInterval
- IMsRdpClientAdvancedSettings2.get_keepAliveInterval
- IMsRdpClientAdvancedSettings2.put_keepAliveInterval
- IMsRdpClientAdvancedSettings3.keepAliveInterval
- IMsRdpClientAdvancedSettings3.get_keepAliveInterval
- IMsRdpClientAdvancedSettings3.put_keepAliveInterval
- IMsRdpClientAdvancedSettings4.keepAliveInterval
- IMsRdpClientAdvancedSettings4.get_keepAliveInterval
- IMsRdpClientAdvancedSettings4.put_keepAliveInterval
- IMsRdpClientAdvancedSettings5.keepAliveInterval
- IMsRdpClientAdvancedSettings5.get_keepAliveInterval
- IMsRdpClientAdvancedSettings5.put_keepAliveInterval
- IMsRdpClientAdvancedSettings6.keepAliveInterval
- IMsRdpClientAdvancedSettings6.get_keepAliveInterval
- IMsRdpClientAdvancedSettings6.put_keepAliveInterval
- IMsRdpClientAdvancedSettings7.keepAliveInterval
- IMsRdpClientAdvancedSettings7.get_keepAliveInterval
- IMsRdpClientAdvancedSettings7.put_keepAliveInterval
- IMsRdpClientAdvancedSettings8.keepAliveInterval
- IMsRdpClientAdvancedSettings8.get_keepAliveInterval
- IMsRdpClientAdvancedSettings8.put_keepAliveInterval
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d15412b5b1803aadcffa08a8617742e0c90b1a0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384310"
---
# <a name="imsrdpclientadvancedsettingskeepaliveinterval-property"></a><span data-ttu-id="016b0-120">IMsRdpClientAdvancedSettings：： keepAliveInterval 屬性</span><span class="sxs-lookup"><span data-stu-id="016b0-120">IMsRdpClientAdvancedSettings::keepAliveInterval property</span></span>

<span data-ttu-id="016b0-121">指定用戶端將 keep-alive 訊息傳送至伺服器的間隔（以毫秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="016b0-121">Specifies an interval, in milliseconds, at which the client sends keep-alive messages to the server.</span></span>

<span data-ttu-id="016b0-122">此群組原則設定會指定是否允許持續性用戶端連接到伺服器，以覆寫此屬性設定。</span><span class="sxs-lookup"><span data-stu-id="016b0-122">A group policy setting that specifies whether persistent client connections to the server are allowed can override this property setting.</span></span>

<span data-ttu-id="016b0-123">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="016b0-123">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="016b0-124">Syntax</span><span class="sxs-lookup"><span data-stu-id="016b0-124">Syntax</span></span>


```C++
HRESULT put_keepAliveInterval(
  [in]  LONG keepAliveInterval
);

HRESULT get_keepAliveInterval(
  [out] LONG *pkeepAliveInterval
);
```



## <a name="property-value"></a><span data-ttu-id="016b0-125">屬性值</span><span class="sxs-lookup"><span data-stu-id="016b0-125">Property value</span></span>

<span data-ttu-id="016b0-126">新的間隔（以毫秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="016b0-126">The new interval, in milliseconds.</span></span> <span data-ttu-id="016b0-127">屬性的預設值為零，它會停用 keep-alive 訊息。</span><span class="sxs-lookup"><span data-stu-id="016b0-127">The default value of the property is zero, which disables keep-alive messages.</span></span> <span data-ttu-id="016b0-128">這個屬性的最小有效值是10000，代表10秒。</span><span class="sxs-lookup"><span data-stu-id="016b0-128">The minimum valid value of this property is 10,000, which represents 10 seconds.</span></span>

## <a name="error-codes"></a><span data-ttu-id="016b0-129">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="016b0-129">Error codes</span></span>

<span data-ttu-id="016b0-130">如果成功，則傳回 **S \_ OK** 。</span><span class="sxs-lookup"><span data-stu-id="016b0-130">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="016b0-131">備註</span><span class="sxs-lookup"><span data-stu-id="016b0-131">Remarks</span></span>

<span data-ttu-id="016b0-132">如需遠端桌面網頁連線的詳細資訊，請參閱 [遠端桌面網頁連線的需求](requirements-for-remote-desktop-web-connection.md)。</span><span class="sxs-lookup"><span data-stu-id="016b0-132">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="016b0-133">規格需求</span><span class="sxs-lookup"><span data-stu-id="016b0-133">Requirements</span></span>



| <span data-ttu-id="016b0-134">需求</span><span class="sxs-lookup"><span data-stu-id="016b0-134">Requirement</span></span> | <span data-ttu-id="016b0-135">值</span><span class="sxs-lookup"><span data-stu-id="016b0-135">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="016b0-136">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="016b0-136">Minimum supported client</span></span><br/> | <span data-ttu-id="016b0-137">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="016b0-137">Windows Vista</span></span><br/>                                                                        |
| <span data-ttu-id="016b0-138">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="016b0-138">Minimum supported server</span></span><br/> | <span data-ttu-id="016b0-139">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="016b0-139">Windows Server 2008</span></span><br/>                                                                  |
| <span data-ttu-id="016b0-140">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="016b0-140">Type library</span></span><br/>             | <dl> <span data-ttu-id="016b0-141"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="016b0-141"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="016b0-142">DLL</span><span class="sxs-lookup"><span data-stu-id="016b0-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="016b0-143"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="016b0-143"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="016b0-144">IID</span><span class="sxs-lookup"><span data-stu-id="016b0-144">IID</span></span><br/>                      | <span data-ttu-id="016b0-145">IID \_ IMsRdpClientAdvancedSettings 定義為3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span><span class="sxs-lookup"><span data-stu-id="016b0-145">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="016b0-146">另請參閱</span><span class="sxs-lookup"><span data-stu-id="016b0-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="016b0-147">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="016b0-147">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="016b0-148">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="016b0-148">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="016b0-149">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="016b0-149">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="016b0-150">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="016b0-150">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="016b0-151">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="016b0-151">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="016b0-152">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="016b0-152">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="016b0-153">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="016b0-153">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="016b0-154">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="016b0-154">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





