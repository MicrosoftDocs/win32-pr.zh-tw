---
title: IMsRdpClientAdvancedSettings2 MaxReconnectAttempts 屬性
description: 指定在自動重新連接期間嘗試重新連接的次數。
ms.assetid: 24bfd3b6-d2de-4e46-8b5f-a4702c18a93c
ms.tgt_platform: multiple
keywords:
- MaxReconnectAttempts 屬性遠端桌面服務
- MaxReconnectAttempts 屬性遠端桌面服務，IMsRdpClientAdvancedSettings2 介面
- IMsRdpClientAdvancedSettings2 介面遠端桌面服務，MaxReconnectAttempts 屬性
- MaxReconnectAttempts 屬性遠端桌面服務，IMsRdpClientAdvancedSettings3 介面
- IMsRdpClientAdvancedSettings3 介面遠端桌面服務，MaxReconnectAttempts 屬性
- MaxReconnectAttempts 屬性遠端桌面服務，IMsRdpClientAdvancedSettings4 介面
- IMsRdpClientAdvancedSettings4 介面遠端桌面服務，MaxReconnectAttempts 屬性
- MaxReconnectAttempts 屬性遠端桌面服務，IMsRdpClientAdvancedSettings5 介面
- IMsRdpClientAdvancedSettings5 介面遠端桌面服務，MaxReconnectAttempts 屬性
- MaxReconnectAttempts 屬性遠端桌面服務，IMsRdpClientAdvancedSettings6 介面
- IMsRdpClientAdvancedSettings6 介面遠端桌面服務，MaxReconnectAttempts 屬性
- MaxReconnectAttempts 屬性遠端桌面服務，IMsRdpClientAdvancedSettings7 介面
- IMsRdpClientAdvancedSettings7 介面遠端桌面服務，MaxReconnectAttempts 屬性
- MaxReconnectAttempts 屬性遠端桌面服務，IMsRdpClientAdvancedSettings8 介面
- IMsRdpClientAdvancedSettings8 介面遠端桌面服務，MaxReconnectAttempts 屬性
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings2.MaxReconnectAttempts
- IMsRdpClientAdvancedSettings2.get_MaxReconnectAttempts
- IMsRdpClientAdvancedSettings2.put_MaxReconnectAttempts
- IMsRdpClientAdvancedSettings3.MaxReconnectAttempts
- IMsRdpClientAdvancedSettings3.get_MaxReconnectAttempts
- IMsRdpClientAdvancedSettings3.put_MaxReconnectAttempts
- IMsRdpClientAdvancedSettings4.MaxReconnectAttempts
- IMsRdpClientAdvancedSettings4.get_MaxReconnectAttempts
- IMsRdpClientAdvancedSettings4.put_MaxReconnectAttempts
- IMsRdpClientAdvancedSettings5.MaxReconnectAttempts
- IMsRdpClientAdvancedSettings5.get_MaxReconnectAttempts
- IMsRdpClientAdvancedSettings5.put_MaxReconnectAttempts
- IMsRdpClientAdvancedSettings6.MaxReconnectAttempts
- IMsRdpClientAdvancedSettings6.get_MaxReconnectAttempts
- IMsRdpClientAdvancedSettings6.put_MaxReconnectAttempts
- IMsRdpClientAdvancedSettings7.MaxReconnectAttempts
- IMsRdpClientAdvancedSettings7.get_MaxReconnectAttempts
- IMsRdpClientAdvancedSettings7.put_MaxReconnectAttempts
- IMsRdpClientAdvancedSettings8.MaxReconnectAttempts
- IMsRdpClientAdvancedSettings8.get_MaxReconnectAttempts
- IMsRdpClientAdvancedSettings8.put_MaxReconnectAttempts
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 322796a2d6ca6a13476dad58af8c385b8bdfa1fb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106965101"
---
# <a name="imsrdpclientadvancedsettings2maxreconnectattempts-property"></a><span data-ttu-id="ee390-118">IMsRdpClientAdvancedSettings2：： MaxReconnectAttempts 屬性</span><span class="sxs-lookup"><span data-stu-id="ee390-118">IMsRdpClientAdvancedSettings2::MaxReconnectAttempts property</span></span>

