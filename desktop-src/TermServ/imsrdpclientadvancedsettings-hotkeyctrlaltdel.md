---
title: IMsRdpClientAdvancedSettings HotKeyCtrlAltDel 屬性
description: 指定要新增至 CTRL + ALT 的虛擬金鑰程式碼，以決定 CTRL + ALT + DELETE 的熱鍵取代，也稱為 (SAS) 的安全注意順序。
ms.assetid: bce55cdb-4444-4291-b443-9bc1b3743e23
ms.tgt_platform: multiple
keywords:
- HotKeyCtrlAltDel 屬性遠端桌面服務
- HotKeyCtrlAltDel 屬性遠端桌面服務，IMsRdpClientAdvancedSettings 介面
- IMsRdpClientAdvancedSettings 介面遠端桌面服務，HotKeyCtrlAltDel 屬性
- HotKeyCtrlAltDel 屬性遠端桌面服務，IMsRdpClientAdvancedSettings2 介面
- IMsRdpClientAdvancedSettings2 介面遠端桌面服務，HotKeyCtrlAltDel 屬性
- HotKeyCtrlAltDel 屬性遠端桌面服務，IMsRdpClientAdvancedSettings3 介面
- IMsRdpClientAdvancedSettings3 介面遠端桌面服務，HotKeyCtrlAltDel 屬性
- HotKeyCtrlAltDel 屬性遠端桌面服務，IMsRdpClientAdvancedSettings4 介面
- IMsRdpClientAdvancedSettings4 介面遠端桌面服務，HotKeyCtrlAltDel 屬性
- HotKeyCtrlAltDel 屬性遠端桌面服務，IMsRdpClientAdvancedSettings5 介面
- IMsRdpClientAdvancedSettings5 介面遠端桌面服務，HotKeyCtrlAltDel 屬性
- HotKeyCtrlAltDel 屬性遠端桌面服務，IMsRdpClientAdvancedSettings6 介面
- IMsRdpClientAdvancedSettings6 介面遠端桌面服務，HotKeyCtrlAltDel 屬性
- HotKeyCtrlAltDel 屬性遠端桌面服務，IMsRdpClientAdvancedSettings7 介面
- IMsRdpClientAdvancedSettings7 介面遠端桌面服務，HotKeyCtrlAltDel 屬性
- HotKeyCtrlAltDel 屬性遠端桌面服務，IMsRdpClientAdvancedSettings8 介面
- IMsRdpClientAdvancedSettings8 介面遠端桌面服務，HotKeyCtrlAltDel 屬性
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.HotKeyCtrlAltDel
- IMsRdpClientAdvancedSettings.get_HotKeyCtrlAltDel
- IMsRdpClientAdvancedSettings.put_HotKeyCtrlAltDel
- IMsRdpClientAdvancedSettings2.HotKeyCtrlAltDel
- IMsRdpClientAdvancedSettings2.get_HotKeyCtrlAltDel
- IMsRdpClientAdvancedSettings2.put_HotKeyCtrlAltDel
- IMsRdpClientAdvancedSettings3.HotKeyCtrlAltDel
- IMsRdpClientAdvancedSettings3.get_HotKeyCtrlAltDel
- IMsRdpClientAdvancedSettings3.put_HotKeyCtrlAltDel
- IMsRdpClientAdvancedSettings4.HotKeyCtrlAltDel
- IMsRdpClientAdvancedSettings4.get_HotKeyCtrlAltDel
- IMsRdpClientAdvancedSettings4.put_HotKeyCtrlAltDel
- IMsRdpClientAdvancedSettings5.HotKeyCtrlAltDel
- IMsRdpClientAdvancedSettings5.get_HotKeyCtrlAltDel
- IMsRdpClientAdvancedSettings5.put_HotKeyCtrlAltDel
- IMsRdpClientAdvancedSettings6.HotKeyCtrlAltDel
- IMsRdpClientAdvancedSettings6.get_HotKeyCtrlAltDel
- IMsRdpClientAdvancedSettings6.put_HotKeyCtrlAltDel
- IMsRdpClientAdvancedSettings7.HotKeyCtrlAltDel
- IMsRdpClientAdvancedSettings7.get_HotKeyCtrlAltDel
- IMsRdpClientAdvancedSettings7.put_HotKeyCtrlAltDel
- IMsRdpClientAdvancedSettings8.HotKeyCtrlAltDel
- IMsRdpClientAdvancedSettings8.get_HotKeyCtrlAltDel
- IMsRdpClientAdvancedSettings8.put_HotKeyCtrlAltDel
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 00fa4c1f963841d0c1ea0375cdf11913b28d0286
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384041"
---
# <a name="imsrdpclientadvancedsettingshotkeyctrlaltdel-property"></a><span data-ttu-id="06e97-120">IMsRdpClientAdvancedSettings：： HotKeyCtrlAltDel 屬性</span><span class="sxs-lookup"><span data-stu-id="06e97-120">IMsRdpClientAdvancedSettings::HotKeyCtrlAltDel property</span></span>

