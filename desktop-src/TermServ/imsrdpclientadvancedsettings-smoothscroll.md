---
title: IMsRdpClientAdvancedSettings SmoothScroll 屬性
description: 不支援這個屬性。 |IMsRdpClientAdvancedSettings SmoothScroll 屬性
ms.assetid: 7f1ce439-0b6e-4426-8dd6-3748509130e1
ms.tgt_platform: multiple
keywords:
- SmoothScroll 屬性遠端桌面服務
- SmoothScroll 屬性遠端桌面服務，IMsRdpClientAdvancedSettings 介面
- IMsRdpClientAdvancedSettings 介面遠端桌面服務，SmoothScroll 屬性
- SmoothScroll 屬性遠端桌面服務，IMsRdpClientAdvancedSettings2 介面
- IMsRdpClientAdvancedSettings2 介面遠端桌面服務，SmoothScroll 屬性
- SmoothScroll 屬性遠端桌面服務，IMsRdpClientAdvancedSettings3 介面
- IMsRdpClientAdvancedSettings3 介面遠端桌面服務，SmoothScroll 屬性
- SmoothScroll 屬性遠端桌面服務，IMsRdpClientAdvancedSettings4 介面
- IMsRdpClientAdvancedSettings4 介面遠端桌面服務，SmoothScroll 屬性
- SmoothScroll 屬性遠端桌面服務，IMsRdpClientAdvancedSettings5 介面
- IMsRdpClientAdvancedSettings5 介面遠端桌面服務，SmoothScroll 屬性
- SmoothScroll 屬性遠端桌面服務，IMsRdpClientAdvancedSettings6 介面
- IMsRdpClientAdvancedSettings6 介面遠端桌面服務，SmoothScroll 屬性
- SmoothScroll 屬性遠端桌面服務，IMsRdpClientAdvancedSettings7 介面
- IMsRdpClientAdvancedSettings7 介面遠端桌面服務，SmoothScroll 屬性
- SmoothScroll 屬性遠端桌面服務，IMsRdpClientAdvancedSettings8 介面
- IMsRdpClientAdvancedSettings8 介面遠端桌面服務，SmoothScroll 屬性
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.SmoothScroll
- IMsRdpClientAdvancedSettings.get_SmoothScroll
- IMsRdpClientAdvancedSettings.put_SmoothScroll
- IMsRdpClientAdvancedSettings2.SmoothScroll
- IMsRdpClientAdvancedSettings2.get_SmoothScroll
- IMsRdpClientAdvancedSettings2.put_SmoothScroll
- IMsRdpClientAdvancedSettings3.SmoothScroll
- IMsRdpClientAdvancedSettings3.get_SmoothScroll
- IMsRdpClientAdvancedSettings3.put_SmoothScroll
- IMsRdpClientAdvancedSettings4.SmoothScroll
- IMsRdpClientAdvancedSettings4.get_SmoothScroll
- IMsRdpClientAdvancedSettings4.put_SmoothScroll
- IMsRdpClientAdvancedSettings5.SmoothScroll
- IMsRdpClientAdvancedSettings5.get_SmoothScroll
- IMsRdpClientAdvancedSettings5.put_SmoothScroll
- IMsRdpClientAdvancedSettings6.SmoothScroll
- IMsRdpClientAdvancedSettings6.get_SmoothScroll
- IMsRdpClientAdvancedSettings6.put_SmoothScroll
- IMsRdpClientAdvancedSettings7.SmoothScroll
- IMsRdpClientAdvancedSettings7.get_SmoothScroll
- IMsRdpClientAdvancedSettings7.put_SmoothScroll
- IMsRdpClientAdvancedSettings8.SmoothScroll
- IMsRdpClientAdvancedSettings8.get_SmoothScroll
- IMsRdpClientAdvancedSettings8.put_SmoothScroll
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 62be8fe85415792116c23b4e12d9ab56fb89e0f4
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "106989163"
---
# <a name="imsrdpclientadvancedsettingssmoothscroll-property"></a><span data-ttu-id="b0346-121">IMsRdpClientAdvancedSettings：： SmoothScroll 屬性</span><span class="sxs-lookup"><span data-stu-id="b0346-121">IMsRdpClientAdvancedSettings::SmoothScroll property</span></span>

<span data-ttu-id="b0346-122">不支援這個屬性。</span><span class="sxs-lookup"><span data-stu-id="b0346-122">This property is not supported.</span></span>

<span data-ttu-id="b0346-123">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="b0346-123">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="b0346-124">Syntax</span><span class="sxs-lookup"><span data-stu-id="b0346-124">Syntax</span></span>


```C++
HRESULT put_SmoothScroll(
  [in]  LONG smoothScroll
);

HRESULT get_SmoothScroll(
  [out] LONG *psmoothScroll
);
```



## <a name="property-value"></a><span data-ttu-id="b0346-125">屬性值</span><span class="sxs-lookup"><span data-stu-id="b0346-125">Property value</span></span>

<span data-ttu-id="b0346-126">將此參數設定為0可停用平滑滾動或非零值，以啟用平滑滾動。</span><span class="sxs-lookup"><span data-stu-id="b0346-126">Set this parameter to 0 to disable smooth scrolling or a nonzero value to enable smooth scrolling.</span></span>

## <a name="error-codes"></a><span data-ttu-id="b0346-127">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="b0346-127">Error codes</span></span>

<span data-ttu-id="b0346-128">傳回 **\_ FALSE**。</span><span class="sxs-lookup"><span data-stu-id="b0346-128">Returns **S\_FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="b0346-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="b0346-129">Requirements</span></span>



| <span data-ttu-id="b0346-130">需求</span><span class="sxs-lookup"><span data-stu-id="b0346-130">Requirement</span></span> | <span data-ttu-id="b0346-131">值</span><span class="sxs-lookup"><span data-stu-id="b0346-131">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b0346-132">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b0346-132">Minimum supported client</span></span><br/> | <span data-ttu-id="b0346-133">都不支援</span><span class="sxs-lookup"><span data-stu-id="b0346-133">None supported</span></span><br/>                                                                       |
| <span data-ttu-id="b0346-134">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b0346-134">Minimum supported server</span></span><br/> | <span data-ttu-id="b0346-135">都不支援</span><span class="sxs-lookup"><span data-stu-id="b0346-135">None supported</span></span><br/>                                                                       |
| <span data-ttu-id="b0346-136">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="b0346-136">End of client support</span></span><br/>    | <span data-ttu-id="b0346-137">都不支援</span><span class="sxs-lookup"><span data-stu-id="b0346-137">None supported</span></span><br/>                                                                       |
| <span data-ttu-id="b0346-138">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="b0346-138">Type library</span></span><br/>             | <dl> <span data-ttu-id="b0346-139"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b0346-139"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="b0346-140">DLL</span><span class="sxs-lookup"><span data-stu-id="b0346-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b0346-141"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b0346-141"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="b0346-142">IID</span><span class="sxs-lookup"><span data-stu-id="b0346-142">IID</span></span><br/>                      | <span data-ttu-id="b0346-143">IID \_ IMsRdpClientAdvancedSettings 定義為3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span><span class="sxs-lookup"><span data-stu-id="b0346-143">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b0346-144">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b0346-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b0346-145">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="b0346-145">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="b0346-146">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="b0346-146">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="b0346-147">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="b0346-147">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="b0346-148">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="b0346-148">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="b0346-149">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="b0346-149">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="b0346-150">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="b0346-150">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="b0346-151">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="b0346-151">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="b0346-152">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="b0346-152">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





