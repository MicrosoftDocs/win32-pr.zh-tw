---
title: IMsRdpClientAdvancedSettings HotKeyCtrlEsc 屬性
description: 指定要新增至 ALT 的虛擬按鍵程式碼，以決定 CTRL + ESC 的熱鍵取代。
ms.assetid: 55d20a97-ce6e-4394-bfdf-c5bc880e7e2f
ms.tgt_platform: multiple
keywords:
- HotKeyCtrlEsc 屬性遠端桌面服務
- HotKeyCtrlEsc 屬性遠端桌面服務，IMsRdpClientAdvancedSettings 介面
- IMsRdpClientAdvancedSettings 介面遠端桌面服務，HotKeyCtrlEsc 屬性
- HotKeyCtrlEsc 屬性遠端桌面服務，IMsRdpClientAdvancedSettings2 介面
- IMsRdpClientAdvancedSettings2 介面遠端桌面服務，HotKeyCtrlEsc 屬性
- HotKeyCtrlEsc 屬性遠端桌面服務，IMsRdpClientAdvancedSettings3 介面
- IMsRdpClientAdvancedSettings3 介面遠端桌面服務，HotKeyCtrlEsc 屬性
- HotKeyCtrlEsc 屬性遠端桌面服務，IMsRdpClientAdvancedSettings4 介面
- IMsRdpClientAdvancedSettings4 介面遠端桌面服務，HotKeyCtrlEsc 屬性
- HotKeyCtrlEsc 屬性遠端桌面服務，IMsRdpClientAdvancedSettings5 介面
- IMsRdpClientAdvancedSettings5 介面遠端桌面服務，HotKeyCtrlEsc 屬性
- HotKeyCtrlEsc 屬性遠端桌面服務，IMsRdpClientAdvancedSettings6 介面
- IMsRdpClientAdvancedSettings6 介面遠端桌面服務，HotKeyCtrlEsc 屬性
- HotKeyCtrlEsc 屬性遠端桌面服務，IMsRdpClientAdvancedSettings7 介面
- IMsRdpClientAdvancedSettings7 介面遠端桌面服務，HotKeyCtrlEsc 屬性
- HotKeyCtrlEsc 屬性遠端桌面服務，IMsRdpClientAdvancedSettings8 介面
- IMsRdpClientAdvancedSettings8 介面遠端桌面服務，HotKeyCtrlEsc 屬性
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.HotKeyCtrlEsc
- IMsRdpClientAdvancedSettings.get_HotKeyCtrlEsc
- IMsRdpClientAdvancedSettings.put_HotKeyCtrlEsc
- IMsRdpClientAdvancedSettings2.HotKeyCtrlEsc
- IMsRdpClientAdvancedSettings2.get_HotKeyCtrlEsc
- IMsRdpClientAdvancedSettings2.put_HotKeyCtrlEsc
- IMsRdpClientAdvancedSettings3.HotKeyCtrlEsc
- IMsRdpClientAdvancedSettings3.get_HotKeyCtrlEsc
- IMsRdpClientAdvancedSettings3.put_HotKeyCtrlEsc
- IMsRdpClientAdvancedSettings4.HotKeyCtrlEsc
- IMsRdpClientAdvancedSettings4.get_HotKeyCtrlEsc
- IMsRdpClientAdvancedSettings4.put_HotKeyCtrlEsc
- IMsRdpClientAdvancedSettings5.HotKeyCtrlEsc
- IMsRdpClientAdvancedSettings5.get_HotKeyCtrlEsc
- IMsRdpClientAdvancedSettings5.put_HotKeyCtrlEsc
- IMsRdpClientAdvancedSettings6.HotKeyCtrlEsc
- IMsRdpClientAdvancedSettings6.get_HotKeyCtrlEsc
- IMsRdpClientAdvancedSettings6.put_HotKeyCtrlEsc
- IMsRdpClientAdvancedSettings7.HotKeyCtrlEsc
- IMsRdpClientAdvancedSettings7.get_HotKeyCtrlEsc
- IMsRdpClientAdvancedSettings7.put_HotKeyCtrlEsc
- IMsRdpClientAdvancedSettings8.HotKeyCtrlEsc
- IMsRdpClientAdvancedSettings8.get_HotKeyCtrlEsc
- IMsRdpClientAdvancedSettings8.put_HotKeyCtrlEsc
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf1a806430e8b93503c7cdc0fef04ba3f0a59b20
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106969585"
---
# <a name="imsrdpclientadvancedsettingshotkeyctrlesc-property"></a><span data-ttu-id="190a9-120">IMsRdpClientAdvancedSettings：： HotKeyCtrlEsc 屬性</span><span class="sxs-lookup"><span data-stu-id="190a9-120">IMsRdpClientAdvancedSettings::HotKeyCtrlEsc property</span></span>

