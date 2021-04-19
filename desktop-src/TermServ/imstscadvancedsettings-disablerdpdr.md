---
title: IMsTscAdvancedSettings DisableRdpdr 屬性
description: 指定是否啟用印表機和剪貼簿重新導向。
ms.assetid: 63e0e024-4792-4efe-a6c5-d122f8adcb0a
ms.tgt_platform: multiple
keywords:
- DisableRdpdr 屬性遠端桌面服務
- DisableRdpdr 屬性遠端桌面服務，IMsTscAdvancedSettings 介面
- IMsTscAdvancedSettings 介面遠端桌面服務，DisableRdpdr 屬性
- DisableRdpdr 屬性遠端桌面服務，IMsRdpClientAdvancedSettings 介面
- IMsRdpClientAdvancedSettings 介面遠端桌面服務，DisableRdpdr 屬性
- DisableRdpdr 屬性遠端桌面服務，IMsRdpClientAdvancedSettings2 介面
- IMsRdpClientAdvancedSettings2 介面遠端桌面服務，DisableRdpdr 屬性
- DisableRdpdr 屬性遠端桌面服務，IMsRdpClientAdvancedSettings3 介面
- IMsRdpClientAdvancedSettings3 介面遠端桌面服務，DisableRdpdr 屬性
- DisableRdpdr 屬性遠端桌面服務，IMsRdpClientAdvancedSettings4 介面
- IMsRdpClientAdvancedSettings4 介面遠端桌面服務，DisableRdpdr 屬性
- DisableRdpdr 屬性遠端桌面服務，IMsRdpClientAdvancedSettings5 介面
- IMsRdpClientAdvancedSettings5 介面遠端桌面服務，DisableRdpdr 屬性
- DisableRdpdr 屬性遠端桌面服務，IMsRdpClientAdvancedSettings6 介面
- IMsRdpClientAdvancedSettings6 介面遠端桌面服務，DisableRdpdr 屬性
- DisableRdpdr 屬性遠端桌面服務，IMsRdpClientAdvancedSettings7 介面
- IMsRdpClientAdvancedSettings7 介面遠端桌面服務，DisableRdpdr 屬性
- DisableRdpdr 屬性遠端桌面服務，IMsRdpClientAdvancedSettings8 介面
- IMsRdpClientAdvancedSettings8 介面遠端桌面服務，DisableRdpdr 屬性
topic_type:
- apiref
api_name:
- IMsTscAdvancedSettings.DisableRdpdr
- IMsTscAdvancedSettings.get_DisableRdpdr
- IMsTscAdvancedSettings.put_DisableRdpdr
- IMsRdpClientAdvancedSettings.DisableRdpdr
- IMsRdpClientAdvancedSettings.get_DisableRdpdr
- IMsRdpClientAdvancedSettings.put_DisableRdpdr
- IMsRdpClientAdvancedSettings2.DisableRdpdr
- IMsRdpClientAdvancedSettings2.get_DisableRdpdr
- IMsRdpClientAdvancedSettings2.put_DisableRdpdr
- IMsRdpClientAdvancedSettings3.DisableRdpdr
- IMsRdpClientAdvancedSettings3.get_DisableRdpdr
- IMsRdpClientAdvancedSettings3.put_DisableRdpdr
- IMsRdpClientAdvancedSettings4.DisableRdpdr
- IMsRdpClientAdvancedSettings4.get_DisableRdpdr
- IMsRdpClientAdvancedSettings4.put_DisableRdpdr
- IMsRdpClientAdvancedSettings5.DisableRdpdr
- IMsRdpClientAdvancedSettings5.get_DisableRdpdr
- IMsRdpClientAdvancedSettings5.put_DisableRdpdr
- IMsRdpClientAdvancedSettings6.DisableRdpdr
- IMsRdpClientAdvancedSettings6.get_DisableRdpdr
- IMsRdpClientAdvancedSettings6.put_DisableRdpdr
- IMsRdpClientAdvancedSettings7.DisableRdpdr
- IMsRdpClientAdvancedSettings7.get_DisableRdpdr
- IMsRdpClientAdvancedSettings7.put_DisableRdpdr
- IMsRdpClientAdvancedSettings8.DisableRdpdr
- IMsRdpClientAdvancedSettings8.get_DisableRdpdr
- IMsRdpClientAdvancedSettings8.put_DisableRdpdr
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0747f37cd5e85c62946c9b8e3a1587f736dd8af9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106967547"
---
# <a name="imstscadvancedsettingsdisablerdpdr-property"></a><span data-ttu-id="02790-122">IMsTscAdvancedSettings：:D isableRdpdr 屬性</span><span class="sxs-lookup"><span data-stu-id="02790-122">IMsTscAdvancedSettings::DisableRdpdr property</span></span>

