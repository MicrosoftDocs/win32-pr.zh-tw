---
title: IMsRdpClientAdvancedSettings HotKeyAltTab 屬性
description: 指定要新增至 ALT 的虛擬金鑰程式碼，以判斷 ALT + TAB 的替換熱鍵。
ms.assetid: d7066fb4-f53f-4e55-ba12-fb4078ece144
ms.tgt_platform: multiple
keywords:
- HotKeyAltTab 屬性遠端桌面服務
- HotKeyAltTab 屬性遠端桌面服務，IMsRdpClientAdvancedSettings 介面
- IMsRdpClientAdvancedSettings 介面遠端桌面服務，HotKeyAltTab 屬性
- HotKeyAltTab 屬性遠端桌面服務，IMsRdpClientAdvancedSettings2 介面
- IMsRdpClientAdvancedSettings2 介面遠端桌面服務，HotKeyAltTab 屬性
- HotKeyAltTab 屬性遠端桌面服務，IMsRdpClientAdvancedSettings3 介面
- IMsRdpClientAdvancedSettings3 介面遠端桌面服務，HotKeyAltTab 屬性
- HotKeyAltTab 屬性遠端桌面服務，IMsRdpClientAdvancedSettings4 介面
- IMsRdpClientAdvancedSettings4 介面遠端桌面服務，HotKeyAltTab 屬性
- HotKeyAltTab 屬性遠端桌面服務，IMsRdpClientAdvancedSettings5 介面
- IMsRdpClientAdvancedSettings5 介面遠端桌面服務，HotKeyAltTab 屬性
- HotKeyAltTab 屬性遠端桌面服務，IMsRdpClientAdvancedSettings6 介面
- IMsRdpClientAdvancedSettings6 介面遠端桌面服務，HotKeyAltTab 屬性
- HotKeyAltTab 屬性遠端桌面服務，IMsRdpClientAdvancedSettings7 介面
- IMsRdpClientAdvancedSettings7 介面遠端桌面服務，HotKeyAltTab 屬性
- HotKeyAltTab 屬性遠端桌面服務，IMsRdpClientAdvancedSettings8 介面
- IMsRdpClientAdvancedSettings8 介面遠端桌面服務，HotKeyAltTab 屬性
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.HotKeyAltTab
- IMsRdpClientAdvancedSettings.get_HotKeyAltTab
- IMsRdpClientAdvancedSettings.put_HotKeyAltTab
- IMsRdpClientAdvancedSettings2.HotKeyAltTab
- IMsRdpClientAdvancedSettings2.get_HotKeyAltTab
- IMsRdpClientAdvancedSettings2.put_HotKeyAltTab
- IMsRdpClientAdvancedSettings3.HotKeyAltTab
- IMsRdpClientAdvancedSettings3.get_HotKeyAltTab
- IMsRdpClientAdvancedSettings3.put_HotKeyAltTab
- IMsRdpClientAdvancedSettings4.HotKeyAltTab
- IMsRdpClientAdvancedSettings4.get_HotKeyAltTab
- IMsRdpClientAdvancedSettings4.put_HotKeyAltTab
- IMsRdpClientAdvancedSettings5.HotKeyAltTab
- IMsRdpClientAdvancedSettings5.get_HotKeyAltTab
- IMsRdpClientAdvancedSettings5.put_HotKeyAltTab
- IMsRdpClientAdvancedSettings6.HotKeyAltTab
- IMsRdpClientAdvancedSettings6.get_HotKeyAltTab
- IMsRdpClientAdvancedSettings6.put_HotKeyAltTab
- IMsRdpClientAdvancedSettings7.HotKeyAltTab
- IMsRdpClientAdvancedSettings7.get_HotKeyAltTab
- IMsRdpClientAdvancedSettings7.put_HotKeyAltTab
- IMsRdpClientAdvancedSettings8.HotKeyAltTab
- IMsRdpClientAdvancedSettings8.get_HotKeyAltTab
- IMsRdpClientAdvancedSettings8.put_HotKeyAltTab
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eec7834a95b83ec43553d0ced1e056860cfb5abe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384313"
---
# <a name="imsrdpclientadvancedsettingshotkeyalttab-property"></a><span data-ttu-id="707b1-120">IMsRdpClientAdvancedSettings：： HotKeyAltTab 屬性</span><span class="sxs-lookup"><span data-stu-id="707b1-120">IMsRdpClientAdvancedSettings::HotKeyAltTab property</span></span>