<span data-ttu-id="ee390-119">指定在自動重新連接期間嘗試重新連接的次數。</span><span class="sxs-lookup"><span data-stu-id="ee390-119">Specifies the number of times to try to reconnect during automatic reconnection.</span></span>

<span data-ttu-id="ee390-120">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="ee390-120">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="ee390-121">Syntax</span><span class="sxs-lookup"><span data-stu-id="ee390-121">Syntax</span></span>


```C++
HRESULT put_MaxReconnectAttempts(
  [in]  LONG MaxReconnectAttempts
);

HRESULT get_MaxReconnectAttempts(
  [out] LONG *pMaxReconnectAttempts
);
```



## <a name="property-value"></a><span data-ttu-id="ee390-122">屬性值</span><span class="sxs-lookup"><span data-stu-id="ee390-122">Property value</span></span>

<span data-ttu-id="ee390-123">新的重試次數。</span><span class="sxs-lookup"><span data-stu-id="ee390-123">The new number of retries.</span></span> <span data-ttu-id="ee390-124">有效的值為0到200（含）。</span><span class="sxs-lookup"><span data-stu-id="ee390-124">The valid values are 0 to 200, inclusive.</span></span>

## <a name="error-codes"></a><span data-ttu-id="ee390-125">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="ee390-125">Error codes</span></span>

<span data-ttu-id="ee390-126">如果成功，則傳回 **S \_ OK** 。</span><span class="sxs-lookup"><span data-stu-id="ee390-126">Return **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="ee390-127">備註</span><span class="sxs-lookup"><span data-stu-id="ee390-127">Remarks</span></span>

<span data-ttu-id="ee390-128">連接控制項時，無法設定這個屬性。</span><span class="sxs-lookup"><span data-stu-id="ee390-128">This property cannot be set when the control is connected.</span></span>

<span data-ttu-id="ee390-129">如需遠端桌面網頁連線的詳細資訊，請參閱 [遠端桌面網頁連線的需求](requirements-for-remote-desktop-web-connection.md)。</span><span class="sxs-lookup"><span data-stu-id="ee390-129">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ee390-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="ee390-130">Requirements</span></span>



| <span data-ttu-id="ee390-131">需求</span><span class="sxs-lookup"><span data-stu-id="ee390-131">Requirement</span></span> | <span data-ttu-id="ee390-132">值</span><span class="sxs-lookup"><span data-stu-id="ee390-132">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ee390-133">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ee390-133">Minimum supported client</span></span><br/> | <span data-ttu-id="ee390-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ee390-134">Windows Vista</span></span><br/>                                                                         |
| <span data-ttu-id="ee390-135">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ee390-135">Minimum supported server</span></span><br/> | <span data-ttu-id="ee390-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ee390-136">Windows Server 2008</span></span><br/>                                                                   |
| <span data-ttu-id="ee390-137">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="ee390-137">Type library</span></span><br/>             | <dl> <span data-ttu-id="ee390-138"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ee390-138"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="ee390-139">DLL</span><span class="sxs-lookup"><span data-stu-id="ee390-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ee390-140"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ee390-140"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="ee390-141">IID</span><span class="sxs-lookup"><span data-stu-id="ee390-141">IID</span></span><br/>                      | <span data-ttu-id="ee390-142">IID \_ IMsRdpClientAdvancedSettings2 定義為9ac42117-2b76-4320-aa44-0e616ab8437b</span><span class="sxs-lookup"><span data-stu-id="ee390-142">IID\_IMsRdpClientAdvancedSettings2 is defined as 9ac42117-2b76-4320-aa44-0e616ab8437b</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ee390-143">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ee390-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ee390-144">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="ee390-144">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="ee390-145">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="ee390-145">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="ee390-146">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="ee390-146">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="ee390-147">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="ee390-147">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="ee390-148">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="ee390-148">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="ee390-149">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="ee390-149">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="ee390-150">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="ee390-150">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> </dl>

 

 





