---
title: IMsRdpClientAdvancedSettings DoubleClickDetect 屬性
description: 指定用戶端是否識別伺服器的按兩下。
ms.assetid: 39e76bef-3d12-406d-a074-8c084fbe9ccc
ms.tgt_platform: multiple
keywords:
- DoubleClickDetect 屬性遠端桌面服務
- DoubleClickDetect 屬性遠端桌面服務，IMsRdpClientAdvancedSettings 介面
- IMsRdpClientAdvancedSettings 介面遠端桌面服務，DoubleClickDetect 屬性
- DoubleClickDetect 屬性遠端桌面服務，IMsRdpClientAdvancedSettings2 介面
- IMsRdpClientAdvancedSettings2 介面遠端桌面服務，DoubleClickDetect 屬性
- DoubleClickDetect 屬性遠端桌面服務，IMsRdpClientAdvancedSettings3 介面
- IMsRdpClientAdvancedSettings3 介面遠端桌面服務，DoubleClickDetect 屬性
- DoubleClickDetect 屬性遠端桌面服務，IMsRdpClientAdvancedSettings4 介面
- IMsRdpClientAdvancedSettings4 介面遠端桌面服務，DoubleClickDetect 屬性
- DoubleClickDetect 屬性遠端桌面服務，IMsRdpClientAdvancedSettings5 介面
- IMsRdpClientAdvancedSettings5 介面遠端桌面服務，DoubleClickDetect 屬性
- DoubleClickDetect 屬性遠端桌面服務，IMsRdpClientAdvancedSettings6 介面
- IMsRdpClientAdvancedSettings6 介面遠端桌面服務，DoubleClickDetect 屬性
- DoubleClickDetect 屬性遠端桌面服務，IMsRdpClientAdvancedSettings7 介面
- IMsRdpClientAdvancedSettings7 介面遠端桌面服務，DoubleClickDetect 屬性
- DoubleClickDetect 屬性遠端桌面服務，IMsRdpClientAdvancedSettings8 介面
- IMsRdpClientAdvancedSettings8 介面遠端桌面服務，DoubleClickDetect 屬性
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.DoubleClickDetect
- IMsRdpClientAdvancedSettings.get_DoubleClickDetect
- IMsRdpClientAdvancedSettings.put_DoubleClickDetect
- IMsRdpClientAdvancedSettings2.DoubleClickDetect
- IMsRdpClientAdvancedSettings2.get_DoubleClickDetect
- IMsRdpClientAdvancedSettings2.put_DoubleClickDetect
- IMsRdpClientAdvancedSettings3.DoubleClickDetect
- IMsRdpClientAdvancedSettings3.get_DoubleClickDetect
- IMsRdpClientAdvancedSettings3.put_DoubleClickDetect
- IMsRdpClientAdvancedSettings4.DoubleClickDetect
- IMsRdpClientAdvancedSettings4.get_DoubleClickDetect
- IMsRdpClientAdvancedSettings4.put_DoubleClickDetect
- IMsRdpClientAdvancedSettings5.DoubleClickDetect
- IMsRdpClientAdvancedSettings5.get_DoubleClickDetect
- IMsRdpClientAdvancedSettings5.put_DoubleClickDetect
- IMsRdpClientAdvancedSettings6.DoubleClickDetect
- IMsRdpClientAdvancedSettings6.get_DoubleClickDetect
- IMsRdpClientAdvancedSettings6.put_DoubleClickDetect
- IMsRdpClientAdvancedSettings7.DoubleClickDetect
- IMsRdpClientAdvancedSettings7.get_DoubleClickDetect
- IMsRdpClientAdvancedSettings7.put_DoubleClickDetect
- IMsRdpClientAdvancedSettings8.DoubleClickDetect
- IMsRdpClientAdvancedSettings8.get_DoubleClickDetect
- IMsRdpClientAdvancedSettings8.put_DoubleClickDetect
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bd771614a80d909e0e7a748ab7256a5310084deb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105869"
---
# <a name="imsrdpclientadvancedsettingsdoubleclickdetect-property"></a><span data-ttu-id="57a36-120">IMsRdpClientAdvancedSettings：:D oubleClickDetect 屬性</span><span class="sxs-lookup"><span data-stu-id="57a36-120">IMsRdpClientAdvancedSettings::DoubleClickDetect property</span></span>

