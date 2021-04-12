---
title: IMsRdpClientAdvancedSettings minInputSendInterval 屬性
description: 指定傳送滑鼠事件的最小間隔（以毫秒為單位）。
ms.assetid: d186c05f-0b45-47bd-8a8e-e1f9baf2bd75
ms.tgt_platform: multiple
keywords:
- minInputSendInterval 屬性遠端桌面服務
- minInputSendInterval 屬性遠端桌面服務，IMsRdpClientAdvancedSettings 介面
- IMsRdpClientAdvancedSettings 介面遠端桌面服務，minInputSendInterval 屬性
- minInputSendInterval 屬性遠端桌面服務，IMsRdpClientAdvancedSettings2 介面
- IMsRdpClientAdvancedSettings2 介面遠端桌面服務，minInputSendInterval 屬性
- minInputSendInterval 屬性遠端桌面服務，IMsRdpClientAdvancedSettings3 介面
- IMsRdpClientAdvancedSettings3 介面遠端桌面服務，minInputSendInterval 屬性
- minInputSendInterval 屬性遠端桌面服務，IMsRdpClientAdvancedSettings4 介面
- IMsRdpClientAdvancedSettings4 介面遠端桌面服務，minInputSendInterval 屬性
- minInputSendInterval 屬性遠端桌面服務，IMsRdpClientAdvancedSettings5 介面
- IMsRdpClientAdvancedSettings5 介面遠端桌面服務，minInputSendInterval 屬性
- minInputSendInterval 屬性遠端桌面服務，IMsRdpClientAdvancedSettings6 介面
- IMsRdpClientAdvancedSettings6 介面遠端桌面服務，minInputSendInterval 屬性
- minInputSendInterval 屬性遠端桌面服務，IMsRdpClientAdvancedSettings7 介面
- IMsRdpClientAdvancedSettings7 介面遠端桌面服務，minInputSendInterval 屬性
- minInputSendInterval 屬性遠端桌面服務，IMsRdpClientAdvancedSettings8 介面
- IMsRdpClientAdvancedSettings8 介面遠端桌面服務，minInputSendInterval 屬性
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.minInputSendInterval
- IMsRdpClientAdvancedSettings.get_minInputSendInterval
- IMsRdpClientAdvancedSettings.put_minInputSendInterval
- IMsRdpClientAdvancedSettings2.minInputSendInterval
- IMsRdpClientAdvancedSettings2.get_minInputSendInterval
- IMsRdpClientAdvancedSettings2.put_minInputSendInterval
- IMsRdpClientAdvancedSettings3.minInputSendInterval
- IMsRdpClientAdvancedSettings3.get_minInputSendInterval
- IMsRdpClientAdvancedSettings3.put_minInputSendInterval
- IMsRdpClientAdvancedSettings4.minInputSendInterval
- IMsRdpClientAdvancedSettings4.get_minInputSendInterval
- IMsRdpClientAdvancedSettings4.put_minInputSendInterval
- IMsRdpClientAdvancedSettings5.minInputSendInterval
- IMsRdpClientAdvancedSettings5.get_minInputSendInterval
- IMsRdpClientAdvancedSettings5.put_minInputSendInterval
- IMsRdpClientAdvancedSettings6.minInputSendInterval
- IMsRdpClientAdvancedSettings6.get_minInputSendInterval
- IMsRdpClientAdvancedSettings6.put_minInputSendInterval
- IMsRdpClientAdvancedSettings7.minInputSendInterval
- IMsRdpClientAdvancedSettings7.get_minInputSendInterval
- IMsRdpClientAdvancedSettings7.put_minInputSendInterval
- IMsRdpClientAdvancedSettings8.minInputSendInterval
- IMsRdpClientAdvancedSettings8.get_minInputSendInterval
- IMsRdpClientAdvancedSettings8.put_minInputSendInterval
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56070e2ba395c4b89dc9caa9e6e5181bb03d81ae
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384306"
---
# <a name="imsrdpclientadvancedsettingsmininputsendinterval-property"></a><span data-ttu-id="0f3b6-120">IMsRdpClientAdvancedSettings：： minInputSendInterval 屬性</span><span class="sxs-lookup"><span data-stu-id="0f3b6-120">IMsRdpClientAdvancedSettings::minInputSendInterval property</span></span>

