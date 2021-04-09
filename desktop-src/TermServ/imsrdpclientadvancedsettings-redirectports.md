---
title: IMsRdpClientAdvancedSettings RedirectPorts 屬性
description: 指定是否允許重新導向本機埠 (例如，COM 和 LPT) 。
ms.assetid: 85e1e40d-8da7-4333-ae96-2bfa44479267
ms.tgt_platform: multiple
keywords:
- RedirectPorts 屬性遠端桌面服務
- RedirectPorts 屬性遠端桌面服務，IMsRdpClientAdvancedSettings 介面
- IMsRdpClientAdvancedSettings 介面遠端桌面服務，RedirectPorts 屬性
- RedirectPorts 屬性遠端桌面服務，IMsRdpClientAdvancedSettings2 介面
- IMsRdpClientAdvancedSettings2 介面遠端桌面服務，RedirectPorts 屬性
- RedirectPorts 屬性遠端桌面服務，IMsRdpClientAdvancedSettings3 介面
- IMsRdpClientAdvancedSettings3 介面遠端桌面服務，RedirectPorts 屬性
- RedirectPorts 屬性遠端桌面服務，IMsRdpClientAdvancedSettings4 介面
- IMsRdpClientAdvancedSettings4 介面遠端桌面服務，RedirectPorts 屬性
- RedirectPorts 屬性遠端桌面服務，IMsRdpClientAdvancedSettings5 介面
- IMsRdpClientAdvancedSettings5 介面遠端桌面服務，RedirectPorts 屬性
- RedirectPorts 屬性遠端桌面服務，IMsRdpClientAdvancedSettings6 介面
- IMsRdpClientAdvancedSettings6 介面遠端桌面服務，RedirectPorts 屬性
- RedirectPorts 屬性遠端桌面服務，IMsRdpClientAdvancedSettings7 介面
- IMsRdpClientAdvancedSettings7 介面遠端桌面服務，RedirectPorts 屬性
- RedirectPorts 屬性遠端桌面服務，IMsRdpClientAdvancedSettings8 介面
- IMsRdpClientAdvancedSettings8 介面遠端桌面服務，RedirectPorts 屬性
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.RedirectPorts
- IMsRdpClientAdvancedSettings.get_RedirectPorts
- IMsRdpClientAdvancedSettings.put_RedirectPorts
- IMsRdpClientAdvancedSettings2.RedirectPorts
- IMsRdpClientAdvancedSettings2.get_RedirectPorts
- IMsRdpClientAdvancedSettings2.put_RedirectPorts
- IMsRdpClientAdvancedSettings3.RedirectPorts
- IMsRdpClientAdvancedSettings3.get_RedirectPorts
- IMsRdpClientAdvancedSettings3.put_RedirectPorts
- IMsRdpClientAdvancedSettings4.RedirectPorts
- IMsRdpClientAdvancedSettings4.get_RedirectPorts
- IMsRdpClientAdvancedSettings4.put_RedirectPorts
- IMsRdpClientAdvancedSettings5.RedirectPorts
- IMsRdpClientAdvancedSettings5.get_RedirectPorts
- IMsRdpClientAdvancedSettings5.put_RedirectPorts
- IMsRdpClientAdvancedSettings6.RedirectPorts
- IMsRdpClientAdvancedSettings6.get_RedirectPorts
- IMsRdpClientAdvancedSettings6.put_RedirectPorts
- IMsRdpClientAdvancedSettings7.RedirectPorts
- IMsRdpClientAdvancedSettings7.get_RedirectPorts
- IMsRdpClientAdvancedSettings7.put_RedirectPorts
- IMsRdpClientAdvancedSettings8.RedirectPorts
- IMsRdpClientAdvancedSettings8.get_RedirectPorts
- IMsRdpClientAdvancedSettings8.put_RedirectPorts
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 714b26081bb4caadface283553b1dd3ebd91192d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103933931"
---
# <a name="imsrdpclientadvancedsettingsredirectports-property"></a><span data-ttu-id="fce22-120">IMsRdpClientAdvancedSettings：： RedirectPorts 屬性</span><span class="sxs-lookup"><span data-stu-id="fce22-120">IMsRdpClientAdvancedSettings::RedirectPorts property</span></span>

