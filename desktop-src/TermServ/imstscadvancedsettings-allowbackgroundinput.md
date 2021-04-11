---
title: IMsTscAdvancedSettings allowBackgroundInput 屬性
description: 指定是否啟用背景輸入模式。
ms.assetid: 2b57ebe9-3aad-400c-bcfb-d01c759b453d
ms.tgt_platform: multiple
keywords:
- allowBackgroundInput 屬性遠端桌面服務
- allowBackgroundInput 屬性遠端桌面服務，IMsTscAdvancedSettings 介面
- IMsTscAdvancedSettings 介面遠端桌面服務，allowBackgroundInput 屬性
- allowBackgroundInput 屬性遠端桌面服務，IMsRdpClientAdvancedSettings 介面
- IMsRdpClientAdvancedSettings 介面遠端桌面服務，allowBackgroundInput 屬性
- allowBackgroundInput 屬性遠端桌面服務，IMsRdpClientAdvancedSettings2 介面
- IMsRdpClientAdvancedSettings2 介面遠端桌面服務，allowBackgroundInput 屬性
- allowBackgroundInput 屬性遠端桌面服務，IMsRdpClientAdvancedSettings3 介面
- IMsRdpClientAdvancedSettings3 介面遠端桌面服務，allowBackgroundInput 屬性
- allowBackgroundInput 屬性遠端桌面服務，IMsRdpClientAdvancedSettings4 介面
- IMsRdpClientAdvancedSettings4 介面遠端桌面服務，allowBackgroundInput 屬性
- allowBackgroundInput 屬性遠端桌面服務，IMsRdpClientAdvancedSettings5 介面
- IMsRdpClientAdvancedSettings5 介面遠端桌面服務，allowBackgroundInput 屬性
- allowBackgroundInput 屬性遠端桌面服務，IMsRdpClientAdvancedSettings6 介面
- IMsRdpClientAdvancedSettings6 介面遠端桌面服務，allowBackgroundInput 屬性
- allowBackgroundInput 屬性遠端桌面服務，IMsRdpClientAdvancedSettings7 介面
- IMsRdpClientAdvancedSettings7 介面遠端桌面服務，allowBackgroundInput 屬性
- allowBackgroundInput 屬性遠端桌面服務，IMsRdpClientAdvancedSettings8 介面
- IMsRdpClientAdvancedSettings8 介面遠端桌面服務，allowBackgroundInput 屬性
topic_type:
- apiref
api_name:
- IMsTscAdvancedSettings.allowBackgroundInput
- IMsTscAdvancedSettings.get_allowBackgroundInput
- IMsTscAdvancedSettings.put_allowBackgroundInput
- IMsRdpClientAdvancedSettings.allowBackgroundInput
- IMsRdpClientAdvancedSettings.get_allowBackgroundInput
- IMsRdpClientAdvancedSettings.put_allowBackgroundInput
- IMsRdpClientAdvancedSettings2.allowBackgroundInput
- IMsRdpClientAdvancedSettings2.get_allowBackgroundInput
- IMsRdpClientAdvancedSettings2.put_allowBackgroundInput
- IMsRdpClientAdvancedSettings3.allowBackgroundInput
- IMsRdpClientAdvancedSettings3.get_allowBackgroundInput
- IMsRdpClientAdvancedSettings3.put_allowBackgroundInput
- IMsRdpClientAdvancedSettings4.allowBackgroundInput
- IMsRdpClientAdvancedSettings4.get_allowBackgroundInput
- IMsRdpClientAdvancedSettings4.put_allowBackgroundInput
- IMsRdpClientAdvancedSettings5.allowBackgroundInput
- IMsRdpClientAdvancedSettings5.get_allowBackgroundInput
- IMsRdpClientAdvancedSettings5.put_allowBackgroundInput
- IMsRdpClientAdvancedSettings6.allowBackgroundInput
- IMsRdpClientAdvancedSettings6.get_allowBackgroundInput
- IMsRdpClientAdvancedSettings6.put_allowBackgroundInput
- IMsRdpClientAdvancedSettings7.allowBackgroundInput
- IMsRdpClientAdvancedSettings7.get_allowBackgroundInput
- IMsRdpClientAdvancedSettings7.put_allowBackgroundInput
- IMsRdpClientAdvancedSettings8.allowBackgroundInput
- IMsRdpClientAdvancedSettings8.get_allowBackgroundInput
- IMsRdpClientAdvancedSettings8.put_allowBackgroundInput
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 938725ea1aa3d774d5993be695ac8568963897fb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104385246"
---
# <a name="imstscadvancedsettingsallowbackgroundinput-property"></a><span data-ttu-id="c51d6-122">IMsTscAdvancedSettings：： allowBackgroundInput 屬性</span><span class="sxs-lookup"><span data-stu-id="c51d6-122">IMsTscAdvancedSettings::allowBackgroundInput property</span></span>

