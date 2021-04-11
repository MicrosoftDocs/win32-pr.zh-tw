---
title: IMsRdpClientAdvancedSettings shutdownTimeout 屬性
description: 指定等待伺服器回應中斷連接要求的時間長度（以秒為單位）。
ms.assetid: 3fa935dc-d4b0-433b-ab67-a644fcf09006
ms.tgt_platform: multiple
keywords:
- shutdownTimeout 屬性遠端桌面服務
- shutdownTimeout 屬性遠端桌面服務，IMsRdpClientAdvancedSettings 介面
- IMsRdpClientAdvancedSettings 介面遠端桌面服務，shutdownTimeout 屬性
- shutdownTimeout 屬性遠端桌面服務，IMsRdpClientAdvancedSettings2 介面
- IMsRdpClientAdvancedSettings2 介面遠端桌面服務，shutdownTimeout 屬性
- shutdownTimeout 屬性遠端桌面服務，IMsRdpClientAdvancedSettings3 介面
- IMsRdpClientAdvancedSettings3 介面遠端桌面服務，shutdownTimeout 屬性
- shutdownTimeout 屬性遠端桌面服務，IMsRdpClientAdvancedSettings4 介面
- IMsRdpClientAdvancedSettings4 介面遠端桌面服務，shutdownTimeout 屬性
- shutdownTimeout 屬性遠端桌面服務，IMsRdpClientAdvancedSettings5 介面
- IMsRdpClientAdvancedSettings5 介面遠端桌面服務，shutdownTimeout 屬性
- shutdownTimeout 屬性遠端桌面服務，IMsRdpClientAdvancedSettings6 介面
- IMsRdpClientAdvancedSettings6 介面遠端桌面服務，shutdownTimeout 屬性
- shutdownTimeout 屬性遠端桌面服務，IMsRdpClientAdvancedSettings7 介面
- IMsRdpClientAdvancedSettings7 介面遠端桌面服務，shutdownTimeout 屬性
- shutdownTimeout 屬性遠端桌面服務，IMsRdpClientAdvancedSettings8 介面
- IMsRdpClientAdvancedSettings8 介面遠端桌面服務，shutdownTimeout 屬性
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.shutdownTimeout
- IMsRdpClientAdvancedSettings.get_shutdownTimeout
- IMsRdpClientAdvancedSettings.put_shutdownTimeout
- IMsRdpClientAdvancedSettings2.shutdownTimeout
- IMsRdpClientAdvancedSettings2.get_shutdownTimeout
- IMsRdpClientAdvancedSettings2.put_shutdownTimeout
- IMsRdpClientAdvancedSettings3.shutdownTimeout
- IMsRdpClientAdvancedSettings3.get_shutdownTimeout
- IMsRdpClientAdvancedSettings3.put_shutdownTimeout
- IMsRdpClientAdvancedSettings4.shutdownTimeout
- IMsRdpClientAdvancedSettings4.get_shutdownTimeout
- IMsRdpClientAdvancedSettings4.put_shutdownTimeout
- IMsRdpClientAdvancedSettings5.shutdownTimeout
- IMsRdpClientAdvancedSettings5.get_shutdownTimeout
- IMsRdpClientAdvancedSettings5.put_shutdownTimeout
- IMsRdpClientAdvancedSettings6.shutdownTimeout
- IMsRdpClientAdvancedSettings6.get_shutdownTimeout
- IMsRdpClientAdvancedSettings6.put_shutdownTimeout
- IMsRdpClientAdvancedSettings7.shutdownTimeout
- IMsRdpClientAdvancedSettings7.get_shutdownTimeout
- IMsRdpClientAdvancedSettings7.put_shutdownTimeout
- IMsRdpClientAdvancedSettings8.shutdownTimeout
- IMsRdpClientAdvancedSettings8.get_shutdownTimeout
- IMsRdpClientAdvancedSettings8.put_shutdownTimeout
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 868a011a0ce484f5bb2dd7d1ec610f4e3a436898
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104383894"
---
# <a name="imsrdpclientadvancedsettingsshutdowntimeout-property"></a><span data-ttu-id="f7de0-120">IMsRdpClientAdvancedSettings：： shutdownTimeout 屬性</span><span class="sxs-lookup"><span data-stu-id="f7de0-120">IMsRdpClientAdvancedSettings::shutdownTimeout property</span></span>

