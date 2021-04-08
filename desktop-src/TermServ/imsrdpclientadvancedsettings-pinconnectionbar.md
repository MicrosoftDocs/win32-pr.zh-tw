---
title: IMsRdpClientAdvancedSettings PinConnectionBar 屬性
description: 指定 UI 連接列的狀態。
ms.assetid: b1f9cb02-3ee3-4574-a874-2584b0d5b47e
ms.tgt_platform: multiple
keywords:
- PinConnectionBar 屬性遠端桌面服務
- PinConnectionBar 屬性遠端桌面服務，IMsRdpClientAdvancedSettings 介面
- IMsRdpClientAdvancedSettings 介面遠端桌面服務，PinConnectionBar 屬性
- PinConnectionBar 屬性遠端桌面服務，IMsRdpClientAdvancedSettings2 介面
- IMsRdpClientAdvancedSettings2 介面遠端桌面服務，PinConnectionBar 屬性
- PinConnectionBar 屬性遠端桌面服務，IMsRdpClientAdvancedSettings3 介面
- IMsRdpClientAdvancedSettings3 介面遠端桌面服務，PinConnectionBar 屬性
- PinConnectionBar 屬性遠端桌面服務，IMsRdpClientAdvancedSettings4 介面
- IMsRdpClientAdvancedSettings4 介面遠端桌面服務，PinConnectionBar 屬性
- PinConnectionBar 屬性遠端桌面服務，IMsRdpClientAdvancedSettings5 介面
- IMsRdpClientAdvancedSettings5 介面遠端桌面服務，PinConnectionBar 屬性
- PinConnectionBar 屬性遠端桌面服務，IMsRdpClientAdvancedSettings6 介面
- IMsRdpClientAdvancedSettings6 介面遠端桌面服務，PinConnectionBar 屬性
- PinConnectionBar 屬性遠端桌面服務，IMsRdpClientAdvancedSettings7 介面
- IMsRdpClientAdvancedSettings7 介面遠端桌面服務，PinConnectionBar 屬性
- PinConnectionBar 屬性遠端桌面服務，IMsRdpClientAdvancedSettings8 介面
- IMsRdpClientAdvancedSettings8 介面遠端桌面服務，PinConnectionBar 屬性
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.PinConnectionBar
- IMsRdpClientAdvancedSettings.get_PinConnectionBar
- IMsRdpClientAdvancedSettings.put_PinConnectionBar
- IMsRdpClientAdvancedSettings2.PinConnectionBar
- IMsRdpClientAdvancedSettings2.get_PinConnectionBar
- IMsRdpClientAdvancedSettings2.put_PinConnectionBar
- IMsRdpClientAdvancedSettings3.PinConnectionBar
- IMsRdpClientAdvancedSettings3.get_PinConnectionBar
- IMsRdpClientAdvancedSettings3.put_PinConnectionBar
- IMsRdpClientAdvancedSettings4.PinConnectionBar
- IMsRdpClientAdvancedSettings4.get_PinConnectionBar
- IMsRdpClientAdvancedSettings4.put_PinConnectionBar
- IMsRdpClientAdvancedSettings5.PinConnectionBar
- IMsRdpClientAdvancedSettings5.get_PinConnectionBar
- IMsRdpClientAdvancedSettings5.put_PinConnectionBar
- IMsRdpClientAdvancedSettings6.PinConnectionBar
- IMsRdpClientAdvancedSettings6.get_PinConnectionBar
- IMsRdpClientAdvancedSettings6.put_PinConnectionBar
- IMsRdpClientAdvancedSettings7.PinConnectionBar
- IMsRdpClientAdvancedSettings7.get_PinConnectionBar
- IMsRdpClientAdvancedSettings7.put_PinConnectionBar
- IMsRdpClientAdvancedSettings8.PinConnectionBar
- IMsRdpClientAdvancedSettings8.get_PinConnectionBar
- IMsRdpClientAdvancedSettings8.put_PinConnectionBar
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0da294d933026194d7307a7fa0a175575761809e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843112"
---
# <a name="imsrdpclientadvancedsettingspinconnectionbar-property"></a><span data-ttu-id="217b2-120">IMsRdpClientAdvancedSettings：:P inConnectionBar 屬性</span><span class="sxs-lookup"><span data-stu-id="217b2-120">IMsRdpClientAdvancedSettings::PinConnectionBar property</span></span>

