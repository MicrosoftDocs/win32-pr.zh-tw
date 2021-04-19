---
title: IMsRdpClientAdvancedSettings2 EnableAutoReconnect 屬性
description: 指定當網路連線中斷時，是否要讓用戶端控制項自動重新連線到會話。
ms.assetid: 9d820f78-bf7f-479a-ae6f-be0f0abe549c
ms.tgt_platform: multiple
keywords:
- EnableAutoReconnect 屬性遠端桌面服務
- EnableAutoReconnect 屬性遠端桌面服務，IMsRdpClientAdvancedSettings2 介面
- IMsRdpClientAdvancedSettings2 介面遠端桌面服務，EnableAutoReconnect 屬性
- EnableAutoReconnect 屬性遠端桌面服務，IMsRdpClientAdvancedSettings3 介面
- IMsRdpClientAdvancedSettings3 介面遠端桌面服務，EnableAutoReconnect 屬性
- EnableAutoReconnect 屬性遠端桌面服務，IMsRdpClientAdvancedSettings4 介面
- IMsRdpClientAdvancedSettings4 介面遠端桌面服務，EnableAutoReconnect 屬性
- EnableAutoReconnect 屬性遠端桌面服務，IMsRdpClientAdvancedSettings5 介面
- IMsRdpClientAdvancedSettings5 介面遠端桌面服務，EnableAutoReconnect 屬性
- EnableAutoReconnect 屬性遠端桌面服務，IMsRdpClientAdvancedSettings6 介面
- IMsRdpClientAdvancedSettings6 介面遠端桌面服務，EnableAutoReconnect 屬性
- EnableAutoReconnect 屬性遠端桌面服務，IMsRdpClientAdvancedSettings7 介面
- IMsRdpClientAdvancedSettings7 介面遠端桌面服務，EnableAutoReconnect 屬性
- EnableAutoReconnect 屬性遠端桌面服務，IMsRdpClientAdvancedSettings8 介面
- IMsRdpClientAdvancedSettings8 介面遠端桌面服務，EnableAutoReconnect 屬性
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings2.EnableAutoReconnect
- IMsRdpClientAdvancedSettings2.get_EnableAutoReconnect
- IMsRdpClientAdvancedSettings2.put_EnableAutoReconnect
- IMsRdpClientAdvancedSettings3.EnableAutoReconnect
- IMsRdpClientAdvancedSettings3.get_EnableAutoReconnect
- IMsRdpClientAdvancedSettings3.put_EnableAutoReconnect
- IMsRdpClientAdvancedSettings4.EnableAutoReconnect
- IMsRdpClientAdvancedSettings4.get_EnableAutoReconnect
- IMsRdpClientAdvancedSettings4.put_EnableAutoReconnect
- IMsRdpClientAdvancedSettings5.EnableAutoReconnect
- IMsRdpClientAdvancedSettings5.get_EnableAutoReconnect
- IMsRdpClientAdvancedSettings5.put_EnableAutoReconnect
- IMsRdpClientAdvancedSettings6.EnableAutoReconnect
- IMsRdpClientAdvancedSettings6.get_EnableAutoReconnect
- IMsRdpClientAdvancedSettings6.put_EnableAutoReconnect
- IMsRdpClientAdvancedSettings7.EnableAutoReconnect
- IMsRdpClientAdvancedSettings7.get_EnableAutoReconnect
- IMsRdpClientAdvancedSettings7.put_EnableAutoReconnect
- IMsRdpClientAdvancedSettings8.EnableAutoReconnect
- IMsRdpClientAdvancedSettings8.get_EnableAutoReconnect
- IMsRdpClientAdvancedSettings8.put_EnableAutoReconnect
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f8d4a1345395b5b5843872df256fe7a113094e1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106996582"
---
# <a name="imsrdpclientadvancedsettings2enableautoreconnect-property"></a><span data-ttu-id="8c6ce-118">IMsRdpClientAdvancedSettings2：： EnableAutoReconnect 屬性</span><span class="sxs-lookup"><span data-stu-id="8c6ce-118">IMsRdpClientAdvancedSettings2::EnableAutoReconnect property</span></span>

<span data-ttu-id="8c6ce-119">指定當網路連線中斷時，是否要讓用戶端控制項自動重新連線到會話。</span><span class="sxs-lookup"><span data-stu-id="8c6ce-119">Specifies whether to enable the client control to reconnect automatically to a session in the event of a network disconnection.</span></span>