<span data-ttu-id="c51d6-123">指定是否啟用背景輸入模式。</span><span class="sxs-lookup"><span data-stu-id="c51d6-123">Specifies whether background input mode is enabled.</span></span> <span data-ttu-id="c51d6-124">當背景輸入啟用時，用戶端可以在用戶端沒有焦點時接受輸入。</span><span class="sxs-lookup"><span data-stu-id="c51d6-124">When background input is enabled the client can accept input when the client does not have focus.</span></span>

<span data-ttu-id="c51d6-125">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="c51d6-125">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="c51d6-126">Syntax</span><span class="sxs-lookup"><span data-stu-id="c51d6-126">Syntax</span></span>


```C++
HRESULT put_allowBackgroundInput(
  [in]  LONG allowBackgroundInput
);

HRESULT get_allowBackgroundInput(
  [out] LONG *pallowBackgroundInput
);
```



## <a name="property-value"></a><span data-ttu-id="c51d6-127">屬性值</span><span class="sxs-lookup"><span data-stu-id="c51d6-127">Property value</span></span>

<span data-ttu-id="c51d6-128">將此參數設定為0可停用背景輸入模式或非零值，以啟用背景輸入模式。</span><span class="sxs-lookup"><span data-stu-id="c51d6-128">Set this parameter to 0 to disable background input mode or a nonzero value to enable background input mode.</span></span>

## <a name="error-codes"></a><span data-ttu-id="c51d6-129">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="c51d6-129">Error codes</span></span>

<span data-ttu-id="c51d6-130">如果成功，則傳回 **S \_ OK** 。</span><span class="sxs-lookup"><span data-stu-id="c51d6-130">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="c51d6-131">備註</span><span class="sxs-lookup"><span data-stu-id="c51d6-131">Remarks</span></span>

<span data-ttu-id="c51d6-132">如需遠端桌面網頁連線的詳細資訊，請參閱 [遠端桌面網頁連線的需求](requirements-for-remote-desktop-web-connection.md)。</span><span class="sxs-lookup"><span data-stu-id="c51d6-132">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c51d6-133">規格需求</span><span class="sxs-lookup"><span data-stu-id="c51d6-133">Requirements</span></span>



| <span data-ttu-id="c51d6-134">需求</span><span class="sxs-lookup"><span data-stu-id="c51d6-134">Requirement</span></span> | <span data-ttu-id="c51d6-135">值</span><span class="sxs-lookup"><span data-stu-id="c51d6-135">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="c51d6-136">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c51d6-136">Minimum supported client</span></span><br/> | <span data-ttu-id="c51d6-137">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c51d6-137">Windows Vista</span></span><br/>                                                                  |
| <span data-ttu-id="c51d6-138">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c51d6-138">Minimum supported server</span></span><br/> | <span data-ttu-id="c51d6-139">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c51d6-139">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="c51d6-140">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="c51d6-140">Type library</span></span><br/>             | <dl> <span data-ttu-id="c51d6-141"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c51d6-141"><dt>MsTscAx.dll</dt></span></span> </dl>    |
| <span data-ttu-id="c51d6-142">DLL</span><span class="sxs-lookup"><span data-stu-id="c51d6-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c51d6-143"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c51d6-143"><dt>MsTscAx.dll</dt></span></span> </dl>    |
| <span data-ttu-id="c51d6-144">IID</span><span class="sxs-lookup"><span data-stu-id="c51d6-144">IID</span></span><br/>                      | <span data-ttu-id="c51d6-145">IID \_ IMsTscAdvancedSettings 定義為809945cc-4b3b-4a92-a6b0-dbf9b5f2ef2d</span><span class="sxs-lookup"><span data-stu-id="c51d6-145">IID\_IMsTscAdvancedSettings is defined as 809945cc-4b3b-4a92-a6b0-dbf9b5f2ef2d</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c51d6-146">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c51d6-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c51d6-147">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="c51d6-147">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="c51d6-148">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="c51d6-148">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="c51d6-149">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="c51d6-149">**IMsRdpClientAdvancedSettings3**</span></span>](imsrdpclientadvancedsettings3.md)
</dt> <dt>

[<span data-ttu-id="c51d6-150">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="c51d6-150">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="c51d6-151">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="c51d6-151">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="c51d6-152">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="c51d6-152">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="c51d6-153">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="c51d6-153">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="c51d6-154">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="c51d6-154">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="c51d6-155">**IMsTscAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="c51d6-155">**IMsTscAdvancedSettings**</span></span>](imstscadvancedsettings-interface.md)
</dt> </dl>

 

 