<span data-ttu-id="0f3b6-121">指定傳送滑鼠事件的最小間隔（以毫秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="0f3b6-121">Specifies the minimum interval, in milliseconds, between the sending of mouse events.</span></span>

<span data-ttu-id="0f3b6-122">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="0f3b6-122">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="0f3b6-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="0f3b6-123">Syntax</span></span>


```C++
HRESULT put_minInputSendInterval(
  [in]  LONG minInputSendInterval
);

HRESULT get_minInputSendInterval(
  [out] LONG *pminInputSendInterval
);
```



## <a name="property-value"></a><span data-ttu-id="0f3b6-124">屬性值</span><span class="sxs-lookup"><span data-stu-id="0f3b6-124">Property value</span></span>

<span data-ttu-id="0f3b6-125">新的間隔（以毫秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="0f3b6-125">The new interval, in milliseconds.</span></span> <span data-ttu-id="0f3b6-126">預設值是 100。</span><span class="sxs-lookup"><span data-stu-id="0f3b6-126">The default value is 100.</span></span>

## <a name="error-codes"></a><span data-ttu-id="0f3b6-127">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="0f3b6-127">Error codes</span></span>

<span data-ttu-id="0f3b6-128">如果成功，則傳回 **S \_ OK** 。</span><span class="sxs-lookup"><span data-stu-id="0f3b6-128">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="0f3b6-129">備註</span><span class="sxs-lookup"><span data-stu-id="0f3b6-129">Remarks</span></span>

<span data-ttu-id="0f3b6-130">如需遠端桌面網頁連線的詳細資訊，請參閱 [遠端桌面網頁連線的需求](requirements-for-remote-desktop-web-connection.md)。</span><span class="sxs-lookup"><span data-stu-id="0f3b6-130">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="0f3b6-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="0f3b6-131">Requirements</span></span>



| <span data-ttu-id="0f3b6-132">需求</span><span class="sxs-lookup"><span data-stu-id="0f3b6-132">Requirement</span></span> | <span data-ttu-id="0f3b6-133">值</span><span class="sxs-lookup"><span data-stu-id="0f3b6-133">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0f3b6-134">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0f3b6-134">Minimum supported client</span></span><br/> | <span data-ttu-id="0f3b6-135">Windows 7</span><span class="sxs-lookup"><span data-stu-id="0f3b6-135">Windows 7</span></span><br/>                                                                            |
| <span data-ttu-id="0f3b6-136">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0f3b6-136">Minimum supported server</span></span><br/> | <span data-ttu-id="0f3b6-137">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="0f3b6-137">Windows Server 2008 R2</span></span><br/>                                                               |
| <span data-ttu-id="0f3b6-138">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="0f3b6-138">Type library</span></span><br/>             | <dl> <span data-ttu-id="0f3b6-139"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0f3b6-139"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="0f3b6-140">DLL</span><span class="sxs-lookup"><span data-stu-id="0f3b6-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0f3b6-141"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0f3b6-141"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="0f3b6-142">IID</span><span class="sxs-lookup"><span data-stu-id="0f3b6-142">IID</span></span><br/>                      | <span data-ttu-id="0f3b6-143">IID \_ IMsRdpClientAdvancedSettings 定義為3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span><span class="sxs-lookup"><span data-stu-id="0f3b6-143">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="0f3b6-144">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0f3b6-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0f3b6-145">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="0f3b6-145">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="0f3b6-146">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="0f3b6-146">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="0f3b6-147">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="0f3b6-147">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="0f3b6-148">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="0f3b6-148">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="0f3b6-149">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="0f3b6-149">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="0f3b6-150">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="0f3b6-150">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="0f3b6-151">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="0f3b6-151">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="0f3b6-152">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="0f3b6-152">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





