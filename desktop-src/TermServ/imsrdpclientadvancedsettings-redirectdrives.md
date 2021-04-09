---
title: IMsRdpClientAdvancedSettings RedirectDrives 屬性
description: 指定是否允許重新導向磁片磁碟機。
ms.assetid: 5ed4cd28-4a1f-4d3b-9f9d-bf44a8483209
ms.tgt_platform: multiple
keywords:
- RedirectDrives 屬性遠端桌面服務
- RedirectDrives 屬性遠端桌面服務，IMsRdpClientAdvancedSettings 介面
- IMsRdpClientAdvancedSettings 介面遠端桌面服務，RedirectDrives 屬性
- RedirectDrives 屬性遠端桌面服務，IMsRdpClientAdvancedSettings2 介面
- IMsRdpClientAdvancedSettings2 介面遠端桌面服務，RedirectDrives 屬性
- RedirectDrives 屬性遠端桌面服務，IMsRdpClientAdvancedSettings3 介面
- IMsRdpClientAdvancedSettings3 介面遠端桌面服務，RedirectDrives 屬性
- RedirectDrives 屬性遠端桌面服務，IMsRdpClientAdvancedSettings4 介面
- IMsRdpClientAdvancedSettings4 介面遠端桌面服務，RedirectDrives 屬性
- RedirectDrives 屬性遠端桌面服務，IMsRdpClientAdvancedSettings5 介面
- IMsRdpClientAdvancedSettings5 介面遠端桌面服務，RedirectDrives 屬性
- RedirectDrives 屬性遠端桌面服務，IMsRdpClientAdvancedSettings6 介面
- IMsRdpClientAdvancedSettings6 介面遠端桌面服務，RedirectDrives 屬性
- RedirectDrives 屬性遠端桌面服務，IMsRdpClientAdvancedSettings7 介面
- IMsRdpClientAdvancedSettings7 介面遠端桌面服務，RedirectDrives 屬性
- RedirectDrives 屬性遠端桌面服務，IMsRdpClientAdvancedSettings8 介面
- IMsRdpClientAdvancedSettings8 介面遠端桌面服務，RedirectDrives 屬性
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.RedirectDrives
- IMsRdpClientAdvancedSettings.get_RedirectDrives
- IMsRdpClientAdvancedSettings.put_RedirectDrives
- IMsRdpClientAdvancedSettings2.RedirectDrives
- IMsRdpClientAdvancedSettings2.get_RedirectDrives
- IMsRdpClientAdvancedSettings2.put_RedirectDrives
- IMsRdpClientAdvancedSettings3.RedirectDrives
- IMsRdpClientAdvancedSettings3.get_RedirectDrives
- IMsRdpClientAdvancedSettings3.put_RedirectDrives
- IMsRdpClientAdvancedSettings4.RedirectDrives
- IMsRdpClientAdvancedSettings4.get_RedirectDrives
- IMsRdpClientAdvancedSettings4.put_RedirectDrives
- IMsRdpClientAdvancedSettings5.RedirectDrives
- IMsRdpClientAdvancedSettings5.get_RedirectDrives
- IMsRdpClientAdvancedSettings5.put_RedirectDrives
- IMsRdpClientAdvancedSettings6.RedirectDrives
- IMsRdpClientAdvancedSettings6.get_RedirectDrives
- IMsRdpClientAdvancedSettings6.put_RedirectDrives
- IMsRdpClientAdvancedSettings7.RedirectDrives
- IMsRdpClientAdvancedSettings7.get_RedirectDrives
- IMsRdpClientAdvancedSettings7.put_RedirectDrives
- IMsRdpClientAdvancedSettings8.RedirectDrives
- IMsRdpClientAdvancedSettings8.get_RedirectDrives
- IMsRdpClientAdvancedSettings8.put_RedirectDrives
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c83d24ae4ea4dae2760c1e468f4fa8b326a94c38
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686504"
---
# <a name="imsrdpclientadvancedsettingsredirectdrives-property"></a><span data-ttu-id="b7545-120">IMsRdpClientAdvancedSettings：： RedirectDrives 屬性</span><span class="sxs-lookup"><span data-stu-id="b7545-120">IMsRdpClientAdvancedSettings::RedirectDrives property</span></span>

