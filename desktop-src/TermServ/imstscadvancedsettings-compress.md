---
title: IMsTscAdvancedSettings 壓縮屬性
description: 指定是否啟用壓縮。
ms.assetid: 274774b3-0442-4a46-95f8-7857f885bfdb
ms.tgt_platform: multiple
keywords:
- 壓縮屬性遠端桌面服務
- 壓縮屬性遠端桌面服務，IMsTscAdvancedSettings 介面
- IMsTscAdvancedSettings 介面遠端桌面服務、壓縮屬性
- 壓縮屬性遠端桌面服務，IMsRdpClientAdvancedSettings 介面
- IMsRdpClientAdvancedSettings 介面遠端桌面服務、壓縮屬性
- 壓縮屬性遠端桌面服務，IMsRdpClientAdvancedSettings2 介面
- IMsRdpClientAdvancedSettings2 介面遠端桌面服務、壓縮屬性
- 壓縮屬性遠端桌面服務，IMsRdpClientAdvancedSettings3 介面
- IMsRdpClientAdvancedSettings3 介面遠端桌面服務、壓縮屬性
- 壓縮屬性遠端桌面服務，IMsRdpClientAdvancedSettings4 介面
- IMsRdpClientAdvancedSettings4 介面遠端桌面服務、壓縮屬性
- 壓縮屬性遠端桌面服務，IMsRdpClientAdvancedSettings5 介面
- IMsRdpClientAdvancedSettings5 介面遠端桌面服務、壓縮屬性
- 壓縮屬性遠端桌面服務，IMsRdpClientAdvancedSettings6 介面
- IMsRdpClientAdvancedSettings6 介面遠端桌面服務、壓縮屬性
- 壓縮屬性遠端桌面服務，IMsRdpClientAdvancedSettings7 介面
- IMsRdpClientAdvancedSettings7 介面遠端桌面服務、壓縮屬性
- 壓縮屬性遠端桌面服務，IMsRdpClientAdvancedSettings8 介面
- IMsRdpClientAdvancedSettings8 介面遠端桌面服務、壓縮屬性
topic_type:
- apiref
api_name:
- IMsTscAdvancedSettings.Compress
- IMsTscAdvancedSettings.get_Compress
- IMsTscAdvancedSettings.put_Compress
- IMsRdpClientAdvancedSettings.Compress
- IMsRdpClientAdvancedSettings.get_Compress
- IMsRdpClientAdvancedSettings.put_Compress
- IMsRdpClientAdvancedSettings2.Compress
- IMsRdpClientAdvancedSettings2.get_Compress
- IMsRdpClientAdvancedSettings2.put_Compress
- IMsRdpClientAdvancedSettings3.Compress
- IMsRdpClientAdvancedSettings3.get_Compress
- IMsRdpClientAdvancedSettings3.put_Compress
- IMsRdpClientAdvancedSettings4.Compress
- IMsRdpClientAdvancedSettings4.get_Compress
- IMsRdpClientAdvancedSettings4.put_Compress
- IMsRdpClientAdvancedSettings5.Compress
- IMsRdpClientAdvancedSettings5.get_Compress
- IMsRdpClientAdvancedSettings5.put_Compress
- IMsRdpClientAdvancedSettings6.Compress
- IMsRdpClientAdvancedSettings6.get_Compress
- IMsRdpClientAdvancedSettings6.put_Compress
- IMsRdpClientAdvancedSettings7.Compress
- IMsRdpClientAdvancedSettings7.get_Compress
- IMsRdpClientAdvancedSettings7.put_Compress
- IMsRdpClientAdvancedSettings8.Compress
- IMsRdpClientAdvancedSettings8.get_Compress
- IMsRdpClientAdvancedSettings8.put_Compress
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c588784d9b06bd2e8e1605a96c8aa9fd157c10eb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934578"
---
# <a name="imstscadvancedsettingscompress-property"></a><span data-ttu-id="f953d-122">IMsTscAdvancedSettings：：壓縮屬性</span><span class="sxs-lookup"><span data-stu-id="f953d-122">IMsTscAdvancedSettings::Compress property</span></span>