<span data-ttu-id="06e97-121">指定要新增至 CTRL + ALT 的虛擬金鑰程式碼，以決定 CTRL + ALT + DELETE 的熱鍵取代，也稱為 (SAS) 的安全注意順序。</span><span class="sxs-lookup"><span data-stu-id="06e97-121">Specifies the virtual-key code to add to CTRL+ALT to determine the hotkey replacement for CTRL+ALT+DELETE, also called the secure attention sequence (SAS).</span></span>

> [!Note]  
> <span data-ttu-id="06e97-122">CTRL + ALT + DELETE 絕不會重新導向至遠端伺服器，即使已啟用 [KeyboardHookMode](imsrdpclientsecuredsettings-keyboardhookmode.md) 屬性;CTRL + ALT + DELETE 是本機 SAS 序列。</span><span class="sxs-lookup"><span data-stu-id="06e97-122">CTRL+ALT+DELETE is never redirected to the remote server, even when the [KeyboardHookMode](imsrdpclientsecuredsettings-keyboardhookmode.md) property is enabled; CTRL+ALT+DELETE is the local SAS sequence.</span></span>

 

<span data-ttu-id="06e97-123">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="06e97-123">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="06e97-124">Syntax</span><span class="sxs-lookup"><span data-stu-id="06e97-124">Syntax</span></span>


```C++
HRESULT put_HotKeyCtrlAltDel(
  [in]  LONG hotKeyCtrlAltDel
);

HRESULT get_HotKeyCtrlAltDel(
  [out] LONG *photKeyCtrlAltDel
);
```



## <a name="property-value"></a><span data-ttu-id="06e97-125">屬性值</span><span class="sxs-lookup"><span data-stu-id="06e97-125">Property value</span></span>

<span data-ttu-id="06e97-126">新的虛擬金鑰程式碼。</span><span class="sxs-lookup"><span data-stu-id="06e97-126">The new virtual-key code.</span></span> <span data-ttu-id="06e97-127">**VK \_END** 是預設值。</span><span class="sxs-lookup"><span data-stu-id="06e97-127">**VK\_END** is the default.</span></span>

## <a name="error-codes"></a><span data-ttu-id="06e97-128">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="06e97-128">Error codes</span></span>

<span data-ttu-id="06e97-129">如果成功，則傳回 **S \_ OK** 。</span><span class="sxs-lookup"><span data-stu-id="06e97-129">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="06e97-130">備註</span><span class="sxs-lookup"><span data-stu-id="06e97-130">Remarks</span></span>

<span data-ttu-id="06e97-131">如需遠端桌面網頁連線的詳細資訊，請參閱 [遠端桌面網頁連線的需求](requirements-for-remote-desktop-web-connection.md)。</span><span class="sxs-lookup"><span data-stu-id="06e97-131">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="06e97-132">規格需求</span><span class="sxs-lookup"><span data-stu-id="06e97-132">Requirements</span></span>



| <span data-ttu-id="06e97-133">需求</span><span class="sxs-lookup"><span data-stu-id="06e97-133">Requirement</span></span> | <span data-ttu-id="06e97-134">值</span><span class="sxs-lookup"><span data-stu-id="06e97-134">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="06e97-135">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="06e97-135">Minimum supported client</span></span><br/> | <span data-ttu-id="06e97-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="06e97-136">Windows Vista</span></span><br/>                                                                        |
| <span data-ttu-id="06e97-137">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="06e97-137">Minimum supported server</span></span><br/> | <span data-ttu-id="06e97-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="06e97-138">Windows Server 2008</span></span><br/>                                                                  |
| <span data-ttu-id="06e97-139">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="06e97-139">Type library</span></span><br/>             | <dl> <span data-ttu-id="06e97-140"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="06e97-140"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="06e97-141">DLL</span><span class="sxs-lookup"><span data-stu-id="06e97-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="06e97-142"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="06e97-142"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="06e97-143">IID</span><span class="sxs-lookup"><span data-stu-id="06e97-143">IID</span></span><br/>                      | <span data-ttu-id="06e97-144">IID \_ IMsRdpClientAdvancedSettings 定義為3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span><span class="sxs-lookup"><span data-stu-id="06e97-144">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="06e97-145">另請參閱</span><span class="sxs-lookup"><span data-stu-id="06e97-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="06e97-146">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="06e97-146">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="06e97-147">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="06e97-147">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="06e97-148">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="06e97-148">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="06e97-149">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="06e97-149">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="06e97-150">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="06e97-150">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="06e97-151">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="06e97-151">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="06e97-152">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="06e97-152">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="06e97-153">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="06e97-153">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





