---
title: IMsRdpClientAdvancedSettings RedirectPrinters 屬性
description: 指定是否允許印表機的重新導向。
ms.assetid: 7d4f28a7-a99d-4d0b-ab51-832a78881900
ms.tgt_platform: multiple
keywords:
- RedirectPrinters 屬性遠端桌面服務
- RedirectPrinters 屬性遠端桌面服務，IMsRdpClientAdvancedSettings 介面
- IMsRdpClientAdvancedSettings 介面遠端桌面服務，RedirectPrinters 屬性
- RedirectPrinters 屬性遠端桌面服務，IMsRdpClientAdvancedSettings2 介面
- IMsRdpClientAdvancedSettings2 介面遠端桌面服務，RedirectPrinters 屬性
- RedirectPrinters 屬性遠端桌面服務，IMsRdpClientAdvancedSettings3 介面
- IMsRdpClientAdvancedSettings3 介面遠端桌面服務，RedirectPrinters 屬性
- RedirectPrinters 屬性遠端桌面服務，IMsRdpClientAdvancedSettings4 介面
- IMsRdpClientAdvancedSettings4 介面遠端桌面服務，RedirectPrinters 屬性
- RedirectPrinters 屬性遠端桌面服務，IMsRdpClientAdvancedSettings5 介面
- IMsRdpClientAdvancedSettings5 介面遠端桌面服務，RedirectPrinters 屬性
- RedirectPrinters 屬性遠端桌面服務，IMsRdpClientAdvancedSettings6 介面
- IMsRdpClientAdvancedSettings6 介面遠端桌面服務，RedirectPrinters 屬性
- RedirectPrinters 屬性遠端桌面服務，IMsRdpClientAdvancedSettings7 介面
- IMsRdpClientAdvancedSettings7 介面遠端桌面服務，RedirectPrinters 屬性
- RedirectPrinters 屬性遠端桌面服務，IMsRdpClientAdvancedSettings8 介面
- IMsRdpClientAdvancedSettings8 介面遠端桌面服務，RedirectPrinters 屬性
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.RedirectPrinters
- IMsRdpClientAdvancedSettings.get_RedirectPrinters
- IMsRdpClientAdvancedSettings.put_RedirectPrinters
- IMsRdpClientAdvancedSettings2.RedirectPrinters
- IMsRdpClientAdvancedSettings2.get_RedirectPrinters
- IMsRdpClientAdvancedSettings2.put_RedirectPrinters
- IMsRdpClientAdvancedSettings3.RedirectPrinters
- IMsRdpClientAdvancedSettings3.get_RedirectPrinters
- IMsRdpClientAdvancedSettings3.put_RedirectPrinters
- IMsRdpClientAdvancedSettings4.RedirectPrinters
- IMsRdpClientAdvancedSettings4.get_RedirectPrinters
- IMsRdpClientAdvancedSettings4.put_RedirectPrinters
- IMsRdpClientAdvancedSettings5.RedirectPrinters
- IMsRdpClientAdvancedSettings5.get_RedirectPrinters
- IMsRdpClientAdvancedSettings5.put_RedirectPrinters
- IMsRdpClientAdvancedSettings6.RedirectPrinters
- IMsRdpClientAdvancedSettings6.get_RedirectPrinters
- IMsRdpClientAdvancedSettings6.put_RedirectPrinters
- IMsRdpClientAdvancedSettings7.RedirectPrinters
- IMsRdpClientAdvancedSettings7.get_RedirectPrinters
- IMsRdpClientAdvancedSettings7.put_RedirectPrinters
- IMsRdpClientAdvancedSettings8.RedirectPrinters
- IMsRdpClientAdvancedSettings8.get_RedirectPrinters
- IMsRdpClientAdvancedSettings8.put_RedirectPrinters
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94fecc3b6f72b8706168c75d220d78fc49340752
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685538"
---
# <a name="imsrdpclientadvancedsettingsredirectprinters-property"></a><span data-ttu-id="676b9-120">IMsRdpClientAdvancedSettings：： RedirectPrinters 屬性</span><span class="sxs-lookup"><span data-stu-id="676b9-120">IMsRdpClientAdvancedSettings::RedirectPrinters property</span></span>

<span data-ttu-id="676b9-121">指定是否允許印表機的重新導向。</span><span class="sxs-lookup"><span data-stu-id="676b9-121">Specifies if redirection of printers is allowed.</span></span>

<span data-ttu-id="676b9-122">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="676b9-122">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="676b9-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="676b9-123">Syntax</span></span>


```C++
HRESULT put_RedirectPrinters(
  [in]  VARIANT_BOOL redirectPrinters
);

HRESULT get_RedirectPrinters(
  [out] VARIANT_BOOL *predirectPrinters
);
```



## <a name="property-value"></a><span data-ttu-id="676b9-124">屬性值</span><span class="sxs-lookup"><span data-stu-id="676b9-124">Property value</span></span>

<span data-ttu-id="676b9-125">請將此參數設定為 **VARIANT \_ TRUE** ，否則允許重新導向或 **VARIANT \_ FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="676b9-125">Set this parameter to **VARIANT\_TRUE** to allow redirection or **VARIANT\_FALSE** otherwise.</span></span>

## <a name="error-codes"></a><span data-ttu-id="676b9-126">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="676b9-126">Error codes</span></span>

<span data-ttu-id="676b9-127">如果成功，則傳回 **S \_ OK** 。</span><span class="sxs-lookup"><span data-stu-id="676b9-127">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="676b9-128">備註</span><span class="sxs-lookup"><span data-stu-id="676b9-128">Remarks</span></span>

<span data-ttu-id="676b9-129">如需遠端桌面網頁連線的詳細資訊，請參閱 [遠端桌面網頁連線的需求](requirements-for-remote-desktop-web-connection.md)。</span><span class="sxs-lookup"><span data-stu-id="676b9-129">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="676b9-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="676b9-130">Requirements</span></span>



| <span data-ttu-id="676b9-131">需求</span><span class="sxs-lookup"><span data-stu-id="676b9-131">Requirement</span></span> | <span data-ttu-id="676b9-132">值</span><span class="sxs-lookup"><span data-stu-id="676b9-132">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="676b9-133">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="676b9-133">Minimum supported client</span></span><br/> | <span data-ttu-id="676b9-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="676b9-134">Windows Vista</span></span><br/>                                                                        |
| <span data-ttu-id="676b9-135">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="676b9-135">Minimum supported server</span></span><br/> | <span data-ttu-id="676b9-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="676b9-136">Windows Server 2008</span></span><br/>                                                                  |
| <span data-ttu-id="676b9-137">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="676b9-137">Type library</span></span><br/>             | <dl> <span data-ttu-id="676b9-138"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="676b9-138"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="676b9-139">DLL</span><span class="sxs-lookup"><span data-stu-id="676b9-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="676b9-140"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="676b9-140"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="676b9-141">IID</span><span class="sxs-lookup"><span data-stu-id="676b9-141">IID</span></span><br/>                      | <span data-ttu-id="676b9-142">IID \_ IMsRdpClientAdvancedSettings 定義為3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span><span class="sxs-lookup"><span data-stu-id="676b9-142">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="676b9-143">另請參閱</span><span class="sxs-lookup"><span data-stu-id="676b9-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="676b9-144">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="676b9-144">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="676b9-145">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="676b9-145">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="676b9-146">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="676b9-146">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="676b9-147">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="676b9-147">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="676b9-148">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="676b9-148">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="676b9-149">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="676b9-149">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="676b9-150">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="676b9-150">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="676b9-151">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="676b9-151">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