<span data-ttu-id="8c6ce-120">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="8c6ce-120">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="8c6ce-121">Syntax</span><span class="sxs-lookup"><span data-stu-id="8c6ce-121">Syntax</span></span>


```C++
HRESULT put_EnableAutoReconnect(
  [in]  VARIANT_BOOL fEnableAutoReconnect
);

HRESULT get_EnableAutoReconnect(
  [out] VARIANT_BOOL *pfEnableAutoReconnect
);
```



## <a name="property-value"></a><span data-ttu-id="8c6ce-122">屬性值</span><span class="sxs-lookup"><span data-stu-id="8c6ce-122">Property value</span></span>

<span data-ttu-id="8c6ce-123">設定為 **variant \_ TRUE** 可啟用自動重新連線，並將變數設為 **\_ FALSE** 以停用。</span><span class="sxs-lookup"><span data-stu-id="8c6ce-123">Set to **VARIANT\_TRUE** to enable automatic reconnection, and to **VARIANT\_FALSE** to disable it.</span></span> <span data-ttu-id="8c6ce-124">預設值為 **VARIANT \_ TRUE**。</span><span class="sxs-lookup"><span data-stu-id="8c6ce-124">The default is **VARIANT\_TRUE**.</span></span>

## <a name="error-codes"></a><span data-ttu-id="8c6ce-125">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="8c6ce-125">Error codes</span></span>

<span data-ttu-id="8c6ce-126">如果成功，則傳回 **S \_ OK** 。</span><span class="sxs-lookup"><span data-stu-id="8c6ce-126">Return **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="8c6ce-127">備註</span><span class="sxs-lookup"><span data-stu-id="8c6ce-127">Remarks</span></span>

<span data-ttu-id="8c6ce-128">連接控制項時，無法設定這個屬性。</span><span class="sxs-lookup"><span data-stu-id="8c6ce-128">This property cannot be set when the control is connected.</span></span>

<span data-ttu-id="8c6ce-129">如需遠端桌面網頁連線的詳細資訊，請參閱 [遠端桌面網頁連線的需求](requirements-for-remote-desktop-web-connection.md)。</span><span class="sxs-lookup"><span data-stu-id="8c6ce-129">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="8c6ce-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="8c6ce-130">Requirements</span></span>



| <span data-ttu-id="8c6ce-131">需求</span><span class="sxs-lookup"><span data-stu-id="8c6ce-131">Requirement</span></span> | <span data-ttu-id="8c6ce-132">值</span><span class="sxs-lookup"><span data-stu-id="8c6ce-132">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8c6ce-133">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8c6ce-133">Minimum supported client</span></span><br/> | <span data-ttu-id="8c6ce-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8c6ce-134">Windows Vista</span></span><br/>                                                                         |
| <span data-ttu-id="8c6ce-135">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8c6ce-135">Minimum supported server</span></span><br/> | <span data-ttu-id="8c6ce-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8c6ce-136">Windows Server 2008</span></span><br/>                                                                   |
| <span data-ttu-id="8c6ce-137">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="8c6ce-137">Type library</span></span><br/>             | <dl> <span data-ttu-id="8c6ce-138"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8c6ce-138"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="8c6ce-139">DLL</span><span class="sxs-lookup"><span data-stu-id="8c6ce-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8c6ce-140"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8c6ce-140"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="8c6ce-141">IID</span><span class="sxs-lookup"><span data-stu-id="8c6ce-141">IID</span></span><br/>                      | <span data-ttu-id="8c6ce-142">IID \_ IMsRdpClientAdvancedSettings2 定義為9ac42117-2b76-4320-aa44-0e616ab8437b</span><span class="sxs-lookup"><span data-stu-id="8c6ce-142">IID\_IMsRdpClientAdvancedSettings2 is defined as 9ac42117-2b76-4320-aa44-0e616ab8437b</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="8c6ce-143">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8c6ce-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8c6ce-144">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="8c6ce-144">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="8c6ce-145">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="8c6ce-145">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="8c6ce-146">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="8c6ce-146">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="8c6ce-147">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="8c6ce-147">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="8c6ce-148">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="8c6ce-148">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="8c6ce-149">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="8c6ce-149">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="8c6ce-150">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="8c6ce-150">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> </dl>

 

 





