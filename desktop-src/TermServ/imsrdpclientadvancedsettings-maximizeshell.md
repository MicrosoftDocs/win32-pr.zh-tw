---
title: IMsRdpClientAdvancedSettings MaximizeShell 屬性
description: 指定是否應將以 StartProgram 屬性啟動的程式最大化。
ms.assetid: d8c194b6-04ef-495f-a763-7e18064230e6
ms.tgt_platform: multiple
keywords:
- MaximizeShell 屬性遠端桌面服務
- MaximizeShell 屬性遠端桌面服務，IMsRdpClientAdvancedSettings 介面
- IMsRdpClientAdvancedSettings 介面遠端桌面服務，MaximizeShell 屬性
- MaximizeShell 屬性遠端桌面服務，IMsRdpClientAdvancedSettings2 介面
- IMsRdpClientAdvancedSettings2 介面遠端桌面服務，MaximizeShell 屬性
- MaximizeShell 屬性遠端桌面服務，IMsRdpClientAdvancedSettings3 介面
- IMsRdpClientAdvancedSettings3 介面遠端桌面服務，MaximizeShell 屬性
- MaximizeShell 屬性遠端桌面服務，IMsRdpClientAdvancedSettings4 介面
- IMsRdpClientAdvancedSettings4 介面遠端桌面服務，MaximizeShell 屬性
- MaximizeShell 屬性遠端桌面服務，IMsRdpClientAdvancedSettings5 介面
- IMsRdpClientAdvancedSettings5 介面遠端桌面服務，MaximizeShell 屬性
- MaximizeShell 屬性遠端桌面服務，IMsRdpClientAdvancedSettings6 介面
- IMsRdpClientAdvancedSettings6 介面遠端桌面服務，MaximizeShell 屬性
- MaximizeShell 屬性遠端桌面服務，IMsRdpClientAdvancedSettings7 介面
- IMsRdpClientAdvancedSettings7 介面遠端桌面服務，MaximizeShell 屬性
- MaximizeShell 屬性遠端桌面服務，IMsRdpClientAdvancedSettings8 介面
- IMsRdpClientAdvancedSettings8 介面遠端桌面服務，MaximizeShell 屬性
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.MaximizeShell
- IMsRdpClientAdvancedSettings.get_MaximizeShell
- IMsRdpClientAdvancedSettings.put_MaximizeShell
- IMsRdpClientAdvancedSettings2.MaximizeShell
- IMsRdpClientAdvancedSettings2.get_MaximizeShell
- IMsRdpClientAdvancedSettings2.put_MaximizeShell
- IMsRdpClientAdvancedSettings3.MaximizeShell
- IMsRdpClientAdvancedSettings3.get_MaximizeShell
- IMsRdpClientAdvancedSettings3.put_MaximizeShell
- IMsRdpClientAdvancedSettings4.MaximizeShell
- IMsRdpClientAdvancedSettings4.get_MaximizeShell
- IMsRdpClientAdvancedSettings4.put_MaximizeShell
- IMsRdpClientAdvancedSettings5.MaximizeShell
- IMsRdpClientAdvancedSettings5.get_MaximizeShell
- IMsRdpClientAdvancedSettings5.put_MaximizeShell
- IMsRdpClientAdvancedSettings6.MaximizeShell
- IMsRdpClientAdvancedSettings6.get_MaximizeShell
- IMsRdpClientAdvancedSettings6.put_MaximizeShell
- IMsRdpClientAdvancedSettings7.MaximizeShell
- IMsRdpClientAdvancedSettings7.get_MaximizeShell
- IMsRdpClientAdvancedSettings7.put_MaximizeShell
- IMsRdpClientAdvancedSettings8.MaximizeShell
- IMsRdpClientAdvancedSettings8.get_MaximizeShell
- IMsRdpClientAdvancedSettings8.put_MaximizeShell
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 02c172dd71fcf57f2028f6ba64c93ceaeec2ffb2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934129"
---
# <a name="imsrdpclientadvancedsettingsmaximizeshell-property"></a><span data-ttu-id="7d777-120">IMsRdpClientAdvancedSettings：： MaximizeShell 屬性</span><span class="sxs-lookup"><span data-stu-id="7d777-120">IMsRdpClientAdvancedSettings::MaximizeShell property</span></span>

