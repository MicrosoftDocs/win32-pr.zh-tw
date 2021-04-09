---
title: IMsRdpClientAdvancedSettings HotKeyFullScreen 屬性
description: 指定要新增至 CTRL + ALT 的虛擬機器碼，以決定切換至全螢幕模式的熱鍵取代。
ms.assetid: 75fda212-ec68-4b68-b7db-2bfcdee7a7de
ms.tgt_platform: multiple
keywords:
- HotKeyFullScreen 屬性遠端桌面服務
- HotKeyFullScreen 屬性遠端桌面服務，IMsRdpClientAdvancedSettings 介面
- IMsRdpClientAdvancedSettings 介面遠端桌面服務，HotKeyFullScreen 屬性
- HotKeyFullScreen 屬性遠端桌面服務，IMsRdpClientAdvancedSettings2 介面
- IMsRdpClientAdvancedSettings2 介面遠端桌面服務，HotKeyFullScreen 屬性
- HotKeyFullScreen 屬性遠端桌面服務，IMsRdpClientAdvancedSettings3 介面
- IMsRdpClientAdvancedSettings3 介面遠端桌面服務，HotKeyFullScreen 屬性
- HotKeyFullScreen 屬性遠端桌面服務，IMsRdpClientAdvancedSettings4 介面
- IMsRdpClientAdvancedSettings4 介面遠端桌面服務，HotKeyFullScreen 屬性
- HotKeyFullScreen 屬性遠端桌面服務，IMsRdpClientAdvancedSettings5 介面
- IMsRdpClientAdvancedSettings5 介面遠端桌面服務，HotKeyFullScreen 屬性
- HotKeyFullScreen 屬性遠端桌面服務，IMsRdpClientAdvancedSettings6 介面
- IMsRdpClientAdvancedSettings6 介面遠端桌面服務，HotKeyFullScreen 屬性
- HotKeyFullScreen 屬性遠端桌面服務，IMsRdpClientAdvancedSettings7 介面
- IMsRdpClientAdvancedSettings7 介面遠端桌面服務，HotKeyFullScreen 屬性
- HotKeyFullScreen 屬性遠端桌面服務，IMsRdpClientAdvancedSettings8 介面
- IMsRdpClientAdvancedSettings8 介面遠端桌面服務，HotKeyFullScreen 屬性
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.HotKeyFullScreen
- IMsRdpClientAdvancedSettings.get_HotKeyFullScreen
- IMsRdpClientAdvancedSettings.put_HotKeyFullScreen
- IMsRdpClientAdvancedSettings2.HotKeyFullScreen
- IMsRdpClientAdvancedSettings2.get_HotKeyFullScreen
- IMsRdpClientAdvancedSettings2.put_HotKeyFullScreen
- IMsRdpClientAdvancedSettings3.HotKeyFullScreen
- IMsRdpClientAdvancedSettings3.get_HotKeyFullScreen
- IMsRdpClientAdvancedSettings3.put_HotKeyFullScreen
- IMsRdpClientAdvancedSettings4.HotKeyFullScreen
- IMsRdpClientAdvancedSettings4.get_HotKeyFullScreen
- IMsRdpClientAdvancedSettings4.put_HotKeyFullScreen
- IMsRdpClientAdvancedSettings5.HotKeyFullScreen
- IMsRdpClientAdvancedSettings5.get_HotKeyFullScreen
- IMsRdpClientAdvancedSettings5.put_HotKeyFullScreen
- IMsRdpClientAdvancedSettings6.HotKeyFullScreen
- IMsRdpClientAdvancedSettings6.get_HotKeyFullScreen
- IMsRdpClientAdvancedSettings6.put_HotKeyFullScreen
- IMsRdpClientAdvancedSettings7.HotKeyFullScreen
- IMsRdpClientAdvancedSettings7.get_HotKeyFullScreen
- IMsRdpClientAdvancedSettings7.put_HotKeyFullScreen
- IMsRdpClientAdvancedSettings8.HotKeyFullScreen
- IMsRdpClientAdvancedSettings8.get_HotKeyFullScreen
- IMsRdpClientAdvancedSettings8.put_HotKeyFullScreen
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed9c53dd0c6dff9e47b87ea8c8697c20b3613a14
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934001"
---
# <a name="imsrdpclientadvancedsettingshotkeyfullscreen-property"></a><span data-ttu-id="f8760-120">IMsRdpClientAdvancedSettings：： HotKeyFullScreen 屬性</span><span class="sxs-lookup"><span data-stu-id="f8760-120">IMsRdpClientAdvancedSettings::HotKeyFullScreen property</span></span>