<span data-ttu-id="190a9-121">指定要新增至 ALT 的虛擬按鍵程式碼，以決定 CTRL + ESC 的熱鍵取代。</span><span class="sxs-lookup"><span data-stu-id="190a9-121">Specifies the virtual-key code to add to ALT to determine the hotkey replacement for CTRL+ESC.</span></span>

<span data-ttu-id="190a9-122">只有在未啟用 [**KeyboardHookMode**](imsrdpclientsecuredsettings-keyboardhookmode.md) 屬性時，這個屬性才有效。</span><span class="sxs-lookup"><span data-stu-id="190a9-122">This property is valid only when the [**KeyboardHookMode**](imsrdpclientsecuredsettings-keyboardhookmode.md) property is not enabled.</span></span>

<span data-ttu-id="190a9-123">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="190a9-123">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="190a9-124">Syntax</span><span class="sxs-lookup"><span data-stu-id="190a9-124">Syntax</span></span>


```C++
HRESULT put_HotKeyCtrlEsc(
  [in]  LONG hotKeyCtrlEsc
);

HRESULT get_HotKeyCtrlEsc(
  [out] LONG *photKeyCtrlEsc
);
```



## <a name="property-value"></a><span data-ttu-id="190a9-125">屬性值</span><span class="sxs-lookup"><span data-stu-id="190a9-125">Property value</span></span>

<span data-ttu-id="190a9-126">新的虛擬金鑰程式碼。</span><span class="sxs-lookup"><span data-stu-id="190a9-126">The new virtual-key code.</span></span> <span data-ttu-id="190a9-127">**VK \_[首頁** ] 是預設值，以 ALT + HOME 作為產生的順序。</span><span class="sxs-lookup"><span data-stu-id="190a9-127">**VK\_HOME** is the default value, with ALT+HOME as the resulting sequence.</span></span>

## <a name="error-codes"></a><span data-ttu-id="190a9-128">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="190a9-128">Error codes</span></span>

<span data-ttu-id="190a9-129">如果成功，則傳回 **S \_ OK** 。</span><span class="sxs-lookup"><span data-stu-id="190a9-129">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="190a9-130">備註</span><span class="sxs-lookup"><span data-stu-id="190a9-130">Remarks</span></span>

<span data-ttu-id="190a9-131">如需遠端桌面網頁連線的詳細資訊，請參閱 [遠端桌面網頁連線的需求](requirements-for-remote-desktop-web-connection.md)。</span><span class="sxs-lookup"><span data-stu-id="190a9-131">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="190a9-132">規格需求</span><span class="sxs-lookup"><span data-stu-id="190a9-132">Requirements</span></span>



| <span data-ttu-id="190a9-133">需求</span><span class="sxs-lookup"><span data-stu-id="190a9-133">Requirement</span></span> | <span data-ttu-id="190a9-134">值</span><span class="sxs-lookup"><span data-stu-id="190a9-134">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="190a9-135">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="190a9-135">Minimum supported client</span></span><br/> | <span data-ttu-id="190a9-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="190a9-136">Windows Vista</span></span><br/>                                                                        |
| <span data-ttu-id="190a9-137">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="190a9-137">Minimum supported server</span></span><br/> | <span data-ttu-id="190a9-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="190a9-138">Windows Server 2008</span></span><br/>                                                                  |
| <span data-ttu-id="190a9-139">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="190a9-139">Type library</span></span><br/>             | <dl> <span data-ttu-id="190a9-140"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="190a9-140"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="190a9-141">DLL</span><span class="sxs-lookup"><span data-stu-id="190a9-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="190a9-142"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="190a9-142"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="190a9-143">IID</span><span class="sxs-lookup"><span data-stu-id="190a9-143">IID</span></span><br/>                      | <span data-ttu-id="190a9-144">IID \_ IMsRdpClientAdvancedSettings 定義為3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span><span class="sxs-lookup"><span data-stu-id="190a9-144">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="190a9-145">另請參閱</span><span class="sxs-lookup"><span data-stu-id="190a9-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="190a9-146">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="190a9-146">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="190a9-147">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="190a9-147">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="190a9-148">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="190a9-148">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="190a9-149">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="190a9-149">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="190a9-150">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="190a9-150">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="190a9-151">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="190a9-151">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="190a9-152">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="190a9-152">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="190a9-153">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="190a9-153">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





