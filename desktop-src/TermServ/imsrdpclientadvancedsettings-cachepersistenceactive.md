---
title: IMsRdpClientAdvancedSettings CachePersistenceActive 屬性
description: 指定是否應該使用持續性點陣圖快取。 持續性快取可以改善效能，但需要額外的磁碟空間。
ms.assetid: 5eb986c4-98dd-426f-8d55-d3a9a526e1b2
ms.tgt_platform: multiple
keywords:
- CachePersistenceActive 屬性遠端桌面服務
- CachePersistenceActive 屬性遠端桌面服務，IMsRdpClientAdvancedSettings 介面
- IMsRdpClientAdvancedSettings 介面遠端桌面服務，CachePersistenceActive 屬性
- CachePersistenceActive 屬性遠端桌面服務，IMsRdpClientAdvancedSettings2 介面
- IMsRdpClientAdvancedSettings2 介面遠端桌面服務，CachePersistenceActive 屬性
- CachePersistenceActive 屬性遠端桌面服務，IMsRdpClientAdvancedSettings3 介面
- IMsRdpClientAdvancedSettings3 介面遠端桌面服務，CachePersistenceActive 屬性
- CachePersistenceActive 屬性遠端桌面服務，IMsRdpClientAdvancedSettings4 介面
- IMsRdpClientAdvancedSettings4 介面遠端桌面服務，CachePersistenceActive 屬性
- CachePersistenceActive 屬性遠端桌面服務，IMsRdpClientAdvancedSettings5 介面
- IMsRdpClientAdvancedSettings5 介面遠端桌面服務，CachePersistenceActive 屬性
- CachePersistenceActive 屬性遠端桌面服務，IMsRdpClientAdvancedSettings6 介面
- IMsRdpClientAdvancedSettings6 介面遠端桌面服務，CachePersistenceActive 屬性
- CachePersistenceActive 屬性遠端桌面服務，IMsRdpClientAdvancedSettings7 介面
- IMsRdpClientAdvancedSettings7 介面遠端桌面服務，CachePersistenceActive 屬性
- CachePersistenceActive 屬性遠端桌面服務，IMsRdpClientAdvancedSettings8 介面
- IMsRdpClientAdvancedSettings8 介面遠端桌面服務，CachePersistenceActive 屬性
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.CachePersistenceActive
- IMsRdpClientAdvancedSettings.get_CachePersistenceActive
- IMsRdpClientAdvancedSettings.put_CachePersistenceActive
- IMsRdpClientAdvancedSettings2.CachePersistenceActive
- IMsRdpClientAdvancedSettings2.get_CachePersistenceActive
- IMsRdpClientAdvancedSettings2.put_CachePersistenceActive
- IMsRdpClientAdvancedSettings3.CachePersistenceActive
- IMsRdpClientAdvancedSettings3.get_CachePersistenceActive
- IMsRdpClientAdvancedSettings3.put_CachePersistenceActive
- IMsRdpClientAdvancedSettings4.CachePersistenceActive
- IMsRdpClientAdvancedSettings4.get_CachePersistenceActive
- IMsRdpClientAdvancedSettings4.put_CachePersistenceActive
- IMsRdpClientAdvancedSettings5.CachePersistenceActive
- IMsRdpClientAdvancedSettings5.get_CachePersistenceActive
- IMsRdpClientAdvancedSettings5.put_CachePersistenceActive
- IMsRdpClientAdvancedSettings6.CachePersistenceActive
- IMsRdpClientAdvancedSettings6.get_CachePersistenceActive
- IMsRdpClientAdvancedSettings6.put_CachePersistenceActive
- IMsRdpClientAdvancedSettings7.CachePersistenceActive
- IMsRdpClientAdvancedSettings7.get_CachePersistenceActive
- IMsRdpClientAdvancedSettings7.put_CachePersistenceActive
- IMsRdpClientAdvancedSettings8.CachePersistenceActive
- IMsRdpClientAdvancedSettings8.get_CachePersistenceActive
- IMsRdpClientAdvancedSettings8.put_CachePersistenceActive
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb34e90cc028e95c750a444d53f42c9c0ab77400
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106965947"
---
# <a name="imsrdpclientadvancedsettingscachepersistenceactive-property"></a><span data-ttu-id="9ca23-121">IMsRdpClientAdvancedSettings：： CachePersistenceActive 屬性</span><span class="sxs-lookup"><span data-stu-id="9ca23-121">IMsRdpClientAdvancedSettings::CachePersistenceActive property</span></span>

