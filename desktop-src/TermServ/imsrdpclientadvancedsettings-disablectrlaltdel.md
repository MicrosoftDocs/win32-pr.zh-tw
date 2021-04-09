---
title: IMsRdpClientAdvancedSettings DisableCtrlAltDel 屬性
description: 指定是否應顯示 Winlogon 中的初始說明畫面。
ms.assetid: 79212472-105f-4e92-8065-f97819637d02
ms.tgt_platform: multiple
keywords:
- DisableCtrlAltDel 屬性遠端桌面服務
- DisableCtrlAltDel 屬性遠端桌面服務，IMsRdpClientAdvancedSettings 介面
- IMsRdpClientAdvancedSettings 介面遠端桌面服務，DisableCtrlAltDel 屬性
- DisableCtrlAltDel 屬性遠端桌面服務，IMsRdpClientAdvancedSettings2 介面
- IMsRdpClientAdvancedSettings2 介面遠端桌面服務，DisableCtrlAltDel 屬性
- DisableCtrlAltDel 屬性遠端桌面服務，IMsRdpClientAdvancedSettings3 介面
- IMsRdpClientAdvancedSettings3 介面遠端桌面服務，DisableCtrlAltDel 屬性
- DisableCtrlAltDel 屬性遠端桌面服務，IMsRdpClientAdvancedSettings4 介面
- IMsRdpClientAdvancedSettings4 介面遠端桌面服務，DisableCtrlAltDel 屬性
- DisableCtrlAltDel 屬性遠端桌面服務，IMsRdpClientAdvancedSettings5 介面
- IMsRdpClientAdvancedSettings5 介面遠端桌面服務，DisableCtrlAltDel 屬性
- DisableCtrlAltDel 屬性遠端桌面服務，IMsRdpClientAdvancedSettings6 介面
- IMsRdpClientAdvancedSettings6 介面遠端桌面服務，DisableCtrlAltDel 屬性
- DisableCtrlAltDel 屬性遠端桌面服務，IMsRdpClientAdvancedSettings7 介面
- IMsRdpClientAdvancedSettings7 介面遠端桌面服務，DisableCtrlAltDel 屬性
- DisableCtrlAltDel 屬性遠端桌面服務，IMsRdpClientAdvancedSettings8 介面
- IMsRdpClientAdvancedSettings8 介面遠端桌面服務，DisableCtrlAltDel 屬性
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.DisableCtrlAltDel
- IMsRdpClientAdvancedSettings.get_DisableCtrlAltDel
- IMsRdpClientAdvancedSettings.put_DisableCtrlAltDel
- IMsRdpClientAdvancedSettings2.DisableCtrlAltDel
- IMsRdpClientAdvancedSettings2.get_DisableCtrlAltDel
- IMsRdpClientAdvancedSettings2.put_DisableCtrlAltDel
- IMsRdpClientAdvancedSettings3.DisableCtrlAltDel
- IMsRdpClientAdvancedSettings3.get_DisableCtrlAltDel
- IMsRdpClientAdvancedSettings3.put_DisableCtrlAltDel
- IMsRdpClientAdvancedSettings4.DisableCtrlAltDel
- IMsRdpClientAdvancedSettings4.get_DisableCtrlAltDel
- IMsRdpClientAdvancedSettings4.put_DisableCtrlAltDel
- IMsRdpClientAdvancedSettings5.DisableCtrlAltDel
- IMsRdpClientAdvancedSettings5.get_DisableCtrlAltDel
- IMsRdpClientAdvancedSettings5.put_DisableCtrlAltDel
- IMsRdpClientAdvancedSettings6.DisableCtrlAltDel
- IMsRdpClientAdvancedSettings6.get_DisableCtrlAltDel
- IMsRdpClientAdvancedSettings6.put_DisableCtrlAltDel
- IMsRdpClientAdvancedSettings7.DisableCtrlAltDel
- IMsRdpClientAdvancedSettings7.get_DisableCtrlAltDel
- IMsRdpClientAdvancedSettings7.put_DisableCtrlAltDel
- IMsRdpClientAdvancedSettings8.DisableCtrlAltDel
- IMsRdpClientAdvancedSettings8.get_DisableCtrlAltDel
- IMsRdpClientAdvancedSettings8.put_DisableCtrlAltDel
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3380aa78c16c7e937637cc727fe81f054649f929
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685672"
---
# <a name="imsrdpclientadvancedsettingsdisablectrlaltdel-property"></a><span data-ttu-id="a08cd-120">IMsRdpClientAdvancedSettings：:D isableCtrlAltDel 屬性</span><span class="sxs-lookup"><span data-stu-id="a08cd-120">IMsRdpClientAdvancedSettings::DisableCtrlAltDel property</span></span>

