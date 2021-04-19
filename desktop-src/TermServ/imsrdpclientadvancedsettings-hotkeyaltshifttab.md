---
title: IMsRdpClientAdvancedSettings HotKeyAltShiftTab 屬性
description: 指定要新增至 ALT 的虛擬按鍵碼，以判斷 ALT + SHIFT + TAB 的替換熱鍵。
ms.assetid: da52f2fb-15cc-4d55-b26e-cf5465290889
ms.tgt_platform: multiple
keywords:
- HotKeyAltShiftTab 屬性遠端桌面服務
- HotKeyAltShiftTab 屬性遠端桌面服務，IMsRdpClientAdvancedSettings 介面
- IMsRdpClientAdvancedSettings 介面遠端桌面服務，HotKeyAltShiftTab 屬性
- HotKeyAltShiftTab 屬性遠端桌面服務，IMsRdpClientAdvancedSettings2 介面
- IMsRdpClientAdvancedSettings2 介面遠端桌面服務，HotKeyAltShiftTab 屬性
- HotKeyAltShiftTab 屬性遠端桌面服務，IMsRdpClientAdvancedSettings3 介面
- IMsRdpClientAdvancedSettings3 介面遠端桌面服務，HotKeyAltShiftTab 屬性
- HotKeyAltShiftTab 屬性遠端桌面服務，IMsRdpClientAdvancedSettings4 介面
- IMsRdpClientAdvancedSettings4 介面遠端桌面服務，HotKeyAltShiftTab 屬性
- HotKeyAltShiftTab 屬性遠端桌面服務，IMsRdpClientAdvancedSettings5 介面
- IMsRdpClientAdvancedSettings5 介面遠端桌面服務，HotKeyAltShiftTab 屬性
- HotKeyAltShiftTab 屬性遠端桌面服務，IMsRdpClientAdvancedSettings6 介面
- IMsRdpClientAdvancedSettings6 介面遠端桌面服務，HotKeyAltShiftTab 屬性
- HotKeyAltShiftTab 屬性遠端桌面服務，IMsRdpClientAdvancedSettings7 介面
- IMsRdpClientAdvancedSettings7 介面遠端桌面服務，HotKeyAltShiftTab 屬性
- HotKeyAltShiftTab 屬性遠端桌面服務，IMsRdpClientAdvancedSettings8 介面
- IMsRdpClientAdvancedSettings8 介面遠端桌面服務，HotKeyAltShiftTab 屬性
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.HotKeyAltShiftTab
- IMsRdpClientAdvancedSettings.get_HotKeyAltShiftTab
- IMsRdpClientAdvancedSettings.put_HotKeyAltShiftTab
- IMsRdpClientAdvancedSettings2.HotKeyAltShiftTab
- IMsRdpClientAdvancedSettings2.get_HotKeyAltShiftTab
- IMsRdpClientAdvancedSettings2.put_HotKeyAltShiftTab
- IMsRdpClientAdvancedSettings3.HotKeyAltShiftTab
- IMsRdpClientAdvancedSettings3.get_HotKeyAltShiftTab
- IMsRdpClientAdvancedSettings3.put_HotKeyAltShiftTab
- IMsRdpClientAdvancedSettings4.HotKeyAltShiftTab
- IMsRdpClientAdvancedSettings4.get_HotKeyAltShiftTab
- IMsRdpClientAdvancedSettings4.put_HotKeyAltShiftTab
- IMsRdpClientAdvancedSettings5.HotKeyAltShiftTab
- IMsRdpClientAdvancedSettings5.get_HotKeyAltShiftTab
- IMsRdpClientAdvancedSettings5.put_HotKeyAltShiftTab
- IMsRdpClientAdvancedSettings6.HotKeyAltShiftTab
- IMsRdpClientAdvancedSettings6.get_HotKeyAltShiftTab
- IMsRdpClientAdvancedSettings6.put_HotKeyAltShiftTab
- IMsRdpClientAdvancedSettings7.HotKeyAltShiftTab
- IMsRdpClientAdvancedSettings7.get_HotKeyAltShiftTab
- IMsRdpClientAdvancedSettings7.put_HotKeyAltShiftTab
- IMsRdpClientAdvancedSettings8.HotKeyAltShiftTab
- IMsRdpClientAdvancedSettings8.get_HotKeyAltShiftTab
- IMsRdpClientAdvancedSettings8.put_HotKeyAltShiftTab
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9819ddcba3f9cb10450525467eb8accce958c2f0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106966915"
---
# <a name="imsrdpclientadvancedsettingshotkeyaltshifttab-property"></a><span data-ttu-id="891f3-120">IMsRdpClientAdvancedSettings：： HotKeyAltShiftTab 屬性</span><span class="sxs-lookup"><span data-stu-id="891f3-120">IMsRdpClientAdvancedSettings::HotKeyAltShiftTab property</span></span>