<span data-ttu-id="9ca23-122">指定是否應該使用持續性點陣圖快取。</span><span class="sxs-lookup"><span data-stu-id="9ca23-122">Specifies whether persistent bitmap caching should be used.</span></span> <span data-ttu-id="9ca23-123">持續性快取可以改善效能，但需要額外的磁碟空間。</span><span class="sxs-lookup"><span data-stu-id="9ca23-123">Persistent caching can improve performance but requires additional disk space.</span></span>

<span data-ttu-id="9ca23-124">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="9ca23-124">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="9ca23-125">Syntax</span><span class="sxs-lookup"><span data-stu-id="9ca23-125">Syntax</span></span>


```C++
HRESULT put_CachePersistenceActive(
  [in]  LONG cachePersistenceActive
);

HRESULT get_CachePersistenceActive(
  [out] LONG *pcachePersistenceActive
);
```



## <a name="property-value"></a><span data-ttu-id="9ca23-126">屬性值</span><span class="sxs-lookup"><span data-stu-id="9ca23-126">Property value</span></span>

<span data-ttu-id="9ca23-127">將此參數設定為0，以停用此功能或非零值以啟用此功能。</span><span class="sxs-lookup"><span data-stu-id="9ca23-127">Set this parameter to 0 to disable the feature or a nonzero value to enable the feature.</span></span>

## <a name="error-codes"></a><span data-ttu-id="9ca23-128">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="9ca23-128">Error codes</span></span>

<span data-ttu-id="9ca23-129">如果成功，則傳回 **S \_ OK** 。</span><span class="sxs-lookup"><span data-stu-id="9ca23-129">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="9ca23-130">備註</span><span class="sxs-lookup"><span data-stu-id="9ca23-130">Remarks</span></span>

<span data-ttu-id="9ca23-131">如需遠端桌面網頁連線的詳細資訊，請參閱 [遠端桌面網頁連線的需求](requirements-for-remote-desktop-web-connection.md)。</span><span class="sxs-lookup"><span data-stu-id="9ca23-131">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="9ca23-132">規格需求</span><span class="sxs-lookup"><span data-stu-id="9ca23-132">Requirements</span></span>



| <span data-ttu-id="9ca23-133">需求</span><span class="sxs-lookup"><span data-stu-id="9ca23-133">Requirement</span></span> | <span data-ttu-id="9ca23-134">值</span><span class="sxs-lookup"><span data-stu-id="9ca23-134">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9ca23-135">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9ca23-135">Minimum supported client</span></span><br/> | <span data-ttu-id="9ca23-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9ca23-136">Windows Vista</span></span><br/>                                                                        |
| <span data-ttu-id="9ca23-137">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9ca23-137">Minimum supported server</span></span><br/> | <span data-ttu-id="9ca23-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9ca23-138">Windows Server 2008</span></span><br/>                                                                  |
| <span data-ttu-id="9ca23-139">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="9ca23-139">Type library</span></span><br/>             | <dl> <span data-ttu-id="9ca23-140"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9ca23-140"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="9ca23-141">DLL</span><span class="sxs-lookup"><span data-stu-id="9ca23-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9ca23-142"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9ca23-142"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="9ca23-143">IID</span><span class="sxs-lookup"><span data-stu-id="9ca23-143">IID</span></span><br/>                      | <span data-ttu-id="9ca23-144">IID \_ IMsRdpClientAdvancedSettings 定義為3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span><span class="sxs-lookup"><span data-stu-id="9ca23-144">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="9ca23-145">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9ca23-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9ca23-146">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="9ca23-146">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="9ca23-147">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="9ca23-147">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="9ca23-148">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="9ca23-148">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="9ca23-149">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="9ca23-149">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="9ca23-150">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="9ca23-150">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="9ca23-151">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="9ca23-151">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="9ca23-152">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="9ca23-152">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="9ca23-153">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="9ca23-153">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





