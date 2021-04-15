---
title: IMsRdpClientAdvancedSettings HotKeyAltEsc 屬性
description: 指定要新增至 ALT 的虛擬按鍵碼，以判斷 ALT + ESC 的熱鍵取代。
ms.assetid: 17cae4ca-8e97-4713-bb4e-ac9a9876c16c
ms.tgt_platform: multiple
keywords:
- HotKeyAltEsc 屬性遠端桌面服務
- HotKeyAltEsc 屬性遠端桌面服務，IMsRdpClientAdvancedSettings 介面
- IMsRdpClientAdvancedSettings 介面遠端桌面服務，HotKeyAltEsc 屬性
- HotKeyAltEsc 屬性遠端桌面服務，IMsRdpClientAdvancedSettings2 介面
- IMsRdpClientAdvancedSettings2 介面遠端桌面服務，HotKeyAltEsc 屬性
- HotKeyAltEsc 屬性遠端桌面服務，IMsRdpClientAdvancedSettings3 介面
- IMsRdpClientAdvancedSettings3 介面遠端桌面服務，HotKeyAltEsc 屬性
- HotKeyAltEsc 屬性遠端桌面服務，IMsRdpClientAdvancedSettings4 介面
- IMsRdpClientAdvancedSettings4 介面遠端桌面服務，HotKeyAltEsc 屬性
- HotKeyAltEsc 屬性遠端桌面服務，IMsRdpClientAdvancedSettings5 介面
- IMsRdpClientAdvancedSettings5 介面遠端桌面服務，HotKeyAltEsc 屬性
- HotKeyAltEsc 屬性遠端桌面服務，IMsRdpClientAdvancedSettings6 介面
- IMsRdpClientAdvancedSettings6 介面遠端桌面服務，HotKeyAltEsc 屬性
- HotKeyAltEsc 屬性遠端桌面服務，IMsRdpClientAdvancedSettings7 介面
- IMsRdpClientAdvancedSettings7 介面遠端桌面服務，HotKeyAltEsc 屬性
- HotKeyAltEsc 屬性遠端桌面服務，IMsRdpClientAdvancedSettings8 介面
- IMsRdpClientAdvancedSettings8 介面遠端桌面服務，HotKeyAltEsc 屬性
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.HotKeyAltEsc
- IMsRdpClientAdvancedSettings.get_HotKeyAltEsc
- IMsRdpClientAdvancedSettings.put_HotKeyAltEsc
- IMsRdpClientAdvancedSettings2.HotKeyAltEsc
- IMsRdpClientAdvancedSettings2.get_HotKeyAltEsc
- IMsRdpClientAdvancedSettings2.put_HotKeyAltEsc
- IMsRdpClientAdvancedSettings3.HotKeyAltEsc
- IMsRdpClientAdvancedSettings3.get_HotKeyAltEsc
- IMsRdpClientAdvancedSettings3.put_HotKeyAltEsc
- IMsRdpClientAdvancedSettings4.HotKeyAltEsc
- IMsRdpClientAdvancedSettings4.get_HotKeyAltEsc
- IMsRdpClientAdvancedSettings4.put_HotKeyAltEsc
- IMsRdpClientAdvancedSettings5.HotKeyAltEsc
- IMsRdpClientAdvancedSettings5.get_HotKeyAltEsc
- IMsRdpClientAdvancedSettings5.put_HotKeyAltEsc
- IMsRdpClientAdvancedSettings6.HotKeyAltEsc
- IMsRdpClientAdvancedSettings6.get_HotKeyAltEsc
- IMsRdpClientAdvancedSettings6.put_HotKeyAltEsc
- IMsRdpClientAdvancedSettings7.HotKeyAltEsc
- IMsRdpClientAdvancedSettings7.get_HotKeyAltEsc
- IMsRdpClientAdvancedSettings7.put_HotKeyAltEsc
- IMsRdpClientAdvancedSettings8.HotKeyAltEsc
- IMsRdpClientAdvancedSettings8.get_HotKeyAltEsc
- IMsRdpClientAdvancedSettings8.put_HotKeyAltEsc
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b661a91a0204177525063629825c478b40b4c29e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104467029"
---
# <a name="imsrdpclientadvancedsettingshotkeyaltesc-property"></a><span data-ttu-id="edec3-120">IMsRdpClientAdvancedSettings：： HotKeyAltEsc 屬性</span><span class="sxs-lookup"><span data-stu-id="edec3-120">IMsRdpClientAdvancedSettings::HotKeyAltEsc property</span></span>