<span data-ttu-id="891f3-121">指定要新增至 ALT 的虛擬按鍵碼，以判斷 ALT + SHIFT + TAB 的替換熱鍵。</span><span class="sxs-lookup"><span data-stu-id="891f3-121">Specifies the virtual-key code to add to ALT to determine the hotkey replacement for ALT+SHIFT+TAB.</span></span>

<span data-ttu-id="891f3-122">只有在未啟用 [**KeyboardHookMode**](imsrdpclientsecuredsettings-keyboardhookmode.md) 屬性時，這個屬性才有效。</span><span class="sxs-lookup"><span data-stu-id="891f3-122">This property is valid only when the [**KeyboardHookMode**](imsrdpclientsecuredsettings-keyboardhookmode.md) property is not enabled.</span></span>

<span data-ttu-id="891f3-123">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="891f3-123">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="891f3-124">Syntax</span><span class="sxs-lookup"><span data-stu-id="891f3-124">Syntax</span></span>


```C++
HRESULT put_HotKeyAltShiftTab(
  [in]  LONG hotKeyAltShiftTab
);

HRESULT get_HotKeyAltShiftTab(
  [out] LONG *photKeyAltShiftTab
);
```



## <a name="property-value"></a><span data-ttu-id="891f3-125">屬性值</span><span class="sxs-lookup"><span data-stu-id="891f3-125">Property value</span></span>

<span data-ttu-id="891f3-126">新的虛擬金鑰程式碼。</span><span class="sxs-lookup"><span data-stu-id="891f3-126">The new virtual-key code.</span></span> <span data-ttu-id="891f3-127">**VK \_NEXT** 是預設值，以 ALT + PAGE DOWN 作為產生的順序。</span><span class="sxs-lookup"><span data-stu-id="891f3-127">**VK\_NEXT** is the default value, with ALT+PAGE DOWN as the resulting sequence.</span></span>

## <a name="error-codes"></a><span data-ttu-id="891f3-128">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="891f3-128">Error codes</span></span>

<span data-ttu-id="891f3-129">如果成功，則傳回 **S \_ OK** 。</span><span class="sxs-lookup"><span data-stu-id="891f3-129">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="891f3-130">備註</span><span class="sxs-lookup"><span data-stu-id="891f3-130">Remarks</span></span>

<span data-ttu-id="891f3-131">如需遠端桌面網頁連線的詳細資訊，請參閱 [遠端桌面網頁連線的需求](requirements-for-remote-desktop-web-connection.md)。</span><span class="sxs-lookup"><span data-stu-id="891f3-131">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="891f3-132">規格需求</span><span class="sxs-lookup"><span data-stu-id="891f3-132">Requirements</span></span>



| <span data-ttu-id="891f3-133">需求</span><span class="sxs-lookup"><span data-stu-id="891f3-133">Requirement</span></span> | <span data-ttu-id="891f3-134">值</span><span class="sxs-lookup"><span data-stu-id="891f3-134">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="891f3-135">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="891f3-135">Minimum supported client</span></span><br/> | <span data-ttu-id="891f3-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="891f3-136">Windows Vista</span></span><br/>                                                                        |
| <span data-ttu-id="891f3-137">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="891f3-137">Minimum supported server</span></span><br/> | <span data-ttu-id="891f3-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="891f3-138">Windows Server 2008</span></span><br/>                                                                  |
| <span data-ttu-id="891f3-139">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="891f3-139">Type library</span></span><br/>             | <dl> <span data-ttu-id="891f3-140"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="891f3-140"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="891f3-141">DLL</span><span class="sxs-lookup"><span data-stu-id="891f3-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="891f3-142"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="891f3-142"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="891f3-143">IID</span><span class="sxs-lookup"><span data-stu-id="891f3-143">IID</span></span><br/>                      | <span data-ttu-id="891f3-144">IID \_ IMsRdpClientAdvancedSettings 定義為3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span><span class="sxs-lookup"><span data-stu-id="891f3-144">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="891f3-145">另請參閱</span><span class="sxs-lookup"><span data-stu-id="891f3-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="891f3-146">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="891f3-146">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="891f3-147">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="891f3-147">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="891f3-148">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="891f3-148">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="891f3-149">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="891f3-149">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="891f3-150">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="891f3-150">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="891f3-151">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="891f3-151">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="891f3-152">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="891f3-152">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="891f3-153">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="891f3-153">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