<span data-ttu-id="b7545-121">指定是否允許重新導向磁片磁碟機。</span><span class="sxs-lookup"><span data-stu-id="b7545-121">Specifies if redirection of disk drives is allowed.</span></span>

<span data-ttu-id="b7545-122">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="b7545-122">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="b7545-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="b7545-123">Syntax</span></span>


```C++
HRESULT put_RedirectDrives(
  [in]  VARIANT_BOOL redirectDrives
);

HRESULT get_RedirectDrives(
  [out] VARIANT_BOOL *predirectDrives
);
```



## <a name="property-value"></a><span data-ttu-id="b7545-124">屬性值</span><span class="sxs-lookup"><span data-stu-id="b7545-124">Property value</span></span>

<span data-ttu-id="b7545-125">請將此參數設定為 **VARIANT \_ TRUE** ，否則允許重新導向或 **VARIANT \_ FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="b7545-125">Set this parameter to **VARIANT\_TRUE** to allow redirection or **VARIANT\_FALSE** otherwise.</span></span> <span data-ttu-id="b7545-126">**變異 \_TRUE** 會提示使用者確認在連接時允許重新導向（基於安全性目的）。</span><span class="sxs-lookup"><span data-stu-id="b7545-126">**VARIANT\_TRUE** prompts the user to confirm allowing redirection at connection time, for security purposes.</span></span>

## <a name="error-codes"></a><span data-ttu-id="b7545-127">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="b7545-127">Error codes</span></span>

<span data-ttu-id="b7545-128">如果成功，則傳回 **S \_ OK** 。</span><span class="sxs-lookup"><span data-stu-id="b7545-128">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="b7545-129">備註</span><span class="sxs-lookup"><span data-stu-id="b7545-129">Remarks</span></span>

<span data-ttu-id="b7545-130">如需遠端桌面網頁連線的詳細資訊，請參閱 [遠端桌面網頁連線的需求](requirements-for-remote-desktop-web-connection.md)。</span><span class="sxs-lookup"><span data-stu-id="b7545-130">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b7545-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="b7545-131">Requirements</span></span>



| <span data-ttu-id="b7545-132">需求</span><span class="sxs-lookup"><span data-stu-id="b7545-132">Requirement</span></span> | <span data-ttu-id="b7545-133">值</span><span class="sxs-lookup"><span data-stu-id="b7545-133">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b7545-134">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b7545-134">Minimum supported client</span></span><br/> | <span data-ttu-id="b7545-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b7545-135">Windows Vista</span></span><br/>                                                                        |
| <span data-ttu-id="b7545-136">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b7545-136">Minimum supported server</span></span><br/> | <span data-ttu-id="b7545-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b7545-137">Windows Server 2008</span></span><br/>                                                                  |
| <span data-ttu-id="b7545-138">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="b7545-138">Type library</span></span><br/>             | <dl> <span data-ttu-id="b7545-139"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b7545-139"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="b7545-140">DLL</span><span class="sxs-lookup"><span data-stu-id="b7545-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b7545-141"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b7545-141"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="b7545-142">IID</span><span class="sxs-lookup"><span data-stu-id="b7545-142">IID</span></span><br/>                      | <span data-ttu-id="b7545-143">IID \_ IMsRdpClientAdvancedSettings 定義為3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span><span class="sxs-lookup"><span data-stu-id="b7545-143">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b7545-144">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b7545-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b7545-145">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="b7545-145">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="b7545-146">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="b7545-146">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="b7545-147">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="b7545-147">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="b7545-148">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="b7545-148">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="b7545-149">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="b7545-149">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="b7545-150">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="b7545-150">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="b7545-151">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="b7545-151">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="b7545-152">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="b7545-152">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