<span data-ttu-id="edec3-121">指定要新增至 ALT 的虛擬按鍵碼，以判斷 ALT + ESC 的熱鍵取代。</span><span class="sxs-lookup"><span data-stu-id="edec3-121">Specifies the virtual-key code to add to ALT to determine the hotkey replacement for ALT+ESC.</span></span>

<span data-ttu-id="edec3-122">只有在未啟用 [**KeyboardHookMode**](imsrdpclientsecuredsettings-keyboardhookmode.md) 屬性時，這個屬性才有效。</span><span class="sxs-lookup"><span data-stu-id="edec3-122">This property is valid only when the [**KeyboardHookMode**](imsrdpclientsecuredsettings-keyboardhookmode.md) property is not enabled.</span></span>

<span data-ttu-id="edec3-123">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="edec3-123">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="edec3-124">Syntax</span><span class="sxs-lookup"><span data-stu-id="edec3-124">Syntax</span></span>


```C++
HRESULT put_HotKeyAltEsc(
  [in]  LONG hotKeyAltEsc
);

HRESULT get_HotKeyAltEsc(
  [out] LONG *photKeyAltEsc
);
```



## <a name="property-value"></a><span data-ttu-id="edec3-125">屬性值</span><span class="sxs-lookup"><span data-stu-id="edec3-125">Property value</span></span>

<span data-ttu-id="edec3-126">新的虛擬金鑰程式碼。</span><span class="sxs-lookup"><span data-stu-id="edec3-126">The new virtual-key code.</span></span> <span data-ttu-id="edec3-127">**VK \_INSERT** 是預設值，以 ALT + INSERT 作為產生的序列。</span><span class="sxs-lookup"><span data-stu-id="edec3-127">**VK\_INSERT** is the default value, with ALT+INSERT as the resulting sequence.</span></span>

## <a name="error-codes"></a><span data-ttu-id="edec3-128">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="edec3-128">Error codes</span></span>

<span data-ttu-id="edec3-129">如果成功，則傳回 **S \_ OK** 。</span><span class="sxs-lookup"><span data-stu-id="edec3-129">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="edec3-130">備註</span><span class="sxs-lookup"><span data-stu-id="edec3-130">Remarks</span></span>

<span data-ttu-id="edec3-131">如需遠端桌面網頁連線的詳細資訊，請參閱 [遠端桌面網頁連線的需求](requirements-for-remote-desktop-web-connection.md)。</span><span class="sxs-lookup"><span data-stu-id="edec3-131">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="edec3-132">規格需求</span><span class="sxs-lookup"><span data-stu-id="edec3-132">Requirements</span></span>



| <span data-ttu-id="edec3-133">需求</span><span class="sxs-lookup"><span data-stu-id="edec3-133">Requirement</span></span> | <span data-ttu-id="edec3-134">值</span><span class="sxs-lookup"><span data-stu-id="edec3-134">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="edec3-135">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="edec3-135">Minimum supported client</span></span><br/> | <span data-ttu-id="edec3-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="edec3-136">Windows Vista</span></span><br/>                                                                        |
| <span data-ttu-id="edec3-137">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="edec3-137">Minimum supported server</span></span><br/> | <span data-ttu-id="edec3-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="edec3-138">Windows Server 2008</span></span><br/>                                                                  |
| <span data-ttu-id="edec3-139">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="edec3-139">Type library</span></span><br/>             | <dl> <span data-ttu-id="edec3-140"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="edec3-140"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="edec3-141">DLL</span><span class="sxs-lookup"><span data-stu-id="edec3-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="edec3-142"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="edec3-142"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="edec3-143">IID</span><span class="sxs-lookup"><span data-stu-id="edec3-143">IID</span></span><br/>                      | <span data-ttu-id="edec3-144">IID \_ IMsRdpClientAdvancedSettings 定義為3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span><span class="sxs-lookup"><span data-stu-id="edec3-144">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="edec3-145">另請參閱</span><span class="sxs-lookup"><span data-stu-id="edec3-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="edec3-146">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="edec3-146">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="edec3-147">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="edec3-147">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="edec3-148">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="edec3-148">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="edec3-149">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="edec3-149">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="edec3-150">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="edec3-150">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="edec3-151">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="edec3-151">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="edec3-152">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="edec3-152">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="edec3-153">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="edec3-153">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