<span data-ttu-id="f8760-121">指定要新增至 CTRL + ALT 的虛擬機器碼，以決定切換至全螢幕模式的熱鍵取代。</span><span class="sxs-lookup"><span data-stu-id="f8760-121">Specifies the virtual-key code to add to CTRL+ALT to determine the hotkey replacement for switching to full-screen mode.</span></span>

<span data-ttu-id="f8760-122">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="f8760-122">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="f8760-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="f8760-123">Syntax</span></span>


```C++
HRESULT put_HotKeyFullScreen(
  [in]  LONG hotKeyFullScreen
);

HRESULT get_HotKeyFullScreen(
  [out] LONG *photKeyFullScreen
);
```



## <a name="property-value"></a><span data-ttu-id="f8760-124">屬性值</span><span class="sxs-lookup"><span data-stu-id="f8760-124">Property value</span></span>

<span data-ttu-id="f8760-125">新的虛擬金鑰程式碼。</span><span class="sxs-lookup"><span data-stu-id="f8760-125">The new virtual-key code.</span></span> <span data-ttu-id="f8760-126">**VK \_[取消** ] 是預設值。</span><span class="sxs-lookup"><span data-stu-id="f8760-126">**VK\_CANCEL** is the default value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="f8760-127">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="f8760-127">Error codes</span></span>

<span data-ttu-id="f8760-128">如果成功，則傳回 **S \_ OK** 。</span><span class="sxs-lookup"><span data-stu-id="f8760-128">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="f8760-129">備註</span><span class="sxs-lookup"><span data-stu-id="f8760-129">Remarks</span></span>

<span data-ttu-id="f8760-130">如需遠端桌面網頁連線的詳細資訊，請參閱 [遠端桌面網頁連線的需求](requirements-for-remote-desktop-web-connection.md)。</span><span class="sxs-lookup"><span data-stu-id="f8760-130">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f8760-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="f8760-131">Requirements</span></span>



| <span data-ttu-id="f8760-132">需求</span><span class="sxs-lookup"><span data-stu-id="f8760-132">Requirement</span></span> | <span data-ttu-id="f8760-133">值</span><span class="sxs-lookup"><span data-stu-id="f8760-133">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f8760-134">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f8760-134">Minimum supported client</span></span><br/> | <span data-ttu-id="f8760-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f8760-135">Windows Vista</span></span><br/>                                                                        |
| <span data-ttu-id="f8760-136">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f8760-136">Minimum supported server</span></span><br/> | <span data-ttu-id="f8760-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f8760-137">Windows Server 2008</span></span><br/>                                                                  |
| <span data-ttu-id="f8760-138">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="f8760-138">Type library</span></span><br/>             | <dl> <span data-ttu-id="f8760-139"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f8760-139"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="f8760-140">DLL</span><span class="sxs-lookup"><span data-stu-id="f8760-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f8760-141"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f8760-141"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="f8760-142">IID</span><span class="sxs-lookup"><span data-stu-id="f8760-142">IID</span></span><br/>                      | <span data-ttu-id="f8760-143">IID \_ IMsRdpClientAdvancedSettings 定義為3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span><span class="sxs-lookup"><span data-stu-id="f8760-143">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f8760-144">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f8760-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f8760-145">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="f8760-145">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="f8760-146">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="f8760-146">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="f8760-147">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="f8760-147">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="f8760-148">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="f8760-148">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="f8760-149">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="f8760-149">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="f8760-150">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="f8760-150">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="f8760-151">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="f8760-151">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="f8760-152">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="f8760-152">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