<span data-ttu-id="217b2-121">指定 UI 連接列的狀態。</span><span class="sxs-lookup"><span data-stu-id="217b2-121">Specifies the state of the UI connection bar.</span></span>

<span data-ttu-id="217b2-122">如果容器呼叫 [**IObjectSafety：： SetInterfaceSafetyOptions**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768225(v=vs.85))方法，這個屬性會傳回 **E \_ >notimpl** 。</span><span class="sxs-lookup"><span data-stu-id="217b2-122">This property returns **E\_NOTIMPL** if the container calls the [**IObjectSafety::SetInterfaceSafetyOptions**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768225(v=vs.85)) method.</span></span>

<span data-ttu-id="217b2-123">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="217b2-123">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="217b2-124">Syntax</span><span class="sxs-lookup"><span data-stu-id="217b2-124">Syntax</span></span>


```C++
HRESULT put_PinConnectionBar(
  [in]  VARIANT_BOOL fPinConnectionBar
);

HRESULT get_PinConnectionBar(
  [out] VARIANT_BOOL *pfPinConnectionBar
);
```



## <a name="property-value"></a><span data-ttu-id="217b2-125">屬性值</span><span class="sxs-lookup"><span data-stu-id="217b2-125">Property value</span></span>

<span data-ttu-id="217b2-126">將此屬性設定為 **VARIANT \_ TRUE** 會將狀態設定為「減少」，也就是使用者看不到，而且無法輸入。</span><span class="sxs-lookup"><span data-stu-id="217b2-126">Setting this property to **VARIANT\_TRUE** sets the state to "lowered", that is, invisible to the user and unavailable for input.</span></span> <span data-ttu-id="217b2-127">**變異 \_FALSE** 會將狀態設定為「已引發」，並可供使用者輸入。</span><span class="sxs-lookup"><span data-stu-id="217b2-127">**VARIANT\_FALSE** sets the state to "raised" and available for user input.</span></span>

## <a name="error-codes"></a><span data-ttu-id="217b2-128">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="217b2-128">Error codes</span></span>

<span data-ttu-id="217b2-129">如果成功，則傳回 **S \_ OK** 。</span><span class="sxs-lookup"><span data-stu-id="217b2-129">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="217b2-130">備註</span><span class="sxs-lookup"><span data-stu-id="217b2-130">Remarks</span></span>

<span data-ttu-id="217b2-131">如需遠端桌面網頁連線的詳細資訊，請參閱 [遠端桌面網頁連線的需求](requirements-for-remote-desktop-web-connection.md)。</span><span class="sxs-lookup"><span data-stu-id="217b2-131">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="217b2-132">規格需求</span><span class="sxs-lookup"><span data-stu-id="217b2-132">Requirements</span></span>



| <span data-ttu-id="217b2-133">需求</span><span class="sxs-lookup"><span data-stu-id="217b2-133">Requirement</span></span> | <span data-ttu-id="217b2-134">值</span><span class="sxs-lookup"><span data-stu-id="217b2-134">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="217b2-135">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="217b2-135">Minimum supported client</span></span><br/> | <span data-ttu-id="217b2-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="217b2-136">Windows Vista</span></span><br/>                                                                        |
| <span data-ttu-id="217b2-137">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="217b2-137">Minimum supported server</span></span><br/> | <span data-ttu-id="217b2-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="217b2-138">Windows Server 2008</span></span><br/>                                                                  |
| <span data-ttu-id="217b2-139">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="217b2-139">Type library</span></span><br/>             | <dl> <span data-ttu-id="217b2-140"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="217b2-140"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="217b2-141">DLL</span><span class="sxs-lookup"><span data-stu-id="217b2-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="217b2-142"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="217b2-142"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="217b2-143">IID</span><span class="sxs-lookup"><span data-stu-id="217b2-143">IID</span></span><br/>                      | <span data-ttu-id="217b2-144">IID \_ IMsRdpClientAdvancedSettings 定義為3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span><span class="sxs-lookup"><span data-stu-id="217b2-144">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="217b2-145">另請參閱</span><span class="sxs-lookup"><span data-stu-id="217b2-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="217b2-146">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="217b2-146">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="217b2-147">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="217b2-147">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="217b2-148">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="217b2-148">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="217b2-149">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="217b2-149">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="217b2-150">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="217b2-150">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="217b2-151">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="217b2-151">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="217b2-152">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="217b2-152">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="217b2-153">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="217b2-153">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