<span data-ttu-id="f7de0-121">指定等待伺服器回應中斷連接要求的時間長度（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="f7de0-121">Specifies the length of time, in seconds, to wait for the server to respond to a disconnection request.</span></span>

<span data-ttu-id="f7de0-122">如果伺服器未在指定的時間內回復，用戶端控制項就會中斷連線。</span><span class="sxs-lookup"><span data-stu-id="f7de0-122">If the server does not reply within the specified time, the client control disconnects.</span></span>

<span data-ttu-id="f7de0-123">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="f7de0-123">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="f7de0-124">Syntax</span><span class="sxs-lookup"><span data-stu-id="f7de0-124">Syntax</span></span>


```C++
HRESULT put_shutdownTimeout(
  [in]  LONG shutdownTimeout
);

HRESULT get_shutdownTimeout(
  [out] LONG *pshutdownTimeout
);
```



## <a name="property-value"></a><span data-ttu-id="f7de0-125">屬性值</span><span class="sxs-lookup"><span data-stu-id="f7de0-125">Property value</span></span>

<span data-ttu-id="f7de0-126">新的時間（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="f7de0-126">The new time, in seconds.</span></span> <span data-ttu-id="f7de0-127">屬性的預設值為10。</span><span class="sxs-lookup"><span data-stu-id="f7de0-127">The default value of the property is 10.</span></span> <span data-ttu-id="f7de0-128">最大值為600，代表10分鐘。</span><span class="sxs-lookup"><span data-stu-id="f7de0-128">The maximum value is 600, which represents 10 minutes.</span></span>

## <a name="error-codes"></a><span data-ttu-id="f7de0-129">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="f7de0-129">Error codes</span></span>

<span data-ttu-id="f7de0-130">如果成功，則傳回 **S \_ OK** 。</span><span class="sxs-lookup"><span data-stu-id="f7de0-130">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="f7de0-131">備註</span><span class="sxs-lookup"><span data-stu-id="f7de0-131">Remarks</span></span>

<span data-ttu-id="f7de0-132">如需遠端桌面網頁連線的詳細資訊，請參閱 [遠端桌面網頁連線的需求](requirements-for-remote-desktop-web-connection.md)。</span><span class="sxs-lookup"><span data-stu-id="f7de0-132">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f7de0-133">規格需求</span><span class="sxs-lookup"><span data-stu-id="f7de0-133">Requirements</span></span>



| <span data-ttu-id="f7de0-134">需求</span><span class="sxs-lookup"><span data-stu-id="f7de0-134">Requirement</span></span> | <span data-ttu-id="f7de0-135">值</span><span class="sxs-lookup"><span data-stu-id="f7de0-135">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f7de0-136">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f7de0-136">Minimum supported client</span></span><br/> | <span data-ttu-id="f7de0-137">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f7de0-137">Windows Vista</span></span><br/>                                                                        |
| <span data-ttu-id="f7de0-138">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f7de0-138">Minimum supported server</span></span><br/> | <span data-ttu-id="f7de0-139">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f7de0-139">Windows Server 2008</span></span><br/>                                                                  |
| <span data-ttu-id="f7de0-140">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="f7de0-140">Type library</span></span><br/>             | <dl> <span data-ttu-id="f7de0-141"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f7de0-141"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="f7de0-142">DLL</span><span class="sxs-lookup"><span data-stu-id="f7de0-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f7de0-143"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f7de0-143"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="f7de0-144">IID</span><span class="sxs-lookup"><span data-stu-id="f7de0-144">IID</span></span><br/>                      | <span data-ttu-id="f7de0-145">IID \_ IMsRdpClientAdvancedSettings 定義為3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span><span class="sxs-lookup"><span data-stu-id="f7de0-145">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f7de0-146">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f7de0-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f7de0-147">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="f7de0-147">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="f7de0-148">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="f7de0-148">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="f7de0-149">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="f7de0-149">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="f7de0-150">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="f7de0-150">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="f7de0-151">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="f7de0-151">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="f7de0-152">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="f7de0-152">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="f7de0-153">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="f7de0-153">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="f7de0-154">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="f7de0-154">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