<span data-ttu-id="7d777-121">指定是否應將以 [**StartProgram**](imstscsecuredsettings-startprogram.md) 屬性啟動的程式最大化。</span><span class="sxs-lookup"><span data-stu-id="7d777-121">Specifies if programs launched with the [**StartProgram**](imstscsecuredsettings-startprogram.md) property should be maximized.</span></span>

<span data-ttu-id="7d777-122">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="7d777-122">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="7d777-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="7d777-123">Syntax</span></span>


```C++
HRESULT put_MaximizeShell(
  [in]  LONG maximizeShell
);

HRESULT get_MaximizeShell(
  [out] LONG *pmaximizeShell
);
```



## <a name="property-value"></a><span data-ttu-id="7d777-124">屬性值</span><span class="sxs-lookup"><span data-stu-id="7d777-124">Property value</span></span>

<span data-ttu-id="7d777-125">將此參數設定為0，以停用此功能或非零值以啟用此功能。</span><span class="sxs-lookup"><span data-stu-id="7d777-125">Set this parameter to 0 to disable the feature or a nonzero value to enable the feature.</span></span>

## <a name="error-codes"></a><span data-ttu-id="7d777-126">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="7d777-126">Error codes</span></span>

<span data-ttu-id="7d777-127">如果成功，則傳回 **S \_ OK** 。</span><span class="sxs-lookup"><span data-stu-id="7d777-127">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="7d777-128">備註</span><span class="sxs-lookup"><span data-stu-id="7d777-128">Remarks</span></span>

<span data-ttu-id="7d777-129">如需遠端桌面網頁連線的詳細資訊，請參閱 [遠端桌面網頁連線的需求](requirements-for-remote-desktop-web-connection.md)。</span><span class="sxs-lookup"><span data-stu-id="7d777-129">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7d777-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="7d777-130">Requirements</span></span>



| <span data-ttu-id="7d777-131">需求</span><span class="sxs-lookup"><span data-stu-id="7d777-131">Requirement</span></span> | <span data-ttu-id="7d777-132">值</span><span class="sxs-lookup"><span data-stu-id="7d777-132">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7d777-133">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7d777-133">Minimum supported client</span></span><br/> | <span data-ttu-id="7d777-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7d777-134">Windows Vista</span></span><br/>                                                                        |
| <span data-ttu-id="7d777-135">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7d777-135">Minimum supported server</span></span><br/> | <span data-ttu-id="7d777-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7d777-136">Windows Server 2008</span></span><br/>                                                                  |
| <span data-ttu-id="7d777-137">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="7d777-137">Type library</span></span><br/>             | <dl> <span data-ttu-id="7d777-138"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7d777-138"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="7d777-139">DLL</span><span class="sxs-lookup"><span data-stu-id="7d777-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7d777-140"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7d777-140"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="7d777-141">IID</span><span class="sxs-lookup"><span data-stu-id="7d777-141">IID</span></span><br/>                      | <span data-ttu-id="7d777-142">IID \_ IMsRdpClientAdvancedSettings 定義為3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span><span class="sxs-lookup"><span data-stu-id="7d777-142">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="7d777-143">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7d777-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7d777-144">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="7d777-144">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="7d777-145">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="7d777-145">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="7d777-146">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="7d777-146">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="7d777-147">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="7d777-147">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="7d777-148">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="7d777-148">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="7d777-149">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="7d777-149">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="7d777-150">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="7d777-150">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="7d777-151">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="7d777-151">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