<span data-ttu-id="707b1-121">指定要新增至 ALT 的虛擬金鑰程式碼，以判斷 ALT + TAB 的替換熱鍵。</span><span class="sxs-lookup"><span data-stu-id="707b1-121">Specifies the virtual-key code to add to ALT to determine the hotkey replacement for ALT+TAB.</span></span>

<span data-ttu-id="707b1-122">只有在未啟用 [**KeyboardHookMode**](imsrdpclientsecuredsettings-keyboardhookmode.md) 屬性時，這個屬性才有效。</span><span class="sxs-lookup"><span data-stu-id="707b1-122">This property is valid only when the [**KeyboardHookMode**](imsrdpclientsecuredsettings-keyboardhookmode.md) property is not enabled.</span></span>

<span data-ttu-id="707b1-123">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="707b1-123">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="707b1-124">Syntax</span><span class="sxs-lookup"><span data-stu-id="707b1-124">Syntax</span></span>


```C++
HRESULT put_HotKeyAltTab(
  [in]  LONG hotKeyAltTab
);

HRESULT get_HotKeyAltTab(
  [out] LONG *photKeyAltTab
);
```



## <a name="property-value"></a><span data-ttu-id="707b1-125">屬性值</span><span class="sxs-lookup"><span data-stu-id="707b1-125">Property value</span></span>

<span data-ttu-id="707b1-126">新的虛擬金鑰程式碼。</span><span class="sxs-lookup"><span data-stu-id="707b1-126">The new virtual-key code.</span></span> <span data-ttu-id="707b1-127">**VK \_先前** 是預設值，以 ALT + PAGE UP 作為產生的序列。</span><span class="sxs-lookup"><span data-stu-id="707b1-127">**VK\_PRIOR** is the default value, with ALT+PAGE UP as the resulting sequence.</span></span>

## <a name="error-codes"></a><span data-ttu-id="707b1-128">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="707b1-128">Error codes</span></span>

<span data-ttu-id="707b1-129">如果成功，則傳回 **S \_ OK** 。</span><span class="sxs-lookup"><span data-stu-id="707b1-129">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="707b1-130">備註</span><span class="sxs-lookup"><span data-stu-id="707b1-130">Remarks</span></span>

<span data-ttu-id="707b1-131">如需遠端桌面網頁連線的詳細資訊，請參閱 [遠端桌面網頁連線的需求](requirements-for-remote-desktop-web-connection.md)。</span><span class="sxs-lookup"><span data-stu-id="707b1-131">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="707b1-132">規格需求</span><span class="sxs-lookup"><span data-stu-id="707b1-132">Requirements</span></span>



| <span data-ttu-id="707b1-133">需求</span><span class="sxs-lookup"><span data-stu-id="707b1-133">Requirement</span></span> | <span data-ttu-id="707b1-134">值</span><span class="sxs-lookup"><span data-stu-id="707b1-134">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="707b1-135">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="707b1-135">Minimum supported client</span></span><br/> | <span data-ttu-id="707b1-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="707b1-136">Windows Vista</span></span><br/>                                                                        |
| <span data-ttu-id="707b1-137">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="707b1-137">Minimum supported server</span></span><br/> | <span data-ttu-id="707b1-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="707b1-138">Windows Server 2008</span></span><br/>                                                                  |
| <span data-ttu-id="707b1-139">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="707b1-139">Type library</span></span><br/>             | <dl> <span data-ttu-id="707b1-140"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="707b1-140"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="707b1-141">DLL</span><span class="sxs-lookup"><span data-stu-id="707b1-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="707b1-142"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="707b1-142"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="707b1-143">IID</span><span class="sxs-lookup"><span data-stu-id="707b1-143">IID</span></span><br/>                      | <span data-ttu-id="707b1-144">IID \_ IMsRdpClientAdvancedSettings 定義為3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span><span class="sxs-lookup"><span data-stu-id="707b1-144">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="707b1-145">另請參閱</span><span class="sxs-lookup"><span data-stu-id="707b1-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="707b1-146">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="707b1-146">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="707b1-147">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="707b1-147">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="707b1-148">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="707b1-148">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="707b1-149">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="707b1-149">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="707b1-150">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="707b1-150">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="707b1-151">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="707b1-151">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="707b1-152">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="707b1-152">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="707b1-153">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="707b1-153">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