<span data-ttu-id="57a36-121">指定用戶端是否識別伺服器的按兩下。</span><span class="sxs-lookup"><span data-stu-id="57a36-121">Specifies if the client identifies double-clicks for the server.</span></span>

<span data-ttu-id="57a36-122">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="57a36-122">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="57a36-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="57a36-123">Syntax</span></span>


```C++
HRESULT put_DoubleClickDetect(
  [in]  LONG doubleClickDetect
);

HRESULT get_DoubleClickDetect(
  [out] LONG *pdoubleClickDetect
);
```



## <a name="property-value"></a><span data-ttu-id="57a36-124">屬性值</span><span class="sxs-lookup"><span data-stu-id="57a36-124">Property value</span></span>

<span data-ttu-id="57a36-125">將此參數設定為0，以停用此功能或非零值以啟用此功能。</span><span class="sxs-lookup"><span data-stu-id="57a36-125">Set this parameter to 0 to disable the feature or a nonzero value to enable the feature.</span></span>

## <a name="error-codes"></a><span data-ttu-id="57a36-126">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="57a36-126">Error codes</span></span>

<span data-ttu-id="57a36-127">如果成功，則傳回 **S \_ OK** 。</span><span class="sxs-lookup"><span data-stu-id="57a36-127">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="57a36-128">備註</span><span class="sxs-lookup"><span data-stu-id="57a36-128">Remarks</span></span>

<span data-ttu-id="57a36-129">如需遠端桌面網頁連線的詳細資訊，請參閱 [遠端桌面網頁連線的需求](requirements-for-remote-desktop-web-connection.md)。</span><span class="sxs-lookup"><span data-stu-id="57a36-129">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="57a36-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="57a36-130">Requirements</span></span>



| <span data-ttu-id="57a36-131">需求</span><span class="sxs-lookup"><span data-stu-id="57a36-131">Requirement</span></span> | <span data-ttu-id="57a36-132">值</span><span class="sxs-lookup"><span data-stu-id="57a36-132">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="57a36-133">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="57a36-133">Minimum supported client</span></span><br/> | <span data-ttu-id="57a36-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="57a36-134">Windows Vista</span></span><br/>                                                                        |
| <span data-ttu-id="57a36-135">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="57a36-135">Minimum supported server</span></span><br/> | <span data-ttu-id="57a36-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="57a36-136">Windows Server 2008</span></span><br/>                                                                  |
| <span data-ttu-id="57a36-137">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="57a36-137">Type library</span></span><br/>             | <dl> <span data-ttu-id="57a36-138"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="57a36-138"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="57a36-139">DLL</span><span class="sxs-lookup"><span data-stu-id="57a36-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="57a36-140"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="57a36-140"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="57a36-141">IID</span><span class="sxs-lookup"><span data-stu-id="57a36-141">IID</span></span><br/>                      | <span data-ttu-id="57a36-142">IID \_ IMsRdpClientAdvancedSettings 定義為3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span><span class="sxs-lookup"><span data-stu-id="57a36-142">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="57a36-143">另請參閱</span><span class="sxs-lookup"><span data-stu-id="57a36-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="57a36-144">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="57a36-144">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="57a36-145">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="57a36-145">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="57a36-146">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="57a36-146">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="57a36-147">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="57a36-147">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="57a36-148">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="57a36-148">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="57a36-149">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="57a36-149">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="57a36-150">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="57a36-150">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="57a36-151">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="57a36-151">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