<span data-ttu-id="f953d-123">指定是否啟用壓縮。</span><span class="sxs-lookup"><span data-stu-id="f953d-123">Specifies whether compression is enabled.</span></span>

<span data-ttu-id="f953d-124">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="f953d-124">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="f953d-125">Syntax</span><span class="sxs-lookup"><span data-stu-id="f953d-125">Syntax</span></span>


```C++
HRESULT put_Compress(
  [in]  LONG compress
);

HRESULT get_Compress(
  [out] LONG *pcompress
);
```



## <a name="property-value"></a><span data-ttu-id="f953d-126">屬性值</span><span class="sxs-lookup"><span data-stu-id="f953d-126">Property value</span></span>

<span data-ttu-id="f953d-127">將此參數設定為0，以停用壓縮或非零值以啟用壓縮。</span><span class="sxs-lookup"><span data-stu-id="f953d-127">Set this parameter to 0 to disable compression or a nonzero value to enable compression.</span></span>

## <a name="error-codes"></a><span data-ttu-id="f953d-128">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="f953d-128">Error codes</span></span>

<span data-ttu-id="f953d-129">如果成功，則傳回 **S \_ OK** 。</span><span class="sxs-lookup"><span data-stu-id="f953d-129">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="f953d-130">備註</span><span class="sxs-lookup"><span data-stu-id="f953d-130">Remarks</span></span>

<span data-ttu-id="f953d-131">如需遠端桌面網頁連線的詳細資訊，請參閱 [遠端桌面網頁連線的需求](requirements-for-remote-desktop-web-connection.md)。</span><span class="sxs-lookup"><span data-stu-id="f953d-131">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f953d-132">規格需求</span><span class="sxs-lookup"><span data-stu-id="f953d-132">Requirements</span></span>



| <span data-ttu-id="f953d-133">需求</span><span class="sxs-lookup"><span data-stu-id="f953d-133">Requirement</span></span> | <span data-ttu-id="f953d-134">值</span><span class="sxs-lookup"><span data-stu-id="f953d-134">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="f953d-135">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f953d-135">Minimum supported client</span></span><br/> | <span data-ttu-id="f953d-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f953d-136">Windows Vista</span></span><br/>                                                                  |
| <span data-ttu-id="f953d-137">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f953d-137">Minimum supported server</span></span><br/> | <span data-ttu-id="f953d-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f953d-138">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="f953d-139">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="f953d-139">Type library</span></span><br/>             | <dl> <span data-ttu-id="f953d-140"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f953d-140"><dt>MsTscAx.dll</dt></span></span> </dl>    |
| <span data-ttu-id="f953d-141">DLL</span><span class="sxs-lookup"><span data-stu-id="f953d-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f953d-142"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f953d-142"><dt>MsTscAx.dll</dt></span></span> </dl>    |
| <span data-ttu-id="f953d-143">IID</span><span class="sxs-lookup"><span data-stu-id="f953d-143">IID</span></span><br/>                      | <span data-ttu-id="f953d-144">IID \_ IMsTscAdvancedSettings 定義為809945cc-4b3b-4a92-a6b0-dbf9b5f2ef2d</span><span class="sxs-lookup"><span data-stu-id="f953d-144">IID\_IMsTscAdvancedSettings is defined as 809945cc-4b3b-4a92-a6b0-dbf9b5f2ef2d</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f953d-145">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f953d-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f953d-146">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="f953d-146">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="f953d-147">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="f953d-147">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="f953d-148">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="f953d-148">**IMsRdpClientAdvancedSettings3**</span></span>](imsrdpclientadvancedsettings3.md)
</dt> <dt>

[<span data-ttu-id="f953d-149">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="f953d-149">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="f953d-150">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="f953d-150">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="f953d-151">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="f953d-151">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="f953d-152">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="f953d-152">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="f953d-153">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="f953d-153">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="f953d-154">**IMsTscAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="f953d-154">**IMsTscAdvancedSettings**</span></span>](imstscadvancedsettings-interface.md)
</dt> </dl>

 

 