<span data-ttu-id="a08cd-121">指定是否應顯示 Winlogon 中的初始說明畫面。</span><span class="sxs-lookup"><span data-stu-id="a08cd-121">Specifies if the initial explanatory screen in Winlogon should display.</span></span>

<span data-ttu-id="a08cd-122">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="a08cd-122">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="a08cd-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="a08cd-123">Syntax</span></span>


```C++
HRESULT put_DisableCtrlAltDel(
  [in]  LONG disableCtrlAltDel
);

HRESULT get_DisableCtrlAltDel(
  [out] LONG *pdisableCtrlAltDel
);
```



## <a name="property-value"></a><span data-ttu-id="a08cd-124">屬性值</span><span class="sxs-lookup"><span data-stu-id="a08cd-124">Property value</span></span>

<span data-ttu-id="a08cd-125">將此參數設定為0，以停用此功能或非零值以啟用此功能。</span><span class="sxs-lookup"><span data-stu-id="a08cd-125">Set this parameter to 0 to disable the feature or a nonzero value to enable the feature.</span></span>

## <a name="error-codes"></a><span data-ttu-id="a08cd-126">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="a08cd-126">Error codes</span></span>

<span data-ttu-id="a08cd-127">如果成功，則傳回 **S \_ OK** 。</span><span class="sxs-lookup"><span data-stu-id="a08cd-127">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="a08cd-128">備註</span><span class="sxs-lookup"><span data-stu-id="a08cd-128">Remarks</span></span>

<span data-ttu-id="a08cd-129">如需遠端桌面網頁連線的詳細資訊，請參閱 [遠端桌面網頁連線的需求](requirements-for-remote-desktop-web-connection.md)。</span><span class="sxs-lookup"><span data-stu-id="a08cd-129">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a08cd-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="a08cd-130">Requirements</span></span>



| <span data-ttu-id="a08cd-131">需求</span><span class="sxs-lookup"><span data-stu-id="a08cd-131">Requirement</span></span> | <span data-ttu-id="a08cd-132">值</span><span class="sxs-lookup"><span data-stu-id="a08cd-132">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a08cd-133">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a08cd-133">Minimum supported client</span></span><br/> | <span data-ttu-id="a08cd-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a08cd-134">Windows Vista</span></span><br/>                                                                        |
| <span data-ttu-id="a08cd-135">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a08cd-135">Minimum supported server</span></span><br/> | <span data-ttu-id="a08cd-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a08cd-136">Windows Server 2008</span></span><br/>                                                                  |
| <span data-ttu-id="a08cd-137">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="a08cd-137">Type library</span></span><br/>             | <dl> <span data-ttu-id="a08cd-138"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a08cd-138"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="a08cd-139">DLL</span><span class="sxs-lookup"><span data-stu-id="a08cd-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a08cd-140"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a08cd-140"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="a08cd-141">IID</span><span class="sxs-lookup"><span data-stu-id="a08cd-141">IID</span></span><br/>                      | <span data-ttu-id="a08cd-142">IID \_ IMsRdpClientAdvancedSettings 定義為3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span><span class="sxs-lookup"><span data-stu-id="a08cd-142">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a08cd-143">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a08cd-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a08cd-144">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="a08cd-144">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="a08cd-145">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="a08cd-145">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="a08cd-146">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="a08cd-146">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="a08cd-147">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="a08cd-147">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="a08cd-148">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="a08cd-148">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="a08cd-149">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="a08cd-149">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="a08cd-150">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="a08cd-150">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="a08cd-151">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="a08cd-151">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