<span data-ttu-id="fce22-121">指定是否允許重新導向本機埠 (例如，COM 和 LPT) 。</span><span class="sxs-lookup"><span data-stu-id="fce22-121">Specifies if redirection of local ports (for example, COM and LPT) is allowed.</span></span>

<span data-ttu-id="fce22-122">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="fce22-122">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="fce22-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="fce22-123">Syntax</span></span>


```C++
HRESULT put_RedirectPorts(
  [in]  VARIANT_BOOL redirectPorts
);

HRESULT get_RedirectPorts(
  [out] VARIANT_BOOL *predirectPorts
);
```



## <a name="property-value"></a><span data-ttu-id="fce22-124">屬性值</span><span class="sxs-lookup"><span data-stu-id="fce22-124">Property value</span></span>

<span data-ttu-id="fce22-125">請將此參數設定為 **VARIANT \_ TRUE** ，否則允許重新導向或 **VARIANT \_ FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="fce22-125">Set this parameter to **VARIANT\_TRUE** to allow redirection or **VARIANT\_FALSE** otherwise.</span></span> <span data-ttu-id="fce22-126">**變異 \_TRUE** 會提示使用者確認在連接時允許重新導向（基於安全性目的）。</span><span class="sxs-lookup"><span data-stu-id="fce22-126">**VARIANT\_TRUE** prompts the user to confirm allowing redirection at connection time, for security purposes.</span></span>

## <a name="error-codes"></a><span data-ttu-id="fce22-127">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="fce22-127">Error codes</span></span>

<span data-ttu-id="fce22-128">如果成功，則傳回 **S \_ OK** 。</span><span class="sxs-lookup"><span data-stu-id="fce22-128">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="fce22-129">備註</span><span class="sxs-lookup"><span data-stu-id="fce22-129">Remarks</span></span>

<span data-ttu-id="fce22-130">如需遠端桌面網頁連線的詳細資訊，請參閱 [遠端桌面網頁連線的需求](requirements-for-remote-desktop-web-connection.md)。</span><span class="sxs-lookup"><span data-stu-id="fce22-130">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="fce22-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="fce22-131">Requirements</span></span>



| <span data-ttu-id="fce22-132">需求</span><span class="sxs-lookup"><span data-stu-id="fce22-132">Requirement</span></span> | <span data-ttu-id="fce22-133">值</span><span class="sxs-lookup"><span data-stu-id="fce22-133">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fce22-134">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="fce22-134">Minimum supported client</span></span><br/> | <span data-ttu-id="fce22-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="fce22-135">Windows Vista</span></span><br/>                                                                        |
| <span data-ttu-id="fce22-136">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="fce22-136">Minimum supported server</span></span><br/> | <span data-ttu-id="fce22-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fce22-137">Windows Server 2008</span></span><br/>                                                                  |
| <span data-ttu-id="fce22-138">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="fce22-138">Type library</span></span><br/>             | <dl> <span data-ttu-id="fce22-139"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fce22-139"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="fce22-140">DLL</span><span class="sxs-lookup"><span data-stu-id="fce22-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fce22-141"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fce22-141"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="fce22-142">IID</span><span class="sxs-lookup"><span data-stu-id="fce22-142">IID</span></span><br/>                      | <span data-ttu-id="fce22-143">IID \_ IMsRdpClientAdvancedSettings 定義為3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span><span class="sxs-lookup"><span data-stu-id="fce22-143">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="fce22-144">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fce22-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fce22-145">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="fce22-145">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="fce22-146">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="fce22-146">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="fce22-147">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="fce22-147">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="fce22-148">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="fce22-148">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="fce22-149">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="fce22-149">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="fce22-150">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="fce22-150">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="fce22-151">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="fce22-151">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="fce22-152">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="fce22-152">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