<span data-ttu-id="02790-123">指定是否啟用印表機和剪貼簿重新導向。</span><span class="sxs-lookup"><span data-stu-id="02790-123">Specifies whether printer and clipboard redirection is enabled.</span></span>

<span data-ttu-id="02790-124">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="02790-124">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="02790-125">Syntax</span><span class="sxs-lookup"><span data-stu-id="02790-125">Syntax</span></span>


```C++
HRESULT put_DisableRdpdr(
  [in]  BOOL DisableRdpdr
);

HRESULT get_DisableRdpdr(
  [out] BOOL *pDisableRdpdr
);
```



## <a name="property-value"></a><span data-ttu-id="02790-126">屬性值</span><span class="sxs-lookup"><span data-stu-id="02790-126">Property value</span></span>

<span data-ttu-id="02790-127">將此參數設定為 **TRUE** ，以停用重新導向或 **FALSE** 來啟用重新導向。</span><span class="sxs-lookup"><span data-stu-id="02790-127">Set this parameter to **TRUE** to disable redirection or **FALSE** to enable redirection.</span></span>

## <a name="error-codes"></a><span data-ttu-id="02790-128">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="02790-128">Error codes</span></span>

<span data-ttu-id="02790-129">如果成功，則傳回 **S \_ OK** 。</span><span class="sxs-lookup"><span data-stu-id="02790-129">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="02790-130">備註</span><span class="sxs-lookup"><span data-stu-id="02790-130">Remarks</span></span>

<span data-ttu-id="02790-131">如需遠端桌面網頁連線的詳細資訊，請參閱 [遠端桌面網頁連線的需求](requirements-for-remote-desktop-web-connection.md)。</span><span class="sxs-lookup"><span data-stu-id="02790-131">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="02790-132">規格需求</span><span class="sxs-lookup"><span data-stu-id="02790-132">Requirements</span></span>



| <span data-ttu-id="02790-133">需求</span><span class="sxs-lookup"><span data-stu-id="02790-133">Requirement</span></span> | <span data-ttu-id="02790-134">值</span><span class="sxs-lookup"><span data-stu-id="02790-134">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="02790-135">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="02790-135">Minimum supported client</span></span><br/> | <span data-ttu-id="02790-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="02790-136">Windows Vista</span></span><br/>                                                                  |
| <span data-ttu-id="02790-137">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="02790-137">Minimum supported server</span></span><br/> | <span data-ttu-id="02790-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="02790-138">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="02790-139">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="02790-139">Type library</span></span><br/>             | <dl> <span data-ttu-id="02790-140"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="02790-140"><dt>MsTscAx.dll</dt></span></span> </dl>    |
| <span data-ttu-id="02790-141">DLL</span><span class="sxs-lookup"><span data-stu-id="02790-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="02790-142"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="02790-142"><dt>MsTscAx.dll</dt></span></span> </dl>    |
| <span data-ttu-id="02790-143">IID</span><span class="sxs-lookup"><span data-stu-id="02790-143">IID</span></span><br/>                      | <span data-ttu-id="02790-144">IID \_ IMsTscAdvancedSettings 定義為809945cc-4b3b-4a92-a6b0-dbf9b5f2ef2d</span><span class="sxs-lookup"><span data-stu-id="02790-144">IID\_IMsTscAdvancedSettings is defined as 809945cc-4b3b-4a92-a6b0-dbf9b5f2ef2d</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="02790-145">另請參閱</span><span class="sxs-lookup"><span data-stu-id="02790-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="02790-146">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="02790-146">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="02790-147">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="02790-147">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="02790-148">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="02790-148">**IMsRdpClientAdvancedSettings3**</span></span>](imsrdpclientadvancedsettings3.md)
</dt> <dt>

[<span data-ttu-id="02790-149">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="02790-149">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="02790-150">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="02790-150">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="02790-151">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="02790-151">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="02790-152">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="02790-152">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="02790-153">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="02790-153">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="02790-154">**IMsTscAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="02790-154">**IMsTscAdvancedSettings**</span></span>](imstscadvancedsettings-interface.md)
</dt> </dl>

 

 





